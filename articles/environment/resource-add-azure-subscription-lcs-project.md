---
title: Adicionar uma subscrição do Azure a um projeto LCS
description: Este tópico fornece informações sobre como ligar a sua subscrição do Azure a um projeto LCS.
author: sigitac
manager: Annbe
ms.date: 04/12/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a80c926ba67a1620e39d8c7677a05678454e6340
ms.sourcegitcommit: 7468d668c48c1d87934aab9a034decd51e56dec6
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880552"
---
# <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="7771d-103">Adicionar uma subscrição do Azure a um projeto LCS</span><span class="sxs-lookup"><span data-stu-id="7771d-103">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="7771d-104">_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_</span><span class="sxs-lookup"><span data-stu-id="7771d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="7771d-105">Os ambientes alojados na cloud têm de ser implementados através de uma subscrição do Azure existente.</span><span class="sxs-lookup"><span data-stu-id="7771d-105">Cloud-hosted environments must be deployed using an existing Azure subscription.</span></span> <span data-ttu-id="7771d-106">Este tópico explica como ligar a sua subscrição do Azure existente a um projeto LCS.</span><span class="sxs-lookup"><span data-stu-id="7771d-106">This topic explains how to connect your existing Azure subscription to an LCS project.</span></span> 

## <a name="grant-admin-consent"></a><span data-ttu-id="7771d-107">Conceder consentimento do administrador</span><span class="sxs-lookup"><span data-stu-id="7771d-107">Grant admin consent</span></span>

1. <span data-ttu-id="7771d-108">No seu projeto LCS, na secção **Ambientes**, selecione **Definições do Microsoft Azure**.</span><span class="sxs-lookup"><span data-stu-id="7771d-108">In your LCS project, in the **Environments** section, select **Microsoft Azure settings**.</span></span>

![Definições do Microsoft Azure](./media/1MicrosoftAzureSettings.png)

2. <span data-ttu-id="7771d-110">Na página **Definições do projeto**, no separador **Conectores do Azure**, selecione **Autorizar**.</span><span class="sxs-lookup"><span data-stu-id="7771d-110">On the **Project settings** page, on the **Azure connectors** tab, select **Authorize**.</span></span> <span data-ttu-id="7771d-111">Isto permite que os ambientes sejam implementados neste projeto.</span><span class="sxs-lookup"><span data-stu-id="7771d-111">This allows environments to be deployed to this project.</span></span>

![Conectores do Azure](./media/2AzureConnectors.png)

3. <span data-ttu-id="7771d-113">Selecione **Autorizar** novamente para fornecer o consentimento do administrador.</span><span class="sxs-lookup"><span data-stu-id="7771d-113">Select **Authorize** again to provide admin consent.</span></span>

![Conceder Consentimento do Administrador](./media/3GrantAdminConsent.png)

4. <span data-ttu-id="7771d-115">Aceite o pedido de permissões.</span><span class="sxs-lookup"><span data-stu-id="7771d-115">Accept the permissions request.</span></span>

![Aceitar o Pedido de Permissão.](./media/4AcceptPermissionRequest.png)

<span data-ttu-id="7771d-117">A autorização está agora concluída.</span><span class="sxs-lookup"><span data-stu-id="7771d-117">The authorization is now complete.</span></span> 

