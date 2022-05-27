---
title: Migrar marcos de faturação totalmente faturados em transição
description: Este tópico explica como migrar marcos de faturação de preços fixos faturados que tenham sido faturados ao cliente para contratos de projeto abertos antes da data de lançamento.
author: sigitac
ms.date: 01/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: ccdba864a68521024b2c479c12cf5cea616c5bbf
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8576284"
---
# <a name="migrate-fully-invoiced-billing-milestones-at-cutover"></a>Migrar marcos de faturação totalmente faturados em transição

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

## <a name="scenario"></a>Cenário

A Contoso lança o Microsoft Dynamics 365 Project Operations para cenários de recursos/sem stock. Como parte das atividades de transição, a equipa de implementação tem de migrar contratos de projeto abertos a partir do antigo sistema. Alguns dos contratos do projeto incluem itens de contratos que utilizam o método de faturação de preço fixo e que já foram parcialmente faturados ao cliente final. A equipa de implementação tem de migrar estes marcos de faturação como **Fatura do cliente publicada**, porque devem estar incluídos no valor total do contrato para efeitos de reconhecimento de receitas. No entanto, os saldos dos clientes nas Contas a receber e na Razão geral não devem ser afetados.

## <a name="solution"></a>Solução

### <a name="prerequisites"></a>Pré-requisitos

- Tem de ser instalado o Dynamics 365 Finance 10.0.24 ou posterior.
- O ambiente onde os passos de migração serão concluídos tem de estar em modo de manutenção. Não devem ser executadas outras atividades enquanto os marcos estão a ser migrados.
- Os passos de migração têm de ser seguidos exatamente como descritos aqui e só podem ser utilizados para a atividade de transição. A Microsoft não suporta outra utilização desta capacidade.

### <a name="create-a-cutover-version-of-the-project-operations-integration-contract-line-milestones-dual-write-map"></a>Criar uma versão de transição do mapa de escrita dupla dos marcos de item de contrato de integração do Project Operations 

1. Certifique-se de que o mapeamento de destino para a entidade **Marcos de item de contrato de integração do Project Operations** está atualizado. 

    1. Em Finanças, aceda a **Gestão de dados** \> **Entidades de dados** e selecione a entidade **Marcos de item de contrato da integração do Project Operations**. 
    2. Selecione **Modificar mapeamentos de destino**. 
    3. Na página **Mapear teste para o destino**, selecione **Gerar mapeamento** e, em seguida, confirme que pretende gerar o mapeamento.

2. Pare e atualize o mapa de escrita dupla **Marcos de item de contrato de integração do Project Operations** (**msdyn\_contractlinescheduleofvalues**). 

    1. Aceda a **Gestão de Dados** \> **Escrita dupla**, selecione o mapa e abra os seus detalhes. 
    2. Selecione **Parar** e aguarde até que o sistema pare o mapa. 
    3. Selecione **Atualizar tabelas**.

3. Adicione um mapeamento para o estado da transação.

    1. Selecione **Adicionar mapeamento**.
    2. Na nova linha, na coluna **Aplicações de Finanças e Operações**, selecione o campo **TRANSSTATUS \[TRANSSTATUS\]**.
    3. Na coluna **Microsoft Dataverse**, selecione o **msdyn\_invoicestatus \[Invoice status\]**.
    4. Na coluna **Mapear tipo**, selecione a seta para a direita (**\>**).
    5. Na caixa de diálogo que aparece, no campo **Direção de sincronização**, selecione **Dataverse para aplicações de Finanças e Operações**.
    6. Selecione **Adicionar transformar**.
    7. No campo **Transformar tipo**, selecione **ValueMap**.
    8. Selecione **Adicionar mapeamento de valores**.
    9. No campo à esquerda, introduza **4**. No campo à direita, introduza **192350001**. 
    10. Selecione **Guardar** e, em seguida, feche a caixa de diálogo.

4. Selecione **Guardar como** para guardar a versão do mapa de escrita dupla. 
5. No painel **Adicionar tabela**, no campo **Editor**, selecione **Editor predefinido**.
6. No campo **Versão**, introduza a versão.
7. No campo **Descrição**, introduza uma nota sobre esta versão de transição do mapa. 
8. Selecione **Guardar**.
9. Inicie o mapa.

### <a name="migrate-invoiced-milestones-to-the-dataverse-environment"></a>Migrar marcos faturados para o ambiente Dataverse

1. No ambiente Project Operations do Dataverse, crie marcos que tenham o estado de fatura de **Pronto para faturação**. Neste momento, não migre marcos que não foram faturados.

    > [!NOTE]
    > Antes de migrar os marcos de faturação, certifique-se de que as dimensões financeiras relacionadas com o item de contrato do projeto estão definidas conforme esperado. Não é possível editar dimensões financeiras depois de concluída a migração.

2. Depois de todos os marcos migrados, pare os seguintes mapas de escrita dupla:

    - Marcos do item de contrato da integração do Project Operations (msdyn\_contractlinescheduleofvalues)
    - Valores reais de integração com o Project Operations (msdyn\_actuals)
    - Proposta de fatura do projeto V2 (faturas)

    Para parar os mapas, siga estes passos:

    1. Em finanças, aceda a **Gestão de Dados** \> **Escrita dupla**, selecione um mapa e abra os seus detalhes.
    2. Selecione **Parar** e aguarde até que o sistema pare o mapa.

3. No ambiente Project Operations do Dataverse, crie e confirme as faturas pro-forma para os marcos de faturação. 

    1. No mapa do site, aceda aos contratos do projeto, selecione os contratos e, em seguida, selecione **Criar faturas**.
    2. Depois de as faturas ser criadas, abra-as a partir do menu **Faturas** no mapa do site e, em seguida, selecione **Confirmar**.

    Este passo cria os dados necessários no ambiente Dataverse. No entanto, não afeta as finanças e as contas a receber, porque os mapas de escrita dupla listados anteriormente foram parados.

4. Depois de todas as faturas pro-forma serem confirmadas, devolva todos os mapas de escrita dual ao estado inicial.

    1. Atualize a versão do mapa de escrita dupla dos **Marcos de item de contrato de integração do Project Operations** (**msdyn\_contractlinescheduleofvalues**) para o original. 
    2. Selecione o mapa de escrita dupla na lista de mapas, selecione **Versão do mapa de tabela** e, em seguida, selecione a versão original do mapa de tabela.
    3. Selecione **Guardar**.
    4. Reinicie os seguintes mapas de escrita dupla:

        - Marcos do item de contrato da integração do Project Operations (msdyn\_contractlinescheduleofvalues)
        - Valores reais de integração com o Project Operations (msdyn\_actuals)
        - Proposta de fatura do projeto V2 (faturas)

Os marcos foram migrados e o sistema está pronto para os passos seguintes na atividade de transição.
