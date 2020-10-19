---
title: Mapear projetos e tarefas para uma linha de proposta baseada no projeto
description: Este tópico fornece informações sobre como mapear os projetos e as tarefas para uma linha de tarefa baseada em projetos.
author: rumant
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d726ab09da0e502da99191f7e7469c47f79b6e7c
ms.sourcegitcommit: 6b396ccf5e76230a42a2f933a3aaa5b8149790bb
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/06/2020
ms.locfileid: "3964921"
---
# <a name="map-projects-and-tasks-to-a-project-based-quote-line"></a><span data-ttu-id="fea43-103">Mapear projetos e tarefas para uma linha de proposta baseada no projeto</span><span class="sxs-lookup"><span data-stu-id="fea43-103">Map projects and tasks to a project-based quote line</span></span>

<span data-ttu-id="fea43-104">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="fea43-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="fea43-105">Nas linhas de proposta baseadas em projetos, pode mapear as tarefas específicas de um projeto que já esteja associado a uma linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="fea43-105">On project-based quote lines, you can map the specific tasks of a project that is already associated to a quote line.</span></span>

<span data-ttu-id="fea43-106">Quando mapeia tarefas para uma linha de proposta, os seguintes itens que definiu na linha de proposta aplicar-se-ão apenas a essas tarefas:</span><span class="sxs-lookup"><span data-stu-id="fea43-106">When you map tasks to a quote line, the following items you defined on the quote line will only apply to those tasks:</span></span>

- <span data-ttu-id="fea43-107">Método de faturação</span><span class="sxs-lookup"><span data-stu-id="fea43-107">Billing method</span></span>
- <span data-ttu-id="fea43-108">Opções de exigibilidade</span><span class="sxs-lookup"><span data-stu-id="fea43-108">Chargeability options</span></span>
- <span data-ttu-id="fea43-109">Limites a não exceder</span><span class="sxs-lookup"><span data-stu-id="fea43-109">Not-to-exceed limits</span></span>
- <span data-ttu-id="fea43-110">Clientes</span><span class="sxs-lookup"><span data-stu-id="fea43-110">Customers</span></span>

<span data-ttu-id="fea43-111">Por exemplo, pode ter um projeto onde uma fase é com preço fixo e todas as outras fases são tempo e materiais.</span><span class="sxs-lookup"><span data-stu-id="fea43-111">For example, you might have a project where one phase is fixed price and all the other phases are time and materials.</span></span> <span data-ttu-id="fea43-112">Neste caso, pode associar a primeira fase, e todas as suas tarefas subordinadas, à linha de proposta para essa fase com um método de faturação de preço fixo.</span><span class="sxs-lookup"><span data-stu-id="fea43-112">In this case, you can associate the first phase, and all of its child tasks, to the quote line for that phase with a fixed price billing method.</span></span> <span data-ttu-id="fea43-113">Em seguida, pode associar todas as outras fases à linha de proposta baseada em tempo e materiais.</span><span class="sxs-lookup"><span data-stu-id="fea43-113">You can then associate all the other phases to the time and materials-based quote line.</span></span>

## <a name="associate-tasks-to-project-based-quote-lines"></a><span data-ttu-id="fea43-114">Associar tarefas a linhas de proposta baseadas em projetos</span><span class="sxs-lookup"><span data-stu-id="fea43-114">Associate tasks to project-based quote lines</span></span>

<span data-ttu-id="fea43-115">Pode associar tarefas a linhas de proposta a partir das seguintes localizações:</span><span class="sxs-lookup"><span data-stu-id="fea43-115">You can associate tasks with quote lines from the following locations:</span></span>

- <span data-ttu-id="fea43-116">Página **Projeto** > **Faturação de tarefas** tab (ideal)</span><span class="sxs-lookup"><span data-stu-id="fea43-116">**Project** page > **Task billing** tab (optimal)</span></span>
- <span data-ttu-id="fea43-117">Página **Linha de Proposta** > separador **Tarefas Faturáveis**</span><span class="sxs-lookup"><span data-stu-id="fea43-117">**Quote Line** page > **Chargeable tasks** tab</span></span> 

### <a name="from-the-project-page"></a><span data-ttu-id="fea43-118">A partir da página Projeto</span><span class="sxs-lookup"><span data-stu-id="fea43-118">From the Project page</span></span>

