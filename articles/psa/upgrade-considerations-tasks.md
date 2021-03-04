---
title: Considerações sobre atualização para a estrutura hierárquica do trabalho
description: Este tópico fornece informações sobre a atualização da estrutura hierárquica do trabalho do Project Service Automation 2.x para 3.x.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
author: ruhercul
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
ms.openlocfilehash: cea8ce7f61fbc0f0c8c8deb522bc332be102238d
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149557"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a><span data-ttu-id="79b5f-103">Considerações sobre atualização para a estrutura hierárquica do trabalho</span><span class="sxs-lookup"><span data-stu-id="79b5f-103">Upgrade considerations for the work breakdown structure</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="79b5f-104">Este tópico fornece informações sobre a atualização da estrutura hierárquica do trabalho do Project Service Automation 2.x para 3.x.</span><span class="sxs-lookup"><span data-stu-id="79b5f-104">This topic provides information about upgrading the work breakdown structure from Project Service Automation 2.x to 3.x.</span></span> <span data-ttu-id="79b5f-105">Este tópico define o estado de funcionamento de um projeto no Project Service Automation (PSA) necessário para uma atualização bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="79b5f-105">This topic defines the healthy state of a project in Project Service Automation (PSA) that is required for a successful upgrade.</span></span> <span data-ttu-id="79b5f-106">Há também informações sobre as condições de bloqueio comuns que causarão falhas na atualização.</span><span class="sxs-lookup"><span data-stu-id="79b5f-106">There is also information about the common blocking conditions that will cause upgrade to fail.</span></span> <span data-ttu-id="79b5f-107">Para obter mais informações sobre como definir tarefas do projeto e as suas funções numa agenda do projeto, consulte [Agendas do projeto](project-creating.md).</span><span class="sxs-lookup"><span data-stu-id="79b5f-107">For more information about defining project tasks and their functions within a project schedule, see [Project schedules](project-creating.md).</span></span>

## <a name="key-entities"></a><span data-ttu-id="79b5f-108">Entidades principais</span><span class="sxs-lookup"><span data-stu-id="79b5f-108">Key entities</span></span>
<span data-ttu-id="79b5f-109">Para uma estrutura hierárquica do trabalho precisa que já esteja carregada com recursos, são necessárias as seguintes entidades:</span><span class="sxs-lookup"><span data-stu-id="79b5f-109">For an accurate work breakdown structure that is already loaded with resources, the following entities are required:</span></span>

- [<span data-ttu-id="79b5f-110">Projeto</span><span class="sxs-lookup"><span data-stu-id="79b5f-110">Project</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)
- [<span data-ttu-id="79b5f-111">Equipa do Projeto</span><span class="sxs-lookup"><span data-stu-id="79b5f-111">Project Team</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)
- [<span data-ttu-id="79b5f-112">Tarefa de Projeto</span><span class="sxs-lookup"><span data-stu-id="79b5f-112">Project Task</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)
- [<span data-ttu-id="79b5f-113">Atribuições de Recursos</span><span class="sxs-lookup"><span data-stu-id="79b5f-113">Resource Assignments</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)
- [<span data-ttu-id="79b5f-114">Dependência de Tarefa de Projeto</span><span class="sxs-lookup"><span data-stu-id="79b5f-114">Project Task Dependency</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)
- [<span data-ttu-id="79b5f-115">Recursos Reserváveis</span><span class="sxs-lookup"><span data-stu-id="79b5f-115">Bookable Resources</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/bookableresource)

<span data-ttu-id="79b5f-116">Para definir uma estrutura hierárquica do trabalho carregada por recurso, deve concluir os seguintes passos:</span><span class="sxs-lookup"><span data-stu-id="79b5f-116">To define a resource loaded work breakdown structure, you must complete the following steps:</span></span>

