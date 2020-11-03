---
title: Fases do projeto
description: Este tópico fornece informações sobre as fases do projeto que estão disponíveis em Operações de Projeto Microsoft Dynamics.
author: ruhercul
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
ms.openlocfilehash: 554ad63bc44cbe5a1fe91eb47fedbb74bbedd4b6
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082531"
---
# <a name="project-stages"></a><span data-ttu-id="ce6a1-103">Fases do projeto</span><span class="sxs-lookup"><span data-stu-id="ce6a1-103">Project stages</span></span>

<span data-ttu-id="ce6a1-104">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="ce6a1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ce6a1-105">As fases de um projeto são concebidas para refletir o estado do projeto à medida que o mesmo progride.</span><span class="sxs-lookup"><span data-stu-id="ce6a1-105">Project stages are designed to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="ce6a1-106">As personalizações podem ser usadas para atualizar automaticamente as fases com fluxos do processo de negócio, Power Automate ou extensões de plug-in.</span><span class="sxs-lookup"><span data-stu-id="ce6a1-106">Customizations can be used to automatically update the stages with business process flows, Power Automate, or plug-in extensions.</span></span>

<span data-ttu-id="ce6a1-107">As fases seguintes são definidas no fluxo do processo de negócio predefinido:</span><span class="sxs-lookup"><span data-stu-id="ce6a1-107">The following stages are defined in the default business process flow:</span></span>

- <span data-ttu-id="ce6a1-108">Nova</span><span class="sxs-lookup"><span data-stu-id="ce6a1-108">New</span></span>
- <span data-ttu-id="ce6a1-109">Proposta</span><span class="sxs-lookup"><span data-stu-id="ce6a1-109">Quote</span></span>
- <span data-ttu-id="ce6a1-110">Plano</span><span class="sxs-lookup"><span data-stu-id="ce6a1-110">Plan</span></span>
- <span data-ttu-id="ce6a1-111">Entregar</span><span class="sxs-lookup"><span data-stu-id="ce6a1-111">Deliver</span></span>
- <span data-ttu-id="ce6a1-112">Concluir</span><span class="sxs-lookup"><span data-stu-id="ce6a1-112">Complete</span></span>
- <span data-ttu-id="ce6a1-113">Fechar</span><span class="sxs-lookup"><span data-stu-id="ce6a1-113">Close</span></span> 

## <a name="new"></a><span data-ttu-id="ce6a1-114">Nova</span><span class="sxs-lookup"><span data-stu-id="ce6a1-114">New</span></span>

<span data-ttu-id="ce6a1-115">Quando cria um projeto, a fase do projeto é definida como **Novo**.</span><span class="sxs-lookup"><span data-stu-id="ce6a1-115">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="ce6a1-116">Se o projeto tiver sido criado a partir de um modelo, este poderá ter dados de agendas, estimativas e da equipa.</span><span class="sxs-lookup"><span data-stu-id="ce6a1-116">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="ce6a1-117">Caso contrário, é um contorno do projeto e os componentes restantes têm de ser introduzidos.</span><span class="sxs-lookup"><span data-stu-id="ce6a1-117">Otherwise, it's an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="ce6a1-118">Proposta</span><span class="sxs-lookup"><span data-stu-id="ce6a1-118">Quote</span></span>

<span data-ttu-id="ce6a1-119">Quando associa um projeto a uma proposta ou quando cria um projeto a partir de uma proposta, a fase de projeto é definida como **Proposta** e as datas de início e de fim estimadas também são atualizadas.</span><span class="sxs-lookup"><span data-stu-id="ce6a1-119">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote** , and the estimated start and end dates are updated.</span></span> <span data-ttu-id="ce6a1-120">Quando o projeto está na fase **Proposta** , o separador **Vendas** na página **Entidade do Projeto** mostra os detalhes da proposta.</span><span class="sxs-lookup"><span data-stu-id="ce6a1-120">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="ce6a1-121">Planear</span><span class="sxs-lookup"><span data-stu-id="ce6a1-121">Plan</span></span>

<span data-ttu-id="ce6a1-122">Quando ganha uma proposta associada a um projeto e quando o projeto é movido para a fase **Contrato** , a fase do projeto é atualizada para **Plano**.</span><span class="sxs-lookup"><span data-stu-id="ce6a1-122">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="ce6a1-123">Quando o projeto está na fase **Plano** , a página **Entidade do Projeto** mostra os detalhes do contrato.</span><span class="sxs-lookup"><span data-stu-id="ce6a1-123">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="ce6a1-124">Entregar</span><span class="sxs-lookup"><span data-stu-id="ce6a1-124">Deliver</span></span>

<span data-ttu-id="ce6a1-125">Quando o plano do projeto estiver concluído, e estiver pronto para iniciar o projeto, o gestor de projeto deverá atualizar a fase do projeto **Entregar** para mostrar que o projeto foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="ce6a1-125">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="ce6a1-126">Concluído</span><span class="sxs-lookup"><span data-stu-id="ce6a1-126">Complete</span></span> 

<span data-ttu-id="ce6a1-127">Quando o trabalho do projeto estiver concluído, o gestor de projeto poderá atualizar a fase para **Concluído**.</span><span class="sxs-lookup"><span data-stu-id="ce6a1-127">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="ce6a1-128">Ao atualizar a fase do projeto para **Concluído** , o gestor de projeto indica que o trabalho está 100% concluído, mas que o projeto está a ser mantido aberto para que qualquer entrada de tempo ou despesa pendente possa ser registada.</span><span class="sxs-lookup"><span data-stu-id="ce6a1-128">By updating the project stage to **Complete** , the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="ce6a1-129">Fechar</span><span class="sxs-lookup"><span data-stu-id="ce6a1-129">Close</span></span>

<span data-ttu-id="ce6a1-130">Quando todas as transações são registadas para o projeto, o gestor de projeto pode atualizar a fase para **Fechar**.</span><span class="sxs-lookup"><span data-stu-id="ce6a1-130">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="ce6a1-131">Nesta altura, não é possível registar nenhuma transação e o projeto está definido como só de leitura.</span><span class="sxs-lookup"><span data-stu-id="ce6a1-131">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>

