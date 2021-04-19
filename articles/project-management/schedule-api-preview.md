---
title: Utilizar APIs de Agenda para realizar operações com entidades de agendamento
description: Este tópico fornece informações e amostras para a utilização de APIs de agenda.
author: sigitac
manager: Annbe
ms.date: 04/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a50a2c6220bb49de8146d0758019827e120e0526
ms.sourcegitcommit: 8ff9fe396db6dec581c21cd6bb9acc2691c815b0
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/07/2021
ms.locfileid: "5868143"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="44298-103">Utilizar APIs de Agenda para realizar operações com entidades de agendamento</span><span class="sxs-lookup"><span data-stu-id="44298-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="44298-104">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="44298-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="44298-105">Algumas ou todas as funcionalidades anotadas neste tópico estão disponíveis como parte de uma versão de pré-visualização.</span><span class="sxs-lookup"><span data-stu-id="44298-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="44298-106">O conteúdo e a funcionalidade estão sujeitos a alterações.</span><span class="sxs-lookup"><span data-stu-id="44298-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="44298-107">Entidades de agendamento</span><span class="sxs-lookup"><span data-stu-id="44298-107">Scheduling entities</span></span>

<span data-ttu-id="44298-108">Agendar APIs fornece a capacidade de executar operações de criar, atualizar e apagar com **Entidades de agendamento**.</span><span class="sxs-lookup"><span data-stu-id="44298-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="44298-109">Estas entidades são geridas através do motor de Agendamento em Projeto para a web.</span><span class="sxs-lookup"><span data-stu-id="44298-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="44298-110">Operações de Criar, atualizar e apagar com **Entidades de agendamento** foram restringidas em lançamentos Dynamics 365 Project Operations anteriores.</span><span class="sxs-lookup"><span data-stu-id="44298-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="44298-111">A tabela seguinte apresenta uma lista completa das **Entidades de Agendamento**.</span><span class="sxs-lookup"><span data-stu-id="44298-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="44298-112">Nome da entidade</span><span class="sxs-lookup"><span data-stu-id="44298-112">Entity name</span></span>  | <span data-ttu-id="44298-113">Nome lógico da entidade</span><span class="sxs-lookup"><span data-stu-id="44298-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="44298-114">Project</span><span class="sxs-lookup"><span data-stu-id="44298-114">Project</span></span> | <span data-ttu-id="44298-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="44298-115">msdyn_project</span></span> |
| <span data-ttu-id="44298-116">Tarefa de Projeto</span><span class="sxs-lookup"><span data-stu-id="44298-116">Project Task</span></span>  | <span data-ttu-id="44298-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="44298-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="44298-118">Dependência de Tarefa de Projeto</span><span class="sxs-lookup"><span data-stu-id="44298-118">Project Task Dependency</span></span>  | <span data-ttu-id="44298-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="44298-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="44298-120">Atribuição de Recurso</span><span class="sxs-lookup"><span data-stu-id="44298-120">Resource Assignment</span></span> | <span data-ttu-id="44298-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="44298-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="44298-122">Registo do Projeto</span><span class="sxs-lookup"><span data-stu-id="44298-122">Project Bucket</span></span>  | <span data-ttu-id="44298-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="44298-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="44298-124">Membro da Equipa do Projeto</span><span class="sxs-lookup"><span data-stu-id="44298-124">Project Team Member</span></span> | <span data-ttu-id="44298-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="44298-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="44298-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="44298-126">OperationSet</span></span>

<span data-ttu-id="44298-127">OperationSet é um padrão de unidade de trabalho que pode ser usado quando vários pedidos de impacto de programação devem ser processados dentro de uma transação.</span><span class="sxs-lookup"><span data-stu-id="44298-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="44298-128">ApIs de agenda</span><span class="sxs-lookup"><span data-stu-id="44298-128">Schedule APIs</span></span>

