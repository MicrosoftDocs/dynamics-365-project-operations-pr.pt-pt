---
title: Sincronizar categorias de despesas do projeto entre o Finance and Operations e o Project Service Automation
description: Este tópico descreve os modelos e as tarefas subjacentes que são utilizados para sincronizar as categorias de despesa do projeto entre o Microsoft Dynamics 365 Finance e o Dynamics 365 Project Service Automation.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 2816d363dbfe6ef2d98a584b214f72d9b30c49bb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999865"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>Sincronizar categorias de despesas do projeto entre o Finance and Operations e o Project Service Automation

[!include[banner](../includes/banner.md)]

Este tópico descreve os modelos e as tarefas subjacentes que são utilizados para sincronizar as categorias de despesa do projeto entre o Dynamics 365 Finance e o Dynamics 365 Project Service Automation.

> [!NOTE]
> - A integração de tarefas do projeto, as categorias de transações de despesas, as estimativas de horas, as estimativas de despesas e o bloqueio de funcionalidades estão disponíveis na versão 8.0.
> - A integração dos valores reais está disponível na versão 8.0.1 ou posterior.
> - Se estiver a utilizar a Enterprise edition 7.3.0 depois de instalar o KB 4132657 e o KB 4132660, poderá utilizar os modelos para integrar tarefas de projeto, categorias de transações de despesas, estimativas de horas, estimativas de despesas e valores reais, e para configurar o bloqueio de funcionalidades. Se tiver de repor as distribuições contabilísticas, recomendamos que também instale o KB 4131710.

## <a name="data-flow-for-project-service-automation-and-finance"></a>Fluxo de dados para o Project Service Automation e o Finance

A solução de integração do Project Service Automation e do Finance utiliza a funcionalidade Integração de Dados para sincronizar os dados entre instâncias do Project Service Automation e do Finance. Os modelos de integração que estão disponíveis com a funcionalidade Integração de dados permitem o fluxo de dados sobre as categorias de transações de despesas do projeto entre o Finance e o Project Service Automation.

Se as categorias de despesas do projeto forem geridas no Finance, o fluxo de integração ocorre primeiro do Finance para o Project Service Automation. Os IDs de integração das categorias de despesas do projeto são então atualizados através da sincronização do Project Service Automation para o Finance.

Se as categorias de despesas do projeto forem geridas no Project Service Automation, o fluxo de integração ocorre primeiro do Project Service Automation para o Finance. As categorias de projetos já têm de estar configuradas no Finance antes da sincronização a partir do Project Service Automation. Em seguida, sincronize do Finance para o Project Service Automation e, depois, de volta do Project Service Automation para o Finance. Desta forma, ajuda a garantir que as categorias estão ligadas e que não são criadas entradas duplicadas.

> [!NOTE]
> Tipicamente, as categorias de despesas do projeto são geridas no Finance. No entanto, se não forem, ou se já tiverem sido criadas categorias de despesas no Project Service Automation, primeiro tem de sincronizar ao utilizar o modelo Categorias de transações de despesas do projeto (PSA para Fin and Ops). Em seguida, sincronize ao utilizar o modelo Categorias de transações de despesas do projeto (Fin and Ops para PSA). Em seguida, deve executar a sincronização entre o Project Service Automation e o Finance mais uma vez.
>
> Se sincronizar primeiro a partir do Project Service Automation, os seguintes requisitos terão de ser cumpridos no Finance antes de a sincronização ser executada:
>
> - A categoria partilhada que corresponde à categoria do projeto que está configurada no Project Service Automation tem de existir, e tem de estar ativada parapara o **Projeto** e as **Despesas**.
> - Para cada entidade jurídica do Finance com a qual tenha de ser feita a integração, têm de existir as seguintes categorias do projeto:
>
>     - Existe a **Categoria do projeto**. 
>     - **Utilização nas Despesas** está ativado.
>     - **Ativo no diário** está ativado.
>     - **Tipo de transação** está definido como **Despesa**.

