---
title: Reservar para um projeto
description: Este tópico fornece informações sobre como reservar um recurso para um projeto.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 19128264ed3db7efeeba948155f0ddbdc806c2a0
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908481"
---
# <a name="book-to-a-project"></a><span data-ttu-id="81d95-103">Reservar para um projeto</span><span class="sxs-lookup"><span data-stu-id="81d95-103">Book to a project</span></span>

<span data-ttu-id="81d95-104">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="81d95-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="81d95-105">Por vezes, um Gestor de Projetos ou Gestor de Recursos terá de alocar um recurso para a um projeto sem que seja definido um requisito específico a partir de um membro da equipa genérico.</span><span class="sxs-lookup"><span data-stu-id="81d95-105">There are times where a Project manager or Resource manager will need to allocate a resource to project without a specific requirement being defined from a generic team member.</span></span> <span data-ttu-id="81d95-106">Isto pode ser conseguido de uma de três formas.</span><span class="sxs-lookup"><span data-stu-id="81d95-106">This can be achieved in one of three ways.</span></span>

- <span data-ttu-id="81d95-107">Reservar a partir da grelha de membro de equipa</span><span class="sxs-lookup"><span data-stu-id="81d95-107">Book from the team member grid</span></span>
- <span data-ttu-id="81d95-108">Reservar a partir do quadro da agenda</span><span class="sxs-lookup"><span data-stu-id="81d95-108">Book from the schedule board</span></span>
- <span data-ttu-id="81d95-109">Reservar a partir do formulário **Projeto**</span><span class="sxs-lookup"><span data-stu-id="81d95-109">Book from the **Project** form</span></span>

## <a name="book-from-the-team-member-grid"></a><span data-ttu-id="81d95-110">Reservar a partir da grelha de membro de equipa</span><span class="sxs-lookup"><span data-stu-id="81d95-110">Book from the team member grid</span></span>

<span data-ttu-id="81d95-111">Se a sua organização estiver a operar no modo híbrido Alocação de recursos, o Gestor de Projetos pode reservar um recurso diretamente para o projeto ao concluir os seguintes passos.</span><span class="sxs-lookup"><span data-stu-id="81d95-111">If your organization is operating in hybrid Resource allocation mode, the Project manager can book a resource directly to the project by completing the following steps.</span></span>

1. <span data-ttu-id="81d95-112">A partir do projeto, vá para a grelha de membro de equipa e selecione **Novo**.</span><span class="sxs-lookup"><span data-stu-id="81d95-112">From the project, go to the team member grid and select **New**.</span></span>
2. <span data-ttu-id="81d95-113">Defina o nome da posição e a função do recurso.</span><span class="sxs-lookup"><span data-stu-id="81d95-113">Define the position name and the role of the resource.</span></span>
3. <span data-ttu-id="81d95-114">Selecione o recurso reservável a partir da pesquisa disponível.</span><span class="sxs-lookup"><span data-stu-id="81d95-114">Select the bookable resource from the available lookup.</span></span>
4. <span data-ttu-id="81d95-115">Depois de selecionar o recurso, defina as seguintes informações do campo para reservar o recurso:</span><span class="sxs-lookup"><span data-stu-id="81d95-115">After you select the resource, define the following field information to book the resource:</span></span>

    - <span data-ttu-id="81d95-116">Data de início</span><span class="sxs-lookup"><span data-stu-id="81d95-116">Start date</span></span>
    - <span data-ttu-id="81d95-117">Data de conclusão</span><span class="sxs-lookup"><span data-stu-id="81d95-117">Finish date</span></span>
    - <span data-ttu-id="81d95-118">Método de alocação</span><span class="sxs-lookup"><span data-stu-id="81d95-118">Allocation method</span></span>
    - <span data-ttu-id="81d95-119">Horas, se aplicável</span><span class="sxs-lookup"><span data-stu-id="81d95-119">Hours, if applicable</span></span>
    - <span data-ttu-id="81d95-120">Aprovador do projeto</span><span class="sxs-lookup"><span data-stu-id="81d95-120">Project approver</span></span>

6. <span data-ttu-id="81d95-121">Selecione **Guardar e Fechar**</span><span class="sxs-lookup"><span data-stu-id="81d95-121">Select **Save and Close**</span></span>

## <a name="book-from-the-schedule-board"></a><span data-ttu-id="81d95-122">Reservar a partir do quadro da agenda</span><span class="sxs-lookup"><span data-stu-id="81d95-122">Book from the schedule board</span></span>

