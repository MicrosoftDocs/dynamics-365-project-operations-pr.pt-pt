---
title: Gerir recursos
description: Este tópico fornece informações sobre como pode gerir recursos.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/13/2019
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
ms.openlocfilehash: 1d47be6c11ced70b94b7497dfbc0c67d1a3f631b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275012"
---
# <a name="manage-resources"></a><span data-ttu-id="bc8ae-103">Gerir recursos</span><span class="sxs-lookup"><span data-stu-id="bc8ae-103">Manage resources</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="bc8ae-104">O Dynamics 365 Project Service Automation inclui um dashboard do gestor de recursos que fornece uma descrição geral visual da procura e utilização de recursos em toda a organização.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-104">Dynamics 365 Project Service Automation includes a resource manager dashboard that provides a visual overview of resource demand and utilization throughout the organization.</span></span> <span data-ttu-id="bc8ae-105">Pode utilizar os gráficos neste dashboard para visualizar as seguintes informações:</span><span class="sxs-lookup"><span data-stu-id="bc8ae-105">You can use the charts on this dashboard to visualize the following information:</span></span>

- <span data-ttu-id="bc8ae-106">**Procura de recursos** – O gráfico **Pedido de Recursos Ativos** mostra os recursos que foram submetidos.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-106">**Resource demand** – The **Active Resource Request** chart shows resources that have been submitted.</span></span> <span data-ttu-id="bc8ae-107">Os recursos são agregados por uma função ou projeto.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-107">The resources are aggregated by either role or project.</span></span>
- <span data-ttu-id="bc8ae-108">**Procura de recursos não submetidos** – O gráfico **Procura de Recursos Não Atribuídos** mostra todos os requisitos de recursos que não foram submetidos.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-108">**Unsubmitted resource demand** – The **Unassigned Resource Demand** chart shows all the resource requirements that haven't been submitted.</span></span> <span data-ttu-id="bc8ae-109">Ajuda os gestores de recursos a visualizarem a procura que não é firme e que pode ser submetida através de um pedido de recurso.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-109">It helps resource managers view demand that isn't firm and might be submitted through a resource request.</span></span>
- <span data-ttu-id="bc8ae-110">**Utilização faturável para a semana passada** – O gráfico **Utilização por Função** mostra a percentagem da utilização faturável real da organização por função relativamente à sua utilização faturável de destino por função.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-110">**Billable utilization for the past week** – The **Utilization by Role** chart shows the percentage of the organization's actual billable utilization by role against its target billable utilization by role.</span></span>

    > [!NOTE]
    > <span data-ttu-id="bc8ae-111">Para disponibilizar o gráfico **Utilização por Função**, crie uma tarefa que execute o fluxo de trabalho UpdateRoleUtilization</span><span class="sxs-lookup"><span data-stu-id="bc8ae-111">To make the **Utilization by Role** chart available, create a job that runs the UpdateRoleUtilization workflow.</span></span> <span data-ttu-id="bc8ae-112">Esta tarefa periódica é executada a cada sete dias para calcular a utilização faturável nos sete dias anteriores.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-112">This recurring job runs every seven days to calculate billable utilization for the previous seven days.</span></span> <span data-ttu-id="bc8ae-113">Os resultados são agregados por função.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-113">The results are aggregated by role.</span></span>

## <a name="manage-project-team-members"></a><span data-ttu-id="bc8ae-114">Gerir membros da equipa do projeto</span><span class="sxs-lookup"><span data-stu-id="bc8ae-114">Manage project team members</span></span>

<span data-ttu-id="bc8ae-115">Os gestores de projeto podem utilizar o dashboard do gestor de recursos para gerir os recursos nos projetos.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-115">Project managers can use the resource manager dashboard to manage the resources on projects.</span></span> <span data-ttu-id="bc8ae-116">Por exemplo, podem adicionar um membro da equipa diretamente a um projeto e reservar um membro da equipa para cumprir os requisitos de recursos que foram capturados por um recurso genérico.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-116">For example, they can add a team member directly to a project and book a team member to fulfill the resource requirements that were captured by a generic resource.</span></span>

### <a name="add-a-team-member-directly-to-a-project"></a><span data-ttu-id="bc8ae-117">Adicionar um membro da equipa diretamente a um projeto</span><span class="sxs-lookup"><span data-stu-id="bc8ae-117">Add a team member directly to a project</span></span>

<span data-ttu-id="bc8ae-118">Para adicionar um membro da equipa diretamente a um projeto, na página **Projetos**, no separador **Equipa**, selecione **Novo**.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-118">To add a team member directly to a project, on the **Projects** page, on the **Team** tab, select **New**.</span></span> <span data-ttu-id="bc8ae-119">É apresentada a caixa de diálogo **Criação Rápida: Membro da Equipa do Projeto**.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-119">The **Quick Create:Project Team Member** dialog box appears.</span></span> <span data-ttu-id="bc8ae-120">Nesta caixa de diálogo, pode efetuar estas tarefas:</span><span class="sxs-lookup"><span data-stu-id="bc8ae-120">In this dialog box, you can perform these tasks:</span></span>

- <span data-ttu-id="bc8ae-121">**Reservar um recurso nomeado** – No campo **Recurso Reservável**, selecione o nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-121">**Book a named resource** – In the **Bookable Resource** field, select the name of the resource.</span></span> <span data-ttu-id="bc8ae-122">Em seguida, selecione a função, defina o período e selecione um método de alocação.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-122">Then select the role, set the period, and select an allocation method.</span></span> <span data-ttu-id="bc8ae-123">O recurso nomeado que selecionou é adicionado ao projeto utilizando o método de alocação selecionado e o calendário de recursos.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-123">The named resource that you selected is added to the project by using the selected allocation method and the resources calendar.</span></span>
- <span data-ttu-id="bc8ae-124">**Adicionar um recurso genérico** – Deixe o campo **Recurso reservável** em branco e, em seguida, selecione a função, defina o período e selecione o método de alocação preferencial.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-124">**Add a generic resource** – Leave the **Bookable resource** field blank, and then select the role, set the period, and select the preferred allocation method.</span></span> <span data-ttu-id="bc8ae-125">Um recurso genérico é adicionado à equipa como um marcador de posição para manter o padrão de procura utilizado para reservar recursos nomeados na equipa.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-125">A generic resource is added to the team as a placeholder to hold the demand pattern that is used to book named resources on the team.</span></span> <span data-ttu-id="bc8ae-126">O requisito é efetuado de acordo com o calendário do projeto.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-126">The requirement is made according to the project calendar.</span></span>
- <span data-ttu-id="bc8ae-127">**Adicionar um recurso nomeado à equipa sem consumir capacidade do recurso** – No campo **Recurso Reservável**, selecione um recurso.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-127">**Add a named resource to the team without consuming resource capacity** – In the **Bookable Resource** field, select a resource.</span></span> <span data-ttu-id="bc8ae-128">Em seguida, selecione o período e selecione **Nenhum** o método de alocação.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-128">Then select the period, and select **None** as the allocation method.</span></span> <span data-ttu-id="bc8ae-129">O recurso é adicionado à equipa, mas a capacidade do recurso não é consumida através de uma reserva.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-129">The resource is added to the team, but the resource's capacity isn't consumed through a booking.</span></span>

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a><span data-ttu-id="bc8ae-130">Reservar um membro da equipa para cumprir os requisitos de recursos para um recurso genérico</span><span class="sxs-lookup"><span data-stu-id="bc8ae-130">Book a team member to fulfill resource requirements for a generic resource</span></span>

