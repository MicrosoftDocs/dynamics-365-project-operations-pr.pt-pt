---
title: Atribuir um recurso a uma tarefa
description: Este tópico fornece informações sobre como atribuir recursos a tarefas.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
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
ms.openlocfilehash: 486371df2de8b400f200dbf38e66cb5e2dec7ae7
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286262"
---
# <a name="assign-a-resource-to-a-task"></a><span data-ttu-id="57f85-103">Atribuir um recurso a uma tarefa</span><span class="sxs-lookup"><span data-stu-id="57f85-103">Assign a resource to a task</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="57f85-104">Existem três formas de atribuir um recurso a uma tarefa no Microsoft Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="57f85-104">There are three ways to assign a resource to a task in Microsoft Dynamics 365 Project Service Automation.</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="57f85-105">Reservar um recurso como um membro da equipa e, em seguida, atribuir o recurso a uma tarefa</span><span class="sxs-lookup"><span data-stu-id="57f85-105">Book a resource as a team member, and then assign the resource to a task</span></span>

<span data-ttu-id="57f85-106">Pode adicionar um recurso à equipa do projeto e, em seguida, atribuir o recurso a tarefas na agenda do projeto.</span><span class="sxs-lookup"><span data-stu-id="57f85-106">You can add a resource to the project team, and then assign the resource to tasks in the project schedule.</span></span>

1. <span data-ttu-id="57f85-107">No separador **Membro da Equipa**, adicione um membro da equipa novo selecionando **Novo**.</span><span class="sxs-lookup"><span data-stu-id="57f85-107">On the **Team Member** tab, add a new team member by selecting **New**.</span></span> 

2. <span data-ttu-id="57f85-108">Abre-se o painel **Criação Rápida de Membros da Equipa**, onde pode selecionar o nome de recurso reservável e definir uma função.</span><span class="sxs-lookup"><span data-stu-id="57f85-108">The **Team Member Quick Create** panel opens, where you can select the bookable resource name and set a role.</span></span> 

    <span data-ttu-id="57f85-109">Escolha um dos seguintes métodos de alocação para a reserva do recurso:</span><span class="sxs-lookup"><span data-stu-id="57f85-109">Select one of the following allocation methods for the resource’s booking:</span></span>

    - <span data-ttu-id="57f85-110">**Capacidade Total** reserva a capacidade total do recurso para as datas de e para especificadas.</span><span class="sxs-lookup"><span data-stu-id="57f85-110">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="57f85-111">**Capacidade de Percentagem** reserva o recurso para a percentagem de capacidade do recurso para as datas de e para especificadas.</span><span class="sxs-lookup"><span data-stu-id="57f85-111">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="57f85-112">**Distribuir Igualmente por Horas** reserva o recurso para um número especificado de horas distribuindo-as uniformemente por dia ao longo das datas de e para especificadas.</span><span class="sxs-lookup"><span data-stu-id="57f85-112">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing them evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="57f85-113">**Carregamento no Início Por Horas** reserva o recurso para um número especificado de horas carregando inicialmente as horas por dia ao longo das datas de e para especificadas.</span><span class="sxs-lookup"><span data-stu-id="57f85-113">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>
    - <span data-ttu-id="57f85-114">**Nenhum** adiciona o recurso à equipa, mas não cria quaisquer reservas que absorvam a sua capacidade.</span><span class="sxs-lookup"><span data-stu-id="57f85-114">**None** adds the resource to the team but doesn’t create any bookings that absorb their capacity.</span></span>

3. <span data-ttu-id="57f85-115">Na grelha **Agenda** para uma tarefa, selecione o ícone **Recurso** na célula de recursos e, em seguida, em **Membros da Equipa**, selecione o membro da equipa que acabou de adicionar.</span><span class="sxs-lookup"><span data-stu-id="57f85-115">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell, and then under **Team Members**, select the team member you just added.</span></span> 

