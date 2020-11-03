---
title: Configurar recursos do projeto
description: Este tópico fornece informações sobre configurar ou pedir recursos de projeto.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7eec8ad5d78019219b2e04ca75eeaa5a3c8a748f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082576"
---
# <a name="set-up-project-resources"></a><span data-ttu-id="e9aae-103">Configurar recursos do projeto</span><span class="sxs-lookup"><span data-stu-id="e9aae-103">Set up project resources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e9aae-104">Tem de configurar um calendário e associá-lo a um empregado ou a um trabalhador.</span><span class="sxs-lookup"><span data-stu-id="e9aae-104">You must set up a calendar and associate it with an employee or a worker.</span></span> <span data-ttu-id="e9aae-105">O calendário é utilizado para agendar o projeto e o tempo de trabalho dos recursos que estão reservados para o projeto.</span><span class="sxs-lookup"><span data-stu-id="e9aae-105">The calendar is used to schedule the project and the working time of the resources that are reserved for the project.</span></span> <span data-ttu-id="e9aae-106">Durante a configuração do calendário, os gestores de projetos podem nivelar os recursos como parte da otimização dos recursos.</span><span class="sxs-lookup"><span data-stu-id="e9aae-106">During calendar setup, project managers can do resource leveling as part of resource optimization.</span></span> <span data-ttu-id="e9aae-107">Baseado na agenda do calendário, podem ser colocadas restrições nos recursos.</span><span class="sxs-lookup"><span data-stu-id="e9aae-107">Based on the calendar schedule, restrictions can be put on resources.</span></span> <span data-ttu-id="e9aae-108">Pode configurar um calendário na página **Calendários**.</span><span class="sxs-lookup"><span data-stu-id="e9aae-108">You can set up a calendar on the **Calendars** page.</span></span>

<span data-ttu-id="e9aae-109">Quando configura um trabalhador como um recurso do projeto, pode selecionar entre os trabalhadores que trabalham na empresa para a qual está a configurar recursos.</span><span class="sxs-lookup"><span data-stu-id="e9aae-109">When you set up a worker as a project resource, you can select from workers who work in the company that you're setting up resources for.</span></span> <span data-ttu-id="e9aae-110">Em alternativa, poderá selecionar trabalhadores de outras empresas na sua organização.</span><span class="sxs-lookup"><span data-stu-id="e9aae-110">Alternatively, you can select workers from other companies in your organization.</span></span> <span data-ttu-id="e9aae-111">Estes trabalhadores são conhecidos como recursos entre empresas.</span><span class="sxs-lookup"><span data-stu-id="e9aae-111">These workers are known as intercompany resources.</span></span>

<span data-ttu-id="e9aae-112">Os seguintes procedimentos explicam como configurar um trabalhador como recurso de projeto na sua empresa e como configurar um recurso de projeto entre empresas.</span><span class="sxs-lookup"><span data-stu-id="e9aae-112">The following procedures explain how to set up a worker as a project resource in your company and how to set up an intercompany project resource.</span></span>

## <a name="set-up-a-worker-as-a-project-resource"></a><span data-ttu-id="e9aae-113">Configurar um trabalhador como recurso do projeto</span><span class="sxs-lookup"><span data-stu-id="e9aae-113">Set up a worker as a project resource</span></span>

1. <span data-ttu-id="e9aae-114">Na página **Trabalhadores** , na lista **Trabalhadores** , selecione o trabalhador que está a adicionar como recurso do projeto e abra o registo do trabalhador.</span><span class="sxs-lookup"><span data-stu-id="e9aae-114">On the **Workers** page, in the **Workers** list, select the worker that you're adding as a project resource, and open the worker record.</span></span>
2. <span data-ttu-id="e9aae-115">No Painel de Ação, selecione **Projeto** &gt; **Configurar** &gt; **Configuração do projeto**.</span><span class="sxs-lookup"><span data-stu-id="e9aae-115">On the Action Pane, select **Project** &gt; **Setup** &gt; **Project setup**.</span></span>
3. <span data-ttu-id="e9aae-116">Selecione um calendário e, em seguida, feche a página.</span><span class="sxs-lookup"><span data-stu-id="e9aae-116">Select a calendar, and then close the page.</span></span>

