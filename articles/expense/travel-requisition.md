---
title: Requisições de viagens
description: Este tópico fornece informações sobre as requisições de viagens.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 0261405abb9305d7f6abcde9cb90d9b184868580
ms.sourcegitcommit: a0f80d024a5d3112a39781815bd31d0c05ddaf6f
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 09/30/2020
ms.locfileid: "3906288"
---
# <a name="travel-requisitions"></a><span data-ttu-id="46bb1-103">Requisições de viagens</span><span class="sxs-lookup"><span data-stu-id="46bb1-103">Travel requisitions</span></span>

<span data-ttu-id="46bb1-104">_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_</span><span class="sxs-lookup"><span data-stu-id="46bb1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="46bb1-105">Uma requisição de viagens lista as despesas que serão incorridas com a finalidade de viajar.</span><span class="sxs-lookup"><span data-stu-id="46bb1-105">A travel requisition lists the expenses that will be incurred for the purpose of travel.</span></span> <span data-ttu-id="46bb1-106">É submetida uma requisição de viagens para revisão e pode ser utilizada para autorizar as despesas.</span><span class="sxs-lookup"><span data-stu-id="46bb1-106">A travel requisition is submitted for review and can be used to authorize expenses.</span></span>

<span data-ttu-id="46bb1-107">Poderá ter de submeter uma requisição de viagens antes de incorrer em qualquer despesa que seja cobrada à organização.</span><span class="sxs-lookup"><span data-stu-id="46bb1-107">You may be required to submit a travel requisition before you incur any expense that is charged to the organization.</span></span> <span data-ttu-id="46bb1-108">Esta requisição aplica-se, independentemente de imputar as despesas a um cartão de crédito da empresa, gastar o dinheiro que recebeu de um adiantamento de tesouraria ou incorrer em despesas correntes que serão reembolsadas pela organização.</span><span class="sxs-lookup"><span data-stu-id="46bb1-108">This requirement applies, regardless of whether you charge expenses to a corporate credit card, spend cash that you received from a cash advance, or incur out-of-pocket expenses that will be reimbursed by the organization.</span></span>

<span data-ttu-id="46bb1-109">As políticas e requisições de viagens poderão ser utilizados para ajudar a gerir as despesas da organização.</span><span class="sxs-lookup"><span data-stu-id="46bb1-109">Travel requisitions and policies can be used to help manage organization expenditures.</span></span> <span data-ttu-id="46bb1-110">Por exemplo, se a sua organização estiver a trabalhar num projeto de preço fixo que exija viagens, as despesas de viagem dos membros da equipa do projeto têm de enquadrar-se no orçamento do projeto.</span><span class="sxs-lookup"><span data-stu-id="46bb1-110">For example, if your organization is working on a fixed-price project that requires travel, the travel expenses of the project's team members must fit within the project budget.</span></span> <span data-ttu-id="46bb1-111">Ao exigir que as despesas de viagem sejam aprovadas antes de serem incorridas, a organização pode ajudar a garantir que o projeto cumpre o orçamento.</span><span class="sxs-lookup"><span data-stu-id="46bb1-111">By requiring that travel expenses be approved before they are incurred, the organization can help make sure that the project remains within budget.</span></span>

## <a name="configuration"></a><span data-ttu-id="46bb1-112">Configuração</span><span class="sxs-lookup"><span data-stu-id="46bb1-112">Configuration</span></span> 

<span data-ttu-id="46bb1-113">As Requisições de Viagens podem ser configurados como "obrigatórios" ao ativarem o parâmetro "A pré-autorização de viagem é obrigatória" nos Parâmetros de Gestão de Despesas.</span><span class="sxs-lookup"><span data-stu-id="46bb1-113">Travel Requisitions can be configured as "mandatory" by enabling the "Pre-authorization of travel is mandatory" parameter in Expense Management Parameters.</span></span> 

## <a name="create-and-submit-a-travel-requisition"></a><span data-ttu-id="46bb1-114">Criar e submeter uma requisição de viagens</span><span class="sxs-lookup"><span data-stu-id="46bb1-114">Create and submit a travel requisition</span></span>

