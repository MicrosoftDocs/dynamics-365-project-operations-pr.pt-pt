---
title: Utilizar o Project Service para planear o seu trabalho no Microsoft Project | MicrosoftDocs
description: Este tópico fornece informações sobre como adicionar, configurar e utilizar o suplemento do Microsoft Project para o Microsoft Project Service.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 04/06/2019
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
ms.openlocfilehash: 1d988419ae5a9d57532902d2553cd7de147e27c1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082534"
---
# <a name="use-the-project-service-automation-add-in-to-plan-your-work-in-microsoft-project"></a><span data-ttu-id="669c4-103">Utilizar o Project Service Automation para planear o seu trabalho no Microsoft Project</span><span class="sxs-lookup"><span data-stu-id="669c4-103">Use the Project Service Automation Add-in to plan your work in Microsoft Project</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="669c4-104">O [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] facilita o planeamento do projeto, incluindo as estimativas.</span><span class="sxs-lookup"><span data-stu-id="669c4-104">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] makes it easier for you to do your project planning, including estimates.</span></span> <span data-ttu-id="669c4-105">É possível definir o trabalho para os custos, o esforço e o valor das vendas serem claros quando a proposta final for submetida.</span><span class="sxs-lookup"><span data-stu-id="669c4-105">You can define the work so that costs, effort, and sales value are clear as the final proposal is submitted.</span></span>  

 <span data-ttu-id="669c4-106">Agora pode instalar o [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] e fazer o trabalho de planeamento no ambiente familiar do [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="669c4-106">Now you can install the [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] and do your planning work in the familiar environment of [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span> <span data-ttu-id="669c4-107">Utilize as funcionalidades de planeamento e gestão robustas do [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] e, em seguida, atualize o seu plano de projeto no Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="669c4-107">Use the robust planning and management capabilities of [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and then update your project plan in Project Service Automation.</span></span>  

> [!IMPORTANT]
> - <span data-ttu-id="669c4-108">Para utilizar a gestão de documentos do SharePoint para armazenar os seus ficheiros do [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] para os projetos do [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], o seu administrador do [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] terá de ativar a gestão de documentos.</span><span class="sxs-lookup"><span data-stu-id="669c4-108">To use SharePoint document management to store your [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] files for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projects, your [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] admin will need to turn on document management.</span></span> 
> - <span data-ttu-id="669c4-109">O [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] só é compatível com o [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.</span><span class="sxs-lookup"><span data-stu-id="669c4-109">The [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] is only compatible with [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.</span></span>  

## <a name="download-and-install-the-add-in"></a><span data-ttu-id="669c4-110">Transferir e instalar o suplemento</span><span class="sxs-lookup"><span data-stu-id="669c4-110">Download and install the add-in</span></span>  
 <span data-ttu-id="669c4-111">Prepare as suas informações de início de sessão da [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="669c4-111">Have your [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sign-in information ready.</span></span> <span data-ttu-id="669c4-112">Irá precisar destas informações para ligar do [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] à [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="669c4-112">You will need this information to connect from [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

1.  <span data-ttu-id="669c4-113">A partir do Centro de Transferências, pode transferir o suplemento para a sua versão suportada do Project Service, [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) ou [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).</span><span class="sxs-lookup"><span data-stu-id="669c4-113">From the Download Center, download the add-in for your supported version of Project Service, either [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) or [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).</span></span>  

2.  <span data-ttu-id="669c4-114">Clique na hiperligação de transferência.</span><span class="sxs-lookup"><span data-stu-id="669c4-114">Click the download link.</span></span>  

3.  <span data-ttu-id="669c4-115">Quando a transferência estiver concluída, clique em **Sim** para instalar o suplemento.</span><span class="sxs-lookup"><span data-stu-id="669c4-115">When the download is complete, click **Yes** to install the add-in.</span></span>  

## <a name="configure-the-add-in"></a><span data-ttu-id="669c4-116">Configurar o suplemento</span><span class="sxs-lookup"><span data-stu-id="669c4-116">Configure the add-in</span></span>  

1. <span data-ttu-id="669c4-117">Abra o [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] e clique no separador **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="669c4-117">Open [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and click the **Project Service** tab.</span></span>  

2. <span data-ttu-id="669c4-118">Clique em **Ligar**.</span><span class="sxs-lookup"><span data-stu-id="669c4-118">Click **Connect**.</span></span>  

3. <span data-ttu-id="669c4-119">Introduza as informações de início de sessão e, em seguida, clique em **Iniciar Sessão**.</span><span class="sxs-lookup"><span data-stu-id="669c4-119">Enter your sign-in information and then click **Sign in**.</span></span>  

   <span data-ttu-id="669c4-120">Já pode começar a utilizar o suplemento.</span><span class="sxs-lookup"><span data-stu-id="669c4-120">Now you can start using the add-in.</span></span>  

## <a name="read-from-a-template"></a><span data-ttu-id="669c4-121">Ler a partir de um modelo</span><span class="sxs-lookup"><span data-stu-id="669c4-121">Read from a template</span></span>  
 <span data-ttu-id="669c4-122">Leia a partir de um modelo criado no [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] e copiado para o [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] para iniciar o planeamento de projetos.</span><span class="sxs-lookup"><span data-stu-id="669c4-122">Read from a template that you created in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] and copied into [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] to start your project planning.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="669c4-123">[Criar um modelo do projeto (Project Service Automation)](../psa/create-project-template.md)</span><span class="sxs-lookup"><span data-stu-id="669c4-123">[Create a project template (Project Service Automation)](../psa/create-project-template.md)</span></span>  

1.  <span data-ttu-id="669c4-124">A partir do separador **Project Service** , cliqie em **Ler** > **Modelo de Projeto do Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="669c4-124">From the **Project Service** tab, click **Read** > **Project Service Automation Project Template**.</span></span>  

2.  <span data-ttu-id="669c4-125">Escolha um modelo de projeto a partir da lista e, em seguida, clique em **Abrir**.</span><span class="sxs-lookup"><span data-stu-id="669c4-125">Choose a project template from the list and then click **Open**.</span></span>  

    > [!NOTE]
    >  <span data-ttu-id="669c4-126">Por predefinição, as tarefas que são copiadas do modelo para o Projeto são definidas como agendadas manualmente.</span><span class="sxs-lookup"><span data-stu-id="669c4-126">By default, the tasks that are copied from the template into Project are set as manually scheduled.</span></span>  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a><span data-ttu-id="669c4-127">Atribuir funções de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] a recursos do projeto</span><span class="sxs-lookup"><span data-stu-id="669c4-127">Assign [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] roles to project resources</span></span>  

1.  <span data-ttu-id="669c4-128">Abra um projeto e clique no friso **Tarefa**.</span><span class="sxs-lookup"><span data-stu-id="669c4-128">Open a project and click the **Task** ribbon.</span></span>  

2.  <span data-ttu-id="669c4-129">Clique no menu **Gráfico Gantt** e escolha **Folha de Recursos**.</span><span class="sxs-lookup"><span data-stu-id="669c4-129">Click the **Gantt Chart** menu and then choose **Resource Sheet**.</span></span>  

3.  <span data-ttu-id="669c4-130">Na Folha de Recursos, clique no menu pendente **Função do Recurso do Project Service** e escolha uma função do Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="669c4-130">On the Resource Sheet, click the **Project Service Resource Role** drop-down menu and choose a Project Service Automation role.</span></span>  

## <a name="staff-your-project-with-resources"></a><span data-ttu-id="669c4-131">Atribuir pessoal ao projeto com recursos</span><span class="sxs-lookup"><span data-stu-id="669c4-131">Staff your project with resources</span></span>  

1.  <span data-ttu-id="669c4-132">A partir do separador Project Service, selecione uma seta e clique em **Localizar Recursos**.</span><span class="sxs-lookup"><span data-stu-id="669c4-132">From the Project Service tab, select a row and click **Find Resources**.</span></span>  

2.  <span data-ttu-id="669c4-133">No ecrã **Reservar Recurso** , selecione o recurso que pretende utilizar para o projeto.</span><span class="sxs-lookup"><span data-stu-id="669c4-133">On the **Book Resource** screen, select the resource that you want to use for the project.</span></span>  

3.  <span data-ttu-id="669c4-134">Clique em **Reservar** e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="669c4-134">Click **Book** and then click **OK**.</span></span>  

## <a name="publish-your-project"></a><span data-ttu-id="669c4-135">Publicar o projeto</span><span class="sxs-lookup"><span data-stu-id="669c4-135">Publish your project</span></span>  
<span data-ttu-id="669c4-136">Quando o planeamento de projeto estiver concluído, o passo seguinte é importar e publicar o projeto para a [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="669c4-136">When your project planning is complete, the next step is to import and publish the project in to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

<span data-ttu-id="669c4-137">O projeto será importado para a [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="669c4-137">The project will import into [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> <span data-ttu-id="669c4-138">É aplicado o processo de geração da equipa e de preços.</span><span class="sxs-lookup"><span data-stu-id="669c4-138">The pricing and team generation process are applied.</span></span> <span data-ttu-id="669c4-139">Abra o projeto na [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] para ver a equipa, as estimativas do projeto e a estrutura hierárquica do trabalho gerada.</span><span class="sxs-lookup"><span data-stu-id="669c4-139">Open the project in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to see that the team, project estimates, and work breakdown structure has been generated.</span></span> <span data-ttu-id="669c4-140">A tabela seguinte mostra onde encontrar os resultados:</span><span class="sxs-lookup"><span data-stu-id="669c4-140">The following table shows where to find the results:</span></span>


|                                                                                          |                                                                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="669c4-141">**Gráfico Gantt**</span><span class="sxs-lookup"><span data-stu-id="669c4-141">**Gantt Chart**</span></span>   | <span data-ttu-id="669c4-142">Importa para o ecrã [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Estrutura Hierárquica do Trabalho**.</span><span class="sxs-lookup"><span data-stu-id="669c4-142">Imports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Work Breakdown Structure** screen.</span></span> |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="669c4-143">**Folha de Recursos**</span><span class="sxs-lookup"><span data-stu-id="669c4-143">**Resource Sheet**</span></span> |   <span data-ttu-id="669c4-144">Importa para o ecrã [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Membros da Equipa do Projeto**.</span><span class="sxs-lookup"><span data-stu-id="669c4-144">Imports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Project Team Members** screen.</span></span>   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="669c4-145">**Utilizar Utilização**</span><span class="sxs-lookup"><span data-stu-id="669c4-145">**Use Usage**</span></span>    |    <span data-ttu-id="669c4-146">Importa para o ecrã [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Estimativas do Projeto**.</span><span class="sxs-lookup"><span data-stu-id="669c4-146">Omports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Project Estimates** screen.</span></span>     |

<span data-ttu-id="669c4-147">**Para importar e publicar o projeto**</span><span class="sxs-lookup"><span data-stu-id="669c4-147">**To import and publish your project**</span></span>  
1. <span data-ttu-id="669c4-148">A partir do separador **Project Service** , clique em **Publicar** > **Novo Projeto do Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="669c4-148">From the **Project Service** tab, click **Publish** > **New Project Service Automation Project**.</span></span>  

2. <span data-ttu-id="669c4-149">Na caixa de diálogo **Publicar num novo projeto no Project Service** , introduza o **Nome do Projeto** e selecione o **Cliente**.</span><span class="sxs-lookup"><span data-stu-id="669c4-149">On **Publish to a new project in Project Service** dialog box, enter the **Project Name** and select the **Customer**.</span></span>  

3. <span data-ttu-id="669c4-150">Opcionalmente, marque **Associar plano do projeto ao Project Service Automation** para associar o ficheiro de Projeto do plano ao Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="669c4-150">Optionally check the **Link project plan to Project Service Automation** to link the plan Project file to Project Service Automation.</span></span>  

4. <span data-ttu-id="669c4-151">Clique em  **Publicar**.</span><span class="sxs-lookup"><span data-stu-id="669c4-151">Click **Publish**.</span></span>  

   <span data-ttu-id="669c4-152">Ao associar o ficheiro do Projeto ao [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], torna o ficheiro do Projeto o registo mestre e define a estrutura hierárquica do trabalho na [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] como só de leitura.</span><span class="sxs-lookup"><span data-stu-id="669c4-152">Linking the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] makes the Project file the master and sets the work breakdown structure in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to read-only.</span></span>  <span data-ttu-id="669c4-153">As alterações ao plano do projeto têm de ser feitas no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] e publicadas como atualizações à [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="669c4-153">In order to make changes to the project plan, you need to make them in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and publish them as updates to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

## <a name="edit-a-project-thats-been-imported"></a><span data-ttu-id="669c4-154">Editar um projeto que foi importado</span><span class="sxs-lookup"><span data-stu-id="669c4-154">Edit a project that’s been imported</span></span>  
 <span data-ttu-id="669c4-155">Para efetuar alterações a um plano do projeto que tenha sido importado para o [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], existem duas opções:</span><span class="sxs-lookup"><span data-stu-id="669c4-155">To make changes to a project plan that's been imported into [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you have two options:</span></span>  

- <span data-ttu-id="669c4-156">Abra o ficheiro mestre e edite-o no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="669c4-156">Open the master file and edit it in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

- <span data-ttu-id="669c4-157">Desassocie o ficheiro e edite-o diretamente no Project Service.</span><span class="sxs-lookup"><span data-stu-id="669c4-157">Unlink the file and edit it directly in Project Service.</span></span> <span data-ttu-id="669c4-158">Por predefinição, um projeto que tenha sido carregado a partir do [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] está bloqueado e só pode ser editado no Project.</span><span class="sxs-lookup"><span data-stu-id="669c4-158">By default, a project that’s been uploaded from [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] is locked and can only be edited in Project.</span></span> <span data-ttu-id="669c4-159">Para editar o ficheiro no [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], o ficheiro tem de estar desassociado.</span><span class="sxs-lookup"><span data-stu-id="669c4-159">To edit the file in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], the file has to be unlinked.</span></span>  

### <a name="edit-in-pn_microsoft_project"></a><span data-ttu-id="669c4-160">Editar no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]</span><span class="sxs-lookup"><span data-stu-id="669c4-160">Edit in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]</span></span>  

1. <span data-ttu-id="669c4-161">No menu principal, clique em **Project Service** > **Projetos**.</span><span class="sxs-lookup"><span data-stu-id="669c4-161">From the main menu, click **Project Service** > **Projects**.</span></span>  

2. <span data-ttu-id="669c4-162">Na lista de projetos, abra aquele que criou no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="669c4-162">From the list of projects, open the one you created in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

3. <span data-ttu-id="669c4-163">Clique em **Abrir no MS Project** a partir do friso.</span><span class="sxs-lookup"><span data-stu-id="669c4-163">Click **Open in MS Project** from the ribbon.</span></span> <span data-ttu-id="669c4-164">É aberto o ficheiro mestre associado no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="669c4-164">This will open the linked master file in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a><span data-ttu-id="669c4-165">Desassocie um ficheiro e edite-o no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service</span><span class="sxs-lookup"><span data-stu-id="669c4-165">Unlink a file and edit in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service</span></span>  

1. <span data-ttu-id="669c4-166">No menu principal, clique em **Project Service** > **Projetos**.</span><span class="sxs-lookup"><span data-stu-id="669c4-166">From the main menu, click **Project Service** > **Projects**.</span></span>  

2. <span data-ttu-id="669c4-167">Na lista de projetos, abra aquele que criou no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="669c4-167">From the list of projects, open the one you created in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

3. <span data-ttu-id="669c4-168">Clique em **Desassociar do MS Project** a partir do friso.</span><span class="sxs-lookup"><span data-stu-id="669c4-168">Click **Unlink from MS Project** from the ribbon.</span></span>  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a><span data-ttu-id="669c4-169">Carregar um ficheiro de Projeto para o SharePoint ou os Grupos do Office</span><span class="sxs-lookup"><span data-stu-id="669c4-169">Upload a Project file to SharePoint or Office Groups</span></span>  
 <span data-ttu-id="669c4-170">Pode carregar o ficheiro do Project para o SharePoint e encontrá-lo em Documentos Associados para o seu projeto do [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="669c4-170">You can upload your Project file to SharePoint and find it under the Associated Documents for your [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  <span data-ttu-id="669c4-171">O respetivo administrador tem de configurar a gestão de documentos do SharePoint e ativá-lo para a entidade do Projeto.</span><span class="sxs-lookup"><span data-stu-id="669c4-171">You need to have your administrator configure SharePoint document management and turn it on for the Project entity.</span></span> 

 <span data-ttu-id="669c4-172">Também pode carregar o ficheiro do Project para o [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] se tiver Grupos do Office configurados.</span><span class="sxs-lookup"><span data-stu-id="669c4-172">You can also upload your Project file to [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] if you have Office Groups set up.</span></span>

### <a name="upload-a-file-for-sharepoint"></a><span data-ttu-id="669c4-173">Carregar um ficheiro para o SharePoint</span><span class="sxs-lookup"><span data-stu-id="669c4-173">Upload a file for SharePoint</span></span>  

1. <span data-ttu-id="669c4-174">No menu principal, clique em **Project Service** > **Carregar**.</span><span class="sxs-lookup"><span data-stu-id="669c4-174">From the main menu, click **Project Service** > **Upload**.</span></span>  

2. <span data-ttu-id="669c4-175">Selecione **Aos Documentos do Projeto do Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="669c4-175">Select **To Project Service Automation Project Documents**.</span></span>  

3. <span data-ttu-id="669c4-176">Na caixa de diálogo **Ativar Abrir no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** , selecione **Sim** ou **Não**.</span><span class="sxs-lookup"><span data-stu-id="669c4-176">On the **Enable Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** dialog, select **Yes** or **No**.</span></span>  

   - <span data-ttu-id="669c4-177">Se clicar em **Sim** , poderá selecionar o botão **Abrir no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** no Project Service Automation, iniciar o [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] e carregar o ficheiro do Projeto a partir da biblioteca de documentos do SharePoint.</span><span class="sxs-lookup"><span data-stu-id="669c4-177">If you click **Yes** , you'll be able select the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button in Project Service Automation, launch [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], and load the Project file from the SharePoint document library.</span></span>  

   - <span data-ttu-id="669c4-178">Se clicar em **Não** , a associação ao botão **Abrir no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** não funcionará.</span><span class="sxs-lookup"><span data-stu-id="669c4-178">If you click **No** , the link for the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button won't work.</span></span>  

4. <span data-ttu-id="669c4-179">O ficheiro do [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] pode ser encontrado no [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] em **Documentos** para o projeto da [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] específico.</span><span class="sxs-lookup"><span data-stu-id="669c4-179">The [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] file can be found in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Documents** for the specific [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  

### <a name="upload-a-file-for-office-groups"></a><span data-ttu-id="669c4-180">Carregar um ficheiro para os Grupos do Office</span><span class="sxs-lookup"><span data-stu-id="669c4-180">Upload a file for Office Groups</span></span>  

1. <span data-ttu-id="669c4-181">No menu principal, clique em **Project Service** > **Carregar**.</span><span class="sxs-lookup"><span data-stu-id="669c4-181">From the main menu, click **Project Service** > **Upload**.</span></span>  

2. <span data-ttu-id="669c4-182">Selecione **Aos Documentos do Projeto do Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="669c4-182">Select **To Project Service Automation Project Documents**.</span></span>  

3. <span data-ttu-id="669c4-183">Na caixa de diálogo **Ativar Abrir no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** , selecione **Sim** ou **Não**.</span><span class="sxs-lookup"><span data-stu-id="669c4-183">On the **Enable Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** dialog, select **Yes** or **No**.</span></span>  

   - <span data-ttu-id="669c4-184">Se clicar em **Sim** , poderá selecionar o botão **Abrir no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** no Project Service Automation, iniciar o [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] e carregar o ficheiro do Projeto a partir da biblioteca de documentos do SharePoint.</span><span class="sxs-lookup"><span data-stu-id="669c4-184">If you click **Yes** , you'll be able to select the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button in Project Service Automation, launch [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], and load the Project file from the SharePoint document library.</span></span>  

   - <span data-ttu-id="669c4-185">Se clicar em **Não** , a associação ao botão **Abrir no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** não funcionará.</span><span class="sxs-lookup"><span data-stu-id="669c4-185">If you click **No** , the link for the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button won't work.</span></span>  

4. <span data-ttu-id="669c4-186">O ficheiro do [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] pode ser encontrado no [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] em **Documentos** para o projeto da [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] específico.</span><span class="sxs-lookup"><span data-stu-id="669c4-186">The [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] file can be found in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Documents** for the specific [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  

## <a name="publish--your-project-as-a-template"></a><span data-ttu-id="669c4-187">Publicar o projeto como um modelo</span><span class="sxs-lookup"><span data-stu-id="669c4-187">Publish  your project as a template</span></span>  
 <span data-ttu-id="669c4-188">Pode guardar o projeto e reutilizá-lo ao guardá-lo como um modelo de projeto na [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="669c4-188">You can save your project and reuse it by saving it as a project template in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  <span data-ttu-id="669c4-189">Os modelos de projeto estão planos de projeto reutilizáveis na [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="669c4-189">Project templates are reusable project plans in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="669c4-190">[Criar um modelo do projeto (Project Service Automation)](../psa/create-project-template.md)</span><span class="sxs-lookup"><span data-stu-id="669c4-190">[Create a project template (Project Service Automation)](../psa/create-project-template.md)</span></span>  

1. <span data-ttu-id="669c4-191">A partir do separador **Project Service** , clique em **Publicar** > **Novo Modelo de Projeto do Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="669c4-191">From the **Project Service** tab, click **Publish** > **New Project Service Automation Project Template**.</span></span>  

2. <span data-ttu-id="669c4-192">Na caixa de diálogo **Publicar num novo modelo de projeto do Project Service** , introduza o **Nome do modelo de projeto**.</span><span class="sxs-lookup"><span data-stu-id="669c4-192">On the **Publish to a new project in Project Service template** dialog box, enter the **Project template name**.</span></span>  

3. <span data-ttu-id="669c4-193">Opcionalmente, marque **Associar plano do projeto ao Project Service Automation** para associar o ficheiro de Projeto ao [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="669c4-193">Optionally, check the **Link project plan to Project Service Automation** to link the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

4. <span data-ttu-id="669c4-194">Clique em  **Publicar**.</span><span class="sxs-lookup"><span data-stu-id="669c4-194">Click **Publish**.</span></span>  

<span data-ttu-id="669c4-195">Ao associar o ficheiro do Projeto à [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], torna o ficheiro do Projeto o registo mestre e define a estrutura hierárquica do trabalho no modelo da [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] como só de leitura.</span><span class="sxs-lookup"><span data-stu-id="669c4-195">Linking the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] makes the Project file the master and sets the work breakdown structure in the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] template to read-only.</span></span>  <span data-ttu-id="669c4-196">As alterações ao plano do projeto têm de ser feitas no [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] e publicadas como atualizações à [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="669c4-196">In order to make changes to the project plan, you need to make them in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and publish them as updates to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>

### <a name="see-also"></a><span data-ttu-id="669c4-197">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="669c4-197">See Also</span></span>  
 [<span data-ttu-id="669c4-198">Guia do Gestor de Projeto</span><span class="sxs-lookup"><span data-stu-id="669c4-198">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
