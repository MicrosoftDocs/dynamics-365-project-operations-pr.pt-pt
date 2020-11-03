---
title: Ativar funcionalidades da aplicação Project Finder Mobile
description: Como ativar funcionalidades da aplicação Project Finder Mobile no Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 749c5682dc2e639843a0a8a085fe8af65502d433
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082411"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a><span data-ttu-id="851b5-103">Ativar funcionalidades da aplicação Project Finder Mobile (Project Service)</span><span class="sxs-lookup"><span data-stu-id="851b5-103">Enable Project Finder Mobile app features (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="851b5-104">Os seus recursos podem utilizar a aplicação Project Finder Mobile no seu telemóvel com o [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] para localizar novos projetos em que pretende trabalhar e atualizar os respetivos conjuntos de competências.</span><span class="sxs-lookup"><span data-stu-id="851b5-104">Your resources can use the Project Finder Mobile app on their phone with [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to find new projects to work on and update their skill sets.</span></span>  
  
 <span data-ttu-id="851b5-105">A aplicação está disponível para os telemóveis [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] e [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].</span><span class="sxs-lookup"><span data-stu-id="851b5-105">The app is available for [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] phones, and [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].</span></span>  
  
 <span data-ttu-id="851b5-106">É necessário especificar um par opções na definição dos parâmetros para a sua unidade organizacional para permitir aos utilizadores ver os requisitos do recurso dos projetos e atualizar as suas competências.</span><span class="sxs-lookup"><span data-stu-id="851b5-106">You need to set a couple of options in the parameters setting for your organizational unit to allow users to view projects' resource requirements and update their skills.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="851b5-107">A aplicação Project Finder Mobile só funciona com o [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], não com instalações no local.</span><span class="sxs-lookup"><span data-stu-id="851b5-107">The Project Finder Mobile app only works with [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], not with on-premises installations.</span></span>  
  
1. <span data-ttu-id="851b5-108">Vá para **Project Service > Parâmetros**.</span><span class="sxs-lookup"><span data-stu-id="851b5-108">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="851b5-109">Clique na definição dos parâmetros que pretende utilizar para permitir as funcionalidades da aplicação Project Finder Mobile.</span><span class="sxs-lookup"><span data-stu-id="851b5-109">Click the parameters setting you want to use for allowing the Project Finder Mobile app features.</span></span>  
  
3. <span data-ttu-id="851b5-110">Na área **Geral** , defina **Requisitos de recursos visíveis para os recursos** como **Sim**.</span><span class="sxs-lookup"><span data-stu-id="851b5-110">In the **General** area, set **Resource requirements visible to resources** to **Yes**.</span></span>  
  
4. <span data-ttu-id="851b5-111">Defina **Permitir a atualização de competência por recurso** como **Sim**.</span><span class="sxs-lookup"><span data-stu-id="851b5-111">Set **Allow skill update by resource** to **Yes**.</span></span>  
  
   <span data-ttu-id="851b5-112">![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span><span class="sxs-lookup"><span data-stu-id="851b5-112">![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span></span>  
  
   <span data-ttu-id="851b5-113">Esta é uma definição global.</span><span class="sxs-lookup"><span data-stu-id="851b5-113">This is a global setting.</span></span> <span data-ttu-id="851b5-114">Os gestores de projetos podem definir se um projeto individual será visível na página **Equipa do Projeto** desse projeto.</span><span class="sxs-lookup"><span data-stu-id="851b5-114">Project managers can set whether an individual project will be visible on that project's **Project Team** page.</span></span>  
  
   <span data-ttu-id="851b5-115">![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span><span class="sxs-lookup"><span data-stu-id="851b5-115">![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span></span>  
  
## <a name="email-notifications"></a><span data-ttu-id="851b5-116">Notificações por e-mail</span><span class="sxs-lookup"><span data-stu-id="851b5-116">Email notifications</span></span>  
 <span data-ttu-id="851b5-117">O [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] envia e-mails relativos aos pedidos de recursos para os seguintes destinatários às seguintes horas:</span><span class="sxs-lookup"><span data-stu-id="851b5-117">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sends emails regarding resource requests to the following recipients at the following times:</span></span>  
  
|<span data-ttu-id="851b5-118">Destinatário</span><span class="sxs-lookup"><span data-stu-id="851b5-118">Recipient</span></span>|<span data-ttu-id="851b5-119">Evento</span><span class="sxs-lookup"><span data-stu-id="851b5-119">Event</span></span>|  
|---------------|-----------|  
|<span data-ttu-id="851b5-120">Gestor de projeto</span><span class="sxs-lookup"><span data-stu-id="851b5-120">Project manager</span></span>|<span data-ttu-id="851b5-121">- Quando um recurso se inscreve num projeto com a aplicação Project Finder Mobile.</span><span class="sxs-lookup"><span data-stu-id="851b5-121">-   When a resource signs up for a project with the Project Finder Mobile app.</span></span>|  
|<span data-ttu-id="851b5-122">Recurso</span><span class="sxs-lookup"><span data-stu-id="851b5-122">Resource</span></span>|<span data-ttu-id="851b5-123">- Quando o trabalho do projeto em que o recurso se inscreveu já tiver sido concluída por outro recurso.</span><span class="sxs-lookup"><span data-stu-id="851b5-123">-   When the project work the resource has signed up for has already been fulfilled by another resource.</span></span><br /><span data-ttu-id="851b5-124">- Quando o pedido de aprovação da competência foi aprovado ou rejeitado.</span><span class="sxs-lookup"><span data-stu-id="851b5-124">-   When their skill approval request has been approved or rejected.</span></span><br /><span data-ttu-id="851b5-125">- Quando o pedido de inscrição no projeto foi aprovado ou rejeitado.</span><span class="sxs-lookup"><span data-stu-id="851b5-125">-   When their project sign up request has been approved or rejected.</span></span>|  
  
## <a name="privacy-notice"></a><span data-ttu-id="851b5-126">Aviso de privacidade</span><span class="sxs-lookup"><span data-stu-id="851b5-126">Privacy notice</span></span>  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a><span data-ttu-id="851b5-127">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="851b5-127">See Also</span></span>  
 [<span data-ttu-id="851b5-128">Configurar recursos</span><span class="sxs-lookup"><span data-stu-id="851b5-128">Set up resources</span></span>](../psa/set-up-resources.md)
