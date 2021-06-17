---
title: Propor recursos do projeto
description: Este tópico fornece informações sobre propor recursos do projeto.
author: ruhercul
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
ms.openlocfilehash: 02e47338e34a37e05455e2bc6e6a175210ed6bc7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997975"
---
# <a name="propose-project-resources"></a><span data-ttu-id="65e39-103">Propor recursos do projeto</span><span class="sxs-lookup"><span data-stu-id="65e39-103">Propose project resources</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="65e39-104">Os gestores de recursos podem propor um recurso ao gestor de projeto utilizando um pedido de recurso.</span><span class="sxs-lookup"><span data-stu-id="65e39-104">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="65e39-105">A partir da grelha de pedido ou do próprio pedido, selecione **Localizar Recursos**.</span><span class="sxs-lookup"><span data-stu-id="65e39-105">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="65e39-106">Na página **Assistente da Agenda**, selecione o recurso e, em seguida, no painel **Criar Reserva de Recursos**, no campo **Estado da Reserva**, selecione **Reservar**.</span><span class="sxs-lookup"><span data-stu-id="65e39-106">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

    ![Recurso proposto selecionado](media/Resource-Management-image62.png)

<span data-ttu-id="65e39-108">Ocorrem as seguintes atualizações de estado:</span><span class="sxs-lookup"><span data-stu-id="65e39-108">The following status updates occur:</span></span>

- <span data-ttu-id="65e39-109">Na página **Assistente da Agenda**, os indicadores de estado são atualizados para indicar que a reserva é proposta, e não reservada de forma fixa.</span><span class="sxs-lookup"><span data-stu-id="65e39-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>

    ![Indicadores de estado para reservas propostas na página Assistente da Agenda](media/Resource-Management-image63.png)

- <span data-ttu-id="65e39-111">No pedido de recurso, o estado é alterado para **Necessita de Revisão**.</span><span class="sxs-lookup"><span data-stu-id="65e39-111">On the resource request, the status is changed to **Needs Review**.</span></span>

    ![Estado do pedido de recurso alterado para Necessita de Revisão](media/Resource-Management-image64.png)

- <span data-ttu-id="65e39-113">No separador **Equipa** do projeto, o valor **Estado do Pedido** do membro da equipa genérico é alterado para **Necessita de Revisão**.</span><span class="sxs-lookup"><span data-stu-id="65e39-113">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

    ![O estado do pedido do membro da equipa genérico foi alterado para Necessita de Revisão no separador Equipa](media/Resource-Management-image48.png)

<span data-ttu-id="65e39-115">O gestor de projeto pode aceitar ou rejeitar a proposta.</span><span class="sxs-lookup"><span data-stu-id="65e39-115">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="65e39-116">Quando os gestores de recursos processam pedidos de recursos, podem utilizar qualquer uma das abordagens seguintes:</span><span class="sxs-lookup"><span data-stu-id="65e39-116">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="65e39-117">Propor vários recursos para satisfazer a procura se não existir um único recurso disponível para cumprir as horas necessárias.</span><span class="sxs-lookup"><span data-stu-id="65e39-117">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="65e39-118">Em seguida, as horas propostas são divididas entre vários recursos que podem satisfazer as horas necessárias.</span><span class="sxs-lookup"><span data-stu-id="65e39-118">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="65e39-119">Neste cenário, as horas não podem ser sobrepostas.</span><span class="sxs-lookup"><span data-stu-id="65e39-119">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="65e39-120">Propor menos recursos do que os necessários.</span><span class="sxs-lookup"><span data-stu-id="65e39-120">Propose fewer resources than are required.</span></span> <span data-ttu-id="65e39-121">Neste cenário, a capacidade do recurso proposto é inferior às horas necessárias que o requerente especificou.</span><span class="sxs-lookup"><span data-stu-id="65e39-121">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="65e39-122">Consequentemente, quando o requerente aceita os recursos propostos, é criado um requisito de recurso não cumprido para capturar a procura restante.</span><span class="sxs-lookup"><span data-stu-id="65e39-122">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="65e39-123">Reservar vários recursos para satisfazer a procura se não existir um único recurso disponível para concluir o trabalho.</span><span class="sxs-lookup"><span data-stu-id="65e39-123">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="65e39-124">Reservar menos recursos do que os necessários.</span><span class="sxs-lookup"><span data-stu-id="65e39-124">Book fewer resources than are required.</span></span> <span data-ttu-id="65e39-125">Nesse cenário, as horas reservadas são menores que as horas necessárias.</span><span class="sxs-lookup"><span data-stu-id="65e39-125">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="65e39-126">O sistema orienta-o a propor recursos em vez de reservas, para que o requerente possa verificar e monitorizar a procura restante.</span><span class="sxs-lookup"><span data-stu-id="65e39-126">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="billable-utilization"></a><span data-ttu-id="65e39-127">Utilização faturável</span><span class="sxs-lookup"><span data-stu-id="65e39-127">Billable utilization</span></span>

