---
title: Modos de agendamento
description: Este tópico fornece informações sobre a modos de agendamento.
author: ruhercul
manager: AnnBe
ms.date: 05/04/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fe54944999617b248ff925148a78601dd4be7aca
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981449"
---
# <a name="scheduling-modes"></a><span data-ttu-id="c39db-103">Modos de agendamento</span><span class="sxs-lookup"><span data-stu-id="c39db-103">Scheduling modes</span></span>

<span data-ttu-id="c39db-104">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="c39db-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="c39db-105">Dynamics 365 Project Operations fornece a capacidade para as organizações definirem como gerem as alterações às variáveis-chave nas tarefas dentro da estrutura hierárquica de trabalho.</span><span class="sxs-lookup"><span data-stu-id="c39db-105">Dynamics 365 Project Operations provides the ability for organizations to define how they manage changes to key variables in tasks within the work breakdown structure.</span></span> <span data-ttu-id="c39db-106">Com base nas necessidades específicas da organização, os gestores de projeto podem fazer alterações ao modo de agendamento quando um projeto é criado.</span><span class="sxs-lookup"><span data-stu-id="c39db-106">Based on the specific needs of the organization, Project Managers can make changes to the scheduling mode when a project is created.</span></span>

<span data-ttu-id="c39db-107">Existem três modos de agendamento disponíveis no Project Operations:</span><span class="sxs-lookup"><span data-stu-id="c39db-107">There are three scheduling modes available in Project Operations:</span></span>

  - <span data-ttu-id="c39db-108">Duração fixa (este é o modo predefinido)</span><span class="sxs-lookup"><span data-stu-id="c39db-108">Fixed duration (this is the default mode)</span></span>
  - <span data-ttu-id="c39db-109">Trabalho fixo</span><span class="sxs-lookup"><span data-stu-id="c39db-109">Fixed work</span></span>
  - <span data-ttu-id="c39db-110">Unidades fixas</span><span class="sxs-lookup"><span data-stu-id="c39db-110">Fixed units</span></span>

<span data-ttu-id="c39db-111">Os valores impactados pela definição de um modo de programação específico são determinados pela seguinte fórmula:</span><span class="sxs-lookup"><span data-stu-id="c39db-111">The values impacted by the definition of a specific scheduling mode are determined by the following formula:</span></span>

  <span data-ttu-id="c39db-112">Esforço (*Trabalho*) = Duração x Unidades</span><span class="sxs-lookup"><span data-stu-id="c39db-112">Effort (*Work*) = Duration x Units</span></span>

<span data-ttu-id="c39db-113">Quando se define o modo de agendamento de um projeto, está a definir um destes valores, que depois não pode ser alterado.</span><span class="sxs-lookup"><span data-stu-id="c39db-113">When you define a project’s scheduling mode, you are setting one of these values, which then can't be changed.</span></span> <span data-ttu-id="c39db-114">Manter este valor como uma constante coloca uma prioridade nesse valor, o que notifica o sistema de não o alterar quando os outros dois valores mudam.</span><span class="sxs-lookup"><span data-stu-id="c39db-114">Holding this value as a constant places a priority on that value, which notifies the system not to change it when the other two values change.</span></span> <span data-ttu-id="c39db-115">A tabela seguinte fornece informações sobre os impactos da seleção de um modo específico.</span><span class="sxs-lookup"><span data-stu-id="c39db-115">The following table provides information about the impacts of selecting a specific mode.</span></span>

| <span data-ttu-id="c39db-116">**Nesta tarefa**</span><span class="sxs-lookup"><span data-stu-id="c39db-116">**In this task**</span></span>             | <span data-ttu-id="c39db-117">**Se rever as unidades**</span><span class="sxs-lookup"><span data-stu-id="c39db-117">**If you revise units**</span></span>   | <span data-ttu-id="c39db-118">**Se rever a duração**</span><span class="sxs-lookup"><span data-stu-id="c39db-118">**If you revise duration**</span></span> | <span data-ttu-id="c39db-119">**Se rever o esforço**</span><span class="sxs-lookup"><span data-stu-id="c39db-119">**If you revise effort**</span></span>  |
|----------------------|---------------------------|----------------------------|---------------------------|
| <span data-ttu-id="c39db-120">Tarefa de unidades fixas</span><span class="sxs-lookup"><span data-stu-id="c39db-120">Fixed units task</span></span>     | <span data-ttu-id="c39db-121">A duração é recalculada.</span><span class="sxs-lookup"><span data-stu-id="c39db-121">Duration is recalculated.</span></span> | <span data-ttu-id="c39db-122">O esforço é recalculado.</span><span class="sxs-lookup"><span data-stu-id="c39db-122">Effort is recalculated.</span></span>    | <span data-ttu-id="c39db-123">A duração é recalculada.</span><span class="sxs-lookup"><span data-stu-id="c39db-123">Duration is recalculated.</span></span> |
| <span data-ttu-id="c39db-124">Tarefa de esforço fixo</span><span class="sxs-lookup"><span data-stu-id="c39db-124">Fixed effort task</span></span>    | <span data-ttu-id="c39db-125">A duração é recalculada.</span><span class="sxs-lookup"><span data-stu-id="c39db-125">Duration is recalculated.</span></span> | <span data-ttu-id="c39db-126">As unidades são recalculadas.</span><span class="sxs-lookup"><span data-stu-id="c39db-126">Units are recalculated.</span></span>    | <span data-ttu-id="c39db-127">A duração é recalculada.</span><span class="sxs-lookup"><span data-stu-id="c39db-127">Duration is recalculated.</span></span> |
| <span data-ttu-id="c39db-128">Tarefa de duração fixa</span><span class="sxs-lookup"><span data-stu-id="c39db-128">Fixed duration task</span></span>  | <span data-ttu-id="c39db-129">O esforço é recalculado.</span><span class="sxs-lookup"><span data-stu-id="c39db-129">Effort is recalculated.</span></span>   | <span data-ttu-id="c39db-130">O esforço é recalculado.</span><span class="sxs-lookup"><span data-stu-id="c39db-130">Effort is recalculated.</span></span>    | <span data-ttu-id="c39db-131">As unidades são recalculadas.</span><span class="sxs-lookup"><span data-stu-id="c39db-131">Units are recalculated.</span></span>   |

