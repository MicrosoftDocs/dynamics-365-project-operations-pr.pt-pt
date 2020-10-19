---
title: Descrição geral do assistente da agenda
description: Este tópico fornece informações sobre como trabalhar com o Assistente da agenda para reservar recursos.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: da551e805f395e466952df1dbb7d193bdddba358
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908464"
---
# <a name="schedule-assistant-overview"></a><span data-ttu-id="3a15d-103">Descrição geral do assistente da agenda</span><span class="sxs-lookup"><span data-stu-id="3a15d-103">Schedule assistant overview</span></span>

<span data-ttu-id="3a15d-104">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="3a15d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3a15d-105">O Assistente da agenda é utilizado para reservar recursos baseado nos requisitos definidos pelo Gestor de projeto.</span><span class="sxs-lookup"><span data-stu-id="3a15d-105">The Schedule assistant is used to book resources based on requirements defined by the Project manager.</span></span> <span data-ttu-id="3a15d-106">O assistente da agenda baseia-se nos parâmetros fornecidos no requisito do recurso para localizar o recurso.</span><span class="sxs-lookup"><span data-stu-id="3a15d-106">The schedule assistant relies on the parameters provided in the resource requirement to find the resource.</span></span> <span data-ttu-id="3a15d-107">O Assistente da agenda recomenda recursos que correspondam aos requisitos relevantes, tais como janelas de tempo ou competências necessárias.</span><span class="sxs-lookup"><span data-stu-id="3a15d-107">The Schedule assistant recommends resources that match relevant requirements, like time windows or skills needed.</span></span>

<span data-ttu-id="3a15d-108">Após a identificação dos recursos adequados, o Gestor de recursos ou o Gestor de projeto pode reservar o recurso para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="3a15d-108">After suitable resources are identified, the Resource or Project manager can book the resource to the work.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3a15d-109">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="3a15d-109">Prerequisites</span></span>

<span data-ttu-id="3a15d-110">O Assistente da agenda faz parte da solução do Universal Resource Scheduling.</span><span class="sxs-lookup"><span data-stu-id="3a15d-110">The Schedule assistant is a part of the Universal Resource Scheduling solution.</span></span> <span data-ttu-id="3a15d-111">Esta solução é incluída e instalada com o Dynamics 365 Project Operations, Dynamics 365 Field Service e Dynamics 365 Customer Service.</span><span class="sxs-lookup"><span data-stu-id="3a15d-111">This solution is included and installed with Dynamics 365 Project Operations, Dynamics 365 Field Service, and Dynamics 365 Customer Service.</span></span>

## <a name="matching-requirements-and-resources"></a><span data-ttu-id="3a15d-112">Requisitos e recursos correspondentes</span><span class="sxs-lookup"><span data-stu-id="3a15d-112">Matching requirements and resources</span></span>

<span data-ttu-id="3a15d-113">Um requisito de recursos gerados baseia-se em detalhes como:</span><span class="sxs-lookup"><span data-stu-id="3a15d-113">A generated resource requirement is based on details such as:</span></span>

-   <span data-ttu-id="3a15d-114">Características</span><span class="sxs-lookup"><span data-stu-id="3a15d-114">Characteristics</span></span>
-   <span data-ttu-id="3a15d-115">Funções</span><span class="sxs-lookup"><span data-stu-id="3a15d-115">Roles</span></span>
-   <span data-ttu-id="3a15d-116">Unidades de negócio</span><span class="sxs-lookup"><span data-stu-id="3a15d-116">Business units</span></span>
-   <span data-ttu-id="3a15d-117">Preferências de recurso</span><span class="sxs-lookup"><span data-stu-id="3a15d-117">Resource preferences</span></span>
-   <span data-ttu-id="3a15d-118">Perfis de esforço</span><span class="sxs-lookup"><span data-stu-id="3a15d-118">Effort contours</span></span>
-   <span data-ttu-id="3a15d-119">Fuso horário</span><span class="sxs-lookup"><span data-stu-id="3a15d-119">Time zone</span></span>

