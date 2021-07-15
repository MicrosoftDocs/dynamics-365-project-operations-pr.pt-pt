---
title: Inscreva-se nas subscrições de pré-visualização do Project Operations para os cenários de recursos/não armazenados
description: Este tópico fornece informações sobre como subscrever e implementar o Project Operations para cenários baseados em recursos/não armazenados.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: da93fcf23ee3f255812842e31cb22b5d39daa963
ms.sourcegitcommit: 52b26950bb3b1596ad81aa4ff91745ee9615d1b0
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334841"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a><span data-ttu-id="8d08d-103">Inscreva-se nas subscrições de pré-visualização do Project Operations para os cenários de recursos/não armazenados</span><span class="sxs-lookup"><span data-stu-id="8d08d-103">Sign up for Project Operations preview subscriptions for resource/ non-stocked scenarios</span></span>

<span data-ttu-id="8d08d-104">_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_</span><span class="sxs-lookup"><span data-stu-id="8d08d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="8d08d-105">Este tópico explica como subscrever a oferta de avaliação e implementar o ambiente do Project Operations para os cenários baseados em recursos/não armazenados.</span><span class="sxs-lookup"><span data-stu-id="8d08d-105">This topic explains how to subscribe to the trial offer and deploy Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="8d08d-106">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="8d08d-106">Prerequisites</span></span>
- <span data-ttu-id="8d08d-107">O utilizador que implementar a pré-visualização tem de ter direitos de administrator global do inquilino do Azure.</span><span class="sxs-lookup"><span data-stu-id="8d08d-107">The user who deploys the preview must have Azure tenant global administrator rights.</span></span> <span data-ttu-id="8d08d-108">Poderá criar um inquilino durante o primeiro resgate da oferta.</span><span class="sxs-lookup"><span data-stu-id="8d08d-108">You can create a tenant during the first offer redemption.</span></span> 
- <span data-ttu-id="8d08d-109">A implementação de um ambiente do Finance requer uma subscrição válida do Azure que será faturada por ambiente.</span><span class="sxs-lookup"><span data-stu-id="8d08d-109">Deploying a Finance environment requires a valid Azure subscription that will be billed per environment.</span></span> <span data-ttu-id="8d08d-110">Poderá utilizar subscrição existente das suas organizações ou utilizar uma [Avaliação do Azure](https://azure.microsoft.com/en-us/free/) para começar.</span><span class="sxs-lookup"><span data-stu-id="8d08d-110">You can use your organizations existing subscription or use an [Azure trial](https://azure.microsoft.com/en-us/free/) to get started.</span></span> <span data-ttu-id="8d08d-111">O ambiente do CDS será disponibilizado gratuitamente durante um período limitado de 30 dias.</span><span class="sxs-lookup"><span data-stu-id="8d08d-111">The CDS environment will be provided free for a limited 30 day period.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8d08d-112">Só uma pessoa, o administrador inquilino, numa organização precisa de executar esta tarefa.</span><span class="sxs-lookup"><span data-stu-id="8d08d-112">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="8d08d-113">Se não for subscritor desta versão, aguarde até a sua organização estar inscrita e receber as suas credenciais de utilizador.</span><span class="sxs-lookup"><span data-stu-id="8d08d-113">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>
> 
> <span data-ttu-id="8d08d-114">As avaliações são de utilização única no inquilino.</span><span class="sxs-lookup"><span data-stu-id="8d08d-114">Trials are single use in the tenant.</span></span> <span data-ttu-id="8d08d-115">Só é possível executar uma avaliação uma vez.</span><span class="sxs-lookup"><span data-stu-id="8d08d-115">You can only run a trial one time.</span></span> <span data-ttu-id="8d08d-116">Recomendamos que crie um novo inquilino para os fins da avaliação.</span><span class="sxs-lookup"><span data-stu-id="8d08d-116">We recommend that you create a new tenant for the purpose of the trial.</span></span>


### <a name="dynamics-365-project-operations-ce---preview-trial"></a><span data-ttu-id="8d08d-117">Dynamics 365 Project Operations (CE) - Avaliação de Pré-visualização</span><span class="sxs-lookup"><span data-stu-id="8d08d-117">Dynamics 365 Project Operations (CE) - Preview Trial</span></span> 

<span data-ttu-id="8d08d-118">Antes de começar, certifique-se de que está a iniciar sessão num browser com a conta de profissional de utilizador no inquilino onde pretende a pré-visualização do Project Operations.</span><span class="sxs-lookup"><span data-stu-id="8d08d-118">Before you begin, make sure you are logged in to a browser with the user work account in the tenant where you want the Project Operations preview.</span></span>

1. <span data-ttu-id="8d08d-119">Resgate o primeiro código de oferta do **Dynamics 365 Project Operations** aqui [Avaliação do Project Operations](https://aka.ms/try-po).</span><span class="sxs-lookup"><span data-stu-id="8d08d-119">Redeem the first offer code, **Dynamics 365 Project Operations** here [Project Operations Trial](https://aka.ms/try-po).</span></span>
2. <span data-ttu-id="8d08d-120">Confirme a encomenda.</span><span class="sxs-lookup"><span data-stu-id="8d08d-120">Confirm your order.</span></span>

  <span data-ttu-id="8d08d-121">Verá que a oferta de confirmação foi resgatada com sucesso.</span><span class="sxs-lookup"><span data-stu-id="8d08d-121">You will see confirmation offer was successfully redeemed.</span></span>

### <a name="dynamics-365-finance-preview-trial"></a><span data-ttu-id="8d08d-122">Avaliação da pré-visualização do Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="8d08d-122">Dynamics 365 Finance preview trial</span></span>

<span data-ttu-id="8d08d-123">Vá para [Avaliação da Pré-visualização do Dynamics 365 for Finance](https://aka.ms/trypoche) e repita os passos da secção anterior com a oferta, Inscrição no Ambiente Alojado na Cloud.</span><span class="sxs-lookup"><span data-stu-id="8d08d-123">Go to [Dynamics 365 for Finance Preview Trial](https://aka.ms/trypoche) and repeat the steps from the previous section with the offer, Sign up for the Cloud Hosted Environment.</span></span>  

## <a name="assign-licenses"></a><span data-ttu-id="8d08d-124">Atribuir licenças</span><span class="sxs-lookup"><span data-stu-id="8d08d-124">Assign licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8d08d-125">Necessitará de acesso administrativo ao Portal Microsoft 365 da sua organização do para concluir os seguintes passos.</span><span class="sxs-lookup"><span data-stu-id="8d08d-125">You will need administrative access to your organization's Microsoft 365 Portal to complete the following steps.</span></span>

1. <span data-ttu-id="8d08d-126">Vá para o [Centro de administração do Microsoft 365](https://portal.office.com/) para atribuir as licenças aos seus utilizadores.</span><span class="sxs-lookup"><span data-stu-id="8d08d-126">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign the licenses to your users.</span></span>

2. <span data-ttu-id="8d08d-127">Na página **Utilizadores ativos**, selecione os utilizadores aos quais pretende atribuir uma licença.</span><span class="sxs-lookup"><span data-stu-id="8d08d-127">On the **Active users** page, select the users that you want to assign a license to.</span></span>

3. <span data-ttu-id="8d08d-128">Verifique se a licença do **Dynamics 365 Project Operations** foi selecionada e selecione **Guardar alterações**.</span><span class="sxs-lookup"><span data-stu-id="8d08d-128">Verify that the **Dynamics 365 Project Operations** license has been selected and select **Save changes**.</span></span>

> [!NOTE]
> <span data-ttu-id="8d08d-129">A oferta de avaliação do Finance não precisa de ser atribuída a um utilizador.</span><span class="sxs-lookup"><span data-stu-id="8d08d-129">The Finance trial offer does not need to be assigned to a user.</span></span>

## <a name="start-a-new-project-in-lcs"></a><span data-ttu-id="8d08d-130">Iniciar um novo projeto no LCS</span><span class="sxs-lookup"><span data-stu-id="8d08d-130">Start a new project in LCS</span></span>

<span data-ttu-id="8d08d-131">Criar um novo projeto LCS conforme descrito no tópico [Iniciar um novo projeto no LCS](create-lcs-project.md)</span><span class="sxs-lookup"><span data-stu-id="8d08d-131">Create a new LCS project as described in the topic, [Start a new project in LCS](create-lcs-project.md)</span></span>

## <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="8d08d-132">Adicionar uma subscrição do Azure a um projeto LCS</span><span class="sxs-lookup"><span data-stu-id="8d08d-132">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="8d08d-133">Para concluir esta tarefa, siga os passos na tópico, [Adicionar uma subscrição do Azure ao projeto LCS](resource-add-azure-subscription-lcs-project.md).</span><span class="sxs-lookup"><span data-stu-id="8d08d-133">To complete this task, follow the steps in the topic, [Add an Azure subscription to LCS project](resource-add-azure-subscription-lcs-project.md).</span></span>

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="8d08d-134">Implementar o ambiente de demonstração do Finance com o Project Operations para cenários de recursos/non armazenados</span><span class="sxs-lookup"><span data-stu-id="8d08d-134">Deploy Finance demo environment with Project Operations for resource/non-stocked scenarios</span></span>

<span data-ttu-id="8d08d-135">Siga as orientações no tópico [Aprovisionar um novo ambiente](resource-provision-new-environment.md) para concluir a implementação.</span><span class="sxs-lookup"><span data-stu-id="8d08d-135">Follow the guidance in the topic, [Provision a new environment](resource-provision-new-environment.md) to complete the deployment.</span></span> <span data-ttu-id="8d08d-136">Utilize o tipo de implementação do [ambiente de demonstração](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) para pré-visualização.</span><span class="sxs-lookup"><span data-stu-id="8d08d-136">Use the [demo environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) deployment type for preview.</span></span> 

## <a name="install-cds-setup-and-configuration-data"></a><span data-ttu-id="8d08d-137">Instalar dados de configuração do CDS</span><span class="sxs-lookup"><span data-stu-id="8d08d-137">Install CDS setup and configuration data</span></span>

<span data-ttu-id="8d08d-138">Instale os dados de configuração do CDS descritos no tópico [Configurar e aplicar dados de configuração no Common Data Service](resource-apply-pro-setup-config-data.md).</span><span class="sxs-lookup"><span data-stu-id="8d08d-138">Install CDS setup and configuration data as described in the topic, [Set up and apply configuration data in the Common Data Service](resource-apply-pro-setup-config-data.md).</span></span>
<span data-ttu-id="8d08d-139">Conclua este passo apenas após a implementação do ambiente de demonstração do Finance e de os dados de demonstração estarem prontos.</span><span class="sxs-lookup"><span data-stu-id="8d08d-139">Complete this step only after Finance demo environment is deployed and demo data is ready.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