<span data-ttu-id="c39db-132">Para obter mais informações sobre as implicações de um determinado modo, consulte [Alterar o tipo de tarefa para agendamento mais preciso](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span><span class="sxs-lookup"><span data-stu-id="c39db-132">For more information about the implications of a given mode, see [Change the task type for more accurate scheduling](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span></span> <span data-ttu-id="c39db-133">No tópico, o termo **Trabalho** é usado em vez de **Esforço**.</span><span class="sxs-lookup"><span data-stu-id="c39db-133">In the topic, the term **Work** is used instead of **Effort**.</span></span>

## <a name="change-the-organizations-scheduling-mode"></a><span data-ttu-id="c39db-134">Alterar o modo de agendamento da organização</span><span class="sxs-lookup"><span data-stu-id="c39db-134">Change the organization’s scheduling mode</span></span>

<span data-ttu-id="c39db-135">Complete os seguintes passos para definir o modo de agendamento de uma organização.</span><span class="sxs-lookup"><span data-stu-id="c39db-135">Complete the following steps to define the scheduling mode of an organization.</span></span>

1. <span data-ttu-id="c39db-136">Vá a **Definições** \> **Geral** \> **Parâmetros** e, em seguida, selecione o parâmetro do projeto.</span><span class="sxs-lookup"><span data-stu-id="c39db-136">Go to **Settings** \> **General** \> **Parameters**, and then select the project parameter.</span></span> 
2. <span data-ttu-id="c39db-137">Na página **Parâmetros do projeto**, selecione o modo de agendamento predefinido para a organização e, em seguida, defina a capacidade para o gestor do Projeto sobrepor a definição ao criar um novo projeto.</span><span class="sxs-lookup"><span data-stu-id="c39db-137">On the **Project Parameters** page, select the default scheduling mode for the organization, and then define ability for the Project manager to override the setting when creating a new project.</span></span>

## <a name="change-the-scheduling-mode-setting-on-a-project"></a><span data-ttu-id="c39db-138">Alterar a definição do modo de agendamento num projeto</span><span class="sxs-lookup"><span data-stu-id="c39db-138">Change the scheduling mode setting on a project</span></span>

<span data-ttu-id="c39db-139">Se uma organização permitir que o gestor do projeto substitua o modo de agendamento predefinido, o gestor do projeto pode fazer essa alteração quando criar um novo projeto.</span><span class="sxs-lookup"><span data-stu-id="c39db-139">If an organization allows the Project manager to override the default scheduling mode, the Project manager can make that change when they create a new project.</span></span> <span data-ttu-id="c39db-140">No entanto, depois de o projeto ter sido salvo, o modo de agendamento não pode ser alterado.</span><span class="sxs-lookup"><span data-stu-id="c39db-140">However, after the project has been saved, the scheduling mode can't be changed.</span></span>

## <a name="copied-projects"></a><span data-ttu-id="c39db-141">Projetos copiados</span><span class="sxs-lookup"><span data-stu-id="c39db-141">Copied projects</span></span>

<span data-ttu-id="c39db-142">Como um projeto é criado quando a ação do projeto copiar é tomada, o gestor do projeto não pode definir o modo de agendamento.</span><span class="sxs-lookup"><span data-stu-id="c39db-142">Because a project is created when the copy project action is taken, the Project manager can't set the scheduling mode.</span></span> <span data-ttu-id="c39db-143">O projeto de destino irá sempre estar predefinido no modo definido a nível organizacional.</span><span class="sxs-lookup"><span data-stu-id="c39db-143">The destination project will always default to the mode defined at the organizational level.</span></span>

## <a name="copied-tasks"></a><span data-ttu-id="c39db-144">Tarefas copiadas</span><span class="sxs-lookup"><span data-stu-id="c39db-144">Copied tasks</span></span>

<span data-ttu-id="c39db-145">Quando uma tarefa é copiada de um projeto para outro, a tarefa herda o modo de agendamento do projeto de destino.</span><span class="sxs-lookup"><span data-stu-id="c39db-145">When a task is copied from one project to another, the task inherits the scheduling mode of the destination project.</span></span>