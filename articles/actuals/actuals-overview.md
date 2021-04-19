---
title: Valores Reais
description: Esta tópico fornece informações sobre como trabalhar com valores reais no Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 04/01/2021
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
ms.openlocfilehash: 304c51a4e502ad6ecec1fd821e98d6604ddd59ba
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852558"
---
# <a name="actuals"></a><span data-ttu-id="6c617-103">Valores Reais</span><span class="sxs-lookup"><span data-stu-id="6c617-103">Actuals</span></span> 

<span data-ttu-id="6c617-104">_**Aplica-se a:** Project Operations para cenários baseados em recursos/não armazenados, implementação leve - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="6c617-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6c617-105">Os valores reais representam os progressos financeiros e de programação revistos e aprovados num projeto.</span><span class="sxs-lookup"><span data-stu-id="6c617-105">Actuals represent the reviewed and approved financial and schedule progress on a project.</span></span> <span data-ttu-id="6c617-106">São criados como resultado da aprovação do tempo, despesas, entradas de utilização de materiais e entradas de diário e faturas.</span><span class="sxs-lookup"><span data-stu-id="6c617-106">They are created as a result of approval of time, expense, material usage entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="6c617-107">Envio de linhas do diário e tempo</span><span class="sxs-lookup"><span data-stu-id="6c617-107">Journal lines and time submission</span></span>

