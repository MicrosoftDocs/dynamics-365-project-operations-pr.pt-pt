---
title: Gerir fusos horários
description: Quando um projeto é criado, o seu fuso horário baseia-se no fuso horário definido no modelo de horas de trabalho aplicado.
author: ruhercul
ms.date: 10/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 1480d68105be1041e791de567b180178b330d71e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997750"
---
# <a name="manage-time-zones"></a><span data-ttu-id="9e3c3-103">Gerir fusos horários</span><span class="sxs-lookup"><span data-stu-id="9e3c3-103">Manage time zones</span></span>

<span data-ttu-id="9e3c3-104">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="9e3c3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


## <a name="projects"></a><span data-ttu-id="9e3c3-105">Projetos</span><span class="sxs-lookup"><span data-stu-id="9e3c3-105">Projects</span></span>

<span data-ttu-id="9e3c3-106">Quando um projeto é criado, o fuso horário baseia-se no fuso horário definido no modelo de horas de trabalho aplicado.</span><span class="sxs-lookup"><span data-stu-id="9e3c3-106">When a project is created, the time zone is based on the time zone defined in the applied work hour template.</span></span> <span data-ttu-id="9e3c3-107">No **Projeto**, as datas são sempre relativas ao fuso horário do utilizador que tem sessão iniciada em cada separador, exceto o separador **Tarefa**. Quando visualizar a estrutura hierárquica do trabalho, as datas serão sempre apresentadas no fuso horário do projeto.</span><span class="sxs-lookup"><span data-stu-id="9e3c3-107">On the **Project** for, the dates are always relative to the time zone of the user that is logged in on each tab, except the **Task** tab. When you view the work breakdown structure, the dates will always be displayed in the project’s time zone.</span></span>

## <a name="tasks"></a><span data-ttu-id="9e3c3-108">Tarefas</span><span class="sxs-lookup"><span data-stu-id="9e3c3-108">Tasks</span></span>

<span data-ttu-id="9e3c3-109">Quando uma tarefa é criada, a hora de início, a hora de fim e as horas/dia são controlados pelas horas de trabalho do projeto.</span><span class="sxs-lookup"><span data-stu-id="9e3c3-109">When a task is created, the start time, end time, and hours/day is controlled by the working hours of the project.</span></span> <span data-ttu-id="9e3c3-110">Por exemplo, se for criada uma tarefa com um projeto cujo fuso horário é -8 PST e tiver as seguintes horas de trabalho: 9:00 às 17:00, segunda a sexta-feira, qualquer tarefa criada sem atribuição respeitará a hora de início e a hora de fim do calendário do projeto.</span><span class="sxs-lookup"><span data-stu-id="9e3c3-110">For example, if a task is created with a project whose time zone is -8 PST and has the following working hours: 9:00 AM to 5:00 PM Monday to Friday, any task created without an assignment will respect the start time and end time of the project calendar.</span></span>

## <a name="manage-resources-with-time-zones"></a><span data-ttu-id="9e3c3-111">Gerir recursos com fusos horários</span><span class="sxs-lookup"><span data-stu-id="9e3c3-111">Manage resources with time zones</span></span>

<span data-ttu-id="9e3c3-112">Para obter resultados precisos e previsíveis ao utilizar **Expandir Reserva**, existem dois pré-requisitos chave que têm de ser cumpridos:</span><span class="sxs-lookup"><span data-stu-id="9e3c3-112">For accurate and predictable results when using **Extend Booking**, there are two key prerequisites that must be met:</span></span>  

- <span data-ttu-id="9e3c3-113">O utilizador tem de configurar o fuso horário do dispositivo para fazer corresponder ao fuso horário definido nas **Definições de Personalização** do sistema.</span><span class="sxs-lookup"><span data-stu-id="9e3c3-113">The user must configure their device's time zone to match the time zone defined in the system's **Personalization Settings**.</span></span>
 
  ![Definições de fuso horário no Windows 10](media/reconcile-assignments-03.png)

  ![Definições de fuso horário nas definições de personalização](media/reconcile-assignments-04.png)
 
- <span data-ttu-id="9e3c3-116">O recurso reservável tem de ter, pelo menos, um minuto de tempo de trabalho que se sobrepõe aos contornos que são utilizados para definir a extensão solicitada.</span><span class="sxs-lookup"><span data-stu-id="9e3c3-116">The bookable resource must have at least one minute of working time that overlaps with the contours that are used to define the requested extension.</span></span> <span data-ttu-id="9e3c3-117">Por exemplo, os seguintes recursos com horas de trabalho que se situam entre as 9:00 e as 19:00 horas.</span><span class="sxs-lookup"><span data-stu-id="9e3c3-117">For example, the following resources with working hours that fall between 9:00 AM and 7:00 PM.</span></span> 

  ![Comparação entre os contornos de recursos](media/reconcile-assignments-05.png)

<span data-ttu-id="9e3c3-119">A tabela seguinte mostra:</span><span class="sxs-lookup"><span data-stu-id="9e3c3-119">The following table shows:</span></span>

