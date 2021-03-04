---
title: Resolução de problemas a trabalhar na grelha de tarefas
description: Esta tópico fornece informações necessárias para a resolução de problemas quando trabalham na grelha de tarefas.
author: ruhercul
manager: tfehr
ms.date: 01/19/2021
ms.topic: article
ms.product: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 89bbad62c2a0a5693a57cf5c9a812ab644486469
ms.sourcegitcommit: c9edb4fc3042d97cb1245be627841e0a984dbdea
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 01/19/2021
ms.locfileid: "5031551"
---
# <a name="troubleshoot-working-in-the-task-grid"></a><span data-ttu-id="08313-103">Resolução de problemas a trabalhar na grelha de tarefas</span><span class="sxs-lookup"><span data-stu-id="08313-103">Troubleshoot working in the Task grid</span></span> 

<span data-ttu-id="08313-104">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="08313-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="08313-105">Este tópico descreve como corrigir problemas que pode encontrar enquanto trabalha com a gestão de custos.</span><span class="sxs-lookup"><span data-stu-id="08313-105">This topic describes how to fix issues that you might encounter while working with cost management.</span></span>

## <a name="enable-cookies"></a><span data-ttu-id="08313-106">Ativar cookies</span><span class="sxs-lookup"><span data-stu-id="08313-106">Enable cookies</span></span>

<span data-ttu-id="08313-107">O Project Operations requer que os cookies de terceiros sejam ativados de forma a compor a estrutura hierárquica do trabalho.</span><span class="sxs-lookup"><span data-stu-id="08313-107">Project Operations requires that third-party cookies be enabled in order to render the work breakdown structure.</span></span> <span data-ttu-id="08313-108">Quando os cookies de terceiros não estiverem ativados, em vez de ver tarefas, verá uma página em branco quando selecionar o separador **Tarefas** na página **Projeto**.</span><span class="sxs-lookup"><span data-stu-id="08313-108">When third-party cookies aren't enabled, instead of seeing tasks, you will see a blank page when you select the **Tasks** tab on the **Project** page.</span></span>

![Separador em branco quando os cookies de terceiros não estão ativados](media/blankschedule.png)


### <a name="workaround"></a><span data-ttu-id="08313-110">Solução</span><span class="sxs-lookup"><span data-stu-id="08313-110">Workaround</span></span>
<span data-ttu-id="08313-111">Para Microsoft Edge ou para os navegadores Google Chrome, os seguintes procedimentos descrevem como atualizar a configuração do seu navegador para ativar cookies de terceiros.</span><span class="sxs-lookup"><span data-stu-id="08313-111">For Microsoft Edge or Google Chrome browsers, the following procedures outline how to update your browser setting to enable third-party cookies.</span></span>

#### <a name="microsoft-edge"></a><span data-ttu-id="08313-112">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="08313-112">Microsoft Edge</span></span>

1. <span data-ttu-id="08313-113">Abra o browser Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="08313-113">Open your Edge browser.</span></span>
2. <span data-ttu-id="08313-114">No canto superior direito, selecione **elipse** (...) e, em seguida, **Definições**.</span><span class="sxs-lookup"><span data-stu-id="08313-114">In the upper-right corner, select the **ellipsis** (...), and then select **Settings**.</span></span>
3. <span data-ttu-id="08313-115">Sob **Cookies e permissões do site**, selecione **Cookies e dados do site**.</span><span class="sxs-lookup"><span data-stu-id="08313-115">Under **Cookies and site permissions**, select **Cookies and site data**.</span></span>
4. <span data-ttu-id="08313-116">Desligue os **cookies de terceiros do bloco**.</span><span class="sxs-lookup"><span data-stu-id="08313-116">Turn off **Block third-party cookies**.</span></span>

#### <a name="google-chrome"></a><span data-ttu-id="08313-117">Google Chrome</span><span class="sxs-lookup"><span data-stu-id="08313-117">Google Chrome</span></span>

