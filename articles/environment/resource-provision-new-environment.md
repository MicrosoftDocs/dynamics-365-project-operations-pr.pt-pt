---
title: Aprovisionar um novo ambiente
description: Este tópico fornece informações sobre como aprovisionar um novo ambiente do Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a43b947207b6d4276ef27ec996713bf3883e7906
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082291"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="3d28c-103">Aprovisionar um novo ambiente</span><span class="sxs-lookup"><span data-stu-id="3d28c-103">Provision a new environment</span></span>

<span data-ttu-id="3d28c-104">_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_</span><span class="sxs-lookup"><span data-stu-id="3d28c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="3d28c-105">Este tópico fornece informações sobre como aprovisionar um novo ambiente do Dynamics 365 Project Operations para cenários baseados em recursos/não armazenados.</span><span class="sxs-lookup"><span data-stu-id="3d28c-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="3d28c-106">Ativar o aprovisionamento automatizado do Project Operations num projeto LCS</span><span class="sxs-lookup"><span data-stu-id="3d28c-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="3d28c-107">Utilize os seguintes passos para ativar o fluxo de aprovisionamento automatizado do Project Operations para o seu projeto LCS.</span><span class="sxs-lookup"><span data-stu-id="3d28c-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="3d28c-108">Vá para [LCS](https://lcs.dynamics.com/v2) e selecione o mosaico **Gestão de funcionalidades de pré-visualização**.</span><span class="sxs-lookup"><span data-stu-id="3d28c-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="3d28c-109">Na lista **Funcionalidade de pré-visualização** , selecione **Funcionalidade Project Operations** e, em seguida, selecione **Funcionalidade de pré-visualização ativada** para ativar o Project Operations.</span><span class="sxs-lookup"><span data-stu-id="3d28c-109">In the **Preview feature** list, select **Project Operations Feature** , and then select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="3d28c-110">Este passo é executado apenas uma vez por projeto LCS.</span><span class="sxs-lookup"><span data-stu-id="3d28c-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="3d28c-111">Aprovisionar um ambiente do Project Operations</span><span class="sxs-lookup"><span data-stu-id="3d28c-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="3d28c-112">Abra um novo [ambiente de demonstração](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) do Dynamics 365 Finance ou implementação do [ambiente de sandbox/ produção](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure).</span><span class="sxs-lookup"><span data-stu-id="3d28c-112">Open a new Dynamics 365 Finance [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="3d28c-113">Percorra o assistente de **Aprovisionamento do ambiente**.</span><span class="sxs-lookup"><span data-stu-id="3d28c-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="3d28c-114">Certifique-se de que a versão de aplicação selecionada é a 10.0.13 ou superior.</span><span class="sxs-lookup"><span data-stu-id="3d28c-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="3d28c-115">Para aprovisionar o Project Operations, em **Definições avançadas** , selecione **Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="3d28c-115">To provision Project Operations, under **Advance settings** , select **Common Data Service**.</span></span> 
4. <span data-ttu-id="3d28c-116">Ative a **Definição do Common Data Service** ao selecionar **Sim** e, em seguida, introduza as informações nos campos obrigatórios:</span><span class="sxs-lookup"><span data-stu-id="3d28c-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="3d28c-117">Nome</span><span class="sxs-lookup"><span data-stu-id="3d28c-117">Name</span></span>
  - <span data-ttu-id="3d28c-118">Região</span><span class="sxs-lookup"><span data-stu-id="3d28c-118">Region</span></span>
  - <span data-ttu-id="3d28c-119">Linguagem</span><span class="sxs-lookup"><span data-stu-id="3d28c-119">Language</span></span>
  - <span data-ttu-id="3d28c-120">Moeda</span><span class="sxs-lookup"><span data-stu-id="3d28c-120">Currency</span></span>
 
5. <span data-ttu-id="3d28c-121">No campo **Modelo do Common Data Service** , selecione **Project Operations**</span><span class="sxs-lookup"><span data-stu-id="3d28c-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="3d28c-122">Selecione o tipo de ambiente para a sua implementação.</span><span class="sxs-lookup"><span data-stu-id="3d28c-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="3d28c-123">Uma avaliação baseada em subscrições permitir-lhe-á implementar um ambiente do CDS durante 30 dias.</span><span class="sxs-lookup"><span data-stu-id="3d28c-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Definições de Implementação](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="3d28c-125">Selecione **Aceitar** para confirmar os temos de serviço e, em seguida, selecione **Concluído** para regressar às definições de implementação.</span><span class="sxs-lookup"><span data-stu-id="3d28c-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Consentimento de Implementação](./media/2DeploymentConsent.png)

