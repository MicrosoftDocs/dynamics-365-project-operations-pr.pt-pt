---
title: Configurar os custos padrão da mão-de-obra e das despesas
description: Este tópico explica como configurar os custos padrão da mão-de-obra e das despesas de um projeto.
author: Yowelle
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b3eb6b1d4d75b095383689dd53a59a15fe9e884a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082461"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="ee264-103">Configurar os custos padrão da mão-de-obra e das despesas</span><span class="sxs-lookup"><span data-stu-id="ee264-103">Configure standard costs for labor and expenses</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ee264-104">Este tópico explica como configurar os custos padrão da mão-de-obra e das despesas de um projeto.</span><span class="sxs-lookup"><span data-stu-id="ee264-104">This topic explains how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="ee264-105">Esta tarefa utiliza o conjunto de dados USSI.</span><span class="sxs-lookup"><span data-stu-id="ee264-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="ee264-106">No painel de navegação, vá para **Módulos > Gestão de projetos e contabilística > Configurar > Preços > Preço de custo (hora)**.</span><span class="sxs-lookup"><span data-stu-id="ee264-106">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (hour)**.</span></span>
2. <span data-ttu-id="ee264-107">Selecione **Novo**.</span><span class="sxs-lookup"><span data-stu-id="ee264-107">Select **New**.</span></span>
3. <span data-ttu-id="ee264-108">No campo **Data efetiva** , introduza uma data.</span><span class="sxs-lookup"><span data-stu-id="ee264-108">In the **Effective date** field, enter a date.</span></span>
4. <span data-ttu-id="ee264-109">No campo **Preço de custo** , introduza um número.</span><span class="sxs-lookup"><span data-stu-id="ee264-109">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="ee264-110">Pode configurar um preço de custo padrão para a categoria do projeto ou configurar um preço de custo por número de trabalhador, número de projeto, categoria, data ou qualquer combinação destes.</span><span class="sxs-lookup"><span data-stu-id="ee264-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="ee264-111">O preço de custo que é aplicado é o preço de custo com o mais alto nível de detalhe.</span><span class="sxs-lookup"><span data-stu-id="ee264-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="ee264-112">Selecione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="ee264-112">Select **Save**.</span></span>
6. <span data-ttu-id="ee264-113">No painel de navegação, vá para **Módulos > Gestão de projetos e contabilística > Configurar > Preços > Preço de venda (hora)**.</span><span class="sxs-lookup"><span data-stu-id="ee264-113">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (hour)**.</span></span>
7. <span data-ttu-id="ee264-114">Selecione **Novo**.</span><span class="sxs-lookup"><span data-stu-id="ee264-114">Select **New**.</span></span>
8. <span data-ttu-id="ee264-115">No campo **Data efetiva** , introduza uma data.</span><span class="sxs-lookup"><span data-stu-id="ee264-115">In the **Effective date** field, enter a date.</span></span>
9. <span data-ttu-id="ee264-116">No campo **Válido até** , selecione uma opção.</span><span class="sxs-lookup"><span data-stu-id="ee264-116">In the **Valid for** field, select an option.</span></span>
10. <span data-ttu-id="ee264-117">No campo **Preços** , introduza um número.</span><span class="sxs-lookup"><span data-stu-id="ee264-117">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="ee264-118">Pode configurar um preço de venda padrão para transações por hora ou para uma categoria de projeto.</span><span class="sxs-lookup"><span data-stu-id="ee264-118">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="ee264-119">Também pode configurar os preços de venda por número de trabalhador, número de projeto, categoria, data de transação ou qualquer combinação destes.</span><span class="sxs-lookup"><span data-stu-id="ee264-119">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="ee264-120">O preço de venda real, que é aplicado quando um trabalhador introduza uma transação no Diário de horas, é o preço de venda com o mais alto nível de detalhe.</span><span class="sxs-lookup"><span data-stu-id="ee264-120">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="ee264-121">Por exemplo, se estiver configurado um preço de venda geral e um preço de venda específico do trabalhador, será utilizado o preço de venda específico do trabalhador.</span><span class="sxs-lookup"><span data-stu-id="ee264-121">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
11. <span data-ttu-id="ee264-122">Selecione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="ee264-122">Select **Save**.</span></span>
12. <span data-ttu-id="ee264-123">Feche a página.</span><span class="sxs-lookup"><span data-stu-id="ee264-123">Close the page.</span></span>
13. <span data-ttu-id="ee264-124">No painel de navegação, vá para **Módulos > Gestão de projetos e contabilística > Configurar > Preços > Preço de custo (despesa)**.</span><span class="sxs-lookup"><span data-stu-id="ee264-124">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (expense)**.</span></span>
14. <span data-ttu-id="ee264-125">Selecione **Novo**.</span><span class="sxs-lookup"><span data-stu-id="ee264-125">Select **New**.</span></span>
15. <span data-ttu-id="ee264-126">No campo **Data efetiva** , introduza uma data.</span><span class="sxs-lookup"><span data-stu-id="ee264-126">In the **Effective date** field, enter a date.</span></span>
16. <span data-ttu-id="ee264-127">No campo **Preço de custo** , introduza um número.</span><span class="sxs-lookup"><span data-stu-id="ee264-127">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="ee264-128">Podem ser preenchidos vários campos, mas este é o mínimo necessário para guardar o registo.</span><span class="sxs-lookup"><span data-stu-id="ee264-128">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
17. <span data-ttu-id="ee264-129">Selecione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="ee264-129">Select **Save**.</span></span>
18. <span data-ttu-id="ee264-130">No painel de navegação, vá para **Módulos > Gestão de projetos e contabilística > Configurar > Preços > Preço de venda (despesa)**.</span><span class="sxs-lookup"><span data-stu-id="ee264-130">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (expense)**.</span></span>
19. <span data-ttu-id="ee264-131">Selecione **Novo**.</span><span class="sxs-lookup"><span data-stu-id="ee264-131">Select **New**.</span></span>
20. <span data-ttu-id="ee264-132">No campo **Data efetiva** , introduza uma data.</span><span class="sxs-lookup"><span data-stu-id="ee264-132">In the **Effective date** field, enter a date.</span></span>
21. <span data-ttu-id="ee264-133">No campo **Válido até** , selecione uma opção.</span><span class="sxs-lookup"><span data-stu-id="ee264-133">In the **Valid for** field, select an option.</span></span>
22. <span data-ttu-id="ee264-134">No campo **Preços** , introduza um número.</span><span class="sxs-lookup"><span data-stu-id="ee264-134">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="ee264-135">O preço de venda real, que é aplicado quando um trabalhador introduza transações num diário de despesas, é o preço de venda com o mais alto nível de detalhe.</span><span class="sxs-lookup"><span data-stu-id="ee264-135">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="ee264-136">Por exemplo, se estiver configurado um preço de venda geral e específico do trabalhador, será utilizado o preço de venda específico do trabalhador.</span><span class="sxs-lookup"><span data-stu-id="ee264-136">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
23. <span data-ttu-id="ee264-137">Selecione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="ee264-137">Select **Save**.</span></span>

