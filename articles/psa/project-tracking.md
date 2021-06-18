---
title: Progresso e consumo de custo do projeto
description: Este tópico fornece informações sobre a monitorização do progresso e o consumo de custo do projeto.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 08/21/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 4fe6adf1a16c1eafc5e37dbd8878dda44cbca230
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009045"
---
# <a name="project-progress-and-cost-consumption"></a><span data-ttu-id="2dbe8-103">Progresso e consumo de custo do projeto</span><span class="sxs-lookup"><span data-stu-id="2dbe8-103">Project progress and cost consumption</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="2dbe8-104">A necessidade de monitorizar o progresso relativamente a uma agenda varia de acordo com o setor.</span><span class="sxs-lookup"><span data-stu-id="2dbe8-104">The need to track progress against a schedule varies by industry.</span></span> <span data-ttu-id="2dbe8-105">Alguns setores monitorizam a um nível granular, ao passo que outros setores monitoram a um nível superior.</span><span class="sxs-lookup"><span data-stu-id="2dbe8-105">Some industries track at a granular level, whereas other industries track at a higher level.</span></span> <span data-ttu-id="2dbe8-106">Este tópico mostra como agendar para satisfazer os requisitos da sua organização.</span><span class="sxs-lookup"><span data-stu-id="2dbe8-106">This topic shows how to schedule in order to meet your organization's requirements.</span></span>

## <a name="effort-tracking-view"></a><span data-ttu-id="2dbe8-107">Visto de controlo do esforço</span><span class="sxs-lookup"><span data-stu-id="2dbe8-107">Effort tracking view</span></span>

<span data-ttu-id="2dbe8-108">A vista **Controlo do Esforço** monitoriza o progresso das tarefas na agenda.</span><span class="sxs-lookup"><span data-stu-id="2dbe8-108">The **Effort tracking** view tracks the progress of tasks in the schedule.</span></span> <span data-ttu-id="2dbe8-109">Esta vista compara as horas de esforço reais de uma tarefa com as horas de esforço planeadas para essa tarefa.</span><span class="sxs-lookup"><span data-stu-id="2dbe8-109">It compares the actual effort hours spent on a task to the task's planned effort hours.</span></span> <span data-ttu-id="2dbe8-110">O Project Service Automation utiliza as seguintes fórmulas para calcular as métricas de monitorização:</span><span class="sxs-lookup"><span data-stu-id="2dbe8-110">Project Service Automation uses the following formulas to calculate the tracking metrics:</span></span>

<span data-ttu-id="2dbe8-111">Inicialmente na criação de tarefas: O custo previsto será definido para o custo estimado ao completar.</span><span class="sxs-lookup"><span data-stu-id="2dbe8-111">Initially on the task creation: Planned cost will be set to the Estimated cost at complete.</span></span> <span data-ttu-id="2dbe8-112">Uma vez que os Atuais são registados na tarefa, o seguinte será o cálculo na vista de Monitorização para Esforço</span><span class="sxs-lookup"><span data-stu-id="2dbe8-112">Once Actuals are recorded on the task, the following will be calculation on the Tracking view for Effort</span></span>

- <span data-ttu-id="2dbe8-113">Percentagem de progresso = Esforço real gasto até à data = Estimativa na conclusão (EAC)</span><span class="sxs-lookup"><span data-stu-id="2dbe8-113">Progress percentage = Actual effort spent to date ÷ Estimate at complete (EAC)</span></span> 
- <span data-ttu-id="2dbe8-114">Estimativa para conclusão (ETC) = Estimativa na conclusão (EAC) – Esforço real gasto até à data</span><span class="sxs-lookup"><span data-stu-id="2dbe8-114">Estimate to complete (ETC) = Estimate at complete (EAC)  – Actual effort spent to date</span></span> 
- <span data-ttu-id="2dbe8-115">EAC = Esforço restante + Esforço real gasto até à data</span><span class="sxs-lookup"><span data-stu-id="2dbe8-115">EAC = Remaining effort + Actual effort spent to date</span></span> 
- <span data-ttu-id="2dbe8-116">Desvio do esforço projetado = Esforço planeado – EAC</span><span class="sxs-lookup"><span data-stu-id="2dbe8-116">Projected effort variance = Planned effort – EAC</span></span>

