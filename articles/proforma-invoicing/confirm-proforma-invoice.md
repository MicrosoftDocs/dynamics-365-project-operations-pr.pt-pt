---
title: Confirmar uma fatura pró-forma baseada em projeto
description: Esta tópico fornece informações sobre a confirmação de uma fatura baseada em projetos pró-forma.
author: rumant
manager: AnnBe
ms.date: 04/05/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 53c647dca506822312053fb5c9b086a2947974c2
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867145"
---
# <a name="confirm-a-proforma-project-based-invoice"></a><span data-ttu-id="8557c-103">Confirmar uma fatura pró-forma baseada em projeto</span><span class="sxs-lookup"><span data-stu-id="8557c-103">Confirm a proforma project-based invoice</span></span>

<span data-ttu-id="8557c-104">_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_</span><span class="sxs-lookup"><span data-stu-id="8557c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="8557c-105">Após a confirmação de uma fatura pró-forma, o estado da fatura do projeto atualiza para **Confirmada**.</span><span class="sxs-lookup"><span data-stu-id="8557c-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="8557c-106">Quando uma fatura é confirmada, torna-se apenas de leitura.</span><span class="sxs-lookup"><span data-stu-id="8557c-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="8557c-107">Avançando, a fatura só pode ser corrigida se houver alguma correção ou crédito iniciado pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="8557c-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits.</span></span>