<span data-ttu-id="bc8ae-131">No PSA, pode reservar um recurso genérico numa equipa do projeto e pode especificar a função, a capacidade necessária e a forma como essa capacidade é distribuída.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-131">In PSA, you can book a generic resource on a project team, and can specify the role, the required capacity, and how that capacity is distributed.</span></span> <span data-ttu-id="bc8ae-132">No requisito de recurso, pode especificar atributos que estão associados ao recurso genérico.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-132">On the resource requirement, you can specify attributes that are associated with the generic resource.</span></span> <span data-ttu-id="bc8ae-133">Estes atributos incluem as competências necessárias, a unidade organizacional preferencial e os recursos preferenciais.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-133">These attributes include required skills, the preferred organizational unit, and preferred resources.</span></span>

<span data-ttu-id="bc8ae-134">Siga estes passos para especificar as competências necessárias num recurso genérico para um programador.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-134">Follow these steps to specify required skills on a generic resource for a developer.</span></span>

1. <span data-ttu-id="bc8ae-135">Na página **Projetos**, no separador **Equipa**, selecione **Novo** para reservar um recurso genérico.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-135">On the **Projects** page, on the **Team** tab, select **New** to book a generic resource.</span></span>

    ![Recurso genérico reservado na equipa](media/Resource-Management-image9.png)

2. <span data-ttu-id="bc8ae-137">Na vista **Todos os Membros da Equipa**, na coluna **Requisito de Recurso**, selecione a ligação para adicionar as competências necessárias para o recurso genérico.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-137">In the **All Team Members** view, in the **Resource Requirement** column, select the link to add required skills for the generic resource.</span></span>

    ![Ligação de requisitos](media/Resource-Management-image10.png)

3. <span data-ttu-id="bc8ae-139">Na página **Requisito de Recurso** que é apresentada, na grelha **Competências**, selecione as reticências (**...**) e, em seguida, selecione **Adicionar Nova Característica de Requisito** para adicionar as competências necessárias para o programador.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-139">On the **Resource Requirement** page that appears, in the **Skills** grid, select the ellipsis (**...**) and then select **Add New Requirement Characteristic** to add the required skills for your developer.</span></span>

    ![Comando Adicionar Nova Característica de Requisito](media/Resource-Management-image11.png)

4. <span data-ttu-id="bc8ae-141">Na caixa de diálogo **Criação Rápida: Característica de Requisito** que é apresentada, no campo **Característica**, selecione a competência necessária.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-141">In the **Quick Create: Requirement Characteristic** dialog box that appears, in the **Characteristic** field, select the required skill.</span></span> <span data-ttu-id="bc8ae-142">Em seguida, no campo **Valor de classificação**, selecione o nível de proficiência para essa competência.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-142">Then, in the **Rating value** field, select the proficiency level for that skill.</span></span> <span data-ttu-id="bc8ae-143">Por fim, no campo **Requisito de Recurso**, defina o requisito como os recursos de origem a partir de unidades organizacionais ou até mesmo de recursos nomeados.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-143">Finally, in the **Resource Requirement** field, set the requirement to source resources from organizational units or even named resources.</span></span> <span data-ttu-id="bc8ae-144">Quando tiver terminado, selecione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-144">When you've finished, select **Save**.</span></span>

    ![Caixa de diálogo Criação Rápida: Característica de Requisito](media/Resource-Management-image12.png)

5. <span data-ttu-id="bc8ae-146">Na página **Requisito de Recurso**, selecione **Reservar** para cumprir o requisito de recurso.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-146">On the **Resource Requirement** page, select **Book** to fulfill the resource requirement.</span></span>

    ![Botão Reservar na página Requisito de Recurso](media/Resource-Management-image13.png)

    <span data-ttu-id="bc8ae-148">Também pode selecionar o recurso genérico na grelha **Todos os Membros da Equipa** e, em seguida, selecione **Reservar**.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-148">You can also select the generic resource in the **All Team Members** grid and then select **Book**.</span></span>

    ![Botão Reservar acima da grelha Todos os Membros da Equipa](media/Resource-Management-image14.png)

    > [!NOTE]
    > <span data-ttu-id="bc8ae-150">Neste exemplo, existem 40 horas necessárias, mas não existem horas reservadas reais, porque os recursos genéricos não têm reservas.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-150">In this example, there are 40 required hours but no actual booked hours, because generic resources don't have bookings.</span></span> <span data-ttu-id="bc8ae-151">Além disso, não existem horas atribuídas, porque o recurso genérico foi adicionado diretamente à equipa.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-151">Additionally, there are no assigned hours, because the generic resource was added directly to the team.</span></span> <span data-ttu-id="bc8ae-152">O mesmo não foi adicionado através da atribuição de tarefas.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-152">It wasn't added by using task assignment.</span></span>

    <span data-ttu-id="bc8ae-153">Na página **Assistente de Agendamento**, pode filtrar os recursos disponíveis de acordo com os requisitos especificados no requisito de recurso.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-153">On the **Scheduling Assistant** page, you can filter available resources by the requirements that are specified on the resource requirement.</span></span> <span data-ttu-id="bc8ae-154">Os recursos são ordenados de acordo com os parâmetros de ordenação especificados no Quadro da Agenda.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-154">Resources are sorted according to the sorting parameters that are specified on the Schedule Board.</span></span>

    ![Página Assistente de Agendamento](media/Resource-Management-image15.png)

    <span data-ttu-id="bc8ae-156">Seguem-se alguns filtros que são frequentemente utilizados:</span><span class="sxs-lookup"><span data-stu-id="bc8ae-156">Here are some filters that are often used:</span></span>

    - <span data-ttu-id="bc8ae-157">**Características juntamente com uma classificação** – Filtrar por competências, certificações e outras qualidades de recursos, para além das classificações de proficiência.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-157">**Characteristics along with a rating** – Filter by skills, certifications, and other resource qualities, in addition to ratings of proficiency.</span></span>
    - <span data-ttu-id="bc8ae-158">**Funções** – Filtrar pelas funções predefinidas atribuídas aos recursos reserváveis.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-158">**Roles** – Filter by the default roles that are assigned to bookable resources.</span></span>
    - <span data-ttu-id="bc8ae-159">**Unidades organizacionais** – Filtrar recursos reserváveis pelas unidades organizacionais às quais estão atribuídos.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-159">**Organizational units** – Filter bookable resources by the organizational units that they are assigned to.</span></span>

