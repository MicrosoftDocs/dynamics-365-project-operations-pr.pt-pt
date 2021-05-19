---
title: Monitorização de custo do projeto
description: Este tópico fornece informações sobre como o Project Operations acompanha o progresso contra o custo da mão de obra e gastos num projeto.
author: rumant
manager: AnnBe
ms.date: 03/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 28cb692c61ae4137a28973dc1bd70ffd989dd535
ms.sourcegitcommit: a1f9f92546ab5d8d8e5a4710ce4c96414ea55d14
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 03/24/2021
ms.locfileid: "5711076"
---
# <a name="labor-cost-tracking-on-projects"></a><span data-ttu-id="31166-103">Monitorização de custos de mão de obra em projetos</span><span class="sxs-lookup"><span data-stu-id="31166-103">Labor cost tracking on projects</span></span>

<span data-ttu-id="31166-104">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="31166-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="31166-105">Dynamics 365 Project Operations rastreia as estimativas de mão de obra e gastos na granularidade mais baixa exigida no plano do projeto.</span><span class="sxs-lookup"><span data-stu-id="31166-105">Dynamics 365 Project Operations tracks labor estimates and spend at the lowest required granularity on the project plan.</span></span> <span data-ttu-id="31166-106">A estimativa financeira do custo da mão de obra baseia-se no esforço planeado e nos recursos genéricos ou nomeados que são atribuídos a cada tarefa de nó de folhas no plano do projeto.</span><span class="sxs-lookup"><span data-stu-id="31166-106">The financial estimate of labor cost is based on the planned effort and the generic or named resources that are assigned to each leaf-node task in the project plan.</span></span> <span data-ttu-id="31166-107">Quando o projeto começa e as pessoas começam a reportar tempo em várias tarefas do projeto, o gasto real em mão de obra é resumido, o que inicia um cálculo das projeções.</span><span class="sxs-lookup"><span data-stu-id="31166-107">When the project begins and people start to report time on various project tasks, the actual spend on labor is summarized which starts a calculation of the projections.</span></span>

## <a name="labor-cost-tracking-view"></a><span data-ttu-id="31166-108">Vista de monitorização de custo de mão de obra</span><span class="sxs-lookup"><span data-stu-id="31166-108">Labor Cost Tracking view</span></span>

<span data-ttu-id="31166-109">Na página **Projetos**, no separador **Monitorização**, pode selecionar **Monitorização** > **Custo** para abrir a vista de **Monitorização de custo** e ver o progresso do gasto de mão de obra em cada tarefa no plano do projeto.</span><span class="sxs-lookup"><span data-stu-id="31166-109">On the **Projects** page, on the **Tracking** tab, you can select **Tracking** > **Cost** to open the **Cost Tracking** view and see the progress of labor spend on each task in the project plan.</span></span> <span data-ttu-id="31166-110">Esta perspetiva também compara o custo real da mão de obra gasto numa tarefa com o custo de mão de obra planeada da tarefa.</span><span class="sxs-lookup"><span data-stu-id="31166-110">This view also compares the actual labor cost spent on a task to the task's planned labor cost.</span></span> <span data-ttu-id="31166-111">O Project Operations utiliza as seguintes fórmulas para calcular as métricas do custo da mão de obra:</span><span class="sxs-lookup"><span data-stu-id="31166-111">Project Operations uses the following formulas to calculate labor cost metrics:</span></span>

- <span data-ttu-id="31166-112">**Custo previsto**: Custo estimado de todas as atribuições de recursos em cada tarefa do nó folha</span><span class="sxs-lookup"><span data-stu-id="31166-112">**Planned cost**: Estimated cost of all resource assignments on each leaf node task</span></span>
- <span data-ttu-id="31166-113">**Custo real**: Soma de todos os custos reais pelo tempo registado na tarefa</span><span class="sxs-lookup"><span data-stu-id="31166-113">**Actual Cost**: Sum of all cost actuals for time recorded on the task</span></span>
- <span data-ttu-id="31166-114">**Percentagem de consumo de custos**: Custo real ÷ Estimativa de custos na conclusão</span><span class="sxs-lookup"><span data-stu-id="31166-114">**Cost consumption percentage**: Actual cost ÷ Cost estimate at complete</span></span>
- <span data-ttu-id="31166-115">**Custo restante**: Estimativa de custo na conclusão – Custo real</span><span class="sxs-lookup"><span data-stu-id="31166-115">**Remaining Cost**: Cost estimate at complete  – Actual cost</span></span>
- <span data-ttu-id="31166-116">**Custo na conclusão**: Custo restante – Custo real</span><span class="sxs-lookup"><span data-stu-id="31166-116">**Cost at Complete**: Remaining cost + Actual cost</span></span>
- <span data-ttu-id="31166-117">**Variação de custo**: Custo planificado – Estimativa de custo na conclusão</span><span class="sxs-lookup"><span data-stu-id="31166-117">**Cost variance**: Planned cost – Cost estimate at complete</span></span>

