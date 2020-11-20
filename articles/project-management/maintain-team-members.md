---
title: Manter membros da equipa
description: Este tópico fornece informações sobre a reserva de recursos nomeados para as equipas do projeto e atribuir às mesmas tarefas
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: abab21ff98481166517be0c74a2c14c36d5e9d1d
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131537"
---
# <a name="maintain-team-members"></a><span data-ttu-id="79bf8-103">Manter membros da equipa</span><span class="sxs-lookup"><span data-stu-id="79bf8-103">Maintain team members</span></span>

<span data-ttu-id="79bf8-104">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="79bf8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="79bf8-105">Pode adicionar um recurso nomeado à sua equipa do projeto, reservando-o diretamente para a equipa.</span><span class="sxs-lookup"><span data-stu-id="79bf8-105">You can add a named resource to your project team by booking them directly to the team.</span></span>

1. <span data-ttu-id="79bf8-106">No Dynamics 365 Project Operations, vá para **Projetos** e selecione para abrir o projeto que está a reservar.</span><span class="sxs-lookup"><span data-stu-id="79bf8-106">In Dynamics 365 Project Operations, go to **Projects**, and select the open the project that you're booking for.</span></span>
2. <span data-ttu-id="79bf8-107">Na página **Projeto**, no separador **Equipa**, selecione **Novo**.</span><span class="sxs-lookup"><span data-stu-id="79bf8-107">On the **Project** page, on the **Team** tab, select **New**.</span></span> 
3. <span data-ttu-id="79bf8-108">Na caixa de diálogo **Criação Rápida de Membro de Equipa do Projeto**, selecione o recurso reservável.</span><span class="sxs-lookup"><span data-stu-id="79bf8-108">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="79bf8-109">O campo **Função** será preenchido com a função predefinida do recurso se tiver atribuído um.</span><span class="sxs-lookup"><span data-stu-id="79bf8-109">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="79bf8-110">Pode alterar a função.</span><span class="sxs-lookup"><span data-stu-id="79bf8-110">You can change the role.</span></span> 
4. <span data-ttu-id="79bf8-111">Selecione as datas de início e fim, em que o recurso será necessário e selecione o método de alocação da capacidade do recurso.</span><span class="sxs-lookup"><span data-stu-id="79bf8-111">Select the from and to dates that the resource will be needed, and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="79bf8-112">No campo **Aprovador do Projeto**, selecione **Sim** se pretender que o membro da equipa seja um aprovador do projeto.</span><span class="sxs-lookup"><span data-stu-id="79bf8-112">In the **Project Approver** field, select **Yes** if you want the team member to be a project approver.</span></span> <span data-ttu-id="79bf8-113">O membro da equipa pode aprovar as entradas de hora e despesas submetidas para este projeto.</span><span class="sxs-lookup"><span data-stu-id="79bf8-113">The team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="79bf8-114">Selecione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="79bf8-114">Select **Save**.</span></span>

<span data-ttu-id="79bf8-115">Agora, pode atribuir o recurso reservado a tarefas no projeto.</span><span class="sxs-lookup"><span data-stu-id="79bf8-115">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="79bf8-116">Na página **Projeto**, selecione o separador **Agenda** para atribuir tarefas ao novo recurso.</span><span class="sxs-lookup"><span data-stu-id="79bf8-116">On the **Project** page, on the **Schedule** tab, assign tasks to the new resource.</span></span> <span data-ttu-id="79bf8-117">O seletor de recursos que é iniciado a partir do campo **Recursos** na grelha de tarefas irá mostrar os membros da equipa que pode selecionar.</span><span class="sxs-lookup"><span data-stu-id="79bf8-117">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>


<span data-ttu-id="79bf8-118">No Project Operations, as reservas de recursos e as atribuições de tarefas não estão intimamente associadas.</span><span class="sxs-lookup"><span data-stu-id="79bf8-118">In Project Operations, resource bookings and task assignments aren't tightly coupled.</span></span> <span data-ttu-id="79bf8-119">Quando utiliza o seletor de recursos na agenda, pode atribuir tarefas a membros da equipa durante mais horas do que as reservas deles cobrem no projeto.</span><span class="sxs-lookup"><span data-stu-id="79bf8-119">When you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>

<span data-ttu-id="79bf8-120">As diferenças entre as reservas dos membros da equipa e as atribuições são mostradas nos separadores **Equipa** e **Reconciliação de Recursos**.</span><span class="sxs-lookup"><span data-stu-id="79bf8-120">The differences between team member bookings and assignments are shown on the **Team** and **Resource Reconciliation** tabs.</span></span> <span data-ttu-id="79bf8-121">Também pode conciliar as diferenças entre as reservas e as atribuições para os recursos a um nível mais detalhado.</span><span class="sxs-lookup"><span data-stu-id="79bf8-121">You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

<span data-ttu-id="79bf8-122">Utilize o seletor de recursos no separador **Agenda** para procurar e selecionar recursos reserváveis que ainda não fazem parte da equipa do projeto.</span><span class="sxs-lookup"><span data-stu-id="79bf8-122">Use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="79bf8-123">Estes recursos são mostrados no seletor de recursos como **Outros Recursos**.</span><span class="sxs-lookup"><span data-stu-id="79bf8-123">These resources are shown in the resource picker as **Other Resources**.</span></span>

<span data-ttu-id="79bf8-124">Quando efetua uma seleção, o recurso é adicionado à equipa do projeto e atribuído à tarefa, mas não são geradas reservas.</span><span class="sxs-lookup"><span data-stu-id="79bf8-124">When you make a selection, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

<span data-ttu-id="79bf8-125">Pode utilizar a capacidade de expansão da reserva do separador **Reconciliação** ou o **Quadro da Agenda** para reservar a capacidade do recurso para o projeto.</span><span class="sxs-lookup"><span data-stu-id="79bf8-125">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

<span data-ttu-id="79bf8-126">Depois de um membro da equipa ficar reservado no seu projeto, pode utilizar **Manter reservas** ou o **Quadro da Agenda** diretamente para gerir as respetivas reservas.</span><span class="sxs-lookup"><span data-stu-id="79bf8-126">After a team member is booked on your project, you can use **Maintain bookings** or the **Schedule Board** directly to manage their bookings.</span></span>
