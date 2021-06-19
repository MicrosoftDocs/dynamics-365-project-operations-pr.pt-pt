---
title: Estimar vendas e custos do projeto quando um recurso reservável preenche várias funções num projeto
description: Este tópico fornece informação sobre como podem ser usadas as dimensões dos preços para suportar as estimativas de preços e custos para um recurso que preenche várias funções num projeto.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 5b2b57f5268a92168952b6da5123886df70cd4e2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013275"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-for-a-project"></a><span data-ttu-id="67f74-103">Estimar vendas e custos do projeto quando um recurso reservável preenche várias funções num projeto</span><span class="sxs-lookup"><span data-stu-id="67f74-103">Estimate project sales and costs when a bookable resource fills multiple roles for a project</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="67f74-104">As empresas baseadas em projetos têm muitas vezes a necessidade que um recurso realize várias funções num projeto.</span><span class="sxs-lookup"><span data-stu-id="67f74-104">Project-based companies often have the need for one resource to perform multiple roles on a project.</span></span> <span data-ttu-id="67f74-105">Cada uma destas funções poderia ser avaliada e ter custos diferentes, o que significa que o tempo do mesmo recurso no projeto poderia obter uma estimativa financeira diferente, dependendo da fatura e das taxas de custo para cada uma das funções.</span><span class="sxs-lookup"><span data-stu-id="67f74-105">Each of these roles could be priced and costed differently, which means the same resource's time on the project could get a different financial estimate depending on the bill and cost rates for each of the roles.</span></span> <span data-ttu-id="67f74-106">O Project Service Automation permite a configuração dos valores no registo do membro da equipa para o recurso nomeado e permite diferentes substituições em cada uma das tarefas a que o membro da equipa está atribuído.</span><span class="sxs-lookup"><span data-stu-id="67f74-106">Project Service Automation allows the setup of the values on the team member record for the named resource and allows for different overrides on each of the tasks that the team member is assigned to.</span></span>

<span data-ttu-id="67f74-107">O exemplo seguinte explica como a simples sobreposição deste valor permite que um recurso tenha múltiplas funções num projeto com diferentes taxas de custo e faturação.</span><span class="sxs-lookup"><span data-stu-id="67f74-107">The following example  explains how the simple override of this value allows a resource to have multiple roles on a project with different cost and bill rates.</span></span>

## <a name="create-tasks"></a><span data-ttu-id="67f74-108">Criar tarefas</span><span class="sxs-lookup"><span data-stu-id="67f74-108">Create tasks</span></span>
<span data-ttu-id="67f74-109">Criar duas tarefas de projeto durante 40 horas cada, Tarefa A e Tarefa B. Selecione a Tarefa A como antecessora da Tarefa B.</span><span class="sxs-lookup"><span data-stu-id="67f74-109">Create two project tasks for 40 hours each, Task A and Task B. Select Task A as a predecessor to Task B.</span></span>

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a><span data-ttu-id="67f74-110">Configurar Função e Unidade da Organização para um membro da equipa de projeto genérico</span><span class="sxs-lookup"><span data-stu-id="67f74-110">Set up Role and Organization Unit for a generic project team member</span></span>

1. <span data-ttu-id="67f74-111">Na página **Agendar**, selecione a linha **Tarefa** para a Tarefa A.</span><span class="sxs-lookup"><span data-stu-id="67f74-111">On the **Schedule** page, select the **Task** row for Task A.</span></span> 
2. <span data-ttu-id="67f74-112">No campo **Recursos**, selecione **Criar** na lista de pendente.</span><span class="sxs-lookup"><span data-stu-id="67f74-112">In the **Resources** field, select **Create** in the drop-down list.</span></span>
3. <span data-ttu-id="67f74-113">Na página **Criação Rápida do Membro da Equipa**, especifique os atributos do membro da equipa genérico que pode executar esta tarefa.</span><span class="sxs-lookup"><span data-stu-id="67f74-113">On the **Team Member Quick Create** page, specify the attributes of the generic team member who can perform this task.</span></span>
4. <span data-ttu-id="67f74-114">Selecione a função e a unidade organizacional apropriadas e, em seguida, selecione **Guardar e Fechar**.</span><span class="sxs-lookup"><span data-stu-id="67f74-114">Select the appropriate role and organizational unit, and then select **Save and Close**.</span></span> <span data-ttu-id="67f74-115">Um membro da equipa genérico é criado e atribuído a esta tarefa.</span><span class="sxs-lookup"><span data-stu-id="67f74-115">A generic team member is created and assigned to this task.</span></span> 

