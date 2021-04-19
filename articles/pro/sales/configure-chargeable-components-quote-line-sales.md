---
title: Configurar os componentes faturáveis de uma linha de proposta
description: Este tópico fornece informações sobre a criação de componentes faturáveis e não faturáveis numa linha de proposta baseada em projetos.
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1a9e1851bd8c5a4070df2774c945d1f3eabaaa8a
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858307"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a><span data-ttu-id="0d291-103">Configurar os componentes faturáveis de uma linha de proposta</span><span class="sxs-lookup"><span data-stu-id="0d291-103">Configure the chargeable components of a quote line</span></span> 

<span data-ttu-id="0d291-104">_**Aplica-se a:** Implementação leve - negociar à faturação pró-forma, Project Operations para cenários baseados em recursos/não armazenados_</span><span class="sxs-lookup"><span data-stu-id="0d291-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="0d291-105">Uma linha de proposta baseada em projeto tem o conceito de componentes *incluídos* e componentes *faturáveis*.</span><span class="sxs-lookup"><span data-stu-id="0d291-105">A project-based quote line has the concept of *included* components and *chargeable* components.</span></span>

<span data-ttu-id="0d291-106">Os componentes incluídos estão sujeitos a:</span><span class="sxs-lookup"><span data-stu-id="0d291-106">Included components are subject to:</span></span>

  - <span data-ttu-id="0d291-107">Método de faturação e divisões de clientes</span><span class="sxs-lookup"><span data-stu-id="0d291-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="0d291-108">Limites a não exceder</span><span class="sxs-lookup"><span data-stu-id="0d291-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="0d291-109">Definições de frequência de fatura definidas na linha de proposta baseada em projeto</span><span class="sxs-lookup"><span data-stu-id="0d291-109">Invoice frequency settings defined on the project-based quote line</span></span>

<span data-ttu-id="0d291-110">Um subconjunto dos componentes incluídos pode ser marcado como faturável utilizando o campo **Tipo de Faturação**.</span><span class="sxs-lookup"><span data-stu-id="0d291-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="0d291-111">O campo **Tipo de Faturação** é um conjunto de opções que permite os seguintes valores no contexto de uma linha de proposta:</span><span class="sxs-lookup"><span data-stu-id="0d291-111">The **Billing Type** field is an option-set that allows the following values in the context of a quote line:</span></span>

  - <span data-ttu-id="0d291-112">Faturável</span><span class="sxs-lookup"><span data-stu-id="0d291-112">Chargeable</span></span>
  - <span data-ttu-id="0d291-113">Não faturável</span><span class="sxs-lookup"><span data-stu-id="0d291-113">Non-chargeable</span></span>

<span data-ttu-id="0d291-114">Os componentes faturáveis podem ser definidos nas categorias de tarefas, funções e transações.</span><span class="sxs-lookup"><span data-stu-id="0d291-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="0d291-115">A capacidade de faturação é definida nas tarefas para uma linha de proposta e aplica-se a todas as classes de transação incluídas na linha.</span><span class="sxs-lookup"><span data-stu-id="0d291-115">Chargeability is defined on the tasks for a quote line and applies to all transaction classes included on that line.</span></span> <span data-ttu-id="0d291-116">Se o campo **Incluir Tarefas** for definido para **Todo o projeto** ou for deixado em branco, o separador **Tarefas Faturáveis** não está disponível.</span><span class="sxs-lookup"><span data-stu-id="0d291-116">If the **Include Tasks** field is set to **Entire project** or left blank, the **Chargeable Tasks** tab isn't available.</span></span>

<span data-ttu-id="0d291-117">A capacidade de faturação é definida nas funções de uma linha de proposta e aplica-se apenas à classe de transação **Tempo**.</span><span class="sxs-lookup"><span data-stu-id="0d291-117">Chargeability is defined on roles for a quote line and only applies to the **Time** transaction class.</span></span> <span data-ttu-id="0d291-118">Se o campo **Incluir Tempo** estiver definido para **Não** numa linha de proposta, o separador **Funções Faturáveis** não está disponível.</span><span class="sxs-lookup"><span data-stu-id="0d291-118">If the field, **Include Time** is set to **No** on a project quote line, the **Chargeable Roles** tab isn't available.</span></span>

