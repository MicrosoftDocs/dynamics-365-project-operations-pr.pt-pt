---
title: Configurar componentes faturáveis de um item de contrato baseado em projetos
description: Este tópico fornece informações sobre como adicionar componentes faturáveis a itens de contrato no Project Operations.
author: rumant
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ddada2cb412ba7370fb0a750325a84772937d8d0
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858487"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a><span data-ttu-id="50245-103">Configurar componentes faturáveis de um item de contrato baseado em projetos</span><span class="sxs-lookup"><span data-stu-id="50245-103">Configure chargeable components of a project-based contract line</span></span>

<span data-ttu-id="50245-104">_**Aplica-se a:** Implementação leve - negociar à faturação pró-forma, Project Operations para cenários baseados em recursos/não armazenados_</span><span class="sxs-lookup"><span data-stu-id="50245-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="50245-105">Um item de contrato baseado em projeto tem componentes *incluídos* e componentes *faturáveis*.</span><span class="sxs-lookup"><span data-stu-id="50245-105">A project-based contract line has *included* components and *chargeable* components.</span></span>

<span data-ttu-id="50245-106">Os componentes incluídos são componentes que estão sujeitos a:</span><span class="sxs-lookup"><span data-stu-id="50245-106">Included components are components that are subject to:</span></span>

  - <span data-ttu-id="50245-107">Método de faturação e divisões de clientes</span><span class="sxs-lookup"><span data-stu-id="50245-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="50245-108">Limites a não exceder</span><span class="sxs-lookup"><span data-stu-id="50245-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="50245-109">Definições de frequência de fatura definidas no item de contrato baseado em projeto</span><span class="sxs-lookup"><span data-stu-id="50245-109">Invoice frequency settings defined on the project-based contract line</span></span>

<span data-ttu-id="50245-110">Um subconjunto dos componentes incluídos pode ser marcado como faturável utilizando o campo **Tipo de Faturação**.</span><span class="sxs-lookup"><span data-stu-id="50245-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="50245-111">O campo **Tipo de Faturação** é um conjunto de opções que permite os seguintes valores no contexto de um item de contrato:</span><span class="sxs-lookup"><span data-stu-id="50245-111">The **Billing Type** field is an option-set that allows the following values in the context of a contract line:</span></span>

  - <span data-ttu-id="50245-112">Faturável</span><span class="sxs-lookup"><span data-stu-id="50245-112">Chargeable</span></span>
  - <span data-ttu-id="50245-113">Não faturável</span><span class="sxs-lookup"><span data-stu-id="50245-113">Non-chargeable</span></span>

<span data-ttu-id="50245-114">Os componentes faturáveis podem ser definidos nas categorias de tarefas, funções e transações.</span><span class="sxs-lookup"><span data-stu-id="50245-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="50245-115">A capacidade de faturação é definida em tarefas para um item de contrato de projeto e aplica-se a todas as classes de transação incluídas no item.</span><span class="sxs-lookup"><span data-stu-id="50245-115">Chargeability is defined on tasks for a project contract line and applies to all transaction classes included on the line.</span></span> <span data-ttu-id="50245-116">Se o campo **Incluir Tarefas** num item de contrato estiver em branco ou definido para **Todo o projeto**, o separador **Tarefas faturáveis** não estará disponível.</span><span class="sxs-lookup"><span data-stu-id="50245-116">If the **Include Tasks** field on a contract line is blank or set to **Entire project**, the **Chargeable tasks** tab will not be available.</span></span>

<span data-ttu-id="50245-117">A capacidade de faturação definida nas funções de um item de contrato de projeto aplica-se apenas à classe de transação **Tempo**.</span><span class="sxs-lookup"><span data-stu-id="50245-117">Chargeability defined on roles for a project contract line only applies to the **Time** transaction class.</span></span> <span data-ttu-id="50245-118">Se o campo **Incluir Tempo** num item de contrato estiver definido para **Não**, o separador **Funções faturáveis** não estará disponível.</span><span class="sxs-lookup"><span data-stu-id="50245-118">If the **Include Time** field on a contract line is set to **No**, the **Chargeable roles** tab will not be available.</span></span>

