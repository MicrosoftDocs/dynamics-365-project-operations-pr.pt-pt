---
title: Criar um modelo de horas de trabalho
description: Este tópico descreve como criar um modelo de horas de trabalho no Project Service.
author: ruhercul
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
ms.openlocfilehash: 105e3cb2ef7b904e96dc21013906e0b7444e3b88
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997210"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="c1980-103">Criar um modelo de horas de trabalho (Project Service)</span><span class="sxs-lookup"><span data-stu-id="c1980-103">Create a work hours template (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="c1980-104">Para criar e gerir um projeto, deve aplicar um modelo de calendário ao projeto.</span><span class="sxs-lookup"><span data-stu-id="c1980-104">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="c1980-105">O modelo de calendário define os seguintes atributos do projeto:</span><span class="sxs-lookup"><span data-stu-id="c1980-105">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="c1980-106">Horário de trabalho, incluindo início e fim</span><span class="sxs-lookup"><span data-stu-id="c1980-106">Working hours, including start and end time</span></span>
- <span data-ttu-id="c1980-107">Dias de trabalho</span><span class="sxs-lookup"><span data-stu-id="c1980-107">Working days</span></span>
- <span data-ttu-id="c1980-108">Exceções do calendário, tais como dias não laborais</span><span class="sxs-lookup"><span data-stu-id="c1980-108">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="c1980-109">O modelo de calendário que é aplicado a um projeto é uma cópia do modelo de calendário definido nas definições da sua organização.</span><span class="sxs-lookup"><span data-stu-id="c1980-109">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="c1980-110">Se alterar o modelo de calendário, essas alterações não se propagam ao horário de trabalho do projeto.</span><span class="sxs-lookup"><span data-stu-id="c1980-110">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="c1980-111">Para alterar o horário de trabalho do projeto, deve ser aplicado um novo modelo.</span><span class="sxs-lookup"><span data-stu-id="c1980-111">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="c1980-112">Para criar um modelo de calendário para a sua organização, existem dois requisitos-chave:</span><span class="sxs-lookup"><span data-stu-id="c1980-112">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="c1980-113">Defina as horas de trabalho desejadas do modelo utilizando um recurso de reserva novo ou existente.</span><span class="sxs-lookup"><span data-stu-id="c1980-113">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="c1980-114">Crie um novo modelo de calendário e associe o modelo ao recurso de reserva.</span><span class="sxs-lookup"><span data-stu-id="c1980-114">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="c1980-115">**Defina as horas de trabalho do modelo**</span><span class="sxs-lookup"><span data-stu-id="c1980-115">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="c1980-116">Aceda a **Recursos** \> **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="c1980-116">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="c1980-117">Crie um novo recurso para fazer referência no modelo de calendário ou selecione um recurso existente.</span><span class="sxs-lookup"><span data-stu-id="c1980-117">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="c1980-118">Selecione o separador **Horas de Trabalho** do recurso e preencha as instruções em [Definir horário de trabalho para um recurso](/dynamics365/field-service/set-work-hours-resource.md) para configurar as regras do calendário.</span><span class="sxs-lookup"><span data-stu-id="c1980-118">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](/dynamics365/field-service/set-work-hours-resource.md) to configure the calendar rules.</span></span>

<span data-ttu-id="c1980-119">**Criar um novo modelo de calendário**</span><span class="sxs-lookup"><span data-stu-id="c1980-119">**Create a new calendar template**</span></span>

1. <span data-ttu-id="c1980-120">Ir a **Definições** \> **Modelo de calendário**.</span><span class="sxs-lookup"><span data-stu-id="c1980-120">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="c1980-121">Selecione **Novo** e introduza um nome, descrição e recurso de modelo.</span><span class="sxs-lookup"><span data-stu-id="c1980-121">Select **New**, and enter a name, description, and template resource.</span></span>


> [!NOTE]
> <span data-ttu-id="c1980-122">Quando um recurso é referenciado num modelo de calendário, uma cópia do calendário do recurso está associada ao modelo do calendário.</span><span class="sxs-lookup"><span data-stu-id="c1980-122">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="c1980-123">Se alterar o modelo copiado das horas de trabalho, essas alterações não se propagam ao modelo de calendário.</span><span class="sxs-lookup"><span data-stu-id="c1980-123">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>


### <a name="see-also"></a><span data-ttu-id="c1980-124">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="c1980-124">See Also</span></span>  
 [<span data-ttu-id="c1980-125">Configurar recursos</span><span class="sxs-lookup"><span data-stu-id="c1980-125">Set up resources</span></span>](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
