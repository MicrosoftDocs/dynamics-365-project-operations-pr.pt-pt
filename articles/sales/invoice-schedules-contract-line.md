---
title: Criar uma agenda de faturação num item de contrato baseado em projeto
description: Este tópico fornece informações sobre como criar marcos e agendas de faturação em itens de contrato.
author: rumant
manager: Annbe
ms.date: 10/17/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 674f4ccced3d0e3178799f60d9f95a2ec27cd153
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180791"
---
# <a name="create-an-invoice-schedule-on-a-project-based-contract-line"></a>Criar uma agenda de faturação num item de contrato baseado em projeto 

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

Pode criar uma agenda de faturação para um item de contrato baseado em projeto. A faturação só é permitida depois do contrato ser ganho e estar a criar um contrato de projeto. Uma agenda de faturação permite a elaboração automática de faturas de rascunho para um item de contrato baseado em projetos. No entanto, se só cria faturas manualmente, pode ignorar a criação de agendas de faturação em itens de contrato.

## <a name="create-a-time-and-material-invoice-schedule-for-a-contract-line"></a>Criar uma agenda de faturação de tempo e material para um item de contrato

Quando um item de contrato baseado em projetos tiver um método de faturação de tempo e material, pode criar uma agenda de faturação baseada na data. Para gerar automaticamente uma agenda de faturação baseada na data, conclua os seguintes passos.

1. Vá para **Definições** > **Frequências de faturação** e configure uma frequência de faturação.
2. Aceda ao registo do contrato do projeto e, no separador **Resumo**, no campo **Data de Entrega Solicitada**, selecione uma data.
3. Abra o item de contrato **Tempo e Material** para a qual está a criar a agenda de faturação baseada na data. 
4. No separador **Agenda de Faturação**, selecione a data de início da faturação e a frequência da faturação.
5. Na subgrelha, selecione **Gerar Agenda de Faturação**. A agenda de faturação é gerada com os campos **Data de Execução da Fatura**, **Data Limite da Transação** e **Estado da Execução** da seguinte forma:

    - **Data de Execução da Fatura**: esta data é ditada pela frequência de faturação.
    - **Data Limite da Transação**: o dia anterior à data de execução da fatura.
    - **Estado da Execução**: definido automaticamente como **Não Executar**. Quando a tarefa de criação automática de faturas é executada para uma determinada data de execução da faturação, este campo é atualizado para **Execução com Êxito** ou **Falha na Execução**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-contract-line"></a>Criar uma agenda de faturação de preço fixo para um item de contrato

Quando o item de contrato tem um método de faturação fixo, pode criar uma agenda de faturação baseada em marcos. 

> [!NOTE]
> Os marcos não podem ser criados num item de contrato se não houver nenhum projeto mapeado para o item de contrato.

Conclua os seguintes passos para gerar uma agenda de faturação baseada em marco para um conjunto fixo de marcos distribuídos igualmente para o período de calendário.

1. Vá para **Definições** > **Frequências de faturação** e configure uma frequência de faturação.
2. Aceda ao registo do contrato do projeto e, no separador **Resumo**, no campo **Data de Entrega Solicitada**, selecione uma data.
3. Abra o item de contrato **Preço Fixo** para a qual está a criar uma agenda de marcos. No separador **Marcos de Faturação**, selecione a data de início da faturação e a frequência da faturação. 
4. Na subgrelha, selecione **Gerar Marcos Periódicos**. A agenda de faturação é gerada com os campos **Nome do Marco**, **Data do Marco** e **Montante do Marco** definidos da seguinte forma:

    - **Nome do Marco**: esta data é ditada pela frequência de faturação.
    - **Data do Marco**: esta data é ditada pela frequência de faturação.
    - **Montante do Marco**: este montante é calculado ao dividir o montante do contrato no item de contrato pelo número de marcos, conforme ditados pela frequência, pelo início de faturação e as datas de entrega pretendidas.

    Se o item de contrato tem um valor no campo **Montante do Imposto Estimado**, este campo também é repartido para cada marco igualmente ao gerar marcos periódicos.

Os marcos da faturação devem ser iguais ao valor contratado do item de contrato. Caso não o façam, receberá um erro na página **Item de Contrato**. Pode corrigir o erro verificando se os marcos de faturação totalizam o valor contratado da linha, criando, editando ou eliminando marcos. Depois de efetuar as alterações, atualize a página para remover o erro.

### <a name="manually-create-milestones"></a>Criar marcos manualmente

Pode gerar manualmente marcos de preço fixo quando não são divididos periodicamente. Conclua os seguintes passos para criar manualmente um marco.

1. Abra o item de contrato de preço fixo para o qual está a criar um marco e, no separador **Agenda de Faturação**, na subgrelha, selecione **+ Criar novo marco de Item de contrato**. 
2. Na página **Criação de Marco**, insira as informações necessárias com base na tabela seguinte.

| Campo | Localização | Descrição | Impacto a jusante |
| --- | --- | --- | --- |
| Nome do Marco | Criação Rápida | Campo de texto para o nome do marco. | Isto é transportado para o marco do item de contrato do projeto e para a fatura. |
| Tarefa de Projeto | Criação Rápida | Se o marco estiver associado à tarefa do projeto, utilize esta referência para adicionar lógica personalizada para definir o estado do marco baseado no estado da tarefa. | A aplicação não tem qualquer impacto a jusante desta referência a uma tarefa. |
| Data do Marco | Criação Rápida | Defina a data em que o processo automático de criação de faturas deve procurar o estado deste marco para considerá-lo para faturação. | Isto é transportado para o marco do item de contrato do projeto e para a fatura. |
| Estado da Fatura | Criação Rápida | Quando um marco é criado, este estado está sempre definido como **Não Pronto para Faturação** ou **Não Começado**. | Isto é transportado para o marco do item de contrato do projeto e para a fatura. |
| Montante de Linha | Criação Rápida | Montante ou valor do marco que será faturado ao cliente. | Isto é transportado para o marco do item de contrato do projeto e para a fatura. |
| Imposto | Criação Rápida | O valor do imposto aplicado ao marco. | Isto é transportado para o marco do item de contrato do projeto e para a fatura. |

3. Selecione **Guardar e Fechar**.