> [!NOTE]
> <span data-ttu-id="57f85-116">Nos separadores **Membro da Equipa** e **Reconciliação**, o recurso mostra as horas reservadas e as horas atribuídas.</span><span class="sxs-lookup"><span data-stu-id="57f85-116">On the **Team Member** and **Reconciliation** tabs, the resource shows booked and assigned hours.</span></span> <span data-ttu-id="57f85-117">As horas devem ser iguais, mas não têm de ser, uma vez que as reservas e as atribuições não estão totalmente ligadas.</span><span class="sxs-lookup"><span data-stu-id="57f85-117">The hours should be the same, but it isn't required as bookings and assignments are not tightly coupled.</span></span> <span data-ttu-id="57f85-118">O separador **Reconciliação** oferece-lhe detalhes quando forem diferentes, por exemplo, quando atribui a um recurso mais horas mais do que as que reservou.</span><span class="sxs-lookup"><span data-stu-id="57f85-118">The **Reconciliation** tab gives you details when they are different, such as when you assign a resource more hours than you have booked.</span></span> <span data-ttu-id="57f85-119">Se necessário, poderá corrigir as informações através da expansão das reservas do recurso ou da alteração da atribuição.</span><span class="sxs-lookup"><span data-stu-id="57f85-119">If needed, you can correct the information by extending the resource's bookings or changing the assignment.</span></span>

## <a name="create-a-generic-team-member-through-task-assignment"></a><span data-ttu-id="57f85-120">Criar um membro da equipa genérico através de atribuição da tarefa</span><span class="sxs-lookup"><span data-stu-id="57f85-120">Create a generic team member through task assignment</span></span>

<span data-ttu-id="57f85-121">Quando cria um membro da equipa genérico através de atribuição da tarefa, cria um marcador de posição ou recurso genérico que descreve as características do recurso nomeado que, em última análise, pretende que funcione nas tarefas.</span><span class="sxs-lookup"><span data-stu-id="57f85-121">When you create a generic team member through task assignment, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks.</span></span> <span data-ttu-id="57f85-122">Em seguida, gera um requisito (ou submete um pedido utilizando o requisito) que é utilizado para procurar e reservar o recurso nomeado.</span><span class="sxs-lookup"><span data-stu-id="57f85-122">You then generate a requirement (or submit a request using the requirement) that is used to search for and book the named resource.</span></span>

1. <span data-ttu-id="57f85-123">Na grelha **Agenda** para uma tarefa, selecione o ícone **Recurso** na célula de recurso.</span><span class="sxs-lookup"><span data-stu-id="57f85-123">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="57f85-124">Escreva um nome para servir como o nome do recurso de marcador de posição.</span><span class="sxs-lookup"><span data-stu-id="57f85-124">Type a name to serve as the placeholder resource’s name.</span></span> <span data-ttu-id="57f85-125">Por exemplo, Gestor do Programa.</span><span class="sxs-lookup"><span data-stu-id="57f85-125">For example, Program Manager.</span></span>

3. <span data-ttu-id="57f85-126">Selecione **Criar** e no campo **Criação Rápida de Membro da Equipa do Projeto**, defina a função do recurso genérico.</span><span class="sxs-lookup"><span data-stu-id="57f85-126">Select **Create**, and in the **Quick Create Project Team Member** field, set the role for the generic resource.</span></span>

4. <span data-ttu-id="57f85-127">Pode continuar a atribuir tarefas a este recurso de marcador de posição selecionando o recurso no **Seletor de Recursos** para a tarefa.</span><span class="sxs-lookup"><span data-stu-id="57f85-127">You can continue to assign tasks to this placeholder resource by selecting the resource on the **Resource Selector** for the task.</span></span> <span data-ttu-id="57f85-128">Estão listados em **Membros da Equipa**.</span><span class="sxs-lookup"><span data-stu-id="57f85-128">They’re listed under **Team Members**.</span></span>

