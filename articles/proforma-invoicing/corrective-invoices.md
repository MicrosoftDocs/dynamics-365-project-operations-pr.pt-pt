---
title: Faturas corretivas baseadas em projeto
description: Esta tópico fornece informações sobre como criar e confirmar faturas corretivas baseadas em projetos no Project Operations.
author: rumant
manager: Annbe
ms.date: 03/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fc96bb40f5207efc381986d46a3e37dfc1dc111c
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867055"
---
# <a name="corrective-project-based-invoices"></a><span data-ttu-id="406da-103">Faturas corretivas baseadas em projeto</span><span class="sxs-lookup"><span data-stu-id="406da-103">Corrective project-based invoices</span></span>

<span data-ttu-id="406da-104">_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_</span><span class="sxs-lookup"><span data-stu-id="406da-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="406da-105">Uma fatura de projeto confirmada pode ser corrigida para processar alterações ou créditos conforme negociado com o cliente e gestor de projeto.</span><span class="sxs-lookup"><span data-stu-id="406da-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="406da-106">Para edição de uma fatura confirmada, abra a fatura confirmada e selecione **Corrigir esta Fatura**.</span><span class="sxs-lookup"><span data-stu-id="406da-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="406da-107">Esta seleção não está disponível a menos que uma fatura do projeto seja confirmada ou a fatura baseada no projeto tenha adiantamentos ou retentores ou reconciliações de adiantamentos ou retentores.</span><span class="sxs-lookup"><span data-stu-id="406da-107">This selection isn't available unless a project invoice is confirmed or the project-based invoice has advances or retainers or reconciliations of advances or retainers.</span></span>

<span data-ttu-id="406da-108">Uma nova fatura é criada a partir da fatura confirmada.</span><span class="sxs-lookup"><span data-stu-id="406da-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="406da-109">Todos os detalhes da linha de fatura da fatura previamente confirmada são copiados para o novo rascunho.</span><span class="sxs-lookup"><span data-stu-id="406da-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="406da-110">Seguem-se alguns dos pontos-chave para compreender os detalhes da linha na nova fatura corrigida:</span><span class="sxs-lookup"><span data-stu-id="406da-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="406da-111">Todas as quantidades são atualizadas para zero.</span><span class="sxs-lookup"><span data-stu-id="406da-111">All quantities are updated to zero.</span></span> <span data-ttu-id="406da-112">Dynamics 365 Project Operations pressupõe que todos os itens faturados são totalmente creditados.</span><span class="sxs-lookup"><span data-stu-id="406da-112">Dynamics 365 Project Operations assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="406da-113">Se necessário, pode atualizar manualmente estas quantidades para refletir a quantidade que está a ser faturada e não a quantidade que está a ser creditada.</span><span class="sxs-lookup"><span data-stu-id="406da-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="406da-114">Com base na quantidade que inseriu, a aplicação calcula a quantidade creditada.</span><span class="sxs-lookup"><span data-stu-id="406da-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="406da-115">Este valor reflete-se nos valores reais que são criados quando a fatura corrigida é confirmada.</span><span class="sxs-lookup"><span data-stu-id="406da-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="406da-116">Se estiver a fazer alterações ao valor do imposto, tem de introduzir o valor correto do imposto e não o valor do imposto que está a ser creditado.</span><span class="sxs-lookup"><span data-stu-id="406da-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="406da-117">As correções de marcos são sempre processadas como créditos completos.</span><span class="sxs-lookup"><span data-stu-id="406da-117">Milestone corrections are always processed as full credits.</span></span>


> [!IMPORTANT]
> <span data-ttu-id="406da-118">Para detalhes da linha de fatura que são correções a outros encargos já faturados, o campo de **Correção** é definido para **Sim**.</span><span class="sxs-lookup"><span data-stu-id="406da-118">For invoice line details that are corrections to other already invoiced charges, the **Correction** field is set to **Yes**.</span></span> <span data-ttu-id="406da-119">Para faturas que têm detalhes de linha de fatura corrigidos, o campo de **Tem correções** é definido para **Sim**.</span><span class="sxs-lookup"><span data-stu-id="406da-119">For invoices that have corrected invoice line details, the **Has corrections** field is set to **Yes**.</span></span>

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a><span data-ttu-id="406da-120">Valores reais criados quando uma fatura corretiva é confirmada</span><span class="sxs-lookup"><span data-stu-id="406da-120">Actuals created when a corrective invoice is confirmed</span></span>