<span data-ttu-id="44298-129">Segue-se uma lista das APIs de agenda.</span><span class="sxs-lookup"><span data-stu-id="44298-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="44298-130">**msdyn_CreateProjectV1**: Esta API pode ser usada para criar um projeto.</span><span class="sxs-lookup"><span data-stu-id="44298-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="44298-131">O projeto e registo de projeto padrão é criado imediatamente.</span><span class="sxs-lookup"><span data-stu-id="44298-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="44298-132">**msdyn_CreateTeamMemberV1**: Esta API pode ser usada para criar um membro da equipa de projeto.</span><span class="sxs-lookup"><span data-stu-id="44298-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="44298-133">O registo de membros da equipa é criado imediatamente.</span><span class="sxs-lookup"><span data-stu-id="44298-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="44298-134">**msdyn_CreateOperationSetV1**: Esta API pode ser utilizada para agendar vários pedidos que devem ser realizados dentro de uma transação.</span><span class="sxs-lookup"><span data-stu-id="44298-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="44298-135">**msdyn_PSSCreateV1**: Esta API pode ser usada para criar uma entidade.</span><span class="sxs-lookup"><span data-stu-id="44298-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="44298-136">A entidade pode ser qualquer uma das entidades de Agendamento que apoiam a operação de criação.</span><span class="sxs-lookup"><span data-stu-id="44298-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="44298-137">**msdyn_PSSUpdateV1**: Esta API pode ser usada para atualizar uma entidade.</span><span class="sxs-lookup"><span data-stu-id="44298-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="44298-138">A entidade pode ser qualquer uma das entidades de Agendamento que apoiam a operação de atualização.</span><span class="sxs-lookup"><span data-stu-id="44298-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="44298-139">**msdyn_PSSDeleteV1**: Esta API pode ser usada para eliminar uma entidade.</span><span class="sxs-lookup"><span data-stu-id="44298-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="44298-140">A entidade pode ser qualquer uma das entidades de Agendamento que apoiam a operação de eliminação.</span><span class="sxs-lookup"><span data-stu-id="44298-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="44298-141">**msdyn_ExecuteOperationSetV1**: Esta API é utilizada para executar todas as operações no âmbito do conjunto de operações.</span><span class="sxs-lookup"><span data-stu-id="44298-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="44298-142">Utilização de APIs de agenda com OperationSet</span><span class="sxs-lookup"><span data-stu-id="44298-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="44298-143">Como os registos com **CreateProjectV1** e **CreateTeamMemberV1** são criados imediatamente, estas APIs não podem ser utilizadas diretamente no **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="44298-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="44298-144">No entanto, pode utilizar a API para criar registos necessários, criar um **OperationSet** e, em seguida, utilizar estes registos pré-criados no **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="44298-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="44298-145">Operações suportadas</span><span class="sxs-lookup"><span data-stu-id="44298-145">Supported operations</span></span>

