---
title: Registos de agendamento de projetos
description: Este artigo fornece informações e exemplos que o ajudarão a usar os registos de Agendamento de Projetos para monitorizar falhas relacionadas com o Serviço de Agendamento de Projetos e APIs de Agendamento de Projetos.
author: ruhercul
ms.date: 11/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: c57419642e90e4def01f2cd2474c9e82dc162b86
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923709"
---
# <a name="project-scheduling-logs"></a>Registos de agendamento de projetos

_**Aplicável a:** Project Operations para cenários baseados em recursos/itens não existentes em stock, implementação Lite - da transação à fatura pró-forma_, _Project for the Web_

O Microsoft Dynamics 365 Project Operations utiliza o [Project for the Web](https://support.microsoft.com/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5) como o seu motor de agendamento primário. Em vez de utilizar as interfaces de programação de aplicações Web (APIs) padrão do Microsoft Dataverse, o Project Operations utiliza as novas APIs de Agendamento de Projetos para criar, atualizar e eliminar tarefas de projeto, atribuições de recursos, dependências de tarefas, buckets de projeto e membros de equipas de projeto. No entanto, quando criar, atualizar ou eliminar operações forem executados programaticamente em entidades da estrutura hierárquica do trabalho (WBS), podem ocorrer erros. Para monitorizar estes erros e o histórico de operações, foram implementados dois novos registos administrativos: **Conjunto de Operações** e **Serviço de Agendamento de Projetos (PSS)**. Para aceder a estes registos, aceda a **Definições** \> **Integração de Agendamento**.

A seguinte ilustração mostra o modelo de dados para os registos do Agendamento de Projetos.

![Modelo de dados para os registos de Agendamento de Projetos.](media/LOGDATAMODEL.jpg)

## <a name="operation-set-log"></a>Registo de Conjunto de Operações

O registo Conjunto de Operações monitoriza a execução de um conjunto de operação que é usado para executar uma ou muitas operações criar, atualizar ou eliminar operações num lote em projetos, tarefas de projeto, atribuições de recursos, dependências de tarefas, buckets de projeto ou membros de equipa de projeto. O campo **Operação em Estado** mostra o estado geral do conjunto de operações. Os detalhes do payload do conjunto de operações são capturados em registos relacionados do Detalhe de Conjunto de Operações.

### <a name="operation-set"></a>Conjunto de Operações

A tabela seguinte mostra os campos que estão relacionados com a entidade **Conjunto de Operações**.

| SchemaName            | Description                                                                                                  | DisplayName            |
|-----------------------|--------------------------------------------------------------------------------------------------------------|------------------------|
| msdyn_completedon     | A data/hora de conclusão ou falha do conjunto de operações.                                                | CompletedOn            |
| msdyn_correlationid   | O valor **correlationId** do pedido.                                                                  | CorrelationId          |
| msdyn_description     | A descrição do conjunto de operações.                                                                        | Description            |
| msdyn_executedon      | A data/hora de execução do registo.                                                                       | Executado Em            |
| msdyn_operationsetId  | O identificador exclusivo das instâncias de entidade.                                                                   | OperationSet           |
| msdyn_Project         | O projeto é relacionado com o conjunto de operações.                                                            | Project                |
| msdyn_projectid       | O valor **projectId** do pedido.                                                                      | ProjectId (Preterido) |
| msdyn_projectName     | Não aplicável.                                                                                              | Não aplicável         |
| msdyn_PSSErrorLog     | O identificador exclusivo do registo de erros do Serviço de Agendamento de Projetos que está associado ao conjunto de operações. | Registo de Erros do PSS          |
| msdyn_PSSErrorLogName | Não aplicável.                                                                                              | Não aplicável         |
| msdyn_status          | O estado do conjunto de operações.                                                                             | Status                 |
| msdyn_statusName      | Não aplicável.                                                                                              | Não aplicável         |
| msdyn_useraadid       | O ID do objeto do Azure Active Directory (Azure AD) do utilizador a que pertence o pedido.                     | UserAADID              |

### <a name="operation-set-detail"></a>Detalhe do Conjunto de Operações

A tabela seguinte mostra os campos que estão relacionados com a entidade **Detalhe do Conjunto de Operações**.

| SchemaName                 | Description                                                                                 | DisplayName           |
|----------------------------|---------------------------------------------------------------------------------------------|-----------------------|
| msdyn_cdspayload           | Os campos serializados do Dataverse para o pedido.                                            | CdsPayload            |
| msdyn_entityname           | O nome da entidade para o pedido.                                                     | EntityName            |
| msdyn_httpverb             | O método de pedido.                                                                         | Verbo HTTP (Preterido) |
| msdyn_httpverbName         | Não aplicável.                                                                             | Não aplicável        |
| msdyn_operationset         | O identificador exclusivo do conjunto de operações a que pertence o registo.                      | OperationSet          |
| msdyn_operationsetdetailId | O identificador exclusivo das instâncias de entidade.                                                  | Detalhe de OperationSet   |
| msdyn_operationsetName     | Não aplicável.                                                                             | Não aplicável        |
| msdyn_operationtype        | O tipo de operação do detalhe do conjunto de operações.                                             | OperationType         |
| msdyn_operationtypeName    | Não aplicável.                                                                             | Não aplicável        |
| msdyn_psspayload           | Os campos serializados do Serviço de Agendamento de Projetos para o pedido.                           | PssPayload            |
| msdyn_recordid             | O identificador do registo de pedido.                                                       | ID de Registo             |
| msdyn_requestnumber        | Um número gerado automaticamente que identifica a ordem em que os pedidos foram recebidos. | Número do Pedido        |

## <a name="project-scheduling-service-error-logs"></a>Registos de erros do Serviço de Agendamento de Projetos

Os registos de erros do Serviço de Agendamento de Projetos capturam falhas que ocorrem quando o Serviço de Agendamento de Projetos tenta uma operação **Guardar** ou **Abrir**. Existem três cenários suportados onde estes registos são gerados:

- As ações iniciadas pelo utilizador falham de forma crítica (por exemplo, uma atribuição não pode ser criada devido a privilégios em falta).
- O Serviço de Agendamento de Projetos não pode criar, atualizar, eliminar ou efetuar qualquer outra operação em cascata numa entidade.
- O utilizador experimenta erros quando um registo não abre (por exemplo, quando um projeto é aberto ou as informações de um membro da equipa são atualizadas).

### <a name="project-scheduling-service-log"></a>Registo do Serviço de Agendamento de Projetos

A tabela seguinte mostra os campos que estão incluídos no registo do Serviço de Agendamento de Projetos.

| SchemaName          | Description                                                                    | DisplayName    |
|---------------------|--------------------------------------------------------------------------------|----------------|
| msdyn_CallStack     | A pilha de chamadas da exceção.                                               | Pilha de Chamadas     |
| msdyn_correlationid | O ID de correlação do erro.                                               | CorrelationId  |
| msdyn_errorcode     | Um campo que é utilizado para armazenar o código de erro do Dataverse ou o código de erro HTTP. | Código de Erro     |
| msdyn_HelpLink      | Uma ligação para a documentação de Ajuda pública.                                       | Ligação de Ajuda      |
| msdyn_log           | O registo do Serviço de Agendamento de Projetos.                                   | Registo            |
| msdyn_project       | O projeto que está associado ao registo de erros.                             | Project        |
| msdyn_projectName   | O nome do projeto se o payload do conjunto de operações será persistido. | Não aplicável |
| msdyn_psserrorlogId | O identificador exclusivo das instâncias de entidade.                                     | Registo de Erros do PSS  |
| msdyn_SessionId     | O de ID de sessão do projeto.                                                        | ID da Sessão     |

## <a name="error-log-cleanup"></a>Limpeza do registo de erros

Por predefinição, tanto os registos de erros do Serviço de Agendamento de Projetos como o registo de Conjunto de Operações podem ser limpos a cada 90 dias. Todos os registos com mais de 90 dias serão eliminados. No entanto, alterando o valor do campo **msdyn_StateOperationSetAge** na página **Parâmetros do Projeto**, os administradores podem ajustar o intervalo de limpeza de modo a que seja entre 1 e 120 dias. Estão disponíveis vários métodos para alterar este valor:

- Personalize a entidade **Parâmetro do Projeto** criando uma página personalizada e adicionando o campo **Idade do Conjunto de Operações Obsoleto**.
- Utilize o código de cliente que utiliza o [Kit de desenvolvimento de software (SDK) WebApi](/powerapps/developer/model-driven-apps/clientapi/reference/xrm-webapi/updaterecord).
- Use o código SDK de Serviço que utiliza o método **updateRecord** do SDK Xrm (referência de API de Cliente) em aplicações condicionadas por modelo. O Power Apps inclui uma descrição e parâmetros suportados para o método **updateRecord**.

    ```C#
    Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter').then(function (response) {
        parameter = response.entities[0];
        var staleOperationValue = prompt("All records older than (x) days will be deleted, please enter X between 1 to 90 days", 1)
        var newData = {};
        newData.msdyn_projectparameterid = parameter.msdyn_projectparameterid;
        newData.msdyn_staleoperationsetage = parseInt(staleOperationValue);
        Xrm.WebApi.updateRecord("msdyn_projectparameter", parameter.msdyn_projectparameterid, newData).then(
            function success(result) {
                console.log("Project Parameter: Stale Operation Expiry is set to: " + newData.msdyn_staleoperationsetage);
                // perform operations on record update
                Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter')
                .then(function (response2) { console.log("Confirmed Project Parameter: Stale Operation Expiry is set to: " + response2.entities[0].msdyn_staleoperationsetage) });
            },
            function (error) {
                console.log("Failed to Update Project Ednpoint with error: " + error.message);
            // handle error conditions
            }
        );
    });
    ```
