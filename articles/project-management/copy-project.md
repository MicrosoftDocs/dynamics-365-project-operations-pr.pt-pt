---
title: Copiar um projeto
description: Este tópico fornece informações sobre copiar projetos no Dynamics 365 Project Operations.
author: ruhercul
ms.date: 05/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c3055ab5b8c07faa2bc9167956d283e2a66029dd
ms.sourcegitcommit: 173f2b1f4e063c440a5f78d76d456c62aadbd89e
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/24/2021
ms.locfileid: "6091268"
---
# <a name="copy-a-project"></a><span data-ttu-id="b17cb-103">Copiar um projeto</span><span class="sxs-lookup"><span data-stu-id="b17cb-103">Copy a project</span></span>

<span data-ttu-id="b17cb-104">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="b17cb-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b17cb-105">Com Dynamics 365 Project Operations, pode rapidamente construir novos projetos selecionando **Copiar projeto** no formulário **Projetos**.</span><span class="sxs-lookup"><span data-stu-id="b17cb-105">With Dynamics 365 Project Operations, you can quickly build new projects by selecting **Copy Project** on the **Projects** form.</span></span> <span data-ttu-id="b17cb-106">Para copiar um projeto, abra o projeto que pretende copiar e, em seguida, selecione **Copiar projeto**.</span><span class="sxs-lookup"><span data-stu-id="b17cb-106">To copy a project, open the project you want to copy, and then select **Copy project**.</span></span> <span data-ttu-id="b17cb-107">A ação copiará o seguinte:</span><span class="sxs-lookup"><span data-stu-id="b17cb-107">The action will copy the following:</span></span>

- <span data-ttu-id="b17cb-108">Propriedades do projeto</span><span class="sxs-lookup"><span data-stu-id="b17cb-108">Project properties</span></span> 
- <span data-ttu-id="b17cb-109">Estrutura Hierárquica do Trabalho</span><span class="sxs-lookup"><span data-stu-id="b17cb-109">Work breakdown structure</span></span>
- <span data-ttu-id="b17cb-110">Membros da equipa do projeto</span><span class="sxs-lookup"><span data-stu-id="b17cb-110">Project team members</span></span>
- <span data-ttu-id="b17cb-111">Estimativas do projeto</span><span class="sxs-lookup"><span data-stu-id="b17cb-111">Project estimates</span></span>
- <span data-ttu-id="b17cb-112">Estimativas de despesa do projeto</span><span class="sxs-lookup"><span data-stu-id="b17cb-112">Project expense estimates</span></span>
- <span data-ttu-id="b17cb-113">Estimativas de material do projeto</span><span class="sxs-lookup"><span data-stu-id="b17cb-113">Project material estimates</span></span>

## <a name="project-properties"></a><span data-ttu-id="b17cb-114">Propriedades do projeto</span><span class="sxs-lookup"><span data-stu-id="b17cb-114">Project properties</span></span>

<span data-ttu-id="b17cb-115">Quando o projeto é copiado, são copiados os valores nos seguintes campos:</span><span class="sxs-lookup"><span data-stu-id="b17cb-115">When the project is copied, the values in the following fields are copied:</span></span>

- <span data-ttu-id="b17cb-116">Nome</span><span class="sxs-lookup"><span data-stu-id="b17cb-116">Name</span></span>
- <span data-ttu-id="b17cb-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="b17cb-117">Description</span></span>
- <span data-ttu-id="b17cb-118">Cliente</span><span class="sxs-lookup"><span data-stu-id="b17cb-118">Customer</span></span>
- <span data-ttu-id="b17cb-119">Modelo de Calendário</span><span class="sxs-lookup"><span data-stu-id="b17cb-119">Calendar Template</span></span>
- <span data-ttu-id="b17cb-120">Moeda</span><span class="sxs-lookup"><span data-stu-id="b17cb-120">Currency</span></span>
- <span data-ttu-id="b17cb-121">Unidade de Contratação</span><span class="sxs-lookup"><span data-stu-id="b17cb-121">Contracting Unit</span></span>
- <span data-ttu-id="b17cb-122">Gestor de Projeto</span><span class="sxs-lookup"><span data-stu-id="b17cb-122">Project Manager</span></span>
- <span data-ttu-id="b17cb-123">Estado</span><span class="sxs-lookup"><span data-stu-id="b17cb-123">Status</span></span>
- <span data-ttu-id="b17cb-124">Estado Geral do Projeto</span><span class="sxs-lookup"><span data-stu-id="b17cb-124">Overall Project Status</span></span>
- <span data-ttu-id="b17cb-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="b17cb-125">Comments</span></span>
- <span data-ttu-id="b17cb-126">Estimativas</span><span class="sxs-lookup"><span data-stu-id="b17cb-126">Estimates</span></span>
- <span data-ttu-id="b17cb-127">Data de Início Estimada: Esta é a data em que o projeto é criado a partir da cópia.</span><span class="sxs-lookup"><span data-stu-id="b17cb-127">Estimated Start Date: This is the date that the project is created from the copy.</span></span>
- <span data-ttu-id="b17cb-128">Data de Conclusão Estimada: Esta data é ajustada com base na data de início do novo projeto que foi feito a partir da cópia.</span><span class="sxs-lookup"><span data-stu-id="b17cb-128">Estimated Finish Date: This date is adjusted based on the start date of the new project that was made from the copy.</span></span>
- <span data-ttu-id="b17cb-129">Esforço (Horas)</span><span class="sxs-lookup"><span data-stu-id="b17cb-129">Effort (Hours)</span></span>
- <span data-ttu-id="b17cb-130">Custo Estimado da Mão-de-Obra</span><span class="sxs-lookup"><span data-stu-id="b17cb-130">Estimated Labor Cost</span></span>
- <span data-ttu-id="b17cb-131">Custo Estimado da Despesa</span><span class="sxs-lookup"><span data-stu-id="b17cb-131">Estimated Expense Cost</span></span>
- <span data-ttu-id="b17cb-132">Custo Estimado do Material</span><span class="sxs-lookup"><span data-stu-id="b17cb-132">Estimated Material Cost</span></span>