<span data-ttu-id="2dbe8-117">O Project Service Automation mostra uma projeção do desvio do esforço na tarefa.</span><span class="sxs-lookup"><span data-stu-id="2dbe8-117">Project Service Automation shows a projection of the effort variance on the task.</span></span> <span data-ttu-id="2dbe8-118">Se a EAC for superior ao esforço planeado, a tarefa é projetada para levar mais tempo do que o planeado originalmente.</span><span class="sxs-lookup"><span data-stu-id="2dbe8-118">If the EAC is more than the planned effort, the task is projected to take more time than was originally planned.</span></span> <span data-ttu-id="2dbe8-119">Consequentemente, está atrasada.</span><span class="sxs-lookup"><span data-stu-id="2dbe8-119">Therefore, it's behind schedule.</span></span> <span data-ttu-id="2dbe8-120">Se a EAC for inferior ao esforço planeado, a tarefa é projetada para levar menos tempo do que o planeado originalmente.</span><span class="sxs-lookup"><span data-stu-id="2dbe8-120">If the EAC is less than the planned effort, the task is projected to take less time than was originally planned.</span></span> <span data-ttu-id="2dbe8-121">Consequentemente, está adiantada.</span><span class="sxs-lookup"><span data-stu-id="2dbe8-121">Therefore, it's ahead of schedule.</span></span>

## <a name="reprojecting-effort"></a><span data-ttu-id="2dbe8-122">Reprojetar o esforço</span><span class="sxs-lookup"><span data-stu-id="2dbe8-122">Reprojecting effort</span></span>

<span data-ttu-id="2dbe8-123">É comum que um gestor de projeto reveja as estimativas originais de uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="2dbe8-123">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="2dbe8-124">As reprojeções do projeto são a perceção de estimativas de um gestor de projeto, dado o estado atual de um projeto.</span><span class="sxs-lookup"><span data-stu-id="2dbe8-124">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="2dbe8-125">No entanto, não recomendamos que os gestores de projeto alterem os valores da linha de base, porque a linha de base do projeto representa a fonte de verdade estabelecida para a agenda e a estimativa de custo do projeto acordadas por todos os intervenientes.</span><span class="sxs-lookup"><span data-stu-id="2dbe8-125">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="2dbe8-126">Existem duas formas de um gestor de projeto poder reprojetar o esforço nas tarefas:</span><span class="sxs-lookup"><span data-stu-id="2dbe8-126">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="2dbe8-127">Substitua a ETC predefinida por uma nova estimativa do esforço real restante na tarefa.</span><span class="sxs-lookup"><span data-stu-id="2dbe8-127">Override the default ETC with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="2dbe8-128">Substitua a percentagem de progresso predefinida por uma nova estimativa do verdadeiro progresso na tarefa.</span><span class="sxs-lookup"><span data-stu-id="2dbe8-128">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="2dbe8-129">Cada uma destas abordagens causa um recálculo da ETC, da EAC e da percentagem de progresso da tarefa e o desvio do esforço projetado numa tarefa.</span><span class="sxs-lookup"><span data-stu-id="2dbe8-129">Each of these approaches cause a recalculation of the task's ETC, EAC, and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="2dbe8-130">A EAC, a ETC e a percentagem de progresso das tarefas de resumo também são recalculadas e produzem uma nova projeção de variância do esforço.</span><span class="sxs-lookup"><span data-stu-id="2dbe8-130">The EAC, ETC, and progress percentage on the summary tasks are also recalculated, and produce a new projection of effort variance.</span></span>

## <a name="reprojection-of-effort-on-summary-tasks"></a><span data-ttu-id="2dbe8-131">Reprojeção do esforço em tarefas de resumo</span><span class="sxs-lookup"><span data-stu-id="2dbe8-131">Reprojection of effort on summary tasks</span></span>

<span data-ttu-id="2dbe8-132">O esforço em tarefas de resumo ou tarefas de contentor pode ser reprojetado.</span><span class="sxs-lookup"><span data-stu-id="2dbe8-132">Effort on summary tasks or container tasks can be reprojected.</span></span> <span data-ttu-id="2dbe8-133">Independentemente de o utilizador reprojetar utilizando o esforço restante ou a percentagem de progresso nas tarefas de resumo, o seguinte conjunto de cálculos começa:</span><span class="sxs-lookup"><span data-stu-id="2dbe8-133">Regardless of whether the user reprojects by using the remaining effort or the progress percentage on the summary tasks, the following set of calculations begins:</span></span>

