---
title: Sincronizar as estimativas do projeto diretamente do Project Service Automation para Finanças e Operações
description: Este artigo descreve os modelos e tarefas subjacentes que são utilizados para sincronizar estimativas de horas do projeto e estimativas de despesas do projeto diretamente do Microsoft Dynamics 365 Project Service Automation para o Dynamics 365 Finance.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: fb39a377a51b09f04564b4fe8527e34f0ea12682
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920856"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a>Sincronizar as estimativas do projeto diretamente do Project Service Automation para Finanças e Operações

[!include[banner](../includes/banner.md)]

Este artigo descreve os modelos e tarefas subjacentes que são utilizados para sincronizar estimativas de horas do projeto e estimativas de despesas do projeto diretamente do Dynamics 365 Project Service Automation para o Dynamics 365 Finance.

> [!NOTE]
> - A integração de tarefas do projeto, as categorias de transações de despesas, as estimativas de horas, as estimativas de despesas e o bloqueio de funcionalidades estão disponíveis na versão 8.0.
> - A integração dos valores reais está disponível na versão 8.0.1 ou posterior.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Fluxo de dados para o Project Service Automation para o Finance

A solução de integração do Project Service Automation para Finance utiliza a funcionalidade Integração de Dados para sincronizar os dados entre instâncias do Project Service Automation e do Finance. Os modelos de integração que estão disponíveis com a funcionalidade Integração de dados permitem o fluxo de dados sobre as estimativas de horas do projeto e as estimativas de despesas do projeto do Project Service Automation para o Finance.

A seguinte ilustração mostra como os dados são sincronizados entre o Project Service Automation e o Finance.