<span data-ttu-id="81d95-123">Quando um Gestor de Recursos precisa de reservar um recurso diretamente para um projeto, pode utilizar o quadro da agenda e os requisitos do projeto.</span><span class="sxs-lookup"><span data-stu-id="81d95-123">When a Resource manager needs to book a resource directly to a project, they can use the schedule board and the project requirement.</span></span> <span data-ttu-id="81d95-124">O requisito do projeto é um requisito de recursos que está sempre disponível para ser reservado novamente.</span><span class="sxs-lookup"><span data-stu-id="81d95-124">The project requirement is a resource requirement that is always available to be booked against.</span></span> <span data-ttu-id="81d95-125">Para reservar diretamente para um formulário de projeto a partir do quadro da agenda, execute os seguintes passos.</span><span class="sxs-lookup"><span data-stu-id="81d95-125">To book directly to a project form the schedule board, complete the following steps.</span></span>

1. <span data-ttu-id="81d95-126">Navegue para o quadro da agenda e, na página esquerda, filtre pelos recursos que está a considerar para o requisito.</span><span class="sxs-lookup"><span data-stu-id="81d95-126">Navigate to the schedule board and on the left page, filter for the resources you are considering for the requirement.</span></span>
2. <span data-ttu-id="81d95-127">No painel inferior, selecione o separador **Projeto** para ver uma lista dos requisitos do projeto.</span><span class="sxs-lookup"><span data-stu-id="81d95-127">In the bottom pane, select the **Project** tab to view a list of project requirements.</span></span>
3. <span data-ttu-id="81d95-128">Arraste o requisito para um recurso e defina as seguintes informações:</span><span class="sxs-lookup"><span data-stu-id="81d95-128">Drag the requirement onto a resource and define the following information:</span></span>

    - <span data-ttu-id="81d95-129">Data de início</span><span class="sxs-lookup"><span data-stu-id="81d95-129">Start date</span></span>
    - <span data-ttu-id="81d95-130">Data de conclusão</span><span class="sxs-lookup"><span data-stu-id="81d95-130">Finish date</span></span>
    - <span data-ttu-id="81d95-131">Estado de reserva</span><span class="sxs-lookup"><span data-stu-id="81d95-131">Booking status</span></span>
    - <span data-ttu-id="81d95-132">Método de reserva</span><span class="sxs-lookup"><span data-stu-id="81d95-132">Booking method</span></span>
    - <span data-ttu-id="81d95-133">Duração</span><span class="sxs-lookup"><span data-stu-id="81d95-133">Duration</span></span>

## <a name="book-from-the-project-form"></a><span data-ttu-id="81d95-134">Reservar a partir do formulário Projeto</span><span class="sxs-lookup"><span data-stu-id="81d95-134">Book from the Project form</span></span>

<span data-ttu-id="81d95-135">Como Gestor de projetos, pode precisar de reservar um recurso para um projeto, mas conhecer apenas os critérios, em vez do nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="81d95-135">As a Project manager, you might need to book a resource to a project, but only know the criteria rather than the name of the resource.</span></span> <span data-ttu-id="81d95-136">Conclua os seguintes passos para utilizar o assistente da agenda para localizar um recurso baseado em quaisquer atributos disponíveis do recurso.</span><span class="sxs-lookup"><span data-stu-id="81d95-136">Complete the following steps to use the schedule assistant to find a resource based on any available attributes of the resource.</span></span> 

1. <span data-ttu-id="81d95-137">Navegue para o projeto e selecione **Reservar** para abrir o Assistente da Agenda.</span><span class="sxs-lookup"><span data-stu-id="81d95-137">Navigate to the project and select **Book** to open the Schedule Assistant.</span></span>
2. <span data-ttu-id="81d95-138">Utilize os filtros no lado esquerdo do Assistente da Agenda para reduzir os critérios e selecione **Procurar**.</span><span class="sxs-lookup"><span data-stu-id="81d95-138">Using the filters on the left side of the Schedule Assistant, narrow the criteria and select **Search.**</span></span>
3. <span data-ttu-id="81d95-139">Baseado nos recursos devolvidos nos resultados, pode reservar um recurso.</span><span class="sxs-lookup"><span data-stu-id="81d95-139">Based on resources returned in the results, you can book a resource.</span></span>

> [!NOTE]
> <span data-ttu-id="81d95-140">Este método não cria quaisquer reservas para o recurso.</span><span class="sxs-lookup"><span data-stu-id="81d95-140">This method doesn't create any bookings for the resource.</span></span> <span data-ttu-id="81d95-141">Em vez disso, adiciona o recurso à equipa.</span><span class="sxs-lookup"><span data-stu-id="81d95-141">Instead, it adds the resource to the team.</span></span> <span data-ttu-id="81d95-142">Depois de o membro da equipa ser adicionado ao projeto, o gestor de projetos pode utilizar a opção para manter as reservas ou prolongar as reservas para adicionar as reservas necessárias ao recurso.</span><span class="sxs-lookup"><span data-stu-id="81d95-142">After the team member has been added to the project, the project manager can use maintain bookings or extend bookings to add the required bookings to the resource.</span></span>
