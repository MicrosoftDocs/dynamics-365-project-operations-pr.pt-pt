---
title: Criar um novo projeto
description: Este tópico fornece informações sobre como criar um novo projeto.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8218747366be8536601cb007318c642ac122536b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006255"
---
# <a name="create-a-new-project"></a><span data-ttu-id="92706-103">Criar um novo projeto</span><span class="sxs-lookup"><span data-stu-id="92706-103">Create a new project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="92706-104">Conclua os seguintes passos para criar um novo projeto.</span><span class="sxs-lookup"><span data-stu-id="92706-104">Complete the following steps to create a new project.</span></span>

1. <span data-ttu-id="92706-105">Na página **Gestão de projetos**, selecione **Novo projeto** e introduza os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="92706-105">On the **Project management** page, select **New project**, and enter the following values:</span></span>

    - <span data-ttu-id="92706-106">**Tipo de projeto:** Tempo e material</span><span class="sxs-lookup"><span data-stu-id="92706-106">**Project type:** Time and material</span></span>
    - <span data-ttu-id="92706-107">**Nome do projeto:** Fase de Atualização 2 XYZ</span><span class="sxs-lookup"><span data-stu-id="92706-107">**Project name:** XYZ Upgrade Phase 2</span></span>
    - <span data-ttu-id="92706-108">**Grupo do projeto:** TM\_WIP</span><span class="sxs-lookup"><span data-stu-id="92706-108">**Project group:** TM\_WIP</span></span>
    - <span data-ttu-id="92706-109">**ID de contrato do projeto:** 00000002</span><span class="sxs-lookup"><span data-stu-id="92706-109">**Project contract ID:** 00000002</span></span>

2. <span data-ttu-id="92706-110">Selecione **Criar projeto**.</span><span class="sxs-lookup"><span data-stu-id="92706-110">Select **Create project**.</span></span>

## <a name="assign-a-resource-to-a-project"></a><span data-ttu-id="92706-111">Atribuir um recurso a um projeto</span><span class="sxs-lookup"><span data-stu-id="92706-111">Assign a resource to a project</span></span>

1. <span data-ttu-id="92706-112">Na página **Trabalhadores**, na lista **Trabalhadores**, selecione o registo para o trabalhador para o qual configurou anteriormente competências, e abra o registo do trabalhador.</span><span class="sxs-lookup"><span data-stu-id="92706-112">On the **Workers** page, in the **Workers** list, select the record for the worker that you previously set up competencies for, and open the worker record.</span></span>
2. <span data-ttu-id="92706-113">No Painel de Ação, no separador **Projeto**, no grupo **Configurar**, selecione **Atribuir projetos**.</span><span class="sxs-lookup"><span data-stu-id="92706-113">On the Action Pane, on the **Project** tab, in the **Setup** group, select **Assign projects**.</span></span>
3. <span data-ttu-id="92706-114">Na página **Atribuições de projetos de validação de recursos**, no separador **Projetos**, no campo **Adicionar o projeto aos projetos selecionados**, filtre pelo projeto **Fase de Atualização 2 XYZ**.</span><span class="sxs-lookup"><span data-stu-id="92706-114">On the **Resource validation project assignments** page, on the **Projects** tab, in the **Add the project to selected projects** field, filter on the **XYZ Upgrade Phase 2** project.</span></span>
4. <span data-ttu-id="92706-115">No painel de **Projetos restantes**, selecione um projeto e, em seguida, selecione o botão de seta para adicioná-lo ao painel **Projetos selecionados**.</span><span class="sxs-lookup"><span data-stu-id="92706-115">In the **Remaining projects** pane, select a project, and then select the arrow button to add it to the **Selected projects** pane.</span></span>

<span data-ttu-id="92706-116">Também pode atribuir categorias para um recurso, conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="92706-116">You can also assign categories for a resource as you require.</span></span> <span data-ttu-id="92706-117">O tipo de categoria é **Custo** ou **Receitas**.</span><span class="sxs-lookup"><span data-stu-id="92706-117">The category type is either **Cost** or **Revenue**.</span></span> <span data-ttu-id="92706-118">O tipo de categoria é determinado pela sua organização.</span><span class="sxs-lookup"><span data-stu-id="92706-118">The category type is determined by your organization.</span></span> <span data-ttu-id="92706-119">Se não forem atribuídas categorias a um recurso, o Finance procura a categoria predefinida nos preços por hora para custos e receitas.</span><span class="sxs-lookup"><span data-stu-id="92706-119">If no categories are assigned for a resource, Finance looks up the default category on hour prices for cost and revenue.</span></span>

