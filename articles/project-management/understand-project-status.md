---
title: Compreender o estado do projeto
description: Este tópico fornece informações sobre o estado atribuído aos projetos no Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: bc5bc174518e46b32cf88ea7231bb2df10fde292
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127307"
---
# <a name="understand-project-status"></a><span data-ttu-id="78479-103">Compreender o estado do projeto</span><span class="sxs-lookup"><span data-stu-id="78479-103">Understand project status</span></span>

<span data-ttu-id="78479-104">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="78479-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="78479-105">A secção **Estado** na página **Entidade do Projeto** fornece um resumo o estado de funcionamento de um projeto baseado no custo e no esforço.</span><span class="sxs-lookup"><span data-stu-id="78479-105">The **Status** section on the **Project Entity** page provides a summary of a project's health based upon cost and effort.</span></span>


## <a name="status-summary-fields"></a><span data-ttu-id="78479-106">Campos Resumo do estado</span><span class="sxs-lookup"><span data-stu-id="78479-106">Status summary fields</span></span>

- <span data-ttu-id="78479-107">O campo **Estado Geral do Projeto** é um campo editável que mostra o estado geral do projeto.</span><span class="sxs-lookup"><span data-stu-id="78479-107">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="78479-108">Este campo utiliza a codificação de cores, tal como verde, amarela e vermelha, para indicar um risco de aumento.</span><span class="sxs-lookup"><span data-stu-id="78479-108">This field uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> 
- <span data-ttu-id="78479-109">O campo **Comentários** permite que o gestor de projeto introduza comentários específicos sobre o estado.</span><span class="sxs-lookup"><span data-stu-id="78479-109">The **Comments** field lets the project manager enter specific comments about the status.</span></span> 
- <span data-ttu-id="78479-110">O campo **Estado atualizado em** não é editável.</span><span class="sxs-lookup"><span data-stu-id="78479-110">The **Status updated on** field isn't editable.</span></span> <span data-ttu-id="78479-111">O valor neste campo é um carimbo de data/hora que indica quando o estado foi atualizado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="78479-111">The value in this field is a timestamp that indicates when the status was last updated.</span></span>
- <span data-ttu-id="78479-112">Os campos **Desempenho de Agendamento** e **Desempenho de Custos** são definidos a partir da grelha de monitorização.</span><span class="sxs-lookup"><span data-stu-id="78479-112">The **Schedule performance** and **Cost performance** fields are set from the tracking grid.</span></span> <span data-ttu-id="78479-113">Quando os desvios da agenda e de custo do nó raiz na vista **Controlo do esforço** são positivos, estes campos são atualizados para **Adiantado**.</span><span class="sxs-lookup"><span data-stu-id="78479-113">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, these fields are updated to **Ahead**.</span></span> <span data-ttu-id="78479-114">Quando a variação da agenda e do custo para o nó raiz é negativa, estes campos são definidos como **Atrasado**.</span><span class="sxs-lookup"><span data-stu-id="78479-114">When the schedule and cost variance for the root node are negative, these fields are set to **Behind**.</span></span>
