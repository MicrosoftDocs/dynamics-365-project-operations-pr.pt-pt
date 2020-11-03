---
title: Sincronizar categorias de despesas do projeto entre o Finance and Operations e o Project Service Automation
description: Este tópico descreve os modelos e as tarefas subjacentes que são utilizados para sincronizar as categorias de despesa do projeto entre o Microsoft Dynamics 365 Finance e o Dynamics 365 Project Service Automation.
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
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: ed7ca3c85d3f99b7eefe10f4ddec822b9aeb1684
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082543"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="ae8c6-103">Sincronizar categorias de despesas do projeto entre o Finance and Operations e o Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="ae8c6-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ae8c6-104">Este tópico descreve os modelos e as tarefas subjacentes que são utilizados para sincronizar as categorias de despesa do projeto entre o Dynamics 365 Finance e o Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="ae8c6-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Dynamics 365 Finance and Dynamics 365 Project Service Automation.</span></span>

> [!NOTE]
> - <span data-ttu-id="ae8c6-105">A integração de tarefas do projeto, as categorias de transações de despesas, as estimativas de horas, as estimativas de despesas e o bloqueio de funcionalidades estão disponíveis na versão 8.0.</span><span class="sxs-lookup"><span data-stu-id="ae8c6-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="ae8c6-106">A integração dos valores reais está disponível na versão 8.0.1 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="ae8c6-106">Actuals integration is available in version 8.0.1 or later.</span></span>
> - <span data-ttu-id="ae8c6-107">Se estiver a utilizar a Enterprise edition 7.3.0 depois de instalar o KB 4132657 e o KB 4132660, poderá utilizar os modelos para integrar tarefas de projeto, categorias de transações de despesas, estimativas de horas, estimativas de despesas e valores reais, e para configurar o bloqueio de funcionalidades.</span><span class="sxs-lookup"><span data-stu-id="ae8c6-107">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="ae8c6-108">Se tiver de repor as distribuições contabilísticas, recomendamos que também instale o KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="ae8c6-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance"></a><span data-ttu-id="ae8c6-109">Fluxo de dados para o Project Service Automation e o Finance</span><span class="sxs-lookup"><span data-stu-id="ae8c6-109">Data flow for Project Service Automation and Finance</span></span>

<span data-ttu-id="ae8c6-110">A solução de integração do Project Service Automation e do Finance utiliza a funcionalidade Integração de Dados para sincronizar os dados entre instâncias do Project Service Automation e do Finance.</span><span class="sxs-lookup"><span data-stu-id="ae8c6-110">The Project Service Automation and Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="ae8c6-111">Os modelos de integração que estão disponíveis com a funcionalidade Integração de dados permitem o fluxo de dados sobre as categorias de transações de despesas do projeto entre o Finance e o Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="ae8c6-111">The integration templates that are available with the Data integration feature enable the flow of data about project expense transaction categories between Finance and Project Service Automation.</span></span>

<span data-ttu-id="ae8c6-112">Se as categorias de despesas do projeto forem geridas no Finance, o fluxo de integração ocorre primeiro do Finance para o Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="ae8c6-112">If the project expense categories are mastered in Finance, the integration flow is first from Finance to Project Service Automation.</span></span> <span data-ttu-id="ae8c6-113">Os IDs de integração das categorias de despesas do projeto são então atualizados através da sincronização do Project Service Automation para o Finance.</span><span class="sxs-lookup"><span data-stu-id="ae8c6-113">The integration IDs of the project expense categories are then updated through synchronization from Project Service Automation to Finance.</span></span>

<span data-ttu-id="ae8c6-114">Se as categorias de despesas do projeto forem geridas no Project Service Automation, o fluxo de integração ocorre primeiro do Project Service Automation para o Finance.</span><span class="sxs-lookup"><span data-stu-id="ae8c6-114">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance.</span></span> <span data-ttu-id="ae8c6-115">As categorias de projetos já têm de estar configuradas no Finance antes da sincronização a partir do Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="ae8c6-115">The project categories must already be configured in Finance before the synchronization from Project Service Automation.</span></span> <span data-ttu-id="ae8c6-116">Em seguida, sincronize do Finance para o Project Service Automation e, depois, de volta do Project Service Automation para o Finance.</span><span class="sxs-lookup"><span data-stu-id="ae8c6-116">Then synchronize from Finance back to Project Service Automation, and then from Project Service Automation to Finance again.</span></span> <span data-ttu-id="ae8c6-117">Desta forma, ajuda a garantir que as categorias estão ligadas e que não são criadas entradas duplicadas.</span><span class="sxs-lookup"><span data-stu-id="ae8c6-117">In this way, you help guarantee that the categories are linked, and that no duplicates are created.</span></span>