1. <span data-ttu-id="46bb1-115">Vá para **As Minhas Despesas: Requisição de viagens** e selecione **Nova requisição de viagens**.</span><span class="sxs-lookup"><span data-stu-id="46bb1-115">Go to **My expenses: Travel Requisition**, and select **New travel Requisition**.</span></span>
2. <span data-ttu-id="46bb1-116">Introduza o objetivo e o destino para a requisição.</span><span class="sxs-lookup"><span data-stu-id="46bb1-116">Enter a purpose and destination for the requisition.</span></span>
3. <span data-ttu-id="46bb1-117">No campo **Descrição da viagem**, introduza quaisquer informações adicionais.</span><span class="sxs-lookup"><span data-stu-id="46bb1-117">In the  **Travel description** field, enter any additional information.</span></span> 
4. <span data-ttu-id="46bb1-118">Para cada uma das despesas esperadas, como Voo, refeições ou aluguer de automóvel, crie um item de despesas.</span><span class="sxs-lookup"><span data-stu-id="46bb1-118">For each of the expected expenses, such as Flight, meals, or car rental, create an expense line item.</span></span> <span data-ttu-id="46bb1-119">Inclua a data estimada, o valor estimado e a moeda para cada despesa.</span><span class="sxs-lookup"><span data-stu-id="46bb1-119">Include the estimated date, estimated amount, and the currency for each expense.</span></span> 
5. <span data-ttu-id="46bb1-120">Quando terminar de adicionar as despesas esperadas, selecione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="46bb1-120">When you have finished adding the expected expenses, select **Save**.</span></span>
6. <span data-ttu-id="46bb1-121">Quando estiver pronto para submeter a requisição de viagens, selecione **Fluxo de trabalho** > **Submeter**.</span><span class="sxs-lookup"><span data-stu-id="46bb1-121">When you are ready to submit the travel requisition, select **Workflow** > **Submit**.</span></span>

<span data-ttu-id="46bb1-122">Pode ver as suas requisições de viagens aprovadas em **As Minhas Despesas: Requisição de Viagens**.</span><span class="sxs-lookup"><span data-stu-id="46bb1-122">You can view your approved travel requisitions under **My Expenses: Travel Requisition**.</span></span> 

## <a name="view-available-travel-requisitions"></a><span data-ttu-id="46bb1-123">Ver requisições de viagens disponíveis</span><span class="sxs-lookup"><span data-stu-id="46bb1-123">View available travel requisitions</span></span>

<span data-ttu-id="46bb1-124">Pode ver todas as suas requisições de viagens aprovadas em **As Minhas Despesas: Requisições de Viagens**.</span><span class="sxs-lookup"><span data-stu-id="46bb1-124">You can view all of your travel requisitions under **My Expenses: Travel Requisitions**.</span></span>

## <a name="approve-travel-requisitions"></a><span data-ttu-id="46bb1-125">Aprovar requisições de viagens</span><span class="sxs-lookup"><span data-stu-id="46bb1-125">Approve travel requisitions</span></span>

<span data-ttu-id="46bb1-126">Selecione a requisição de viagens que pretende aprovar e, em seguida, selecione **Fluxo de trabalho** > **Aprovar**.</span><span class="sxs-lookup"><span data-stu-id="46bb1-126">Select the travel requisition that you want to approve, and then select **Workflow** > **Approve**.</span></span>  

## <a name="submit-an-expense-report-using-your-approved-travel-requisition"></a><span data-ttu-id="46bb1-127">Submeta um relatório de despesas através da sua requisição de viagem aprovada</span><span class="sxs-lookup"><span data-stu-id="46bb1-127">Submit an expense report using your approved travel requisition</span></span>

1. <span data-ttu-id="46bb1-128">Crie um novo relatório de despesas e, no cabeçalho do relatório de despesas, e a partir da lista de requisições de viagem aprovadas, selecione **Mapear para a Requisição de viagens**.</span><span class="sxs-lookup"><span data-stu-id="46bb1-128">Create a new expense report and in the expense report header, and from the list of approved travel requisitions, select **Map to Travel requisition**.</span></span>
2. <span data-ttu-id="46bb1-129">O campo **Montante da requisição de viagens** é atualizado automaticamente no cabeçalho do relatório de despesas.</span><span class="sxs-lookup"><span data-stu-id="46bb1-129">The **Travel requisition amount** field is automatically updated in the expense report header.</span></span>
3. <span data-ttu-id="46bb1-130">Adicione cada despesa incorrida para a viagem.</span><span class="sxs-lookup"><span data-stu-id="46bb1-130">Add each expense incurred for the trip.</span></span> <span data-ttu-id="46bb1-131">Se o campo **Pré-autorizado** estiver ativado, o montante reconciliado e o montante autorizado para a categoria de despesas específica serão atualizados.</span><span class="sxs-lookup"><span data-stu-id="46bb1-131">If the **Pre-authorized** field is enabled, the reconciled amount and authorized amount for the specific expense category will be updated.</span></span>

> [!NOTE]
> <span data-ttu-id="46bb1-132">Quando mapeia um relatório de despesas para uma requisição de viagens aprovada, o valor da transação não pode ser superior ao valor autorizado.</span><span class="sxs-lookup"><span data-stu-id="46bb1-132">When you map an expense report to an approved travel requisition, the transaction amount can't be greater than the authorized amount.</span></span> 
