---
title: Adicionar uma subscrição do Azure a um projeto LCS
description: Este tópico fornece informações sobre como ligar a sua subscrição do Azure a um projeto LCS.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ad1ddd69cbb8db7780b8277a7ed7533d3ea3d053
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289923"
---
# <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="a20d8-103">Adicionar uma subscrição do Azure a um projeto LCS</span><span class="sxs-lookup"><span data-stu-id="a20d8-103">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="a20d8-104">_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_</span><span class="sxs-lookup"><span data-stu-id="a20d8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="a20d8-105">Os ambientes alojados na cloud têm de ser implementados através de uma subscrição do Azure existente.</span><span class="sxs-lookup"><span data-stu-id="a20d8-105">Cloud-hosted environments must be deployed using an existing Azure subscription.</span></span> <span data-ttu-id="a20d8-106">Este tópico explica como ligar a sua subscrição do Azure existente a um projeto LCS.</span><span class="sxs-lookup"><span data-stu-id="a20d8-106">This topic explains how to connect your existing Azure subscription to an LCS project.</span></span> 

## <a name="grant-admin-consent"></a><span data-ttu-id="a20d8-107">Conceder consentimento do administrador</span><span class="sxs-lookup"><span data-stu-id="a20d8-107">Grant admin consent</span></span>

1. <span data-ttu-id="a20d8-108">No seu projeto LCS, na secção **Ambientes**, selecione **Definições do Microsoft Azure**.</span><span class="sxs-lookup"><span data-stu-id="a20d8-108">In your LCS project, in the **Environments** section, select **Microsoft Azure settings**.</span></span>

![Definições do Microsoft Azure](./media/1MicrosoftAzureSettings.png)

2. <span data-ttu-id="a20d8-110">Na página **Definições do projeto**, no separador **Conectores do Azure**, selecione **Autorizar**.</span><span class="sxs-lookup"><span data-stu-id="a20d8-110">On the **Project settings** page, on the **Azure connectors** tab, select **Authorize**.</span></span> <span data-ttu-id="a20d8-111">Isto permite que os ambientes sejam implementados neste projeto.</span><span class="sxs-lookup"><span data-stu-id="a20d8-111">This allows environments to be deployed to this project.</span></span>

![Conectores do Azure](./media/2AzureConnectors.png)

3. <span data-ttu-id="a20d8-113">Selecione **Autorizar** novamente para fornecer o consentimento do administrador.</span><span class="sxs-lookup"><span data-stu-id="a20d8-113">Select **Authorize** again to provide admin consent.</span></span>

![Conceder Consentimento do Administrador](./media/3GrantAdminConsent.png)

4. <span data-ttu-id="a20d8-115">Aceite o pedido de permissões.</span><span class="sxs-lookup"><span data-stu-id="a20d8-115">Accept the permissions request.</span></span>

![Aceitar o Pedido de Permissão.](./media/4AcceptPermissionRequest.png)

<span data-ttu-id="a20d8-117">A autorização está agora concluída.</span><span class="sxs-lookup"><span data-stu-id="a20d8-117">The authorization is now complete.</span></span> 

