---
title: Conjuntos de aprovações
description: Este tópico fornece informações sobre o conjunto de aprovações, os pedidos e os subconjuntos dessas operações.
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: ac73313420029ece740d0bdb9c21c7abaa9defc6
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116885"
---
# <a name="approval-sets"></a><span data-ttu-id="54e4f-103">Conjuntos de aprovações</span><span class="sxs-lookup"><span data-stu-id="54e4f-103">Approval sets</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="54e4f-104">Os conjuntos de aprovações agrupam os pedidos de aprovação em subconjuntos de operações mais pequenos.</span><span class="sxs-lookup"><span data-stu-id="54e4f-104">Approval sets group approval requests together into smaller subsets of operations.</span></span> <span data-ttu-id="54e4f-105">Este agrupamento permite que as aprovações sejam processadas por ordem do Projeto e permite a repetição e sequenciação.</span><span class="sxs-lookup"><span data-stu-id="54e4f-105">This grouping allows approvals to be processed in order by Project and allows for retrying and sequencing.</span></span> <span data-ttu-id="54e4f-106">O agrupamento melhora a fiabilidade e a rastreabilidade do processamento de aprovação para grandes volumes de aprovações.</span><span class="sxs-lookup"><span data-stu-id="54e4f-106">Grouping improves the reliability and traceability of approval processing for large volumes of approvals.</span></span>

<span data-ttu-id="54e4f-107">Os conjuntos de aprovações indicam o estado geral de processamento dos seus registos relacionados.</span><span class="sxs-lookup"><span data-stu-id="54e4f-107">Approval sets indicate the overall processing state of their related records.</span></span> <span data-ttu-id="54e4f-108">Quando um registo de aprovação é processado usando um conjunto de aprovação, o registo passa de **Submetido** a **Aprovado** e é desassociado do conjunto de aprovação.</span><span class="sxs-lookup"><span data-stu-id="54e4f-108">When an approval record is processed using an approval set, the record moves from **Submitted** to **Approved**, and is unlinked from the approval set.</span></span> <span data-ttu-id="54e4f-109">Se um registo falhar quando for submetido a aprovação, o registo permanece num estado de **Submetido** e o conjunto de aprovação é marcado como falhado.</span><span class="sxs-lookup"><span data-stu-id="54e4f-109">If a record fails when it is submitted for approval, the record remains in a status of **Submitted** and the approval set is marked as failed.</span></span> <span data-ttu-id="54e4f-110">O conjunto de aprovação regista a mensagem de erro da falha.</span><span class="sxs-lookup"><span data-stu-id="54e4f-110">The approval set logs the error message of the failure.</span></span>

## <a name="processing-approvals-and-approval-sets"></a><span data-ttu-id="54e4f-111">Processamento de aprovações e conjuntos de aprovações</span><span class="sxs-lookup"><span data-stu-id="54e4f-111">Processing approvals and approval sets</span></span>
<span data-ttu-id="54e4f-112">As aprovações que estão em fila para processamento são visíveis na vista **Processamento de Aprovações**.</span><span class="sxs-lookup"><span data-stu-id="54e4f-112">Approvals that are queued for processing are visible in the **Processing Approvals** view.</span></span> <span data-ttu-id="54e4f-113">O sistema tenta processar todas as entradas várias vezes assincronamente, incluindo repetir uma aprovação se as tentativas anteriores tiverem falhado.</span><span class="sxs-lookup"><span data-stu-id="54e4f-113">The system tries to process all the entries multiple times asynchronously, including retrying an approval if previous attempts failed.</span></span>

<span data-ttu-id="54e4f-114">O campo **Duração do Conjunto de Aprovação** regista o número de tentativas restantes para processar o conjunto antes de ser marcado como falhado.</span><span class="sxs-lookup"><span data-stu-id="54e4f-114">The **Approval Set Lifetime** field records the number of attempts left to process the set before it's marked as failed.</span></span>

