---
title: Definir competências e proficiências
description: Este tópico fornece informações sobre como configurar os modelos de proficiência para avaliar os recursos.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 9376e0b268a3ab682716da604ceecfa1e878da68
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897645"
---
# <a name="define-skills-and-proficiencies"></a><span data-ttu-id="4ca2c-103">Definir competências e proficiências</span><span class="sxs-lookup"><span data-stu-id="4ca2c-103">Define skills and proficiencies</span></span>

<span data-ttu-id="4ca2c-104">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="4ca2c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4ca2c-105">As competências são características do recurso partilhadas entre o Dynamics 365 Project Operations e, se existir, o Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="4ca2c-105">Skills are resource characteristics that are shared between Dynamics 365 Project Operations and if present, Dynamics 365 Field Service.</span></span> 

- <span data-ttu-id="4ca2c-106">Para manter o repositório de competências nas operações de Projeto, aceda a **Recursos** \> **Competências do Recurso**.</span><span class="sxs-lookup"><span data-stu-id="4ca2c-106">To maintain the repository of skills in Project Operations, go to **Resources** \> **Resource Skills**.</span></span> 

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="4ca2c-107">Utilizar modelos de proficiência para classificar recursos</span><span class="sxs-lookup"><span data-stu-id="4ca2c-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="4ca2c-108">As competências para os recursos são classificadas por modelos de proficiência.</span><span class="sxs-lookup"><span data-stu-id="4ca2c-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="4ca2c-109">As classificações individuais estão num modelo de proficiência.</span><span class="sxs-lookup"><span data-stu-id="4ca2c-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="4ca2c-110">Para criar um modelo de proficiência, aceda a **Recursos** \> **Modelos de Proficiência** e selecione **Novo**.</span><span class="sxs-lookup"><span data-stu-id="4ca2c-110">To create a proficiency model, go to **Resources** \> **Proficiency Models**, and then select **New**.</span></span>
2. <span data-ttu-id="4ca2c-111">No novo modelo de classificação, especifique o valor mínimo de classificação, o valor máximo de classificação e a entidade que está a ser avaliada.</span><span class="sxs-lookup"><span data-stu-id="4ca2c-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="4ca2c-112">Na subgrelha **Valores de Classificação**, é possível definir os diferentes valores de classificação, desde o mínimo até ao máximo.</span><span class="sxs-lookup"><span data-stu-id="4ca2c-112">In the **Rating Values** sub-grid, you can define the different rating values, from the minimum to the maximum.</span></span>


<span data-ttu-id="4ca2c-113">Estes valores de classificação são apresentados nos filtros **Requisitos de Recursos**, **Quadro da Agenda** e **Assistente da Agenda**.</span><span class="sxs-lookup"><span data-stu-id="4ca2c-113">These rating values are shown on the **Resource Requirements**, **Schedule Board**, and **Schedule Assistant** filters.</span></span>