<span data-ttu-id="fea43-119">A página **Projeto** proporciona a experiência ideal para associar tarefas a linhas de proposta.</span><span class="sxs-lookup"><span data-stu-id="fea43-119">The **Project** page provides the optimal experience for associating tasks to quote lines.</span></span> <span data-ttu-id="fea43-120">Pode utilizar esta página para selecionar várias tarefas e associar todas, bem com as respetivas tarefas subordinadas, à linha de proposta selecionada.</span><span class="sxs-lookup"><span data-stu-id="fea43-120">You can use this page to select multiple tasks and associate all of them, plus their child tasks, to the selected quote line.</span></span>

1. <span data-ttu-id="fea43-121">No separador **Geral** de uma linha de proposta baseada em projetos, verifique se o campo **Projeto** está preenchido.</span><span class="sxs-lookup"><span data-stu-id="fea43-121">On the **General** tab of a project–based quote line, verify the **Project** field is filled out.</span></span>
2. <span data-ttu-id="fea43-122">No campo **Tarefas incluídas**, selecione **Apenas tarefas selecionadas**.</span><span class="sxs-lookup"><span data-stu-id="fea43-122">In the **Included tasks** field, select **Selected tasks only**.</span></span>
3. <span data-ttu-id="fea43-123">Guarde a linha de proposta baseada em projetos.</span><span class="sxs-lookup"><span data-stu-id="fea43-123">Save the project-based quote line.</span></span> <span data-ttu-id="fea43-124">Quando o formulário é atualizado, é apresentado o separador **Tarefas Faturáveis**.</span><span class="sxs-lookup"><span data-stu-id="fea43-124">When the form refreshes, the **Chargeable tasks** tab displays.</span></span>
4. <span data-ttu-id="fea43-125">No separador **Geral**, selecione a ligação para o projeto a partir do campo **Projeto**.</span><span class="sxs-lookup"><span data-stu-id="fea43-125">On the **General** tab, select the link for the project from the **Project** field.</span></span>
5. <span data-ttu-id="fea43-126">Na página **Projeto**, selecione o separador **Faturação de Tarefas**.</span><span class="sxs-lookup"><span data-stu-id="fea43-126">On the **Project** page, select the **Task billing** tab.</span></span>
6. <span data-ttu-id="fea43-127">Na segunda grelha, que se aplica à configuração da faturação específica da tarefa, selecione uma ou mais tarefas e, em seguida, selecione **Associar linhas de proposta**.</span><span class="sxs-lookup"><span data-stu-id="fea43-127">In the second grid, which applies to task-specific billing setup, select one or more tasks and then select **Associate quote lines**.</span></span>
7. <span data-ttu-id="fea43-128">Na página de diálogo apresentada, selecione uma linha de proposta que apresente linhas de proposta baseadas em projetos na proposta.</span><span class="sxs-lookup"><span data-stu-id="fea43-128">In the dialog page that appears, select a quote line that displays project-based quote lines on the quote.</span></span>
8. <span data-ttu-id="fea43-129">No campo **Tipo de faturação**, indique se estas tarefas são faturáveis ou não faturáveis.</span><span class="sxs-lookup"><span data-stu-id="fea43-129">In the **Billing type** field, indicate if these tasks are chargeable or non-chargeable.</span></span>
9. <span data-ttu-id="fea43-130">Selecione a caixa de verificação para indicar se a associação deve incluir as tarefas subordinadas das tarefas selecionadas.</span><span class="sxs-lookup"><span data-stu-id="fea43-130">Select the check box to indicate if the association should include child tasks of the selected tasks.</span></span> <span data-ttu-id="fea43-131">Selecionar a caixa irá associar as tarefas subordinadas das tarefas selecionadas à linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="fea43-131">Checking the box will associate the child tasks of the selected tasks to the quote line.</span></span>
10. <span data-ttu-id="fea43-132">Selecione **OK** para fechar a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="fea43-132">Select **OK** to close the dialog.</span></span>

### <a name="from-the-quote-line-page"></a><span data-ttu-id="fea43-133">A partir da página Linha de proposta</span><span class="sxs-lookup"><span data-stu-id="fea43-133">From the Quote line page</span></span>

<span data-ttu-id="fea43-134">Pode associar tarefas de projeto a linhas de proposta a partir do separador **Tarefas Faturáveis** na página **Linha de proposta**.</span><span class="sxs-lookup"><span data-stu-id="fea43-134">You can associate project tasks to quote lines from the **Chargeable tasks** tab on **Quote line** page.</span></span>

