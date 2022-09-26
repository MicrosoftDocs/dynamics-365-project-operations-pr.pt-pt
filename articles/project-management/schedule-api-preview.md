---
title: Utilizar APIs de Agenda do Project para executar operações com entidades de Agendamento
description: Este artigo fornece informações e amostras para utilizar APIs da agenda do Projeto.
author: sigitac
ms.date: 01/13/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 159d395efff98f2af780e5ed1e5ab3d6483cba89
ms.sourcegitcommit: b1c26ea57be721c5b0b1a33f2de0380ad102648f
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 09/20/2022
ms.locfileid: "9541139"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Utilizar APIs de Agenda do Project para executar operações com entidades de Agendamento

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_


**Entidades de agendamento**

As APIs de agenda do Project permitem executar operações de criação, atualização e eliminação com **Entidades de agendamento**. Estas entidades são geridas através do motor de Agendamento em Projeto para a web. Operações de Criar, atualizar e apagar com **Entidades de agendamento** foram restringidas em lançamentos Dynamics 365 Project Operations anteriores.

A tabela seguinte fornece uma lista completa das entidades de agendamento do Project.

| **Nome da entidade**         | **Nome lógico da entidade**     |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Tarefa de Projeto            | msdyn_projecttask           |
| Dependência de Tarefa de Projeto | msdyn_projecttaskdependency |
| Atribuição de Recurso     | msdyn_resourceassignment    |
| Registo do Projeto          | msdyn_projectbucket         |
| Membro da Equipa do Projeto     | msdyn_projectteam           |
| Listas de Verificação do Projeto      | msdyn_projectchecklist      |
| Etiqueta do Projeto           | msdyn_projectlabel          |
| Tarefa do Projeto para Etiquetar   | msdyn_projecttasktolabel    |
| Sprint do Projeto          | msdyn_projectsprint         |

**OperationSet**

OperationSet é um padrão de unidade de trabalho que pode ser usado quando vários pedidos de impacto de programação devem ser processados dentro de uma transação.

**APIs de agenda do Project**

Segue-se uma lista das APIs de agenda do Project atuais.

| **API**                                 | Description                                                                                                                       |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| **msdyn_CreateProjectV1**               | Esta API é utilizada para criar um projeto. O projeto e o registo de projeto predefinido são criados imediatamente.                         |
| **msdyn_CreateTeamMemberV1**            | Esta API é utilizada para criar um membro da equipa do projeto. O registo de membros da equipa é criado imediatamente.                                  |
| **msdyn_CreateOperationSetV1**          | Esta API é utilizada para agendar vários pedidos que devem ser realizados dentro de uma transação.                                        |
| **msdyn_PssCreateV1**                   | Esta API é utilizada para criar uma entidade. A entidade pode ser qualquer uma das entidades de agendamento do Project que suportam a operação de criação. |
| **msdyn_PssUpdateV1**                   | Esta API é utilizada para atualizar uma entidade. A entidade pode ser qualquer uma das entidades de agendamento do Project que suportam a operação de atualização  |
| **msdyn_PssDeleteV1**                   | Esta API é utilizada para eliminar uma entidade. A entidade pode ser qualquer uma das entidades de agendamento do Project que suportam a operação de eliminação. |
| **msdyn_ExecuteOperationSetV1**         | Esta API é utilizada para executar todas as operações no âmbito do conjunto de operações.                                                 |
| **msdyn_PssUpdateResourceAssignmentV1** | Esta API é utilizada para atualizar um contorno de trabalho planeado da Atribuição de Recursos.                                                        |



**Utilizar APIs de agenda do Project com OperationSet**

Como os registos com **CreateProjectV1** e **CreateTeamMemberV1** são criados imediatamente, estas APIs não podem ser utilizadas diretamente no **OperationSet**. No entanto, pode utilizar a API para criar registos necessários, criar um **OperationSet** e, em seguida, utilizar estes registos pré-criados no **OperationSet**.

**Operações suportadas**

| **Entidade de agendamento**   | **Criar** | **Update** | **Delete** | **Considerações importantes**                                                                                                                                                                                                                                                                                                                            |
|-------------------------|------------|------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tarefa de projeto            | Sim        | Sim        | Sim        | Os campos **Progresso**, **EffortCompleted** e **EffortRemaining** podem ser editados no Project for the Web, mas não podem ser editados no Project Operations.                                                                                                                                                                                             |
| Dependência de tarefa de projeto | Sim        | No         | Sim        | Os registos de dependência de tarefas do projeto não estão atualizados. Em vez disso, um registo antigo pode ser apagado e pode ser criado um novo registo.                                                                                                                                                                                                                                 |
| Atribuição de recurso     | Sim        | Sim\*      | Sim        | As operações com os seguintes campos não são suportadas: **BookableResourceID**, **Esforço**, **EffortCompleted**, **EffortRemaining** e **PlannedWork**. Os registos de atribuição de recursos não estão atualizados. Em vez disso, o registo antigo pode ser apagado e pode ser criado um novo registo. Foi fornecida uma API separada para atualizar os contornos da Atribuição de Recursos. |
| Registo do projeto          | Sim        | Sim        | Sim        | O registo predefinido é criado utilizando a API **CreateProjectV1**. O suporte para criação e eliminação de registos de projeto foi adicionado na Versão 16 da atualização.                                                                                                                                                                                                   |
| Membro da equipa do projeto     | Sim        | Sim        | Sim        | Para a operação de criação, utilize a API **CreateTeamMemberV1**.                                                                                                                                                                                                                                                                                           |
| Project                 | Sim        | Sim        |            | As operações com os seguintes campos não são suportadas: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Esforço**, **EffortCompleted**, **EffortRemaining**, **Progresso**, **Terminar**, **TaskEarliestStart** e **Duração**.                                                                                       |
| Listas de Verificação do Projeto      | Sim        | Sim        | Sim        |                                                                                                                                                                                                                                                                                                                                                         |
| Etiqueta do Projeto           | No         | Sim        | No         | É possível alterar nomes de etiquetas. Esta caraterística só está disponível para o Project for the Web                                                                                                                                                                                                                                                                      |
| Tarefa do Projeto para Etiquetar   | Sim        | No         | Sim        | Esta caraterística só está disponível para o Project for the Web                                                                                                                                                                                                                                                                                                  |
| Sprint do Projeto          | Sim        | Sim        | Sim        | O campo **Iniciar** tem de ter uma data anterior à do campo **Concluir**. As sprints para o mesmo projeto não podem sobrepor-se entre si. Esta caraterística só está disponível para o Project for the Web                                                                                                                                                                    |