<span data-ttu-id="8557c-108">A tabela seguinte lista os valores reais criados pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="8557c-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="8557c-109">Estes valores reais são criados quando determinadas operações são realizadas na fatura do projeto antes de ser confirmada.</span><span class="sxs-lookup"><span data-stu-id="8557c-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="8557c-110">
                    <strong>Cenário</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8557c-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="8557c-111">
                    <strong>Valores reais criados ao confirmar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8557c-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8557c-112">Faturar um adiantamento ou um sinal</span><span class="sxs-lookup"><span data-stu-id="8557c-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8557c-113">Um valor real de vendas faturado do tipo <strong>Sinal</strong> é criado para o montante sobre o adiantamento ou sinal.</span><span class="sxs-lookup"><span data-stu-id="8557c-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8557c-114">Um valor real de venda não faturada com um montante negativo do retentor ou adiantamento a utilizar para a reconciliação.</span><span class="sxs-lookup"><span data-stu-id="8557c-114">An unbilled sales actual with a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8557c-115">Depois de reconciliar completamente um sinal ou adiantamento numa fatura.</span><span class="sxs-lookup"><span data-stu-id="8557c-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8557c-116">Uma inversão de vendas não faturada do sinal ou adiantamento que foi criado para a reconciliação.</span><span class="sxs-lookup"><span data-stu-id="8557c-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="8557c-117">Este montante é positivo porque se destina a anular o negativo que foi criado quando o sinal ou adiantamento foi faturado.</span><span class="sxs-lookup"><span data-stu-id="8557c-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8557c-118">Um valor real de vendas faturado para o valor nesta fatura.</span><span class="sxs-lookup"><span data-stu-id="8557c-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="8557c-119">Depois de reconciliar parcialmente um sinal ou adiantamento numa fatura.</span><span class="sxs-lookup"><span data-stu-id="8557c-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8557c-120">Uma inversão de vendas não faturada do sinal ou adiantamento que foi criado para a reconciliação.</span><span class="sxs-lookup"><span data-stu-id="8557c-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="8557c-121">Este montante é positivo porque se destina a anular o negativo que foi criado quando o sinal ou adiantamento foi faturado.</span><span class="sxs-lookup"><span data-stu-id="8557c-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8557c-122">Um valor real de vendas faturado para o valor nesta fatura.</span><span class="sxs-lookup"><span data-stu-id="8557c-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8557c-123">Um valor real de vendas não faturado negativo do montante restante do sinal ou adiantamento a ser utilizado para a reconciliação em faturas futuras.</span><span class="sxs-lookup"><span data-stu-id="8557c-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8557c-124">Faturar uma transação de tempo sem edições na fatura de rascunho.</span><span class="sxs-lookup"><span data-stu-id="8557c-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8557c-125">Uma inversão de vendas não faturada para as horas e montante na aprovação de tempo original.</span><span class="sxs-lookup"><span data-stu-id="8557c-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8557c-126">Um valor real de vendas faturado para as horas e montante na aprovação de tempo original.</span><span class="sxs-lookup"><span data-stu-id="8557c-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="8557c-127">Faturar uma transação de tempo que foi editada para reduzir a quantidade.</span><span class="sxs-lookup"><span data-stu-id="8557c-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8557c-128">Uma inversão de vendas não faturada para as horas e montante na aprovação de tempo original.</span><span class="sxs-lookup"><span data-stu-id="8557c-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8557c-129">Um novo valor real de vendas não faturada que é faturável pelas horas e montante no detalhe da linha de fatura editada, uma inversão do valor real de vendas, e um valor real de vendas faturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="8557c-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8557c-130">Uma nova venda não faturada real que é não faturável para as horas restantes e montante após dedução dos valores corrigidos no detalhe da linha de fatura editada, uma inversão das vendas efetivas e um equivalente faturado de valor real de vendas.</span><span class="sxs-lookup"><span data-stu-id="8557c-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8557c-131">Faturar uma transação de tempo que foi editada para aumentar a quantidade.</span><span class="sxs-lookup"><span data-stu-id="8557c-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8557c-132">Uma inversão de vendas não faturada para as horas e montante na aprovação de tempo original.</span><span class="sxs-lookup"><span data-stu-id="8557c-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8557c-133">Um novo valor real de vendas não faturada que é faturável pelas horas e montante no detalhe da linha de fatura editada, uma inversão do valor real de vendas não faturado, e um valor real de vendas faturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="8557c-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8557c-134">Faturar uma transação de despesa sem edições na fatura de rascunho.</span><span class="sxs-lookup"><span data-stu-id="8557c-134">Invoicing an expense transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8557c-135">Uma inversão de vendas não faturada para a quantidade e montante na aprovação de despesa original.</span><span class="sxs-lookup"><span data-stu-id="8557c-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8557c-136">Um valor real de vendas faturado para a quantidade e montante na aprovação de despesa original.</span><span class="sxs-lookup"><span data-stu-id="8557c-136">A billed sales actual for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="8557c-137">Faturar uma transação de despesa que foi editada para reduzir a quantidade.</span><span class="sxs-lookup"><span data-stu-id="8557c-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8557c-138">Uma inversão de vendas não faturada para a quantidade e montante na aprovação de despesa original.</span><span class="sxs-lookup"><span data-stu-id="8557c-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8557c-139">Um novo valor real de vendas não faturada que é faturável pela quantidade e montante no detalhe da linha de fatura editada, uma inversão do valor real de vendas não faturado, e um valor real de vendas faturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="8557c-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8557c-140">Um novo valor real de vendas não faturada que é não faturável pela quantidade e montante restantes depois de deduzir os números corrigidos no detalhe da linha de fatura editada, uma inversão do valor real de vendas não faturado, e um valor real de vendas faturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="8557c-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8557c-141">Faturar uma transação de despesa que foi editada para aumentar a quantidade.</span><span class="sxs-lookup"><span data-stu-id="8557c-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8557c-142">Uma inversão de vendas não faturada para a quantidade e montante na aprovação de despesa original.</span><span class="sxs-lookup"><span data-stu-id="8557c-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8557c-143">Um novo valor real de vendas não faturada que é faturável pela quantidade e montante no detalhe da linha de fatura editada, uma inversão do valor real de vendas não faturado, e um valor real de vendas faturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="8557c-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8557c-144">Faturação de uma transação material sem edições na fatura do projeto.</span><span class="sxs-lookup"><span data-stu-id="8557c-144">Invoicing a material transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8557c-145">Uma inversão de vendas não faturadas para a quantidade e montante na aprovação original de utilização do material.</span><span class="sxs-lookup"><span data-stu-id="8557c-145">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8557c-146">Um valor real de vendas faturadas para a quantidade e montante na aprovação original de utilização do material.</span><span class="sxs-lookup"><span data-stu-id="8557c-146">A billed sales actual for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="8557c-147">Faturar uma transação de material que foi editada para reduzir a quantidade.</span><span class="sxs-lookup"><span data-stu-id="8557c-147">Invoicing a material transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8557c-148">Uma inversão de vendas não faturadas para a quantidade e montante na aprovação original de tempo original.</span><span class="sxs-lookup"><span data-stu-id="8557c-148">An unbilled sales reversal for the quantity and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8557c-149">Um novo valor real de vendas não faturada que é faturável pela quantidade e montante no detalhe da linha de fatura editada, uma inversão do valor real de vendas não faturado, e um valor real de vendas faturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="8557c-149">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8557c-150">Um novo valor real de vendas não faturada que é não faturável pela quantidade e montante restantes depois de deduzir os números corrigidos no detalhe da linha de fatura editada, uma inversão do valor real de vendas não faturado, e um valor real de vendas faturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="8557c-150">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8557c-151">Faturar uma transação de material que foi editada para aumentar a quantidade.</span><span class="sxs-lookup"><span data-stu-id="8557c-151">Invoicing a material transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8557c-152">Uma inversão de vendas não faturadas para a quantidade e montante na aprovação original de utilização do material.</span><span class="sxs-lookup"><span data-stu-id="8557c-152">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8557c-153">Um novo valor real de vendas não faturada que é faturável pela quantidade e montante no detalhe da linha de fatura editada, uma inversão do valor real de vendas não faturado, e um valor real de vendas faturado equivalente.</span><span class="sxs-lookup"><span data-stu-id="8557c-153">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8557c-154">Faturar uma taxa.</span><span class="sxs-lookup"><span data-stu-id="8557c-154">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8557c-155">Uma inversão de vendas não faturada para o montante da taxa na linha do diário original.</span><span class="sxs-lookup"><span data-stu-id="8557c-155">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8557c-156">Um valor real de vendas faturado para a quantidade e montante na linha de diário de taxa original.</span><span class="sxs-lookup"><span data-stu-id="8557c-156">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="8557c-157">Faturar um marco.</span><span class="sxs-lookup"><span data-stu-id="8557c-157">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8557c-158">Um valor real de vendas faturado para o montante de marco no marco original no item de contrato do projeto.</span><span class="sxs-lookup"><span data-stu-id="8557c-158">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
       
    </tbody>
</table>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