<span data-ttu-id="65e39-128">Os recursos podem ter uma utilização faturável de destino.</span><span class="sxs-lookup"><span data-stu-id="65e39-128">Resources can have a target billable utilization.</span></span> <span data-ttu-id="65e39-129">Esta utilização de destino é definida como um atributo na função predefinida de um recurso ou definida no registo do recurso reservável individual.</span><span class="sxs-lookup"><span data-stu-id="65e39-129">This target utilization is either defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="65e39-130">Os cálculos de utilização baseiam-se nas horas reais que os recursos reportaram através da utilização de entradas de tempo aprovadas.</span><span class="sxs-lookup"><span data-stu-id="65e39-130">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="65e39-131">As fórmulas que se seguem são utilizadas para calcular a utilização:</span><span class="sxs-lookup"><span data-stu-id="65e39-131">The following formulas are used to calculate utilization:</span></span>

- <span data-ttu-id="65e39-132">Utilização faturável = Horas reais faturáveis ÷ Capacidade do recurso</span><span class="sxs-lookup"><span data-stu-id="65e39-132">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
- <span data-ttu-id="65e39-133">Utilização não faturável = Tempo real com ID do tipo de faturação = Não faturável, Grátis ou Não disponível ÷ Capacidade do recurso</span><span class="sxs-lookup"><span data-stu-id="65e39-133">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
- <span data-ttu-id="65e39-134">Interno = Tempo real sem contrato de vendas ÷ Capacidade do recurso</span><span class="sxs-lookup"><span data-stu-id="65e39-134">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
- <span data-ttu-id="65e39-135">Capacidade do recurso = Horas de trabalho de recursos – Fora do escritório – Dias de descanso</span><span class="sxs-lookup"><span data-stu-id="65e39-135">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="65e39-136">Pode localizar a vista **Utilização de Recursos** no painel **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="65e39-136">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

![Vista de Utilização de Recursos](media/Resource-Management-image65.png)

<span data-ttu-id="65e39-138">Cada célula da grelha representa a percentagem de utilização faturável do recurso num período, tal como um dia, uma semana ou um mês.</span><span class="sxs-lookup"><span data-stu-id="65e39-138">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="65e39-139">As fórmulas que se seguem são utilizadas para colorir as células:</span><span class="sxs-lookup"><span data-stu-id="65e39-139">The following formulas are used to color the cells:</span></span>

- <span data-ttu-id="65e39-140">**Verde:** Utilização faturável \>= Utilização de destino do recurso</span><span class="sxs-lookup"><span data-stu-id="65e39-140">**Green:** Billable utilization \>= Resource target utilization</span></span>
- <span data-ttu-id="65e39-141">**Amarelo:** Utilização de destino – 20 \<= Utilização faturável \< Utilização de destino</span><span class="sxs-lookup"><span data-stu-id="65e39-141">**Yellow:** Target utilization – 20 \<= Billable utilization \< Target utilization</span></span>
- <span data-ttu-id="65e39-142">**Vermelho:** Utilização faturável \< Utilização de destino – 20</span><span class="sxs-lookup"><span data-stu-id="65e39-142">**Red:** Billable utilization \< Target utilization – 20</span></span>

<span data-ttu-id="65e39-143">Uma vez a vista **Utilização de Recursos** é baseada no Quadro da Agenda, pode utilizar as capacidades de filtragem do Quadro da Agenda para filtrar os resultados.</span><span class="sxs-lookup"><span data-stu-id="65e39-143">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="65e39-144">A grelha requer que defina uma utilização de destino na função ou no recurso individual.</span><span class="sxs-lookup"><span data-stu-id="65e39-144">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="65e39-145">Para efetuar esta configuração, aceda a **Recursos** \> **Funções do recurso**.</span><span class="sxs-lookup"><span data-stu-id="65e39-145">To do this setup, go to **Resources** \> **Resource roles**.</span></span>

