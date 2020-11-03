---
title: Desempenho do agendamento de recursos do projeto
description: Este tópico fornece informações sobre como melhorar o desempenho do agendamento de recursos para um grande número de projetos.
author: Yowelle
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: c3f219ce0635545976a6a4639233f166e18468af
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082387"
---
# <a name="project-resource-scheduling-performance"></a><span data-ttu-id="21c4a-103">Desempenho do agendamento de recursos do projeto</span><span class="sxs-lookup"><span data-stu-id="21c4a-103">Project resource scheduling performance</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


<span data-ttu-id="21c4a-104">Os problemas de desempenho relacionadas com o agendamento de recursos podem ocorrer quando o número de projetos chega aos milhares.</span><span class="sxs-lookup"><span data-stu-id="21c4a-104">Performance issues related to resource scheduling can occur when the number of projects reaches into the thousands.</span></span> <span data-ttu-id="21c4a-105">Para melhorar o desempenho do agendamento de recursos, existe uma funcionalidade que permite aos utilizadores reduzir o tempo que demora a iniciar o formulário de disponibilidade de recursos.</span><span class="sxs-lookup"><span data-stu-id="21c4a-105">To improve resource scheduling performance, a feature is available that allows users to reduce the time that it takes to launch the resource availability form.</span></span> <span data-ttu-id="21c4a-106">Especificamente, isto remove o processo de sincronização de roll-up de capacidade de recursos e utiliza a tabela **ResProjectResource** para acelerar a procura de recursos.</span><span class="sxs-lookup"><span data-stu-id="21c4a-106">Specifically, this removes the resource capacity roll-up synchronization process and uses the **ResProjectResource** table to speed up the resource lookup.</span></span> <span data-ttu-id="21c4a-107">Note que a tabela **ResRollup** deixará de ser utilizada.</span><span class="sxs-lookup"><span data-stu-id="21c4a-107">Note that the **ResRollup** table will no longer be used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="21c4a-108">Se houver uma dependência do processo de sincronização da capacidade de recursos ou da tabela **ResProjectResource** , não utilize esta funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="21c4a-108">If there is a dependency on either the resource capacity roll-up synchronization process or the **ResProjectResource** table, do not use this feature.</span></span>

## <a name="enable-resource-scheduling-performance-enhancement"></a><span data-ttu-id="21c4a-109">Ativar a melhoria do desempenho do agendamento de recursos</span><span class="sxs-lookup"><span data-stu-id="21c4a-109">Enable resource scheduling performance enhancement</span></span>
<span data-ttu-id="21c4a-110">Para ativar o melhoramento do desempenho do agendamento de recursos, complete os seguintes passos.</span><span class="sxs-lookup"><span data-stu-id="21c4a-110">To enable resource scheduling performance enhancement, complete the following steps.</span></span>

1. <span data-ttu-id="21c4a-111">Vá a **Gestão de funcionalidades** > **Todas** e, na lista de funcionalidades, localize **Ativar a funcionalidade de melhoria do desempenho de agendamento de recursos do projeto**.</span><span class="sxs-lookup"><span data-stu-id="21c4a-111">Go to **Feature management** > **All** , and in the feature list, locate **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="21c4a-112">Selecione **Ativar agora**.</span><span class="sxs-lookup"><span data-stu-id="21c4a-112">Select **Enable now**.</span></span>

> [!NOTE]
> <span data-ttu-id="21c4a-113">Se não conseguir encontrar a funcionalidade na lista, selecione **Verificar se há atualizações** para atualizar a lista.</span><span class="sxs-lookup"><span data-stu-id="21c4a-113">If you can't find the feature in the list, select **Check for updates** to refresh the list.</span></span>

3. <span data-ttu-id="21c4a-114">Atualize o seu browser e, em seguida, vá para **Gestão de projetos e contabilística** > **Periódico** > **Recursos do projeto** > **Sincronizar a capacidade dos calendários de recursos em todas as empresas**.</span><span class="sxs-lookup"><span data-stu-id="21c4a-114">Refresh your browser, and then go to **Project management and accounting** > **Periodic** > **Project resources** > **Synchronize resource calendars capacity across all companies**.</span></span>
4. <span data-ttu-id="21c4a-115">Defina **Remover registos de capacidade existentes** como **Sim** para remover dados anteriores.</span><span class="sxs-lookup"><span data-stu-id="21c4a-115">Set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="21c4a-116">Se pretender gerar dados incrementais, defina-o para **Não**.</span><span class="sxs-lookup"><span data-stu-id="21c4a-116">If you want generate incremental data, set it to **No**.</span></span>
5. <span data-ttu-id="21c4a-117">No campo **Código de período** , selecione o período em que os dados devem ser gerados.</span><span class="sxs-lookup"><span data-stu-id="21c4a-117">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="21c4a-118">Se selecionar um código de período, não é necessário definir uma data de início e de fim.</span><span class="sxs-lookup"><span data-stu-id="21c4a-118">If you select a period code, a start and end date do not need to be defined.</span></span>
6. <span data-ttu-id="21c4a-119">Se deixar o campo **Código de período** em branco, selecione datas específicas de início e de fim para gerar dados.</span><span class="sxs-lookup"><span data-stu-id="21c4a-119">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
7. <span data-ttu-id="21c4a-120">Selecione **OK**.</span><span class="sxs-lookup"><span data-stu-id="21c4a-120">Select **OK**.</span></span>

 > [!NOTE]
 > <span data-ttu-id="21c4a-121">Isto irá distribuir dados gerais para a tabela **ResCalendarCapacity** em todas as empresas do seu ambiente, pelo que a tarefa de lote só precisa de ser executado numa entidade legal.</span><span class="sxs-lookup"><span data-stu-id="21c4a-121">This will distribute general data to the **ResCalendarCapacity** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="21c4a-122">Os dados nesta tarefa de lote são necessários para calcular a capacidade de recursos através do calendário associado.</span><span class="sxs-lookup"><span data-stu-id="21c4a-122">The data in this batch job is needed to calculate resource capacity through the associated calendar.</span></span>

