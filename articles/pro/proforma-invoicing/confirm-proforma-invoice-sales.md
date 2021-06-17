---
title: Confirmar uma fatura pró-forma do projeto
description: Esta tópico fornece informações sobre a confirmação de faturas pró-forma de projetos no Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0ab40e38f221e57368949b7491578caa8ba88c02
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004140"
---
# <a name="confirm-a-proforma-project-invoice"></a><span data-ttu-id="7cfa6-103">Confirmar uma fatura pró-forma do projeto</span><span class="sxs-lookup"><span data-stu-id="7cfa6-103">Confirm a proforma project invoice</span></span> 

<span data-ttu-id="7cfa6-104">_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_</span><span class="sxs-lookup"><span data-stu-id="7cfa6-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="7cfa6-105">Após a confirmação de uma fatura pró-forma, o estado da fatura do projeto atualiza para **Confirmada**.</span><span class="sxs-lookup"><span data-stu-id="7cfa6-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="7cfa6-106">Quando uma fatura é confirmada, torna-se apenas de leitura.</span><span class="sxs-lookup"><span data-stu-id="7cfa6-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="7cfa6-107">Avançando, a fatura só pode ser corrigida se houver alguma correção ou crédito iniciado pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="7cfa6-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits.</span></span>

<span data-ttu-id="7cfa6-108">A tabela seguinte lista os valores reais criados pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="7cfa6-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="7cfa6-109">Estes valores reais são criados quando determinadas operações são realizadas na fatura do projeto antes de ser confirmada.</span><span class="sxs-lookup"><span data-stu-id="7cfa6-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="7cfa6-110">
                    <strong>Cenário</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7cfa6-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="7cfa6-111">
                    <strong>Valores reais criados ao confirmar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7cfa6-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="7cfa6-112">Faturar um adiantamento ou um sinal</span><span class="sxs-lookup"><span data-stu-id="7cfa6-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7cfa6-113">Um valor real de vendas faturado do tipo <strong>Sinal</strong> é criado para o montante sobre o adiantamento ou sinal.</span><span class="sxs-lookup"><span data-stu-id="7cfa6-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7cfa6-114">Um valor real de vendas não faturado de um montante negativo do sinal ou em adiantamento a ser utilizado para a reconciliação.</span><span class="sxs-lookup"><span data-stu-id="7cfa6-114">An unbilled sales actual of a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="7cfa6-115">Depois de reconciliar completamente um sinal ou adiantamento numa fatura.</span><span class="sxs-lookup"><span data-stu-id="7cfa6-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7cfa6-116">Uma inversão de vendas não faturada do sinal ou adiantamento que foi criado para a reconciliação.</span><span class="sxs-lookup"><span data-stu-id="7cfa6-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="7cfa6-117">Este montante é positivo porque se destina a anular o negativo que foi criado quando o sinal ou adiantamento foi faturado.</span><span class="sxs-lookup"><span data-stu-id="7cfa6-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7cfa6-118">Um valor real de vendas faturado para o valor nesta fatura.</span><span class="sxs-lookup"><span data-stu-id="7cfa6-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="7cfa6-119">Depois de reconciliar parcialmente um sinal ou adiantamento numa fatura.</span><span class="sxs-lookup"><span data-stu-id="7cfa6-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7cfa6-120">Uma inversão de vendas não faturada do sinal ou adiantamento que foi criado para a reconciliação.</span><span class="sxs-lookup"><span data-stu-id="7cfa6-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="7cfa6-121">Este montante é positivo porque se destina a anular o negativo que foi criado quando o sinal ou adiantamento foi faturado.</span><span class="sxs-lookup"><span data-stu-id="7cfa6-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7cfa6-122">Um valor real de vendas faturado para o valor nesta fatura.</span><span class="sxs-lookup"><span data-stu-id="7cfa6-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7cfa6-123">Um valor real de vendas não faturado negativo do montante restante do sinal ou adiantamento a ser utilizado para a reconciliação em faturas futuras.</span><span class="sxs-lookup"><span data-stu-id="7cfa6-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="7cfa6-124">Faturar uma transação de tempo sem edições na fatura de rascunho.</span><span class="sxs-lookup"><span data-stu-id="7cfa6-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7cfa6-125">Uma inversão de vendas não faturada para as horas e montante na aprovação de tempo original.</span><span class="sxs-lookup"><span data-stu-id="7cfa6-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7cfa6-126">Um valor real de vendas faturado para as horas e montante na aprovação de tempo original.</span><span class="sxs-lookup"><span data-stu-id="7cfa6-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="7cfa6-127">Faturar uma transação de tempo que foi editada para reduzir a quantidade.</span><span class="sxs-lookup"><span data-stu-id="7cfa6-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7cfa6-128">Uma inversão de vendas não faturada para as horas e montante na aprovação de tempo original.</span><span class="sxs-lookup"><span data-stu-id="7cfa6-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7cfa6-129">Um novo valor real de vendas não faturada que é faturável pelas horas e montante no detalhe da linha de fatura editada, uma inversão do valor real de vendas, e um valor real de vendas faturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="7cfa6-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7cfa6-130">Um novo valor real de vendas não faturada que é não faturável pelas horas e montante restantes depois de deduzir os números corrigidos no detalhe da linha de fatura editada, uma inversão do valor real de vendas, e um valor real de vendas faturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="7cfa6-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="7cfa6-131">Faturar uma transação de tempo que foi editada para aumentar a quantidade.</span><span class="sxs-lookup"><span data-stu-id="7cfa6-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7cfa6-132">Uma inversão de vendas não faturada para as horas e montante na aprovação de tempo original.</span><span class="sxs-lookup"><span data-stu-id="7cfa6-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7cfa6-133">Um novo valor real de vendas não faturada que é faturável pelas horas e montante no detalhe da linha de fatura editada, uma inversão do valor real de vendas não faturado, e um valor real de vendas faturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="7cfa6-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="7cfa6-134">Faturar uma transação de despesa sem edições na fatura de rascunho.</span><span class="sxs-lookup"><span data-stu-id="7cfa6-134">Invoicing an expense transaction without any edits on draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7cfa6-135">Uma inversão de vendas não faturada para a quantidade e montante na aprovação de despesa original.</span><span class="sxs-lookup"><span data-stu-id="7cfa6-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7cfa6-136">Um valor real de vendas faturado para a quantidade e montante na aprovação de despesa original</span><span class="sxs-lookup"><span data-stu-id="7cfa6-136">A billed sales actual for the quantity and amount on the original expense approval</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="7cfa6-137">Faturar uma transação de despesa que foi editada para reduzir a quantidade.</span><span class="sxs-lookup"><span data-stu-id="7cfa6-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7cfa6-138">Uma inversão de vendas não faturada para a quantidade e montante na aprovação de despesa original.</span><span class="sxs-lookup"><span data-stu-id="7cfa6-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7cfa6-139">Um novo valor real de vendas não faturada que é faturável pela quantidade e montante no detalhe da linha de fatura editada, uma inversão do valor real de vendas não faturado, e um valor real de vendas faturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="7cfa6-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7cfa6-140">Um novo valor real de vendas não faturada que é não faturável pela quantidade e montante restantes depois de deduzir os números corrigidos no detalhe da linha de fatura editada, uma inversão do valor real de vendas não faturado, e um valor real de vendas faturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="7cfa6-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="7cfa6-141">Faturar uma transação de despesa que foi editada para aumentar a quantidade.</span><span class="sxs-lookup"><span data-stu-id="7cfa6-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7cfa6-142">Uma inversão de vendas não faturada para a quantidade e montante na aprovação de despesa original.</span><span class="sxs-lookup"><span data-stu-id="7cfa6-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7cfa6-143">Um novo valor real de vendas não faturada que é faturável pela quantidade e montante no detalhe da linha de fatura editada, uma inversão do valor real de vendas não faturado, e um valor real de vendas faturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="7cfa6-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="7cfa6-144">Faturação de uma transação material sem edições na fatura do projeto.</span><span class="sxs-lookup"><span data-stu-id="7cfa6-144">Invoicing a material transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7cfa6-145">Uma inversão de vendas não faturadas para a quantidade e montante na aprovação original de utilização do material.</span><span class="sxs-lookup"><span data-stu-id="7cfa6-145">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7cfa6-146">Um valor real de vendas faturadas para a quantidade e montante na aprovação original de utilização do material.</span><span class="sxs-lookup"><span data-stu-id="7cfa6-146">A billed sales actual for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="7cfa6-147">Faturar uma transação de material que foi editada para reduzir a quantidade.</span><span class="sxs-lookup"><span data-stu-id="7cfa6-147">Invoicing a material transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7cfa6-148">Uma inversão de vendas não faturadas para a quantidade e montante na aprovação original de tempo original.</span><span class="sxs-lookup"><span data-stu-id="7cfa6-148">An unbilled sales reversal for the quantity and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7cfa6-149">Um novo valor real de vendas não faturada que é faturável pela quantidade e montante no detalhe da linha de fatura editada, uma inversão do valor real de vendas não faturado, e um valor real de vendas faturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="7cfa6-149">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7cfa6-150">Um novo valor real de vendas não faturada que é não faturável pela quantidade e montante restantes depois de deduzir os números corrigidos no detalhe da linha de fatura editada, uma inversão do valor real de vendas não faturado, e um valor real de vendas faturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="7cfa6-150">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="7cfa6-151">Faturar uma transação de material que foi editada para aumentar a quantidade.</span><span class="sxs-lookup"><span data-stu-id="7cfa6-151">Invoicing a material transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7cfa6-152">Uma inversão de vendas não faturadas para a quantidade e montante na aprovação original de utilização do material.</span><span class="sxs-lookup"><span data-stu-id="7cfa6-152">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7cfa6-153">Um novo valor real de vendas não faturada que é faturável pela quantidade e montante no detalhe da linha de fatura editada, uma inversão do valor real de vendas não faturado, e um valor real de vendas faturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="7cfa6-153">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="7cfa6-154">Faturar uma taxa.</span><span class="sxs-lookup"><span data-stu-id="7cfa6-154">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7cfa6-155">Uma inversão de vendas não faturada para o montante da taxa na linha do diário original.</span><span class="sxs-lookup"><span data-stu-id="7cfa6-155">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7cfa6-156">Um valor real de vendas faturado para a quantidade e montante na linha de diário de taxa original.</span><span class="sxs-lookup"><span data-stu-id="7cfa6-156">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="7cfa6-157">Faturar um marco.</span><span class="sxs-lookup"><span data-stu-id="7cfa6-157">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7cfa6-158">Um valor real de vendas faturado para o montante de marco no marco original no item de contrato do projeto.</span><span class="sxs-lookup"><span data-stu-id="7cfa6-158">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="7cfa6-159">Faturar um item de contrato baseado em produtos.</span><span class="sxs-lookup"><span data-stu-id="7cfa6-159">Invoicing a product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="7cfa6-160">Um valor real de vendas faturado para a linha do produto com a quantidade e montante provenientes do item de contrato baseado em produtos.</span><span class="sxs-lookup"><span data-stu-id="7cfa6-160">A billed sales actual for the product line with the quantity and amount coming from the product-based contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
