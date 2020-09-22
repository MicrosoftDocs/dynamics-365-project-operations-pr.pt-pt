---
title: Valores Reais
description: Este tópico fornece informações sobre os valores reais do projeto.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 44c6e85f-5b21-4e24-999c-15a2f065d977
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8291e0eb8531e8e9690368675f333c44b6e92e48
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754598"
---
# <a name="actuals"></a><span data-ttu-id="f67c7-103">Valores Reais</span><span class="sxs-lookup"><span data-stu-id="f67c7-103">Actuals</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="f67c7-104">Os valores reais são a quantidade de trabalho que foi concluída num projeto.</span><span class="sxs-lookup"><span data-stu-id="f67c7-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="f67c7-105">Os valores reais do projeto podem ser novamente rastreados para os documentos de origem.</span><span class="sxs-lookup"><span data-stu-id="f67c7-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="f67c7-106">Estes documentos de origem incluem horas, despesas e entradas de diário, além de faturas.</span><span class="sxs-lookup"><span data-stu-id="f67c7-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Como os valores reais do projeto são rastreados para os documentos de origem](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="f67c7-108">Submeter uma entrada de tempo</span><span class="sxs-lookup"><span data-stu-id="f67c7-108">Submitting a time entry</span></span>

<span data-ttu-id="f67c7-109">No PSA, quando é submetida uma entrada de tempo para um projeto que está mapeado para um item de contrato de hora e material, são criadas duas linhas do diário.</span><span class="sxs-lookup"><span data-stu-id="f67c7-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="f67c7-110">Uma linha é para o custo e a outra linha é para as vendas não faturadas.</span><span class="sxs-lookup"><span data-stu-id="f67c7-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="f67c7-111">Quando é submetida uma entrada de tempo para um projeto que está mapeado para um item de contrato de preço fixo, é criada uma linha do diário apenas para o custo.</span><span class="sxs-lookup"><span data-stu-id="f67c7-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="f67c7-112">A lógica para a introdução de preços predefinidos reside na linha do diário.</span><span class="sxs-lookup"><span data-stu-id="f67c7-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="f67c7-113">Todos os valores de campo de uma entrada de tempo são copiados para a linha do diário.</span><span class="sxs-lookup"><span data-stu-id="f67c7-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="f67c7-114">Estes campos incluem a data da transação, o item de contrato para o qual o projeto está mapeado e a moeda resulta na lista de preços apropriada.</span><span class="sxs-lookup"><span data-stu-id="f67c7-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="f67c7-115">Os campos que afetam os preços predefinidos, como **Função** e **Unidade Organizacional** fazem com que seja introduzido um preço apropriado por predefinição na linha do diário.</span><span class="sxs-lookup"><span data-stu-id="f67c7-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="f67c7-116">Se adicionar um campo personalizado à entrada de tempo e pretender que o valor do campo seja propagado aos valores reais, crie o campo na entidade Valores Reais e utilize mapeamentos de campos para copiar o campo a partir da entrada de tempo para o valor real.</span><span class="sxs-lookup"><span data-stu-id="f67c7-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="f67c7-117">Submeter uma entrada de despesa</span><span class="sxs-lookup"><span data-stu-id="f67c7-117">Submitting an expense entry</span></span>