> [!NOTE]
> <span data-ttu-id="ae8c6-118">Tipicamente, as categorias de despesas do projeto são geridas no Finance.</span><span class="sxs-lookup"><span data-stu-id="ae8c6-118">Typically, the project expense categories are mastered in Finance.</span></span> <span data-ttu-id="ae8c6-119">No entanto, se não forem, ou se já tiverem sido criadas categorias de despesas no Project Service Automation, primeiro tem de sincronizar ao utilizar o modelo Categorias de transações de despesas do projeto (PSA para Fin and Ops).</span><span class="sxs-lookup"><span data-stu-id="ae8c6-119">However, if they aren't, or if expense categories have already been created in Project Service Automation, you must first synchronize by using the Project expense transaction categories (PSA to Fin and Ops) template.</span></span> <span data-ttu-id="ae8c6-120">Em seguida, sincronize ao utilizar o modelo Categorias de transações de despesas do projeto (Fin and Ops para PSA).</span><span class="sxs-lookup"><span data-stu-id="ae8c6-120">Then synchronize by using the Project expense transaction categories (Fin and Ops to PSA) template.</span></span> <span data-ttu-id="ae8c6-121">Em seguida, deve executar a sincronização entre o Project Service Automation e o Finance mais uma vez.</span><span class="sxs-lookup"><span data-stu-id="ae8c6-121">You should then run the synchronization from Project Service Automation to Finance one more time.</span></span>
>
> <span data-ttu-id="ae8c6-122">Se sincronizar primeiro a partir do Project Service Automation, os seguintes requisitos terão de ser cumpridos no Finance antes de a sincronização ser executada:</span><span class="sxs-lookup"><span data-stu-id="ae8c6-122">If you synchronize first from Project Service Automation, the following requirements must be met in Finance before the synchronization is run:</span></span>
>
> - <span data-ttu-id="ae8c6-123">A categoria partilhada que corresponde à categoria do projeto que está configurada no Project Service Automation tem de existir, e tem de estar ativada parapara o **Projeto** e as **Despesas**.</span><span class="sxs-lookup"><span data-stu-id="ae8c6-123">The shared category that matches the project category that is set up in Project Service Automation must exist, and it must be enabled for both **Project** and **Expense**.</span></span>
> - <span data-ttu-id="ae8c6-124">Para cada entidade jurídica do Finance com a qual tenha de ser feita a integração, têm de existir as seguintes categorias do projeto:</span><span class="sxs-lookup"><span data-stu-id="ae8c6-124">For each Finance legal entity that must be integrated with, the following project categories must exist:</span></span>
>
>     - <span data-ttu-id="ae8c6-125">Existe a **Categoria do projeto**.</span><span class="sxs-lookup"><span data-stu-id="ae8c6-125">**Project category** exists.</span></span> 
>     - <span data-ttu-id="ae8c6-126">**Utilização nas Despesas** está ativado.</span><span class="sxs-lookup"><span data-stu-id="ae8c6-126">**Use in Expense** is enabled.</span></span>
>     - <span data-ttu-id="ae8c6-127">**Ativo no diário** está ativado.</span><span class="sxs-lookup"><span data-stu-id="ae8c6-127">**Active in journal** is enabled.</span></span>
>     - <span data-ttu-id="ae8c6-128">**Tipo de transação** está definido como **Despesa**.</span><span class="sxs-lookup"><span data-stu-id="ae8c6-128">**Transaction type** is set to **Expense**.</span></span>