<span data-ttu-id="3a15d-120">O Assistente da agenda utiliza estes detalhes para filtrar recursos.</span><span class="sxs-lookup"><span data-stu-id="3a15d-120">The Schedule assistant uses these details to filter resources.</span></span>

## <a name="launch-the-schedule-assistant"></a><span data-ttu-id="3a15d-121">Iniciar o Assistente da agenda</span><span class="sxs-lookup"><span data-stu-id="3a15d-121">Launch the Schedule assistant</span></span>

<span data-ttu-id="3a15d-122">O assistente da agenda pode ser iniciado de duas formas.</span><span class="sxs-lookup"><span data-stu-id="3a15d-122">There are two ways in which the schedule assistant is launched.</span></span> <span data-ttu-id="3a15d-123">Se estiver a utilizar o modo híbrido, na grelha de membro de equipa pode selecionar qualquer membro da equipa com um requisito de recurso não concluído e, em seguida, selecione **Reservar**.</span><span class="sxs-lookup"><span data-stu-id="3a15d-123">If you're using the hybrid mode, in the team member grid you can select any team member with an unfulfilled resource requirement, and then select **Book**.</span></span> <span data-ttu-id="3a15d-124">Se estiver a utilizar o modo central, o Gestor de recursos localiza e seleciona o recurso.</span><span class="sxs-lookup"><span data-stu-id="3a15d-124">If you're using the central mode, the Resource manager finds and selects the resource.</span></span>

## <a name="schedule-assistant-filters"></a><span data-ttu-id="3a15d-125">Filtro do assistente da agenda</span><span class="sxs-lookup"><span data-stu-id="3a15d-125">Schedule assistant filters</span></span>

<span data-ttu-id="3a15d-126">Após a execução do Assistente da agenda, os detalhes do requisito do recurso são apresentados como valores filtrados no painel esquerdo.</span><span class="sxs-lookup"><span data-stu-id="3a15d-126">After the Schedule assistant runs, the details from the resource requirement are displayed as filtered values in the left pane.</span></span> <span data-ttu-id="3a15d-127">O Gestor de recursos ou o Gestor de projeto pode otimizar os resultados ao ajustar os filtros para satisfazer as necessidades de agendamento.</span><span class="sxs-lookup"><span data-stu-id="3a15d-127">The Resource manager or the Project manager can fine-tune results by adjusting filters to meet the scheduling needs.</span></span>

<span data-ttu-id="3a15d-128">O painel de filtro mostra opções relacionadas com o trabalho, incluindo:</span><span class="sxs-lookup"><span data-stu-id="3a15d-128">The filter pane shows work-related options, including:</span></span>

-   <span data-ttu-id="3a15d-129">Início e fim do trabalho</span><span class="sxs-lookup"><span data-stu-id="3a15d-129">Work start and end</span></span>
-   <span data-ttu-id="3a15d-130">Características</span><span class="sxs-lookup"><span data-stu-id="3a15d-130">Characteristics</span></span>
-   <span data-ttu-id="3a15d-131">Funções</span><span class="sxs-lookup"><span data-stu-id="3a15d-131">Roles</span></span>
-   <span data-ttu-id="3a15d-132">Unidades organizacionais</span><span class="sxs-lookup"><span data-stu-id="3a15d-132">Organizational units</span></span>
-   <span data-ttu-id="3a15d-133">Empresa de recursos</span><span class="sxs-lookup"><span data-stu-id="3a15d-133">Resourcing company</span></span>
-   <span data-ttu-id="3a15d-134">Tipos de recursos</span><span class="sxs-lookup"><span data-stu-id="3a15d-134">Resource types</span></span>
-   <span data-ttu-id="3a15d-135">Recursos preferenciais</span><span class="sxs-lookup"><span data-stu-id="3a15d-135">Preferred resources</span></span>