<span data-ttu-id="f67c7-118">No PSA, quando é submetida uma entrada de despesa para um projeto que está mapeado para um item de contrato de hora e material, são criadas duas linhas do diário.</span><span class="sxs-lookup"><span data-stu-id="f67c7-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="f67c7-119">Uma linha é para o custo e a outra linha é para as vendas não faturadas.</span><span class="sxs-lookup"><span data-stu-id="f67c7-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="f67c7-120">Quando é submetida uma entrada de despesa para um projeto que está mapeado para um item de contrato de preço fixo, é criada uma linha do diário apenas para o custo.</span><span class="sxs-lookup"><span data-stu-id="f67c7-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="f67c7-121">A lógica para a entrada de preços predefinidos para despesas é baseada na categoria de despesa que é selecionada na página **Entrada de despesa**,</span><span class="sxs-lookup"><span data-stu-id="f67c7-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="f67c7-122">A data da transação, o item de contrato para o qual o projeto está mapeado e a moeda são utilizados para determinar a lista de preços apropriada.</span><span class="sxs-lookup"><span data-stu-id="f67c7-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="f67c7-123">No entanto, para o preço propriamente dito, o montante introduzido pelo utilizador é definido diretamente nas linhas do diário de despesas relacionadas para o custo e as vendas, por predefinição.</span><span class="sxs-lookup"><span data-stu-id="f67c7-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="f67c7-124">Na versão atual do PSA, a entrada baseada em categorias de preços predefinidos por unidade em entradas de despesa não está disponível.</span><span class="sxs-lookup"><span data-stu-id="f67c7-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-journals-to-record-costs"></a><span data-ttu-id="f67c7-125">Utilizar diários para registar custos</span><span class="sxs-lookup"><span data-stu-id="f67c7-125">Using journals to record costs</span></span>

<span data-ttu-id="f67c7-126">Em PSA, os diários permitem-lhe registar o custo ou a receita nas classes de material, taxa, hora, despesa ou imposto.</span><span class="sxs-lookup"><span data-stu-id="f67c7-126">In PSA, journals let you record cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="f67c7-127">Um diário tem um cabeçalho, linhas e uma ação de **Confirmação**.</span><span class="sxs-lookup"><span data-stu-id="f67c7-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="f67c7-128">Seguem-se alguns cenários em que poderá utilizar um diário:</span><span class="sxs-lookup"><span data-stu-id="f67c7-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="f67c7-129">Tem de registar os custos reais de materiais e as vendas num projeto.</span><span class="sxs-lookup"><span data-stu-id="f67c7-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="f67c7-130">Tem de mover os valores reais da transação a partir de outro sistema para o PSA.</span><span class="sxs-lookup"><span data-stu-id="f67c7-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="f67c7-131">Tem de registar os custos que ocorreram noutro sistema, tal como os custos de aprovisionamento ou subcontratação.</span><span class="sxs-lookup"><span data-stu-id="f67c7-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="f67c7-132">Registar valores reais com base em eventos de projeto</span><span class="sxs-lookup"><span data-stu-id="f67c7-132">Recording actuals based on project events</span></span>

