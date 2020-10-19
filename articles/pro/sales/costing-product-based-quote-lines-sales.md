---
title: Custo das linhas de proposta baseadas em produtos
description: Este tópico fornece informações sobre como aplicar um preço de custo a uma linha de proposta baseada em produtos.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 17b377eab5bcbc1a2327cb3ff87cc75d8de40953
ms.sourcegitcommit: a0f80d024a5d3112a39781815bd31d0c05ddaf6f
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 09/30/2020
ms.locfileid: "3906286"
---
# <a name="costing-product-based-quote-lines"></a><span data-ttu-id="444dd-103">Custo das linhas de proposta baseadas em produtos</span><span class="sxs-lookup"><span data-stu-id="444dd-103">Costing product-based quote lines</span></span>

<span data-ttu-id="444dd-104">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="444dd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="444dd-105">As linhas de proposta baseadas em produtos no Dynamics 365 Project Operations também têm um campo **Preço de Custo**.</span><span class="sxs-lookup"><span data-stu-id="444dd-105">Product-based quote lines in Dynamics 365 Project Operations also have a **Cost Price** field.</span></span> <span data-ttu-id="444dd-106">Este campo é utilizado para monitorizar o preço de custo do produto na linha de proposta e para os cálculos de rentabilidade a jusante.</span><span class="sxs-lookup"><span data-stu-id="444dd-106">This field is used to track the cost price for the product on the quote line and for downstream profitability calculations.</span></span>

<span data-ttu-id="444dd-107">Quando uma linha de proposta baseada em produtos é criada para um produto do catálogo, o custo da linha de proposta baseado em produtos assume por predefinição o valor do campo **Custo Padrão** no catálogo de produtos.</span><span class="sxs-lookup"><span data-stu-id="444dd-107">When a product-based quote line is created for a catalog product, the cost of the product-based quote line is defaulted from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="444dd-108">O campo de custo padrão no catálogo de produtos está configurado na moeda base da Organização.</span><span class="sxs-lookup"><span data-stu-id="444dd-108">The standard cost field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="444dd-109">O custo unitário predefinido na linha da proposta baseada em produtos é convertido para a moeda de venda na proposta.</span><span class="sxs-lookup"><span data-stu-id="444dd-109">The default unit cost on the product-based quote line is converted to the sales currency on the quote.</span></span>

## <a name="unit-cost-on-a-product-based-quote-line"></a><span data-ttu-id="444dd-110">Custo unitário numa linha de proposta baseada em produtos</span><span class="sxs-lookup"><span data-stu-id="444dd-110">Unit cost on a product-based quote line</span></span>

<span data-ttu-id="444dd-111">Ter um custo unitário numa linha de proposta baseada em produtos tem como objetivo permitir custos diferentes para um produto para cada venda.</span><span class="sxs-lookup"><span data-stu-id="444dd-111">The purpose of having a unit cost on a product-based quote line is to allow for different costs for a product for each sale.</span></span> <span data-ttu-id="444dd-112">Este não é um cenário típico, mas por vezes o custo do produto pode ser descontado pelo fornecedor, dependendo do cliente da venda final.</span><span class="sxs-lookup"><span data-stu-id="444dd-112">This is not a typical scenario, but sometimes the cost of the product may be discounted by the supplier depending on the customer of the final sale.</span></span>

<span data-ttu-id="444dd-113">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="444dd-113">For example:</span></span>

<span data-ttu-id="444dd-114">A Fabrikam Robotics está a instalar braços robóticos nas linhas de montagem da A Datum Corporation.</span><span class="sxs-lookup"><span data-stu-id="444dd-114">Fabrikam Robotics is installing robotic arms at A Datum Corporation's assembly lines.</span></span> <span data-ttu-id="444dd-115">A Fabrikam presta serviços de instalação, mas os braços robóticos são adquiridos à Trey robotics.</span><span class="sxs-lookup"><span data-stu-id="444dd-115">Fabrikam provides installation services but the robotic arms are procured from Trey robotics.</span></span> <span data-ttu-id="444dd-116">Se a instalação de braços robóticos na A Datum Corporation abrir uma nova indústria vertical para os braços robóticos da Trey, a Trey pode oferecer um desconto especial para este negócio à Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="444dd-116">If the installation of robotic arms at A Datum Corporation opens a new industry vertical for Trey's robotic arms, Trey could give a special discount for this deal to Fabrikam.</span></span>

<span data-ttu-id="444dd-117">Neste caso, a Fabrikam criará uma linha de proposta baseada em produtos para a Robotic Arms e introduzirá um custo unitário especial para esta proposta.</span><span class="sxs-lookup"><span data-stu-id="444dd-117">In this case, Fabrikam will create product-based quote line for Robotic Arms and input a special per unit cost for this quote.</span></span> <span data-ttu-id="444dd-118">Este custo é diferente do custo padrão da Trey Robotic Arms.</span><span class="sxs-lookup"><span data-stu-id="444dd-118">This cost is different from the standard cost of Trey Robotic Arms.</span></span>
