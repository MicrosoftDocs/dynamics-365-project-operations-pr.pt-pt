---
title: Inscrever-se para obter uma subscrição de pré-visualização – lite
description: Este tópico fornece informações sobre como subscrever e implementar o Project Operations lite - oportunidade potencial para fatura pró-forma.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 44edf2613ea4b26dadbd9edc47c784c488c577de
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290058"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a><span data-ttu-id="b2b69-103">Inscrever-se para obter uma subscrição de pré-visualização – lite</span><span class="sxs-lookup"><span data-stu-id="b2b69-103">Sign up for a preview subscription - lite</span></span> 

<span data-ttu-id="b2b69-104">Este tópico explica como subscrever a oferta do parceiro de pré-visualização e implementar o Dynamics 365 Project Operations lite para faturação proforma.</span><span class="sxs-lookup"><span data-stu-id="b2b69-104">This topic explains how to subscribe to the preview partner offer and deploy Dynamics 365 Project Operations lite deployment - deal to proforma invoicing.</span></span>

> [!NOTE]
> <span data-ttu-id="b2b69-105">Este processo será alterado nas próximas versões do Project Operations.</span><span class="sxs-lookup"><span data-stu-id="b2b69-105">This process will change in upcoming releases of Project Operations.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b2b69-106">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="b2b69-106">Prerequisites</span></span>

- <span data-ttu-id="b2b69-107">Receberá um e-mail a convidá-lo para participar na pré-visualização.</span><span class="sxs-lookup"><span data-stu-id="b2b69-107">You'll receive an email inviting you to participate in the preview.</span></span> <span data-ttu-id="b2b69-108">Pode solicitar uma pré-visualização no [Web site do Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span><span class="sxs-lookup"><span data-stu-id="b2b69-108">You can request a preview on the [Project Operations website](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span></span>
- <span data-ttu-id="b2b69-109">O utilizador que implementar a pré-visualização tem de ter direitos de administrator global do inquilino do Azure.</span><span class="sxs-lookup"><span data-stu-id="b2b69-109">The user who deploys the preview must have Azure tenant global administrator rights.</span></span>
- <span data-ttu-id="b2b69-110">Reveja todos os termos e condições.</span><span class="sxs-lookup"><span data-stu-id="b2b69-110">Review all terms and conditions.</span></span>

## <a name="subscribe"></a><span data-ttu-id="b2b69-111">Subscrever</span><span class="sxs-lookup"><span data-stu-id="b2b69-111">Subscribe</span></span>

<span data-ttu-id="b2b69-112">Quando receber uma aprovação de [pedido de pré-visualização](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u), receberá duas ofertas da Microsoft por e-mail.</span><span class="sxs-lookup"><span data-stu-id="b2b69-112">When you receive a [preview request](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) approval, you'll receive two offers from Microsoft by email.</span></span> <span data-ttu-id="b2b69-113">Estas ofertas permitem implementar a Pré-visualização do Project Operations:</span><span class="sxs-lookup"><span data-stu-id="b2b69-113">These offers allow you to deploy the Project Operations Preview:</span></span>

- <span data-ttu-id="b2b69-114">Dynamics 365 Project Operations (CRM) – Avaliação da Pré-visualização</span><span class="sxs-lookup"><span data-stu-id="b2b69-114">Dynamics 365 Project Operations (CRM) - Preview Trial</span></span>
- <span data-ttu-id="b2b69-115">Office 365 Project Operations – Avaliação da Pré-visualização</span><span class="sxs-lookup"><span data-stu-id="b2b69-115">Office 365 Project Operations - Preview Trial</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b2b69-116">Só uma pessoa, o administrador inquilino, numa organização precisa de executar esta tarefa.</span><span class="sxs-lookup"><span data-stu-id="b2b69-116">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="b2b69-117">Se não for subscritor desta versão, aguarde até a sua organização estar inscrita e receber as suas credenciais de utilizador.</span><span class="sxs-lookup"><span data-stu-id="b2b69-117">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>

### <a name="dynamics-365-project-operations-crm---preview-trial"></a><span data-ttu-id="b2b69-118">Dynamics 365 Project Operations (CRM) – Avaliação da Pré-visualização</span><span class="sxs-lookup"><span data-stu-id="b2b69-118">Dynamics 365 Project Operations (CRM) - Preview Trial</span></span> 

<span data-ttu-id="b2b69-119">Antes de começar, certifique-se de que está a iniciar sessão num browser com a conta de profissional de utilizador no inquilino onde pretende a pré-visualização do Project Operations.</span><span class="sxs-lookup"><span data-stu-id="b2b69-119">Before you begin, make sure you are logged in to a browser with the user work account in the tenant where you want the Project Operations preview.</span></span>

1. <span data-ttu-id="b2b69-120">Resgate o primeiro código de oferta, **Dynamics 365 Project Operations (CRM) – Avaliação da Pré-visualização**, colando-o no URL do browser.</span><span class="sxs-lookup"><span data-stu-id="b2b69-120">Redeem the first offer code, **Dynamics 365 Project Operations (CRM) - Preview Trial** by pasting it into the browser URL.</span></span>

![Resgatar Oferta](./media/16RedeemFirstOfferNew.png)

2. <span data-ttu-id="b2b69-122">Confirme a encomenda.</span><span class="sxs-lookup"><span data-stu-id="b2b69-122">Confirm your order.</span></span>
<span data-ttu-id="b2b69-123">![Confirme a encomenda](./media/17ConfirmOrderNew.png)</span><span class="sxs-lookup"><span data-stu-id="b2b69-123">![Confirm the order](./media/17ConfirmOrderNew.png)</span></span>