5. <span data-ttu-id="57f85-129">Quando tiver terminado a atribuição de recurso genérico, selecione-o no separador **Equipa** e selecione **Gerar Requisito** para criar um requisito de recurso para o recurso genérico.</span><span class="sxs-lookup"><span data-stu-id="57f85-129">When you’re done assigning the generic resource, select the generic resource on the **Team** tab, and then select **Generate Requirement** to create a resource requirement for the generic resource.</span></span>

6. <span data-ttu-id="57f85-130">Selecione **Reservar** para o recurso genérico.</span><span class="sxs-lookup"><span data-stu-id="57f85-130">Select **Book** for the generic resource.</span></span> <span data-ttu-id="57f85-131">Em seguida, pode utilizar o quadro da Agenda para localizar e reservar um recurso real.</span><span class="sxs-lookup"><span data-stu-id="57f85-131">You can then use the Schedule board to find and book a real resource.</span></span> <span data-ttu-id="57f85-132">Também é possível enviar o requisito para preenchimento por um gestor de recursos.</span><span class="sxs-lookup"><span data-stu-id="57f85-132">You can also submit the requirement for fulfillment by a resource manager.</span></span>

7. <span data-ttu-id="57f85-133">Quando o recurso genérico é preenchido com um recurso nomeado, o recurso genérico é removido da equipa e as atribuições de tarefas para o recurso genérico são atribuídas ao recurso nomeado que preencheu o requisito de recurso genérico do recurso.</span><span class="sxs-lookup"><span data-stu-id="57f85-133">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a><span data-ttu-id="57f85-134">Atribuir um recurso nomeado da lista de todos os recursos reserváveis</span><span class="sxs-lookup"><span data-stu-id="57f85-134">Assign a named resource from the list of all bookable resources</span></span>

<span data-ttu-id="57f85-135">Pode utilizar a caixa de pesquisa no **Seletor de Recursos** para procurar todos os recursos reserváveis e atribui-los a uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="57f85-135">You can use the search box in the **Resource Selector** to search all bookable resources and assign them to a task.</span></span>

<span data-ttu-id="57f85-136">Os recursos atribuídos desta forma são adicionados à equipa sem quaisquer reservas.</span><span class="sxs-lookup"><span data-stu-id="57f85-136">Resources assigned this way are added to the team without any bookings.</span></span> <span data-ttu-id="57f85-137">Isto é semelhante à adição de um membro da equipa e à seleção de Nenhum como o método de alocação.</span><span class="sxs-lookup"><span data-stu-id="57f85-137">This is similar to adding a team member and selecting None as the allocation method.</span></span> <span data-ttu-id="57f85-138">O recurso é apresentado nos separadores **Equipa** e **Reconciliação** como recursos com atribuições apenas e um deficit de reserva.</span><span class="sxs-lookup"><span data-stu-id="57f85-138">The resource is displayed in the **Team** and **Reconciliation** tabs as resources with only assignments and a booking deficit.</span></span> <span data-ttu-id="57f85-139">Reserve-os se quiser utilizar a sua disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="57f85-139">Book them if you want to use their availability.</span></span>

1. <span data-ttu-id="57f85-140">Na grelha **Agenda** para uma tarefa, selecione o ícone **Recurso** na célula de recurso.</span><span class="sxs-lookup"><span data-stu-id="57f85-140">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="57f85-141">Comece a escrever um nome.</span><span class="sxs-lookup"><span data-stu-id="57f85-141">Start typing a name.</span></span> <span data-ttu-id="57f85-142">Os resultados da pesquisa para o nome são apresentados no **Seletor de Recursos** em **Outros Recursos**.</span><span class="sxs-lookup"><span data-stu-id="57f85-142">The search results for the name are displayed in the **Resource Selector** under **Other Resources**.</span></span>

3. <span data-ttu-id="57f85-143">Selecione o recurso que pretende atribuir à tarefa.</span><span class="sxs-lookup"><span data-stu-id="57f85-143">Select the resource that you want to assign to the task.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]