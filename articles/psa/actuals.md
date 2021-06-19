---
title: Descrição geral dos valores reais
description: Este tópico fornece informações sobre os valores reais do projeto.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 08/03/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 73f1b14bbb4cc53111a1b3a93756a86db04475ab
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014670"
---
# <a name="actuals-overview"></a><span data-ttu-id="ae6be-103">Descrição geral dos valores reais</span><span class="sxs-lookup"><span data-stu-id="ae6be-103">Actuals overview</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="ae6be-104">Os valores reais são a quantidade de trabalho que foi concluída num projeto.</span><span class="sxs-lookup"><span data-stu-id="ae6be-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="ae6be-105">Os valores reais do projeto podem ser novamente rastreados para os documentos de origem.</span><span class="sxs-lookup"><span data-stu-id="ae6be-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="ae6be-106">Estes documentos de origem incluem horas, despesas e entradas de diário, além de faturas.</span><span class="sxs-lookup"><span data-stu-id="ae6be-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Como os valores reais do projeto são rastreados para os documentos de origem](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="ae6be-108">Submeter uma entrada de tempo</span><span class="sxs-lookup"><span data-stu-id="ae6be-108">Submitting a time entry</span></span>

<span data-ttu-id="ae6be-109">No PSA, quando é submetida uma entrada de tempo para um projeto que está mapeado para um item de contrato de hora e material, são criadas duas linhas do diário.</span><span class="sxs-lookup"><span data-stu-id="ae6be-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="ae6be-110">Uma linha é para o custo e a outra linha é para as vendas não faturadas.</span><span class="sxs-lookup"><span data-stu-id="ae6be-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="ae6be-111">Quando é submetida uma entrada de tempo para um projeto que está mapeado para um item de contrato de preço fixo, é criada uma linha do diário apenas para o custo.</span><span class="sxs-lookup"><span data-stu-id="ae6be-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="ae6be-112">A lógica para a introdução de preços predefinidos reside na linha do diário.</span><span class="sxs-lookup"><span data-stu-id="ae6be-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="ae6be-113">Todos os valores de campo de uma entrada de tempo são copiados para a linha do diário.</span><span class="sxs-lookup"><span data-stu-id="ae6be-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="ae6be-114">Estes campos incluem a data da transação, o item de contrato para o qual o projeto está mapeado e a moeda resulta na lista de preços apropriada.</span><span class="sxs-lookup"><span data-stu-id="ae6be-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="ae6be-115">Os campos que afetam os preços predefinidos, como **Função** e **Unidade Organizacional** fazem com que seja introduzido um preço apropriado por predefinição na linha do diário.</span><span class="sxs-lookup"><span data-stu-id="ae6be-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="ae6be-116">Se adicionar um campo personalizado à entrada de tempo e pretender que o valor do campo seja propagado aos valores reais, crie o campo na entidade Valores Reais e utilize mapeamentos de campos para copiar o campo a partir da entrada de tempo para o valor real.</span><span class="sxs-lookup"><span data-stu-id="ae6be-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="ae6be-117">Submeter uma entrada de despesa</span><span class="sxs-lookup"><span data-stu-id="ae6be-117">Submitting an expense entry</span></span>

