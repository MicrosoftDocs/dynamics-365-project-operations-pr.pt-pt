---
title: Configurar componentes faturáveis de um item de contrato baseado em projetos
description: Este tópico fornece informações sobre como adicionar componentes faturáveis a itens de contrato no Project Operations.
author: rumant
ms.date: 10/08/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b29c912828aa4af2d2d9cb47869012087cb834b4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003735"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a><span data-ttu-id="7062f-103">Configurar componentes faturáveis de um item de contrato baseado em projetos</span><span class="sxs-lookup"><span data-stu-id="7062f-103">Configure chargeable components of a project-based contract line</span></span>

<span data-ttu-id="7062f-104">_**Aplica-se a:** Implementação leve - negociar à faturação pró-forma, Project Operations para cenários baseados em recursos/não armazenados_</span><span class="sxs-lookup"><span data-stu-id="7062f-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="7062f-105">Um item de contrato baseado em projeto tem componentes *incluídos* e componentes *faturáveis*.</span><span class="sxs-lookup"><span data-stu-id="7062f-105">A project-based contract line has *included* components and *chargeable* components.</span></span>

<span data-ttu-id="7062f-106">Os componentes incluídos são componentes que estão sujeitos a:</span><span class="sxs-lookup"><span data-stu-id="7062f-106">Included components are components that are subject to:</span></span>

  - <span data-ttu-id="7062f-107">Método de faturação e divisões de clientes</span><span class="sxs-lookup"><span data-stu-id="7062f-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="7062f-108">Limites a não exceder</span><span class="sxs-lookup"><span data-stu-id="7062f-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="7062f-109">Definições de frequência de fatura definidas no item de contrato baseado em projeto</span><span class="sxs-lookup"><span data-stu-id="7062f-109">Invoice frequency settings defined on the project-based contract line</span></span>

<span data-ttu-id="7062f-110">Um subconjunto dos componentes incluídos pode ser marcado como faturável utilizando o campo **Tipo de Faturação**.</span><span class="sxs-lookup"><span data-stu-id="7062f-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="7062f-111">O campo **Tipo de Faturação** é um conjunto de opções que permite os seguintes valores no contexto de um item de contrato:</span><span class="sxs-lookup"><span data-stu-id="7062f-111">The **Billing Type** field is an option-set that allows the following values in the context of a contract line:</span></span>

  - <span data-ttu-id="7062f-112">Faturável</span><span class="sxs-lookup"><span data-stu-id="7062f-112">Chargeable</span></span>
  - <span data-ttu-id="7062f-113">Não faturável</span><span class="sxs-lookup"><span data-stu-id="7062f-113">Non-chargeable</span></span>

<span data-ttu-id="7062f-114">Os componentes faturáveis podem ser definidos nas categorias de tarefas, funções e transações.</span><span class="sxs-lookup"><span data-stu-id="7062f-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="7062f-115">A capacidade de faturação é definida em tarefas para um item de contrato de projeto e aplica-se a todas as classes de transação incluídas no item.</span><span class="sxs-lookup"><span data-stu-id="7062f-115">Chargeability is defined on tasks for a project contract line and applies to all transaction classes included on the line.</span></span> <span data-ttu-id="7062f-116">Se o campo **Incluir Tarefas** num item de contrato estiver em branco ou definido para **Todo o projeto**, o separador **Tarefas faturáveis** não estará disponível.</span><span class="sxs-lookup"><span data-stu-id="7062f-116">If the **Include Tasks** field on a contract line is blank or set to **Entire project**, the **Chargeable tasks** tab will not be available.</span></span>

<span data-ttu-id="7062f-117">A capacidade de faturação definida nas funções de um item de contrato de projeto aplica-se apenas à classe de transação **Tempo**.</span><span class="sxs-lookup"><span data-stu-id="7062f-117">Chargeability defined on roles for a project contract line only applies to the **Time** transaction class.</span></span> <span data-ttu-id="7062f-118">Se o campo **Incluir Tempo** num item de contrato estiver definido para **Não**, o separador **Funções faturáveis** não estará disponível.</span><span class="sxs-lookup"><span data-stu-id="7062f-118">If the **Include Time** field on a contract line is set to **No**, the **Chargeable roles** tab will not be available.</span></span>

