---
title: Como atribuir um recurso reservável a uma tarefa na aplicação Web
description: Uma descrição geral das maneiras pelas quais pode atribuir recursos reserváveis.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 32a04ddef901515cd77262b5ae6be2458cb6b00c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993321"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a><span data-ttu-id="c5f1f-103">Como atribuir um recurso reservável a uma tarefa na aplicação Web (aplicação Project Service v2.x)?</span><span class="sxs-lookup"><span data-stu-id="c5f1f-103">How do I assign a bookable resource to a task in the web app (Project Service app v2.x)?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="c5f1f-104">Existem duas formas de atribuir um recurso a uma tarefa no Project Service.</span><span class="sxs-lookup"><span data-stu-id="c5f1f-104">There are two ways to assign a resource to a task in Project Service.</span></span> <span data-ttu-id="c5f1f-105">Pode reservar um recurso como um membro da equipa e, em seguida, atribui-lo a uma tarefa</span><span class="sxs-lookup"><span data-stu-id="c5f1f-105">You can book a resource as a team member and then assign it to a task.</span></span> <span data-ttu-id="c5f1f-106">Alternativamente, pode criar um membro da equipa genérico através de atribuição de função de tarefas, gerar uma equipa e, em seguida, cumprir os requisitos de cópia de segurança com um recurso nomeado.</span><span class="sxs-lookup"><span data-stu-id="c5f1f-106">Or, you can create a generic team member through role assignment on tasks, generate a team, and then fulfill the backing requirements with a named resource.</span></span>

<span data-ttu-id="c5f1f-107">Tenha em atenção que se pretende atribuir um recurso reservável a uma tarefa, membro da equipa do recurso reservável tem de ter reservas disponíveis suficientes.</span><span class="sxs-lookup"><span data-stu-id="c5f1f-107">Note that if you’d like to assign a bookable resource to a task, the bookable resource team member must have enough available bookings.</span></span> <span data-ttu-id="c5f1f-108">O estado da reserva tem de ser Tipo de Submissão Reserva Forçada e em estado Submetida.</span><span class="sxs-lookup"><span data-stu-id="c5f1f-108">The status of the booking must be Commit Type Hard Book and Status Committed.</span></span> <span data-ttu-id="c5f1f-109">Se existirem reservas suficientes para o recurso, o Project Service remove a atribuição e apresenta a seguinte mensagem de erro:</span><span class="sxs-lookup"><span data-stu-id="c5f1f-109">If there aren’t enough bookings for the resource, Project Service removes the assignment and displays the following error message:</span></span>

<span data-ttu-id="c5f1f-110">*Não é possível atribuir recursos à tarefa – os seguintes recursos não têm horas suficientes reservadas para o projeto*</span><span class="sxs-lookup"><span data-stu-id="c5f1f-110">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project*</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="c5f1f-111">Reservd um recurso como um membro da equipa e, em seguida, atribua o recurso a uma tarefa</span><span class="sxs-lookup"><span data-stu-id="c5f1f-111">Book a resource as a team member and then assign the resource to a task</span></span>

<span data-ttu-id="c5f1f-112">Com este método, adiciona um recurso à equipa do projeto e, em seguida, atribui tarefas ao recurso na agenda do projeto.</span><span class="sxs-lookup"><span data-stu-id="c5f1f-112">With this method you add a resource to the project team and then assign tasks to the resource in the project schedule.</span></span> <span data-ttu-id="c5f1f-113">Eis como fazê-lo:</span><span class="sxs-lookup"><span data-stu-id="c5f1f-113">Here’s how you do this:</span></span>
1.  <span data-ttu-id="c5f1f-114">Na grelha de membro da equipa, adicione um membro da equipa novo selecionando **Novo**.</span><span class="sxs-lookup"><span data-stu-id="c5f1f-114">On the team member grid, add a new team member by selecting **New**.</span></span>
2.  <span data-ttu-id="c5f1f-115">No ecrã Criação Rápida de Membro da Equipa, selecione o nome de recurso reservável e defina uma função.</span><span class="sxs-lookup"><span data-stu-id="c5f1f-115">On the Team Member Quick Create screen, select the bookable resource name and set a role.</span></span>
3.  <span data-ttu-id="c5f1f-116">Selecione as datas **De** e **Para**.</span><span class="sxs-lookup"><span data-stu-id="c5f1f-116">Select the **From** and **To** dates.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="c5f1f-117">![Captura de ecrã da adição de membro da equipa](media/FAQ-Resources-to-Tasks2-1.png "Captura de ecrã da adição de membro da equipa")</span><span class="sxs-lookup"><span data-stu-id="c5f1f-117">![Screenshot of adding team member](media/FAQ-Resources-to-Tasks2-1.png "Screenshot of adding team member")</span></span>
 
