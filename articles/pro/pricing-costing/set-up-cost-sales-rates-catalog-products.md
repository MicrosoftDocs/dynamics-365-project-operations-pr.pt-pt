---
title: Configurar taxas de custo e de venda para produtos de catálogo – lite
description: Este tópico fornece informações sobre como configurar taxas de custo e de vendas para itens num catálogo de produtos.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 135b182af73bdab7a3520589431332ad059ec497
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176715"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="50d52-103">Configurar taxas de custo e de venda para produtos de catálogo – lite</span><span class="sxs-lookup"><span data-stu-id="50d52-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="50d52-104">_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_</span><span class="sxs-lookup"><span data-stu-id="50d52-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="50d52-105">A configuração de preços para itens de catálogo de produtos no Dynamics 365 Project Operations é a mesma que no Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="50d52-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="50d52-106">Como os produtos não podem ser estimados ou utilizados em projetos no Project Operations, não há necessidade de definir preços do catálogo de produtos nas listas de preços do projeto para propostas e contratos.</span><span class="sxs-lookup"><span data-stu-id="50d52-106">Because products can't be estimated or used on projects in Project Operations, there is no need to set product catalog prices on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="50d52-107">Os preços do catálogo de produtos devem ser configurados no campo **Preço do Produto** de uma proposta, contrato ou conta.</span><span class="sxs-lookup"><span data-stu-id="50d52-107">Product catalog prices should be set up in the **Product Price** field of a quote, contract, or account.</span></span> <span data-ttu-id="50d52-108">Não configure preços de catálogo de produtos nas listas de preços do projeto para estas entidades.</span><span class="sxs-lookup"><span data-stu-id="50d52-108">Don't set up product catalog prices in the project price lists for these entities.</span></span> <span data-ttu-id="50d52-109">As listas de preços do projeto são exclusivas do Project Operations.</span><span class="sxs-lookup"><span data-stu-id="50d52-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="50d52-110">Existe uma lógica de negócio específica para aplicações que copia as listas de preços de uma proposta para um contrato.</span><span class="sxs-lookup"><span data-stu-id="50d52-110">There is application-specific business logic that copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="50d52-111">O resultado é uma lista de preços específica do contrato.</span><span class="sxs-lookup"><span data-stu-id="50d52-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="50d52-112">A operação de cópia pode atrasar o processo de ganho da proposta se a lista de preços do projeto na proposta ficar demasiado grande.</span><span class="sxs-lookup"><span data-stu-id="50d52-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="50d52-113">As listas de preços do produto não são copiadas para criar listas de preços personalizadas em contratos.</span><span class="sxs-lookup"><span data-stu-id="50d52-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="50d52-114">Isto significa que as listas de preços do produto não têm impacto no desempenho do processo de ganho das propostas.</span><span class="sxs-lookup"><span data-stu-id="50d52-114">This means that product price lists don't impact the performance of the quote win process.</span></span>
