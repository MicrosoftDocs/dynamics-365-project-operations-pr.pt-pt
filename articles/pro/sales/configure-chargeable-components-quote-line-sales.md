---
title: Configurar os componentes faturáveis de uma linha de proposta
description: Este tópico fornece informações sobre a criação de componentes faturáveis e não faturáveis numa linha de proposta baseada em projetos.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c933a3800aae72624dbcbe3f06df20e5981d74d4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003780"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a><span data-ttu-id="f3a46-103">Configurar os componentes faturáveis de uma linha de proposta</span><span class="sxs-lookup"><span data-stu-id="f3a46-103">Configure the chargeable components of a quote line</span></span> 

<span data-ttu-id="f3a46-104">_**Aplica-se a:** Implementação leve - negociar à faturação pró-forma, Project Operations para cenários baseados em recursos/não armazenados_</span><span class="sxs-lookup"><span data-stu-id="f3a46-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="f3a46-105">Uma linha de proposta baseada em projeto tem o conceito de componentes *incluídos* e componentes *faturáveis*.</span><span class="sxs-lookup"><span data-stu-id="f3a46-105">A project-based quote line has the concept of *included* components and *chargeable* components.</span></span>

<span data-ttu-id="f3a46-106">Os componentes incluídos estão sujeitos a:</span><span class="sxs-lookup"><span data-stu-id="f3a46-106">Included components are subject to:</span></span>

  - <span data-ttu-id="f3a46-107">Método de faturação e divisões de clientes</span><span class="sxs-lookup"><span data-stu-id="f3a46-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="f3a46-108">Limites a não exceder</span><span class="sxs-lookup"><span data-stu-id="f3a46-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="f3a46-109">Definições de frequência de fatura definidas na linha de proposta baseada em projeto</span><span class="sxs-lookup"><span data-stu-id="f3a46-109">Invoice frequency settings defined on the project-based quote line</span></span>

<span data-ttu-id="f3a46-110">Um subconjunto dos componentes incluídos pode ser marcado como faturável utilizando o campo **Tipo de Faturação**.</span><span class="sxs-lookup"><span data-stu-id="f3a46-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="f3a46-111">O campo **Tipo de Faturação** é um conjunto de opções que permite os seguintes valores no contexto de uma linha de proposta:</span><span class="sxs-lookup"><span data-stu-id="f3a46-111">The **Billing Type** field is an option-set that allows the following values in the context of a quote line:</span></span>

  - <span data-ttu-id="f3a46-112">Faturável</span><span class="sxs-lookup"><span data-stu-id="f3a46-112">Chargeable</span></span>
  - <span data-ttu-id="f3a46-113">Não faturável</span><span class="sxs-lookup"><span data-stu-id="f3a46-113">Non-chargeable</span></span>

<span data-ttu-id="f3a46-114">Os componentes faturáveis podem ser definidos nas categorias de tarefas, funções e transações.</span><span class="sxs-lookup"><span data-stu-id="f3a46-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="f3a46-115">A capacidade de faturação é definida nas tarefas para uma linha de proposta e aplica-se a todas as classes de transação incluídas na linha.</span><span class="sxs-lookup"><span data-stu-id="f3a46-115">Chargeability is defined on the tasks for a quote line and applies to all transaction classes included on that line.</span></span> <span data-ttu-id="f3a46-116">Se o campo **Incluir Tarefas** for definido para **Todo o projeto** ou for deixado em branco, o separador **Tarefas Faturáveis** não está disponível.</span><span class="sxs-lookup"><span data-stu-id="f3a46-116">If the **Include Tasks** field is set to **Entire project** or left blank, the **Chargeable Tasks** tab isn't available.</span></span>

<span data-ttu-id="f3a46-117">A capacidade de faturação é definida nas funções de uma linha de proposta e aplica-se apenas à classe de transação **Tempo**.</span><span class="sxs-lookup"><span data-stu-id="f3a46-117">Chargeability is defined on roles for a quote line and only applies to the **Time** transaction class.</span></span> <span data-ttu-id="f3a46-118">Se o campo **Incluir Tempo** estiver definido para **Não** numa linha de proposta, o separador **Funções Faturáveis** não está disponível.</span><span class="sxs-lookup"><span data-stu-id="f3a46-118">If the field, **Include Time** is set to **No** on a project quote line, the **Chargeable Roles** tab isn't available.</span></span>

