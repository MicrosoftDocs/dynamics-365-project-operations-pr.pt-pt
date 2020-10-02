---
title: Listas de preços de produtos
description: Este tópico fornece informações sobre as listas de preços nos preços do catálogo utilizados para propostas e contratos de projeto.
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
ms.openlocfilehash: 3570aeb78804e9b267caa55a27e02d6c8df9a5c6
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898185"
---
# <a name="product-price-lists"></a><span data-ttu-id="391c5-103">Listas de preços de produtos</span><span class="sxs-lookup"><span data-stu-id="391c5-103">Product price lists</span></span>

<span data-ttu-id="391c5-104">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="391c5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="391c5-105">As listas de preços e as entidades de itens da lista de preços oferecem suporte à definição de preços do catálogo de produtos.</span><span class="sxs-lookup"><span data-stu-id="391c5-105">Price lists and price list item entities support product catalog pricing.</span></span> <span data-ttu-id="391c5-106">Na maioria das vezes, esta funcionalidade é utilizada para linhas baseadas no catálogo em propostas e contratos de projetos.</span><span class="sxs-lookup"><span data-stu-id="391c5-106">For the most part, this functionality is used for catalog-based lines on project quotes and project contracts.</span></span>

<span data-ttu-id="391c5-107">Para linhas baseadas em projetos, um contrato representa o negócio depois de ser ganho.</span><span class="sxs-lookup"><span data-stu-id="391c5-107">For project-based lines, a contract represents the deal after it was won.</span></span> <span data-ttu-id="391c5-108">Como o processo de negociação geralmente precede o ganho, o preço anexado à proposta é sempre copiado como está para uma nova lista de preços e anexado ao contrato.</span><span class="sxs-lookup"><span data-stu-id="391c5-108">Because the process of negotiation usually precedes the win, the pricing that is attached to the quote is always copied as-is to a new price list and attached to the contract.</span></span> <span data-ttu-id="391c5-109">Esta nova lista de preços não pode ser alterada fora do âmbito do contrato.</span><span class="sxs-lookup"><span data-stu-id="391c5-109">This new price list can't be changed outside the scope of the contract.</span></span> <span data-ttu-id="391c5-110">Esta limitação ajuda a proteger o cartão de taxas negociado face a quaisquer alterações de preço que ocorram na lista de preços principal.</span><span class="sxs-lookup"><span data-stu-id="391c5-110">This limitation helps protect the rate card that was negotiated from any price changes that occur in the master price list.</span></span>

<span data-ttu-id="391c5-111">Os produtos devem ser configurados de modo a que tenham listas de custos e preços predefinidas no catálogo de produtos.</span><span class="sxs-lookup"><span data-stu-id="391c5-111">Products should be set up so that they have default cost and price lists in the product catalog.</span></span> <span data-ttu-id="391c5-112">Utilize o preço de lista, o custo padrão e o custo atual para configurar o custo predefinido e os preços de lista.</span><span class="sxs-lookup"><span data-stu-id="391c5-112">Use the list price, standard cost, and current cost to configure default cost and list prices.</span></span> <span data-ttu-id="391c5-113">Os preços de lista predefinidos são utilizados numa linha de proposta ou num item de contrato do projeto apenas quando o sistema não consegue localizar uma linha da lista de preços para esse produto na lista de preços do produto para a proposta ou o contrato do projeto.</span><span class="sxs-lookup"><span data-stu-id="391c5-113">The default list prices are used on a quote line or a project contract line only when the system can't find a price list line for that product in the product price list for the quote or project contract.</span></span>

<span data-ttu-id="391c5-114">O preço de custo das linhas do catálogo de produtos pode ser alterado entre aspas.</span><span class="sxs-lookup"><span data-stu-id="391c5-114">The cost price of product catalog lines can be changed between quotes.</span></span> <span data-ttu-id="391c5-115">Esta capacidade é importante, porque se não monitorizar com precisão os custos, não poderá determinar os lucros operacionais das cativações de projetos.</span><span class="sxs-lookup"><span data-stu-id="391c5-115">This capability is important, because if you don't accurately track costs, you can't determine operational profits on project engagements.</span></span> <span data-ttu-id="391c5-116">Por predefinição, o custo padrão do produto é utilizado como o preço de custo.</span><span class="sxs-lookup"><span data-stu-id="391c5-116">By default, the standard cost of the product is used as the cost price.</span></span> <span data-ttu-id="391c5-117">No entanto, o preço de custo predefinido pode ser atualizado na linha de proposta se existir um preço de custo diferente para essa proposta.</span><span class="sxs-lookup"><span data-stu-id="391c5-117">However, the default cost price can be updated on the quote line if there's a different cost price for that quote.</span></span>

