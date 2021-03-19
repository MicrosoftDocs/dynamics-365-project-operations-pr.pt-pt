---
title: Criar uma lista de preços
description: Como criar uma lista de preços no Project Service
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 0732ccca43e404412efae8a91873e43c28d041ca
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290328"
---
# <a name="create-a-price-list-project-service"></a><span data-ttu-id="4f507-103">Criar uma lista de preços (Project Service)</span><span class="sxs-lookup"><span data-stu-id="4f507-103">Create a price list (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="4f507-104">As listas de preços fornecem um modelo que os gestores de contas podem utilizar para criar propostas e projetos, bem como para estabelecer os custos de um projeto.</span><span class="sxs-lookup"><span data-stu-id="4f507-104">Price lists provide a template your account managers can use for creating quotes and projects, and for establishing the costs of a project.</span></span> <span data-ttu-id="4f507-105">Fornecem uma lista de itens das funções e das despesas, bem como o preço cobrará por cada.</span><span class="sxs-lookup"><span data-stu-id="4f507-105">They provide a line item list of roles and expenses, and the price you will charge for each.</span></span> <span data-ttu-id="4f507-106">Pode criar várias listas de preços para manter estruturas de preços separadas para diferentes regiões em que vende os seus produtos ou para canais de vendas diferentes.</span><span class="sxs-lookup"><span data-stu-id="4f507-106">You can create multiple price lists so that you can maintain separate price structures for different regions you sell your products in or for different sales channels.</span></span> <span data-ttu-id="4f507-107">Recomenda-se que crie pelo menos uma lista de preços para cada moeda em que planeie faturar os clientes.</span><span class="sxs-lookup"><span data-stu-id="4f507-107">It’s a good idea to create at least one price list for every currency you plan to bill your customers in.</span></span>  
  
<span data-ttu-id="4f507-108">Para criar estimativas financeiras para o trabalho a entregar, certifique-se de que cada projeto tem uma lista de preços de venda e um custo de suporte.</span><span class="sxs-lookup"><span data-stu-id="4f507-108">To create financial estimates for the work to be delivered, make sure every project has a backing cost and sales price list.</span></span> <span data-ttu-id="4f507-109">Configure um custo predefinido e uma lista de preços de venda que se apliquem a todos os projetos criados na sua organização.</span><span class="sxs-lookup"><span data-stu-id="4f507-109">Set up a default cost and sales pricelist that applies to all projects created in your organization.</span></span>  
  
<span data-ttu-id="4f507-110">As listas de preços baseiam-se nas funções e nas categorias de despesas, pelo que antes de criar uma lista de preços deve certificar-se de que já configurou as funções e as categorias de despesas que pretende utilizar quando cria a lista de preços.</span><span class="sxs-lookup"><span data-stu-id="4f507-110">Price lists rely on roles and expense categories, so before you create a price list, make sure you’ve already configured the roles and expense categories you want to use while creating the price list.</span></span>  
  
1.  <span data-ttu-id="4f507-111">Vá para **Project Service > Listas de Preços**.</span><span class="sxs-lookup"><span data-stu-id="4f507-111">Go to **Project Service > Price Lists**.</span></span>  
  
2.  <span data-ttu-id="4f507-112">Clique em **Novo**.</span><span class="sxs-lookup"><span data-stu-id="4f507-112">Click **New**.</span></span>  
  
3.  <span data-ttu-id="4f507-113">Em **Contexto**, selecione se esta lista de preços é para **Custo**, **Compra** ou **Vendas**.</span><span class="sxs-lookup"><span data-stu-id="4f507-113">In **Context**, select whether this price list is for **Cost**, **Purchase**, or **Sales**.</span></span>  
  
4.  <span data-ttu-id="4f507-114">Em **Nome**, introduza o nome da lista de preços.</span><span class="sxs-lookup"><span data-stu-id="4f507-114">In **Name**, enter a name for the price list.</span></span>  
  
5.  <span data-ttu-id="4f507-115">Em **Moeda**, selecione a moeda que vai utilizar para faturação ou definição de custos.</span><span class="sxs-lookup"><span data-stu-id="4f507-115">In **Currency**, select the currency you’re going to use for billing or costing.</span></span>  
  
