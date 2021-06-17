---
title: O que há de novo março de 2021 - Implementação de Project Operations lite
description: Este tópico fornece informações sobre as atualizações de qualidade disponíveis na versão de março de 2021 da implementação do Project Operations lite – negócio para faturação pró-forma.
author: sigitac
ms.date: 03/03/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: efddb96b2cb428b9dc0488c32eb5670d01322bcb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993880"
---
# <a name="whats-new-march-2021---project-operations-lite-deployment"></a><span data-ttu-id="aae39-103">O que há de novo março de 2021 - Implementação de Project Operations lite</span><span class="sxs-lookup"><span data-stu-id="aae39-103">What's new March 2021 - Project Operations lite deployment</span></span>

<span data-ttu-id="aae39-104">_Aplica-se a: Implementação lite – negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="aae39-104">_Applies To: Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="aae39-105">Este tópico aplica-se aos seguintes componentes e versões do Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="aae39-105">This topic applies to the following Dynamics 365 Project Operations components and versions:</span></span>

- <span data-ttu-id="aae39-106">Project Operations na versão 4.8.0.91 do ambiente Dataverse</span><span class="sxs-lookup"><span data-stu-id="aae39-106">Project Operations on Dataverse environment version 4.8.0.91</span></span> 

## <a name="quality-updates"></a><span data-ttu-id="aae39-107">Atualizações de qualidade</span><span class="sxs-lookup"><span data-stu-id="aae39-107">Quality updates</span></span>

| <span data-ttu-id="aae39-108">**Área de funcionalidades**</span><span class="sxs-lookup"><span data-stu-id="aae39-108">**Feature area**</span></span> | <span data-ttu-id="aae39-109">**Número de referência**</span><span class="sxs-lookup"><span data-stu-id="aae39-109">**Reference number**</span></span> | <span data-ttu-id="aae39-110">**Atualização de qualidade**</span><span class="sxs-lookup"><span data-stu-id="aae39-110">**Quality update**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="aae39-111">Faturação e preços</span><span class="sxs-lookup"><span data-stu-id="aae39-111">Billing and pricing</span></span> | <span data-ttu-id="aae39-112">2133873</span><span class="sxs-lookup"><span data-stu-id="aae39-112">2133873</span></span> | <span data-ttu-id="aae39-113">Definiu o visor do símbolo da **moeda de preço de venda** unitária na grelha de **estimativas de despesas**.</span><span class="sxs-lookup"><span data-stu-id="aae39-113">Fixed the display of **Unit Sales Price** currency symbol in the **Expense Estimates** grid.</span></span> |
| <span data-ttu-id="aae39-114">Faturação e preços</span><span class="sxs-lookup"><span data-stu-id="aae39-114">Billing and pricing</span></span> | <span data-ttu-id="aae39-115">2174616</span><span class="sxs-lookup"><span data-stu-id="aae39-115">2174616</span></span> | <span data-ttu-id="aae39-116">Quando uma proposta é ganha, a lista de preços personalizados do contrato é referenciada em detalhes do item de contrato que são copiados da proposta.</span><span class="sxs-lookup"><span data-stu-id="aae39-116">When a quote is won, the contract custom pricelist is referenced on contract line details that are copied from the quote.</span></span> |
| <span data-ttu-id="aae39-117">Gestão de oportunidades</span><span class="sxs-lookup"><span data-stu-id="aae39-117">Opportunity Management</span></span> | <span data-ttu-id="aae39-118">2167475</span><span class="sxs-lookup"><span data-stu-id="aae39-118">2167475</span></span> | <span data-ttu-id="aae39-119">Montante fixo do imposto na fatura de correção que originou uma entrada efetiva não faturada.</span><span class="sxs-lookup"><span data-stu-id="aae39-119">Fixed tax amount in the correction invoice that originated an unbilled actual entry.</span></span> |
| <span data-ttu-id="aae39-120">Gestão de oportunidades</span><span class="sxs-lookup"><span data-stu-id="aae39-120">Opportunity Management</span></span> | <span data-ttu-id="aae39-121">2176285</span><span class="sxs-lookup"><span data-stu-id="aae39-121">2176285</span></span> | <span data-ttu-id="aae39-122">O montante do imposto não deve ser copiado dos detalhes do item de contrato de venda/cotação para os detalhes do item de contrato/cotação de custos.</span><span class="sxs-lookup"><span data-stu-id="aae39-122">Tax amount must not be copied from sales contract/quote line details to cost contract/quote line details.</span></span> |
| <span data-ttu-id="aae39-123">Gestão de oportunidades</span><span class="sxs-lookup"><span data-stu-id="aae39-123">Opportunity Management</span></span> | <span data-ttu-id="aae39-124">2188079</span><span class="sxs-lookup"><span data-stu-id="aae39-124">2188079</span></span> | <span data-ttu-id="aae39-125">A regra de faturação dividida não deve ser criada para contratos que não sejam baseados no trabalho.</span><span class="sxs-lookup"><span data-stu-id="aae39-125">Split billing rule must not be created for contracts that are not work-based.</span></span> |
| <span data-ttu-id="aae39-126">Planeamento e deteção de movimentos</span><span class="sxs-lookup"><span data-stu-id="aae39-126">Planning and Tracking</span></span> | <span data-ttu-id="aae39-127">2138853</span><span class="sxs-lookup"><span data-stu-id="aae39-127">2138853</span></span> | <span data-ttu-id="aae39-128">Função de cópia do projeto atualizada para garantir linhas de estimativa de despesas que as tarefas de referência são copiadas para o projeto de destino.</span><span class="sxs-lookup"><span data-stu-id="aae39-128">Project copy function updated to ensure expense estimate lines that reference tasks are copied to the destination project.</span></span> |
| <span data-ttu-id="aae39-129">Planeamento e deteção de movimentos</span><span class="sxs-lookup"><span data-stu-id="aae39-129">Planning and Tracking</span></span> | <span data-ttu-id="aae39-130">2173259</span><span class="sxs-lookup"><span data-stu-id="aae39-130">2173259</span></span> | <span data-ttu-id="aae39-131">Função de cópia do projeto atualizada para garantir que não exibe a mensagem de erro **A copiar WBS** em certos cenários.</span><span class="sxs-lookup"><span data-stu-id="aae39-131">Project copy function updated to ensure it doesn't display the **Copying WBS** error message in certain scenarios.</span></span> |
| <span data-ttu-id="aae39-132">Tempo e Despesa</span><span class="sxs-lookup"><span data-stu-id="aae39-132">Time and Expense</span></span> | <span data-ttu-id="aae39-133">2148910</span><span class="sxs-lookup"><span data-stu-id="aae39-133">2148910</span></span> | <span data-ttu-id="aae39-134">Problema de exibição solucionado com a página de **Editar entrada** na grelha de **Entrada de tempo**.</span><span class="sxs-lookup"><span data-stu-id="aae39-134">Fixed display issue with the **Edit Entry** page in the **Time Entry** grid.</span></span> |
| <span data-ttu-id="aae39-135">Tempo e Despesa</span><span class="sxs-lookup"><span data-stu-id="aae39-135">Time and Expense</span></span> | <span data-ttu-id="aae39-136">2159798</span><span class="sxs-lookup"><span data-stu-id="aae39-136">2159798</span></span> | <span data-ttu-id="aae39-137">Controlos apertados para garantir que as entradas de despesas aprovadas não podem ser editadas.</span><span class="sxs-lookup"><span data-stu-id="aae39-137">Tightened controls to ensure approved expense entries can't be edited.</span></span> |


