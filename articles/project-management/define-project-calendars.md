---
title: Definir calendários de projetos
description: Esta tópico fornece informações sobre como aplicar um modelo de calendário a um projeto para acompanhar o calendário do projeto.
author: ruhercul
manager: AnnBe
ms.date: 02/05/2021
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
ms.openlocfilehash: 1d5642d7a2246dc878b2bc4f504f138b71d29a69
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981314"
---
# <a name="define-project-calendars"></a><span data-ttu-id="06f93-103">Definir calendários de projetos</span><span class="sxs-lookup"><span data-stu-id="06f93-103">Define project calendars</span></span>

<span data-ttu-id="06f93-104">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="06f93-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="06f93-105">Para criar e gerir um projeto, deve aplicar um modelo de calendário ao projeto.</span><span class="sxs-lookup"><span data-stu-id="06f93-105">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="06f93-106">O modelo de calendário define os seguintes atributos do projeto:</span><span class="sxs-lookup"><span data-stu-id="06f93-106">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="06f93-107">Horário de trabalho, incluindo início e fim</span><span class="sxs-lookup"><span data-stu-id="06f93-107">Working hours, including start and end time</span></span>
- <span data-ttu-id="06f93-108">Dias de trabalho</span><span class="sxs-lookup"><span data-stu-id="06f93-108">Working days</span></span>
- <span data-ttu-id="06f93-109">Exceções do calendário, tais como dias não laborais</span><span class="sxs-lookup"><span data-stu-id="06f93-109">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="06f93-110">O modelo de calendário que é aplicado a um projeto é uma cópia do modelo de calendário definido nas definições da sua organização.</span><span class="sxs-lookup"><span data-stu-id="06f93-110">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="06f93-111">Se alterar o modelo de calendário, essas alterações não se propagam ao horário de trabalho do projeto.</span><span class="sxs-lookup"><span data-stu-id="06f93-111">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="06f93-112">Para alterar o horário de trabalho do projeto, deve ser aplicado um novo modelo.</span><span class="sxs-lookup"><span data-stu-id="06f93-112">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="06f93-113">Para criar um modelo de calendário para a sua organização, existem dois requisitos-chave:</span><span class="sxs-lookup"><span data-stu-id="06f93-113">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="06f93-114">Defina as horas de trabalho desejadas do modelo utilizando um recurso de reserva novo ou existente.</span><span class="sxs-lookup"><span data-stu-id="06f93-114">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="06f93-115">Crie um novo modelo de calendário e associe o modelo ao recurso de reserva.</span><span class="sxs-lookup"><span data-stu-id="06f93-115">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="06f93-116">**Defina as horas de trabalho do modelo**</span><span class="sxs-lookup"><span data-stu-id="06f93-116">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="06f93-117">Aceda a **Recursos** \> **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="06f93-117">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="06f93-118">Crie um novo recurso para fazer referência no modelo de calendário ou selecione um recurso existente.</span><span class="sxs-lookup"><span data-stu-id="06f93-118">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="06f93-119">Selecione o separador **Horas de Trabalho** do recurso e preencha as instruções em [Definir horário de trabalho para um recurso](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) para configurar as regras do calendário.</span><span class="sxs-lookup"><span data-stu-id="06f93-119">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) to configure the calendar rules.</span></span>

<span data-ttu-id="06f93-120">**Criar um novo modelo de calendário**</span><span class="sxs-lookup"><span data-stu-id="06f93-120">**Create a new calendar template**</span></span>

1. <span data-ttu-id="06f93-121">Ir a **Definições** \> **Modelo de calendário**.</span><span class="sxs-lookup"><span data-stu-id="06f93-121">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="06f93-122">Selecione **Novo** e introduza um nome, descrição e recurso de modelo.</span><span class="sxs-lookup"><span data-stu-id="06f93-122">Select **New**, and enter a name, description, and template resource.</span></span>

> [!NOTE]
> <span data-ttu-id="06f93-123">Quando um recurso é referenciado num modelo de calendário, uma cópia do calendário do recurso está associada ao modelo do calendário.</span><span class="sxs-lookup"><span data-stu-id="06f93-123">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="06f93-124">Se alterar o modelo copiado das horas de trabalho, essas alterações não se propagam ao modelo de calendário.</span><span class="sxs-lookup"><span data-stu-id="06f93-124">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>

<span data-ttu-id="06f93-125">Agora, pode associar o modelo de trabalho a um modelo de calendário do projeto.</span><span class="sxs-lookup"><span data-stu-id="06f93-125">You can now associate the work template with a project calendar template.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]

