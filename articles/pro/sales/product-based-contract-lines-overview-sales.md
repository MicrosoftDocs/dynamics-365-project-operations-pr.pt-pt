---
title: Descrição geral dos itens de contrato baseados em produtos – lite
description: Este tópico fornece informações sobre itens de contrato baseados em produtos.
author: rumant
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f248865287cdd3b1fdb3bbc40ad1c48b5302c2c0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994555"
---
# <a name="product-based-contract-lines-overview---lite"></a><span data-ttu-id="bcc08-103">Descrição geral dos itens de contrato baseados em produtos – lite</span><span class="sxs-lookup"><span data-stu-id="bcc08-103">Product-based contract lines overview - lite</span></span>

<span data-ttu-id="bcc08-104">_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_</span><span class="sxs-lookup"><span data-stu-id="bcc08-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="bcc08-105">É possível itens de contrato baseados em produto no Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="bcc08-105">You can create product-based contract lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="bcc08-106">Os itens de contrato baseados em produtos podem ser linhas criadas manualmente ou podem ser itens do catálogo de produtos.</span><span class="sxs-lookup"><span data-stu-id="bcc08-106">Product-based contract lines can be manually created lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="bcc08-107">Catálogo de produtos</span><span class="sxs-lookup"><span data-stu-id="bcc08-107">Product catalog</span></span>

<span data-ttu-id="bcc08-108">Os produtos no catálogo de produtos têm uma unidade e um grupo de unidades predefinidos.</span><span class="sxs-lookup"><span data-stu-id="bcc08-108">The products in the product catalog have a default unit and unit group.</span></span> <span data-ttu-id="bcc08-109">Se vários produtos partilharem o mesmo conjunto de atributos, pode criar uma família de produtos que também tenha esses atributos.</span><span class="sxs-lookup"><span data-stu-id="bcc08-109">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="bcc08-110">Todos os produtos de uma família de produtos herdam o mesmo conjunto de atributos.</span><span class="sxs-lookup"><span data-stu-id="bcc08-110">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="bcc08-111">Por exemplo, uma empresa vende licenças de subscrição para diferentes tipos de software.</span><span class="sxs-lookup"><span data-stu-id="bcc08-111">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="bcc08-112">Todo o software de subscrição possui os seguintes dois atributos:</span><span class="sxs-lookup"><span data-stu-id="bcc08-112">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="bcc08-113">Número de utilizadores</span><span class="sxs-lookup"><span data-stu-id="bcc08-113">Number of users</span></span>
- <span data-ttu-id="bcc08-114">Duração da subscrição (em meses)</span><span class="sxs-lookup"><span data-stu-id="bcc08-114">Subscription duration (in months)</span></span>

<span data-ttu-id="bcc08-115">Para manter este tipo de catálogo, crie uma família de produtos que se chama **Software de Subscrição**.</span><span class="sxs-lookup"><span data-stu-id="bcc08-115">To maintain this type of catalog, create a product family that is named **Subscription Software**.</span></span> <span data-ttu-id="bcc08-116">Adicione os atributos, **Número de utilizadores** e **Duração da subscrição** à família de produtos.</span><span class="sxs-lookup"><span data-stu-id="bcc08-116">Add the attributes, **Number of users** and **Subscription duration** to the product family.</span></span> <span data-ttu-id="bcc08-117">Em seguida, adicione produtos individuais à família de produtos **Software de Subscrição**.</span><span class="sxs-lookup"><span data-stu-id="bcc08-117">Then, add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-contract"></a><span data-ttu-id="bcc08-118">Adicionar itens do catálogo de produtos a um Contrato do projeto</span><span class="sxs-lookup"><span data-stu-id="bcc08-118">Add product catalog items to a project Contract</span></span>