<span data-ttu-id="ae8c6-129">A seguinte ilustração mostra como os dados são sincronizados entre o Project Service Automation e o Finance.</span><span class="sxs-lookup"><span data-stu-id="ae8c6-129">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="ae8c6-130">[![Fluxo de dados para a integração do Project Service Automation com o Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="ae8c6-130">[![Data flow for Project Service Automation integration with Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a><span data-ttu-id="ae8c6-131">Sincronização das categorias de despesas do projeto do Finance para o Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="ae8c6-131">Project expense category synchronization from Finance to Project Service Automation</span></span>

### <a name="template-and-task"></a><span data-ttu-id="ae8c6-132">Modelo e tarefa</span><span class="sxs-lookup"><span data-stu-id="ae8c6-132">Template and task</span></span>

<span data-ttu-id="ae8c6-133">Para aceder ao modelo, no centro de administração do Microsoft Power Apps, selecione **Projetos** e, em seguida, no canto superior direito, selecione **Novo projeto** para selecionar modelos públicos.</span><span class="sxs-lookup"><span data-stu-id="ae8c6-133">To access the template, in the Microsoft Power Apps admin center, select **Projects** , and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="ae8c6-134">O modelo seguinte e a tarefa subjacente são utilizados para sincronizar as categorias de despesa do Finance para o Project Service Automation:</span><span class="sxs-lookup"><span data-stu-id="ae8c6-134">The following template and underlying task are used to synchronize project expense categories from Finance to Project Service Automation:</span></span>

- <span data-ttu-id="ae8c6-135">**Nome do modelo na Integração de dados:** Categorias de transações de despesas do projeto (Fin and Ops para PSA)</span><span class="sxs-lookup"><span data-stu-id="ae8c6-135">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
- <span data-ttu-id="ae8c6-136">**Nome da tarefa no projeto:** sincronizar categorias para o PSA</span><span class="sxs-lookup"><span data-stu-id="ae8c6-136">**Name of the task in the project:** Sync categories to PSA</span></span>

### <a name="entity-set"></a><span data-ttu-id="ae8c6-137">Conjunto de entidades</span><span class="sxs-lookup"><span data-stu-id="ae8c6-137">Entity set</span></span>

| <span data-ttu-id="ae8c6-138">Finanças</span><span class="sxs-lookup"><span data-stu-id="ae8c6-138">Finance</span></span>                           | <span data-ttu-id="ae8c6-139">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="ae8c6-139">Project Service Automation</span></span> |
|-----------------------------------|----------------------------|
| <span data-ttu-id="ae8c6-140">Entidade de integração para categorias</span><span class="sxs-lookup"><span data-stu-id="ae8c6-140">Integration entity for categories</span></span> | <span data-ttu-id="ae8c6-141">Categorias de transações</span><span class="sxs-lookup"><span data-stu-id="ae8c6-141">Transaction categories</span></span>     |

### <a name="entity-flow"></a><span data-ttu-id="ae8c6-142">Fluxo de entidades</span><span class="sxs-lookup"><span data-stu-id="ae8c6-142">Entity flow</span></span>

<span data-ttu-id="ae8c6-143">As categorias de despesas do projeto são geridas no Finance e sincronizadas com o Project Service Automation como categorias de transações.</span><span class="sxs-lookup"><span data-stu-id="ae8c6-143">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="ae8c6-144">Power Query</span><span class="sxs-lookup"><span data-stu-id="ae8c6-144">Power Query</span></span>

<span data-ttu-id="ae8c6-145">Quando estiver a sincronizar com o Project Service Automation, tem de utilizar o Microsoft Power Query para Excel definir o tipo de faturação na categoria de transação.</span><span class="sxs-lookup"><span data-stu-id="ae8c6-145">When you're synchronizing to Project Service Automation, you must use Microsoft Power Query for Excel to set the billing type on the transaction category.</span></span> <span data-ttu-id="ae8c6-146">O modelo Categorias de transações de despesas do projeto (Fin and Ops para PSA) fornece uma coluna e mapeamento predefinidos.</span><span class="sxs-lookup"><span data-stu-id="ae8c6-146">The Project expense transaction categories (Fin and Ops to PSA) template provides a default column and mapping.</span></span> <span data-ttu-id="ae8c6-147">Se criar o seu próprio modelo, tem de adicionar uma coluna condicional no Power Query.</span><span class="sxs-lookup"><span data-stu-id="ae8c6-147">If you create your own template, you must add a conditional column in Power Query.</span></span> <span data-ttu-id="ae8c6-148">Siga estes passos.</span><span class="sxs-lookup"><span data-stu-id="ae8c6-148">Follow these steps.</span></span>

1. <span data-ttu-id="ae8c6-149">Clique na seta para abrir o mapeamento da tarefa das categorias de despesas do projeto no modelo Categorias de transações de despesas do projeto (Fin and Ops para PSA).</span><span class="sxs-lookup"><span data-stu-id="ae8c6-149">Click the arrow to open the mapping of the project expense categories task in the Project expense transaction categories (Fin and Ops to PSA) template.</span></span>
2. <span data-ttu-id="ae8c6-150">Clique na ligação **Consulta e Filtragem Avançadas** para abrir o Power Query.</span><span class="sxs-lookup"><span data-stu-id="ae8c6-150">Click the **Advance Query and Filtering** link to open Power Query.</span></span>
2. <span data-ttu-id="ae8c6-151">Selecione **Adicionar Coluna Condicional**.</span><span class="sxs-lookup"><span data-stu-id="ae8c6-151">Select **Add Conditional Column**.</span></span>
3. <span data-ttu-id="ae8c6-152">Introduza um nome para a nova coluna, como **BillingType**.</span><span class="sxs-lookup"><span data-stu-id="ae8c6-152">Enter a name for the new column, such as **BillingType**.</span></span>
4. <span data-ttu-id="ae8c6-153">Introduza a seguinte condição: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span><span class="sxs-lookup"><span data-stu-id="ae8c6-153">Enter the following condition: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
5. <span data-ttu-id="ae8c6-154">Clique em **OK** na coluna.</span><span class="sxs-lookup"><span data-stu-id="ae8c6-154">Click **OK** on the column.</span></span>
6. <span data-ttu-id="ae8c6-155">Certifique-se de mapeia esta nova coluna na página de mapeamento.</span><span class="sxs-lookup"><span data-stu-id="ae8c6-155">Be sure to map this new column on the mapping page.</span></span>

<span data-ttu-id="ae8c6-156">A seguinte ilustração mostra um exemplo do mapeamento de tarefas do modelo na Integração de Dados.</span><span class="sxs-lookup"><span data-stu-id="ae8c6-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="ae8c6-157">O mapeamento mostra as informações do campo que serão sincronizadas entre o Finance e o Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="ae8c6-157">The mapping shows the field information that will be synchronized from Finance to Project Service Automation.</span></span>

<span data-ttu-id="ae8c6-158">[![Categorias de despesas de projeto para o mapeamento do modelo do Project Service Automation](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="ae8c6-158">[![Project expense category to Project Service Automation template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a><span data-ttu-id="ae8c6-159">Sincronização das categorias de despesas do projeto do Project Service Automation para o Finance</span><span class="sxs-lookup"><span data-stu-id="ae8c6-159">Project expense category synchronization from Project Service Automation to Finance</span></span>

### <a name="template-and-task"></a><span data-ttu-id="ae8c6-160">Modelo e tarefa</span><span class="sxs-lookup"><span data-stu-id="ae8c6-160">Template and task</span></span>

<span data-ttu-id="ae8c6-161">O modelo seguinte e a tarefa subjacente são utilizados para sincronizar as categorias de despesa do Project Service Automation para o Finance:</span><span class="sxs-lookup"><span data-stu-id="ae8c6-161">The following template and underlying task are used to synchronize project expense categories from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="ae8c6-162">**Nome do modelo na Integração de dados:** Categorias de transações de despesas do projeto (PSA para Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="ae8c6-162">**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="ae8c6-163">**Nome da tarefa no projeto:** sincronizar categorias para o Fin Ops</span><span class="sxs-lookup"><span data-stu-id="ae8c6-163">**Name of the task in the project:** Sync categories to Fin Ops</span></span>

### <a name="entity-set"></a><span data-ttu-id="ae8c6-164">Conjunto de entidades</span><span class="sxs-lookup"><span data-stu-id="ae8c6-164">Entity set</span></span>

| <span data-ttu-id="ae8c6-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="ae8c6-165">Project Service Automation</span></span> | <span data-ttu-id="ae8c6-166">Finanças</span><span class="sxs-lookup"><span data-stu-id="ae8c6-166">Finance</span></span>                           |
|----------------------------|-----------------------------------|
| <span data-ttu-id="ae8c6-167">Categorias de transações</span><span class="sxs-lookup"><span data-stu-id="ae8c6-167">Transaction categories</span></span>     | <span data-ttu-id="ae8c6-168">Entidade de integração para categorias</span><span class="sxs-lookup"><span data-stu-id="ae8c6-168">Integration entity for categories</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="ae8c6-169">Fluxo de entidades</span><span class="sxs-lookup"><span data-stu-id="ae8c6-169">Entity flow</span></span>

<span data-ttu-id="ae8c6-170">As categorias de despesas do projeto são geridas no Finance e sincronizadas com o Project Service Automation como categorias de transações.</span><span class="sxs-lookup"><span data-stu-id="ae8c6-170">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="ae8c6-171">A sincronização de volta para o Finance atualiza a categoria do projeto no Finance com o ID de integração a partir do Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="ae8c6-171">The synchronization back to Finance updates the project category in Finance with the integration ID from Project Service Automation.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="ae8c6-172">Mapeamento de modelos na Integração de dados</span><span class="sxs-lookup"><span data-stu-id="ae8c6-172">Template mapping in Data integration</span></span>

<span data-ttu-id="ae8c6-173">A seguinte ilustração mostra um exemplo do mapeamento de tarefas do modelo na Integração de Dados.</span><span class="sxs-lookup"><span data-stu-id="ae8c6-173">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="ae8c6-174">O mapeamento mostra as informações do campo que serão sincronizadas do Project Service Automation para Finance.</span><span class="sxs-lookup"><span data-stu-id="ae8c6-174">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="ae8c6-175">[![Mapeamento do modelo do Project Service Automation para o Finance](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="ae8c6-175">[![Project Service Automation to Finance template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>
