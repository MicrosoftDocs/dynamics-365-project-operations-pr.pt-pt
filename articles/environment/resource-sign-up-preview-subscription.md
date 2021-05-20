---
title: Inscreva-se nas subscrições de pré-visualização do Project Operations para os cenários de recursos/não armazenados
description: Este tópico fornece informações sobre como subscrever e implementar o Project Operations para cenários baseados em recursos/não armazenados.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 917ead8ff6d9d3ef8374f8ccde608b6cebd50c8c
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948478"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a><span data-ttu-id="ace8a-103">Inscreva-se nas subscrições de pré-visualização do Project Operations para os cenários de recursos/não armazenados</span><span class="sxs-lookup"><span data-stu-id="ace8a-103">Sign up for Project Operations preview subscriptions for resource/ non-stocked scenarios</span></span>

<span data-ttu-id="ace8a-104">_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_</span><span class="sxs-lookup"><span data-stu-id="ace8a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="ace8a-105">Este tópico explica como subscrever a oferta pré-visualizar/parceiro e implementar o ambiente do Project Operations para os cenários baseados em recursos/não armazenados.</span><span class="sxs-lookup"><span data-stu-id="ace8a-105">This topic explains how to subscribe to the preview/partner offer and deploy Project Operations environment for resource/ non-stocked based scenarios.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ace8a-106">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="ace8a-106">Prerequisites</span></span>