## <a name="price-list-items"></a><span data-ttu-id="391c5-118">Itens da lista de preços</span><span class="sxs-lookup"><span data-stu-id="391c5-118">Price list items</span></span>

<span data-ttu-id="391c5-119">Pode adicionar produtos de um catálogo de produtos a listas de preços diferentes.</span><span class="sxs-lookup"><span data-stu-id="391c5-119">You can add products from a product catalog to different price lists.</span></span> <span data-ttu-id="391c5-120">As linhas da lista de preços para produtos referenciam sempre uma unidade específica.</span><span class="sxs-lookup"><span data-stu-id="391c5-120">Price list lines for products always reference a specific unit.</span></span> <span data-ttu-id="391c5-121">Os preços de um produto nos itens da lista de preços podem ser configurados como um montante de moeda.</span><span class="sxs-lookup"><span data-stu-id="391c5-121">Pricing for a product on price list items can be configured as a currency amount.</span></span> <span data-ttu-id="391c5-122">Em alternativa, pode ser configurado como uma função do preço de lista, custo atual ou custo padrão.</span><span class="sxs-lookup"><span data-stu-id="391c5-122">Alternatively, it can be configured as a function of the list price, current cost, or standard cost.</span></span>

<span data-ttu-id="391c5-123">O PSA suporta várias opções de arredondamento quando os preços são configurados como uma função do preço de lista, custo padrão ou custo atual.</span><span class="sxs-lookup"><span data-stu-id="391c5-123">PSA supports various rounding options when prices are configured as a function of the list price, standard cost, or current cost.</span></span> <span data-ttu-id="391c5-124">Além de tirar partido de vários métodos de definição de preços e opções de arredondamento, pode associar listas de descontos aos itens da lista de preços.</span><span class="sxs-lookup"><span data-stu-id="391c5-124">In addition to taking advantage of multiple pricing methods and rounding options, you can associate discount lists with price list items.</span></span> 

<span data-ttu-id="391c5-125">Quando cria uma nova lista de preços personalizada para uma proposta selecionando **Criar Lista de Preços Personalizada** na página **Proposta do Projeto**, é feita uma cópia da lista de preços e o campo **Entidade** no cabeçalho da nova lista de preços é definido como **Entidade de Vendas**.</span><span class="sxs-lookup"><span data-stu-id="391c5-125">When you create a new custom price list for a quote by selecting **Create Custom Pricing** on the **Project Quote** page, a copy of the price list is made, and the **Entity** field on the header of the new price list is set to **Sales Entity**.</span></span> <span data-ttu-id="391c5-126">O nome da nova lista de preços é anexado ao nome da proposta e um carimbo de data/hora.</span><span class="sxs-lookup"><span data-stu-id="391c5-126">The name of the new price list is appended with the name of the quote and a timestamp.</span></span> <span data-ttu-id="391c5-127">Também pode utilizar o nome da nova lista de preços e o nome da proposta em fluxos de trabalho personalizados para acionar a análise e as aprovações adicionais para as propostas que utilizam preços personalizados.</span><span class="sxs-lookup"><span data-stu-id="391c5-127">You also can use the name of the new price list and the name of the quote in custom workflows to trigger additional review and approvals for quotes that use custom pricing.</span></span>

 
## <a name="default-product-price-list"></a><span data-ttu-id="391c5-128">Lista de preços do produto predefinida</span><span class="sxs-lookup"><span data-stu-id="391c5-128">Default product price list</span></span>
<span data-ttu-id="391c5-129">Cada registo de cliente tem um campo **Lista de Preços Predefinida**, onde pode especificar uma lista de preços que corresponda à moeda do cliente.</span><span class="sxs-lookup"><span data-stu-id="391c5-129">Each customer record has a **Default Price List** field, where you can specify a price list that matches the currency of the customer.</span></span> <span data-ttu-id="391c5-130">Um valor predefinido não é introduzido automaticamente neste campo.</span><span class="sxs-lookup"><span data-stu-id="391c5-130">A default value isn't automatically entered in this field.</span></span> <span data-ttu-id="391c5-131">Quando existe um contrato de preços personalizado com um cliente específico, pode utilizar este campo para associar uma lista de preços a esse cliente.</span><span class="sxs-lookup"><span data-stu-id="391c5-131">When a custom pricing agreement with a specific customer exists, you can use this field to associate a price list with that customer.</span></span>