## <a name="set-up-project-resource-and-role-characteristics"></a><span data-ttu-id="92706-120">Configurar características de recursos e funções do projeto</span><span class="sxs-lookup"><span data-stu-id="92706-120">Set up project resource and role characteristics</span></span>

<span data-ttu-id="92706-121">Um gestor de projetos pode utilizar a funcionalidade de atribuição de recursos do projeto para criar as funções necessárias para o projeto.</span><span class="sxs-lookup"><span data-stu-id="92706-121">A project manager can use the project resourcing functionality to create the roles that are required for the project.</span></span> <span data-ttu-id="92706-122">As funções podem ser utilizadas se os recursos confirmados ainda forem desconhecidos quando os recursos estão a ser reservados.</span><span class="sxs-lookup"><span data-stu-id="92706-122">Roles can be used if confirmed resources are still unknown when resources are being reserved.</span></span> <span data-ttu-id="92706-123">As funções podem ser reservadas temporariamente como recursos planeados para poder continuar as fases de planeamento do projeto.</span><span class="sxs-lookup"><span data-stu-id="92706-123">Roles can be temporarily reserved as planned resources, so that you can continue the project planning stages.</span></span>

<span data-ttu-id="92706-124">[![Exemplo de uma função](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span><span class="sxs-lookup"><span data-stu-id="92706-124">[![Example of a role](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span></span> 

<span data-ttu-id="92706-125">**Cenário:** A Contoso foi contratada para concluir um projeto de Tempo e material que tem uma carta de projeto aprovada.</span><span class="sxs-lookup"><span data-stu-id="92706-125">**Scenario:** Contoso was hired to complete a Time and material project that has an approved project charter.</span></span> <span data-ttu-id="92706-126">O gestor de projetos junior ainda está a concluir o âmbito do projeto.</span><span class="sxs-lookup"><span data-stu-id="92706-126">The junior project manager is still completing the scope of the project.</span></span> <span data-ttu-id="92706-127">O gestor de recursos está neste momento a identificar os recursos específicos que serão reservados para trabalhar no novo projeto.</span><span class="sxs-lookup"><span data-stu-id="92706-127">The resource manager is currently identifying specific resources that will be reserved to work on the new project.</span></span> <span data-ttu-id="92706-128">Dada a natureza crítica do projeto, o patrocinador do projeto solicitou o gestor de projeto sénior como uma das funções.</span><span class="sxs-lookup"><span data-stu-id="92706-128">Because of the critical nature of the project, the project sponsor requested Senior project manager as one of the roles.</span></span> <span data-ttu-id="92706-129">O gestor de recursos tem de adquirir o novo recurso e definir a função no sistema no caso de o gestor de projeto júnior necessitar de informações dos recursos durante o planeamento do projeto.</span><span class="sxs-lookup"><span data-stu-id="92706-129">The resource manager must acquire the new resource and define the role in the system in case the junior project manager requires the resource information during project planning.</span></span>

<span data-ttu-id="92706-130">Os passos seguintes mostram como o gestor de recursos pode configurar a função de gestor de projetos Sénior e associar características de recursos a ele.</span><span class="sxs-lookup"><span data-stu-id="92706-130">The following steps show how the resource manager can set up the Senior project manager role and associate resource characteristics with it.</span></span> <span data-ttu-id="92706-131">Mais tarde, a função pode ser utilizada para procurar recursos disponíveis que correspondam às competências de recursos necessárias.</span><span class="sxs-lookup"><span data-stu-id="92706-131">Later, the role can be used to search for available resources that match the required resource competencies.</span></span>

1. <span data-ttu-id="92706-132">Na página **Configurar funções**, selecione **Novo** e introduza os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="92706-132">On the **Setup roles** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="92706-133">**ID de função:** Gestor de Projetos Sénior</span><span class="sxs-lookup"><span data-stu-id="92706-133">**Role ID:** Senior Project Manager</span></span>
    - <span data-ttu-id="92706-134">**Descrição:** Gestor de Projetos Sénior</span><span class="sxs-lookup"><span data-stu-id="92706-134">**Description:** Senior Project Manager</span></span>

2. <span data-ttu-id="92706-135">Selecione **Criar**.</span><span class="sxs-lookup"><span data-stu-id="92706-135">Select **Create**.</span></span>
3. <span data-ttu-id="92706-136">Selecione a função **Gestor de Projetos Sénior** e, em seguida, selecione **Configurar características**.</span><span class="sxs-lookup"><span data-stu-id="92706-136">Select the **Senior Project Manager** role, and then select **Configure characteristics**.</span></span>
4. <span data-ttu-id="92706-137">No campo **Tipo de características**, selecione **Aptidão**.</span><span class="sxs-lookup"><span data-stu-id="92706-137">In the **Characteristics type** field, select **Skill**.</span></span>
5. <span data-ttu-id="92706-138">No campo **Características disponíveis**, introduza a aptidão a procurar.</span><span class="sxs-lookup"><span data-stu-id="92706-138">In the **Available characteristics** field, enter the skill to search for.</span></span>
6. <span data-ttu-id="92706-139">No campo **Tipo de característica**, selecione **Certificado**.</span><span class="sxs-lookup"><span data-stu-id="92706-139">In the **Characteristic type** field, select **Certificate**.</span></span>
7. <span data-ttu-id="92706-140">No campo **Características disponíveis**, introduza o tipo de certificado a procurar.</span><span class="sxs-lookup"><span data-stu-id="92706-140">In the **Available characteristics** field, enter the certificate type to search for.</span></span>

## <a name="assign-a-project-resource-to-a-project"></a><span data-ttu-id="92706-141">Atribuir um recurso de projeto a um projeto</span><span class="sxs-lookup"><span data-stu-id="92706-141">Assign a project resource to a project</span></span>

1. <span data-ttu-id="92706-142">Na página **Todos os projetos**, selecione o projeto **Fase de Atualização 2 XYZ**.</span><span class="sxs-lookup"><span data-stu-id="92706-142">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="92706-143">No separador **Equipa do projeto e agendamento**, selecione **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="92706-143">On the **Project team and scheduling** tab, select **Add**.</span></span>
3. <span data-ttu-id="92706-144">No campo **Função**, selecione **Membro da equipa**.</span><span class="sxs-lookup"><span data-stu-id="92706-144">In the **Role** field, select **Team member**.</span></span>
4. <span data-ttu-id="92706-145">Selecione **Reservar no calendário**.</span><span class="sxs-lookup"><span data-stu-id="92706-145">Select **Book from calendar**.</span></span>
5. <span data-ttu-id="92706-146">Na página **Disponibilidade do recurso**, selecione **Ver definições**.</span><span class="sxs-lookup"><span data-stu-id="92706-146">On the **Resource availability** page, select **View settings**.</span></span>
6. <span data-ttu-id="92706-147">Na página **'Ajustar definições da vista**, introduza os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="92706-147">On the **Adjust view settings** page, enter the following values:</span></span>

    - <span data-ttu-id="92706-148">**Formato para a vista de intervalo de datas:** Dia</span><span class="sxs-lookup"><span data-stu-id="92706-148">**Format for date range view:** Day</span></span>
    - <span data-ttu-id="92706-149">**Apresentar descrições de disponibilidade:** Sim</span><span class="sxs-lookup"><span data-stu-id="92706-149">**Display availability descriptions:** Yes</span></span>
    - <span data-ttu-id="92706-150">**Apresentar capacidade restante:** Sim</span><span class="sxs-lookup"><span data-stu-id="92706-150">**Display remaining capacity:** Yes</span></span>

7. <span data-ttu-id="92706-151">Na lista de recursos, selecione um recurso.</span><span class="sxs-lookup"><span data-stu-id="92706-151">In the list of resources, select a resource.</span></span>
8. <span data-ttu-id="92706-152">Selecione **Reserva Fixa** e **Capacidade Total**.</span><span class="sxs-lookup"><span data-stu-id="92706-152">Select **Hard book** and **Full capacity**.</span></span>

## <a name="assign-a-resource-to-a-default-role"></a><span data-ttu-id="92706-153">Atribuir um recurso a uma função predefinida</span><span class="sxs-lookup"><span data-stu-id="92706-153">Assign a resource to a default role</span></span>

<span data-ttu-id="92706-154">Para ajudar os gestores de projetos ou recursos, podem desagregar mais nos recursos que podem ser reservados para um projeto.</span><span class="sxs-lookup"><span data-stu-id="92706-154">To help project or resource managers can drill down further on the resources that can be reserved for a project.</span></span> <span data-ttu-id="92706-155">Pode associar uma função predefinida a um recurso existente ou a um recurso adquirido recentemente.</span><span class="sxs-lookup"><span data-stu-id="92706-155">You can associate a default role with an existing resource or a newly acquired resource.</span></span> <span data-ttu-id="92706-156">Por exemplo, quando o Daniel foi contratado, tinha experiência e aptidões para preencher a função Analista de negócios.</span><span class="sxs-lookup"><span data-stu-id="92706-156">For example, when Daniel was hired, he had the experience and skills to fill the Business analyst role.</span></span> <span data-ttu-id="92706-157">O gestor de recursos atribuiu esta função como função predefinida de Daniel.</span><span class="sxs-lookup"><span data-stu-id="92706-157">The resource manager assigned this role as Daniel's default role.</span></span> <span data-ttu-id="92706-158">Por isso, o gestor de recursos adicionou Daniel a um conjunto de analistas de negócios que estão disponíveis para trabalhar em projetos.</span><span class="sxs-lookup"><span data-stu-id="92706-158">Therefore, the resource manager added Daniel to a pool of business analysts who are available to work on projects.</span></span>

<span data-ttu-id="92706-159">Durante a reserva de recursos, os gestores de projetos podem filtrar os recursos da função que estão disponíveis para trabalhar em projetos.</span><span class="sxs-lookup"><span data-stu-id="92706-159">During resource reservation, project managers can filter the role resources that are available to work on projects.</span></span> <span data-ttu-id="92706-160">Podem utilizar esta informação como um critério quando executam a análise de decisões de vários critérios durante a execução dos recursos.</span><span class="sxs-lookup"><span data-stu-id="92706-160">They can use this information as one criterion when they perform multi-criteria decision analysis during resource fulfillment.</span></span> <span data-ttu-id="92706-161">Podem ainda adicionar outras características de recursos ao filtro para procurar recursos com aptidões, formação e experiência específicas para um determinado projeto.</span><span class="sxs-lookup"><span data-stu-id="92706-161">They can also add other resource characteristics to the filter to search for resources that have specific skills, education, and experience for a given project.</span></span>

<span data-ttu-id="92706-162">**Cenário:** foi iniciado um projeto aprovado e a função de de gestor de projetos Sénior foi reservada como recurso planeado durante a fase de planeamento do projeto.</span><span class="sxs-lookup"><span data-stu-id="92706-162">**Scenario:** An approved project has started, and the Senior project manager role was reserved as a planned resource during the project planning stage.</span></span> <span data-ttu-id="92706-163">O gestor de recursos adquiriu agora um recurso para executar a função Gestor de projetos sénior.</span><span class="sxs-lookup"><span data-stu-id="92706-163">The resource manager has now acquired a resource to fulfill the Senior project manager role.</span></span>

1. <span data-ttu-id="92706-164">Na página **Lista de recursos**, selecione **Daniel Goldschmidt**.</span><span class="sxs-lookup"><span data-stu-id="92706-164">On the **Resources list** page, select **Daniel Goldschmidt**.</span></span>
2. <span data-ttu-id="92706-165">Na página **Função do recurso**, selecione **Novo** e introduza os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="92706-165">On the **Resource role** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="92706-166">**Data Efetiva:** Introduza a data atual.</span><span class="sxs-lookup"><span data-stu-id="92706-166">**Effective:** Enter the current date.</span></span>
    - <span data-ttu-id="92706-167">**Expiração:** introduza **Nunca**.</span><span class="sxs-lookup"><span data-stu-id="92706-167">**Expiration:** Enter **Never**.</span></span>
    - <span data-ttu-id="92706-168">**Função:** introduza **Gestor de Projetos Sénior**.</span><span class="sxs-lookup"><span data-stu-id="92706-168">**Role:** Enter **Senior Project Manager**.</span></span>

3. <span data-ttu-id="92706-169">Selecione **Guardar** e feche a página.</span><span class="sxs-lookup"><span data-stu-id="92706-169">Select **Save**, and then close the page.</span></span>
4. <span data-ttu-id="92706-170">No separador **Competências**, adicione a aptidão **ProjectMgmt** e o certificado **PMP**.</span><span class="sxs-lookup"><span data-stu-id="92706-170">On the **Competencies** tab, add the **ProjectMgmt** skill and the **PMP** certificate.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]