---
title: Agendar recursos para um projeto
description: Como agendar recursos para um projeto no Project Service
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: c67633960bb448d2190ec1bfde4e964f4fcb7969
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008505"
---
# <a name="schedule-resources-for-a-project-project-service"></a><span data-ttu-id="1ea2c-103">Agendar recursos para um projeto (Project Service)</span><span class="sxs-lookup"><span data-stu-id="1ea2c-103">Schedule resources for a project (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="1ea2c-104">Pode verificar a disponibilidade de recursos para obter uma visão global das reservas dos seus recursos ou filtrar a vista por competências, equipa, localização, entre outras opções.</span><span class="sxs-lookup"><span data-stu-id="1ea2c-104">You can check resource availability to get an overall view of how booked your resources are, or you can filter the view by skills, team, location, and other options.</span></span>  
  
<span data-ttu-id="1ea2c-105">O quadro da agenda mostra a lista de recursos e a respetiva disponibilidade.</span><span class="sxs-lookup"><span data-stu-id="1ea2c-105">The schedule board shows list of resources and their availability.</span></span> <span data-ttu-id="1ea2c-106">Selecione um modo de vista para mostrar a disponibilidade por **Horas**, **Dia**, **Semana** ou **Mês**.</span><span class="sxs-lookup"><span data-stu-id="1ea2c-106">Select a view mode to show availability by **Hours**, **Day**, **Week**, or **Month**.</span></span>  
  
<span data-ttu-id="1ea2c-107">Antes de utilizar o quadro da agenda, é importante configurá-lo.</span><span class="sxs-lookup"><span data-stu-id="1ea2c-107">Before you use the schedule board, it’s important to set it up.</span></span> <span data-ttu-id="1ea2c-108">Para mais informações, consulte [Configurar o quadro da agenda (Field Service ou Project Service Automation)](/dynamics365/field-service/configure-schedule-board).</span><span class="sxs-lookup"><span data-stu-id="1ea2c-108">For more information, see [Configure the schedule board (Field Service or Project Service Automation)](/dynamics365/field-service/configure-schedule-board).</span></span>
  
<span data-ttu-id="1ea2c-109">Se estiver a utilizar uma versão mais antiga, para a disponibilidade de recursos, consulte [Ver disponibilidade de recursos](../psa/view-resource-availability.md).</span><span class="sxs-lookup"><span data-stu-id="1ea2c-109">If you are using an older version, for resource availability, see [View resource availability](../psa/view-resource-availability.md).</span></span>  

> [!IMPORTANT]
>  <span data-ttu-id="1ea2c-110">Para utilizar a funcionalidade de reserva do quadro da agenda, a geocodificação e os serviços de localização é necessário ativar os mapas.</span><span class="sxs-lookup"><span data-stu-id="1ea2c-110">To use the schedule board booking functionality, geocoding, and location services, you need to turn on maps.</span></span>  
> 
> 1. <span data-ttu-id="1ea2c-111">No menu principal, selecione **Agendamento de Recursos** > **Administração**.</span><span class="sxs-lookup"><span data-stu-id="1ea2c-111">On the main menu, select **Resource Scheduling** > **Administration**.</span></span>  
> 2. <span data-ttu-id="1ea2c-112">Clique em **Parâmetros de agendamento**.</span><span class="sxs-lookup"><span data-stu-id="1ea2c-112">Click **Scheduling parameters**.</span></span>  
> 3. <span data-ttu-id="1ea2c-113">Abra o registo e desloque-se para baixo para a secção **Resource Scheduling Optimization**.</span><span class="sxs-lookup"><span data-stu-id="1ea2c-113">Open record and scroll down to the **Resource Scheduling Optimization** section.</span></span>  
> 4. <span data-ttu-id="1ea2c-114">No campo **Ligar a Mapas**, escolha **Sim**.</span><span class="sxs-lookup"><span data-stu-id="1ea2c-114">On the **Connect to Maps** field, choose **Yes**.</span></span>  
> 5. <span data-ttu-id="1ea2c-115">Aceitar termos e guardar o registo.</span><span class="sxs-lookup"><span data-stu-id="1ea2c-115">Accept terms and save the record.</span></span>  
> 6. <span data-ttu-id="1ea2c-116">No menu principal, selecione **Project Service** > **Quadro da agenda**.</span><span class="sxs-lookup"><span data-stu-id="1ea2c-116">On the main menu, select **Project Service** > **Schedule board**.</span></span> <span data-ttu-id="1ea2c-117">A partir daqui, existem várias formas de agendar manualmente um requisito de reserva.</span><span class="sxs-lookup"><span data-stu-id="1ea2c-117">From here, there are several ways to manually schedule a booking requirement.</span></span> <span data-ttu-id="1ea2c-118">Escolha o método que funciona para si.</span><span class="sxs-lookup"><span data-stu-id="1ea2c-118">Choose the method that works for you.</span></span>
  
## <a name="find-available-resources"></a><span data-ttu-id="1ea2c-119">Localizar recursos disponíveis</span><span class="sxs-lookup"><span data-stu-id="1ea2c-119">Find available resources</span></span>

