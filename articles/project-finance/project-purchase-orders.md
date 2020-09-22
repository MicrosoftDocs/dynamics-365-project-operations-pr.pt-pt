---
title: Notas de encomenda para um projeto
description: Este artigo descreve os vários métodos que pode utilizar para criar notas de encomenda para um projeto. O método que utilizar depende do objetivo da nota de encomenda e quando os itens são consumidos e cobrados a um projeto.
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a4975b9f9e20906fb1259e36a07d8ef3db4f4fee
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754523"
---
# <a name="purchase-orders-for-a-project"></a><span data-ttu-id="02614-104">Notas de encomenda para um projeto</span><span class="sxs-lookup"><span data-stu-id="02614-104">Purchase orders for a project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="02614-105">Este artigo descreve os vários métodos que pode utilizar para criar notas de encomenda para um projeto.</span><span class="sxs-lookup"><span data-stu-id="02614-105">This article describes the various methods that you can use to create purchase orders for a project.</span></span> <span data-ttu-id="02614-106">O método que utilizar depende do objetivo da nota de encomenda e quando os itens são consumidos e cobrados a um projeto.</span><span class="sxs-lookup"><span data-stu-id="02614-106">The method that you use depends on the purpose of the purchase order, and when the purchased items are consumed and charged to a project.</span></span>

### <a name="methods-for-creating-a-purchase-order"></a><span data-ttu-id="02614-107">Métodos para criar uma nota de encomenda</span><span class="sxs-lookup"><span data-stu-id="02614-107">Methods for creating a purchase order</span></span>

<span data-ttu-id="02614-108">Pode utilizar um dos seguintes métodos para criar uma nota de encomenda em Gestão de projetos e contabilística.</span><span class="sxs-lookup"><span data-stu-id="02614-108">You can use one of the following methods to create a purchase order in Project management and accounting.</span></span> <span data-ttu-id="02614-109">O objetivo da nota de encomenda é determinar quando nota de encomenda é consumida e, portanto, quando os itens são cobrados a um projeto.</span><span class="sxs-lookup"><span data-stu-id="02614-109">The purpose of the purchase order determines when the purchase order is consumed and, therefore, when items are charged to a project.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="02614-110">Método</span><span class="sxs-lookup"><span data-stu-id="02614-110">Method</span></span></th>
<th><span data-ttu-id="02614-111">Objetivo</span><span class="sxs-lookup"><span data-stu-id="02614-111">Purpose</span></span></th>
<th><span data-ttu-id="02614-112">Consumo de itens</span><span class="sxs-lookup"><span data-stu-id="02614-112">Consumption of items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="02614-113">Crie uma nota de encomenda diretamente a partir de um projeto.</span><span class="sxs-lookup"><span data-stu-id="02614-113">Create a purchase order directly from a project.</span></span></td>
<td><span data-ttu-id="02614-114">Utilize este método para comprar itens a um fornecedor externo para consumo num projeto.</span><span class="sxs-lookup"><span data-stu-id="02614-114">Use this method to purchase items from an external vendor for consumption on a project.</span></span> <span data-ttu-id="02614-115">Pode criar a nota de encomenda de duas formas:</span><span class="sxs-lookup"><span data-stu-id="02614-115">You can create the purchase order in two ways:</span></span>
<ul>
<li><span data-ttu-id="02614-116">A partir do próprio projeto.</span><span class="sxs-lookup"><span data-stu-id="02614-116">From the project itself.</span></span> <span data-ttu-id="02614-117">Neste caso, o projeto já está definido para a nota de encomenda.</span><span class="sxs-lookup"><span data-stu-id="02614-117">In this case, the project is already defined for the purchase order.</span></span></li>
<li><span data-ttu-id="02614-118">Ao navegar para a nota de encomenda do projeto.</span><span class="sxs-lookup"><span data-stu-id="02614-118">By navigating to the project purchase order.</span></span> <span data-ttu-id="02614-119">Tem de selecionar o fornecedor e o projeto para o qual pretende criar a nota de encomenda.</span><span class="sxs-lookup"><span data-stu-id="02614-119">You must select both the vendor and the project to create the purchase order for.</span></span></li>
</ul></td>
<td><span data-ttu-id="02614-120">Os itens são consumidos quando a fatura do fornecedor é atualizada.</span><span class="sxs-lookup"><span data-stu-id="02614-120">Items are consumed when the vendor invoice is updated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="02614-121">Crie uma nota de encomenda a partir de uma nota de encomenda.</span><span class="sxs-lookup"><span data-stu-id="02614-121">Create a purchase order from a sales order.</span></span></td>
<td><span data-ttu-id="02614-122">Utilize este método para comprar itens quando criar uma ordem de venda a partir de um projeto.</span><span class="sxs-lookup"><span data-stu-id="02614-122">Use this method to purchase items when you create a sales order from a project.</span></span></td>
<td><span data-ttu-id="02614-123">Os itens são consumidos quando a ordem de venda é faturada ao cliente.</span><span class="sxs-lookup"><span data-stu-id="02614-123">Items are consumed when the sales order is invoiced to the customer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="02614-124">Crie uma nota de encomenda a partir de um requisito de item.</span><span class="sxs-lookup"><span data-stu-id="02614-124">Create a purchase order from an item requirement.</span></span></td>
<td><span data-ttu-id="02614-125">Utilize este método para comprar itens quando criar um requisito de item a partir de um projeto.</span><span class="sxs-lookup"><span data-stu-id="02614-125">Use this method to purchase items when you create an item requirement from a project.</span></span></td>
<td><span data-ttu-id="02614-126">Os itens são consumidos quando o recibo de entrega do requisito de item é atualizado.</span><span class="sxs-lookup"><span data-stu-id="02614-126">Items are consumed when the item requirement packing slip is updated.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE] 
> <span data-ttu-id="02614-127">Quando atualiza a fatura do fornecedor ou o recibo de entrega, é-lhe solicitado que atualize o recibo de entrega no requisito de item.</span><span class="sxs-lookup"><span data-stu-id="02614-127">When you update the vendor invoice or packing slip, you're prompted to update the packing slip on the item requirement.</span></span>

<span data-ttu-id="02614-128">Para mais informações, consulte [Receber itens na nota de encomenda a partir do requisito do item](tasks/receive-items-purchase-order-item-requirement.md).</span><span class="sxs-lookup"><span data-stu-id="02614-128">For more information, see [Receive items on purchase order from item requirement](tasks/receive-items-purchase-order-item-requirement.md).</span></span>

