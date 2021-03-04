---
title: Reservar recursos nomeados a partir de requisitos de recursos
description: Este tópico fornece informações sobre a reserva de recursos nomeados para um requisito de recurso genérico.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: c7a6370bde434b74d05e342240abd9bba84d34d8
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145117"
---
# <a name="book-named-resources-from-resource-requirements"></a><span data-ttu-id="1539d-103">Reservar recursos nomeados a partir de requisitos de recursos</span><span class="sxs-lookup"><span data-stu-id="1539d-103">Book named resources from resource requirements</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="1539d-104">Pode reservar um recurso nomeado para substituir o recurso genérico que tem um requisito de recurso.</span><span class="sxs-lookup"><span data-stu-id="1539d-104">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="1539d-105">No Project Service Automation (PSA), na página **Projetos**, clique no separador **Equipa**.</span><span class="sxs-lookup"><span data-stu-id="1539d-105">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab.</span></span>
2. <span data-ttu-id="1539d-106">Selecione o recurso genérico que tem um requisito de recurso a partir da lista e, em seguida, clique em **Reservar**.</span><span class="sxs-lookup"><span data-stu-id="1539d-106">Select the generic resource that has a resource requirement from the list and then click **Book**.</span></span> <span data-ttu-id="1539d-107">Ou abra o requisito de recurso e, em seguida, clique em **Reservar**.</span><span class="sxs-lookup"><span data-stu-id="1539d-107">Or, open the resource requirement and then click **Book**.</span></span>


![Reservar um membro da equipa genérico](media/RM-how-to-14.png)


3. <span data-ttu-id="1539d-109">Na página **Assistente da Agenda**, selecione um recurso nomeado para reservar na sua equipa do projeto e, em seguida, clique em **Reservar**.</span><span class="sxs-lookup"><span data-stu-id="1539d-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then click **Book**.</span></span>

![Reservar um membro da equipa genérico utilizando o assistente da agenda](media/RM-how-to-15.png)

<span data-ttu-id="1539d-111">Quando a reserva é concluída e cumprida por um recurso nomeado, o recurso genérico é substituído pelo recurso nomeado.</span><span class="sxs-lookup"><span data-stu-id="1539d-111">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

![Membro da equipa nomeado que substitui um membro da equipa genérico](media/RM-how-to-16.png)

<span data-ttu-id="1539d-113">As atribuições na agenda também são atualizadas com o recurso nomeado.</span><span class="sxs-lookup"><span data-stu-id="1539d-113">The assignments on the schedule are updated with the named resource as well.</span></span>

![Membro da equipa nomeado atribuído a tarefas do projeto](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="1539d-115">Cumprir um recurso genérico com vários recursos nomeados</span><span class="sxs-lookup"><span data-stu-id="1539d-115">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="1539d-116">O cumprimento de um requisito para um recurso genérico com vários recursos nomeados é semelhante à atribuição de um único recurso nomeado.</span><span class="sxs-lookup"><span data-stu-id="1539d-116">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="1539d-117">Por exemplo, existe uma tarefa com uma duração de cinco dias e 120 horas de esforço.</span><span class="sxs-lookup"><span data-stu-id="1539d-117">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="1539d-118">Esta tarefa não pode ser concluída por um recurso que funciona num dia de oito horas normal numa semana de cinco dias.</span><span class="sxs-lookup"><span data-stu-id="1539d-118">This task can't be completed by one resource that works a typical eight-hour day over a five day week.</span></span> 

![Uma tarefa que necessita de 120 horas de esforço durante cinco dias](media/RM-how-to-21.png)

<span data-ttu-id="1539d-120">O requisito é de 120 horas de engenharia robótica em cinco dias, ou seja, 24 horas por dia.</span><span class="sxs-lookup"><span data-stu-id="1539d-120">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

![Requisito por dia](media/RM-how-to-22.png)

<span data-ttu-id="1539d-122">Este é um exemplo de quando são necessários vários recursos nomeados para cumprir um pedido de recurso genérico.</span><span class="sxs-lookup"><span data-stu-id="1539d-122">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="1539d-123">Terá de reservar vários recursos para cumprir o requisito.</span><span class="sxs-lookup"><span data-stu-id="1539d-123">You will need to book multiple resources to fulfill the requirement.</span></span>

![Reservar vários recursos para cumprir o requisito](media/RM-how-to-23.png)

<span data-ttu-id="1539d-125">A principal diferença neste cenário é que o recurso genérico permanece na equipa atribuída à tarefa, e os membros da equipa de recursos nomeados reservados não são atribuídos como parte da posição.</span><span class="sxs-lookup"><span data-stu-id="1539d-125">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="1539d-126">O gestor de projeto pode atribuir o trabalho conforme adequado aos recursos nomeados.</span><span class="sxs-lookup"><span data-stu-id="1539d-126">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="1539d-127">A vista **Reconciliação** pode ajudar um gestor de projeto a dividir as reservas em vários recursos em atribuições de tarefas.</span><span class="sxs-lookup"><span data-stu-id="1539d-127">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="1539d-128">Isto não é efetuado automaticamente porque, em qualquer cenário mais complicado do que o exemplo simples acima, como, por exemplo, o local onde tem um grupo de tarefas que compõem o requisito, a intenção de como o gestor de projeto pretende atribuir, precisa de ser assumida pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="1539d-128">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement, the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="1539d-129">Uma vez que o sistema não consegue compreender as intenções, é provável que as suposições sejam diferentes das pretendidas e irá acontecer um resultado incorreto ou imprevisível.</span><span class="sxs-lookup"><span data-stu-id="1539d-129">Because the system can't understand intent, chances are that the assumptions will be different than intended and an incorrect or unpredictable result will happen.</span></span> <span data-ttu-id="1539d-130">O resultado previsível é que o recurso genérico permanece atribuído até que o gestor de projeto crie deliberadamente as atribuições, com a ajuda da vista **Reconciliação**.</span><span class="sxs-lookup"><span data-stu-id="1539d-130">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>


