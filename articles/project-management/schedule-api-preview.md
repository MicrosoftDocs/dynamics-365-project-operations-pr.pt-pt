---
title: Utilizar APIs de Agenda para realizar operações com entidades de agendamento
description: Este tópico fornece informações e amostras para a utilização de APIs de agenda.
author: sigitac
manager: Annbe
ms.date: 04/27/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e03f4e6c49a835206b23cade3fabe3fd26693441
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950818"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="86785-103">Utilizar APIs de Agenda para realizar operações com entidades de agendamento</span><span class="sxs-lookup"><span data-stu-id="86785-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="86785-104">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="86785-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="86785-105">Algumas ou todas as funcionalidades anotadas neste tópico estão disponíveis como parte de uma versão de pré-visualização.</span><span class="sxs-lookup"><span data-stu-id="86785-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="86785-106">O conteúdo e a funcionalidade estão sujeitos a alterações.</span><span class="sxs-lookup"><span data-stu-id="86785-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="86785-107">Entidades de agendamento</span><span class="sxs-lookup"><span data-stu-id="86785-107">Scheduling entities</span></span>

<span data-ttu-id="86785-108">Agendar APIs fornece a capacidade de executar operações de criar, atualizar e apagar com **Entidades de agendamento**.</span><span class="sxs-lookup"><span data-stu-id="86785-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="86785-109">Estas entidades são geridas através do motor de Agendamento em Projeto para a web.</span><span class="sxs-lookup"><span data-stu-id="86785-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="86785-110">Operações de Criar, atualizar e apagar com **Entidades de agendamento** foram restringidas em lançamentos Dynamics 365 Project Operations anteriores.</span><span class="sxs-lookup"><span data-stu-id="86785-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="86785-111">A tabela seguinte apresenta uma lista completa das **Entidades de Agendamento**.</span><span class="sxs-lookup"><span data-stu-id="86785-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="86785-112">Nome da entidade</span><span class="sxs-lookup"><span data-stu-id="86785-112">Entity name</span></span>  | <span data-ttu-id="86785-113">Nome lógico da entidade</span><span class="sxs-lookup"><span data-stu-id="86785-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="86785-114">Project</span><span class="sxs-lookup"><span data-stu-id="86785-114">Project</span></span> | <span data-ttu-id="86785-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="86785-115">msdyn_project</span></span> |
| <span data-ttu-id="86785-116">Tarefa de Projeto</span><span class="sxs-lookup"><span data-stu-id="86785-116">Project Task</span></span>  | <span data-ttu-id="86785-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="86785-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="86785-118">Dependência de Tarefa de Projeto</span><span class="sxs-lookup"><span data-stu-id="86785-118">Project Task Dependency</span></span>  | <span data-ttu-id="86785-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="86785-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="86785-120">Atribuição de Recurso</span><span class="sxs-lookup"><span data-stu-id="86785-120">Resource Assignment</span></span> | <span data-ttu-id="86785-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="86785-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="86785-122">Registo do Projeto</span><span class="sxs-lookup"><span data-stu-id="86785-122">Project Bucket</span></span>  | <span data-ttu-id="86785-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="86785-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="86785-124">Membro da Equipa do Projeto</span><span class="sxs-lookup"><span data-stu-id="86785-124">Project Team Member</span></span> | <span data-ttu-id="86785-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="86785-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="86785-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="86785-126">OperationSet</span></span>

<span data-ttu-id="86785-127">OperationSet é um padrão de unidade de trabalho que pode ser usado quando vários pedidos de impacto de programação devem ser processados dentro de uma transação.</span><span class="sxs-lookup"><span data-stu-id="86785-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="86785-128">ApIs de agenda</span><span class="sxs-lookup"><span data-stu-id="86785-128">Schedule APIs</span></span>

<span data-ttu-id="86785-129">Segue-se uma lista das APIs de agenda.</span><span class="sxs-lookup"><span data-stu-id="86785-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="86785-130">**msdyn_CreateProjectV1**: Esta API pode ser usada para criar um projeto.</span><span class="sxs-lookup"><span data-stu-id="86785-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="86785-131">O projeto e registo de projeto padrão é criado imediatamente.</span><span class="sxs-lookup"><span data-stu-id="86785-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="86785-132">**msdyn_CreateTeamMemberV1**: Esta API pode ser usada para criar um membro da equipa de projeto.</span><span class="sxs-lookup"><span data-stu-id="86785-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="86785-133">O registo de membros da equipa é criado imediatamente.</span><span class="sxs-lookup"><span data-stu-id="86785-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="86785-134">**msdyn_CreateOperationSetV1**: Esta API pode ser utilizada para agendar vários pedidos que devem ser realizados dentro de uma transação.</span><span class="sxs-lookup"><span data-stu-id="86785-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="86785-135">**msdyn_PSSCreateV1**: Esta API pode ser usada para criar uma entidade.</span><span class="sxs-lookup"><span data-stu-id="86785-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="86785-136">A entidade pode ser qualquer uma das entidades de Agendamento que apoiam a operação de criação.</span><span class="sxs-lookup"><span data-stu-id="86785-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="86785-137">**msdyn_PSSUpdateV1**: Esta API pode ser usada para atualizar uma entidade.</span><span class="sxs-lookup"><span data-stu-id="86785-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="86785-138">A entidade pode ser qualquer uma das entidades de Agendamento que apoiam a operação de atualização.</span><span class="sxs-lookup"><span data-stu-id="86785-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="86785-139">**msdyn_PSSDeleteV1**: Esta API pode ser usada para eliminar uma entidade.</span><span class="sxs-lookup"><span data-stu-id="86785-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="86785-140">A entidade pode ser qualquer uma das entidades de Agendamento que apoiam a operação de eliminação.</span><span class="sxs-lookup"><span data-stu-id="86785-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="86785-141">**msdyn_ExecuteOperationSetV1**: Esta API é utilizada para executar todas as operações no âmbito do conjunto de operações.</span><span class="sxs-lookup"><span data-stu-id="86785-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="86785-142">Utilização de APIs de agenda com OperationSet</span><span class="sxs-lookup"><span data-stu-id="86785-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="86785-143">Como os registos com **CreateProjectV1** e **CreateTeamMemberV1** são criados imediatamente, estas APIs não podem ser utilizadas diretamente no **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="86785-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="86785-144">No entanto, pode utilizar a API para criar registos necessários, criar um **OperationSet** e, em seguida, utilizar estes registos pré-criados no **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="86785-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="86785-145">Operações suportadas</span><span class="sxs-lookup"><span data-stu-id="86785-145">Supported operations</span></span>

