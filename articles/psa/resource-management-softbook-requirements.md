---
title: Efetuar reserva flexível de requisitos
description: Este tópico fornece informações sobre como reservar requisitos de forma flexível.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 861e484ea2fc251e0082b4cb0cd5409a45a74057
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082614"
---
# <a name="soft-book-requirements"></a><span data-ttu-id="6dee2-103">Efetuar reserva flexível de requisitos</span><span class="sxs-lookup"><span data-stu-id="6dee2-103">Soft-book requirements</span></span>

<span data-ttu-id="6dee2-104">Um requisito de recurso pode ser reservado de forma fixa.</span><span class="sxs-lookup"><span data-stu-id="6dee2-104">A resource requirement can be hard-booked.</span></span> <span data-ttu-id="6dee2-105">Uma reserva fixa cria uma proposta que consome a capacidade de um recurso.</span><span class="sxs-lookup"><span data-stu-id="6dee2-105">A hard booking creates a proposal that consumes a resource's capacity.</span></span> <span data-ttu-id="6dee2-106">Em seguida, a proposta é enviada para o requerente para aprovação.</span><span class="sxs-lookup"><span data-stu-id="6dee2-106">The proposal is then sent back to the requester for approval.</span></span> <span data-ttu-id="6dee2-107">Uma reserva flexível adiciona provisoriamente um recurso a uma equipa do projeto e tem um estado diferente no Quadro da Agenda, mas não consome a capacidade do recurso.</span><span class="sxs-lookup"><span data-stu-id="6dee2-107">A soft booking tentatively adds a resource to a project team and has a different status on the Schedule Board, but it doesn't consume the resource's capacity.</span></span> <span data-ttu-id="6dee2-108">Para efetuar uma reserva flexível de um recurso do Quadro da Agenda, defina o campo **Estado de Reserva** como **Flexível**.</span><span class="sxs-lookup"><span data-stu-id="6dee2-108">To soft-book a resource from the Schedule Board, set the **Booking Status** field to **Soft**.</span></span>

![Estado da reserva definido como Flexível](media/Resource-Management-image77.png)

<span data-ttu-id="6dee2-110">Quando o separador **Equipa** se encontra na vista **Membros da Equipa Nomeados** , o recurso é apresentado nesse ponto.</span><span class="sxs-lookup"><span data-stu-id="6dee2-110">When the **Team** tab is in the **Named Team Members** view, the resource appears there.</span></span> <span data-ttu-id="6dee2-111">As horas reservadas de forma flexível são reportadas na coluna **Horas com Reserva Flexível**.</span><span class="sxs-lookup"><span data-stu-id="6dee2-111">The soft-booked hours are reported in the **Soft Booked Hours** column.</span></span>

![Horas reservadas de forma flexível na vista Membros da Equipa Nomeados](media/Resource-Management-image78.png)

<span data-ttu-id="6dee2-113">Os membros da equipa reservados de forma flexível podem ser atribuídos às tarefas.</span><span class="sxs-lookup"><span data-stu-id="6dee2-113">Soft-booked team members can be assigned to tasks.</span></span>

![Membro da equipa reservado de forma flexível atribuído a uma tarefa](media/Resource-Management-image79.png)

<span data-ttu-id="6dee2-115">No separador **Reconciliação** , não são mostradas reservas para um recurso com reserva flexível, porque o separador **Reconciliação** só considera as reservas fixas.</span><span class="sxs-lookup"><span data-stu-id="6dee2-115">On the **Reconciliation** tab, no bookings are shown for a soft-book resource, because the **Reconciliation** tab considers only hard-bookings.</span></span>

![Recurso reservado de forma flexível sem reservas no separador Reconciliação](media/Resource-Management-image80.png)

> [!NOTE]
> <span data-ttu-id="6dee2-117">Não é possível efetuar uma reserva flexível de um recurso a partir de um requisito gerado a partir de um membro da equipa genérico.</span><span class="sxs-lookup"><span data-stu-id="6dee2-117">You can't soft-book a resource from a requirement that was generated from a generic team member.</span></span>

<span data-ttu-id="6dee2-118">No Quadro da Agenda, é utilizada uma cor diferente para as reservas flexíveis de um recurso.</span><span class="sxs-lookup"><span data-stu-id="6dee2-118">On the Schedule Board, a different coloring is used for soft bookings for a resource.</span></span>

![Reservas flexíveis no Quadro da Agenda](media/Resource-Management-image81.png)

<span data-ttu-id="6dee2-120">Para converter uma reserva flexível numa reserva fixa, no Quadro da Agenda, clique com o botão direito do rato na reserva flexível e selecione **Alterar Estado** \> **Reserva Fixa** \> **Fixa**.</span><span class="sxs-lookup"><span data-stu-id="6dee2-120">To convert a soft booking to a hard booking, on the Schedule Board, right-click the soft booking, and then select **Change Status** \> **Hard Book** \> **Hard**.</span></span>

![Alterar o estado de reserva para Fixa](media/Resource-Management-image82.png)

<span data-ttu-id="6dee2-122">A reserva é alterada e o estado é alterado no Quadro da Agenda.</span><span class="sxs-lookup"><span data-stu-id="6dee2-122">The booking is changed, and the status is changed on the Schedule Board.</span></span> <span data-ttu-id="6dee2-123">Uma vez que o estado de reserva é **Fixa** , o recurso é mostrado como reservado e a sua capacidade e disponibilidade são ajustadas.</span><span class="sxs-lookup"><span data-stu-id="6dee2-123">Because the booking status is now **Hard** , the resource is shown as booked, and its capacity and availability are adjusted.</span></span>

<span data-ttu-id="6dee2-124">Pode utilizar o mesmo método para cancelar uma reserva fixa ou uma reserva flexível a partir do Quadro da Agenda.</span><span class="sxs-lookup"><span data-stu-id="6dee2-124">You can use the same method to cancel a hard booking or a soft booking from the Schedule Board.</span></span>

<span data-ttu-id="6dee2-125">Para converter um recurso com reserva flexível em fixa no separador **Equipa** , selecione o recurso e, em seguida, selecione **Confirmar**.</span><span class="sxs-lookup"><span data-stu-id="6dee2-125">To convert a resource that is soft-booked to hard-booked on the project's **Team** tab, select the resource, and then select **Confirm**.</span></span>

![Comando Confirmar](media/Resource-Management-image83.png)
