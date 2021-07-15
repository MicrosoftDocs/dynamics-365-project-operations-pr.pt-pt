---
title: Integração com o Microsoft Project Client
description: Planear e manter uma agenda de projetos pode ser complexo, pelo que os gestores de projetos precisam de utilizar ferramentas que os ajudem a gerir esta tarefa. A integração com o Microsoft Project Client fornece suporte para abrir e gerir uma estrutura hierárquica do trabalho do projeto.
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: b312ec5b1f4e6a98a2cbf1667b2f55b758b2d613
ms.sourcegitcommit: 3a4b181be08ef0428104d72b54a3e61ac2782f14
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/17/2021
ms.locfileid: "6269849"
---
# <a name="microsoft-project-client-integration"></a><span data-ttu-id="205bf-104">Integração com o Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="205bf-104">Microsoft Project client integration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="205bf-105">Planear e manter uma agenda de projetos pode ser complexo, pelo que os gestores de projetos precisam de utilizar ferramentas que os ajudem a gerir esta tarefa.</span><span class="sxs-lookup"><span data-stu-id="205bf-105">Planning and maintaining a project schedule can be complex, so project managers need to use tools that help them manage this task.</span></span> <span data-ttu-id="205bf-106">A integração com o Microsoft Project Client fornece suporte para abrir e gerir uma estrutura hierárquica do trabalho do projeto.</span><span class="sxs-lookup"><span data-stu-id="205bf-106">Integration with Microsoft Project Client provides support to open and manage a project work breakdown structure.</span></span> <span data-ttu-id="205bf-107">O gestor de projetos pode lançar quaisquer alterações de volta à estrutura hierárquica do trabalho do projeto do Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="205bf-107">The project manager can publish any changes back to the Dynamics 365 Finance project work breakdown structure.</span></span>

> [!NOTE]
> <span data-ttu-id="205bf-108">Se estiver a utilizar a atualização de julho (versão 10.0.4), tem de instalar o KB 4054797 e KB 4055884.</span><span class="sxs-lookup"><span data-stu-id="205bf-108">If you are using the July update (version 10.0.4), you must install KB 4054797 and 4055884.</span></span>

## <a name="configure-the-microsoft-project-client-add-in"></a><span data-ttu-id="205bf-109">Configurar o suplemento do Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="205bf-109">Configure the Microsoft Project Client add-in</span></span>
<span data-ttu-id="205bf-110">Para ativar a integração com o Microsoft Project Client, é necessário instalar um suplemento do Microsoft Dynamics 365 na aplicação Microsoft Project Client do utilizador.</span><span class="sxs-lookup"><span data-stu-id="205bf-110">To enable the integration with Microsoft Project Client, a Microsoft Dynamics 365 add-in is required to be installed in the user’s client Microsoft Project application.</span></span> <span data-ttu-id="205bf-111">Isto é feito ao abrir a **Área de trabalho de gestão de projetos**.</span><span class="sxs-lookup"><span data-stu-id="205bf-111">This is done by opening the **Project management workspace**.</span></span>

<span data-ttu-id="205bf-112">•   Clique em **Configurar o suplemento de cliente do projeto** a partir da secção **Ligações** > **Configurar** da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="205bf-112">•   Click **Configure project client add-in** from the **Links** > **Setup** section of the workspace.</span></span>

