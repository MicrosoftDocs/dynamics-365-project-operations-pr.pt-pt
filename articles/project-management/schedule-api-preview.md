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
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Utilizar APIs de Agenda para realizar operações com entidades de agendamento

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

> [!IMPORTANT] 
> Algumas ou todas as funcionalidades anotadas neste tópico estão disponíveis como parte de uma versão de pré-visualização. O conteúdo e a funcionalidade estão sujeitos a alterações. 

## <a name="scheduling-entities"></a>Entidades de agendamento

Agendar APIs fornece a capacidade de executar operações de criar, atualizar e apagar com **Entidades de agendamento**. Estas entidades são geridas através do motor de Agendamento em Projeto para a web. Operações de Criar, atualizar e apagar com **Entidades de agendamento** foram restringidas em lançamentos Dynamics 365 Project Operations anteriores.

A tabela seguinte apresenta uma lista completa das **Entidades de Agendamento**.

| Nome da entidade  | Nome lógico da entidade |
| --- | --- |
| Project | msdyn_project |
| Tarefa de Projeto  | msdyn_projecttask  |
| Dependência de Tarefa de Projeto  | msdyn_projecttaskdependency  |
| Atribuição de Recurso | msdyn_resourceassignment |
| Registo do Projeto  | msdyn_projectbucket |
| Membro da Equipa do Projeto | msdyn_projectteam |

## <a name="operationset"></a>OperationSet

OperationSet é um padrão de unidade de trabalho que pode ser usado quando vários pedidos de impacto de programação devem ser processados dentro de uma transação.

## <a name="schedule-apis"></a>ApIs de agenda

Segue-se uma lista das APIs de agenda.

- **msdyn_CreateProjectV1**: Esta API pode ser usada para criar um projeto. O projeto e registo de projeto padrão é criado imediatamente.
- **msdyn_CreateTeamMemberV1**: Esta API pode ser usada para criar um membro da equipa de projeto. O registo de membros da equipa é criado imediatamente.
- **msdyn_CreateOperationSetV1**: Esta API pode ser utilizada para agendar vários pedidos que devem ser realizados dentro de uma transação.
- **msdyn_PSSCreateV1**: Esta API pode ser usada para criar uma entidade. A entidade pode ser qualquer uma das entidades de Agendamento que apoiam a operação de criação.
- **msdyn_PSSUpdateV1**: Esta API pode ser usada para atualizar uma entidade. A entidade pode ser qualquer uma das entidades de Agendamento que apoiam a operação de atualização.
- **msdyn_PSSDeleteV1**: Esta API pode ser usada para eliminar uma entidade. A entidade pode ser qualquer uma das entidades de Agendamento que apoiam a operação de eliminação.
- **msdyn_ExecuteOperationSetV1**: Esta API é utilizada para executar todas as operações no âmbito do conjunto de operações.

## <a name="using-schedule-apis-with-operationset"></a>Utilização de APIs de agenda com OperationSet

Como os registos com **CreateProjectV1** e **CreateTeamMemberV1** são criados imediatamente, estas APIs não podem ser utilizadas diretamente no **OperationSet**. No entanto, pode utilizar a API para criar registos necessários, criar um **OperationSet** e, em seguida, utilizar estes registos pré-criados no **OperationSet**.

## <a name="supported-operations"></a>Operações suportadas

| Entidade de agendamento | Criar | Actualizar | Delete | Considerações importantes |
| --- | --- | --- | --- | --- |
Tarefa de projeto | Sim | Sim | Sim | Nenhuma |
| Dependência de tarefa de projeto | Sim | Sim | | Os registos de dependência de tarefas do projeto não estão atualizados. Em vez disso, um registo antigo pode ser apagado e um novo recorde pode ser criado. |
| Atribuição de recurso | Sim | Sim | | As operações com os seguintes campos não são suportadas: **BookableResourceID**, **Esforço**, **EffortCompleted**, **EffortRemaining** e **PlannedWork**. Os registos de atribuição de recursos não estão atualizados. Em vez disso, o registo antigo pode ser apagado e um novo recorde pode ser criado. |
| Registo do projeto | N/D | N/D | N/D | O registo predefinido é criado utilizando a API **CreateProjectV1**. |
| Membro da equipa do projeto | Sim | Sim | Sim | Para a operação de criação, utilize a API **CreateTeamMemberV1**. |
| Project | Sim | Sim | N/D | As operações com os seguintes campos não são suportadas: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Esforço**, **EffortCompleted**, **EffortRemaining**, **Progresso**, **Terminar**, **TaskEarliestStart** e **Duração**. |

Estas APIs podem ser chamadas com objetos de entidade que incluem campos personalizados.

A propriedade ID é opcional. Se for fornecido, o sistema tenta usá-lo e abre uma exceção se não puder ser usado. Se não for fornecido, o sistema irá gerá-lo.

## <a name="limitations-and-known-issues"></a>Problemas conhecidos e de limitações
Segue-se uma lista de limitações e questões conhecidas:

- As APIs de agenda só podem ser utilizadas pelos **Utilizadores com licença de projeto da Microsoft.** Não podem ser usadas por:
    - Utilizadores da aplicação
    - Utilizadores do sistema
    - Utilizadores de integração
    - Outros utilizadores que não têm a licença necessária
- Cada **OperationSet** só pode ter um máximo de 100 operações.
- Cada utilizador só pode ter um máximo de 10 **OperationSet** abertas.
- O Project Operations suporta atualmente um máximo de 500 tarefas totais num projeto.
- O estado de falha e os registos de avarias do **OperationSet** não estão atualmente disponíveis.
- As APIs da agenda estão em pré-visualização pública. A utilização destas APIs num ambiente de Produção não é suportada pela Microsoft.

## <a name="sample-scenario"></a>Cenário de exemplo

Neste cenário, irá criar um projeto, um membro da equipa, quatro tarefas e duas atribuições de recursos. Em seguida, atualizará uma tarefa, atualizará o projeto, eliminará uma tarefa, eliminará uma atribuição de recursos e criará uma dependência de tarefas.

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

## <a name="additional-samples"></a>Amostras adicionais

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