<span data-ttu-id="65e39-146">Além disso, deve ser atribuída uma função predefinida a cada recurso reservável.</span><span class="sxs-lookup"><span data-stu-id="65e39-146">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="65e39-147">Aceda a **Recursos** \> **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="65e39-147">Go to **Resources** \> **Resources**.</span></span> <span data-ttu-id="65e39-148">No separador **Project Service**, verifique se está definida uma função de recurso e se o campo **É Predefinição** está definido como **Sim**.</span><span class="sxs-lookup"><span data-stu-id="65e39-148">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field for it is set to **Yes**.</span></span> <span data-ttu-id="65e39-149">Pode adicionar funções adicionais em que **É Predefinição = Não**.</span><span class="sxs-lookup"><span data-stu-id="65e39-149">You can add additional roles where **Is Default = No**.</span></span> <span data-ttu-id="65e39-150">A função em que **É Predefinição = Sim** é utilizada para avaliar a utilização do recurso relativamente ao alvo dessa função.</span><span class="sxs-lookup"><span data-stu-id="65e39-150">The role where the **Is Default = Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

![Função predefinida definida](media/Resource-Management-image67.png)

<span data-ttu-id="65e39-152">No separador **Project Service**, também pode definir uma utilização de destino individual para o recurso.</span><span class="sxs-lookup"><span data-stu-id="65e39-152">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="65e39-153">Em seguida, o cálculo da utilização utiliza essa utilização de destino para avaliar o destino do recurso em vez do destino da função predefinida do recurso.</span><span class="sxs-lookup"><span data-stu-id="65e39-153">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="65e39-154">A utilização é mostrada para um recurso apenas se esse recurso tiver aprovado, um tempo faturável durante o período mostrado na grelha.</span><span class="sxs-lookup"><span data-stu-id="65e39-154">Utilization is shown for a resource only if that resource has approved, chargeable time during the period that is shown in the grid.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="65e39-155">Disponibilidade do recurso</span><span class="sxs-lookup"><span data-stu-id="65e39-155">Resource availability</span></span>

<span data-ttu-id="65e39-156">É importante que os gestores de recursos possam ver a disponibilidade de recursos e atualizar as reservas.</span><span class="sxs-lookup"><span data-stu-id="65e39-156">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="65e39-157">Em alguns casos, não há uma procura formal (pedido de recurso), mas um gestor de recursos deve responder a uma procura não planeada que vem através de canais como e-mail, chamada telefónica ou mensagem instantânea.</span><span class="sxs-lookup"><span data-stu-id="65e39-157">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="65e39-158">Os gestores de recursos utilizam o Quadro da Agenda para atualizar recursos e reservas.</span><span class="sxs-lookup"><span data-stu-id="65e39-158">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="65e39-159">As horas de trabalho dos recursos são utilizadas como base para calcular a disponibilidade de um recurso.</span><span class="sxs-lookup"><span data-stu-id="65e39-159">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="65e39-160">As reservas de recursos consomem a capacidade dos recursos.</span><span class="sxs-lookup"><span data-stu-id="65e39-160">Resource bookings consume the capacity of the resources.</span></span>

![Quadro da Agenda](media/Resource-Management-image68.png)

<span data-ttu-id="65e39-162">O Quadro da Agenda utiliza cores e sombreamento para mostrar reservas, disponibilidade e reservas em excesso, bem como o estado das reservas.</span><span class="sxs-lookup"><span data-stu-id="65e39-162">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="65e39-163">Uma definição nas definições do Quadro da Agenda permite-lhe mostrar uma legenda.</span><span class="sxs-lookup"><span data-stu-id="65e39-163">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="65e39-164">Se uma seta a apontar para a direita aparecer ao lado de um recurso reservável individual no Quadro da Agenda, o recurso poderá ser expandido para mostrar os detalhes do trabalho em que o recurso está reservado.</span><span class="sxs-lookup"><span data-stu-id="65e39-164">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

![Recurso reservável expandido no Quadro da Agenda](media/Resource-Management-image69.png)

<span data-ttu-id="65e39-166">Uma vez que o Dynamics 365 Project Service Automation utiliza o motor de Universal Resource Scheduling, se tiver o Dynamics 365 Field Service instalado, pode ver os detalhes das reservas de recursos para projetos, ordens de intervenção e outras entidades para as quais expandiu o agendamento.</span><span class="sxs-lookup"><span data-stu-id="65e39-166">Because Dynamics 365 Project Service Automation uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

![Detalhes de reservas de recursos para projetos e ordens de intervenção](media/Resource-Management-image70.png)

<span data-ttu-id="65e39-168">Para ver mais detalhes sobre um recurso individual, clique com o botão direito do rato para abrir o cartão do recurso.</span><span class="sxs-lookup"><span data-stu-id="65e39-168">To view more details about an individual resource, right-click it to open the resource card.</span></span>

![Cartão do recurso](media/Resource-Management-image71.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]