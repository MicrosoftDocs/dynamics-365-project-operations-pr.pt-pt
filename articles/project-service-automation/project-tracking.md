---
title: Progresso e consumo de custo de um projeto
description: Este tópico fornece informações sobre como monitorizar o progresso e o consumo de custo do projeto.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 0d742164-5469-421d-8917-63160a81f651
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8aa5814938129f30885d8161a7c86197ab013364
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754594"
---
# <a name="project-progress-and-cost-consumption"></a><span data-ttu-id="a6eba-103">Progresso e consumo de custo de um projeto</span><span class="sxs-lookup"><span data-stu-id="a6eba-103">Project progress and cost consumption</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="a6eba-104">A necessidade de monitorizar o progresso relativamente a uma agenda varia de acordo com o setor.</span><span class="sxs-lookup"><span data-stu-id="a6eba-104">The need to track progress against a schedule varies by industry.</span></span> <span data-ttu-id="a6eba-105">Alguns setores monitorizam a um nível granular, ao passo que outros setores monitoram a um nível superior.</span><span class="sxs-lookup"><span data-stu-id="a6eba-105">Some industries track at a granular level, whereas other industries track at a higher level.</span></span> <span data-ttu-id="a6eba-106">Este tópico mostra como agendar para satisfazer os requisitos da sua organização.</span><span class="sxs-lookup"><span data-stu-id="a6eba-106">This topic shows how to schedule in order to meet your organization's requirements.</span></span>

## <a name="effort-tracking-view"></a><span data-ttu-id="a6eba-107">Visto de controlo do esforço</span><span class="sxs-lookup"><span data-stu-id="a6eba-107">Effort tracking view</span></span>

<span data-ttu-id="a6eba-108">A vista **Controlo do Esforço** monitoriza o progresso das tarefas na agenda.</span><span class="sxs-lookup"><span data-stu-id="a6eba-108">The **Effort tracking** view tracks the progress of tasks in the schedule.</span></span> <span data-ttu-id="a6eba-109">Esta vista compara as horas de esforço reais que foram gastas numa tarefa com as horas de esforço planeadas para essa tarefa.</span><span class="sxs-lookup"><span data-stu-id="a6eba-109">It compares the actual effort hours that have been spent on a task to the planned effort hours for that task.</span></span> <span data-ttu-id="a6eba-110">O PSA utiliza as seguintes fórmulas para calcular as métricas de monitorização:</span><span class="sxs-lookup"><span data-stu-id="a6eba-110">PSA uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="a6eba-111">Percentagem do progresso = Esforço real gasto até à data ÷ Esforço planeado para a tarefa</span><span class="sxs-lookup"><span data-stu-id="a6eba-111">Progress percentage = Actual effort spent to date ÷ Planned effort for the task</span></span> 
- <span data-ttu-id="a6eba-112">Estimativa para conclusão (ETC) = Esforço planeado – Esforço real gasto até à data</span><span class="sxs-lookup"><span data-stu-id="a6eba-112">Estimate to complete (ETC) = Planned effort – Actual effort spent to date</span></span> 
- <span data-ttu-id="a6eba-113">Estimativa na conclusão (EAC) = Esforço restante + Esforço real gasto até à data</span><span class="sxs-lookup"><span data-stu-id="a6eba-113">Estimate at complete (EAC) = Remaining effort + Actual effort spent to date</span></span> 
- <span data-ttu-id="a6eba-114">Desvio do esforço projetado = Esforço planeado – EAC</span><span class="sxs-lookup"><span data-stu-id="a6eba-114">Projected effort variance = Planned effort – EAC</span></span>

<span data-ttu-id="a6eba-115">O PSA mostra uma projeção do desvio do esforço na tarefa.</span><span class="sxs-lookup"><span data-stu-id="a6eba-115">PSA shows a projection of the effort variance on the task.</span></span> <span data-ttu-id="a6eba-116">Se a EAC for superior ao esforço planeado, a tarefa é projetada para levar mais tempo do que o planeado originalmente.</span><span class="sxs-lookup"><span data-stu-id="a6eba-116">If the EAC is more than the planned effort, the task is projected to take more time than was originally planned.</span></span> <span data-ttu-id="a6eba-117">Consequentemente, está atrasada.</span><span class="sxs-lookup"><span data-stu-id="a6eba-117">Therefore, it's behind schedule.</span></span> <span data-ttu-id="a6eba-118">Se a EAC for inferior ao esforço planeado, a tarefa é projetada para levar menos tempo do que o planeado originalmente.</span><span class="sxs-lookup"><span data-stu-id="a6eba-118">If the EAC is less than the planned effort, the task is projected to take less time than was originally planned.</span></span> <span data-ttu-id="a6eba-119">Consequentemente, está adiantada.</span><span class="sxs-lookup"><span data-stu-id="a6eba-119">Therefore, it's ahead of schedule.</span></span>