6. <span data-ttu-id="bc8ae-160">Se não estiver satisfeito com os resultados da pesquisa inicial de requisitos, pode alterar os critérios de filtro.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-160">If you aren't satisfied with the results of the initial requirement search, you can change the filter criteria.</span></span> <span data-ttu-id="bc8ae-161">Expanda o painel **Vista de Filtro** à esquerda e, em seguida, selecione **Pesquisar** para localizar recursos adicionais.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-161">Expand the **Filter View** pane on the left, and then select **Search** to find additional resources.</span></span>

    ![Painel Vista de Filtro](media/Resource-Management-image16.png)

7. <span data-ttu-id="bc8ae-163">Para alterar a forma como os resultados são ordenados, selecione **Ordenar**.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-163">To change how the results are sorted, select **Sort**.</span></span>

    ![Comando Ordenar](media/Resource-Management-image17.png)

8. <span data-ttu-id="bc8ae-165">Selecione recursos de acordo com a procura especificada no requisito, conforme indicado na parte superior da grelha.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-165">Select resources according to the demand that is specified on the requirement, as indicated at the top of the grid.</span></span> <span data-ttu-id="bc8ae-166">Pode limpar a seleção de células na grelha e deixar a capacidade do recurso aberta.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-166">You can clear the selection of cells in the grid and leave that resource capacity open.</span></span> <span data-ttu-id="bc8ae-167">Só é possível selecionar um recurso de cada vez como está reservado.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-167">Only one resource at a time can be selected as booked.</span></span>

9. <span data-ttu-id="bc8ae-168">Selecione **Reservar** para reservar o recurso selecionado e deixar o Quadro da Agenda aberto, para que possa selecionar recursos adicionais.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-168">Select **Book** to book the selected resource and leave the Schedule Board open, so that you can select additional resources.</span></span> <span data-ttu-id="bc8ae-169">Em alternativa, selecione **Reservar e Sair** para reservar o recurso selecionado e fechar o Quadro da Agenda.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-169">Alternatively, select **Book & Exit** to book the selected resource and close the Schedule Board.</span></span>

    ![Recurso a reservar](media/Resource-Management-image19.png)

    <span data-ttu-id="bc8ae-171">Recebe uma notificação sobre as horas reservadas.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-171">You receive a notification about booked hours.</span></span> <span data-ttu-id="bc8ae-172">Os indicadores de procura mostram a quantidade de tempo de reserva satisfeita e a quantidade de tempo restante.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-172">The demand indicators show how much the booking requirement is satisfied and how much remains.</span></span> <span data-ttu-id="bc8ae-173">Também pode ver a quantidade de capacidade do recurso selecionada que é consumida.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-173">You can also see how much of the selected resource's capacity is consumed.</span></span> <span data-ttu-id="bc8ae-174">Selecione **Expandir** para ver mais detalhes sobre as reservas de recursos.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-174">Select **Expand** to view more details about resource bookings.</span></span>

9. <span data-ttu-id="bc8ae-175">Volte à vista **Todos os Membros da Equipa**.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-175">Return to the **All Team Members** view.</span></span> <span data-ttu-id="bc8ae-176">Na grelha, note que o recurso genérico foi substituído pelo recurso nomeado e as 40 horas estão listadas como reservadas para esse recurso.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-176">In the grid, notice that the generic resource has been replaced by the named resource, and 40 hours are listed as booked for that resource.</span></span>

    ![Grelha Todos os Membros da Equipa atualizada](media/Resource-Management-image20.png)

    > [!NOTE]
    > <span data-ttu-id="bc8ae-178">Não são apresentadas as horas atribuídas, porque estavam reservadas diretamente na equipa.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-178">No assigned hours are shown, because they were booked directly on the team.</span></span> <span data-ttu-id="bc8ae-179">Não foram reservadas através da atribuição de tarefas.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-179">They weren't booked by using task assignment.</span></span>

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a><span data-ttu-id="bc8ae-180">Atribuir recursos genéricos a tarefas e gerar requisitos de recursos</span><span class="sxs-lookup"><span data-stu-id="bc8ae-180">Assign generic resources to tasks and generate resource requirements</span></span>

<span data-ttu-id="bc8ae-181">No PSA, é possível criar tarefas e, em seguida, atribuir-lhes recursos genéricos.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-181">In PSA, you can create tasks and then assign generic resources to them.</span></span> <span data-ttu-id="bc8ae-182">Desta forma, a procura de recursos pode ser representada por marcadores de posição enquanto estima a agenda e os números financeiros.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-182">In this way, resource demand can be represented by placeholders while you estimate your schedule and financial numbers.</span></span> <span data-ttu-id="bc8ae-183">Em seguida, pode gerar requisitos de recursos para os recursos genéricos e cumpri-los.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-183">You can then generate resource requirements for the generic resources and fulfill them.</span></span>

1. <span data-ttu-id="bc8ae-184">Na página **Projetos**, no separador **Agenda**, selecione **Adicionar** para criar uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-184">On the **Projects** page, on the **Schedule** tab, select **Add** to create a task.</span></span>

    ![Nova tarefa criada](media/Resource-Management-image21.png)

2. <span data-ttu-id="bc8ae-186">No campo **Recursos**, selecione o símbolo **Seletor de Recursos**.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-186">In the **Resources** field, select the **Resource Picker** symbol.</span></span> <span data-ttu-id="bc8ae-187">O Seletor de Recursos é apresentado e mostra os membros da equipa existentes para o projeto.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-187">The Resource Picker appears and shows existing team members for the project.</span></span>

    ![Seletor de Recursos](media/Resource-Management-image22.png)

3. <span data-ttu-id="bc8ae-189">Introduza o nome do novo recurso genérico e, em seguida, selecione **Criar**.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-189">Enter the name of the new generic resource, and then select **Create**.</span></span>

    ![Nome de um novo recurso genérico introduzido](media/Resource-Management-image23.png)

4. <span data-ttu-id="bc8ae-191">Na caixa de diálogo **Criação Rápida: Membro da Equipa do Projeto** que é apresentada, no campo **Função**, selecione a função para o recurso genérico.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-191">In the **Quick Create: Project Team Member** dialog box that appears, in the **Role** field, select the role for the generic resource.</span></span> <span data-ttu-id="bc8ae-192">No campo **Unidade de Atribuição de Recursos**, selecione a unidade organizacional para o recurso genérico.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-192">In the **Resourcing Unit** field, select the organizational unit for the generic resource.</span></span> <span data-ttu-id="bc8ae-193">Em seguida, selecione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-193">Then select **Save**.</span></span>

    ![Caixa de diálogo Criação Rápida: Membro da Equipa do Projeto](media/Resource-Management-image24.png)

    <span data-ttu-id="bc8ae-195">Agora, o membro da equipa genérico está atribuído à tarefa.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-195">The generic team member is now assigned to the task.</span></span>

    ![Membro da equipa genérico atribuído à tarefa](media/Resource-Management-image25.png)

    <span data-ttu-id="bc8ae-197">No separador **Equipa**, verá o novo membro da equipa genérico.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-197">On the **Team** tab, you will see the new generic team member.</span></span> <span data-ttu-id="bc8ae-198">Tenha em atenção que apenas tem horas atribuídas.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-198">Notice that it has only assigned hours.</span></span> <span data-ttu-id="bc8ae-199">Estas horas são a soma de todas as tarefas que estão atribuídas ao membro da equipa genérico.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-199">These hours are the sum of all tasks that are assigned to the generic team member.</span></span> <span data-ttu-id="bc8ae-200">O membro da equipa genérico ainda não tem horas ou um requisito de recurso necessário.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-200">The generic team member doesn't yet have required hours or a resource requirement.</span></span>

    ![Membro da equipa genérico no separador Equipa](media/Resource-Management-image26.png)