| <span data-ttu-id="86785-146">Entidade de agendamento</span><span class="sxs-lookup"><span data-stu-id="86785-146">Scheduling entity</span></span> | <span data-ttu-id="86785-147">Criar</span><span class="sxs-lookup"><span data-stu-id="86785-147">Create</span></span> | <span data-ttu-id="86785-148">Actualizar</span><span class="sxs-lookup"><span data-stu-id="86785-148">Update</span></span> | <span data-ttu-id="86785-149">Delete</span><span class="sxs-lookup"><span data-stu-id="86785-149">Delete</span></span> | <span data-ttu-id="86785-150">Considerações importantes</span><span class="sxs-lookup"><span data-stu-id="86785-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="86785-151">Tarefa de projeto</span><span class="sxs-lookup"><span data-stu-id="86785-151">Project task</span></span> | <span data-ttu-id="86785-152">Sim</span><span class="sxs-lookup"><span data-stu-id="86785-152">Yes</span></span> | <span data-ttu-id="86785-153">Sim</span><span class="sxs-lookup"><span data-stu-id="86785-153">Yes</span></span> | <span data-ttu-id="86785-154">Sim</span><span class="sxs-lookup"><span data-stu-id="86785-154">Yes</span></span> | <span data-ttu-id="86785-155">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="86785-155">None</span></span> |
| <span data-ttu-id="86785-156">Dependência de tarefa de projeto</span><span class="sxs-lookup"><span data-stu-id="86785-156">Project task dependency</span></span> | <span data-ttu-id="86785-157">Sim</span><span class="sxs-lookup"><span data-stu-id="86785-157">Yes</span></span> | <span data-ttu-id="86785-158">Sim</span><span class="sxs-lookup"><span data-stu-id="86785-158">Yes</span></span> | | <span data-ttu-id="86785-159">Os registos de dependência de tarefas do projeto não estão atualizados.</span><span class="sxs-lookup"><span data-stu-id="86785-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="86785-160">Em vez disso, um registo antigo pode ser apagado e um novo recorde pode ser criado.</span><span class="sxs-lookup"><span data-stu-id="86785-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="86785-161">Atribuição de recurso</span><span class="sxs-lookup"><span data-stu-id="86785-161">Resource assignment</span></span> | <span data-ttu-id="86785-162">Sim</span><span class="sxs-lookup"><span data-stu-id="86785-162">Yes</span></span> | <span data-ttu-id="86785-163">Sim</span><span class="sxs-lookup"><span data-stu-id="86785-163">Yes</span></span> | | <span data-ttu-id="86785-164">As operações com os seguintes campos não são suportadas: **BookableResourceID**, **Esforço**, **EffortCompleted**, **EffortRemaining** e **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="86785-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="86785-165">Os registos de atribuição de recursos não estão atualizados.</span><span class="sxs-lookup"><span data-stu-id="86785-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="86785-166">Em vez disso, o registo antigo pode ser apagado e um novo recorde pode ser criado.</span><span class="sxs-lookup"><span data-stu-id="86785-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="86785-167">Registo do projeto</span><span class="sxs-lookup"><span data-stu-id="86785-167">Project bucket</span></span> | <span data-ttu-id="86785-168">N/D</span><span class="sxs-lookup"><span data-stu-id="86785-168">N/A</span></span> | <span data-ttu-id="86785-169">N/D</span><span class="sxs-lookup"><span data-stu-id="86785-169">N/A</span></span> | <span data-ttu-id="86785-170">N/D</span><span class="sxs-lookup"><span data-stu-id="86785-170">N/A</span></span> | <span data-ttu-id="86785-171">O registo predefinido é criado utilizando a API **CreateProjectV1**.</span><span class="sxs-lookup"><span data-stu-id="86785-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="86785-172">Membro da equipa do projeto</span><span class="sxs-lookup"><span data-stu-id="86785-172">Project team member</span></span> | <span data-ttu-id="86785-173">Sim</span><span class="sxs-lookup"><span data-stu-id="86785-173">Yes</span></span> | <span data-ttu-id="86785-174">Sim</span><span class="sxs-lookup"><span data-stu-id="86785-174">Yes</span></span> | <span data-ttu-id="86785-175">Sim</span><span class="sxs-lookup"><span data-stu-id="86785-175">Yes</span></span> | <span data-ttu-id="86785-176">Para a operação de criação, utilize a API **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="86785-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="86785-177">Project</span><span class="sxs-lookup"><span data-stu-id="86785-177">Project</span></span> | <span data-ttu-id="86785-178">Sim</span><span class="sxs-lookup"><span data-stu-id="86785-178">Yes</span></span> | <span data-ttu-id="86785-179">Sim</span><span class="sxs-lookup"><span data-stu-id="86785-179">Yes</span></span> | <span data-ttu-id="86785-180">N/D</span><span class="sxs-lookup"><span data-stu-id="86785-180">N/A</span></span> | <span data-ttu-id="86785-181">As operações com os seguintes campos não são suportadas: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Esforço**, **EffortCompleted**, **EffortRemaining**, **Progresso**, **Terminar**, **TaskEarliestStart** e **Duração**.</span><span class="sxs-lookup"><span data-stu-id="86785-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="86785-182">Estas APIs podem ser chamadas com objetos de entidade que incluem campos personalizados.</span><span class="sxs-lookup"><span data-stu-id="86785-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="86785-183">A propriedade ID é opcional.</span><span class="sxs-lookup"><span data-stu-id="86785-183">The ID property is optional.</span></span> <span data-ttu-id="86785-184">Se for fornecido, o sistema tenta usá-lo e abre uma exceção se não puder ser usado.</span><span class="sxs-lookup"><span data-stu-id="86785-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="86785-185">Se não for fornecido, o sistema irá gerá-lo.</span><span class="sxs-lookup"><span data-stu-id="86785-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="86785-186">Campos restritos</span><span class="sxs-lookup"><span data-stu-id="86785-186">Restricted fields</span></span>

<span data-ttu-id="86785-187">As tabelas que se seguem definem os campos que estão restringidos de **Criar** e **Editar.**</span><span class="sxs-lookup"><span data-stu-id="86785-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="86785-188">Tarefa de projeto</span><span class="sxs-lookup"><span data-stu-id="86785-188">Project task</span></span>

