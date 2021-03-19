---
title: Configurar taxas de custo e de venda para produtos de catálogo – lite
description: Este tópico fornece informações sobre como configurar taxas de custo e de vendas para itens num catálogo de produtos.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f0941c549cc38f0938a5819e8cb6ca9912f14790
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274472"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="e65b6-103">Configurar taxas de custo e de venda para produtos de catálogo – lite</span><span class="sxs-lookup"><span data-stu-id="e65b6-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="e65b6-104">_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_</span><span class="sxs-lookup"><span data-stu-id="e65b6-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="e65b6-105">Definir preços para artigos de catálogo de produtos em Dynamics 365 Project Operations é o mesmo que no Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="e65b6-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="e65b6-106">No Project Operations, os produtos não podem ser estimados ou utilizados em projetos, pelo que os preços do catálogo de produtos não precisam de ser definidos nas listas de preços do projeto para cotações e contratos.</span><span class="sxs-lookup"><span data-stu-id="e65b6-106">In Project Operations, products can't be estimated or used on projects, so product catalog prices don't need to be set on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="e65b6-107">Utilize o campo **preço do produto** de uma cotação, contrato ou conta para configurar os preços do catálogo de produtos.</span><span class="sxs-lookup"><span data-stu-id="e65b6-107">Use the **Product Price** field of a quote, contract, or account to set up product catalog prices.</span></span> <span data-ttu-id="e65b6-108">Não estabeleça preços de catálogo de produtos nas listas de preços do projeto.</span><span class="sxs-lookup"><span data-stu-id="e65b6-108">Don't set up product catalog prices in the project price lists.</span></span> <span data-ttu-id="e65b6-109">As listas de preços do projeto são exclusivas do Project Operations.</span><span class="sxs-lookup"><span data-stu-id="e65b6-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="e65b6-110">A lógica de negócio específica da aplicação copia as listas de preços de uma cotação para um contrato.</span><span class="sxs-lookup"><span data-stu-id="e65b6-110">Application-specific business logic copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="e65b6-111">O resultado é uma lista de preços específica do contrato.</span><span class="sxs-lookup"><span data-stu-id="e65b6-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="e65b6-112">A operação de cópia pode atrasar o processo de ganho da proposta se a lista de preços do projeto na proposta ficar demasiado grande.</span><span class="sxs-lookup"><span data-stu-id="e65b6-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="e65b6-113">As listas de preços do produto não são copiadas para criar listas de preços personalizadas em contratos.</span><span class="sxs-lookup"><span data-stu-id="e65b6-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="e65b6-114">Como não há cópias envolvidas, o desempenho do processo de citação não é afetado.</span><span class="sxs-lookup"><span data-stu-id="e65b6-114">Because there's no copying involved, the performance of the quote process isn't affected.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]