<span data-ttu-id="406da-121">A tabela a seguir lista os factos que são criados quando uma fatura corretiva é confirmada.</span><span class="sxs-lookup"><span data-stu-id="406da-121">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="406da-122">
                    <strong>Cenário</strong>
                </span><span class="sxs-lookup"><span data-stu-id="406da-122">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="406da-123">
                    <strong>Valores reais criados ao confirmar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="406da-123">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="406da-124">Faturar o crédito total de uma transação de tempo previamente faturada.</span><span class="sxs-lookup"><span data-stu-id="406da-124">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="406da-125">Uma inversão de vendas faturada para as horas e montante no detalhe de linha original para tempo.</span><span class="sxs-lookup"><span data-stu-id="406da-125">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="406da-126">Um novo valor real de vendas por faturar para as horas e o montante no detalhe de linha da fatura original para tempo.</span><span class="sxs-lookup"><span data-stu-id="406da-126">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="406da-127">Faturar o crédito parcial numa transação de tempo.</span><span class="sxs-lookup"><span data-stu-id="406da-127">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="406da-128">Uma inversão de vendas faturada para as horas e montante faturados no detalhe de linha original para tempo.</span><span class="sxs-lookup"><span data-stu-id="406da-128">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="406da-129">Um novo valor real de vendas não faturada que é faturável pelas horas e montante no detalhe da linha de fatura editada, uma inversão deste, e um valor real de vendas faturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="406da-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="406da-130">Um novo valor real de vendas não faturado que é faturável para as horas e montante restante após a dedução dos valores corrigidos no detalhe da linha de fatura.</span><span class="sxs-lookup"><span data-stu-id="406da-130">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="406da-131">Faturar crédito total de uma transação de despesas previamente faturada.</span><span class="sxs-lookup"><span data-stu-id="406da-131">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="406da-132">Uma inversão de vendas faturada para a quantidade e o montante no detalhe de linha da fatura original para as despesas.</span><span class="sxs-lookup"><span data-stu-id="406da-132">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="406da-133">Um novo valor real de vendas por faturar para a quantidade e o montante no detalhe de linha da fatura original para as despesas.</span><span class="sxs-lookup"><span data-stu-id="406da-133">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="406da-134">Faturar crédito parcial de uma transação de despesas previamente faturada.</span><span class="sxs-lookup"><span data-stu-id="406da-134">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="406da-135">Uma inversão de vendas faturada para a quantidade e o montante faturado no detalhe de linha da fatura original para uma despesa.</span><span class="sxs-lookup"><span data-stu-id="406da-135">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="406da-136">Um novo valor real de vendas não faturada que é faturável pela quantidade e montante no detalhe da linha de fatura corrigida, uma inversão deste, e um valor real de vendas faturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="406da-136">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="406da-137">Um novo valor real de vendas não faturado que é faturável para a quantidade e montante restante após a dedução dos valores corrigidos no detalhe da linha de fatura.</span><span class="sxs-lookup"><span data-stu-id="406da-137">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
                <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="406da-138">Faturação do crédito integral de uma transação material previamente faturada.</span><span class="sxs-lookup"><span data-stu-id="406da-138">Invoicing the full credit of a previously invoiced material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="406da-139">Uma inversão de vendas faturadas para a quantidade e montante no detalhe de linha de fatura para o material.</span><span class="sxs-lookup"><span data-stu-id="406da-139">A billed sales reversal for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="406da-140">Um novo valor real de vendas não faturadas para a quantidade e montante no detalhe de linha de fatura para o material.</span><span class="sxs-lookup"><span data-stu-id="406da-140">A new unbilled sales actual for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="406da-141">Faturar o crédito parcial numa transação material.</span><span class="sxs-lookup"><span data-stu-id="406da-141">Invoicing the partial credit on a material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="406da-142">Uma inversão de vendas faturadas para a quantidade e montante faturado no detalhe de linha de fatura para o material.</span><span class="sxs-lookup"><span data-stu-id="406da-142">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="406da-143">Um novo valor real de vendas não faturadas é faturável pela quantidade e montante no detalhe da linha de fatura editada, uma inversão desta e um valor real de venda de faturação equivalente.</span><span class="sxs-lookup"><span data-stu-id="406da-143">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="406da-144">Um novo valor real de vendas não faturado que é faturável para a quantidade e montante restante após a dedução dos valores corrigidos no detalhe da linha de fatura.</span><span class="sxs-lookup"><span data-stu-id="406da-144">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="406da-145">Faturar o crédito total de uma transação de honorários previamente faturada.</span><span class="sxs-lookup"><span data-stu-id="406da-145">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="406da-146">Uma inversão de vendas faturada para a quantidade e o montante no detalhe de linha da fatura original para os honorários.</span><span class="sxs-lookup"><span data-stu-id="406da-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="406da-147">Um novo valor real de vendas por faturar para a quantidade e o montante no detalhe de linha da fatura original para os honorários.</span><span class="sxs-lookup"><span data-stu-id="406da-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="406da-148">Faturar o crédito parcial de uma transação de honorários previamente faturada.</span><span class="sxs-lookup"><span data-stu-id="406da-148">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="406da-149">Uma inversão de vendas faturada para a quantidade e o montante faturado no detalhe de linha da fatura original para honorários.</span><span class="sxs-lookup"><span data-stu-id="406da-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="406da-150">Um novo valor real de vendas não faturada que é faturável pela quantidade e montante no detalhe da linha de fatura corretiva editada, uma inversão deste, e um valor real de vendas faturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="406da-150">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="406da-151">Faturar o crédito total de um marco previamente faturado.</span><span class="sxs-lookup"><span data-stu-id="406da-151">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="406da-152">Uma inversão de vendas faturada para o montante no detalhe de linha original para o marco.</span><span class="sxs-lookup"><span data-stu-id="406da-152">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="406da-153">O estado da fatura no marco é atualizado de <b>Fatura de cliente publicada</b> para <b>Pronta a faturar</b>.</span><span class="sxs-lookup"><span data-stu-id="406da-153">The invoice status of the milestone is updated from <b>Customer Invoice Posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="406da-154">Faturar o crédito parcial de um marco previamente faturado.</span><span class="sxs-lookup"><span data-stu-id="406da-154">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="406da-155">Este cenário não é suportado.</span><span class="sxs-lookup"><span data-stu-id="406da-155">This scenario isn't supported.</span></span>
                </p>
            </td>
        </tr>       
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