| <span data-ttu-id="86785-189">**Nome lógico**</span><span class="sxs-lookup"><span data-stu-id="86785-189">**Logical name**</span></span>                       | <span data-ttu-id="86785-190">**Pode criar**</span><span class="sxs-lookup"><span data-stu-id="86785-190">**Can create**</span></span> | <span data-ttu-id="86785-191">**Pode editar**</span><span class="sxs-lookup"><span data-stu-id="86785-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="86785-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="86785-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="86785-193">não</span><span class="sxs-lookup"><span data-stu-id="86785-193">no</span></span>             | <span data-ttu-id="86785-194">não</span><span class="sxs-lookup"><span data-stu-id="86785-194">no</span></span>               |
| <span data-ttu-id="86785-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="86785-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="86785-196">não</span><span class="sxs-lookup"><span data-stu-id="86785-196">no</span></span>             | <span data-ttu-id="86785-197">não</span><span class="sxs-lookup"><span data-stu-id="86785-197">no</span></span>               |
| <span data-ttu-id="86785-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="86785-198">msdyn_actualend</span></span>                        | <span data-ttu-id="86785-199">não</span><span class="sxs-lookup"><span data-stu-id="86785-199">no</span></span>             | <span data-ttu-id="86785-200">não</span><span class="sxs-lookup"><span data-stu-id="86785-200">no</span></span>               |
| <span data-ttu-id="86785-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="86785-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="86785-202">não</span><span class="sxs-lookup"><span data-stu-id="86785-202">no</span></span>             | <span data-ttu-id="86785-203">não</span><span class="sxs-lookup"><span data-stu-id="86785-203">no</span></span>               |
| <span data-ttu-id="86785-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="86785-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="86785-205">não</span><span class="sxs-lookup"><span data-stu-id="86785-205">no</span></span>             | <span data-ttu-id="86785-206">não</span><span class="sxs-lookup"><span data-stu-id="86785-206">no</span></span>               |
| <span data-ttu-id="86785-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="86785-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="86785-208">não</span><span class="sxs-lookup"><span data-stu-id="86785-208">no</span></span>             | <span data-ttu-id="86785-209">não</span><span class="sxs-lookup"><span data-stu-id="86785-209">no</span></span>               |
| <span data-ttu-id="86785-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="86785-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="86785-211">não</span><span class="sxs-lookup"><span data-stu-id="86785-211">no</span></span>             | <span data-ttu-id="86785-212">não</span><span class="sxs-lookup"><span data-stu-id="86785-212">no</span></span>               |
| <span data-ttu-id="86785-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="86785-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="86785-214">não</span><span class="sxs-lookup"><span data-stu-id="86785-214">no</span></span>             | <span data-ttu-id="86785-215">não</span><span class="sxs-lookup"><span data-stu-id="86785-215">no</span></span>               |
| <span data-ttu-id="86785-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="86785-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="86785-217">não</span><span class="sxs-lookup"><span data-stu-id="86785-217">no</span></span>             | <span data-ttu-id="86785-218">não</span><span class="sxs-lookup"><span data-stu-id="86785-218">no</span></span>               |
| <span data-ttu-id="86785-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="86785-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="86785-220">não</span><span class="sxs-lookup"><span data-stu-id="86785-220">no</span></span>             | <span data-ttu-id="86785-221">não</span><span class="sxs-lookup"><span data-stu-id="86785-221">no</span></span>               |
| <span data-ttu-id="86785-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="86785-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="86785-223">não</span><span class="sxs-lookup"><span data-stu-id="86785-223">no</span></span>             | <span data-ttu-id="86785-224">não</span><span class="sxs-lookup"><span data-stu-id="86785-224">no</span></span>               |
| <span data-ttu-id="86785-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="86785-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="86785-226">não</span><span class="sxs-lookup"><span data-stu-id="86785-226">no</span></span>             | <span data-ttu-id="86785-227">não</span><span class="sxs-lookup"><span data-stu-id="86785-227">no</span></span>               |
| <span data-ttu-id="86785-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="86785-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="86785-229">não</span><span class="sxs-lookup"><span data-stu-id="86785-229">no</span></span>             | <span data-ttu-id="86785-230">não</span><span class="sxs-lookup"><span data-stu-id="86785-230">no</span></span>               |
| <span data-ttu-id="86785-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="86785-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="86785-232">não</span><span class="sxs-lookup"><span data-stu-id="86785-232">no</span></span>             | <span data-ttu-id="86785-233">não</span><span class="sxs-lookup"><span data-stu-id="86785-233">no</span></span>               |
| <span data-ttu-id="86785-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="86785-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="86785-235">não</span><span class="sxs-lookup"><span data-stu-id="86785-235">no</span></span>             | <span data-ttu-id="86785-236">não</span><span class="sxs-lookup"><span data-stu-id="86785-236">no</span></span>               |
| <span data-ttu-id="86785-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="86785-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="86785-238">não</span><span class="sxs-lookup"><span data-stu-id="86785-238">no</span></span>             | <span data-ttu-id="86785-239">não</span><span class="sxs-lookup"><span data-stu-id="86785-239">no</span></span>               |
| <span data-ttu-id="86785-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="86785-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="86785-241">não</span><span class="sxs-lookup"><span data-stu-id="86785-241">no</span></span>             | <span data-ttu-id="86785-242">não</span><span class="sxs-lookup"><span data-stu-id="86785-242">no</span></span>               |
| <span data-ttu-id="86785-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="86785-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="86785-244">não</span><span class="sxs-lookup"><span data-stu-id="86785-244">no</span></span>             | <span data-ttu-id="86785-245">não</span><span class="sxs-lookup"><span data-stu-id="86785-245">no</span></span>               |
| <span data-ttu-id="86785-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="86785-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="86785-247">não</span><span class="sxs-lookup"><span data-stu-id="86785-247">no</span></span>             | <span data-ttu-id="86785-248">não</span><span class="sxs-lookup"><span data-stu-id="86785-248">no</span></span>               |
| <span data-ttu-id="86785-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="86785-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="86785-250">não</span><span class="sxs-lookup"><span data-stu-id="86785-250">no</span></span>             | <span data-ttu-id="86785-251">não</span><span class="sxs-lookup"><span data-stu-id="86785-251">no</span></span>               |
| <span data-ttu-id="86785-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="86785-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="86785-253">não</span><span class="sxs-lookup"><span data-stu-id="86785-253">no</span></span>             | <span data-ttu-id="86785-254">não</span><span class="sxs-lookup"><span data-stu-id="86785-254">no</span></span>               |
| <span data-ttu-id="86785-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="86785-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="86785-256">não</span><span class="sxs-lookup"><span data-stu-id="86785-256">no</span></span>             | <span data-ttu-id="86785-257">não</span><span class="sxs-lookup"><span data-stu-id="86785-257">no</span></span>               |
| <span data-ttu-id="86785-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="86785-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="86785-259">não</span><span class="sxs-lookup"><span data-stu-id="86785-259">no</span></span>             | <span data-ttu-id="86785-260">não</span><span class="sxs-lookup"><span data-stu-id="86785-260">no</span></span>               |
| <span data-ttu-id="86785-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="86785-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="86785-262">não</span><span class="sxs-lookup"><span data-stu-id="86785-262">no</span></span>             | <span data-ttu-id="86785-263">não</span><span class="sxs-lookup"><span data-stu-id="86785-263">no</span></span>               |
| <span data-ttu-id="86785-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="86785-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="86785-265">não</span><span class="sxs-lookup"><span data-stu-id="86785-265">no</span></span>             | <span data-ttu-id="86785-266">não</span><span class="sxs-lookup"><span data-stu-id="86785-266">no</span></span>               |
| <span data-ttu-id="86785-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="86785-267">msdyn_progress</span></span>                         | <span data-ttu-id="86785-268">não</span><span class="sxs-lookup"><span data-stu-id="86785-268">no</span></span>             | <span data-ttu-id="86785-269">não (sim para P4W)</span><span class="sxs-lookup"><span data-stu-id="86785-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="86785-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="86785-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="86785-271">não</span><span class="sxs-lookup"><span data-stu-id="86785-271">no</span></span>             | <span data-ttu-id="86785-272">não</span><span class="sxs-lookup"><span data-stu-id="86785-272">no</span></span>               |
| <span data-ttu-id="86785-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="86785-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="86785-274">não</span><span class="sxs-lookup"><span data-stu-id="86785-274">no</span></span>             | <span data-ttu-id="86785-275">não</span><span class="sxs-lookup"><span data-stu-id="86785-275">no</span></span>               |
| <span data-ttu-id="86785-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="86785-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="86785-277">não</span><span class="sxs-lookup"><span data-stu-id="86785-277">no</span></span>             | <span data-ttu-id="86785-278">não</span><span class="sxs-lookup"><span data-stu-id="86785-278">no</span></span>               |
| <span data-ttu-id="86785-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="86785-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="86785-280">não</span><span class="sxs-lookup"><span data-stu-id="86785-280">no</span></span>             | <span data-ttu-id="86785-281">não</span><span class="sxs-lookup"><span data-stu-id="86785-281">no</span></span>               |
| <span data-ttu-id="86785-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="86785-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="86785-283">não</span><span class="sxs-lookup"><span data-stu-id="86785-283">no</span></span>             | <span data-ttu-id="86785-284">não</span><span class="sxs-lookup"><span data-stu-id="86785-284">no</span></span>               |
| <span data-ttu-id="86785-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="86785-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="86785-286">não</span><span class="sxs-lookup"><span data-stu-id="86785-286">no</span></span>             | <span data-ttu-id="86785-287">não</span><span class="sxs-lookup"><span data-stu-id="86785-287">no</span></span>               |
| <span data-ttu-id="86785-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="86785-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="86785-289">não</span><span class="sxs-lookup"><span data-stu-id="86785-289">no</span></span>             | <span data-ttu-id="86785-290">não</span><span class="sxs-lookup"><span data-stu-id="86785-290">no</span></span>               |
| <span data-ttu-id="86785-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="86785-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="86785-292">não</span><span class="sxs-lookup"><span data-stu-id="86785-292">no</span></span>             | <span data-ttu-id="86785-293">não</span><span class="sxs-lookup"><span data-stu-id="86785-293">no</span></span>               |
| <span data-ttu-id="86785-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="86785-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="86785-295">não</span><span class="sxs-lookup"><span data-stu-id="86785-295">no</span></span>             | <span data-ttu-id="86785-296">não</span><span class="sxs-lookup"><span data-stu-id="86785-296">no</span></span>               |
| <span data-ttu-id="86785-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="86785-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="86785-298">não</span><span class="sxs-lookup"><span data-stu-id="86785-298">no</span></span>             | <span data-ttu-id="86785-299">não</span><span class="sxs-lookup"><span data-stu-id="86785-299">no</span></span>               |
| <span data-ttu-id="86785-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="86785-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="86785-301">não</span><span class="sxs-lookup"><span data-stu-id="86785-301">no</span></span>             | <span data-ttu-id="86785-302">não</span><span class="sxs-lookup"><span data-stu-id="86785-302">no</span></span>               |
| <span data-ttu-id="86785-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="86785-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="86785-304">não</span><span class="sxs-lookup"><span data-stu-id="86785-304">no</span></span>             | <span data-ttu-id="86785-305">não</span><span class="sxs-lookup"><span data-stu-id="86785-305">no</span></span>               |
| <span data-ttu-id="86785-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="86785-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="86785-307">não</span><span class="sxs-lookup"><span data-stu-id="86785-307">no</span></span>             | <span data-ttu-id="86785-308">não</span><span class="sxs-lookup"><span data-stu-id="86785-308">no</span></span>               |
| <span data-ttu-id="86785-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="86785-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="86785-310">não</span><span class="sxs-lookup"><span data-stu-id="86785-310">no</span></span>             | <span data-ttu-id="86785-311">não</span><span class="sxs-lookup"><span data-stu-id="86785-311">no</span></span>               |
| <span data-ttu-id="86785-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="86785-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="86785-313">não</span><span class="sxs-lookup"><span data-stu-id="86785-313">no</span></span>             | <span data-ttu-id="86785-314">não</span><span class="sxs-lookup"><span data-stu-id="86785-314">no</span></span>               |
| <span data-ttu-id="86785-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="86785-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="86785-316">não</span><span class="sxs-lookup"><span data-stu-id="86785-316">no</span></span>             | <span data-ttu-id="86785-317">não</span><span class="sxs-lookup"><span data-stu-id="86785-317">no</span></span>               |
| <span data-ttu-id="86785-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="86785-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="86785-319">não</span><span class="sxs-lookup"><span data-stu-id="86785-319">no</span></span>             | <span data-ttu-id="86785-320">não</span><span class="sxs-lookup"><span data-stu-id="86785-320">no</span></span>               |
| <span data-ttu-id="86785-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="86785-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="86785-322">não</span><span class="sxs-lookup"><span data-stu-id="86785-322">no</span></span>             | <span data-ttu-id="86785-323">não</span><span class="sxs-lookup"><span data-stu-id="86785-323">no</span></span>               |
| <span data-ttu-id="86785-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="86785-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="86785-325">não</span><span class="sxs-lookup"><span data-stu-id="86785-325">no</span></span>             | <span data-ttu-id="86785-326">não</span><span class="sxs-lookup"><span data-stu-id="86785-326">no</span></span>               |
| <span data-ttu-id="86785-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="86785-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="86785-328">não</span><span class="sxs-lookup"><span data-stu-id="86785-328">no</span></span>             | <span data-ttu-id="86785-329">não</span><span class="sxs-lookup"><span data-stu-id="86785-329">no</span></span>               |
| <span data-ttu-id="86785-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="86785-330">msdyn_summary</span></span>                          | <span data-ttu-id="86785-331">não</span><span class="sxs-lookup"><span data-stu-id="86785-331">no</span></span>             | <span data-ttu-id="86785-332">não</span><span class="sxs-lookup"><span data-stu-id="86785-332">no</span></span>               |
| <span data-ttu-id="86785-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="86785-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="86785-334">não</span><span class="sxs-lookup"><span data-stu-id="86785-334">no</span></span>             | <span data-ttu-id="86785-335">não</span><span class="sxs-lookup"><span data-stu-id="86785-335">no</span></span>               |
| <span data-ttu-id="86785-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="86785-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="86785-337">não</span><span class="sxs-lookup"><span data-stu-id="86785-337">no</span></span>             | <span data-ttu-id="86785-338">não</span><span class="sxs-lookup"><span data-stu-id="86785-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="86785-339">Dependência de tarefa de projeto</span><span class="sxs-lookup"><span data-stu-id="86785-339">Project task dependency</span></span>

