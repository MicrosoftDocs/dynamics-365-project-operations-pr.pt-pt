---
title: Descrição geral do assistente da agenda
description: Este tópico fornece informações sobre como trabalhar com o Assistente da agenda para reservar recursos.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.custom: intro-internal
ms.openlocfilehash: 83583c97e4ecb5f1fdc0d8d98098afe8e12d27e4
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368130"
---
# <a name="schedule-assistant-overview"></a><span data-ttu-id="bcab4-103">Descrição geral do assistente da agenda</span><span class="sxs-lookup"><span data-stu-id="bcab4-103">Schedule assistant overview</span></span>

<span data-ttu-id="bcab4-104">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="bcab4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="bcab4-105">O Assistente da agenda é utilizado para reservar recursos baseado nos requisitos definidos pelo Gestor de projeto.</span><span class="sxs-lookup"><span data-stu-id="bcab4-105">The Schedule assistant is used to book resources based on requirements defined by the Project manager.</span></span> <span data-ttu-id="bcab4-106">O assistente da agenda baseia-se nos parâmetros fornecidos no requisito do recurso para localizar o recurso.</span><span class="sxs-lookup"><span data-stu-id="bcab4-106">The schedule assistant relies on the parameters provided in the resource requirement to find the resource.</span></span> <span data-ttu-id="bcab4-107">O Assistente da agenda recomenda recursos que correspondam aos requisitos relevantes, tais como janelas de tempo ou competências necessárias.</span><span class="sxs-lookup"><span data-stu-id="bcab4-107">The Schedule assistant recommends resources that match relevant requirements, like time windows or skills needed.</span></span>

<span data-ttu-id="bcab4-108">Após a identificação dos recursos adequados, o Gestor de recursos ou o Gestor de projeto pode reservar o recurso para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="bcab4-108">After suitable resources are identified, the Resource or Project manager can book the resource to the work.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="bcab4-109">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="bcab4-109">Prerequisites</span></span>

<span data-ttu-id="bcab4-110">O Assistente da agenda faz parte da solução do Universal Resource Scheduling.</span><span class="sxs-lookup"><span data-stu-id="bcab4-110">The Schedule assistant is a part of the Universal Resource Scheduling solution.</span></span> <span data-ttu-id="bcab4-111">Esta solução está incluída e instalada com o Dynamics 365 Project Operations, Dynamics 365 Field Service e Dynamics 365 Customer Service.</span><span class="sxs-lookup"><span data-stu-id="bcab4-111">This solution is included and installed with Dynamics 365 Project Operations, Dynamics 365 Field Service, and Dynamics 365 Customer Service.</span></span>

## <a name="matching-requirements-and-resources"></a><span data-ttu-id="bcab4-112">Requisitos e recursos correspondentes</span><span class="sxs-lookup"><span data-stu-id="bcab4-112">Matching requirements and resources</span></span>

<span data-ttu-id="bcab4-113">Um requisito de recursos gerados baseia-se em detalhes como:</span><span class="sxs-lookup"><span data-stu-id="bcab4-113">A generated resource requirement is based on details such as:</span></span>

-   <span data-ttu-id="bcab4-114">Características</span><span class="sxs-lookup"><span data-stu-id="bcab4-114">Characteristics</span></span>
-   <span data-ttu-id="bcab4-115">Funções</span><span class="sxs-lookup"><span data-stu-id="bcab4-115">Roles</span></span>
-   <span data-ttu-id="bcab4-116">Unidades de negócio</span><span class="sxs-lookup"><span data-stu-id="bcab4-116">Business units</span></span>
-   <span data-ttu-id="bcab4-117">Preferências de recurso</span><span class="sxs-lookup"><span data-stu-id="bcab4-117">Resource preferences</span></span>
-   <span data-ttu-id="bcab4-118">Perfis de esforço</span><span class="sxs-lookup"><span data-stu-id="bcab4-118">Effort contours</span></span>
-   <span data-ttu-id="bcab4-119">Fuso horário</span><span class="sxs-lookup"><span data-stu-id="bcab4-119">Time zone</span></span>

