---
title: Desativar listas de preços
description: Este tópico explica como desativar ou remover listas de preços não reutilizadas ou antigas.
author: rumant
manager: AnnBe
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3fa902e93815002be7d6915880cd7759dbbde5ef
ms.sourcegitcommit: 386921f44f1e9a8a828b140206d52945de07aee7
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 03/22/2021
ms.locfileid: "5701962"
---
# <a name="deactivate-price-lists"></a><span data-ttu-id="5c815-103">Desativar listas de preços</span><span class="sxs-lookup"><span data-stu-id="5c815-103">Deactivate price lists</span></span> 

<span data-ttu-id="5c815-104">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="5c815-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5c815-105">Para remover listas de preços antigos ou não reutilizados de Dynamics 365 Project Operations, há dois passos que deve realizar.</span><span class="sxs-lookup"><span data-stu-id="5c815-105">To remove old or unused price lists from Dynamics 365 Project Operations, there are two steps you must complete.</span></span> 

1. <span data-ttu-id="5c815-106">Remova ou elimine a lista de preços de páginas específicas.</span><span class="sxs-lookup"><span data-stu-id="5c815-106">Remove or delete the price list from specific pages.</span></span>
2. <span data-ttu-id="5c815-107">Desativar ou eliminar a lista de preços das listas de preços Ativos na página **Listas de preços**.</span><span class="sxs-lookup"><span data-stu-id="5c815-107">Deactivate or delete the price list from the Active price lists on the **Price Lists** page.</span></span>

>[!IMPORTANT]
> <span data-ttu-id="5c815-108">Tem de completar ambos os passos para remover totalmente uma lista de preços.</span><span class="sxs-lookup"><span data-stu-id="5c815-108">You must complete both steps to fully remove a price list.</span></span> <span data-ttu-id="5c815-109">Apenas a realização do passo 2, que consiste em eliminar ou desativar diretamente a lista de preços da vista das Listas de Preços Ativos, não é suficiente.</span><span class="sxs-lookup"><span data-stu-id="5c815-109">Only performing step 2, which is to directly delete or deactivate the price list from the Active Price Lists view, is not sufficient.</span></span> <span data-ttu-id="5c815-110">Deve também eliminar a associação desta lista de preços de todos os locais mencionados no passo 1.</span><span class="sxs-lookup"><span data-stu-id="5c815-110">You must also delete the association of this price list from all the places mentioned in step 1.</span></span>

## <a name="delete-the-price-list-from-specific-pages"></a><span data-ttu-id="5c815-111">Elimine a lista de preços de páginas específicas</span><span class="sxs-lookup"><span data-stu-id="5c815-111">Delete the price list from specific pages</span></span>
1. <span data-ttu-id="5c815-112">Para eliminar uma lista de preços do Project Operations, aceda às seguintes páginas:</span><span class="sxs-lookup"><span data-stu-id="5c815-112">To delete a price list from Project Operations, go to the following pages:</span></span>  

      - <span data-ttu-id="5c815-113">Página **Parâmetros de projeto** > separador **Listas de preços**</span><span class="sxs-lookup"><span data-stu-id="5c815-113">**Project parameters** page > **Price Lists** tab</span></span>
      - <span data-ttu-id="5c815-114">Página da **Unidade Organizacional** > grelha de **Listas de preços**</span><span class="sxs-lookup"><span data-stu-id="5c815-114">**Organizational Unit** page > **Price Lists** grid</span></span>
      - <span data-ttu-id="5c815-115">Página **Conta** > grelha **Listas de preço de projetos**</span><span class="sxs-lookup"><span data-stu-id="5c815-115">**Account** page > **Project Price Lists** grid</span></span>
      - <span data-ttu-id="5c815-116">Página de **Propostas de projeto** > grelha de **Listas de preços do projeto**: isto aplica-se a todas as propostas de projetos ativas.</span><span class="sxs-lookup"><span data-stu-id="5c815-116">**Project Quotes** page > **Project Price Lists** grid: This applies to all active project quotes.</span></span>
      - <span data-ttu-id="5c815-117">Página de **Contratos de projeto** > grelha de **Listas de preços do projeto**: isto aplica-se a todos os contratos de projetos ativos.</span><span class="sxs-lookup"><span data-stu-id="5c815-117">**Project Contracts** page > **Project Price Lists** grid: This applies to all active project contracts.</span></span>

 2. <span data-ttu-id="5c815-118">Para cada página, tem de selecionar a lista de preços que pretende eliminar e, em seguida, selecionar **Eliminar**.</span><span class="sxs-lookup"><span data-stu-id="5c815-118">For each page, you need to select the price list that you want to delete, and then select **Delete**.</span></span> 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a><span data-ttu-id="5c815-119">Eliminar ou desativar a lista de preços da página Listas de preços</span><span class="sxs-lookup"><span data-stu-id="5c815-119">Delete or deactivate the price list from the Price Lists page</span></span>
 
1. <span data-ttu-id="5c815-120">Para eliminar uma lista de preços das listas de preços ativas, vá a **Vendas** > **Clientes** > **Listas de preços**.</span><span class="sxs-lookup"><span data-stu-id="5c815-120">To delete a price list from the active price lists, go to **Sales** > **Customers** > **Price Lists**.</span></span> 
2. <span data-ttu-id="5c815-121">Selecione a lista de preços que pretende eliminar e, em seguida, selecione **Eliminar**.</span><span class="sxs-lookup"><span data-stu-id="5c815-121">Select the price list that you want to delete and then select **Delete**.</span></span> <span data-ttu-id="5c815-122">Se a lista de preços for referenciada em quaisquer transações existentes, não poderá eliminá-la.</span><span class="sxs-lookup"><span data-stu-id="5c815-122">If the price list is referenced on any existing transactions, you won't be able to delete it.</span></span> <span data-ttu-id="5c815-123">Se isso acontecer, pode desativar a lista de preços para que não apareça em nenhuma opinião.</span><span class="sxs-lookup"><span data-stu-id="5c815-123">If this happens, you can deactivate the price list so that it doesn't appear in any views.</span></span> 
3. <span data-ttu-id="5c815-124">Para desativar a lista de preços, selecione novamente a lista de preços e, em seguida, selecione **Desativar**.</span><span class="sxs-lookup"><span data-stu-id="5c815-124">To deactivate the price list, select the price list again, and then select **Deactivate**.</span></span>   
