---
title: Implementar o Project Operations – lite
description: Este tópico fornece informações sobre como instalar a implementação do Project Operations lite - oportunidade potencial para fatura pró-forma.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 2470d573f4537cb22de4dbd98caff148cbe0bda3
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950278"
---
# <a name="deploy-project-operations---lite"></a><span data-ttu-id="a12be-103">Implementar o Project Operations – lite</span><span class="sxs-lookup"><span data-stu-id="a12be-103">Deploy Project Operations - lite</span></span>

<span data-ttu-id="a12be-104">_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_</span><span class="sxs-lookup"><span data-stu-id="a12be-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="a12be-105">O Project Operations suporta vários modelos de implementação.</span><span class="sxs-lookup"><span data-stu-id="a12be-105">Project Operations supports multiple deployment models.</span></span> <span data-ttu-id="a12be-106">Para determinar o melhor modelo de implementação, consulte [Tipo de implementação](determine-deployment-type.md).</span><span class="sxs-lookup"><span data-stu-id="a12be-106">To determine the best deployment model, see [Deployment types](determine-deployment-type.md).</span></span>


> [!IMPORTANT]
> <span data-ttu-id="a12be-107">Esta implementação, Implementação leve - oportunidade potencial para fatura pró-forma, resulta numa **Implementação só do Common Data Service do Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="a12be-107">This deployment, Lite deployment – deal to proforma invoicing, results in a **Common Data Service-only deployment of Project Operations**.</span></span>

- [<span data-ttu-id="a12be-108">Instalar o Project Operations num novo ambiente do CDS</span><span class="sxs-lookup"><span data-stu-id="a12be-108">Install Project Operations into a new CDS environment</span></span>](#new)
- [<span data-ttu-id="a12be-109">Instalar num ambiente do CDS existente</span><span class="sxs-lookup"><span data-stu-id="a12be-109">Install into an existing CDS environment</span></span>](#existing)



## <a name="install-project-operations-to-a-new-cds-environment"></a><a name="new"></a><span data-ttu-id="a12be-110">Instalar o Project Operations num novo ambiente do CDS</span><span class="sxs-lookup"><span data-stu-id="a12be-110">Install Project Operations to a new CDS environment</span></span>

1. <span data-ttu-id="a12be-111">Como [Administrador Global ou Administrador do Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) com uma licença do Project Operations, crie um novo ambiente do CDS no [Centro de administração do PowerPlatform](https://admin.powerplatform.com).</span><span class="sxs-lookup"><span data-stu-id="a12be-111">As the [Global or Power Platform Administrator](/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, create a new CDS environment in the [PowerPlatform admin center](https://admin.powerplatform.com).</span></span> <span data-ttu-id="a12be-112">Certifique-se de que a **Base de dados do CDS** e **Aplicações do Dynamics 365** estão ativados.</span><span class="sxs-lookup"><span data-stu-id="a12be-112">Make sure that **CDS database** and **Dynamics 365 Apps** are enabled.</span></span> <span data-ttu-id="a12be-113">Para mais informações, consulte [Criar e gerir ambientes no Centro de administração do Power Platform](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span><span class="sxs-lookup"><span data-stu-id="a12be-113">For more information, see [Create and manage environments in the Power Platform admin center](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span></span>
2. <span data-ttu-id="a12be-114">Selecione **Microsoft Dynamics 365 Project Operations** da lista de implementação de aplicações do Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="a12be-114">Select **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span>


## <a name="install-project-operations-to-an-existing-cds-environment"></a><a name="existing"></a><span data-ttu-id="a12be-115">Instalar o Project Operations num ambiente do CDS existente</span><span class="sxs-lookup"><span data-stu-id="a12be-115">Install Project Operations to an existing CDS environment</span></span>

1. <span data-ttu-id="a12be-116">Como [Administrador Global ou do Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) com uma licença do Project Operations, localize o ambiente no [Centro de administração do PowerPlatform](https://admin.powerplatform.com) onde pretende instalar o Project Operations.</span><span class="sxs-lookup"><span data-stu-id="a12be-116">As the [Global or Power Platform Administrator](/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, locate the environment in the [PowerPlatform admin center](https://admin.powerplatform.com) where you want to install Project Operations.</span></span>
2. <span data-ttu-id="a12be-117">Instale o **Microsoft Dynamics 365 Project Operations** da lista de implementação de aplicações do Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="a12be-117">Install **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span> <span data-ttu-id="a12be-118">Para mais informações, consulte [Gerir Aplicações do Dynamics 365](/power-platform/admin/manage-apps).</span><span class="sxs-lookup"><span data-stu-id="a12be-118">For more information, see [Manage Dynamics 365 apps](/power-platform/admin/manage-apps).</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]