[![Fluxo de dados para a integração do Project Service Automation com o Finance.](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)

## <a name="project-hour-estimates"></a>Estimativas de horas do projeto

### <a name="template-and-tasks"></a>Modelo e tarefas

Para aceder aos modelos disponíveis, no centro de administração do Microsoft Power Apps, selecione **Projetos** e, em seguida, no canto superior direito, selecione **Novo projeto** para selecionar modelos públicos.

O modelo seguinte e as tarefas subjacentes são utilizados para sincronizar as estimativas de horas do projeto do Project Service Automation para o Finance:

- **Nome do modelo na Integração de dados:** estimativas de horas do projeto (PSA para Fin and Ops)
- **Nome das tarefas no projeto:**

    - Relações de transação
    - Estimativas de despesas

### <a name="entity-set"></a>Conjunto de entidades

| Project Service Automation | Finanças                                       |
|----------------------------|-----------------------------------------------|
| Tarefas do projeto              | Entidade de integração para estimativas de horas do projeto |

### <a name="entity-flow"></a>Fluxo de entidades

As estimativas de horas do projeto são geridas no Project Service Automation e sincronizadas com o Finance como previsões de horas do projeto.

### <a name="prerequisites"></a>Pré-requisitos

Antes de poder ocorrer a sincronização das estimativas de horas do projeto, tem de sincronizar os projetos, tarefas de projeto e categorias de transações de despesas de projeto.

### <a name="power-query"></a>Power Query

No modelo de estimativas de horas do projeto, tem de utilizar o Microsoft Power Query para Excel para concluir estas tarefas:

- Estabeleça o modelo de previsão predefinido que será utilizado quando a integração criar novas previsões de horas.
- Filtrar quaisquer registos específicos de recursos na tarefa que falhem na integração em previsões de horas.
- Filtrar quaisquer linhas de categoria de transações vazias. A não execução desta tarefa poderá resultar em previsões de horas incorretas.

#### <a name="set-the-default-forecast-model-id"></a>Estabelecer o ID do modelo de previsão predefinido

Para atualizar o ID de modelo de previsão predefinido no modelo, clique na seta **Mapear** para abrir o mapeamento. Em seguida, selecione a ligação **Consulta e Filtragem Avançadas**.

- Se estiver a utilizar o modelo Estimativas de horas do projeto (PSA para Fin and Ops) predefinido, selecione a **Condição Inserida** na lista de **Passos Aplicados**. Na entrada **Função**, substitua **O\_forecast** pelo nome do ID de modelo de previsão que deve ser utilizado com a integração. O modelo predefinido tem um ID de modelo de previsão dos dados de demonstração.
- Se estiver a criar um novo modelo, tem de adicionar esta coluna. Em Power Query, selecione **Adicionar coluna condicional** e, em seguida, introduza um nome para a nova coluna, como **ModelID**. Introduza a condição para a coluna, onde, se a tarefa do Projeto for não nula, então \<enter the forecast model ID\>; ou então nulo.

#### <a name="filter-out-resource-specific-records"></a>Filtrar os registos específicos de recursos

O modelo Estimativas de horas do projeto (PSA para Fin and Ops) tem um filtro predefinido que remove quaisquer registos específicos do recurso. Se criar o seu próprio modelo, terá de adicionar este filtro. Selecione a ligação **Consulta e Filtragem Avançadas** para filtrar na coluna **msdyn\_islinetask** para só serem incluídos registos com **False**.

#### <a name="filter-out-empty-transaction-category-rows"></a>Filtrar as linhas de categoria de transações vazias

Tem de adicionar um filtro para remover quaisquer linhas que tenham categorias de transações vazias. Esta tarefa é obrigatória, independentemente de estar a usar o modelo predefinido ou a criar o seu próprio modelo. Este filtro remove quaisquer linhas de resumo do Project Service Automation que possam fazer com que as previsões de horas no Finance sejam incorretas. Selecione a ligação **Consulta e Filtragem Avançadas** para filtrar registos Null na coluna **msdyn\_transactioncategory\_value**.

### <a name="template-mapping-in-data-integration"></a>Mapeamento de modelos na Integração de dados

A seguinte ilustração mostra um exemplo do mapeamento de tarefas do modelo na Integração de Dados. O mapeamento mostra as informações do campo que serão sincronizadas do Project Service Automation para Finance.

[![Mapeamento de tarefas de modelo na integração de dados.](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)

## <a name="project-expense-estimates"></a>Estimativas de despesa do projeto

### <a name="template-and-tasks"></a>Modelo e tarefas

O modelo seguinte e as tarefas subjacentes são utilizados para sincronizar as estimativas de despesa do projeto do Project Service Automation para o Finance:

- **Nome do modelo na Integração de dados:** estimativas de despesa do projeto (PSA para Fin and Ops)
- **Nome das tarefas no projeto:**

    - Relações de transação 
    - Estimativas de despesas

### <a name="entity-set"></a>Conjunto de entidades

| Project Service Automation | Finanças                                                  |
|----------------------------|----------------------------------------------------------|
| Ligações da Transação    | Entidade de integração para as relações de transações do projeto |
| Linhas de Estimativa             | Entidade de integração para estimativas de despesa do projeto         |

### <a name="entity-flow"></a>Fluxo de entidades

As estimativas de despesa do projeto são geridas no Project Service Automation e sincronizadas com o Finance como previsões de despesa do projeto.

### <a name="prerequisites"></a>Pré-requisitos

Antes de poder ocorrer a sincronização das estimativas de despesa do projeto, tem de sincronizar os projetos, tarefas de projeto e categorias de transações de despesas de projeto.

### <a name="power-query"></a>Power Query

No modelo de estimativas de despesas do projeto, tem de utilizar o Microsoft Power Query para concluir as seguintes tarefas:

- Filtrar para incluir apenas os registos de item de estimativa de despesa.
- Estabeleça o modelo de previsão predefinido que será utilizado quando a integração criar novas previsões de horas.
- Transformar os tipos de faturação.
- Transformar os tipos de transação.

#### <a name="filter-to-include-only-expense-estimate-lines"></a>Filtrar para incluir apenas os itens de estimativa de despesa

O modelo Estimativas de despesa do projeto (PSA para Fin and Ops) tem um filtro predefinido que inclui apenas os itens de despesa na integração. Se criar o seu próprio modelo, terá de adicionar este filtro. Selecione a tarefa **Relações de transação** e, em seguida, clique na seta **Mapear** para abrir o mapeamento. Selecione a ligação **Consulta e Filtragem Avançadas**. Filtre a coluna **msdyn\_transactiontype1** para incluir apenas **msdyn\_estimateline**.

#### <a name="set-the-default-forecast-model-id"></a>Estabelecer o ID do modelo de previsão predefinido

Para atualizar o ID de modelo de previsão predefinido no modelo, selecione a tarefa **Estimativas de despesas** e clique na seta **Mapear** para abrir o mapeamento. Selecione a ligação **Consulta e Filtragem Avançadas**.

- Se estiver a utilizar o modelo predefinido de estimativa de despesas do Projeto (PSA para Fin e Ops), no Power Query, selecione a primeira **Condição introduzida** da secção **Passos Aplicados**. Na entrada **Função**, substitua **O\_forecast** pelo nome do ID de modelo de previsão que deve ser utilizado com a integração. O modelo predefinido tem um ID de modelo de previsão dos dados de demonstração.
- Se estiver a criar um novo modelo, tem de adicionar esta coluna. Em Power Query, selecione **Adicionar coluna condicional** e, em seguida, introduza um nome para a nova coluna, como **ModelID**. Introduza a condição para a coluna, onde, se o ID da linha de Estimativa for não nula, então \<enter the forecast model ID\>; ou então nulo.

#### <a name="transform-the-billing-types"></a>Transformar os tipos de faturação

O modelo Estimativas de despesa do projeto (PSA para Fin and Ops) inclui uma coluna condicional que é utilizada para transformar os tipos de faturação que são recebidos do Project Service Automation durante a integração. Se criar o seu próprio modelo, terá de adicionar esta coluna condicional. Selecione a ligação **Consulta e Filtragem Avançadas** e, em seguida, selecione **Adicionar Coluna Condicional**. Introduza um nome para a nova coluna, como **BillingType**. Em seguida, introduza a seguinte condição:

If **msdyn\_billingtype** = 192350000, then **NonChargeable**  
else if **msdyn\_billingtype** = 192350001, then **Chargeable**  
else if **msdyn\_billingtype** = 192350002, then **Complimentary**  
else **NotAvailable**

#### <a name="transform-the-transaction-types"></a>Transformar os tipos de transação

O modelo Estimativas de despesa do projeto (PSA para Fin and Ops) inclui uma coluna condicional que é utilizada para transformar os tipos de transação que são recebidos do Project Service Automation durante a integração. Se criar o seu próprio modelo, terá de adicionar esta coluna condicional. Selecione a ligação **Consulta e Filtragem Avançadas** e, em seguida, selecione **Adicionar Coluna Condicional**. Introduza um nome para a nova coluna, como **TransactionType**. Em seguida, introduza a seguinte condição:

If **msdyn\_transactiontypecode** = 192350000, then **Cost**  
else if **msdyn\_transactiontypecode** = 192350005, then **Sales**  
else **null**

### <a name="template-mapping-in-data-integration"></a>Mapeamento de modelos na Integração de dados

As seguintes ilustrações mostram exemplos dos mapeamentos de tarefas do modelo na Integração de Dados. O mapeamento mostra as informações do campo que serão sincronizadas do Project Service Automation para Finance.

[![Mapeamento do modelo das transações de estimativa de despesas.](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)

[![Mapeamento do modelo das estimativas de despesas.](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]