<span data-ttu-id="f3a46-119">A capacidade de faturação é definida nas categorias de transação de uma linha de proposta e aplica-se apenas à classe de transação **Despesa**.</span><span class="sxs-lookup"><span data-stu-id="f3a46-119">Chargeability is defined on transaction categories for a  quote line and only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="f3a46-120">Se o campo **Incluir Despesas** estiver definido para **Não** numa linha de proposta, o separador **Categorias Faturáveis** não está disponível.</span><span class="sxs-lookup"><span data-stu-id="f3a46-120">If the field, **Include Expenses** is set to **No** on a project quote line, the **Chargeable Categories** tab isn't available.</span></span>

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="f3a46-121">Atualizar uma tarefa de projeto para faturável ou não faturável</span><span class="sxs-lookup"><span data-stu-id="f3a46-121">Update a project task to be chargeable or non-chargeable</span></span>

<span data-ttu-id="f3a46-122">Uma tarefa do projeto pode ser faturável ou não faturável no contexto de uma linha de proposta baseada em projeto específica que torna possível a seguinte configuração.</span><span class="sxs-lookup"><span data-stu-id="f3a46-122">A project task can be chargeable or non-chargeable in the context of a specific project-based quote line, which makes the following setup possible.</span></span>

<span data-ttu-id="f3a46-123">Se uma linha de proposta baseada em projeto inclui **Tempo** e a tarefa **T1**, a tarefa está associada à linha de proposta como faturável.</span><span class="sxs-lookup"><span data-stu-id="f3a46-123">If a project-based quote line includes **Time** and the task **T1**, the task is associated to the quote line as chargeable.</span></span> <span data-ttu-id="f3a46-124">Se houver uma segunda linha de proposta que inclua **Despesas**, pode associar a tarefa **T1** à linha de proposta como não faturável.</span><span class="sxs-lookup"><span data-stu-id="f3a46-124">If there is a second quote line that includes **Expenses**, you can associate the **T1** task on the quote line as non-chargeable.</span></span> <span data-ttu-id="f3a46-125">O resultado é que todo o tempo registado na tarefa é faturado e todas as despesas registadas na tarefa são não faturáveis.</span><span class="sxs-lookup"><span data-stu-id="f3a46-125">The result is that all time recorded on the task is chargeable and all expenses recorded on the task are non-chargeable.</span></span>

<span data-ttu-id="f3a46-126">O tipo de faturação de uma tarefa pode ser configurado no separador **Tarefas Faturáveis** de uma linha de proposta baseada em projeto, atualizando o campo **Tipo de Faturação** na subgrelha **Tarefas da linha de Proposta**.</span><span class="sxs-lookup"><span data-stu-id="f3a46-126">A task's billing type can be configured on the **Chargeable Tasks** tab of a project-based quote line by updating the **Billing Type** field on the **Quote Line Tasks** subgrid.</span></span> <span data-ttu-id="f3a46-127">Em alternativa, pode atualizar o tipo de faturação para uma tarefa de projeto no campo **Tipo de Faturação** na subgrelha na configuração de faturação da tarefa de um projeto que mostra as linhas de proposta associadas a uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="f3a46-127">Alternatively, you can update the billing type for a project task in the **Billing Type** field on the subgrid on the task billing setup of a project that shows the quote lines associated to a task.</span></span>

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="f3a46-128">Atualizar uma função de projeto como faturável ou não faturável</span><span class="sxs-lookup"><span data-stu-id="f3a46-128">Update a role to be chargeable or non-chargeable</span></span>

<span data-ttu-id="f3a46-129">Uma função pode ser faturável ou não faturável no contexto de uma linha de proposta específica baseada em projetos.</span><span class="sxs-lookup"><span data-stu-id="f3a46-129">A role can be chargeable or non-chargeable in the context of a specific project-based quote line.</span></span>

<span data-ttu-id="f3a46-130">O tipo de faturação de uma função pode ser configurado no separador **Funções Faturáveis** de uma linha de proposta baseada em projeto, atualizando o campo **Tipo de Faturação** na subgrelha **Funções Faturáveis**.</span><span class="sxs-lookup"><span data-stu-id="f3a46-130">A role's billing type can be configured on the **Chargeable Roles** tab of a quote line by updating the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="f3a46-131">Atualizar uma categoria de transação como faturável ou não faturável</span><span class="sxs-lookup"><span data-stu-id="f3a46-131">Update a transaction category to be chargeable or non-chargeable</span></span>