4.  <span data-ttu-id="c5f1f-118">Escolha um dos seguintes métodos de alocação para o agendamento do recurso:</span><span class="sxs-lookup"><span data-stu-id="c5f1f-118">Select one of the following allocation methods for booking the resource:</span></span>
    - <span data-ttu-id="c5f1f-119">**Capacidade Total** reserva a capacidade total do recurso para as datas de e para especificadas.</span><span class="sxs-lookup"><span data-stu-id="c5f1f-119">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="c5f1f-120">**Capacidade de Percentagem** reserva o recurso para a percentagem de capacidade do recurso para as datas de e para especificadas.</span><span class="sxs-lookup"><span data-stu-id="c5f1f-120">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="c5f1f-121">**Distribuir Igualmente por Horas** reserva o recurso para um número especificado de horas distribuindo-as uniformemente por dia ao longo das datas de e para especificadas.</span><span class="sxs-lookup"><span data-stu-id="c5f1f-121">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing it evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="c5f1f-122">**Carregamento no Início Por Horas** reserva o recurso para um número especificado de horas carregando inicialmente as horas por dia ao longo das datas de e para especificadas.</span><span class="sxs-lookup"><span data-stu-id="c5f1f-122">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>

    <span data-ttu-id="c5f1f-123">Não selecione **Nenhum** porque adiciona o recurso à equipa do projeto, mas não cria quaisquer reservas que absorvam a capacidade do recurso.</span><span class="sxs-lookup"><span data-stu-id="c5f1f-123">Don’t select **None** because it adds the resource to the team but doesn’t create any bookings that absorb the resource's capacity.</span></span>
5.  <span data-ttu-id="c5f1f-124">Selecione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="c5f1f-124">Select **Save**.</span></span>

    <span data-ttu-id="c5f1f-125">Tenha em atenção que as horas da reserva têm de ser suficientes para abranger as horas de esforço e os intervalos de datas das tarefas a que atribui este recurso.</span><span class="sxs-lookup"><span data-stu-id="c5f1f-125">Note that the hours of the booking must be enough to cover the effort hours and date ranges of the tasks that you assign this resource to.</span></span> <span data-ttu-id="c5f1f-126">Se não estiverem em alinhamento, não pode atribuir o recurso para a tarefa.</span><span class="sxs-lookup"><span data-stu-id="c5f1f-126">If they aren’t in alignment, you can’t assign the resource to the task.</span></span>

