---
title: Inscrever-se para obter uma subscrição de pré-visualização – lite
description: Este tópico fornece informações sobre como subscrever e implementar o Project Operations lite - oportunidade potencial para fatura pró-forma.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2b5a65f5e29915c349d40400ebbf3e4923b36a67
ms.sourcegitcommit: 52b26950bb3b1596ad81aa4ff91745ee9615d1b0
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334796"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a><span data-ttu-id="b1359-103">Inscrever-se para obter uma subscrição de pré-visualização - leve</span><span class="sxs-lookup"><span data-stu-id="b1359-103">Sign up for a preview subscription - lite</span></span> 

<span data-ttu-id="b1359-104">Este tópico explica como subscrever a oferta de avaliação e proceder à implementação leve Dynamics 365 Project Operations - oportunidade potencial para fatura pro forma.</span><span class="sxs-lookup"><span data-stu-id="b1359-104">This topic explains how to subscribe to the trial offer and deploy Dynamics 365 Project Operations lite deployment - deal to proforma invoicing.</span></span>

> [!NOTE]
> <span data-ttu-id="b1359-105">Este processo será alterado nas próximas versões do Project Operations.</span><span class="sxs-lookup"><span data-stu-id="b1359-105">This process will change in upcoming releases of Project Operations.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b1359-106">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="b1359-106">Prerequisites</span></span>
- <span data-ttu-id="b1359-107">O utilizador que implementar a pré-visualização tem de ter direitos de administrator global do inquilino do Azure.</span><span class="sxs-lookup"><span data-stu-id="b1359-107">The user who deploys the preview must have Azure tenant global administrator rights.</span></span> <span data-ttu-id="b1359-108">Poderá criar um inquilino durante o primeiro resgate da oferta.</span><span class="sxs-lookup"><span data-stu-id="b1359-108">You can create a tenant during the first offer redemption.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b1359-109">Só uma pessoa, o administrador inquilino, numa organização precisa de executar esta tarefa.</span><span class="sxs-lookup"><span data-stu-id="b1359-109">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="b1359-110">Se não for subscritor desta versão, aguarde até a sua organização estar inscrita e receber as suas credenciais de utilizador.</span><span class="sxs-lookup"><span data-stu-id="b1359-110">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>
> 
> <span data-ttu-id="b1359-111">As avaliações são de utilização única no inquilino.</span><span class="sxs-lookup"><span data-stu-id="b1359-111">Trials are single use in the tenant.</span></span> <span data-ttu-id="b1359-112">Só é possível executar uma avaliação uma vez.</span><span class="sxs-lookup"><span data-stu-id="b1359-112">You can only run a trial one time.</span></span> <span data-ttu-id="b1359-113">Recomendamos que crie um novo inquilino para os fins da avaliação.</span><span class="sxs-lookup"><span data-stu-id="b1359-113">We recommend that you create a new tenant for the purpose of the trial.</span></span>

### <a name="dynamics-365-project-operations-trial"></a><span data-ttu-id="b1359-114">Avaliação do Dynamics 365 Project Operations</span><span class="sxs-lookup"><span data-stu-id="b1359-114">Dynamics 365 Project Operations trial</span></span> 

<span data-ttu-id="b1359-115">Antes de começar, certifique-se de que está a iniciar sessão num browser com a conta de profissional de utilizador no inquilino onde pretende a pré-visualização do Project Operations.</span><span class="sxs-lookup"><span data-stu-id="b1359-115">Before you begin, make sure you are logged in to a browser with the user work account in the tenant where you want the Project Operations preview.</span></span>