- <span data-ttu-id="ace8a-107">Receberá um e-mail a convidá-lo para participar na pré-visualização.</span><span class="sxs-lookup"><span data-stu-id="ace8a-107">You will receive an email inviting you to participate in the preview.</span></span> <span data-ttu-id="ace8a-108">Pode solicitar uma pré-visualização no [Web site do Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span><span class="sxs-lookup"><span data-stu-id="ace8a-108">You can request a preview on the [Project Operations website](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span></span>
- <span data-ttu-id="ace8a-109">O utilizador que implementar a pré-visualização tem de ter direitos de administrator global do inquilino do Azure.</span><span class="sxs-lookup"><span data-stu-id="ace8a-109">The user who deploys the preview must have Azure tenant global administrator rights.</span></span>
- <span data-ttu-id="ace8a-110">A implementação de um ambiente do Finance requer uma subscrição válida do Azure que será faturada por ambiente.</span><span class="sxs-lookup"><span data-stu-id="ace8a-110">Deploying a Finance environment requires a valid Azure subscription that will be billed per environment.</span></span> <span data-ttu-id="ace8a-111">Poderá utilizar subscrição existente das suas organizações ou utilizar uma [Avaliação do Azure](https://azure.microsoft.com/en-us/free/) para começar.</span><span class="sxs-lookup"><span data-stu-id="ace8a-111">You can use your organizations existing subscription or use an [Azure trial](https://azure.microsoft.com/en-us/free/) to get started.</span></span> <span data-ttu-id="ace8a-112">O ambiente do CDS será disponibilizado gratuitamente durante um período limitado de 30 dias.</span><span class="sxs-lookup"><span data-stu-id="ace8a-112">The CDS environment will be provided free for a limited 30 day period.</span></span>

## <a name="subscribe"></a><span data-ttu-id="ace8a-113">Subscrever</span><span class="sxs-lookup"><span data-stu-id="ace8a-113">Subscribe</span></span>

<span data-ttu-id="ace8a-114">Quando o seu [pedido de pré-visualização](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) for aprovado, receberá três ofertas da Microsoft por e-mail.</span><span class="sxs-lookup"><span data-stu-id="ace8a-114">When your [preview request](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) is approved, you will receive three offers from Microsoft by email.</span></span> <span data-ttu-id="ace8a-115">Estas ofertas permitem implementar a Pré-visualização do Project Operations:</span><span class="sxs-lookup"><span data-stu-id="ace8a-115">These offers allow you to deploy the Project Operations Preview:</span></span>

- <span data-ttu-id="ace8a-116">Dynamics 365 Project Operations (CRM) – Avaliação da Pré-visualização</span><span class="sxs-lookup"><span data-stu-id="ace8a-116">Dynamics 365 Project Operations (CRM) - Preview Trial</span></span>
- <span data-ttu-id="ace8a-117">Office 365 Project Operations – Avaliação da Pré-visualização</span><span class="sxs-lookup"><span data-stu-id="ace8a-117">Office 365 Project Operations - Preview Trial</span></span>
- <span data-ttu-id="ace8a-118">Dynamics 365 Finance – Avaliação da Pré-visualização</span><span class="sxs-lookup"><span data-stu-id="ace8a-118">Dynamics 365 Finance - Preview Trial</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ace8a-119">Só uma pessoa, o administrador inquilino, numa organização precisa de executar esta tarefa.</span><span class="sxs-lookup"><span data-stu-id="ace8a-119">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="ace8a-120">Se não for subscritor desta versão, aguarde até a sua organização estar inscrita e receber as suas credenciais de utilizador.</span><span class="sxs-lookup"><span data-stu-id="ace8a-120">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>

### <a name="dynamics-365-project-operations-crm---preview-trial"></a><span data-ttu-id="ace8a-121">Dynamics 365 Project Operations (CRM) – Avaliação da Pré-visualização</span><span class="sxs-lookup"><span data-stu-id="ace8a-121">Dynamics 365 Project Operations (CRM) - Preview Trial</span></span> 

<span data-ttu-id="ace8a-122">Antes de começar, certifique-se de que está a iniciar sessão num browser com a conta de profissional de utilizador no inquilino onde pretende a pré-visualização do Project Operations.</span><span class="sxs-lookup"><span data-stu-id="ace8a-122">Before you begin, make sure you are logged in to a browser with the user work account in the tenant where you want the Project Operations preview.</span></span>

1. <span data-ttu-id="ace8a-123">Resgate o primeiro código de oferta, **Dynamics 365 Project Operations (CRM) – Avaliação da Pré-visualização**, colando-o no URL do browser.</span><span class="sxs-lookup"><span data-stu-id="ace8a-123">Redeem the first offer code, **Dynamics 365 Project Operations (CRM) - Preview Trial** by pasting it into the browser URL.</span></span>

![Resgatar Oferta](./media/16RedeemFirstOfferNew.png)

2. <span data-ttu-id="ace8a-125">Confirme a encomenda.</span><span class="sxs-lookup"><span data-stu-id="ace8a-125">Confirm your order.</span></span>

![Confirme a encomenda](./media/17ConfirmOrderNew.png)

<span data-ttu-id="ace8a-127">Verá que a oferta de confirmação foi resgatada com sucesso.</span><span class="sxs-lookup"><span data-stu-id="ace8a-127">You will see confirmation offer was successfully redeemed.</span></span>

![Confirmação](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a><span data-ttu-id="ace8a-129">Office 365 Project Operations – Avaliação da Pré-visualização</span><span class="sxs-lookup"><span data-stu-id="ace8a-129">Office 365 Project Operations - Preview Trial</span></span>

<span data-ttu-id="ace8a-130">Repita os mesmos passos que com o primeiro código de oferta.</span><span class="sxs-lookup"><span data-stu-id="ace8a-130">Repeat the same steps as with the first offer code.</span></span> <span data-ttu-id="ace8a-131">Certifique-se de que adiciona o segundo código de oferta usando a mesma conta de utilizador que foi usada com o código da primeira oferta.</span><span class="sxs-lookup"><span data-stu-id="ace8a-131">Make sure to add the second offer code using the same user account that was used with the first offer code.</span></span>

### <a name="dynamics-365-finance-preview-trial"></a><span data-ttu-id="ace8a-132">Avaliação da pré-visualização do Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="ace8a-132">Dynamics 365 Finance preview trial</span></span>

<span data-ttu-id="ace8a-133">Repita os mesmos passos com a última oferta do e-mail de boas-vindas.</span><span class="sxs-lookup"><span data-stu-id="ace8a-133">Repeat the same steps with the last offer from the Welcome email.</span></span>

## <a name="assign-licenses"></a><span data-ttu-id="ace8a-134">Atribuir licenças</span><span class="sxs-lookup"><span data-stu-id="ace8a-134">Assign licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ace8a-135">Necessitará de acesso administrativo ao Portal Microsoft 365 da sua organização do para concluir os seguintes passos.</span><span class="sxs-lookup"><span data-stu-id="ace8a-135">You will need administrative access to your organization's Microsoft 365 Portal to complete the following steps.</span></span>

1. <span data-ttu-id="ace8a-136">Vá para o [Centro de administração do Microsoft 365](https://portal.office.com/) para atribuir as licenças aos seus utilizadores.</span><span class="sxs-lookup"><span data-stu-id="ace8a-136">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign the licenses to your users.</span></span>

![Home page do centro de administração](./media/14AdminPortal.png)

2. <span data-ttu-id="ace8a-138">Na página **Utilizadores ativos**, selecione os utilizadores aos quais pretende atribuir uma licença.</span><span class="sxs-lookup"><span data-stu-id="ace8a-138">On the **Active users** page, select the users that you want to assign a license to.</span></span>

![Atribuir Licenças](./media/15AssignLicenses.png)

3. <span data-ttu-id="ace8a-140">Verifique se as licenças **Pré-visualização do Dynamics 365 Project Operations (CRM)** e **Office 365 Project Operations – Pré-visualização** foram selecionadas e selecione **Guardar alterações**.</span><span class="sxs-lookup"><span data-stu-id="ace8a-140">Verify that the **Dynamics 365 Project Operations (CRM) Preview** and **Office 365 Project Operations - Preview** license have been selected and select **Save changes**.</span></span>

> [!NOTE]
> <span data-ttu-id="ace8a-141">A oferta de avaliação do Finance não precisa de ser atribuída a um utilizador.</span><span class="sxs-lookup"><span data-stu-id="ace8a-141">The Finance trial offer does not need to be assigned to a user.</span></span>

## <a name="start-a-new-project-in-lcs"></a><span data-ttu-id="ace8a-142">Iniciar um novo projeto no LCS</span><span class="sxs-lookup"><span data-stu-id="ace8a-142">Start a new project in LCS</span></span>

<span data-ttu-id="ace8a-143">Criar um novo projeto LCS conforme descrito no tópico [Iniciar um novo projeto no LCS](create-lcs-project.md)</span><span class="sxs-lookup"><span data-stu-id="ace8a-143">Create a new LCS project as described in the topic, [Start a new project in LCS](create-lcs-project.md)</span></span>

## <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="ace8a-144">Adicionar uma subscrição do Azure a um projeto LCS</span><span class="sxs-lookup"><span data-stu-id="ace8a-144">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="ace8a-145">Para concluir esta tarefa, siga os passos na tópico, [Adicionar uma subscrição do Azure ao projeto LCS](resource-add-azure-subscription-lcs-project.md).</span><span class="sxs-lookup"><span data-stu-id="ace8a-145">To complete this task, follow the steps in the topic, [Add an Azure subscription to LCS project](resource-add-azure-subscription-lcs-project.md).</span></span>

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="ace8a-146">Implementar o ambiente de demonstração do Finance com o Project Operations para cenários de recursos/non armazenados</span><span class="sxs-lookup"><span data-stu-id="ace8a-146">Deploy Finance demo environment with Project Operations for resource/non-stocked scenarios</span></span>

<span data-ttu-id="ace8a-147">Siga as orientações no tópico [Aprovisionar um novo ambiente](resource-provision-new-environment.md) para concluir a implementação.</span><span class="sxs-lookup"><span data-stu-id="ace8a-147">Follow the guidance in the topic, [Provision a new environment](resource-provision-new-environment.md) to complete the deployment.</span></span> <span data-ttu-id="ace8a-148">Utilize o tipo de implementação do [ambiente de demonstração](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) para pré-visualização.</span><span class="sxs-lookup"><span data-stu-id="ace8a-148">Use the [demo environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) deployment type for preview.</span></span> 

## <a name="install-cds-setup-and-configuration-data"></a><span data-ttu-id="ace8a-149">Instalar dados de configuração do CDS</span><span class="sxs-lookup"><span data-stu-id="ace8a-149">Install CDS setup and configuration data</span></span>

<span data-ttu-id="ace8a-150">Instale os dados de configuração do CDS descritos no tópico [Configurar e aplicar dados de configuração no Common Data Service](resource-apply-pro-setup-config-data.md).</span><span class="sxs-lookup"><span data-stu-id="ace8a-150">Install CDS setup and configuration data as described in the topic, [Set up and apply configuration data in the Common Data Service](resource-apply-pro-setup-config-data.md).</span></span>
<span data-ttu-id="ace8a-151">Complete este passo apenas após a implementação do ambiente de demonstração do Finance e os dados de demonstração no FO estarem prontos.</span><span class="sxs-lookup"><span data-stu-id="ace8a-151">Complete this step only after Finance demo environment is deployed and demo data in FO is ready.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]