1.  <span data-ttu-id="1ea2c-120">A partir da lista **Requisitos de Reserva**, clique com o botão direito do rato numa reserva não agendada e escolha uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="1ea2c-120">From the **Booking Requirement** list, right-click an unscheduled booking and choose one of the following:</span></span>  
  
- <span data-ttu-id="1ea2c-121">Escolha **Localizar disponibilidade - Recursos Atuais** para localizar um recurso disponível a partir da lista no quadro da agenda.</span><span class="sxs-lookup"><span data-stu-id="1ea2c-121">Choose **Find availability - Current Resources** to find an available resource from the list on the schedule board.</span></span>  
- <span data-ttu-id="1ea2c-122">Escolha **Localizar disponibilidade - Todos os Recursos** para localizar um recurso disponível a partir dos recursos no sistema</span><span class="sxs-lookup"><span data-stu-id="1ea2c-122">Choose **Find availability - All Resources**, to find an available resource from resources in the system</span></span>  
   > [!NOTE]
   >  <span data-ttu-id="1ea2c-123">Quando o fizer, os filtros mostrarão as opções para o requisito de reserva selecionado.</span><span class="sxs-lookup"><span data-stu-id="1ea2c-123">When you do this, the filters will show options for the selected booking requirement.</span></span>  
  
2. <span data-ttu-id="1ea2c-124">Quando o horário disponível for apresentado, clique com o botão direito do rato no horário no quadro da agenda e escolha **Reservar**.</span><span class="sxs-lookup"><span data-stu-id="1ea2c-124">When you see an available slot, right-click the time slot on the schedule board and choose **Book Here**.</span></span> <span data-ttu-id="1ea2c-125">Em alternativa, arraste e largue o requisito de reserva para o horário disponível.</span><span class="sxs-lookup"><span data-stu-id="1ea2c-125">Or, drag and drop the booking requirement to the available time slot.</span></span>  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a><span data-ttu-id="1ea2c-126">Agendar um recurso através da vista diária e determinar quem está sub-reservado</span><span class="sxs-lookup"><span data-stu-id="1ea2c-126">Book a resource using the daily view and find who’s under-booked</span></span>
  
1.  <span data-ttu-id="1ea2c-127">No quadro da agenda, selecione **Modo de Vista** e selecione **Dias**.</span><span class="sxs-lookup"><span data-stu-id="1ea2c-127">On the schedule board, select **View Mode** and select **Days**.</span></span>  
  
    <span data-ttu-id="1ea2c-128">Mostra uma vista de grelha com o número de horas que um recurso está reservado por dia e em que dias está livre.</span><span class="sxs-lookup"><span data-stu-id="1ea2c-128">This shows a grid view of how many hours a resource is booked per day and which days they are free.</span></span>  
  
2.  <span data-ttu-id="1ea2c-129">Clique no nome do recurso que pretende reservar e, em seguida, selecione **Reservar**.</span><span class="sxs-lookup"><span data-stu-id="1ea2c-129">Click the name of the resource you want to book, and then select **Book**.</span></span>  
  
3.  <span data-ttu-id="1ea2c-130">Na caixa de diálogo **Reserva de recursos (criar)**, escolha o projeto para o qual pretende reservar o recurso, juntamente com o método de reserva e as horas de início e de fim.</span><span class="sxs-lookup"><span data-stu-id="1ea2c-130">On the **Resource booking (create)** dialog box, choose the project that you want to book the resource for along with booking method and start and end times.</span></span>  
  
4.  <span data-ttu-id="1ea2c-131">Quando terminar, selecione **Reservar**.</span><span class="sxs-lookup"><span data-stu-id="1ea2c-131">When you’re done, select **Book**.</span></span>  
  
## <a name="view-to-the-schedule-board"></a><span data-ttu-id="1ea2c-132">Ver o quadro da agenda</span><span class="sxs-lookup"><span data-stu-id="1ea2c-132">View to the schedule board</span></span>
  
1.  <span data-ttu-id="1ea2c-133">Selecione um requisito de reserva com agendamento anulado na lista na parte inferior.</span><span class="sxs-lookup"><span data-stu-id="1ea2c-133">Select an unscheduled booking requirement from the list at the bottom.</span></span>  
  
2.  <span data-ttu-id="1ea2c-134">Arraste o requisito de reserva para um recurso/intervalo de tempo disponível no quadro da agenda.</span><span class="sxs-lookup"><span data-stu-id="1ea2c-134">Drag the booking requirement to an available resource/time slot on the schedule board.</span></span>  
  
3.  <span data-ttu-id="1ea2c-135">Quando terminar, selecione **Reservar**.</span><span class="sxs-lookup"><span data-stu-id="1ea2c-135">When you're done, select **Book**.</span></span>  
  
### <a name="additional-resources"></a><span data-ttu-id="1ea2c-136">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="1ea2c-136">Additional resources</span></span>  
 [<span data-ttu-id="1ea2c-137">Manual do gestor de recursos</span><span class="sxs-lookup"><span data-stu-id="1ea2c-137">Resource manager guide</span></span>](../psa/resource-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]