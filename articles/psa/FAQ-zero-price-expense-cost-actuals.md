---
title: Porque é que o preço padrão é zero em despesas de custos em valores reais?
description: Resolução de problemas de porque é que o preço padrão é 0 para custos de despesas em valores reais.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/22/2018
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
ms.openlocfilehash: 9f4ff8a96250d675faeda3246c2d0a6c5bd83286
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082425"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="6596b-103">Porque é que o preço padrão é zero em despesas de custos em valores reais?</span><span class="sxs-lookup"><span data-stu-id="6596b-103">Why is the price defaulting to zero on expense cost actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="6596b-104">Este FAQ é aplicável às despesas em valores reais onde a classe de transação está definida como Despesa e tipo de transação é Custos.</span><span class="sxs-lookup"><span data-stu-id="6596b-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="6596b-105">Resolução de problemas de taxas de custo em custos de despesas em valores reais</span><span class="sxs-lookup"><span data-stu-id="6596b-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="6596b-106">Vá para a entrada de despesas relacionada e certifique-se de que existe um valor no campo de entrada despesas.</span><span class="sxs-lookup"><span data-stu-id="6596b-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="6596b-107">Se a entrada de despesa não tiver o campo de valor preenchido, então, localizou o problema.</span><span class="sxs-lookup"><span data-stu-id="6596b-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="6596b-108">Para resolver este problema, recrie a entrada de despesas com um valor válido e aprove-o.</span><span class="sxs-lookup"><span data-stu-id="6596b-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>