- <span data-ttu-id="2dbe8-134">A EAC, a ETC e a percentagem de progresso na tarefa são calculadas.</span><span class="sxs-lookup"><span data-stu-id="2dbe8-134">The EAC, ETC, and progress percentage on the task are calculated.</span></span>
- <span data-ttu-id="2dbe8-135">A nova EAC é distribuída para as tarefas subordinadas na mesma proporção que a EAC original na tarefa.</span><span class="sxs-lookup"><span data-stu-id="2dbe8-135">The new EAC is distributed down to the child tasks in the same proportion as the original EAC was on the task.</span></span>
- <span data-ttu-id="2dbe8-136">A nova EAC em cada uma das tarefas individuais até às tarefas do nó de folha é calculada.</span><span class="sxs-lookup"><span data-stu-id="2dbe8-136">The new EAC on each of the individual tasks down to the leaf node tasks is calculated.</span></span> 
- <span data-ttu-id="2dbe8-137">As tarefas subordinadas afetadas até ao nó de folha têm a ETC e a percentagem de progresso recalculada com base no valor da EAC.</span><span class="sxs-lookup"><span data-stu-id="2dbe8-137">The affected child tasks down to the leaf nodes have their ETC and progress percentage recalculated based on the EAC value.</span></span> <span data-ttu-id="2dbe8-138">Isto resulta numa nova projeção para o desvio do esforço da tarefa.</span><span class="sxs-lookup"><span data-stu-id="2dbe8-138">This results in a new projection for the effort variance of the task.</span></span> 
- <span data-ttu-id="2dbe8-139">As EACs das tarefas de resumo até ao nó raiz são recalculadas.</span><span class="sxs-lookup"><span data-stu-id="2dbe8-139">The EACs of the summary tasks all the way to the root node are recalculated.</span></span>

### <a name="cost-tracking-view"></a><span data-ttu-id="2dbe8-140">Vista Controlo dos custos</span><span class="sxs-lookup"><span data-stu-id="2dbe8-140">Cost tracking view</span></span> 

<span data-ttu-id="2dbe8-141">A vista **Controlo dos custos** compara o custo real gasto numa tarefa com o custo planeado.</span><span class="sxs-lookup"><span data-stu-id="2dbe8-141">The **Cost tracking** view compares the actual cost that was spent on a task to the planned cost.</span></span> 

> [!NOTE]
> <span data-ttu-id="2dbe8-142">Esta vista mostra apenas os custos de mão de obra e não inclui os custos das estimativas de despesas.</span><span class="sxs-lookup"><span data-stu-id="2dbe8-142">This view shows only labor costs and doesn’t include costs from the expense estimates.</span></span> 

<span data-ttu-id="2dbe8-143">O Project Service Automation utiliza as seguintes fórmulas para calcular as métricas de monitorização:</span><span class="sxs-lookup"><span data-stu-id="2dbe8-143">Project Service Automation uses the following formulas to calculate the tracking metrics:</span></span>

<span data-ttu-id="2dbe8-144">Quando uma tarefa é criada, o custo previsto é igual ao custo estimado aquando da conclusão.</span><span class="sxs-lookup"><span data-stu-id="2dbe8-144">When a task is created, the planned cost is equal to the estimated cost at complete.</span></span> <span data-ttu-id="2dbe8-145">Depois dos Atuais serem registados na tarefa, o seguinte é calculado na vista **Monitorização** para o custo:</span><span class="sxs-lookup"><span data-stu-id="2dbe8-145">After actuals are recorded on the task, the following is calculated on the **Tracking** view for cost:</span></span>

 - <span data-ttu-id="2dbe8-146">Percentagem do custo consumido = Custo real gasto até à data ÷ Custo estimado na conclusão para a tarefa</span><span class="sxs-lookup"><span data-stu-id="2dbe8-146">Percentage of cost consumed = Actual cost spent to date ÷ Estimated cost at complete for the task</span></span>
 - <span data-ttu-id="2dbe8-147">Custo para conclusão (CTC) = Custo estimado na conclusão – Custo real gasto até à data</span><span class="sxs-lookup"><span data-stu-id="2dbe8-147">Cost to complete (CTC) = Estimated cost at complete – Actual cost spent to date</span></span>
 - <span data-ttu-id="2dbe8-148">Custo estimado na conclusão = CTC + Custo real gasto até à data</span><span class="sxs-lookup"><span data-stu-id="2dbe8-148">Estimated cost at complete = CTC + Actual cost spent to date</span></span>
 - <span data-ttu-id="2dbe8-149">Variância de custos projetados = Custo planeado – Custo estimado na conclusão</span><span class="sxs-lookup"><span data-stu-id="2dbe8-149">Projected cost variance = Planned cost – Estimated cost at complete</span></span>

