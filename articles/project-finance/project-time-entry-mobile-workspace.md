---
title: Área de trabalho móvel da entrada de hora do projeto
description: Este tópico fornece informações sobre a área de trabalho móvel da entrada de hora do Projeto. Esta área de trabalho permite aos utilizadores introduzir e guardar as horas num projeto através do seu dispositivo móvel.
author: KimANelson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: ee11f7f392676adb59bd25f6549737482faf5fdb
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754548"
---
# <a name="project-time-entry-mobile-workspace"></a><span data-ttu-id="cc75f-104">Área de trabalho móvel da entrada de hora do projeto</span><span class="sxs-lookup"><span data-stu-id="cc75f-104">Project time entry mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cc75f-105">Este tópico fornece informações sobre a área de trabalho móvel **Entrada de hora do projeto**.</span><span class="sxs-lookup"><span data-stu-id="cc75f-105">This topic provides information about the **Project time entry** mobile workspace.</span></span> <span data-ttu-id="cc75f-106">Esta área de trabalho permite aos utilizadores introduzir e guardar as horas num projeto através do seu dispositivo móvel.</span><span class="sxs-lookup"><span data-stu-id="cc75f-106">This workspace lets users enter and save time against a project by using their mobile device.</span></span>

<span data-ttu-id="cc75f-107">Esta área de trabalho móvel destina-se a ser utilizada com a aplicação móvel Dynamics 365 Unified Ops.</span><span class="sxs-lookup"><span data-stu-id="cc75f-107">This mobile workspace is intended to be used with the Dynamics 365 Unified Ops mobile app.</span></span> 

## <a name="overview"></a><span data-ttu-id="cc75f-108">Descrição Geral</span><span class="sxs-lookup"><span data-stu-id="cc75f-108">Overview</span></span>
<span data-ttu-id="cc75f-109">Como parte do seu trabalho diário, os recursos do projeto estão muitas vezes no local ou a viajar.</span><span class="sxs-lookup"><span data-stu-id="cc75f-109">As part of their daily work, project resources are often on-site or traveling.</span></span> <span data-ttu-id="cc75f-110">A área de trabalho móvel **Entrada de hora do projeto** permite que os utilizadores introduzam as horas faturáveis ou não faturáveis para um projeto no dispositivo móvel à sua escolha.</span><span class="sxs-lookup"><span data-stu-id="cc75f-110">The **Project time entry** mobile workspace lets users enter their billable or non-billable time against a project on the mobile device of their choice.</span></span> <span data-ttu-id="cc75f-111">Por isso, os recursos do projeto podem registar entradas de hora a qualquer altura e em qualquer lugar.</span><span class="sxs-lookup"><span data-stu-id="cc75f-111">Therefore, project resources can record time entries anytime and anywhere.</span></span> <span data-ttu-id="cc75f-112">Também podem ver as entradas de hora que já foram registadas.</span><span class="sxs-lookup"><span data-stu-id="cc75f-112">They can also view time entries that have already been recorded.</span></span> 

<span data-ttu-id="cc75f-113">Especificamente, na área de trabalho móvel **Entrada de hora do projeto**, os utilizadores podem executar estas tarefas:</span><span class="sxs-lookup"><span data-stu-id="cc75f-113">Specifically, in the **Project time entry** mobile workspace, users can perform these tasks:</span></span>