<span data-ttu-id="67f74-116">Repita estes passos para a Tarefa B e certifique-se de que a função e a unidade organizacional no membro da equipa genérico criado para a Tarefa B é diferente da Tarefa A.</span><span class="sxs-lookup"><span data-stu-id="67f74-116">Repeat these steps for Task B and make sure that the role and organizational unit on the generic team member created for Task B is different than Task A.</span></span> 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a><span data-ttu-id="67f74-117">Configurar função e unidade da organização para uma tarefa de projeto</span><span class="sxs-lookup"><span data-stu-id="67f74-117">Set up role and organization unit for a project task</span></span>

1. <span data-ttu-id="67f74-118">Depois de criar a Tarefa A, selecione a tarefa e, em seguida, selecione **Editar tarefa**.</span><span class="sxs-lookup"><span data-stu-id="67f74-118">After you create Task A, select the task, and then select **Edit task**.</span></span>
2. <span data-ttu-id="67f74-119">Na página **Detalhes da Tarefa**, encontre os campos **Função** e **Unidade Organizacional**, adicione os valores necessários para que um recurso que executaria esta tarefa.</span><span class="sxs-lookup"><span data-stu-id="67f74-119">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="67f74-120">Se estiver a completar estes cenários utilizando dados de demonstração do Project Service Automation, selecione **Líder de Consultoria** como função e **Fabrikam US** como unidade organizacional.</span><span class="sxs-lookup"><span data-stu-id="67f74-120">If you are completing this scenarios using Project Service Automation demo data, select **Consulting Lead** for the role, and **Fabrikam US** as the organizational unit.</span></span>

3. <span data-ttu-id="67f74-121">Selecione Tarefa B e, em seguida, selecione **Editar tarefa**.</span><span class="sxs-lookup"><span data-stu-id="67f74-121">Select Task B and then select **Edit task**.</span></span>
4. <span data-ttu-id="67f74-122">Na página **Detalhes da Tarefa**, encontre os campos **Função** e **Unidade Organizacional**, adicione os valores necessários para que um recurso que executaria esta tarefa.</span><span class="sxs-lookup"><span data-stu-id="67f74-122">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> <span data-ttu-id="67f74-123">Certifique-se de que os valores nos campos **Função** e **Unidade organizacional** sejam diferentes para a Tarefa B dos valores da Tarefa A.</span><span class="sxs-lookup"><span data-stu-id="67f74-123">Make sure that the values in the **Role** and **Organizational Unit** fields are different for Task B from the values for Task A.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="67f74-124">Se estiver a completar estes cenários utilizando dados de demonstração do Project Service Automation, selecione **Técnico de Rede** como função e **Fabrikam US** como unidade organizacional.</span><span class="sxs-lookup"><span data-stu-id="67f74-124">If you are completing this scenarios using Project Service Automation demo data, select **Network Technician** for the role, and **Fabrikam US** as the organizational unit.</span></span>

5. <span data-ttu-id="67f74-125">Guarde e feche a página **Detalhes da Tarefa**.</span><span class="sxs-lookup"><span data-stu-id="67f74-125">Save and close the **Task Details** page.</span></span> 

## <a name="team-member-and-estimates-behavior"></a><span data-ttu-id="67f74-126">Comportamento de membro da equipa e estimativa</span><span class="sxs-lookup"><span data-stu-id="67f74-126">Team member and estimates behavior</span></span> 