| <span data-ttu-id="86785-340">**Nome lógico**</span><span class="sxs-lookup"><span data-stu-id="86785-340">**Logical name**</span></span>              | <span data-ttu-id="86785-341">**Pode criar**</span><span class="sxs-lookup"><span data-stu-id="86785-341">**Can create**</span></span> | <span data-ttu-id="86785-342">**Pode editar**</span><span class="sxs-lookup"><span data-stu-id="86785-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="86785-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="86785-343">msdyn_linktype</span></span>                | <span data-ttu-id="86785-344">não</span><span class="sxs-lookup"><span data-stu-id="86785-344">no</span></span>             | <span data-ttu-id="86785-345">não</span><span class="sxs-lookup"><span data-stu-id="86785-345">no</span></span>           |
| <span data-ttu-id="86785-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="86785-346">msdyn_linktypename</span></span>            | <span data-ttu-id="86785-347">não</span><span class="sxs-lookup"><span data-stu-id="86785-347">no</span></span>             | <span data-ttu-id="86785-348">não</span><span class="sxs-lookup"><span data-stu-id="86785-348">no</span></span>           |
| <span data-ttu-id="86785-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="86785-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="86785-350">sim</span><span class="sxs-lookup"><span data-stu-id="86785-350">yes</span></span>            | <span data-ttu-id="86785-351">não</span><span class="sxs-lookup"><span data-stu-id="86785-351">no</span></span>           |
| <span data-ttu-id="86785-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="86785-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="86785-353">sim</span><span class="sxs-lookup"><span data-stu-id="86785-353">yes</span></span>            | <span data-ttu-id="86785-354">não</span><span class="sxs-lookup"><span data-stu-id="86785-354">no</span></span>           |
| <span data-ttu-id="86785-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="86785-355">msdyn_project</span></span>                 | <span data-ttu-id="86785-356">sim</span><span class="sxs-lookup"><span data-stu-id="86785-356">yes</span></span>            | <span data-ttu-id="86785-357">não</span><span class="sxs-lookup"><span data-stu-id="86785-357">no</span></span>           |
| <span data-ttu-id="86785-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="86785-358">msdyn_projectname</span></span>             | <span data-ttu-id="86785-359">sim</span><span class="sxs-lookup"><span data-stu-id="86785-359">yes</span></span>            | <span data-ttu-id="86785-360">não</span><span class="sxs-lookup"><span data-stu-id="86785-360">no</span></span>           |
| <span data-ttu-id="86785-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="86785-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="86785-362">sim</span><span class="sxs-lookup"><span data-stu-id="86785-362">yes</span></span>            | <span data-ttu-id="86785-363">não</span><span class="sxs-lookup"><span data-stu-id="86785-363">no</span></span>           |
| <span data-ttu-id="86785-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="86785-364">msdyn_successortask</span></span>           | <span data-ttu-id="86785-365">sim</span><span class="sxs-lookup"><span data-stu-id="86785-365">yes</span></span>            | <span data-ttu-id="86785-366">não</span><span class="sxs-lookup"><span data-stu-id="86785-366">no</span></span>           |
| <span data-ttu-id="86785-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="86785-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="86785-368">sim</span><span class="sxs-lookup"><span data-stu-id="86785-368">yes</span></span>            | <span data-ttu-id="86785-369">não</span><span class="sxs-lookup"><span data-stu-id="86785-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="86785-370">Atribuição de recurso</span><span class="sxs-lookup"><span data-stu-id="86785-370">Resource assignment</span></span>