<span data-ttu-id="f3a46-132">Uma categoria de transação pode ser faturável ou não faturável numa linha de proposta específica.</span><span class="sxs-lookup"><span data-stu-id="f3a46-132">A transaction category can be chargeable or non-chargeable on a specific quote line.</span></span>

<span data-ttu-id="f3a46-133">O tipo de faturação de uma transação pode ser configurado no separador **Categorias Faturáveis** de uma linha de proposta baseada em projeto, atualizando o campo **Tipo de Faturação** na subgrelha **Categorias Faturáveis**.</span><span class="sxs-lookup"><span data-stu-id="f3a46-133">A transaction's billing type can be configured on the **Chargeable Categories** tab of a quote line by updating the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="f3a46-134">Resolver a capacidade de faturação</span><span class="sxs-lookup"><span data-stu-id="f3a46-134">Resolve chargeability</span></span>
<span data-ttu-id="f3a46-135">Uma estimativa ou um valor real criado para o tempo só será considerado faturável se:</span><span class="sxs-lookup"><span data-stu-id="f3a46-135">An estimate or actual created for time will only be considered chargeable if:</span></span>

   - <span data-ttu-id="f3a46-136">**Tempo** está incluído na linha da proposta.</span><span class="sxs-lookup"><span data-stu-id="f3a46-136">**Time** is included on the quote line.</span></span>
   - <span data-ttu-id="f3a46-137">**Função** é configurado como responsável na linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="f3a46-137">**Role** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="f3a46-138">**Tarefas incluídas** estão definidas para **Tarefas selecionadas** na linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="f3a46-138">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span> 

<span data-ttu-id="f3a46-139">Se estas três coisas forem verdadeiras, a **Tarefa** é também configurada como faturável.</span><span class="sxs-lookup"><span data-stu-id="f3a46-139">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="f3a46-140">Uma estimativa ou um valor real criado para a despesa só é considerado faturável se:</span><span class="sxs-lookup"><span data-stu-id="f3a46-140">An estimate or actual created for expense is only considered chargeable if:</span></span> 

   - <span data-ttu-id="f3a46-141">**Despesa** está incluído na linha da proposta.</span><span class="sxs-lookup"><span data-stu-id="f3a46-141">**Expense** is included on the quote line.</span></span>
   - <span data-ttu-id="f3a46-142">**Categoria de transação** é configurado como faturável na linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="f3a46-142">**Transaction category** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="f3a46-143">**Tarefas incluídas** estão definidas para **Tarefas selecionadas** na linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="f3a46-143">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="f3a46-144">Se estas três coisas forem verdadeiras, a **Tarefa** é também configurada como faturável.</span><span class="sxs-lookup"><span data-stu-id="f3a46-144">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="f3a46-145">Uma estimativa ou um valor real criado para o material só será considerado faturável se:</span><span class="sxs-lookup"><span data-stu-id="f3a46-145">An estimate or actual created for material will only be considered chargeable if:</span></span>

   - <span data-ttu-id="f3a46-146">**Materiais** está incluído na linha da proposta.</span><span class="sxs-lookup"><span data-stu-id="f3a46-146">**Materials** is included on the quote line.</span></span>
   - <span data-ttu-id="f3a46-147">**Tarefas incluídas** estão definidas para **Tarefas selecionadas** na linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="f3a46-147">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="f3a46-148">Se estas duas coisas forem verdadeiras, a **Tarefa** também deveria ser configurada como faturável.</span><span class="sxs-lookup"><span data-stu-id="f3a46-148">If these two things are true, the **Task** should also be configured as chargeable.</span></span> 


