---
title: Copiar um projeto
description: Este tópico fornece informações sobre copiar projetos no Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 02/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: af1942e81691d9e13fdcbbf68599c1a8a4004582
ms.sourcegitcommit: 24528bb9c0ef8898077cb3bc672daa211c0e73aa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 03/04/2021
ms.locfileid: "5479533"
---
# <a name="copy-a-project"></a><span data-ttu-id="d9203-103">Copiar um projeto</span><span class="sxs-lookup"><span data-stu-id="d9203-103">Copy a project</span></span>

<span data-ttu-id="d9203-104">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="d9203-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d9203-105">Com Dynamics 365 Project Operations, pode rapidamente construir novos projetos selecionando **Copiar projeto** no formulário **Projetos**.</span><span class="sxs-lookup"><span data-stu-id="d9203-105">With Dynamics 365 Project Operations, you can quickly build new projects by selecting **Copy Project** on the **Projects** form.</span></span> <span data-ttu-id="d9203-106">Para copiar um projeto, abra o projeto que pretende copiar e, em seguida, selecione **Copiar projeto**.</span><span class="sxs-lookup"><span data-stu-id="d9203-106">To copy a project, open the project you want to copy, and then select **Copy project**.</span></span> <span data-ttu-id="d9203-107">A ação copiará:</span><span class="sxs-lookup"><span data-stu-id="d9203-107">The action will copy:</span></span>

- <span data-ttu-id="d9203-108">Propriedades do projeto (A data de início estimada é copiada do projeto fonte)</span><span class="sxs-lookup"><span data-stu-id="d9203-108">Project properties (The estimated start date is copied from the source project)</span></span>
- <span data-ttu-id="d9203-109">A Estrutura Hierárquica do Trabalho</span><span class="sxs-lookup"><span data-stu-id="d9203-109">The Work breakdown structure</span></span>
- <span data-ttu-id="d9203-110">Membros da equipa do projeto</span><span class="sxs-lookup"><span data-stu-id="d9203-110">Project team members</span></span>
- <span data-ttu-id="d9203-111">Estimativas do projeto</span><span class="sxs-lookup"><span data-stu-id="d9203-111">Project estimates</span></span>
- <span data-ttu-id="d9203-112">Estimativas de despesa do projeto</span><span class="sxs-lookup"><span data-stu-id="d9203-112">Project expense estimates</span></span>

## <a name="project-properties"></a><span data-ttu-id="d9203-113">Propriedades do projeto</span><span class="sxs-lookup"><span data-stu-id="d9203-113">Project properties</span></span>

<span data-ttu-id="d9203-114">Quando o projeto é copiado, são copiados os valores nos seguintes campos:</span><span class="sxs-lookup"><span data-stu-id="d9203-114">When the project is copied, the values in the following fields are copied:</span></span>

- <span data-ttu-id="d9203-115">Nome</span><span class="sxs-lookup"><span data-stu-id="d9203-115">Name</span></span>
- <span data-ttu-id="d9203-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="d9203-116">Description</span></span>
- <span data-ttu-id="d9203-117">Cliente</span><span class="sxs-lookup"><span data-stu-id="d9203-117">Customer</span></span>
- <span data-ttu-id="d9203-118">Modelo de Calendário</span><span class="sxs-lookup"><span data-stu-id="d9203-118">Calendar Template</span></span>
- <span data-ttu-id="d9203-119">Moeda</span><span class="sxs-lookup"><span data-stu-id="d9203-119">Currency</span></span>
- <span data-ttu-id="d9203-120">Unidade de Contratação</span><span class="sxs-lookup"><span data-stu-id="d9203-120">Contracting Unit</span></span>
- <span data-ttu-id="d9203-121">Gestor de Projeto</span><span class="sxs-lookup"><span data-stu-id="d9203-121">Project Manager</span></span>
- <span data-ttu-id="d9203-122">Estado</span><span class="sxs-lookup"><span data-stu-id="d9203-122">Status</span></span>
- <span data-ttu-id="d9203-123">Estado Geral do Projeto</span><span class="sxs-lookup"><span data-stu-id="d9203-123">Overall Project Status</span></span>
- <span data-ttu-id="d9203-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="d9203-124">Comments</span></span>
- <span data-ttu-id="d9203-125">Estimativas</span><span class="sxs-lookup"><span data-stu-id="d9203-125">Estimates</span></span>
- <span data-ttu-id="d9203-126">Data de Início Estimada</span><span class="sxs-lookup"><span data-stu-id="d9203-126">Estimated Start Date</span></span>
- <span data-ttu-id="d9203-127">Data de Conclusão</span><span class="sxs-lookup"><span data-stu-id="d9203-127">Finish Date</span></span>
- <span data-ttu-id="d9203-128">Esforço (Horas)</span><span class="sxs-lookup"><span data-stu-id="d9203-128">Effort (Hours)</span></span>
- <span data-ttu-id="d9203-129">Custo Estimado da Mão-de-Obra</span><span class="sxs-lookup"><span data-stu-id="d9203-129">Estimated Labor Cost</span></span>
- <span data-ttu-id="d9203-130">Custo Estimado da Despesa</span><span class="sxs-lookup"><span data-stu-id="d9203-130">Estimated Expense Cost</span></span>