<span data-ttu-id="ae6be-118">No PSA, quando é submetida uma entrada de despesa para um projeto que está mapeado para um item de contrato de hora e material, são criadas duas linhas do diário.</span><span class="sxs-lookup"><span data-stu-id="ae6be-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="ae6be-119">Uma linha é para o custo e a outra linha é para as vendas não faturadas.</span><span class="sxs-lookup"><span data-stu-id="ae6be-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="ae6be-120">Quando é submetida uma entrada de despesa para um projeto que está mapeado para um item de contrato de preço fixo, é criada uma linha do diário apenas para o custo.</span><span class="sxs-lookup"><span data-stu-id="ae6be-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="ae6be-121">A lógica para a entrada de preços predefinidos para despesas é baseada na categoria de despesa que é selecionada na página **Entrada de despesa**,</span><span class="sxs-lookup"><span data-stu-id="ae6be-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="ae6be-122">A data da transação, o item de contrato para o qual o projeto está mapeado e a moeda são utilizados para determinar a lista de preços apropriada.</span><span class="sxs-lookup"><span data-stu-id="ae6be-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="ae6be-123">No entanto, para o preço propriamente dito, o montante introduzido pelo utilizador é definido diretamente nas linhas do diário de despesas relacionadas para o custo e as vendas, por predefinição.</span><span class="sxs-lookup"><span data-stu-id="ae6be-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="ae6be-124">Na versão atual do PSA, a entrada baseada em categorias de preços predefinidos por unidade em entradas de despesa não está disponível.</span><span class="sxs-lookup"><span data-stu-id="ae6be-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="ae6be-125">Utilizar diários de Entrada para registar custos</span><span class="sxs-lookup"><span data-stu-id="ae6be-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="ae6be-126">Em PSA, os diários de Entrada permitem-lhe registar o custo ou a receita nas classes de material, taxa, hora, despesa ou imposto.</span><span class="sxs-lookup"><span data-stu-id="ae6be-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="ae6be-127">Um diário tem um cabeçalho, linhas e uma ação de **Confirmação**.</span><span class="sxs-lookup"><span data-stu-id="ae6be-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="ae6be-128">Seguem-se alguns cenários em que poderá utilizar um diário:</span><span class="sxs-lookup"><span data-stu-id="ae6be-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="ae6be-129">Tem de registar os custos reais de materiais e as vendas num projeto.</span><span class="sxs-lookup"><span data-stu-id="ae6be-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="ae6be-130">Tem de mover os valores reais da transação a partir de outro sistema para o PSA.</span><span class="sxs-lookup"><span data-stu-id="ae6be-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="ae6be-131">Tem de registar os custos que ocorreram noutro sistema, tal como os custos de aprovisionamento ou subcontratação.</span><span class="sxs-lookup"><span data-stu-id="ae6be-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ae6be-132">A utilização de diários de Entrada para criar valores reais deve ser feita apenas por um utilizador que esteja plenamente consciente do impacto contabilístico que os Valores Reais têm no projeto.</span><span class="sxs-lookup"><span data-stu-id="ae6be-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="ae6be-133">Isto porque a aplicação não valida o tipo de linha do diário, ou o preço relacionado que é introduzido na linha do diário.</span><span class="sxs-lookup"><span data-stu-id="ae6be-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="ae6be-134">Devido ao impacto deste tipo de diário, tenha o cuidado adequado a quem é dado acesso para criar diários de Entrada.</span><span class="sxs-lookup"><span data-stu-id="ae6be-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="ae6be-135">Registar valores reais com base em eventos de projeto</span><span class="sxs-lookup"><span data-stu-id="ae6be-135">Recording actuals based on project events</span></span>

