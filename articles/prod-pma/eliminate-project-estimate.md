---
title: Eliminar uma estimativa do projeto
description: Este tópico fornece informações sobre a eliminação de uma estimativa do projeto após a sua conclusão.
author: Yowelle
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 000eabdac41f30a6e7dd37e34b8fd91d7c51f6c4
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270692"
---
# <a name="eliminate-a-project-estimate"></a><span data-ttu-id="d63e2-103">Eliminar uma estimativa do projeto</span><span class="sxs-lookup"><span data-stu-id="d63e2-103">Eliminate a project estimate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d63e2-104">As estimativas do projeto fornecem a vista financeira do trabalho estimado e agendado para um projeto.</span><span class="sxs-lookup"><span data-stu-id="d63e2-104">Project estimates provide the financial view for work that is estimated and scheduled for a project.</span></span> <span data-ttu-id="d63e2-105">Para trabalhar com estimativas para um projeto, é necessário anexar o projeto a um projeto de estimativa.</span><span class="sxs-lookup"><span data-stu-id="d63e2-105">To work with estimates for a project, you must attach the project to an estimate project.</span></span> <span data-ttu-id="d63e2-106">Um projeto de estimativa baseia-se sempre num projeto existente, no entanto, vários projetos podem referir-se a um único projeto de estimativa.</span><span class="sxs-lookup"><span data-stu-id="d63e2-106">An estimate project is always based on an existing project, however multiple projects can refer to a single estimate project.</span></span> <span data-ttu-id="d63e2-107">Apenas os projetos de preço fixo e de investimento podem ser associados a projetos de estimativa, devendo esses projetos pertencer ao mesmo grupo de projetos que o projeto de estimativa.</span><span class="sxs-lookup"><span data-stu-id="d63e2-107">Only fixed-price and investment projects can be attached to estimate projects, and those projects must belong to the same project group as the estimate project.</span></span>

<span data-ttu-id="d63e2-108">Para eliminar um projeto de estimativa, tem de estar completo.</span><span class="sxs-lookup"><span data-stu-id="d63e2-108">To eliminate an estimate project, it must be complete.</span></span> <span data-ttu-id="d63e2-109">Os seguintes passos explicam como eliminar uma estimativa.</span><span class="sxs-lookup"><span data-stu-id="d63e2-109">The following steps explain how to eliminate an estimate.</span></span>

1. <span data-ttu-id="d63e2-110">Vá para **Gestão de projetos e contabilística** > **Todos os Projetos** e abra o projeto.</span><span class="sxs-lookup"><span data-stu-id="d63e2-110">Go to **Project management and accounting** > **All Projects** and open the project.</span></span> 
2. <span data-ttu-id="d63e2-111">No separador **Gerir**, selecione **Estimativas** e, na página **Estimativa**, selecione **Eliminar**.</span><span class="sxs-lookup"><span data-stu-id="d63e2-111">On the **Manage** tab, select **Estimates**, and on the **Estimate** page select **Eliminate**.</span></span>
3. <span data-ttu-id="d63e2-112">Na página **Eliminar estimativa** no separador **Geral**, defina as seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="d63e2-112">On the **Eliminate estimate** page on the **General** tab, set the following options:</span></span>

   - <span data-ttu-id="d63e2-113">**Código do período**: selecione o código do período para escolher os projetos de estimativa adequados.</span><span class="sxs-lookup"><span data-stu-id="d63e2-113">**Period code**: Select the period code to choose the appropriate estimate projects.</span></span> 
   - <span data-ttu-id="d63e2-114">**Data de estimativa**: selecione a data de estimativa adequada para a eliminação.</span><span class="sxs-lookup"><span data-stu-id="d63e2-114">**Estimate date**: Select the appropriate estimate date for elimination.</span></span>
   - <span data-ttu-id="d63e2-115">**Eliminar com avisos WIP**: ative esta opção para fornecer notificação quando uma estimativa que está associada a um trabalho em curso (WIP) será eliminada.</span><span class="sxs-lookup"><span data-stu-id="d63e2-115">**Eliminate with WIP warnings**: Enable this option to provide notification when an estimate that is associated with a work in progress (WIP) will be eliminated.</span></span> <span data-ttu-id="d63e2-116">Quando esta opção não está ativada, a eliminação não pode continuar se existirem transações não estimadas.</span><span class="sxs-lookup"><span data-stu-id="d63e2-116">When this option is not enabled, elimination can’t continue if any non-estimated transactions exist.</span></span> 
   > [!NOTE]
   > <span data-ttu-id="d63e2-117">Esta opção só está disponível quando a eliminação é aplicada a um projeto de estimativa.</span><span class="sxs-lookup"><span data-stu-id="d63e2-117">This option is available only when elimination is applied to an estimate project.</span></span> <span data-ttu-id="d63e2-118">Não está disponível se estiver a utilizar publicações periódicas.</span><span class="sxs-lookup"><span data-stu-id="d63e2-118">It is not available if you are using periodic postings.</span></span> <span data-ttu-id="d63e2-119">Esta definição funciona com as definições no separador **Estimativa** na página **Parâmetros do projeto**, no grupo de campos **Permitir a eliminação quando existem transações não estimadas**.</span><span class="sxs-lookup"><span data-stu-id="d63e2-119">This setting works with the settings on the **Estimate** tab on the **Project parameters** page, in the **Allow elimination when non-estimated transactions exist** field group.</span></span>
   - <span data-ttu-id="d63e2-120">**Definir fase para Terminada**: ative esta opção para definir a fase do projeto de estimativa para **Terminado** depois de executar a eliminação.</span><span class="sxs-lookup"><span data-stu-id="d63e2-120">**Set stage to Finished**: Enable this option to set the estimate project’s stage to **Finished** after you run the elimination.</span></span>
   - <span data-ttu-id="d63e2-121">**Imprimir lista de estimativas**: selecione as informações a incluir quando a lista de estimativas for impressa.</span><span class="sxs-lookup"><span data-stu-id="d63e2-121">**Print estimate list**: Select the information to be included when the estimate list is printed.</span></span>
   - <span data-ttu-id="d63e2-122">**Mostrar Infolog**: ative esta opção para exibir o Infolog.</span><span class="sxs-lookup"><span data-stu-id="d63e2-122">**Show Infolog**: Enable this option to display the Infolog.</span></span>
   - <span data-ttu-id="d63e2-123">**Data da publicação**: escolha a data de publicação do livro razão da estimativa.</span><span class="sxs-lookup"><span data-stu-id="d63e2-123">**Posting date**: Choose the ledger posting date of the estimate.</span></span>

4.  <span data-ttu-id="d63e2-124">Selecione **OK**.</span><span class="sxs-lookup"><span data-stu-id="d63e2-124">Select **OK**.</span></span>
5. <span data-ttu-id="d63e2-125">Após o processo de eliminação estar concluído, o projeto de estimativa eliminado é apresentado com um valor negativo.</span><span class="sxs-lookup"><span data-stu-id="d63e2-125">After the elimination process is complete, the eliminated estimate project is displayed with a negative value.</span></span> 

<span data-ttu-id="d63e2-126">Se não pretendeu eliminar uma estimativa, pode selecionar a estimativa eliminada e selecionar **Reverter eliminação**.</span><span class="sxs-lookup"><span data-stu-id="d63e2-126">If you did not intend to eliminate an estimate, you can select the eliminated estimate and select **Reverse elimination**.</span></span>   


[!INCLUDE[footer-include](../includes/footer-banner.md)]