1. <span data-ttu-id="b1359-116">Vá para [Avaliação do Project Operations](https://aka.ms/try-po) para resgatar o primeiro código de oferta, **Dynamics 365 Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="b1359-116">Go to [Project Operations Trial](https://aka.ms/try-po) to redeem the first offer code, **Dynamics 365 Project Operations**.</span></span>
2. <span data-ttu-id="b1359-117">Confirme a encomenda.</span><span class="sxs-lookup"><span data-stu-id="b1359-117">Confirm your order.</span></span>

  <span data-ttu-id="b1359-118">Verá que a oferta de confirmação foi resgatada com êxito.</span><span class="sxs-lookup"><span data-stu-id="b1359-118">You'll see the confirmation offer was successfully redeemed.</span></span>

## <a name="assign-licenses"></a><span data-ttu-id="b1359-119">Atribuir licenças</span><span class="sxs-lookup"><span data-stu-id="b1359-119">Assign licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b1359-120">Necessitará de acesso administrativo ao Portal Microsoft 365 da sua organização do para concluir os seguintes passos.</span><span class="sxs-lookup"><span data-stu-id="b1359-120">You will need administrative access to your organization's Microsoft 365 Portal to complete the following steps.</span></span>


1. <span data-ttu-id="b1359-121">Vá para o [Centro de administração do Microsoft 365](https://portal.office.com/) para atribuir as licenças aos seus utilizadores.</span><span class="sxs-lookup"><span data-stu-id="b1359-121">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign the licenses to your users.</span></span>
2. <span data-ttu-id="b1359-122">Na página **Utilizadores ativos**, selecione os utilizadores aos quais pretende atribuir uma licença.</span><span class="sxs-lookup"><span data-stu-id="b1359-122">On the **Active users** page, select the users that you want to assign a license to.</span></span>
3. <span data-ttu-id="b1359-123">Verifique se a licença **Dynamics 365 Project Operations** foi selecionada.</span><span class="sxs-lookup"><span data-stu-id="b1359-123">Verify that the **Dynamics 365 Project Operations** license is selected.</span></span> 
4. <span data-ttu-id="b1359-124">Selecione **Guardar alterações**.</span><span class="sxs-lookup"><span data-stu-id="b1359-124">Select **Save changes**.</span></span>

## <a name="create-a-new-dataverse-environment"></a><span data-ttu-id="b1359-125">Criar um novo ambiente do Dataverse</span><span class="sxs-lookup"><span data-stu-id="b1359-125">Create a new Dataverse environment</span></span>

1. <span data-ttu-id="b1359-126">Aprovisione um novo ambiente de implementação do Project Operations Dataverse ao seguir as instruções no tópico [Modelo de implementação do Dataverse](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="b1359-126">Provision a new Project Operations Dataverse deployment environment by following instructions in the topic, [Dataverse deployment model](lite-deployment.md).</span></span> <span data-ttu-id="b1359-127">Ao selecionar o tipo de ambiente, certifique-se de que utiliza **Avaliação (baseado em Subscrição)**.</span><span class="sxs-lookup"><span data-stu-id="b1359-127">When you select the environment type, make sure to use **Trial (Subscription based)**.</span></span>

  ![Novo ambiente](./media/19CreateEnvironment.png)

2. <span data-ttu-id="b1359-129">Selecione a definição **Ativar aplicações do Dynamics 365** e deixe **Implementar automaticamente estas aplicações** em branco.</span><span class="sxs-lookup"><span data-stu-id="b1359-129">Select the **Enable Dynamics 365 apps** setting, and leave **Automatically deploy these apps** blank.</span></span>  
3. <span data-ttu-id="b1359-130">Selecione **Guardar** para criar o ambiente.</span><span class="sxs-lookup"><span data-stu-id="b1359-130">Select **Save** to create the environment.</span></span>

  ![Adicionar base de dados](./media/20CreateEnvironment1.png)

4. <span data-ttu-id="b1359-132">Depois de criar o ambiente, instale a solução **Microsoft Dynamics 365 Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="b1359-132">After the environment is created, install **Microsoft Dynamics 365 Project Operations** solution.</span></span> 

![Instalar Solução](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a><span data-ttu-id="b1359-134">Instalar uma configuração CDS e dados de demonstração da configuração</span><span class="sxs-lookup"><span data-stu-id="b1359-134">Install a CDS configuration and setup demo data</span></span>

<span data-ttu-id="b1359-135">Instale a configuração CDS e configure os dados de demonstração da configuração ao seguir as instruções no tópico [Aplicar dados de configuração da demonstração](lite-apply-demo-setup-config-data.md).</span><span class="sxs-lookup"><span data-stu-id="b1359-135">Install the CDS configuration and set up demo data by following instructions in the topic, [Apply demo setup and configuration data](lite-apply-demo-setup-config-data.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
