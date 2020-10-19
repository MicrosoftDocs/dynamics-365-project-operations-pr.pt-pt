---
title: Criar propostas do projeto a partir de oportunidades
description: Este tópico fornece informações sobre como criar uma proposta de projeto a partir de uma oportunidade.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 606098473db479d0015e3a7a3c01a3d3b6de9db1
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898546"
---
# <a name="create-project-quotes-from-opportunities"></a><span data-ttu-id="adc20-103">Criar propostas do projeto a partir de oportunidades</span><span class="sxs-lookup"><span data-stu-id="adc20-103">Create project quotes from opportunities</span></span>

<span data-ttu-id="adc20-104">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="adc20-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="adc20-105">As propostas podem ser criadas a partir de oportunidades do projeto das seguintes formas:</span><span class="sxs-lookup"><span data-stu-id="adc20-105">Quotes can be created from project opportunities in the following ways:</span></span>

- <span data-ttu-id="adc20-106">A partir do separador **Propostas** na página **Oportunidade de Projeto**</span><span class="sxs-lookup"><span data-stu-id="adc20-106">From the **Quotes** tab on the **Project Opportunity** page</span></span>
- <span data-ttu-id="adc20-107">A partir do Fluxo do processo de vendas de oportunidade</span><span class="sxs-lookup"><span data-stu-id="adc20-107">From the Opportunity sales process flow</span></span>
- <span data-ttu-id="adc20-108">Ao atualizar a referência da oportunidade numa proposta existente</span><span class="sxs-lookup"><span data-stu-id="adc20-108">By updating the opportunity reference on an existing quote</span></span>

## <a name="from-the-quotes-tab-of-the-project-opportunity-page"></a><span data-ttu-id="adc20-109">A partir do separador Propostas da página Oportunidade de Projeto</span><span class="sxs-lookup"><span data-stu-id="adc20-109">From the Quotes tab of the Project Opportunity page</span></span>

<span data-ttu-id="adc20-110">Para criar uma proposta de projeto a partir de uma oportunidade, conclua os seguintes passos.</span><span class="sxs-lookup"><span data-stu-id="adc20-110">To create a project quote from an opportunity, complete the following steps.</span></span>

1. <span data-ttu-id="adc20-111">Abra a página **Oportunidade de Projeto** e selecione o separador **Propostas**.</span><span class="sxs-lookup"><span data-stu-id="adc20-111">Open the **Project Opportunity** page and select the **Quotes** tab.</span></span> 
2. <span data-ttu-id="adc20-112">Na subgrelha **Propostas**, selecione **+** para criar uma nova proposta de projeto baseada na oportunidade.</span><span class="sxs-lookup"><span data-stu-id="adc20-112">On the **Quotes** sub-grid, select the **+** to create a new project quote based on the opportunity.</span></span> <span data-ttu-id="adc20-113">Todas as linhas de oportunidade e listas de preços do Projeto relacionadas são copiadas para a nova proposta a partir da oportunidade.</span><span class="sxs-lookup"><span data-stu-id="adc20-113">All of the opportunity lines and related Project price lists are copied to the new quote from the opportunity.</span></span>

## <a name="from-the-opportunity-sales-process-flow"></a><span data-ttu-id="adc20-114">A partir do Fluxo do processo de vendas de oportunidade</span><span class="sxs-lookup"><span data-stu-id="adc20-114">From the Opportunity sales process flow</span></span>

<span data-ttu-id="adc20-115">Para criar uma proposta a partir do Fluxo do processo de vendas de oportunidade, conclua os seguintes passos.</span><span class="sxs-lookup"><span data-stu-id="adc20-115">To create a quote from the Opportunity sales process flow, complete the following steps.</span></span>