## <a name="re-projecting-effort"></a><span data-ttu-id="a6eba-120">Reprojetar o esforço</span><span class="sxs-lookup"><span data-stu-id="a6eba-120">Re-projecting effort</span></span>

<span data-ttu-id="a6eba-121">É comum que um gestor de projeto reveja as estimativas originais de uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="a6eba-121">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="a6eba-122">As reprojeções do projeto são a perceção de estimativas de um gestor de projeto, dado o estado atual de um projeto.</span><span class="sxs-lookup"><span data-stu-id="a6eba-122">Project re-projections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="a6eba-123">No entanto, não recomendamos que os gestores de projeto alterem os valores da linha de base, porque a linha de base do projeto representa a fonte de verdade estabelecida para a agenda e a estimativa de custo do projeto acordadas por todos os intervenientes.</span><span class="sxs-lookup"><span data-stu-id="a6eba-123">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="a6eba-124">Existem duas formas de um gestor de projeto poder reprojetar o esforço nas tarefas:</span><span class="sxs-lookup"><span data-stu-id="a6eba-124">There are two ways that a project manager can re-project effort on tasks:</span></span>

- <span data-ttu-id="a6eba-125">Substitua a ETC predefinida por uma nova estimativa do esforço real restante na tarefa.</span><span class="sxs-lookup"><span data-stu-id="a6eba-125">Override the default ETC with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="a6eba-126">Substitua a percentagem de progresso predefinida por uma nova estimativa do verdadeiro progresso na tarefa.</span><span class="sxs-lookup"><span data-stu-id="a6eba-126">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="a6eba-127">Cada uma destas abordagens causa um recálculo da ETC, da EAC e da percentagem de progresso da tarefa e o desvio do esforço projetado numa tarefa.</span><span class="sxs-lookup"><span data-stu-id="a6eba-127">Each of these approaches cause a recalculation of the task's ETC, EAC, and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="a6eba-128">A EAC, a ETC e a percentagem de progresso das tarefas de resumo também são recalculadas e produzem uma nova projeção de variância do esforço.</span><span class="sxs-lookup"><span data-stu-id="a6eba-128">The EAC, ETC, and progress percentage on the summary tasks are also recalculated, and produce a new projection of effort variance.</span></span>

## <a name="re-projection-of-effort-on-summary-tasks"></a><span data-ttu-id="a6eba-129">Reprojeção do esforço em tarefas de resumo</span><span class="sxs-lookup"><span data-stu-id="a6eba-129">Re-projection of effort on summary tasks</span></span>

<span data-ttu-id="a6eba-130">O esforço em tarefas de resumo ou tarefas de contentor pode ser reprojetado.</span><span class="sxs-lookup"><span data-stu-id="a6eba-130">Effort on summary tasks or container tasks can be re-projected.</span></span> <span data-ttu-id="a6eba-131">Independentemente de o utilizador reprojetar utilizando o esforço restante ou a percentagem de progresso nas tarefas de resumo, o seguinte conjunto de cálculos começa:</span><span class="sxs-lookup"><span data-stu-id="a6eba-131">Regardless of whether the user re-projects by using the remaining effort or the progress percentage on the summary tasks, the following set of calculations begins:</span></span>