1. <span data-ttu-id="08313-118">Abra o browser Chrome.</span><span class="sxs-lookup"><span data-stu-id="08313-118">Open your Chrome browser.</span></span>
2. <span data-ttu-id="08313-119">No canto superior direito, selecione os três pontos verticais e, em seguida, selecione **Definições**.</span><span class="sxs-lookup"><span data-stu-id="08313-119">In the upper-right corner, select the three vertical dots, and then select **Settings**.</span></span>
3. <span data-ttu-id="08313-120">Sob **Privacidade e segurança**, selecione **Cookies e outros dados do site**.</span><span class="sxs-lookup"><span data-stu-id="08313-120">Under **Privacy and security**, select **Cookies and other site data**.</span></span>
4. <span data-ttu-id="08313-121">Selecione **Permitir todas as cookies**.</span><span class="sxs-lookup"><span data-stu-id="08313-121">Select **Allow all cookies**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="08313-122">Se bloquear cookies de terceiros, todos os cookies e dados do site de outros sites serão bloqueados, mesmo que o site seja permitido na sua lista de exceções.</span><span class="sxs-lookup"><span data-stu-id="08313-122">If you block third-party cookies, all cookies and site data from other sites will be blocked, even if the site is allowed on your exceptions list.</span></span>

## <a name="pex-endpoint"></a><span data-ttu-id="08313-123">Ponto final de PEX</span><span class="sxs-lookup"><span data-stu-id="08313-123">PEX Endpoint</span></span>

<span data-ttu-id="08313-124">O Project Operations requer que um parâmetro de projeto refira o ponto final PEX.</span><span class="sxs-lookup"><span data-stu-id="08313-124">Project Operations requires that a project parameter reference the PEX Endpoint.</span></span> <span data-ttu-id="08313-125">Este ponto final é necessário para comunicar com o serviço utilizado para compor a estrutura hierárquica do trabalho.</span><span class="sxs-lookup"><span data-stu-id="08313-125">This endpoint is required to communicate with the service used to render the work breakdown structure.</span></span> <span data-ttu-id="08313-126">Se o parâmetro não estiver ativado, receberá o erro: "O parâmetro do projeto não é válido".</span><span class="sxs-lookup"><span data-stu-id="08313-126">If the parameter isn't enabled, you will receive the error, "The project parameter is not valid".</span></span> 

### <a name="workaround"></a><span data-ttu-id="08313-127">Solução</span><span class="sxs-lookup"><span data-stu-id="08313-127">Workaround</span></span>
 ![Campo PEX ponto final no parâmetro do projeto](media/projectparameter.png)

1. <span data-ttu-id="08313-129">Adicione o campo **ponto final PEX** à página **Parâmetros do Projeto**.</span><span class="sxs-lookup"><span data-stu-id="08313-129">Add the **PEX Endpoint** field to the **Project Parameters** page.</span></span>
2. <span data-ttu-id="08313-130">Atualize o campo com o seguinte valor: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`</span><span class="sxs-lookup"><span data-stu-id="08313-130">Update the field with the following value: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`</span></span>
3. <span data-ttu-id="08313-131">Retire o campo da página **Parâmetros do Projeto**.</span><span class="sxs-lookup"><span data-stu-id="08313-131">Remove the field from the **Project Parameters** page.</span></span>

## <a name="privileges-for-project-for-the-web"></a><span data-ttu-id="08313-132">Privilégios para Projeto para a Web</span><span class="sxs-lookup"><span data-stu-id="08313-132">Privileges for Project for the Web</span></span>

