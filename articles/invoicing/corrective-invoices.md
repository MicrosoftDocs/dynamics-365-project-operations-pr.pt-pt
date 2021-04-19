---
title: Criar faturas de correção baseadas em projeto
description: Esta tópico fornece informações sobre faturas corretivas no Project Operations.
author: rumant
manager: Annbe
ms.date: 03/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 32772d64b3fc77f0af9618edff40e3b295593454
ms.sourcegitcommit: 504c09365bf404c1f1aa9b5034c1e1e5bc9d0d54
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788886"
---
# <a name="create-corrective-project-based-invoices"></a><span data-ttu-id="0cb23-103">Criar faturas de correção baseadas em projeto</span><span class="sxs-lookup"><span data-stu-id="0cb23-103">Create corrective project-based invoices</span></span> 

<span data-ttu-id="0cb23-104">_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_</span><span class="sxs-lookup"><span data-stu-id="0cb23-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="0cb23-105">Uma fatura de projeto confirmada pode ser corrigida para processar alterações ou créditos conforme negociado com o cliente e gestor de projeto.</span><span class="sxs-lookup"><span data-stu-id="0cb23-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="0cb23-106">Para edição de uma fatura confirmada, abra a fatura confirmada e selecione **Corrigir esta Fatura**.</span><span class="sxs-lookup"><span data-stu-id="0cb23-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="0cb23-107">Esta seleção não está disponível a menos que uma fatura do projeto seja confirmada.</span><span class="sxs-lookup"><span data-stu-id="0cb23-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="0cb23-108">Uma nova fatura é criada a partir da fatura confirmada.</span><span class="sxs-lookup"><span data-stu-id="0cb23-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="0cb23-109">Todos os detalhes da linha de fatura da fatura previamente confirmada são copiados para o novo rascunho.</span><span class="sxs-lookup"><span data-stu-id="0cb23-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="0cb23-110">Seguem-se alguns pontos-chave para o ajudar a compreender mais sobre os detalhes da linha na nova fatura corrigida:</span><span class="sxs-lookup"><span data-stu-id="0cb23-110">The following are some key points to help you understand more about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="0cb23-111">Todas as quantidades são atualizadas para zero.</span><span class="sxs-lookup"><span data-stu-id="0cb23-111">All quantities are updated to zero.</span></span> <span data-ttu-id="0cb23-112">Isto pressupõe que todos os itens faturados são totalmente creditados.</span><span class="sxs-lookup"><span data-stu-id="0cb23-112">This assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="0cb23-113">Se necessário, pode atualizar manualmente estas quantidades para refletir a quantidade que está a ser faturada e não a quantidade que está a ser creditada.</span><span class="sxs-lookup"><span data-stu-id="0cb23-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="0cb23-114">Com base na quantidade que inseriu, a aplicação calcula a quantidade creditada.</span><span class="sxs-lookup"><span data-stu-id="0cb23-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="0cb23-115">Este valor reflete-se nos valores reais que são criados quando a fatura corrigida é confirmada.</span><span class="sxs-lookup"><span data-stu-id="0cb23-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="0cb23-116">Se estiver a fazer alterações ao valor do imposto, tem de introduzir o valor correto do imposto e não o valor do imposto que está a ser creditado.</span><span class="sxs-lookup"><span data-stu-id="0cb23-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="0cb23-117">As correções de marcos são sempre processadas como créditos completos.</span><span class="sxs-lookup"><span data-stu-id="0cb23-117">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="0cb23-118">Os valores de sinal ou de adiantamento podem ser corrigidos se o cliente tiver sido faturado por um valor incorreto.</span><span class="sxs-lookup"><span data-stu-id="0cb23-118">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="0cb23-119">As reconciliações entre os sinais e os adiantamentos podem ser corrigidas se for utilizado um montante incorreto para conciliar com as acusações de uma fatura previamente confirmada.</span><span class="sxs-lookup"><span data-stu-id="0cb23-119">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0cb23-120">Os detalhes da linha de fatura que são correções a outros encargos já faturados têm o campo de **Correção** definido para **Sim**.</span><span class="sxs-lookup"><span data-stu-id="0cb23-120">Invoice line details that are corrections to other already invoiced charges have the **Correction** field set to **Yes**.</span></span> <span data-ttu-id="0cb23-121">As faturas que corrigiram os detalhes da linha de fatura têm um campo chamado **Tem correções** que também está definido para **Sim**.</span><span class="sxs-lookup"><span data-stu-id="0cb23-121">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a><span data-ttu-id="0cb23-122">Valores reais criados na confirmação de uma fatura corretiva</span><span class="sxs-lookup"><span data-stu-id="0cb23-122">Actuals created on confirmation of a corrective invoice</span></span>

