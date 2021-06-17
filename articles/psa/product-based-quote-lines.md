---
title: Linhas de proposta baseadas em produtos
description: Este tópico fornece informações sobre linhas de proposta baseadas em produtos.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
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
ms.openlocfilehash: 1bd789f4ee4d5b4603093be24aa25addafa9e8e8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998515"
---
# <a name="product-based-quote-lines"></a><span data-ttu-id="24208-103">Linhas de proposta baseadas em produtos</span><span class="sxs-lookup"><span data-stu-id="24208-103">Product-based quote lines</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


<span data-ttu-id="24208-104">É possível criar linhas de proposta baseadas em produtos no Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="24208-104">You can create product-based quote lines in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="24208-105">As linhas de proposta baseadas em produtos podem ser linhas "acrescentadas manualmente" ou podem ser itens do catálogo de produtos.</span><span class="sxs-lookup"><span data-stu-id="24208-105">Product-based quote lines can be "write-in" lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="24208-106">Catálogo de produtos</span><span class="sxs-lookup"><span data-stu-id="24208-106">Product catalog</span></span>

<span data-ttu-id="24208-107">Os produtos existentes num catálogo de produtos do Dynamics 365 têm uma unidade e um grupo de unidades predefinidos.</span><span class="sxs-lookup"><span data-stu-id="24208-107">The products in a Dynamics 365 product catalog have a default unit and unit group.</span></span> <span data-ttu-id="24208-108">Se vários produtos partilharem o mesmo conjunto de atributos, pode criar uma família de produtos que também tenha esses atributos.</span><span class="sxs-lookup"><span data-stu-id="24208-108">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="24208-109">Todos os produtos de uma família de produtos herdam o mesmo conjunto de atributos.</span><span class="sxs-lookup"><span data-stu-id="24208-109">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="24208-110">Por exemplo, uma empresa vende licenças de subscrição para uma variedade de softwares.</span><span class="sxs-lookup"><span data-stu-id="24208-110">For example, a company sells subscription licenses for a variety of software.</span></span> <span data-ttu-id="24208-111">Todo o software de subscrição possui os seguintes dois atributos:</span><span class="sxs-lookup"><span data-stu-id="24208-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="24208-112">Número de utilizadores</span><span class="sxs-lookup"><span data-stu-id="24208-112">Number of users</span></span> 
- <span data-ttu-id="24208-113">Duração da subscrição (em meses)</span><span class="sxs-lookup"><span data-stu-id="24208-113">Subscription duration (in months)</span></span>

<span data-ttu-id="24208-114">Uma boa forma de manter este tipo de catálogo consiste em criar uma família de produtos denominada **Software de Subscrição** e com o **Número de utilizadores** e **Duração da subscrição** como atributos.</span><span class="sxs-lookup"><span data-stu-id="24208-114">A good way to maintain this type of catalog is to create a product family that is named **Subscription Software**, and that has **Number of users** and **Subscription duration** as attributes.</span></span> <span data-ttu-id="24208-115">Em seguida, pode adicionar produtos individuais, tais como **Dynamics 365 Sales** ou **Dynamics 365 Field Service** à família de produtos **Software de Subscrição**.</span><span class="sxs-lookup"><span data-stu-id="24208-115">You can then add individual products, such as **Dynamics 365 Sales** or **Dynamics 365 Field Service** to the **Subscription Software** product family.</span></span>

## <a name="adding-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="24208-116">Adicionar itens do catálogo de produtos a uma proposta do projeto</span><span class="sxs-lookup"><span data-stu-id="24208-116">Adding product catalog items to a project quote</span></span>

<span data-ttu-id="24208-117">As páginas da proposta do projeto e do contrato do projeto têm secções para dois tipos de linha: linhas baseadas em projetos e linhas baseadas em produtos.</span><span class="sxs-lookup"><span data-stu-id="24208-117">Project quote and project contract pages have sections for two types of lines: project-based lines and product-based lines.</span></span> <span data-ttu-id="24208-118">Quanto às linhas baseadas em produtos, o Dynamics 365 é utilizado para adicionar itens de um catálogo de produtos a uma proposta.</span><span class="sxs-lookup"><span data-stu-id="24208-118">For product-based lines, Dynamics 365 is used to add items from a product catalog to a quote.</span></span> <span data-ttu-id="24208-119">A lista pendente na linha de proposta ou no item de contrato do projeto inclui todos os produtos e unidades existentes na lista de preços do produto anexada à proposta ou ao contrato do projeto.</span><span class="sxs-lookup"><span data-stu-id="24208-119">The drop-down list on the quote line or project contract line includes all the products and units in the product price list that is attached to the quote or project contract.</span></span> <span data-ttu-id="24208-120">Também pode adicionar produtos que não fazem parte da lista de preços do produto da proposta.</span><span class="sxs-lookup"><span data-stu-id="24208-120">You can also add products that aren't part of quote's product price list.</span></span>