<span data-ttu-id="b2b69-124">Verá que a oferta de confirmação foi resgatada com sucesso.</span><span class="sxs-lookup"><span data-stu-id="b2b69-124">You'll see confirmation offer was successfully redeemed.</span></span>

![Confirmação](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a><span data-ttu-id="b2b69-126">Office 365 Project Operations – Avaliação da Pré-visualização</span><span class="sxs-lookup"><span data-stu-id="b2b69-126">Office 365 Project Operations - Preview Trial</span></span>

<span data-ttu-id="b2b69-127">Repita os mesmos passos que com o primeiro código de oferta.</span><span class="sxs-lookup"><span data-stu-id="b2b69-127">Repeat the same steps as with the first offer code.</span></span> <span data-ttu-id="b2b69-128">Certifique-se de que adiciona o segundo código de oferta usando a mesma conta de utilizador que foi usada com o código da primeira oferta.</span><span class="sxs-lookup"><span data-stu-id="b2b69-128">Make sure to add the second offer code using the same user account that was used with the first offer code.</span></span>

## <a name="assign-licenses"></a><span data-ttu-id="b2b69-129">Atribuir licenças</span><span class="sxs-lookup"><span data-stu-id="b2b69-129">Assign licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b2b69-130">Necessitará de acesso administrativo ao Portal Microsoft 365 da sua organização do para concluir os seguintes passos.</span><span class="sxs-lookup"><span data-stu-id="b2b69-130">You will need administrative access to your organization's Microsoft 365 Portal to complete the following steps.</span></span>


1. <span data-ttu-id="b2b69-131">Vá para o [Centro de administração do Microsoft 365](https://portal.office.com/) para atribuir as licenças aos seus utilizadores.</span><span class="sxs-lookup"><span data-stu-id="b2b69-131">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign the licenses to your users.</span></span>

![Home page do centro de administração](./media/14AdminPortal.png)

2. <span data-ttu-id="b2b69-133">Na página **Utilizadores ativos**, selecione os utilizadores aos quais pretende atribuir uma licença.</span><span class="sxs-lookup"><span data-stu-id="b2b69-133">On the **Active users** page, select the users that you want to assign a license to.</span></span>

![Atribuir Licenças](./media/15AssignLicenses.png)

3. <span data-ttu-id="b2b69-135">Verifique se estão selecionadas as licenças de pré-visualização **Dynamics 365 Project Operations (CRM)** e **Office 365Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="b2b69-135">Verify that the **Dynamics 365 Project Operations (CRM) Preview** and **Office 365 Project Operations - Preview** licenses are selected.</span></span> 
4. <span data-ttu-id="b2b69-136">Selecione **Guardar alterações**.</span><span class="sxs-lookup"><span data-stu-id="b2b69-136">Select **Save changes**.</span></span>

## <a name="create-a-new-cds-environment"></a><span data-ttu-id="b2b69-137">Criar um novo ambiente de CDS</span><span class="sxs-lookup"><span data-stu-id="b2b69-137">Create a new CDS environment</span></span>

1. <span data-ttu-id="b2b69-138">Aprovisione um novo ambiente de implementação de CDS do Project Operations ao seguir as instruções no tópico [Modelo de implementação CDS](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="b2b69-138">Provision a new Project Operations CDS deployment environment by following instructions in the topic, [CDS deployment model](lite-deployment.md).</span></span> <span data-ttu-id="b2b69-139">Ao selecionar o tipo de ambiente, certifique-se de que utiliza **Avaliação (baseado em Subscrição)**.</span><span class="sxs-lookup"><span data-stu-id="b2b69-139">When you select the environment type, make sure to use **Trial (Subscription based)**.</span></span>
<span data-ttu-id="b2b69-140">![Novo ambiente](./media/19CreateEnvironment.png)</span><span class="sxs-lookup"><span data-stu-id="b2b69-140">![New environment](./media/19CreateEnvironment.png)</span></span>

2. <span data-ttu-id="b2b69-141">Selecione a definição **Ativar aplicações do Dynamics 365** e deixe **Implementar automaticamente estas aplicações** em branco.</span><span class="sxs-lookup"><span data-stu-id="b2b69-141">Select the **Enable Dynamics 365 apps** setting, and leave **Automatically deploy these apps** blank.</span></span>  
3. <span data-ttu-id="b2b69-142">Selecione **Guardar** para criar o ambiente.</span><span class="sxs-lookup"><span data-stu-id="b2b69-142">Select **Save** to create the environment.</span></span>

![Adicionar base de dados](./media/20CreateEnvironment1.png)

4. <span data-ttu-id="b2b69-144">Depois de criar o ambiente, instale a solução **Microsoft Dynamics 365 Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="b2b69-144">After the environment is created, install **Microsoft Dynamics 365 Project Operations** solution.</span></span> 

![Instalar Solução](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a><span data-ttu-id="b2b69-146">Instalar uma configuração CDS e dados de demonstração da configuração</span><span class="sxs-lookup"><span data-stu-id="b2b69-146">Install a CDS configuration and setup demo data</span></span>

<span data-ttu-id="b2b69-147">Instale a configuração CDS e configure os dados de demonstração da configuração ao seguir as instruções no tópico [Aplicar dados de configuração da demonstração](lite-apply-demo-setup-config-data.md).</span><span class="sxs-lookup"><span data-stu-id="b2b69-147">Install the CDS configuration and set up demo data by following instructions in the topic, [Apply demo setup and configuration data](lite-apply-demo-setup-config-data.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]