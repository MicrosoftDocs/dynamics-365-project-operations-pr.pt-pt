---
title: Descrição geral do Project Service Automation
description: Este tópico fornece informações sobre a solução de integração do Dynamics 365 Project Service Automation com o Dynamics 365 Finance.
author: ruhercul
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: ruhercul
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9ccbb29d5035ea061d232011af87cef2c81e76c
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642467"
---
# <a name="project-service-automation-overview"></a><span data-ttu-id="ef04f-103">Descrição geral do Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="ef04f-103">Project Service Automation overview</span></span>

[!include[banner](../includes/banner.md)]
[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="ef04f-104">A solução de integração do Project Service Automation para Finance utiliza a funcionalidade Integração de Dados para sincronizar os dados entre instâncias do Dynamics 365 Finance e do Dynamics 365 Project Service Automation via Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="ef04f-104">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Dynamics 365 Finance and Dynamics 365 Project Service Automation via Common Data Service.</span></span> <span data-ttu-id="ef04f-105">Os modelos de integração disponíveis com a funcionalidade Integração de dados permitem o fluxo de projetos, contratos de projetos, projetos, itens de contrato do projeto, marcos de itens de contrato do projeto, tarefas do projeto, categorias de transações de despesas, estimativas de horas e estimativas de despesa do Project Service Automation para o Finance.</span><span class="sxs-lookup"><span data-stu-id="ef04f-105">The integration templates that are available with the Data integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="ef04f-106">Se estiver a utilizar a versão 7.3.0, tem de instalar o KB 4074835.</span><span class="sxs-lookup"><span data-stu-id="ef04f-106">If you're using version 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="ef04f-107">Em seguida, poderá integrar projetos de preço fixo.</span><span class="sxs-lookup"><span data-stu-id="ef04f-107">You will then be able to integrate fixed price projects.</span></span>
> - <span data-ttu-id="ef04f-108">Se estiver a utilizar a versão 7.3.0 e estiver a transferir transações de tarifas a partir do Project Service Automation, terá de instalar o KB 4345320 para incluir essas tarifas na fatura do projeto.</span><span class="sxs-lookup"><span data-stu-id="ef04f-108">If you're using version 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="ef04f-109">Se estiver a utilizar a versão 8.0, poderá utilizar a integração de tarefas do projeto, as categorias de transações de despesas, as estimativas de horas, as estimativas de despesas e o bloqueio de funcionalidades.</span><span class="sxs-lookup"><span data-stu-id="ef04f-109">If you're using version 8.0, you will be able to use project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
> - <span data-ttu-id="ef04f-110">Se estiver a utilizar a versão 8.0.1 ou posterior, poderá sincronizar os valores reais.</span><span class="sxs-lookup"><span data-stu-id="ef04f-110">If you're using version 8.0.1 or later, you will be able to synchronize actuals.</span></span>

<span data-ttu-id="ef04f-111">Antes de poder integrar o Project Service Automation Finance, tem de configurar os parâmetros de integração do Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="ef04f-111">Before you can integrate Project Service Automation Finance, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="ef04f-112">Pata mais informações, consulte [Parâmetros de integração do Project Service Automation](PSA-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="ef04f-112">For more information, see [Project Service Automation integration parameters](PSA-parameters.md).</span></span>

<span data-ttu-id="ef04f-113">Esta solução de integração permite a sincronização direta nos seguintes cenários:</span><span class="sxs-lookup"><span data-stu-id="ef04f-113">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="ef04f-114">Mantenha os contratos do projeto no Project Service Automation e sincronize-os diretamente do Project Service Automation para o Finance.</span><span class="sxs-lookup"><span data-stu-id="ef04f-114">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="ef04f-115">Crie projetos no Project Service Automation e sincronize-os diretamente do Project Service Automation para o Finance.</span><span class="sxs-lookup"><span data-stu-id="ef04f-115">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="ef04f-116">Mantenha os itens de contrato do projeto no Project Service Automation e sincronize-os diretamente do Project Service Automation para o Finance.</span><span class="sxs-lookup"><span data-stu-id="ef04f-116">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="ef04f-117">Mantenha os marcos de itens de contrato do projeto no Project Service Automation e sincronize-os diretamente do Project Service Automation para o Finance.</span><span class="sxs-lookup"><span data-stu-id="ef04f-117">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="ef04f-118">Mantenha as tarefas do projeto no Project Service Automation e sincronize-os diretamente do Project Service Automation para o Finance.</span><span class="sxs-lookup"><span data-stu-id="ef04f-118">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="ef04f-119">Mantenha as categorias de transações de despesas no Finance e sincronize-os diretamente do Finance para o Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="ef04f-119">Maintain expense transaction categories in Finance, and synchronize them directly from Finance to Project Service Automation.</span></span>
- <span data-ttu-id="ef04f-120">Crie estimativas de horas do projeto Project Service Automation e sincronize-as diretamente do Project Service Automation para o Finance.</span><span class="sxs-lookup"><span data-stu-id="ef04f-120">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="ef04f-121">Crie estimativas de despesa do projeto Project Service Automation e sincronize-as diretamente do Project Service Automation para o Finance.</span><span class="sxs-lookup"><span data-stu-id="ef04f-121">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="ef04f-122">Crie dados reais de tempo, despesa e tarifas no Project Service Automation, e crie transações do projeto no diário de integração do Project Service Automation para poderem ser lançados no Finance.</span><span class="sxs-lookup"><span data-stu-id="ef04f-122">Create project time, expense, and fee actuals in Project Service Automation, and create project transactions in the Project Service Automation integration journal so that they can be posted in Finance.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="ef04f-123">Sincronização de dados</span><span class="sxs-lookup"><span data-stu-id="ef04f-123">Data synchronization</span></span>

<span data-ttu-id="ef04f-124">A seguinte ilustração mostra como os dados são sincronizados como parte da integração entre o Project Service Automation e o Finance.</span><span class="sxs-lookup"><span data-stu-id="ef04f-124">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance.</span></span>

> [!NOTE]
> <span data-ttu-id="ef04f-125">Nem todos os modelos estão disponíveis atualmente.</span><span class="sxs-lookup"><span data-stu-id="ef04f-125">Not all templates are currently available.</span></span> <span data-ttu-id="ef04f-126">Os modelos serão lançados à medida que forem concluídos.</span><span class="sxs-lookup"><span data-stu-id="ef04f-126">Templates will be released as they are completed.</span></span>

<span data-ttu-id="ef04f-127">[![Integração do Project Service Automation com o Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="ef04f-127">[![Project Service Automation integration with Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance"></a><span data-ttu-id="ef04f-128">Requisitos doe sistema para o Finance</span><span class="sxs-lookup"><span data-stu-id="ef04f-128">System requirements for Finance</span></span>

<span data-ttu-id="ef04f-129">Para utilizar a solução de integração do Project Service Automation para o Finance, tem de instalar o Enterprise edition 7.3 com Platform update 12 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="ef04f-129">To use the Project Service Automation to Finance integration solution, you must install Enterprise edition 7.3 with Platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="ef04f-130">Requisitos de sistema para o Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="ef04f-130">System requirements for Project Service Automation</span></span>

<span data-ttu-id="ef04f-131">Para utilizar a solução de integração do Project Service Automation para o Finance, tem de instalar os seguintes componentes:</span><span class="sxs-lookup"><span data-stu-id="ef04f-131">To use the Project Service Automation to Finance integration solution, you must install the following components:</span></span>

- <span data-ttu-id="ef04f-132">Dynamics 365 Project Service Automation versão 9.0.0.0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="ef04f-132">Dynamics 365 Project Service Automation version 9.0.0.0 or later</span></span>
- <span data-ttu-id="ef04f-133">Solução de perspetiva de venda para o Dynamics 365 Sales, versão 1.14.0.0 (v14) ou posterior</span><span class="sxs-lookup"><span data-stu-id="ef04f-133">Prospect to cash solution for Dynamics 365 Sales, version 1.14.0.0 (v14) or later</span></span>
- <span data-ttu-id="ef04f-134">Solução Project Service Automation para Finance para o Dynamics 365 Project Service Automation versão 1.0.0.0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="ef04f-134">Project Service Automation to Finance solution for Dynamics 365 Project Service Automation version 1.0.0.0 or later</span></span>

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="ef04f-135">Instalar a solução de integração Project Service Automation para Finance na sua instância do Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="ef04f-135">Install the Project Service Automation to Finance integration solution in your Project Service Automation instance</span></span>

<span data-ttu-id="ef04f-136">Transfira a solução de integração Project Service Automation para Finance a partir do [Centro de Transferências da Microsoft](https://www.microsoft.com/download/details.aspx?id=57016) e siga as instruções incluídas com a solução.</span><span class="sxs-lookup"><span data-stu-id="ef04f-136">Download the Project Service Automation to Finance integration solution from [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016), and follow the instructions that are included with the solution.</span></span>
