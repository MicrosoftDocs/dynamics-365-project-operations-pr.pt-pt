---
title: Cumprimento dos requisitos genéricos de recursos
description: Este tópico fornece informações sobre como reservar recursos nomeados para um requisito de recurso genérico.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3c4d02fd589d4a5d39380688852377f57fceb05b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130322"
---
# <a name="generic-resource-requirement-fulfillment"></a><span data-ttu-id="90ec1-103">Cumprimento dos requisitos genéricos de recursos</span><span class="sxs-lookup"><span data-stu-id="90ec1-103">Generic resource requirement fulfillment</span></span>

<span data-ttu-id="90ec1-104">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="90ec1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="90ec1-105">Pode reservar um recurso nomeado para substituir o recurso genérico que tem um requisito de recurso.</span><span class="sxs-lookup"><span data-stu-id="90ec1-105">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="90ec1-106">Na página **Projetos**, selecione o separador **Equipa**.</span><span class="sxs-lookup"><span data-stu-id="90ec1-106">On the **Projects** page, select the **Team** tab.</span></span>
2. <span data-ttu-id="90ec1-107">Selecione o recurso genérico que tem um requisito de recurso a partir da lista e, em seguida, selecione **Reservar**.</span><span class="sxs-lookup"><span data-stu-id="90ec1-107">Select the generic resource that has a resource requirement from the list, and then select **Book**.</span></span> <span data-ttu-id="90ec1-108">Ou abra o requisito de recurso e, em seguida, selecione **Reservar**.</span><span class="sxs-lookup"><span data-stu-id="90ec1-108">Or, open the resource requirement and then select **Book**.</span></span>
3. <span data-ttu-id="90ec1-109">Na página **Assistente da Agenda**, selecione um recurso nomeado para reservar na sua equipa do projeto e, em seguida, selecione **Reservar**.</span><span class="sxs-lookup"><span data-stu-id="90ec1-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then select **Book**.</span></span>

<span data-ttu-id="90ec1-110">Quando a reserva é concluída e cumprida por um recurso nomeado, o recurso genérico é substituído pelo recurso nomeado.</span><span class="sxs-lookup"><span data-stu-id="90ec1-110">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

<span data-ttu-id="90ec1-111">As atribuições na agenda também são atualizadas com o recurso nomeado.</span><span class="sxs-lookup"><span data-stu-id="90ec1-111">The assignments on the schedule are updated with the named resource as well.</span></span>

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="90ec1-112">Cumprir um recurso genérico com vários recursos nomeados</span><span class="sxs-lookup"><span data-stu-id="90ec1-112">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="90ec1-113">O cumprimento de um requisito para um recurso genérico com vários recursos nomeados é semelhante à atribuição de um único recurso nomeado.</span><span class="sxs-lookup"><span data-stu-id="90ec1-113">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="90ec1-114">Por exemplo, existe uma tarefa com uma duração de cinco dias e 120 horas de esforço.</span><span class="sxs-lookup"><span data-stu-id="90ec1-114">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="90ec1-115">Esta tarefa não pode ser concluída por um recurso que funciona num dia de oito horas normal numa semana de cinco dias.</span><span class="sxs-lookup"><span data-stu-id="90ec1-115">This task can't be completed by one resource that works a typical eight-hour day over a five-day week.</span></span> 

<span data-ttu-id="90ec1-116">O requisito é de 120 horas de engenharia robótica em cinco dias, ou seja, 24 horas por dia.</span><span class="sxs-lookup"><span data-stu-id="90ec1-116">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

<span data-ttu-id="90ec1-117">Este é um exemplo de quando são necessários vários recursos nomeados para cumprir um pedido de recurso genérico.</span><span class="sxs-lookup"><span data-stu-id="90ec1-117">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="90ec1-118">Terá de reservar vários recursos para cumprir o requisito.</span><span class="sxs-lookup"><span data-stu-id="90ec1-118">You will need to book multiple resources to fulfill the requirement.</span></span>

<span data-ttu-id="90ec1-119">A principal diferença neste cenário é que o recurso genérico permanece na equipa atribuída à tarefa, e os membros da equipa de recursos nomeados reservados não são atribuídos como parte da posição.</span><span class="sxs-lookup"><span data-stu-id="90ec1-119">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="90ec1-120">O gestor de projeto pode atribuir o trabalho conforme adequado aos recursos nomeados.</span><span class="sxs-lookup"><span data-stu-id="90ec1-120">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="90ec1-121">A vista **Reconciliação** pode ajudar um gestor de projeto a dividir as reservas em vários recursos em atribuições de tarefas.</span><span class="sxs-lookup"><span data-stu-id="90ec1-121">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="90ec1-122">Isto não é efetuado automaticamente porque, em qualquer cenário mais complicado do que o exemplo simples acima, como, por exemplo, o local onde tem um grupo de tarefas que compõem o requisito ou a intenção de como o gestor de projeto pretende atribuir, precisa de ser assumida pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="90ec1-122">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement or the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="90ec1-123">Como o sistema não pode compreender a intenção, é provável que as suposições sejam diferentes das pretensões e um resultado incorreto ou imprevisível será obtido.</span><span class="sxs-lookup"><span data-stu-id="90ec1-123">Because the system can't understand intent, it's likely that the assumptions will be different than intended and an incorrect or unpredictable result will occur.</span></span> <span data-ttu-id="90ec1-124">O resultado previsível é que o recurso genérico permanece atribuído até que o gestor de projeto crie deliberadamente as atribuições, com a ajuda da vista **Reconciliação**.</span><span class="sxs-lookup"><span data-stu-id="90ec1-124">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>