![Autorização Com Êxito](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a><span data-ttu-id="7771d-119">Fornecer acesso dos Serviços de Implementação do Dynamics à sua subscrição do Azure</span><span class="sxs-lookup"><span data-stu-id="7771d-119">Provide Dynamics Deployment Services access to your Azure subscription</span></span>

1. <span data-ttu-id="7771d-120">Vá para to [Faturação do Microsoft Azure](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) e selecione a sua subscrição.</span><span class="sxs-lookup"><span data-stu-id="7771d-120">Go to [Microsoft Azure billing](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) and select your subscription.</span></span> <span data-ttu-id="7771d-121">Os Serviços de Implementação do Dynamics precisam de acesso a esta subscrição para conseguirem implementar ambientes.</span><span class="sxs-lookup"><span data-stu-id="7771d-121">Dynamics Deployment Services needs to access this subscription to be able to deploy environments.</span></span>

![Detalhes da Subscrição do Azure](./media/6AzureSubscription.png)

2. <span data-ttu-id="7771d-123">Selecione **Controlo de acesso (IAM)** no painel de navegação e selecione **Adicionar Atribuição de Função**.</span><span class="sxs-lookup"><span data-stu-id="7771d-123">Select **Access control (IAM)** in the navigation pane, and then select **Add role assignment**.</span></span>
3. <span data-ttu-id="7771d-124">No controlo de deslize no lado direito, selecione **Função de contribuidor** e, na lista fornecida, localize e selecione **Serviços de Implementação do Dynamics**.</span><span class="sxs-lookup"><span data-stu-id="7771d-124">In the slider on the right side, select **Contributor role**, and in the list provided, find and select **Dynamics Deployment Services**.</span></span> 
4. <span data-ttu-id="7771d-125">Selecione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="7771d-125">Select **Save**.</span></span>

![Acesso à Subscrição](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a><span data-ttu-id="7771d-127">Adicionar um conector de subscrição a um projeto LCS</span><span class="sxs-lookup"><span data-stu-id="7771d-127">Add a subscription connector to an LCS project</span></span>

1. <span data-ttu-id="7771d-128">No seu projeto LCS, na página **Definições do Microsoft Azure**, selecione **Adicionar** para adicionar um novo conector.</span><span class="sxs-lookup"><span data-stu-id="7771d-128">In your LCS project, on the **Microsoft Azure settings** page, select **Add** to add a new connector.</span></span>
2. <span data-ttu-id="7771d-129">Introduza o seu ID de subscrição do Azure.</span><span class="sxs-lookup"><span data-stu-id="7771d-129">Enter your Azure subscription ID.</span></span> <span data-ttu-id="7771d-130">Poderá localizar o seu ID de subscrição do Azure no [Portal do Azure](https://ms.portal.azure.com/), em  **Definições** na parte inferior esquerda do ecrã.</span><span class="sxs-lookup"><span data-stu-id="7771d-130">You can find your Azure subscription ID in the [Azure portal](https://ms.portal.azure.com/), under  **Settings**  in the lower left of the screen.</span></span>
3. <span data-ttu-id="7771d-131">No campo **Configurar para utilizar o Azure Resource Manager**, selecione **Sim**.</span><span class="sxs-lookup"><span data-stu-id="7771d-131">In the **Configure to use Azure Resource Manager** field, select **Yes**.</span></span>
4. <span data-ttu-id="7771d-132">Certifique-se de que o Domínio do Inquilino do AAD da Subscrição do Azure corresponde à subscrição do Azure proprietária do domínio que está utilizar e selecione **Seguinte**.</span><span class="sxs-lookup"><span data-stu-id="7771d-132">Make sure Azure's Subscription AAD Tenant Domain matches the domain-owning Azure subscription that you are using, and select **Next**.</span></span>
5. <span data-ttu-id="7771d-133">No ecrã **Configuração do Microsoft Azure**, selecione **Seguinte** para confirmar.</span><span class="sxs-lookup"><span data-stu-id="7771d-133">On the **Microsoft Azure Setup** screen, select **Next** to confirm.</span></span> <span data-ttu-id="7771d-134">Se receber um erro neste ecrã, volte à secção [Fornecer acesso aos Serviços de Implementação do Dynamics à subscrição do Azure](#provide) neste tópico e certifique-se de que concluiu todos os passos.</span><span class="sxs-lookup"><span data-stu-id="7771d-134">If you receive an error on this screen, return to the section [Provide Dynamics Deployment Services access to Azure subscription](#provide) in this topic and make sure you have completed all of the steps.</span></span>
6. <span data-ttu-id="7771d-135">Faça o download do Certificado de Gestão Azure para uma pasta local no seu computador.</span><span class="sxs-lookup"><span data-stu-id="7771d-135">Download the Azure Management Certificate to a local folder on your computer.</span></span> <span data-ttu-id="7771d-136">Peça ao seu Administrador de subscrição Azure para fazer enviar o certificado para o Portal de Gestão do Azure, selecionando a subscrição e indo para **Definições** > **Certificados de Gestão**.</span><span class="sxs-lookup"><span data-stu-id="7771d-136">Ask your Azure subscription administrator to upload the certificate to Azure Management Portal by selecting the subscription and going to **Settings** > **Management Certificates**.</span></span> <span data-ttu-id="7771d-137">Este certificado permite que o LCS comunique com a Azure em seu nome.</span><span class="sxs-lookup"><span data-stu-id="7771d-137">This certificate enables LCS to communicate with Azure on your behalf.</span></span> <span data-ttu-id="7771d-138">Pode ignorar este passo se o seu utilizador tiver acesso à subscrição.</span><span class="sxs-lookup"><span data-stu-id="7771d-138">You can skip this step if your user has access to the subscription.</span></span>
7. <span data-ttu-id="7771d-139">Selecione **Seguinte**.</span><span class="sxs-lookup"><span data-stu-id="7771d-139">Select  **Next**.</span></span>
8. <span data-ttu-id="7771d-140">Selecione a região do Azure onde fazer a implementação e selecione um centro de dados que esteja perto de onde planeia utilizar este sistema.</span><span class="sxs-lookup"><span data-stu-id="7771d-140">Select the Azure region to deploy in and select a data center that is close to where you plan to use this system.</span></span>
9.  <span data-ttu-id="7771d-141">Selecione **Ligar**.</span><span class="sxs-lookup"><span data-stu-id="7771d-141">Select  **Connect**.</span></span>

<span data-ttu-id="7771d-142">Ligou com êxito a sua subscrição do Azure.</span><span class="sxs-lookup"><span data-stu-id="7771d-142">You have successfully connected your Azure subscription.</span></span> <span data-ttu-id="7771d-143">Pode agora implementar os ambientes alojados na cloud do Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="7771d-143">You can now deploy Dynamics 365 Finance cloud-hosted environments.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
