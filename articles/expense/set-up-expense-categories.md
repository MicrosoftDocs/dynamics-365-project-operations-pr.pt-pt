---
title: Configurar categorias de despesas
description: Este tópico fornece informações sobre como configurar categorias de despesas e categorias partilhadas para relatórios de despesas.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 1589cf82626e744d35f31fef8e8437a5ad71360d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276137"
---
# <a name="set-up-expense-categories"></a><span data-ttu-id="fb971-103">Configurar categorias de despesas</span><span class="sxs-lookup"><span data-stu-id="fb971-103">Set up expense categories</span></span>

<span data-ttu-id="fb971-104">_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_</span><span class="sxs-lookup"><span data-stu-id="fb971-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="fb971-105">Quando os colaboradores criam relatórios de despesas, cada despesa que registam tem de ser associada a uma categoria de despesas.</span><span class="sxs-lookup"><span data-stu-id="fb971-105">When employees create expense reports, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="fb971-106">As categorias de despesas são derivadas das categorias partilhadas que podem ser partilhadas pelas entidades legais na sua organização.</span><span class="sxs-lookup"><span data-stu-id="fb971-106">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="fb971-107">Consoante a forma como a sua organização é definida, estas categorias de despesas também podem ser partilhadas noutras áreas.</span><span class="sxs-lookup"><span data-stu-id="fb971-107">Depending on how your organization is defined, these expense categories can also be shared in other areas.</span></span> <span data-ttu-id="fb971-108">Com base na definição da sua organização e na orientação da equipa de implementação, tem de determinar se as categorias que são utilizadas na Gestão de despesas serão utilizadas apenas na Gestão de despesas ou se devem ser partilhadas noutras áreas.</span><span class="sxs-lookup"><span data-stu-id="fb971-108">Based on the definition of your organization and guidance from the implementation team, you must determine whether the categories that are used in Expense management will be used only in Expense management or should be shared in other areas.</span></span>

> [!NOTE]
> <span data-ttu-id="fb971-109">Estas categorias podem ser partilhadas entre a Gestão de projeto, a Gestão contabilística e a Gestão de despesas, ou entre a Gestão de projeto, a Gestão contabilística e a Produção.</span><span class="sxs-lookup"><span data-stu-id="fb971-109">These categories can be shared between Project management and accounting and Expense management, or between Project management and accounting and Production.</span></span> <span data-ttu-id="fb971-110">No entanto, não podem ser partilhadas entre a Gestão de despesas e a Produção.</span><span class="sxs-lookup"><span data-stu-id="fb971-110">However, they can't be shared between Expense management and Production.</span></span>

<span data-ttu-id="fb971-111">Antes de iniciar o processo de configuração, têm de ser tomadas as seguintes decisões para cada categoria de despesas:</span><span class="sxs-lookup"><span data-stu-id="fb971-111">Before you can begin the setup process, the following decisions must be made for each expense category:</span></span>