- <span data-ttu-id="a6eba-132">A EAC, a ETC e a percentagem de progresso na tarefa são calculadas.</span><span class="sxs-lookup"><span data-stu-id="a6eba-132">The EAC, ETC, and progress percentage on the task are calculated.</span></span>
- <span data-ttu-id="a6eba-133">A nova EAC é distribuída para as tarefas subordinadas na mesma proporção que a EAC original na tarefa.</span><span class="sxs-lookup"><span data-stu-id="a6eba-133">The new EAC is distributed down to the child tasks in the same proportion as the original EAC was on the task.</span></span>
- <span data-ttu-id="a6eba-134">A nova EAC em cada uma das tarefas individuais até às tarefas do nó de folha é calculada.</span><span class="sxs-lookup"><span data-stu-id="a6eba-134">The new EAC on each of the individualt tasks down to the leaf node tasks is calculated.</span></span> 
- <span data-ttu-id="a6eba-135">As tarefas subordinadas afetadas até ao nó de folha têm a ETC e a percentagem de progresso recalculada com base no valor da EAC.</span><span class="sxs-lookup"><span data-stu-id="a6eba-135">The affected child tasks down to the leaf nodes have their ETC and progress percentage recalculated based on the EAC value.</span></span> <span data-ttu-id="a6eba-136">Isto resulta numa nova projeção para o desvio do esforço da tarefa.</span><span class="sxs-lookup"><span data-stu-id="a6eba-136">This results in a new projection for the effort variance of the task.</span></span> 
- <span data-ttu-id="a6eba-137">As EACs das tarefas de resumo até ao nó raiz são recalculadas.</span><span class="sxs-lookup"><span data-stu-id="a6eba-137">The EACs of the summary tasks all the way to the root node are recalculated.</span></span>

### <a name="cost-tracking-view"></a><span data-ttu-id="a6eba-138">Vista Controlo dos custos</span><span class="sxs-lookup"><span data-stu-id="a6eba-138">Cost tracking view</span></span> 

<span data-ttu-id="a6eba-139">A vista **Controlo dos custos** compara o custo real gasto numa tarefa com o custo planeado numa tarefa.</span><span class="sxs-lookup"><span data-stu-id="a6eba-139">The **Cost tracking** view compares the actual cost that was spent on a task to the planned cost on a task.</span></span> 

> [!NOTE]
> <span data-ttu-id="a6eba-140">Esta vista mostra apenas os custos de mão de obra e não inclui os custos das estimativas de despesas.</span><span class="sxs-lookup"><span data-stu-id="a6eba-140">This view shows only labor costs and doesn’t include costs from the expense estimates.</span></span> 

<span data-ttu-id="a6eba-141">O PSA utiliza as seguintes fórmulas para calcular as métricas de monitorização:</span><span class="sxs-lookup"><span data-stu-id="a6eba-141">PSA uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="a6eba-142">Percentagem do custo consumido = Custo real gasto até ao momento cost ÷ Custo planeado para a tarefa</span><span class="sxs-lookup"><span data-stu-id="a6eba-142">Percentage of cost consumed = Actual cost spent to date ÷ Planned cost for the task</span></span>
- <span data-ttu-id="a6eba-143">Custo para conclusão (CTC) = Custo planeado – Custo real gasto até à data</span><span class="sxs-lookup"><span data-stu-id="a6eba-143">Cost to complete (CTC) = Planned cost – Actual cost spent to date</span></span>
- <span data-ttu-id="a6eba-144">EAC = CTC + Custo real gasto até à data</span><span class="sxs-lookup"><span data-stu-id="a6eba-144">EAC = CTC + Actual cost spent to date</span></span>
- <span data-ttu-id="a6eba-145">Desvio de custo projetado = Custo planeado – EAC</span><span class="sxs-lookup"><span data-stu-id="a6eba-145">Projected cost variance = Planned cost – EAC</span></span>

<span data-ttu-id="a6eba-146">Uma projeção do desvio de custo é mostrada na tarefa.</span><span class="sxs-lookup"><span data-stu-id="a6eba-146">A projection of the cost variance is shown on the task.</span></span> <span data-ttu-id="a6eba-147">Se a EAC for superior ao custo planeado, a tarefa é projetada para custar mais do que o planeado originalmente.</span><span class="sxs-lookup"><span data-stu-id="a6eba-147">If the EAC is more than the planned cost, the task is projected to cost more than was originally planned.</span></span> <span data-ttu-id="a6eba-148">Portanto, está acima do orçamento.</span><span class="sxs-lookup"><span data-stu-id="a6eba-148">Therefore, it's trending over budget.</span></span> <span data-ttu-id="a6eba-149">Se a EAC for inferior ao custo planeado, a tarefa é projetada para custar menos do que o planeado originalmente.</span><span class="sxs-lookup"><span data-stu-id="a6eba-149">If the EAC is less than the planned cost, the task is projected to cost less than was originally planned.</span></span> <span data-ttu-id="a6eba-150">Portanto, está abaixo do orçamento.</span><span class="sxs-lookup"><span data-stu-id="a6eba-150">Therefore, it's trending under budget.</span></span>

