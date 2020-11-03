---
title: Sincronizar estimativas do projetos diretamente do Project Service Automation para o Finance and Operations
description: Este tópico descreve os modelos e as tarefas subjacentes que são utilizados para sincronizar as estimativas de horas do projeto e as estimativas de despesas do projeto diretamente do Microsoft Dynamics 365 Project Service Automation para o Dynamics 365 Finance.
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 336de474c859d30d1ec07ae34bf0c3d578faeef1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082532"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="942b4-103">Sincronizar estimativas do projetos diretamente do Project Service Automation para o Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="942b4-103">Synchronize project estimates directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="942b4-104">Este tópico descreve os modelos e as tarefas subjacentes que são utilizados para sincronizar as estimativas de horas do projeto e as estimativas de despesas do projeto diretamente do Dynamics 365 Project Service Automation para o Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="942b4-104">This topic describes the templates and underlying tasks that are used to synchronize project hour estimates and project expense estimates directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="942b4-105">A integração de tarefas do projeto, as categorias de transações de despesas, as estimativas de horas, as estimativas de despesas e o bloqueio de funcionalidades estão disponíveis na versão 8.0.</span><span class="sxs-lookup"><span data-stu-id="942b4-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in version 8.0.</span></span>
> - <span data-ttu-id="942b4-106">A integração dos valores reais está disponível na versão 8.0.1 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="942b4-106">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="942b4-107">Fluxo de dados para o Project Service Automation para o Finance</span><span class="sxs-lookup"><span data-stu-id="942b4-107">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="942b4-108">A solução de integração do Project Service Automation para Finance utiliza a funcionalidade Integração de Dados para sincronizar os dados entre instâncias do Project Service Automation e do Finance.</span><span class="sxs-lookup"><span data-stu-id="942b4-108">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="942b4-109">Os modelos de integração que estão disponíveis com a funcionalidade Integração de dados permitem o fluxo de dados sobre as estimativas de horas do projeto e as estimativas de despesas do projeto do Project Service Automation para o Finance.</span><span class="sxs-lookup"><span data-stu-id="942b4-109">The integration templates that are available with the Data integration feature enable the flow of data about project hour estimates and project expense estimates from Project Service Automation to Finance.</span></span>