<span data-ttu-id="bcab4-120">O Assistente da agenda utiliza estes detalhes para filtrar recursos.</span><span class="sxs-lookup"><span data-stu-id="bcab4-120">The Schedule assistant uses these details to filter resources.</span></span>

## <a name="launch-the-schedule-assistant"></a><span data-ttu-id="bcab4-121">Iniciar o Assistente da agenda</span><span class="sxs-lookup"><span data-stu-id="bcab4-121">Launch the Schedule assistant</span></span>

<span data-ttu-id="bcab4-122">O assistente da agenda pode ser iniciado de duas formas.</span><span class="sxs-lookup"><span data-stu-id="bcab4-122">There are two ways in which the schedule assistant is launched.</span></span> <span data-ttu-id="bcab4-123">Se estiver a utilizar o modo híbrido, na grelha de membro de equipa pode selecionar qualquer membro da equipa com um requisito de recurso não concluído e, em seguida, selecione **Reservar**.</span><span class="sxs-lookup"><span data-stu-id="bcab4-123">If you're using the hybrid mode, in the team member grid you can select any team member with an unfulfilled resource requirement, and then select **Book**.</span></span> <span data-ttu-id="bcab4-124">Se estiver a utilizar o modo central, o Gestor de recursos localiza e seleciona o recurso.</span><span class="sxs-lookup"><span data-stu-id="bcab4-124">If you're using the central mode, the Resource manager finds and selects the resource.</span></span>

## <a name="schedule-assistant-filters"></a><span data-ttu-id="bcab4-125">Filtro do assistente da agenda</span><span class="sxs-lookup"><span data-stu-id="bcab4-125">Schedule assistant filters</span></span>

<span data-ttu-id="bcab4-126">Após a execução do Assistente da agenda, os detalhes do requisito do recurso são apresentados como valores filtrados no painel esquerdo.</span><span class="sxs-lookup"><span data-stu-id="bcab4-126">After the Schedule assistant runs, the details from the resource requirement are displayed as filtered values in the left pane.</span></span> <span data-ttu-id="bcab4-127">O Gestor de recursos ou o Gestor de projeto pode otimizar os resultados ao ajustar os filtros para satisfazer as necessidades de agendamento.</span><span class="sxs-lookup"><span data-stu-id="bcab4-127">The Resource manager or the Project manager can fine-tune results by adjusting filters to meet the scheduling needs.</span></span>

<span data-ttu-id="bcab4-128">O painel de filtro mostra opções relacionadas com o trabalho, incluindo:</span><span class="sxs-lookup"><span data-stu-id="bcab4-128">The filter pane shows work-related options, including:</span></span>

-   <span data-ttu-id="bcab4-129">Início e fim do trabalho</span><span class="sxs-lookup"><span data-stu-id="bcab4-129">Work start and end</span></span>
-   <span data-ttu-id="bcab4-130">Características</span><span class="sxs-lookup"><span data-stu-id="bcab4-130">Characteristics</span></span>
-   <span data-ttu-id="bcab4-131">Funções</span><span class="sxs-lookup"><span data-stu-id="bcab4-131">Roles</span></span>
-   <span data-ttu-id="bcab4-132">Unidades organizacionais</span><span class="sxs-lookup"><span data-stu-id="bcab4-132">Organizational units</span></span>
-   <span data-ttu-id="bcab4-133">Empresa de recursos</span><span class="sxs-lookup"><span data-stu-id="bcab4-133">Resourcing company</span></span>
-   <span data-ttu-id="bcab4-134">Tipos de recursos</span><span class="sxs-lookup"><span data-stu-id="bcab4-134">Resource types</span></span>
-   <span data-ttu-id="bcab4-135">Recursos preferenciais</span><span class="sxs-lookup"><span data-stu-id="bcab4-135">Preferred resources</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]