A propriedade ID é opcional. Se for fornecido, o sistema tenta usá-lo e abre uma exceção se não puder ser usado. Se não for fornecido, o sistema irá gerá-lo.

**Problemas conhecidos e de limitações**

Segue-se uma lista de limitações e questões conhecidas:

-   As API de Agenda do projeto só podem ser utilizadas pelos **Utilizadores com Licença do Microsoft Project**. Não podem ser usadas por:
    -   Utilizadores da aplicação
    -   Utilizadores do sistema
    -   Utilizadores de integração
    -   Outros utilizadores que não têm a licença necessária
-   Cada **OperationSet** só pode ter um máximo de 100 operações.
-   Cada utilizador só pode ter um máximo de 10 **OperationSet** abertas.
-   O Project Operations suporta atualmente um máximo de 500 tarefas totais num projeto.
-   Cada operação Atualizar Contorno de Atribuição de Recursos conta como uma única operação.
-   Cada lista de contornos atualizados pode conter um máximo de 100 setores de tempo.
-   O estado de falha e os registos de avarias do **OperationSet** não estão atualmente disponíveis.
-   Existe um máximo de 400 sprints por projeto.
-   [Limites e fronteiras em projetos e tarefas](/project-for-the-web/project-for-the-web-limits-and-boundaries).
-   Atualmente, as etiquetas só estão disponíveis para o Project for the Web.

**Processamento de erros**

-   Para rever os erros gerados a partir dos Conjuntos de Operação, aceda a **Configurações** \> **Integração de Agendamento** \> **Conjuntos de operações**.
-   Para rever os erros gerados a partir do Serviço de agendamento do Project, vá para **Definições** \> **Integração de Agenda** \> **Registos de Erros de PSS**.

**Editar Contornos da Atribuição de Recursos**

Ao contrário de todas as outras APIs de agendamento de projetos que atualizam uma entidade, a API de contorno de atribuição de recursos é a única responsável por atualizações a um campo único campo, msdyn_plannedwork, numa única entidade.

O modo de agendamento dado é:

-   **unidades fixas**
-   o calendário do projeto é 9-5p é 9-5pst, Seg., Ter., Qui., Sexta-feira (SEM TRABALHO ÀS QUARTA-FEIRAS)
-   e o calendário de recursos é 9-1p PST Seg. a Sex.

Esta atribuição é para uma semana, quatro horas por dia. Isto porque o calendário de recursos é das 9-1 PST ou quatro horas por dia.

| &nbsp;     | Tarefa | Data de Início | Data de Fim  | Quantidade | 13/6/2022 | 14/6/2022 | 15/6/2022 | 16/6/2022 | 17/6/2022 |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| Trabalhador 9-1 |  T1  | 13/6/2022  | 17/6/2022 | 20       | 4         | 4         | 4         | 4         | 4         |

Por exemplo, se quiser que o trabalhador trabalhe só três horas por dia esta semana e permita uma hora para outras tarefas.

#### <a name="updatedcontours-sample-payload"></a>Payload de amostra UpdatedContours:

```json
[{

"minutes":900.0,

"start":"2022-06-13T00:00:00-07:00",

"end":"2022-06-18T00:00:00-07:00"

}]
```

Esta é a atribuição após a execução da API de Atualizar Agendamento de Contorno.

| &nbsp;     | Tarefa | Data de Início | Data de Fim  | Quantidade | 13/6/2022 | 14/6/2022 | 15/6/2022 | 16/6/2022 | 17/6/2022 |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| Trabalhador 9-1 | T1   | 13/6/2022  | 17/6/2022 | 15       | 3         | 3         | 3         | 3         | 3         |


**Cenário de exemplo**

Neste cenário, irá criar um projeto, um membro da equipa, quatro tarefas e duas atribuições de recursos. Em seguida, atualizará uma tarefa, atualizará o projeto, eliminará uma tarefa, eliminará uma atribuição de recursos e criará uma dependência de tarefas.

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

** Amostras adicionais

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