| <span data-ttu-id="86785-371">**Nome lógico**</span><span class="sxs-lookup"><span data-stu-id="86785-371">**Logical name**</span></span>             | <span data-ttu-id="86785-372">**Pode criar**</span><span class="sxs-lookup"><span data-stu-id="86785-372">**Can create**</span></span> | <span data-ttu-id="86785-373">**Pode editar**</span><span class="sxs-lookup"><span data-stu-id="86785-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="86785-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="86785-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="86785-375">sim</span><span class="sxs-lookup"><span data-stu-id="86785-375">yes</span></span>            | <span data-ttu-id="86785-376">não</span><span class="sxs-lookup"><span data-stu-id="86785-376">no</span></span>           |
| <span data-ttu-id="86785-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="86785-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="86785-378">sim</span><span class="sxs-lookup"><span data-stu-id="86785-378">yes</span></span>            | <span data-ttu-id="86785-379">não</span><span class="sxs-lookup"><span data-stu-id="86785-379">no</span></span>           |
| <span data-ttu-id="86785-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="86785-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="86785-381">não</span><span class="sxs-lookup"><span data-stu-id="86785-381">no</span></span>             | <span data-ttu-id="86785-382">não</span><span class="sxs-lookup"><span data-stu-id="86785-382">no</span></span>           |
| <span data-ttu-id="86785-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="86785-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="86785-384">não</span><span class="sxs-lookup"><span data-stu-id="86785-384">no</span></span>             | <span data-ttu-id="86785-385">não</span><span class="sxs-lookup"><span data-stu-id="86785-385">no</span></span>           |
| <span data-ttu-id="86785-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="86785-386">msdyn_committype</span></span>             | <span data-ttu-id="86785-387">não</span><span class="sxs-lookup"><span data-stu-id="86785-387">no</span></span>             | <span data-ttu-id="86785-388">não</span><span class="sxs-lookup"><span data-stu-id="86785-388">no</span></span>           |
| <span data-ttu-id="86785-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="86785-389">msdyn_committypename</span></span>         | <span data-ttu-id="86785-390">não</span><span class="sxs-lookup"><span data-stu-id="86785-390">no</span></span>             | <span data-ttu-id="86785-391">não</span><span class="sxs-lookup"><span data-stu-id="86785-391">no</span></span>           |
| <span data-ttu-id="86785-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="86785-392">msdyn_effort</span></span>                 | <span data-ttu-id="86785-393">não</span><span class="sxs-lookup"><span data-stu-id="86785-393">no</span></span>             | <span data-ttu-id="86785-394">não</span><span class="sxs-lookup"><span data-stu-id="86785-394">no</span></span>           |
| <span data-ttu-id="86785-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="86785-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="86785-396">não</span><span class="sxs-lookup"><span data-stu-id="86785-396">no</span></span>             | <span data-ttu-id="86785-397">não</span><span class="sxs-lookup"><span data-stu-id="86785-397">no</span></span>           |
| <span data-ttu-id="86785-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="86785-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="86785-399">não</span><span class="sxs-lookup"><span data-stu-id="86785-399">no</span></span>             | <span data-ttu-id="86785-400">não</span><span class="sxs-lookup"><span data-stu-id="86785-400">no</span></span>           |
| <span data-ttu-id="86785-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="86785-401">msdyn_finish</span></span>                 | <span data-ttu-id="86785-402">não</span><span class="sxs-lookup"><span data-stu-id="86785-402">no</span></span>             | <span data-ttu-id="86785-403">não</span><span class="sxs-lookup"><span data-stu-id="86785-403">no</span></span>           |
| <span data-ttu-id="86785-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="86785-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="86785-405">não</span><span class="sxs-lookup"><span data-stu-id="86785-405">no</span></span>             | <span data-ttu-id="86785-406">não</span><span class="sxs-lookup"><span data-stu-id="86785-406">no</span></span>           |
| <span data-ttu-id="86785-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="86785-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="86785-408">não</span><span class="sxs-lookup"><span data-stu-id="86785-408">no</span></span>             | <span data-ttu-id="86785-409">não</span><span class="sxs-lookup"><span data-stu-id="86785-409">no</span></span>           |
| <span data-ttu-id="86785-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="86785-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="86785-411">não</span><span class="sxs-lookup"><span data-stu-id="86785-411">no</span></span>             | <span data-ttu-id="86785-412">não</span><span class="sxs-lookup"><span data-stu-id="86785-412">no</span></span>           |
| <span data-ttu-id="86785-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="86785-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="86785-414">não</span><span class="sxs-lookup"><span data-stu-id="86785-414">no</span></span>             | <span data-ttu-id="86785-415">não</span><span class="sxs-lookup"><span data-stu-id="86785-415">no</span></span>           |
| <span data-ttu-id="86785-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="86785-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="86785-417">não</span><span class="sxs-lookup"><span data-stu-id="86785-417">no</span></span>             | <span data-ttu-id="86785-418">não</span><span class="sxs-lookup"><span data-stu-id="86785-418">no</span></span>           |
| <span data-ttu-id="86785-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="86785-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="86785-420">não</span><span class="sxs-lookup"><span data-stu-id="86785-420">no</span></span>             | <span data-ttu-id="86785-421">não</span><span class="sxs-lookup"><span data-stu-id="86785-421">no</span></span>           |
| <span data-ttu-id="86785-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="86785-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="86785-423">não</span><span class="sxs-lookup"><span data-stu-id="86785-423">no</span></span>             | <span data-ttu-id="86785-424">não</span><span class="sxs-lookup"><span data-stu-id="86785-424">no</span></span>           |
| <span data-ttu-id="86785-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="86785-425">msdyn_projectid</span></span>              | <span data-ttu-id="86785-426">sim</span><span class="sxs-lookup"><span data-stu-id="86785-426">yes</span></span>            | <span data-ttu-id="86785-427">não</span><span class="sxs-lookup"><span data-stu-id="86785-427">no</span></span>           |
| <span data-ttu-id="86785-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="86785-428">msdyn_projectidname</span></span>          | <span data-ttu-id="86785-429">não</span><span class="sxs-lookup"><span data-stu-id="86785-429">no</span></span>             | <span data-ttu-id="86785-430">não</span><span class="sxs-lookup"><span data-stu-id="86785-430">no</span></span>           |
| <span data-ttu-id="86785-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="86785-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="86785-432">não</span><span class="sxs-lookup"><span data-stu-id="86785-432">no</span></span>             | <span data-ttu-id="86785-433">não</span><span class="sxs-lookup"><span data-stu-id="86785-433">no</span></span>           |
| <span data-ttu-id="86785-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="86785-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="86785-435">não</span><span class="sxs-lookup"><span data-stu-id="86785-435">no</span></span>             | <span data-ttu-id="86785-436">não</span><span class="sxs-lookup"><span data-stu-id="86785-436">no</span></span>           |
| <span data-ttu-id="86785-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="86785-437">msdyn_start</span></span>                  | <span data-ttu-id="86785-438">não</span><span class="sxs-lookup"><span data-stu-id="86785-438">no</span></span>             | <span data-ttu-id="86785-439">não</span><span class="sxs-lookup"><span data-stu-id="86785-439">no</span></span>           |
| <span data-ttu-id="86785-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="86785-440">msdyn_taskid</span></span>                 | <span data-ttu-id="86785-441">não</span><span class="sxs-lookup"><span data-stu-id="86785-441">no</span></span>             | <span data-ttu-id="86785-442">não</span><span class="sxs-lookup"><span data-stu-id="86785-442">no</span></span>           |
| <span data-ttu-id="86785-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="86785-443">msdyn_taskidname</span></span>             | <span data-ttu-id="86785-444">não</span><span class="sxs-lookup"><span data-stu-id="86785-444">no</span></span>             | <span data-ttu-id="86785-445">não</span><span class="sxs-lookup"><span data-stu-id="86785-445">no</span></span>           |
| <span data-ttu-id="86785-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="86785-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="86785-447">não</span><span class="sxs-lookup"><span data-stu-id="86785-447">no</span></span>             | <span data-ttu-id="86785-448">não</span><span class="sxs-lookup"><span data-stu-id="86785-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="86785-449">Membro da equipa do projeto</span><span class="sxs-lookup"><span data-stu-id="86785-449">Project team member</span></span>