6.  <span data-ttu-id="c5f1f-127">Na estrutura hierárquica do trabalho (WBS) para a tarefa, clique no menu suspenso da célula do recurso.</span><span class="sxs-lookup"><span data-stu-id="c5f1f-127">On the work breakdown structure (WBS) for the task, click the resource cell dropdown.</span></span> <span data-ttu-id="c5f1f-128">Então:</span><span class="sxs-lookup"><span data-stu-id="c5f1f-128">Then:</span></span> 

    1. <span data-ttu-id="c5f1f-129">Selecione **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="c5f1f-129">Select **Add**.</span></span>
    2. <span data-ttu-id="c5f1f-130">Selecione o menu suspenso em **Recursos** e selecione o membro da equipa que adicionou acima.</span><span class="sxs-lookup"><span data-stu-id="c5f1f-130">Select the dropdown under **Resources** and select the team member you added above.</span></span>
    3. <span data-ttu-id="c5f1f-131">Selecione **OK**.</span><span class="sxs-lookup"><span data-stu-id="c5f1f-131">Select **OK**.</span></span> <span data-ttu-id="c5f1f-132">Agora, o membro da equipa está atribuído à tarefa.</span><span class="sxs-lookup"><span data-stu-id="c5f1f-132">The team member is now assigned to the task.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="c5f1f-133">![Captura de ecrã da adição de recursos com WBS](media/FAQ-Resources-to-Tasks2-2.png "Captura de ecrã da adição de recursos com WBS")</span><span class="sxs-lookup"><span data-stu-id="c5f1f-133">![Screenshot of adding resources with WBS](media/FAQ-Resources-to-Tasks2-2.png "Screenshot of adding resources with WBS")</span></span>
 
<span data-ttu-id="c5f1f-134">Na grelha de membro da equipa, verá o agregado das horas atribuídas ao recurso em Horas Atribuídas.</span><span class="sxs-lookup"><span data-stu-id="c5f1f-134">On the team member grid, you’ll see the aggregate of the resource’s assigned hours under Assigned Hours.</span></span> <span data-ttu-id="c5f1f-135">Serão menos ou iguais às horas reservadas para o recurso.</span><span class="sxs-lookup"><span data-stu-id="c5f1f-135">It will be less than or equal to the booked hours for the resource.</span></span> 

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="c5f1f-136">![Captura de ecrã das horas atribuídas a um recurso](media/FAQ-Resources-to-Tasks2-3.png "Captura de ecrã das horas atribuídas a um recurso")</span><span class="sxs-lookup"><span data-stu-id="c5f1f-136">![Screenshot of assigned hours for a resource](media/FAQ-Resources-to-Tasks2-3.png "Screenshot of assigned hours for a resource")</span></span>
 
<span data-ttu-id="c5f1f-137">Se a tarefa que estiver a tentar atribuir ao recurso iniciar após a data de fim das reservas dos recursos, o recurso não aparecerá no menu suspenso.</span><span class="sxs-lookup"><span data-stu-id="c5f1f-137">If the task you’re attempting to assign to the resource starts after the end date of the resources bookings, the resource won’t appear in the dropdown.</span></span>

<span data-ttu-id="c5f1f-138">Tenha em atenção que pode atribuir um recurso a mais horas do que as respetivas horas reservadas se o recurso tiver alguma capacidade restante não atribuída.</span><span class="sxs-lookup"><span data-stu-id="c5f1f-138">Note that you can assign a resource to more hours than their booked hours if the resource has some remaining unassigned capacity.</span></span> <span data-ttu-id="c5f1f-139">Neste caso, o recurso será apenas parcialmente atribuído até às reservas.</span><span class="sxs-lookup"><span data-stu-id="c5f1f-139">In this case the resource will only be partially assigned up to their bookings.</span></span> <span data-ttu-id="c5f1f-140">Pode ver estas horas tarefas nãos atribuídas restantes adicionando a coluna de Horas com Falta de Recursos à estrutura hierárquica do trabalho.</span><span class="sxs-lookup"><span data-stu-id="c5f1f-140">You can see these remaining unassigned task hours by adding the Unstaffed Hours column to the work breakdown structure.</span></span>

<span data-ttu-id="c5f1f-141">Se os recursos são atribuídos às respetivas horas reservadas (as respetivas horas reservadas são iguais às suas horas atribuídas), verá a seguinte mensagem de erro ao tentar atribuir-lhes mais tarefas:</span><span class="sxs-lookup"><span data-stu-id="c5f1f-141">If resources are assigned to their booked hours (their booked hours equals their assigned hours), you’ll see the following error message when you attempt to assign them further tasks:</span></span>

<span data-ttu-id="c5f1f-142">*Não é possível atribuir recursos à tarefa – os seguintes recursos não têm horas suficientes reservadas para o projeto.*</span><span class="sxs-lookup"><span data-stu-id="c5f1f-142">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project.*</span></span>

