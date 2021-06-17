---
title: Analisar recursos propostos
description: Este tópico fornece informações sobre como propor recursos do projeto.
author: ruhercul
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 987ea08c77c1824182856c0d52ee0cd15e7029b9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000765"
---
# <a name="review-proposed-resources"></a><span data-ttu-id="34dd1-103">Analisar recursos propostos</span><span class="sxs-lookup"><span data-stu-id="34dd1-103">Review proposed resources</span></span>

<span data-ttu-id="34dd1-104">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="34dd1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="34dd1-105">Os gestores de recursos podem propor um recurso ao gestor de projeto utilizando um pedido de recurso.</span><span class="sxs-lookup"><span data-stu-id="34dd1-105">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="34dd1-106">A partir da grelha de pedido ou do próprio pedido, selecione **Localizar Recursos**.</span><span class="sxs-lookup"><span data-stu-id="34dd1-106">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="34dd1-107">Na página **Assistente da Agenda**, selecione o recurso e, em seguida, no painel **Criar Reserva de Recursos**, no campo **Estado da Reserva**, selecione **Reservar**.</span><span class="sxs-lookup"><span data-stu-id="34dd1-107">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

<span data-ttu-id="34dd1-108">Ocorrem as seguintes atualizações de estado:</span><span class="sxs-lookup"><span data-stu-id="34dd1-108">The following status updates occur:</span></span>

- <span data-ttu-id="34dd1-109">Na página **Assistente da Agenda**, os indicadores de estado são atualizados para indicar que a reserva é proposta, e não reservada de forma fixa.</span><span class="sxs-lookup"><span data-stu-id="34dd1-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>
- <span data-ttu-id="34dd1-110">No pedido de recurso, o estado é alterado para **Necessita de Revisão**.</span><span class="sxs-lookup"><span data-stu-id="34dd1-110">On the resource request, the status is changed to **Needs Review**.</span></span>
- <span data-ttu-id="34dd1-111">No separador **Equipa** do projeto, o valor **Estado do Pedido** do membro da equipa genérico é alterado para **Necessita de Revisão**.</span><span class="sxs-lookup"><span data-stu-id="34dd1-111">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

<span data-ttu-id="34dd1-112">O gestor de projeto pode aceitar ou rejeitar a proposta.</span><span class="sxs-lookup"><span data-stu-id="34dd1-112">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="34dd1-113">Quando os gestores de recursos processam pedidos de recursos, podem utilizar qualquer uma das abordagens seguintes:</span><span class="sxs-lookup"><span data-stu-id="34dd1-113">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="34dd1-114">Propor vários recursos para satisfazer a procura se não existir um único recurso disponível para cumprir as horas necessárias.</span><span class="sxs-lookup"><span data-stu-id="34dd1-114">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="34dd1-115">Em seguida, as horas propostas são divididas entre vários recursos que podem satisfazer as horas necessárias.</span><span class="sxs-lookup"><span data-stu-id="34dd1-115">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="34dd1-116">Neste cenário, as horas não podem ser sobrepostas.</span><span class="sxs-lookup"><span data-stu-id="34dd1-116">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="34dd1-117">Propor menos recursos do que os necessários.</span><span class="sxs-lookup"><span data-stu-id="34dd1-117">Propose fewer resources than are required.</span></span> <span data-ttu-id="34dd1-118">Neste cenário, a capacidade do recurso proposto é inferior às horas necessárias que o requerente especificou.</span><span class="sxs-lookup"><span data-stu-id="34dd1-118">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="34dd1-119">Consequentemente, quando o requerente aceita os recursos propostos, é criado um requisito de recurso não cumprido para capturar a procura restante.</span><span class="sxs-lookup"><span data-stu-id="34dd1-119">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="34dd1-120">Reservar vários recursos para satisfazer a procura se não existir um único recurso disponível para concluir o trabalho.</span><span class="sxs-lookup"><span data-stu-id="34dd1-120">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="34dd1-121">Reservar menos recursos do que os necessários.</span><span class="sxs-lookup"><span data-stu-id="34dd1-121">Book fewer resources than are required.</span></span> <span data-ttu-id="34dd1-122">Nesse cenário, as horas reservadas são menores que as horas necessárias.</span><span class="sxs-lookup"><span data-stu-id="34dd1-122">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="34dd1-123">O sistema orienta-o a propor recursos em vez de reservas, para que o requerente possa verificar e monitorizar a procura restante.</span><span class="sxs-lookup"><span data-stu-id="34dd1-123">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="34dd1-124">Disponibilidade do recurso</span><span class="sxs-lookup"><span data-stu-id="34dd1-124">Resource availability</span></span>

<span data-ttu-id="34dd1-125">É importante que os gestores de recursos possam ver a disponibilidade de recursos e atualizar as reservas.</span><span class="sxs-lookup"><span data-stu-id="34dd1-125">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="34dd1-126">Em alguns casos, não há uma procura formal (pedido de recurso), mas um gestor de recursos deve responder a uma procura não planeada que vem através de canais como e-mail, chamada telefónica ou mensagem instantânea.</span><span class="sxs-lookup"><span data-stu-id="34dd1-126">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="34dd1-127">Os gestores de recursos utilizam o Quadro da Agenda para atualizar recursos e reservas.</span><span class="sxs-lookup"><span data-stu-id="34dd1-127">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="34dd1-128">As horas de trabalho dos recursos são utilizadas como base para calcular a disponibilidade de um recurso.</span><span class="sxs-lookup"><span data-stu-id="34dd1-128">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="34dd1-129">As reservas de recursos consomem a capacidade dos recursos.</span><span class="sxs-lookup"><span data-stu-id="34dd1-129">Resource bookings consume the capacity of the resources.</span></span>

<span data-ttu-id="34dd1-130">O Quadro da Agenda utiliza cores e sombreamento para mostrar reservas, disponibilidade e reservas em excesso, bem como o estado das reservas.</span><span class="sxs-lookup"><span data-stu-id="34dd1-130">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="34dd1-131">Uma definição nas definições do Quadro da Agenda permite-lhe mostrar uma legenda.</span><span class="sxs-lookup"><span data-stu-id="34dd1-131">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="34dd1-132">Se uma seta a apontar para a direita aparecer ao lado de um recurso reservável individual no Quadro da Agenda, o recurso poderá ser expandido para mostrar os detalhes do trabalho em que o recurso está reservado.</span><span class="sxs-lookup"><span data-stu-id="34dd1-132">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

<span data-ttu-id="34dd1-133">Uma vez que o Dynamics 365 Project Operations utiliza o motor de Universal Resource Scheduling, se tiver o Dynamics 365 Field Service instalado, pode ver os detalhes das reservas de recursos para projetos, ordens de intervenção e outras entidades para as quais expandiu o agendamento.</span><span class="sxs-lookup"><span data-stu-id="34dd1-133">Because Dynamics 365 Project Operations uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

<span data-ttu-id="34dd1-134">Para ver mais detalhes sobre um recurso individual, clique com o botão direito do rato para abrir o cartão do recurso.</span><span class="sxs-lookup"><span data-stu-id="34dd1-134">To view more details about an individual resource, right-click it to open the resource card.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]