## <a name="failed-approvals-and-approval-sets"></a><span data-ttu-id="54e4f-115">Aprovações e conjuntos de aprovações falhados</span><span class="sxs-lookup"><span data-stu-id="54e4f-115">Failed approvals and approval sets</span></span>
<span data-ttu-id="54e4f-116">A vista **Aprovações Falhadas** lista todas as aprovações que requerem intervenção do utilizador.</span><span class="sxs-lookup"><span data-stu-id="54e4f-116">The **Failed Approvals** view lists all approvals that require user intervention.</span></span> <span data-ttu-id="54e4f-117">Abra os registos de conjunto de aprovação associados para identificar a causa da falha.</span><span class="sxs-lookup"><span data-stu-id="54e4f-117">Open the associated approval set logs to identify the cause of the failure.</span></span>
<span data-ttu-id="54e4f-118">A seleção de **Repetir** adiciona à contagem de duração do conjunto de aprovação, move o conjunto de aprovação para um estado de **Processamento** e tenta processar os registos restantes.</span><span class="sxs-lookup"><span data-stu-id="54e4f-118">Selecting **Retry** adds to the approval set lifetime count, moves the approval set back to a status of **Processing**, and attempts to process the remaining records.</span></span>

## <a name="configure-approval-sets"></a><span data-ttu-id="54e4f-119">Configurar conjuntos de aprovação</span><span class="sxs-lookup"><span data-stu-id="54e4f-119">Configure approval sets</span></span>

###  <a name="enable-the-approval-sets-feature"></a><span data-ttu-id="54e4f-120">Ativar a funcionalidade Conjuntos de aprovação</span><span class="sxs-lookup"><span data-stu-id="54e4f-120">Enable the Approval sets feature</span></span>
<span data-ttu-id="54e4f-121">Antes de ativar a funcionalidade de Conjuntos de aprovação, verifique se não existem aprovações atualmente em processamento.</span><span class="sxs-lookup"><span data-stu-id="54e4f-121">Before you enable the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="54e4f-122">Aceda à página **Parâmetros do projeto** e selecione **Controlo de Funcionalidades** > **Ativar Aprovações Modernas**.</span><span class="sxs-lookup"><span data-stu-id="54e4f-122">Go to the **Project parameters** page and select **Feature Control** > **Enable Modern Approvals**.</span></span>

### <a name="turn-off-the-approval-sets-feature"></a><span data-ttu-id="54e4f-123">Desativar a funcionalidade Conjuntos de aprovação</span><span class="sxs-lookup"><span data-stu-id="54e4f-123">Turn off the Approval sets feature</span></span>
<span data-ttu-id="54e4f-124">Antes de desativar a funcionalidade de Conjuntos de aprovação, verifique se não existem aprovações atualmente em processamento.</span><span class="sxs-lookup"><span data-stu-id="54e4f-124">Before you turn off the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="54e4f-125">Aceda à página **Parâmetros do Projeto** e selecione **Controlo de Funcionalidades** > **Desativar Aprovações Modernas**.</span><span class="sxs-lookup"><span data-stu-id="54e4f-125">Go to the **Project Parameters** page and select **Feature Control** > **Disable Modern Approvals**.</span></span>

### <a name="configuring-the-asynchronous-threshold"></a><span data-ttu-id="54e4f-126">Configurar o limiar assíncrono</span><span class="sxs-lookup"><span data-stu-id="54e4f-126">Configuring the asynchronous threshold</span></span> 
<span data-ttu-id="54e4f-127">Quando os conjuntos de aprovação são criados, o processamento move-se para segundo plano quando o número selecionado de registos de aprovação excede o limiar indicado.</span><span class="sxs-lookup"><span data-stu-id="54e4f-127">When approval sets are created, processing moves to the background when the selected number of records for approval exceeds the indicated threshold.</span></span> <span data-ttu-id="54e4f-128">Utilize o campo **Limiar Assíncrono** para configurar quando o processamento de aprovação deve ser executado de forma síncrona ou assíncrona.</span><span class="sxs-lookup"><span data-stu-id="54e4f-128">Use the **Asynchronous Threshold** field to configure when approval processing should be run synchronously or asynchronously.</span></span>
<span data-ttu-id="54e4f-129">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="54e4f-129">Valid values are:</span></span>

  - <span data-ttu-id="54e4f-130">Zero: Todos os pedidos devem ser processados assincronamente.</span><span class="sxs-lookup"><span data-stu-id="54e4f-130">Zero: All requests should be processed asynchronously.</span></span> 
  - <span data-ttu-id="54e4f-131">Números superiores a zero: As aprovações são processadas assincronamente apenas quando o número de aprovações submetidas excede este valor.</span><span class="sxs-lookup"><span data-stu-id="54e4f-131">Numbers greater than zero: Approvals are processed asynchronously only when the submitted number of approvals exceeds this value.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