8. <span data-ttu-id="21c4a-123">Vá à **Gestão de projetos e contabilística** > **Periódico** > **Recursos do projeto** > **Preencher recursos do projeto em todas as empresas** e, em seguida, selecione **OK**.</span><span class="sxs-lookup"><span data-stu-id="21c4a-123">Go to **Project management and accounting** > **Periodic** > **Project resources** > **Populate project resources across all companies** and then select **OK**.</span></span> <span data-ttu-id="21c4a-124">Este é o script de atualização de versão dos dados para dados gerais nas tabelas **ResProjectResource** , **ResCalendarDateTimeRange** e **ResEffectiveDateTimeRange**.</span><span class="sxs-lookup"><span data-stu-id="21c4a-124">This is the data upgrade script for general data in the **ResProjectResource** , **ResCalendarDateTimeRange** , and **ResEffectiveDateTimeRange** tables.</span></span> <span data-ttu-id="21c4a-125">Os valores para o campo **PSAPRojSchedRole.RootActivity** também são atualizados.</span><span class="sxs-lookup"><span data-stu-id="21c4a-125">Values for the **PSAPRojSchedRole.RootActivity** field are also updated.</span></span> <span data-ttu-id="21c4a-126">Se isto não for executado, receberá um aviso quando tentar executar operações de agendamento de recursos.</span><span class="sxs-lookup"><span data-stu-id="21c4a-126">If this is not run, you will receive a warning when you try to execute resource scheduling operations.</span></span>
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a><span data-ttu-id="21c4a-127">Desativar a melhoria do desempenho do agendamento de recursos</span><span class="sxs-lookup"><span data-stu-id="21c4a-127">Turn off resource scheduling performance enhancement</span></span>

1. <span data-ttu-id="21c4a-128">Vá a **Gestão de funcionalidades** > **Todas** e procure por **Ativar a funcionalidade de melhoria do desempenho de agendamento de recursos do projeto**.</span><span class="sxs-lookup"><span data-stu-id="21c4a-128">Go to **Feature management** > **All**  and search for **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="21c4a-129">Selecione a funcionalidade e, em seguida, selecione o botão **Desativar**.</span><span class="sxs-lookup"><span data-stu-id="21c4a-129">Select the feature, and then select the **Disable** button.</span></span>
3. <span data-ttu-id="21c4a-130">Atualize o seu browser.</span><span class="sxs-lookup"><span data-stu-id="21c4a-130">Refresh your browser.</span></span>
4. <span data-ttu-id="21c4a-131">Aceda a **Gestão de projetos e contabilística** > **Periódico** > **Sincronização da capacidade** > **Sincronizar roll-ups de capacidade dos recursos**.</span><span class="sxs-lookup"><span data-stu-id="21c4a-131">Go to **Project management and accounting** > **Periodic** > **Capacity synchronization** > **Synchronize resource capacity roll-ups**.</span></span>
5. <span data-ttu-id="21c4a-132">Na página **Sincronização de roll-up de capacidade** , defina **Remover registos de capacidade existentes** como **Sim** para remover dados anteriores.</span><span class="sxs-lookup"><span data-stu-id="21c4a-132">On the **Capacity roll-up synchronization** page, set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="21c4a-133">Se pretender gerar dados incrementais, defina-o para **Não**.</span><span class="sxs-lookup"><span data-stu-id="21c4a-133">If you want to generate incremental data, set it to **No**.</span></span>
6. <span data-ttu-id="21c4a-134">No campo **Código de período** , selecione o período em que os dados devem ser gerados.</span><span class="sxs-lookup"><span data-stu-id="21c4a-134">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="21c4a-135">Se selecionar um código de período, não é necessário definir uma data de início e de fim.</span><span class="sxs-lookup"><span data-stu-id="21c4a-135">If you select a period code, a start and end date do not need to be defined.</span></span>
7. <span data-ttu-id="21c4a-136">Se deixar o campo **Código de período** em branco, selecione datas específicas de início e de fim para gerar dados.</span><span class="sxs-lookup"><span data-stu-id="21c4a-136">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
8. <span data-ttu-id="21c4a-137">Selecione **OK**.</span><span class="sxs-lookup"><span data-stu-id="21c4a-137">Select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="21c4a-138">Isto irá distribuir dados gerais para a tabela **ResRollup** em todas as empresas do seu ambiente, pelo que a tarefa de lote só precisa de ser executado numa entidade legal.</span><span class="sxs-lookup"><span data-stu-id="21c4a-138">This will distribute general data to the **ResRollup** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="21c4a-139">Esta tarefa de lote é necessária para todas as vistas **Disponibilidade de Recursos**.</span><span class="sxs-lookup"><span data-stu-id="21c4a-139">This batch job is needed for all **Resource Availability** views.</span></span> <span data-ttu-id="21c4a-140">Se esta tarefa de lote não for executada, os dados **ResRollup** serão gerados no momento, o que pode levar tempo.</span><span class="sxs-lookup"><span data-stu-id="21c4a-140">If this batch job is not run, the **ResRollup** data will be generated on the fly, which can take time.</span></span>
