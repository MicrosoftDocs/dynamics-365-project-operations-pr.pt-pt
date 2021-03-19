---
title: Itens de oportunidade baseados em produtos – lite
description: Este tópico fornece informações sobre os itens da oportunidade baseada em produtos no Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4f8da5258a1dd0aa4229654c0e1e222b8cf3a21a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272627"
---
# <a name="product-based-opportunity-lines---lite"></a><span data-ttu-id="ef77d-103">Itens de oportunidade baseados em produtos – lite</span><span class="sxs-lookup"><span data-stu-id="ef77d-103">Product-based opportunity lines - lite</span></span>

<span data-ttu-id="ef77d-104">_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_</span><span class="sxs-lookup"><span data-stu-id="ef77d-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ef77d-105">As linhas de oportunidade baseadas em produtos são itens na Oportunidade.</span><span class="sxs-lookup"><span data-stu-id="ef77d-105">Product-based opportunity lines are line items on the Opportunity.</span></span> <span data-ttu-id="ef77d-106">Estes itens de linha distintos estão na fatura eventual que é fornecida ao cliente.</span><span class="sxs-lookup"><span data-stu-id="ef77d-106">These distinct line items are on the eventual invoice that is provided to the customer.</span></span> <span data-ttu-id="ef77d-107">A fatura não inclui outros serviços adicionais.</span><span class="sxs-lookup"><span data-stu-id="ef77d-107">The invoice doesn't include any other additional services.</span></span> <span data-ttu-id="ef77d-108">Os gastos e consumos associados não são monitorizados em tarefas de quaisquer projetos relacionados.</span><span class="sxs-lookup"><span data-stu-id="ef77d-108">The associated spend and consumption isn't tracked on tasks of any related projects.</span></span>

<span data-ttu-id="ef77d-109">As linhas baseadas no produto podem ser itens de catálogo ou produtos acrescentados manualmente.</span><span class="sxs-lookup"><span data-stu-id="ef77d-109">Product-based lines can be catalog items or write-in products.</span></span> <span data-ttu-id="ef77d-110">A maior parte da funcionalidade nas linhas baseadas em produtos da Oportunidade segue a funcionalidade fornecida pela aplicação Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="ef77d-110">Most of the functionality on an Opportunity's product-based lines follows the functionality provided by the Dynamics 365 Sales application.</span></span> <span data-ttu-id="ef77d-111">Para mais informações sobre as linhas de oportunidade baseadas em produtos, consulte [Adicionar produtos a uma oportunidade](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span><span class="sxs-lookup"><span data-stu-id="ef77d-111">For more information about product-based opportunity lines, see [Add products to an opportunity](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span></span>

<span data-ttu-id="ef77d-112">O **Orçamento do cliente** é um conceito específico para linhas de oportunidade baseadas em projetos.</span><span class="sxs-lookup"><span data-stu-id="ef77d-112">**Customer budget** is a concept that is specific to project-based opportunity lines.</span></span> <span data-ttu-id="ef77d-113">O campo do **Orçamento do cliente** rastreia o valor que o cliente está disposto a pagar pelo item.</span><span class="sxs-lookup"><span data-stu-id="ef77d-113">The **Customer budget** field tracks the amount the customer is willing to pay for the item.</span></span>

<span data-ttu-id="ef77d-114">Quando o método de receita do resumo de Oportunidade é **Calculado pelo sistema**, os valores orçamentais do cliente através das linhas de oportunidade são resumidos para calcular as receitas estimadas.</span><span class="sxs-lookup"><span data-stu-id="ef77d-114">When the revenue method of the Opportunity summary is **System Calculated**, the customer budget values across the opportunity lines are summarized to calculate the estimated revenue.</span></span> 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]