5. <span data-ttu-id="bc8ae-202">Agora, pode atribuir o membro da equipa genérico a outras tarefas utilizando o Seletor de Recursos.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-202">You can now assign the generic team member to other tasks by using the Resource Picker.</span></span>

    ![Membro da equipa genérico no Seletor de Recursos](media/Resource-Management-image27.png)

    <span data-ttu-id="bc8ae-204">Quando tiver terminado a atribuição do recurso genérico às tarefas, poderá gerar um requisito de recurso para o recurso genérico.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-204">When you've finished assigning the generic resource to tasks, you can generate a resource requirement for the generic resource.</span></span>

5. <span data-ttu-id="bc8ae-205">No separador **Equipa**, selecione o recurso genérico e, em seguida, selecione **Gerar Requisito**.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-205">On the **Team** tab, select the generic resource, and then select **Generate Requirement**.</span></span>

    ![Comando Gerar Requisito](media/Resource-Management-image28.png)

    <span data-ttu-id="bc8ae-207">Quando o requisito for gerado, o membro da equipa genérico terá as horas necessárias e uma ligação para o requisito de recurso.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-207">When the requirement is generated, the generic team member will have required hours and a link for the resource requirement.</span></span>

    ![Ligação Requisito de recurso](media/Resource-Management-image29.png)

    <span data-ttu-id="bc8ae-209">Depois de reservar um recurso nomeado, o recurso genérico é removido da equipa e é substituído pelo recurso nomeado.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-209">After you book a named resource, the generic resource is removed from the team and replaced by the named resource.</span></span>

    ![Recurso genérico substituído pelo recurso nomeado](media/Resource-Management-image30.png)

    <span data-ttu-id="bc8ae-211">No separador **Agenda**, as atribuições de recursos genéricos são removidas e substituídas pelo recurso nomeado.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-211">On the **Schedule** tab, the generic resource assignments are removed and replaced by the named resource.</span></span>

    ![Atribuições de recursos genéricos substituídas pelo recurso nomeado no separador Agenda](media/Resource-Management-image31.png)

    > [!NOTE]
    > <span data-ttu-id="bc8ae-213">Este comportamento só ocorre quando um recurso nomeado é totalmente reservado para o requisito de recurso genérico.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-213">This behavior occurs only when a named resource is fully booked for the generic resource requirement.</span></span> <span data-ttu-id="bc8ae-214">Quando um recurso nomeado substitui parcialmente o requisito de recurso genérico ou os vários recursos nomeados substituem o requisito de recurso genérico, o recurso genérico permanece atribuído à tarefa.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-214">When either a named resource partially replaces the generic resource requirement or multiple named resources replace the generic resource requirement, the generic resource remains assigned to the task.</span></span>

    <span data-ttu-id="bc8ae-215">Na ilustração seguinte, foi planeada uma tarefa de 80 horas para uma duração de cinco dias (16 horas por dia durante cinco dias) e atribuída ao recurso genérico com o nome **Funcional**.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-215">In the following illustration, an 80-hour task has been planned for a five-day duration (16 hours per day over five days) and assigned to the generic resource that is named **Functional**.</span></span>

    ![Tarefa de oitenta horas e cinco dias atribuída ao recurso genérico Funcional](media/Resource-Management-image32.png)

    <span data-ttu-id="bc8ae-217">Quando gera o requisito, dura 80 horas em cinco dias.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-217">When you generate the requirement, it's for 80 hours over five days.</span></span>

    ![Requisito gerado durante 80 horas durante cinco dias](media/Resource-Management-image33.png)

    <span data-ttu-id="bc8ae-219">Visto que os recursos disponíveis só funcionam oito horas por dia, são necessários dois recursos para cumprir o requisito.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-219">Because available resources work only eight hours per day, two resources are needed to fulfill the requirement.</span></span>

    ![Segundo recurso](media/Resource-Management-image35.png)

    <span data-ttu-id="bc8ae-221">No separador **Equipa**, pode ver que o recurso genérico não tem horas necessárias, mas as horas atribuídas continuam a aparecer juntamente com os dois recursos nomeados que compõem o cumprimento.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-221">On the **Team** tab, you can now see that the generic resource has no required hours, but the assigned hours still appear together with the two named resources that make up the fulfillment.</span></span>

    ![Dois recursos nomeados no separador Equipa](media/Resource-Management-image36.png)

    <span data-ttu-id="bc8ae-223">No separador **Agenda**, o recurso genérico permanece atribuído à tarefa.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-223">On the **Schedule** tab, the generic resource remains assigned to the task.</span></span>

    ![Recursos genéricos no separador Agenda](media/Resource-Management-image37.png)

<span data-ttu-id="bc8ae-225">O PSA não atribui ambos os recursos à tarefa, pois esse comportamento produziria uma agenda menos previsível.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-225">PSA doesn't assign both resources to the task, because that behavior would produce a less predictable schedule.</span></span> <span data-ttu-id="bc8ae-226">Neste exemplo simples, é fácil dividir as horas igualmente entre dois recursos.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-226">In this simple example, it's easy to divide the hours equally between two resources.</span></span> <span data-ttu-id="bc8ae-227">No entanto, em cenários mais complexos que envolvam várias tarefas e vários recursos, o PSA teria de dar suposições sobre como deve alocar as reservas que são recebidas para vários recursos em várias tarefas.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-227">However, in more complex scenarios that involve multiple tasks and multiple resources, PSA would have to make assumptions about how it should allocate the bookings that are received for multiple resources across multiple tasks.</span></span>

<span data-ttu-id="bc8ae-228">Consequentemente, nestes cenários, o gestor de projeto é responsável pela análise de várias reservas e pela atribuição das mesmas, conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-228">Therefore, in these scenarios, the project manager is responsible for parsing the multiple bookings and assigning them as needed.</span></span> <span data-ttu-id="bc8ae-229">Para alocar as reservas, o gestor de projeto atribui as tarefas dos recursos genéricos aos recursos nomeados e, em seguida, utiliza a vista **Reconciliação** para garantir que a alocação funciona com as reservas.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-229">To allocate the bookings, the project manager assigns the tasks from the generic resources to the named resources and then uses the **Reconciliation** view to make sure that the allocation works with the bookings.</span></span>