<span data-ttu-id="24208-121">Além disso, pode selecionar produtos de outras listas de preços ou pode selecionar produtos diretamente a partir do catálogo de produtos.</span><span class="sxs-lookup"><span data-stu-id="24208-121">Additionally, you can select products from other price lists, or you can select products directly from the product catalog.</span></span> <span data-ttu-id="24208-122">Quando seleciona produtos diretamente a partir de um catálogo de produtos, a lista de preços predefinida desse produto é utilizada para obter o preço de venda do produto.</span><span class="sxs-lookup"><span data-stu-id="24208-122">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="24208-123">Se não for definida uma lista de preços predefinida, o preço é definido como 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="24208-123">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="24208-124">Se uma linha de proposta for baseada num catálogo de produtos, pode definir manualmente o preço de venda diretamente na linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="24208-124">If a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="24208-125">Tenha em atenção que uma linha de proposta no Dynamics 365 tem um campo **Definição de Preços**.</span><span class="sxs-lookup"><span data-stu-id="24208-125">Note that a quote line in Dynamics 365 has a **Pricing** field.</span></span> <span data-ttu-id="24208-126">Estão disponíveis dois valores:</span><span class="sxs-lookup"><span data-stu-id="24208-126">Two values are available:</span></span>

- <span data-ttu-id="24208-127">Definir preço manualmente</span><span class="sxs-lookup"><span data-stu-id="24208-127">Override pricing</span></span>  
- <span data-ttu-id="24208-128">Utilizar predefinição</span><span class="sxs-lookup"><span data-stu-id="24208-128">Use default</span></span>

<span data-ttu-id="24208-129">Se definir este campo como **Definir preço manualmente**, o Dynamics 365 não define um preço predefinido.</span><span class="sxs-lookup"><span data-stu-id="24208-129">If you set this field to **Override pricing**, Dynamics 365 doesn't set a default price.</span></span> <span data-ttu-id="24208-130">Tem de introduzir um preço para o produto na linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="24208-130">You must enter a price for the product on the quote line.</span></span> <span data-ttu-id="24208-131">Se definir este campo para **Utilizar predefinição**, o Dynamics 365 utiliza o preço de venda predefinido e bloqueia o campo para impedir a edição.</span><span class="sxs-lookup"><span data-stu-id="24208-131">If you set this field to **Use default**, Dynamics 365 uses the default sales price and locks the field to prevent editing.</span></span>

<span data-ttu-id="24208-132">Depois de instalar o PSA, os preços de venda predefinidos são introduzidos nos itens baseados em produtos numa proposta.</span><span class="sxs-lookup"><span data-stu-id="24208-132">After you install PSA, default sales prices are entered on the product-based lines on a quote.</span></span> <span data-ttu-id="24208-133">O campo **Definição de Preços** é definido para **Definir preço manualmente**, para que possa editar o preço predefinido nas linhas de proposta.</span><span class="sxs-lookup"><span data-stu-id="24208-133">The **Pricing** field is then set to **Override pricing** so that you can edit the default price on the quote lines.</span></span>

> ![Definir preço manualmente](media/basic-guide-10.png)
 
## <a name="quantity-factors-for-products"></a><span data-ttu-id="24208-135">Fatores de quantidade para produtos</span><span class="sxs-lookup"><span data-stu-id="24208-135">Quantity factors for products</span></span>

<span data-ttu-id="24208-136">O PSA utiliza fatores de quantidade para suportar a venda de produtos baseados em subscrições.</span><span class="sxs-lookup"><span data-stu-id="24208-136">PSA uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="24208-137">Para produtos baseados em subscrições, a quantidade na proposta ou item de contrato do projeto é expressa como o número de meses do utilizador.</span><span class="sxs-lookup"><span data-stu-id="24208-137">For subscription-based products, the quantity on the quote or project contract line is expressed as the number of user months.</span></span>