<span data-ttu-id="e9aae-117">Também pode especificar projetos predefinidos para um recurso como um tipo de pré-atribuição.</span><span class="sxs-lookup"><span data-stu-id="e9aae-117">You can also specify default projects for a resource as a type of pre-assignment.</span></span> <span data-ttu-id="e9aae-118">As pré-atribuições podem ser utilizadas quando o gestor de recursos ou o gestor de projetos sabe antecipadamente em que projetos o recurso irá trabalhar.</span><span class="sxs-lookup"><span data-stu-id="e9aae-118">Pre-assignments can be used when the resource manager or project manager knows which projects the resource will be working on in advance.</span></span> <span data-ttu-id="e9aae-119">As pré-atribuições também podem basear-se no pedido de um patrocinador ou cliente do projeto.</span><span class="sxs-lookup"><span data-stu-id="e9aae-119">Pre-assignments can also be based on the request of a project sponsor or customer.</span></span> <span data-ttu-id="e9aae-120">Para pré-atribuir um projeto, na página **Atribuir projetos** , no separador **Projetos** , na lista **Projetos restantes** , selecione o projeto adequado.</span><span class="sxs-lookup"><span data-stu-id="e9aae-120">To pre-assign a project, on the **Assign projects** page, on the **Projects** tab, in the **Remaining projects** list, select the appropriate project.</span></span>

## <a name="set-up-an-intercompany-resource"></a><span data-ttu-id="e9aae-121">Configurar um recurso entre empresas</span><span class="sxs-lookup"><span data-stu-id="e9aae-121">Set up an intercompany resource</span></span>

<span data-ttu-id="e9aae-122">Quando configura um trabalhador como um recurso entre empresas, tem de concluir a configuração tanto na empresa prestadora como na empresa tomadora.</span><span class="sxs-lookup"><span data-stu-id="e9aae-122">When you set up a worker as an intercompany resource, you must complete the setup in both the lending company and the borrowing company.</span></span>

### <a name="in-the-lending-company"></a><span data-ttu-id="e9aae-123">Na empresa prestadora</span><span class="sxs-lookup"><span data-stu-id="e9aae-123">In the lending company</span></span>

1. <span data-ttu-id="e9aae-124">No Finance, verifique se a empresa prestadora está selecionada e, em seguida, conclua o procedimento na secção anterior: "Configurar um trabalhador como recurso do projeto".</span><span class="sxs-lookup"><span data-stu-id="e9aae-124">In Finance, verify that the lending company is selected, and then complete the procedure in the previous section, "Set up a worker as a project resource."</span></span>
2. <span data-ttu-id="e9aae-125">Na página **Gestão contabilística entre empresas** , selecione **Novo**.</span><span class="sxs-lookup"><span data-stu-id="e9aae-125">On the **Intercompany accounting** page, select **New**.</span></span>
3. <span data-ttu-id="e9aae-126">No campo **ID da entidade jurídica** , selecione a empresa prestadora.</span><span class="sxs-lookup"><span data-stu-id="e9aae-126">In the **Legal entity ID** field, select the lending company.</span></span> <span data-ttu-id="e9aae-127">Preencha os campos restantes conforme adequado e, em seguida, selecione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="e9aae-127">Fill in the remaining fields as appropriate, and then select **Save**.</span></span>
4. <span data-ttu-id="e9aae-128">Na página **Preço de transferência** , selecione **Novo**.</span><span class="sxs-lookup"><span data-stu-id="e9aae-128">On the **Transfer price** page, select **New**.</span></span>
5. <span data-ttu-id="e9aae-129">No campo **Entidade jurídica tomadora** , selecione a empresa adequada.</span><span class="sxs-lookup"><span data-stu-id="e9aae-129">In the **Borrowing legal entity** field, select the appropriate company.</span></span>
6. <span data-ttu-id="e9aae-130">Para emprestar à empresa tomadora apenas o recurso que criou no início desta secção, no campo **Recurso** , selecione o nome do recurso que criou.</span><span class="sxs-lookup"><span data-stu-id="e9aae-130">To lend the borrowing company only the resource that you created at the beginning of this section, in the **Resource** field, select the name of the resource that you created.</span></span> <span data-ttu-id="e9aae-131">Para disponibilizar todos os recursos na empresa prestadora à empresa tomadora, deixe o campo **Recursos** em branco.</span><span class="sxs-lookup"><span data-stu-id="e9aae-131">To make all resources in the lending company available to the borrowing company, leave the **Resource** field blank.</span></span>
7. <span data-ttu-id="e9aae-132">Na página **Parâmetros da gestão de projetos e contabilística** , no separador **Entre empresas** , defina a opção **Ativar as folhas de horas e o agendamento de recursos entre empresas** para **Sim**.</span><span class="sxs-lookup"><span data-stu-id="e9aae-132">On the **Project management and accounting parameters** page, on the **Intercompany** tab, set the **Enable intercompany resource scheduling and timesheets** option to **Yes**.</span></span>