> [!NOTE]
> <span data-ttu-id="b17cb-133">Copiar projeto é uma operação de execução prolongada.</span><span class="sxs-lookup"><span data-stu-id="b17cb-133">Copy project is a long running operation.</span></span> <span data-ttu-id="b17cb-134">Os registos do projeto, os seus atributos relevantes e muitas entidades relacionadas também são copiados.</span><span class="sxs-lookup"><span data-stu-id="b17cb-134">Project records, their relevant attributes, and many related entities are also copied.</span></span> <span data-ttu-id="b17cb-135">Devido à natureza de execução prolongada da operação, após o início da cópia, a página de destino do projecto está bloqueada para edição até que a operação da cópia esteja concluída.</span><span class="sxs-lookup"><span data-stu-id="b17cb-135">Because of the long running nature of the operation, after the copy starts, the target project page is locked for editing until the copy operation is complete.</span></span>

## <a name="work-breakdown-structure"></a><span data-ttu-id="b17cb-136">Estrutura Hierárquica do Trabalho</span><span class="sxs-lookup"><span data-stu-id="b17cb-136">Work breakdown structure</span></span>

<span data-ttu-id="b17cb-137">Quando o projeto é copiado, é copiada toda a estrutura hierárquica do trabalho carregada pelos recursos.</span><span class="sxs-lookup"><span data-stu-id="b17cb-137">When the project is copied, the entire resource-loaded work breakdown structure is copied.</span></span> <span data-ttu-id="b17cb-138">Os recursos nomeados são substituídos por recursos genéricos.</span><span class="sxs-lookup"><span data-stu-id="b17cb-138">Named resources are replaced with generic resources.</span></span> <span data-ttu-id="b17cb-139">Se os recursos nomeados não tiverem as mesmas horas de trabalho que o recurso genérico, a agenda será recalculada e as durações das tarefas poderão mudar.</span><span class="sxs-lookup"><span data-stu-id="b17cb-139">If the named resources don't have the same working hours as the generic resource, the schedule will be recalculated and task durations may change.</span></span>

## <a name="project-team-members"></a><span data-ttu-id="b17cb-140">Membros da equipa do projeto</span><span class="sxs-lookup"><span data-stu-id="b17cb-140">Project team members</span></span>

<span data-ttu-id="b17cb-141">Quando uma equipa do projeto é copiada a partir do projeto de origem, são copiados os recursos genéricos.</span><span class="sxs-lookup"><span data-stu-id="b17cb-141">When a project team is copied from the source project, the generic resources are copied.</span></span> <span data-ttu-id="b17cb-142">As atribuições de recursos genéricos também são mantidas como no projeto de origem.</span><span class="sxs-lookup"><span data-stu-id="b17cb-142">Generic resource assignments are also maintained as they were in the source project.</span></span> <span data-ttu-id="b17cb-143">Os recursos nomeados serão convertidos para membros genéricos da equipa.</span><span class="sxs-lookup"><span data-stu-id="b17cb-143">Named resources will be converted to generic team members.</span></span>

## <a name="estimates"></a><span data-ttu-id="b17cb-144">Estimativas</span><span class="sxs-lookup"><span data-stu-id="b17cb-144">Estimates</span></span>

<span data-ttu-id="b17cb-145">Quando o projeto é copiado, as linhas de estimativa de recursos, despesas e materiais são copiadas do projeto de origem.</span><span class="sxs-lookup"><span data-stu-id="b17cb-145">When the project is copied, resource, expense and material estimate lines are copied from the source project.</span></span> 

<span data-ttu-id="b17cb-146">Para obter informações sobre como aceder programaticamente a Copiar Projeto, consulte [Programar modelos de projeto com Copiar Projeto](dev-copy-project.md).</span><span class="sxs-lookup"><span data-stu-id="b17cb-146">For information on how to programmatically access Copy Project, see [Develop project templates with Copy Project](dev-copy-project.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