<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="f3a46-149">
                    <strong>Inclui Tempo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f3a46-149">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="f3a46-150">
                    <strong>Inclui Despesa</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="f3a46-150">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="f3a46-151">
                    <strong>Incluir materiais</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="f3a46-151">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="f3a46-152">
                    <strong>Tarefas Incluídas</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="f3a46-152">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="f3a46-153">
                    <strong>Função</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="f3a46-153">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="f3a46-154">
                    <strong>Categoria</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="f3a46-154">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="f3a46-155">
                    <strong>Tarefa</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="f3a46-155">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="f3a46-156">
                    <strong>Impacto da possível faturação</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f3a46-156">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="f3a46-157">Sim</span><span class="sxs-lookup"><span data-stu-id="f3a46-157">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="f3a46-158">Sim</span><span class="sxs-lookup"><span data-stu-id="f3a46-158">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="f3a46-159">Sim</span><span class="sxs-lookup"><span data-stu-id="f3a46-159">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="f3a46-160">Todo o Projeto</span><span class="sxs-lookup"><span data-stu-id="f3a46-160">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="f3a46-161">Faturável</span><span class="sxs-lookup"><span data-stu-id="f3a46-161">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="f3a46-162">Faturável</span><span class="sxs-lookup"><span data-stu-id="f3a46-162">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="f3a46-163">Não pode ser definido</span><span class="sxs-lookup"><span data-stu-id="f3a46-163">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="f3a46-164">Faturação num valor real de tempo: Faturável</span><span class="sxs-lookup"><span data-stu-id="f3a46-164">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="f3a46-165">Tipo de faturação em valor real de despesas: Faturável</span><span class="sxs-lookup"><span data-stu-id="f3a46-165">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="f3a46-166">Tipo de faturação em valor real de material: Faturável</span><span class="sxs-lookup"><span data-stu-id="f3a46-166">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="f3a46-167">Sim</span><span class="sxs-lookup"><span data-stu-id="f3a46-167">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="f3a46-168">Sim</span><span class="sxs-lookup"><span data-stu-id="f3a46-168">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="f3a46-169">Sim</span><span class="sxs-lookup"><span data-stu-id="f3a46-169">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="f3a46-170">Apenas tarefas selecionadas</span><span class="sxs-lookup"><span data-stu-id="f3a46-170">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="f3a46-171">Faturável</span><span class="sxs-lookup"><span data-stu-id="f3a46-171">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="f3a46-172">Faturável</span><span class="sxs-lookup"><span data-stu-id="f3a46-172">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="f3a46-173">Faturável</span><span class="sxs-lookup"><span data-stu-id="f3a46-173">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="f3a46-174">Faturação num valor real de tempo: Faturável</span><span class="sxs-lookup"><span data-stu-id="f3a46-174">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="f3a46-175">Tipo de faturação em valor real de despesas: Faturável</span><span class="sxs-lookup"><span data-stu-id="f3a46-175">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="f3a46-176">Tipo de faturação em valor real de material: Faturável</span><span class="sxs-lookup"><span data-stu-id="f3a46-176">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="f3a46-177">Sim</span><span class="sxs-lookup"><span data-stu-id="f3a46-177">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="f3a46-178">Sim</span><span class="sxs-lookup"><span data-stu-id="f3a46-178">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="f3a46-179">Sim</span><span class="sxs-lookup"><span data-stu-id="f3a46-179">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="f3a46-180">Apenas tarefas selecionadas</span><span class="sxs-lookup"><span data-stu-id="f3a46-180">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="f3a46-181">
                    <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f3a46-181">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="f3a46-182">Faturável</span><span class="sxs-lookup"><span data-stu-id="f3a46-182">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="f3a46-183">Faturável</span><span class="sxs-lookup"><span data-stu-id="f3a46-183">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="f3a46-184">Faturação num valor real de tempo: <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f3a46-184">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="f3a46-185">Tipo de faturação em valor real de despesas: Faturável</span><span class="sxs-lookup"><span data-stu-id="f3a46-185">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="f3a46-186">Tipo de faturação em valor real de material: Faturável</span><span class="sxs-lookup"><span data-stu-id="f3a46-186">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="f3a46-187">Sim</span><span class="sxs-lookup"><span data-stu-id="f3a46-187">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="f3a46-188">Sim</span><span class="sxs-lookup"><span data-stu-id="f3a46-188">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="f3a46-189">Sim</span><span class="sxs-lookup"><span data-stu-id="f3a46-189">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="f3a46-190">Apenas tarefas selecionadas</span><span class="sxs-lookup"><span data-stu-id="f3a46-190">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="f3a46-191">Faturável</span><span class="sxs-lookup"><span data-stu-id="f3a46-191">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="f3a46-192">Faturável</span><span class="sxs-lookup"><span data-stu-id="f3a46-192">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="f3a46-193">
                    <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f3a46-193">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="f3a46-194">Faturação num valor real de tempo: <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f3a46-194">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="f3a46-195">Tipo de faturação em valor real de despesas: <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f3a46-195">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="f3a46-196">Tipo de faturação em valor real de material: <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f3a46-196">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="f3a46-197">Sim</span><span class="sxs-lookup"><span data-stu-id="f3a46-197">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="f3a46-198">Sim</span><span class="sxs-lookup"><span data-stu-id="f3a46-198">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="f3a46-199">Sim</span><span class="sxs-lookup"><span data-stu-id="f3a46-199">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="f3a46-200">Apenas tarefas selecionadas</span><span class="sxs-lookup"><span data-stu-id="f3a46-200">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="f3a46-201">
                    <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f3a46-201">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="f3a46-202">Faturável</span><span class="sxs-lookup"><span data-stu-id="f3a46-202">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="f3a46-203">
                    <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f3a46-203">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="f3a46-204">Faturação num valor real de tempo: <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f3a46-204">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="f3a46-205">Tipo de faturação em valor real de despesas: <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f3a46-205">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="f3a46-206">Tipo de faturação em valor real de material: <strong> Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f3a46-206">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="f3a46-207">Sim</span><span class="sxs-lookup"><span data-stu-id="f3a46-207">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="f3a46-208">Sim</span><span class="sxs-lookup"><span data-stu-id="f3a46-208">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="f3a46-209">Sim</span><span class="sxs-lookup"><span data-stu-id="f3a46-209">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="f3a46-210">Apenas tarefas selecionadas</span><span class="sxs-lookup"><span data-stu-id="f3a46-210">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="f3a46-211">
                    <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f3a46-211">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="f3a46-212">
                    <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f3a46-212">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="f3a46-213">Faturável</span><span class="sxs-lookup"><span data-stu-id="f3a46-213">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="f3a46-214">Faturação num valor real de tempo: <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f3a46-214">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="f3a46-215">Tipo de faturação em valor real de despesas: <strong> Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f3a46-215">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="f3a46-216">Tipo de faturação em valor real de material: Faturável</span><span class="sxs-lookup"><span data-stu-id="f3a46-216">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="f3a46-217">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f3a46-217">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="f3a46-218">Sim</span><span class="sxs-lookup"><span data-stu-id="f3a46-218">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="f3a46-219">Sim</span><span class="sxs-lookup"><span data-stu-id="f3a46-219">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="f3a46-220">Todo o Projeto</span><span class="sxs-lookup"><span data-stu-id="f3a46-220">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="f3a46-221">Não pode ser definido</span><span class="sxs-lookup"><span data-stu-id="f3a46-221">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="f3a46-222">
                    <strong>Faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f3a46-222">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="f3a46-223">Não pode ser definido</span><span class="sxs-lookup"><span data-stu-id="f3a46-223">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="f3a46-224">Faturação num valor real de tempo: <strong>Não disponível</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f3a46-224">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="f3a46-225">Tipo de faturação em valor real de despesas: Faturável</span><span class="sxs-lookup"><span data-stu-id="f3a46-225">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="f3a46-226">Tipo de faturação em valor real de material: Faturável</span><span class="sxs-lookup"><span data-stu-id="f3a46-226">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="f3a46-227">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f3a46-227">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="f3a46-228">Sim</span><span class="sxs-lookup"><span data-stu-id="f3a46-228">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="f3a46-229">Sim</span><span class="sxs-lookup"><span data-stu-id="f3a46-229">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="f3a46-230">Todo o Projeto</span><span class="sxs-lookup"><span data-stu-id="f3a46-230">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="f3a46-231">Não pode ser definido</span><span class="sxs-lookup"><span data-stu-id="f3a46-231">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="f3a46-232">
                    <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f3a46-232">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="f3a46-233">Não pode ser definido</span><span class="sxs-lookup"><span data-stu-id="f3a46-233">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="f3a46-234">Faturação num valor real de tempo: <strong>Não disponível</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f3a46-234">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="f3a46-235">Tipo de faturação em valor real de despesas: <strong> Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f3a46-235">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="f3a46-236">Tipo de faturação em valor real de material: Faturável</span><span class="sxs-lookup"><span data-stu-id="f3a46-236">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="f3a46-237">Sim</span><span class="sxs-lookup"><span data-stu-id="f3a46-237">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="f3a46-238">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f3a46-238">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="f3a46-239">Sim</span><span class="sxs-lookup"><span data-stu-id="f3a46-239">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="f3a46-240">Todo o Projeto</span><span class="sxs-lookup"><span data-stu-id="f3a46-240">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="f3a46-241">Faturável</span><span class="sxs-lookup"><span data-stu-id="f3a46-241">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="f3a46-242">Não pode ser definido</span><span class="sxs-lookup"><span data-stu-id="f3a46-242">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="f3a46-243">Não pode ser definido</span><span class="sxs-lookup"><span data-stu-id="f3a46-243">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="f3a46-244">Faturação num valor real de tempo: Faturável</span><span class="sxs-lookup"><span data-stu-id="f3a46-244">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="f3a46-245">Tipo de faturação em valor real de despesas:<strong> Não disponível</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f3a46-245">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="f3a46-246">Tipo de faturação em valor real de material: Faturável</span><span class="sxs-lookup"><span data-stu-id="f3a46-246">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="f3a46-247">Sim</span><span class="sxs-lookup"><span data-stu-id="f3a46-247">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="f3a46-248">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f3a46-248">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="f3a46-249">Sim</span><span class="sxs-lookup"><span data-stu-id="f3a46-249">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="f3a46-250">Todo o Projeto</span><span class="sxs-lookup"><span data-stu-id="f3a46-250">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="f3a46-251">
                    <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f3a46-251">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="f3a46-252">Não pode ser definido</span><span class="sxs-lookup"><span data-stu-id="f3a46-252">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="f3a46-253">Não pode ser definido</span><span class="sxs-lookup"><span data-stu-id="f3a46-253">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="f3a46-254">Faturação num valor real de tempo: <strong>Não faturável </strong>
                </span><span class="sxs-lookup"><span data-stu-id="f3a46-254">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="f3a46-255">Tipo de faturação em valor real de despesas:<strong> Não disponível</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f3a46-255">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="f3a46-256">Tipo de faturação em valor real de material: Faturável</span><span class="sxs-lookup"><span data-stu-id="f3a46-256">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="f3a46-257">Sim</span><span class="sxs-lookup"><span data-stu-id="f3a46-257">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="f3a46-258">Sim</span><span class="sxs-lookup"><span data-stu-id="f3a46-258">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="f3a46-259">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f3a46-259">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="f3a46-260">Todo o Projeto</span><span class="sxs-lookup"><span data-stu-id="f3a46-260">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="f3a46-261">Faturável</span><span class="sxs-lookup"><span data-stu-id="f3a46-261">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="f3a46-262">Faturável</span><span class="sxs-lookup"><span data-stu-id="f3a46-262">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="f3a46-263">Não pode ser definido</span><span class="sxs-lookup"><span data-stu-id="f3a46-263">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="f3a46-264">Faturação num valor real de tempo: Faturável</span><span class="sxs-lookup"><span data-stu-id="f3a46-264">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="f3a46-265">Tipo de faturação em valor real de despesas: Faturável</span><span class="sxs-lookup"><span data-stu-id="f3a46-265">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="f3a46-266">Tipo de faturação em valor real de material: <strong> Não disponível</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f3a46-266">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="f3a46-267">Sim</span><span class="sxs-lookup"><span data-stu-id="f3a46-267">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="f3a46-268">Sim</span><span class="sxs-lookup"><span data-stu-id="f3a46-268">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="f3a46-269">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f3a46-269">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="f3a46-270">Todo o Projeto</span><span class="sxs-lookup"><span data-stu-id="f3a46-270">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="f3a46-271">
                    <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f3a46-271">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="f3a46-272">
                    <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f3a46-272">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="f3a46-273">Não pode ser definido</span><span class="sxs-lookup"><span data-stu-id="f3a46-273">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="f3a46-274">Faturação num valor real de tempo: <strong>Não faturável </strong>
                </span><span class="sxs-lookup"><span data-stu-id="f3a46-274">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="f3a46-275">Tipo de faturação em valor real de despesas:<strong> Não faturável </strong>
                </span><span class="sxs-lookup"><span data-stu-id="f3a46-275">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="f3a46-276">Tipo de faturação em valor real de material:<strong> Não disponível</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f3a46-276">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
