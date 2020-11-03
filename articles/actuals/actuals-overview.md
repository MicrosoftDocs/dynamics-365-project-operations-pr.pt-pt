---
title: Valores Reais
description: Este tópico fornece informações sobre como trabalhar com valores reais no Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 93a945ffbe9c6dd998456b506b95e717ab8fbab7
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082394"
---
# <a name="actuals"></a><span data-ttu-id="d09b8-103">Valores Reais</span><span class="sxs-lookup"><span data-stu-id="d09b8-103">Actuals</span></span> 

<span data-ttu-id="d09b8-104">_**Aplica-se a:** Project Operations para cenários baseados em recursos/não armazenados_</span><span class="sxs-lookup"><span data-stu-id="d09b8-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="d09b8-105">Os valores reais são a quantidade de trabalho que foi concluída num projeto.</span><span class="sxs-lookup"><span data-stu-id="d09b8-105">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="d09b8-106">São criados como resultado de entradas de hora e despesa, e entradas de diário e faturas.</span><span class="sxs-lookup"><span data-stu-id="d09b8-106">They are created as a result of time and expense entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="d09b8-107">Envio de linhas do diário e tempo</span><span class="sxs-lookup"><span data-stu-id="d09b8-107">Journal lines and time submission</span></span>

<span data-ttu-id="d09b8-108">Para mais informações sobre a entrada de hora, consulte [Descrição geral da entrada de hora](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d09b8-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="d09b8-109">Hora e materiais</span><span class="sxs-lookup"><span data-stu-id="d09b8-109">Time and materials</span></span>

<span data-ttu-id="d09b8-110">Quando uma entrada de hora que é submetida está associada a um projeto que é mapeado para um item de contrato de tempo e materiais, o sistema cria duas linhas do diário, uma para o custo e uma para as vendas não faturadas.</span><span class="sxs-lookup"><span data-stu-id="d09b8-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="d09b8-111">Preço fixo</span><span class="sxs-lookup"><span data-stu-id="d09b8-111">Fixed price</span></span>

<span data-ttu-id="d09b8-112">Quando uma entrada de hora que é submetida está associada a um projeto que está mapeado para um item de contrato de preço fixo, o sistema cria uma linha do diário para o custo.</span><span class="sxs-lookup"><span data-stu-id="d09b8-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="d09b8-113">Preço predefinido</span><span class="sxs-lookup"><span data-stu-id="d09b8-113">Default pricing</span></span>

<span data-ttu-id="d09b8-114">A lógica para criar preços predefinidos reside na linha do diário.</span><span class="sxs-lookup"><span data-stu-id="d09b8-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="d09b8-115">Os valores do campo da entrada de hora são copiados para a linha do diário.</span><span class="sxs-lookup"><span data-stu-id="d09b8-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="d09b8-116">Estes valores incluem a data da transação, o item de contrato para o qual o projeto está mapeado e a moeda resulta na lista de preços apropriada.</span><span class="sxs-lookup"><span data-stu-id="d09b8-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="d09b8-117">Os campos que afetam os preços predefinidos, como **Função** e **Unidade Organizacional** são utilizados para determinar o preço adequado na linha do diário.</span><span class="sxs-lookup"><span data-stu-id="d09b8-117">The fields that affect default pricing, such as **Role** and **Org Unit** , are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="d09b8-118">Pode adicionar um campo personalizado na entrada de hora.</span><span class="sxs-lookup"><span data-stu-id="d09b8-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="d09b8-119">Se pretende que o valor do campo seja propagado aos valores reais, crie o campo na entidade Valores Reais e utilize mapeamentos de campos para copiar o campo a partir da entrada de hora para o valor real.</span><span class="sxs-lookup"><span data-stu-id="d09b8-119">If you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="d09b8-120">Submissão de linhas do diário e despesas básicas</span><span class="sxs-lookup"><span data-stu-id="d09b8-120">Journal lines and basic expense submission</span></span>

<span data-ttu-id="d09b8-121">Para mais informações sobre a entrada de despesa, consulte [Descrição geral da despesa](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d09b8-121">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="d09b8-122">Hora e materiais</span><span class="sxs-lookup"><span data-stu-id="d09b8-122">Time and materials</span></span>

<span data-ttu-id="d09b8-123">Quando uma entrada de despesa básica que é submetida está associada a um projeto que é mapeado para um item de contrato de tempo e materiais, o sistema cria duas linhas do diário, uma para o custo e uma para as vendas não faturadas.</span><span class="sxs-lookup"><span data-stu-id="d09b8-123">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="d09b8-124">Preço fixo</span><span class="sxs-lookup"><span data-stu-id="d09b8-124">Fixed price</span></span>

<span data-ttu-id="d09b8-125">Quando uma entrada de despesa básica que é submetida está associada a um projeto que está mapeado para um item de contrato de preço fixo, o sistema cria uma linha do diário para o custo.</span><span class="sxs-lookup"><span data-stu-id="d09b8-125">When a basic expense entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="d09b8-126">Preço predefinido</span><span class="sxs-lookup"><span data-stu-id="d09b8-126">Default pricing</span></span>

<span data-ttu-id="d09b8-127">A lógica para introduzir os preços predefinidos para as despesas baseia-se na categoria de despesa.</span><span class="sxs-lookup"><span data-stu-id="d09b8-127">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="d09b8-128">A data da transação, o item de contrato para o qual o projeto está mapeado e a moeda são utilizados para determinar a lista de preços apropriada.</span><span class="sxs-lookup"><span data-stu-id="d09b8-128">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="d09b8-129">No entanto, por predefinição, o montante que é introduzido para o preço é definido diretamente nas linhas do diário de despesas relacionadas para o custo e as vendas.</span><span class="sxs-lookup"><span data-stu-id="d09b8-129">However, by default, the amount that is entered for the price itself is set directly on the related expense journal lines for cost and sales.</span></span>

<span data-ttu-id="d09b8-130">A entrada baseada em categorias de preços predefinidos por unidade em entradas de despesa não está disponível.</span><span class="sxs-lookup"><span data-stu-id="d09b8-130">Category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="d09b8-131">Utilizar diários de entrada para registar custos</span><span class="sxs-lookup"><span data-stu-id="d09b8-131">Use entry journals to record costs</span></span>

<span data-ttu-id="d09b8-132">Poderá utilizar os diários de entrada para registar o custo ou a receita nas classes de material, taxa, hora, despesa ou imposto.</span><span class="sxs-lookup"><span data-stu-id="d09b8-132">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="d09b8-133">Os diários podem ser utilizadas para as finalidades seguintes:</span><span class="sxs-lookup"><span data-stu-id="d09b8-133">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="d09b8-134">Registe o custo real dos materiais e vendas num projeto.</span><span class="sxs-lookup"><span data-stu-id="d09b8-134">Record the actual cost of materials and sales on a project.</span></span>
- <span data-ttu-id="d09b8-135">Mova os valores reais da transação a partir de outro sistema para o Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="d09b8-135">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="d09b8-136">Registe os custos que ocorreram noutro sistema.</span><span class="sxs-lookup"><span data-stu-id="d09b8-136">Record costs that occurred in another system.</span></span> <span data-ttu-id="d09b8-137">Estes custos podem incluir os custos de aprovisionamento ou subcontratação.</span><span class="sxs-lookup"><span data-stu-id="d09b8-137">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d09b8-138">A aplicação não valida o tipo de linha de diário ou o preço relacionado que é introduzido na linha do diário.</span><span class="sxs-lookup"><span data-stu-id="d09b8-138">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="d09b8-139">Assim, só um utilizador plenamente consciente do impacto contabilístico que os valores reais têm no projeto deve utilizar diários de entrada para criar valores reais.</span><span class="sxs-lookup"><span data-stu-id="d09b8-139">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="d09b8-140">Dado o impacto deste tipo de diário, deve escolher cuidadosamente quem tem acesso para criar diários de entrada.</span><span class="sxs-lookup"><span data-stu-id="d09b8-140">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>
## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="d09b8-141">Registar os valores reais baseado nos eventos do projeto</span><span class="sxs-lookup"><span data-stu-id="d09b8-141">Record actuals based on project events</span></span>

<span data-ttu-id="d09b8-142">O Project Operations regista as transações financeiras que ocorrem durante um projeto.</span><span class="sxs-lookup"><span data-stu-id="d09b8-142">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="d09b8-143">Estas transações são registadas como reais.</span><span class="sxs-lookup"><span data-stu-id="d09b8-143">These transactions are recorded as actuals.</span></span> <span data-ttu-id="d09b8-144">As tabelas seguintes mostram os diferentes tipos de valores reais criados, dependendo do facto de o projeto ser um projeto de tempo e material ou de preço fixo, que se encontra na fase pré-venda, ou é um projeto interno.</span><span class="sxs-lookup"><span data-stu-id="d09b8-144">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="d09b8-145">O recurso pertence à mesma unidade organizacional que a unidade organizacional do projeto</span><span class="sxs-lookup"><span data-stu-id="d09b8-145">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="d09b8-146">Evento</span><span class="sxs-lookup"><span data-stu-id="d09b8-146">Event</span></span></th>
<th colspan="4"><span data-ttu-id="d09b8-147">Projeto faturável ou vendido</span><span class="sxs-lookup"><span data-stu-id="d09b8-147">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="d09b8-148">Projeto na fase pré-venda</span><span class="sxs-lookup"><span data-stu-id="d09b8-148">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="d09b8-149">Projeto interno</span><span class="sxs-lookup"><span data-stu-id="d09b8-149">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="d09b8-150">Hora e materiais</span><span class="sxs-lookup"><span data-stu-id="d09b8-150">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="d09b8-151">Preço fixo</span><span class="sxs-lookup"><span data-stu-id="d09b8-151">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="d09b8-152">Valores Reais</span><span class="sxs-lookup"><span data-stu-id="d09b8-152">Actuals</span></span></th>
<th><span data-ttu-id="d09b8-153">Moeda da transação</span><span class="sxs-lookup"><span data-stu-id="d09b8-153">Transaction currency</span></span></th>
<th><span data-ttu-id="d09b8-154">Preço fixo</span><span class="sxs-lookup"><span data-stu-id="d09b8-154">Fixed price</span></span></th>
<th><span data-ttu-id="d09b8-155">Moeda da transação</span><span class="sxs-lookup"><span data-stu-id="d09b8-155">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d09b8-156">É criada uma entrada de hora.</span><span class="sxs-lookup"><span data-stu-id="d09b8-156">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="d09b8-157">Sem atividade na entidade Valores Reais</span><span class="sxs-lookup"><span data-stu-id="d09b8-157">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d09b8-158">É submetida uma entrada de hora.</span><span class="sxs-lookup"><span data-stu-id="d09b8-158">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="d09b8-159">Sem atividade na entidade Valores Reais</span><span class="sxs-lookup"><span data-stu-id="d09b8-159">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="d09b8-160">A hora é aprovada e não ocorre nenhuma alteração ou aumento nas horas faturáveis durante a aprovação.</span><span class="sxs-lookup"><span data-stu-id="d09b8-160">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="d09b8-161">Custo real</span><span class="sxs-lookup"><span data-stu-id="d09b8-161">Cost actual</span></span></td>
<td><span data-ttu-id="d09b8-162">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="d09b8-162">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="d09b8-163">Custo real</span><span class="sxs-lookup"><span data-stu-id="d09b8-163">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="d09b8-164">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="d09b8-164">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="d09b8-165">Custo real</span><span class="sxs-lookup"><span data-stu-id="d09b8-165">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="d09b8-166">Custo real</span><span class="sxs-lookup"><span data-stu-id="d09b8-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d09b8-167">Valor real de vendas não faturadas – Faturável</span><span class="sxs-lookup"><span data-stu-id="d09b8-167">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="d09b8-168">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="d09b8-168">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="d09b8-169">A hora é aprovada e ocorre uma diminuição nas horas faturáveis durante a aprovação.</span><span class="sxs-lookup"><span data-stu-id="d09b8-169">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="d09b8-170">Custo real</span><span class="sxs-lookup"><span data-stu-id="d09b8-170">Cost actual</span></span></td>
<td><span data-ttu-id="d09b8-171">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="d09b8-171">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="d09b8-172">Custo real</span><span class="sxs-lookup"><span data-stu-id="d09b8-172">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="d09b8-173">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="d09b8-173">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="d09b8-174">Custo real</span><span class="sxs-lookup"><span data-stu-id="d09b8-174">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="d09b8-175">Custo real</span><span class="sxs-lookup"><span data-stu-id="d09b8-175">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d09b8-176">Valor real de vendas não faturadas – Faturável para a nova quantidade</span><span class="sxs-lookup"><span data-stu-id="d09b8-176">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="d09b8-177">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="d09b8-177">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d09b8-178">Valor real de vendas não faturadas – Não faturável para a diferença</span><span class="sxs-lookup"><span data-stu-id="d09b8-178">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="d09b8-179">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="d09b8-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="d09b8-180">É confirmada uma fatura e não ocorre nenhuma alteração ou aumento nas horas faturáveis.</span><span class="sxs-lookup"><span data-stu-id="d09b8-180">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="d09b8-181">Estorno de vendas não faturadas</span><span class="sxs-lookup"><span data-stu-id="d09b8-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="d09b8-182">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="d09b8-182">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="d09b8-183">Vendas faturadas para marco</span><span class="sxs-lookup"><span data-stu-id="d09b8-183">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="d09b8-184">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="d09b8-184">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="d09b8-185">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="d09b8-185">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="d09b8-186">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="d09b8-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d09b8-187">Vendas faturadas</span><span class="sxs-lookup"><span data-stu-id="d09b8-187">Billed sales</span></span></td>
<td><span data-ttu-id="d09b8-188">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="d09b8-188">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="d09b8-189">É confirmada uma fatura e ocorre uma diminuição nas horas faturáveis.</span><span class="sxs-lookup"><span data-stu-id="d09b8-189">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="d09b8-190">Estorno de vendas não faturadas</span><span class="sxs-lookup"><span data-stu-id="d09b8-190">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="d09b8-191">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="d09b8-191">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="d09b8-192">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="d09b8-192">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="d09b8-193">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="d09b8-193">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="d09b8-194">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="d09b8-194">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="d09b8-195">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="d09b8-195">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d09b8-196">Vendas faturadas – Faturável para a nova quantidade</span><span class="sxs-lookup"><span data-stu-id="d09b8-196">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="d09b8-197">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="d09b8-197">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d09b8-198">Vendas não faturadas – Não faturável para a diferença</span><span class="sxs-lookup"><span data-stu-id="d09b8-198">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="d09b8-199">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="d09b8-199">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="d09b8-200">Uma fatura é corrigida para aumentar a quantidade faturável.</span><span class="sxs-lookup"><span data-stu-id="d09b8-200">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="d09b8-201">Vendas faturadas – Estorno</span><span class="sxs-lookup"><span data-stu-id="d09b8-201">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="d09b8-202">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="d09b8-202">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="d09b8-203">Estorno de vendas faturadas para marco</span><span class="sxs-lookup"><span data-stu-id="d09b8-203">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="d09b8-204">Alterar o estado do marco de <strong>Faturado</strong> para <strong>Pronto para faturação</strong></span><span class="sxs-lookup"><span data-stu-id="d09b8-204">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="d09b8-205">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="d09b8-205">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="d09b8-206">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="d09b8-206">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="d09b8-207">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="d09b8-207">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d09b8-208">Vendas faturadas</span><span class="sxs-lookup"><span data-stu-id="d09b8-208">Billed sales</span></span></td>
<td><span data-ttu-id="d09b8-209">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="d09b8-209">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="d09b8-210">Uma fatura é corrigida para diminuir a quantidade faturável.</span><span class="sxs-lookup"><span data-stu-id="d09b8-210">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="d09b8-211">Vendas faturadas – Estorno</span><span class="sxs-lookup"><span data-stu-id="d09b8-211">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="d09b8-212">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="d09b8-212">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d09b8-213">Vendas faturadas para a nova quantidade</span><span class="sxs-lookup"><span data-stu-id="d09b8-213">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="d09b8-214">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="d09b8-214">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d09b8-215">Vendas não faturadas – Faturável para a diferença</span><span class="sxs-lookup"><span data-stu-id="d09b8-215">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="d09b8-216">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="d09b8-216">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="d09b8-217">O recurso pertence a uma unidade organizacional que difere da unidade organizacional do projeto</span><span class="sxs-lookup"><span data-stu-id="d09b8-217">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="d09b8-218">Evento</span><span class="sxs-lookup"><span data-stu-id="d09b8-218">Event</span></span></th>
<th colspan="4"><span data-ttu-id="d09b8-219">Projeto faturável ou vendido</span><span class="sxs-lookup"><span data-stu-id="d09b8-219">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="d09b8-220">Projeto na fase pré-venda</span><span class="sxs-lookup"><span data-stu-id="d09b8-220">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="d09b8-221">Projeto interno</span><span class="sxs-lookup"><span data-stu-id="d09b8-221">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="d09b8-222">Hora e materiais</span><span class="sxs-lookup"><span data-stu-id="d09b8-222">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="d09b8-223">Preço fixo</span><span class="sxs-lookup"><span data-stu-id="d09b8-223">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="d09b8-224">Valores Reais</span><span class="sxs-lookup"><span data-stu-id="d09b8-224">Actuals</span></span></th>
<th><span data-ttu-id="d09b8-225">Moeda da transação</span><span class="sxs-lookup"><span data-stu-id="d09b8-225">Transaction currency</span></span></th>
<th><span data-ttu-id="d09b8-226">Preço fixo</span><span class="sxs-lookup"><span data-stu-id="d09b8-226">Fixed price</span></span></th>
<th><span data-ttu-id="d09b8-227">Moeda da transação</span><span class="sxs-lookup"><span data-stu-id="d09b8-227">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d09b8-228">É criada uma entrada de hora.</span><span class="sxs-lookup"><span data-stu-id="d09b8-228">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="d09b8-229">Sem atividade na entidade Valores Reais</span><span class="sxs-lookup"><span data-stu-id="d09b8-229">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d09b8-230">É submetida uma entrada de hora.</span><span class="sxs-lookup"><span data-stu-id="d09b8-230">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="d09b8-231">Sem atividade na entidade Valores Reais</span><span class="sxs-lookup"><span data-stu-id="d09b8-231">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="d09b8-232">A hora é aprovada e não ocorre nenhuma alteração ou aumento nas horas faturáveis durante a aprovação.</span><span class="sxs-lookup"><span data-stu-id="d09b8-232">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="d09b8-233">Custo real</span><span class="sxs-lookup"><span data-stu-id="d09b8-233">Cost actual</span></span></td>
<td><span data-ttu-id="d09b8-234">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="d09b8-234">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="d09b8-235">Custo real</span><span class="sxs-lookup"><span data-stu-id="d09b8-235">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="d09b8-236">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="d09b8-236">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="d09b8-237">Custo real</span><span class="sxs-lookup"><span data-stu-id="d09b8-237">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="d09b8-238">Custo real</span><span class="sxs-lookup"><span data-stu-id="d09b8-238">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d09b8-239">Valor real de vendas não faturadas – Faturável</span><span class="sxs-lookup"><span data-stu-id="d09b8-239">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="d09b8-240">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="d09b8-240">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d09b8-241">Custo de unidade de atribuição de recursos</span><span class="sxs-lookup"><span data-stu-id="d09b8-241">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="d09b8-242">Moeda da unidade de atribuição de recursos</span><span class="sxs-lookup"><span data-stu-id="d09b8-242">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d09b8-243">Vendas interorganizacionais</span><span class="sxs-lookup"><span data-stu-id="d09b8-243">Interorganizational sales</span></span></td>
<td><span data-ttu-id="d09b8-244">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="d09b8-244">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="d09b8-245">A hora é aprovada e ocorre uma diminuição nas horas faturáveis durante a aprovação.</span><span class="sxs-lookup"><span data-stu-id="d09b8-245">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="d09b8-246">Custo real</span><span class="sxs-lookup"><span data-stu-id="d09b8-246">Cost actual</span></span></td>
<td><span data-ttu-id="d09b8-247">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="d09b8-247">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="d09b8-248">Custo real</span><span class="sxs-lookup"><span data-stu-id="d09b8-248">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="d09b8-249">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="d09b8-249">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="d09b8-250">Custo real</span><span class="sxs-lookup"><span data-stu-id="d09b8-250">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="d09b8-251">Custo real</span><span class="sxs-lookup"><span data-stu-id="d09b8-251">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d09b8-252">Custo de unidade de atribuição de recursos</span><span class="sxs-lookup"><span data-stu-id="d09b8-252">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="d09b8-253">Moeda da unidade de atribuição de recursos</span><span class="sxs-lookup"><span data-stu-id="d09b8-253">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d09b8-254">Vendas interorganizacionais</span><span class="sxs-lookup"><span data-stu-id="d09b8-254">Interorganizational sales</span></span></td>
<td><span data-ttu-id="d09b8-255">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="d09b8-255">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d09b8-256">Valor real de vendas não faturadas – Faturável para a nova quantidade</span><span class="sxs-lookup"><span data-stu-id="d09b8-256">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="d09b8-257">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="d09b8-257">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d09b8-258">Valor real de vendas não faturadas – Não faturável para a diferença</span><span class="sxs-lookup"><span data-stu-id="d09b8-258">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="d09b8-259">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="d09b8-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="d09b8-260">É confirmada uma fatura e não ocorre nenhuma alteração ou aumento nas horas faturáveis.</span><span class="sxs-lookup"><span data-stu-id="d09b8-260">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="d09b8-261">Estorno de vendas não faturadas</span><span class="sxs-lookup"><span data-stu-id="d09b8-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="d09b8-262">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="d09b8-262">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="d09b8-263">Vendas faturadas para marco</span><span class="sxs-lookup"><span data-stu-id="d09b8-263">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="d09b8-264">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="d09b8-264">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="d09b8-265">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="d09b8-265">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="d09b8-266">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="d09b8-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d09b8-267">Vendas faturadas</span><span class="sxs-lookup"><span data-stu-id="d09b8-267">Billed sales</span></span></td>
<td><span data-ttu-id="d09b8-268">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="d09b8-268">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="d09b8-269">É confirmada uma fatura e ocorre uma diminuição nas horas faturáveis.</span><span class="sxs-lookup"><span data-stu-id="d09b8-269">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="d09b8-270">Estorno de vendas não faturadas</span><span class="sxs-lookup"><span data-stu-id="d09b8-270">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="d09b8-271">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="d09b8-271">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="d09b8-272">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="d09b8-272">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="d09b8-273">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="d09b8-273">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="d09b8-274">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="d09b8-274">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="d09b8-275">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="d09b8-275">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d09b8-276">Vendas faturadas – Faturável para a nova quantidade</span><span class="sxs-lookup"><span data-stu-id="d09b8-276">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="d09b8-277">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="d09b8-277">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d09b8-278">Vendas não faturadas – Não faturável para a diferença</span><span class="sxs-lookup"><span data-stu-id="d09b8-278">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="d09b8-279">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="d09b8-279">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="d09b8-280">Uma fatura é corrigida para aumentar a quantidade faturável.</span><span class="sxs-lookup"><span data-stu-id="d09b8-280">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="d09b8-281">Vendas faturadas – Estorno</span><span class="sxs-lookup"><span data-stu-id="d09b8-281">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="d09b8-282">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="d09b8-282">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="d09b8-283">Estorno de vendas faturadas para marco</span><span class="sxs-lookup"><span data-stu-id="d09b8-283">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="d09b8-284">Alterar o estado do marco de <strong>Faturado</strong> para <strong>Pronto para faturação</strong></span><span class="sxs-lookup"><span data-stu-id="d09b8-284">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="d09b8-285">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="d09b8-285">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="d09b8-286">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="d09b8-286">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="d09b8-287">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="d09b8-287">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d09b8-288">Vendas faturadas</span><span class="sxs-lookup"><span data-stu-id="d09b8-288">Billed sales</span></span></td>
<td><span data-ttu-id="d09b8-289">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="d09b8-289">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="d09b8-290">Uma fatura é corrigida para diminuir a quantidade faturável.</span><span class="sxs-lookup"><span data-stu-id="d09b8-290">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="d09b8-291">Vendas faturadas – Estorno</span><span class="sxs-lookup"><span data-stu-id="d09b8-291">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="d09b8-292">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="d09b8-292">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d09b8-293">Vendas faturadas para a nova quantidade</span><span class="sxs-lookup"><span data-stu-id="d09b8-293">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="d09b8-294">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="d09b8-294">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d09b8-295">Vendas não faturadas – Faturável para a diferença</span><span class="sxs-lookup"><span data-stu-id="d09b8-295">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="d09b8-296">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="d09b8-296">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
