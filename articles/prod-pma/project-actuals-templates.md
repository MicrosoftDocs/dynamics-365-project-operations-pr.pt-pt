---
title: Sincronizar valores reais do projeto diretamente a partir do Project Service Automation para o diário de integração do projeto para lançamento no Finance and Operations
description: Este tópico descreve os modelos e as tarefas subjacentes que são utilizados para sincronizar os valores reais do projeto diretamente do Microsoft Dynamics 365 Project Service Automation para o Finance and Operations.
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: cff62e739e88dc45e7c3d1ea044875f0600f2bc1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082536"
---
# <a name="synchronize-project-actuals-directly-from-project-service-automation-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>Sincronizar valores reais do projeto diretamente a partir do Project Service Automation para o diário de integração do projeto para lançamento no Finance and Operations

[!include[banner](../includes/banner.md)]

Este tópico descreve os modelos e as tarefas subjacentes que são utilizados para sincronizar os valores reais do projeto diretamente do Dynamics 365 Project Service Automation para o Dynamics 365 Finance.

O modelo sincroniza as transações do Project Service Automation para uma tabela de transição no Finance. Após a conclusão da sincronização, **tem de** importar os dados da tabela de transição para o diário de integração.

> [!NOTE]
> - A integração dos valores reais do projeto está disponível a partir da versão 8.0.1.
> - Se estiver a utilizar a Enterprise edition 7.3.0 depois de instalar o KB 4132657 e o KB 4132660, poderá utilizar os modelos para integrar tarefas de projeto, categorias de transações de despesas, estimativas de horas, estimativas de despesas e valores reais, e para configurar o bloqueio de funcionalidades. Se tiver de repor as distribuições contabilísticas, recomendamos que também instale o KB 4131710.
> - Se estiver a utilizar a versão 7.3.0 e estiver a transferir transações de tarifas a partir do Project Service Automation, terá de instalar o KB 4345320 para incluir essas tarifas na fatura do projeto.
> - Se estiver a introduzir os valores do imposto sobre vendas a tempo ou as transações de despesas no Project Service Automation, tem de instalar o Project Service Automation Update 7. Caso contrário, os valores reais de impostos não serão ligados aos dados reais de despesas ou tempo associados, e não serão sincronizados com o Finance. Para mais informações, contacte o Suporte.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Fluxo de dados para o Project Service Automation para o Finance

A solução de integração do Project Service Automation para Finance utiliza a funcionalidade Integração de Dados para sincronizar os dados entre instâncias do Project Service Automation e do Finance. Os modelos de integração que estão disponíveis com a funcionalidade Integração de dados permitem o fluxo de dados sobre os valores reais do projeto entre o Project Service Automation e o Finance.

A seguinte ilustração mostra como os dados são sincronizados entre o Project Service Automation e o Finance.