<span data-ttu-id="08313-133">O Project Operations conta com um serviço de agendamento externo.</span><span class="sxs-lookup"><span data-stu-id="08313-133">Project Operations relies on an external scheduling service.</span></span> <span data-ttu-id="08313-134">O serviço requer que um utilizador tenha várias funções atribuídas para ler e escrever a entidades relacionadas com a estrutura hierárquica do trabalho.</span><span class="sxs-lookup"><span data-stu-id="08313-134">The service requires that a user have several roles assigned to read and write to entities related to the work breakdown structure.</span></span> <span data-ttu-id="08313-135">Estas entidades incluem tarefas de projeto, atribuições de recursos e dependências de tarefas.</span><span class="sxs-lookup"><span data-stu-id="08313-135">These entities include project tasks, resource assignments, and task dependencies.</span></span> <span data-ttu-id="08313-136">Se um utilizador não consegue tornar a estrutura hierárquica do trabalho quando vai para o separador **Tarefas**, é provavelmente porque o Project for Project Operations não foi ativado.</span><span class="sxs-lookup"><span data-stu-id="08313-136">If a user can't render the work breakdown structure when they go to the **Tasks** tab, it's probably because Project for Project Operations hasn't been enabled.</span></span> <span data-ttu-id="08313-137">Um utilizador pode receber um erro de direito de acesso ou um erro relacionado com uma negação de acesso.</span><span class="sxs-lookup"><span data-stu-id="08313-137">A user might receive either a security role error, or an error related to a denial of access.</span></span>


## <a name="workaround"></a><span data-ttu-id="08313-138">Solução</span><span class="sxs-lookup"><span data-stu-id="08313-138">Workaround</span></span>

1. <span data-ttu-id="08313-139">Ir para **Definição > Segurança > Utilizadores > Utilizadores de Aplicações**.</span><span class="sxs-lookup"><span data-stu-id="08313-139">Go to **Setting > Security > Users > Application Users**.</span></span>  

   ![Leitor de aplicação](media/applicationuser.jpg)
   
2. <span data-ttu-id="08313-141">Clique duas vezes no registo do utilizador da aplicação para verificar o seguinte:</span><span class="sxs-lookup"><span data-stu-id="08313-141">Double-click the application user record to verify the following:</span></span>

 - <span data-ttu-id="08313-142">O utilizador tem acesso ao projeto.</span><span class="sxs-lookup"><span data-stu-id="08313-142">The user has access to the project.</span></span> <span data-ttu-id="08313-143">Esta verificação é normalmente feita garantindo que o utilizador tem direito de acesso ao **Gestor de projeto**.</span><span class="sxs-lookup"><span data-stu-id="08313-143">This verification is typically done by ensuring that the user has **Project Manager** security role.</span></span>
 - <span data-ttu-id="08313-144">O utilizador da aplicação Microsoft Project existe e está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="08313-144">The Microsoft Project application user exists and is configured correctly.</span></span>
 
3. <span data-ttu-id="08313-145">Seeste utilizador não existir, pode criar um novo registo de utilizador.</span><span class="sxs-lookup"><span data-stu-id="08313-145">If this user doesn't exist, you can create a new user record.</span></span> <span data-ttu-id="08313-146">Selecionar **Novos utilizadores**.</span><span class="sxs-lookup"><span data-stu-id="08313-146">Select **New Users**.</span></span> <span data-ttu-id="08313-147">Altere o formulário de inscrição para **Utilizador de Aplicações** e adicione o **ID da aplicação**.</span><span class="sxs-lookup"><span data-stu-id="08313-147">Change the entry form to **Application User**, and then add the **Application ID**.</span></span>

   ![Detalhes da candidatura do utilizador](media/applicationuserdetails.jpg)

