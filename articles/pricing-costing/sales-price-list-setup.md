---
title: Configuração de lista de preços de vendas
description: Este tópico fornece informação sobre as listas de preços de vendas para preços do projeto.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1d2c797b72666123eb0a18d2d0c1df9fe3d207f7
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082459"
---
# <a name="sales-price-list-setup"></a><span data-ttu-id="77ecd-103">Configuração de lista de preços de vendas</span><span class="sxs-lookup"><span data-stu-id="77ecd-103">Sales price list setup</span></span>

<span data-ttu-id="77ecd-104">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="77ecd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="77ecd-105">Para obter propostas e contratos do projeto, uma lista de preços do projeto tem um padrão de substituição de preços diferente da lista de preços de produtos.</span><span class="sxs-lookup"><span data-stu-id="77ecd-105">For project quotes and contracts, a project price list has a different price override pattern than a product price list.</span></span> <span data-ttu-id="77ecd-106">Num item de proposta baseado no catálogo de produtos, pode substituir o preço por funções e categorias diretamente na linha de proposta, porque cada linha de proposta aponta para exatamente um item de catálogo.</span><span class="sxs-lookup"><span data-stu-id="77ecd-106">On a product catalog–based quote line, you can override the price to roles and categories directly on the quote line, because each quote line points to exactly one catalog item.</span></span> <span data-ttu-id="77ecd-107">No entanto, numa linha de proposta com base em projetos, não pode substituir o preço por funções e categorias diretamente na linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="77ecd-107">However, on a project-based quote line, you can't override the price to roles and categories directly on the quote line.</span></span> <span data-ttu-id="77ecd-108">Pode usar a lista de preços do projeto para trabalhar com os dois padrões distintos de definição manual.</span><span class="sxs-lookup"><span data-stu-id="77ecd-108">You can use the project price list to work with the two distinct override patterns.</span></span>

> [!NOTE]
> <span data-ttu-id="77ecd-109">Recomendamos que tenha uma lista de preços separada para os recursos do seu projeto e itens do catálogo, devido às diferenças de comportamento entre os dois quando os preços são substituídos.</span><span class="sxs-lookup"><span data-stu-id="77ecd-109">We recommend that you have a separate price list for your project resources and your catalog items, because of the behavior differences between the two when you override pricing.</span></span>

<span data-ttu-id="77ecd-110">Cada uma das seguintes entidades pode ter uma ou mais listas de preços de venda associadas para a definição de preços do projeto:</span><span class="sxs-lookup"><span data-stu-id="77ecd-110">Each of the following entities can have one or more associated sales price lists for project pricing:</span></span>

- <span data-ttu-id="77ecd-111">Cliente (conta)</span><span class="sxs-lookup"><span data-stu-id="77ecd-111">Customer (account)</span></span> 
- <span data-ttu-id="77ecd-112">Oportunidade</span><span class="sxs-lookup"><span data-stu-id="77ecd-112">Opportunity</span></span> 
- <span data-ttu-id="77ecd-113">Proposta</span><span class="sxs-lookup"><span data-stu-id="77ecd-113">Quote</span></span> 
- <span data-ttu-id="77ecd-114">Contrato do Projeto</span><span class="sxs-lookup"><span data-stu-id="77ecd-114">Project Contract</span></span>

<span data-ttu-id="77ecd-115">A associação destas entidades com uma lista de preços é indicada pelas listas de preços do projeto.</span><span class="sxs-lookup"><span data-stu-id="77ecd-115">The association of these entities with a price list is indicated by the project price lists.</span></span> <span data-ttu-id="77ecd-116">Pode associar uma ou mais listas de preços às entidades de vendas Cliente, Oportunidade, Proposta e Contrato do Projeto.</span><span class="sxs-lookup"><span data-stu-id="77ecd-116">You can associate one or more price lists with the Customer, Opportunity, Quote, and Project Contract sales entities.</span></span>