### <a name="edit-a-resource-requirement"></a><span data-ttu-id="bc8ae-230">Editar um requisito de recurso</span><span class="sxs-lookup"><span data-stu-id="bc8ae-230">Edit a resource requirement</span></span>

<span data-ttu-id="bc8ae-231">Depois de criar um requisito de recurso, um gestor de projeto ou um gestor de recursos poderá pretender editar os detalhes para refinar os critérios de pesquisa quando o Quadro da Agenda for utilizado.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-231">After a resource requirement has been created, a project manager or resource manager might want to edit the details to refine the search criteria when the Schedule Board is used.</span></span> <span data-ttu-id="bc8ae-232">Para editar o requisito de recurso, siga estes passos.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-232">To edit the resource requirement, follow these steps.</span></span>

1. <span data-ttu-id="bc8ae-233">Na página **Projetos**, no separador **Equipa**, selecione a ligação para qualquer requisito num recurso genérico.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-233">On the **Projects** page, on the **Team** tab, select the link to any requirement on a generic resource.</span></span>
2. <span data-ttu-id="bc8ae-234">Na página **Requisito de Recurso** que aparece, pode atualizar vários atributos.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-234">On the **Resource Requirement** page that appears, you can update several attributes.</span></span> <span data-ttu-id="bc8ae-235">Seguem-se alguns exemplos:</span><span class="sxs-lookup"><span data-stu-id="bc8ae-235">Here are some examples:</span></span>

    - <span data-ttu-id="bc8ae-236">Nome</span><span class="sxs-lookup"><span data-stu-id="bc8ae-236">Name</span></span>
    - <span data-ttu-id="bc8ae-237">Da Data</span><span class="sxs-lookup"><span data-stu-id="bc8ae-237">From Date</span></span>
    - <span data-ttu-id="bc8ae-238">À Data</span><span class="sxs-lookup"><span data-stu-id="bc8ae-238">To Date</span></span>
    - <span data-ttu-id="bc8ae-239">Duração</span><span class="sxs-lookup"><span data-stu-id="bc8ae-239">Duration</span></span>
    - <span data-ttu-id="bc8ae-240">Tipo de Recurso</span><span class="sxs-lookup"><span data-stu-id="bc8ae-240">Resource Type</span></span>

<span data-ttu-id="bc8ae-241">Na página **Requisito de Recurso**, o gestor de projeto ou o gestor de recursos também podem definir as seguintes informações:</span><span class="sxs-lookup"><span data-stu-id="bc8ae-241">On the **Resource Requirement** page, the project manager or resource manager can also define the following information:</span></span>

- <span data-ttu-id="bc8ae-242">Competências</span><span class="sxs-lookup"><span data-stu-id="bc8ae-242">Skills</span></span>
- <span data-ttu-id="bc8ae-243">Funções</span><span class="sxs-lookup"><span data-stu-id="bc8ae-243">Roles</span></span>
- <span data-ttu-id="bc8ae-244">Preferências de recurso</span><span class="sxs-lookup"><span data-stu-id="bc8ae-244">Resource preferences</span></span>
- <span data-ttu-id="bc8ae-245">Unidade organizacional preferencial</span><span class="sxs-lookup"><span data-stu-id="bc8ae-245">Preferred organizational unit</span></span>

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a><span data-ttu-id="bc8ae-246">Atualizar as reservas de recursos depois de estarem reservados num projeto</span><span class="sxs-lookup"><span data-stu-id="bc8ae-246">Update resource bookings after they are booked on a project</span></span>

<span data-ttu-id="bc8ae-247">Depois de ter adicionado um recurso genérico ou nomeado a uma equipa do projeto, pode alterar as reservas do recurso.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-247">After you've added a generic or named resource to a project team, you can change the resource's bookings.</span></span>

1. <span data-ttu-id="bc8ae-248">Na página **Projetos**, no separador **Equipa**, selecione um membro da equipa e, em seguida, selecione **Manter Reservas**.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-248">On the **Projects** page, on the **Team** tab, select a team member, and then select **Maintain Bookings**.</span></span>

    ![Quadro da Agenda aberto para o membro da equipa selecionado](media/Resource-Management-image40.png)

    <span data-ttu-id="bc8ae-250">O Quadro da Agenda é apresentado e mostra as reservas do membro da equipa do projeto.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-250">The Schedule Board appears and shows the project team member's bookings.</span></span> <span data-ttu-id="bc8ae-251">Expanda o registo do membro da equipa para ver as horas que foram reservadas para este projeto e outros projetos que estão a consumir a capacidade do membro da equipa.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-251">Expand the team member's record to view the hours that have been booked against this project and other projects that are consuming the team member's capacity.</span></span>

2. <span data-ttu-id="bc8ae-252">Selecione e arraste a reserva para expandir ou reduzir o seu tamanho.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-252">Select and drag the booking to extend or shorten it.</span></span> <span data-ttu-id="bc8ae-253">É apresentada a caixa de diálogo **Criar Reserva de Recursos** que lhe permite ajustar a reserva.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-253">A **Create Resource Booking** dialog box appears that lets you adjust the booking.</span></span>

    ![Caixa de diálogo Criar Reserva de Recursos](media/Resource-Management-image41.png)

3. <span data-ttu-id="bc8ae-255">Clique com o botão direito do rato na reserva.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-255">Right-click the booking.</span></span> <span data-ttu-id="bc8ae-256">Em seguida, pode utilizar o menu de atalho para concluir as seguintes ações:</span><span class="sxs-lookup"><span data-stu-id="bc8ae-256">You can then use the shortcut menu to complete the following actions:</span></span>

    - <span data-ttu-id="bc8ae-257">Altere o estado da reserva.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-257">Change the booking status.</span></span>
    - <span data-ttu-id="bc8ae-258">Edite a reserva.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-258">Edit the booking.</span></span>
    - <span data-ttu-id="bc8ae-259">Substitua um recurso na equipa do projeto.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-259">Substitute a resource on the project team.</span></span>

### <a name="change-the-booking-status"></a><span data-ttu-id="bc8ae-260">Alterar o estado da reserva</span><span class="sxs-lookup"><span data-stu-id="bc8ae-260">Change the booking status</span></span>

<span data-ttu-id="bc8ae-261">Pode alterar qualquer estado da reserva predefinido ou personalizado.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-261">You can change any default or custom booking status.</span></span>

![Comando Alterar Estado](media/Resource-Management-image42.png)

<span data-ttu-id="bc8ae-263">Os seguintes estados estão incluídos no PSA:</span><span class="sxs-lookup"><span data-stu-id="bc8ae-263">The following statuses are included in PSA:</span></span>