<span data-ttu-id="f67c7-133">O PSA regista as transações financeiras que ocorrem durante um projeto.</span><span class="sxs-lookup"><span data-stu-id="f67c7-133">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="f67c7-134">Estas transações são registadas como **reais**.</span><span class="sxs-lookup"><span data-stu-id="f67c7-134">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="f67c7-135">As tabelas seguintes mostram os diferentes tipos de valores reais criados, dependendo do facto de o projeto ser um projeto de tempo e material ou de preço fixo, que se encontra na fase pré-venda, ou é um projeto interno.</span><span class="sxs-lookup"><span data-stu-id="f67c7-135">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="f67c7-136">**O recurso pertence à mesma unidade organizacional que a unidade organizacional do projeto**</span><span class="sxs-lookup"><span data-stu-id="f67c7-136">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="f67c7-137">Evento</span><span class="sxs-lookup"><span data-stu-id="f67c7-137">Event</span></span></th>
<th colspan="4"><span data-ttu-id="f67c7-138">Projeto faturável ou vendido</span><span class="sxs-lookup"><span data-stu-id="f67c7-138">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="f67c7-139">Projeto na fase pré-venda</span><span class="sxs-lookup"><span data-stu-id="f67c7-139">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="f67c7-140">Projeto interno</span><span class="sxs-lookup"><span data-stu-id="f67c7-140">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="f67c7-141">Hora e materiais</span><span class="sxs-lookup"><span data-stu-id="f67c7-141">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="f67c7-142">Preço fixo</span><span class="sxs-lookup"><span data-stu-id="f67c7-142">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="f67c7-143">Valores Reais</span><span class="sxs-lookup"><span data-stu-id="f67c7-143">Actuals</span></span></th>
<th><span data-ttu-id="f67c7-144">Moeda da transação</span><span class="sxs-lookup"><span data-stu-id="f67c7-144">Transaction currency</span></span></th>
<th><span data-ttu-id="f67c7-145">Preço fixo</span><span class="sxs-lookup"><span data-stu-id="f67c7-145">Fixed price</span></span></th>
<th><span data-ttu-id="f67c7-146">Moeda da transação</span><span class="sxs-lookup"><span data-stu-id="f67c7-146">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f67c7-147">É criada uma entrada de tempo.</span><span class="sxs-lookup"><span data-stu-id="f67c7-147">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="f67c7-148">Sem atividade na entidade Valores Reais</span><span class="sxs-lookup"><span data-stu-id="f67c7-148">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f67c7-149">É submetida uma entrada de tempo.</span><span class="sxs-lookup"><span data-stu-id="f67c7-149">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="f67c7-150">Sem atividade na entidade Valores Reais</span><span class="sxs-lookup"><span data-stu-id="f67c7-150">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="f67c7-151">A hora é aprovada e não ocorre nenhuma alteração ou aumento nas horas faturáveis durante a aprovação.</span><span class="sxs-lookup"><span data-stu-id="f67c7-151">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="f67c7-152">Custo real</span><span class="sxs-lookup"><span data-stu-id="f67c7-152">Cost actual</span></span></td>
<td><span data-ttu-id="f67c7-153">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="f67c7-153">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="f67c7-154">Custo real</span><span class="sxs-lookup"><span data-stu-id="f67c7-154">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="f67c7-155">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="f67c7-155">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="f67c7-156">Custo real</span><span class="sxs-lookup"><span data-stu-id="f67c7-156">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="f67c7-157">Custo real</span><span class="sxs-lookup"><span data-stu-id="f67c7-157">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f67c7-158">Valor real de vendas não faturadas – Faturável</span><span class="sxs-lookup"><span data-stu-id="f67c7-158">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="f67c7-159">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="f67c7-159">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="f67c7-160">A hora é aprovada e ocorre uma diminuição nas horas faturáveis durante a aprovação.</span><span class="sxs-lookup"><span data-stu-id="f67c7-160">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="f67c7-161">Custo real</span><span class="sxs-lookup"><span data-stu-id="f67c7-161">Cost actual</span></span></td>
<td><span data-ttu-id="f67c7-162">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="f67c7-162">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="f67c7-163">Custo real</span><span class="sxs-lookup"><span data-stu-id="f67c7-163">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="f67c7-164">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="f67c7-164">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="f67c7-165">Custo real</span><span class="sxs-lookup"><span data-stu-id="f67c7-165">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="f67c7-166">Custo real</span><span class="sxs-lookup"><span data-stu-id="f67c7-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f67c7-167">Valor real de vendas não faturadas – Faturável para a nova quantidade</span><span class="sxs-lookup"><span data-stu-id="f67c7-167">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="f67c7-168">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="f67c7-168">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f67c7-169">Valor real de vendas não faturadas – Não faturável para a diferença</span><span class="sxs-lookup"><span data-stu-id="f67c7-169">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="f67c7-170">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="f67c7-170">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="f67c7-171">É confirmada uma fatura e não ocorre nenhuma alteração ou aumento nas horas faturáveis.</span><span class="sxs-lookup"><span data-stu-id="f67c7-171">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="f67c7-172">Estorno de vendas não faturadas</span><span class="sxs-lookup"><span data-stu-id="f67c7-172">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="f67c7-173">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="f67c7-173">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="f67c7-174">Vendas faturadas para marco</span><span class="sxs-lookup"><span data-stu-id="f67c7-174">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="f67c7-175">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="f67c7-175">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="f67c7-176">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="f67c7-176">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="f67c7-177">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="f67c7-177">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f67c7-178">Vendas faturadas</span><span class="sxs-lookup"><span data-stu-id="f67c7-178">Billed sales</span></span></td>
<td><span data-ttu-id="f67c7-179">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="f67c7-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="f67c7-180">É confirmada uma fatura e ocorre uma diminuição nas horas faturáveis.</span><span class="sxs-lookup"><span data-stu-id="f67c7-180">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="f67c7-181">Estorno de vendas não faturadas</span><span class="sxs-lookup"><span data-stu-id="f67c7-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="f67c7-182">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="f67c7-182">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="f67c7-183">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="f67c7-183">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="f67c7-184">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="f67c7-184">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="f67c7-185">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="f67c7-185">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="f67c7-186">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="f67c7-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f67c7-187">Vendas faturadas – Faturável para a nova quantidade</span><span class="sxs-lookup"><span data-stu-id="f67c7-187">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="f67c7-188">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="f67c7-188">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f67c7-189">Vendas não faturadas – Não faturável para a diferença</span><span class="sxs-lookup"><span data-stu-id="f67c7-189">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="f67c7-190">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="f67c7-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="f67c7-191">Uma fatura é corrigida para aumentar a quantidade faturável.</span><span class="sxs-lookup"><span data-stu-id="f67c7-191">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="f67c7-192">Vendas faturadas – Estorno</span><span class="sxs-lookup"><span data-stu-id="f67c7-192">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="f67c7-193">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="f67c7-193">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="f67c7-194">Estorno de vendas faturadas para marco</span><span class="sxs-lookup"><span data-stu-id="f67c7-194">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="f67c7-195">Alterar o estado do marco de <strong>Faturado</strong> para <strong>Pronto para faturação</strong></span><span class="sxs-lookup"><span data-stu-id="f67c7-195">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="f67c7-196">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="f67c7-196">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="f67c7-197">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="f67c7-197">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="f67c7-198">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="f67c7-198">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f67c7-199">Vendas faturadas</span><span class="sxs-lookup"><span data-stu-id="f67c7-199">Billed sales</span></span></td>
<td><span data-ttu-id="f67c7-200">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="f67c7-200">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="f67c7-201">Uma fatura é corrigida para diminuir a quantidade faturável.</span><span class="sxs-lookup"><span data-stu-id="f67c7-201">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="f67c7-202">Vendas faturadas – Estorno</span><span class="sxs-lookup"><span data-stu-id="f67c7-202">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="f67c7-203">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="f67c7-203">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f67c7-204">Vendas faturadas para a nova quantidade</span><span class="sxs-lookup"><span data-stu-id="f67c7-204">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="f67c7-205">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="f67c7-205">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f67c7-206">Vendas não faturadas – Faturável para a diferença</span><span class="sxs-lookup"><span data-stu-id="f67c7-206">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="f67c7-207">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="f67c7-207">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f67c7-208">**O recurso pertence a uma unidade organizacional que difere da unidade organizacional do projeto**</span><span class="sxs-lookup"><span data-stu-id="f67c7-208">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="f67c7-209">Evento</span><span class="sxs-lookup"><span data-stu-id="f67c7-209">Event</span></span></th>
<th colspan="4"><span data-ttu-id="f67c7-210">Projeto faturável ou vendido</span><span class="sxs-lookup"><span data-stu-id="f67c7-210">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="f67c7-211">Projeto na fase pré-venda</span><span class="sxs-lookup"><span data-stu-id="f67c7-211">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="f67c7-212">Projeto interno</span><span class="sxs-lookup"><span data-stu-id="f67c7-212">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="f67c7-213">Hora e materiais</span><span class="sxs-lookup"><span data-stu-id="f67c7-213">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="f67c7-214">Preço fixo</span><span class="sxs-lookup"><span data-stu-id="f67c7-214">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="f67c7-215">Valores Reais</span><span class="sxs-lookup"><span data-stu-id="f67c7-215">Actuals</span></span></th>
<th><span data-ttu-id="f67c7-216">Moeda da transação</span><span class="sxs-lookup"><span data-stu-id="f67c7-216">Transaction currency</span></span></th>
<th><span data-ttu-id="f67c7-217">Preço fixo</span><span class="sxs-lookup"><span data-stu-id="f67c7-217">Fixed price</span></span></th>
<th><span data-ttu-id="f67c7-218">Moeda da transação</span><span class="sxs-lookup"><span data-stu-id="f67c7-218">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f67c7-219">É criada uma entrada de tempo.</span><span class="sxs-lookup"><span data-stu-id="f67c7-219">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="f67c7-220">Sem atividade na entidade Valores Reais</span><span class="sxs-lookup"><span data-stu-id="f67c7-220">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f67c7-221">É submetida uma entrada de tempo.</span><span class="sxs-lookup"><span data-stu-id="f67c7-221">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="f67c7-222">Sem atividade na entidade Valores Reais</span><span class="sxs-lookup"><span data-stu-id="f67c7-222">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="f67c7-223">A hora é aprovada e não ocorre nenhuma alteração ou aumento nas horas faturáveis durante a aprovação.</span><span class="sxs-lookup"><span data-stu-id="f67c7-223">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="f67c7-224">Custo real</span><span class="sxs-lookup"><span data-stu-id="f67c7-224">Cost actual</span></span></td>
<td><span data-ttu-id="f67c7-225">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="f67c7-225">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="f67c7-226">Custo real</span><span class="sxs-lookup"><span data-stu-id="f67c7-226">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="f67c7-227">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="f67c7-227">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="f67c7-228">Custo real</span><span class="sxs-lookup"><span data-stu-id="f67c7-228">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="f67c7-229">Custo real</span><span class="sxs-lookup"><span data-stu-id="f67c7-229">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f67c7-230">Valor real de vendas não faturadas – Faturável</span><span class="sxs-lookup"><span data-stu-id="f67c7-230">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="f67c7-231">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="f67c7-231">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f67c7-232">Custo de unidade de atribuição de recursos</span><span class="sxs-lookup"><span data-stu-id="f67c7-232">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="f67c7-233">Moeda da unidade de atribuição de recursos</span><span class="sxs-lookup"><span data-stu-id="f67c7-233">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f67c7-234">Vendas interorganizacionais</span><span class="sxs-lookup"><span data-stu-id="f67c7-234">Interorganizational sales</span></span></td>
<td><span data-ttu-id="f67c7-235">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="f67c7-235">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="f67c7-236">A hora é aprovada e ocorre uma diminuição nas horas faturáveis durante a aprovação.</span><span class="sxs-lookup"><span data-stu-id="f67c7-236">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="f67c7-237">Custo real</span><span class="sxs-lookup"><span data-stu-id="f67c7-237">Cost actual</span></span></td>
<td><span data-ttu-id="f67c7-238">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="f67c7-238">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="f67c7-239">Custo real</span><span class="sxs-lookup"><span data-stu-id="f67c7-239">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="f67c7-240">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="f67c7-240">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="f67c7-241">Custo real</span><span class="sxs-lookup"><span data-stu-id="f67c7-241">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="f67c7-242">Custo real</span><span class="sxs-lookup"><span data-stu-id="f67c7-242">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f67c7-243">Custo de unidade de atribuição de recursos</span><span class="sxs-lookup"><span data-stu-id="f67c7-243">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="f67c7-244">Moeda da unidade de atribuição de recursos</span><span class="sxs-lookup"><span data-stu-id="f67c7-244">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f67c7-245">Vendas interorganizacionais</span><span class="sxs-lookup"><span data-stu-id="f67c7-245">Interorganizational sales</span></span></td>
<td><span data-ttu-id="f67c7-246">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="f67c7-246">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f67c7-247">Valor real de vendas não faturadas – Faturável para a nova quantidade</span><span class="sxs-lookup"><span data-stu-id="f67c7-247">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="f67c7-248">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="f67c7-248">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f67c7-249">Valor real de vendas não faturadas – Não faturável para a diferença</span><span class="sxs-lookup"><span data-stu-id="f67c7-249">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="f67c7-250">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="f67c7-250">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="f67c7-251">É confirmada uma fatura e não ocorre nenhuma alteração ou aumento nas horas faturáveis.</span><span class="sxs-lookup"><span data-stu-id="f67c7-251">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="f67c7-252">Estorno de vendas não faturadas</span><span class="sxs-lookup"><span data-stu-id="f67c7-252">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="f67c7-253">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="f67c7-253">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="f67c7-254">Vendas faturadas para marco</span><span class="sxs-lookup"><span data-stu-id="f67c7-254">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="f67c7-255">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="f67c7-255">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="f67c7-256">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="f67c7-256">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="f67c7-257">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="f67c7-257">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f67c7-258">Vendas faturadas</span><span class="sxs-lookup"><span data-stu-id="f67c7-258">Billed sales</span></span></td>
<td><span data-ttu-id="f67c7-259">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="f67c7-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="f67c7-260">É confirmada uma fatura e ocorre uma diminuição nas horas faturáveis.</span><span class="sxs-lookup"><span data-stu-id="f67c7-260">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="f67c7-261">Estorno de vendas não faturadas</span><span class="sxs-lookup"><span data-stu-id="f67c7-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="f67c7-262">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="f67c7-262">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="f67c7-263">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="f67c7-263">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="f67c7-264">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="f67c7-264">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="f67c7-265">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="f67c7-265">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="f67c7-266">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="f67c7-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f67c7-267">Vendas faturadas – Faturável para a nova quantidade</span><span class="sxs-lookup"><span data-stu-id="f67c7-267">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="f67c7-268">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="f67c7-268">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f67c7-269">Vendas não faturadas – Não faturável para a diferença</span><span class="sxs-lookup"><span data-stu-id="f67c7-269">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="f67c7-270">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="f67c7-270">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="f67c7-271">Uma fatura é corrigida para aumentar a quantidade faturável.</span><span class="sxs-lookup"><span data-stu-id="f67c7-271">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="f67c7-272">Vendas faturadas – Estorno</span><span class="sxs-lookup"><span data-stu-id="f67c7-272">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="f67c7-273">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="f67c7-273">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="f67c7-274">Estorno de vendas faturadas para marco</span><span class="sxs-lookup"><span data-stu-id="f67c7-274">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="f67c7-275">Alterar o estado do marco de <strong>Faturado</strong> para <strong>Pronto para faturação</strong></span><span class="sxs-lookup"><span data-stu-id="f67c7-275">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="f67c7-276">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="f67c7-276">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="f67c7-277">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="f67c7-277">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="f67c7-278">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="f67c7-278">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f67c7-279">Vendas faturadas</span><span class="sxs-lookup"><span data-stu-id="f67c7-279">Billed sales</span></span></td>
<td><span data-ttu-id="f67c7-280">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="f67c7-280">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="f67c7-281">Uma fatura é corrigida para diminuir a quantidade faturável.</span><span class="sxs-lookup"><span data-stu-id="f67c7-281">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="f67c7-282">Vendas faturadas – Estorno</span><span class="sxs-lookup"><span data-stu-id="f67c7-282">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="f67c7-283">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="f67c7-283">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f67c7-284">Vendas faturadas para a nova quantidade</span><span class="sxs-lookup"><span data-stu-id="f67c7-284">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="f67c7-285">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="f67c7-285">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f67c7-286">Vendas não faturadas – Faturável para a diferença</span><span class="sxs-lookup"><span data-stu-id="f67c7-286">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="f67c7-287">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="f67c7-287">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