<span data-ttu-id="0d291-119">A capacidade de faturação é definida nas categorias de transação de uma linha de proposta e aplica-se apenas à classe de transação **Despesa**.</span><span class="sxs-lookup"><span data-stu-id="0d291-119">Chargeability is defined on transaction categories for a  quote line and only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="0d291-120">Se o campo **Incluir Despesas** estiver definido para **Não** numa linha de proposta, o separador **Categorias Faturáveis** não está disponível.</span><span class="sxs-lookup"><span data-stu-id="0d291-120">If the field, **Include Expenses** is set to **No** on a project quote line, the **Chargeable Categories** tab isn't available.</span></span>

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="0d291-121">Atualizar uma tarefa de projeto para faturável ou não faturável</span><span class="sxs-lookup"><span data-stu-id="0d291-121">Update a project task to be chargeable or non-chargeable</span></span>

<span data-ttu-id="0d291-122">Uma tarefa do projeto pode ser faturável ou não faturável no contexto de uma linha de proposta baseada em projeto específica que torna possível a seguinte configuração.</span><span class="sxs-lookup"><span data-stu-id="0d291-122">A project task can be chargeable or non-chargeable in the context of a specific project-based quote line, which makes the following setup possible.</span></span>

<span data-ttu-id="0d291-123">Se uma linha de proposta baseada em projeto inclui **Tempo** e a tarefa **T1**, a tarefa está associada à linha de proposta como faturável.</span><span class="sxs-lookup"><span data-stu-id="0d291-123">If a project-based quote line includes **Time** and the task **T1**, the task is associated to the quote line as chargeable.</span></span> <span data-ttu-id="0d291-124">Se houver uma segunda linha de proposta que inclua **Despesas**, pode associar a tarefa **T1** à linha de proposta como não faturável.</span><span class="sxs-lookup"><span data-stu-id="0d291-124">If there is a second quote line that includes **Expenses**, you can associate the **T1** task on the quote line as non-chargeable.</span></span> <span data-ttu-id="0d291-125">O resultado é que todo o tempo registado na tarefa é faturado e todas as despesas registadas na tarefa são não faturáveis.</span><span class="sxs-lookup"><span data-stu-id="0d291-125">The result is that all time recorded on the task is chargeable and all expenses recorded on the task are non-chargeable.</span></span>

<span data-ttu-id="0d291-126">O tipo de faturação de uma tarefa pode ser configurado no separador **Tarefas Faturáveis** de uma linha de proposta baseada em projeto, atualizando o campo **Tipo de Faturação** na subgrelha **Tarefas da linha de Proposta**.</span><span class="sxs-lookup"><span data-stu-id="0d291-126">A task's billing type can be configured on the **Chargeable Tasks** tab of a project-based quote line by updating the **Billing Type** field on the **Quote Line Tasks** subgrid.</span></span> <span data-ttu-id="0d291-127">Em alternativa, pode atualizar o tipo de faturação para uma tarefa de projeto no campo **Tipo de Faturação** na subgrelha na configuração de faturação da tarefa de um projeto que mostra as linhas de proposta associadas a uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="0d291-127">Alternatively, you can update the billing type for a project task in the **Billing Type** field on the subgrid on the task billing setup of a project that shows the quote lines associated to a task.</span></span>

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="0d291-128">Atualizar uma função de projeto como faturável ou não faturável</span><span class="sxs-lookup"><span data-stu-id="0d291-128">Update a role to be chargeable or non-chargeable</span></span>

<span data-ttu-id="0d291-129">Uma função pode ser faturável ou não faturável no contexto de uma linha de proposta específica baseada em projetos.</span><span class="sxs-lookup"><span data-stu-id="0d291-129">A role can be chargeable or non-chargeable in the context of a specific project-based quote line.</span></span>