- <span data-ttu-id="bc8ae-264">**Cancelado** – Este estado cancela a reserva de um recurso e liberta a capacidade do recurso.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-264">**Canceled** – This status cancels a resource's booking and frees up the resource's capacity.</span></span>
- <span data-ttu-id="bc8ae-265">**Reserva Fixa** – Este estado consome a capacidade de um recurso.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-265">**Hard Book** – This status consumes a resource's capacity.</span></span> <span data-ttu-id="bc8ae-266">Normalmente, uma reserva tem este estado quando abre **Manter Reservas** a partir da grelha **Todos os Membros da Equipa** na página **Projetos**.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-266">A booking typically has this status when you open **Maintain Bookings** from the **All Team Members** grid on the **Projects** page.</span></span>
- <span data-ttu-id="bc8ae-267">**Reserva Flexível** – Este estado adiciona um recurso a uma equipa, mas não consome a capacidade do recurso.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-267">**Soft Book** – This status adds a resource to a team but doesn't consume the resource's capacity.</span></span> <span data-ttu-id="bc8ae-268">Indica que o recurso foi reservado para trabalho potencial, mas ainda tem capacidade se for necessário em outras tarefas.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-268">It indicates that the resource has been reserved for potential work but still has capacity if it's needed on other jobs.</span></span> <span data-ttu-id="bc8ae-269">Na vista da disponibilidade geral do recurso, as reservas flexíveis têm um estado diferente das reservas fixas.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-269">In the view of overall resource availability, soft bookings have a different status than hard bookings.</span></span>
- <span data-ttu-id="bc8ae-270">**Proposto** – Este estado representa a proposta do gestor de recursos ou do gestor de projeto para um recurso.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-270">**Proposed** – This status represents a resource manager's or project manager's proposal for a resource.</span></span> <span data-ttu-id="bc8ae-271">As propostas não consomem a capacidade de um recurso e o recurso não é adicionado à equipa do projeto.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-271">Proposals don't consume the capacity of a resource, and the resource isn't added to the project team.</span></span> <span data-ttu-id="bc8ae-272">Para efetuar a reserva fixa do recurso na equipa, o gestor de projeto tem de aceitar a proposta.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-272">To hard-book the resource on the team, the project manager must accept the proposal.</span></span>

### <a name="submit-resource-requests"></a><span data-ttu-id="bc8ae-273">Submeter pedidos de recursos</span><span class="sxs-lookup"><span data-stu-id="bc8ae-273">Submit resource requests</span></span>

<span data-ttu-id="bc8ae-274">Os pedidos de recursos são utilizados para transportar a procura (requisito de recurso) que tem de ser cumprida por um gestor de recursos.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-274">Resource requests are used to carry the demand (resource requirement) that must be fulfilled by a resource manager.</span></span> <span data-ttu-id="bc8ae-275">No caso de um recurso genérico que já esteja na equipa, pode submeter diretamente um pedido de recurso.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-275">For a generic resource that is already on the team, you can submit a resource request directly.</span></span> <span data-ttu-id="bc8ae-276">Um pedido de recurso pode ser cumprido de duas formas:</span><span class="sxs-lookup"><span data-stu-id="bc8ae-276">A resource request can be fulfilled in two ways:</span></span>

- <span data-ttu-id="bc8ae-277">O gestor de recursos cumpre diretamente o pedido.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-277">The resource manager directly fulfills the request.</span></span> <span data-ttu-id="bc8ae-278">Neste caso, o recurso genérico é substituído por uma reserva fixa que tem um recurso nomeado.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-278">In this case, the generic resource is replaced by a hard booking that has a named resource.</span></span>
- <span data-ttu-id="bc8ae-279">O gestor de recursos propõe um recurso ao gestor de projeto e o gestor de projeto aprova ou rejeita o recurso proposto.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-279">The resource manager proposes a resource to the project manager, and the project manager approves or rejects the proposed resource.</span></span>

#### <a name="direct-fulfillment-of-resource-requests"></a><span data-ttu-id="bc8ae-280">Cumprimento direto de pedidos de recursos</span><span class="sxs-lookup"><span data-stu-id="bc8ae-280">Direct fulfillment of resource requests</span></span>

<span data-ttu-id="bc8ae-281">Quando um requisito de recurso é gerado, um gestor de projeto pode submeter um pedido de recurso para um recurso genérico selecionando o recurso e, em seguida, selecionando **Submeter Pedido**.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-281">When a resource requirement is generated, a project manager can submit a resource request for a generic resource by selecting the resource and then selecting **Submit Request**.</span></span>

![Botão Submeter Pedido](media/Resource-Management-image45.png)

<span data-ttu-id="bc8ae-283">Os comentários sobre o recurso podem ser fornecidos ao gestor de recursos que está a cumprir o pedido.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-283">Comments about the resource can be provided to the resource manager who is fulfilling the request.</span></span> <span data-ttu-id="bc8ae-284">Depois de o pedido ser submetido, o campo **Estado** para o membro da equipa é alterado para **Submetido**.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-284">After the request is submitted, the **Status** field for the team member is changed to **Submitted**.</span></span>

![Introduzir comentários opcionais](media/Resource-Management-image46.png)

<span data-ttu-id="bc8ae-286">Quando o gestor de recursos cumpre o pedido, o membro da equipa genérico é substituído pelo recurso nomeado na grelha **Todos os Membros da Equipa**.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-286">When the resource manager fulfills the request, the generic team member is replaced by the named resource in the **All Team Members** grid.</span></span>

![Membro da equipa genérico substituído pelo recurso nomeado na grelha Todos os Membros da Equipa](media/Resource-Management-image47.png)

#### <a name="use-a-resource-proposal-for-resource-requests"></a><span data-ttu-id="bc8ae-288">Utilizar uma proposta de recursos para pedidos de recursos</span><span class="sxs-lookup"><span data-stu-id="bc8ae-288">Use a resource proposal for resource requests</span></span>

<span data-ttu-id="bc8ae-289">Em vez de reservar diretamente um recurso num pedido de recurso, um gestor de recursos pode propor um recurso ao gestor de projeto.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-289">Instead of directly booking a resource on a resource request, a resource manager can propose a resource to the project manager.</span></span> <span data-ttu-id="bc8ae-290">Um gestor de recursos poderá utilizar esta opção quando não estiver disponível uma correspondência exata para os requisitos.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-290">A resource manager might use this option when an exact match for the requirements isn't available.</span></span> <span data-ttu-id="bc8ae-291">Quando um gestor de recursos propõe um recurso, o gestor de projeto vê que o campo **Estado** do membro da equipa genérico é alterado para **Necessita de Revisão**.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-291">When a resource manager proposes a resource, the project manager sees that the **Status** field for the generic team member is changed to **Needs Review**.</span></span>

![Estado do membro da equipa genérico alterado para Necessita de Revisão](media/Resource-Management-image48.png)

<span data-ttu-id="bc8ae-293">Para ver o recurso proposto juntamente com uma visualização do efeito da reserva da proposta, faça duplo clique no membro da equipa que tem o estado **Necessita de Revisão**.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-293">To view the proposed resource together with a visualization of the effect of the proposal's booking, double-click the team member that has a status of **Needs Review**.</span></span> <span data-ttu-id="bc8ae-294">Em seguida, selecione o separador **Recursos Propostos**.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-294">Then select the **Proposed Resources** tab.</span></span>

