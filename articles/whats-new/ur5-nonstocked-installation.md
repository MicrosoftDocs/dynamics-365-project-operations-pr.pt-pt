---
title: Atualizar o Project Operations no seu ambiente financeiro
description: Este tópico fornece informações sobre como atualizar o Project Operations no seu ambiente Dynamics 365 Finance.
author: ruhercul
manager: tfehr
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d68296ec59f0bd58f848154c90e02c58f275ab12
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291993"
---
# <a name="update-project-operations-in-your-finance-environment"></a><span data-ttu-id="8af66-103">Atualizar o Project Operations no seu ambiente financeiro</span><span class="sxs-lookup"><span data-stu-id="8af66-103">Update Project Operations in your Finance environment</span></span>

<span data-ttu-id="8af66-104">_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_</span><span class="sxs-lookup"><span data-stu-id="8af66-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="8af66-105">Este tópico fornece informações sobre como atualizar o Dynamics 365 Project Operations no seu ambiente Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="8af66-105">This topic provides information about how to update Dynamics 365 Project Operations in your Dynamics 365 Finance environment.</span></span> <span data-ttu-id="8af66-106">Existem três procedimentos que são necessários para atualizar o Project Operations para a Atualização 5 (UR5):</span><span class="sxs-lookup"><span data-stu-id="8af66-106">There are three procedures that are required to update Project Operations to Update 5 (UR5):</span></span>

