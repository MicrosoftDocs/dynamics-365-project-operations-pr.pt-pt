---
title: Fases do projeto
description: Este tópico fornece informações sobre as fases do projeto.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 983c25a0-ed21-4151-a109-b385a88285fa
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 70aa057e127df7ba925e84f5d056a06a4cc8833e
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754510"
---
# <a name="project-stages"></a><span data-ttu-id="026a9-103">Fases do projeto</span><span class="sxs-lookup"><span data-stu-id="026a9-103">Project stages</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="026a9-104">As fases de um projeto são atualizadas para refletir o estado do projeto à medida que o mesmo progride.</span><span class="sxs-lookup"><span data-stu-id="026a9-104">Project stages are updated to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="026a9-105">O fluxo do processo de negócio predefinido atualiza automaticamente algumas fases do projeto, enquanto outras são atualizadas manualmente pelo gestor de projeto.</span><span class="sxs-lookup"><span data-stu-id="026a9-105">The default business process flow automatically updates some stages of the project while others are manually updated by the project manager.</span></span> 

<span data-ttu-id="026a9-106">As fases seguintes são definidas no BPF predefinido:</span><span class="sxs-lookup"><span data-stu-id="026a9-106">The following stages are defined in the default BPF:</span></span>

- <span data-ttu-id="026a9-107">Novo</span><span class="sxs-lookup"><span data-stu-id="026a9-107">New</span></span>
- <span data-ttu-id="026a9-108">Proposta</span><span class="sxs-lookup"><span data-stu-id="026a9-108">Quote</span></span>
- <span data-ttu-id="026a9-109">Planear</span><span class="sxs-lookup"><span data-stu-id="026a9-109">Plan</span></span>
- <span data-ttu-id="026a9-110">Entregar</span><span class="sxs-lookup"><span data-stu-id="026a9-110">Deliver</span></span>
- <span data-ttu-id="026a9-111">Concluído</span><span class="sxs-lookup"><span data-stu-id="026a9-111">Complete</span></span>
- <span data-ttu-id="026a9-112">Fechar</span><span class="sxs-lookup"><span data-stu-id="026a9-112">Close</span></span> 

## <a name="new"></a><span data-ttu-id="026a9-113">Novo</span><span class="sxs-lookup"><span data-stu-id="026a9-113">New</span></span>

<span data-ttu-id="026a9-114">Quando cria um projeto, a fase do projeto é definida como **Novo**.</span><span class="sxs-lookup"><span data-stu-id="026a9-114">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="026a9-115">Se o projeto tiver sido criado a partir de um modelo, este poderá ter dados de agendas, estimativas e da equipa.</span><span class="sxs-lookup"><span data-stu-id="026a9-115">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="026a9-116">Caso contrário, é apenas um contorno do projeto e os componentes restantes têm de ser introduzidos.</span><span class="sxs-lookup"><span data-stu-id="026a9-116">Otherwise, it's just an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="026a9-117">Proposta</span><span class="sxs-lookup"><span data-stu-id="026a9-117">Quote</span></span>

<span data-ttu-id="026a9-118">Quando associa um projeto a uma proposta ou quando cria um projeto a partir de uma proposta, a fase de projeto é definida como **Proposta** e as datas de início e de fim estimadas também são atualizadas.</span><span class="sxs-lookup"><span data-stu-id="026a9-118">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="026a9-119">Quando o projeto está na fase **Proposta**, o separador **Vendas** na página **Entidade do Projeto** mostra os detalhes da proposta.</span><span class="sxs-lookup"><span data-stu-id="026a9-119">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="026a9-120">Planear</span><span class="sxs-lookup"><span data-stu-id="026a9-120">Plan</span></span>

<span data-ttu-id="026a9-121">Quando ganha uma proposta associada a um projeto e quando o projeto é movido para a fase **Contrato**, a fase do projeto é atualizada para **Plano**.</span><span class="sxs-lookup"><span data-stu-id="026a9-121">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="026a9-122">Quando o projeto está na fase **Plano**, a página **Entidade do Projeto** mostra os detalhes do contrato.</span><span class="sxs-lookup"><span data-stu-id="026a9-122">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="026a9-123">Entregar</span><span class="sxs-lookup"><span data-stu-id="026a9-123">Deliver</span></span>

<span data-ttu-id="026a9-124">Quando o plano do projeto estiver concluído, e estiver pronto para iniciar o projeto, o gestor de projeto deverá atualizar a fase do projeto **Entregar** para mostrar que o projeto foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="026a9-124">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="026a9-125">Concluído</span><span class="sxs-lookup"><span data-stu-id="026a9-125">Complete</span></span> 

<span data-ttu-id="026a9-126">Quando o trabalho do projeto estiver concluído, o gestor de projeto poderá atualizar a fase para **Concluído**.</span><span class="sxs-lookup"><span data-stu-id="026a9-126">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="026a9-127">Ao atualizar a fase do projeto para **Concluído**, o gestor de projeto indica que o trabalho está 100% concluído, mas que o projeto está a ser mantido aberto para que qualquer entrada de tempo ou despesa pendente possa ser registada.</span><span class="sxs-lookup"><span data-stu-id="026a9-127">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="026a9-128">Fechar</span><span class="sxs-lookup"><span data-stu-id="026a9-128">Close</span></span>

<span data-ttu-id="026a9-129">Quando todas as transações são registadas para o projeto, o gestor de projeto pode atualizar a fase para **Fechar**.</span><span class="sxs-lookup"><span data-stu-id="026a9-129">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="026a9-130">Nesta altura, não é possível registar nenhuma transação e o projeto está definido como só de leitura.</span><span class="sxs-lookup"><span data-stu-id="026a9-130">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>