![Separador Recursos Propostos](media/Resource-Management-image49.png)

<span data-ttu-id="bc8ae-296">Selecione **Aceitar Todas as Propostas** para aceitar todos os recursos propostos ou **Rejeitar Todas as Propostas** para rejeitá-los.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-296">Select **Accept All Proposals** to accept all proposed resources or **Reject All Proposals** to reject them.</span></span> <span data-ttu-id="bc8ae-297">Se aceitar os recursos propostos, estes serão reservados de forma fixa no projeto como membros da equipa e substituem os recursos genéricos.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-297">If you accept the proposed resources, they are hard-booked on the project as team members and replace the generic resources.</span></span>

> [!NOTE]
> <span data-ttu-id="bc8ae-298">Tem de aceitar ou rejeitar todos os recursos propostos.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-298">You must either accept or reject all proposed resources.</span></span> <span data-ttu-id="bc8ae-299">Não é possível aceitá-los ou rejeitá-los parcialmente.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-299">You can't partially accept or reject them.</span></span>

### <a name="substitute-a-resource-on-the-project-team"></a><span data-ttu-id="bc8ae-300">Substituir um recurso na equipa do projeto</span><span class="sxs-lookup"><span data-stu-id="bc8ae-300">Substitute a resource on the project team</span></span>

<span data-ttu-id="bc8ae-301">Por vezes, um gestor de projeto tem de substituir um membro da equipa reservado num projeto.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-301">Sometimes, a project manager must substitute a booked team member on a project.</span></span>

1. <span data-ttu-id="bc8ae-302">Na página **Projetos**, no separador **Equipa**, selecione o recurso que necessita de um substituto e, em seguida, selecione **Manter Reservas**.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-302">On the **Projects** page, on the **Team** tab, select the resource that needs a substitute, and then select **Maintain Bookings**.</span></span>
2. <span data-ttu-id="bc8ae-303">Expanda o recurso para ver os projetos aos quais está atribuído.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-303">Expand the resource to view the projects that it's assigned to.</span></span>

    ![Recurso expandido para mostrar os projetos atribuídos](media/Resource-Management-image50.png)

3. <span data-ttu-id="bc8ae-305">Clique com o botão direito do rato no projeto e selecione **Substituir Recurso**.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-305">Right-click the project, and then select **Substitute Resource**.</span></span>
4. <span data-ttu-id="bc8ae-306">Se souber o recurso que pretende substituir pelo recurso atual, selecione ou escreva o nome e, em seguida, selecione **Reatribuir**.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-306">If you know the resource that you want to substitute for the current resource, select or type the name, and then select **Re-assign**.</span></span>

    ![Especificar um recurso substituto](media/Resource-Management-image51.png)

    <span data-ttu-id="bc8ae-308">Em alternativa, siga estes passos para procurar um recurso:</span><span class="sxs-lookup"><span data-stu-id="bc8ae-308">Alternatively, follow these steps to search for a resource:</span></span>

    1. <span data-ttu-id="bc8ae-309">Selecione **Localizar Substituição**.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-309">Select **Find Substitution**.</span></span>

        ![Procurar um recurso substituto](media/Resource-Management-image52.png)

        <span data-ttu-id="bc8ae-311">O Assistente da Agenda devolve uma lista de substitutos disponíveis.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-311">The Schedule Assistant returns a list of available substitutes.</span></span> <span data-ttu-id="bc8ae-312">No Assistente da Agenda, pode filtrar ainda mais os recursos disponíveis para localizar um substituto adequado.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-312">In the Schedule Assistant, you can further filter the available resources to find a suitable substitute.</span></span>

        ![Lista de substitutos disponíveis](media/Resource-Management-image53.png)

    2. <span data-ttu-id="bc8ae-314">Para substituir o recurso, selecione o recurso pretendido e, em seguida, selecione **Substituir**.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-314">To substitute the resource, select the resource that you want, and then select **Substitute**.</span></span>

        ![Recurso substituto selecionado](media/Resource-Management-image54.png)

    <span data-ttu-id="bc8ae-316">As reservas e as atribuições são substituídas pelo novo recurso.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-316">The bookings and assignments are substituted with the new resource.</span></span>

    ![Reservas e atribuições substituídas pelo novo recurso](media/Resource-Management-image55.png)

## <a name="reconcile-team-member-bookings-and-assignments"></a><span data-ttu-id="bc8ae-318">Reconciliar reservas e atribuições de membros da equipa</span><span class="sxs-lookup"><span data-stu-id="bc8ae-318">Reconcile team member bookings and assignments</span></span>

<span data-ttu-id="bc8ae-319">Quanto aos membros da equipa, as reservas e as atribuições têm uma ligação fraca.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-319">For team members, bookings and assignments are loosely coupled.</span></span> <span data-ttu-id="bc8ae-320">Por outras palavras, os recursos podem ter atribuições, mas não reservas, ou podem ter reservas, mas não atribuições.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-320">In other words, resources can have assignments but no bookings, or they can have bookings but no assignments.</span></span> <span data-ttu-id="bc8ae-321">Idealmente, as reservas e atribuições devem ser alinhadas, para que os recursos tenham capacidade comprometida para executar as atribuições de tarefas.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-321">Ideally, bookings and assignments should be aligned, so that resources have committed capacity to perform the task assignments.</span></span> <span data-ttu-id="bc8ae-322">No entanto, as reservas podem basear-se na disponibilidade e as temporizações das tarefas podem mudar à medida que o projeto continua.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-322">However, the bookings might be based on availability, and task timings might change as the project continues.</span></span> <span data-ttu-id="bc8ae-323">Portanto, a ligação fraca de reservas e atribuições fornece flexibilidade.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-323">Therefore, the loose coupling of bookings and assignments provides flexibility.</span></span>

<span data-ttu-id="bc8ae-324">O PSA tem um separador **Reconciliação** que permite que os gestores de projeto reconciliem os reservas de membros da equipa e as respetivas atribuições para as equipas do projeto.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-324">PSA has a **Reconciliation** tab that lets project managers reconcile team members' bookings and their assignments for project teams.</span></span>

![Separador Reconciliação](media/Resource-Management-image56.png)

<span data-ttu-id="bc8ae-326">O separador **Reconciliação** mostra as reservas e as atribuições até ao nível da atribuição de tarefas individuais para cada membro da equipa.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-326">The **Reconciliation** tab shows bookings and assignments down to the level of the individual task assignment for each team member.</span></span> <span data-ttu-id="bc8ae-327">Mostra horas nas células que representam períodos de meses a dias.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-327">It shows hours in cells that represent time periods from months down to days.</span></span>

<span data-ttu-id="bc8ae-328">O separador também mostra um total líquido global para o projeto, juntamente com uma coluna total.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-328">The tab also shows an overall net total for the project, together with a total column.</span></span>