>[!NOTE]
><span data-ttu-id="fea43-135">O local ideal para associar tarefas de projeto a linhas de proposta é o separador **Faturação de tarefas** na página **Projeto**.</span><span class="sxs-lookup"><span data-stu-id="fea43-135">The optimal place to associate project tasks to quote lines is on the **Task billing** tab on the **Project** page.</span></span> <span data-ttu-id="fea43-136">Se associar tarefas a partir do separador **Tarefas Faturáveis** na página **Linha de proposta**, tem de associar manualmente cada projeto.</span><span class="sxs-lookup"><span data-stu-id="fea43-136">If you associate tasks from the **Chargeable tasks** tab on **Quote line** page, you must manually associate each project.</span></span>

1. <span data-ttu-id="fea43-137">No separador **Geral** de uma linha de proposta baseada em projetos, verifique se existe um projeto selecionado no campo **Projeto**.</span><span class="sxs-lookup"><span data-stu-id="fea43-137">On the **General** tab of a project–based quote line, verify that there is a project selected in the **Project** field.</span></span>
2. <span data-ttu-id="fea43-138">No campo **Tarefas incluídas**, selecione **Apenas tarefas selecionadas**.</span><span class="sxs-lookup"><span data-stu-id="fea43-138">In the **Included tasks** field, select **Selected tasks only**.</span></span>
3. <span data-ttu-id="fea43-139">Guarde a linha de proposta baseada em projetos.</span><span class="sxs-lookup"><span data-stu-id="fea43-139">Save the project-based quote line.</span></span> <span data-ttu-id="fea43-140">Quando o formulário é atualizado, é apresentado o separador **Tarefas Faturáveis**.</span><span class="sxs-lookup"><span data-stu-id="fea43-140">When the form refreshes, the **Chargeable tasks** tab displays.</span></span>
4. <span data-ttu-id="fea43-141">No separador **Tarefas Faturáveis**, selecione **Adicionar uma tarefa de linha de proposta**.</span><span class="sxs-lookup"><span data-stu-id="fea43-141">On the **Chargeable tasks** tab, select **Add a quote line task**.</span></span>
5. <span data-ttu-id="fea43-142">Na página **Tarefa da Linha de Proposta**, no campo **Tarefas**, selecione a tarefa e, no campo **Tipo de faturação**, selecione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="fea43-142">On the **Quote line task** page, in the **Tasks** field, select the task and in the **Billing type** field, select **Save**.</span></span> 
6. <span data-ttu-id="fea43-143">Feche a página.</span><span class="sxs-lookup"><span data-stu-id="fea43-143">Close the page.</span></span> <span data-ttu-id="fea43-144">A tarefa selecionada está agora associada à linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="fea43-144">The selected task is now associated to the quote line.</span></span>

## <a name="disassociate-tasks-from-projectbased-quote-lines"></a><span data-ttu-id="fea43-145">Desassociar tarefas a partir de linhas de proposta baseadas em projetos</span><span class="sxs-lookup"><span data-stu-id="fea43-145">Disassociate tasks from project–based quote lines</span></span>

### <a name="from-the-project-page"></a><span data-ttu-id="fea43-146">A partir da página Projeto</span><span class="sxs-lookup"><span data-stu-id="fea43-146">From the Project page</span></span>

<span data-ttu-id="fea43-147">Este método proporciona a melhor experiência para desassociar as tarefas das linhas de proposta.</span><span class="sxs-lookup"><span data-stu-id="fea43-147">This method provides the most optimal experience for disassociating tasks from quote lines.</span></span> <span data-ttu-id="fea43-148">Pode selecionar várias tarefas e desassociar todas, bem com as respetivas tarefas subordinadas, da linha de proposta selecionada.</span><span class="sxs-lookup"><span data-stu-id="fea43-148">You can select multiple tasks and disassociate all of the them, plus their child tasks, from the selected quote line.</span></span>

