---
title: Faturas corrigidas
description: Este tópico fornece informações sobre as faturas corrigidas.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e14da1c07d5b697de6caf1b9041c30581ecff102
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898095"
---
# <a name="corrected-invoices"></a><span data-ttu-id="a181e-103">Faturas corrigidas</span><span class="sxs-lookup"><span data-stu-id="a181e-103">Corrected invoices</span></span>

<span data-ttu-id="a181e-104">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="a181e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a181e-105">As faturas corrigidas podem ser editadas.</span><span class="sxs-lookup"><span data-stu-id="a181e-105">Confirmed invoices can be edited.</span></span> <span data-ttu-id="a181e-106">Quando edita uma fatura confirmada, um rascunho da fatura corrigida é criado.</span><span class="sxs-lookup"><span data-stu-id="a181e-106">When you edit a confirmed invoice, a draft of the corrected invoice is created.</span></span> <span data-ttu-id="a181e-107">Dado que a pressuposição é que pretende reverter todas as transações e quantidades da fatura original, a fatura corrigida inclui todas as transações da fatura original e todas as quantidades são zero (0).</span><span class="sxs-lookup"><span data-stu-id="a181e-107">Because the assumption is that you want to reverse all the transactions and quantities from the original invoice, the corrected invoice includes all the transactions from the original invoice, and all the quantities on it are zero (0).</span></span>

<span data-ttu-id="a181e-108">Quando alguma transação não necessitar de correção, pode removê-la da fatura corretiva de rascunho.</span><span class="sxs-lookup"><span data-stu-id="a181e-108">When transactions don't require correction, you can remove them from the draft corrective invoice.</span></span> <span data-ttu-id="a181e-109">Para reverter ou devolver apenas uma quantidade parcial, pode editar o campo Quantidade no detalhe de linha.</span><span class="sxs-lookup"><span data-stu-id="a181e-109">To reverse or return only a partial quantity, you can edit the Quantity field on the line detail.</span></span> <span data-ttu-id="a181e-110">Se abrir o detalhe de linha de fatura, poderá ver a quantidade original da fatura.</span><span class="sxs-lookup"><span data-stu-id="a181e-110">If you open the invoice line detail, you can see the original invoice quantity.</span></span> <span data-ttu-id="a181e-111">Em seguida, pode editar a quantidade da fatura atual para que seja inferior ou superior à quantidade original da fatura.</span><span class="sxs-lookup"><span data-stu-id="a181e-111">You can then edit the current invoice quantity so that it's less than or more than the original invoice quantity.</span></span>

<span data-ttu-id="a181e-112">Quando confirma uma fatura corretiva, o valor real de vendas faturadas originais é revertido e é criado um novo valor real de vendas faturadas.</span><span class="sxs-lookup"><span data-stu-id="a181e-112">When you confirm a corrective invoice, the original billed sales actual is reversed, and a new billed sales actual is created.</span></span> <span data-ttu-id="a181e-113">Se a quantidade tiver sido reduzida, a diferença causará a criação de um novo valor real de vendas não faturadas.</span><span class="sxs-lookup"><span data-stu-id="a181e-113">If the quantity was reduced, the difference will cause a new unbilled sales actual to be created too.</span></span> <span data-ttu-id="a181e-114">Por exemplo, se a venda faturada original era de oito horas e o detalhe de linha de fatura corrigida tiver uma quantidade reduzida de seis horas, a linha de vendas faturadas originais é revertida e são criados dois novos valores reais:</span><span class="sxs-lookup"><span data-stu-id="a181e-114">For example, if the original billed sale was for eight hours, and the corrected invoice line detail has a reduced quantity of six hours, the original billed sales line is revered and two new actuals are created:</span></span>

- <span data-ttu-id="a181e-115">Um valor real de vendas faturadas durante seis horas.</span><span class="sxs-lookup"><span data-stu-id="a181e-115">A billed sales actual for six hours.</span></span>
- <span data-ttu-id="a181e-116">Uma valor real de vendas não faturadas para as duas horas restantes.</span><span class="sxs-lookup"><span data-stu-id="a181e-116">An unbilled sales actual for the remaining two hours.</span></span> <span data-ttu-id="a181e-117">Esta transação pode ser faturada mais tarde ou marcada como não faturável, dependendo das negociações com o cliente.</span><span class="sxs-lookup"><span data-stu-id="a181e-117">This transaction can either be billed later or marked as non-chargeable, depending on the negotiations with the customer.</span></span>