<span data-ttu-id="205bf-113">•   Clique em **Abrir** e, em seguida, clique em **Executar** quando for solicitado.</span><span class="sxs-lookup"><span data-stu-id="205bf-113">•   Click **Open**, then click **Run** when prompted.</span></span>

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a><span data-ttu-id="205bf-114">Abrir e editar uma estrutura hierárquica do trabalho existente de rascunho no Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="205bf-114">Open and edit an existing draft work breakdown structure in Microsoft Project Client</span></span>
<span data-ttu-id="205bf-115">Se um projeto no Dynamics 365 Finance já tiver uma estrutura hierárquica do trabalho criada, esta poderá ser aberta na aplicação Microsoft Project Client se a estrutura hierárquica do trabalho estiver no estado de rascunho.</span><span class="sxs-lookup"><span data-stu-id="205bf-115">If a project in Dynamics 365 Finance already has a work breakdown structure created, the work breakdown structure can be opened in the Microsoft Project Client application if the work breakdown structure is in a draft status.</span></span> <span data-ttu-id="205bf-116">Para abrir a partir da página **Projeto**, clique na ligação **Abrir no Microsoft Project** a partir do separador **Plano**. Esta página também pode ser aberta a partir da aplicação Microsoft Project Client ao clicar em **Abrir** no separador **Microsoft Dynamics 365**. Selecione a **Entidade jurídica** e **Projeto** a partir da lista.</span><span class="sxs-lookup"><span data-stu-id="205bf-116">To open from the **Project** page, click **Open in Microsoft Project** link from the **Plan** tab. This page can also be opened from within the Microsoft Project Client application by clicking **Open** in the **Microsoft Dynamics 365** tab. Select the **Legal entity** and **Project** from the list.</span></span>

> [!NOTE]
> <span data-ttu-id="205bf-117">Se estiver a utilizar o Internet Explorer como browser, terá de clicar em **Guardar** para abrir manualmente a partir da localização para a qual o ficheiro foi transferido.</span><span class="sxs-lookup"><span data-stu-id="205bf-117">If you're using Internet Explorer as your browser, you will need to click **Save** to manually open from the location that the file is downloaded to.</span></span> <span data-ttu-id="205bf-118">Ou clique em **Guardar e abrir** para abrir o ficheiro no Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="205bf-118">Or, click **Save and open** to open the file in Microsoft Project Client.</span></span> <span data-ttu-id="205bf-119">Não mude o nome do ficheiro ao guardar.</span><span class="sxs-lookup"><span data-stu-id="205bf-119">Do not rename the file name when saving.</span></span>

<span data-ttu-id="205bf-120">Antes de fazer quaisquer edições ao ficheiro através do Microsoft Project Client, terá de verificá-lo. Clique em **Dar saída** no separador **Microsoft Dynamics 365**. Isto evitará que outros utilizadores editem simultaneamente a estrutura hierárquica do trabalho a partir do Finance.</span><span class="sxs-lookup"><span data-stu-id="205bf-120">Before making any edits to the file using Microsoft Project Client, you need to check it out. Click **Check out** in the **Microsoft Dynamics 365** tab. This will prevent other users from editing the work breakdown structure from within Finance at the same time.</span></span> <span data-ttu-id="205bf-121">Para publicar a estrutura hierárquica do trabalho depois de concluir quaisquer edições, clique em **Dar entrada** no separador **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="205bf-121">To publish the work breakdown structure after completing any edits, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

<span data-ttu-id="205bf-122">Se já foi adicionada uma equipa de projeto ao projeto no Finance, a lista de recursos será preenchida com os membros da equipa.</span><span class="sxs-lookup"><span data-stu-id="205bf-122">If a project team has already been added to the project in Finance, the resource list will be populated with the team members.</span></span> <span data-ttu-id="205bf-123">Se uma equipa de projeto ainda não tiver sido adicionada ao projeto, poderá selecionar os recursos e criar a equipa no Microsoft Project Client ao clicar no botão **Recursos** no separador **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="205bf-123">If a project team has not yet been added to the project, you can select resources and build the team within Microsoft Project Client by clicking the **Resources** button on the **Microsoft Dynamics 365** tab.</span></span> 

<span data-ttu-id="205bf-124">Os seguintes dados serão sincronizados de volta com o Finance como parte do processo de registo de entrada:</span><span class="sxs-lookup"><span data-stu-id="205bf-124">The following data will be synced back to Finance as part of the check-in process:</span></span>

<span data-ttu-id="205bf-125">•   Nome da tarefa</span><span class="sxs-lookup"><span data-stu-id="205bf-125">•   Task name</span></span>