1. <span data-ttu-id="79b5f-117">Crie um projeto.</span><span class="sxs-lookup"><span data-stu-id="79b5f-117">Create a new project.</span></span> <span data-ttu-id="79b5f-118">Para obter mais informações sobre como criar um projeto, consulte [msdyn_project](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).</span><span class="sxs-lookup"><span data-stu-id="79b5f-118">For more information about how to create a new project, see [msdyn_project](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).</span></span>
2. <span data-ttu-id="79b5f-119">Crie uma ou mais tarefas.</span><span class="sxs-lookup"><span data-stu-id="79b5f-119">Create one or more tasks.</span></span> <span data-ttu-id="79b5f-120">Para obter mais informações sobre como criar uma tarefa, consulte [msdyn_projecttask](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).</span><span class="sxs-lookup"><span data-stu-id="79b5f-120">For more information about how to create a task, see [msdyn_projecttask](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).</span></span>
3. <span data-ttu-id="79b5f-121">Defina as dependências da tarefa.</span><span class="sxs-lookup"><span data-stu-id="79b5f-121">Define the task dependencies.</span></span> <span data-ttu-id="79b5f-122">Para mais informações, consulte [Dependência de Tarefas do Projeto](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).</span><span class="sxs-lookup"><span data-stu-id="79b5f-122">For more information, see [Project Task Dependency](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).</span></span>
4. <span data-ttu-id="79b5f-123">Atribua membros da equipa do projeto ao projeto.</span><span class="sxs-lookup"><span data-stu-id="79b5f-123">Assign project team members to the project.</span></span> <span data-ttu-id="79b5f-124">Para obter mais informações, consulte [msdyn_projectteam](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).</span><span class="sxs-lookup"><span data-stu-id="79b5f-124">For more information, see [msdyn_projectteam](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).</span></span>
5. <span data-ttu-id="79b5f-125">Atribua membros da equipa do projeto às tarefas.</span><span class="sxs-lookup"><span data-stu-id="79b5f-125">Assign project team members to the tasks.</span></span> <span data-ttu-id="79b5f-126">Para obter mais informações, consulte [msdyn_resourceassignment](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).</span><span class="sxs-lookup"><span data-stu-id="79b5f-126">For more information, see [msdyn_resourceassignment](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).</span></span>

## <a name="project-team-relationships"></a><span data-ttu-id="79b5f-127">Relações da equipa do projeto</span><span class="sxs-lookup"><span data-stu-id="79b5f-127">Project team relationships</span></span>

<span data-ttu-id="79b5f-128">Para garantir uma atualização bem-sucedida, as seguintes relações devem ser mantidas corretamente:</span><span class="sxs-lookup"><span data-stu-id="79b5f-128">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>
- <span data-ttu-id="79b5f-129">Todos os membros da equipa do projeto devem estar associados a um recurso reservável.</span><span class="sxs-lookup"><span data-stu-id="79b5f-129">All project team members must be associated with a bookable resource.</span></span>
- <span data-ttu-id="79b5f-130">Todos os membros da equipa do projeto devem estar associados ao mesmo projeto.</span><span class="sxs-lookup"><span data-stu-id="79b5f-130">All project team members must be associated with the same project.</span></span> 

## <a name="project-task-relationships"></a><span data-ttu-id="79b5f-131">Relações de tarefas do projeto</span><span class="sxs-lookup"><span data-stu-id="79b5f-131">Project task relationships</span></span>
<span data-ttu-id="79b5f-132">Para garantir uma atualização bem-sucedida, as seguintes relações devem ser mantidas corretamente:</span><span class="sxs-lookup"><span data-stu-id="79b5f-132">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="79b5f-133">Todas as tarefas relacionadas devem ser associadas ao mesmo projeto.</span><span class="sxs-lookup"><span data-stu-id="79b5f-133">Any related tasks must be associated with the same project.</span></span>
- <span data-ttu-id="79b5f-134">Todas as tarefas de linha devem ter uma tarefa principal.</span><span class="sxs-lookup"><span data-stu-id="79b5f-134">Every line task must have a parent task.</span></span>
- <span data-ttu-id="79b5f-135">Todas as tarefas devem ter um projeto principal.</span><span class="sxs-lookup"><span data-stu-id="79b5f-135">Every task must have a parent project.</span></span>

