---
title: Planifique o seu trabalho no Microsoft Project com o Project Service
description: Este tópico fornece informações sobre como utilizar o suplemento do Microsoft Project para o serviço do Microsoft Project Service.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 01/07/2021
ms.topic: article
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
ms.openlocfilehash: 0c0ea75d34047f7145466ab427d213c5df27fbed
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014580"
---
# <a name="plan-your-work-in-microsoft-project-with-the-project-service-add-in"></a>Planifique o seu trabalho no Microsoft Project com o Project Service

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3x](../includes/cc-applies-to-psa-app-3x.md)]

O [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] facilita o planeamento do projeto, incluindo as estimativas. É possível definir o trabalho para os custos, o esforço e o valor das vendas serem claros quando a proposta final for submetida.  

Pode instalar o [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] e fazer o trabalho de planeamento no ambiente familiar do [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]. Utilize as funcionalidades de planeamento e gestão robustas do [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] e, em seguida, atualize o seu plano de projeto no Project Service Automation.  

> [!IMPORTANT]
> - Para utilizar a gestão de documentos do SharePoint para armazenar os seus ficheiros do [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] para os projetos do [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], o seu administrador do [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] terá de ativar a gestão de documentos. 
> - O [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] só é compatível com o [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.  

## <a name="download-and-install-the-add-in"></a>Transferir e instalar o suplemento  
 Prepare as suas informações de início de sessão da [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Irá precisar destas informações para ligar do [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] à [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

1.  A partir do Centro de Transferências, pode transferir o suplemento para a sua versão suportada do Project Service, [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) ou [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).  

2.  Selecione a hiperligação de transferência.  

3.  Quando a transferência estiver concluída, selecione **Sim** para instalar o suplemento.  

## <a name="configure-the-add-in"></a>Configurar o suplemento  

1. Abra o [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] e selecione o separador **Project Service**.  

2. Selecione **Ligar**.  

3. Introduza as informações de início de sessão e, em seguida, selecione **Iniciar Sessão**.  

   Já pode começar a utilizar o suplemento.  

## <a name="read-from-a-template"></a>Ler a partir de um modelo  
 Leia a partir de um modelo criado no [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] e copiado para o [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] para iniciar o planeamento de projetos. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Criar um modelo do projeto (Project Service Automation)](../psa/create-project-template.md)  

1.  A partir do separador **Serviço do projeto**, selecione **Ler** > **Modelo de Projeto do Project Service Automation**.  

2.  Escolha um modelo de projeto a partir da lista e, em seguida, selecione **Abrir**.  

    > [!NOTE]
    >  Por predefinição, as tarefas que são copiadas do modelo para o Projeto são definidas como agendadas manualmente.  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a>Atribuir funções de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] a recursos do projeto  

1.  Abra um projeto e selecione o friso **Tarefa**.  

2. Selecione o menu **Gráfico Gantt** e escolha **Folha de Recursos**.  

3. Na Folha de Recursos, selecione o menu pendente **Função do Recurso do Project Service** e escolha uma função do Project Service Automation.  

## <a name="staff-your-project-with-resources"></a>Atribuir pessoal ao projeto com recursos  

1.  A partir do separador Project Service, selecione uma seta e selecione **Localizar Recursos**.  

2.  No ecrã **Reservar Recurso**, selecione o recurso que pretende utilizar para o projeto.  

3.  Selecione **Reservar** e selecione **OK**.  

## <a name="publish-your-project"></a>Publicar o projeto  
Quando o planeamento de projeto estiver concluído, o passo seguinte é importar e publicar o projeto para a [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

O projeto será importado para a [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. É aplicado o processo de geração da equipa e de preços. Abra o projeto no [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] para ver a equipa, as estimativas do projeto e a estrutura discriminada do trabalho gerada. A tabela seguinte mostra onde encontrar os resultados.


|              Microsoft Project                                                           |                      Project Service Automation                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Gráfico Gantt**   | Importa para o ecrã [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Estrutura Hierárquica do Trabalho**. |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Folha de Recursos** |   Importa para o ecrã [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Membros da Equipa do Projeto**.   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Utilizar Utilização**    |    Importa para o ecrã [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Estimativas do Projeto**.     |

**Para importar e publicar o projeto**  
1. No separador **Serviço do projeto**, ir a **Publicar** > **Novo Projeto do Project Service Automation**.  

2. Na caixa de diálogo **Publicar num novo projeto no Project Service**, introduza o **Nome do Projeto** e selecione o **Cliente**.  

3. Opcionalmente, selecione **Associar plano do projeto ao Project Service Automation** para associar o ficheiro de Projeto do plano ao Project Service Automation.  

4. Selecione **Publicar**.  

   Ao associar o ficheiro do Projeto ao [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], torna o ficheiro do Projeto o registo mestre e define a estrutura hierárquica do trabalho na [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] como só de leitura.  As alterações ao plano do projeto têm de ser feitas no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] e publicadas como atualizações à [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

## <a name="edit-a-project-thats-been-imported"></a>Editar um projeto que foi importado  
 Para efetuar alterações a um plano do projeto que tenha sido importado para o [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], existem duas opções:  

- Abra o ficheiro mestre e edite-o no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

- Desassocie o ficheiro e edite-o diretamente no Project Service. Por predefinição, um projeto que tenha sido carregado a partir do [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] está bloqueado e só pode ser editado no Project. Para editar o ficheiro no [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], o ficheiro tem de estar desassociado.  

### <a name="edit-in-pn_microsoft_project"></a>Editar no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]  

1. No menu principal, ir a **Project Service** > **Projetos**.  

2. Na lista de projetos, abra aquele que criou no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Selecione **Abrir no MS Project** a partir do friso. É aberto o ficheiro mestre associado no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a>Desassocie um ficheiro e edite-o no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service  

1. No menu principal, ir a **Project Service** > **Projetos**.  

2. Na lista de projetos, abra aquele que criou no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Selecione **Desassociar do MS Project** a partir do friso.  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a>Carregar um ficheiro de Projeto para o SharePoint ou os Grupos do Office  
 Pode carregar o ficheiro do Project para o SharePoint e encontrá-lo em Documentos Associados para o seu projeto do [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  O respetivo administrador tem de configurar a gestão de documentos do SharePoint e ativá-lo para a entidade do Projeto. 

 Também pode carregar o ficheiro do Project para o [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] se tiver Grupos do Office configurados.

### <a name="upload-a-file-for-sharepoint"></a>Carregar um ficheiro para o SharePoint  

1. No menu principal, ir a **Project Service** > **Carregar**.  

2. Selecione **Aos Documentos do Projeto do Project Service Automation**.  

3. Na caixa de diálogo **Ativar Abrir no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**, selecionar **Sim** ou **Não**.  

   - Se selecionar **Sim**, poderá selecionar o botão **Abrir no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** no Project Service Automation e iniciar o [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] e carregar o ficheiro do Project a partir da biblioteca de documentos do SharePoint.  

   - Se selecionar **Não**, o link para **Abrir no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** não funcionará.  

4. O ficheiro do [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] pode ser encontrado no [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] em **Documentos** para o projeto da [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] específico.  

### <a name="upload-a-file-for-office-groups"></a>Carregar um ficheiro para os Grupos do Office  

1. No menu principal, ir a **Project Service** > **Carregar**.  

2. Selecione **Aos Documentos do Projeto do Project Service Automation**.  

3. Na caixa de diálogo **Ativar Abrir no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**, selecionar **Sim** ou **Não**.  

   - Se selecionar **Sim**, poderá selecionar **Abrir no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** no Project Service Automation e iniciar o [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] e carregar o ficheiro do Project a partir da biblioteca de documentos do SharePoint.  

   - Se selecionar **Não**, o link para **Abrir no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** não funcionará.  

4. O ficheiro do [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] pode ser encontrado no [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] em **Documentos** para o projeto da [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] específico.  

## <a name="publish--your-project-as-a-template"></a>Publicar o projeto como um modelo  
 Pode guardar o projeto e reutilizá-lo ao guardá-lo como um modelo de projeto na [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Os modelos de projeto estão planos de projeto reutilizáveis na [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Para obter mais informações, consulte [Criar um modelo de projeto (Project Service Automation)](../psa/create-project-template.md). 

1. No separador **Serviço do projeto**, ir a **Publicar** > **Novo Modelo de Projeto do Project Service Automation**.  

2. Na caixa de diálogo **Publicar num novo modelo de projeto do Project Service**, introduza o **Nome do modelo de projeto**.  

3. Opcionalmente, selecione **Associar plano do projeto ao Project Service Automation** para associar o ficheiro de Projeto a [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

4. Selecione **Publicar**.  

Ao associar o ficheiro do Projeto à [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], torna o ficheiro do Projeto o registo mestre e define a estrutura hierárquica do trabalho no modelo da [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] como só de leitura.  As alterações ao plano do projeto têm de ser feitas no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] e publicadas como atualizações à [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].

## <a name="read-a-resource-loaded-schedule"></a>Ler uma agenda carregada de recursos

Ao ler um projeto do Project Service Automation, o calendário do recurso não é sincronizado para o cliente de ambiente de trabalho. Se há diferenças nas durações de tarefa, esforço ou fim, é provavelmente porque os recursos e o cliente do ambiente de trabalho não têm o mesmo calendário de modelo de hora de trabalho aplicado ao projeto.


## <a name="data-synchronization"></a>Sincronização de dados
As tabelas desta secção fornecem informações sobre a sincronização dos dados da entidade entre a o Project Service Automation e o suplemento de secretária do Microsoft Project.

### <a name="project-task-entity-table"></a>Tabela de entidades de tarefas de projeto
A tabela que se segue descreve como os dados são de entidade de tarefa de Projeto são sincronizados entre o Project Service Automation e o suplemento de ambiente de trabalho do Microsoft Project.

| **Entidade** | **Campo** | **Microsoft Project para Project Service Automation** | **Project Service Automation para Microsoft Project** |
| --- | --- | --- | --- |
| Tarefa de Projeto | Data Para Conclusão | Synchronized | Não sincronizado |
| Tarefa de Projeto | Esforço Estimado | Synchronized | Não sincronizado |
| Tarefa de Projeto | ID do Cliente de MS Project | Synchronized | Não sincronizado |
| Tarefa de Projeto | Tarefa Principal | Synchronized | Não sincronizado |
| Tarefa de Projeto | Project | Synchronized | Não sincronizado |
| Tarefa de Projeto | Tarefa de projeto | Synchronized | Não sincronizado |
| Tarefa de Projeto | Nome da Tarefa de Projeto | Synchronized | Não sincronizado |
| Tarefa de Projeto | Unidade de atribuição de recursos (Preterido na v3.0) | Synchronized | Não sincronizado |
| Tarefa de Projeto | Duração Agendada | Synchronized | Não sincronizado |
| Tarefa de Projeto | Data de Início | Synchronized | Não sincronizado |
| Tarefa de Projeto | ID de WBS | Synchronized | Não sincronizado |

### <a name="team-member-entity-table"></a>Tabela de entidades de membros da equipa
A tabela que se segue descreve como os dados da entidade de membro da equipa são sincronizados entre o Project Service Automation e o Micros

| **Entidade** | **Campo** | **Microsoft Project para Project Service Automation** | **Project Service Automation para Microsoft Project** |
| --- | --- | --- | --- |
| Membro da Equipa | ID do Cliente de MS Project | Synchronized | Não sincronizado |
| Membro da Equipa | Nome da Posição | Synchronized | Não sincronizado |
| Membro da Equipa | projeto | Synchronized | Synchronized |
| Membro da Equipa | Equipa do Projeto | Synchronized | Synchronized |
| Membro da Equipa | Unidade de Atribuição de Recursos | Não sincronizado | Synchronized |
| Membro da Equipa | Função | Não sincronizado | Synchronized |
| Membro da Equipa | Horas de Trabalho | Não sincronizado | Não sincronizado |

### <a name="resource-assignment-entity-table"></a>Tabela de entidades de atribuição de recursos
A tabela que se segue descreve como os dados da entidade de atribuição de recursos são sincronizados entre o Project Service Automation e o Micros

| **Entidade** | **Campo** | **Microsoft Project para Project Service Automation** | **Project Service Automation para Microsoft Project** |
| --- | --- | --- | --- |
| Atribuição de Recurso | Da Data | Synchronized | Não sincronizado |
| Atribuição de Recurso | Horas | Synchronized | Não sincronizado |
| Atribuição de Recurso | ID do Cliente de MS Project | Synchronized | Não sincronizado |
| Atribuição de Recurso | Trabalho Planeado | Synchronized | Não sincronizado |
| Atribuição de Recurso | Project | Synchronized | Não sincronizado |
| Atribuição de Recurso | Equipa do Projeto | Synchronized | Não sincronizado |
| Atribuição de Recurso | Atribuição de Recurso | Synchronized | Não sincronizado |
| Atribuição de Recurso | Tarefa | Synchronized | Não sincronizado |
| Atribuição de Recurso | Até à Data | Synchronized | Não sincronizado |

### <a name="project-task-dependencies-entity-table"></a>Tabela de entidades de tarefas de dependências
A tabela que se segue descreve como os dados da entidade de dependências de tarefa de projeto são sincronizados entre o Project Service Automation e o Micros

| **Entidade** | **Campo** | **Microsoft Project para Project Service Automation** | **Project Service Automation para Microsoft Project** |
| --- | --- | --- | --- |
| Dependências de Tarefa de Projeto | Dependência de Tarefa de Projeto | Synchronized | Não sincronizado |
| Dependências de Tarefa de Projeto | Tipo de Ligação | Synchronized | Não sincronizado |
| Dependências de Tarefa de Projeto | Tarefa Antecessora | Synchronized | Não sincronizado |
| Dependências de Tarefa de Projeto | Project | Synchronized | Não sincronizado |
| Dependências de Tarefa de Projeto | Tarefa Sucessora | Synchronized | Não sincronizado |

### <a name="additional-resources"></a>Recursos adicionais
 [Guia do Gestor de Projeto](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]