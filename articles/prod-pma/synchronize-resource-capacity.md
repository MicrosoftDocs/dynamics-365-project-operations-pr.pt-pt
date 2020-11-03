---
title: Sincronizar capacidade dos recursos
description: Este tópico fornece informações sobre como sincronizar a capacidade de um recurso em calendários e projetos.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 006ebbfea42572f17663fab324a20a10321b78f0
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082382"
---
# <a name="synchronize-resource-capacity"></a><span data-ttu-id="8c9d0-103">Sincronizar capacidade dos recursos</span><span class="sxs-lookup"><span data-stu-id="8c9d0-103">Synchronize resource capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8c9d0-104">Os processos para a sincronização de recursos ajudam a garantir que a informação para o calendário e o calendário base passam para o agendamento de recursos do projeto.</span><span class="sxs-lookup"><span data-stu-id="8c9d0-104">The processes for resource synchronization help guarantee that information for the calendar and base calendar trickles down into project resource scheduling.</span></span> <span data-ttu-id="8c9d0-105">Se o calendário for alterado, os processos fazem as atualizações necessárias ao agendamento dos recursos do projeto.</span><span class="sxs-lookup"><span data-stu-id="8c9d0-105">If the calendar is changed, the processes make the required updates to the scheduling of project resources.</span></span> <span data-ttu-id="8c9d0-106">Os processos também ajudam a melhorar o desempenho, porque a informação dos recursos do calendário é sincronizada com antecedência.</span><span class="sxs-lookup"><span data-stu-id="8c9d0-106">The processes also help improve performance, because the calendar's resource information is synchronized in advance.</span></span> <span data-ttu-id="8c9d0-107">Por isso, as atualizações da informação de agendamento de recursos são mais rápidas.</span><span class="sxs-lookup"><span data-stu-id="8c9d0-107">Therefore, updates to resource scheduling information occur more quickly.</span></span> <span data-ttu-id="8c9d0-108">Recomendamos que agende os processos em lote em vez de individualmente.</span><span class="sxs-lookup"><span data-stu-id="8c9d0-108">We recommend that you schedule the processes as a batch instead of one at a time.</span></span> <span data-ttu-id="8c9d0-109">Caso contrário, existe o risco de alguém esquecer as datas inclusivas quando a informação foi sincronizada pela última vez.</span><span class="sxs-lookup"><span data-stu-id="8c9d0-109">Otherwise, there is a risk that someone will forget the inclusive dates when the information was last synchronized.</span></span> <span data-ttu-id="8c9d0-110">Se não forem utilizadas datas inclusivas, poderão ocorrer lacunas durante a sincronização de datas.</span><span class="sxs-lookup"><span data-stu-id="8c9d0-110">If inclusive dates aren't used, gaps can occur during date synchronization.</span></span>

![Sincronização do calendário](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a><span data-ttu-id="8c9d0-112">Sincronizar acumulações de capacidade dos recursos</span><span class="sxs-lookup"><span data-stu-id="8c9d0-112">Synchronize resource capacity roll-ups</span></span>

<span data-ttu-id="8c9d0-113">O processo de sincronização foi concebido para sincronizar todas as informações do calendário de recursos.</span><span class="sxs-lookup"><span data-stu-id="8c9d0-113">The synchronization process is designed to synchronize all resource calendar information.</span></span> <span data-ttu-id="8c9d0-114">Estas informações incluem as informações base do calendário sobre quaisquer alterações à tabela de capacidade do Calendário de recursos do projeto.</span><span class="sxs-lookup"><span data-stu-id="8c9d0-114">This information includes base calendar information about any changes to the project's Resource calendar capacity table.</span></span> <span data-ttu-id="8c9d0-115">Se forem adicionados novos recursos no projeto, a sincronização ajuda a garantir que a informação do calendário atualizada está disponível.</span><span class="sxs-lookup"><span data-stu-id="8c9d0-115">If new resources are added in the project, synchronization helps guarantee that the updated calendar information is available.</span></span> <span data-ttu-id="8c9d0-116">Esta sincronização pode ser feita em qualquer altura.</span><span class="sxs-lookup"><span data-stu-id="8c9d0-116">This synchronization can be done at any time.</span></span>

<span data-ttu-id="8c9d0-117">Recomendamos que utilize um lote.</span><span class="sxs-lookup"><span data-stu-id="8c9d0-117">We recommend that you use a batch.</span></span> <span data-ttu-id="8c9d0-118">As opções estão disponíveis durante a sincronização das reservas de capacidade.</span><span class="sxs-lookup"><span data-stu-id="8c9d0-118">The options are available during synchronization of capacity reservations.</span></span>

1. <span data-ttu-id="8c9d0-119">Selecione **Gestão de projetos e contabilística** &gt; **Periódico** &gt; **Sincronização da capacidade** &gt; **Sincronizar acumulações de capacidade dos recursos**.</span><span class="sxs-lookup"><span data-stu-id="8c9d0-119">Select **Project management and accounting** &gt; **Periodic** &gt; **Capacity synchronization** &gt; **Synchronize resources capacity roll-ups**.</span></span>
2. <span data-ttu-id="8c9d0-120">Defina as opções na seguinte tabela.</span><span class="sxs-lookup"><span data-stu-id="8c9d0-120">Set the options in the following table.</span></span>

    | <span data-ttu-id="8c9d0-121">Opção</span><span class="sxs-lookup"><span data-stu-id="8c9d0-121">Option</span></span>      | <span data-ttu-id="8c9d0-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="8c9d0-122">Description</span></span> |
    |-------------|-------------|
    | <span data-ttu-id="8c9d0-123">Código de período</span><span class="sxs-lookup"><span data-stu-id="8c9d0-123">Period code</span></span> | <span data-ttu-id="8c9d0-124">Opcionalmente, selecione o código do intervalo de datas do Razão geral para definir as datas de início e fim para o processo de sincronização para acumulações de capacidade de recursos.</span><span class="sxs-lookup"><span data-stu-id="8c9d0-124">Optionally select the General ledger date interval code to set the start and end dates for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="8c9d0-125">Data de início</span><span class="sxs-lookup"><span data-stu-id="8c9d0-125">Start date</span></span>  | <span data-ttu-id="8c9d0-126">Introduza a data de início para o processo de sincronização para acumulações de capacidade de recursos.</span><span class="sxs-lookup"><span data-stu-id="8c9d0-126">Enter the start date for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="8c9d0-127">Data de fim</span><span class="sxs-lookup"><span data-stu-id="8c9d0-127">End date</span></span>    | <span data-ttu-id="8c9d0-128">Introduza a data de fim para o processo de sincronização para acumulações de capacidade de recursos.</span><span class="sxs-lookup"><span data-stu-id="8c9d0-128">Enter the end date for the synchronization process for resource capacity roll-ups.</span></span> |

<span data-ttu-id="8c9d0-129">[![Processo de sincronização](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span><span class="sxs-lookup"><span data-stu-id="8c9d0-129">[![Synchronization process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span></span>