<span data-ttu-id="7062f-119">A capacidade de faturação definida nas categorias de transação de um item de contrato de projeto aplica-se apenas à classe de transação **Despesa**.</span><span class="sxs-lookup"><span data-stu-id="7062f-119">Chargeability defined on transaction categories for a project contract line only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="7062f-120">Se o campo **Incluir Despesas** estiver definido para **Não**, o separador **Categorias faturáveis** não estará disponível.</span><span class="sxs-lookup"><span data-stu-id="7062f-120">If the **Include Expenses** field is set to **No**, the **Chargeable Categories** tab will not be available.</span></span>

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a><span data-ttu-id="7062f-121">Atualizar uma tarefa de projeto como faturável ou não faturável</span><span class="sxs-lookup"><span data-stu-id="7062f-121">Update a project task as chargeable or non-chargeable</span></span>

<span data-ttu-id="7062f-122">Uma tarefa do projeto pode ser faturável ou não faturável num item de contrato específico, que torna possível a seguinte configuração:</span><span class="sxs-lookup"><span data-stu-id="7062f-122">A project task can be chargeable or non-chargeable on a specific contract line, which makes the following setup possible:</span></span>

<span data-ttu-id="7062f-123">Se um item de contrato baseado em projeto incluir **Tempo** e uma determinada tarefa, **T1** é associado a ela como faturável.</span><span class="sxs-lookup"><span data-stu-id="7062f-123">If a project-based contract line includes **Time** and a certain task, **T1** is associated to it as chargeable.</span></span> <span data-ttu-id="7062f-124">Se houver um segundo item de contrato que inclua **Despesas**, pode associar a tarefa T1 ao item de contrato como não faturável.</span><span class="sxs-lookup"><span data-stu-id="7062f-124">If there is a second contract line that includes **Expense**, you can associate the T1 task on the contract line as non-chargeable.</span></span> <span data-ttu-id="7062f-125">O resultado é que todo o tempo registado na tarefa é faturado e todas as despesas são não faturáveis.</span><span class="sxs-lookup"><span data-stu-id="7062f-125">The result is that all of the time recorded on the task is chargeable and all expenses are non-chargeable.</span></span>

<span data-ttu-id="7062f-126">O tipo de faturação de uma tarefa pode ser configurado no separador **Tarefas Faturáveis** de um item de contrato, atualizando o campo **Tipo de Faturação** na subgrelha de tarefas do item de contrato.</span><span class="sxs-lookup"><span data-stu-id="7062f-126">A task's billing type can be configured on the **Chargeable Tasks** tab of the contract line by updating the **Billing Type** field on the contract line tasks subgrid.</span></span> <span data-ttu-id="7062f-127">Em alternativa, pode atualizar o campo **Tipo de Faturação** na subgrelha da configuração de Faturação da tarefa de itens de contrato associados a uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="7062f-127">Alternatively, you can update the **Billing Type** field on the subgrid of the task Billing setup of a project that shows the contract lines associated to a task.</span></span>

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a><span data-ttu-id="7062f-128">Atualizar uma função de projeto como faturável ou não faturável</span><span class="sxs-lookup"><span data-stu-id="7062f-128">Update a role as chargeable or non-chargeable</span></span>

<span data-ttu-id="7062f-129">Uma função pode ser faturável ou não faturável num item de contrato específico.</span><span class="sxs-lookup"><span data-stu-id="7062f-129">A role can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="7062f-130">O tipo de faturação de uma função pode ser configurado no separador **Funções faturáveis** de um item de contrato.</span><span class="sxs-lookup"><span data-stu-id="7062f-130">A role's billing type can be configured on the **Chargeable Roles** tab of a contract line.</span></span> <span data-ttu-id="7062f-131">Para isso, atualize o campo **Tipo de Faturação** na subgrelha **Funções Faturáveis**.</span><span class="sxs-lookup"><span data-stu-id="7062f-131">To do this, update the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a><span data-ttu-id="7062f-132">Atualizar uma categoria de transação como faturável ou não faturável</span><span class="sxs-lookup"><span data-stu-id="7062f-132">Update a transaction category as chargeable or non-chargeable</span></span>