6.  <span data-ttu-id="4f507-116">Em **Unidade de Tempo**, especifique o período de tempo durante o qual o preço é aplicado, por exemplo, dia ou hora.</span><span class="sxs-lookup"><span data-stu-id="4f507-116">In **Time Unit**, specify the period of time the price applies to, such as day or hour.</span></span>  
  
7.  <span data-ttu-id="4f507-117">Preencha a **Data de Início**, **Data de Fim** e **Descrição**, conforme for necessário.</span><span class="sxs-lookup"><span data-stu-id="4f507-117">Fill in the **Start Date**, **End Date**, and **Description** as needed.</span></span>  
  
8.  <span data-ttu-id="4f507-118">Clique em **Guardar** para criar o registo para poder continuar a editá-lo.</span><span class="sxs-lookup"><span data-stu-id="4f507-118">Click **Save** to create the record so you can continue editing it.</span></span>  
  
9. <span data-ttu-id="4f507-119">Para adicionar uma função de preços à lista de preços, clique em **+** em **Preços da função**.</span><span class="sxs-lookup"><span data-stu-id="4f507-119">To add a role price to the price list, click **+** under **Role prices**.</span></span>  
  
10. <span data-ttu-id="4f507-120">No painel **Preço da Função**, preencha os detalhes e, em seguida, clique em **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="4f507-120">In the **Role Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="4f507-121">Continue a adicionar preços da função, conforme for necessário.</span><span class="sxs-lookup"><span data-stu-id="4f507-121">Continue adding role prices as necessary.</span></span> <span data-ttu-id="4f507-122">Quando terminar, clique em **Guardar** no canto inferior direito do ecrã.</span><span class="sxs-lookup"><span data-stu-id="4f507-122">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
11. <span data-ttu-id="4f507-123">Para adicionar um preço da categoria de despesas à lista de preços, clique em **+** em **Preços de categoria**.</span><span class="sxs-lookup"><span data-stu-id="4f507-123">To add an expense category price to the price list, click **+** under **Category prices**.</span></span>  
  
12. <span data-ttu-id="4f507-124">No painel **Preço de Categoria de Transação**, preencha os detalhes e, em seguida, clique em **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="4f507-124">In the **Transaction Category Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="4f507-125">Continue a adicionar preços de categoria, conforme for necessário.</span><span class="sxs-lookup"><span data-stu-id="4f507-125">Continue adding category prices as necessary.</span></span> <span data-ttu-id="4f507-126">Quando terminar, clique em **Guardar** no canto inferior direito do ecrã.</span><span class="sxs-lookup"><span data-stu-id="4f507-126">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
13. <span data-ttu-id="4f507-127">Para adicionar itens da lista de preços à lista de preços, clique em **+** em **Itens da lista de preços**.</span><span class="sxs-lookup"><span data-stu-id="4f507-127">To add price list items to the price list, click **+** under **Price List Items**.</span></span>  
  
14. <span data-ttu-id="4f507-128">No painel **Item da Lista de Preços**, preencha os detalhes e, em seguida, clique em **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="4f507-128">In the **Price List Item** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="4f507-129">Continue a adicionar itens da lista de preços, conforme for necessário.</span><span class="sxs-lookup"><span data-stu-id="4f507-129">Continue adding price list items as necessary.</span></span> <span data-ttu-id="4f507-130">Quando terminar, clique em **Guardar** no canto inferior direito do ecrã.</span><span class="sxs-lookup"><span data-stu-id="4f507-130">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
15. <span data-ttu-id="4f507-131">Para adicionar relações de território à lista de preços, clique em **+** em **Relações de Territórios**.</span><span class="sxs-lookup"><span data-stu-id="4f507-131">To add territory relationships to the price list, click **+** under **Territory Relationships**.</span></span>  
  
16. <span data-ttu-id="4f507-132">Na janela **Nova Ligação**, preencha os detalhes e, em seguida, clique em **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="4f507-132">In the **New Connection** window, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="4f507-133">Continue a adicionar relações de território, conforme for necessário.</span><span class="sxs-lookup"><span data-stu-id="4f507-133">Continue adding territory relationships as necessary.</span></span> <span data-ttu-id="4f507-134">Quando terminar, clique em **Guardar** no canto inferior direito do ecrã.</span><span class="sxs-lookup"><span data-stu-id="4f507-134">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="4f507-135">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="4f507-135">See Also</span></span>  
 [<span data-ttu-id="4f507-136">Configurar Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="4f507-136">Configure Project Service Automation</span></span>](../psa/configure.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]