<span data-ttu-id="205bf-126">•   Data de início</span><span class="sxs-lookup"><span data-stu-id="205bf-126">•   Start date</span></span>

<span data-ttu-id="205bf-127">•   Data de conclusão</span><span class="sxs-lookup"><span data-stu-id="205bf-127">•   Finish date</span></span>

<span data-ttu-id="205bf-128">•   Antecessores</span><span class="sxs-lookup"><span data-stu-id="205bf-128">•   Predecessors</span></span>

<span data-ttu-id="205bf-129">•   Nomes de recursos</span><span class="sxs-lookup"><span data-stu-id="205bf-129">•   Resource names</span></span>

<span data-ttu-id="205bf-130">•   Categoria</span><span class="sxs-lookup"><span data-stu-id="205bf-130">•   Category</span></span>

<span data-ttu-id="205bf-131">•   Categoria de recurso</span><span class="sxs-lookup"><span data-stu-id="205bf-131">•   Resource category</span></span>

<span data-ttu-id="205bf-132">•   Horas de trabalho</span><span class="sxs-lookup"><span data-stu-id="205bf-132">•   Work hours</span></span>

<span data-ttu-id="205bf-133">•   Notas</span><span class="sxs-lookup"><span data-stu-id="205bf-133">•   Notes</span></span>

<span data-ttu-id="205bf-134">•   Prioridade</span><span class="sxs-lookup"><span data-stu-id="205bf-134">•   Priority</span></span>

> [!NOTE]
> <span data-ttu-id="205bf-135">Se adicionar quaisquer outras colunas ao seu ficheiro do Microsoft Project Client, elas não serão guardadas no ficheiro e não serão apresentadas quando o ficheiro for reaberto.</span><span class="sxs-lookup"><span data-stu-id="205bf-135">If you add any other columns to your Microsoft Project Client file, they will not be saved to the file and will not be displayed when the file is opened again.</span></span>

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="205bf-136">Crie a estrutura hierárquica do trabalho para um projeto existente ao utilizar o Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="205bf-136">Create the work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="205bf-137">Para criar uma nova estrutura hierárquica do trabalho ao utilizar o Microsoft Project Client, siga estes passos:</span><span class="sxs-lookup"><span data-stu-id="205bf-137">To create a new work breakdown structure using Microsoft Project Client, follow these steps:</span></span>


1.  <span data-ttu-id="205bf-138">Abra o Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="205bf-138">Open Microsoft Project Client.</span></span>

2.  <span data-ttu-id="205bf-139">No separador **Microsoft Dynamics 365**, clique em **Abrir**.</span><span class="sxs-lookup"><span data-stu-id="205bf-139">On the **Microsoft Dynamics 365** tab, click **Open**.</span></span>

3.  <span data-ttu-id="205bf-140">Selecione a **Entidade jurídica** para o projeto.</span><span class="sxs-lookup"><span data-stu-id="205bf-140">Select the **Legal entity** for the project.</span></span>

4.  <span data-ttu-id="205bf-141">Selecione o **Projeto**.</span><span class="sxs-lookup"><span data-stu-id="205bf-141">Select the **Project**.</span></span>

5.  <span data-ttu-id="205bf-142">Clique em **Registo de saída** no separador **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="205bf-142">Click **Check out** on the **Microsoft Dynamics 365** tab.</span></span>

6.  <span data-ttu-id="205bf-143">Quando estiver pronto para publicar no Finance, clique em **Registo de entrada** no separador **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="205bf-143">When ready to publish to Finance, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="205bf-144">Substitua a estrutura hierárquica do trabalho existente para um projeto existente ao utilizar o Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="205bf-144">Replace the existing work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="205bf-145">Para criar uma nova estrutura hierárquica do trabalho ao utilizar o Microsoft Project Client e substituir uma estrutura hierárquica do trabalho existente para um projeto existente, siga estes passos:</span><span class="sxs-lookup"><span data-stu-id="205bf-145">To create a new work breakdown structure using Microsoft Project Client and replace an existing work breakdown structure for an existing project, follow these steps:</span></span>