[![Fluxo de dados para a integração do Project Service Automation com o Finance and Operations](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)

## <a name="project-actuals-from-project-service-automation"></a>Valores reais do projeto a partir do Project Service Automation

### <a name="template-and-tasks"></a>Modelo e tarefas

Para aceder aos modelos disponíveis, no centro de administração do Microsoft Power Apps, selecione **Projetos** e, em seguida, no canto superior direito, selecione **Novo projeto** para selecionar modelos públicos.

O modelo seguinte e as tarefas subjacentes são utilizados para sincronizar os valores reais do projeto do Project Service Automation para o Finance:

- **Nome do modelo na Integração de dados:** Valores reais do projeto (PSA para Fin and Ops)
- **Nome das tarefas no projeto:**

    - Valores Reais
    - TransactionConnections

### <a name="entity-set"></a>Conjunto de entidades

| Project Service Automation | Finanças                                   |
|----------------------------|----------------------------------------------------------|
| Valores Reais                    | Entidade de integração para os valores reais do projeto                   |
| Ligações da Transação    | Entidade de integração para as relações de transações do projeto |

### <a name="entity-flow"></a>Fluxo de entidades

Os valores reais do projeto são geridos no Project Service Automation e sincronizados com o diário de integração do projeto no Finance. A contabilidade será aplicada baseada nas dimensões financeiras predefinidas e na configuração do lançamento.

### <a name="prerequisites"></a>Pré-requisitos

Antes de poder ocorrer a sincronização dos valores reais, tem de configurar os parâmetros de integração do Project Service Automation e sincronizar os projetos, tarefas do projeto e categorias de transação de despesas do projeto.

### <a name="power-query"></a>Power Query

No modelo de valores reais do projeto, tem de utilizar o Microsoft Power Query para o Excel para concluir estas tarefas:

- Transforme o tipo de transação no Project Service Automation para o tipo de transação correto no Finance. Esta transformação já está definida no modelo Dados reais do projeto (PSA para Fin and Ops).
- Transforme o tipo de faturação no Project Service Automation para o tipo de faturação correto no Finance. Esta transformação já está definida no modelo Dados reais do projeto (PSA para Fin and Ops). O tipo de faturação é então mapeado para a propriedade da linha, baseado na configuração na página **Parâmetros de integração do Project Service Automation**.
- Filtre por unidades organizacionais específicas que têm de ser sincronizadas com este modelo.
- Se o tempo entre empresas ou os valores reais da despesa entre empresas forem sincronizados com o Finance, tem de transformar a unidade organizacional contratual com a entidade jurídica correta no Finance. No modelo Valores reais do projeto (PSA para Fin and Ops), é definida uma coluna condicional com base nos dados de demonstração. Tem de atualizar a última coluna condicional inserida para as entidades jurídicas corretas. Caso contrário, pode ocorrer um erro de integração ou podem ser importadas transações de valores reais incorretas para o Finance.
- Se o tempo entre empresas ou os valores reais de despesa entre empresas não forem sincronizados com o Finance, tem de eliminar a última coluna condicional inserida do seu modelo. Caso contrário, pode ocorrer um erro de integração ou podem ser importadas transações de valores reais incorretas para o Finance.

#### <a name="contract-organizational-unit"></a>Unidade organizacional do contrato
Para atualizar a coluna condicional inserida no modelo, clique na seta **Mapear** para abrir o mapeamento. Selecione a ligação **Consulta e Filtragem Avançadas** para abrir o Power Query.

- Se estiver a utilizar o modelo Valores reais do projeto (PSA para Fin and Ops) predefinido, no Power Query, selecione a última **Condição Inserida** a partir da secção **Passos Aplicados**. Na entrada **Função** , substitua **USSI** pelo nome da entidade jurídica que deve ser utilizada com a integração. Adicione condições adicionais à entrada **Função** conforme for necessário e atualize a condição **else** a partir de **USMF** para a entidade jurídica correta.
- Se estiver a criar um novo modelo, tem de adicionar a coluna para suportar o tempo e as despesas entre empresas. Selecione **Adicionar Coluna Condicional** e introduza um nome para a coluna, como **EntidadeJurídica**. Introduza uma condição para a coluna, onde, se **msdyn\_contractorganizationalunitid.msdyn\_name** é \<organizational unit\>, em seguida \<enter the legal entity\>; ou então nulo.

### <a name="template-mapping-in-data-integration"></a>Mapeamento de modelos na Integração de dados

As seguintes ilustrações mostram um exemplo do mapeamento de tarefas do modelo na Integração de Dados. O mapeamento mostra as informações do campo que serão sincronizadas do Project Service Automation para Finance.

[![Mapeamento de modelos – Valores reais](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![Mapeamento de modelos – Ligações de transação](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table-after-integration-from-project-service-automation"></a>Importar a partir da tabela de transição após a integração do Project Service Automation

O processo periódico Importar da tabela de transição tem de ser executado após a sincronização dos valores reais do Project Service Automation para o Finance. Este processo importará as transações do projeto da tabela de transição para o diário de integração do Project Service Automation, onde a contabilidade é aplicada e as transações importadas podem ser lançadas. Recomendamos que execute este processo em modo de lote; pode ser configurado opcionalmente para ser executado como um lote recorrente.

## <a name="update-actuals-from-finance"></a>Atualizar valores reais a partir do Finance

### <a name="template-and-tasks"></a>Modelo e tarefas

O modelo seguinte e as tarefas subjacentes são utilizados para sincronizar o número de voucher e os impostos sobre as vendas para as transações do projeto lançadas a partir do Finance para o Project Service Automation:

- **Nome do modelo na Integração de dados:** Atualização dos valores reais do projeto (Fin Ops para PSA)
- **Nome das tarefas no projeto:**

    - Valores Reais 
    - TransactionConnections

### <a name="entity-set"></a>Conjunto de entidades

| Finanças                                                  | Project Service Automation |
|----------------------------------------------------------|----------------------------|
| Entidade de integração para os valores reais do projeto                   | Valores Reais                    |
| Entidade de integração para as relações de transações do projeto | Ligações da Transação    |

### <a name="entity-flow"></a>Fluxo de entidades

Os valores reais do projeto são geridos no Project Service Automation e sincronizados com o diário de integração do projeto no Finance. Depois de lançados os valores reais no Finance, são atualizados no Project Service Automation com o número de voucher do Finance. Se tiverem sido adicionados impostos sobre as vendas no Finance, são criados novos valores reais de impostos no Project Service Automation.

### <a name="power-query"></a>Power Query

No modelo de atualização dos valores reais do projeto, tem de utilizar o Power Query para concluir estas tarefas:

- Transforme o tipo de transação no Finance para o tipo de transação correto no Project Service Automation. Esta transformação já está definida no modelo Atualização de dados reais do projeto (Fin Ops para PSA).
- Transforme o tipo de faturação no Finance para o tipo de faturação correto no Project Service Automation. Esta transformação já está definida no modelo Atualização de dados reais do projeto (Fin Ops para PSA).

### <a name="template-mapping-in-data-integration"></a>Mapeamento de modelos na Integração de dados

As seguintes ilustrações mostram exemplos dos mapeamentos de tarefas do modelo na Integração de Dados. O mapeamento mostra as informações do campo que serão sincronizadas entre o Finance e o Project Service Automation.

[![Mapeamento de modelos – Atualização de valores reais](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![Mapeamento de modelos – Atualização de transação](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)
