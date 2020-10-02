---
title: Desativar uma dimensão de definição de preços
description: Este tópico fornece informações sobre como desativar dimensões de definição de preço.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
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
ms.openlocfilehash: 54e02726138f7306481ca50d5204ee29a3b68549
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896520"
---
# <a name="turning-off-a-pricing-dimension"></a><span data-ttu-id="510a1-103">Desativar uma dimensão de definição de preços</span><span class="sxs-lookup"><span data-stu-id="510a1-103">Turning off a pricing dimension</span></span>

<span data-ttu-id="510a1-104">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="510a1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="510a1-105">Poderá ter de analisar e atualizar a sua estratégia de definição de preços a cada ano.</span><span class="sxs-lookup"><span data-stu-id="510a1-105">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="510a1-106">Quaisquer atualizações feitas podem exigir que desative uma dimensão de definição de preços existente e crie uma nova.</span><span class="sxs-lookup"><span data-stu-id="510a1-106">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="510a1-107">Por exemplo, poderá ter de definir o preço anteriormente por **Função**, mas agora decidiu definir o preço por **Experiência de Trabalho**.</span><span class="sxs-lookup"><span data-stu-id="510a1-107">For example, you may have previously priced by **Role**, but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="510a1-108">Isto poderá fazer com que seja necessário desativar a **Função** como uma dimensão de definição de preços e criar uma **Experiência de Trabalho** como uma nova dimensão de definição de preços.</span><span class="sxs-lookup"><span data-stu-id="510a1-108">This may require you to turn off **Role** as a pricing dimension and create **Work Experience** as a new pricing dimension.</span></span> 

<span data-ttu-id="510a1-109">A desativação de uma dimensão de definição de preços, independentemente de a mesma ser fornecida com o programa ou personalizada, pode ser efetuada definindo os campos **Aplicável ao Custo** e **Aplicável às Vendas** da Dimensão de Definição de Preços como **Não**.</span><span class="sxs-lookup"><span data-stu-id="510a1-109">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="510a1-110">No entanto, quando o fizer, poderá receber a mensagem de erro, **a dimensão da definição dos preços não pode ser atualizada ou eliminada se existirem registos de preços associados.**</span><span class="sxs-lookup"><span data-stu-id="510a1-110">However, when you do this, you might receive the error message, **Pricing dimension cannot be updated or deleted if there are associated price records.**</span></span>

<span data-ttu-id="510a1-111">Esta mensagem de erro indica que existem registos de preços configurados anteriormente para a dimensão que está a ser desativada.</span><span class="sxs-lookup"><span data-stu-id="510a1-111">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="510a1-112">Todos os registos **Preço da Função** e **Margem de Lucro do Preço da Função** que façam referência a uma dimensão têm de ser eliminados antes de a aplicabilidade da dimensão poder ser definida como **Não**.</span><span class="sxs-lookup"><span data-stu-id="510a1-112">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="510a1-113">Esta regra aplica-se às dimensões de definição de preços fornecidas com o programa e a quaisquer dimensões de definição de preços personalizadas que possa ter criado.</span><span class="sxs-lookup"><span data-stu-id="510a1-113">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="510a1-114">O motivo desta validação é porque cada registo **Preço da Função** deve ter uma combinação exclusiva de dimensões.</span><span class="sxs-lookup"><span data-stu-id="510a1-114">The reason for this validation is because each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="510a1-115">Por exemplo, numa lista de preços denominada **Taxas de custo nos EUA 2018**, tem as seguintes linhas de **Preço da Função**.</span><span class="sxs-lookup"><span data-stu-id="510a1-115">For example, on a price list called **US Cost Rates 2018**, you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="510a1-116">Título Padrão</span><span class="sxs-lookup"><span data-stu-id="510a1-116">Standard Title</span></span>         | <span data-ttu-id="510a1-117">Unidade Organizacional</span><span class="sxs-lookup"><span data-stu-id="510a1-117">Org Unit</span></span>    |<span data-ttu-id="510a1-118">Unidade</span><span class="sxs-lookup"><span data-stu-id="510a1-118">Unit</span></span>   |<span data-ttu-id="510a1-119">Preço</span><span class="sxs-lookup"><span data-stu-id="510a1-119">Price</span></span>  |<span data-ttu-id="510a1-120">Moeda</span><span class="sxs-lookup"><span data-stu-id="510a1-120">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="510a1-121">Engenheiro de Sistemas</span><span class="sxs-lookup"><span data-stu-id="510a1-121">Systems Engineer</span></span>|<span data-ttu-id="510a1-122">Contoso EUA</span><span class="sxs-lookup"><span data-stu-id="510a1-122">Contoso US</span></span>|<span data-ttu-id="510a1-123">Hour</span><span class="sxs-lookup"><span data-stu-id="510a1-123">Hour</span></span>| <span data-ttu-id="510a1-124">100</span><span class="sxs-lookup"><span data-stu-id="510a1-124">100</span></span>|<span data-ttu-id="510a1-125">USD</span><span class="sxs-lookup"><span data-stu-id="510a1-125">USD</span></span>|
| <span data-ttu-id="510a1-126">Engenheiro de Sistemas Sénior</span><span class="sxs-lookup"><span data-stu-id="510a1-126">Senior Systems Engineer</span></span>|<span data-ttu-id="510a1-127">Contoso EUA</span><span class="sxs-lookup"><span data-stu-id="510a1-127">Contoso US</span></span>|<span data-ttu-id="510a1-128">Hour</span><span class="sxs-lookup"><span data-stu-id="510a1-128">Hour</span></span>| <span data-ttu-id="510a1-129">150</span><span class="sxs-lookup"><span data-stu-id="510a1-129">150</span></span>| <span data-ttu-id="510a1-130">USD</span><span class="sxs-lookup"><span data-stu-id="510a1-130">USD</span></span>|


<span data-ttu-id="510a1-131">Quando desativar o **Título Padrão** como a dimensão de definição de preços e o motor de definição de preços procurar um preço, só irá utilizar o valor **Unidade Organizacional** do contexto de entrada.</span><span class="sxs-lookup"><span data-stu-id="510a1-131">When you turn off **Standard Title** as the pricing dimension, and the pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="510a1-132">Se a **Unidade Organizacional** do contexto de entrada for "Contoso US", o resultado será não determinístico porque as duas linhas corresponderão.</span><span class="sxs-lookup"><span data-stu-id="510a1-132">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="510a1-133">Para evitar este cenário, quando cria registos de **Preço da Função**, o sistema valida que a combinação de dimensões é exclusiva.</span><span class="sxs-lookup"><span data-stu-id="510a1-133">To avoid this scenario, when you create **Role Price** records, the system validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="510a1-134">Se a dimensão for desativada após a criação dos registos de **Preço da Função**, esta restrição poderá ser violada.</span><span class="sxs-lookup"><span data-stu-id="510a1-134">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="510a1-135">Consequentemente, é necessário que, antes de desativar uma dimensão, elimine todas as linhas de **Preço da Função** e **Margem de Lucro do Preço da Função** que tenham esse valor de dimensão preenchido.</span><span class="sxs-lookup"><span data-stu-id="510a1-135">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>