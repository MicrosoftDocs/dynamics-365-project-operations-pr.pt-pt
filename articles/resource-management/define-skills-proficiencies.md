---
title: Definir competências e proficiências
description: Este tópico fornece informações sobre como configurar os modelos de proficiência para avaliar os recursos.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
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
ms.openlocfilehash: d1ef50a3aa297ef439b54d37de629414ca66c820
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279692"
---
# <a name="define-skills-and-proficiencies"></a><span data-ttu-id="ee5bf-103">Definir competências e proficiências</span><span class="sxs-lookup"><span data-stu-id="ee5bf-103">Define skills and proficiencies</span></span>

<span data-ttu-id="ee5bf-104">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="ee5bf-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ee5bf-105">As competências são características do recurso partilhadas entre o Dynamics 365 Project Operations e, se existir, o Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="ee5bf-105">Skills are resource characteristics that are shared between Dynamics 365 Project Operations and if present, Dynamics 365 Field Service.</span></span> 

- <span data-ttu-id="ee5bf-106">Para manter o repositório de competências nas operações de Projeto, aceda a **Recursos** \> **Competências do Recurso**.</span><span class="sxs-lookup"><span data-stu-id="ee5bf-106">To maintain the repository of skills in Project Operations, go to **Resources** \> **Resource Skills**.</span></span> 

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="ee5bf-107">Utilizar modelos de proficiência para classificar recursos</span><span class="sxs-lookup"><span data-stu-id="ee5bf-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="ee5bf-108">As competências para os recursos são classificadas por modelos de proficiência.</span><span class="sxs-lookup"><span data-stu-id="ee5bf-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="ee5bf-109">As classificações individuais estão num modelo de proficiência.</span><span class="sxs-lookup"><span data-stu-id="ee5bf-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="ee5bf-110">Para criar um modelo de proficiência, aceda a **Recursos** \> **Modelos de Proficiência** e selecione **Novo**.</span><span class="sxs-lookup"><span data-stu-id="ee5bf-110">To create a proficiency model, go to **Resources** \> **Proficiency Models**, and then select **New**.</span></span>
2. <span data-ttu-id="ee5bf-111">No novo modelo de classificação, especifique o valor mínimo de classificação, o valor máximo de classificação e a entidade que está a ser avaliada.</span><span class="sxs-lookup"><span data-stu-id="ee5bf-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="ee5bf-112">Na subgrelha **Valores de Classificação**, é possível definir os diferentes valores de classificação, desde o mínimo até ao máximo.</span><span class="sxs-lookup"><span data-stu-id="ee5bf-112">In the **Rating Values** subgrid, you can define the different rating values, from the minimum to the maximum.</span></span>


<span data-ttu-id="ee5bf-113">Estes valores de classificação são apresentados nos filtros **Requisitos de Recursos**, **Quadro da Agenda** e **Assistente da Agenda**.</span><span class="sxs-lookup"><span data-stu-id="ee5bf-113">These rating values are shown on the **Resource Requirements**, **Schedule Board**, and **Schedule Assistant** filters.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]