<span data-ttu-id="31166-118">Cada tarefa apresenta uma projeção do desvio de custo na tarefa.</span><span class="sxs-lookup"><span data-stu-id="31166-118">Each task shows a projection of the cost variance on the task.</span></span> <span data-ttu-id="31166-119">Se a estimativa de custos na conclusão for superior ao custo previsto, prevê-se que a tarefa ultrapasse o orçamento.</span><span class="sxs-lookup"><span data-stu-id="31166-119">If the cost estimate at complete is more than the planned cost, the task is projected to go over budget.</span></span> <span data-ttu-id="31166-120">Se a estimativa de custos na conclusão for inferior ao custo previsto, prevê-se que a tarefa termine abaixo do orçamento.</span><span class="sxs-lookup"><span data-stu-id="31166-120">If the cost estimate at complete is less than the planned cost, the task is projected to finish under budget.</span></span>

>[!NOTE]
> <span data-ttu-id="31166-121">O Project Operations só mostra os custos de mão de obra na página do **Projeto** no separador **Monitorização**. Embora os materiais e despesas possam ser estimados e rastreados para consumo, estes custos não estão incluídos nos custos indicados no separador **Monitorização**. Este separador destina-se a funcionar apenas para tornar a projetar os custos da mão de obra através da nova projeção do esforço.</span><span class="sxs-lookup"><span data-stu-id="31166-121">Project Operations only shows labor costs on the **Project** page on the **Tracking** tab. While materials and expenses can be estimated and tracked for consumption, these costs are not included in the costs shown on the **Tracking** tab. This tab is designed to work only for reprojecting labor costs by reprojecting effort.</span></span>
<span data-ttu-id="31166-122">Todos os montantes de custos apresentados são convertidos para a moeda de custo do projeto a partir da moeda de preço do projeto utilizada para determinar a taxa de custo.</span><span class="sxs-lookup"><span data-stu-id="31166-122">All cost amounts shown are converted to the project's cost currency from the project's cost price currency used to determine the cost rate.</span></span> <span data-ttu-id="31166-123">A moeda de custo do projeto é a moeda da unidade de contratação do projeto.</span><span class="sxs-lookup"><span data-stu-id="31166-123">The cost currency of the project is the currency of the contracting unit on the project.</span></span> <span data-ttu-id="31166-124">Os valores de custo estimados para o tempo que são mostrados no separador **Estimativas** na página do **Projeto** podem não somar o custo planeado no separador **Monitorização**. A razão desta discrepância deve-se às diferenças de como o custo estimado é resumido na grelha de **Estimativas** e como o custo planeado é calculado na rede de **Monitorização**.</span><span class="sxs-lookup"><span data-stu-id="31166-124">The estimated cost values for time that are shown on the **Estimates** tab on the **Project** page might not add up to the planned cost on the **Tracking** tab. The reason for this discrepancy is because of the differences in how estimated cost is summarized on the **Estimates** grid and how planned cost is calculated on the **Tracking** grid.</span></span> 
>
> - <span data-ttu-id="31166-125">O separador **Estimativa** calcula o custo estimado utilizando a mesma moeda da taxa de custo na tabela de preços.</span><span class="sxs-lookup"><span data-stu-id="31166-125">The **Estimates tab** calculates the estimated cost by using the same currency of the cost rate in the price list.</span></span> <span data-ttu-id="31166-126">Em seguida, o custo estimado na moeda da lista de preços é convertido para o custo estimado na moeda de custo do projeto.</span><span class="sxs-lookup"><span data-stu-id="31166-126">Then, the estimated cost in the price list currency is converted to the estimated cost in the project's cost currency.</span></span> <span data-ttu-id="31166-127">O custo estimado na moeda do projeto é apresentado arredondado para 2 casas decimais.</span><span class="sxs-lookup"><span data-stu-id="31166-127">The estimated cost in the project currency is shown rounded to 2 decimal places.</span></span> <span data-ttu-id="31166-128">Em nenhum momento durante esta conversão é aplicada a precisão cambial.</span><span class="sxs-lookup"><span data-stu-id="31166-128">At no point during this conversion is currency precision applied.</span></span> 
> - <span data-ttu-id="31166-129">No separador **Monitorização**, o cálculo de custos previsto segue uma ordem de cálculo ligeiramente diferente que envolve a aplicação da precisão da moeda em duas fases:</span><span class="sxs-lookup"><span data-stu-id="31166-129">On the **Tracking** tab, the planned cost calculation follows a slightly different calculation order that involves currency precision being applied in two stages:</span></span> 
   ><ol>
   ><li><span data-ttu-id="31166-130">O valor estimado do custo na moeda da lista de preços é convertido para a moeda base (conversão 1).</span><span class="sxs-lookup"><span data-stu-id="31166-130">The estimated cost amount in the price list currency is converted to the base currency (conversion 1).</span></span></li>
   ><li><span data-ttu-id="31166-131">O valor estimado do custo na moeda base é convertido para a moeda do projeto (conversão 2).</span><span class="sxs-lookup"><span data-stu-id="31166-131">The estimated cost amount in the base currency is converted to the project cost currency (conversion 2).</span></span> </li>
   ></ol>
   ><span data-ttu-id="31166-132">A precisão da moeda é aplicada em ambas as etapas para obter um custo planeado (no separador **Monitorização**) que se desvia ligeiramente do custo estimado (na vista **tempo - vista faseada** no separador **Estimativas**).</span><span class="sxs-lookup"><span data-stu-id="31166-132">Currency precision is applied in both steps to get a planned cost (on the **Tracking** tab) that deviates slightly from the estimated cost (on the **Time - phased** view on the **Estimates** tab).</span></span> 
   