![Autorização Com Êxito](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a><span data-ttu-id="a20d8-119">Fornecer acesso dos Serviços de Implementação do Dynamics à sua subscrição do Azure</span><span class="sxs-lookup"><span data-stu-id="a20d8-119">Provide Dynamics Deployment Services access to your Azure subscription</span></span>

1. <span data-ttu-id="a20d8-120">Vá para to [Faturação do Microsoft Azure](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) e selecione a sua subscrição.</span><span class="sxs-lookup"><span data-stu-id="a20d8-120">Go to [Microsoft Azure billing](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) and select your subscription.</span></span> <span data-ttu-id="a20d8-121">Os Serviços de Implementação do Dynamics precisam de acesso a esta subscrição para conseguirem implementar ambientes.</span><span class="sxs-lookup"><span data-stu-id="a20d8-121">Dynamics Deployment Services needs to access this subscription to be able to deploy environments.</span></span>

![Detalhes da Subscrição do Azure](./media/6AzureSubscription.png)

2. <span data-ttu-id="a20d8-123">Selecione **Controlo de acesso (IAM)** no painel de navegação e selecione **Adicionar Atribuição de Função**.</span><span class="sxs-lookup"><span data-stu-id="a20d8-123">Select **Access control (IAM)** in the navigation pane, and then select **Add role assignment**.</span></span>
3. <span data-ttu-id="a20d8-124">No controlo de deslize no lado direito, selecione **Função de contribuidor** e, na lista fornecida, localize e selecione **Serviços de Implementação do Dynamics**.</span><span class="sxs-lookup"><span data-stu-id="a20d8-124">In the slider on the right side, select **Contributor role**, and in the list provided, find and select **Dynamics Deployment Services**.</span></span> 
4. <span data-ttu-id="a20d8-125">Selecione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="a20d8-125">Select **Save**.</span></span>

![Acesso à Subscrição](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a><span data-ttu-id="a20d8-127">Adicionar um conector de subscrição a um projeto LCS</span><span class="sxs-lookup"><span data-stu-id="a20d8-127">Add a subscription connector to an LCS project</span></span>

1. <span data-ttu-id="a20d8-128">No seu projeto LCS, na página **Definições do Microsoft Azure**, selecione **Adicionar** para adicionar um novo conector.</span><span class="sxs-lookup"><span data-stu-id="a20d8-128">In your LCS project, on the **Microsoft Azure settings** page, select **Add** to add a new connector.</span></span>
2. <span data-ttu-id="a20d8-129">Introduza o seu ID de subscrição do Azure.</span><span class="sxs-lookup"><span data-stu-id="a20d8-129">Enter your Azure subscription ID.</span></span> <span data-ttu-id="a20d8-130">Poderá localizar o seu ID de subscrição do Azure no [Portal do Azure](https://ms.portal.azure.com/), em  **Definições** na parte inferior esquerda do ecrã.</span><span class="sxs-lookup"><span data-stu-id="a20d8-130">You can find your Azure subscription ID in the [Azure portal](https://ms.portal.azure.com/), under  **Settings**  in the lower left of the screen.</span></span>
3. <span data-ttu-id="a20d8-131">No campo **Configurar para utilizar o Azure Resource Manager**, selecione **Sim**.</span><span class="sxs-lookup"><span data-stu-id="a20d8-131">In the **Configure to use Azure Resource Manager** field, select **Yes**.</span></span>
4. <span data-ttu-id="a20d8-132">Certifique-se de que o Domínio do Inquilino do AAD da Subscrição do Azure corresponde à subscrição do Azure proprietária do domínio que está utilizar e selecione **Seguinte**.</span><span class="sxs-lookup"><span data-stu-id="a20d8-132">Make sure Azure's Subscription AAD Tenant Domain matches the domain-owning Azure subscription that you are using, and select **Next**.</span></span>
5. <span data-ttu-id="a20d8-133">No ecrã **Configuração do Microsoft Azure**, selecione **Seguinte** para confirmar.</span><span class="sxs-lookup"><span data-stu-id="a20d8-133">On the **Microsoft Azure Setup** screen, select **Next** to confirm.</span></span> <span data-ttu-id="a20d8-134">Se receber um erro neste ecrã, volte à secção [Fornecer acesso aos Serviços de Implementação do Dynamics à subscrição do Azure](#provide) neste tópico e certifique-se de que concluiu todos os passos.</span><span class="sxs-lookup"><span data-stu-id="a20d8-134">If you receive an error on this screen, return to the section [Provide Dynamics Deployment Services access to Azure subscription](#provide) in this topic and make sure you have completed all of the steps.</span></span>
6. <span data-ttu-id="a20d8-135">Transfira o Certificado de Gestão do Azure para uma pasta local no seu computador e, em seguida, carregue-a para o Portal de Gestão do Azure em **Definições** > **Certificados de Gestão**.</span><span class="sxs-lookup"><span data-stu-id="a20d8-135">Download the Azure Management Certificate to a local folder on your computer, and then upload it to Azure Management Portal by going to **Settings** > **Management Certificates**.</span></span> <span data-ttu-id="a20d8-136">Este certificado permitirá que o LCS comunique com a Azure em seu nome.</span><span class="sxs-lookup"><span data-stu-id="a20d8-136">This certificate will enable LCS to communicate with Azure on your behalf.</span></span> <span data-ttu-id="a20d8-137">Pode ignorar este passo se o seu utilizador tiver acesso à subscrição.</span><span class="sxs-lookup"><span data-stu-id="a20d8-137">You can skip this step if your user has access to the subscription.</span></span>
7. <span data-ttu-id="a20d8-138">Selecione **Seguinte**.</span><span class="sxs-lookup"><span data-stu-id="a20d8-138">Select  **Next**.</span></span>
8. <span data-ttu-id="a20d8-139">Selecione a região do Azure onde fazer a implementação e selecione um centro de dados que esteja perto de onde planeia utilizar este sistema.</span><span class="sxs-lookup"><span data-stu-id="a20d8-139">Select the Azure region to deploy in and select a data center that is close to where you plan to use this system.</span></span>
9.  <span data-ttu-id="a20d8-140">Selecione **Ligar**.</span><span class="sxs-lookup"><span data-stu-id="a20d8-140">Select  **Connect**.</span></span>

<span data-ttu-id="a20d8-141">Ligou com êxito a sua subscrição do Azure.</span><span class="sxs-lookup"><span data-stu-id="a20d8-141">You have successfully connected your Azure subscription.</span></span> <span data-ttu-id="a20d8-142">Pode agora implementar os ambientes alojados na cloud do Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="a20d8-142">You can now deploy Dynamics 365 Finance cloud-hosted environments.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]