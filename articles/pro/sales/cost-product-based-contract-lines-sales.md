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
ms.openlocfilehash: a81c972f36179621f0547c24fc53d294485f638c
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764473"
---
# <a name="cost-product-based-contract-lines---lite"></a><span data-ttu-id="9a29e-103">Custo dos itens de contrato baseados em produtos – lite</span><span class="sxs-lookup"><span data-stu-id="9a29e-103">Cost product-based contract lines - lite</span></span>

<span data-ttu-id="9a29e-104">_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_</span><span class="sxs-lookup"><span data-stu-id="9a29e-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="9a29e-105">As linhas de contrato baseadas no produto Dynamics 365 Project Operations incluem o campo **Preço de custo**, que armazena o preço de custo do produto para cálculos de rendibilidade a jusante.</span><span class="sxs-lookup"><span data-stu-id="9a29e-105">Product-based contract lines in Dynamics 365 Project Operations include the **Cost Price** field, which stores the cost price of the product for downstream profitability calculations.</span></span>

<span data-ttu-id="9a29e-106">Quando uma linha de contrato baseada em produtos é criada para um produto de catálogo, o custo da linha assume o campo **Custo padrão** no catálogo de produtos.</span><span class="sxs-lookup"><span data-stu-id="9a29e-106">When a product-based contract line is created for a catalog product, the cost of the line defaults from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="9a29e-107">O campo **Custo Padrão** no catálogo de produtos está configurado na moeda base da Organização.</span><span class="sxs-lookup"><span data-stu-id="9a29e-107">The **Standard Cost** field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="9a29e-108">Quando o custo unitário assume a predefinição no item de contrato, é convertido na moeda de venda do contrato.</span><span class="sxs-lookup"><span data-stu-id="9a29e-108">When the unit cost defaults on the contract line, it's converted into the sales currency on the contract.</span></span>

## <a name="unit-cost-on-a-product-based-contract-line"></a><span data-ttu-id="9a29e-109">Custo unitário num item de contrato baseado em produtos</span><span class="sxs-lookup"><span data-stu-id="9a29e-109">Unit cost on a product-based contract line</span></span>

<span data-ttu-id="9a29e-110">Ter um custo unitário num item de contrato baseado em produtos permite custos diferentes para produtos para cada venda de uma unidade.</span><span class="sxs-lookup"><span data-stu-id="9a29e-110">Having a unit cost on a product-based contract line allows for different product costs for each sale of a unit.</span></span> <span data-ttu-id="9a29e-111">Embora nem sempre seja necessário, existem certos cenários em que o custo do produto pode ser descontado para o cliente pelo fornecedor.</span><span class="sxs-lookup"><span data-stu-id="9a29e-111">While not always necessary, there are certain scenarios where the cost of the product may be discounted for the customer by the supplier.</span></span> <span data-ttu-id="9a29e-112">Considere o seguinte cenário:</span><span class="sxs-lookup"><span data-stu-id="9a29e-112">Consider the following scenario:</span></span>

<span data-ttu-id="9a29e-113">A Fabrikam Robotics está a instalar braços robóticos nas linhas de montagem da Adatum Corporation.</span><span class="sxs-lookup"><span data-stu-id="9a29e-113">Fabrikam Robotics is installing robotic arms at Adatum Corporation's assembly lines.</span></span> <span data-ttu-id="9a29e-114">A Fabrikam presta serviços de instalação, mas os braços robóticos são da Trey Research.</span><span class="sxs-lookup"><span data-stu-id="9a29e-114">Fabrikam provides installation services but the robotic arms are from Trey Research.</span></span> <span data-ttu-id="9a29e-115">Se a instalação de braços robóticos na Adatum Corporation abrir uma nova indústria vertical para a Trey Research, pode oferecer um desconto especial para este negócio à Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="9a29e-115">If the installation of robotic arms at Adatum Corporation opens a new industry vertical for Trey Research, they could offer a special discount for this deal to Fabrikam.</span></span> <span data-ttu-id="9a29e-116">Neste caso, a Fabrikam cria uma linha de contrato baseada em produtos para braços robóticos.</span><span class="sxs-lookup"><span data-stu-id="9a29e-116">In this case, Fabrikam creates a product-based contract line for Robotic Arms.</span></span> <span data-ttu-id="9a29e-117">É celebrado um custo por unidade para este contrato.</span><span class="sxs-lookup"><span data-stu-id="9a29e-117">A per unit cost is entered for this contract.</span></span> <span data-ttu-id="9a29e-118">O custo é diferente do custo dos braços robóticos da Trey Research.</span><span class="sxs-lookup"><span data-stu-id="9a29e-118">The cost is different from the cost of robotic arms from Trey Research.</span></span>
