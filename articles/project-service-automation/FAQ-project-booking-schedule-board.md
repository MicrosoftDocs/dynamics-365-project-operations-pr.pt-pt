---
title: Criar uma reserva de projeto no quadro da Agenda
description: Este tópico fornece informações sobre como criar uma reserva de projeto a partir do quadro da agenda.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
ms.topic: article
ms.prod: Dynamics 365 Project Service Automation 2.x and 3.x
ms.technology: ''
ms.assetid: bbc1bbe2-3482-4b84-9e89-f7e0e585ade8
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 7b6c7e07ea6451e0654ccf1ba7be10e7b38e0d09
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754595"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a><span data-ttu-id="d26ac-103">Criar uma reserva de projeto no quadro da Agenda</span><span class="sxs-lookup"><span data-stu-id="d26ac-103">Create a project booking from the Schedule board</span></span>

<span data-ttu-id="d26ac-104">Pode reservar um recurso para um projeto diretamente no separador **Equipa** do projeto ou através da geração de um requisito de recurso de uma atribuição de membro da equipa genérico e, em seguida, preenchendo o requisito gerado com um membro da equipa do projeto.</span><span class="sxs-lookup"><span data-stu-id="d26ac-104">You can book a resource onto a project directly from the **Team** tab of the project or by generating a resource requirement from a generic team member assignment and then fulfilling the generated requirement with a project team member.</span></span>

<span data-ttu-id="d26ac-105">Também é possível reservar um recurso para um projeto diretamente do quadro da Agenda.</span><span class="sxs-lookup"><span data-stu-id="d26ac-105">You can also book a resource onto a project directly from the Schedule board.</span></span> <span data-ttu-id="d26ac-106">Existem três formas de o fazer:</span><span class="sxs-lookup"><span data-stu-id="d26ac-106">There are three ways to do this:</span></span>

- <span data-ttu-id="d26ac-107">**Reservar a partir de um requisito de recurso gerado:** pode gerar um requisito de recurso depois de criar um recurso genérico e atribuir tarefas num projeto.</span><span class="sxs-lookup"><span data-stu-id="d26ac-107">**Book from a generated resource requirement:** You can generate a resource requirement after you create a generic resource and assign tasks within a project.</span></span>

- <span data-ttu-id="d26ac-108">**Reservar a partir do requisito principal:** os requisitos principais são mostrados no quadro da Agenda no separador **Projeto**.</span><span class="sxs-lookup"><span data-stu-id="d26ac-108">**Book from the primary requirement:** The primary requirements show up on the Schedule board on the **Project** tab.</span></span> 

- <span data-ttu-id="d26ac-109">**Reservar a partir de um requisito de recurso novo:** pode criar um requisito de recurso do zero e associá-lo a um projeto.</span><span class="sxs-lookup"><span data-stu-id="d26ac-109">**Book from a new resource requirement:** You can create a resource requirement from scratch and associate it with a project.</span></span> <span data-ttu-id="d26ac-110">No quadro da Agenda, o requisito de recurso é mostrado no separador **Abrir Requisitos**.</span><span class="sxs-lookup"><span data-stu-id="d26ac-110">On the Schedule board, the resource requirement shows up on the **Open Requirements** tab.</span></span>

## <a name="book-from-a-generated-resource-requirement"></a><span data-ttu-id="d26ac-111">Reservar a partir de um requisito de recurso gerado</span><span class="sxs-lookup"><span data-stu-id="d26ac-111">Book from a generated resource requirement</span></span>

<span data-ttu-id="d26ac-112">Pode criar um recurso genérico e atribuí-lo a uma ou mais tarefas dentro de um projeto.</span><span class="sxs-lookup"><span data-stu-id="d26ac-112">You can create a generic resource and assign it one or more tasks within a project.</span></span> <span data-ttu-id="d26ac-113">Em seguida, pode gerar um requisito de recurso a partir do membro da equipa genérico.</span><span class="sxs-lookup"><span data-stu-id="d26ac-113">Then you can generate a resource requirement from the generic team member.</span></span> 