7. <span data-ttu-id="3d28c-127">Preencha os campos obrigatórios restantes no assistente e confirme a implementação.</span><span class="sxs-lookup"><span data-stu-id="3d28c-127">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="3d28c-128">O tempo de aprovisionamento do ambiente varia com base no tipo de ambiente.</span><span class="sxs-lookup"><span data-stu-id="3d28c-128">Environment provisioning time varies based on the environment type.</span></span> <span data-ttu-id="3d28c-129">O aprovisionamento pode demorar até seis horas.</span><span class="sxs-lookup"><span data-stu-id="3d28c-129">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="3d28c-130">Depois de a implementação ser concluída com êxito, o ambiente será mostrado como **Implementado**.</span><span class="sxs-lookup"><span data-stu-id="3d28c-130">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

8. <span data-ttu-id="3d28c-131">Para confirmar que o ambiente foi implementado com êxito, selecione **Iniciar sessão** e inicie sessão no ambiente para confirmar.</span><span class="sxs-lookup"><span data-stu-id="3d28c-131">To confirm the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![Detalhes do ambiente ](./media/3EnvironmentDetails.png)

## <a name="apply-project-operations-finance-demo-data-optional-step"></a><span data-ttu-id="3d28c-133">Aplicar dados de demonstração do Project Operations Finance (passo opcional)</span><span class="sxs-lookup"><span data-stu-id="3d28c-133">Apply Project Operations Finance demo data (optional step)</span></span>

<span data-ttu-id="3d28c-134">Aplique os dados de demonstração do Project Operations Finance à versão de serviço 10.0.13 do Cloud Hosted Environment, tal como descrito [neste artigo](resource-apply-finance-demo-data.md).</span><span class="sxs-lookup"><span data-stu-id="3d28c-134">Apply Project Operations Finance demo data to 10.0.13 service release Cloud Hosted Environment as described in [this article](resource-apply-finance-demo-data.md).</span></span>

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="3d28c-135">Aplicar atualizações ao ambiente do Finance</span><span class="sxs-lookup"><span data-stu-id="3d28c-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="3d28c-136">O Project Operations requer um ambiente do Finance com versão de aplicação **10.0.13 (10.0.569.20009)** ou superior.</span><span class="sxs-lookup"><span data-stu-id="3d28c-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="3d28c-137">Poderá precisar de aplicar atualizações de qualidade ao seu ambiente do Finance para receber esta versão.</span><span class="sxs-lookup"><span data-stu-id="3d28c-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="3d28c-138">No LCS, na página **Detalhes do ambiente** , na secção **Atualizações Disponíveis** , selecione **Ver Atualização**.</span><span class="sxs-lookup"><span data-stu-id="3d28c-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Ver Atualizações](./media/5ViewUpdates.png)

2. <span data-ttu-id="3d28c-140">Na página **Atualizações binárias** , selecione **Guardar pacote**.</span><span class="sxs-lookup"><span data-stu-id="3d28c-140">On the **Binary updates** page, select **Save package.**</span></span>

![Guardar pacote](./media/6SavePackage.png)

3. <span data-ttu-id="3d28c-142">Clique em **Selecionar tudo** e, em seguida, selecione **Guardar pacote**.</span><span class="sxs-lookup"><span data-stu-id="3d28c-142">Click **Select all** and then select **Save package**.</span></span>

