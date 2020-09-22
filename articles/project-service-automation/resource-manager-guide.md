---
title: Manual do gestor de recursos
description: Um manual para a gestão de recursos no Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 4a3f3fa7-ae1a-4139-974b-f61cc8a8bda7
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 67b400fe3e6bb60775ee144c1d3720a311204d7d
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754611"
---
# <a name="resource-manager-guide-project-service"></a><span data-ttu-id="12b21-103">Manual do gestor de recursos (Project Service)</span><span class="sxs-lookup"><span data-stu-id="12b21-103">Resource manager guide (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="12b21-104">As capacidades do [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] no [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] ajudam a localizar os recursos certos no momento certo para o projeto certo e assegurar que todos os recursos são utilizados de forma eficiente.</span><span class="sxs-lookup"><span data-stu-id="12b21-104">The [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] help you find the right resources at the right time for the right project and make sure all resources are utilized efficiently.</span></span>  
  
 <span data-ttu-id="12b21-105">Implemente os consultores da sua empresa de forma eficaz e eficiente com o [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="12b21-105">Deploy your company’s consultants efficiently and effectively with the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> <span data-ttu-id="12b21-106">Estes capacidades fornecem as ferramentas necessárias para agendar os recursos com base nos requisitos e nas agendas dos projetos de consultoria e nas competências e na disponibilidade dos seus consultores.</span><span class="sxs-lookup"><span data-stu-id="12b21-106">These provide you with the tools you need to schedule resources based on the requirements and schedules of consulting projects and on the skills and availability of your consultants.</span></span> <span data-ttu-id="12b21-107">Poderá localizar rapidamente os consultores mais qualificados disponíveis para trabalhar nos projetos e poderá ver facilmente como melhor agendá-los no decurso de cada projeto.</span><span class="sxs-lookup"><span data-stu-id="12b21-107">You can quickly find the most qualified consultants who are available to work on projects, and you can easily see how to better schedule them during the course of each project.</span></span>  
  
 <span data-ttu-id="12b21-108">O agendamento de recursos ajuda a fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="12b21-108">Resource scheduling helps you do the following:</span></span>  
  
- <span data-ttu-id="12b21-109">Faze corresponder os recursos aos projetos, com base na forma como as competências e os níveis de proficiência correspondem aos requisitos de recursos do projeto.</span><span class="sxs-lookup"><span data-stu-id="12b21-109">Match resources to projects, based on how well their skills and proficiency levels match the project resource requirements.</span></span>  
  
- <span data-ttu-id="12b21-110">Fazer corresponder a agenda de um recurso a um calendário de projeto, com base na sua disponibilidade e licenças agendadas.</span><span class="sxs-lookup"><span data-stu-id="12b21-110">Match a resource’s schedule to a project calendar, based on their availability and scheduled time off.</span></span> <span data-ttu-id="12b21-111">O calendário codificado por cores oferece pistas visuais sobre a disponibilidade dos recursos.</span><span class="sxs-lookup"><span data-stu-id="12b21-111">The color-coded calendar gives you visual cues about resource availability.</span></span>  
  
- <span data-ttu-id="12b21-112">Rever a capacidade de cada consultor e determinar como essa capacidade está a ser utilizada atualmente.</span><span class="sxs-lookup"><span data-stu-id="12b21-112">Review the capacity of each consultant and determine how that capacity is currently used.</span></span> <span data-ttu-id="12b21-113">Isto pode ajudar a determinar onde um consultor poderá estar a ser sub ou sobreutilizado, ou se está à sua plena capacidade.</span><span class="sxs-lookup"><span data-stu-id="12b21-113">This can help you find where a consultant might be under- or over-utilized, or if they’re working at capacity.</span></span>  
  
- <span data-ttu-id="12b21-114">Atribuir uma percentagem ou um número específico de horas da capacidade de um trabalhador a um projeto.</span><span class="sxs-lookup"><span data-stu-id="12b21-114">Assign a percentage or a specific number of hours for a worker’s capacity to a project.</span></span>  
  
- <span data-ttu-id="12b21-115">Fazer reservas de recursos de grupo.</span><span class="sxs-lookup"><span data-stu-id="12b21-115">Make group resource bookings.</span></span>  
  
- <span data-ttu-id="12b21-116">Fazer reservas flexíveis ou fixas de recursos e converter as horas com reservas flexíveis em horas com reservas fixas num só passo.</span><span class="sxs-lookup"><span data-stu-id="12b21-116">Soft book or hard book resources, and convert soft-booked hours into hard-booked hours in one step.</span></span>  
  
- <span data-ttu-id="12b21-117">Formar automaticamente uma equipa de projeto com base nos recursos definidos na estrutura hierárquica do trabalho de um projeto.</span><span class="sxs-lookup"><span data-stu-id="12b21-117">Automatically form a project team based on resources defined in a work breakdown structure for a project.</span></span>  
  
- <span data-ttu-id="12b21-118">Satisfazer os pedidos dos recursos (reservar, propor, localizar recursos de substituição).</span><span class="sxs-lookup"><span data-stu-id="12b21-118">Fulfill resource requests (book, propose, find substitute resources).</span></span>  
  
- <span data-ttu-id="12b21-119">Atribuir recursos de acordo com um modelo central (o gestor de recursos atribui) ou híbrido (o gestor de recursos e outros gestores podem atribuir).</span><span class="sxs-lookup"><span data-stu-id="12b21-119">Assign resources according to a central (resource manager assigns) or hybrid model (resource manager and other managers can assign).</span></span> <span data-ttu-id="12b21-120">Para mais informações sobre como definir um modelo de gestão de recursos central versus híbrido, consulte [Configurar definições adicionais dos parâmetros (Project Service)](../project-service/configure-additional-parameters-settings.md).</span><span class="sxs-lookup"><span data-stu-id="12b21-120">For more information about setting a central versus hybrid resource management model, see [Configure additional parameters settings (Project Service)](../project-service/configure-additional-parameters-settings.md).</span></span>  
  
  <span data-ttu-id="12b21-121">Poderá gerir os recursos de forma eficiente em vários projetos e assegurar que os projetos têm os recursos adequados.</span><span class="sxs-lookup"><span data-stu-id="12b21-121">You can manage resources efficiently across projects and ensure that projects are staffed appropriately.</span></span> <span data-ttu-id="12b21-122">Terá de efetuar as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="12b21-122">You’ll need to perform the following tasks:</span></span>  
  
- <span data-ttu-id="12b21-123">[Gerir pedidos de recursos](../project-service/manage-resource-requests.md).</span><span class="sxs-lookup"><span data-stu-id="12b21-123">[Manage resource requests](../project-service/manage-resource-requests.md).</span></span> <span data-ttu-id="12b21-124">Fazer corresponder as competências e as proficiências dos seus consultores aos projetos certos.</span><span class="sxs-lookup"><span data-stu-id="12b21-124">Match the skills and proficiencies of your consultants to the right projects.</span></span>  
  
- <span data-ttu-id="12b21-125">[Ver disponibilidade de recursos](../project-service/view-resource-availability.md).</span><span class="sxs-lookup"><span data-stu-id="12b21-125">[View resource availability](../project-service/view-resource-availability.md).</span></span> <span data-ttu-id="12b21-126">Verificar a disponibilidade dos consultores numa vista de calendário.</span><span class="sxs-lookup"><span data-stu-id="12b21-126">Check consultants’ availability in a calendar view.</span></span>  
  
- <span data-ttu-id="12b21-127">[Ver utilização dos recursos](../project-service/view-resource-utilization.md).</span><span class="sxs-lookup"><span data-stu-id="12b21-127">[View resource utilization](../project-service/view-resource-utilization.md).</span></span> <span data-ttu-id="12b21-128">Ver a percentagem de tempo que os seus consultores estão atualmente reservados.</span><span class="sxs-lookup"><span data-stu-id="12b21-128">See the percentage of time that your consultants are currently booked.</span></span>  
  
- <span data-ttu-id="12b21-129">[Agendar recursos para um projeto](../project-service/schedule-resources-project.md).</span><span class="sxs-lookup"><span data-stu-id="12b21-129">[Schedule resources for a project](../project-service/schedule-resources-project.md).</span></span> <span data-ttu-id="12b21-130">Agendar consultores para um projeto.</span><span class="sxs-lookup"><span data-stu-id="12b21-130">Schedule consultants for a project.</span></span>  
  
  <span data-ttu-id="12b21-131">Para mais informações sobre como enviar pedidos de recursos para projetos individuais, consulte [Submeter pedidos de recursos](../project-service/submit-resource-requests.md).</span><span class="sxs-lookup"><span data-stu-id="12b21-131">For more information about submitting resource requests for individual projects, see [Submit resource requests](../project-service/submit-resource-requests.md).</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="12b21-132">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="12b21-132">See Also</span></span>  
 <span data-ttu-id="12b21-133">[Descrição Geral do Project Service](../project-service/overview.md) </span><span class="sxs-lookup"><span data-stu-id="12b21-133">[Overview of Project Service](../project-service/overview.md) </span></span>  
 <span data-ttu-id="12b21-134">[Guia do Administrador](../project-service/admin-guide.md) </span><span class="sxs-lookup"><span data-stu-id="12b21-134">[Administrator Guide](../project-service/admin-guide.md) </span></span>  
 <span data-ttu-id="12b21-135">[Guia do Gestor de Contas](../project-service/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="12b21-135">[Account Manager Guiden](../project-service/account-manager-guide.md) </span></span>  
 <span data-ttu-id="12b21-136">[Guia do Gestor de Projeto](../project-service/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="12b21-136">[Project Manager Guide](../project-service/project-manager-guide.md) </span></span>  
 [<span data-ttu-id="12b21-137">Guia de Tempo, Despesa e Colaboração</span><span class="sxs-lookup"><span data-stu-id="12b21-137">Time, Expense, and Collaboration Guide</span></span>](../project-service/time-expense-collaboration-guide.md)