1. <span data-ttu-id="fea43-149">No separador **Geral** de uma linha de proposta baseada em projetos, no campo **Projeto**, selecione a ligação do projeto.</span><span class="sxs-lookup"><span data-stu-id="fea43-149">On the **General** tab of a project–based quote line, in the **Project** field, select the project link.</span></span>
2. <span data-ttu-id="fea43-150">Na página **Projeto**, selecione o separador **Faturação de Tarefas**.</span><span class="sxs-lookup"><span data-stu-id="fea43-150">On the **Project** page, select the **Task billing** tab.</span></span>
3. <span data-ttu-id="fea43-151">Na segunda grelha, que se aplica à configuração da faturação específica da tarefa, selecione uma ou mais tarefas e, em seguida, selecione **Desassociar linhas de proposta**.</span><span class="sxs-lookup"><span data-stu-id="fea43-151">In the second grid, which applies to task-specific billing setup, select one or more tasks, and then select **Disassociate quote lines**.</span></span>
4. <span data-ttu-id="fea43-152">Na página de diálogo apresentada, selecione uma linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="fea43-152">In the dialog page that appears, select a quote line.</span></span>
5. <span data-ttu-id="fea43-153">Selecione a caixa de verificação para indicar se a associação também deve ser removida das tarefas subordinadas das tarefas selecionadas.</span><span class="sxs-lookup"><span data-stu-id="fea43-153">Select the check box to indicate whether the association should also be removed from child tasks of the selected tasks.</span></span> <span data-ttu-id="fea43-154">Selecionar a caixa irá desassociar as tarefas subordinadas das tarefas selecionadas à linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="fea43-154">Checking the box will also disassociate the child tasks of the selected tasks to the quote line.</span></span>
6. <span data-ttu-id="fea43-155">Selecione **OK**.</span><span class="sxs-lookup"><span data-stu-id="fea43-155">Select **OK**.</span></span> <span data-ttu-id="fea43-156">Uma mensagem de aviso informa-o de que, se remover esta associação, quaisquer valores reais registados anteriormente na tarefa poderão ser revertidos.</span><span class="sxs-lookup"><span data-stu-id="fea43-156">A warning message informs you that if you remove this association, any actuals previously recorded on the task could be reversed.</span></span> 
7. <span data-ttu-id="fea43-157">Selecione **OK** para continuar e remover a associação entre a tarefa e a linha de proposta baseada em projetos.</span><span class="sxs-lookup"><span data-stu-id="fea43-157">Select **OK** to continue and remove the association between the task and the project-based quote line.</span></span>

### <a name="from-the-quote-line-page"></a><span data-ttu-id="fea43-158">A partir da página Linha de proposta</span><span class="sxs-lookup"><span data-stu-id="fea43-158">From the Quote line page</span></span>

<span data-ttu-id="fea43-159">Também pode desassociar tarefas de projeto de linhas de proposta a partir do separador **Tarefas Faturáveis** na página **Linha de proposta**.</span><span class="sxs-lookup"><span data-stu-id="fea43-159">You can also disassociate project tasks to quote lines from the **Chargeable tasks** tab on **Quote line** page.</span></span>

1. <span data-ttu-id="fea43-160">No separador **Tarefas Faturáveis**, selecione **Eliminar uma tarefa de linha de proposta**.</span><span class="sxs-lookup"><span data-stu-id="fea43-160">On the **Chargeable tasks** tab, select **Delete a quote line task**.</span></span>
2. <span data-ttu-id="fea43-161">Selecione **OK**.</span><span class="sxs-lookup"><span data-stu-id="fea43-161">Select **OK**.</span></span> <span data-ttu-id="fea43-162">Uma mensagem de aviso informa-o de que, se remover esta associação, quaisquer valores reais registados anteriormente na tarefa poderão ser revertidos.</span><span class="sxs-lookup"><span data-stu-id="fea43-162">A warning message informs you that if you remove this association, any actuals previously recorded on the task could be reversed.</span></span> 
3. <span data-ttu-id="fea43-163">Selecione **OK** para continuar e remover a associação entre a tarefa e a linha de proposta baseada em projetos.</span><span class="sxs-lookup"><span data-stu-id="fea43-163">Select **OK** to continue and remove the association between the task and the project-based quote line.</span></span>

>[!NOTE]
> <span data-ttu-id="fea43-164">Este procedimento não elimina a tarefa do projeto.</span><span class="sxs-lookup"><span data-stu-id="fea43-164">This procedure doesn't delete the task from the project.</span></span> <span data-ttu-id="fea43-165">Apenas remove a associação da tarefa da linha de proposta baseada em projetos.</span><span class="sxs-lookup"><span data-stu-id="fea43-165">It only removes the task association from the project-based quote line.</span></span>