- <span data-ttu-id="fb971-112">O que é uma categoria de despesa?</span><span class="sxs-lookup"><span data-stu-id="fb971-112">What is the expense category?</span></span> <span data-ttu-id="fb971-113">Os exemplos incluem categorias para voos, hotel ou quilometragem.</span><span class="sxs-lookup"><span data-stu-id="fb971-113">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="fb971-114">A categoria de despesa também pode ser utilizada na Gestão de projetos e contabilística?</span><span class="sxs-lookup"><span data-stu-id="fb971-114">Can the expense category also be used in Project management and accounting?</span></span> <span data-ttu-id="fb971-115">Se puder, também tem de tomar as seguintes decisões:</span><span class="sxs-lookup"><span data-stu-id="fb971-115">If it can, you must also make the following decisions:</span></span>

    - <span data-ttu-id="fb971-116">Que contas de custos serão utilizadas para as seguintes despesas?</span><span class="sxs-lookup"><span data-stu-id="fb971-116">Which cost accounts will be used for the following expenses?</span></span>

        - <span data-ttu-id="fb971-117">Custo</span><span class="sxs-lookup"><span data-stu-id="fb971-117">Cost</span></span>
        - <span data-ttu-id="fb971-118">Alocação de vencimentos</span><span class="sxs-lookup"><span data-stu-id="fb971-118">Payroll allocation</span></span>
        - <span data-ttu-id="fb971-119">Valor do custo WIP</span><span class="sxs-lookup"><span data-stu-id="fb971-119">WIP-cost value</span></span>
        - <span data-ttu-id="fb971-120">Item de custo</span><span class="sxs-lookup"><span data-stu-id="fb971-120">Cost-item</span></span>
        - <span data-ttu-id="fb971-121">Item de valor de custo WIP</span><span class="sxs-lookup"><span data-stu-id="fb971-121">WIP-cost value-item</span></span>
        - <span data-ttu-id="fb971-122">Perdas acumuladas</span><span class="sxs-lookup"><span data-stu-id="fb971-122">Accrued loss</span></span>
        - <span data-ttu-id="fb971-123">Perdas acumuladas WIP</span><span class="sxs-lookup"><span data-stu-id="fb971-123">WIP-accrued loss</span></span>

    - <span data-ttu-id="fb971-124">Que contas de receitas serão utilizadas para as seguintes origens de receitas?</span><span class="sxs-lookup"><span data-stu-id="fb971-124">Which revenue accounts will be used for the following sources of revenue?</span></span>

        - <span data-ttu-id="fb971-125">Receitas faturadas</span><span class="sxs-lookup"><span data-stu-id="fb971-125">Invoiced revenue</span></span>
        - <span data-ttu-id="fb971-126">Valor das vendas de receitas acumuladas</span><span class="sxs-lookup"><span data-stu-id="fb971-126">Accrued revenue-sales value</span></span>
        - <span data-ttu-id="fb971-127">Valor de vendas WIP</span><span class="sxs-lookup"><span data-stu-id="fb971-127">WIP-sales value</span></span>
        - <span data-ttu-id="fb971-128">Produção de receitas acumuladas</span><span class="sxs-lookup"><span data-stu-id="fb971-128">Accrued revenue-production</span></span>
        - <span data-ttu-id="fb971-129">Produção WIP</span><span class="sxs-lookup"><span data-stu-id="fb971-129">WIP-production</span></span>
        - <span data-ttu-id="fb971-130">Lucros de receitas acumuladas</span><span class="sxs-lookup"><span data-stu-id="fb971-130">Accrued revenue-profit</span></span>
        - <span data-ttu-id="fb971-131">Lucros WIP</span><span class="sxs-lookup"><span data-stu-id="fb971-131">WIP-profit</span></span>
        - <span data-ttu-id="fb971-132">Subscrição de receitas acumuladas</span><span class="sxs-lookup"><span data-stu-id="fb971-132">Accrued revenue-subscription</span></span>
        - <span data-ttu-id="fb971-133">Subscrição WIP</span><span class="sxs-lookup"><span data-stu-id="fb971-133">WIP-subscription</span></span>

- <span data-ttu-id="fb971-134">O que é um tipo de despesa?</span><span class="sxs-lookup"><span data-stu-id="fb971-134">What is the expense type?</span></span>
- <span data-ttu-id="fb971-135">Qual o método de pagamento predefinido para a categoria de despesa?</span><span class="sxs-lookup"><span data-stu-id="fb971-135">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="fb971-136">As despesas na categoria de despesa têm de ser discriminadas?</span><span class="sxs-lookup"><span data-stu-id="fb971-136">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="fb971-137">Qual a conta predefinida principal para a categoria de despesa?</span><span class="sxs-lookup"><span data-stu-id="fb971-137">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="fb971-138">Qual o grupo de impostos sobre as vendas de artigos predefinido para a categoria de despesa?</span><span class="sxs-lookup"><span data-stu-id="fb971-138">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="fb971-139">São permitidos métodos de pagamento adicionais para a categoria de despesa?</span><span class="sxs-lookup"><span data-stu-id="fb971-139">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="fb971-140">Nesse caso, o que são?</span><span class="sxs-lookup"><span data-stu-id="fb971-140">If so, what are they?</span></span>
- <span data-ttu-id="fb971-141">Existem subcategorias nesta categoria de despesa?</span><span class="sxs-lookup"><span data-stu-id="fb971-141">Are there subcategories in this expense category?</span></span> <span data-ttu-id="fb971-142">Se existirem subcategorias, também tem de tomar as seguintes decisões:</span><span class="sxs-lookup"><span data-stu-id="fb971-142">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="fb971-143">Alguma das subcategorias está excluída da recuperação de impostos?</span><span class="sxs-lookup"><span data-stu-id="fb971-143">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="fb971-144">Qual o grupo impostos sobre vendas de artigos das subcategorias?</span><span class="sxs-lookup"><span data-stu-id="fb971-144">What is the item sales tax group of the subcategories?</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]