<span data-ttu-id="c5f1f-143">Além disso, o membro da equipa gestor do projeto predefinido que é adicionado à equipa quando cria o projeto é adicionado sem quaisquer reservas e não pode ser atribuído a qualquer tarefa.</span><span class="sxs-lookup"><span data-stu-id="c5f1f-143">Additionally, the default project manager team member that is added to the team when you create the project is added without any bookings and can’t be assigned to any task.</span></span> <span data-ttu-id="c5f1f-144">Eles não aparecerão no menu suspenso de recursos para tarefas.</span><span class="sxs-lookup"><span data-stu-id="c5f1f-144">They won’t show up in the resource dropdown for tasks.</span></span>

<span data-ttu-id="c5f1f-145">Se pretender atribuir este recurso, será necessário removê-las da equipa e adicioná-las novamente com um método de alocação diferente de Nenhum.</span><span class="sxs-lookup"><span data-stu-id="c5f1f-145">If you want to assign this resource, you need to remove them from the team and then re-add them with an allocation method other than None.</span></span> <span data-ttu-id="c5f1f-146">A razão pela qual são adicionados à equipa aquando da criação do projeto é para que um projeto tenha, pelo menos, uma aprovador de projeto por predefinição.</span><span class="sxs-lookup"><span data-stu-id="c5f1f-146">The reason they’re added to the team when the project is created is so that a project has at least one project approver by default.</span></span>

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a><span data-ttu-id="c5f1f-147">Criar um membro da equipa genérico através de atribuição de funções em tarefas</span><span class="sxs-lookup"><span data-stu-id="c5f1f-147">Create a generic team member through role assignment on tasks</span></span>

<span data-ttu-id="c5f1f-148">Este método assegura que os recursos têm reservas suficientes para tarefas.</span><span class="sxs-lookup"><span data-stu-id="c5f1f-148">This method assures that resources have enough bookings for tasks.</span></span> <span data-ttu-id="c5f1f-149">Em primeiro lugar, cria um marcador de posição ou recurso genérico que descreve as características do recurso nomeado que, em última análise, pretende que trabalhe nas tarefas ao gerar uma equipa depois de atribuir funções a tarefas.</span><span class="sxs-lookup"><span data-stu-id="c5f1f-149">First, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks by generating a team after assigning roles to tasks.</span></span> <span data-ttu-id="c5f1f-150">Eis como fazê-lo:</span><span class="sxs-lookup"><span data-stu-id="c5f1f-150">Here’s how you do this:</span></span>

1. <span data-ttu-id="c5f1f-151">Na estrutura hierárquica do trabalho, selecione uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="c5f1f-151">On the work breakdown structure, select a task.</span></span>
2. <span data-ttu-id="c5f1f-152">Selecione o ícone do menu suspenso **Função Atribuída** na célula do recurso.</span><span class="sxs-lookup"><span data-stu-id="c5f1f-152">Select the **Assigned Role** dropdown icon in the resource cell.</span></span>
3. <span data-ttu-id="c5f1f-153">Selecione o menu suspenso **Função** e selecione a função para o recurso genérico.</span><span class="sxs-lookup"><span data-stu-id="c5f1f-153">Select the **Role** dropdown and select the role for the generic resource.</span></span>
4. <span data-ttu-id="c5f1f-154">Selecione **OK**.</span><span class="sxs-lookup"><span data-stu-id="c5f1f-154">Select **OK**.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="c5f1f-155">![Captura de ecrã da utilização de WBS para adicionar recurso](media/FAQ-Resources-to-Tasks2-4.png "Captura de ecrã da utilização de WBS para adicionar recurso")</span><span class="sxs-lookup"><span data-stu-id="c5f1f-155">![Screenshot of using WBS to add resource](media/FAQ-Resources-to-Tasks2-4.png "Screenshot of using WBS to add resource")</span></span>
 