### <a name="valid-conditions"></a><span data-ttu-id="79b5f-136">Condições válidas</span><span class="sxs-lookup"><span data-stu-id="79b5f-136">Valid conditions</span></span>

- <span data-ttu-id="79b5f-137">Todas as durações de tarefa devem ser maiores ou iguais a (>=) uma hora e inferiores a 1.800.000 minutos (1250 dias).\*</span><span class="sxs-lookup"><span data-stu-id="79b5f-137">All task durations must be greater than or equal to (>=) one hour and less than 1,800,000 minutes (1,250 days).\*</span></span>
- <span data-ttu-id="79b5f-138">Todas as tarefas devem ter uma data de início não anterior a 2000/01/01.\*</span><span class="sxs-lookup"><span data-stu-id="79b5f-138">All tasks must have a start date no earlier than 2000/01/01.\*</span></span>
- <span data-ttu-id="79b5f-139">Todas as tarefas devem ter uma data de início, de no máximo 17 anos a partir do dia atual.\*</span><span class="sxs-lookup"><span data-stu-id="79b5f-139">All tasks must have a start date no later than 17 years from the present day.\*</span></span>
- <span data-ttu-id="79b5f-140">Todas as tarefas devem ter uma data de início anterior ou igual à data de conclusão.</span><span class="sxs-lookup"><span data-stu-id="79b5f-140">All tasks must have a start date earlier or equal to their finish date.</span></span>
- <span data-ttu-id="79b5f-141">Todos os tipos de transação nas classificações (Despesa, Material, Imposto e Tempo) devem ter valores para **Unidade Predefinida** e **Grupo de Unidades**.</span><span class="sxs-lookup"><span data-stu-id="79b5f-141">All transaction types on classifications (Expense, Material, Tax, and Time) must have values for **Default Unit** and **Unit Group**.</span></span>
- <span data-ttu-id="79b5f-142">Os formatos de data com letras devem ser evitados.</span><span class="sxs-lookup"><span data-stu-id="79b5f-142">Date formats with letters should be avoided.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="79b5f-143">Passos potenciais de mitigação</span><span class="sxs-lookup"><span data-stu-id="79b5f-143">Potential mitigation steps</span></span>
- <span data-ttu-id="79b5f-144">Utilize a Localização Avançada para identificar tarefas de Projeto que não contenham um ID de Projeto.</span><span class="sxs-lookup"><span data-stu-id="79b5f-144">Use Advanced Find to identify Project tasks that do not contain a Project ID.</span></span>
- <span data-ttu-id="79b5f-145">Utilize a Localização Avançada para identificar tarefas de Projeto em que a duração agendada seja superior a > 1.800.000.</span><span class="sxs-lookup"><span data-stu-id="79b5f-145">Use Advanced Find to identify Project tasks where the scheduled duration is greater than > 1,800,000.</span></span>
- <span data-ttu-id="79b5f-146">Antes de efetuar alterações a dados, deve investigar eventuais personalizações associadas à entidade que poderão ter levado à obtenção dos dados num estado incorreto.</span><span class="sxs-lookup"><span data-stu-id="79b5f-146">Prior to making any data changes, you should investigate any customizations associated with the entity that may have led to getting the data into a bad state.</span></span> <span data-ttu-id="79b5f-147">Estas personalizações devem ser resolvidas antes de prosseguir com quaisquer atualizações relacionadas com os dados.</span><span class="sxs-lookup"><span data-stu-id="79b5f-147">These customizations should be addressed before proceeding with any data-related updates.</span></span>
- <span data-ttu-id="79b5f-148">Para as tarefas identificadas que ficaram órfãs, considere a possibilidade de eliminar estas tarefas se não forem necessárias ou se elas tiverem de ser associadas ao projeto principal correto.</span><span class="sxs-lookup"><span data-stu-id="79b5f-148">For the identified tasks that have been orphaned, consider deleting these tasks if they are not needed or if they should be associated with the correct parent project.</span></span>
- <span data-ttu-id="79b5f-149">Para qualquer tarefa na qual a duração seja superior a 1.250 dias, considere adicionar várias tarefas para representar a duração total, se possível.</span><span class="sxs-lookup"><span data-stu-id="79b5f-149">For any tasks where the duration is greater than 1,250 days, consider adding multiple tasks to represent the total duration, if feasible.</span></span>