| <span data-ttu-id="44298-146">Entidade de agendamento</span><span class="sxs-lookup"><span data-stu-id="44298-146">Scheduling entity</span></span> | <span data-ttu-id="44298-147">Criar</span><span class="sxs-lookup"><span data-stu-id="44298-147">Create</span></span> | <span data-ttu-id="44298-148">Actualizar</span><span class="sxs-lookup"><span data-stu-id="44298-148">Update</span></span> | <span data-ttu-id="44298-149">Delete</span><span class="sxs-lookup"><span data-stu-id="44298-149">Delete</span></span> | <span data-ttu-id="44298-150">Considerações importantes</span><span class="sxs-lookup"><span data-stu-id="44298-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="44298-151">Tarefa de projeto</span><span class="sxs-lookup"><span data-stu-id="44298-151">Project task</span></span> | <span data-ttu-id="44298-152">Sim</span><span class="sxs-lookup"><span data-stu-id="44298-152">Yes</span></span> | <span data-ttu-id="44298-153">Sim</span><span class="sxs-lookup"><span data-stu-id="44298-153">Yes</span></span> | <span data-ttu-id="44298-154">Sim</span><span class="sxs-lookup"><span data-stu-id="44298-154">Yes</span></span> | <span data-ttu-id="44298-155">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="44298-155">None</span></span> |
| <span data-ttu-id="44298-156">Dependência de tarefa de projeto</span><span class="sxs-lookup"><span data-stu-id="44298-156">Project task dependency</span></span> | <span data-ttu-id="44298-157">Sim</span><span class="sxs-lookup"><span data-stu-id="44298-157">Yes</span></span> | <span data-ttu-id="44298-158">Sim</span><span class="sxs-lookup"><span data-stu-id="44298-158">Yes</span></span> | | <span data-ttu-id="44298-159">Os registos de dependência de tarefas do projeto não estão atualizados.</span><span class="sxs-lookup"><span data-stu-id="44298-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="44298-160">Em vez disso, um registo antigo pode ser apagado e um novo recorde pode ser criado.</span><span class="sxs-lookup"><span data-stu-id="44298-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="44298-161">Atribuição de recurso</span><span class="sxs-lookup"><span data-stu-id="44298-161">Resource assignment</span></span> | <span data-ttu-id="44298-162">Sim</span><span class="sxs-lookup"><span data-stu-id="44298-162">Yes</span></span> | <span data-ttu-id="44298-163">Sim</span><span class="sxs-lookup"><span data-stu-id="44298-163">Yes</span></span> | | <span data-ttu-id="44298-164">As operações com os seguintes campos não são suportadas: **BookableResourceID**, **Esforço**, **EffortCompleted**, **EffortRemaining** e **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="44298-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="44298-165">Os registos de atribuição de recursos não estão atualizados.</span><span class="sxs-lookup"><span data-stu-id="44298-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="44298-166">Em vez disso, o registo antigo pode ser apagado e um novo recorde pode ser criado.</span><span class="sxs-lookup"><span data-stu-id="44298-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="44298-167">Registo do projeto</span><span class="sxs-lookup"><span data-stu-id="44298-167">Project bucket</span></span> | <span data-ttu-id="44298-168">N/D</span><span class="sxs-lookup"><span data-stu-id="44298-168">N/A</span></span> | <span data-ttu-id="44298-169">N/D</span><span class="sxs-lookup"><span data-stu-id="44298-169">N/A</span></span> | <span data-ttu-id="44298-170">N/D</span><span class="sxs-lookup"><span data-stu-id="44298-170">N/A</span></span> | <span data-ttu-id="44298-171">O registo predefinido é criado utilizando a API **CreateProjectV1**.</span><span class="sxs-lookup"><span data-stu-id="44298-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="44298-172">Membro da equipa do projeto</span><span class="sxs-lookup"><span data-stu-id="44298-172">Project team member</span></span> | <span data-ttu-id="44298-173">Sim</span><span class="sxs-lookup"><span data-stu-id="44298-173">Yes</span></span> | <span data-ttu-id="44298-174">Sim</span><span class="sxs-lookup"><span data-stu-id="44298-174">Yes</span></span> | <span data-ttu-id="44298-175">Sim</span><span class="sxs-lookup"><span data-stu-id="44298-175">Yes</span></span> | <span data-ttu-id="44298-176">Para a operação de criação, utilize a API **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="44298-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="44298-177">Project</span><span class="sxs-lookup"><span data-stu-id="44298-177">Project</span></span> | <span data-ttu-id="44298-178">Sim</span><span class="sxs-lookup"><span data-stu-id="44298-178">Yes</span></span> | <span data-ttu-id="44298-179">Sim</span><span class="sxs-lookup"><span data-stu-id="44298-179">Yes</span></span> | <span data-ttu-id="44298-180">N/D</span><span class="sxs-lookup"><span data-stu-id="44298-180">N/A</span></span> | <span data-ttu-id="44298-181">As operações com os seguintes campos não são suportadas: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Esforço**, **EffortCompleted**, **EffortRemaining**, **Progresso**, **Terminar**, **TaskEarliestStart** e **Duração**.</span><span class="sxs-lookup"><span data-stu-id="44298-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="44298-182">Estas APIs podem ser chamadas com objetos de entidade que incluem campos personalizados.</span><span class="sxs-lookup"><span data-stu-id="44298-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="44298-183">A propriedade ID é opcional.</span><span class="sxs-lookup"><span data-stu-id="44298-183">The ID property is optional.</span></span> <span data-ttu-id="44298-184">Se for fornecido, o sistema tenta usá-lo e abre uma exceção se não puder ser usado.</span><span class="sxs-lookup"><span data-stu-id="44298-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="44298-185">Se não for fornecido, o sistema irá gerá-lo.</span><span class="sxs-lookup"><span data-stu-id="44298-185">If it isn't provided, the system will generate it.</span></span>