<span data-ttu-id="50245-119">A capacidade de faturação definida nas categorias de transação de um item de contrato de projeto aplica-se apenas à classe de transação **Despesa**.</span><span class="sxs-lookup"><span data-stu-id="50245-119">Chargeability defined on transaction categories for a project contract line only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="50245-120">Se o campo **Incluir Despesas** estiver definido para **Não**, o separador **Categorias faturáveis** não estará disponível.</span><span class="sxs-lookup"><span data-stu-id="50245-120">If the **Include Expenses** field is set to **No**, the **Chargeable Categories** tab will not be available.</span></span>

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a><span data-ttu-id="50245-121">Atualizar uma tarefa de projeto como faturável ou não faturável</span><span class="sxs-lookup"><span data-stu-id="50245-121">Update a project task as chargeable or non-chargeable</span></span>

<span data-ttu-id="50245-122">Uma tarefa do projeto pode ser faturável ou não faturável num item de contrato específico, que torna possível a seguinte configuração:</span><span class="sxs-lookup"><span data-stu-id="50245-122">A project task can be chargeable or non-chargeable on a specific contract line, which makes the following setup possible:</span></span>

<span data-ttu-id="50245-123">Se um item de contrato baseado em projeto incluir **Tempo** e uma determinada tarefa, **T1** é associado a ela como faturável.</span><span class="sxs-lookup"><span data-stu-id="50245-123">If a project-based contract line includes **Time** and a certain task, **T1** is associated to it as chargeable.</span></span> <span data-ttu-id="50245-124">Se houver um segundo item de contrato que inclua **Despesas**, pode associar a tarefa T1 ao item de contrato como não faturável.</span><span class="sxs-lookup"><span data-stu-id="50245-124">If there is a second contract line that includes **Expense**, you can associate the T1 task on the contract line as non-chargeable.</span></span> <span data-ttu-id="50245-125">O resultado é que todo o tempo registado na tarefa é faturado e todas as despesas são não faturáveis.</span><span class="sxs-lookup"><span data-stu-id="50245-125">The result is that all of the time recorded on the task is chargeable and all expenses are non-chargeable.</span></span>

<span data-ttu-id="50245-126">O tipo de faturação de uma tarefa pode ser configurado no separador **Tarefas Faturáveis** de um item de contrato, atualizando o campo **Tipo de Faturação** na subgrelha de tarefas do item de contrato.</span><span class="sxs-lookup"><span data-stu-id="50245-126">A task's billing type can be configured on the **Chargeable Tasks** tab of the contract line by updating the **Billing Type** field on the contract line tasks subgrid.</span></span> <span data-ttu-id="50245-127">Em alternativa, pode atualizar o campo **Tipo de Faturação** na subgrelha da configuração de Faturação da tarefa de itens de contrato associados a uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="50245-127">Alternatively, you can update the **Billing Type** field on the subgrid of the task Billing setup of a project that shows the contract lines associated to a task.</span></span>

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a><span data-ttu-id="50245-128">Atualizar uma função de projeto como faturável ou não faturável</span><span class="sxs-lookup"><span data-stu-id="50245-128">Update a role as chargeable or non-chargeable</span></span>

<span data-ttu-id="50245-129">Uma função pode ser faturável ou não faturável num item de contrato específico.</span><span class="sxs-lookup"><span data-stu-id="50245-129">A role can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="50245-130">O tipo de faturação de uma função pode ser configurado no separador **Funções faturáveis** de um item de contrato.</span><span class="sxs-lookup"><span data-stu-id="50245-130">A role's billing type can be configured on the **Chargeable Roles** tab of a contract line.</span></span> <span data-ttu-id="50245-131">Para isso, atualize o campo **Tipo de Faturação** na subgrelha **Funções Faturáveis**.</span><span class="sxs-lookup"><span data-stu-id="50245-131">To do this, update the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a><span data-ttu-id="50245-132">Atualizar uma categoria de transação como faturável ou não faturável</span><span class="sxs-lookup"><span data-stu-id="50245-132">Update a transaction category as chargeable or non-chargeable</span></span>

