---
title: Receber itens na nota de encomenda a partir do requisito do item
description: Este tópico explica como receber itens numa nota de encomenda a partir de um requisito de item.
author: Yowelle
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a5b3622458da957ed150311f6ea75d5f1444d5f1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082571"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="9da71-103">Receber itens na nota de encomenda a partir do requisito do item</span><span class="sxs-lookup"><span data-stu-id="9da71-103">Receive items on purchase order from item requirement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9da71-104">Este tópico explica como receber itens numa nota de encomenda a partir de um requisito de item.</span><span class="sxs-lookup"><span data-stu-id="9da71-104">This topic explains how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="9da71-105">Ao utilizar um requisito de item em vez de uma transação de item, pode planear a entrega imediatamente antes de o item ser realmente utilizado, criar uma nota de encomenda, incluir o item no quadro do acordo comercial e incluir o requisito de item no planeamento da produção.</span><span class="sxs-lookup"><span data-stu-id="9da71-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="9da71-106">Esta tarefa utiliza o conjunto de dados USSI.</span><span class="sxs-lookup"><span data-stu-id="9da71-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="9da71-107">No painel de navegação, vá para **Módulos > Gestão de projetos e contabilística > Projetos > Todos os projetos**.</span><span class="sxs-lookup"><span data-stu-id="9da71-107">In the navigation pane, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="9da71-108">Na lista, selecione a ligação na linha pretendida.</span><span class="sxs-lookup"><span data-stu-id="9da71-108">In the list, select the link in the desired row.</span></span>
3. <span data-ttu-id="9da71-109">No Painel de Ação, selecione **Plano**.</span><span class="sxs-lookup"><span data-stu-id="9da71-109">On the Action Pane, select **Plan**.</span></span>
4. <span data-ttu-id="9da71-110">Selecione **Requisitos do item**.</span><span class="sxs-lookup"><span data-stu-id="9da71-110">Select **Item requirements**.</span></span>
5. <span data-ttu-id="9da71-111">Selecione **Novo**.</span><span class="sxs-lookup"><span data-stu-id="9da71-111">Select **New**.</span></span>
6. <span data-ttu-id="9da71-112">Na nova linha, introduza ou selecione um valor no campo **Número de item**.</span><span class="sxs-lookup"><span data-stu-id="9da71-112">In the new row, enter or select a value in the **Item number** field.</span></span>
7. <span data-ttu-id="9da71-113">No campo **Quantidade** , introduza um número.</span><span class="sxs-lookup"><span data-stu-id="9da71-113">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="9da71-114">Selecione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="9da71-114">Select **Save**.</span></span>
9. <span data-ttu-id="9da71-115">No Painel de Ação, selecione **Gestor**.</span><span class="sxs-lookup"><span data-stu-id="9da71-115">On the Action Pane, select **Manage**.</span></span>
10. <span data-ttu-id="9da71-116">Selecione **Funções**.</span><span class="sxs-lookup"><span data-stu-id="9da71-116">Select **Functions**.</span></span>
11. <span data-ttu-id="9da71-117">Selecione **Criar nota de encomenda**.</span><span class="sxs-lookup"><span data-stu-id="9da71-117">Select **Create purchase order**.</span></span>
12. <span data-ttu-id="9da71-118">Selecione a caixa de verificação **Incluir tudo**.</span><span class="sxs-lookup"><span data-stu-id="9da71-118">Select the **Include all** check box.</span></span>
13. <span data-ttu-id="9da71-119">No campo **Conta de fornecedores** , introduza ou selecione um valor.</span><span class="sxs-lookup"><span data-stu-id="9da71-119">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="9da71-120">Selecione **OK**.</span><span class="sxs-lookup"><span data-stu-id="9da71-120">Select **OK**.</span></span>
15. <span data-ttu-id="9da71-121">No painel de navegação, vá para **Módulos > Contas a pagar > Notas de encomenda > Todas as notas de encomenda**.</span><span class="sxs-lookup"><span data-stu-id="9da71-121">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
16. <span data-ttu-id="9da71-122">Na lista, selecione a ligação na linha pretendida.</span><span class="sxs-lookup"><span data-stu-id="9da71-122">In the list, select the link in the desired row.</span></span>
17. <span data-ttu-id="9da71-123">No Painel de Ação, selecione **Compra**.</span><span class="sxs-lookup"><span data-stu-id="9da71-123">On the Action Pane, select **Purchase**.</span></span>
18. <span data-ttu-id="9da71-124">Selecione **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="9da71-124">Select **Confirm**.</span></span>
19. <span data-ttu-id="9da71-125">No Painel de Ação, selecione **Receber**.</span><span class="sxs-lookup"><span data-stu-id="9da71-125">On the Action Pane, select **Receive**.</span></span>
20. <span data-ttu-id="9da71-126">Selecione **Receção de produto**.</span><span class="sxs-lookup"><span data-stu-id="9da71-126">Select **Product receipt**.</span></span>
21. <span data-ttu-id="9da71-127">No campo **Receção de produto** , digite um valor.</span><span class="sxs-lookup"><span data-stu-id="9da71-127">In the **Product receipt** field, type a value.</span></span>
22. <span data-ttu-id="9da71-128">Selecione **OK**.</span><span class="sxs-lookup"><span data-stu-id="9da71-128">Select **OK**.</span></span>

