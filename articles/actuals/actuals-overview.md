---
title: Valores Reais
description: Esta tópico fornece informações sobre como trabalhar com valores reais no Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 6a94bd143b0d0dad2a08511a34e592a057b6d2a1
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291813"
---
# <a name="actuals"></a><span data-ttu-id="94fc4-103">Valores Reais</span><span class="sxs-lookup"><span data-stu-id="94fc4-103">Actuals</span></span> 

<span data-ttu-id="94fc4-104">_**Aplica-se a:** Project Operations para cenários baseados em recursos/não armazenados_</span><span class="sxs-lookup"><span data-stu-id="94fc4-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="94fc4-105">Os valores reais são a quantidade de trabalho que foi concluída num projeto.</span><span class="sxs-lookup"><span data-stu-id="94fc4-105">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="94fc4-106">São criados como resultado de entradas de hora e despesa, e entradas de diário e faturas.</span><span class="sxs-lookup"><span data-stu-id="94fc4-106">They are created as a result of time and expense entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="94fc4-107">Envio de linhas do diário e tempo</span><span class="sxs-lookup"><span data-stu-id="94fc4-107">Journal lines and time submission</span></span>

<span data-ttu-id="94fc4-108">Para mais informações sobre a entrada de hora, consulte [Descrição geral da entrada de hora](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="94fc4-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="94fc4-109">Hora e materiais</span><span class="sxs-lookup"><span data-stu-id="94fc4-109">Time and materials</span></span>

<span data-ttu-id="94fc4-110">Quando uma entrada de hora que é submetida está associada a um projeto que é mapeado para um item de contrato de tempo e materiais, o sistema cria duas linhas do diário, uma para o custo e uma para as vendas não faturadas.</span><span class="sxs-lookup"><span data-stu-id="94fc4-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="94fc4-111">Preço fixo</span><span class="sxs-lookup"><span data-stu-id="94fc4-111">Fixed price</span></span>

<span data-ttu-id="94fc4-112">Quando uma entrada de hora que é submetida está associada a um projeto que está mapeado para um item de contrato de preço fixo, o sistema cria uma linha do diário para o custo.</span><span class="sxs-lookup"><span data-stu-id="94fc4-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="94fc4-113">Preço predefinido</span><span class="sxs-lookup"><span data-stu-id="94fc4-113">Default pricing</span></span>

<span data-ttu-id="94fc4-114">A lógica para criar preços predefinidos reside na linha do diário.</span><span class="sxs-lookup"><span data-stu-id="94fc4-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="94fc4-115">Os valores do campo da entrada de hora são copiados para a linha do diário.</span><span class="sxs-lookup"><span data-stu-id="94fc4-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="94fc4-116">Estes valores incluem a data da transação, o item de contrato para o qual o projeto está mapeado e a moeda resulta na lista de preços apropriada.</span><span class="sxs-lookup"><span data-stu-id="94fc4-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="94fc4-117">Os campos que afetam os preços predefinidos, como **Função** e **Unidade Organizacional** são utilizados para determinar o preço adequado na linha do diário.</span><span class="sxs-lookup"><span data-stu-id="94fc4-117">The fields that affect default pricing, such as **Role** and **Org Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="94fc4-118">Pode adicionar um campo personalizado na entrada de hora.</span><span class="sxs-lookup"><span data-stu-id="94fc4-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="94fc4-119">Se pretende que o valor do campo seja propagado aos valores reais, crie o campo na entidade Valores Reais e utilize mapeamentos de campos para copiar o campo a partir da entrada de hora para o valor real.</span><span class="sxs-lookup"><span data-stu-id="94fc4-119">If you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="94fc4-120">Submissão de linhas do diário e despesas básicas</span><span class="sxs-lookup"><span data-stu-id="94fc4-120">Journal lines and basic expense submission</span></span>

<span data-ttu-id="94fc4-121">Para mais informações sobre a entrada de despesa, consulte [Descrição geral da despesa](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="94fc4-121">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="94fc4-122">Hora e materiais</span><span class="sxs-lookup"><span data-stu-id="94fc4-122">Time and materials</span></span>

<span data-ttu-id="94fc4-123">Quando uma entrada de despesa básica que é submetida está associada a um projeto que é mapeado para um item de contrato de tempo e materiais, o sistema cria duas linhas do diário, uma para o custo e uma para as vendas não faturadas.</span><span class="sxs-lookup"><span data-stu-id="94fc4-123">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="94fc4-124">Preço fixo</span><span class="sxs-lookup"><span data-stu-id="94fc4-124">Fixed price</span></span>

<span data-ttu-id="94fc4-125">Quando uma entrada de despesa básica que é submetida está associada a um projeto que está mapeado para um item de contrato de preço fixo, o sistema cria uma linha do diário para o custo.</span><span class="sxs-lookup"><span data-stu-id="94fc4-125">When a basic expense entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="94fc4-126">Preço predefinido</span><span class="sxs-lookup"><span data-stu-id="94fc4-126">Default pricing</span></span>

<span data-ttu-id="94fc4-127">A lógica para introduzir os preços predefinidos para as despesas baseia-se na categoria de despesa.</span><span class="sxs-lookup"><span data-stu-id="94fc4-127">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="94fc4-128">A data da transação, o item de contrato para o qual o projeto está mapeado e a moeda são utilizados para determinar a lista de preços apropriada.</span><span class="sxs-lookup"><span data-stu-id="94fc4-128">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="94fc4-129">No entanto, por predefinição, o montante que é introduzido para o preço é definido diretamente nas linhas do diário de despesas relacionadas para o custo e as vendas.</span><span class="sxs-lookup"><span data-stu-id="94fc4-129">However, by default, the amount that is entered for the price itself is set directly on the related expense journal lines for cost and sales.</span></span>

<span data-ttu-id="94fc4-130">A entrada baseada em categorias de preços predefinidos por unidade em entradas de despesa não está disponível.</span><span class="sxs-lookup"><span data-stu-id="94fc4-130">Category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="94fc4-131">Utilizar diários de entrada para registar custos</span><span class="sxs-lookup"><span data-stu-id="94fc4-131">Use entry journals to record costs</span></span>

<span data-ttu-id="94fc4-132">Poderá utilizar os diários de entrada para registar o custo ou a receita nas classes de material, taxa, hora, despesa ou imposto.</span><span class="sxs-lookup"><span data-stu-id="94fc4-132">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="94fc4-133">Os diários podem ser utilizadas para as finalidades seguintes:</span><span class="sxs-lookup"><span data-stu-id="94fc4-133">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="94fc4-134">Registe o custo real dos materiais e vendas num projeto.</span><span class="sxs-lookup"><span data-stu-id="94fc4-134">Record the actual cost of materials and sales on a project.</span></span>
- <span data-ttu-id="94fc4-135">Mover os valores reais da transação a partir de outro sistema para o Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="94fc4-135">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="94fc4-136">Registe os custos que ocorreram noutro sistema.</span><span class="sxs-lookup"><span data-stu-id="94fc4-136">Record costs that occurred in another system.</span></span> <span data-ttu-id="94fc4-137">Estes custos podem incluir os custos de aprovisionamento ou subcontratação.</span><span class="sxs-lookup"><span data-stu-id="94fc4-137">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="94fc4-138">A aplicação não valida o tipo de linha de diário ou o preço relacionado que é introduzido na linha do diário.</span><span class="sxs-lookup"><span data-stu-id="94fc4-138">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="94fc4-139">Assim, só um utilizador plenamente consciente do impacto contabilístico que os valores reais têm no projeto deve utilizar diários de entrada para criar valores reais.</span><span class="sxs-lookup"><span data-stu-id="94fc4-139">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="94fc4-140">Dado o impacto deste tipo de diário, deve escolher cuidadosamente quem tem acesso para criar diários de entrada.</span><span class="sxs-lookup"><span data-stu-id="94fc4-140">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>
## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="94fc4-141">Registar os valores reais baseado nos eventos do projeto</span><span class="sxs-lookup"><span data-stu-id="94fc4-141">Record actuals based on project events</span></span>

<span data-ttu-id="94fc4-142">O Project Operations regista as transações financeiras que ocorrem durante um projeto.</span><span class="sxs-lookup"><span data-stu-id="94fc4-142">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="94fc4-143">Estas transações são registadas como reais.</span><span class="sxs-lookup"><span data-stu-id="94fc4-143">These transactions are recorded as actuals.</span></span> <span data-ttu-id="94fc4-144">As tabelas seguintes mostram os diferentes tipos de valores reais criados, dependendo do facto de o projeto ser um projeto de tempo e material ou de preço fixo, que se encontra na fase pré-venda, ou é um projeto interno.</span><span class="sxs-lookup"><span data-stu-id="94fc4-144">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="94fc4-145">O recurso pertence à mesma unidade organizacional que a unidade organizacional do projeto</span><span class="sxs-lookup"><span data-stu-id="94fc4-145">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="94fc4-146">Evento</span><span class="sxs-lookup"><span data-stu-id="94fc4-146">Event</span></span></th>
<th colspan="4"><span data-ttu-id="94fc4-147">Projeto faturável ou vendido</span><span class="sxs-lookup"><span data-stu-id="94fc4-147">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="94fc4-148">Projeto na fase pré-venda</span><span class="sxs-lookup"><span data-stu-id="94fc4-148">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="94fc4-149">Projeto interno</span><span class="sxs-lookup"><span data-stu-id="94fc4-149">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="94fc4-150">Hora e materiais</span><span class="sxs-lookup"><span data-stu-id="94fc4-150">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="94fc4-151">Preço fixo</span><span class="sxs-lookup"><span data-stu-id="94fc4-151">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="94fc4-152">Valores Reais</span><span class="sxs-lookup"><span data-stu-id="94fc4-152">Actuals</span></span></th>
<th><span data-ttu-id="94fc4-153">Moeda da transação</span><span class="sxs-lookup"><span data-stu-id="94fc4-153">Transaction currency</span></span></th>
<th><span data-ttu-id="94fc4-154">Preço fixo</span><span class="sxs-lookup"><span data-stu-id="94fc4-154">Fixed price</span></span></th>
<th><span data-ttu-id="94fc4-155">Moeda da transação</span><span class="sxs-lookup"><span data-stu-id="94fc4-155">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="94fc4-156">É criada uma entrada de hora.</span><span class="sxs-lookup"><span data-stu-id="94fc4-156">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="94fc4-157">Sem atividade na entidade Valores Reais</span><span class="sxs-lookup"><span data-stu-id="94fc4-157">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94fc4-158">É submetida uma entrada de hora.</span><span class="sxs-lookup"><span data-stu-id="94fc4-158">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="94fc4-159">Sem atividade na entidade Valores Reais</span><span class="sxs-lookup"><span data-stu-id="94fc4-159">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="94fc4-160">A hora é aprovada e não ocorre nenhuma alteração ou aumento nas horas faturáveis durante a aprovação.</span><span class="sxs-lookup"><span data-stu-id="94fc4-160">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="94fc4-161">Custo real</span><span class="sxs-lookup"><span data-stu-id="94fc4-161">Cost actual</span></span></td>
<td><span data-ttu-id="94fc4-162">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="94fc4-162">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="94fc4-163">Custo real</span><span class="sxs-lookup"><span data-stu-id="94fc4-163">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="94fc4-164">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="94fc4-164">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="94fc4-165">Custo real</span><span class="sxs-lookup"><span data-stu-id="94fc4-165">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="94fc4-166">Custo real</span><span class="sxs-lookup"><span data-stu-id="94fc4-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94fc4-167">Valor real de vendas não faturadas – Faturável</span><span class="sxs-lookup"><span data-stu-id="94fc4-167">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="94fc4-168">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="94fc4-168">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="94fc4-169">A hora é aprovada e ocorre uma diminuição nas horas faturáveis durante a aprovação.</span><span class="sxs-lookup"><span data-stu-id="94fc4-169">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="94fc4-170">Custo real</span><span class="sxs-lookup"><span data-stu-id="94fc4-170">Cost actual</span></span></td>
<td><span data-ttu-id="94fc4-171">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="94fc4-171">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="94fc4-172">Custo real</span><span class="sxs-lookup"><span data-stu-id="94fc4-172">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="94fc4-173">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="94fc4-173">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="94fc4-174">Custo real</span><span class="sxs-lookup"><span data-stu-id="94fc4-174">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="94fc4-175">Custo real</span><span class="sxs-lookup"><span data-stu-id="94fc4-175">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94fc4-176">Valor real de vendas não faturadas – Faturável para a nova quantidade</span><span class="sxs-lookup"><span data-stu-id="94fc4-176">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="94fc4-177">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="94fc4-177">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94fc4-178">Valor real de vendas não faturadas – Não faturável para a diferença</span><span class="sxs-lookup"><span data-stu-id="94fc4-178">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="94fc4-179">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="94fc4-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="94fc4-180">É confirmada uma fatura e não ocorre nenhuma alteração ou aumento nas horas faturáveis.</span><span class="sxs-lookup"><span data-stu-id="94fc4-180">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="94fc4-181">Estorno de vendas não faturadas</span><span class="sxs-lookup"><span data-stu-id="94fc4-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="94fc4-182">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="94fc4-182">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="94fc4-183">Vendas faturadas para marco</span><span class="sxs-lookup"><span data-stu-id="94fc4-183">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="94fc4-184">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="94fc4-184">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="94fc4-185">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="94fc4-185">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="94fc4-186">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="94fc4-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94fc4-187">Vendas faturadas</span><span class="sxs-lookup"><span data-stu-id="94fc4-187">Billed sales</span></span></td>
<td><span data-ttu-id="94fc4-188">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="94fc4-188">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="94fc4-189">É confirmada uma fatura e ocorre uma diminuição nas horas faturáveis.</span><span class="sxs-lookup"><span data-stu-id="94fc4-189">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="94fc4-190">Estorno de vendas não faturadas</span><span class="sxs-lookup"><span data-stu-id="94fc4-190">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="94fc4-191">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="94fc4-191">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="94fc4-192">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="94fc4-192">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="94fc4-193">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="94fc4-193">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="94fc4-194">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="94fc4-194">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="94fc4-195">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="94fc4-195">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94fc4-196">Vendas faturadas – Faturável para a nova quantidade</span><span class="sxs-lookup"><span data-stu-id="94fc4-196">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="94fc4-197">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="94fc4-197">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94fc4-198">Vendas não faturadas – Não faturável para a diferença</span><span class="sxs-lookup"><span data-stu-id="94fc4-198">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="94fc4-199">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="94fc4-199">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="94fc4-200">Uma fatura é corrigida para aumentar a quantidade faturável.</span><span class="sxs-lookup"><span data-stu-id="94fc4-200">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="94fc4-201">Vendas faturadas – Estorno</span><span class="sxs-lookup"><span data-stu-id="94fc4-201">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="94fc4-202">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="94fc4-202">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="94fc4-203">Estorno de vendas faturadas para marco</span><span class="sxs-lookup"><span data-stu-id="94fc4-203">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="94fc4-204">Alterar o estado do marco de <strong>Faturado</strong> para <strong>Pronto para faturação</strong></span><span class="sxs-lookup"><span data-stu-id="94fc4-204">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="94fc4-205">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="94fc4-205">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="94fc4-206">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="94fc4-206">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="94fc4-207">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="94fc4-207">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94fc4-208">Vendas faturadas</span><span class="sxs-lookup"><span data-stu-id="94fc4-208">Billed sales</span></span></td>
<td><span data-ttu-id="94fc4-209">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="94fc4-209">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="94fc4-210">Uma fatura é corrigida para diminuir a quantidade faturável.</span><span class="sxs-lookup"><span data-stu-id="94fc4-210">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="94fc4-211">Vendas faturadas – Estorno</span><span class="sxs-lookup"><span data-stu-id="94fc4-211">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="94fc4-212">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="94fc4-212">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94fc4-213">Vendas faturadas para a nova quantidade</span><span class="sxs-lookup"><span data-stu-id="94fc4-213">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="94fc4-214">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="94fc4-214">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94fc4-215">Vendas não faturadas – Faturável para a diferença</span><span class="sxs-lookup"><span data-stu-id="94fc4-215">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="94fc4-216">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="94fc4-216">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="94fc4-217">O recurso pertence a uma unidade organizacional que difere da unidade organizacional do projeto</span><span class="sxs-lookup"><span data-stu-id="94fc4-217">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="94fc4-218">Evento</span><span class="sxs-lookup"><span data-stu-id="94fc4-218">Event</span></span></th>
<th colspan="4"><span data-ttu-id="94fc4-219">Projeto faturável ou vendido</span><span class="sxs-lookup"><span data-stu-id="94fc4-219">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="94fc4-220">Projeto na fase pré-venda</span><span class="sxs-lookup"><span data-stu-id="94fc4-220">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="94fc4-221">Projeto interno</span><span class="sxs-lookup"><span data-stu-id="94fc4-221">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="94fc4-222">Hora e materiais</span><span class="sxs-lookup"><span data-stu-id="94fc4-222">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="94fc4-223">Preço fixo</span><span class="sxs-lookup"><span data-stu-id="94fc4-223">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="94fc4-224">Valores Reais</span><span class="sxs-lookup"><span data-stu-id="94fc4-224">Actuals</span></span></th>
<th><span data-ttu-id="94fc4-225">Moeda da transação</span><span class="sxs-lookup"><span data-stu-id="94fc4-225">Transaction currency</span></span></th>
<th><span data-ttu-id="94fc4-226">Preço fixo</span><span class="sxs-lookup"><span data-stu-id="94fc4-226">Fixed price</span></span></th>
<th><span data-ttu-id="94fc4-227">Moeda da transação</span><span class="sxs-lookup"><span data-stu-id="94fc4-227">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="94fc4-228">É criada uma entrada de hora.</span><span class="sxs-lookup"><span data-stu-id="94fc4-228">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="94fc4-229">Sem atividade na entidade Valores Reais</span><span class="sxs-lookup"><span data-stu-id="94fc4-229">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94fc4-230">É submetida uma entrada de hora.</span><span class="sxs-lookup"><span data-stu-id="94fc4-230">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="94fc4-231">Sem atividade na entidade Valores Reais</span><span class="sxs-lookup"><span data-stu-id="94fc4-231">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="94fc4-232">A hora é aprovada e não ocorre nenhuma alteração ou aumento nas horas faturáveis durante a aprovação.</span><span class="sxs-lookup"><span data-stu-id="94fc4-232">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="94fc4-233">Custo real</span><span class="sxs-lookup"><span data-stu-id="94fc4-233">Cost actual</span></span></td>
<td><span data-ttu-id="94fc4-234">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="94fc4-234">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="94fc4-235">Custo real</span><span class="sxs-lookup"><span data-stu-id="94fc4-235">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="94fc4-236">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="94fc4-236">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="94fc4-237">Custo real</span><span class="sxs-lookup"><span data-stu-id="94fc4-237">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="94fc4-238">Custo real</span><span class="sxs-lookup"><span data-stu-id="94fc4-238">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94fc4-239">Valor real de vendas não faturadas – Faturável</span><span class="sxs-lookup"><span data-stu-id="94fc4-239">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="94fc4-240">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="94fc4-240">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94fc4-241">Custo de unidade de atribuição de recursos</span><span class="sxs-lookup"><span data-stu-id="94fc4-241">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="94fc4-242">Moeda da unidade de atribuição de recursos</span><span class="sxs-lookup"><span data-stu-id="94fc4-242">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94fc4-243">Vendas interorganizacionais</span><span class="sxs-lookup"><span data-stu-id="94fc4-243">Interorganizational sales</span></span></td>
<td><span data-ttu-id="94fc4-244">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="94fc4-244">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="94fc4-245">A hora é aprovada e ocorre uma diminuição nas horas faturáveis durante a aprovação.</span><span class="sxs-lookup"><span data-stu-id="94fc4-245">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="94fc4-246">Custo real</span><span class="sxs-lookup"><span data-stu-id="94fc4-246">Cost actual</span></span></td>
<td><span data-ttu-id="94fc4-247">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="94fc4-247">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="94fc4-248">Custo real</span><span class="sxs-lookup"><span data-stu-id="94fc4-248">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="94fc4-249">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="94fc4-249">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="94fc4-250">Custo real</span><span class="sxs-lookup"><span data-stu-id="94fc4-250">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="94fc4-251">Custo real</span><span class="sxs-lookup"><span data-stu-id="94fc4-251">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94fc4-252">Custo de unidade de atribuição de recursos</span><span class="sxs-lookup"><span data-stu-id="94fc4-252">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="94fc4-253">Moeda da unidade de atribuição de recursos</span><span class="sxs-lookup"><span data-stu-id="94fc4-253">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94fc4-254">Vendas interorganizacionais</span><span class="sxs-lookup"><span data-stu-id="94fc4-254">Interorganizational sales</span></span></td>
<td><span data-ttu-id="94fc4-255">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="94fc4-255">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94fc4-256">Valor real de vendas não faturadas – Faturável para a nova quantidade</span><span class="sxs-lookup"><span data-stu-id="94fc4-256">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="94fc4-257">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="94fc4-257">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94fc4-258">Valor real de vendas não faturadas – Não faturável para a diferença</span><span class="sxs-lookup"><span data-stu-id="94fc4-258">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="94fc4-259">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="94fc4-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="94fc4-260">É confirmada uma fatura e não ocorre nenhuma alteração ou aumento nas horas faturáveis.</span><span class="sxs-lookup"><span data-stu-id="94fc4-260">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="94fc4-261">Estorno de vendas não faturadas</span><span class="sxs-lookup"><span data-stu-id="94fc4-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="94fc4-262">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="94fc4-262">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="94fc4-263">Vendas faturadas para marco</span><span class="sxs-lookup"><span data-stu-id="94fc4-263">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="94fc4-264">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="94fc4-264">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="94fc4-265">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="94fc4-265">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="94fc4-266">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="94fc4-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94fc4-267">Vendas faturadas</span><span class="sxs-lookup"><span data-stu-id="94fc4-267">Billed sales</span></span></td>
<td><span data-ttu-id="94fc4-268">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="94fc4-268">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="94fc4-269">É confirmada uma fatura e ocorre uma diminuição nas horas faturáveis.</span><span class="sxs-lookup"><span data-stu-id="94fc4-269">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="94fc4-270">Estorno de vendas não faturadas</span><span class="sxs-lookup"><span data-stu-id="94fc4-270">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="94fc4-271">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="94fc4-271">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="94fc4-272">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="94fc4-272">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="94fc4-273">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="94fc4-273">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="94fc4-274">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="94fc4-274">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="94fc4-275">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="94fc4-275">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94fc4-276">Vendas faturadas – Faturável para a nova quantidade</span><span class="sxs-lookup"><span data-stu-id="94fc4-276">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="94fc4-277">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="94fc4-277">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94fc4-278">Vendas não faturadas – Não faturável para a diferença</span><span class="sxs-lookup"><span data-stu-id="94fc4-278">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="94fc4-279">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="94fc4-279">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="94fc4-280">Uma fatura é corrigida para aumentar a quantidade faturável.</span><span class="sxs-lookup"><span data-stu-id="94fc4-280">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="94fc4-281">Vendas faturadas – Estorno</span><span class="sxs-lookup"><span data-stu-id="94fc4-281">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="94fc4-282">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="94fc4-282">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="94fc4-283">Estorno de vendas faturadas para marco</span><span class="sxs-lookup"><span data-stu-id="94fc4-283">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="94fc4-284">Alterar o estado do marco de <strong>Faturado</strong> para <strong>Pronto para faturação</strong></span><span class="sxs-lookup"><span data-stu-id="94fc4-284">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="94fc4-285">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="94fc4-285">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="94fc4-286">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="94fc4-286">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="94fc4-287">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="94fc4-287">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94fc4-288">Vendas faturadas</span><span class="sxs-lookup"><span data-stu-id="94fc4-288">Billed sales</span></span></td>
<td><span data-ttu-id="94fc4-289">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="94fc4-289">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="94fc4-290">Uma fatura é corrigida para diminuir a quantidade faturável.</span><span class="sxs-lookup"><span data-stu-id="94fc4-290">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="94fc4-291">Vendas faturadas – Estorno</span><span class="sxs-lookup"><span data-stu-id="94fc4-291">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="94fc4-292">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="94fc4-292">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94fc4-293">Vendas faturadas para a nova quantidade</span><span class="sxs-lookup"><span data-stu-id="94fc4-293">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="94fc4-294">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="94fc4-294">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="94fc4-295">Vendas não faturadas – Faturável para a diferença</span><span class="sxs-lookup"><span data-stu-id="94fc4-295">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="94fc4-296">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="94fc4-296">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]