1.  <span data-ttu-id="d26ac-114">No quadro da Agenda, este recurso será mostrado no separador **Abrir Requisitos**. Também poderá ter de utilizar os filtros de coluna na grelha se tiver muitos requisitos abertos.</span><span class="sxs-lookup"><span data-stu-id="d26ac-114">On the Schedule board, this resource will show up on the **Open Requirements** tab. You might need to use column filters on the grid if you have many open requirements.</span></span> 

    <span data-ttu-id="d26ac-115">![Abrir o separador Requisitos no quadro Agenda](media/FAQ-Project-Booking-Schedule-Board-1.png "Captura de ecrã da tabela de reservas e atribuições")</span><span class="sxs-lookup"><span data-stu-id="d26ac-115">![Open Requirements tab on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-1.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="d26ac-116">Selecione o requisito.</span><span class="sxs-lookup"><span data-stu-id="d26ac-116">Select the requirement.</span></span> <span data-ttu-id="d26ac-117">O separador **Localizar Disponibilidade** será apresentado na parte superior da linha selecionada.</span><span class="sxs-lookup"><span data-stu-id="d26ac-117">The **Find Availability** tab will appear at the top of the selected row.</span></span>
 
3. <span data-ttu-id="d26ac-118">Quando selecionar o separador, o modo de Assistente de Agenda do quadro da agenda é aberto e, em seguida, filtra os recursos disponíveis que cumprem o requisito de recurso.</span><span class="sxs-lookup"><span data-stu-id="d26ac-118">When you select the tab, the Schedule Assistant mode of the Schedule board opens and then filters the available resources that meet the resource requirement.</span></span> <span data-ttu-id="d26ac-119">Depois disso, pode reservar um recurso.</span><span class="sxs-lookup"><span data-stu-id="d26ac-119">After that, you can book a resource.</span></span>

4. <span data-ttu-id="d26ac-120">Também pode arrastar e largar a linha selecionada da parte inferior do quadro da Agenda numa célula de recurso na grelha acima.</span><span class="sxs-lookup"><span data-stu-id="d26ac-120">You can also drag and drop the selected row from the bottom of the Schedule board to a resource cell in the grid above.</span></span> <span data-ttu-id="d26ac-121">Quando for largado, abre o painel **Criar Reserva de Recursos** à direita.</span><span class="sxs-lookup"><span data-stu-id="d26ac-121">When you drop it, it opens the **Create Resource Booking** panel on the right.</span></span>

    <span data-ttu-id="d26ac-122">Selecionar **Reservar** reserva o recurso para a equipa do projeto.</span><span class="sxs-lookup"><span data-stu-id="d26ac-122">Selecting **Book** books the resource onto the project team.</span></span>

![Painel Criar Reserva de Recursos](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a><span data-ttu-id="d26ac-124">Reservar a partir do Requisito Principal</span><span class="sxs-lookup"><span data-stu-id="d26ac-124">Book from the Primary Requirement</span></span>

<span data-ttu-id="d26ac-125">Criar um projeto no Project Service automaticamente cria um requisito de recursos denominado o Requisito Principal.</span><span class="sxs-lookup"><span data-stu-id="d26ac-125">Creating a project in Project Service automatically creates a resource requirement called the Primary Requirement.</span></span> <span data-ttu-id="d26ac-126">Este é um requisito vazio que é utilizado para reservar rapidamente um recurso com quadro da Agenda sem a geração de um requisito ou a criação de um do zero.</span><span class="sxs-lookup"><span data-stu-id="d26ac-126">This is an empty requirement that is used to quickly book a resource with the Schedule board without generating a requirement or creating one from scratch.</span></span> <span data-ttu-id="d26ac-127">Visto que o requisito está vazio, terá de especificar as datas, bem como o método de alocação e as horas, se aplicável.</span><span class="sxs-lookup"><span data-stu-id="d26ac-127">Because the requirement is empty, you’ll need to specify dates as well as the allocation method and hours, if applicable.</span></span> 

1. <span data-ttu-id="d26ac-128">Para reservar um recurso com o Requisito Principal, no quadro da Agenda, selecione o separador **Projeto**. Se tiver vários projetos, poderá ter de utilizar o filtro de colunas no **Projeto**.</span><span class="sxs-lookup"><span data-stu-id="d26ac-128">To book a resource with the Primary Requirement, on the Schedule board, select the **Project** tab. You might need to use the column filter on the **Project** column if you have many projects.</span></span>

   <span data-ttu-id="d26ac-129">![Filtros de colunas no quadro Agenda](media/FAQ-Project-Booking-Schedule-Board-2.png "Captura de ecrã da tabela de reservas e atribuições")</span><span class="sxs-lookup"><span data-stu-id="d26ac-129">![Column filters on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-2.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="d26ac-130">Selecione o requisito que só tem o nome do projeto como o respetivo nome e uma duração de zero (0).</span><span class="sxs-lookup"><span data-stu-id="d26ac-130">Select the requirement that only has the project name as its name and has a duration of zero (0).</span></span>

3. <span data-ttu-id="d26ac-131">Selecione o separador **Localizar Disponibilidade** que é apresentado na linha.</span><span class="sxs-lookup"><span data-stu-id="d26ac-131">Select the **Find Availability** tab that appears on the row.</span></span> <span data-ttu-id="d26ac-132">Isto coloca o quadro da Agenda no modo do Assistente de Agenda e mostra os recursos disponíveis que podem ser reservados para o projeto.</span><span class="sxs-lookup"><span data-stu-id="d26ac-132">This puts the Schedule board in Schedule Assistant mode and shows the available resources that can be booked onto the project.</span></span>

4. <span data-ttu-id="d26ac-133">Como um **Requisito Principal** é um requisito vazio com duração zero (0), terá de definir a duração no painel **Criar Reserva de Recursos** quando selecionar e reservar um recurso.</span><span class="sxs-lookup"><span data-stu-id="d26ac-133">Because a **Primary Requirement** is an empty requirement with zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when selecting and booking a resource.</span></span>

5. <span data-ttu-id="d26ac-134">Também pode selecionar o **Requisito Principal do Projeto** na parte inferior da quadro da Agenda e arraste e largue-o num recurso para reservá-lo.</span><span class="sxs-lookup"><span data-stu-id="d26ac-134">You can also select the **Project Primary Requirement** at the bottom of the Schedule board and drag and drop it on a resource to book it.</span></span>
 
    <span data-ttu-id="d26ac-135">Como o **Requisito Principal** é um requisito vazio com duração zero (0), terá de definir a duração no painel **Criar Reserva de Recursos** quando selecionar e reservar um recurso.</span><span class="sxs-lookup"><span data-stu-id="d26ac-135">Because the **Primary Requirement** is an empty requirement that has zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when you select and book a resource.</span></span>
 
    <span data-ttu-id="d26ac-136">Quando reserva um recurso através do **Requisito Principal** no quadro da Agenda, adiciona-o à equipa do projeto sem quaisquer atribuições.</span><span class="sxs-lookup"><span data-stu-id="d26ac-136">When you book a resource through the **Primary Requirement** on the Schedule board, you add it to the project team without any assignments.</span></span>
 
## <a name="book-from-a-new-resource-requirement"></a><span data-ttu-id="d26ac-137">Reservar a partir de um requisito de recurso novo</span><span class="sxs-lookup"><span data-stu-id="d26ac-137">Book from a new resource requirement</span></span>
<span data-ttu-id="d26ac-138">Conclua os seguintes passos para reservar a partir de um novo requisito de recurso.</span><span class="sxs-lookup"><span data-stu-id="d26ac-138">Complete the following steps to book from a new resource requirement.</span></span> 

1. <span data-ttu-id="d26ac-139">Aceda a **Requisitos de Recursos** e, em seguida, selecione **Novo** para criar um novo requisito de recurso.</span><span class="sxs-lookup"><span data-stu-id="d26ac-139">Go to **Resource Requirements**, and then select **New** to create a new resource requirement.</span></span>

2. <span data-ttu-id="d26ac-140">No separador **Projeto**, selecione um projeto para associar o requisito ao projeto.</span><span class="sxs-lookup"><span data-stu-id="d26ac-140">On the **Project** tab, select a project to associate the requirement to the project.</span></span>
 
    <span data-ttu-id="d26ac-141">No quadro da Agenda, este novo requisito é apresentado como um **Requisito Aberto** que pode preencher.</span><span class="sxs-lookup"><span data-stu-id="d26ac-141">On the Schedule board, this new requirement shows as an **Open Requirement** that you can fulfill.</span></span>

3. <span data-ttu-id="d26ac-142">Reserve o recurso para adicioná-lo à equipa do projeto.</span><span class="sxs-lookup"><span data-stu-id="d26ac-142">Book the resource to add it to the project team.</span></span>

4. <span data-ttu-id="d26ac-143">Agora que o recurso está reservado, tem de atribuir tarefas manualmente.</span><span class="sxs-lookup"><span data-stu-id="d26ac-143">Now that the resource is booked, you must assign tasks manually.</span></span>