<span data-ttu-id="bc8ae-329">Para cada recurso, o separador calcula a diferença entre as reservas do membro da equipa e um rollup das atribuições de tarefas do membro da equipa.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-329">For each resource, the tab calculates the difference between the team member's bookings and a rollup of the team member's task assignments.</span></span> <span data-ttu-id="bc8ae-330">O ideal é que esta diferença seja 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="bc8ae-330">Ideally, this difference should be 0 (zero).</span></span> <span data-ttu-id="bc8ae-331">Por outras palavras, não deve haver diferença entre as reservas e as atribuições.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-331">In other words, there should be no difference between bookings and assignments.</span></span> <span data-ttu-id="bc8ae-332">As diferenças são coloridas e sombreadas para chamar a atenção para duas condições:</span><span class="sxs-lookup"><span data-stu-id="bc8ae-332">Differences are colored and shaded to draw attention to two conditions:</span></span>

- <span data-ttu-id="bc8ae-333">**Falta de reserva** – Uma falta de reserva ocorre quando um recurso tem mais atribuições do que reservas.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-333">**Booking shortage** – A booking shortage occurs when a resource has more assignments than bookings.</span></span> <span data-ttu-id="bc8ae-334">Como essa capacidade não foi reservada, um gestor de projeto pode querer corrigir esta condição, expandindo as reservas do recurso para cobrir o deficit.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-334">Because this capacity hasn't been reserved, a project manager might want to correct this condition by extending the resource's bookings to cover the deficit.</span></span>
- <span data-ttu-id="bc8ae-335">**Reservas em excesso** – As reservas em excesso ocorrem quando um recurso foi reservado para o projeto, mas ainda não foi atribuído às tarefas.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-335">**Excess bookings** – Excess bookings occur when a resource has been booked to the project but hasn't been assigned to tasks.</span></span> <span data-ttu-id="bc8ae-336">Esta condição poderá ser aceitável nos casos em que o recurso esteve reservado para o projeto antes da atribuição de tarefas.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-336">This condition might be acceptable in the cases where the resource was booked to the project before task assignment occurred.</span></span> <span data-ttu-id="bc8ae-337">No entanto, em outros casos, o recurso não está planeado para ser atribuído a tarefas.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-337">However, in other cases, the resource isn't planned to be assigned to tasks.</span></span> <span data-ttu-id="bc8ae-338">Nestes casos, o gestor de projeto deverá considerar o cancelamento das reservas do recurso, para que a capacidade possa ser utilizada para outro projeto.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-338">In these cases, the project manager should consider canceling the resource's bookings, so that the capacity can be used for another project.</span></span>

<span data-ttu-id="bc8ae-339">Em alguns casos, quando visualiza o tempo num nível superior ao nível do dia (por exemplo, o nível de mês), poderá ver uma diferença líquida de zero para um recurso (por outras palavras, reservas = atribuições).</span><span class="sxs-lookup"><span data-stu-id="bc8ae-339">In some cases, when you view time at a higher level than the day level (for example, the month level), you might see a net difference of zero for a resource (in other words, bookings = assignments).</span></span> <span data-ttu-id="bc8ae-340">No entanto, se visualizar o tempo no nível da semana, poderá ver que existem atribuições de zero horas e reservas de 40 horas na primeira semana, mas atribuições de 40 horas e reservas de zero horas na segunda semana.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-340">However, if you view time at the week level, you might see that there are assignments of zero hours and bookings of 40 hours in the first week, but assignments of 40 hours and bookings of zero hours in the second week.</span></span> <span data-ttu-id="bc8ae-341">Globalmente, as reservas e as atribuições são reconciliadas, mas diferem de uma semana para a seguinte.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-341">Overall, the bookings and assignments are reconciled, but they differ from one week to the next.</span></span>

<span data-ttu-id="bc8ae-342">Quando visualiza o tempo em níveis superiores, as células no separador **Reconciliação** têm um indicador para informá-lo de que existem diferenças em níveis inferiores.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-342">When you view time at higher levels, cells in the **Reconciliation** tab have an indicator to inform you that there are differences at lower levels.</span></span> <span data-ttu-id="bc8ae-343">Ao clicar duas vezes numa célula, pode ampliar para ver a diferença.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-343">By double-clicking in a cell, you can zoom in to view the difference.</span></span> <span data-ttu-id="bc8ae-344">Em seguida, pode clicar com o botão direito do rato para reduzir. Ao selecionar um recurso e, em seguida, utilizar o controlo **Diferença seguinte** na barra de ferramentas de grelha, pode ir para a próxima diferença entre as reservas e as atribuições para esse recurso.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-344">You can then right-click to zoom out. By selecting a resource and then using the **Next difference** control on the grid toolbar, you can go to the next difference between bookings and assignments for that resource.</span></span> <span data-ttu-id="bc8ae-345">Em seguida, pode utilizar o controlo **Diferença anterior** para voltar.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-345">You can then use the **Previous difference** control to go back.</span></span> <span data-ttu-id="bc8ae-346">Também pode desativar o indicador de diferença e o comportamento de navegação em **Definições**.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-346">You can also turn off the difference indicator and navigation behavior under **Settings**.</span></span>

![Indicador de diferença](media/Resource-Management-image57.png)

<span data-ttu-id="bc8ae-348">Se tiver atribuições de tarefas para um recurso, mas não tiver reservas, na página **Projetos**, no separador **Reconciliação**, selecione a falta de reserva e, em seguida, selecione **Expandir Reserva**.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-348">If you have task assignments for a resource but no bookings, on the **Projects** page, on the **Reconciliation** tab, select the booking shortage, and then select **Extend Booking**.</span></span> <span data-ttu-id="bc8ae-349">É apresentada a caixa de diálogo **Falta de Reserva** e mostra a reserva necessária para resolver a falta do recurso.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-349">The **Extend Booking** dialog box appears and shows the booking that is needed to address the resource's shortage.</span></span> <span data-ttu-id="bc8ae-350">Também mostra as reservas existentes do recurso em todos os projetos ou outras entidades agendáveis.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-350">It also shows the resource's existing bookings across all projects or other schedulable entities.</span></span> <span data-ttu-id="bc8ae-351">Se selecionar **OK** para criar a reserva para o recurso, independentemente da disponibilidade do recurso, poderá causar uma reserva em excesso.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-351">If you select **OK** to create the booking for the resource, regardless of that resource's availability, you might cause overbooking.</span></span>

![Caixa de diálogo Expandir Reserva](media/Resource-Management-image58.png)

<span data-ttu-id="bc8ae-353">Em seguida, o gestor de projeto ou o gestor de recursos pode utilizar o Quadro da Agenda para gerir qualquer situação em que um recurso tenha uma reserva em excesso além da sua capacidade.</span><span class="sxs-lookup"><span data-stu-id="bc8ae-353">The project manager or resource manager can then use the Schedule Board to manage any situations where a resource is overbooked beyond its capacity.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]