## <a name="reprojecting-costs-on-leaf-node-tasks"></a><span data-ttu-id="31166-133">Reprojetar os custos nas tarefas do nó folha</span><span class="sxs-lookup"><span data-stu-id="31166-133">Reprojecting costs on leaf node tasks</span></span>

<span data-ttu-id="31166-134">Os custos de mão de obra numa tarefa de nó de folha não podem ser reprojetados diretamente no separador **Monitorização** na página do **Projeto**.</span><span class="sxs-lookup"><span data-stu-id="31166-134">Labor costs on a leaf node task can't be directly reprojected on the **Tracking** tab on the **Project page**.</span></span> <span data-ttu-id="31166-135">No entanto, pode utilizar a vista **Esforço de monitorização** para reprojetar o esforço restante numa tarefa.</span><span class="sxs-lookup"><span data-stu-id="31166-135">However, you can use the **Effort Tracking** view to reproject the remaining effort on a task.</span></span> <span data-ttu-id="31166-136">Isto provoca um recálculo do custo remanescente da tarefa.</span><span class="sxs-lookup"><span data-stu-id="31166-136">This causes a recalculation of the remaining cost on the task.</span></span> <span data-ttu-id="31166-137">Segue-se uma descrição de como isto funciona.</span><span class="sxs-lookup"><span data-stu-id="31166-137">The following is a description of how this works.</span></span>