- [<span data-ttu-id="8af66-107">Importe o pacote no seu projeto de pré-visualização</span><span class="sxs-lookup"><span data-stu-id="8af66-107">Import the package into your preview project</span></span>](#import)
- [<span data-ttu-id="8af66-108">Aplicar a atualização</span><span class="sxs-lookup"><span data-stu-id="8af66-108">Apply the update</span></span>](#apply)
- [<span data-ttu-id="8af66-109">Atualizar o seu ambiente Dataverse</span><span class="sxs-lookup"><span data-stu-id="8af66-109">Update your Dataverse environment</span></span>](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a><span data-ttu-id="8af66-110">Importe o pacote para o seu projeto de LCS</span><span class="sxs-lookup"><span data-stu-id="8af66-110">Import the package into your LCS project</span></span>

1. <span data-ttu-id="8af66-111">Iniciar sessão nos [Lifecycle Services (LCS)](https://lcs.dynamics.com/) como Proprietário de Projeto ou Gestor de Ambiente.</span><span class="sxs-lookup"><span data-stu-id="8af66-111">Sign in to [Lifecycle Services (LCS)](https://lcs.dynamics.com/) as a Project Owner or Environment manager.</span></span>
2. <span data-ttu-id="8af66-112">Da lista de projetos, selecione o seu projeto LCS.</span><span class="sxs-lookup"><span data-stu-id="8af66-112">From the list of projects, select your LCS project.</span></span>
3. <span data-ttu-id="8af66-113">Na página do **Projeto**, no grupo **Ambientes**, abra o ambiente que pretende atualizar.</span><span class="sxs-lookup"><span data-stu-id="8af66-113">On the **Project** page, in the **Environments** group, open the environment that you want to update.</span></span>
4. <span data-ttu-id="8af66-114">Verifique se o ambiente está a funcionar.</span><span class="sxs-lookup"><span data-stu-id="8af66-114">Verify that the environment is running.</span></span> <span data-ttu-id="8af66-115">Se não tiver iniciado, inicie o ambiente.</span><span class="sxs-lookup"><span data-stu-id="8af66-115">If it isn't started, start the environment.</span></span>
5. <span data-ttu-id="8af66-116">Na secção **Nova versão** em **Atualizações disponíveis**, selecione **Ver atualização** para 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="8af66-116">In the **New release** section under **Available updates**, select **View update** for 10.0.15.</span></span>

![Ver botão de atualização](media/view-update.png)

6. <span data-ttu-id="8af66-118">Na página **Atualizações binárias**, selecione **Guardar pacote**.</span><span class="sxs-lookup"><span data-stu-id="8af66-118">On the **Binary updates** page, select **Save package**.</span></span>
7. <span data-ttu-id="8af66-119">Na página **Rever e guardar atualizações**, selecione **Guardar pacote**.</span><span class="sxs-lookup"><span data-stu-id="8af66-119">On the **Review and save updates** page, select **Save package**.</span></span>
8. <span data-ttu-id="8af66-120">No painel **Guardar para a biblioteca de ativos** que se abre, introduza o nome do pacote e, em seguida, selecione **Guardar o pacote**.</span><span class="sxs-lookup"><span data-stu-id="8af66-120">On the **Save package to asset library** pane that opens, enter the package name and then select **Save package**.</span></span>
9. <span data-ttu-id="8af66-121">Quando o LCS terminar de guardar o pacote, o botão **Feito** está ativado.</span><span class="sxs-lookup"><span data-stu-id="8af66-121">When LCS has finished saving the package, the **Done** button is enabled.</span></span> <span data-ttu-id="8af66-122">Selecione **Concluído**.</span><span class="sxs-lookup"><span data-stu-id="8af66-122">Select **Done**.</span></span> <span data-ttu-id="8af66-123">O LCS verificará o pacote.</span><span class="sxs-lookup"><span data-stu-id="8af66-123">LCS will verify the package.</span></span> <span data-ttu-id="8af66-124">A verificação pode demorar alguns minutos ou até uma hora.</span><span class="sxs-lookup"><span data-stu-id="8af66-124">Verification can take a few minutes or up to one hour.</span></span>


## <a name="apply-the-package-update"></a><a name="apply"></a><span data-ttu-id="8af66-125">Aplique a atualização de pacote</span><span class="sxs-lookup"><span data-stu-id="8af66-125">Apply the package update</span></span>

1. <span data-ttu-id="8af66-126">No LCS, na página de **Detalhes do ambiente**, selecione **Manter** > **Aplicar atualizações**.</span><span class="sxs-lookup"><span data-stu-id="8af66-126">In LCS, on the **Environment details** page, select **Maintain** > **Apply Updates**.</span></span>
2. <span data-ttu-id="8af66-127">Na lista, selecione o pacote que guardou anteriormente e, em seguida, selecione **Aplicar**.</span><span class="sxs-lookup"><span data-stu-id="8af66-127">From the list, select the package that you saved earlier, and then select **Apply**.</span></span>
3. <span data-ttu-id="8af66-128">Selecione **Sim** para confirmar que deseja implementar o pacote.</span><span class="sxs-lookup"><span data-stu-id="8af66-128">Select **Yes** to confirm that you want to deploy the package.</span></span>

![Confirme a caixa de diálogo de implementação do pacote](media/confirm-package-deployment.png)

4. <span data-ttu-id="8af66-130">Selecione **Sim** para confirmar que deseja atualizar a aplicação.</span><span class="sxs-lookup"><span data-stu-id="8af66-130">Select **Yes** to confirm that you want to update the application.</span></span>

![Confirme a caixa de diálogo de atualização de aplicações](media/confirm-application-update.png)

<span data-ttu-id="8af66-132">A atualização de implementação e aplicação começará.</span><span class="sxs-lookup"><span data-stu-id="8af66-132">The deployment and application update will start.</span></span> 

<span data-ttu-id="8af66-133">Na página de **Detalhes do ambiente**, no canto superior direito, o estado do ambiente atualizará para **Em manutenção**.</span><span class="sxs-lookup"><span data-stu-id="8af66-133">On the **Environment details** page, in the top-right corner, the environment status will update to **Servicing**.</span></span> <span data-ttu-id="8af66-134">Em aproximadamente duas horas, a atualização estará completa.</span><span class="sxs-lookup"><span data-stu-id="8af66-134">In approximately two hours, the update will be complete.</span></span> <span data-ttu-id="8af66-135">As informações de libertação da aplicação serão atualizadas para **Microsoft Dynamics 365 for Finance and Operations 10.0.15** e o estado do ambiente será atualizado para **Implementado**.</span><span class="sxs-lookup"><span data-stu-id="8af66-135">The application release information will update to **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** and the environment status will update to **Deployed**.</span></span>


## <a name="update-your-dataverse-environment"></a><a name="update"></a><span data-ttu-id="8af66-136">Atualizar o seu ambiente Dataverse</span><span class="sxs-lookup"><span data-stu-id="8af66-136">Update your Dataverse environment</span></span>

1. <span data-ttu-id="8af66-137">Inicie sessão no [centro de administração do Power Platform](https://admin.powerplatform.com/).</span><span class="sxs-lookup"><span data-stu-id="8af66-137">Sign in to the [Power Platform admin center](https://admin.powerplatform.com/).</span></span>
2. <span data-ttu-id="8af66-138">Na lista, encontre e abra o ambiente que usou para instalar o Project Operations.</span><span class="sxs-lookup"><span data-stu-id="8af66-138">In the list, find and open the environment that you used to install Project Operations.</span></span>
3. <span data-ttu-id="8af66-139">Na página **Ambientes**, selecione **Recurso** > **apps Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="8af66-139">On the **Environments** page, select **Resource** > **Dynamics 365 apps**.</span></span>
4. <span data-ttu-id="8af66-140">Na lista, localizar **Microsoft Dynamics 365 Project Operations**, e na coluna **Estado**, selecione **Atualização disponível**.</span><span class="sxs-lookup"><span data-stu-id="8af66-140">In the list, locate **Microsoft Dynamics 365 Project Operations**, and in the **Status** column, select **Update Available**.</span></span>
5. <span data-ttu-id="8af66-141">Selecione **Concordo com os termos da caixa de verificação de serviço** e, em seguida, selecione **Atualizar**.</span><span class="sxs-lookup"><span data-stu-id="8af66-141">Select the **I agree to the terms of service** check box, and then select **Update**.</span></span> <span data-ttu-id="8af66-142">A versão mais recente da solução será instalada.</span><span class="sxs-lookup"><span data-stu-id="8af66-142">The latest version of the solution will be installed.</span></span>

<span data-ttu-id="8af66-143">Depois de concluída a instalação, terá a versão 4.5.0.134 instalada.</span><span class="sxs-lookup"><span data-stu-id="8af66-143">After the installation is complete, you'll have version 4.5.0.134 installed.</span></span>

## <a name="configure-new-features"></a><span data-ttu-id="8af66-144">Configurar novas funcionalidades</span><span class="sxs-lookup"><span data-stu-id="8af66-144">Configure new features</span></span>

### <a name="enable-dual-write-mapping"></a><span data-ttu-id="8af66-145">Possibilita o mapeamento de escrita dupla</span><span class="sxs-lookup"><span data-stu-id="8af66-145">Enable dual-write mapping</span></span>

<span data-ttu-id="8af66-146">Depois de concluir a atualização sobre as Finanças e ambientes Dataverse, pode ativar os mapeamentos de dupla escrita necessários.</span><span class="sxs-lookup"><span data-stu-id="8af66-146">After you complete the update on the Finance and Dataverse environments, you can enable the required dual-write mappings.</span></span> <span data-ttu-id="8af66-147">Conclua os seguintes procedimentos para possibilitar os mapeamentos de escrita dupla.</span><span class="sxs-lookup"><span data-stu-id="8af66-147">Complete the following procedures to enable dual-write mappings.</span></span>

- [<span data-ttu-id="8af66-148">Atualizar definições de segurança no ambiente do Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="8af66-148">Update security settings on Customer Engagement environment</span></span>](#security)
- [<span data-ttu-id="8af66-149">Atualizar entidades de dados</span><span class="sxs-lookup"><span data-stu-id="8af66-149">Refresh data entities</span></span>](#refresh)
- [<span data-ttu-id="8af66-150">Atualizar e executar os mapeamentos de dupla escrita</span><span class="sxs-lookup"><span data-stu-id="8af66-150">Update and run the dual-write mappings</span></span>](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a><span data-ttu-id="8af66-151">Atualizar definições de segurança no ambiente do Dataverse</span><span class="sxs-lookup"><span data-stu-id="8af66-151">Update security settings on the Dataverse environment</span></span>

<span data-ttu-id="8af66-152">As seguintes atualizações aos privilégios de segurança para as entidades são necessárias como parte da atualização para UR5.</span><span class="sxs-lookup"><span data-stu-id="8af66-152">The following updates to the security privileges for entities are required as part of the update to UR5.</span></span>

1. <span data-ttu-id="8af66-153">No seu ambiente Dataverse, vá a **Definições** e no grupo **Sistema**, selecione **Segurança**.</span><span class="sxs-lookup"><span data-stu-id="8af66-153">In your Dataverse environment, go to **Settings**, and in the **System** group, select **Security**.</span></span>

![Definições do ambiente Dataverse](media/Picture21.png)

2. <span data-ttu-id="8af66-155">Selecionar **Direitos de Acesso**.</span><span class="sxs-lookup"><span data-stu-id="8af66-155">Select **Security Roles**.</span></span>
3. <span data-ttu-id="8af66-156">A partir da lista de funções, selecione **utilizador de aplicações de dupla escrita** e selecione o separador **Entidades Personalizadas**.</span><span class="sxs-lookup"><span data-stu-id="8af66-156">From the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span> 
4. <span data-ttu-id="8af66-157">Verifique se a função tem permissões de **leitura** e **acrescentar a** para:</span><span class="sxs-lookup"><span data-stu-id="8af66-157">Verify that the role has **Read** and **Append To** permissions for:</span></span>

      - <span data-ttu-id="8af66-158">**Tipo de taxa de cambio de moeda**</span><span class="sxs-lookup"><span data-stu-id="8af66-158">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="8af66-159">**Tabela de contas**</span><span class="sxs-lookup"><span data-stu-id="8af66-159">**Chart Of Accounts**</span></span> 
      - <span data-ttu-id="8af66-160">**Calendário Fiscal**</span><span class="sxs-lookup"><span data-stu-id="8af66-160">**Fiscal Calendar**</span></span> 
      - <span data-ttu-id="8af66-161">**Livro-razão**</span><span class="sxs-lookup"><span data-stu-id="8af66-161">**Ledger**</span></span>

5. <span data-ttu-id="8af66-162">Depois de o direito de acesso ser atualizado, vá a **Definições** > **Segurança** > **Equipas**.</span><span class="sxs-lookup"><span data-stu-id="8af66-162">After the security role is updated, go to **Settings** > **Security** > **Teams**.</span></span> <span data-ttu-id="8af66-163">Verifique se a função de **utilizador de aplicações de dupla escrita** foi aplicada à equipa.</span><span class="sxs-lookup"><span data-stu-id="8af66-163">Verify that the **dual-write app user** role has been applied to the team.</span></span> 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a><span data-ttu-id="8af66-164">Atualizar entidades de dados a partir da atualização</span><span class="sxs-lookup"><span data-stu-id="8af66-164">Refresh data entities from the update</span></span>

1. <span data-ttu-id="8af66-165">No seu ambiente de Finanças, abra o espaço de trabalho de **gestão de dados** e, em seguida, abra a página de **parâmetros-quadro**.</span><span class="sxs-lookup"><span data-stu-id="8af66-165">In your Finance environment, open the **Data management** workspace, and then open the **Framework parameters** page.</span></span>
2. <span data-ttu-id="8af66-166">No separador **definições de entidade**, selecione **Atualizar lista de entidades**.</span><span class="sxs-lookup"><span data-stu-id="8af66-166">On the **Entity settings** tab, select **Refresh entity list**.</span></span>
3. <span data-ttu-id="8af66-167">Selecione **Fechar** para confirmar a atualização da entidade.</span><span class="sxs-lookup"><span data-stu-id="8af66-167">Select **Close** to confirm the entity refresh.</span></span>

 > [!NOTE]
 > <span data-ttu-id="8af66-168">Este processo irá demorar cerca de 20 minutos a concluir.</span><span class="sxs-lookup"><span data-stu-id="8af66-168">This process will take approximately 20 minutes to complete.</span></span> <span data-ttu-id="8af66-169">Será notificado quando a atualização estiver completa.</span><span class="sxs-lookup"><span data-stu-id="8af66-169">You will be notified when the refresh is complete.</span></span>

### <a name="update-dual-write-mappings"></a><a name="run"></a><span data-ttu-id="8af66-170">Atualizar mapeamentos de escrita dupla</span><span class="sxs-lookup"><span data-stu-id="8af66-170">Update dual-write mappings</span></span>

1. <span data-ttu-id="8af66-171">No espaço de trabalho de **gestão de dados**, selecione **Escrita dupla**.</span><span class="sxs-lookup"><span data-stu-id="8af66-171">In the **Data management** workspace, select **Dual-write**.</span></span>
2. <span data-ttu-id="8af66-172">Selecione **Aplicar soluções**, selecione ambas as soluções na lista e, em seguida, selecione **Aplicar**.</span><span class="sxs-lookup"><span data-stu-id="8af66-172">Select **Apply solutions**, select both solutions in the list, and then select **Apply**.</span></span>
3. <span data-ttu-id="8af66-173">Na página de **escrita dupla**, selecione os seguintes mapas de tabela e, em seguida, selecione **Parar**.</span><span class="sxs-lookup"><span data-stu-id="8af66-173">On the **Dual-write** page, select the following table maps, and then select **Stop**.</span></span>

    - <span data-ttu-id="8af66-174">**Valores reais de integração com o Project Operations (msdyn_actuals)**</span><span class="sxs-lookup"><span data-stu-id="8af66-174">**Project Operations integration actuals (msdyn_actuals)**</span></span>
    - <span data-ttu-id="8af66-175">**Categorias de despesas de projeto de integração do Project Operations (msdyn_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="8af66-175">**Project Operations integration project expense categories (msdyn_expensecategories)**</span></span>
    - <span data-ttu-id="8af66-176">**Entidade de exportação de despesas de projeto de integração de valores reais do Project Operations (msdyn_expenses)**</span><span class="sxs-lookup"><span data-stu-id="8af66-176">**Project Operations integration actuals project expenses export entity (msdyn_expenses)**</span></span>

4. <span data-ttu-id="8af66-177">Na página da **versão do mapa de tabela**, aplique uma nova versão do mapa a cada uma das três entidades.</span><span class="sxs-lookup"><span data-stu-id="8af66-177">On the **Table map version** page, apply a new version of the map to each of the three entities.</span></span>
5. <span data-ttu-id="8af66-178">Na página de **escrita dupla**, selecione executar para reiniciar os mapas.</span><span class="sxs-lookup"><span data-stu-id="8af66-178">On the **Dual-write** page, select run to restart the maps.</span></span>
6. <span data-ttu-id="8af66-179">Na lista de mapas, selecione o mapa **Livro-razão (msdyn_ledgers)** com todos os pré-requisitos e selecione a caixa de verificação de **sincronização inicial**.</span><span class="sxs-lookup"><span data-stu-id="8af66-179">From the list of maps, select the **Ledger (msdyn_ledgers)** map with all prerequisites and select the **Initial sync** check box.</span></span> 
7. <span data-ttu-id="8af66-180">No campo **Master para sincronização inicial**, selecione **apps Finance and Operations** e, em seguida, selecione **Executar**.</span><span class="sxs-lookup"><span data-stu-id="8af66-180">In the **Master for initial sync** field, select **Finance and Operations apps** and then select **Run**.</span></span>
 
 ![Sincronização do mapa de livros](media/DW6.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]