<span data-ttu-id="7062f-133">Uma categoria de transação pode ser faturável ou não faturável num item de contrato específico.</span><span class="sxs-lookup"><span data-stu-id="7062f-133">A transaction category can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="7062f-134">O tipo de faturação de uma transação pode ser configurado no separador **Categorias faturáveis** de um item de contrato baseado em projeto.</span><span class="sxs-lookup"><span data-stu-id="7062f-134">A transaction's billing type can be configured on the **Chargeable Categories** tab of a project-based contract line.</span></span> <span data-ttu-id="7062f-135">Para isso, atualize o campo **Tipo de Faturação** na subgrelha **Categorias Faturáveis**.</span><span class="sxs-lookup"><span data-stu-id="7062f-135">To do this, update the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="7062f-136">Resolver a capacidade de faturação</span><span class="sxs-lookup"><span data-stu-id="7062f-136">Resolve chargeability</span></span>

<span data-ttu-id="7062f-137">Uma estimativa ou um valor real criado para o tempo só é considerado faturável se:</span><span class="sxs-lookup"><span data-stu-id="7062f-137">An estimate or actual created for time is only considered chargeable if:</span></span>

   - <span data-ttu-id="7062f-138">**Tempo** está incluído na linha do contrato.</span><span class="sxs-lookup"><span data-stu-id="7062f-138">**Time** is included on the contract line.</span></span>
   - <span data-ttu-id="7062f-139">**Função** é configurado como responsável no item de contrato.</span><span class="sxs-lookup"><span data-stu-id="7062f-139">**Role** is configured as chargeable on the contract line.</span></span>
   - <span data-ttu-id="7062f-140">**Tarefas incluídas** estão definidas para **Tarefas selecionadas** no item de contrato.</span><span class="sxs-lookup"><span data-stu-id="7062f-140">**Included Tasks** is set to **Selected tasks** on the contract line.</span></span>
 
 <span data-ttu-id="7062f-141">Se estas três coisas forem verdadeiras, a tarefa é configurada como faturável.</span><span class="sxs-lookup"><span data-stu-id="7062f-141">If these three things are true, the task is configured as chargeable.</span></span> 

<span data-ttu-id="7062f-142">Uma estimativa ou um valor real criado para a despesa só é considerado faturável se:</span><span class="sxs-lookup"><span data-stu-id="7062f-142">An estimate or actual created for expense is only considered chargeable if:</span></span>

   - <span data-ttu-id="7062f-143">**Despesa** está incluído no item de contrato</span><span class="sxs-lookup"><span data-stu-id="7062f-143">**Expense** is included on the contract line</span></span>
   - <span data-ttu-id="7062f-144">**Categoria de transação** é configurado como faturável no item de contrato</span><span class="sxs-lookup"><span data-stu-id="7062f-144">**Transaction category** is configured as chargeable on the contract line</span></span>
   - <span data-ttu-id="7062f-145">**Tarefas incluídas** estão definidas para **Tarefa selecionadas** no item de contrato</span><span class="sxs-lookup"><span data-stu-id="7062f-145">**Included Tasks** is set to **Selected task** on the contract line</span></span>
  
 <span data-ttu-id="7062f-146">Se estas três coisas forem verdadeiras, a **Tarefa** é configurada como faturável.</span><span class="sxs-lookup"><span data-stu-id="7062f-146">If these three things are true, the **Task** is configured as chargeable.</span></span> 

<span data-ttu-id="7062f-147">Uma estimativa ou um valor real criado para o material só é considerado faturável se:</span><span class="sxs-lookup"><span data-stu-id="7062f-147">An estimate or actual created for material is only considered chargeable if:</span></span>

   - <span data-ttu-id="7062f-148">**Materiais** está incluído no item de contrato</span><span class="sxs-lookup"><span data-stu-id="7062f-148">**Materials** is included on the contract line</span></span>
   - <span data-ttu-id="7062f-149">**Tarefas incluídas** estão definidas para **Tarefas selecionadas** no item de contrato</span><span class="sxs-lookup"><span data-stu-id="7062f-149">**Included Tasks** is set to **Selected tasks** on the contract line</span></span>

