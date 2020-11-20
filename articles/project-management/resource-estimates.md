---
title: Estimativas de recursos
description: Este tópico fornece informações sobre como as estimativas de recursos são calculadas no Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 454b8931db53739a7bc19364911109802a1ed087
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127388"
---
# <a name="resource-estimates"></a><span data-ttu-id="ed5e6-103">Estimativas de recursos</span><span class="sxs-lookup"><span data-stu-id="ed5e6-103">Resource estimates</span></span>

<span data-ttu-id="ed5e6-104">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="ed5e6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ed5e6-105">As estimativas de recursos provêm de um esforço faseado no tempo que é definido na estrutura hierárquica do trabalho, juntamente com as dimensões de preços aplicáveis.</span><span class="sxs-lookup"><span data-stu-id="ed5e6-105">Resource estimates come from time-phased effort that is defined in the work breakdown structure along with applicable pricing dimensions.</span></span> <span data-ttu-id="ed5e6-106">Tipicamente, o cálculo é **tarifa/hora para cada função x horas**.</span><span class="sxs-lookup"><span data-stu-id="ed5e6-106">Typically, the calculation is **rate/hr for each role x hours.**</span></span> <span data-ttu-id="ed5e6-107">O esforço faseado no tempo para cada recurso é armazenado no registo de atribuição de recursos.</span><span class="sxs-lookup"><span data-stu-id="ed5e6-107">The time-phased effort for each resource is stored in the resource assignment record.</span></span> <span data-ttu-id="ed5e6-108">Os preços são armazenados numa lista de preços predefinida.</span><span class="sxs-lookup"><span data-stu-id="ed5e6-108">The pricing is stored in a pre-defined price list.</span></span> <span data-ttu-id="ed5e6-109">A conversão de unidades é aplicada com base na lista de preços aplicável.</span><span class="sxs-lookup"><span data-stu-id="ed5e6-109">Unit conversion is applied based on the applicable price list.</span></span>

![Estimativas de Recursos](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a><span data-ttu-id="ed5e6-111">Preço de custo e moeda de custo predefinidos</span><span class="sxs-lookup"><span data-stu-id="ed5e6-111">Default cost price and cost currency</span></span>

<span data-ttu-id="ed5e6-112">Os preços de custos são assumidos por predefinição a partir da Unidade Organizacional.</span><span class="sxs-lookup"><span data-stu-id="ed5e6-112">Cost prices are defaulted from the Organizational Unit.</span></span>

## <a name="default-bill-rate-and-sales-currency"></a><span data-ttu-id="ed5e6-113">Taxa de faturação e moeda de venda predefinidas</span><span class="sxs-lookup"><span data-stu-id="ed5e6-113">Default bill rate and sales currency</span></span>

<span data-ttu-id="ed5e6-114">Os preços de venda são aplicados uma vez por negócio.</span><span class="sxs-lookup"><span data-stu-id="ed5e6-114">Sales prices are applied once per deal.</span></span> <span data-ttu-id="ed5e6-115">A hierarquia para assumir por predefinição a lista de preços de venda é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="ed5e6-115">The hierarchy for sale price list defaulting is as follows:</span></span>

1. <span data-ttu-id="ed5e6-116">Organização</span><span class="sxs-lookup"><span data-stu-id="ed5e6-116">Organization</span></span>
2. <span data-ttu-id="ed5e6-117">Cliente</span><span class="sxs-lookup"><span data-stu-id="ed5e6-117">Customer</span></span>
3. <span data-ttu-id="ed5e6-118">Proposta/contrato</span><span class="sxs-lookup"><span data-stu-id="ed5e6-118">Quote/contract</span></span>