<span data-ttu-id="50245-133">Uma categoria de transação pode ser faturável ou não faturável num item de contrato específico.</span><span class="sxs-lookup"><span data-stu-id="50245-133">A transaction category can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="50245-134">O tipo de faturação de uma transação pode ser configurado no separador **Categorias faturáveis** de um item de contrato baseado em projeto.</span><span class="sxs-lookup"><span data-stu-id="50245-134">A transaction's billing type can be configured on the **Chargeable Categories** tab of a project-based contract line.</span></span> <span data-ttu-id="50245-135">Para isso, atualize o campo **Tipo de Faturação** na subgrelha **Categorias Faturáveis**.</span><span class="sxs-lookup"><span data-stu-id="50245-135">To do this, update the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="50245-136">Resolver a capacidade de faturação</span><span class="sxs-lookup"><span data-stu-id="50245-136">Resolve chargeability</span></span>

<span data-ttu-id="50245-137">Uma estimativa ou um valor real criado para o tempo só é considerado faturável se:</span><span class="sxs-lookup"><span data-stu-id="50245-137">An estimate or actual created for time is only considered chargeable if:</span></span>

   - <span data-ttu-id="50245-138">**Tempo** está incluído na linha do contrato.</span><span class="sxs-lookup"><span data-stu-id="50245-138">**Time** is included on the contract line.</span></span>
   - <span data-ttu-id="50245-139">**Função** é configurado como responsável no item de contrato.</span><span class="sxs-lookup"><span data-stu-id="50245-139">**Role** is configured as chargeable on the contract line.</span></span>
   - <span data-ttu-id="50245-140">**Tarefas incluídas** estão definidas para **Tarefas selecionadas** no item de contrato.</span><span class="sxs-lookup"><span data-stu-id="50245-140">**Included Tasks** is set to **Selected tasks** on the contract line.</span></span>
 
 <span data-ttu-id="50245-141">Se estas três coisas forem verdadeiras, a tarefa é configurada como faturável.</span><span class="sxs-lookup"><span data-stu-id="50245-141">If these three things are true, the task is configured as chargeable.</span></span> 

<span data-ttu-id="50245-142">Uma estimativa ou um valor real criado para a despesa só é considerado faturável se:</span><span class="sxs-lookup"><span data-stu-id="50245-142">An estimate or actual created for expense is only considered chargeable if:</span></span>

   - <span data-ttu-id="50245-143">**Despesa** está incluído no item de contrato</span><span class="sxs-lookup"><span data-stu-id="50245-143">**Expense** is included on the contract line</span></span>
   - <span data-ttu-id="50245-144">**Categoria de transação** é configurado como faturável no item de contrato</span><span class="sxs-lookup"><span data-stu-id="50245-144">**Transaction category** is configured as chargeable on the contract line</span></span>
   - <span data-ttu-id="50245-145">**Tarefas incluídas** estão definidas para **Tarefa selecionadas** no item de contrato</span><span class="sxs-lookup"><span data-stu-id="50245-145">**Included Tasks** is set to **Selected task** on the contract line</span></span>
  
 <span data-ttu-id="50245-146">Se estas três coisas forem verdadeiras, a **Tarefa** é configurada como faturável.</span><span class="sxs-lookup"><span data-stu-id="50245-146">If these three things are true, the **Task** is configured as chargeable.</span></span> 

<span data-ttu-id="50245-147">Uma estimativa ou um valor real criado para o material só é considerado faturável se:</span><span class="sxs-lookup"><span data-stu-id="50245-147">An estimate or actual created for material is only considered chargeable if:</span></span>

   - <span data-ttu-id="50245-148">**Materiais** está incluído no item de contrato</span><span class="sxs-lookup"><span data-stu-id="50245-148">**Materials** is included on the contract line</span></span>
   - <span data-ttu-id="50245-149">**Tarefas incluídas** estão definidas para **Tarefas selecionadas** no item de contrato</span><span class="sxs-lookup"><span data-stu-id="50245-149">**Included Tasks** is set to **Selected tasks** on the contract line</span></span>

