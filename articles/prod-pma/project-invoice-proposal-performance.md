---
title: Desempenho da proposta de fatura de projeto
description: Este tópico fornece informações sobre melhorias de desempenho nas propostas de faturas do projeto.
author: Yowelle
manager: AnnBe
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 20121-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1641d5f731029fdbdc16c4b652cc752a583058c6
ms.sourcegitcommit: 68d52fc983861114e654ffc8d2472b4db9b48981
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920316"
---
# <a name="project-invoice-proposal-performance"></a><span data-ttu-id="1712a-103">Desempenho da proposta de fatura de projeto</span><span class="sxs-lookup"><span data-stu-id="1712a-103">Project invoice proposal performance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1712a-104">Quando criar uma nova proposta de fatura poderá encontrar problemas de desempenho à medida que o número de projetos e subprojectos aumenta.</span><span class="sxs-lookup"><span data-stu-id="1712a-104">When you create a new invoice proposal you might encounter performance issues as the number of projects and subprojects increase.</span></span> <span data-ttu-id="1712a-105">Para melhorar o desempenho, existe uma funcionalidade que reduz o tempo necessário para criar uma nova proposta de fatura para transações de projetos publicados.</span><span class="sxs-lookup"><span data-stu-id="1712a-105">To improve performance, a feature is available that reduces the time needed to create a new invoice proposal for posted project transactions.</span></span>

## <a name="enable-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="1712a-106">Permitir a melhoria do desempenho da proposta de fatura do projeto</span><span class="sxs-lookup"><span data-stu-id="1712a-106">Enable project invoice proposal performance enhancement</span></span>
<span data-ttu-id="1712a-107">Para ativar a funcionalidade de melhoria do desempenho da proposta de fatura do projeto, complete os seguintes passos.</span><span class="sxs-lookup"><span data-stu-id="1712a-107">To enable the project invoice proposal performance enhancement feature, complete the following steps.</span></span>

1.  <span data-ttu-id="1712a-108">Vá à **Gestão de recursos** > **Tudo**.</span><span class="sxs-lookup"><span data-stu-id="1712a-108">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="1712a-109">Na lista de funcionalidades, localize **Desempenho da proposta de fatura do Projeto**.</span><span class="sxs-lookup"><span data-stu-id="1712a-109">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="1712a-110">Selecione **Ativar agora**.</span><span class="sxs-lookup"><span data-stu-id="1712a-110">Select **Enable now**.</span></span>
3.  <span data-ttu-id="1712a-111">Atualize o seu navegador e, em seguida, crie uma nova proposta de fatura.</span><span class="sxs-lookup"><span data-stu-id="1712a-111">Refresh your browser, and then create a new invoice proposal.</span></span>

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="1712a-112">Desligue a melhoria do desempenho da proposta de fatura do projeto</span><span class="sxs-lookup"><span data-stu-id="1712a-112">Turn off project invoice proposal performance enhancement</span></span>
<span data-ttu-id="1712a-113">Complete os passos seguintes para desligar a melhoria do desempenho da proposta de fatura do projeto.</span><span class="sxs-lookup"><span data-stu-id="1712a-113">Complete the following steps to turn off the project invoice proposal performance enhancement.</span></span>

1.  <span data-ttu-id="1712a-114">Vá à **Gestão de recursos** > **Tudo**.</span><span class="sxs-lookup"><span data-stu-id="1712a-114">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="1712a-115">Na lista de funcionalidades, localize **Desempenho da proposta de fatura do Projeto**.</span><span class="sxs-lookup"><span data-stu-id="1712a-115">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="1712a-116">Selecione **Desativar**.</span><span class="sxs-lookup"><span data-stu-id="1712a-116">Select **Disable**.</span></span>
3.  <span data-ttu-id="1712a-117">Atualize o seu browser.</span><span class="sxs-lookup"><span data-stu-id="1712a-117">Refresh your browser.</span></span>

> [!NOTE]
> <span data-ttu-id="1712a-118">O desempenho da proposta de fatura não pode ser aplicado quando as regras de faturação estão ativadas ou os processos de lote estão em execução.</span><span class="sxs-lookup"><span data-stu-id="1712a-118">Invoice proposal performance can't be applied when billing rules are enabled or batch processes are running.</span></span>
