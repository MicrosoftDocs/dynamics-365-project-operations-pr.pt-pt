---
title: Custo dos itens de contrato baseados em produtos – lite
description: Este tópico fornece informações sobre como criar
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0e961bcf32a5dd662b7cd27a23eb5f664c45c292
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177255"
---
# <a name="cost-product-based-contract-lines---lite"></a><span data-ttu-id="c2360-103">Custo dos itens de contrato baseados em produtos – lite</span><span class="sxs-lookup"><span data-stu-id="c2360-103">Cost product-based contract lines - lite</span></span>

<span data-ttu-id="c2360-104">_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_</span><span class="sxs-lookup"><span data-stu-id="c2360-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="c2360-105">Os itens de contrato baseados em produtos no Dynamics 365 Project Operations incluem o campo **Preço de Custo**, que armazena o preço de custo do produto para cálculos de rentabilidade a jusante.</span><span class="sxs-lookup"><span data-stu-id="c2360-105">Product-based contract lines in Dynamics 365 Project Operations include the **Cost Price** field, which stores the cost price of the product for downstream profitability calculations.</span></span>

<span data-ttu-id="c2360-106">Quando um item de contrato baseado em produtos é criado para um produto do catálogo, o custo do item de contrato baseado em produtos assume a predefinição o valor do campo **Custo Padrão** no catálogo de produtos.</span><span class="sxs-lookup"><span data-stu-id="c2360-106">When a product-based contract line is created for a catalog product, the cost of the product-based contract line defaults from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="c2360-107">O campo **Custo Padrão** no catálogo de produtos está configurado na moeda base da Organização.</span><span class="sxs-lookup"><span data-stu-id="c2360-107">The **Standard Cost** field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="c2360-108">Quando o custo unitário assume a predefinição no item de contrato, é convertido na moeda de venda do contrato.</span><span class="sxs-lookup"><span data-stu-id="c2360-108">When the unit cost defaults on the contract line, it's converted into the sales currency on the contract.</span></span>

## <a name="unit-cost-on-a-product-based-contract-line"></a><span data-ttu-id="c2360-109">Custo unitário num item de contrato baseado em produtos</span><span class="sxs-lookup"><span data-stu-id="c2360-109">Unit cost on a product-based contract line</span></span>

<span data-ttu-id="c2360-110">Ter um custo unitário num item de contrato baseado em produtos permite custos diferentes para produtos para cada venda de uma unidade.</span><span class="sxs-lookup"><span data-stu-id="c2360-110">Having a unit cost on a product-based contract line allows for different product costs for each sale of a unit.</span></span> <span data-ttu-id="c2360-111">Embora nem sempre seja necessário, existem certos cenários em que o custo do produto pode ser descontado para o cliente pelo fornecedor.</span><span class="sxs-lookup"><span data-stu-id="c2360-111">While not always necessary, there are certain scenarios where the cost of the product may be discounted for the customer by the supplier.</span></span> <span data-ttu-id="c2360-112">Considere o seguinte cenário:</span><span class="sxs-lookup"><span data-stu-id="c2360-112">Consider the following scenario:</span></span>

<span data-ttu-id="c2360-113">A Fabrikam Robotics está a instalar braços robóticos nas linhas de montagem da Adatum Corporation.</span><span class="sxs-lookup"><span data-stu-id="c2360-113">Fabrikam Robotics is installing robotic arms at Adatum Corporation's assembly lines.</span></span> <span data-ttu-id="c2360-114">A Fabrikam presta serviços de instalação, mas os braços robóticos são adquiridos à Trey Research.</span><span class="sxs-lookup"><span data-stu-id="c2360-114">Fabrikam provides installation services but the robotic arms are procured from Trey Research.</span></span> <span data-ttu-id="c2360-115">Se a instalação de braços robóticos na Adatum Corporation abrir uma nova indústria vertical para a Trey Research, pode oferecer um desconto especial para este negócio à Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="c2360-115">If the installation of robotic arms at Adatum Corporation opens a new industry vertical for Trey Research, they could offer a special discount for this deal to Fabrikam.</span></span> <span data-ttu-id="c2360-116">Neste caso, a Fabrikam cria um item de contrato baseado em produtos para Braços Robóticos e insere um custo por unidade para este contrato que é diferente do custo padrão dos braços robóticos da Trey Research.</span><span class="sxs-lookup"><span data-stu-id="c2360-116">In this case, Fabrikam creates a product-based contract line for Robotic Arms and inputs a per unit cost for this contract that is different from the standard cost of robotic arms from Trey Research.</span></span>