1.  <span data-ttu-id="205bf-146">Abra o Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="205bf-146">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="205bf-147">Crie a agenda no Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="205bf-147">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="205bf-148">No separador **Microsoft Dynamics 365**, clique em **Guardar alterações** > **Substituir o projeto existente**.</span><span class="sxs-lookup"><span data-stu-id="205bf-148">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Replace existing project**.</span></span>

4.  <span data-ttu-id="205bf-149">Selecione a **Entidade jurídica** para o projeto.</span><span class="sxs-lookup"><span data-stu-id="205bf-149">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="205bf-150">Selecione o **Projeto**.</span><span class="sxs-lookup"><span data-stu-id="205bf-150">Select the **Project**.</span></span>

6.  <span data-ttu-id="205bf-151">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="205bf-151">Click **OK**.</span></span>

## <a name="create-a-new-project-from-within-microsoft-project-client"></a><span data-ttu-id="205bf-152">Criar um novo projeto a partir do Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="205bf-152">Create a new project from within Microsoft Project Client</span></span>


1.  <span data-ttu-id="205bf-153">Abra o Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="205bf-153">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="205bf-154">Crie a agenda no Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="205bf-154">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="205bf-155">No separador **Microsoft Dynamics 365**, clique em **Guardar alterações** > **Guardar no novo Projeto**.</span><span class="sxs-lookup"><span data-stu-id="205bf-155">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Save to new Project**.</span></span>

4.  <span data-ttu-id="205bf-156">Selecione a **Entidade jurídica** para o projeto.</span><span class="sxs-lookup"><span data-stu-id="205bf-156">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="205bf-157">Introduza o **ID de projeto**, se for necessário.</span><span class="sxs-lookup"><span data-stu-id="205bf-157">Enter the **Project ID**, if necessary.</span></span>

6.  <span data-ttu-id="205bf-158">Introduza o **Nome do projeto**.</span><span class="sxs-lookup"><span data-stu-id="205bf-158">Enter the **Project name**.</span></span>

7.  <span data-ttu-id="205bf-159">Selecione o **Tipo de projeto**, **Grupo do projeto** e o **ID do contrato de projeto**.</span><span class="sxs-lookup"><span data-stu-id="205bf-159">Select the **Project type**, **Project group** and the **Project contract ID**.</span></span> <span data-ttu-id="205bf-160">Em alternativa, pode criar um novo contrato de projeto ao clicar em **Novo**.</span><span class="sxs-lookup"><span data-stu-id="205bf-160">Alternatively, you can create a new project contract by clicking **New**.</span></span>

8.  <span data-ttu-id="205bf-161">Selecione o **Calendário** a utilizar para a atribuição de recursos.</span><span class="sxs-lookup"><span data-stu-id="205bf-161">Select the **Calendar** to be used for resourcing.</span></span>

11. <span data-ttu-id="205bf-162">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="205bf-162">Click **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="205bf-163">O suplemento Project Client não suporta os seguintes caracteres no formato de ID do projeto:</span><span class="sxs-lookup"><span data-stu-id="205bf-163">The Project Client add-in doesn’t support the following characters in the project ID format:</span></span>
> 
>   - <span data-ttu-id="205bf-164">Caráter de sublinhado</span><span class="sxs-lookup"><span data-stu-id="205bf-164">Underscore</span></span>
>   - <span data-ttu-id="205bf-165">Período</span><span class="sxs-lookup"><span data-stu-id="205bf-165">Period</span></span>
>   - <span data-ttu-id="205bf-166">Espaço</span><span class="sxs-lookup"><span data-stu-id="205bf-166">Space</span></span>
>   - <span data-ttu-id="205bf-167">Barra</span><span class="sxs-lookup"><span data-stu-id="205bf-167">Slash</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