A seguinte ilustração mostra como os dados são sincronizados entre o Project Service Automation e o Finance.

[![Fluxo de dados para a integração do Project Service Automation com o Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a>Sincronização das categorias de despesas do projeto do Finance para o Project Service Automation

### <a name="template-and-task"></a>Modelo e tarefa

Para aceder ao modelo, no centro de administração do Microsoft Power Apps, selecione **Projetos** e, em seguida, no canto superior direito, selecione **Novo projeto** para selecionar modelos públicos.

O modelo seguinte e a tarefa subjacente são utilizados para sincronizar as categorias de despesa do Finance para o Project Service Automation:

- **Nome do modelo na Integração de dados:** Categorias de transações de despesas do projeto (Fin and Ops para PSA)
- **Nome da tarefa no projeto:** sincronizar categorias para o PSA

### <a name="entity-set"></a>Conjunto de entidades

| Finanças                           | Project Service Automation |
|-----------------------------------|----------------------------|
| Entidade de integração para categorias | Categorias de transações     |

### <a name="entity-flow"></a>Fluxo de entidades

As categorias de despesas do projeto são geridas no Finance e sincronizadas com o Project Service Automation como categorias de transações.

### <a name="power-query"></a>Power Query

Quando estiver a sincronizar com o Project Service Automation, tem de utilizar o Microsoft Power Query para Excel definir o tipo de faturação na categoria de transação. O modelo Categorias de transações de despesas do projeto (Fin and Ops para PSA) fornece uma coluna e mapeamento predefinidos. Se criar o seu próprio modelo, tem de adicionar uma coluna condicional no Power Query. Siga estes passos.

1. Clique na seta para abrir o mapeamento da tarefa das categorias de despesas do projeto no modelo Categorias de transações de despesas do projeto (Fin and Ops para PSA).
2. Clique na ligação **Consulta e Filtragem Avançadas** para abrir o Power Query.
2. Selecione **Adicionar Coluna Condicional**.
3. Introduza um nome para a nova coluna, como **BillingType**.
4. Introduza a seguinte condição: **if CATEGORYID not equal to null then 19235001, Otherwise null**.
5. Clique em **OK** na coluna.
6. Certifique-se de mapeia esta nova coluna na página de mapeamento.

A seguinte ilustração mostra um exemplo do mapeamento de tarefas do modelo na Integração de Dados. O mapeamento mostra as informações do campo que serão sincronizadas entre o Finance e o Project Service Automation.

[![Categorias de despesas de projeto para o mapeamento do modelo do Project Service Automation](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a>Sincronização das categorias de despesas do projeto do Project Service Automation para o Finance

### <a name="template-and-task"></a>Modelo e tarefa

O modelo seguinte e a tarefa subjacente são utilizados para sincronizar as categorias de despesa do Project Service Automation para o Finance:

- **Nome do modelo na Integração de dados:** Categorias de transações de despesas do projeto (PSA para Fin and Ops)
- **Nome da tarefa no projeto:** sincronizar categorias para o Fin Ops

### <a name="entity-set"></a>Conjunto de entidades

| Project Service Automation | Finanças                           |
|----------------------------|-----------------------------------|
| Categorias de transações     | Entidade de integração para categorias |

### <a name="entity-flow"></a>Fluxo de entidades

As categorias de despesas do projeto são geridas no Finance e sincronizadas com o Project Service Automation como categorias de transações. A sincronização de volta para o Finance atualiza a categoria do projeto no Finance com o ID de integração a partir do Project Service Automation.

### <a name="template-mapping-in-data-integration"></a>Mapeamento de modelos na Integração de dados

A seguinte ilustração mostra um exemplo do mapeamento de tarefas do modelo na Integração de Dados.

> [!NOTE]
> O mapeamento mostra as informações do campo que serão sincronizadas do Project Service Automation para Finance.

[![Mapeamento do modelo do Project Service Automation para o Finance](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]