<span data-ttu-id="0d291-130">O tipo de faturação de uma função pode ser configurado no separador **Funções Faturáveis** de uma linha de proposta baseada em projeto, atualizando o campo **Tipo de Faturação** na subgrelha **Funções Faturáveis**.</span><span class="sxs-lookup"><span data-stu-id="0d291-130">A role's billing type can be configured on the **Chargeable Roles** tab of a quote line by updating the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="0d291-131">Atualizar uma categoria de transação como faturável ou não faturável</span><span class="sxs-lookup"><span data-stu-id="0d291-131">Update a transaction category to be chargeable or non-chargeable</span></span>

<span data-ttu-id="0d291-132">Uma categoria de transação pode ser faturável ou não faturável numa linha de proposta específica.</span><span class="sxs-lookup"><span data-stu-id="0d291-132">A transaction category can be chargeable or non-chargeable on a specific quote line.</span></span>

<span data-ttu-id="0d291-133">O tipo de faturação de uma transação pode ser configurado no separador **Categorias Faturáveis** de uma linha de proposta baseada em projeto, atualizando o campo **Tipo de Faturação** na subgrelha **Categorias Faturáveis**.</span><span class="sxs-lookup"><span data-stu-id="0d291-133">A transaction's billing type can be configured on the **Chargeable Categories** tab of a quote line by updating the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="0d291-134">Resolver a capacidade de faturação</span><span class="sxs-lookup"><span data-stu-id="0d291-134">Resolve chargeability</span></span>
<span data-ttu-id="0d291-135">Uma estimativa ou um valor real criado para o tempo só será considerado faturável se:</span><span class="sxs-lookup"><span data-stu-id="0d291-135">An estimate or actual created for time will only be considered chargeable if:</span></span>

   - <span data-ttu-id="0d291-136">**Tempo** está incluído na linha da proposta.</span><span class="sxs-lookup"><span data-stu-id="0d291-136">**Time** is included on the quote line.</span></span>
   - <span data-ttu-id="0d291-137">**Função** é configurado como responsável na linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="0d291-137">**Role** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="0d291-138">**Tarefas incluídas** estão definidas para **Tarefas selecionadas** na linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="0d291-138">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span> 

<span data-ttu-id="0d291-139">Se estas três coisas forem verdadeiras, a **Tarefa** é também configurada como faturável.</span><span class="sxs-lookup"><span data-stu-id="0d291-139">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="0d291-140">Uma estimativa ou um valor real criado para a despesa só é considerado faturável se:</span><span class="sxs-lookup"><span data-stu-id="0d291-140">An estimate or actual created for expense is only considered chargeable if:</span></span> 

   - <span data-ttu-id="0d291-141">**Despesa** está incluído na linha da proposta.</span><span class="sxs-lookup"><span data-stu-id="0d291-141">**Expense** is included on the quote line.</span></span>
   - <span data-ttu-id="0d291-142">**Categoria de transação** é configurado como faturável na linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="0d291-142">**Transaction category** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="0d291-143">**Tarefas incluídas** estão definidas para **Tarefas selecionadas** na linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="0d291-143">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="0d291-144">Se estas três coisas forem verdadeiras, a **Tarefa** é também configurada como faturável.</span><span class="sxs-lookup"><span data-stu-id="0d291-144">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="0d291-145">Uma estimativa ou um valor real criado para o material só será considerado faturável se:</span><span class="sxs-lookup"><span data-stu-id="0d291-145">An estimate or actual created for material will only be considered chargeable if:</span></span>

   - <span data-ttu-id="0d291-146">**Materiais** está incluído na linha da proposta.</span><span class="sxs-lookup"><span data-stu-id="0d291-146">**Materials** is included on the quote line.</span></span>
   - <span data-ttu-id="0d291-147">**Tarefas incluídas** estão definidas para **Tarefas selecionadas** na linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="0d291-147">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="0d291-148">Se estas duas coisas forem verdadeiras, a **Tarefa** também deveria ser configurada como faturável.</span><span class="sxs-lookup"><span data-stu-id="0d291-148">If these two things are true, the **Task** should also be configured as chargeable.</span></span> 


