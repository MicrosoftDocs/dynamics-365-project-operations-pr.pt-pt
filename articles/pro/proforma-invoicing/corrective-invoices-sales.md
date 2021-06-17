---
title: Faturas corretivas de projeto
description: Este tópico fornece informações sobre como criar e confirmar faturas corretivas no Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: dfa5535597ee6e144259c9246b33075f3492285e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004095"
---
# <a name="corrective-project-invoices"></a><span data-ttu-id="4cb24-103">Faturas corretivas de projeto</span><span class="sxs-lookup"><span data-stu-id="4cb24-103">Corrective project invoices</span></span>

<span data-ttu-id="4cb24-104">_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_</span><span class="sxs-lookup"><span data-stu-id="4cb24-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4cb24-105">Uma fatura de projeto confirmada pode ser corrigida para processar alterações ou créditos conforme negociado com o cliente e gestor de projeto.</span><span class="sxs-lookup"><span data-stu-id="4cb24-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="4cb24-106">Para edição de uma fatura confirmada, abra a fatura confirmada e selecione **Corrigir esta Fatura**.</span><span class="sxs-lookup"><span data-stu-id="4cb24-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="4cb24-107">Esta seleção não está disponível a menos que uma fatura do projeto seja confirmada.</span><span class="sxs-lookup"><span data-stu-id="4cb24-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="4cb24-108">Uma nova fatura é criada a partir da fatura confirmada.</span><span class="sxs-lookup"><span data-stu-id="4cb24-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="4cb24-109">Todos os detalhes da linha de fatura da fatura previamente confirmada são copiados para o novo rascunho.</span><span class="sxs-lookup"><span data-stu-id="4cb24-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="4cb24-110">Seguem-se alguns dos pontos-chave para compreender os detalhes da linha na nova fatura corrigida:</span><span class="sxs-lookup"><span data-stu-id="4cb24-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="4cb24-111">Todas as quantidades são atualizadas para zero.</span><span class="sxs-lookup"><span data-stu-id="4cb24-111">All quantities are updated to zero.</span></span> <span data-ttu-id="4cb24-112">A aplicação pressupõe que todos os itens faturados são totalmente creditados.</span><span class="sxs-lookup"><span data-stu-id="4cb24-112">The application assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="4cb24-113">Se necessário, pode atualizar manualmente estas quantidades para refletir a quantidade que está a ser faturada e não a quantidade que está a ser creditada.</span><span class="sxs-lookup"><span data-stu-id="4cb24-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="4cb24-114">Com base na quantidade que inseriu, a aplicação calcula a quantidade creditada.</span><span class="sxs-lookup"><span data-stu-id="4cb24-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="4cb24-115">Este valor reflete-se nos valores reais que são criados quando a fatura corrigida é confirmada.</span><span class="sxs-lookup"><span data-stu-id="4cb24-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="4cb24-116">Se estiver a fazer alterações ao valor do imposto, tem de introduzir o valor correto do imposto e não o valor do imposto que está a ser creditado.</span><span class="sxs-lookup"><span data-stu-id="4cb24-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="4cb24-117">Os itens de contrato baseados em produtos previamente confirmados não são copiados.</span><span class="sxs-lookup"><span data-stu-id="4cb24-117">Previously confirmed product-based contract lines are not copied over.</span></span> <span data-ttu-id="4cb24-118">As correções de processamento de uma fatura de projeto baseada em produtos não são suportadas.</span><span class="sxs-lookup"><span data-stu-id="4cb24-118">Processing corrections on a product-based project invoice is not supported.</span></span>
- <span data-ttu-id="4cb24-119">As correções de marcos são sempre processadas como créditos completos.</span><span class="sxs-lookup"><span data-stu-id="4cb24-119">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="4cb24-120">Os valores de sinal ou de adiantamento podem ser corrigidos se o cliente tiver sido faturado por um valor incorreto.</span><span class="sxs-lookup"><span data-stu-id="4cb24-120">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="4cb24-121">As reconciliações entre os sinais e os adiantamentos podem ser corrigidas se for utilizado um montante incorreto para conciliar com as acusações de uma fatura previamente confirmada.</span><span class="sxs-lookup"><span data-stu-id="4cb24-121">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4cb24-122">Os detalhes da linha de fatura que são correções a outros encargos já faturados têm o campo **Correção** definido para **Sim**.</span><span class="sxs-lookup"><span data-stu-id="4cb24-122">Invoice line details that are corrections to other already invoiced charges have the field **Correction** set to **Yes**.</span></span> <span data-ttu-id="4cb24-123">As faturas que corrigiram os detalhes da linha de fatura têm um campo chamado **Tem correções** que também está definido para **Sim**.</span><span class="sxs-lookup"><span data-stu-id="4cb24-123">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a><span data-ttu-id="4cb24-124">Valores reais criados quando uma fatura corretiva é confirmada</span><span class="sxs-lookup"><span data-stu-id="4cb24-124">Actuals created when a corrective invoice is confirmed</span></span>

