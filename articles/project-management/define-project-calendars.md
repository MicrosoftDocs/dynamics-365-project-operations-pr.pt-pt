---
title: Definir calendários de projetos
description: Este tópico fornece informações sobre a utilização de um calendário de projeto para monitorizar o cronograma do projeto.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e25b11b6b947627ca2ac88952e74aecccc346c89
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286982"
---
# <a name="define-project-calendars"></a><span data-ttu-id="625f4-103">Definir calendários de projetos</span><span class="sxs-lookup"><span data-stu-id="625f4-103">Define project calendars</span></span>

<span data-ttu-id="625f4-104">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="625f4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="625f4-105">Para criar uma agenda de projeto, cria um modelo de calendário do projeto que define o número de horas de trabalho por dia e todos os encerramentos de companhia.</span><span class="sxs-lookup"><span data-stu-id="625f4-105">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="625f4-106">Para criar um modelo de calendário do projeto, associe um modelo de trabalho ao campo **Modelo de calendário** do projeto.</span><span class="sxs-lookup"><span data-stu-id="625f4-106">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="625f4-107">Siga estes passos para criar um modelo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="625f4-107">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="625f4-108">No painel de navegação esquerdo, selecione **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="625f4-108">In the left navigation pane, select **Resources**.</span></span> 
2. <span data-ttu-id="625f4-109">Na página da lista de **Recursos**, abra o registo de utilizador e selecione **Mostrar Horas de Trabalho**.</span><span class="sxs-lookup"><span data-stu-id="625f4-109">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="625f4-110">Certifique-se de que permite pop-ups na página do browser.</span><span class="sxs-lookup"><span data-stu-id="625f4-110">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="625f4-111">Isto permite-lhe ver as horas de trabalho definidas para o recurso.</span><span class="sxs-lookup"><span data-stu-id="625f4-111">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="625f4-112">No separador **Vista Mensal**, selecione **Configurar**.</span><span class="sxs-lookup"><span data-stu-id="625f4-112">On the **Monthly View** tab, select **Set Up**.</span></span> <span data-ttu-id="625f4-113">É apresentada uma lista de três opções:</span><span class="sxs-lookup"><span data-stu-id="625f4-113">A list of three options appears:</span></span> 

  - <span data-ttu-id="625f4-114">Nova Agenda Semanal</span><span class="sxs-lookup"><span data-stu-id="625f4-114">New Weekly Schedule</span></span>
  - <span data-ttu-id="625f4-115">Agenda de Trabalho Para Um Dia</span><span class="sxs-lookup"><span data-stu-id="625f4-115">Work Schedule for One Day</span></span>
  - <span data-ttu-id="625f4-116">Licença</span><span class="sxs-lookup"><span data-stu-id="625f4-116">Time Off</span></span>

4. <span data-ttu-id="625f4-117">Selecione **Nova Agenda Semanal** e, em seguida, defina as opções para esta agenda de recursos.</span><span class="sxs-lookup"><span data-stu-id="625f4-117">Select **New Weekly Schedule**, and then set the options for this resource schedule.</span></span> <span data-ttu-id="625f4-118">É possível definir uma agenda semanal periódica, os parâmetros de hora diária, os encerramentos de companhia e muito mais.</span><span class="sxs-lookup"><span data-stu-id="625f4-118">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="625f4-119">Defina o intervalo de datas, selecione **Guardar** e selecione **Fechar**.</span><span class="sxs-lookup"><span data-stu-id="625f4-119">Set the date range, select **Save**, and then select **Close**.</span></span> 
6. <span data-ttu-id="625f4-120">Volte à página da lista de **Recursos** e selecione o recurso para o qual define as horas de trabalho.</span><span class="sxs-lookup"><span data-stu-id="625f4-120">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="625f4-121">Selecione **Definir Calendário Como** para definir o modelo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="625f4-121">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="625f4-122">Na caixa de diálogo **Modelo de Trabalho**, introduza um nome para o modelo de trabalho e selecione **Aplicar**.</span><span class="sxs-lookup"><span data-stu-id="625f4-122">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="625f4-123">Agora, pode associar o modelo de trabalho a um modelo de calendário do projeto.</span><span class="sxs-lookup"><span data-stu-id="625f4-123">You can now associate the work template with a project calendar template.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]