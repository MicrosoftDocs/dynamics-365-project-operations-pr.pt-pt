---
title: Campos das Operações do projeto como dimensões de definição de preços
description: Este tópico fornece informações usando campos como dimensões dos preços no Dynamics 365 Project Operations.
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
ms.openlocfilehash: 3ddf3098e45fdc9b99067b64df05e2adc0b6ad05
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896430"
---
# <a name="project-operations-fields-as-pricing-dimensions"></a><span data-ttu-id="52bc4-103">Campos das Operações do projeto como dimensões de definição de preços</span><span class="sxs-lookup"><span data-stu-id="52bc4-103">Project Operations fields as pricing dimensions</span></span>

<span data-ttu-id="52bc4-104">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="52bc4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="52bc4-105">A entidade **Atuais** tem muitos campos que podem ser usados como dimensões de definição de preços para preços baseados em recursos.</span><span class="sxs-lookup"><span data-stu-id="52bc4-105">The **Actuals** entity has many fields that can be used as pricing dimensions for resource-based pricing.</span></span> <span data-ttu-id="52bc4-106">Por exemplo, um campo comum é o **Recurso Reservável**.</span><span class="sxs-lookup"><span data-stu-id="52bc4-106">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="52bc4-107">Empresas pequenas, com menos de 20-30 recursos faturáveis, podem achar que ter taxas de faturação e de custo específicas para cada recurso é uma abordagem mais simples.</span><span class="sxs-lookup"><span data-stu-id="52bc4-107">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="52bc4-108">No entanto, à medida que a mão de obra faturada aumenta, pode tornar-se irrealista manter as taxas específicas de recursos.</span><span class="sxs-lookup"><span data-stu-id="52bc4-108">However, as the billable workforce grows, resource-secific rates could become unrealistic to maintain.</span></span> <span data-ttu-id="52bc4-109">O custo dos recursos e taxas de faturação começam a variar à medida que os recursos são promovidos, ganham mais experiência ou adquirem um conjunto diferente de competências.</span><span class="sxs-lookup"><span data-stu-id="52bc4-109">Resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different set of skills.</span></span> 

<span data-ttu-id="52bc4-110">Outro exemplo é a categoria de transação.</span><span class="sxs-lookup"><span data-stu-id="52bc4-110">Another example is that of transaction category.</span></span> <span data-ttu-id="52bc4-111">Os clientes e os implementadores utilizavam a categoria de transação para classificar o trabalho e utilizavam o campo para definir o preço e o custo com base na categoria do trabalho.</span><span class="sxs-lookup"><span data-stu-id="52bc4-111">Customers and Implementers have used the transaction category to classify work and use the field to price and cost based on the category of work.</span></span>