## <a name="work-breakdown-structure"></a><span data-ttu-id="d9203-131">Estrutura Hierárquica do Trabalho</span><span class="sxs-lookup"><span data-stu-id="d9203-131">Work breakdown structure</span></span>

<span data-ttu-id="d9203-132">Quando o projeto é copiado, é copiada toda a estrutura hierárquica do trabalho carregada pelos recursos.</span><span class="sxs-lookup"><span data-stu-id="d9203-132">When the project is copied, the entire resource-loaded work breakdown structure is copied.</span></span> <span data-ttu-id="d9203-133">Os recursos nomeados são substituídos por recursos genéricos.</span><span class="sxs-lookup"><span data-stu-id="d9203-133">Named resources are replaced with generic resources.</span></span> <span data-ttu-id="d9203-134">Se os recursos nomeados não tiverem as mesmas horas de trabalho que o recurso genérico, a agenda será recalculada e as durações das tarefas poderão mudar.</span><span class="sxs-lookup"><span data-stu-id="d9203-134">If the named resources don't have the same working hours as the generic resource, the schedule will be recalculated and task durations may change.</span></span>

## <a name="project-team-members"></a><span data-ttu-id="d9203-135">Membros da equipa do projeto</span><span class="sxs-lookup"><span data-stu-id="d9203-135">Project team members</span></span>

<span data-ttu-id="d9203-136">Quando uma equipa do projeto é copiada a partir do projeto de origem, são copiados os recursos genéricos.</span><span class="sxs-lookup"><span data-stu-id="d9203-136">When a project team is copied from the source project, the generic resources are copied.</span></span> <span data-ttu-id="d9203-137">As atribuições de recursos genéricos também são mantidas como no projeto de origem.</span><span class="sxs-lookup"><span data-stu-id="d9203-137">Generic resource assignments are also maintained as they were in the source project.</span></span> <span data-ttu-id="d9203-138">Os recursos nomeados serão convertidos para membros genéricos da equipa.</span><span class="sxs-lookup"><span data-stu-id="d9203-138">Named resources will be converted to generic team members.</span></span>

## <a name="estimates"></a><span data-ttu-id="d9203-139">Estimativas</span><span class="sxs-lookup"><span data-stu-id="d9203-139">Estimates</span></span>

<span data-ttu-id="d9203-140">Quando o projeto é copiado, são copiadas as linhas de estimativa de recursos e despesas a partir do projeto de origem.</span><span class="sxs-lookup"><span data-stu-id="d9203-140">When the project is copied, both resource and expense estimate lines are copied from the source project.</span></span> 

<span data-ttu-id="d9203-141">Para obter informações sobre como aceder programaticamente a Copiar Projeto, consulte [Programar modelos de projeto com Copiar Projeto](dev-copy-project.md).</span><span class="sxs-lookup"><span data-stu-id="d9203-141">For information on how to programmatically access Copy Project, see [Develop project templates with Copy Project](dev-copy-project.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
