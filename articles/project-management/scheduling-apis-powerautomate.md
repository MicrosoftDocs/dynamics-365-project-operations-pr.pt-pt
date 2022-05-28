---
title: Utilizar API de agenda do projeto com o Power Automate
description: Este tópico fornece um fluxo de amostra que utiliza as interfaces de programação de aplicações (API) da agenda de projeto.
author: ruhercul
ms.date: 01/26/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 9708226b0955cfa6c405b9616c14765f9ebc21f7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8597720"
---
# <a name="use-project-schedule-apis-with-power-automate"></a>Utilizar API de agenda do projeto com o Power Automate

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

Este tópico descreve um fluxo de amostra que descrece como criar um plano de projeto completo com o Microsoft Power Automate, como criar um Conjunto de Operações e como atualizar uma entidade. O exemplo demonstra como criar um projeto, membro da equipa do projeto, Conjuntos de Operações, tarefas de projeto e atribuições de recursos. Este tópico explica também como atualizar uma entidade e executar um Conjunto de Operações.

Em seguida, segue-se uma lista completa dos passos documentados no fluxo de amostra neste tópico:

1. [Criar um acionador PowerApps](#1)
2. [Criar um projeto](#2)
3. [Iniciar uma variável para o membro da equipa](#3)
4. [Criar um mebro de equipa genérico](#4)
5. [Criar um Conjunto de operações](#5)
6. [Criar um registo de projeto](#6)
7. [Iniciar uma variável para o estado da ligação](#7)
8. [Iniciar uma variável para o número de tarefas](#8)
9. [Iniciar uma variável para o ID de tarefas do projeto](#9)
10. [Fazer até](#10)
11. [Definir uma tarefa do projeto](#11)
12. [Criar uma tarefa do projeto](#12)
13. [Criar uma atribuição de recursos](#13)
14. [Reduzir uma variável](#14)
15. [Renomear uma tarefa de projeto](#15)
16. [Executar um Conjunto de operações](#16)

## <a name="assumptions"></a>Suposições

Este tópico supõe que tem conhecimentos básicos sobre a plataforma Dataverse, os fluxos na cloud e a Interface de Programação de Aplicações (API) da Agenda do Projeto. Para mais informações, consulte a secção [Referências](#references) mais à frente neste tópico.

## <a name="create-a-flow"></a>Criar um fluxo

### <a name="select-an-environment"></a>Selecionar um ambiente

É possível criar o fluxo Power Automate no seu ambiente.

1. Aceda a <https://flow.microsoft.com> e use as suas credenciais de administrador para iniciar sessão.
2. No canto superior direito, selecione **Ambientes**.
3. Na lista, selecione o ambiente em que o Dynamics 365 Project Operations está instalado.

### <a name="create-a-solution"></a>Criar uma solução

Siga estes passos para criar um [fluxo consciente da solução](/power-automate/overview-solution-flows). Ao criar um fluxo consciente da solução, pode exportar mais facilmente o fluxo para o utilizar mais tarde.

1. No painel de navegação esquerdo, selecione **Soluções**.
2. Na página **Soluções**, selecione **Nova solução**.
3. Na caixa de diálogo **Nova solução**, defina os campos necessários e, em seguida, selecione **Criar**.

## <a name="step-1-create-a-powerapps-trigger"></a><a id="1"></a>Passo 1: criar um acionador PowerApps

1. Na página **Soluções**, selecione a solução que criou e, em seguida, selecione **Novo**.
2. No painel esquerdo, selecione **Fluxos na Cloud** \> **Automatização** \> **Fluxo na cloud** \> **Instantâneo**.
3. No campo **Nome do fluxo**, introduza **Fluxo de demonstração da API da agenda**.
4. Na lista **Escolher como acionar este fluxo**, selecione **Power Apps**. Quando cria um acionador Power Apps, a lógica é da sua responsabilidade como autor. Neste tópico, deixe os parâmetros de entrada em branco para efeitos de teste.
5. Selecione **Criar**.

## <a name="step-2-create-a-project"></a><a id="2"></a>Passo 2: Criar um projeto

Siga estes passos para criar um projeto de amostra.

1. No fluxo que criou, selecione **Novo passo**.

    ![Adicionar um novo passo.](media/newstep.png)

2. Na caixa de diálogo **Escolher uma operação**, no campo de pesquisa, introduza **Executar uma ação sem restrições** . Em seguida, no separador **Ações**, selecione a operação na lista de resultados.

    ![Selecionar uma operação.](media/chooseactiontab.png)

3. No novo passo, selecione as reticências (**...**) e, em seguida, selecione **Renomear**.

![Renomear um passo.](media/renamestep.png)

4. Renomear o passo **Criar Projeto**.
5. No campo **Nome da ação**, introduza **msdyn\_CreateProjectV1**.
6. No campo **msdyn\_subject**, selecione **Adicionar conteúdo dinâmico**.
7. No separador **Expressão**, no campo função, introduza **Nome do projeto - utcNow()**.
8. Selecione **OK**.

## <a name="step-3-initialize-a-variable-for-the-team-member"></a><a id="3"></a>Passo 3: iniciar uma variável para o membro da equipa

1. No fluxo, selecione **Novo passo**.
2. Na caixa de diálogo **Escolher uma operação**, no campo de pesquisa, introduza **iniciar variável** . Em seguida, no separador **Ações**, selecione a operação na lista de resultados.
3. No novo passo, selecione as reticências (**...**) e, em seguida, selecione **Renomear**.
4. Renomear o passo **Iniciar membro da equipa**.
5. No campo **Nome**, introduza **TeamMemberAction**.
6. No campo **Tipo**, selecione **Cadeia**.
7. No campo **Valor**, introduza **msdyn\_CreateTeamMemberV1**.

## <a name="step-4-create-a-generic-team-member"></a><a id="4"></a>Passo 4: criar um membro da equipa genérico

1. No fluxo, selecione **Novo passo**.
2. Na caixa de diálogo **Escolher uma operação**, no campo de pesquisa, introduza **Executar uma ação sem restrições** . Em seguida, no separador **Ações**, selecione a operação na lista de resultados.
3. No novo passo, selecione as reticências (**...**) e, em seguida, selecione **Renomear**.
4. Renomear o passo **Criar membro da equipa**.
5. Para o campo **Nome da ação**, selecione **TeamMemberAction** na caixa de diálogo **Conteúdo dinâmico**.
6. No campo **Parâmetros de Ação**, introduza as seguintes informações de parâmetros.

    ```
    {
        "TeamMember": {
            "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projectteam",
            "msdyn_projectteamid": "@{guid()}",
            "msdyn_project@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})",
            "msdyn_name": "ScheduleAPIDemoTM1"
        }
    } 
    ```

    Eis uma explicação dos parâmetros:

    - **\@\@odata.type** – O nome da entidade. Por exemplo, introduza **"Microsoft.Dynamics.CRM.msdyn\_projectteam"**.
    - **msdyn\_projectteamid** – A chave principal do ID da equipa de projeto. O valor é uma expressão de identificador exclusivo global (GUID).   O ID é gerado a partir do separador de expressão.

    - **msdyn\_project\@odata.bind** – O ID de projeto do próprio projeto. O valor terá conteúdo dinâmico, que vem da resposta do passo "Criar Projeto". Certifique-se de que introduz o caminho completo e adiciona conteúdo dinâmico entre os parênteses. São necessárias aspas. Introduza, por exemplo **"/msdyn\_projects(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_name** – O nome do membro da equipa. Introduza, por exemplo **"ScheduleAPIDemoTM1"**.

## <a name="step-5-create-an-operation-set"></a><a id="5"></a>Passo 5: criar um Conjunto de operações

1. No fluxo, selecione **Novo passo**.
2. Na caixa de diálogo **Escolher uma operação**, no campo de pesquisa, introduza **Executar uma ação sem restrições** . Em seguida, no separador **Ações**, selecione a operação na lista de resultados.
3. No novo passo, selecione as reticências (**...**) e, em seguida, selecione **Renomear**.
4. Renomear o passo **Criar conjunto de operações**.
5. No campo **Nome da Ação**, selecione a ação personalizada **msdyn\_CreateOperationSetV1** Dataverse.
6. No campo **Descrição**, introduza **ScheduleAPIDemoOperationSet**.
7. No campo **Projeto**, introduza **/msdyn\_projects(**.
8. Na caixa de diálogo **Conteúdo dinâmico**, selecione **msdyn\_CreateProjectV1Response ProjectId**.
9. No campo **Projeto**, introduza **)**.

## <a name="step-6-create-a-project-bucket"></a><a id="6"></a>Passo 6: criar um registo de projeto

1. No fluxo, selecione **Novo passo**.
2. Na caixa de diálogo **Escolher uma operação**, no campo de pesquisa, introduza **adicionar nova linha** . Em seguida, no separador **Ações**, selecione a operação na lista de resultados.
3. No novo passo, selecione as reticências (**...**) e, em seguida, selecione **Renomear**.
4. Renomear o passo **Criar registo**.
5. No campo **Nome da tabela**, selecione **Registos de projeto**.
6. No campo **Nome**, introduza **ScheduleAPIDemoBucket1**.
7. Para o campo **Projeto**, selecione **msdyn\_CreateProjectV1Response ProjectId** na caixa de diálogo **Conteúdo dinâmico**.

## <a name="step-7-initialize-a-variable-for-the-link-status"></a><a id="7"></a>Passo 7: iniciar uma variável para o estado da ligação

1. No fluxo, selecione **Novo passo**.
2. Na caixa de diálogo **Escolher uma operação**, no campo de pesquisa, introduza **iniciar variável** . Em seguida, no separador **Ações**, selecione a operação na lista de resultados.
3. No novo passo, selecione as reticências (**...**) e, em seguida, selecione **Renomear**.
4. Renomear o passo **Iniciar linkstatus**.
5. No campo **Nome**, introduza **linkstatus**.
6. No campo **Tipo**, selecione **Número inteiro**.
7. No campo **Valor**, introduza **192350000**.

## <a name="step-8-initialize-a-variable-for-the-number-of-tasks"></a><a id="8"></a>Passo 8: iniciar uma variável para o número de tarefas

1. No fluxo, selecione **Novo passo**.
2. Na caixa de diálogo **Escolher uma operação**, no campo de pesquisa, introduza **iniciar variável** . Em seguida, no separador **Ações**, selecione a operação na lista de resultados.
3. No novo passo, selecione as reticências (**...**) e, em seguida, selecione **Renomear**.
4. Renomear o passo **Iniciar número de tarefas**.
5. No campo **Nome**, introduza **número de tarefas**.
6. No campo **Tipo**, selecione **Número inteiro**.
7. No campo **Valor**, introduza **5**.

## <a name="step-9-initialize-a-variable-for-the-project-task-id"></a><a id="9"></a>Passo 9: iniciar uma variável para o ID de tarefas do projeto

1. No fluxo, selecione **Novo passo**.
2. Na caixa de diálogo **Escolher uma operação**, no campo de pesquisa, introduza **iniciar variável** . Em seguida, no separador **Ações**, selecione a operação na lista de resultados.
3. No novo passo, selecione as reticências (**...**) e, em seguida, selecione **Renomear**.
4. Renomear o passo **Iniciar ProjectTaskID**.
5. No campo **Nome**, introduza **número de tarefas**.
6. No campo **Tipo**, selecione **Cadeia**.
7. Para o campo **Valor**, introduza **guid()** no construtor de expressões.

## <a name="step-10-do-until"></a><a id="10"></a>Passo 10: fazer até

1. No fluxo, selecione **Novo passo**.
2. Na caixa de diálogo **Escolher uma operação**, no campo de pesquisa, introduza **fazer até** . Em seguida, no separador **Ações**, selecione a operação na lista de resultados.
3. Defina o primeiro valor na instrução condicional com o **número de tarefas** variável da caixa de diálogo **Conteúdo dinâmico**.
4. Defina a condição para **menos do que igual a**.
5. Defina o segundo valor na instrução condicional como **0**.

## <a name="step-11-set-a-project-task"></a><a id="11"></a>Passo 11: definir uma tarefa do projeto

1. No fluxo, selecione **Novo passo**.
2. Na caixa de diálogo **Escolher uma operação**, no campo de pesquisa, introduza **definir variável** . Em seguida, no separador **Ações**, selecione a operação na lista de resultados.
3. No novo passo, selecione as reticências (**...**) e, em seguida, selecione **Renomear**.
4. Renomear o passo **Definir tarefa do projeto**.
5. No campo **Nome**, selecione **msdyn\_projecttaskid**.
6. Para o campo **Valor**, introduza **guid()** no construtor de expressões.

## <a name="step-12-create-a-project-task"></a><a id="12"></a>Passo 12: criar uma tarefa de projeto

Siga estes passos para criar uma tarefa de projeto que tenha um ID exclusivo que pertence ao projeto atual e ao registo de projeto que criou.

1. No fluxo, selecione **Novo passo**.
2. Na caixa de diálogo **Escolher uma operação**, no campo de pesquisa, introduza **Executar uma ação sem restrições** . Em seguida, no separador **Ações**, selecione a operação na lista de resultados.
3. No passo, selecione as reticências (**...**) e, em seguida, selecione **Renomear**.
4. Renomear o passo **Criar tarefa do projeto**.
5. No campo **Nome da ação**, introduza **msdyn\_PssCreateV1**.
6. No campo **Entidade**, introduza as seguintes informações de parâmetros.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_project@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})",
        "msdyn_subject": "ScheduleAPIDemoTask1",
        "msdyn_projectbucket@odata.bind": "/msdyn_projectbuckets(@{outputs('Create_Project_Buckets')?['body/msdyn_projectbucketid']})",
        "msdyn_start": "@{addDays(utcNow(), 1)}",
        "msdyn_scheduledstart": "@{utcNow()}",
        "msdyn_scheduledend": "@{addDays(utcNow(), 5)}",
        "msdyn_LinkStatus": "192350000"
    }
    ```

    Eis uma explicação dos parâmetros:

    - **\@\@odata.type** – O nome da entidade. Por exemplo, introduza **"Microsoft.Dynamics.CRM.msdyn\_projecttask"**.
    - **msdyn\_projecttaskid** – O ID exclusivo da tarefa. O valor deve ser definido como uma variável dinâmica de **msdyn\_projecttaskid**.
    - **msdyn\_project\@odata.bind** – O ID de projeto do próprio projeto. O valor terá conteúdo dinâmico, que vem da resposta do passo "Criar Projeto". Certifique-se de que introduz o caminho completo e adiciona conteúdo dinâmico entre os parênteses. São necessárias aspas. Introduza, por exemplo **"/msdyn\_projects(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_subject** – Qualquer nome da tarefa.
    - **msdyn\_projectbucket\@odata.bind** – O registo de projeto que contém as tarefas. O valor terá conteúdo dinâmico, que vem da resposta do passo "Criar Registo". Certifique-se de que introduz o caminho completo e adiciona conteúdo dinâmico entre os parênteses. São necessárias aspas. Introduza, por exemplo **"/msdyn\_projectbuckets(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_start** – Conteúdo dinâmico para a data de início. Por exemplo, amanhã será representado como **"addDays(utcNow(), 1)"**.
    - **msdyn\_scheduledstart** – A data de início agendada. Por exemplo, amanhã será representado como **"addDays(utcNow(), 1)"**.
    - **msdyn\_scheduleend** – A data de fim agendada. Selecione uma data no futuro. Por exemplo, especifique **"addDays(utcNow(), 5)"**.
    - **msdyn\_LinkStatus** – O estado da ligação. Introduza, por exemplo **"192350000"**.

7. Para o campo **OperationSetId**, selecione **msdyn\_CreateOperationSetV1Response** na caixa de diálogo **Conteúdo dinâmico**.

## <a name="step-13-create-a-resource-assignment"></a><a id="13"></a>Passo 13: Criar uma atribuição de recursos

1. No fluxo, selecione **Novo passo**.
2. Na caixa de diálogo **Escolher uma operação**, no campo de pesquisa, introduza **Executar uma ação sem restrições** . Em seguida, no separador **Ações**, selecione a operação na lista de resultados.
3. No passo, selecione as reticências (**...**) e, em seguida, selecione **Renomear**.
4. Renomear o passo **Criar atribuição**.
5. No campo **Nome da ação**, introduza **msdyn\_PssCreateV1**.
6. No campo **Entidade**, introduza as seguintes informações de parâmetros.

    ```
    {
        "@odata.type": "Microsoft.Dynamics.CRM.msdyn_resourceassignment",
        "msdyn_resourceassignmentid": "@{guid()}",
        "msdyn_name": "ScheduleAPIDemoAssign1",
        "msdyn_taskid@odata.bind": "/msdyn_projecttasks(@{variables('msdyn_projecttaskid')})",
        "msdyn_projectteamid@odata.bind": "/msdyn_projectteams(@{outputs('Create_Team_Member')?['body/TeamMemberId']})",
        "msdyn_projectid@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})"
    }
    ```

7. Para o campo **OperationSetId**, selecione **msdyn\_CreateOperationSetV1Response** na caixa de diálogo **Conteúdo dinâmico**.

## <a name="step-14-decrement-a-variable"></a><a id="14"></a>Passo 14: reduzir uma variável

1. No fluxo, selecione **Novo passo**.
2. Na caixa de diálogo **Escolher uma operação**, no campo de pesquisa, introduza **reduzir variável** . Em seguida, no separador **Ações**, selecione a operação na lista de resultados.
3. No campo **Nome**, selecione **número de tarefas**.
4. No campo **Valor**, introduza **1**.

## <a name="step-15-rename-a-project-task"></a><a id="15"></a>Passo 15: renomear uma tarefa do projeto

1. No fluxo, selecione **Novo passo**.
2. Na caixa de diálogo **Escolher uma operação**, no campo de pesquisa, introduza **Executar uma ação sem restrições** . Em seguida, no separador **Ações**, selecione a operação na lista de resultados.
3. No passo, selecione as reticências (**...**) e, em seguida, selecione **Renomear**.
4. Renomear o passo **Renomear tarefa do projeto**.
5. No campo **Nome da ação**, introduza **msdyn\_PssUpdateV1**.
6. No campo **Entidade**, introduza as seguintes informações de parâmetros.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_subject": "ScheduleDemoTask1-UpdatedName"
    }
    ```

7. Para o campo **OperationSetId**, selecione **msdyn\_CreateOperationSetV1Response** na caixa de diálogo **Conteúdo dinâmico**.

## <a name="step-16-run-an-operation-set"></a><a id="16"></a>Passo 16: executar um Conjunto de operações

1. No fluxo, selecione **Novo passo**.
2. Na caixa de diálogo **Escolher uma operação**, no campo de pesquisa, introduza **Executar uma ação sem restrições** . Em seguida, no separador **Ações**, selecione a operação na lista de resultados.
3. No passo, selecione as reticências (**...**) e, em seguida, selecione **Renomear**.
4. Renomear o passo **Executar conjunto de operações**.
5. No campo **Nome da ação**, introduza **msdyn\_ExecuteOperationSetV1**.
6. Para o campo **OperationSetId**, selecione **msdyn\_CreateOperationSetV1Response OperationSetId** na caixa de diálogo **Conteúdo dinâmico**.

## <a name="references"></a>Referências

- [Descrição geral de como integrar fluxos com o Dataverse - Power Automate](/power-automate/dataverse/overview?WT.mc_id=email)
- [Utilizar APIs de Agenda do Project para executar operações com entidades de Agendamento](schedule-api-preview.md)
- [Vista global dos fluxos da cloud - Power Automate](/power-automate/overview-cloud?WT.mc_id=email)
- [Visão geral dos fluxos conscientes da solução - Power Automate](/power-automate/overview-solution-flows?WT.mc_id=email)