1. <span data-ttu-id="31166-138">Um gestor de projeto pode reprojetar esforço em tarefas atualizando o valor padrão no campo **Esforço Restante** com uma nova estimativa do esforço restante na tarefa.</span><span class="sxs-lookup"><span data-stu-id="31166-138">A project manager can reproject effort on tasks by updating the default value in the **Remaining Effort** field with a new estimate of the remaining effort on the task.</span></span> <span data-ttu-id="31166-139">A reprojeção provoca um recalcular da estimativa de esforço da tarefa na conclusão (EAC), percentagem de progresso e variação de esforço projetada numa tarefa.</span><span class="sxs-lookup"><span data-stu-id="31166-139">Reprojecting causes a recalculation of the task's effort estimate at complete (EAC), progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="31166-140">A EAC, estimativa de concusão (ETC) e a percentagem de progresso das tarefas de resumo também são recalculadas e produzem uma nova projeção de variância do esforço.</span><span class="sxs-lookup"><span data-stu-id="31166-140">The EAC, estimate to complete (ETC), and progress percentage on the summary tasks are also recalculated and produce a new projection of effort variance.</span></span>
2. <span data-ttu-id="31166-141">Com base no novo valor para o esforço restante na tarefa, o sistema calcula o custo remanescente na vista de **Monitorização de custos**.</span><span class="sxs-lookup"><span data-stu-id="31166-141">Based on the new value for the remaining effort on the task, the system calculates the remaining cost on the **Cost Tracking** view.</span></span> <span data-ttu-id="31166-142">Para calcular o custo remanescente com base no esforço remanescente, o sistema calcula primeiro o custo médio de uma hora de esforço na tarefa como custo planeado ou esforço planeado.</span><span class="sxs-lookup"><span data-stu-id="31166-142">To calculate the remaining cost based on the remaining effort, the system first calculates the average cost of one hour of effort on the task as planned cost or planned effort.</span></span> <span data-ttu-id="31166-143">O custo previsto é a soma do custo de todas as atribuições de recursos na tarefa.</span><span class="sxs-lookup"><span data-stu-id="31166-143">The planned cost is the sum of the cost of all resource assignments on the task.</span></span> <span data-ttu-id="31166-144">O custo médio por hora é utilizado para calcular o custo remanescente para o esforço remanescente recentemente projetado na tarefa.</span><span class="sxs-lookup"><span data-stu-id="31166-144">The average cost per hour is used to compute the remaining cost for the newly projected remaining effort on the task.</span></span>
3. <span data-ttu-id="31166-145">O custo em percentagem completa e de consumo de custos na tarefa do nó folha é recalculado.</span><span class="sxs-lookup"><span data-stu-id="31166-145">The cost at complete and cost consumption percentage on the leaf-node task are re-calculated.</span></span>
4. <span data-ttu-id="31166-146">O custo em valor completo das tarefas de resumo até ao nó raiz é recalculado.</span><span class="sxs-lookup"><span data-stu-id="31166-146">The cost at complete value of the summary tasks all the way to the root node are recalculated.</span></span>

## <a name="reprojecting-costs-on-summary-tasks"></a><span data-ttu-id="31166-147">Reprojetar os custos nas tarefas de resumo</span><span class="sxs-lookup"><span data-stu-id="31166-147">Reprojecting costs on summary tasks</span></span>

<span data-ttu-id="31166-148">Pode reprojetar os custos de mão de obra em tarefas de resumo ou tarefas de contentores.</span><span class="sxs-lookup"><span data-stu-id="31166-148">You can reproject labor costs on summary tasks or container tasks.</span></span> <span data-ttu-id="31166-149">No entanto, não pode reprojetar custos de mão de obra diretamente numa tarefa de resumo de projeto no separador **Monitorização** na página **Projeto**.</span><span class="sxs-lookup"><span data-stu-id="31166-149">However, you can't directly reproject labor cost on a summary project task on the **Tracking** tab on the **Project** page.</span></span> <span data-ttu-id="31166-150">Semelhantes às tarefas do nó de folhas, o resumo reprojetar e as tarefas do contentor podem ser feitas utilizando a vista **Monitorização de esforço**.</span><span class="sxs-lookup"><span data-stu-id="31166-150">Similar to leaf node tasks, reprojecting summary and container tasks can be done using the **Effort Tracking** view.</span></span> <span data-ttu-id="31166-151">Nesta vista, pode reprojetar o esforço restante numa tarefa de resumo que provoque um recálculo do custo remanescente na tarefa de resumo.</span><span class="sxs-lookup"><span data-stu-id="31166-151">In this view, you can reproject the remaining effort on a summary task causing a recalculation of the remaining cost on the summary task.</span></span> <span data-ttu-id="31166-152">Segue-se uma descrição de como isto funciona.</span><span class="sxs-lookup"><span data-stu-id="31166-152">The following is a description of how this works.</span></span>

