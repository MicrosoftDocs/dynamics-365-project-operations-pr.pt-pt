---
title: Itens de oportunidade baseados em produtos
description: Este tópico fornece informações sobre os itens da oportunidade baseada em produtos no Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 17ffcf8dc94d42102115281d281d6b553cf1fa17
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082330"
---
# <a name="product-based-opportunity-lines"></a><span data-ttu-id="dd6b8-103">Itens de oportunidade baseados em produtos</span><span class="sxs-lookup"><span data-stu-id="dd6b8-103">Product-based opportunity lines</span></span>

<span data-ttu-id="dd6b8-104">_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_</span><span class="sxs-lookup"><span data-stu-id="dd6b8-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="dd6b8-105">As linhas de oportunidade baseadas em produtos são itens na Oportunidade.</span><span class="sxs-lookup"><span data-stu-id="dd6b8-105">Product-based opportunity lines are line items on the Opportunity.</span></span> <span data-ttu-id="dd6b8-106">Estas linhas são entregues ao cliente como itens distintos na fatura eventual, sem quaisquer outros serviços de valor acrescentado.</span><span class="sxs-lookup"><span data-stu-id="dd6b8-106">These lines are delivered to the customer as distinct line items on the eventual invoice without any other value-added services.</span></span> <span data-ttu-id="dd6b8-107">Os gastos e consumos associados não são monitorizados em tarefas de quaisquer projetos relacionados.</span><span class="sxs-lookup"><span data-stu-id="dd6b8-107">The associated spend and consumption isn't tracked on tasks of any related projects.</span></span>

<span data-ttu-id="dd6b8-108">As linhas baseadas no produto podem ser itens de catálogo ou produtos acrescentados manualmente.</span><span class="sxs-lookup"><span data-stu-id="dd6b8-108">Product-based lines can be catalog items or write-in products.</span></span> <span data-ttu-id="dd6b8-109">A maior parte da funcionalidade nas linhas baseadas em produtos da Oportunidade segue a funcionalidade fornecida pela aplicação Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="dd6b8-109">Most of the functionality on an Opportunity's product-based lines follows the functionality provided by the Dynamics 365 Sales application.</span></span> <span data-ttu-id="dd6b8-110">Para mais informações sobre as linhas de oportunidade baseadas em produtos, consulte [Adicionar produtos a uma oportunidade](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span><span class="sxs-lookup"><span data-stu-id="dd6b8-110">For more information about product-based opportunity lines, see [Add products to an opportunity](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span></span>

<span data-ttu-id="dd6b8-111">Um conceito sobre as linhas de oportunidade baseadas em produtos específicas para oportunidades baseadas em projetos é **Orçamento do Cliente**.</span><span class="sxs-lookup"><span data-stu-id="dd6b8-111">One concept about product-based opportunity lines that is specific to project-based opportunities is **Customer Budget**.</span></span> <span data-ttu-id="dd6b8-112">Utilize este campo para monitorizar o montante que o cliente está disposto a pagar pelo item.</span><span class="sxs-lookup"><span data-stu-id="dd6b8-112">Use this field to track the amount the customer is willing to pay for the line item.</span></span>

<span data-ttu-id="dd6b8-113">Se o método de receitas do Resumo da oportunidade for definido como **Calculada pelo Sistema** , os valores do orçamento do cliente nas linhas baseadas em produtos e projetos são resumidos para calcular as receitas estimadas.</span><span class="sxs-lookup"><span data-stu-id="dd6b8-113">If the revenue method of the Opportunity summary is set to **System Calculated** , the customer budget values across product- and project-based lines are summarized to calculate the estimated revenue.</span></span>