1. <span data-ttu-id="67f74-127">Na página **Dados da Tarefa**, em **Membro da Equipa**, selecione os dois membros da equipa genéricos e, em seguida, selecione **Gerar Requisitos**.</span><span class="sxs-lookup"><span data-stu-id="67f74-127">On the **Task Details** page, on the **Team Member**, select the two generic team Members and then select **Generate Requirements**.</span></span> 
2. <span data-ttu-id="67f74-128">Selecione a linha de membro da equipa de **Líder de Consultoria** e, em seguida, selecione **Reservar**.</span><span class="sxs-lookup"><span data-stu-id="67f74-128">Select the team member row for **Consulting Lead** and then select **Book**.</span></span> <span data-ttu-id="67f74-129">O quadro da agenda é aberto e reserva um recurso para esse requisito.</span><span class="sxs-lookup"><span data-stu-id="67f74-129">The schedule board opens and books a resource to that requirement.</span></span>
3. <span data-ttu-id="67f74-130">Selecione a linha de membro da equipa de **Técnico de Rede** e, em seguida, selecione **Reservar**.</span><span class="sxs-lookup"><span data-stu-id="67f74-130">Select the team member row for **Network Technician** and the select **Book**.</span></span> <span data-ttu-id="67f74-131">O quadro da agenda é aberto e reserva o mesmo recurso nesse requisito.</span><span class="sxs-lookup"><span data-stu-id="67f74-131">The schedule board opens and books the same resource on that requirement.</span></span>

### <a name="team-member-grid"></a><span data-ttu-id="67f74-132">Grelha Membro da Equipa</span><span class="sxs-lookup"><span data-stu-id="67f74-132">Team Member grid</span></span> 
<span data-ttu-id="67f74-133">Na grelha **Membro da Equipa**, note que os dois registos de membros da equipa genéricos são eliminados e foram substituídos por um recurso.</span><span class="sxs-lookup"><span data-stu-id="67f74-133">On the **Team Member** grid, notice that the two generic team member records are deleted and have been replaced one resource.</span></span> <span data-ttu-id="67f74-134">Há um conjunto de valores para esse recurso que mostra um conjunto padrão de valores para **Função** e **Unidade Organizacional**.</span><span class="sxs-lookup"><span data-stu-id="67f74-134">There is one set of values for that resource that shows a default set of values for **Role** and **Organizational Unit**.</span></span>
<span data-ttu-id="67f74-135">Quando expandir a linha desse registo de Membro da Equipa, pode ver atribuições distintas no registo do membro da equipa para ambas as tarefas.</span><span class="sxs-lookup"><span data-stu-id="67f74-135">When you expand the row of that Team Member record, you can see distinct assignments on the team member record for both of those tasks.</span></span> <span data-ttu-id="67f74-136">Cada linha de atribuição tem valores específicos de tarefa para **Função** e **Unidade Organizacional**.</span><span class="sxs-lookup"><span data-stu-id="67f74-136">Each assignment row has task-specific values for **Role** and **Organizational Unit**.</span></span> 

### <a name="estimates-grid"></a><span data-ttu-id="67f74-137">Grelha Estimativas</span><span class="sxs-lookup"><span data-stu-id="67f74-137">Estimates grid</span></span> 
<span data-ttu-id="67f74-138">Ao navegar para a grelha **Estimativas**, notará que ambas as atribuições para o mesmo recurso têm um preço diferente.</span><span class="sxs-lookup"><span data-stu-id="67f74-138">When you navigate to the **Estimates** grid, you will notice that both assignments for the same resource are priced differently.</span></span>
<span data-ttu-id="67f74-139">A atribuição do recurso na Tarefa A tem o preço utilizando o valor de atributo **Função** de **Líder de Consultoria**.</span><span class="sxs-lookup"><span data-stu-id="67f74-139">The assignment for the resource on Task A is priced using the **Role** attribute value of **Consulting Lead**.</span></span> <span data-ttu-id="67f74-140">A atribuição do mesmo recurso na Tarefa B tem o preço utilizando o valor de atributo **Função** de **Técnico de Rede**.</span><span class="sxs-lookup"><span data-stu-id="67f74-140">The assignment for the same resource on Task B is priced using the **Role** attribute value of **Network Technician**.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]