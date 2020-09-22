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
ms.prod: ''
ms.technology: ''
ms.assetid: 038c5c66-f136-4c7e-88c2-30ada80bbf38
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 9265ee78b20899026277e5af8e589112cd9fac74
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754470"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a>Ativar funcionalidades da aplicação Project Finder Mobile (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Os seus recursos podem utilizar a aplicação Project Finder Mobile no seu telemóvel com o [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] para localizar novos projetos em que pretende trabalhar e atualizar os respetivos conjuntos de competências.  
  
 A aplicação está disponível para os telemóveis [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] e [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].  
  
 É necessário especificar um par opções na definição dos parâmetros para a sua unidade organizacional para permitir aos utilizadores ver os requisitos do recurso dos projetos e atualizar as suas competências.  
  
> [!NOTE]
>  A aplicação Project Finder Mobile só funciona com o [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], não com instalações no local.  
  
1. Vá para **Project Service > Parâmetros**.  
  
2. Clique na definição dos parâmetros que pretende utilizar para permitir as funcionalidades da aplicação Project Finder Mobile.  
  
3. Na área **Geral**, defina **Requisitos de recursos visíveis para os recursos** como **Sim**.  
  
4. Defina **Permitir a atualização de competência por recurso** como **Sim**.  
  
   ![ProjectService_ProjectFinderEnable](../project-service/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")  
  
   Esta é uma definição global. Os gestores de projetos podem definir se um projeto individual será visível na página **Equipa do Projeto** desse projeto.  
  
   ![ProjectService_ProjectTeamVisible](../project-service/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")  
  
## <a name="email-notifications"></a>Notificações por e-mail  
 O [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] envia e-mails relativos aos pedidos de recursos para os seguintes destinatários às seguintes horas:  
  
|Destinatário|Evento|  
|---------------|-----------|  
|Gestor de projeto|- Quando um recurso se inscreve num projeto com a aplicação Project Finder Mobile.|  
|Recurso|- Quando o trabalho do projeto em que o recurso se inscreveu já tiver sido concluída por outro recurso.<br />- Quando o pedido de aprovação da competência foi aprovado ou rejeitado.<br />- Quando o pedido de inscrição no projeto foi aprovado ou rejeitado.|  
  
## <a name="privacy-notice"></a>Aviso de privacidade  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a>Consulte Também  
 [Configurar recursos](../project-service/set-up-resources.md)
