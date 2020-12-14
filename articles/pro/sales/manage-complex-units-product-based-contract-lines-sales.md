---
title: Gerir unidades complexas para itens de contrato baseados em produtos – lite
description: Este tópico fornece informações sobre o suporte à venda de produtos baseados em subscrições.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a58a13c8186f36e6031fe3c6f3c3a57ea920ac9e
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177390"
---
# <a name="manage-complex-units-for-product-based-contract-lines---lite"></a><span data-ttu-id="7d7de-103">Gerir unidades complexas para itens de contrato baseados em produtos – lite</span><span class="sxs-lookup"><span data-stu-id="7d7de-103">Manage complex units for product-based contract lines - lite</span></span>

<span data-ttu-id="7d7de-104">_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_</span><span class="sxs-lookup"><span data-stu-id="7d7de-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="7d7de-105">O Dynamics 365 Project Operations utiliza fatores de quantidade para suportar a venda de produtos baseados em subscrições.</span><span class="sxs-lookup"><span data-stu-id="7d7de-105">Dynamics 365 Project Operations uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="7d7de-106">Para produtos baseados em subscrições, a quantidade no contrato ou item de contrato do projeto é expressa como o número de meses do utilizador.</span><span class="sxs-lookup"><span data-stu-id="7d7de-106">For subscription-based products, the quantity on the contract or project contract line is expressed as the number of user-months.</span></span>

<span data-ttu-id="7d7de-107">O preço do software de subscrição é armazenado no catálogo como o preço por utilizador, por mês.</span><span class="sxs-lookup"><span data-stu-id="7d7de-107">The price of subscription software is stored in the catalog as the price per-user, per-month.</span></span> <span data-ttu-id="7d7de-108">Durante o processo de vendas, o preço no item de contrato é, normalmente, o preço por utilizador e por mês negociado e descontado pelo agente de vendas.</span><span class="sxs-lookup"><span data-stu-id="7d7de-108">During the sales process, the price on the contract line is usually the per-user, per-month price that was negotiated and discounted by the sales agent.</span></span> <span data-ttu-id="7d7de-109">Cada negócio tem um número diferente de utilizadores e um número diferente de meses de subscrição.</span><span class="sxs-lookup"><span data-stu-id="7d7de-109">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="7d7de-110">A quantidade utilizada para calcular o montante do item de contrato é um produto do número de utilizadores e do número de meses de subscrição.</span><span class="sxs-lookup"><span data-stu-id="7d7de-110">The quantity used to calculate the amount of the contract line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="7d7de-111">Para suportar este tipo de venda, o Project Operations suporta o conceito de *fatores de quantidade*.</span><span class="sxs-lookup"><span data-stu-id="7d7de-111">To support this type of sale, Project Operations supports the concept of *quantity factors*.</span></span> <span data-ttu-id="7d7de-112">Os fatores de quantidade dependem dos atributos do produto.</span><span class="sxs-lookup"><span data-stu-id="7d7de-112">Quantity factors rely on product attributes.</span></span> <span data-ttu-id="7d7de-113">Quando configura propriedades específicas para um produto, pode sinalizar um subconjunto dessas propriedades, ou todas as propriedades, como fatores de quantidade.</span><span class="sxs-lookup"><span data-stu-id="7d7de-113">When you configure specific properties for a product, you can flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="7d7de-114">O Project Operations valida que apenas as propriedades numéricas ou as propriedades de produto que têm um tipo de dados numérico são sinalizadas como fatores de quantidade.</span><span class="sxs-lookup"><span data-stu-id="7d7de-114">Project Operations validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="7d7de-115">Quando um produto com fatores de quantidade configurados é adicionado a um item de contrato, o campo **Quantidade** torna-se apenas de leitura.</span><span class="sxs-lookup"><span data-stu-id="7d7de-115">When a product with configured quantity factors is added to a contract line, the **Quantity** field  becomes read-only.</span></span> <span data-ttu-id="7d7de-116">Depois de introduzir valores para propriedades de produto que são fatores de quantidade, o Project Operations calcula a quantidade do item de contrato.</span><span class="sxs-lookup"><span data-stu-id="7d7de-116">After you enter values for product properties that are quantity factors, Project Operations calculates the quantity of the contract line.</span></span>