<span data-ttu-id="2dbe8-150">Uma projeção do desvio de custo é mostrada na tarefa.</span><span class="sxs-lookup"><span data-stu-id="2dbe8-150">A projection of the cost variance is shown on the task.</span></span> <span data-ttu-id="2dbe8-151">Se o custo estimado na conclusão for superior ao custo planeado, a tarefa é projetada para custar mais do que o planeado originalmente.</span><span class="sxs-lookup"><span data-stu-id="2dbe8-151">If the estimated cost at complete is more than the planned cost, the task is projected to cost more than was originally planned.</span></span> <span data-ttu-id="2dbe8-152">Portanto, está acima do orçamento.</span><span class="sxs-lookup"><span data-stu-id="2dbe8-152">Therefore, it's trending over budget.</span></span> <span data-ttu-id="2dbe8-153">Se o custo Estimado na conclusão for inferior ao custo planeado, a tarefa é projetada para custar menos do que o planeado originalmente e está dentro do orçamento.</span><span class="sxs-lookup"><span data-stu-id="2dbe8-153">If the Estimated cost at complete is less than the planned cost, the task is projected to cost less than was originally planned and is trending under budget.</span></span>

## <a name="project-managers-reprojection-of-cost"></a><span data-ttu-id="2dbe8-154">Reprojeção de custos do gestor de projeto</span><span class="sxs-lookup"><span data-stu-id="2dbe8-154">Project manager’s reprojection of cost</span></span>

<span data-ttu-id="2dbe8-155">Quando o esforço é reprojetado, o CTC, o Custo estimado na conclusão, a percentagem do custo consumido e o desvio de custo projetado são todos recalculados na vista **Controlo dos custos**.</span><span class="sxs-lookup"><span data-stu-id="2dbe8-155">When effort is reprojected, the CTC, Estimated cost at complete, percentage of cost consumed, and projected cost variance are all recalculated in the **Cost tracking** view.</span></span>

## <a name="project-status-summary"></a><span data-ttu-id="2dbe8-156">Resumo do estado do projeto</span><span class="sxs-lookup"><span data-stu-id="2dbe8-156">Project status summary</span></span>

<span data-ttu-id="2dbe8-157">Os dados de monitorização nas vistas **Controlo do esforço** e **Controlo dos custos** mostram o progresso e o consumo de custo no nó raiz do projeto, nas tarefas de resumo e nos níveis de tarefas dos nós de folha.</span><span class="sxs-lookup"><span data-stu-id="2dbe8-157">Tracking data in the **Effort tracking** and **Cost tracking** views shows the progress and cost consumption at the project root node, summary tasks, and leaf node tasks levels.</span></span> <span data-ttu-id="2dbe8-158">A secção **Estado** na página **Entidade do Projeto** mostra um resumo do estado do nível do projeto.</span><span class="sxs-lookup"><span data-stu-id="2dbe8-158">The **Status** section on the **Project entity** page shows a summary of project-level status.</span></span>

## <a name="status-summary-fields"></a><span data-ttu-id="2dbe8-159">Campos Resumo do estado</span><span class="sxs-lookup"><span data-stu-id="2dbe8-159">Status summary fields</span></span>

<span data-ttu-id="2dbe8-160">O campo **Estado Geral do Projeto** é um campo editável que mostra o estado geral do projeto.</span><span class="sxs-lookup"><span data-stu-id="2dbe8-160">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="2dbe8-161">Utiliza a codificação de cores, tal como verde, amarela e vermelha, para indicar um risco de aumento.</span><span class="sxs-lookup"><span data-stu-id="2dbe8-161">It uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> <span data-ttu-id="2dbe8-162">O campo **Comentários** permite que o gestor de projeto introduza comentários específicos sobre o estado.</span><span class="sxs-lookup"><span data-stu-id="2dbe8-162">The **Comments** field lets the project manager enter specific comments about the status.</span></span> <span data-ttu-id="2dbe8-163">O campo **Estado atualizado em** não é editável e o valor é um carimbo de data/hora que indica quando o estado foi atualizado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="2dbe8-163">The **Status updated on** field is not editable and the value is a timestamp that indicates when the status was last updated.</span></span>

<span data-ttu-id="2dbe8-164">Os campos **Desempenho de Agendamento** e **Desempenho de Custos** são definidos a partir da data de monitorização.</span><span class="sxs-lookup"><span data-stu-id="2dbe8-164">The **Schedule performance** and **Cost performance** fields are set from the tracking date.</span></span> <span data-ttu-id="2dbe8-165">Quando os desvios da agenda e de custo do nó raiz na vista **Controlo do esforço** são positivos, é possível definir estes campos como **Adiantado**.</span><span class="sxs-lookup"><span data-stu-id="2dbe8-165">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, you can set these fields to **Ahead**.</span></span> <span data-ttu-id="2dbe8-166">Quando os desvios da agenda e de custo do nó raiz são negativos, é possível defini-los como **Atrasado**.</span><span class="sxs-lookup"><span data-stu-id="2dbe8-166">When the schedule and cost variance for the root node are negative, you can set them to **Behind**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]