## <a name="project-managers-re-projection-of-cost"></a><span data-ttu-id="a6eba-151">Reprojeção de custos do gestor de projeto</span><span class="sxs-lookup"><span data-stu-id="a6eba-151">Project manager’s re-projection of cost</span></span>

<span data-ttu-id="a6eba-152">Quando o esforço é reprojetado, o CTC, a EAC, a percentagem do custo consumido e o desvio de custo projetado são todos recalculados na vista **Controlo dos custos**.</span><span class="sxs-lookup"><span data-stu-id="a6eba-152">When effort is re-projected, the CTC, EAC, percentage of cost consumed, and projected cost variance are all recalculated in the **Cost tracking** view.</span></span>

## <a name="project-status-summary"></a><span data-ttu-id="a6eba-153">Resumo do estado do projeto</span><span class="sxs-lookup"><span data-stu-id="a6eba-153">Project status summary</span></span>

<span data-ttu-id="a6eba-154">Os dados de monitorização nas vistas **Controlo do esforço** e **Controlo dos custos** mostram o progresso e o consumo de custo no nó raiz do projeto, nas tarefas de resumo e nos níveis de tarefas dos nós de folha.</span><span class="sxs-lookup"><span data-stu-id="a6eba-154">Tracking data in the **Effort tracking** and **Cost tracking** views shows the progress and cost consumption at the project root node, summary tasks, and leaf node tasks levels.</span></span> <span data-ttu-id="a6eba-155">A secção **Estado** na página **Entidade do Projeto** mostra um resumo do estado do nível do projeto.</span><span class="sxs-lookup"><span data-stu-id="a6eba-155">The **Status** section on the **Project entity** page shows a summary of project-level status.</span></span>

## <a name="status-summary-fields"></a><span data-ttu-id="a6eba-156">Campos Resumo do estado</span><span class="sxs-lookup"><span data-stu-id="a6eba-156">Status summary fields</span></span>

<span data-ttu-id="a6eba-157">O campo **Estado Geral do Projeto** é um campo editável que mostra o estado geral do projeto.</span><span class="sxs-lookup"><span data-stu-id="a6eba-157">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="a6eba-158">Utiliza a codificação de cores, tal como verde, amarela e vermelha, para indicar um risco de aumento.</span><span class="sxs-lookup"><span data-stu-id="a6eba-158">It uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> <span data-ttu-id="a6eba-159">O campo **Comentários** permite que o gestor de projeto introduza comentários específicos sobre o estado.</span><span class="sxs-lookup"><span data-stu-id="a6eba-159">The **Comments** field lets the project manager enter specific comments about the status.</span></span> <span data-ttu-id="a6eba-160">O campo **Estado atualizado em** não é editável e o valor é um carimbo de data/hora que indica quando o estado foi atualizado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="a6eba-160">The **Status updated on** field is not editable and the value is a timestamp that indicates when the status was last updated.</span></span>

<span data-ttu-id="a6eba-161">Os campos **Desempenho de Agendamento** e **Desempenho de Custos** são definidos a partir da data de monitorização.</span><span class="sxs-lookup"><span data-stu-id="a6eba-161">The **Schedule performance** and **Cost performance** fields are set from the tracking date.</span></span> <span data-ttu-id="a6eba-162">Quando os desvios da agenda e de custo do nó raiz na vista **Controlo do esforço** são positivos, é possível definir estes campos como **Adiantado**.</span><span class="sxs-lookup"><span data-stu-id="a6eba-162">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, you can set these fields to **Ahead**.</span></span> <span data-ttu-id="a6eba-163">Quando os desvios da agenda e de custo do nó raiz são negativos, é possível defini-los como **Atrasado**.</span><span class="sxs-lookup"><span data-stu-id="a6eba-163">When the schedule and cost variance for the root node are negative, you can set them to **Behind**.</span></span>