<span data-ttu-id="77ecd-117">Uma lista de preços predefinida do projeto não é introduzida automaticamente num registo de cliente.</span><span class="sxs-lookup"><span data-stu-id="77ecd-117">A default project price list isn't automatically entered on a customer record.</span></span> <span data-ttu-id="77ecd-118">No entanto, pode anexar manualmente uma lista de preços do projeto ao registo de cliente.</span><span class="sxs-lookup"><span data-stu-id="77ecd-118">However, you can manually attach a project price list to the customer record.</span></span> <span data-ttu-id="77ecd-119">No entanto, deverá anexar manualmente uma lista de preços do projeto quando tiver um contrato de preços personalizado com o cliente.</span><span class="sxs-lookup"><span data-stu-id="77ecd-119">Nevertheless, you should manually attach a project price list only when you have a custom pricing agreement with the customer.</span></span> 

<span data-ttu-id="77ecd-120">Quando uma lista de preços do projeto é associada a uma entidade de vendas, as seguintes informações são validadas:</span><span class="sxs-lookup"><span data-stu-id="77ecd-120">When a project price list is attached to a sales entity, the following information is validated:</span></span>

- <span data-ttu-id="77ecd-121">A lista de preços tem um contexto de **Vendas**.</span><span class="sxs-lookup"><span data-stu-id="77ecd-121">The price list has a context of **Sales**.</span></span> 
- <span data-ttu-id="77ecd-122">A moeda da lista de preços corresponde com a moeda do cliente.</span><span class="sxs-lookup"><span data-stu-id="77ecd-122">The price list currency matches the customer currency.</span></span> 

<span data-ttu-id="77ecd-123">Num contrato do projeto, a seguinte ordem de precedência é usada para definir automaticamente as listas de preços relacionadas com os projetos:</span><span class="sxs-lookup"><span data-stu-id="77ecd-123">On a project contract, the following order of precedence is used to automatically set related project price lists:</span></span>

1. <span data-ttu-id="77ecd-124">Proposta</span><span class="sxs-lookup"><span data-stu-id="77ecd-124">Quote</span></span>
2. <span data-ttu-id="77ecd-125">Oportunidade</span><span class="sxs-lookup"><span data-stu-id="77ecd-125">Opportunity</span></span>
3. <span data-ttu-id="77ecd-126">Cliente</span><span class="sxs-lookup"><span data-stu-id="77ecd-126">Customer</span></span> 
4. <span data-ttu-id="77ecd-127">Definições globais</span><span class="sxs-lookup"><span data-stu-id="77ecd-127">Global settings</span></span> 

<span data-ttu-id="77ecd-128">Quando uma lista de preços do projeto é introduzida por predefinição, o sistema valida que a moeda corresponde com a moeda do cliente e que as listas de preços predefinidas que foram introduzidas têm um contexto de **Vendas**.</span><span class="sxs-lookup"><span data-stu-id="77ecd-128">When a project price list is entered by default, the system validates that the currency matches the customer’s currency, and that the default price lists that have been entered have a context of **Sales**.</span></span>

<span data-ttu-id="77ecd-129">Pode associar várias listas de preços do projeto às entidades Cliente, Oportunidade, Proposta e Contrato do Projeto.</span><span class="sxs-lookup"><span data-stu-id="77ecd-129">You can associate multiple project price lists with the Customer, Opportunity, Quote, and Project Contract entities.</span></span> <span data-ttu-id="77ecd-130">Esta capacidade suporta preços predefinidos específicos de data para um contrato do projeto de execução demorada, onde poderá necessitar de mais de uma lista de preços para contabilizar as atualizações de preços que ocorrem devido à inflação.</span><span class="sxs-lookup"><span data-stu-id="77ecd-130">This capability supports date-specific default prices for a long-running project contract, where you might require more than one price list to account for price updates that occur because of inflation.</span></span> <span data-ttu-id="77ecd-131">No entanto, se as listas de preços associadas è entidade Cliente, Oportunidade, Proposta ou Contrato do Projeto tiverem a data efetiva sobreposta, os preços predefinidos poderão estar incorretos.</span><span class="sxs-lookup"><span data-stu-id="77ecd-131">However, if the price lists that you associate with the Customer, Opportunity, Quote, or Project Contract entity have overlapping date effectivity, the default prices might be incorrect.</span></span> <span data-ttu-id="77ecd-132">Consequentemente, deve certificar-se de que as listas de preços do projeto que têm a data efetiva sobreposta não estão associadas a essas entidades.</span><span class="sxs-lookup"><span data-stu-id="77ecd-132">Therefore, you should make sure that project price lists that have overlapping date effectivity aren't associated with those entities.</span></span>