-   <span data-ttu-id="cc75f-114">Para qualquer data selecionada, introduza o número de horas que gastou numa tarefa específica.</span><span class="sxs-lookup"><span data-stu-id="cc75f-114">For any selected date, enter the number of hours that you spent on a specific task.</span></span>
-   <span data-ttu-id="cc75f-115">Procure por nome de projeto ou cliente para localizar o projeto para o qual pretende introduzir horas.</span><span class="sxs-lookup"><span data-stu-id="cc75f-115">Search by project name or customer to find the project to enter time for.</span></span>
-   <span data-ttu-id="cc75f-116">Especifique a categoria e a atividade pelo tempo que dedicou.</span><span class="sxs-lookup"><span data-stu-id="cc75f-116">Specify the category and activity for the time that you spent.</span></span>
-   <span data-ttu-id="cc75f-117">Registe o tempo como faturável ou não faturável para o projeto.</span><span class="sxs-lookup"><span data-stu-id="cc75f-117">Record the time as billable or non-billable for the project.</span></span>
-   <span data-ttu-id="cc75f-118">Opcionalmente,: introduza quaisquer comentários externos ou internos.</span><span class="sxs-lookup"><span data-stu-id="cc75f-118">Optionally enter any external or internal comments.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="cc75f-119">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="cc75f-119">Prerequisites</span></span>
<span data-ttu-id="cc75f-120">Os pré-requisitos diferem consoante a versão do Microsoft Dynamics 365 que foi implementada para a sua organização.</span><span class="sxs-lookup"><span data-stu-id="cc75f-120">The prerequisites differ, based on the version of Microsoft Dynamics 365 that has been deployed for your organization.</span></span>

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a><span data-ttu-id="cc75f-121">Pré-requisitos se utilizar o Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="cc75f-121">Prerequisites if you use Dynamics 365 Finance</span></span>
<span data-ttu-id="cc75f-122">Se o Finance foi implementado para a sua organização, o administrador de sistema tem de publicar a área de trabalho móvel **Entrada de hora do projeto**.</span><span class="sxs-lookup"><span data-stu-id="cc75f-122">If Finance has been deployed for your organization, the system administrator must publish the **Project time entry** mobile workspace.</span></span> <span data-ttu-id="cc75f-123">Para obter instruções, consulte [Publicar uma área de trabalho móvel](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="cc75f-123">For instructions, see [Publish a mobile workspace](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span></span>

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a><span data-ttu-id="cc75f-124">Pré-requisitos se utilizar a versão 1611 com a Platform update 3 ou posterior</span><span class="sxs-lookup"><span data-stu-id="cc75f-124">Prerequisites if you use version 1611 with Platform update 3 or later</span></span>
<span data-ttu-id="cc75f-125">Se a versão 1611 com a Platform update 3 ou posterior tiver sido implementada para a sua organização, o administrador de sistema tem de satisfazer os seguintes pré-requisitos.</span><span class="sxs-lookup"><span data-stu-id="cc75f-125">If version 1611 with Platform update 3 or later has been deployed for your organization, the system administrator must complete the following prerequisites.</span></span> 

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="cc75f-126">Pré-requisito</span><span class="sxs-lookup"><span data-stu-id="cc75f-126">Prerequisite</span></span></th>
<th><span data-ttu-id="cc75f-127">Função</span><span class="sxs-lookup"><span data-stu-id="cc75f-127">Role</span></span></th>
<th><span data-ttu-id="cc75f-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="cc75f-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">

<td><span data-ttu-id="cc75f-129">Implementar KB 4018050.</span><span class="sxs-lookup"><span data-stu-id="cc75f-129">Implement KB 4018050.</span></span></td>
<td><span data-ttu-id="cc75f-130">Administrador de sistema</span><span class="sxs-lookup"><span data-stu-id="cc75f-130">System administrator</span></span></td>
<td><span data-ttu-id="cc75f-131">O KB 4018050 é uma atualização de is X++ ou correção de metadados que contém a área de trabalho móvel <strong>Entrada de hora do projeto</strong>.</span><span class="sxs-lookup"><span data-stu-id="cc75f-131">KB 4018050 is an X++ update or metadata hotfix that contains the <strong>Project time entry</strong> mobile workspace.</span></span> <span data-ttu-id="cc75f-132">Para implementar o KB 4018050, o seu administrador de sistema tem de seguir estes passos.</span><span class="sxs-lookup"><span data-stu-id="cc75f-132">To implement KB 4018050, your system administrator must follow these steps.</span></span>
<ol>
<li><span data-ttu-id="cc75f-133"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Transfira a correção de metadados do Microsoft Dynamics Lifecycle Services (LCS)</a>.</span><span class="sxs-lookup"><span data-stu-id="cc75f-133"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Download the metadata hotfix from Microsoft Dynamics Lifecycle Services (LCS)</a>.</span></span></li>
<li><span data-ttu-id="cc75f-134"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Instale a correção de metadados</a>.</span><span class="sxs-lookup"><span data-stu-id="cc75f-134"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Install the metadata hotfix</a>.</span></span></li>
<li><span data-ttu-id="cc75f-135"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Crie um pacote implementável</a> que contenha os modelos <strong>ApplicationSuite</strong> e <strong>ProjectMobile</strong> e, em seguida, carregue o pacote implementável para o LCS.</span><span class="sxs-lookup"><span data-stu-id="cc75f-135"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Create a deployable package</a> that contains the <strong>ApplicationSuite</strong> and <strong>ProjectMobile</strong> models, and then upload the deployable package to LCS.</span></span></li>
<li><span data-ttu-id="cc75f-136"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Aplique o pacote implementável</a>.</span><span class="sxs-lookup"><span data-stu-id="cc75f-136"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Apply the deployable package</a>.</span></span></li>

</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cc75f-137">Publique a área de trabalho móvel <strong>Entrada de hora do projeto</strong>.</span><span class="sxs-lookup"><span data-stu-id="cc75f-137">Publish the <strong>Project time entry</strong> mobile workspace.</span></span></td>
<td><span data-ttu-id="cc75f-138">Administrador de sistema</span><span class="sxs-lookup"><span data-stu-id="cc75f-138">System administrator</span></span></td>
<td><span data-ttu-id="cc75f-139">Consulte <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Publicar uma área de trabalho móvel</a>.</span><span class="sxs-lookup"><span data-stu-id="cc75f-139">See <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="cc75f-140">Transferir e instalar a aplicação móvel</span><span class="sxs-lookup"><span data-stu-id="cc75f-140">Download and install the mobile app</span></span>

<span data-ttu-id="cc75f-141">Transferir e instalar a aplicação móvel Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="cc75f-141">Download and install the Finance and Operations mobile app:</span></span>

-   [<span data-ttu-id="cc75f-142">Para telemóveis Android</span><span class="sxs-lookup"><span data-stu-id="cc75f-142">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="cc75f-143">Para iPhones</span><span class="sxs-lookup"><span data-stu-id="cc75f-143">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="cc75f-144">Iniciar sessão na aplicação móvel</span><span class="sxs-lookup"><span data-stu-id="cc75f-144">Sign in to the mobile app</span></span>
1.  <span data-ttu-id="cc75f-145">Inicie a aplicação no seu dispositivo móvel.</span><span class="sxs-lookup"><span data-stu-id="cc75f-145">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="cc75f-146">Introduza o seu URL do Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="cc75f-146">Enter your Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="cc75f-147">Quando iniciar sessão pela primeira vez, ser-lhe-á solicitado o nome de utilizador e a palavra-passe.</span><span class="sxs-lookup"><span data-stu-id="cc75f-147">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="cc75f-148">Introduza as suas credenciais.</span><span class="sxs-lookup"><span data-stu-id="cc75f-148">Enter your credentials.</span></span>
4.  <span data-ttu-id="cc75f-149">Depois de iniciar sessão, são mostradas as áreas de trabalho disponíveis para a sua empresa.</span><span class="sxs-lookup"><span data-stu-id="cc75f-149">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="cc75f-150">Note que, se o seu administrador de sistema publicar uma nova área de trabalho mais tarde, terá de atualizar a lista de áreas de trabalho móveis.</span><span class="sxs-lookup"><span data-stu-id="cc75f-150">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

<span data-ttu-id="cc75f-151">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="cc75f-151">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a><span data-ttu-id="cc75f-152">Introduza o tempo através da área de trabalho móvel Entrada de hora do projeto</span><span class="sxs-lookup"><span data-stu-id="cc75f-152">Enter time by using the Project time entry mobile workspace</span></span>
1.  <span data-ttu-id="cc75f-153">No seu dispositivo móvel, selecione a área de trabalho **Entrada de hora do projeto**.</span><span class="sxs-lookup"><span data-stu-id="cc75f-153">On your mobile device, select the **Project time entry** workspace.</span></span>
2.  <span data-ttu-id="cc75f-154">Selecione **Entrada de hora**.</span><span class="sxs-lookup"><span data-stu-id="cc75f-154">Select **Time entry**.</span></span> <span data-ttu-id="cc75f-155">São mostradas as datas do calendário da semana atual.</span><span class="sxs-lookup"><span data-stu-id="cc75f-155">The calendar dates for the current week are shown.</span></span>
3.  <span data-ttu-id="cc75f-156">Para uma data selecionada, selecione **Ações** &gt; **Nova entrada**.</span><span class="sxs-lookup"><span data-stu-id="cc75f-156">For a selected date, select **Actions** &gt; **New entry**.</span></span>
4.  <span data-ttu-id="cc75f-157">Introduza o número de horas a registar.</span><span class="sxs-lookup"><span data-stu-id="cc75f-157">Enter the number of hours to record.</span></span>
5.  <span data-ttu-id="cc75f-158">Selecione o projeto para a entrada de hora.</span><span class="sxs-lookup"><span data-stu-id="cc75f-158">Select the project for the time entry.</span></span> <span data-ttu-id="cc75f-159">Uma lista mostra os projetos que são carregados na sua aplicação para utilização offline.</span><span class="sxs-lookup"><span data-stu-id="cc75f-159">A list shows the projects that are loaded into your app for offline use.</span></span> <span data-ttu-id="cc75f-160">Por predefinição, são carregados 50 itens, mas um programador pode alterar este número.</span><span class="sxs-lookup"><span data-stu-id="cc75f-160">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="cc75f-161">Para mais informações, consulte [Plataforma móvel](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span><span class="sxs-lookup"><span data-stu-id="cc75f-161">For more information, see [Mobile platform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span></span>
6.  <span data-ttu-id="cc75f-162">Se o seu projeto não estiver na lista, selecione **Procurar**.</span><span class="sxs-lookup"><span data-stu-id="cc75f-162">If your project isn't in the list, select **Search**.</span></span> <span data-ttu-id="cc75f-163">Procure por nome ou mude para a pesquisa por nome de projeto ou cliente.</span><span class="sxs-lookup"><span data-stu-id="cc75f-163">Search by name, or switch to search by project name or customer.</span></span>
7.  <span data-ttu-id="cc75f-164">Selecione uma categoria.</span><span class="sxs-lookup"><span data-stu-id="cc75f-164">Select a category.</span></span> <span data-ttu-id="cc75f-165">Uma lista mostra as categorias que são carregadas na sua aplicação para utilização offline.</span><span class="sxs-lookup"><span data-stu-id="cc75f-165">A list shows the categories that are loaded into your app for offline use.</span></span> <span data-ttu-id="cc75f-166">Por predefinição, são carregados 50 itens, mas um programador pode alterar este número.</span><span class="sxs-lookup"><span data-stu-id="cc75f-166">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="cc75f-167">Para mais informações, consulte [Plataforma móvel](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span><span class="sxs-lookup"><span data-stu-id="cc75f-167">For more information, see [Mobile platform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span></span>
8.  <span data-ttu-id="cc75f-168">Se a sua categoria não estiver na lista, selecione **Procurar**.</span><span class="sxs-lookup"><span data-stu-id="cc75f-168">If your category isn't in the list, select **Search**.</span></span> <span data-ttu-id="cc75f-169">Procure por categoria ou mude para a pesquisa por nome de categoria.</span><span class="sxs-lookup"><span data-stu-id="cc75f-169">Search by category, or switch to search by category name.</span></span>
9.  <span data-ttu-id="cc75f-170">Selecione uma atividade.</span><span class="sxs-lookup"><span data-stu-id="cc75f-170">Select an activity.</span></span> <span data-ttu-id="cc75f-171">Uma lista mostra as atividades que são carregadas na sua aplicação para utilização offline.</span><span class="sxs-lookup"><span data-stu-id="cc75f-171">A list shows the activities that are loaded into your app for offline use.</span></span> <span data-ttu-id="cc75f-172">Por predefinição, são carregados 50 itens, mas um programador pode alterar este número.</span><span class="sxs-lookup"><span data-stu-id="cc75f-172">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="cc75f-173">Para mais informações, consulte [Plataforma móvel](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span><span class="sxs-lookup"><span data-stu-id="cc75f-173">For more information, see [Mobile platform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span></span>
10. <span data-ttu-id="cc75f-174">Se a sua atividade não estiver na lista, selecione **Procurar**.</span><span class="sxs-lookup"><span data-stu-id="cc75f-174">If your activity isn't in the list, select **Search**.</span></span> <span data-ttu-id="cc75f-175">Procure por número de atividade ou mude para a pesquisa finalidade.</span><span class="sxs-lookup"><span data-stu-id="cc75f-175">Search by activity number, or switch to search by purpose.</span></span>

11. <span data-ttu-id="cc75f-176">Selecione a propriedade da linha.</span><span class="sxs-lookup"><span data-stu-id="cc75f-176">Select the line property.</span></span>
12. <span data-ttu-id="cc75f-177">Opcional: introduza quaisquer comentários externos e internos.</span><span class="sxs-lookup"><span data-stu-id="cc75f-177">Optional: Enter any external and internal comments.</span></span>
13. <span data-ttu-id="cc75f-178">Selecione **Concluído**.</span><span class="sxs-lookup"><span data-stu-id="cc75f-178">Select **Done**.</span></span>