- <span data-ttu-id="9e3c3-120">Um modelo de calendário de projeto</span><span class="sxs-lookup"><span data-stu-id="9e3c3-120">A project calendar template</span></span>
- <span data-ttu-id="9e3c3-121">Recurso A: este recurso tem o mesmo calendário e está no mesmo fuso horário que o projeto.</span><span class="sxs-lookup"><span data-stu-id="9e3c3-121">Resource A: This resource has the same calendar and is in the same time zone as the project.</span></span> <span data-ttu-id="9e3c3-122">A hora de início das reservas será 9h00.</span><span class="sxs-lookup"><span data-stu-id="9e3c3-122">The start time of the bookings will be 9:00 AM.</span></span>
- <span data-ttu-id="9e3c3-123">Recurso B: este recurso está localizado num fuso horário diferente daquele do projeto e começa às 7:00 no seu fuso horário.</span><span class="sxs-lookup"><span data-stu-id="9e3c3-123">Resource B: This resource is located in a different time zone than the project and starts at 7:00 AM in their time zone.</span></span> <span data-ttu-id="9e3c3-124">No entanto, as reservas começarão às 9h00, uma vez que se trata da hora de início mais antiga do contorno da atribuição.</span><span class="sxs-lookup"><span data-stu-id="9e3c3-124">However, the bookings will begin at 9:00 AM as that is the earliest start time of the assignment contour.</span></span>
- <span data-ttu-id="9e3c3-125">Recursos C e D: os recursos estão localizados em fusos horários diferentes, entre si e do projeto, e as suas reservas não começam antes das respetivas horas de início disponíveis.</span><span class="sxs-lookup"><span data-stu-id="9e3c3-125">Resources C and D: The resources are located in different time zones, both different from each other and the project, and their bookings start no earlier than their respective available start times.</span></span>

|<span data-ttu-id="9e3c3-126">Entidade</span><span class="sxs-lookup"><span data-stu-id="9e3c3-126">Entity</span></span>  |<span data-ttu-id="9e3c3-127">Calendário</span><span class="sxs-lookup"><span data-stu-id="9e3c3-127">Calendar</span></span>  |
|-|-|
|<span data-ttu-id="9e3c3-128">Modelo de calendário de projeto</span><span class="sxs-lookup"><span data-stu-id="9e3c3-128">Project calendar template</span></span>   | ![calendário do projeto](media/reconcile-assignments-06.png) |
|<span data-ttu-id="9e3c3-130">Recurso A</span><span class="sxs-lookup"><span data-stu-id="9e3c3-130">Resource A</span></span>  | ![Calendário do Recurso A](media/reconcile-assignments-06.png) |
|<span data-ttu-id="9e3c3-132">Recurso B</span><span class="sxs-lookup"><span data-stu-id="9e3c3-132">Resource B</span></span>  |  ![Calendário do Recurso B](media/reconcile-assignments-07.png) |
|<span data-ttu-id="9e3c3-134">Recurso C</span><span class="sxs-lookup"><span data-stu-id="9e3c3-134">Resource C</span></span>  |  ![Calendário do Recurso C](media/reconcile-assignments-08.png) |
|<span data-ttu-id="9e3c3-136">Recurso D</span><span class="sxs-lookup"><span data-stu-id="9e3c3-136">Resource D</span></span>  | ![Calendário do Recurso D](media/reconcile-assignments-09.png)  |
 
<span data-ttu-id="9e3c3-138">Quando navega para a vista **Reconciliação**, são apresentadas as atribuições de recursos e as faltas de reservas associadas.</span><span class="sxs-lookup"><span data-stu-id="9e3c3-138">When you navigate to the **Reconciliation** view, the resource assignments and the associated booking shortages are displayed.</span></span>

![Vista de reconciliação antes da extensão](media/reconcile-assignments-10.png)

<span data-ttu-id="9e3c3-140">Após a utilização da funcionalidade Expandir Reserva para cada recurso, as reservas são expandidas com êxito para cada recurso porque as horas de trabalho de cada recurso sobrepõem-se aos perfis da escassez.</span><span class="sxs-lookup"><span data-stu-id="9e3c3-140">After the extend booking functionality has been used for each resource, bookings are successfully extended for each resource because each resource’s working hours overlapped with the contours of the shortage.</span></span>

![Vista de reconciliação após a extensão da reserva](media/reconcile-assignments-11.png) 

<span data-ttu-id="9e3c3-142">Note que um olhar mais atento aos detalhes das reservas mostra diferenças na hora de início das reservas.</span><span class="sxs-lookup"><span data-stu-id="9e3c3-142">Notice that a closer look at the details of the bookings shows differences in the start time of the bookings.</span></span> <span data-ttu-id="9e3c3-143">As reservas não começam antes da hora de início do perfil da atribuição e não antes da hora de início disponível do recurso.</span><span class="sxs-lookup"><span data-stu-id="9e3c3-143">The bookings start no earlier than the start time of the assignment contour and no earlier than the available start time of the resource.</span></span>

![Novas reservas dos recursos no quadro da agenda](media/reconcile-assignments-12.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]