### <a name="in-the-borrowing-company"></a><span data-ttu-id="e9aae-133">Na empresa tomadora</span><span class="sxs-lookup"><span data-stu-id="e9aae-133">In the borrowing company</span></span>

- <span data-ttu-id="e9aae-134">Na página **Lista de recursos** , no filtro de pesquisa, insira o nome do recurso que criou para a empresa prestadora para verificar se o nome está incluído na lista de recursos da empresa tomadora.</span><span class="sxs-lookup"><span data-stu-id="e9aae-134">On the **Resources list** page, in the search filter, enter the name of the resource that you created for the lending company, to verify that the name is included in the resource list for the borrowing company.</span></span>

## <a name="request-project-resources"></a><span data-ttu-id="e9aae-135">Pedir recursos de projeto</span><span class="sxs-lookup"><span data-stu-id="e9aae-135">Request project resources</span></span>
<span data-ttu-id="e9aae-136">A funcionalidade para o agendamento de recursos do projeto só permite que os gestores de recursos distribuam recursos com pessoal em compromissos ou projetos.</span><span class="sxs-lookup"><span data-stu-id="e9aae-136">The functionality for project resource scheduling only lets resource managers distribute staffed resources on engagements or projects.</span></span> <span data-ttu-id="e9aae-137">Para ativar esta funcionalidade, execute as seguintes tarefas ou verifique se foram concluídas:</span><span class="sxs-lookup"><span data-stu-id="e9aae-137">To enable this functionality, complete the following tasks, or verify that they have been completed:</span></span>

- <span data-ttu-id="e9aae-138">Configurar sequências de números.</span><span class="sxs-lookup"><span data-stu-id="e9aae-138">Set up number sequences.</span></span>
- <span data-ttu-id="e9aae-139">Configurar os fluxos de trabalho de gestão de projetos e contabilística.</span><span class="sxs-lookup"><span data-stu-id="e9aae-139">Set up project management and accounting workflows.</span></span>
- <span data-ttu-id="e9aae-140">Ativar os fluxos de trabalho de pedido de recursos.</span><span class="sxs-lookup"><span data-stu-id="e9aae-140">Enable resource request workflows.</span></span>

<span data-ttu-id="e9aae-141">Após a conclusão das tarefas anteriores, pode concluir as seguintes tarefas, conforme necessário:</span><span class="sxs-lookup"><span data-stu-id="e9aae-141">After the preceding tasks have been completed, you can complete the following tasks as you require:</span></span>

- <span data-ttu-id="e9aae-142">Criar um pedido de recurso a partir de um recurso com pessoal com reserva flexível.</span><span class="sxs-lookup"><span data-stu-id="e9aae-142">Create a resource request from a soft-booked staffed resource.</span></span>
- <span data-ttu-id="e9aae-143">Monitorizar pedidos de recursos.</span><span class="sxs-lookup"><span data-stu-id="e9aae-143">Monitor resource requests.</span></span>
- <span data-ttu-id="e9aae-144">Executar pedidos de recursos.</span><span class="sxs-lookup"><span data-stu-id="e9aae-144">Fulfill resource requests.</span></span>
- <span data-ttu-id="e9aae-145">Pedir um recurso com pessoal de uma WBS.</span><span class="sxs-lookup"><span data-stu-id="e9aae-145">Request a staffed resource from a WBS.</span></span>
- <span data-ttu-id="e9aae-146">ReservAr recursos para um projeto sem ter um pedido de recurso com pessoal.</span><span class="sxs-lookup"><span data-stu-id="e9aae-146">Book resources to a project without having a request for a staffed resource.</span></span>