![Rever e guardar atualizações](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="3d28c-144">Introduza um nome e uma descrição do pacote e, em seguida, selecione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="3d28c-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="3d28c-145">Consoante a ligação à Internet, este processo poderá demorar algum tempo.</span><span class="sxs-lookup"><span data-stu-id="3d28c-145">Depending on the internet connection, this process might take some time.</span></span>

![Carregar pacote para a Biblioteca de Recursos](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="3d28c-147">Depois de guardar o pacote, selecione **Concluído** e guarde este pacote na Biblioteca de Recursos no seu projeto LCS.</span><span class="sxs-lookup"><span data-stu-id="3d28c-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="3d28c-148">Guardar e validar o pacote pode demorar ~15 minutos.</span><span class="sxs-lookup"><span data-stu-id="3d28c-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="3d28c-149">Para aplicar a atualização, navegue para a página **Detalhes do ambiente** no LCS e selecione **Manter** > **Aplicar atualizações**.</span><span class="sxs-lookup"><span data-stu-id="3d28c-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Manter Ambientes](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="3d28c-151">Na lista de atualizações, selecione o pacote que criou e selecione **Aplicar**.</span><span class="sxs-lookup"><span data-stu-id="3d28c-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Aplicar Atualizações](./media/10ApplyUpdates.png)

<span data-ttu-id="3d28c-153">A manutenção do ambiente vai demorar algum tempo.</span><span class="sxs-lookup"><span data-stu-id="3d28c-153">Environment servicing will take some time.</span></span> <span data-ttu-id="3d28c-154">Depois de concluída, o ambiente voltará ao estado implementado.</span><span class="sxs-lookup"><span data-stu-id="3d28c-154">After it is complete, the environment will return to a deployed state.</span></span>

![Ambiente Implementado](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="3d28c-156">Estabelecer uma ligação de Escrita Dupla</span><span class="sxs-lookup"><span data-stu-id="3d28c-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="3d28c-157">No seu projeto LCS, vá para a página **Detalhes do ambiente**.</span><span class="sxs-lookup"><span data-stu-id="3d28c-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="3d28c-158">Em **Informações do ambiente do Common Data Service** , selecione **Ligação ao CDS for Apps**.</span><span class="sxs-lookup"><span data-stu-id="3d28c-158">Under **Common Data Service Environment Information** , select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="3d28c-159">Depois de concluída a ligação, selecione novamente **Ligação ao CDS for Apps**.</span><span class="sxs-lookup"><span data-stu-id="3d28c-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="3d28c-160">Será redirecionado para a Escrita Dupla no Finance.</span><span class="sxs-lookup"><span data-stu-id="3d28c-160">You will be redirected to Dual Write in Finance.</span></span>

![Associar ao CDS](./media/12LinktoCDS.png)

4. <span data-ttu-id="3d28c-162">Selecione **Aplicar Solução** para aceder às entidades que serão mapeadas na integração.</span><span class="sxs-lookup"><span data-stu-id="3d28c-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Aplicar Soluções](./media/13ApplySolutions.png)

5. <span data-ttu-id="3d28c-164">Selecione as duas soluções, **Mapa de Entidades de Escrita Dupla do Dynamics 365 Finance and Operations** e **Mapas de Entidades de Escrita Dupla do Dynamics 365 Project Operations** , e selecione **Aplicar**.</span><span class="sxs-lookup"><span data-stu-id="3d28c-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps** , and then select **Apply**.</span></span>

![Confirmar Soluções](./media/14ConfirmSolutions.png)

<span data-ttu-id="3d28c-166">Depois de aplicadas as soluções, as entidades de Escrita Dupla são aplicadas ao ambiente.</span><span class="sxs-lookup"><span data-stu-id="3d28c-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Aplicar Soluções](./media/15ApplyingSolutions.png)

<span data-ttu-id="3d28c-168">Depois de aplicadas as entidades, todos os mapeamentos disponíveis são listados no ambiente.</span><span class="sxs-lookup"><span data-stu-id="3d28c-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Mapas de Escrita Dupla](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="3d28c-170">Atualizar as entidades de dados após a atualização</span><span class="sxs-lookup"><span data-stu-id="3d28c-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="3d28c-171">No Finance, vá para a área de trabalho **Gestão de dados**.</span><span class="sxs-lookup"><span data-stu-id="3d28c-171">In Finance, go to the **Data management** workspace.</span></span>

![Área de trabalho de gestão de dados](./media/16DataManagement.png)

2. <span data-ttu-id="3d28c-173">Selecione o mosaico **Parâmetros do marco**.</span><span class="sxs-lookup"><span data-stu-id="3d28c-173">Select the **Framework parameters** tile.</span></span>

![Parâmetros do Quadro](./media/17FrameworkParameters.png)

3. <span data-ttu-id="3d28c-175">Na página **Definições da entidade** , selecione **Atualizar lista de entidades**.</span><span class="sxs-lookup"><span data-stu-id="3d28c-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Atualizar lista de entidades](./media/18RefreshEntityList.png)

<span data-ttu-id="3d28c-177">A atualização vai demorar aproximadamente 20 minutos.</span><span class="sxs-lookup"><span data-stu-id="3d28c-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="3d28c-178">Receberá um alerta quando estiver concluída.</span><span class="sxs-lookup"><span data-stu-id="3d28c-178">You will receive an alert when it is complete.</span></span>

![Atualizar Confirmar](./media/19RefreshConfirmation.png)

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="3d28c-180">Executar mapas de Escrita Dupla do Project Operations</span><span class="sxs-lookup"><span data-stu-id="3d28c-180">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="3d28c-181">No seu projeto LCS, vá para a página **Detalhes do ambiente**.</span><span class="sxs-lookup"><span data-stu-id="3d28c-181">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="3d28c-182">Em **Informações do ambiente do Common Data Service** , selecione **Ligação ao CDS for Apps**.</span><span class="sxs-lookup"><span data-stu-id="3d28c-182">Under **Common Data Service Environment Information** , select **Link to CDS for Apps.**</span></span> <span data-ttu-id="3d28c-183">Depois de selecionar a ligação, será redirecionado para a lista de entidades nos mapeamentos.</span><span class="sxs-lookup"><span data-stu-id="3d28c-183">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="3d28c-184">Inicie os mapas,, conforme descrito na tabela seguinte.</span><span class="sxs-lookup"><span data-stu-id="3d28c-184">Start the maps as described in the following table.</span></span> <span data-ttu-id="3d28c-185">Certifique-se de segue a sequência conforme listado.</span><span class="sxs-lookup"><span data-stu-id="3d28c-185">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="3d28c-186">**Mapa da Entidade**</span><span class="sxs-lookup"><span data-stu-id="3d28c-186">**Entity Map**</span></span> | <span data-ttu-id="3d28c-187">**Atualizar entidade**</span><span class="sxs-lookup"><span data-stu-id="3d28c-187">**Refresh entity**</span></span> | <span data-ttu-id="3d28c-188">**Sincronização inicial**</span><span class="sxs-lookup"><span data-stu-id="3d28c-188">**Initial sync**</span></span> | <span data-ttu-id="3d28c-189">**Mestre para sincronização inicial**</span><span class="sxs-lookup"><span data-stu-id="3d28c-189">**Master for initial sync**</span></span> | <span data-ttu-id="3d28c-190">**Executar pré-requisitos**</span><span class="sxs-lookup"><span data-stu-id="3d28c-190">**Run prerequisites**</span></span> | <span data-ttu-id="3d28c-191">**Sincronização inicial dos pré-requisitos**</span><span class="sxs-lookup"><span data-stu-id="3d28c-191">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="3d28c-192">**Funções de Recursos de Projeto para Todas as Empresas (bookableresourcecategories)**</span><span class="sxs-lookup"><span data-stu-id="3d28c-192">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="3d28c-193">No</span><span class="sxs-lookup"><span data-stu-id="3d28c-193">No</span></span> | <span data-ttu-id="3d28c-194">Sim</span><span class="sxs-lookup"><span data-stu-id="3d28c-194">Yes</span></span> | <span data-ttu-id="3d28c-195">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="3d28c-195">Common Data Service</span></span> | <span data-ttu-id="3d28c-196">No</span><span class="sxs-lookup"><span data-stu-id="3d28c-196">No</span></span> | <span data-ttu-id="3d28c-197">N/A</span><span class="sxs-lookup"><span data-stu-id="3d28c-197">N\A</span></span> |
| <span data-ttu-id="3d28c-198">**Entidades legais (cdm\_empresas)**</span><span class="sxs-lookup"><span data-stu-id="3d28c-198">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="3d28c-199">No</span><span class="sxs-lookup"><span data-stu-id="3d28c-199">No</span></span> | <span data-ttu-id="3d28c-200">Sim</span><span class="sxs-lookup"><span data-stu-id="3d28c-200">Yes</span></span> | <span data-ttu-id="3d28c-201">Aplicações do Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="3d28c-201">Finance and Operations apps</span></span> | <span data-ttu-id="3d28c-202">No</span><span class="sxs-lookup"><span data-stu-id="3d28c-202">No</span></span> | <span data-ttu-id="3d28c-203">N/A</span><span class="sxs-lookup"><span data-stu-id="3d28c-203">N\A</span></span> |
| <span data-ttu-id="3d28c-204">**Valores reais de integração com o Project Operations (msdyn\_valores reais)**</span><span class="sxs-lookup"><span data-stu-id="3d28c-204">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="3d28c-205">No</span><span class="sxs-lookup"><span data-stu-id="3d28c-205">No</span></span> | <span data-ttu-id="3d28c-206">No</span><span class="sxs-lookup"><span data-stu-id="3d28c-206">No</span></span> | <span data-ttu-id="3d28c-207">N/A</span><span class="sxs-lookup"><span data-stu-id="3d28c-207">N\A</span></span> | <span data-ttu-id="3d28c-208">Sim</span><span class="sxs-lookup"><span data-stu-id="3d28c-208">Yes</span></span> | <span data-ttu-id="3d28c-209">No</span><span class="sxs-lookup"><span data-stu-id="3d28c-209">No</span></span> |
| <span data-ttu-id="3d28c-210">**Itens de contrato do projeto (salesorderdetails)**</span><span class="sxs-lookup"><span data-stu-id="3d28c-210">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="3d28c-211">No</span><span class="sxs-lookup"><span data-stu-id="3d28c-211">No</span></span> | <span data-ttu-id="3d28c-212">No</span><span class="sxs-lookup"><span data-stu-id="3d28c-212">No</span></span> | <span data-ttu-id="3d28c-213">N/A</span><span class="sxs-lookup"><span data-stu-id="3d28c-213">N\A</span></span> | <span data-ttu-id="3d28c-214">No</span><span class="sxs-lookup"><span data-stu-id="3d28c-214">No</span></span> | <span data-ttu-id="3d28c-215">No</span><span class="sxs-lookup"><span data-stu-id="3d28c-215">No</span></span> |
| <span data-ttu-id="3d28c-216">**Entidade de integração para as relações de transações do projeto (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="3d28c-216">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="3d28c-217">No</span><span class="sxs-lookup"><span data-stu-id="3d28c-217">No</span></span> | <span data-ttu-id="3d28c-218">No</span><span class="sxs-lookup"><span data-stu-id="3d28c-218">No</span></span> | <span data-ttu-id="3d28c-219">N/A</span><span class="sxs-lookup"><span data-stu-id="3d28c-219">N\A</span></span> | <span data-ttu-id="3d28c-220">No</span><span class="sxs-lookup"><span data-stu-id="3d28c-220">No</span></span> | <span data-ttu-id="3d28c-221">N/A</span><span class="sxs-lookup"><span data-stu-id="3d28c-221">N\A</span></span> |
| <span data-ttu-id="3d28c-222">**Marcos do item de contrato de integração com o Project Operations (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="3d28c-222">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="3d28c-223">No</span><span class="sxs-lookup"><span data-stu-id="3d28c-223">No</span></span> | <span data-ttu-id="3d28c-224">No</span><span class="sxs-lookup"><span data-stu-id="3d28c-224">No</span></span> | <span data-ttu-id="3d28c-225">N/A</span><span class="sxs-lookup"><span data-stu-id="3d28c-225">N\A</span></span> | <span data-ttu-id="3d28c-226">No</span><span class="sxs-lookup"><span data-stu-id="3d28c-226">No</span></span> | <span data-ttu-id="3d28c-227">N/A</span><span class="sxs-lookup"><span data-stu-id="3d28c-227">N\A</span></span> |
| <span data-ttu-id="3d28c-228">**Entidade de integração com o Project Operations para estimativas de despesa (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="3d28c-228">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="3d28c-229">No</span><span class="sxs-lookup"><span data-stu-id="3d28c-229">No</span></span> | <span data-ttu-id="3d28c-230">No</span><span class="sxs-lookup"><span data-stu-id="3d28c-230">No</span></span> | <span data-ttu-id="3d28c-231">N/A</span><span class="sxs-lookup"><span data-stu-id="3d28c-231">N\A</span></span> | <span data-ttu-id="3d28c-232">No</span><span class="sxs-lookup"><span data-stu-id="3d28c-232">No</span></span> | <span data-ttu-id="3d28c-233">N/A</span><span class="sxs-lookup"><span data-stu-id="3d28c-233">N\A</span></span> |
| <span data-ttu-id="3d28c-234">**Entidade de exportação de categorias de despesas do projeto de integração com o Project Operations (msdyn\_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="3d28c-234">**Project Operations integration project expense categories export entity (msdyn\_expensecategories)**</span></span> | <span data-ttu-id="3d28c-235">No</span><span class="sxs-lookup"><span data-stu-id="3d28c-235">No</span></span> | <span data-ttu-id="3d28c-236">No</span><span class="sxs-lookup"><span data-stu-id="3d28c-236">No</span></span> | <span data-ttu-id="3d28c-237">N/A</span><span class="sxs-lookup"><span data-stu-id="3d28c-237">N\A</span></span> | <span data-ttu-id="3d28c-238">No</span><span class="sxs-lookup"><span data-stu-id="3d28c-238">No</span></span> | <span data-ttu-id="3d28c-239">N/A</span><span class="sxs-lookup"><span data-stu-id="3d28c-239">N\A</span></span> |
| <span data-ttu-id="3d28c-240">**Entidade de exportação de despesas do projeto de integração com o Project Operations (msdyn\_despesas)**</span><span class="sxs-lookup"><span data-stu-id="3d28c-240">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="3d28c-241">Sim</span><span class="sxs-lookup"><span data-stu-id="3d28c-241">Yes</span></span> | <span data-ttu-id="3d28c-242">No</span><span class="sxs-lookup"><span data-stu-id="3d28c-242">No</span></span> | <span data-ttu-id="3d28c-243">N/A</span><span class="sxs-lookup"><span data-stu-id="3d28c-243">N\A</span></span> | <span data-ttu-id="3d28c-244">No</span><span class="sxs-lookup"><span data-stu-id="3d28c-244">No</span></span> | <span data-ttu-id="3d28c-245">N/A</span><span class="sxs-lookup"><span data-stu-id="3d28c-245">N\A</span></span> |
| <span data-ttu-id="3d28c-246">**Entidade de integração com o Project Operations para estimativas de horas (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="3d28c-246">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="3d28c-247">Sim</span><span class="sxs-lookup"><span data-stu-id="3d28c-247">Yes</span></span> | <span data-ttu-id="3d28c-248">No</span><span class="sxs-lookup"><span data-stu-id="3d28c-248">No</span></span> | <span data-ttu-id="3d28c-249">N/A</span><span class="sxs-lookup"><span data-stu-id="3d28c-249">N\A</span></span> | <span data-ttu-id="3d28c-250">No</span><span class="sxs-lookup"><span data-stu-id="3d28c-250">No</span></span> | <span data-ttu-id="3d28c-251">N/A</span><span class="sxs-lookup"><span data-stu-id="3d28c-251">N\A</span></span> |


4. <span data-ttu-id="3d28c-252">Para atualizar a entidade, selecione o nome do mapa e, em seguida, selecione **Atualizar entidades**.</span><span class="sxs-lookup"><span data-stu-id="3d28c-252">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 


![Atualizar Mapa](./media/20RefreshMapping.png)

5. <span data-ttu-id="3d28c-254">Após a conclusão da atualização, execute o mapa.</span><span class="sxs-lookup"><span data-stu-id="3d28c-254">After the refresh is complete, run the map.</span></span> <span data-ttu-id="3d28c-255">Antes de ativar o mapa seguinte, verifique se o mapa da tabela está no estado **Em execução**.</span><span class="sxs-lookup"><span data-stu-id="3d28c-255">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="3d28c-256">A execução de mapas com um maior número de pré-requisitos poderá demorar algum tempo.</span><span class="sxs-lookup"><span data-stu-id="3d28c-256">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="3d28c-257">Para executar um mapa com pré-requisitos, ative o seletor **Mostrar mapas de entidade relacionados**.</span><span class="sxs-lookup"><span data-stu-id="3d28c-257">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="3d28c-258">Se a tabela indicar que **Sincronização inicial dos pré-requisitos** é **Não** , verifique se o sinalizador **Sincronização inicial** está **Desativada** em todos os mapas de pré-requisitos antes de executá-lo.</span><span class="sxs-lookup"><span data-stu-id="3d28c-258">If the table indicates **Prerequisite initial sync** is **No** , verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Executar Mapa](./media/21RunMap.png)

6. <span data-ttu-id="3d28c-260">Valide que todos os mapas relacionados com o projeto estão no estado de execução.</span><span class="sxs-lookup"><span data-stu-id="3d28c-260">Validate all project related maps are in the running state.</span></span>

![Todos os mapas em execução](./media/22AllMapsRunning.png)

<span data-ttu-id="3d28c-262">O seu ambiente do Project Operations está agora aprovisionado e configurado.</span><span class="sxs-lookup"><span data-stu-id="3d28c-262">Your Project Operations environment is now provisioned and configured.</span></span>