<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="0d291-149">
                    <strong>Inclui Tempo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0d291-149">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="0d291-150">
                    <strong>Inclui Despesa</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="0d291-150">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="0d291-151">
                    <strong>Incluir materiais</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="0d291-151">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="0d291-152">
                    <strong>Tarefas Incluídas</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="0d291-152">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="0d291-153">
                    <strong>Função</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="0d291-153">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="0d291-154">
                    <strong>Categoria</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="0d291-154">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="0d291-155">
                    <strong>Tarefa</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="0d291-155">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="0d291-156">
                    <strong>Impacto da possível faturação</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0d291-156">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="0d291-157">Sim</span><span class="sxs-lookup"><span data-stu-id="0d291-157">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="0d291-158">Sim</span><span class="sxs-lookup"><span data-stu-id="0d291-158">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="0d291-159">Sim</span><span class="sxs-lookup"><span data-stu-id="0d291-159">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="0d291-160">Todo o Projeto</span><span class="sxs-lookup"><span data-stu-id="0d291-160">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="0d291-161">Faturável</span><span class="sxs-lookup"><span data-stu-id="0d291-161">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="0d291-162">Faturável</span><span class="sxs-lookup"><span data-stu-id="0d291-162">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="0d291-163">Não pode ser definido</span><span class="sxs-lookup"><span data-stu-id="0d291-163">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="0d291-164">Faturação num valor real de tempo: Faturável</span><span class="sxs-lookup"><span data-stu-id="0d291-164">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="0d291-165">Tipo de faturação em valor real de despesas: Faturável</span><span class="sxs-lookup"><span data-stu-id="0d291-165">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="0d291-166">Tipo de faturação em valor real de material: Faturável</span><span class="sxs-lookup"><span data-stu-id="0d291-166">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="0d291-167">Sim</span><span class="sxs-lookup"><span data-stu-id="0d291-167">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="0d291-168">Sim</span><span class="sxs-lookup"><span data-stu-id="0d291-168">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="0d291-169">Sim</span><span class="sxs-lookup"><span data-stu-id="0d291-169">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="0d291-170">Apenas tarefas selecionadas</span><span class="sxs-lookup"><span data-stu-id="0d291-170">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="0d291-171">Faturável</span><span class="sxs-lookup"><span data-stu-id="0d291-171">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="0d291-172">Faturável</span><span class="sxs-lookup"><span data-stu-id="0d291-172">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="0d291-173">Faturável</span><span class="sxs-lookup"><span data-stu-id="0d291-173">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="0d291-174">Faturação num valor real de tempo: Faturável</span><span class="sxs-lookup"><span data-stu-id="0d291-174">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="0d291-175">Tipo de faturação em valor real de despesas: Faturável</span><span class="sxs-lookup"><span data-stu-id="0d291-175">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="0d291-176">Tipo de faturação em valor real de material: Faturável</span><span class="sxs-lookup"><span data-stu-id="0d291-176">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="0d291-177">Sim</span><span class="sxs-lookup"><span data-stu-id="0d291-177">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="0d291-178">Sim</span><span class="sxs-lookup"><span data-stu-id="0d291-178">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="0d291-179">Sim</span><span class="sxs-lookup"><span data-stu-id="0d291-179">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="0d291-180">Apenas tarefas selecionadas</span><span class="sxs-lookup"><span data-stu-id="0d291-180">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="0d291-181">
                    <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0d291-181">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="0d291-182">Faturável</span><span class="sxs-lookup"><span data-stu-id="0d291-182">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="0d291-183">Faturável</span><span class="sxs-lookup"><span data-stu-id="0d291-183">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="0d291-184">Faturação num valor real de tempo: <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0d291-184">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="0d291-185">Tipo de faturação em valor real de despesas: Faturável</span><span class="sxs-lookup"><span data-stu-id="0d291-185">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="0d291-186">Tipo de faturação em valor real de material: Faturável</span><span class="sxs-lookup"><span data-stu-id="0d291-186">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="0d291-187">Sim</span><span class="sxs-lookup"><span data-stu-id="0d291-187">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="0d291-188">Sim</span><span class="sxs-lookup"><span data-stu-id="0d291-188">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="0d291-189">Sim</span><span class="sxs-lookup"><span data-stu-id="0d291-189">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="0d291-190">Apenas tarefas selecionadas</span><span class="sxs-lookup"><span data-stu-id="0d291-190">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="0d291-191">Faturável</span><span class="sxs-lookup"><span data-stu-id="0d291-191">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="0d291-192">Faturável</span><span class="sxs-lookup"><span data-stu-id="0d291-192">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="0d291-193">
                    <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0d291-193">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="0d291-194">Faturação num valor real de tempo: <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0d291-194">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="0d291-195">Tipo de faturação em valor real de despesas: <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0d291-195">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="0d291-196">Tipo de faturação em valor real de material: <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0d291-196">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="0d291-197">Sim</span><span class="sxs-lookup"><span data-stu-id="0d291-197">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="0d291-198">Sim</span><span class="sxs-lookup"><span data-stu-id="0d291-198">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="0d291-199">Sim</span><span class="sxs-lookup"><span data-stu-id="0d291-199">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="0d291-200">Apenas tarefas selecionadas</span><span class="sxs-lookup"><span data-stu-id="0d291-200">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="0d291-201">
                    <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0d291-201">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="0d291-202">Faturável</span><span class="sxs-lookup"><span data-stu-id="0d291-202">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="0d291-203">
                    <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0d291-203">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="0d291-204">Faturação num valor real de tempo: <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0d291-204">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="0d291-205">Tipo de faturação em valor real de despesas: <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0d291-205">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="0d291-206">Tipo de faturação em valor real de material: <strong> Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0d291-206">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="0d291-207">Sim</span><span class="sxs-lookup"><span data-stu-id="0d291-207">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="0d291-208">Sim</span><span class="sxs-lookup"><span data-stu-id="0d291-208">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="0d291-209">Sim</span><span class="sxs-lookup"><span data-stu-id="0d291-209">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="0d291-210">Apenas tarefas selecionadas</span><span class="sxs-lookup"><span data-stu-id="0d291-210">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="0d291-211">
                    <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0d291-211">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="0d291-212">
                    <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0d291-212">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="0d291-213">Faturável</span><span class="sxs-lookup"><span data-stu-id="0d291-213">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="0d291-214">Faturação num valor real de tempo: <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0d291-214">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="0d291-215">Tipo de faturação em valor real de despesas: <strong> Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0d291-215">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="0d291-216">Tipo de faturação em valor real de material: Faturável</span><span class="sxs-lookup"><span data-stu-id="0d291-216">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="0d291-217">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0d291-217">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="0d291-218">Sim</span><span class="sxs-lookup"><span data-stu-id="0d291-218">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="0d291-219">Sim</span><span class="sxs-lookup"><span data-stu-id="0d291-219">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="0d291-220">Todo o Projeto</span><span class="sxs-lookup"><span data-stu-id="0d291-220">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="0d291-221">Não pode ser definido</span><span class="sxs-lookup"><span data-stu-id="0d291-221">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="0d291-222">
                    <strong>Faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0d291-222">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="0d291-223">Não pode ser definido</span><span class="sxs-lookup"><span data-stu-id="0d291-223">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="0d291-224">Faturação num valor real de tempo: <strong>Não disponível</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0d291-224">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="0d291-225">Tipo de faturação em valor real de despesas: Faturável</span><span class="sxs-lookup"><span data-stu-id="0d291-225">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="0d291-226">Tipo de faturação em valor real de material: Faturável</span><span class="sxs-lookup"><span data-stu-id="0d291-226">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="0d291-227">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0d291-227">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="0d291-228">Sim</span><span class="sxs-lookup"><span data-stu-id="0d291-228">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="0d291-229">Sim</span><span class="sxs-lookup"><span data-stu-id="0d291-229">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="0d291-230">Todo o Projeto</span><span class="sxs-lookup"><span data-stu-id="0d291-230">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="0d291-231">Não pode ser definido</span><span class="sxs-lookup"><span data-stu-id="0d291-231">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="0d291-232">
                    <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0d291-232">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="0d291-233">Não pode ser definido</span><span class="sxs-lookup"><span data-stu-id="0d291-233">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="0d291-234">Faturação num valor real de tempo: <strong>Não disponível</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0d291-234">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="0d291-235">Tipo de faturação em valor real de despesas: <strong> Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0d291-235">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="0d291-236">Tipo de faturação em valor real de material: Faturável</span><span class="sxs-lookup"><span data-stu-id="0d291-236">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="0d291-237">Sim</span><span class="sxs-lookup"><span data-stu-id="0d291-237">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="0d291-238">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0d291-238">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="0d291-239">Sim</span><span class="sxs-lookup"><span data-stu-id="0d291-239">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="0d291-240">Todo o Projeto</span><span class="sxs-lookup"><span data-stu-id="0d291-240">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="0d291-241">Faturável</span><span class="sxs-lookup"><span data-stu-id="0d291-241">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="0d291-242">Não pode ser definido</span><span class="sxs-lookup"><span data-stu-id="0d291-242">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="0d291-243">Não pode ser definido</span><span class="sxs-lookup"><span data-stu-id="0d291-243">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="0d291-244">Faturação num valor real de tempo: Faturável</span><span class="sxs-lookup"><span data-stu-id="0d291-244">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="0d291-245">Tipo de faturação em valor real de despesas:<strong> Não disponível</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0d291-245">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="0d291-246">Tipo de faturação em valor real de material: Faturável</span><span class="sxs-lookup"><span data-stu-id="0d291-246">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="0d291-247">Sim</span><span class="sxs-lookup"><span data-stu-id="0d291-247">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="0d291-248">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0d291-248">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="0d291-249">Sim</span><span class="sxs-lookup"><span data-stu-id="0d291-249">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="0d291-250">Todo o Projeto</span><span class="sxs-lookup"><span data-stu-id="0d291-250">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="0d291-251">
                    <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0d291-251">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="0d291-252">Não pode ser definido</span><span class="sxs-lookup"><span data-stu-id="0d291-252">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="0d291-253">Não pode ser definido</span><span class="sxs-lookup"><span data-stu-id="0d291-253">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="0d291-254">Faturação num valor real de tempo: <strong>Não faturável </strong>
                </span><span class="sxs-lookup"><span data-stu-id="0d291-254">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="0d291-255">Tipo de faturação em valor real de despesas:<strong> Não disponível</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0d291-255">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="0d291-256">Tipo de faturação em valor real de material: Faturável</span><span class="sxs-lookup"><span data-stu-id="0d291-256">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="0d291-257">Sim</span><span class="sxs-lookup"><span data-stu-id="0d291-257">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="0d291-258">Sim</span><span class="sxs-lookup"><span data-stu-id="0d291-258">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="0d291-259">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0d291-259">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="0d291-260">Todo o Projeto</span><span class="sxs-lookup"><span data-stu-id="0d291-260">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="0d291-261">Faturável</span><span class="sxs-lookup"><span data-stu-id="0d291-261">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="0d291-262">Faturável</span><span class="sxs-lookup"><span data-stu-id="0d291-262">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="0d291-263">Não pode ser definido</span><span class="sxs-lookup"><span data-stu-id="0d291-263">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="0d291-264">Faturação num valor real de tempo: Faturável</span><span class="sxs-lookup"><span data-stu-id="0d291-264">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="0d291-265">Tipo de faturação em valor real de despesas: Faturável</span><span class="sxs-lookup"><span data-stu-id="0d291-265">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="0d291-266">Tipo de faturação em valor real de material: <strong> Não disponível</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0d291-266">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="0d291-267">Sim</span><span class="sxs-lookup"><span data-stu-id="0d291-267">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="0d291-268">Sim</span><span class="sxs-lookup"><span data-stu-id="0d291-268">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="0d291-269">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0d291-269">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="0d291-270">Todo o Projeto</span><span class="sxs-lookup"><span data-stu-id="0d291-270">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="0d291-271">
                    <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0d291-271">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="0d291-272">
                    <strong>Não faturável</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0d291-272">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="0d291-273">Não pode ser definido</span><span class="sxs-lookup"><span data-stu-id="0d291-273">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="0d291-274">Faturação num valor real de tempo: <strong>Não faturável </strong>
                </span><span class="sxs-lookup"><span data-stu-id="0d291-274">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="0d291-275">Tipo de faturação em valor real de despesas:<strong> Não faturável </strong>
                </span><span class="sxs-lookup"><span data-stu-id="0d291-275">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="0d291-276">Tipo de faturação em valor real de material:<strong> Não disponível</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0d291-276">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