<span data-ttu-id="7062f-150">Se estas duas coisas forem verdadeiras, a **Tarefa** é configurada como faturável.</span><span class="sxs-lookup"><span data-stu-id="7062f-150">If these two things are true, the **Task** is configured as chargeable.</span></span> 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="7062f-151">
                    <strong>Inclui Tempo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7062f-151">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="7062f-152">
                    <strong>Inclui Despesa</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="7062f-152">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="7062f-153">
                    <strong>Incluir materiais</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="7062f-153">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="7062f-154">
                    <strong>Tarefas Incluídas</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="7062f-154">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="7062f-155">
                    <strong>Função</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="7062f-155">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="7062f-156">
                    <strong>Categoria</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="7062f-156">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="7062f-157">
                    <strong>Tarefa</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="7062f-157">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="7062f-158">
                    <strong>Impacto da possível faturação</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7062f-158">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="7062f-159">Sim</span><span class="sxs-lookup"><span data-stu-id="7062f-159">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="7062f-160">Sim</span><span class="sxs-lookup"><span data-stu-id="7062f-160">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="7062f-161">Sim</span><span class="sxs-lookup"><span data-stu-id="7062f-161">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="7062f-162">Todo o Projeto</span><span class="sxs-lookup"><span data-stu-id="7062f-162">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="7062f-163">Faturável</span><span class="sxs-lookup"><span data-stu-id="7062f-163">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="7062f-164">Faturável</span><span class="sxs-lookup"><span data-stu-id="7062f-164">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="7062f-165">Não pode ser definido</span><span class="sxs-lookup"><span data-stu-id="7062f-165">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="7062f-166">Faturação num valor real de tempo: <strong>Faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7062f-166">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="7062f-167">Tipo de faturação em valor real de despesas: <strong>Faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7062f-167">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="7062f-168">Tipo de faturação em valor real de material: <strong>Faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7062f-168">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="7062f-169">Sim</span><span class="sxs-lookup"><span data-stu-id="7062f-169">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="7062f-170">Sim</span><span class="sxs-lookup"><span data-stu-id="7062f-170">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="7062f-171">Sim</span><span class="sxs-lookup"><span data-stu-id="7062f-171">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="7062f-172">Apenas tarefas selecionadas</span><span class="sxs-lookup"><span data-stu-id="7062f-172">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="7062f-173">Faturável</span><span class="sxs-lookup"><span data-stu-id="7062f-173">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="7062f-174">Faturável</span><span class="sxs-lookup"><span data-stu-id="7062f-174">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="7062f-175">Faturável</span><span class="sxs-lookup"><span data-stu-id="7062f-175">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="7062f-176">Faturação num valor real de tempo: <strong>Faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7062f-176">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="7062f-177">Tipo de faturação em valor real de despesas: <strong>Faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7062f-177">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="7062f-178">Tipo de faturação em valor real de material: <strong>Faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7062f-178">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="7062f-179">Sim</span><span class="sxs-lookup"><span data-stu-id="7062f-179">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="7062f-180">Sim</span><span class="sxs-lookup"><span data-stu-id="7062f-180">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="7062f-181">Sim</span><span class="sxs-lookup"><span data-stu-id="7062f-181">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="7062f-182">Apenas tarefas selecionadas</span><span class="sxs-lookup"><span data-stu-id="7062f-182">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="7062f-183">
                    <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7062f-183">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="7062f-184">Faturável</span><span class="sxs-lookup"><span data-stu-id="7062f-184">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="7062f-185">Faturável</span><span class="sxs-lookup"><span data-stu-id="7062f-185">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="7062f-186">Faturação num valor real de tempo: <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7062f-186">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="7062f-187">Tipo de faturação em valor real de despesas: Faturável</span><span class="sxs-lookup"><span data-stu-id="7062f-187">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="7062f-188">Tipo de faturação em valor real de material: Faturável</span><span class="sxs-lookup"><span data-stu-id="7062f-188">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="7062f-189">Sim</span><span class="sxs-lookup"><span data-stu-id="7062f-189">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="7062f-190">Sim</span><span class="sxs-lookup"><span data-stu-id="7062f-190">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="7062f-191">Sim</span><span class="sxs-lookup"><span data-stu-id="7062f-191">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="7062f-192">Apenas tarefas selecionadas</span><span class="sxs-lookup"><span data-stu-id="7062f-192">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="7062f-193">Faturável</span><span class="sxs-lookup"><span data-stu-id="7062f-193">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="7062f-194">Faturável</span><span class="sxs-lookup"><span data-stu-id="7062f-194">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="7062f-195">
                    <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7062f-195">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="7062f-196">Faturação num valor real de tempo: <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7062f-196">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="7062f-197">Tipo de faturação em valor real de despesas: <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7062f-197">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="7062f-198">Tipo de faturação em valor real de material: <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7062f-198">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="7062f-199">Sim</span><span class="sxs-lookup"><span data-stu-id="7062f-199">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="7062f-200">Sim</span><span class="sxs-lookup"><span data-stu-id="7062f-200">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="7062f-201">Sim</span><span class="sxs-lookup"><span data-stu-id="7062f-201">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="7062f-202">Apenas tarefas selecionadas</span><span class="sxs-lookup"><span data-stu-id="7062f-202">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="7062f-203">
                    <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7062f-203">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="7062f-204">Faturável</span><span class="sxs-lookup"><span data-stu-id="7062f-204">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="7062f-205">
                    <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7062f-205">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="7062f-206">Faturação num valor real de tempo: <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7062f-206">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="7062f-207">Tipo de faturação em valor real de despesas: <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7062f-207">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="7062f-208">Tipo de faturação em valor real de material: <strong> Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7062f-208">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="7062f-209">Sim</span><span class="sxs-lookup"><span data-stu-id="7062f-209">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="7062f-210">Sim</span><span class="sxs-lookup"><span data-stu-id="7062f-210">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="7062f-211">Sim</span><span class="sxs-lookup"><span data-stu-id="7062f-211">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="7062f-212">Apenas tarefas selecionadas</span><span class="sxs-lookup"><span data-stu-id="7062f-212">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="7062f-213">
                    <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7062f-213">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="7062f-214">
                    <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7062f-214">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="7062f-215">Faturável</span><span class="sxs-lookup"><span data-stu-id="7062f-215">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="7062f-216">Faturação num valor real de tempo: <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7062f-216">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="7062f-217">Tipo de faturação em valor real de despesas: <strong> Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7062f-217">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="7062f-218">Tipo de faturação em valor real de material: Faturável</span><span class="sxs-lookup"><span data-stu-id="7062f-218">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="7062f-219">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7062f-219">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="7062f-220">Sim</span><span class="sxs-lookup"><span data-stu-id="7062f-220">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="7062f-221">Sim</span><span class="sxs-lookup"><span data-stu-id="7062f-221">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="7062f-222">Todo o Projeto</span><span class="sxs-lookup"><span data-stu-id="7062f-222">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="7062f-223">Não pode ser definido</span><span class="sxs-lookup"><span data-stu-id="7062f-223">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="7062f-224">
                    <strong>Faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7062f-224">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="7062f-225">Não pode ser definido</span><span class="sxs-lookup"><span data-stu-id="7062f-225">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="7062f-226">Faturação num valor real de tempo: <strong>Não disponível</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7062f-226">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="7062f-227">Tipo de faturação em valor real de despesas: Faturável</span><span class="sxs-lookup"><span data-stu-id="7062f-227">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="7062f-228">Tipo de faturação em valor real de material: Faturável</span><span class="sxs-lookup"><span data-stu-id="7062f-228">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="7062f-229">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7062f-229">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="7062f-230">Sim</span><span class="sxs-lookup"><span data-stu-id="7062f-230">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="7062f-231">Sim</span><span class="sxs-lookup"><span data-stu-id="7062f-231">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="7062f-232">Todo o Projeto</span><span class="sxs-lookup"><span data-stu-id="7062f-232">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="7062f-233">Não pode ser definido</span><span class="sxs-lookup"><span data-stu-id="7062f-233">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="7062f-234">
                    <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7062f-234">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="7062f-235">Não pode ser definido</span><span class="sxs-lookup"><span data-stu-id="7062f-235">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="7062f-236">Faturação num valor real de tempo: <strong>Não disponível</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7062f-236">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="7062f-237">Tipo de faturação em valor real de despesas: <strong> Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7062f-237">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="7062f-238">Tipo de faturação em valor real de material: Faturável</span><span class="sxs-lookup"><span data-stu-id="7062f-238">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="7062f-239">Sim</span><span class="sxs-lookup"><span data-stu-id="7062f-239">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="7062f-240">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7062f-240">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="7062f-241">Sim</span><span class="sxs-lookup"><span data-stu-id="7062f-241">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="7062f-242">Todo o Projeto</span><span class="sxs-lookup"><span data-stu-id="7062f-242">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="7062f-243">Faturável</span><span class="sxs-lookup"><span data-stu-id="7062f-243">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="7062f-244">Não pode ser definido</span><span class="sxs-lookup"><span data-stu-id="7062f-244">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="7062f-245">Não pode ser definido</span><span class="sxs-lookup"><span data-stu-id="7062f-245">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="7062f-246">Faturação num valor real de tempo: Faturável</span><span class="sxs-lookup"><span data-stu-id="7062f-246">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="7062f-247">Tipo de faturação em valor real de despesas:<strong> Não disponível</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7062f-247">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="7062f-248">Tipo de faturação em valor real de material: Faturável</span><span class="sxs-lookup"><span data-stu-id="7062f-248">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="7062f-249">Sim</span><span class="sxs-lookup"><span data-stu-id="7062f-249">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="7062f-250">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7062f-250">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="7062f-251">Sim</span><span class="sxs-lookup"><span data-stu-id="7062f-251">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="7062f-252">Todo o Projeto</span><span class="sxs-lookup"><span data-stu-id="7062f-252">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="7062f-253">
                    <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7062f-253">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="7062f-254">Não pode ser definido</span><span class="sxs-lookup"><span data-stu-id="7062f-254">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="7062f-255">Não pode ser definido</span><span class="sxs-lookup"><span data-stu-id="7062f-255">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="7062f-256">Faturação num valor real de tempo: <strong>Não faturável </strong>
                </span><span class="sxs-lookup"><span data-stu-id="7062f-256">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="7062f-257">Tipo de faturação em valor real de despesas:<strong> Não disponível</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7062f-257">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="7062f-258">Tipo de faturação em valor real de material: Faturável</span><span class="sxs-lookup"><span data-stu-id="7062f-258">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="7062f-259">Sim</span><span class="sxs-lookup"><span data-stu-id="7062f-259">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="7062f-260">Sim</span><span class="sxs-lookup"><span data-stu-id="7062f-260">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="7062f-261">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7062f-261">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="7062f-262">Todo o Projeto</span><span class="sxs-lookup"><span data-stu-id="7062f-262">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="7062f-263">Faturável</span><span class="sxs-lookup"><span data-stu-id="7062f-263">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="7062f-264">Faturável</span><span class="sxs-lookup"><span data-stu-id="7062f-264">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="7062f-265">Não pode ser definido</span><span class="sxs-lookup"><span data-stu-id="7062f-265">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="7062f-266">Faturação num valor real de tempo: Faturável</span><span class="sxs-lookup"><span data-stu-id="7062f-266">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="7062f-267">Tipo de faturação em valor real de despesas: Faturável</span><span class="sxs-lookup"><span data-stu-id="7062f-267">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="7062f-268">Tipo de faturação em valor real de material: <strong> Não disponível</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7062f-268">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="7062f-269">Sim</span><span class="sxs-lookup"><span data-stu-id="7062f-269">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="7062f-270">Sim</span><span class="sxs-lookup"><span data-stu-id="7062f-270">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="7062f-271">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7062f-271">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="7062f-272">Todo o Projeto</span><span class="sxs-lookup"><span data-stu-id="7062f-272">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="7062f-273">
                    <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7062f-273">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="7062f-274">
                    <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7062f-274">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="7062f-275">Não pode ser definido</span><span class="sxs-lookup"><span data-stu-id="7062f-275">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="7062f-276">Faturação num valor real de tempo: <strong>Não faturável </strong>
                </span><span class="sxs-lookup"><span data-stu-id="7062f-276">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="7062f-277">Tipo de faturação em valor real de despesas:<strong> Não faturável </strong>
                </span><span class="sxs-lookup"><span data-stu-id="7062f-277">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="7062f-278">Tipo de faturação em valor real de material:<strong> Não disponível</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7062f-278">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