## <a name="limitations-and-known-issues"></a><span data-ttu-id="44298-186">Problemas conhecidos e de limitações</span><span class="sxs-lookup"><span data-stu-id="44298-186">Limitations and known issues</span></span>
<span data-ttu-id="44298-187">Segue-se uma lista de limitações e questões conhecidas:</span><span class="sxs-lookup"><span data-stu-id="44298-187">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="44298-188">As APIs de agenda só podem ser utilizadas pelos **Utilizadores com licença de projeto da Microsoft.**</span><span class="sxs-lookup"><span data-stu-id="44298-188">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="44298-189">Não podem ser usadas por:</span><span class="sxs-lookup"><span data-stu-id="44298-189">They can't be used by:</span></span>
    - <span data-ttu-id="44298-190">Utilizadores da aplicação</span><span class="sxs-lookup"><span data-stu-id="44298-190">Application users</span></span>
    - <span data-ttu-id="44298-191">Utilizadores do sistema</span><span class="sxs-lookup"><span data-stu-id="44298-191">System users</span></span>
    - <span data-ttu-id="44298-192">Utilizadores de integração</span><span class="sxs-lookup"><span data-stu-id="44298-192">Integration users</span></span>
    - <span data-ttu-id="44298-193">Outros utilizadores que não têm a licença necessária</span><span class="sxs-lookup"><span data-stu-id="44298-193">Other users that don't have the required license</span></span>
- <span data-ttu-id="44298-194">Cada **OperationSet** só pode ter um máximo de 100 operações.</span><span class="sxs-lookup"><span data-stu-id="44298-194">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="44298-195">Cada utilizador só pode ter um máximo de 10 **OperationSet** abertas.</span><span class="sxs-lookup"><span data-stu-id="44298-195">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="44298-196">O Project Operations suporta atualmente um máximo de 500 tarefas totais num projeto.</span><span class="sxs-lookup"><span data-stu-id="44298-196">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="44298-197">O estado de falha e os registos de avarias do **OperationSet** não estão atualmente disponíveis.</span><span class="sxs-lookup"><span data-stu-id="44298-197">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- <span data-ttu-id="44298-198">As APIs da agenda estão em pré-visualização pública.</span><span class="sxs-lookup"><span data-stu-id="44298-198">Schedule APIs are in Public preview.</span></span> <span data-ttu-id="44298-199">A utilização destas APIs num ambiente de Produção não é suportada pela Microsoft.</span><span class="sxs-lookup"><span data-stu-id="44298-199">Using these APIs in a Production environment isn't supported by Microsoft.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="44298-200">Cenário de exemplo</span><span class="sxs-lookup"><span data-stu-id="44298-200">Sample scenario</span></span>

<span data-ttu-id="44298-201">Neste cenário, irá criar um projeto, um membro da equipa, quatro tarefas e duas atribuições de recursos.</span><span class="sxs-lookup"><span data-stu-id="44298-201">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="44298-202">Em seguida, atualizará uma tarefa, atualizará o projeto, eliminará uma tarefa, eliminará uma atribuição de recursos e criará uma dependência de tarefas.</span><span class="sxs-lookup"><span data-stu-id="44298-202">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

```C#
Entity project = CreateProject();
project.Id = CallCreateProjectAction(project);
var projectReference = project.ToEntityReference();

var teamMember = new Entity("msdyn_projectteam", Guid.NewGuid());
teamMember["msdyn_name"] = $"TM {DateTime.Now.ToShortTimeString()}";
teamMember["msdyn_project"] = projectReference;
var createTeamMemberResponse = CallCreateTeamMemberAction(teamMember);

var description = $"My demo {DateTime.Now.ToShortTimeString()}";
var operationSetId = CallCreateOperationSetAction(project.Id, description);

var task1 = GetTask("1WW", projectReference);
var task2 = GetTask("2XX", projectReference, task1.ToEntityReference());
var task3 = GetTask("3YY", projectReference);
var task4 = GetTask("4ZZ";, projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment"R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

varassignment1Response = CallPssCreateAction(assignment1, operationSetId);
varassignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

varassignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a><span data-ttu-id="44298-203">Amostras adicionais</span><span class="sxs-lookup"><span data-stu-id="44298-203">Additional samples</span></span>

```C#
#region Call actions 

///<summary>
/// Calls the action to create an operationSet
/// </summary>
/// <paramname="projectId">project id for the operations to be included in this operationSet>/param>
/// <paramname="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
privatestring CallCreateOperationSetAction(Guid projectId, string description)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_CreateOperationSetV1");
    operationSetRequest["ProjectId"] = projectId.ToString();
    operationSetRequest["Description"] = description;
    OrganizationResponse response = organizationService.Execute(operationSetRequest);
    return response["OperationSetId"].ToString();
}

