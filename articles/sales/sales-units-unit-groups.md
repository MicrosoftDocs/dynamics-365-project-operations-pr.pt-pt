---
title: Unidades e grupos de unidades
description: Este tópico fornece informações sobre como criar unidades e grupos de unidades no Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 162366f4b7aa678b4e39d9745a657037bf36cbe0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277352"
---
# <a name="units-and-unit-groups"></a><span data-ttu-id="8e2eb-103">Unidades e grupos de unidades</span><span class="sxs-lookup"><span data-stu-id="8e2eb-103">Units and unit groups</span></span>

<span data-ttu-id="8e2eb-104">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="8e2eb-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8e2eb-105">As unidades são as quantidades ou medidas em que vende os produtos ou serviços.</span><span class="sxs-lookup"><span data-stu-id="8e2eb-105">Units are the quantities or measurements that you sell your products or services in.</span></span> <span data-ttu-id="8e2eb-106">Por exemplo, se vender artigos de jardinagem, poderá vender sementes em unidades de pacotes, caixas e paletes.</span><span class="sxs-lookup"><span data-stu-id="8e2eb-106">For example, if you sell gardening supplies, you might sell seeds in units of packets, boxes, and pallets.</span></span> <span data-ttu-id="8e2eb-107">Um grupo de unidades é uma coleção destas unidades diferentes.</span><span class="sxs-lookup"><span data-stu-id="8e2eb-107">A unit group is a collection of these different units.</span></span>

<span data-ttu-id="8e2eb-108">Para completar os passos deste tópico, certifique-se de que lhe foi atribuída a função de Administrador do Sistema ou de Gestor Sales Professional ou que tem permissões equivalentes.</span><span class="sxs-lookup"><span data-stu-id="8e2eb-108">To complete the steps in this topic, make sure that you have been assigned to the System Administrator or Sales Professional Manager role or have equivalent permissions.</span></span>

## <a name="create-a-unit-group"></a><span data-ttu-id="8e2eb-109">Criar um grupo de unidades</span><span class="sxs-lookup"><span data-stu-id="8e2eb-109">Create a unit group</span></span>

1. <span data-ttu-id="8e2eb-110">No mapa do site, selecione **Unidades**.</span><span class="sxs-lookup"><span data-stu-id="8e2eb-110">In the site map, select **Units**.</span></span>
2. <span data-ttu-id="8e2eb-111">Selecione **Novo**, e na caixa de diálogo **Criar grupo de unidades**, introduza o nome da unidade.</span><span class="sxs-lookup"><span data-stu-id="8e2eb-111">Select **New**, and in the **Create Unit Group** dialog box, enter the unit name.</span></span>
3. <span data-ttu-id="8e2eb-112">No campo **Unidade primária**, introduza a unidade de medida comum mais baixa na qual o produto será vendido.</span><span class="sxs-lookup"><span data-stu-id="8e2eb-112">In the **Primary unit** field, enter the lowest common unit of measure that the product will be sold in.</span></span> <span data-ttu-id="8e2eb-113">Por exemplo, pode introduzir "peça" ou "onça".</span><span class="sxs-lookup"><span data-stu-id="8e2eb-113">For example, you might enter "piece" or "ounce".</span></span>
4. <span data-ttu-id="8e2eb-114">Selecione **OK**.</span><span class="sxs-lookup"><span data-stu-id="8e2eb-114">Select **OK**.</span></span>

## <a name="add-units-to-a-unit-group"></a><span data-ttu-id="8e2eb-115">Adicionar unidades a um grupo de unidades</span><span class="sxs-lookup"><span data-stu-id="8e2eb-115">Add units to a unit group</span></span>

1. <span data-ttu-id="8e2eb-116">Abra um grupo de unidades e, no separador **Relacionado**, selecione **Unidades**.</span><span class="sxs-lookup"><span data-stu-id="8e2eb-116">Open a unit group, and on the **Related** tab, select **Units**.</span></span> <span data-ttu-id="8e2eb-117">Verá que a unidade primária já foi adicionada.</span><span class="sxs-lookup"><span data-stu-id="8e2eb-117">You will see that the primary unit is already added.</span></span>
2. <span data-ttu-id="8e2eb-118">Selecione **Adicionar Nova Unidade**, e na página **Criar rápido: Unidade**, no campo **Nome**, introduza o nome da unidade.</span><span class="sxs-lookup"><span data-stu-id="8e2eb-118">Select **Add New Unit**, and on the **Quick Create: Unit** page, in the **Name** field, enter the nanem of the unit.</span></span>
3. <span data-ttu-id="8e2eb-119">No campo **Quantidade**, introduza a quantidade que a unidade irá conter.</span><span class="sxs-lookup"><span data-stu-id="8e2eb-119">In the **QUantity** field, enter the quantity that the unit will contain.</span></span> <span data-ttu-id="8e2eb-120">Por exemplo, se uma caixa contém dois artigos, introduza "2".</span><span class="sxs-lookup"><span data-stu-id="8e2eb-120">For example, if a box contains two pieces, enter "2".</span></span> 
4. <span data-ttu-id="8e2eb-121">No campo **unidade base**, selecione uma unidade base para estabelecer a unidade de medição mais baixa para a unidade.</span><span class="sxs-lookup"><span data-stu-id="8e2eb-121">In the **Base unit** field, select a base unit to establish the lowest unit of measurement for the unit.</span></span> <span data-ttu-id="8e2eb-122">Por exemplo, pode selecionar "Peça".</span><span class="sxs-lookup"><span data-stu-id="8e2eb-122">For example, you might select "Piece".</span></span>
5. <span data-ttu-id="8e2eb-123">Selecione **Guardar**:</span><span class="sxs-lookup"><span data-stu-id="8e2eb-123">Select **Save**:</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]