> [!NOTE]
> <span data-ttu-id="79b5f-150">Os itens anotados com um asterisco (\*) têm limites porque a gestão das relações com os clientes (CRM) oferece suporte a apenas 7320 expansões de recorrência.</span><span class="sxs-lookup"><span data-stu-id="79b5f-150">Items noted with an asterisk (\*) have limits that are due to the fact that customer relationship management (CRM) supports only 7,320 recurrence expansions.</span></span> <span data-ttu-id="79b5f-151">Deve permanecer abaixo deste limite.</span><span class="sxs-lookup"><span data-stu-id="79b5f-151">You must stay below this limit.</span></span>

## <a name="resource-assignment-relationships"></a><span data-ttu-id="79b5f-152">Relações de Atribuição de Recursos</span><span class="sxs-lookup"><span data-stu-id="79b5f-152">Resource Assignment relationships</span></span>
<span data-ttu-id="79b5f-153">Para garantir uma atualização bem-sucedida, as seguintes relações devem ser mantidas corretamente:</span><span class="sxs-lookup"><span data-stu-id="79b5f-153">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="79b5f-154">Todas as Atribuições de Recursos numa estrutura hierárquica do trabalho devem estar relacionadas com o mesmo projeto.</span><span class="sxs-lookup"><span data-stu-id="79b5f-154">All Resource Assignments in a work breakdown structure must be related to the same project.</span></span>
- <span data-ttu-id="79b5f-155">Todas as Atribuições de Recursos numa estrutura hierárquica do trabalho devem ser associadas aos membros da equipa do projeto no mesmo projeto.</span><span class="sxs-lookup"><span data-stu-id="79b5f-155">All Resource Assignments in a work breakdown structure must be associated to project team members in the same project.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="79b5f-156">Passos potenciais de mitigação</span><span class="sxs-lookup"><span data-stu-id="79b5f-156">Potential mitigation steps</span></span>
- <span data-ttu-id="79b5f-157">Identifique todas as tarefas que estejam fora das condições descritas acima.</span><span class="sxs-lookup"><span data-stu-id="79b5f-157">Identify all tasks that fall outside the conditions described above.</span></span>  
- <span data-ttu-id="79b5f-158">Todas as Atribuições de Recursos que já não sejam válidas devem ser eliminadas.</span><span class="sxs-lookup"><span data-stu-id="79b5f-158">Any Resource Assignments that are no longer valid should be deleted.</span></span>

## <a name="project-task-dependency-relationships"></a><span data-ttu-id="79b5f-159">Relações de dependência de tarefas do projeto</span><span class="sxs-lookup"><span data-stu-id="79b5f-159">Project task dependency relationships</span></span>
<span data-ttu-id="79b5f-160">Para garantir uma atualização bem-sucedida, as seguintes relações devem ser mantidas corretamente:</span><span class="sxs-lookup"><span data-stu-id="79b5f-160">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="79b5f-161">Todas as dependências de tarefa do projeto devem estar relacionadas com o mesmo projeto.</span><span class="sxs-lookup"><span data-stu-id="79b5f-161">All project task dependencies must be related to the same project.</span></span>
- <span data-ttu-id="79b5f-162">Uma tarefa não pode ter a mesma dependência referenciada mais de uma vez.</span><span class="sxs-lookup"><span data-stu-id="79b5f-162">A task can't have the same dependency referenced more than once.</span></span>