4. <span data-ttu-id="08313-149">Verifique se o utilizador foi atribuído a licença correta e se o serviço está ativado nos detalhes dos planos de serviço da licença.</span><span class="sxs-lookup"><span data-stu-id="08313-149">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
5. <span data-ttu-id="08313-150">Verifique se o utilizador pode abrir project.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="08313-150">Verify that the user can open project.microsoft.com.</span></span>
6. <span data-ttu-id="08313-151">Verifique através dos parâmetros do projeto que o sistema está apontando para o projeto correto ponto final.</span><span class="sxs-lookup"><span data-stu-id="08313-151">Verify through the project parameters that the system is pointing to the correct project endpoint.</span></span>
7. <span data-ttu-id="08313-152">Verifique se a candidatura de projeto do utilizador foi criada</span><span class="sxs-lookup"><span data-stu-id="08313-152">Verify that the project application user is created.</span></span>
8. <span data-ttu-id="08313-153">Aplicar as seguintes funções de segurança ao utilizador:</span><span class="sxs-lookup"><span data-stu-id="08313-153">Apply the following security roles to the user:</span></span>

  - <span data-ttu-id="08313-154">Utilizador do Dataverse</span><span class="sxs-lookup"><span data-stu-id="08313-154">Dataverse User</span></span>
  - <span data-ttu-id="08313-155">Sistema do Project Operations</span><span class="sxs-lookup"><span data-stu-id="08313-155">Project Operations System</span></span>
  - <span data-ttu-id="08313-156">Sistema do projeto</span><span class="sxs-lookup"><span data-stu-id="08313-156">Project System</span></span>

## <a name="error-when-updating-the-work-breakdown-structure"></a><span data-ttu-id="08313-157">Erro ao atualizar a estrutura hierárquica do trabalho</span><span class="sxs-lookup"><span data-stu-id="08313-157">Error when updating the work breakdown structure</span></span>

<span data-ttu-id="08313-158">Quando uma ou mais atualizações são feitas para a estrutura hierárquica do trabalho, as alterações acabam por falhar e não são salvas.</span><span class="sxs-lookup"><span data-stu-id="08313-158">When one or more updates are made to the work breakdown structure, the changes eventually fail and aren't saved.</span></span> <span data-ttu-id="08313-159">Ocorre um erro na grelha de agenda, notando que "Não foi possível salvar a mudança recente que fez."</span><span class="sxs-lookup"><span data-stu-id="08313-159">An error occurs in the schedule grid noting that “Recent change you’ve made couldn’t be saved.”</span></span>

### <a name="workaround"></a><span data-ttu-id="08313-160">Solução</span><span class="sxs-lookup"><span data-stu-id="08313-160">Workaround</span></span>

1. <span data-ttu-id="08313-161">Verifique se o utilizador foi atribuído a licença correta e se o serviço está ativado nos detalhes dos planos de serviço da licença.</span><span class="sxs-lookup"><span data-stu-id="08313-161">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
2. <span data-ttu-id="08313-162">Verifique se o utilizador pode abrir project.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="08313-162">Verify that the user can open project.microsoft.com.</span></span>
3. <span data-ttu-id="08313-163">Verifique que o sistema está a apontar para o projeto correto ponto final.</span><span class="sxs-lookup"><span data-stu-id="08313-163">Verify that the system is pointing to the correct project endpoint,.</span></span>
4. <span data-ttu-id="08313-164">Verifique se a Candidatura de projeto do utilizador tenha sido criada.</span><span class="sxs-lookup"><span data-stu-id="08313-164">Verify that the Project Application user has been created.</span></span>
5. <span data-ttu-id="08313-165">Aplicar as seguintes funções de segurança ao utilizador:</span><span class="sxs-lookup"><span data-stu-id="08313-165">Apply the following security roles to the user:</span></span>
  
  - <span data-ttu-id="08313-166">Utilizador ou Utilizador base Dataverse</span><span class="sxs-lookup"><span data-stu-id="08313-166">Dataverse user or Base user</span></span>
  - <span data-ttu-id="08313-167">Sistema do Project Operations</span><span class="sxs-lookup"><span data-stu-id="08313-167">Project Operations System</span></span>
  - <span data-ttu-id="08313-168">Sistema do projeto</span><span class="sxs-lookup"><span data-stu-id="08313-168">Project System</span></span>
  - <span data-ttu-id="08313-169">Sistema de Escrita Dupla do Project Operations (Esta função é necessária se estiver a implementar o cenário baseado em recursos/não armazenados do Project Operations.)</span><span class="sxs-lookup"><span data-stu-id="08313-169">Project Operations Dual Write System (This role is required if you are deploying the resource/non-stocked based scenario of Project Operations.)</span></span>