<span data-ttu-id="0cb23-123">A tabela a seguir lista os factos que são criados quando uma fatura corretiva é confirmada.</span><span class="sxs-lookup"><span data-stu-id="0cb23-123">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="0cb23-124">
                    <strong>Cenário</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0cb23-124">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="0cb23-125">
                    <strong>Valores reais criados ao confirmar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0cb23-125">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="0cb23-126">Confirme a correção de um adiantamento ou sinal faturado.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="0cb23-126">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0cb23-127">Uma inversão de vendas não faturada do sinal ou adiantamento que foi criado para a reconciliação.</span><span class="sxs-lookup"><span data-stu-id="0cb23-127">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="0cb23-128">Este montante é positivo porque se destina a anular o negativo que foi criado quando o sinal ou adiantamento foi faturado.</span><span class="sxs-lookup"><span data-stu-id="0cb23-128">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0cb23-129">É criado um valor real de inversão de vendas faturado para o montante do sinal ou adiantamento para inverter as vendas faturadas originais.</span><span class="sxs-lookup"><span data-stu-id="0cb23-129">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0cb23-130">É criado um novo valor real de vendas faturado para o valor corrigido na linha de sinal ou de linha de fatura corrigida com base em adiantamento.</span><span class="sxs-lookup"><span data-stu-id="0cb23-130">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0cb23-131">Um valor real de vendas não faturado de montante negativo da linha de fatura corrigida baseada em sinal ou em adiantamento, que será utilizada para a reconciliação.</span><span class="sxs-lookup"><span data-stu-id="0cb23-131">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="0cb23-132">Confirmação da correção de um sinal ou adiantamento previamente reconciliado.</span><span class="sxs-lookup"><span data-stu-id="0cb23-132">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0cb23-133">Uma inversão de vendas não faturada do sinal ou adiantamento que foi criado para a reconciliação.</span><span class="sxs-lookup"><span data-stu-id="0cb23-133">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="0cb23-134">Este montante é positivo e destina-se a anular o negativo que foi criado quando a reconciliação anterior ocorreu.</span><span class="sxs-lookup"><span data-stu-id="0cb23-134">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0cb23-135">Um valor real de reversão de vendas faturado para o valor da fatura anterior.</span><span class="sxs-lookup"><span data-stu-id="0cb23-135">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0cb23-136">É criado um novo valor real de vendas faturado para o montante de sinal corrigido que é aplicado na fatura corrigida.</span><span class="sxs-lookup"><span data-stu-id="0cb23-136">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0cb23-137">Um valor real de vendas não faturado com um montante negativo do sinal ou em adiantamento restante corrigido, que será utilizada para a reconciliação ou faturas posteriores.</span><span class="sxs-lookup"><span data-stu-id="0cb23-137">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0cb23-138">Faturar o crédito total de uma transação de tempo previamente faturada.</span><span class="sxs-lookup"><span data-stu-id="0cb23-138">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0cb23-139">Uma inversão de vendas faturada para as horas e montante no detalhe de linha original para tempo.</span><span class="sxs-lookup"><span data-stu-id="0cb23-139">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0cb23-140">Um novo valor real de vendas por faturar para as horas e o montante no detalhe de linha da fatura original para tempo.</span><span class="sxs-lookup"><span data-stu-id="0cb23-140">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="0cb23-141">Faturar o crédito parcial numa transação de tempo.</span><span class="sxs-lookup"><span data-stu-id="0cb23-141">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0cb23-142">Uma inversão de vendas faturada para as horas e montante faturados no detalhe de linha original para tempo.</span><span class="sxs-lookup"><span data-stu-id="0cb23-142">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0cb23-143">Um novo valor real de vendas não faturada que é faturável pelas horas e montante no detalhe da linha de fatura editada, uma inversão deste, e um valor real de vendas faturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="0cb23-143">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0cb23-144">Um novo valor real de vendas não faturado que é faturável para as horas e montante restante após a dedução dos valores corrigidos no detalhe da linha de fatura.</span><span class="sxs-lookup"><span data-stu-id="0cb23-144">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0cb23-145">Faturar crédito total de uma transação de despesas previamente faturada.</span><span class="sxs-lookup"><span data-stu-id="0cb23-145">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0cb23-146">Uma inversão de vendas faturada para a quantidade e o montante no detalhe de linha da fatura original para as despesas.</span><span class="sxs-lookup"><span data-stu-id="0cb23-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0cb23-147">Um novo valor real de vendas por faturar para a quantidade e o montante no detalhe de linha da fatura original para as despesas.</span><span class="sxs-lookup"><span data-stu-id="0cb23-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="0cb23-148">Faturar crédito parcial de uma transação de despesas previamente faturada.</span><span class="sxs-lookup"><span data-stu-id="0cb23-148">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0cb23-149">Uma inversão de vendas faturada para a quantidade e o montante faturado no detalhe de linha da fatura original para uma despesa.</span><span class="sxs-lookup"><span data-stu-id="0cb23-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0cb23-150">Um novo valor real de vendas não faturada que é faturável pela quantidade e montante no detalhe da linha de fatura corrigida, uma inversão deste, e um valor real de vendas faturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="0cb23-150">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0cb23-151">Um novo valor real de vendas não faturado que é faturável para a quantidade e montante restante após a dedução dos valores corrigidos no detalhe da linha de fatura.</span><span class="sxs-lookup"><span data-stu-id="0cb23-151">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0cb23-152">Faturar o crédito total de uma transação de honorários previamente faturada.</span><span class="sxs-lookup"><span data-stu-id="0cb23-152">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0cb23-153">Uma inversão de vendas faturada para a quantidade e o montante no detalhe de linha da fatura original para os honorários.</span><span class="sxs-lookup"><span data-stu-id="0cb23-153">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0cb23-154">Um novo valor real de vendas por faturar para a quantidade e o montante no detalhe de linha da fatura original para os honorários.</span><span class="sxs-lookup"><span data-stu-id="0cb23-154">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0cb23-155">Faturar o crédito parcial de uma transação de honorários previamente faturada.</span><span class="sxs-lookup"><span data-stu-id="0cb23-155">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0cb23-156">Uma inversão de vendas faturada para a quantidade e o montante faturado no detalhe de linha da fatura original para honorários.</span><span class="sxs-lookup"><span data-stu-id="0cb23-156">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0cb23-157">Um novo valor real de vendas não faturada que é faturável pela quantidade e montante no detalhe da linha de fatura corretiva editada, uma inversão deste, e um valor real de vendas faturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="0cb23-157">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="0cb23-158">Faturar o crédito total de um marco previamente faturado.</span><span class="sxs-lookup"><span data-stu-id="0cb23-158">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0cb23-159">Uma inversão de vendas faturada para o montante no detalhe de linha original para o marco.</span><span class="sxs-lookup"><span data-stu-id="0cb23-159">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="0cb23-160">O estado da fatura no marco é atualizado a partir da fatura do <b>Fatura de cliente publicada</b> para <b>Pronta a faturar</b>.</span><span class="sxs-lookup"><span data-stu-id="0cb23-160">The invoice status on the milestone is updated from <b>Customer invoice posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="0cb23-161">Faturar o crédito parcial de um marco previamente faturado.</span><span class="sxs-lookup"><span data-stu-id="0cb23-161">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="0cb23-162">Não suportado</span><span class="sxs-lookup"><span data-stu-id="0cb23-162">Unsupported</span></span> </p>
            </td>
        </tr>        
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
