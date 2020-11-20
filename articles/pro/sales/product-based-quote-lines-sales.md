---
title: Descrição geral de linhas de proposta baseadas em produtos – lite
description: Este tópico fornece informações sobre trabalhar com linhas de proposta baseadas em produtos.
author: rumant
manager: Annbe
ms.date: 10/30/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f6aa428c486f149308ad078f9d7a80a0be0f0f04
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/30/2020
ms.locfileid: "4178202"
---
# <a name="product-based-quote-lines-overview---lite"></a><span data-ttu-id="5b802-103">Descrição geral de linhas de proposta baseadas em produtos – lite</span><span class="sxs-lookup"><span data-stu-id="5b802-103">Product-based quote lines overview - lite</span></span>

<span data-ttu-id="5b802-104">_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_</span><span class="sxs-lookup"><span data-stu-id="5b802-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5b802-105">É possível criar linhas de proposta baseadas em produtos no Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="5b802-105">You can create product-based quote lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="5b802-106">As linhas de proposta baseadas em produtos podem ser adicionadas manualmente ou podem ser itens do catálogo de produtos.</span><span class="sxs-lookup"><span data-stu-id="5b802-106">Product-based quote lines can be manually added, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="5b802-107">Catálogo de produtos</span><span class="sxs-lookup"><span data-stu-id="5b802-107">Product catalog</span></span>

<span data-ttu-id="5b802-108">Cada produto no catálogo de produtos tem uma unidade e um grupo de unidades predefinidos.</span><span class="sxs-lookup"><span data-stu-id="5b802-108">Each product in the product catalog has a default unit and unit group.</span></span> <span data-ttu-id="5b802-109">Se vários produtos partilharem o mesmo conjunto de atributos, pode criar uma família de produtos que partilhe esses atributos.</span><span class="sxs-lookup"><span data-stu-id="5b802-109">If multiple products share the same set of attributes, you can create a product family that share those attributes.</span></span> 

<span data-ttu-id="5b802-110">Por exemplo, uma empresa vende licenças de subscrição para diferentes tipos de software.</span><span class="sxs-lookup"><span data-stu-id="5b802-110">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="5b802-111">Todo o software de subscrição possui os seguintes dois atributos:</span><span class="sxs-lookup"><span data-stu-id="5b802-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="5b802-112">Número de utilizadores</span><span class="sxs-lookup"><span data-stu-id="5b802-112">Number of users</span></span>
- <span data-ttu-id="5b802-113">Uma duração da subscrição medida em meses</span><span class="sxs-lookup"><span data-stu-id="5b802-113">A subscription duration measured in months</span></span>

<span data-ttu-id="5b802-114">Para manter este tipo de catálogo, crie uma família de produtos denominada **Software de Subscrição** e com o número de utilizadores e duração da subscrição como atributos.</span><span class="sxs-lookup"><span data-stu-id="5b802-114">To maintain this type of catalog, create a product family named **Subscription Software** and add the number of users and the subscription duration as attributes.</span></span> <span data-ttu-id="5b802-115">Em seguida, pode adicionar produtos individuais à família de produtos de **Software de Subscrição**.</span><span class="sxs-lookup"><span data-stu-id="5b802-115">Next, you can add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="5b802-116">Adicionar itens do catálogo de produtos a uma proposta do projeto</span><span class="sxs-lookup"><span data-stu-id="5b802-116">Add product catalog items to a project quote</span></span>

<span data-ttu-id="5b802-117">As páginas **Proposta do Projeto** e **Contrato do Projeto** têm secções para linhas baseadas em projetos e linhas baseadas em produtos.</span><span class="sxs-lookup"><span data-stu-id="5b802-117">The **Project Quote** and **Project Contract** pages have sections for project-based lines and product-based lines.</span></span> <span data-ttu-id="5b802-118">Para linhas baseadas em produtos, a lista pendente na linha de proposta ou no item de contrato do projeto inclui todos os produtos e unidades existentes na lista de preços.</span><span class="sxs-lookup"><span data-stu-id="5b802-118">For product-based lines, the drop-down list on the quote line or project contract line includes all the products and units in the product price list.</span></span> <span data-ttu-id="5b802-119">Também pode adicionar produtos que não fazem parte da lista de preços do produto.</span><span class="sxs-lookup"><span data-stu-id="5b802-119">You can also add products that aren't part of the product price list.</span></span>

<span data-ttu-id="5b802-120">Além disso, pode selecionar produtos de outras listas de preços ou diretamente a partir do catálogo de produtos.</span><span class="sxs-lookup"><span data-stu-id="5b802-120">Additionally, you can select products from other price lists or directly from the product catalog.</span></span> <span data-ttu-id="5b802-121">Quando seleciona produtos diretamente a partir de um catálogo de produtos, a lista de preços predefinida desse produto é utilizada para obter o preço de venda do produto.</span><span class="sxs-lookup"><span data-stu-id="5b802-121">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="5b802-122">Se não for definida uma lista de preços predefinida, o preço é definido como zero (0).</span><span class="sxs-lookup"><span data-stu-id="5b802-122">If a default price list isn't set, the price is set to zero (0).</span></span>

<span data-ttu-id="5b802-123">Quando uma linha de proposta for baseada num catálogo de produtos, pode definir manualmente o preço de venda diretamente na linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="5b802-123">When a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="5b802-124">Uma linha de proposta no campo de **Preços** com dois valores disponíveis:</span><span class="sxs-lookup"><span data-stu-id="5b802-124">A quote line in **Pricing** field with two available values:</span></span>

- <span data-ttu-id="5b802-125">**Definir Preço Manualmente**</span><span class="sxs-lookup"><span data-stu-id="5b802-125">**Override Pricing**</span></span>
- <span data-ttu-id="5b802-126">**Utilizar Predefinição**</span><span class="sxs-lookup"><span data-stu-id="5b802-126">**Use Default**</span></span>

<span data-ttu-id="5b802-127">Se selecionar **Definir Preço Manualmente**, o preço predefinido não está definido.</span><span class="sxs-lookup"><span data-stu-id="5b802-127">If you select **Override Pricing**, the default price isn't set.</span></span> <span data-ttu-id="5b802-128">Em vez disso, tem de introduzir um preço para o produto na linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="5b802-128">Instead, you must enter a price for the product on the quote line.</span></span> <span data-ttu-id="5b802-129">Se selecionar **Utilizar Predefinição**, o preço de vendas predefinido é utilizado e o campo está bloqueado para edição.</span><span class="sxs-lookup"><span data-stu-id="5b802-129">If you select **Use Default**, the default sales price is used and the field is locked for editing.</span></span>

<span data-ttu-id="5b802-130">Os preços de vendas predefinidos são introduzidos nas linhas baseadas em produtos de uma proposta.</span><span class="sxs-lookup"><span data-stu-id="5b802-130">Default sales prices are entered on the product-based lines of a quote.</span></span> <span data-ttu-id="5b802-131">O campo **Preços** é definido para **Definir Preço Manualmente**, para que possa editar o preço predefinido nas linhas de proposta.</span><span class="sxs-lookup"><span data-stu-id="5b802-131">The **Pricing** field is then set to **Override Pricing** so that you can edit the default price on the quote lines.</span></span> <span data-ttu-id="5b802-132">Esta é uma definição manual específica do Project Operations do comportamento das linhas baseadas em produtos no Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="5b802-132">This is a Project Operations-specific override to the product-based lines behavior in Dynamics 365 Sales.</span></span>