<span data-ttu-id="bcc08-119">Os contratos do projeto e do contrato do projeto têm secções para dois tipos de linha, baseadas em projetos e baseadas em produtos.</span><span class="sxs-lookup"><span data-stu-id="bcc08-119">Project contracts have sections for two types of lines, project-based and product-based.</span></span> <span data-ttu-id="bcc08-120">As linhas baseadas em produtos incluem todos os produtos e unidades na lista de preços do produto no contrato.</span><span class="sxs-lookup"><span data-stu-id="bcc08-120">Product-based lines include all of the products and units in the product price list on the contract.</span></span> <span data-ttu-id="bcc08-121">Os produtos que não fazem parte da lista de preços de um contrato podem ser adicionados.</span><span class="sxs-lookup"><span data-stu-id="bcc08-121">Products that aren't part of contract's product price list can be added.</span></span>

<span data-ttu-id="bcc08-122">Pode selecionar produtos de outras listas de preços, ou diretamente do catálogo de produtos.</span><span class="sxs-lookup"><span data-stu-id="bcc08-122">You can select products from other price lists, or directly from the product catalog.</span></span> <span data-ttu-id="bcc08-123">Quando seleciona produtos diretamente a partir de um catálogo de produtos, a lista de preços predefinida desse produto é utilizada para o preço de venda do produto.</span><span class="sxs-lookup"><span data-stu-id="bcc08-123">When you select products directly from a product catalog, the default price list of that product is used for the product's sales price.</span></span> <span data-ttu-id="bcc08-124">Se não for definida uma lista de preços predefinida, o preço é definido como 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="bcc08-124">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="bcc08-125">Se um item de contrato for baseado num catálogo de produtos, pode definir manualmente o preço de venda diretamente no item.</span><span class="sxs-lookup"><span data-stu-id="bcc08-125">If a contract line is based on a product catalog, you can override the sales price directly on the line.</span></span> <span data-ttu-id="bcc08-126">Um item de contrato tem o campo **Definir preço** com os dois valores:</span><span class="sxs-lookup"><span data-stu-id="bcc08-126">A contract line has the **Pricing** field with the two values:</span></span>

- <span data-ttu-id="bcc08-127">**Definir preço manualmente**</span><span class="sxs-lookup"><span data-stu-id="bcc08-127">**Override pricing**</span></span>
- <span data-ttu-id="bcc08-128">**Utilizar predefinição**</span><span class="sxs-lookup"><span data-stu-id="bcc08-128">**Use default**</span></span>

<span data-ttu-id="bcc08-129">Se definir o campo como **Definir preço**, para **Definir preço manualmente**, o preço predefinido não é definido.</span><span class="sxs-lookup"><span data-stu-id="bcc08-129">If you set the **Pricing** field to **Override pricing**, the default price isn't set.</span></span> <span data-ttu-id="bcc08-130">Introduza um preço para o produto no item de contrato.</span><span class="sxs-lookup"><span data-stu-id="bcc08-130">Enter a price for the product on the contract line.</span></span> <span data-ttu-id="bcc08-131">Se definir o campo para **Utilizar predefinição**, o preço de vendas predefinido é utilizado e o campo não pode ser editado.</span><span class="sxs-lookup"><span data-stu-id="bcc08-131">If you set the field to **Use default**, the default sales price is used and the field can't be edited.</span></span>

<span data-ttu-id="bcc08-132">Depois de instalar o Project Operations, os preços de venda predefinidos são introduzidos nos itens baseados em produtos num contrato.</span><span class="sxs-lookup"><span data-stu-id="bcc08-132">After you install Project Operations, default sales prices are entered on the product-based lines on a contract.</span></span> <span data-ttu-id="bcc08-133">O campo **Definir preço** é definido para **Definir preço manualmente**, para que possa editar o preço predefinido nos itens de contrato.</span><span class="sxs-lookup"><span data-stu-id="bcc08-133">The **Pricing** field is set to **Override pricing** so that you can edit the default price on the contract lines.</span></span> <span data-ttu-id="bcc08-134">Esta é uma definição manual específica do Project Operations ao comportamento de linhas baseadas em produtos no Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="bcc08-134">This is a Project Operations-specific override to product-based lines behavior in Dynamics 365 Sales.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]