| <span data-ttu-id="86785-450">**Nome lógico**</span><span class="sxs-lookup"><span data-stu-id="86785-450">**Logical name**</span></span>                                 | <span data-ttu-id="86785-451">**Pode criar**</span><span class="sxs-lookup"><span data-stu-id="86785-451">**Can create**</span></span> | <span data-ttu-id="86785-452">**Pode editar**</span><span class="sxs-lookup"><span data-stu-id="86785-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="86785-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="86785-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="86785-454">não</span><span class="sxs-lookup"><span data-stu-id="86785-454">no</span></span>             | <span data-ttu-id="86785-455">não</span><span class="sxs-lookup"><span data-stu-id="86785-455">no</span></span>           |
| <span data-ttu-id="86785-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="86785-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="86785-457">não</span><span class="sxs-lookup"><span data-stu-id="86785-457">no</span></span>             | <span data-ttu-id="86785-458">não</span><span class="sxs-lookup"><span data-stu-id="86785-458">no</span></span>           |
| <span data-ttu-id="86785-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="86785-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="86785-460">não</span><span class="sxs-lookup"><span data-stu-id="86785-460">no</span></span>             | <span data-ttu-id="86785-461">não</span><span class="sxs-lookup"><span data-stu-id="86785-461">no</span></span>           |
| <span data-ttu-id="86785-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="86785-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="86785-463">não</span><span class="sxs-lookup"><span data-stu-id="86785-463">no</span></span>             | <span data-ttu-id="86785-464">não</span><span class="sxs-lookup"><span data-stu-id="86785-464">no</span></span>           |
| <span data-ttu-id="86785-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="86785-465">msdyn_effort</span></span>                                     | <span data-ttu-id="86785-466">não</span><span class="sxs-lookup"><span data-stu-id="86785-466">no</span></span>             | <span data-ttu-id="86785-467">não</span><span class="sxs-lookup"><span data-stu-id="86785-467">no</span></span>           |
| <span data-ttu-id="86785-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="86785-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="86785-469">não</span><span class="sxs-lookup"><span data-stu-id="86785-469">no</span></span>             | <span data-ttu-id="86785-470">não</span><span class="sxs-lookup"><span data-stu-id="86785-470">no</span></span>           |
| <span data-ttu-id="86785-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="86785-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="86785-472">não</span><span class="sxs-lookup"><span data-stu-id="86785-472">no</span></span>             | <span data-ttu-id="86785-473">não</span><span class="sxs-lookup"><span data-stu-id="86785-473">no</span></span>           |
| <span data-ttu-id="86785-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="86785-474">msdyn_finish</span></span>                                     | <span data-ttu-id="86785-475">não</span><span class="sxs-lookup"><span data-stu-id="86785-475">no</span></span>             | <span data-ttu-id="86785-476">não</span><span class="sxs-lookup"><span data-stu-id="86785-476">no</span></span>           |
| <span data-ttu-id="86785-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="86785-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="86785-478">não</span><span class="sxs-lookup"><span data-stu-id="86785-478">no</span></span>             | <span data-ttu-id="86785-479">não</span><span class="sxs-lookup"><span data-stu-id="86785-479">no</span></span>           |
| <span data-ttu-id="86785-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="86785-480">msdyn_hours</span></span>                                      | <span data-ttu-id="86785-481">não</span><span class="sxs-lookup"><span data-stu-id="86785-481">no</span></span>             | <span data-ttu-id="86785-482">não</span><span class="sxs-lookup"><span data-stu-id="86785-482">no</span></span>           |
| <span data-ttu-id="86785-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="86785-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="86785-484">não</span><span class="sxs-lookup"><span data-stu-id="86785-484">no</span></span>             | <span data-ttu-id="86785-485">não</span><span class="sxs-lookup"><span data-stu-id="86785-485">no</span></span>           |
| <span data-ttu-id="86785-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="86785-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="86785-487">não</span><span class="sxs-lookup"><span data-stu-id="86785-487">no</span></span>             | <span data-ttu-id="86785-488">não</span><span class="sxs-lookup"><span data-stu-id="86785-488">no</span></span>           |
| <span data-ttu-id="86785-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="86785-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="86785-490">não</span><span class="sxs-lookup"><span data-stu-id="86785-490">no</span></span>             | <span data-ttu-id="86785-491">não</span><span class="sxs-lookup"><span data-stu-id="86785-491">no</span></span>           |
| <span data-ttu-id="86785-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="86785-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="86785-493">não</span><span class="sxs-lookup"><span data-stu-id="86785-493">no</span></span>             | <span data-ttu-id="86785-494">não</span><span class="sxs-lookup"><span data-stu-id="86785-494">no</span></span>           |
| <span data-ttu-id="86785-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="86785-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="86785-496">não</span><span class="sxs-lookup"><span data-stu-id="86785-496">no</span></span>             | <span data-ttu-id="86785-497">não</span><span class="sxs-lookup"><span data-stu-id="86785-497">no</span></span>           |
| <span data-ttu-id="86785-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="86785-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="86785-499">não</span><span class="sxs-lookup"><span data-stu-id="86785-499">no</span></span>             | <span data-ttu-id="86785-500">não</span><span class="sxs-lookup"><span data-stu-id="86785-500">no</span></span>           |
| <span data-ttu-id="86785-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="86785-501">msdyn_start</span></span>                                      | <span data-ttu-id="86785-502">não</span><span class="sxs-lookup"><span data-stu-id="86785-502">no</span></span>             | <span data-ttu-id="86785-503">não</span><span class="sxs-lookup"><span data-stu-id="86785-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="86785-504">Project</span><span class="sxs-lookup"><span data-stu-id="86785-504">Project</span></span>

