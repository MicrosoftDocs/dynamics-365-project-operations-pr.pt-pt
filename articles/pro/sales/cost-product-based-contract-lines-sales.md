---
title: Custo dos itens de contrato baseados em produtos – lite
description: Este tópico fornece informações sobre como criar
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 001b0b54abcdd5fcd1eca7f3271cc78392f68860
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273707"
---
# <a name="cost-product-based-contract-lines---lite"></a><span data-ttu-id="281fe-103">Custo dos itens de contrato baseados em produtos – lite</span><span class="sxs-lookup"><span data-stu-id="281fe-103">Cost product-based contract lines - lite</span></span>

<span data-ttu-id="281fe-104">_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_</span><span class="sxs-lookup"><span data-stu-id="281fe-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="281fe-105">As linhas de contrato baseadas no produto Dynamics 365 Project Operations incluem o campo **Preço de custo**, que armazena o preço de custo do produto para cálculos de rendibilidade a jusante.</span><span class="sxs-lookup"><span data-stu-id="281fe-105">Product-based contract lines in Dynamics 365 Project Operations include the **Cost Price** field, which stores the cost price of the product for downstream profitability calculations.</span></span>

<span data-ttu-id="281fe-106">Quando uma linha de contrato baseada em produtos é criada para um produto de catálogo, o custo da linha assume o campo **Custo padrão** no catálogo de produtos.</span><span class="sxs-lookup"><span data-stu-id="281fe-106">When a product-based contract line is created for a catalog product, the cost of the line defaults from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="281fe-107">O campo **Custo Padrão** no catálogo de produtos está configurado na moeda base da Organização.</span><span class="sxs-lookup"><span data-stu-id="281fe-107">The **Standard Cost** field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="281fe-108">Quando o custo unitário assume a predefinição no item de contrato, é convertido na moeda de venda do contrato.</span><span class="sxs-lookup"><span data-stu-id="281fe-108">When the unit cost defaults on the contract line, it's converted into the sales currency on the contract.</span></span>

## <a name="unit-cost-on-a-product-based-contract-line"></a><span data-ttu-id="281fe-109">Custo unitário num item de contrato baseado em produtos</span><span class="sxs-lookup"><span data-stu-id="281fe-109">Unit cost on a product-based contract line</span></span>

<span data-ttu-id="281fe-110">Ter um custo unitário num item de contrato baseado em produtos permite custos diferentes para produtos para cada venda de uma unidade.</span><span class="sxs-lookup"><span data-stu-id="281fe-110">Having a unit cost on a product-based contract line allows for different product costs for each sale of a unit.</span></span> <span data-ttu-id="281fe-111">Embora nem sempre seja necessário, existem certos cenários em que o custo do produto pode ser descontado para o cliente pelo fornecedor.</span><span class="sxs-lookup"><span data-stu-id="281fe-111">While not always necessary, there are certain scenarios where the cost of the product may be discounted for the customer by the supplier.</span></span> <span data-ttu-id="281fe-112">Considere o seguinte cenário:</span><span class="sxs-lookup"><span data-stu-id="281fe-112">Consider the following scenario:</span></span>

<span data-ttu-id="281fe-113">A Fabrikam Robotics está a instalar braços robóticos nas linhas de montagem da Adatum Corporation.</span><span class="sxs-lookup"><span data-stu-id="281fe-113">Fabrikam Robotics is installing robotic arms at Adatum Corporation's assembly lines.</span></span> <span data-ttu-id="281fe-114">A Fabrikam presta serviços de instalação, mas os braços robóticos são da Trey Research.</span><span class="sxs-lookup"><span data-stu-id="281fe-114">Fabrikam provides installation services but the robotic arms are from Trey Research.</span></span> <span data-ttu-id="281fe-115">Se a instalação de braços robóticos na Adatum Corporation abrir uma nova indústria vertical para a Trey Research, pode oferecer um desconto especial para este negócio à Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="281fe-115">If the installation of robotic arms at Adatum Corporation opens a new industry vertical for Trey Research, they could offer a special discount for this deal to Fabrikam.</span></span> <span data-ttu-id="281fe-116">Neste caso, a Fabrikam cria uma linha de contrato baseada em produtos para braços robóticos.</span><span class="sxs-lookup"><span data-stu-id="281fe-116">In this case, Fabrikam creates a product-based contract line for Robotic Arms.</span></span> <span data-ttu-id="281fe-117">É celebrado um custo por unidade para este contrato.</span><span class="sxs-lookup"><span data-stu-id="281fe-117">A per unit cost is entered for this contract.</span></span> <span data-ttu-id="281fe-118">O custo é diferente do custo dos braços robóticos da Trey Research.</span><span class="sxs-lookup"><span data-stu-id="281fe-118">The cost is different from the cost of robotic arms from Trey Research.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]