<span data-ttu-id="50245-150">Se estas duas coisas forem verdadeiras, a **Tarefa** é configurada como faturável.</span><span class="sxs-lookup"><span data-stu-id="50245-150">If these two things are true, the **Task** is configured as chargeable.</span></span> 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="50245-151">
                    <strong>Inclui Tempo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50245-151">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="50245-152">
                    <strong>Inclui Despesa</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="50245-152">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="50245-153">
                    <strong>Incluir materiais</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="50245-153">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="50245-154">
                    <strong>Tarefas Incluídas</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="50245-154">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="50245-155">
                    <strong>Função</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="50245-155">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="50245-156">
                    <strong>Categoria</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="50245-156">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="50245-157">
                    <strong>Tarefa</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="50245-157">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="50245-158">
                    <strong>Impacto da possível faturação</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50245-158">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="50245-159">Sim</span><span class="sxs-lookup"><span data-stu-id="50245-159">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="50245-160">Sim</span><span class="sxs-lookup"><span data-stu-id="50245-160">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="50245-161">Sim</span><span class="sxs-lookup"><span data-stu-id="50245-161">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="50245-162">Todo o Projeto</span><span class="sxs-lookup"><span data-stu-id="50245-162">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="50245-163">Faturável</span><span class="sxs-lookup"><span data-stu-id="50245-163">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="50245-164">Faturável</span><span class="sxs-lookup"><span data-stu-id="50245-164">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="50245-165">Não pode ser definido</span><span class="sxs-lookup"><span data-stu-id="50245-165">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="50245-166">Faturação num valor real de tempo: <strong>Faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50245-166">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="50245-167">Tipo de faturação em valor real de despesas: <strong>Faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50245-167">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="50245-168">Tipo de faturação em valor real de material: <strong>Faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50245-168">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="50245-169">Sim</span><span class="sxs-lookup"><span data-stu-id="50245-169">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="50245-170">Sim</span><span class="sxs-lookup"><span data-stu-id="50245-170">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="50245-171">Sim</span><span class="sxs-lookup"><span data-stu-id="50245-171">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="50245-172">Apenas tarefas selecionadas</span><span class="sxs-lookup"><span data-stu-id="50245-172">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="50245-173">Faturável</span><span class="sxs-lookup"><span data-stu-id="50245-173">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="50245-174">Faturável</span><span class="sxs-lookup"><span data-stu-id="50245-174">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="50245-175">Faturável</span><span class="sxs-lookup"><span data-stu-id="50245-175">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="50245-176">Faturação num valor real de tempo: <strong>Faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50245-176">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="50245-177">Tipo de faturação em valor real de despesas: <strong>Faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50245-177">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="50245-178">Tipo de faturação em valor real de material: <strong>Faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50245-178">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="50245-179">Sim</span><span class="sxs-lookup"><span data-stu-id="50245-179">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="50245-180">Sim</span><span class="sxs-lookup"><span data-stu-id="50245-180">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="50245-181">Sim</span><span class="sxs-lookup"><span data-stu-id="50245-181">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="50245-182">Apenas tarefas selecionadas</span><span class="sxs-lookup"><span data-stu-id="50245-182">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="50245-183">
                    <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50245-183">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="50245-184">Faturável</span><span class="sxs-lookup"><span data-stu-id="50245-184">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="50245-185">Faturável</span><span class="sxs-lookup"><span data-stu-id="50245-185">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="50245-186">Faturação num valor real de tempo: <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50245-186">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="50245-187">Tipo de faturação em valor real de despesas: Faturável</span><span class="sxs-lookup"><span data-stu-id="50245-187">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="50245-188">Tipo de faturação em valor real de material: Faturável</span><span class="sxs-lookup"><span data-stu-id="50245-188">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="50245-189">Sim</span><span class="sxs-lookup"><span data-stu-id="50245-189">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="50245-190">Sim</span><span class="sxs-lookup"><span data-stu-id="50245-190">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="50245-191">Sim</span><span class="sxs-lookup"><span data-stu-id="50245-191">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="50245-192">Apenas tarefas selecionadas</span><span class="sxs-lookup"><span data-stu-id="50245-192">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="50245-193">Faturável</span><span class="sxs-lookup"><span data-stu-id="50245-193">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="50245-194">Faturável</span><span class="sxs-lookup"><span data-stu-id="50245-194">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="50245-195">
                    <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50245-195">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="50245-196">Faturação num valor real de tempo: <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50245-196">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="50245-197">Tipo de faturação em valor real de despesas: <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50245-197">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="50245-198">Tipo de faturação em valor real de material: <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50245-198">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="50245-199">Sim</span><span class="sxs-lookup"><span data-stu-id="50245-199">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="50245-200">Sim</span><span class="sxs-lookup"><span data-stu-id="50245-200">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="50245-201">Sim</span><span class="sxs-lookup"><span data-stu-id="50245-201">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="50245-202">Apenas tarefas selecionadas</span><span class="sxs-lookup"><span data-stu-id="50245-202">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="50245-203">
                    <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50245-203">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="50245-204">Faturável</span><span class="sxs-lookup"><span data-stu-id="50245-204">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="50245-205">
                    <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50245-205">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="50245-206">Faturação num valor real de tempo: <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50245-206">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="50245-207">Tipo de faturação em valor real de despesas: <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50245-207">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="50245-208">Tipo de faturação em valor real de material: <strong> Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50245-208">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="50245-209">Sim</span><span class="sxs-lookup"><span data-stu-id="50245-209">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="50245-210">Sim</span><span class="sxs-lookup"><span data-stu-id="50245-210">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="50245-211">Sim</span><span class="sxs-lookup"><span data-stu-id="50245-211">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="50245-212">Apenas tarefas selecionadas</span><span class="sxs-lookup"><span data-stu-id="50245-212">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="50245-213">
                    <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50245-213">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="50245-214">
                    <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50245-214">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="50245-215">Faturável</span><span class="sxs-lookup"><span data-stu-id="50245-215">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="50245-216">Faturação num valor real de tempo: <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50245-216">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="50245-217">Tipo de faturação em valor real de despesas: <strong> Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50245-217">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="50245-218">Tipo de faturação em valor real de material: Faturável</span><span class="sxs-lookup"><span data-stu-id="50245-218">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="50245-219">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50245-219">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="50245-220">Sim</span><span class="sxs-lookup"><span data-stu-id="50245-220">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="50245-221">Sim</span><span class="sxs-lookup"><span data-stu-id="50245-221">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="50245-222">Todo o Projeto</span><span class="sxs-lookup"><span data-stu-id="50245-222">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="50245-223">Não pode ser definido</span><span class="sxs-lookup"><span data-stu-id="50245-223">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="50245-224">
                    <strong>Faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50245-224">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="50245-225">Não pode ser definido</span><span class="sxs-lookup"><span data-stu-id="50245-225">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="50245-226">Faturação num valor real de tempo: <strong>Não disponível</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50245-226">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="50245-227">Tipo de faturação em valor real de despesas: Faturável</span><span class="sxs-lookup"><span data-stu-id="50245-227">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="50245-228">Tipo de faturação em valor real de material: Faturável</span><span class="sxs-lookup"><span data-stu-id="50245-228">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="50245-229">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50245-229">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="50245-230">Sim</span><span class="sxs-lookup"><span data-stu-id="50245-230">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="50245-231">Sim</span><span class="sxs-lookup"><span data-stu-id="50245-231">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="50245-232">Todo o Projeto</span><span class="sxs-lookup"><span data-stu-id="50245-232">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="50245-233">Não pode ser definido</span><span class="sxs-lookup"><span data-stu-id="50245-233">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="50245-234">
                    <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50245-234">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="50245-235">Não pode ser definido</span><span class="sxs-lookup"><span data-stu-id="50245-235">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="50245-236">Faturação num valor real de tempo: <strong>Não disponível</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50245-236">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="50245-237">Tipo de faturação em valor real de despesas: <strong> Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50245-237">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="50245-238">Tipo de faturação em valor real de material: Faturável</span><span class="sxs-lookup"><span data-stu-id="50245-238">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="50245-239">Sim</span><span class="sxs-lookup"><span data-stu-id="50245-239">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="50245-240">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50245-240">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="50245-241">Sim</span><span class="sxs-lookup"><span data-stu-id="50245-241">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="50245-242">Todo o Projeto</span><span class="sxs-lookup"><span data-stu-id="50245-242">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="50245-243">Faturável</span><span class="sxs-lookup"><span data-stu-id="50245-243">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="50245-244">Não pode ser definido</span><span class="sxs-lookup"><span data-stu-id="50245-244">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="50245-245">Não pode ser definido</span><span class="sxs-lookup"><span data-stu-id="50245-245">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="50245-246">Faturação num valor real de tempo: Faturável</span><span class="sxs-lookup"><span data-stu-id="50245-246">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="50245-247">Tipo de faturação em valor real de despesas:<strong> Não disponível</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50245-247">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="50245-248">Tipo de faturação em valor real de material: Faturável</span><span class="sxs-lookup"><span data-stu-id="50245-248">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="50245-249">Sim</span><span class="sxs-lookup"><span data-stu-id="50245-249">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="50245-250">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50245-250">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="50245-251">Sim</span><span class="sxs-lookup"><span data-stu-id="50245-251">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="50245-252">Todo o Projeto</span><span class="sxs-lookup"><span data-stu-id="50245-252">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="50245-253">
                    <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50245-253">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="50245-254">Não pode ser definido</span><span class="sxs-lookup"><span data-stu-id="50245-254">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="50245-255">Não pode ser definido</span><span class="sxs-lookup"><span data-stu-id="50245-255">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="50245-256">Faturação num valor real de tempo: <strong>Não faturável </strong>
                </span><span class="sxs-lookup"><span data-stu-id="50245-256">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="50245-257">Tipo de faturação em valor real de despesas:<strong> Não disponível</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50245-257">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="50245-258">Tipo de faturação em valor real de material: Faturável</span><span class="sxs-lookup"><span data-stu-id="50245-258">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="50245-259">Sim</span><span class="sxs-lookup"><span data-stu-id="50245-259">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="50245-260">Sim</span><span class="sxs-lookup"><span data-stu-id="50245-260">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="50245-261">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50245-261">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="50245-262">Todo o Projeto</span><span class="sxs-lookup"><span data-stu-id="50245-262">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="50245-263">Faturável</span><span class="sxs-lookup"><span data-stu-id="50245-263">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="50245-264">Faturável</span><span class="sxs-lookup"><span data-stu-id="50245-264">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="50245-265">Não pode ser definido</span><span class="sxs-lookup"><span data-stu-id="50245-265">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="50245-266">Faturação num valor real de tempo: Faturável</span><span class="sxs-lookup"><span data-stu-id="50245-266">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="50245-267">Tipo de faturação em valor real de despesas: Faturável</span><span class="sxs-lookup"><span data-stu-id="50245-267">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="50245-268">Tipo de faturação em valor real de material: <strong> Não disponível</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50245-268">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="50245-269">Sim</span><span class="sxs-lookup"><span data-stu-id="50245-269">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="50245-270">Sim</span><span class="sxs-lookup"><span data-stu-id="50245-270">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="50245-271">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50245-271">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="50245-272">Todo o Projeto</span><span class="sxs-lookup"><span data-stu-id="50245-272">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="50245-273">
                    <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50245-273">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="50245-274">
                    <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50245-274">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="50245-275">Não pode ser definido</span><span class="sxs-lookup"><span data-stu-id="50245-275">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="50245-276">Faturação num valor real de tempo: <strong>Não faturável </strong>
                </span><span class="sxs-lookup"><span data-stu-id="50245-276">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="50245-277">Tipo de faturação em valor real de despesas:<strong> Não faturável </strong>
                </span><span class="sxs-lookup"><span data-stu-id="50245-277">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="50245-278">Tipo de faturação em valor real de material:<strong> Não disponível</strong>
                </span><span class="sxs-lookup"><span data-stu-id="50245-278">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