| <span data-ttu-id="86785-505">**Nome lógico**</span><span class="sxs-lookup"><span data-stu-id="86785-505">**Logical name**</span></span>                       | <span data-ttu-id="86785-506">**Pode criar**</span><span class="sxs-lookup"><span data-stu-id="86785-506">**Can create**</span></span> | <span data-ttu-id="86785-507">**Pode editar**</span><span class="sxs-lookup"><span data-stu-id="86785-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="86785-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="86785-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="86785-509">não</span><span class="sxs-lookup"><span data-stu-id="86785-509">no</span></span>             | <span data-ttu-id="86785-510">não</span><span class="sxs-lookup"><span data-stu-id="86785-510">no</span></span>           |
| <span data-ttu-id="86785-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="86785-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="86785-512">não</span><span class="sxs-lookup"><span data-stu-id="86785-512">no</span></span>             | <span data-ttu-id="86785-513">não</span><span class="sxs-lookup"><span data-stu-id="86785-513">no</span></span>           |
| <span data-ttu-id="86785-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="86785-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="86785-515">não</span><span class="sxs-lookup"><span data-stu-id="86785-515">no</span></span>             | <span data-ttu-id="86785-516">não</span><span class="sxs-lookup"><span data-stu-id="86785-516">no</span></span>           |
| <span data-ttu-id="86785-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="86785-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="86785-518">não</span><span class="sxs-lookup"><span data-stu-id="86785-518">no</span></span>             | <span data-ttu-id="86785-519">não</span><span class="sxs-lookup"><span data-stu-id="86785-519">no</span></span>           |
| <span data-ttu-id="86785-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="86785-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="86785-521">não</span><span class="sxs-lookup"><span data-stu-id="86785-521">no</span></span>             | <span data-ttu-id="86785-522">não</span><span class="sxs-lookup"><span data-stu-id="86785-522">no</span></span>           |
| <span data-ttu-id="86785-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="86785-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="86785-524">não</span><span class="sxs-lookup"><span data-stu-id="86785-524">no</span></span>             | <span data-ttu-id="86785-525">não</span><span class="sxs-lookup"><span data-stu-id="86785-525">no</span></span>           |
| <span data-ttu-id="86785-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="86785-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="86785-527">sim</span><span class="sxs-lookup"><span data-stu-id="86785-527">yes</span></span>            | <span data-ttu-id="86785-528">não</span><span class="sxs-lookup"><span data-stu-id="86785-528">no</span></span>           |
| <span data-ttu-id="86785-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="86785-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="86785-530">sim</span><span class="sxs-lookup"><span data-stu-id="86785-530">yes</span></span>            | <span data-ttu-id="86785-531">não</span><span class="sxs-lookup"><span data-stu-id="86785-531">no</span></span>           |
| <span data-ttu-id="86785-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="86785-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="86785-533">sim</span><span class="sxs-lookup"><span data-stu-id="86785-533">yes</span></span>            | <span data-ttu-id="86785-534">não</span><span class="sxs-lookup"><span data-stu-id="86785-534">no</span></span>           |
| <span data-ttu-id="86785-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="86785-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="86785-536">não</span><span class="sxs-lookup"><span data-stu-id="86785-536">no</span></span>             | <span data-ttu-id="86785-537">não</span><span class="sxs-lookup"><span data-stu-id="86785-537">no</span></span>           |
| <span data-ttu-id="86785-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="86785-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="86785-539">não</span><span class="sxs-lookup"><span data-stu-id="86785-539">no</span></span>             | <span data-ttu-id="86785-540">não</span><span class="sxs-lookup"><span data-stu-id="86785-540">no</span></span>           |
| <span data-ttu-id="86785-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="86785-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="86785-542">não</span><span class="sxs-lookup"><span data-stu-id="86785-542">no</span></span>             | <span data-ttu-id="86785-543">não</span><span class="sxs-lookup"><span data-stu-id="86785-543">no</span></span>           |
| <span data-ttu-id="86785-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="86785-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="86785-545">não</span><span class="sxs-lookup"><span data-stu-id="86785-545">no</span></span>             | <span data-ttu-id="86785-546">não</span><span class="sxs-lookup"><span data-stu-id="86785-546">no</span></span>           |
| <span data-ttu-id="86785-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="86785-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="86785-548">não</span><span class="sxs-lookup"><span data-stu-id="86785-548">no</span></span>             | <span data-ttu-id="86785-549">não</span><span class="sxs-lookup"><span data-stu-id="86785-549">no</span></span>           |
| <span data-ttu-id="86785-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="86785-550">msdyn_duration</span></span>                         | <span data-ttu-id="86785-551">não</span><span class="sxs-lookup"><span data-stu-id="86785-551">no</span></span>             | <span data-ttu-id="86785-552">não</span><span class="sxs-lookup"><span data-stu-id="86785-552">no</span></span>           |
| <span data-ttu-id="86785-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="86785-553">msdyn_effort</span></span>                           | <span data-ttu-id="86785-554">não</span><span class="sxs-lookup"><span data-stu-id="86785-554">no</span></span>             | <span data-ttu-id="86785-555">não</span><span class="sxs-lookup"><span data-stu-id="86785-555">no</span></span>           |
| <span data-ttu-id="86785-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="86785-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="86785-557">não</span><span class="sxs-lookup"><span data-stu-id="86785-557">no</span></span>             | <span data-ttu-id="86785-558">não</span><span class="sxs-lookup"><span data-stu-id="86785-558">no</span></span>           |
| <span data-ttu-id="86785-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="86785-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="86785-560">não</span><span class="sxs-lookup"><span data-stu-id="86785-560">no</span></span>             | <span data-ttu-id="86785-561">não</span><span class="sxs-lookup"><span data-stu-id="86785-561">no</span></span>           |
| <span data-ttu-id="86785-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="86785-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="86785-563">não</span><span class="sxs-lookup"><span data-stu-id="86785-563">no</span></span>             | <span data-ttu-id="86785-564">não</span><span class="sxs-lookup"><span data-stu-id="86785-564">no</span></span>           |
| <span data-ttu-id="86785-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="86785-565">msdyn_finish</span></span>                           | <span data-ttu-id="86785-566">sim</span><span class="sxs-lookup"><span data-stu-id="86785-566">yes</span></span>            | <span data-ttu-id="86785-567">sim</span><span class="sxs-lookup"><span data-stu-id="86785-567">yes</span></span>          |
| <span data-ttu-id="86785-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="86785-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="86785-569">não</span><span class="sxs-lookup"><span data-stu-id="86785-569">no</span></span>             | <span data-ttu-id="86785-570">não</span><span class="sxs-lookup"><span data-stu-id="86785-570">no</span></span>           |
| <span data-ttu-id="86785-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="86785-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="86785-572">não</span><span class="sxs-lookup"><span data-stu-id="86785-572">no</span></span>             | <span data-ttu-id="86785-573">não</span><span class="sxs-lookup"><span data-stu-id="86785-573">no</span></span>           |
| <span data-ttu-id="86785-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="86785-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="86785-575">não</span><span class="sxs-lookup"><span data-stu-id="86785-575">no</span></span>             | <span data-ttu-id="86785-576">não</span><span class="sxs-lookup"><span data-stu-id="86785-576">no</span></span>           |
| <span data-ttu-id="86785-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="86785-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="86785-578">não</span><span class="sxs-lookup"><span data-stu-id="86785-578">no</span></span>             | <span data-ttu-id="86785-579">não</span><span class="sxs-lookup"><span data-stu-id="86785-579">no</span></span>           |
| <span data-ttu-id="86785-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="86785-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="86785-581">não</span><span class="sxs-lookup"><span data-stu-id="86785-581">no</span></span>             | <span data-ttu-id="86785-582">não</span><span class="sxs-lookup"><span data-stu-id="86785-582">no</span></span>           |
| <span data-ttu-id="86785-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="86785-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="86785-584">não</span><span class="sxs-lookup"><span data-stu-id="86785-584">no</span></span>             | <span data-ttu-id="86785-585">não</span><span class="sxs-lookup"><span data-stu-id="86785-585">no</span></span>           |
| <span data-ttu-id="86785-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="86785-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="86785-587">não</span><span class="sxs-lookup"><span data-stu-id="86785-587">no</span></span>             | <span data-ttu-id="86785-588">não</span><span class="sxs-lookup"><span data-stu-id="86785-588">no</span></span>           |
| <span data-ttu-id="86785-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="86785-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="86785-590">não</span><span class="sxs-lookup"><span data-stu-id="86785-590">no</span></span>             | <span data-ttu-id="86785-591">não</span><span class="sxs-lookup"><span data-stu-id="86785-591">no</span></span>           |
| <span data-ttu-id="86785-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="86785-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="86785-593">não</span><span class="sxs-lookup"><span data-stu-id="86785-593">no</span></span>             | <span data-ttu-id="86785-594">não</span><span class="sxs-lookup"><span data-stu-id="86785-594">no</span></span>           |
| <span data-ttu-id="86785-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="86785-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="86785-596">não</span><span class="sxs-lookup"><span data-stu-id="86785-596">no</span></span>             | <span data-ttu-id="86785-597">não</span><span class="sxs-lookup"><span data-stu-id="86785-597">no</span></span>           |
| <span data-ttu-id="86785-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="86785-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="86785-599">não</span><span class="sxs-lookup"><span data-stu-id="86785-599">no</span></span>             | <span data-ttu-id="86785-600">não</span><span class="sxs-lookup"><span data-stu-id="86785-600">no</span></span>           |
| <span data-ttu-id="86785-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="86785-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="86785-602">não</span><span class="sxs-lookup"><span data-stu-id="86785-602">no</span></span>             | <span data-ttu-id="86785-603">não</span><span class="sxs-lookup"><span data-stu-id="86785-603">no</span></span>           |
| <span data-ttu-id="86785-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="86785-604">msdyn_progress</span></span>                         | <span data-ttu-id="86785-605">não</span><span class="sxs-lookup"><span data-stu-id="86785-605">no</span></span>             | <span data-ttu-id="86785-606">não</span><span class="sxs-lookup"><span data-stu-id="86785-606">no</span></span>           |
| <span data-ttu-id="86785-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="86785-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="86785-608">não</span><span class="sxs-lookup"><span data-stu-id="86785-608">no</span></span>             | <span data-ttu-id="86785-609">não</span><span class="sxs-lookup"><span data-stu-id="86785-609">no</span></span>           |
| <span data-ttu-id="86785-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="86785-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="86785-611">não</span><span class="sxs-lookup"><span data-stu-id="86785-611">no</span></span>             | <span data-ttu-id="86785-612">não</span><span class="sxs-lookup"><span data-stu-id="86785-612">no</span></span>           |
| <span data-ttu-id="86785-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="86785-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="86785-614">não</span><span class="sxs-lookup"><span data-stu-id="86785-614">no</span></span>             | <span data-ttu-id="86785-615">não</span><span class="sxs-lookup"><span data-stu-id="86785-615">no</span></span>           |
| <span data-ttu-id="86785-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="86785-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="86785-617">não</span><span class="sxs-lookup"><span data-stu-id="86785-617">no</span></span>             | <span data-ttu-id="86785-618">não</span><span class="sxs-lookup"><span data-stu-id="86785-618">no</span></span>           |
| <span data-ttu-id="86785-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="86785-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="86785-620">não</span><span class="sxs-lookup"><span data-stu-id="86785-620">no</span></span>             | <span data-ttu-id="86785-621">não</span><span class="sxs-lookup"><span data-stu-id="86785-621">no</span></span>           |
| <span data-ttu-id="86785-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="86785-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="86785-623">não</span><span class="sxs-lookup"><span data-stu-id="86785-623">no</span></span>             | <span data-ttu-id="86785-624">não</span><span class="sxs-lookup"><span data-stu-id="86785-624">no</span></span>           |
| <span data-ttu-id="86785-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="86785-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="86785-626">não</span><span class="sxs-lookup"><span data-stu-id="86785-626">no</span></span>             | <span data-ttu-id="86785-627">não</span><span class="sxs-lookup"><span data-stu-id="86785-627">no</span></span>           |
| <span data-ttu-id="86785-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="86785-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="86785-629">não</span><span class="sxs-lookup"><span data-stu-id="86785-629">no</span></span>             | <span data-ttu-id="86785-630">não</span><span class="sxs-lookup"><span data-stu-id="86785-630">no</span></span>           |
| <span data-ttu-id="86785-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="86785-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="86785-632">não</span><span class="sxs-lookup"><span data-stu-id="86785-632">no</span></span>             | <span data-ttu-id="86785-633">não</span><span class="sxs-lookup"><span data-stu-id="86785-633">no</span></span>           |
| <span data-ttu-id="86785-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="86785-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="86785-635">não</span><span class="sxs-lookup"><span data-stu-id="86785-635">no</span></span>             | <span data-ttu-id="86785-636">não</span><span class="sxs-lookup"><span data-stu-id="86785-636">no</span></span>           |
| <span data-ttu-id="86785-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="86785-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="86785-638">não</span><span class="sxs-lookup"><span data-stu-id="86785-638">no</span></span>             | <span data-ttu-id="86785-639">não</span><span class="sxs-lookup"><span data-stu-id="86785-639">no</span></span>           |
| <span data-ttu-id="86785-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="86785-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="86785-641">não</span><span class="sxs-lookup"><span data-stu-id="86785-641">no</span></span>             | <span data-ttu-id="86785-642">não</span><span class="sxs-lookup"><span data-stu-id="86785-642">no</span></span>           |
| <span data-ttu-id="86785-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="86785-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="86785-644">não</span><span class="sxs-lookup"><span data-stu-id="86785-644">no</span></span>             | <span data-ttu-id="86785-645">não</span><span class="sxs-lookup"><span data-stu-id="86785-645">no</span></span>           |
| <span data-ttu-id="86785-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="86785-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="86785-647">não</span><span class="sxs-lookup"><span data-stu-id="86785-647">no</span></span>             | <span data-ttu-id="86785-648">não</span><span class="sxs-lookup"><span data-stu-id="86785-648">no</span></span>           |
| <span data-ttu-id="86785-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="86785-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="86785-650">não</span><span class="sxs-lookup"><span data-stu-id="86785-650">no</span></span>             | <span data-ttu-id="86785-651">não</span><span class="sxs-lookup"><span data-stu-id="86785-651">no</span></span>           |
| <span data-ttu-id="86785-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="86785-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="86785-653">não</span><span class="sxs-lookup"><span data-stu-id="86785-653">no</span></span>             | <span data-ttu-id="86785-654">não</span><span class="sxs-lookup"><span data-stu-id="86785-654">no</span></span>           |
| <span data-ttu-id="86785-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="86785-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="86785-656">não</span><span class="sxs-lookup"><span data-stu-id="86785-656">no</span></span>             | <span data-ttu-id="86785-657">não</span><span class="sxs-lookup"><span data-stu-id="86785-657">no</span></span>           |
| <span data-ttu-id="86785-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="86785-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="86785-659">não</span><span class="sxs-lookup"><span data-stu-id="86785-659">no</span></span>             | <span data-ttu-id="86785-660">não</span><span class="sxs-lookup"><span data-stu-id="86785-660">no</span></span>           |
| <span data-ttu-id="86785-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="86785-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="86785-662">não</span><span class="sxs-lookup"><span data-stu-id="86785-662">no</span></span>             | <span data-ttu-id="86785-663">não</span><span class="sxs-lookup"><span data-stu-id="86785-663">no</span></span>           |
| <span data-ttu-id="86785-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="86785-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="86785-665">não</span><span class="sxs-lookup"><span data-stu-id="86785-665">no</span></span>             | <span data-ttu-id="86785-666">não</span><span class="sxs-lookup"><span data-stu-id="86785-666">no</span></span>           |
| <span data-ttu-id="86785-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="86785-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="86785-668">não</span><span class="sxs-lookup"><span data-stu-id="86785-668">no</span></span>             | <span data-ttu-id="86785-669">não</span><span class="sxs-lookup"><span data-stu-id="86785-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="86785-670">Problemas conhecidos e de limitações</span><span class="sxs-lookup"><span data-stu-id="86785-670">Limitations and known issues</span></span>
<span data-ttu-id="86785-671">Segue-se uma lista de limitações e questões conhecidas:</span><span class="sxs-lookup"><span data-stu-id="86785-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="86785-672">As APIs de agenda só podem ser utilizadas pelos **Utilizadores com licença de projeto da Microsoft.**</span><span class="sxs-lookup"><span data-stu-id="86785-672">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="86785-673">Não podem ser usadas por:</span><span class="sxs-lookup"><span data-stu-id="86785-673">They can't be used by:</span></span>
    - <span data-ttu-id="86785-674">Utilizadores da aplicação</span><span class="sxs-lookup"><span data-stu-id="86785-674">Application users</span></span>
    - <span data-ttu-id="86785-675">Utilizadores do sistema</span><span class="sxs-lookup"><span data-stu-id="86785-675">System users</span></span>
    - <span data-ttu-id="86785-676">Utilizadores de integração</span><span class="sxs-lookup"><span data-stu-id="86785-676">Integration users</span></span>
    - <span data-ttu-id="86785-677">Outros utilizadores que não têm a licença necessária</span><span class="sxs-lookup"><span data-stu-id="86785-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="86785-678">Cada **OperationSet** só pode ter um máximo de 100 operações.</span><span class="sxs-lookup"><span data-stu-id="86785-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="86785-679">Cada utilizador só pode ter um máximo de 10 **OperationSet** abertas.</span><span class="sxs-lookup"><span data-stu-id="86785-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="86785-680">O Project Operations suporta atualmente um máximo de 500 tarefas totais num projeto.</span><span class="sxs-lookup"><span data-stu-id="86785-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="86785-681">O estado de falha e os registos de avarias do **OperationSet** não estão atualmente disponíveis.</span><span class="sxs-lookup"><span data-stu-id="86785-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- <span data-ttu-id="86785-682">As APIs da agenda estão em pré-visualização pública.</span><span class="sxs-lookup"><span data-stu-id="86785-682">Schedule APIs are in Public preview.</span></span> <span data-ttu-id="86785-683">A utilização destas APIs num ambiente de Produção não é suportada pela Microsoft.</span><span class="sxs-lookup"><span data-stu-id="86785-683">Using these APIs in a Production environment isn't supported by Microsoft.</span></span>
