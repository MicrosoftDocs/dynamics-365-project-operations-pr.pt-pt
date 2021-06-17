---
title: Valores Reais
description: Esta tópico fornece informações sobre como trabalhar com valores reais no Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 78c7a9486d0338adfd7770447f21d17509e654f7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996625"
---
# <a name="actuals"></a><span data-ttu-id="9fbaa-103">Valores Reais</span><span class="sxs-lookup"><span data-stu-id="9fbaa-103">Actuals</span></span> 

<span data-ttu-id="9fbaa-104">_**Aplica-se a:** Project Operations para cenários baseados em recursos/não armazenados, implementação leve - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="9fbaa-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9fbaa-105">Os valores reais representam os progressos financeiros e de programação revistos e aprovados num projeto.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-105">Actuals represent the reviewed and approved financial and schedule progress on a project.</span></span> <span data-ttu-id="9fbaa-106">São criados como resultado da aprovação do tempo, despesas, entradas de utilização de materiais e entradas de diário e faturas.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-106">They are created as a result of approval of time, expense, material usage entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="9fbaa-107">Envio de linhas do diário e tempo</span><span class="sxs-lookup"><span data-stu-id="9fbaa-107">Journal lines and time submission</span></span>

<span data-ttu-id="9fbaa-108">Para mais informações sobre a entrada de hora, consulte [Descrição geral da entrada de hora](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="9fbaa-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="9fbaa-109">Hora e materiais</span><span class="sxs-lookup"><span data-stu-id="9fbaa-109">Time and materials</span></span>

<span data-ttu-id="9fbaa-110">Quando uma entrada de hora que é submetida está associada a um projeto que é mapeado para um item de contrato de tempo e materiais, o sistema cria duas linhas do diário, uma para o custo e uma para as vendas não faturadas.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="9fbaa-111">Preço fixo</span><span class="sxs-lookup"><span data-stu-id="9fbaa-111">Fixed price</span></span>

<span data-ttu-id="9fbaa-112">Quando uma entrada de hora que é submetida está associada a um projeto que está mapeado para um item de contrato de preço fixo, o sistema cria uma linha do diário para o custo.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="9fbaa-113">Preço predefinido</span><span class="sxs-lookup"><span data-stu-id="9fbaa-113">Default pricing</span></span>

<span data-ttu-id="9fbaa-114">A lógica para criar preços predefinidos reside na linha do diário.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="9fbaa-115">Os valores do campo da entrada de hora são copiados para a linha do diário.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="9fbaa-116">Estes valores incluem a data da transação, o item de contrato para o qual o projeto está mapeado e a moeda resulta na lista de preços apropriada.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="9fbaa-117">Os campos que afetam os preços predefinidos, como **Função** e **Unidade de recursos** são usados para determinar o preço apropriado na linha do diário.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-117">The fields that affect default pricing, such as **Role** and **Resourcing Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="9fbaa-118">Pode adicionar um campo personalizado na entrada de hora.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="9fbaa-119">Se pretender que o valor do campo seja propagado aos valores reais, crie o campo nas tabelas **Valores reais** e **Linha do diário**.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-119">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="9fbaa-120">Utilize código personalizado para propagar o valor de campo selecionado da Entrada de Tempo para Valores reais através da linha do diário utilizando as origens de transação.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-120">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="9fbaa-121">Para obter mais informações sobre as origens e ligações de transações, consulte [Ligar valores reais a registos originais](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="9fbaa-121">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="9fbaa-122">Submissão de linhas do diário e despesas básicas</span><span class="sxs-lookup"><span data-stu-id="9fbaa-122">Journal lines and basic expense submission</span></span>

<span data-ttu-id="9fbaa-123">Para mais informações sobre a entrada de despesa, consulte [Descrição geral da despesa](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="9fbaa-123">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="9fbaa-124">Hora e materiais</span><span class="sxs-lookup"><span data-stu-id="9fbaa-124">Time and materials</span></span>

<span data-ttu-id="9fbaa-125">Quando uma entrada de despesa básica que é submetida está associada a um projeto que é mapeado para um item de contrato de tempo e materiais, o sistema cria duas linhas do diário, uma para o custo e uma para as vendas não faturadas.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-125">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="9fbaa-126">Preço fixo</span><span class="sxs-lookup"><span data-stu-id="9fbaa-126">Fixed price</span></span>

<span data-ttu-id="9fbaa-127">Quando uma entrada de despesa submetida é ligada a um projeto que está mapeado para um item de contrato de preço fixo, o sistema cria uma linha do diário para o custo.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-127">When a submitted basic expense entry is linked to a project that's mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="9fbaa-128">Preço predefinido</span><span class="sxs-lookup"><span data-stu-id="9fbaa-128">Default pricing</span></span>

<span data-ttu-id="9fbaa-129">A lógica para introduzir os preços predefinidos para as despesas baseia-se na categoria de despesa.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-129">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="9fbaa-130">A data da transação, o item de contrato para o qual o projeto está mapeado e a moeda são utilizados para determinar a lista de preços apropriada.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-130">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="9fbaa-131">Os campos que afetam os preços predefinidos, como **Categoria de transação** e **Unidade** são usados para determinar o preço apropriado na linha do diário.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-131">The fields that affect default pricing, such as **Transaction Category** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="9fbaa-132">No entanto, isto só funciona quando o método de preços na tabela de preços é **Preço por unidade**.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-132">However, this only works when the pricing method in the price list is **Price per unit**.</span></span> <span data-ttu-id="9fbaa-133">Se o método de preços for **A custo** ou **Margem de lucro sobre o custo**, o preço introduzido quando a entrada de despesas é criada é utilizado para o custo e o preço na linha de diário de vendas é calculado com base no método de preços.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-133">If pricing method is **At cost** or **Markup over cost**, the price entered when the expense entry is created is used for cost and the price on the sales journal line is calculated based on the pricing method.</span></span> 

<span data-ttu-id="9fbaa-134">Pode adicionar um campo personalizado na entrada de despesas.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-134">You can add a custom field on the expense entry.</span></span> <span data-ttu-id="9fbaa-135">Se pretender que o valor do campo seja propagado aos valores reais, crie o campo nas tabelas **Valores reais** e **Linha do diário**.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-135">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="9fbaa-136">Utilize código personalizado para propagar o valor de campo selecionado da Entrada de Tempo para Valores reais através da linha do diário utilizando as origens de transação.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-136">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="9fbaa-137">Para obter mais informações sobre as origens e ligações de transações, consulte [Ligar valores reais a registos originais](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="9fbaa-137">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-material-usage-log-submission"></a><span data-ttu-id="9fbaa-138">Submissão de linhas de diário e de registo de utilização de materiais</span><span class="sxs-lookup"><span data-stu-id="9fbaa-138">Journal lines and material usage log submission</span></span>

<span data-ttu-id="9fbaa-139">Para obter mais informações sobre a entrada de despesas, consulte o [Registo de utilização de materiais.](../material/material-usage-log.md)</span><span class="sxs-lookup"><span data-stu-id="9fbaa-139">For more information about expense entry, see [Material Usage Log](../material/material-usage-log.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="9fbaa-140">Hora e materiais</span><span class="sxs-lookup"><span data-stu-id="9fbaa-140">Time and materials</span></span>

<span data-ttu-id="9fbaa-141">Quando uma entrada de registo de utilização de material submetida está ligada a um projeto que está mapeado para uma linha de contrato de tempo e materiais, o sistema cria duas linhas do diário, uma para custo e outra para vendas não faturadas.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-141">When a submitted material usage log entry is linked to a project that is mapped to a time and materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="9fbaa-142">Preço fixo</span><span class="sxs-lookup"><span data-stu-id="9fbaa-142">Fixed price</span></span>

<span data-ttu-id="9fbaa-143">Quando uma entrada de registo de utilização de material é ligada a um projeto que está mapeado para um item de contrato de preço fixo, o sistema cria uma linha do diário para o custo.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-143">When a submitted material usage log entry is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="9fbaa-144">Preço predefinido</span><span class="sxs-lookup"><span data-stu-id="9fbaa-144">Default pricing</span></span>

<span data-ttu-id="9fbaa-145">A lógica para introduzir preços predefinidos para o material baseia-se na combinação do produto e da unidade.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-145">The logic for entering default prices for material is based on the product and unit combination.</span></span> <span data-ttu-id="9fbaa-146">A data da transação, o item de contrato para o qual o projeto está mapeado e a moeda são utilizados para determinar a lista de preços apropriada.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-146">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="9fbaa-147">Os campos que afetam os preços predefinidos, como **ID do produto** e **Unidade** são usados para determinar o preço apropriado na linha do diário.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-147">The fields that affect default pricing, such as **Product ID** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="9fbaa-148">No entanto, isto só funciona para produtos de catálogo.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-148">However, this only works for catalog products.</span></span> <span data-ttu-id="9fbaa-149">Para os produtos de write-in, o preço introduzido quando a entrada de registo de utilização do material é criado é utilizado para o custo e preço de venda nas linhas de diário.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-149">For write-in products, the price entered when the material usage log entry is created is used for cost and sales price on the journal lines.</span></span> 

<span data-ttu-id="9fbaa-150">Pode adicionar um campo personalizado na entrada **Registo de utilização de material**.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-150">You can add a custom field on the **Material Usage Log** entry.</span></span> <span data-ttu-id="9fbaa-151">Se pretender que o valor do campo seja propagado aos valores reais, crie o campo nas tabelas **Valores reais** e **Linha do diário**.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-151">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="9fbaa-152">Utilize código personalizado para propagar o valor de campo selecionado da Entrada de Tempo para Valores reais através da linha do diário utilizando as origens de transação.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-152">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="9fbaa-153">Para obter mais informações sobre as origens e ligações de transações, consulte [Ligar valores reais a registos originais](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="9fbaa-153">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="9fbaa-154">Utilizar diários de entrada para registar custos</span><span class="sxs-lookup"><span data-stu-id="9fbaa-154">Use entry journals to record costs</span></span>

<span data-ttu-id="9fbaa-155">Poderá utilizar os diários de entrada para registar o custo ou a receita nas classes de material, taxa, hora, despesa ou imposto.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-155">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="9fbaa-156">Os diários podem ser utilizadas para as finalidades seguintes:</span><span class="sxs-lookup"><span data-stu-id="9fbaa-156">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="9fbaa-157">Mover os valores reais da transação a partir de outro sistema para o Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-157">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="9fbaa-158">Registe os custos que ocorreram noutro sistema.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-158">Record costs that occurred in another system.</span></span> <span data-ttu-id="9fbaa-159">Estes custos podem incluir os custos de aprovisionamento ou subcontratação.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-159">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9fbaa-160">A aplicação não valida o tipo de linha de diário ou o preço relacionado que é introduzido na linha do diário.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-160">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="9fbaa-161">Assim, só um utilizador plenamente consciente do impacto contabilístico que os valores reais têm no projeto deve utilizar diários de entrada para criar valores reais.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-161">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="9fbaa-162">Dado o impacto deste tipo de diário, deve escolher cuidadosamente quem tem acesso para criar diários de entrada.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-162">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>

## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="9fbaa-163">Registar os valores reais baseado nos eventos do projeto</span><span class="sxs-lookup"><span data-stu-id="9fbaa-163">Record actuals based on project events</span></span>

<span data-ttu-id="9fbaa-164">O Project Operations regista as transações financeiras que ocorrem durante um projeto.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-164">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="9fbaa-165">Estas transações são registadas como reais.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-165">These transactions are recorded as actuals.</span></span> <span data-ttu-id="9fbaa-166">As tabelas seguintes mostram os diferentes tipos de valores reais criados, dependendo do facto de o projeto ser um projeto de tempo e material ou de preço fixo, que se encontra na fase pré-venda, ou é um projeto interno.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-166">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="9fbaa-167">O recurso pertence à mesma unidade organizacional que a unidade organizacional do projeto</span><span class="sxs-lookup"><span data-stu-id="9fbaa-167">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="9fbaa-168">Evento</span><span class="sxs-lookup"><span data-stu-id="9fbaa-168">Event</span></span></th>
<th colspan="4"><span data-ttu-id="9fbaa-169">Projeto faturável ou vendido</span><span class="sxs-lookup"><span data-stu-id="9fbaa-169">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="9fbaa-170">Projeto na fase pré-venda</span><span class="sxs-lookup"><span data-stu-id="9fbaa-170">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="9fbaa-171">Projeto interno</span><span class="sxs-lookup"><span data-stu-id="9fbaa-171">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="9fbaa-172">Hora e materiais</span><span class="sxs-lookup"><span data-stu-id="9fbaa-172">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="9fbaa-173">Preço fixo</span><span class="sxs-lookup"><span data-stu-id="9fbaa-173">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="9fbaa-174">Valores Reais</span><span class="sxs-lookup"><span data-stu-id="9fbaa-174">Actuals</span></span></th>
<th><span data-ttu-id="9fbaa-175">Moeda da transação</span><span class="sxs-lookup"><span data-stu-id="9fbaa-175">Transaction currency</span></span></th>
<th><span data-ttu-id="9fbaa-176">Preço fixo</span><span class="sxs-lookup"><span data-stu-id="9fbaa-176">Fixed price</span></span></th>
<th><span data-ttu-id="9fbaa-177">Moeda da transação</span><span class="sxs-lookup"><span data-stu-id="9fbaa-177">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9fbaa-178">É criada uma entrada de hora.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-178">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="9fbaa-179">Sem atividade na entidade Valores Reais</span><span class="sxs-lookup"><span data-stu-id="9fbaa-179">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fbaa-180">É submetida uma entrada de hora.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-180">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="9fbaa-181">Sem atividade na entidade Valores Reais</span><span class="sxs-lookup"><span data-stu-id="9fbaa-181">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="9fbaa-182">A hora é aprovada e não ocorre nenhuma alteração ou aumento nas horas faturáveis durante a aprovação.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-182">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="9fbaa-183">Custo real</span><span class="sxs-lookup"><span data-stu-id="9fbaa-183">Cost actual</span></span></td>
<td><span data-ttu-id="9fbaa-184">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="9fbaa-184">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="9fbaa-185">Custo real</span><span class="sxs-lookup"><span data-stu-id="9fbaa-185">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="9fbaa-186">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="9fbaa-186">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="9fbaa-187">Custo real</span><span class="sxs-lookup"><span data-stu-id="9fbaa-187">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="9fbaa-188">Custo real</span><span class="sxs-lookup"><span data-stu-id="9fbaa-188">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fbaa-189">Valor real de vendas não faturadas – Faturável</span><span class="sxs-lookup"><span data-stu-id="9fbaa-189">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="9fbaa-190">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="9fbaa-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="9fbaa-191">A hora é aprovada e ocorre uma diminuição nas horas faturáveis durante a aprovação.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-191">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="9fbaa-192">Custo real</span><span class="sxs-lookup"><span data-stu-id="9fbaa-192">Cost actual</span></span></td>
<td><span data-ttu-id="9fbaa-193">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="9fbaa-193">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="9fbaa-194">Custo real</span><span class="sxs-lookup"><span data-stu-id="9fbaa-194">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="9fbaa-195">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="9fbaa-195">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="9fbaa-196">Custo real</span><span class="sxs-lookup"><span data-stu-id="9fbaa-196">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="9fbaa-197">Custo real</span><span class="sxs-lookup"><span data-stu-id="9fbaa-197">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fbaa-198">Valor real de vendas não faturadas – Faturável para a nova quantidade</span><span class="sxs-lookup"><span data-stu-id="9fbaa-198">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="9fbaa-199">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="9fbaa-199">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fbaa-200">Valor real de vendas não faturadas – Não faturável para a diferença</span><span class="sxs-lookup"><span data-stu-id="9fbaa-200">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="9fbaa-201">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="9fbaa-201">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="9fbaa-202">É confirmada uma fatura e não ocorre nenhuma alteração ou aumento nas horas faturáveis.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-202">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="9fbaa-203">Estorno de vendas não faturadas</span><span class="sxs-lookup"><span data-stu-id="9fbaa-203">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="9fbaa-204">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="9fbaa-204">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="9fbaa-205">Vendas faturadas para marco</span><span class="sxs-lookup"><span data-stu-id="9fbaa-205">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="9fbaa-206">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="9fbaa-206">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="9fbaa-207">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="9fbaa-207">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="9fbaa-208">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="9fbaa-208">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fbaa-209">Vendas faturadas</span><span class="sxs-lookup"><span data-stu-id="9fbaa-209">Billed sales</span></span></td>
<td><span data-ttu-id="9fbaa-210">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="9fbaa-210">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="9fbaa-211">É confirmada uma fatura e ocorre uma diminuição nas horas faturáveis.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-211">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="9fbaa-212">Estorno de vendas não faturadas</span><span class="sxs-lookup"><span data-stu-id="9fbaa-212">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="9fbaa-213">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="9fbaa-213">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="9fbaa-214">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="9fbaa-214">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="9fbaa-215">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="9fbaa-215">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="9fbaa-216">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="9fbaa-216">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="9fbaa-217">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="9fbaa-217">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fbaa-218">Vendas faturadas – Faturável para a nova quantidade</span><span class="sxs-lookup"><span data-stu-id="9fbaa-218">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="9fbaa-219">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="9fbaa-219">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fbaa-220">Vendas não faturadas – Não faturável para a diferença</span><span class="sxs-lookup"><span data-stu-id="9fbaa-220">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="9fbaa-221">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="9fbaa-221">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="9fbaa-222">Uma fatura é corrigida para aumentar a quantidade faturável.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-222">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="9fbaa-223">Vendas faturadas – Estorno</span><span class="sxs-lookup"><span data-stu-id="9fbaa-223">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="9fbaa-224">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="9fbaa-224">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="9fbaa-225">Estorno de vendas faturadas para marco</span><span class="sxs-lookup"><span data-stu-id="9fbaa-225">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="9fbaa-226">Alterar o estado do marco de <strong>Faturado</strong> para <strong>Pronto para faturação</strong></span><span class="sxs-lookup"><span data-stu-id="9fbaa-226">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="9fbaa-227">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="9fbaa-227">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="9fbaa-228">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="9fbaa-228">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="9fbaa-229">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="9fbaa-229">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fbaa-230">Vendas faturadas</span><span class="sxs-lookup"><span data-stu-id="9fbaa-230">Billed sales</span></span></td>
<td><span data-ttu-id="9fbaa-231">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="9fbaa-231">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="9fbaa-232">Uma fatura é corrigida para diminuir a quantidade faturável.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-232">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="9fbaa-233">Vendas faturadas – Estorno</span><span class="sxs-lookup"><span data-stu-id="9fbaa-233">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="9fbaa-234">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="9fbaa-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fbaa-235">Vendas faturadas para a nova quantidade</span><span class="sxs-lookup"><span data-stu-id="9fbaa-235">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="9fbaa-236">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="9fbaa-236">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fbaa-237">Vendas não faturadas – Faturável para a diferença</span><span class="sxs-lookup"><span data-stu-id="9fbaa-237">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="9fbaa-238">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="9fbaa-238">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="9fbaa-239">O recurso pertence a uma unidade organizacional que difere da unidade organizacional do projeto</span><span class="sxs-lookup"><span data-stu-id="9fbaa-239">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="9fbaa-240">Evento</span><span class="sxs-lookup"><span data-stu-id="9fbaa-240">Event</span></span></th>
<th colspan="4"><span data-ttu-id="9fbaa-241">Projeto faturável ou vendido</span><span class="sxs-lookup"><span data-stu-id="9fbaa-241">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="9fbaa-242">Projeto na fase pré-venda</span><span class="sxs-lookup"><span data-stu-id="9fbaa-242">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="9fbaa-243">Projeto interno</span><span class="sxs-lookup"><span data-stu-id="9fbaa-243">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="9fbaa-244">Hora e materiais</span><span class="sxs-lookup"><span data-stu-id="9fbaa-244">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="9fbaa-245">Preço fixo</span><span class="sxs-lookup"><span data-stu-id="9fbaa-245">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="9fbaa-246">Valores Reais</span><span class="sxs-lookup"><span data-stu-id="9fbaa-246">Actuals</span></span></th>
<th><span data-ttu-id="9fbaa-247">Moeda da transação</span><span class="sxs-lookup"><span data-stu-id="9fbaa-247">Transaction currency</span></span></th>
<th><span data-ttu-id="9fbaa-248">Preço fixo</span><span class="sxs-lookup"><span data-stu-id="9fbaa-248">Fixed price</span></span></th>
<th><span data-ttu-id="9fbaa-249">Moeda da transação</span><span class="sxs-lookup"><span data-stu-id="9fbaa-249">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9fbaa-250">É criada uma entrada de hora.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-250">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="9fbaa-251">Sem atividade na entidade Valores Reais</span><span class="sxs-lookup"><span data-stu-id="9fbaa-251">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fbaa-252">É submetida uma entrada de hora.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-252">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="9fbaa-253">Sem atividade na entidade Valores Reais</span><span class="sxs-lookup"><span data-stu-id="9fbaa-253">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="9fbaa-254">A hora é aprovada e não ocorre nenhuma alteração ou aumento nas horas faturáveis durante a aprovação.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-254">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="9fbaa-255">Custo real</span><span class="sxs-lookup"><span data-stu-id="9fbaa-255">Cost actual</span></span></td>
<td><span data-ttu-id="9fbaa-256">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="9fbaa-256">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="9fbaa-257">Custo real</span><span class="sxs-lookup"><span data-stu-id="9fbaa-257">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="9fbaa-258">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="9fbaa-258">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="9fbaa-259">Custo real</span><span class="sxs-lookup"><span data-stu-id="9fbaa-259">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="9fbaa-260">Custo real</span><span class="sxs-lookup"><span data-stu-id="9fbaa-260">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fbaa-261">Valor real de vendas não faturadas – Faturável</span><span class="sxs-lookup"><span data-stu-id="9fbaa-261">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="9fbaa-262">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="9fbaa-262">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fbaa-263">Custo de unidade de atribuição de recursos</span><span class="sxs-lookup"><span data-stu-id="9fbaa-263">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="9fbaa-264">Moeda da unidade de atribuição de recursos</span><span class="sxs-lookup"><span data-stu-id="9fbaa-264">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fbaa-265">Vendas interorganizacionais</span><span class="sxs-lookup"><span data-stu-id="9fbaa-265">Interorganizational sales</span></span></td>
<td><span data-ttu-id="9fbaa-266">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="9fbaa-266">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="9fbaa-267">A hora é aprovada e ocorre uma diminuição nas horas faturáveis durante a aprovação.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-267">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="9fbaa-268">Custo real</span><span class="sxs-lookup"><span data-stu-id="9fbaa-268">Cost actual</span></span></td>
<td><span data-ttu-id="9fbaa-269">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="9fbaa-269">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="9fbaa-270">Custo real</span><span class="sxs-lookup"><span data-stu-id="9fbaa-270">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="9fbaa-271">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="9fbaa-271">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="9fbaa-272">Custo real</span><span class="sxs-lookup"><span data-stu-id="9fbaa-272">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="9fbaa-273">Custo real</span><span class="sxs-lookup"><span data-stu-id="9fbaa-273">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fbaa-274">Custo de unidade de atribuição de recursos</span><span class="sxs-lookup"><span data-stu-id="9fbaa-274">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="9fbaa-275">Moeda da unidade de atribuição de recursos</span><span class="sxs-lookup"><span data-stu-id="9fbaa-275">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fbaa-276">Vendas interorganizacionais</span><span class="sxs-lookup"><span data-stu-id="9fbaa-276">Interorganizational sales</span></span></td>
<td><span data-ttu-id="9fbaa-277">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="9fbaa-277">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fbaa-278">Valor real de vendas não faturadas – Faturável para a nova quantidade</span><span class="sxs-lookup"><span data-stu-id="9fbaa-278">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="9fbaa-279">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="9fbaa-279">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fbaa-280">Valor real de vendas não faturadas – Não faturável para a diferença</span><span class="sxs-lookup"><span data-stu-id="9fbaa-280">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="9fbaa-281">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="9fbaa-281">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="9fbaa-282">É confirmada uma fatura e não ocorre nenhuma alteração ou aumento nas horas faturáveis.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-282">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="9fbaa-283">Estorno de vendas não faturadas</span><span class="sxs-lookup"><span data-stu-id="9fbaa-283">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="9fbaa-284">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="9fbaa-284">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="9fbaa-285">Vendas faturadas para marco</span><span class="sxs-lookup"><span data-stu-id="9fbaa-285">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="9fbaa-286">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="9fbaa-286">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="9fbaa-287">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="9fbaa-287">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="9fbaa-288">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="9fbaa-288">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fbaa-289">Vendas faturadas</span><span class="sxs-lookup"><span data-stu-id="9fbaa-289">Billed sales</span></span></td>
<td><span data-ttu-id="9fbaa-290">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="9fbaa-290">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="9fbaa-291">É confirmada uma fatura e ocorre uma diminuição nas horas faturáveis.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-291">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="9fbaa-292">Estorno de vendas não faturadas</span><span class="sxs-lookup"><span data-stu-id="9fbaa-292">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="9fbaa-293">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="9fbaa-293">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="9fbaa-294">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="9fbaa-294">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="9fbaa-295">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="9fbaa-295">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="9fbaa-296">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="9fbaa-296">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="9fbaa-297">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="9fbaa-297">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fbaa-298">Vendas faturadas – Faturável para a nova quantidade</span><span class="sxs-lookup"><span data-stu-id="9fbaa-298">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="9fbaa-299">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="9fbaa-299">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fbaa-300">Vendas não faturadas – Não faturável para a diferença</span><span class="sxs-lookup"><span data-stu-id="9fbaa-300">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="9fbaa-301">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="9fbaa-301">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="9fbaa-302">Uma fatura é corrigida para aumentar a quantidade faturável.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-302">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="9fbaa-303">Vendas faturadas – Estorno</span><span class="sxs-lookup"><span data-stu-id="9fbaa-303">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="9fbaa-304">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="9fbaa-304">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="9fbaa-305">Estorno de vendas faturadas para marco</span><span class="sxs-lookup"><span data-stu-id="9fbaa-305">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="9fbaa-306">Alterar o estado do marco de <strong>Faturado</strong> para <strong>Pronto para faturação</strong></span><span class="sxs-lookup"><span data-stu-id="9fbaa-306">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="9fbaa-307">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="9fbaa-307">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="9fbaa-308">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="9fbaa-308">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="9fbaa-309">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="9fbaa-309">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fbaa-310">Vendas faturadas</span><span class="sxs-lookup"><span data-stu-id="9fbaa-310">Billed sales</span></span></td>
<td><span data-ttu-id="9fbaa-311">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="9fbaa-311">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="9fbaa-312">Uma fatura é corrigida para diminuir a quantidade faturável.</span><span class="sxs-lookup"><span data-stu-id="9fbaa-312">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="9fbaa-313">Vendas faturadas – Estorno</span><span class="sxs-lookup"><span data-stu-id="9fbaa-313">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="9fbaa-314">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="9fbaa-314">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fbaa-315">Vendas faturadas para a nova quantidade</span><span class="sxs-lookup"><span data-stu-id="9fbaa-315">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="9fbaa-316">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="9fbaa-316">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fbaa-317">Vendas não faturadas – Faturável para a diferença</span><span class="sxs-lookup"><span data-stu-id="9fbaa-317">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="9fbaa-318">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="9fbaa-318">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