<span data-ttu-id="7d7de-117">Por exemplo, o Dynamics 365 Sales poderá ter as seguintes propriedades:</span><span class="sxs-lookup"><span data-stu-id="7d7de-117">For example, Dynamics 365 Sales might have the following properties:</span></span>

- <span data-ttu-id="7d7de-118">**N.º de utilizadores**: O número de utilizadores.</span><span class="sxs-lookup"><span data-stu-id="7d7de-118">**No of users**: The number of users.</span></span>
- <span data-ttu-id="7d7de-119">**N.º de Meses**: O número de meses da subscrição.</span><span class="sxs-lookup"><span data-stu-id="7d7de-119">**No of Months**: The number of subscription months.</span></span>
- <span data-ttu-id="7d7de-120">**SKU do Produto**: A unidade de armazenamento (SKU) do produto.</span><span class="sxs-lookup"><span data-stu-id="7d7de-120">**Product SKU**: The stock keeping unit (SKU) for the product.</span></span>

<span data-ttu-id="7d7de-121">O **N.º de Utilizadores** e **N.º de Meses** podem ser sinalizadas como fatores de quantidade editando as propriedades da linha de produto.</span><span class="sxs-lookup"><span data-stu-id="7d7de-121">The **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span>

<span data-ttu-id="7d7de-122">Para criar fatores de quantidade a partir de propriedades do produto, complete os seguintes passos.</span><span class="sxs-lookup"><span data-stu-id="7d7de-122">To create quantity factors from product properties, complete the following steps.</span></span>

1. <span data-ttu-id="7d7de-123">No **Project Operations**, selecione **Produtos de Vendas**.</span><span class="sxs-lookup"><span data-stu-id="7d7de-123">On the **Project Operations**, select **Sales-Products**.</span></span>
2. <span data-ttu-id="7d7de-124">Abra o produto para o qual necessita de configurar fatores de quantidade.</span><span class="sxs-lookup"><span data-stu-id="7d7de-124">Open the product for which you need to set up quantity factors.</span></span> <span data-ttu-id="7d7de-125">Certifique-se de que o produto já tem propriedades configuradas.</span><span class="sxs-lookup"><span data-stu-id="7d7de-125">Make sure that the product has properties already set up.</span></span>
3. <span data-ttu-id="7d7de-126">Na página **Informações do projeto**, selecione o separador **Fatores de Quantidade**.</span><span class="sxs-lookup"><span data-stu-id="7d7de-126">On the **Project Information** page, select the **Quantity Factors** tab.</span></span>
4. <span data-ttu-id="7d7de-127">Na subgrelha, selecione **+ Novo cálculo do campo**.</span><span class="sxs-lookup"><span data-stu-id="7d7de-127">In the subgrid, select **+ New field computation**.</span></span>
5. <span data-ttu-id="7d7de-128">Introduza o nome do **Fator de Quantidade** e selecione o valor da propriedade que mapeia para o cálculo do campo.</span><span class="sxs-lookup"><span data-stu-id="7d7de-128">Enter the name of the **Quantity Factor** and select the property value that maps to the field computation.</span></span>
6. <span data-ttu-id="7d7de-129">Guarde e feche o formulário.</span><span class="sxs-lookup"><span data-stu-id="7d7de-129">Save and close the form.</span></span>
7. <span data-ttu-id="7d7de-130">Repita os passos 2-6 para todas as propriedades que, em conjunto, compõem a quantidade do item de contrato baseado em produtos.</span><span class="sxs-lookup"><span data-stu-id="7d7de-130">Repeat steps 2-6 for all the properties that together will make up the quantity for the product-based contract line.</span></span>

<span data-ttu-id="7d7de-131">Com os fatores de quantidade configurados, quando o utilizador cria um item de contrato para este produto, a quantidade do item de contrato é bloqueado.</span><span class="sxs-lookup"><span data-stu-id="7d7de-131">With quantity factors set up, when the user creates a contract line for this product, the quantity of the contract line is locked.</span></span> <span data-ttu-id="7d7de-132">A quantidade é então calculada como um produto dos valores de propriedade para esse item de contrato.</span><span class="sxs-lookup"><span data-stu-id="7d7de-132">The quantity is then calculated as a product of the property values for that contract line.</span></span>