<span data-ttu-id="4cb24-125">A tabela a seguir lista os factos que são criados quando uma fatura corretiva é confirmada.</span><span class="sxs-lookup"><span data-stu-id="4cb24-125">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="4cb24-126">
                    <strong>Cenário</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4cb24-126">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="4cb24-127">
                    <strong>Valores reais criados ao confirmar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4cb24-127">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="4cb24-128">Confirme a correção de um adiantamento ou sinal faturado.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="4cb24-128">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4cb24-129">Uma inversão de vendas não faturada do sinal ou adiantamento que foi criado para a reconciliação.</span><span class="sxs-lookup"><span data-stu-id="4cb24-129">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="4cb24-130">Este montante é positivo porque se destina a anular o negativo que foi criado quando o sinal ou adiantamento foi faturado.</span><span class="sxs-lookup"><span data-stu-id="4cb24-130">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4cb24-131">É criado um valor real de inversão de vendas faturado para o montante do sinal ou adiantamento para inverter as vendas faturadas originais.</span><span class="sxs-lookup"><span data-stu-id="4cb24-131">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4cb24-132">É criado um novo valor real de vendas faturado para o valor corrigido na linha de sinal ou de linha de fatura corrigida com base em adiantamento.</span><span class="sxs-lookup"><span data-stu-id="4cb24-132">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4cb24-133">Um valor real de vendas não faturado de montante negativo da linha de fatura corrigida baseada em sinal ou em adiantamento, que será utilizada para a reconciliação.</span><span class="sxs-lookup"><span data-stu-id="4cb24-133">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="4cb24-134">Confirmação da correção de um sinal ou adiantamento previamente reconciliado.</span><span class="sxs-lookup"><span data-stu-id="4cb24-134">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4cb24-135">Uma inversão de vendas não faturada do sinal ou adiantamento que foi criado para a reconciliação.</span><span class="sxs-lookup"><span data-stu-id="4cb24-135">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="4cb24-136">Este montante é positivo e destina-se a anular o negativo que foi criado quando a reconciliação anterior ocorreu.</span><span class="sxs-lookup"><span data-stu-id="4cb24-136">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4cb24-137">Um valor real de reversão de vendas faturado para o valor da fatura anterior.</span><span class="sxs-lookup"><span data-stu-id="4cb24-137">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4cb24-138">É criado um novo valor real de vendas faturado para o montante de sinal corrigido que é aplicado na fatura corrigida.</span><span class="sxs-lookup"><span data-stu-id="4cb24-138">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4cb24-139">Um valor real de vendas não faturado com um montante negativo do sinal ou em adiantamento restante corrigido, que será utilizada para a reconciliação ou faturas posteriores.</span><span class="sxs-lookup"><span data-stu-id="4cb24-139">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4cb24-140">Faturar o crédito total de uma transação de tempo previamente faturada.</span><span class="sxs-lookup"><span data-stu-id="4cb24-140">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4cb24-141">Uma inversão de vendas faturada para as horas e montante no detalhe de linha original para tempo.</span><span class="sxs-lookup"><span data-stu-id="4cb24-141">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4cb24-142">Um novo valor real de vendas por faturar para as horas e o montante no detalhe de linha da fatura original para tempo.</span><span class="sxs-lookup"><span data-stu-id="4cb24-142">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="4cb24-143">Faturar o crédito parcial numa transação de tempo.</span><span class="sxs-lookup"><span data-stu-id="4cb24-143">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4cb24-144">Uma inversão de vendas faturada para as horas e montante faturados no detalhe de linha original para tempo.</span><span class="sxs-lookup"><span data-stu-id="4cb24-144">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4cb24-145">Um novo valor real de vendas não faturada que é faturável pelas horas e montante no detalhe da linha de fatura editada, uma inversão deste, e um valor real de vendas faturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="4cb24-145">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4cb24-146">Um novo valor real de vendas não faturado que é faturável para as horas e montante restante após a dedução dos valores corrigidos no detalhe da linha de fatura.</span><span class="sxs-lookup"><span data-stu-id="4cb24-146">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4cb24-147">Faturar crédito total de uma transação de despesas previamente faturada.</span><span class="sxs-lookup"><span data-stu-id="4cb24-147">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4cb24-148">Uma inversão de vendas faturada para a quantidade e o montante no detalhe de linha da fatura original para as despesas.</span><span class="sxs-lookup"><span data-stu-id="4cb24-148">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4cb24-149">Um novo valor real de vendas por faturar para a quantidade e o montante no detalhe de linha da fatura original para as despesas.</span><span class="sxs-lookup"><span data-stu-id="4cb24-149">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="4cb24-150">Faturar crédito parcial de uma transação de despesas previamente faturada.</span><span class="sxs-lookup"><span data-stu-id="4cb24-150">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4cb24-151">Uma inversão de vendas faturada para a quantidade e o montante faturado no detalhe de linha da fatura original para uma despesa.</span><span class="sxs-lookup"><span data-stu-id="4cb24-151">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4cb24-152">Um novo valor real de vendas não faturada que é faturável pela quantidade e montante no detalhe da linha de fatura corrigida, uma inversão deste, e um valor real de vendas faturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="4cb24-152">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4cb24-153">Um novo valor real de vendas não faturado que é faturável para a quantidade e montante restante após a dedução dos valores corrigidos no detalhe da linha de fatura.</span><span class="sxs-lookup"><span data-stu-id="4cb24-153">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4cb24-154">Faturação do crédito integral de uma transação material previamente faturada.</span><span class="sxs-lookup"><span data-stu-id="4cb24-154">Invoicing the full credit of a previously invoiced material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4cb24-155">Uma inversão de vendas faturadas para a quantidade e montante no detalhe de linha de fatura para o material.</span><span class="sxs-lookup"><span data-stu-id="4cb24-155">A billed sales reversal for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4cb24-156">Um novo valor real de vendas não faturadas para a quantidade e montante no detalhe de linha de fatura para o material.</span><span class="sxs-lookup"><span data-stu-id="4cb24-156">A new unbilled sales actual for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="4cb24-157">Faturar o crédito parcial numa transação material.</span><span class="sxs-lookup"><span data-stu-id="4cb24-157">Invoicing the partial credit on a material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4cb24-158">Uma inversão de vendas faturadas para a quantidade e montante faturado no detalhe de linha de fatura para o material.</span><span class="sxs-lookup"><span data-stu-id="4cb24-158">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4cb24-159">Um novo valor real de vendas não faturadas é faturável pela quantidade e montante no detalhe da linha de fatura editada, uma inversão desta e um valor real de venda de faturação equivalente.</span><span class="sxs-lookup"><span data-stu-id="4cb24-159">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4cb24-160">Um novo valor real de vendas não faturado que é faturável para a quantidade e montante restante após a dedução dos valores corrigidos no detalhe da linha de fatura.</span><span class="sxs-lookup"><span data-stu-id="4cb24-160">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4cb24-161">Faturar o crédito total de uma transação de honorários previamente faturada.</span><span class="sxs-lookup"><span data-stu-id="4cb24-161">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4cb24-162">Uma inversão de vendas faturada para a quantidade e o montante no detalhe de linha da fatura original para os honorários.</span><span class="sxs-lookup"><span data-stu-id="4cb24-162">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4cb24-163">Um novo valor real de vendas por faturar para a quantidade e o montante no detalhe de linha da fatura original para os honorários.</span><span class="sxs-lookup"><span data-stu-id="4cb24-163">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4cb24-164">Faturar o crédito parcial de uma transação de honorários previamente faturada.</span><span class="sxs-lookup"><span data-stu-id="4cb24-164">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4cb24-165">Uma inversão de vendas faturada para a quantidade e o montante faturado no detalhe de linha da fatura original para honorários.</span><span class="sxs-lookup"><span data-stu-id="4cb24-165">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4cb24-166">Um novo valor real de vendas não faturada que é faturável pela quantidade e montante no detalhe da linha de fatura corretiva editada, uma inversão deste, e um valor real de vendas faturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="4cb24-166">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="4cb24-167">Faturar o crédito total de um marco previamente faturado.</span><span class="sxs-lookup"><span data-stu-id="4cb24-167">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4cb24-168">Uma inversão de vendas faturada para o montante no detalhe de linha original para o marco.</span><span class="sxs-lookup"><span data-stu-id="4cb24-168">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="4cb24-169">O estado da fatura no marco é atualizado de <b>Fatura de cliente publicada</b> para <b>Pronta a faturar</b>.</span><span class="sxs-lookup"><span data-stu-id="4cb24-169">The invoice status of the milestone is updated from <b>Customer Invoice Posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="4cb24-170">Faturar o crédito parcial de um marco previamente faturado.</span><span class="sxs-lookup"><span data-stu-id="4cb24-170">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4cb24-171">Não suportado</span><span class="sxs-lookup"><span data-stu-id="4cb24-171">Unsupported</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="4cb24-172">Créditos e correções de um item de contrato baseado em produto previamente faturado.</span><span class="sxs-lookup"><span data-stu-id="4cb24-172">Credits and corrections of a previously invoiced product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4cb24-173">Não suportado</span><span class="sxs-lookup"><span data-stu-id="4cb24-173">Unsupported</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