<span data-ttu-id="942b4-110">A seguinte ilustração mostra como os dados são sincronizados entre o Project Service Automation e o Finance.</span><span class="sxs-lookup"><span data-stu-id="942b4-110">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="942b4-111">[![Fluxo de dados para a integração do Project Service Automation com o Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="942b4-111">[![Data flow for Project Service Automation integration with Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span></span>

## <a name="project-hour-estimates"></a><span data-ttu-id="942b4-112">Estimativas de horas do projeto</span><span class="sxs-lookup"><span data-stu-id="942b4-112">Project hour estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="942b4-113">Modelo e tarefas</span><span class="sxs-lookup"><span data-stu-id="942b4-113">Template and tasks</span></span>

<span data-ttu-id="942b4-114">Para aceder aos modelos disponíveis, no centro de administração do Microsoft Power Apps, selecione **Projetos** e, em seguida, no canto superior direito, selecione **Novo projeto** para selecionar modelos públicos.</span><span class="sxs-lookup"><span data-stu-id="942b4-114">To access the available templates, in the Microsoft Power Apps admin center, select **Projects** , and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="942b4-115">O modelo seguinte e as tarefas subjacentes são utilizados para sincronizar as estimativas de horas do projeto do Project Service Automation para o Finance:</span><span class="sxs-lookup"><span data-stu-id="942b4-115">The following template and underlying tasks are used to synchronize project hour estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="942b4-116">**Nome do modelo na Integração de dados:** estimativas de horas do projeto (PSA para Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="942b4-116">**Name of the template in Data integration:** Project hour estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="942b4-117">**Nome das tarefas no projeto:**</span><span class="sxs-lookup"><span data-stu-id="942b4-117">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="942b4-118">Relações de transação</span><span class="sxs-lookup"><span data-stu-id="942b4-118">Transaction relationships</span></span>
    - <span data-ttu-id="942b4-119">Estimativas de despesas</span><span class="sxs-lookup"><span data-stu-id="942b4-119">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="942b4-120">Conjunto de entidades</span><span class="sxs-lookup"><span data-stu-id="942b4-120">Entity set</span></span>

| <span data-ttu-id="942b4-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="942b4-121">Project Service Automation</span></span> | <span data-ttu-id="942b4-122">Finanças</span><span class="sxs-lookup"><span data-stu-id="942b4-122">Finance</span></span>                                       |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="942b4-123">Tarefas do projeto</span><span class="sxs-lookup"><span data-stu-id="942b4-123">Project tasks</span></span>              | <span data-ttu-id="942b4-124">Entidade de integração para estimativas de horas do projeto</span><span class="sxs-lookup"><span data-stu-id="942b4-124">Integration entity for project hour estimates</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="942b4-125">Fluxo de entidades</span><span class="sxs-lookup"><span data-stu-id="942b4-125">Entity flow</span></span>

<span data-ttu-id="942b4-126">As estimativas de horas do projeto são geridas no Project Service Automation e sincronizadas com o Finance como previsões de horas do projeto.</span><span class="sxs-lookup"><span data-stu-id="942b4-126">Project hour estimates are managed in Project Service Automation, and they are synchronized to Finance as project hour forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="942b4-127">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="942b4-127">Prerequisites</span></span>

<span data-ttu-id="942b4-128">Antes de poder ocorrer a sincronização das estimativas de horas do projeto, tem de sincronizar os projetos, tarefas de projeto e categorias de transações de despesas de projeto.</span><span class="sxs-lookup"><span data-stu-id="942b4-128">Before synchronization of project hour estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="942b4-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="942b4-129">Power Query</span></span>

<span data-ttu-id="942b4-130">No modelo de estimativas de horas do projeto, tem de utilizar o Microsoft Power Query para o Excel para concluir estas tarefas:</span><span class="sxs-lookup"><span data-stu-id="942b4-130">In the project hour estimates template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="942b4-131">Estabeleça o modelo de previsão predefinido que será utilizado quando a integração criar novas previsões de horas.</span><span class="sxs-lookup"><span data-stu-id="942b4-131">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="942b4-132">Filtrar quaisquer registos específicos de recursos na tarefa que falhem na integração em previsões de horas.</span><span class="sxs-lookup"><span data-stu-id="942b4-132">Filter out any resource-specific records in the task that will fail the integration into hour forecasts.</span></span>
- <span data-ttu-id="942b4-133">Filtrar quaisquer linhas de categoria de transações vazias.</span><span class="sxs-lookup"><span data-stu-id="942b4-133">Filter out any empty transaction category rows.</span></span> <span data-ttu-id="942b4-134">A não execução desta tarefa poderá resultar em previsões de horas incorretas.</span><span class="sxs-lookup"><span data-stu-id="942b4-134">Failure to complete this task might result in incorrect hour forecasts.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="942b4-135">Estabelecer o ID do modelo de previsão predefinido</span><span class="sxs-lookup"><span data-stu-id="942b4-135">Set the default forecast model ID</span></span>

<span data-ttu-id="942b4-136">Para atualizar o ID de modelo de previsão predefinido no modelo, clique na seta **Mapear** para abrir o mapeamento.</span><span class="sxs-lookup"><span data-stu-id="942b4-136">To update the default forecast model ID in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="942b4-137">Em seguida, selecione a ligação **Consulta e Filtragem Avançadas**.</span><span class="sxs-lookup"><span data-stu-id="942b4-137">Then select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="942b4-138">Se estiver a utilizar o modelo Estimativas de horas do projeto (PSA para Fin and Ops) predefinido, selecione a **Condição Inserida** na lista de **Passos Aplicados**.</span><span class="sxs-lookup"><span data-stu-id="942b4-138">If you're using the default Project hour estimates (PSA to Fin and Ops) template, select the **Inserted Condition** in the list of **Applied Steps**.</span></span> <span data-ttu-id="942b4-139">Na entrada **Função** , substitua **O\_forecast** pelo nome do ID de modelo de previsão que deve ser utilizado com a integração.</span><span class="sxs-lookup"><span data-stu-id="942b4-139">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="942b4-140">O modelo predefinido tem um ID de modelo de previsão dos dados de demonstração.</span><span class="sxs-lookup"><span data-stu-id="942b4-140">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="942b4-141">Se estiver a criar um novo modelo, tem de adicionar esta coluna.</span><span class="sxs-lookup"><span data-stu-id="942b4-141">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="942b4-142">No Power Query, selecione **Adicionar Coluna Condicional** e introduza um nome para a nova coluna, como **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="942b4-142">In Power Query, select **Add Conditional Column** , and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="942b4-143">Introduza a condição para a coluna, onde, se a tarefa do Projeto for não nula, então \<enter the forecast model ID\>; ou então nulo.</span><span class="sxs-lookup"><span data-stu-id="942b4-143">Enter the condition for the column, where, if Project task is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="filter-out-resource-specific-records"></a><span data-ttu-id="942b4-144">Filtrar os registos específicos de recursos</span><span class="sxs-lookup"><span data-stu-id="942b4-144">Filter out resource-specific records</span></span>

<span data-ttu-id="942b4-145">O modelo Estimativas de horas do projeto (PSA para Fin and Ops) tem um filtro predefinido que remove quaisquer registos específicos do recurso.</span><span class="sxs-lookup"><span data-stu-id="942b4-145">The Project hour estimates (PSA to Fin and Ops) template has a default filter that removes any resource-specific records.</span></span> <span data-ttu-id="942b4-146">Se criar o seu próprio modelo, terá de adicionar este filtro.</span><span class="sxs-lookup"><span data-stu-id="942b4-146">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="942b4-147">Selecione a ligação **Consulta e Filtragem Avançadas** para filtrar na coluna **msdyn\_islinetask** para só serem incluídos registos com **False**.</span><span class="sxs-lookup"><span data-stu-id="942b4-147">Select the **Advanced Query and Filtering** link to filter on the **msdyn\_islinetask** column so that only **False** records are included.</span></span>

#### <a name="filter-out-empty-transaction-category-rows"></a><span data-ttu-id="942b4-148">Filtrar as linhas de categoria de transações vazias</span><span class="sxs-lookup"><span data-stu-id="942b4-148">Filter out empty transaction category rows</span></span>

<span data-ttu-id="942b4-149">Tem de adicionar um filtro para remover quaisquer linhas que tenham categorias de transações vazias.</span><span class="sxs-lookup"><span data-stu-id="942b4-149">You must add a filter to remove any rows that have empty transaction categories.</span></span> <span data-ttu-id="942b4-150">Esta tarefa é obrigatória, independentemente de estar a usar o modelo predefinido ou a criar o seu próprio modelo.</span><span class="sxs-lookup"><span data-stu-id="942b4-150">This task is required, regardless of whether you're using the default template or creating your own template.</span></span> <span data-ttu-id="942b4-151">Este filtro remove quaisquer linhas de resumo do Project Service Automation que possam fazer com que as previsões de horas no Finance sejam incorretas.</span><span class="sxs-lookup"><span data-stu-id="942b4-151">This filter removes any summary rows from Project Service Automation that might cause the hour forecasts in Finance to be incorrect.</span></span> <span data-ttu-id="942b4-152">Selecione a ligação **Consulta e Filtragem Avançadas** para filtrar registos Null na coluna **msdyn\_transactioncategory\_value**.</span><span class="sxs-lookup"><span data-stu-id="942b4-152">Select **Advanced Query and Filtering** link to filter out null records in the **msdyn\_transactioncategory\_value** column.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="942b4-153">Mapeamento de modelos na Integração de dados</span><span class="sxs-lookup"><span data-stu-id="942b4-153">Template mapping in Data integration</span></span>

<span data-ttu-id="942b4-154">A seguinte ilustração mostra um exemplo do mapeamento de tarefas do modelo na Integração de Dados.</span><span class="sxs-lookup"><span data-stu-id="942b4-154">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="942b4-155">O mapeamento mostra as informações do campo que serão sincronizadas do Project Service Automation para Finance.</span><span class="sxs-lookup"><span data-stu-id="942b4-155">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="942b4-156">[![Mapeamento de tarefas de modelo na integração de dados](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="942b4-156">[![Template task mapping in data integration](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span></span>

## <a name="project-expense-estimates"></a><span data-ttu-id="942b4-157">Estimativas de despesa do projeto</span><span class="sxs-lookup"><span data-stu-id="942b4-157">Project expense estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="942b4-158">Modelo e tarefas</span><span class="sxs-lookup"><span data-stu-id="942b4-158">Template and tasks</span></span>

<span data-ttu-id="942b4-159">O modelo seguinte e as tarefas subjacentes são utilizados para sincronizar as estimativas de despesa do projeto do Project Service Automation para o Finance:</span><span class="sxs-lookup"><span data-stu-id="942b4-159">The following template and underlying tasks are used to synchronize project expense estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="942b4-160">**Nome do modelo na Integração de dados:** estimativas de despesa do projeto (PSA para Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="942b4-160">**Name of the template in Data integration:** Project expense estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="942b4-161">**Nome das tarefas no projeto:**</span><span class="sxs-lookup"><span data-stu-id="942b4-161">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="942b4-162">Relações de transação</span><span class="sxs-lookup"><span data-stu-id="942b4-162">Transaction relationships</span></span> 
    - <span data-ttu-id="942b4-163">Estimativas de despesas</span><span class="sxs-lookup"><span data-stu-id="942b4-163">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="942b4-164">Conjunto de entidades</span><span class="sxs-lookup"><span data-stu-id="942b4-164">Entity set</span></span>

| <span data-ttu-id="942b4-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="942b4-165">Project Service Automation</span></span> | <span data-ttu-id="942b4-166">Finanças</span><span class="sxs-lookup"><span data-stu-id="942b4-166">Finance</span></span>                                                  |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="942b4-167">Ligações da Transação</span><span class="sxs-lookup"><span data-stu-id="942b4-167">Transaction Connections</span></span>    | <span data-ttu-id="942b4-168">Entidade de integração para as relações de transações do projeto</span><span class="sxs-lookup"><span data-stu-id="942b4-168">Integration entity for project transaction relationships</span></span> |
| <span data-ttu-id="942b4-169">Linhas de Estimativa</span><span class="sxs-lookup"><span data-stu-id="942b4-169">Estimate Lines</span></span>             | <span data-ttu-id="942b4-170">Entidade de integração para estimativas de despesa do projeto</span><span class="sxs-lookup"><span data-stu-id="942b4-170">Integration entity for project expense estimates</span></span>         |

### <a name="entity-flow"></a><span data-ttu-id="942b4-171">Fluxo de entidades</span><span class="sxs-lookup"><span data-stu-id="942b4-171">Entity flow</span></span>

<span data-ttu-id="942b4-172">As estimativas de despesa do projeto são geridas no Project Service Automation e sincronizadas com o Finance como previsões de despesa do projeto.</span><span class="sxs-lookup"><span data-stu-id="942b4-172">Project expense estimates are managed in Project Service Automation, and they are synchronized to Finance as project expense forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="942b4-173">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="942b4-173">Prerequisites</span></span>

<span data-ttu-id="942b4-174">Antes de poder ocorrer a sincronização das estimativas de despesa do projeto, tem de sincronizar os projetos, tarefas de projeto e categorias de transações de despesas de projeto.</span><span class="sxs-lookup"><span data-stu-id="942b4-174">Before synchronization of project expense estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="942b4-175">Power Query</span><span class="sxs-lookup"><span data-stu-id="942b4-175">Power Query</span></span>

<span data-ttu-id="942b4-176">No modelo de estimativas de despesa do projeto, tem de utilizar o Power Query para concluir as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="942b4-176">In the project expense estimates template, you must use Power Query to complete the following tasks:</span></span>

- <span data-ttu-id="942b4-177">Filtrar para incluir apenas os registos de item de estimativa de despesa.</span><span class="sxs-lookup"><span data-stu-id="942b4-177">Filter to include only expense estimate line records.</span></span>
- <span data-ttu-id="942b4-178">Estabeleça o modelo de previsão predefinido que será utilizado quando a integração criar novas previsões de horas.</span><span class="sxs-lookup"><span data-stu-id="942b4-178">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="942b4-179">Transformar os tipos de faturação.</span><span class="sxs-lookup"><span data-stu-id="942b4-179">Transform the billing types.</span></span>
- <span data-ttu-id="942b4-180">Transformar os tipos de transação.</span><span class="sxs-lookup"><span data-stu-id="942b4-180">Transform the transaction types.</span></span>

#### <a name="filter-to-include-only-expense-estimate-lines"></a><span data-ttu-id="942b4-181">Filtrar para incluir apenas os itens de estimativa de despesa</span><span class="sxs-lookup"><span data-stu-id="942b4-181">Filter to include only expense estimate lines</span></span>

<span data-ttu-id="942b4-182">O modelo Estimativas de despesa do projeto (PSA para Fin and Ops) tem um filtro predefinido que inclui apenas os itens de despesa na integração.</span><span class="sxs-lookup"><span data-stu-id="942b4-182">The Project expense estimates (PSA to Fin and Ops) template has a default filter that includes only expense lines in the integration.</span></span> <span data-ttu-id="942b4-183">Se criar o seu próprio modelo, terá de adicionar este filtro.</span><span class="sxs-lookup"><span data-stu-id="942b4-183">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="942b4-184">Selecione a tarefa **Relações de transação** e, em seguida, clique na seta **Mapear** para abrir o mapeamento.</span><span class="sxs-lookup"><span data-stu-id="942b4-184">Select the **Transaction relationships** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="942b4-185">Selecione a ligação **Consulta e Filtragem Avançadas**.</span><span class="sxs-lookup"><span data-stu-id="942b4-185">Select the **Advanced Query and Filtering** link.</span></span> <span data-ttu-id="942b4-186">Filtre a coluna **msdyn\_transactiontype1** para incluir apenas **msdyn\_estimateline**.</span><span class="sxs-lookup"><span data-stu-id="942b4-186">Filter the **msdyn\_transactiontype1** column so that it includes only **msdyn\_estimateline**.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="942b4-187">Estabelecer o ID do modelo de previsão predefinido</span><span class="sxs-lookup"><span data-stu-id="942b4-187">Set the default forecast model ID</span></span>

<span data-ttu-id="942b4-188">Para atualizar o ID de modelo de previsão predefinido no modelo, selecione a tarefa **Estimativas de despesas** e clique na seta **Mapear** para abrir o mapeamento.</span><span class="sxs-lookup"><span data-stu-id="942b4-188">To update the default forecast model ID in the template, select the **Expense estimates** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="942b4-189">Selecione a ligação **Consulta e Filtragem Avançadas**.</span><span class="sxs-lookup"><span data-stu-id="942b4-189">Select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="942b4-190">Se estiver a utilizar o modelo Estimativas de despesa do projeto (PSA para Fin and Ops) predefinido, no Power Query, selecione a primeira **Condição Inserida** a partir da secção **Passos Aplicados**.</span><span class="sxs-lookup"><span data-stu-id="942b4-190">If you're using the default Project expense estimates (PSA to Fin and Ops) template, in Power Query, select the first **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="942b4-191">Na entrada **Função** , substitua **O\_forecast** pelo nome do ID de modelo de previsão que deve ser utilizado com a integração.</span><span class="sxs-lookup"><span data-stu-id="942b4-191">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="942b4-192">O modelo predefinido tem um ID de modelo de previsão dos dados de demonstração.</span><span class="sxs-lookup"><span data-stu-id="942b4-192">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="942b4-193">Se estiver a criar um novo modelo, tem de adicionar esta coluna.</span><span class="sxs-lookup"><span data-stu-id="942b4-193">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="942b4-194">No Power Query, selecione **Adicionar Coluna Condicional** e introduza um nome para a nova coluna, como **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="942b4-194">In Power Query, select **Add Conditional Column** , and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="942b4-195">Introduza a condição para a coluna, onde, se o ID da linha de Estimativa for não nula, então \<enter the forecast model ID\>; ou então nulo.</span><span class="sxs-lookup"><span data-stu-id="942b4-195">Enter the condition for the column, where, if Estimate line ID is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="transform-the-billing-types"></a><span data-ttu-id="942b4-196">Transformar os tipos de faturação</span><span class="sxs-lookup"><span data-stu-id="942b4-196">Transform the billing types</span></span>

<span data-ttu-id="942b4-197">O modelo Estimativas de despesa do projeto (PSA para Fin and Ops) inclui uma coluna condicional que é utilizada para transformar os tipos de faturação que são recebidos do Project Service Automation durante a integração.</span><span class="sxs-lookup"><span data-stu-id="942b4-197">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the billing types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="942b4-198">Se criar o seu próprio modelo, terá de adicionar esta coluna condicional.</span><span class="sxs-lookup"><span data-stu-id="942b4-198">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="942b4-199">Selecione a ligação **Consulta e Filtragem Avançadas** e, em seguida, selecione **Adicionar Coluna Condicional**.</span><span class="sxs-lookup"><span data-stu-id="942b4-199">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="942b4-200">Introduza um nome para a nova coluna, como **BillingType**.</span><span class="sxs-lookup"><span data-stu-id="942b4-200">Enter a name for the new column, such as **BillingType**.</span></span> <span data-ttu-id="942b4-201">Em seguida, introduza a seguinte condição:</span><span class="sxs-lookup"><span data-stu-id="942b4-201">Then enter the following condition:</span></span>

<span data-ttu-id="942b4-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span><span class="sxs-lookup"><span data-stu-id="942b4-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span></span>  
<span data-ttu-id="942b4-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span><span class="sxs-lookup"><span data-stu-id="942b4-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span></span>  
<span data-ttu-id="942b4-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span><span class="sxs-lookup"><span data-stu-id="942b4-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span></span>  
<span data-ttu-id="942b4-205">else **NotAvailable**</span><span class="sxs-lookup"><span data-stu-id="942b4-205">else **NotAvailable**</span></span>

#### <a name="transform-the-transaction-types"></a><span data-ttu-id="942b4-206">Transformar os tipos de transação</span><span class="sxs-lookup"><span data-stu-id="942b4-206">Transform the transaction types</span></span>

<span data-ttu-id="942b4-207">O modelo Estimativas de despesa do projeto (PSA para Fin and Ops) inclui uma coluna condicional que é utilizada para transformar os tipos de transação que são recebidos do Project Service Automation durante a integração.</span><span class="sxs-lookup"><span data-stu-id="942b4-207">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the transaction types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="942b4-208">Se criar o seu próprio modelo, terá de adicionar esta coluna condicional.</span><span class="sxs-lookup"><span data-stu-id="942b4-208">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="942b4-209">Selecione a ligação **Consulta e Filtragem Avançadas** e, em seguida, selecione **Adicionar Coluna Condicional**.</span><span class="sxs-lookup"><span data-stu-id="942b4-209">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="942b4-210">Introduza um nome para a nova coluna, como **TransactionType**.</span><span class="sxs-lookup"><span data-stu-id="942b4-210">Enter a name for the new column, such as **TransactionType**.</span></span> <span data-ttu-id="942b4-211">Em seguida, introduza a seguinte condição:</span><span class="sxs-lookup"><span data-stu-id="942b4-211">Then enter the following condition:</span></span>

<span data-ttu-id="942b4-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span><span class="sxs-lookup"><span data-stu-id="942b4-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span></span>  
<span data-ttu-id="942b4-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span><span class="sxs-lookup"><span data-stu-id="942b4-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span></span>  
<span data-ttu-id="942b4-214">else **null**</span><span class="sxs-lookup"><span data-stu-id="942b4-214">else **null**</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="942b4-215">Mapeamento de modelos na Integração de dados</span><span class="sxs-lookup"><span data-stu-id="942b4-215">Template mapping in Data integration</span></span>

<span data-ttu-id="942b4-216">As seguintes ilustrações mostram exemplos dos mapeamentos de tarefas do modelo na Integração de Dados.</span><span class="sxs-lookup"><span data-stu-id="942b4-216">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="942b4-217">O mapeamento mostra as informações do campo que serão sincronizadas do Project Service Automation para Finance.</span><span class="sxs-lookup"><span data-stu-id="942b4-217">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="942b4-218">[![Mapeamento do modelo das transações de estimativa de despesas](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="942b4-218">[![Template mapping of expense estimate transactions](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span></span>

<span data-ttu-id="942b4-219">[![Mapeamento do modelo das estimativas de despesas](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="942b4-219">[![Template mapping of expense estimates](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span></span>