1. <span data-ttu-id="adc20-116">A partir do Fluxo do processo de vendas de oportunidade, abra a Oportunidade.</span><span class="sxs-lookup"><span data-stu-id="adc20-116">From the Opportunity sales process flow, open the Opportunity.</span></span>
2. <span data-ttu-id="adc20-117">Selecione a fase **Qualificar**.</span><span class="sxs-lookup"><span data-stu-id="adc20-117">Select the **Qualify** stage.</span></span> 
3. <span data-ttu-id="adc20-118">Selecione **Seguinte** e, em seguida, selecione **+ Criar** para criar uma nova proposta.</span><span class="sxs-lookup"><span data-stu-id="adc20-118">Select **Next** and then select **+ Create** to create a new quote.</span></span> <span data-ttu-id="adc20-119">A maioria das informações no separador **Resumo** para esta nova proposta terão sido assumidas por predefinição a partir da oportunidade.</span><span class="sxs-lookup"><span data-stu-id="adc20-119">Most of the information on the **Summary** tab for this new quote will have defaulted from the opportunity.</span></span> 
4. <span data-ttu-id="adc20-120">Introduza todas as informações necessárias em falta ou atualize os valores predefinidos, conforme necessário no separador **Resumo**.</span><span class="sxs-lookup"><span data-stu-id="adc20-120">Enter in any required information that is missing, or update defaulted values as necessary on the **Summary** tab,</span></span>
5. <span data-ttu-id="adc20-121">Selecione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="adc20-121">Select **Save**.</span></span> <span data-ttu-id="adc20-122">A nova proposta é criada e associada à oportunidade.</span><span class="sxs-lookup"><span data-stu-id="adc20-122">The new quote is created and associated to the opportunity.</span></span> <span data-ttu-id="adc20-123">Pode agora ver as informações da proposta no separador **Propostas** da página **Oportunidade**.</span><span class="sxs-lookup"><span data-stu-id="adc20-123">You can now view the quote information on the **Quotes** tab of the **Opportunity** page.</span></span> 

   <span data-ttu-id="adc20-124">O Processo de vendas da oportunidade avança para a fase seguinte, **Propor**.</span><span class="sxs-lookup"><span data-stu-id="adc20-124">The Opportunity sales process moves to the next stage, **Propose**.</span></span>


## <a name="by-updating-the-opportunity-reference-on-an-existing-quote"></a><span data-ttu-id="adc20-125">Ao atualizar a referência da oportunidade numa proposta existente</span><span class="sxs-lookup"><span data-stu-id="adc20-125">By updating the opportunity reference on an existing quote</span></span>

<span data-ttu-id="adc20-126">Uma proposta existente pode ser associada a uma Oportunidade.</span><span class="sxs-lookup"><span data-stu-id="adc20-126">An existing quote can be linked to an Opportunity.</span></span> <span data-ttu-id="adc20-127">Conclua os seguintes passos para atualizar as Informações da oportunidade numa proposta existente.</span><span class="sxs-lookup"><span data-stu-id="adc20-127">Complete the following steps to update the Opportunity information on an existing quote.</span></span>

1. <span data-ttu-id="adc20-128">Abra a página **Proposta** e selecione o separador **Resumo**.</span><span class="sxs-lookup"><span data-stu-id="adc20-128">Open the **Quote** page and select the **Summary** tab.</span></span>
2. <span data-ttu-id="adc20-129">No campo **Oportunidade**, selecione a oportunidade que pretende associar à proposta.</span><span class="sxs-lookup"><span data-stu-id="adc20-129">In the **Opportunity** field, select the opportunity that you want to link to the quote.</span></span> <span data-ttu-id="adc20-130">Pode ver a proposta na grelha **Propostas** da Oportunidade.</span><span class="sxs-lookup"><span data-stu-id="adc20-130">You can see the quote in the **Quotes** grid of the Opportunity.</span></span> 
3. <span data-ttu-id="adc20-131">Ao utilizar o Processo de vendas da oportunidade, a oportunidade pode avançar para a fase seguinte, **Propor**.</span><span class="sxs-lookup"><span data-stu-id="adc20-131">Using the Opportunity sales process, the opportunity can be moved to the next stage, **Propose**.</span></span> 

   <span data-ttu-id="adc20-132">Ao fazer uma oportunidade avançar para esta fase, pode selecionar esta proposta a partir de uma lista de propostas associadas a esta oportunidade.</span><span class="sxs-lookup"><span data-stu-id="adc20-132">When you move an opportunity to this stage, you can select this quote from a list of quotes associated with this opportunity.</span></span> <span data-ttu-id="adc20-133">A seleção desta proposta indica que está a avançar com ela.</span><span class="sxs-lookup"><span data-stu-id="adc20-133">Selecting this quote indicates that you're moving forward with it.</span></span>

   <span data-ttu-id="adc20-134">Todas as outras propostas associadas à Oportunidade continuarão disponíveis e ativas até uma delas ser ganha.</span><span class="sxs-lookup"><span data-stu-id="adc20-134">All the other quotes associated with the Opportunity will still be available and active until one of them is won.</span></span> <span data-ttu-id="adc20-135">Pode fazer retroceder o processo de vendas para a fase anterior **Qualificar** e escolher outra proposta com a qual avançar.</span><span class="sxs-lookup"><span data-stu-id="adc20-135">You can move the sales process back to the previous stage **Qualify**, and pick another quote to move forward with.</span></span>
