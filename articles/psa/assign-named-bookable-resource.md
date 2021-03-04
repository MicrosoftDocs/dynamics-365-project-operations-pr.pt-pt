---
title: Reservar recursos reserváveis nomeados para uma equipa do projeto e atribuir tarefas
description: Este tópico fornece informações sobre como reservar recursos nomeados para as equipas do projeto e atribui-los a tarefas.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
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
ms.openlocfilehash: d8a49b6ae8423cb99c710e40704475b4a71d3724
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145372"
---
# <a name="book-named-bookable-resources-to-a-project-team-and-assign-tasks"></a><span data-ttu-id="a09a7-103">Reservar recursos reserváveis nomeados para uma equipa do projeto e atribuir tarefas</span><span class="sxs-lookup"><span data-stu-id="a09a7-103">Book named bookable resources to a project team and assign tasks</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="a09a7-104">Pode adicionar um recurso nomeado à sua equipa do projeto, reservando-o diretamente para a equipa.</span><span class="sxs-lookup"><span data-stu-id="a09a7-104">You can  add a named resource to your project team by booking them directly onto the team.</span></span> <span data-ttu-id="a09a7-105">Para o fazer, conclua os seguintes passos.</span><span class="sxs-lookup"><span data-stu-id="a09a7-105">To do this, complete the following steps.</span></span>

1. <span data-ttu-id="a09a7-106">No Project Service Automation, aceda a **Projetos** e selecione para abrir o projeto que está a reservar.</span><span class="sxs-lookup"><span data-stu-id="a09a7-106">In  Project Service Automation, go to **Projects**, and select the open the project that you are booking for.</span></span>
2. <span data-ttu-id="a09a7-107">Na página **Projeto**, no separador **Equipa**, clique em **Novo**.</span><span class="sxs-lookup"><span data-stu-id="a09a7-107">On the **Project** page, on the **Team** tab, click **New**.</span></span> 

![Adicionar um membro da equipa a partir do separador equipa](media/RM-how-to-1.png)

3. <span data-ttu-id="a09a7-109">Na caixa de diálogo **Criação Rápida de Membro de Equipa do Projeto**, selecione o recurso reservável.</span><span class="sxs-lookup"><span data-stu-id="a09a7-109">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="a09a7-110">O campo **Função** será preenchido com a função predefinida do recurso se tiver atribuído um.</span><span class="sxs-lookup"><span data-stu-id="a09a7-110">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="a09a7-111">Poderá alterar a função, se for necessário.</span><span class="sxs-lookup"><span data-stu-id="a09a7-111">You can change the role if needed.</span></span> 
4. <span data-ttu-id="a09a7-112">Selecione as datas de início e fim, em que o recurso será necessário e selecione o método de alocação da capacidade do recurso.</span><span class="sxs-lookup"><span data-stu-id="a09a7-112">Select the from and to dates that the resource will be needed and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="a09a7-113">Se pretender que o membro da equipa seja um aprovador do projeto, selecione **Sim** no campo **Aprovador do Projeto**.</span><span class="sxs-lookup"><span data-stu-id="a09a7-113">If you want the team member to be a project approver, select **Yes** in the **Project Approver** field.</span></span> <span data-ttu-id="a09a7-114">Isto significa que o membro da equipa pode aprovar as entradas de tempo e despesas submetidas para este projeto.</span><span class="sxs-lookup"><span data-stu-id="a09a7-114">This will mean that the team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="a09a7-115">Clique em **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="a09a7-115">Click **Save**.</span></span>

![Adicionar um membro da equipa no formulário criação rápida](media/RM-how-to-2.png)


<span data-ttu-id="a09a7-117">Agora, pode atribuir o recurso reservado a tarefas no projeto.</span><span class="sxs-lookup"><span data-stu-id="a09a7-117">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="a09a7-118">Na página **Projeto**, clique no separador **Agenda** para atribuir tarefas ao novo recurso.</span><span class="sxs-lookup"><span data-stu-id="a09a7-118">On the **Project** page, click the **Schedule** tab to assign tasks to the new resource.</span></span> <span data-ttu-id="a09a7-119">O seletor de recursos que é iniciado a partir do campo **Recursos** na grelha de tarefas irá mostrar os membros da equipa que pode selecionar.</span><span class="sxs-lookup"><span data-stu-id="a09a7-119">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>

![Atribuir um membro da equipa a uma tarefa no separador agenda](media/RM-how-to-3.png)

<span data-ttu-id="a09a7-121">Na versão 3 do Project Service Automation (PSA), as reservas de recursos e as atribuições de tarefas não estão totalmente ligadas.</span><span class="sxs-lookup"><span data-stu-id="a09a7-121">In version 3 for Project Service Automation (PSA), resource bookings and task assignments are not tightly coupled.</span></span> <span data-ttu-id="a09a7-122">Isto significa que, quando utiliza o seletor de recursos na agenda, pode atribuir tarefas a membros da equipa durante mais horas do que as reservas deles cobrem no projeto.</span><span class="sxs-lookup"><span data-stu-id="a09a7-122">This means that when you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>
<span data-ttu-id="a09a7-123">Pode ver as diferenças entre as reservas e as atribuições de membros da equipa no separador **Equipa** ou no separador **Reconciliação de Recursos**. Também pode reconciliar as diferenças entre as reservas e as atribuições de recursos a um nível mais detalhado.</span><span class="sxs-lookup"><span data-stu-id="a09a7-123">You can see the differences between team member bookings and assignments on the **Team** tab or on the **Resource Reconciliation** tab. You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

![Separador Reconciliação de recursos](media/RM-how-to-4.png)

<span data-ttu-id="a09a7-125">Também pode utilizar o seletor de recursos no separador **Agenda** para procurar e selecionar recursos reserváveis que ainda não fazem parte da equipa do projeto.</span><span class="sxs-lookup"><span data-stu-id="a09a7-125">You can also use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="a09a7-126">Estes são mostrados no seletor de recursos como **Outros Recursos**.</span><span class="sxs-lookup"><span data-stu-id="a09a7-126">These are shown in the resource picker as **Other Resources**.</span></span>

![Atribuir um recurso de um membro não pertencente à equipa a uma tarefa](media/RM-how-to-5.png)

<span data-ttu-id="a09a7-128">Quando efetua este procedimento, o recurso é adicionado à equipa do projeto e atribuído à tarefa, mas não são geradas reservas.</span><span class="sxs-lookup"><span data-stu-id="a09a7-128">When you do this, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

![Membro da equipa com atribuições e sem reservas](media/RM-how-to-6.png)

<span data-ttu-id="a09a7-130">Pode utilizar a capacidade de expansão da reserva do separador **Reconciliação** ou o **Quadro da Agenda** para reservar a capacidade do recurso para o projeto.</span><span class="sxs-lookup"><span data-stu-id="a09a7-130">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

![Expandir reservas para um membro da equipa no separador reconciliação de recursos](media/RM-how-to-7.png)

<span data-ttu-id="a09a7-132">Depois de um membro da equipa ficar reservado no seu projeto, pode manter as reservas ou utilizar o Quadro da Agenda diretamente para gerir as respetivas reservas.</span><span class="sxs-lookup"><span data-stu-id="a09a7-132">After a team member is booked on your project, you can use maintain bookings or use the Schedule Board directly to manage their bookings.</span></span>