<span data-ttu-id="24208-138">Normalmente, o preço do software de subscrição é armazenado no catálogo como o preço por utilizador, por mês.</span><span class="sxs-lookup"><span data-stu-id="24208-138">Usually, the price of subscription software is stored in the catalog as the price per user per month.</span></span> <span data-ttu-id="24208-139">No entanto, pode utilizar outras descrições de tempo.</span><span class="sxs-lookup"><span data-stu-id="24208-139">However, you can use other time descriptions instead.</span></span> <span data-ttu-id="24208-140">Durante o processo de vendas, o preço na linha de proposta é, normalmente, o preço por utilizador e por mês negociado e descontado pelo agente de vendas de TI.</span><span class="sxs-lookup"><span data-stu-id="24208-140">During the sales process, the price on the quote line is usually the per-user, per-month price that was negotiated and discounted by the IT sales agent.</span></span> <span data-ttu-id="24208-141">Cada negócio tem um número diferente de utilizadores e um número diferente de meses de subscrição.</span><span class="sxs-lookup"><span data-stu-id="24208-141">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="24208-142">A quantidade que é utilizada para calcular o montante da linha de proposta é um produto do número de utilizadores e do número de meses de subscrição.</span><span class="sxs-lookup"><span data-stu-id="24208-142">The quantity that is used to compute the amount of the quote line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="24208-143">Para suportar este tipo de venda, o PSA introduziu o conceito de fatores de quantidade.</span><span class="sxs-lookup"><span data-stu-id="24208-143">To support this type of sale, PSA introduced the concept of quantity factors.</span></span> <span data-ttu-id="24208-144">Os fatores de quantidade dependem dos atributos do produto no Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="24208-144">Quantity factors rely on the product attributes in Dynamics 365.</span></span> <span data-ttu-id="24208-145">Quando configura propriedades específicas para um produto, o PSA permite-lhe sinalizar um subconjunto dessas propriedades, ou todas as propriedades, como fatores de quantidade.</span><span class="sxs-lookup"><span data-stu-id="24208-145">When you configure specific properties for a product, PSA lets you flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="24208-146">O PSA valida que apenas as propriedades numéricas ou as propriedades de produto que têm um tipo de dados numérico são sinalizadas como fatores de quantidade.</span><span class="sxs-lookup"><span data-stu-id="24208-146">PSA validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="24208-147">Quando um produto para o qual os fatores de quantidade estão configurados é adicionado a uma linha de proposta, o campo **Quantidade** na linha da proposta passa a ser um campo só de leitura.</span><span class="sxs-lookup"><span data-stu-id="24208-147">When a product that quantity factors are configured for is added to a quote line, the **Quantity** field on the quote line becomes a read-only field.</span></span> <span data-ttu-id="24208-148">Depois de introduzir valores para propriedades de produto que são fatores de quantidade, o PSA calcula a quantidade da linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="24208-148">After you enter values for product properties that are quantity factors, PSA computes the quantity of the quote line.</span></span>

<span data-ttu-id="24208-149">Por exemplo, o Dynamics 365 poderá ter as seguintes propriedades:</span><span class="sxs-lookup"><span data-stu-id="24208-149">For example, Dynamics 365 might have the following properties:</span></span> 

- <span data-ttu-id="24208-150">**N.º de utilizadores** - O número de utilizadores</span><span class="sxs-lookup"><span data-stu-id="24208-150">**No of users** - The number of users</span></span> 
- <span data-ttu-id="24208-151">**N.º de Meses** - O número de meses da subscrição</span><span class="sxs-lookup"><span data-stu-id="24208-151">**No of Months** - The number of subscription months</span></span>
- <span data-ttu-id="24208-152">**SKU do Produto**</span><span class="sxs-lookup"><span data-stu-id="24208-152">**Product SKU**</span></span> 

<span data-ttu-id="24208-153">As propriedades **N.º de Utilizadores** e **N.º de Meses** podem ser sinalizadas como fatores de quantidade editando as propriedades da linha de produto.</span><span class="sxs-lookup"><span data-stu-id="24208-153">Tne **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span> 

> ![Sinalizar N.º de Utilizadores e N.º de Meses como fatores de qualidade](media/basic-guide-11.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]