<span data-ttu-id="391c5-132">As entidades Oportunidade, Proposta e Contrato do Projeto utilizam a seguinte ordem para introduzir listas de preços de produtos predefinidas.</span><span class="sxs-lookup"><span data-stu-id="391c5-132">The Opportunity, Quote, and Project Contract entities use the following order to enter default product price lists.</span></span> <span data-ttu-id="391c5-133">A mesma ordem é utilizada para as listas de preços do projeto.</span><span class="sxs-lookup"><span data-stu-id="391c5-133">The same order is used for project price lists.</span></span>

1.  <span data-ttu-id="391c5-134">Proposta</span><span class="sxs-lookup"><span data-stu-id="391c5-134">Quote</span></span>
2.  <span data-ttu-id="391c5-135">Oportunidade</span><span class="sxs-lookup"><span data-stu-id="391c5-135">Opportunity</span></span>
3.  <span data-ttu-id="391c5-136">Cliente</span><span class="sxs-lookup"><span data-stu-id="391c5-136">Customer</span></span>
4.  <span data-ttu-id="391c5-137">Definições globais</span><span class="sxs-lookup"><span data-stu-id="391c5-137">Global settings</span></span> 

<span data-ttu-id="391c5-138">Por predefinição, o campo **Produto** na linha de proposta lista todos os produtos ativos na lista de preços do produto da proposta.</span><span class="sxs-lookup"><span data-stu-id="391c5-138">By default, the **Product** field on the quote line lists all the active products in the product price list of the quote.</span></span> <span data-ttu-id="391c5-139">Se um produto tiver sido inativado, ou se for um produto de rascunho, o mesmo não está listado, mesmo que esteja na lista de preços.</span><span class="sxs-lookup"><span data-stu-id="391c5-139">If a product has been inactivated, or if it's a draft product, it isn't listed, even if it's in the price list.</span></span> 

<span data-ttu-id="391c5-140">As linhas do catálogo de produtos são adicionadas como linhas de fatura na primeira fatura que é criada para um contrato do projeto.</span><span class="sxs-lookup"><span data-stu-id="391c5-140">Product catalog lines are added as invoice lines on the first invoice that is created for a project contract.</span></span> <span data-ttu-id="391c5-141">Numa fatura de rascunho, essas linhas de fatura podem ser eliminadas.</span><span class="sxs-lookup"><span data-stu-id="391c5-141">On a draft invoice, those invoice lines can be deleted.</span></span> <span data-ttu-id="391c5-142">Neste caso, as linhas serão apresentadas numa fatura subsequente até serem faturadas, ou até a fatura ser enviada para o cliente.</span><span class="sxs-lookup"><span data-stu-id="391c5-142">In that case, the lines will appear on a subsequent invoice until they are invoiced, or until the invoice is sent to the customer.</span></span> <span data-ttu-id="391c5-143">Não é possível faturar uma quantidade parcial de uma linha de fatura do produto.</span><span class="sxs-lookup"><span data-stu-id="391c5-143">You can't invoice a partial quantity of a product invoice line.</span></span> <span data-ttu-id="391c5-144">Quando as linhas de produto do contrato do projeto são faturadas, os valores reais são criados.</span><span class="sxs-lookup"><span data-stu-id="391c5-144">When the product lines from the project contract are invoiced, actuals are created.</span></span> <span data-ttu-id="391c5-145">No entanto, esses valores reais não estão associados à entidade do projeto relacionada.</span><span class="sxs-lookup"><span data-stu-id="391c5-145">However, those actuals aren't linked to the related project entity.</span></span> <span data-ttu-id="391c5-146">Por outras palavras, os itens de contrato do projeto baseados em produtos são independentes de qualquer utilização baseada no projeto.</span><span class="sxs-lookup"><span data-stu-id="391c5-146">In other words, product-based project contract lines are independent of any project-based use.</span></span> <span data-ttu-id="391c5-147">O consumo de material nos projetos não é monitorizado.</span><span class="sxs-lookup"><span data-stu-id="391c5-147">Material consumption on projects isn't tracked.</span></span>