---
title: Modelos de competências e proficiência
description: Este tópico fornece informações sobre como utilizar os modelos de competências e proficiência.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/13/2019
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
ms.openlocfilehash: cd243544df062e5801bbfa0a3bd75c4d9a116a6f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082624"
---
# <a name="skills-and-proficiency-models"></a><span data-ttu-id="0ecc4-103">Modelos de competências e proficiência</span><span class="sxs-lookup"><span data-stu-id="0ecc4-103">Skills and proficiency models</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="0ecc4-104">As competências são características do recurso partilhadas entre o Dynamics 365 Project Service Automation e, se existir, o Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="0ecc4-104">Skills are resource characteristics that are shared between Dynamics 365 Project Service Automation and if present, Dynamics 365 Field Service.</span></span> 

<span data-ttu-id="0ecc4-105">Para manter o repositório de competências no Project Service Automation, aceda a **Recursos** \> **Competências do Recurso**.</span><span class="sxs-lookup"><span data-stu-id="0ecc4-105">To maintain the repository of skills in Project Service Automation, go to **Resources** \> **Resource Skills**.</span></span> 

> ![Competências do Recurso](media/Resource-Management-image84.png)

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="0ecc4-107">Utilizar modelos de proficiência para classificar recursos</span><span class="sxs-lookup"><span data-stu-id="0ecc4-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="0ecc4-108">As competências para os recursos são classificadas por modelos de proficiência.</span><span class="sxs-lookup"><span data-stu-id="0ecc4-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="0ecc4-109">As classificações individuais estão num modelo de proficiência.</span><span class="sxs-lookup"><span data-stu-id="0ecc4-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="0ecc4-110">Para criar um modelo de proficiência, aceda a **Recursos** \> **Modelos de Proficiência** e selecione **Novo**.</span><span class="sxs-lookup"><span data-stu-id="0ecc4-110">To create a proficiency model, go to **Resources** \> **Proficiency Models** , and then select **New**.</span></span>
2. <span data-ttu-id="0ecc4-111">No novo modelo de classificação, especifique o valor mínimo de classificação, o valor máximo de classificação e a entidade que está a ser avaliada.</span><span class="sxs-lookup"><span data-stu-id="0ecc4-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="0ecc4-112">Na subgrelha **Valores de Classificação** , é possível definir os diferentes valores de classificação, desde o mínimo até ao máximo.</span><span class="sxs-lookup"><span data-stu-id="0ecc4-112">In the **Rating Values** sub-grid, you can define the different rating values, from the minimum to the maximum.</span></span>

> ![Classificações mínimas e máximas definidas](media/Resource-Management-image85.png)

<span data-ttu-id="0ecc4-114">Estes valores de classificação são apresentados nos filtros **Requisitos de Recursos** , **Quadro da Agenda** e **Assistente da Agenda**.</span><span class="sxs-lookup"><span data-stu-id="0ecc4-114">These rating values are shown on the **Resource Requirements** , **Schedule Board** , and **Schedule Assistant** filters.</span></span>
