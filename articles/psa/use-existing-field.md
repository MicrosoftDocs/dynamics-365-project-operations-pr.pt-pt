---
title: Utilizar um campo existente no Project Service como dimensão de definição de preços
description: Este tópico inclui informações sobre a utilização de campos existentes do Project Service como dimensões de definição de preços.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 415e346f88e60cb064f3327bfb35e21bd1c89014
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082482"
---
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a><span data-ttu-id="d571b-103">Utilizar um campo existente no Project Service como dimensão de definição de preços</span><span class="sxs-lookup"><span data-stu-id="d571b-103">Use an existing field in Project Service as a pricing dimension</span></span>

<span data-ttu-id="d571b-104">O PSA (Project Service Automation) tem vários campos na entidade **Valores Reais** que podem ser utilizados como dimensões de definição de preços para a definição de preços com base em recursos em organizações de projetos.</span><span class="sxs-lookup"><span data-stu-id="d571b-104">Project Service Automation (PSA) has many fields on the **Actuals** entity that can be used as pricing dimensions for resource-based pricing in project organizations.</span></span> <span data-ttu-id="d571b-105">Por exemplo, um campo comum é o **Recurso Reservável**.</span><span class="sxs-lookup"><span data-stu-id="d571b-105">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="d571b-106">Empresas pequenas, com menos de 20-30 recursos faturáveis, podem achar que ter taxas de faturação e de custo específicas para cada recurso é uma abordagem mais simples.</span><span class="sxs-lookup"><span data-stu-id="d571b-106">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="d571b-107">Entretanto, à medida que a força de trabalho faturável cresce, isto pode tornar-se irreal de manter, pois as taxas de faturação e o custo dos recursos começam a variar à medida que os recursos são promovidos, ganham mais experiência ou adquirem conjuntos de competências diferentes.</span><span class="sxs-lookup"><span data-stu-id="d571b-107">However, as the billable workforce grows, this could become unrealistic to maintain as resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different skill sets.</span></span> <span data-ttu-id="d571b-108">Como esta abordagem ainda funciona para empresas de um determinado porte, consulte o tópico [Utilizar um recurso reservável como uma dimensão de definição de preços](bookable-resource-pricing-dimension.md) para compreender como um campo existente do Project Service pode ser utilizado como uma dimensão de definição de preços.</span><span class="sxs-lookup"><span data-stu-id="d571b-108">Because this approach still works for companies of a certain size, see the topic, [Use a bookable resource as a pricing dimension](bookable-resource-pricing-dimension.md) to understand how an existing Project Service field can be used as a pricing dimension.</span></span>

<span data-ttu-id="d571b-109">Outro exemplo é a categoria de transação.</span><span class="sxs-lookup"><span data-stu-id="d571b-109">Another example is that of transaction category.</span></span> <span data-ttu-id="d571b-110">Os clientes e os implementadores utilizavam a categoria de transação do PSA para classificar o trabalho e utilizavam o campo para definir o preço e o custo com base na categoria do trabalho.</span><span class="sxs-lookup"><span data-stu-id="d571b-110">Customers and Implementers have used the transaction category in PSA to classify work and use the field to price and cost based on the category of work.</span></span> <span data-ttu-id="d571b-111">Para obter mais informações, consulte [Utilizar categoria de transação como uma dimensão de definição de preços](transaction-category-pricing-dimension.md).</span><span class="sxs-lookup"><span data-stu-id="d571b-111">For more information, see [Use transaction category as a pricing dimension](transaction-category-pricing-dimension.md).</span></span>
