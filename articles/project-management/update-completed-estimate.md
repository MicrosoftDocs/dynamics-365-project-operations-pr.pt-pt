---
title: Atualizar estimativa na conclusão
description: Este tópico fornece informações sobre a atualização da projeção do esforço num projeto.
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
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
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 42824cc4cfc2b934f69d319944fe7ee43183955c
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897780"
---
# <a name="update-estimate-at-completion"></a><span data-ttu-id="e9109-103">Atualizar estimativa na conclusão</span><span class="sxs-lookup"><span data-stu-id="e9109-103">Update estimate at completion</span></span>

<span data-ttu-id="e9109-104">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="e9109-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e9109-105">É comum que um gestor de projeto reveja as estimativas originais de uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="e9109-105">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="e9109-106">As reprojeções do projeto são a perceção de estimativas de um gestor de projeto, dado o estado atual de um projeto.</span><span class="sxs-lookup"><span data-stu-id="e9109-106">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="e9109-107">No entanto, não recomendamos que os gestores de projeto alterem os valores da linha de base, porque a linha de base do projeto representa a fonte de verdade estabelecida para a agenda e a estimativa de custo do projeto acordadas por todos os intervenientes.</span><span class="sxs-lookup"><span data-stu-id="e9109-107">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="e9109-108">Existem duas formas de um gestor de projeto poder reprojetar o esforço nas tarefas:</span><span class="sxs-lookup"><span data-stu-id="e9109-108">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="e9109-109">Substitua a estimativa predefinida para terminar (ETC) por uma nova estimativa do esforço real restante na tarefa.</span><span class="sxs-lookup"><span data-stu-id="e9109-109">Override the default estimate to complete (ETC) with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="e9109-110">Substitua a percentagem de progresso predefinida por uma nova estimativa do verdadeiro progresso na tarefa.</span><span class="sxs-lookup"><span data-stu-id="e9109-110">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="e9109-111">Cada uma destas abordagens causa um novo cálculo da ETC, da EAC e da estimativa a completar (EAC) e percentagem de progresso da tarefa e o desvio do esforço projetado numa tarefa.</span><span class="sxs-lookup"><span data-stu-id="e9109-111">Each of these approaches cause a recalculation of the task's ETC, estimate at complete (EAC), and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="e9109-112">A EAC, a ETC e a percentagem de progresso das tarefas de resumo são recalculadas e produzem uma nova projeção de variância do esforço.</span><span class="sxs-lookup"><span data-stu-id="e9109-112">The EAC, ETC, and progress percentage on the summary tasks are recalculated, and produce a new projection of effort variance.</span></span>