<span data-ttu-id="ae6be-136">O PSA regista as transações financeiras que ocorrem durante um projeto.</span><span class="sxs-lookup"><span data-stu-id="ae6be-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="ae6be-137">Estas transações são registadas como **reais**.</span><span class="sxs-lookup"><span data-stu-id="ae6be-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="ae6be-138">As tabelas seguintes mostram os diferentes tipos de valores reais criados, dependendo do facto de o projeto ser um projeto de tempo e material ou de preço fixo, que se encontra na fase pré-venda, ou é um projeto interno.</span><span class="sxs-lookup"><span data-stu-id="ae6be-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="ae6be-139">**O recurso pertence à mesma unidade organizacional que a unidade organizacional do projeto**</span><span class="sxs-lookup"><span data-stu-id="ae6be-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="ae6be-140">Evento</span><span class="sxs-lookup"><span data-stu-id="ae6be-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="ae6be-141">Projeto faturável ou vendido</span><span class="sxs-lookup"><span data-stu-id="ae6be-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="ae6be-142">Projeto na fase pré-venda</span><span class="sxs-lookup"><span data-stu-id="ae6be-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="ae6be-143">Projeto interno</span><span class="sxs-lookup"><span data-stu-id="ae6be-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="ae6be-144">Hora e materiais</span><span class="sxs-lookup"><span data-stu-id="ae6be-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="ae6be-145">Preço fixo</span><span class="sxs-lookup"><span data-stu-id="ae6be-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="ae6be-146">Valores Reais</span><span class="sxs-lookup"><span data-stu-id="ae6be-146">Actuals</span></span></th>
<th><span data-ttu-id="ae6be-147">Moeda da transação</span><span class="sxs-lookup"><span data-stu-id="ae6be-147">Transaction currency</span></span></th>
<th><span data-ttu-id="ae6be-148">Preço fixo</span><span class="sxs-lookup"><span data-stu-id="ae6be-148">Fixed price</span></span></th>
<th><span data-ttu-id="ae6be-149">Moeda da transação</span><span class="sxs-lookup"><span data-stu-id="ae6be-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ae6be-150">É criada uma entrada de hora.</span><span class="sxs-lookup"><span data-stu-id="ae6be-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="ae6be-151">Sem atividade na entidade Valores Reais</span><span class="sxs-lookup"><span data-stu-id="ae6be-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ae6be-152">É submetida uma entrada de hora.</span><span class="sxs-lookup"><span data-stu-id="ae6be-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="ae6be-153">Sem atividade na entidade Valores Reais</span><span class="sxs-lookup"><span data-stu-id="ae6be-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="ae6be-154">A hora é aprovada e não ocorre nenhuma alteração ou aumento nas horas faturáveis durante a aprovação.</span><span class="sxs-lookup"><span data-stu-id="ae6be-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="ae6be-155">Custo real</span><span class="sxs-lookup"><span data-stu-id="ae6be-155">Cost actual</span></span></td>
<td><span data-ttu-id="ae6be-156">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="ae6be-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="ae6be-157">Custo real</span><span class="sxs-lookup"><span data-stu-id="ae6be-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="ae6be-158">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="ae6be-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="ae6be-159">Custo real</span><span class="sxs-lookup"><span data-stu-id="ae6be-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="ae6be-160">Custo real</span><span class="sxs-lookup"><span data-stu-id="ae6be-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ae6be-161">Valor real de vendas não faturadas – Faturável</span><span class="sxs-lookup"><span data-stu-id="ae6be-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="ae6be-162">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="ae6be-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="ae6be-163">A hora é aprovada e ocorre uma diminuição nas horas faturáveis durante a aprovação.</span><span class="sxs-lookup"><span data-stu-id="ae6be-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="ae6be-164">Custo real</span><span class="sxs-lookup"><span data-stu-id="ae6be-164">Cost actual</span></span></td>
<td><span data-ttu-id="ae6be-165">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="ae6be-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="ae6be-166">Custo real</span><span class="sxs-lookup"><span data-stu-id="ae6be-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="ae6be-167">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="ae6be-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="ae6be-168">Custo real</span><span class="sxs-lookup"><span data-stu-id="ae6be-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="ae6be-169">Custo real</span><span class="sxs-lookup"><span data-stu-id="ae6be-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ae6be-170">Valor real de vendas não faturadas – Faturável para a nova quantidade</span><span class="sxs-lookup"><span data-stu-id="ae6be-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="ae6be-171">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="ae6be-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ae6be-172">Valor real de vendas não faturadas – Não faturável para a diferença</span><span class="sxs-lookup"><span data-stu-id="ae6be-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="ae6be-173">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="ae6be-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="ae6be-174">É confirmada uma fatura e não ocorre nenhuma alteração ou aumento nas horas faturáveis.</span><span class="sxs-lookup"><span data-stu-id="ae6be-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="ae6be-175">Estorno de vendas não faturadas</span><span class="sxs-lookup"><span data-stu-id="ae6be-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="ae6be-176">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="ae6be-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="ae6be-177">Vendas faturadas para marco</span><span class="sxs-lookup"><span data-stu-id="ae6be-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="ae6be-178">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="ae6be-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="ae6be-179">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="ae6be-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="ae6be-180">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="ae6be-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ae6be-181">Vendas faturadas</span><span class="sxs-lookup"><span data-stu-id="ae6be-181">Billed sales</span></span></td>
<td><span data-ttu-id="ae6be-182">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="ae6be-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="ae6be-183">É confirmada uma fatura e ocorre uma diminuição nas horas faturáveis.</span><span class="sxs-lookup"><span data-stu-id="ae6be-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="ae6be-184">Estorno de vendas não faturadas</span><span class="sxs-lookup"><span data-stu-id="ae6be-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="ae6be-185">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="ae6be-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="ae6be-186">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="ae6be-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="ae6be-187">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="ae6be-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="ae6be-188">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="ae6be-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="ae6be-189">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="ae6be-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ae6be-190">Vendas faturadas – Faturável para a nova quantidade</span><span class="sxs-lookup"><span data-stu-id="ae6be-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="ae6be-191">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="ae6be-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ae6be-192">Vendas não faturadas – Não faturável para a diferença</span><span class="sxs-lookup"><span data-stu-id="ae6be-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="ae6be-193">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="ae6be-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="ae6be-194">Uma fatura é corrigida para aumentar a quantidade faturável.</span><span class="sxs-lookup"><span data-stu-id="ae6be-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="ae6be-195">Vendas faturadas – Estorno</span><span class="sxs-lookup"><span data-stu-id="ae6be-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="ae6be-196">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="ae6be-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="ae6be-197">Estorno de vendas faturadas para marco</span><span class="sxs-lookup"><span data-stu-id="ae6be-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="ae6be-198">Alterar o estado do marco de <strong>Faturado</strong> para <strong>Pronto para faturação</strong></span><span class="sxs-lookup"><span data-stu-id="ae6be-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="ae6be-199">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="ae6be-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="ae6be-200">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="ae6be-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="ae6be-201">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="ae6be-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ae6be-202">Vendas faturadas</span><span class="sxs-lookup"><span data-stu-id="ae6be-202">Billed sales</span></span></td>
<td><span data-ttu-id="ae6be-203">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="ae6be-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="ae6be-204">Uma fatura é corrigida para diminuir a quantidade faturável.</span><span class="sxs-lookup"><span data-stu-id="ae6be-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="ae6be-205">Vendas faturadas – Estorno</span><span class="sxs-lookup"><span data-stu-id="ae6be-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="ae6be-206">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="ae6be-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ae6be-207">Vendas faturadas para a nova quantidade</span><span class="sxs-lookup"><span data-stu-id="ae6be-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="ae6be-208">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="ae6be-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ae6be-209">Vendas não faturadas – Faturável para a diferença</span><span class="sxs-lookup"><span data-stu-id="ae6be-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="ae6be-210">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="ae6be-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ae6be-211">**O recurso pertence a uma unidade organizacional que difere da unidade organizacional do projeto**</span><span class="sxs-lookup"><span data-stu-id="ae6be-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="ae6be-212">Evento</span><span class="sxs-lookup"><span data-stu-id="ae6be-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="ae6be-213">Projeto faturável ou vendido</span><span class="sxs-lookup"><span data-stu-id="ae6be-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="ae6be-214">Projeto na fase pré-venda</span><span class="sxs-lookup"><span data-stu-id="ae6be-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="ae6be-215">Projeto interno</span><span class="sxs-lookup"><span data-stu-id="ae6be-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="ae6be-216">Hora e materiais</span><span class="sxs-lookup"><span data-stu-id="ae6be-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="ae6be-217">Preço fixo</span><span class="sxs-lookup"><span data-stu-id="ae6be-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="ae6be-218">Valores Reais</span><span class="sxs-lookup"><span data-stu-id="ae6be-218">Actuals</span></span></th>
<th><span data-ttu-id="ae6be-219">Moeda da transação</span><span class="sxs-lookup"><span data-stu-id="ae6be-219">Transaction currency</span></span></th>
<th><span data-ttu-id="ae6be-220">Preço fixo</span><span class="sxs-lookup"><span data-stu-id="ae6be-220">Fixed price</span></span></th>
<th><span data-ttu-id="ae6be-221">Moeda da transação</span><span class="sxs-lookup"><span data-stu-id="ae6be-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ae6be-222">É criada uma entrada de hora.</span><span class="sxs-lookup"><span data-stu-id="ae6be-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="ae6be-223">Sem atividade na entidade Valores Reais</span><span class="sxs-lookup"><span data-stu-id="ae6be-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ae6be-224">É submetida uma entrada de hora.</span><span class="sxs-lookup"><span data-stu-id="ae6be-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="ae6be-225">Sem atividade na entidade Valores Reais</span><span class="sxs-lookup"><span data-stu-id="ae6be-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="ae6be-226">A hora é aprovada e não ocorre nenhuma alteração ou aumento nas horas faturáveis durante a aprovação.</span><span class="sxs-lookup"><span data-stu-id="ae6be-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="ae6be-227">Custo real</span><span class="sxs-lookup"><span data-stu-id="ae6be-227">Cost actual</span></span></td>
<td><span data-ttu-id="ae6be-228">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="ae6be-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="ae6be-229">Custo real</span><span class="sxs-lookup"><span data-stu-id="ae6be-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="ae6be-230">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="ae6be-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="ae6be-231">Custo real</span><span class="sxs-lookup"><span data-stu-id="ae6be-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="ae6be-232">Custo real</span><span class="sxs-lookup"><span data-stu-id="ae6be-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ae6be-233">Valor real de vendas não faturadas – Faturável</span><span class="sxs-lookup"><span data-stu-id="ae6be-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="ae6be-234">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="ae6be-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ae6be-235">Custo de unidade de atribuição de recursos</span><span class="sxs-lookup"><span data-stu-id="ae6be-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="ae6be-236">Moeda da unidade de atribuição de recursos</span><span class="sxs-lookup"><span data-stu-id="ae6be-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ae6be-237">Vendas interorganizacionais</span><span class="sxs-lookup"><span data-stu-id="ae6be-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="ae6be-238">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="ae6be-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="ae6be-239">A hora é aprovada e ocorre uma diminuição nas horas faturáveis durante a aprovação.</span><span class="sxs-lookup"><span data-stu-id="ae6be-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="ae6be-240">Custo real</span><span class="sxs-lookup"><span data-stu-id="ae6be-240">Cost actual</span></span></td>
<td><span data-ttu-id="ae6be-241">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="ae6be-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="ae6be-242">Custo real</span><span class="sxs-lookup"><span data-stu-id="ae6be-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="ae6be-243">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="ae6be-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="ae6be-244">Custo real</span><span class="sxs-lookup"><span data-stu-id="ae6be-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="ae6be-245">Custo real</span><span class="sxs-lookup"><span data-stu-id="ae6be-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ae6be-246">Custo de unidade de atribuição de recursos</span><span class="sxs-lookup"><span data-stu-id="ae6be-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="ae6be-247">Moeda da unidade de atribuição de recursos</span><span class="sxs-lookup"><span data-stu-id="ae6be-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ae6be-248">Vendas interorganizacionais</span><span class="sxs-lookup"><span data-stu-id="ae6be-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="ae6be-249">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="ae6be-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ae6be-250">Valor real de vendas não faturadas – Faturável para a nova quantidade</span><span class="sxs-lookup"><span data-stu-id="ae6be-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="ae6be-251">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="ae6be-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ae6be-252">Valor real de vendas não faturadas – Não faturável para a diferença</span><span class="sxs-lookup"><span data-stu-id="ae6be-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="ae6be-253">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="ae6be-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="ae6be-254">É confirmada uma fatura e não ocorre nenhuma alteração ou aumento nas horas faturáveis.</span><span class="sxs-lookup"><span data-stu-id="ae6be-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="ae6be-255">Estorno de vendas não faturadas</span><span class="sxs-lookup"><span data-stu-id="ae6be-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="ae6be-256">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="ae6be-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="ae6be-257">Vendas faturadas para marco</span><span class="sxs-lookup"><span data-stu-id="ae6be-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="ae6be-258">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="ae6be-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="ae6be-259">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="ae6be-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="ae6be-260">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="ae6be-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ae6be-261">Vendas faturadas</span><span class="sxs-lookup"><span data-stu-id="ae6be-261">Billed sales</span></span></td>
<td><span data-ttu-id="ae6be-262">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="ae6be-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="ae6be-263">É confirmada uma fatura e ocorre uma diminuição nas horas faturáveis.</span><span class="sxs-lookup"><span data-stu-id="ae6be-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="ae6be-264">Estorno de vendas não faturadas</span><span class="sxs-lookup"><span data-stu-id="ae6be-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="ae6be-265">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="ae6be-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="ae6be-266">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="ae6be-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="ae6be-267">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="ae6be-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="ae6be-268">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="ae6be-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="ae6be-269">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="ae6be-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ae6be-270">Vendas faturadas – Faturável para a nova quantidade</span><span class="sxs-lookup"><span data-stu-id="ae6be-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="ae6be-271">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="ae6be-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ae6be-272">Vendas não faturadas – Não faturável para a diferença</span><span class="sxs-lookup"><span data-stu-id="ae6be-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="ae6be-273">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="ae6be-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="ae6be-274">Uma fatura é corrigida para aumentar a quantidade faturável.</span><span class="sxs-lookup"><span data-stu-id="ae6be-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="ae6be-275">Vendas faturadas – Estorno</span><span class="sxs-lookup"><span data-stu-id="ae6be-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="ae6be-276">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="ae6be-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="ae6be-277">Estorno de vendas faturadas para marco</span><span class="sxs-lookup"><span data-stu-id="ae6be-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="ae6be-278">Alterar o estado do marco de <strong>Faturado</strong> para <strong>Pronto para faturação</strong></span><span class="sxs-lookup"><span data-stu-id="ae6be-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="ae6be-279">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="ae6be-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="ae6be-280">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="ae6be-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="ae6be-281">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="ae6be-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ae6be-282">Vendas faturadas</span><span class="sxs-lookup"><span data-stu-id="ae6be-282">Billed sales</span></span></td>
<td><span data-ttu-id="ae6be-283">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="ae6be-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="ae6be-284">Uma fatura é corrigida para diminuir a quantidade faturável.</span><span class="sxs-lookup"><span data-stu-id="ae6be-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="ae6be-285">Vendas faturadas – Estorno</span><span class="sxs-lookup"><span data-stu-id="ae6be-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="ae6be-286">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="ae6be-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ae6be-287">Vendas faturadas para a nova quantidade</span><span class="sxs-lookup"><span data-stu-id="ae6be-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="ae6be-288">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="ae6be-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ae6be-289">Vendas não faturadas – Faturável para a diferença</span><span class="sxs-lookup"><span data-stu-id="ae6be-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="ae6be-290">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="ae6be-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]