<span data-ttu-id="6c617-108">Para mais informações sobre a entrada de hora, consulte [Descrição geral da entrada de hora](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="6c617-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="6c617-109">Hora e materiais</span><span class="sxs-lookup"><span data-stu-id="6c617-109">Time and materials</span></span>

<span data-ttu-id="6c617-110">Quando uma entrada de hora que é submetida está associada a um projeto que é mapeado para um item de contrato de tempo e materiais, o sistema cria duas linhas do diário, uma para o custo e uma para as vendas não faturadas.</span><span class="sxs-lookup"><span data-stu-id="6c617-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="6c617-111">Preço fixo</span><span class="sxs-lookup"><span data-stu-id="6c617-111">Fixed price</span></span>

<span data-ttu-id="6c617-112">Quando uma entrada de hora que é submetida está associada a um projeto que está mapeado para um item de contrato de preço fixo, o sistema cria uma linha do diário para o custo.</span><span class="sxs-lookup"><span data-stu-id="6c617-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="6c617-113">Preço predefinido</span><span class="sxs-lookup"><span data-stu-id="6c617-113">Default pricing</span></span>

<span data-ttu-id="6c617-114">A lógica para criar preços predefinidos reside na linha do diário.</span><span class="sxs-lookup"><span data-stu-id="6c617-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="6c617-115">Os valores do campo da entrada de hora são copiados para a linha do diário.</span><span class="sxs-lookup"><span data-stu-id="6c617-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="6c617-116">Estes valores incluem a data da transação, o item de contrato para o qual o projeto está mapeado e a moeda resulta na lista de preços apropriada.</span><span class="sxs-lookup"><span data-stu-id="6c617-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="6c617-117">Os campos que afetam os preços predefinidos, como **Função** e **Unidade de recursos** são usados para determinar o preço apropriado na linha do diário.</span><span class="sxs-lookup"><span data-stu-id="6c617-117">The fields that affect default pricing, such as **Role** and **Resourcing Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="6c617-118">Pode adicionar um campo personalizado na entrada de hora.</span><span class="sxs-lookup"><span data-stu-id="6c617-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="6c617-119">Se pretender que o valor do campo seja propagado aos valores reais, crie o campo nas tabelas **Valores reais** e **Linha do diário**.</span><span class="sxs-lookup"><span data-stu-id="6c617-119">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="6c617-120">Utilize código personalizado para propagar o valor de campo selecionado da Entrada de Tempo para Valores reais através da linha do diário utilizando as origens de transação.</span><span class="sxs-lookup"><span data-stu-id="6c617-120">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="6c617-121">Para obter mais informações sobre as origens e ligações de transações, consulte [Ligar valores reais a registos originais](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="6c617-121">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="6c617-122">Submissão de linhas do diário e despesas básicas</span><span class="sxs-lookup"><span data-stu-id="6c617-122">Journal lines and basic expense submission</span></span>

<span data-ttu-id="6c617-123">Para mais informações sobre a entrada de despesa, consulte [Descrição geral da despesa](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="6c617-123">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="6c617-124">Hora e materiais</span><span class="sxs-lookup"><span data-stu-id="6c617-124">Time and materials</span></span>

<span data-ttu-id="6c617-125">Quando uma entrada de despesa básica que é submetida está associada a um projeto que é mapeado para um item de contrato de tempo e materiais, o sistema cria duas linhas do diário, uma para o custo e uma para as vendas não faturadas.</span><span class="sxs-lookup"><span data-stu-id="6c617-125">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="6c617-126">Preço fixo</span><span class="sxs-lookup"><span data-stu-id="6c617-126">Fixed price</span></span>

<span data-ttu-id="6c617-127">Quando uma entrada de despesa submetida é ligada a um projeto que está mapeado para um item de contrato de preço fixo, o sistema cria uma linha do diário para o custo.</span><span class="sxs-lookup"><span data-stu-id="6c617-127">When a submitted basic expense entry is linked to a project that's mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="6c617-128">Preço predefinido</span><span class="sxs-lookup"><span data-stu-id="6c617-128">Default pricing</span></span>

<span data-ttu-id="6c617-129">A lógica para introduzir os preços predefinidos para as despesas baseia-se na categoria de despesa.</span><span class="sxs-lookup"><span data-stu-id="6c617-129">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="6c617-130">A data da transação, o item de contrato para o qual o projeto está mapeado e a moeda são utilizados para determinar a lista de preços apropriada.</span><span class="sxs-lookup"><span data-stu-id="6c617-130">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="6c617-131">Os campos que afetam os preços predefinidos, como **Categoria de transação** e **Unidade** são usados para determinar o preço apropriado na linha do diário.</span><span class="sxs-lookup"><span data-stu-id="6c617-131">The fields that affect default pricing, such as **Transaction Category** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="6c617-132">No entanto, isto só funciona quando o método de preços na tabela de preços é **Preço por unidade**.</span><span class="sxs-lookup"><span data-stu-id="6c617-132">However, this only works when the pricing method in the price list is **Price per unit**.</span></span> <span data-ttu-id="6c617-133">Se o método de preços for **A custo** ou **Margem de lucro sobre o custo**, o preço introduzido quando a entrada de despesas é criada é utilizado para o custo e o preço na linha de diário de vendas é calculado com base no método de preços.</span><span class="sxs-lookup"><span data-stu-id="6c617-133">If pricing method is **At cost** or **Markup over cost**, the price entered when the expense entry is created is used for cost and the price on the sales journal line is calculated based on the pricing method.</span></span> 

<span data-ttu-id="6c617-134">Pode adicionar um campo personalizado na entrada de despesas.</span><span class="sxs-lookup"><span data-stu-id="6c617-134">You can add a custom field on the expense entry.</span></span> <span data-ttu-id="6c617-135">Se pretender que o valor do campo seja propagado aos valores reais, crie o campo nas tabelas **Valores reais** e **Linha do diário**.</span><span class="sxs-lookup"><span data-stu-id="6c617-135">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="6c617-136">Utilize código personalizado para propagar o valor de campo selecionado da Entrada de Tempo para Valores reais através da linha do diário utilizando as origens de transação.</span><span class="sxs-lookup"><span data-stu-id="6c617-136">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="6c617-137">Para obter mais informações sobre as origens e ligações de transações, consulte [Ligar valores reais a registos originais](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="6c617-137">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-material-usage-log-submission"></a><span data-ttu-id="6c617-138">Submissão de linhas de diário e de registo de utilização de materiais</span><span class="sxs-lookup"><span data-stu-id="6c617-138">Journal lines and material usage log submission</span></span>

<span data-ttu-id="6c617-139">Para obter mais informações sobre a entrada de despesas, consulte o [Registo de utilização de materiais.](../material/material-usage-log.md)</span><span class="sxs-lookup"><span data-stu-id="6c617-139">For more information about expense entry, see [Material Usage Log](../material/material-usage-log.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="6c617-140">Hora e materiais</span><span class="sxs-lookup"><span data-stu-id="6c617-140">Time and materials</span></span>

<span data-ttu-id="6c617-141">Quando uma entrada de registo de utilização de material submetida está ligada a um projeto que está mapeado para uma linha de contrato de tempo e materiais, o sistema cria duas linhas do diário, uma para custo e outra para vendas não faturadas.</span><span class="sxs-lookup"><span data-stu-id="6c617-141">When a submitted material usage log entry is linked to a project that is mapped to a time and materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="6c617-142">Preço fixo</span><span class="sxs-lookup"><span data-stu-id="6c617-142">Fixed price</span></span>

<span data-ttu-id="6c617-143">Quando uma entrada de registo de utilização de material é ligada a um projeto que está mapeado para um item de contrato de preço fixo, o sistema cria uma linha do diário para o custo.</span><span class="sxs-lookup"><span data-stu-id="6c617-143">When a submitted material usage log entry is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="6c617-144">Preço predefinido</span><span class="sxs-lookup"><span data-stu-id="6c617-144">Default pricing</span></span>

<span data-ttu-id="6c617-145">A lógica para introduzir preços predefinidos para o material baseia-se na combinação do produto e da unidade.</span><span class="sxs-lookup"><span data-stu-id="6c617-145">The logic for entering default prices for material is based on the product and unit combination.</span></span> <span data-ttu-id="6c617-146">A data da transação, o item de contrato para o qual o projeto está mapeado e a moeda são utilizados para determinar a lista de preços apropriada.</span><span class="sxs-lookup"><span data-stu-id="6c617-146">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="6c617-147">Os campos que afetam os preços predefinidos, como **ID do produto** e **Unidade** são usados para determinar o preço apropriado na linha do diário.</span><span class="sxs-lookup"><span data-stu-id="6c617-147">The fields that affect default pricing, such as **Product ID** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="6c617-148">No entanto, isto só funciona para produtos de catálogo.</span><span class="sxs-lookup"><span data-stu-id="6c617-148">However, this only works for catalog products.</span></span> <span data-ttu-id="6c617-149">Para os produtos de write-in, o preço introduzido quando a entrada de registo de utilização do material é criado é utilizado para o custo e preço de venda nas linhas de diário.</span><span class="sxs-lookup"><span data-stu-id="6c617-149">For write-in products, the price entered when the material usage log entry is created is used for cost and sales price on the journal lines.</span></span> 

<span data-ttu-id="6c617-150">Pode adicionar um campo personalizado na entrada **Registo de utilização de material**.</span><span class="sxs-lookup"><span data-stu-id="6c617-150">You can add a custom field on the **Material Usage Log** entry.</span></span> <span data-ttu-id="6c617-151">Se pretender que o valor do campo seja propagado aos valores reais, crie o campo nas tabelas **Valores reais** e **Linha do diário**.</span><span class="sxs-lookup"><span data-stu-id="6c617-151">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="6c617-152">Utilize código personalizado para propagar o valor de campo selecionado da Entrada de Tempo para Valores reais através da linha do diário utilizando as origens de transação.</span><span class="sxs-lookup"><span data-stu-id="6c617-152">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="6c617-153">Para obter mais informações sobre as origens e ligações de transações, consulte [Ligar valores reais a registos originais](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="6c617-153">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="6c617-154">Utilizar diários de entrada para registar custos</span><span class="sxs-lookup"><span data-stu-id="6c617-154">Use entry journals to record costs</span></span>

<span data-ttu-id="6c617-155">Poderá utilizar os diários de entrada para registar o custo ou a receita nas classes de material, taxa, hora, despesa ou imposto.</span><span class="sxs-lookup"><span data-stu-id="6c617-155">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="6c617-156">Os diários podem ser utilizadas para as finalidades seguintes:</span><span class="sxs-lookup"><span data-stu-id="6c617-156">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="6c617-157">Mover os valores reais da transação a partir de outro sistema para o Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="6c617-157">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="6c617-158">Registe os custos que ocorreram noutro sistema.</span><span class="sxs-lookup"><span data-stu-id="6c617-158">Record costs that occurred in another system.</span></span> <span data-ttu-id="6c617-159">Estes custos podem incluir os custos de aprovisionamento ou subcontratação.</span><span class="sxs-lookup"><span data-stu-id="6c617-159">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6c617-160">A aplicação não valida o tipo de linha de diário ou o preço relacionado que é introduzido na linha do diário.</span><span class="sxs-lookup"><span data-stu-id="6c617-160">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="6c617-161">Assim, só um utilizador plenamente consciente do impacto contabilístico que os valores reais têm no projeto deve utilizar diários de entrada para criar valores reais.</span><span class="sxs-lookup"><span data-stu-id="6c617-161">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="6c617-162">Dado o impacto deste tipo de diário, deve escolher cuidadosamente quem tem acesso para criar diários de entrada.</span><span class="sxs-lookup"><span data-stu-id="6c617-162">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>

## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="6c617-163">Registar os valores reais baseado nos eventos do projeto</span><span class="sxs-lookup"><span data-stu-id="6c617-163">Record actuals based on project events</span></span>

<span data-ttu-id="6c617-164">O Project Operations regista as transações financeiras que ocorrem durante um projeto.</span><span class="sxs-lookup"><span data-stu-id="6c617-164">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="6c617-165">Estas transações são registadas como reais.</span><span class="sxs-lookup"><span data-stu-id="6c617-165">These transactions are recorded as actuals.</span></span> <span data-ttu-id="6c617-166">As tabelas seguintes mostram os diferentes tipos de valores reais criados, dependendo do facto de o projeto ser um projeto de tempo e material ou de preço fixo, que se encontra na fase pré-venda, ou é um projeto interno.</span><span class="sxs-lookup"><span data-stu-id="6c617-166">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="6c617-167">O recurso pertence à mesma unidade organizacional que a unidade organizacional do projeto</span><span class="sxs-lookup"><span data-stu-id="6c617-167">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="6c617-168">Evento</span><span class="sxs-lookup"><span data-stu-id="6c617-168">Event</span></span></th>
<th colspan="4"><span data-ttu-id="6c617-169">Projeto faturável ou vendido</span><span class="sxs-lookup"><span data-stu-id="6c617-169">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="6c617-170">Projeto na fase pré-venda</span><span class="sxs-lookup"><span data-stu-id="6c617-170">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="6c617-171">Projeto interno</span><span class="sxs-lookup"><span data-stu-id="6c617-171">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="6c617-172">Hora e materiais</span><span class="sxs-lookup"><span data-stu-id="6c617-172">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="6c617-173">Preço fixo</span><span class="sxs-lookup"><span data-stu-id="6c617-173">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="6c617-174">Valores Reais</span><span class="sxs-lookup"><span data-stu-id="6c617-174">Actuals</span></span></th>
<th><span data-ttu-id="6c617-175">Moeda da transação</span><span class="sxs-lookup"><span data-stu-id="6c617-175">Transaction currency</span></span></th>
<th><span data-ttu-id="6c617-176">Preço fixo</span><span class="sxs-lookup"><span data-stu-id="6c617-176">Fixed price</span></span></th>
<th><span data-ttu-id="6c617-177">Moeda da transação</span><span class="sxs-lookup"><span data-stu-id="6c617-177">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6c617-178">É criada uma entrada de hora.</span><span class="sxs-lookup"><span data-stu-id="6c617-178">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="6c617-179">Sem atividade na entidade Valores Reais</span><span class="sxs-lookup"><span data-stu-id="6c617-179">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c617-180">É submetida uma entrada de hora.</span><span class="sxs-lookup"><span data-stu-id="6c617-180">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="6c617-181">Sem atividade na entidade Valores Reais</span><span class="sxs-lookup"><span data-stu-id="6c617-181">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="6c617-182">A hora é aprovada e não ocorre nenhuma alteração ou aumento nas horas faturáveis durante a aprovação.</span><span class="sxs-lookup"><span data-stu-id="6c617-182">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="6c617-183">Custo real</span><span class="sxs-lookup"><span data-stu-id="6c617-183">Cost actual</span></span></td>
<td><span data-ttu-id="6c617-184">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="6c617-184">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="6c617-185">Custo real</span><span class="sxs-lookup"><span data-stu-id="6c617-185">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="6c617-186">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="6c617-186">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="6c617-187">Custo real</span><span class="sxs-lookup"><span data-stu-id="6c617-187">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="6c617-188">Custo real</span><span class="sxs-lookup"><span data-stu-id="6c617-188">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c617-189">Valor real de vendas não faturadas – Faturável</span><span class="sxs-lookup"><span data-stu-id="6c617-189">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="6c617-190">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="6c617-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="6c617-191">A hora é aprovada e ocorre uma diminuição nas horas faturáveis durante a aprovação.</span><span class="sxs-lookup"><span data-stu-id="6c617-191">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="6c617-192">Custo real</span><span class="sxs-lookup"><span data-stu-id="6c617-192">Cost actual</span></span></td>
<td><span data-ttu-id="6c617-193">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="6c617-193">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="6c617-194">Custo real</span><span class="sxs-lookup"><span data-stu-id="6c617-194">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="6c617-195">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="6c617-195">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="6c617-196">Custo real</span><span class="sxs-lookup"><span data-stu-id="6c617-196">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="6c617-197">Custo real</span><span class="sxs-lookup"><span data-stu-id="6c617-197">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c617-198">Valor real de vendas não faturadas – Faturável para a nova quantidade</span><span class="sxs-lookup"><span data-stu-id="6c617-198">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="6c617-199">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="6c617-199">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c617-200">Valor real de vendas não faturadas – Não faturável para a diferença</span><span class="sxs-lookup"><span data-stu-id="6c617-200">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="6c617-201">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="6c617-201">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="6c617-202">É confirmada uma fatura e não ocorre nenhuma alteração ou aumento nas horas faturáveis.</span><span class="sxs-lookup"><span data-stu-id="6c617-202">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="6c617-203">Estorno de vendas não faturadas</span><span class="sxs-lookup"><span data-stu-id="6c617-203">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="6c617-204">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="6c617-204">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="6c617-205">Vendas faturadas para marco</span><span class="sxs-lookup"><span data-stu-id="6c617-205">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="6c617-206">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="6c617-206">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="6c617-207">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="6c617-207">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="6c617-208">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="6c617-208">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c617-209">Vendas faturadas</span><span class="sxs-lookup"><span data-stu-id="6c617-209">Billed sales</span></span></td>
<td><span data-ttu-id="6c617-210">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="6c617-210">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="6c617-211">É confirmada uma fatura e ocorre uma diminuição nas horas faturáveis.</span><span class="sxs-lookup"><span data-stu-id="6c617-211">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="6c617-212">Estorno de vendas não faturadas</span><span class="sxs-lookup"><span data-stu-id="6c617-212">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="6c617-213">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="6c617-213">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="6c617-214">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="6c617-214">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="6c617-215">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="6c617-215">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="6c617-216">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="6c617-216">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="6c617-217">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="6c617-217">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c617-218">Vendas faturadas – Faturável para a nova quantidade</span><span class="sxs-lookup"><span data-stu-id="6c617-218">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="6c617-219">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="6c617-219">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c617-220">Vendas não faturadas – Não faturável para a diferença</span><span class="sxs-lookup"><span data-stu-id="6c617-220">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="6c617-221">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="6c617-221">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="6c617-222">Uma fatura é corrigida para aumentar a quantidade faturável.</span><span class="sxs-lookup"><span data-stu-id="6c617-222">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="6c617-223">Vendas faturadas – Estorno</span><span class="sxs-lookup"><span data-stu-id="6c617-223">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="6c617-224">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="6c617-224">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="6c617-225">Estorno de vendas faturadas para marco</span><span class="sxs-lookup"><span data-stu-id="6c617-225">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="6c617-226">Alterar o estado do marco de <strong>Faturado</strong> para <strong>Pronto para faturação</strong></span><span class="sxs-lookup"><span data-stu-id="6c617-226">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="6c617-227">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="6c617-227">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="6c617-228">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="6c617-228">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="6c617-229">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="6c617-229">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c617-230">Vendas faturadas</span><span class="sxs-lookup"><span data-stu-id="6c617-230">Billed sales</span></span></td>
<td><span data-ttu-id="6c617-231">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="6c617-231">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="6c617-232">Uma fatura é corrigida para diminuir a quantidade faturável.</span><span class="sxs-lookup"><span data-stu-id="6c617-232">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="6c617-233">Vendas faturadas – Estorno</span><span class="sxs-lookup"><span data-stu-id="6c617-233">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="6c617-234">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="6c617-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c617-235">Vendas faturadas para a nova quantidade</span><span class="sxs-lookup"><span data-stu-id="6c617-235">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="6c617-236">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="6c617-236">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c617-237">Vendas não faturadas – Faturável para a diferença</span><span class="sxs-lookup"><span data-stu-id="6c617-237">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="6c617-238">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="6c617-238">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="6c617-239">O recurso pertence a uma unidade organizacional que difere da unidade organizacional do projeto</span><span class="sxs-lookup"><span data-stu-id="6c617-239">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="6c617-240">Evento</span><span class="sxs-lookup"><span data-stu-id="6c617-240">Event</span></span></th>
<th colspan="4"><span data-ttu-id="6c617-241">Projeto faturável ou vendido</span><span class="sxs-lookup"><span data-stu-id="6c617-241">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="6c617-242">Projeto na fase pré-venda</span><span class="sxs-lookup"><span data-stu-id="6c617-242">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="6c617-243">Projeto interno</span><span class="sxs-lookup"><span data-stu-id="6c617-243">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="6c617-244">Hora e materiais</span><span class="sxs-lookup"><span data-stu-id="6c617-244">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="6c617-245">Preço fixo</span><span class="sxs-lookup"><span data-stu-id="6c617-245">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="6c617-246">Valores Reais</span><span class="sxs-lookup"><span data-stu-id="6c617-246">Actuals</span></span></th>
<th><span data-ttu-id="6c617-247">Moeda da transação</span><span class="sxs-lookup"><span data-stu-id="6c617-247">Transaction currency</span></span></th>
<th><span data-ttu-id="6c617-248">Preço fixo</span><span class="sxs-lookup"><span data-stu-id="6c617-248">Fixed price</span></span></th>
<th><span data-ttu-id="6c617-249">Moeda da transação</span><span class="sxs-lookup"><span data-stu-id="6c617-249">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6c617-250">É criada uma entrada de hora.</span><span class="sxs-lookup"><span data-stu-id="6c617-250">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="6c617-251">Sem atividade na entidade Valores Reais</span><span class="sxs-lookup"><span data-stu-id="6c617-251">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c617-252">É submetida uma entrada de hora.</span><span class="sxs-lookup"><span data-stu-id="6c617-252">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="6c617-253">Sem atividade na entidade Valores Reais</span><span class="sxs-lookup"><span data-stu-id="6c617-253">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="6c617-254">A hora é aprovada e não ocorre nenhuma alteração ou aumento nas horas faturáveis durante a aprovação.</span><span class="sxs-lookup"><span data-stu-id="6c617-254">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="6c617-255">Custo real</span><span class="sxs-lookup"><span data-stu-id="6c617-255">Cost actual</span></span></td>
<td><span data-ttu-id="6c617-256">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="6c617-256">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="6c617-257">Custo real</span><span class="sxs-lookup"><span data-stu-id="6c617-257">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="6c617-258">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="6c617-258">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="6c617-259">Custo real</span><span class="sxs-lookup"><span data-stu-id="6c617-259">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="6c617-260">Custo real</span><span class="sxs-lookup"><span data-stu-id="6c617-260">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c617-261">Valor real de vendas não faturadas – Faturável</span><span class="sxs-lookup"><span data-stu-id="6c617-261">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="6c617-262">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="6c617-262">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c617-263">Custo de unidade de atribuição de recursos</span><span class="sxs-lookup"><span data-stu-id="6c617-263">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="6c617-264">Moeda da unidade de atribuição de recursos</span><span class="sxs-lookup"><span data-stu-id="6c617-264">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c617-265">Vendas interorganizacionais</span><span class="sxs-lookup"><span data-stu-id="6c617-265">Interorganizational sales</span></span></td>
<td><span data-ttu-id="6c617-266">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="6c617-266">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="6c617-267">A hora é aprovada e ocorre uma diminuição nas horas faturáveis durante a aprovação.</span><span class="sxs-lookup"><span data-stu-id="6c617-267">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="6c617-268">Custo real</span><span class="sxs-lookup"><span data-stu-id="6c617-268">Cost actual</span></span></td>
<td><span data-ttu-id="6c617-269">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="6c617-269">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="6c617-270">Custo real</span><span class="sxs-lookup"><span data-stu-id="6c617-270">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="6c617-271">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="6c617-271">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="6c617-272">Custo real</span><span class="sxs-lookup"><span data-stu-id="6c617-272">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="6c617-273">Custo real</span><span class="sxs-lookup"><span data-stu-id="6c617-273">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c617-274">Custo de unidade de atribuição de recursos</span><span class="sxs-lookup"><span data-stu-id="6c617-274">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="6c617-275">Moeda da unidade de atribuição de recursos</span><span class="sxs-lookup"><span data-stu-id="6c617-275">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c617-276">Vendas interorganizacionais</span><span class="sxs-lookup"><span data-stu-id="6c617-276">Interorganizational sales</span></span></td>
<td><span data-ttu-id="6c617-277">Moeda da unidade de contratação</span><span class="sxs-lookup"><span data-stu-id="6c617-277">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c617-278">Valor real de vendas não faturadas – Faturável para a nova quantidade</span><span class="sxs-lookup"><span data-stu-id="6c617-278">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="6c617-279">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="6c617-279">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c617-280">Valor real de vendas não faturadas – Não faturável para a diferença</span><span class="sxs-lookup"><span data-stu-id="6c617-280">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="6c617-281">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="6c617-281">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="6c617-282">É confirmada uma fatura e não ocorre nenhuma alteração ou aumento nas horas faturáveis.</span><span class="sxs-lookup"><span data-stu-id="6c617-282">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="6c617-283">Estorno de vendas não faturadas</span><span class="sxs-lookup"><span data-stu-id="6c617-283">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="6c617-284">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="6c617-284">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="6c617-285">Vendas faturadas para marco</span><span class="sxs-lookup"><span data-stu-id="6c617-285">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="6c617-286">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="6c617-286">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="6c617-287">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="6c617-287">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="6c617-288">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="6c617-288">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c617-289">Vendas faturadas</span><span class="sxs-lookup"><span data-stu-id="6c617-289">Billed sales</span></span></td>
<td><span data-ttu-id="6c617-290">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="6c617-290">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="6c617-291">É confirmada uma fatura e ocorre uma diminuição nas horas faturáveis.</span><span class="sxs-lookup"><span data-stu-id="6c617-291">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="6c617-292">Estorno de vendas não faturadas</span><span class="sxs-lookup"><span data-stu-id="6c617-292">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="6c617-293">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="6c617-293">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="6c617-294">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="6c617-294">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="6c617-295">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="6c617-295">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="6c617-296">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="6c617-296">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="6c617-297">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="6c617-297">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c617-298">Vendas faturadas – Faturável para a nova quantidade</span><span class="sxs-lookup"><span data-stu-id="6c617-298">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="6c617-299">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="6c617-299">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c617-300">Vendas não faturadas – Não faturável para a diferença</span><span class="sxs-lookup"><span data-stu-id="6c617-300">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="6c617-301">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="6c617-301">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="6c617-302">Uma fatura é corrigida para aumentar a quantidade faturável.</span><span class="sxs-lookup"><span data-stu-id="6c617-302">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="6c617-303">Vendas faturadas – Estorno</span><span class="sxs-lookup"><span data-stu-id="6c617-303">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="6c617-304">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="6c617-304">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="6c617-305">Estorno de vendas faturadas para marco</span><span class="sxs-lookup"><span data-stu-id="6c617-305">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="6c617-306">Alterar o estado do marco de <strong>Faturado</strong> para <strong>Pronto para faturação</strong></span><span class="sxs-lookup"><span data-stu-id="6c617-306">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="6c617-307">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="6c617-307">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="6c617-308">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="6c617-308">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="6c617-309">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="6c617-309">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c617-310">Vendas faturadas</span><span class="sxs-lookup"><span data-stu-id="6c617-310">Billed sales</span></span></td>
<td><span data-ttu-id="6c617-311">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="6c617-311">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="6c617-312">Uma fatura é corrigida para diminuir a quantidade faturável.</span><span class="sxs-lookup"><span data-stu-id="6c617-312">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="6c617-313">Vendas faturadas – Estorno</span><span class="sxs-lookup"><span data-stu-id="6c617-313">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="6c617-314">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="6c617-314">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c617-315">Vendas faturadas para a nova quantidade</span><span class="sxs-lookup"><span data-stu-id="6c617-315">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="6c617-316">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="6c617-316">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="6c617-317">Vendas não faturadas – Faturável para a diferença</span><span class="sxs-lookup"><span data-stu-id="6c617-317">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="6c617-318">Moeda do contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="6c617-318">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