1. <span data-ttu-id="31166-153">Um gestor de projeto pode reprojetar esforço em tarefas de resumo atualizando o valor padrão do esforço restante com uma nova estimativa do esforço restante na tarefa.</span><span class="sxs-lookup"><span data-stu-id="31166-153">A project manager can reproject effort on summary tasks by updating the default value of the remaining effort with a new estimate on the task.</span></span> <span data-ttu-id="31166-154">Esta atualização provoca um recalcular da estimativa de resumo da tarefa na conclusão (EAC), percentagem de progresso e variação de esforço projetada numa tarefa.</span><span class="sxs-lookup"><span data-stu-id="31166-154">This update causes a recalculation of the summary task's estimate at complete (EAC), progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="31166-155">A EAC, a ETC e a percentagem de progresso das tarefas de resumo também são recalculadas e produzem uma nova projeção de variância do esforço.</span><span class="sxs-lookup"><span data-stu-id="31166-155">The EAC, ETC, and progress percentage on the summary tasks are also recalculated and produce a new projection of effort variance.</span></span>
2. <span data-ttu-id="31166-156">Com base no novo valor para o esforço restante na tarefa de resumo, o sistema calcula o custo remanescente na vista de **Monitorização de custos**.</span><span class="sxs-lookup"><span data-stu-id="31166-156">Based on the new value for remaining effort on the summary task, the system calculates the remaining cost on the **Cost Tracking** view.</span></span> <span data-ttu-id="31166-157">Para calcular o custo remanescente com base no esforço remanescente, o sistema calcula primeiro o custo médio de uma hora de esforço na tarefa de resumo como custo planeado ou esforço planeado.</span><span class="sxs-lookup"><span data-stu-id="31166-157">To calculate the remaining cost based on the remaining effort, the system first calculates the average cost of one hour of effort on the summary task as planned cost or planned effort.</span></span> <span data-ttu-id="31166-158">O custo médio por hora é utilizado para calcular o custo do novo esforço remanescente projetado na tarefa de resumo.</span><span class="sxs-lookup"><span data-stu-id="31166-158">The average cost per hour is used to calculate the cost of the newly projected remaining effort on the summary task.</span></span>
3. <span data-ttu-id="31166-159">O custo em percentagem completa e de consumo de custos na tarefa de resumo é recalculado.</span><span class="sxs-lookup"><span data-stu-id="31166-159">The cost at complete and cost consumption percentage on the summary task are re-calculated.</span></span>
4. <span data-ttu-id="31166-160">O novo custo na conclusão é distribuído para as tarefas de elemento subordinado na mesma proporção que o custo planificado tinha na tarefa.</span><span class="sxs-lookup"><span data-stu-id="31166-160">The new cost at complete is distributed down to the child tasks in the same proportion as the original planned cost was on the task.</span></span>
5. <span data-ttu-id="31166-161">O novo custo com valor completo em cada uma das tarefas individuais até às tarefas do nó de folha é calculado.</span><span class="sxs-lookup"><span data-stu-id="31166-161">The new cost at complete value on each of the individual tasks down to the leaf node tasks is calculated.</span></span> <span data-ttu-id="31166-162">Com base neste valor, as tarefas de elemento subordinado afetadas até aos nós das folhas terão o seu custo remanescente e a percentagem de consumo de custos recalculadas com base no custo pelo valor total.</span><span class="sxs-lookup"><span data-stu-id="31166-162">Based on this value, the affected child tasks down to the leaf nodes will have their remaining cost and cost consumption percentage recalculated based on the cost at complete value.</span></span> <span data-ttu-id="31166-163">Este valor resulta numa nova projeção para o desvio de custo da tarefa.</span><span class="sxs-lookup"><span data-stu-id="31166-163">This value results in a new projection for the cost variance of the task.</span></span> 


<span data-ttu-id="31166-164">O campo **Desempenho de custo** pode ser definido a partir dos dados de monitorização.</span><span class="sxs-lookup"><span data-stu-id="31166-164">The **Cost performance** field can be set from the tracking data.</span></span> <span data-ttu-id="31166-165">Quando a variação de custos para o nó raiz na vista **Monitorização de custo** é negativa, pode definir este campo como **Abaixo do orçamento**.</span><span class="sxs-lookup"><span data-stu-id="31166-165">When the cost variance for the root node in the **Cost tracking** view is negative, you can set this field to **Under Budget**.</span></span> <span data-ttu-id="31166-166">Quando a variação de custo para o nó de raiz é positiva, pode definir o valor como **Acima do orçamento**.</span><span class="sxs-lookup"><span data-stu-id="31166-166">When the cost variance for the root node is positive, you can set the value to **Over Budget**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]