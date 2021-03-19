---
title: Porque é que o preço padrão é zero em despesas de custos em valores reais?
description: Resolução de problemas de porque é que o preço padrão é 0 para custos de despesas em valores reais.
author: rumant
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 742b0b9c495b4b3ecb4705be3ece5656f0322ca9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285863"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="b0d5e-103">Por razão o preço predefinido do valor real do custo da despesa é zero</span><span class="sxs-lookup"><span data-stu-id="b0d5e-103">Why is the price defaulting to zero on expense cost actuals</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="b0d5e-104">Este FAQ é aplicável às despesas em valores reais onde a classe de transação está definida como Despesa e tipo de transação é Custos.</span><span class="sxs-lookup"><span data-stu-id="b0d5e-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="b0d5e-105">Resolução de problemas de taxas de custo em custos de despesas em valores reais</span><span class="sxs-lookup"><span data-stu-id="b0d5e-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="b0d5e-106">Vá para a entrada de despesas relacionada e certifique-se de que existe um valor no campo de entrada despesas.</span><span class="sxs-lookup"><span data-stu-id="b0d5e-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="b0d5e-107">Se a entrada de despesa não tiver o campo de valor preenchido, então, localizou o problema.</span><span class="sxs-lookup"><span data-stu-id="b0d5e-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="b0d5e-108">Para resolver este problema, recrie a entrada de despesas com um valor válido e aprove-o.</span><span class="sxs-lookup"><span data-stu-id="b0d5e-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]