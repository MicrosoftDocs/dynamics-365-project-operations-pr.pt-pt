---
title: Implementar o Project Operations – lite
description: Este tópico fornece informações sobre como instalar a implementação do Project Operations lite - oportunidade potencial para fatura pró-forma.
author: stsporen
ms.date: 02/28/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: e33506504665f2e7ef7ad48469082f9f64a2a44b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580746"
---
# <a name="deploy-project-operations---lite"></a>Implementar o Project Operations – lite

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_



O Project Operations suporta vários modelos de implementação. Para determinar o melhor modelo de implementação, consulte [Tipo de implementação](determine-deployment-type.md).


> [!IMPORTANT]
> Esta implementação, Implementação leve - oportunidade potencial para fatura pró-forma, resulta numa **Implementação só do Dataverse do Project Operations**.

- [Instalar o Project Operations num novo ambiente Dataverse](#new)
- [Instalar num ambiente Dataverse existente](#existing)



## <a name="install-project-operations-to-a-new-dataverse-environment"></a><a name="new"></a>Instalar o Project Operations num novo ambiente Dataverse

1. Como [Administrador Global ou do Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) com uma licença do Project Operations, crie um novo ambiente Dataverse no [Centro de administração do PowerPlatform](https://admin.powerplatform.com). Certifique-se de que a **Criação de uma base de dados para este ambiente** e **as aplicações do Dynamics 365** estão ativadas. Para mais informações, consulte [Criar e gerir ambientes no Centro de administração do Power Platform](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
2. Selecione **Microsoft Dynamics 365 Project Operations** da lista de implementação de aplicações do Dynamics 365.


## <a name="install-project-operations-to-an-existing-dataverse-environment"></a><a name="existing"></a>Instalar o Project Operations num ambiente Dataverse existente
1. Certifique-se de que o ambiente não foi configurado com [escrita dupla](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview) já que a instalação irá então instalar as capacidades do [Project Operations para cenários baseados em recursos/sem stock](project-operations-integrated-deployment-overview.md).
2. Como [Administrador Global ou do Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) com uma licença do Project Operations, localize o ambiente no [Centro de administração do PowerPlatform](https://admin.powerplatform.com) onde pretende instalar o Project Operations.
3. Instale o **Microsoft Dynamics 365 Project Operations** da lista de implementação de aplicações do Dynamics 365. Para mais informações, consulte [Gerir Aplicações do Dynamics 365](/power-platform/admin/manage-apps).




[!INCLUDE[footer-include](../includes/footer-banner.md)]
