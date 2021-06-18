---
title: Receber itens na nota de encomenda a partir do requisito do item
description: Este tópico explica como receber itens numa nota de encomenda a partir de um requisito de item.
author: Yowelle
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0e0c4a75f1d86538cc773af1f7c0ae3c83ef0ad5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011700"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="5501e-103">Receber itens na nota de encomenda a partir do requisito do item</span><span class="sxs-lookup"><span data-stu-id="5501e-103">Receive items on purchase order from item requirement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5501e-104">Este tópico explica como receber itens numa nota de encomenda a partir de um requisito de item.</span><span class="sxs-lookup"><span data-stu-id="5501e-104">This topic explains how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="5501e-105">Ao utilizar um requisito de item em vez de uma transação de item, pode planear a entrega imediatamente antes de o item ser realmente utilizado, criar uma nota de encomenda, incluir o item no quadro do acordo comercial e incluir o requisito de item no planeamento da produção.</span><span class="sxs-lookup"><span data-stu-id="5501e-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="5501e-106">Esta tarefa utiliza o conjunto de dados USSI.</span><span class="sxs-lookup"><span data-stu-id="5501e-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="5501e-107">No painel de navegação, vá para **Módulos > Gestão de projetos e contabilística > Projetos > Todos os projetos**.</span><span class="sxs-lookup"><span data-stu-id="5501e-107">In the navigation pane, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="5501e-108">Na lista, selecione a ligação na linha pretendida.</span><span class="sxs-lookup"><span data-stu-id="5501e-108">In the list, select the link in the desired row.</span></span>
3. <span data-ttu-id="5501e-109">No Painel de Ação, selecione **Plano**.</span><span class="sxs-lookup"><span data-stu-id="5501e-109">On the Action Pane, select **Plan**.</span></span>
4. <span data-ttu-id="5501e-110">Selecione **Requisitos do item**.</span><span class="sxs-lookup"><span data-stu-id="5501e-110">Select **Item requirements**.</span></span>
5. <span data-ttu-id="5501e-111">Selecione **Novo**.</span><span class="sxs-lookup"><span data-stu-id="5501e-111">Select **New**.</span></span>
6. <span data-ttu-id="5501e-112">Na nova linha, introduza ou selecione um valor no campo **Número de item**.</span><span class="sxs-lookup"><span data-stu-id="5501e-112">In the new row, enter or select a value in the **Item number** field.</span></span>
7. <span data-ttu-id="5501e-113">No campo **Quantidade**, introduza um número.</span><span class="sxs-lookup"><span data-stu-id="5501e-113">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="5501e-114">Selecione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="5501e-114">Select **Save**.</span></span>
9. <span data-ttu-id="5501e-115">No Painel de Ação, selecione **Gestor**.</span><span class="sxs-lookup"><span data-stu-id="5501e-115">On the Action Pane, select **Manage**.</span></span>
10. <span data-ttu-id="5501e-116">Selecione **Funções**.</span><span class="sxs-lookup"><span data-stu-id="5501e-116">Select **Functions**.</span></span>
11. <span data-ttu-id="5501e-117">Selecione **Criar nota de encomenda**.</span><span class="sxs-lookup"><span data-stu-id="5501e-117">Select **Create purchase order**.</span></span>
12. <span data-ttu-id="5501e-118">Selecione a caixa de verificação **Incluir tudo**.</span><span class="sxs-lookup"><span data-stu-id="5501e-118">Select the **Include all** check box.</span></span>
13. <span data-ttu-id="5501e-119">No campo **Conta de fornecedores**, introduza ou selecione um valor.</span><span class="sxs-lookup"><span data-stu-id="5501e-119">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="5501e-120">Selecione **OK**.</span><span class="sxs-lookup"><span data-stu-id="5501e-120">Select **OK**.</span></span>
15. <span data-ttu-id="5501e-121">No painel de navegação, vá para **Módulos > Contas a pagar > Notas de encomenda > Todas as notas de encomenda**.</span><span class="sxs-lookup"><span data-stu-id="5501e-121">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
16. <span data-ttu-id="5501e-122">Na lista, selecione a ligação na linha pretendida.</span><span class="sxs-lookup"><span data-stu-id="5501e-122">In the list, select the link in the desired row.</span></span>
17. <span data-ttu-id="5501e-123">No Painel de Ação, selecione **Compra**.</span><span class="sxs-lookup"><span data-stu-id="5501e-123">On the Action Pane, select **Purchase**.</span></span>
18. <span data-ttu-id="5501e-124">Selecione **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="5501e-124">Select **Confirm**.</span></span>
19. <span data-ttu-id="5501e-125">No Painel de Ação, selecione **Receber**.</span><span class="sxs-lookup"><span data-stu-id="5501e-125">On the Action Pane, select **Receive**.</span></span>
20. <span data-ttu-id="5501e-126">Selecione **Receção de produto**.</span><span class="sxs-lookup"><span data-stu-id="5501e-126">Select **Product receipt**.</span></span>
21. <span data-ttu-id="5501e-127">No campo **Receção de produto**, digite um valor.</span><span class="sxs-lookup"><span data-stu-id="5501e-127">In the **Product receipt** field, type a value.</span></span>
22. <span data-ttu-id="5501e-128">Selecione **OK**.</span><span class="sxs-lookup"><span data-stu-id="5501e-128">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]