/// <summary>
/// Calls the action to create an entity, only Task and Resource Assignment for now
/// </summary>
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary<
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssUpdateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssUpdateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task and Resource Assignment for now
/// <summary>
/// <paramname="recordId">Id of the record to be deleted</param>
/// <paramname="entityLogicalName">Entity logical name of the record</param>
/// <paramname="operationSetId">OperationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssDeleteAction(string recordId, string entityLogicalName, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssDeleteV1");
    operationSetRequest["RecordId"] = recordId;
    operationSetRequest["EntityLogicalName"] = entityLogicalName;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to execute requests in an operationSet
/// <summary>
/// <paramname="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallExecuteOperationSetAction(string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_ExecuteOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// This can be used to abandon an operationSet that is no longer needed
/// </summary>
/// <paramname="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
protected OperationSetResponse CallAbandonOperationSetAction(Guid operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_AbandonOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId.ToString();
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to create a new project
/// </summary>
/// <paramname="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1";
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);

    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <paramname="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
privatestring CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject><OperationSetResponse>
    ((string)orgResponse.Results["OperationSetResponse";]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet(";msdyn_project", "msdyn_name");
    var getDefaultBucket = new QueryExpression("msdyn_projectbucket")
    {
        ColumnSet = columnsToFetch,
        Criteria =
        {
            Conditions =
            {
                new ConditionExpression("msdyn_project", ConditionOperator.Equal, projectReference.Id),
                new ConditionExpression("msdyn_name", ConditionOperator.Equal, "Bucket 1")
            }
        }
    };
    return organizationService.RetrieveMultiple(getDefaultBucket);
}

private Entity GetBucket(EntityReference projectReference)
{
    var bucketCollection = GetDefaultBucket(projectReference);
    if (bucketCollection.Entities.Count > 0)
    {
    return bucketCollection[0].ToEntity<Entity>();
    }

    throw new Exception($"Please open project with id {projectReference.Id} in the Dynamics UI and navigate to the Tasks tab");
}

private Entity CreateProject()
{
    var project = new Entity("msdyn_project", Guid.NewGuid());
    project["msdyn_subject"] = $"Proj {DateTime.Now.ToShortTimeString()}";
    return project;
}

private Entity GetTask(string name, EntityReference projectReference, EntityReference parentReference = null)
{
    var task = new Entity("msdyn_projecttask", Guid.NewGuid());
    task["msdyn_project"] = projectReference;
    task["msdyn_subject"] = name;
    task["msdyn_effort";] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
        task["new_custom1"] = "Just my test";
        task[";new_age"] = 98;
        task["new_amount"] = 591.34m;
        task["new_isready"] = new OptionSetValue(100000000);
    */

    if (parentReference == null)
    {
        task["msdyn_outlinelevel"] = 1;
    }
    else
    {
        task["msdyn_parenttask"] = parentReference;
    }
    return task;
}

private Entity GetResourceAssignment(string name, Entity teamMember, Entity task, Entity project)
{
    var assignment = new Entity("msdyn_resourceassignment", Guid.NewGuid());
    assignment["msdyn_projectteamid"] = teamMember.ToEntityReference();
    assignment["msdyn_taskid"] = task.ToEntityReference();
    assignment["msdyn_projectid"] = project.ToEntityReference();
    assignment["msdyn_name"] = name;
    assignment["msdyn_start"] = DateTime.Now;
    assignment["msdyn_finish"] = DateTime.Now;
    return assignment;
}

protected Entity GetTaskDependency(Entity project, Entity predecessor, Entity successor)
{
    var taskDependency = new Entity("msdyn_projecttaskdependency", Guid.NewGuid());
    taskDependency["msdyn_project"] = project.ToEntityReference();
    taskDependency["msdyn_predecessortask"] = predecessor.ToEntityReference();
    taskDependency["msdyn_successortask"] = successor.ToEntityReference();
    taskDependency["msdyn_linktype"] = new OptionSetValue(192350000);
    return taskDependency;
}

#endregion

#region OperationSetResponse DataContract --- Sample code ----

[DataContract]
publicclassOperationSetResponse
{
    [DataMember(Name = "operationSetId")]
    public Guid OperationSetId { get; set; }

    [DataMember(Name = "operationSetDetailId")]
    public Guid OperationSetDetailId { get; set; }

    [DataMember(Name = "operationType")]
    publicstring OperationType { get; set; }

    [DataMember(Name = "recordId")]
    publicstring RecordId { get; set; }

    [DataMember(Name = "correlationId")]
    publicstring CorrelationId { get; set; }
}

#endregion
```