- [<span data-ttu-id="86785-684">Limites e fronteiras em projetos e tarefas</span><span class="sxs-lookup"><span data-stu-id="86785-684">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="86785-685">Processamento de erros</span><span class="sxs-lookup"><span data-stu-id="86785-685">Error handling</span></span>

   - <span data-ttu-id="86785-686">Para rever os erros gerados a partir dos Conjuntos de Operação, aceda a **Configurações** \> **Integração de Agendamento** \> **Conjuntos de operações**.</span><span class="sxs-lookup"><span data-stu-id="86785-686">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="86785-687">Para rever os erros gerados a partir do Serviço de Agendamento de Projetos, aceda a **Definições** \> **Integração de agendamento** \> **Registos de erros PSS**.</span><span class="sxs-lookup"><span data-stu-id="86785-687">To review errors generated from the Project Scheduling Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="86785-688">Cenário de exemplo</span><span class="sxs-lookup"><span data-stu-id="86785-688">Sample scenario</span></span>

<span data-ttu-id="86785-689">Neste cenário, irá criar um projeto, um membro da equipa, quatro tarefas e duas atribuições de recursos.</span><span class="sxs-lookup"><span data-stu-id="86785-689">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="86785-690">Em seguida, atualizará uma tarefa, atualizará o projeto, eliminará uma tarefa, eliminará uma atribuição de recursos e criará uma dependência de tarefas.</span><span class="sxs-lookup"><span data-stu-id="86785-690">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

```csharp
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
var task4 = GetTask("4ZZ", projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment("R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

var assignment1Response = CallPssCreateAction(assignment1, operationSetId);
var assignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

var assignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a><span data-ttu-id="86785-691">Amostras adicionais</span><span class="sxs-lookup"><span data-stu-id="86785-691">Additional samples</span></span>

```csharp
#region Call actions --- Sample code ----

/// <summary>
/// Calls the action to create an operationSet
/// </summary>
/// <param name="projectId">project id for the operations to be included in this operationSet</param>
/// <param name="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
private string CallCreateOperationSetAction(Guid projectId, string description)
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
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>

private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet Id</param>
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
/// </summary>
/// <param name="recordId">Id of the record to be deleted</param>
/// <param name="entityLogicalName">Entity logical name of the record</param>
/// <param name="operationSetId">OperationSet Id</param>
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
/// </summary>
/// <param name="operationSetId">operationSet id</param>
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
/// <param name="operationSetId">operationSet id</param>
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
/// <param name="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1");
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);
    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <param name="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
private string CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject<OperationSetResponse>((string)orgResponse.Results["OperationSetResponse"]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet("msdyn_project", "msdyn_name");
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
    task["msdyn_effort"] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
    task["new_custom1"] = "Just my test";
    task["new_age"] = 98;
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
public class OperationSetResponse
{
[DataMember(Name = "operationSetId")]
public Guid OperationSetId { get; set; }

[DataMember(Name = "operationSetDetailId")]
public Guid OperationSetDetailId { get; set; }

[DataMember(Name = "operationType")]
public string OperationType { get; set; }

[DataMember(Name = "recordId")]
public string RecordId { get; set; }

[DataMember(Name = "correlationId")]
public string CorrelationId { get; set; }
}

#endregion
```