<span data-ttu-id="c5f1f-156">Quando tiver concluído a atribuição de funções às tarefas no WBS, selecione **Gerar Equipa do Projeto**.</span><span class="sxs-lookup"><span data-stu-id="c5f1f-156">Once you’ve completed assigning roles to the tasks in the WBS, select **Generate Project Team**.</span></span> <span data-ttu-id="c5f1f-157">O Project Service cria a quantidade mínima de membros da equipa genéricos com base nas funções, unidades de organização e calendário do projeto ao agregar as atribuições de tarefas.</span><span class="sxs-lookup"><span data-stu-id="c5f1f-157">Project Service creates the minimum number of generic team members based on the roles, resourcing organization units, and project calendar by aggregating the task assignments.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="c5f1f-158">![Captura de ecrã da geração da equipa do projeto](media/FAQ-Resources-to-Tasks2-5.png "Captura de ecrã da geração da equipa do projeto")</span><span class="sxs-lookup"><span data-stu-id="c5f1f-158">![Screenshot of generating project team](media/FAQ-Resources-to-Tasks2-5.png "Screenshot of generating project team")</span></span>
 
<span data-ttu-id="c5f1f-159">Na grelha Membro da Equipa, verá recursos do tipo Recurso Genérico com o nome da função e posição.</span><span class="sxs-lookup"><span data-stu-id="c5f1f-159">On the Team Member grid, you’ll see resources of the Generic Resource type with the role and position name.</span></span> <span data-ttu-id="c5f1f-160">Se forem necessários dois recursos para uma função concluir o trabalho, a funcionalidade Gerar Equipa cria dois membros da equipa e utiliza o nome de posição para os diferenciar.</span><span class="sxs-lookup"><span data-stu-id="c5f1f-160">If two resources are needed for a role to complete the work, the Generate Team feature creates two team members and uses position name to set them apart.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="c5f1f-161">![Captura de ecrã da adição de dois recursos genéricos](media/FAQ-Resources-to-Tasks2-6.png "Captura de ecrã da adição de dois recursos genéricos")</span><span class="sxs-lookup"><span data-stu-id="c5f1f-161">![Screenshot of adding two generic resources](media/FAQ-Resources-to-Tasks2-6.png "Screenshot of adding two generic resources")</span></span>
 
<span data-ttu-id="c5f1f-162">Pode abrir o requisito de recursos de cópia de segurança do membro da equipa genérico selecionando a ligação em Requisito de Recurso.</span><span class="sxs-lookup"><span data-stu-id="c5f1f-162">You can open the backing resource requirement for the generic team member by selecting the link under Resource Requirement.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="c5f1f-163">![Captura de ecrã da abertura de suporte do requisito de recurso](media/FAQ-Resources-to-Tasks2-7.png "Captura de ecrã da abertura de suporte do requisito de recurso")</span><span class="sxs-lookup"><span data-stu-id="c5f1f-163">![Screenshot of opening backing resource requirement](media/FAQ-Resources-to-Tasks2-7.png "Screenshot of opening backing resource requirement")</span></span>

<span data-ttu-id="c5f1f-164">Selecione **Reservar** para o recurso genérico e, em seguida, pode utilizar o quadro da agenda para localizar e reservar um recurso real.</span><span class="sxs-lookup"><span data-stu-id="c5f1f-164">Select **Book** for the generic resource, and then you can use the schedule board to find and book a real resource.</span></span> <span data-ttu-id="c5f1f-165">Também é possível enviar o requisito para preenchimento por um gestor de recursos selecionando **Enviar Pedido**.</span><span class="sxs-lookup"><span data-stu-id="c5f1f-165">You can also submit the requirement for fulfillment by a resource manager by selecting **Submit Request**.</span></span>

<span data-ttu-id="c5f1f-166">Quando o recurso genérico é preenchido com um recurso nomeado, o recurso genérico é removido da equipa e as atribuições de tarefas para o recurso genérico são atribuídas ao recurso nomeado que preencheu o requisito de recurso genérico do recurso.</span><span class="sxs-lookup"><span data-stu-id="c5f1f-166">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>
 



[!INCLUDE[footer-include](../includes/footer-banner.md)]