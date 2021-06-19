---
title: Desativar uma dimensão de definição de preços
description: Este tópico mostra como configurar dimensões de definição de preços na solução do Project Service.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: da8615fa147838d9088c639039d5a2534e662e82
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014310"
---
# <a name="turn-off-a-pricing-dimension"></a><span data-ttu-id="44b6d-103">Desativar uma dimensão de definição de preços</span><span class="sxs-lookup"><span data-stu-id="44b6d-103">Turn off a pricing dimension</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="44b6d-104">Poderá ter de analisar e atualizar a sua estratégia de definição de preços a cada ano.</span><span class="sxs-lookup"><span data-stu-id="44b6d-104">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="44b6d-105">Quaisquer atualizações feitas podem exigir que desative uma dimensão de definição de preços existente e crie uma nova.</span><span class="sxs-lookup"><span data-stu-id="44b6d-105">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="44b6d-106">Por exemplo, poderá ter de definir o preço anteriormente por **Função**, mas agora decidiu definir o preço por **Experiência de Trabalho**.</span><span class="sxs-lookup"><span data-stu-id="44b6d-106">For example, you may have previously priced by **Role**, but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="44b6d-107">Isto poderá fazer com que seja necessário desativar a **Função** como uma dimensão de definição de preços e criar uma **Experiência de Trabalho** como uma nova dimensão de definição de preços.</span><span class="sxs-lookup"><span data-stu-id="44b6d-107">This may require you to turn off **Role** as a pricing dimension and create **Work Expereince** as a new pricing dimension.</span></span> 

<span data-ttu-id="44b6d-108">A desativação de uma dimensão de definição de preços, independentemente de a mesma ser fornecida com o programa ou personalizada, pode ser efetuada definindo os campos **Aplicável ao Custo** e **Aplicável às Vendas** da Dimensão de Definição de Preços como **Não**.</span><span class="sxs-lookup"><span data-stu-id="44b6d-108">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="44b6d-109">No entanto, ao fazê-lo, poderá receber a seguinte mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="44b6d-109">However, when you do this, you might receive the following error message.</span></span>

![É provável que haja um erro no processo de negócio ao desativar uma dimensão de definição de preços](media/Business-Process-Error.png)


<span data-ttu-id="44b6d-111">Esta mensagem de erro indica que existem registos de preços configurados anteriormente para a dimensão que está a ser desativada.</span><span class="sxs-lookup"><span data-stu-id="44b6d-111">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="44b6d-112">Todos os registos **Preço da Função** e **Margem de Lucro do Preço da Função** que façam referência a uma dimensão têm de ser eliminados antes de a aplicabilidade da dimensão poder ser definida como **Não**.</span><span class="sxs-lookup"><span data-stu-id="44b6d-112">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="44b6d-113">Esta regra aplica-se às dimensões de definição de preços fornecidas com o programa e a quaisquer dimensões de definição de preços personalizadas que possa ter criado.</span><span class="sxs-lookup"><span data-stu-id="44b6d-113">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="44b6d-114">O motivo dessa validação é porque o Project Service tem uma restrição de que cada registo **Preço da Função** deve ter uma combinação exclusiva de dimensões.</span><span class="sxs-lookup"><span data-stu-id="44b6d-114">The reason for this validation is because Project Service has a constraint that each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="44b6d-115">Por exemplo, numa lista de preços denominada **Taxas de custo nos EUA 2018**, tem as seguintes linhas de **Preço da Função**.</span><span class="sxs-lookup"><span data-stu-id="44b6d-115">For example, on a price list called **US Cost Rates 2018**, you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="44b6d-116">Título Padrão</span><span class="sxs-lookup"><span data-stu-id="44b6d-116">Standard Title</span></span>         | <span data-ttu-id="44b6d-117">Unidade Organizacional</span><span class="sxs-lookup"><span data-stu-id="44b6d-117">Org Unit</span></span>    |<span data-ttu-id="44b6d-118">Unidade</span><span class="sxs-lookup"><span data-stu-id="44b6d-118">Unit</span></span>   |<span data-ttu-id="44b6d-119">Preço</span><span class="sxs-lookup"><span data-stu-id="44b6d-119">Price</span></span>  |<span data-ttu-id="44b6d-120">Moeda</span><span class="sxs-lookup"><span data-stu-id="44b6d-120">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="44b6d-121">Engenheiro de Sistemas</span><span class="sxs-lookup"><span data-stu-id="44b6d-121">Systems Engineer</span></span>|<span data-ttu-id="44b6d-122">Contoso E.U.A.</span><span class="sxs-lookup"><span data-stu-id="44b6d-122">Contoso US</span></span>|<span data-ttu-id="44b6d-123">Hora</span><span class="sxs-lookup"><span data-stu-id="44b6d-123">Hour</span></span>| <span data-ttu-id="44b6d-124">100</span><span class="sxs-lookup"><span data-stu-id="44b6d-124">100</span></span>|<span data-ttu-id="44b6d-125">USD</span><span class="sxs-lookup"><span data-stu-id="44b6d-125">USD</span></span>|
| <span data-ttu-id="44b6d-126">Engenheiro de Sistemas Sénior</span><span class="sxs-lookup"><span data-stu-id="44b6d-126">Senior Systems Engineer</span></span>|<span data-ttu-id="44b6d-127">Contoso E.U.A.</span><span class="sxs-lookup"><span data-stu-id="44b6d-127">Contoso US</span></span>|<span data-ttu-id="44b6d-128">Hora</span><span class="sxs-lookup"><span data-stu-id="44b6d-128">Hour</span></span>| <span data-ttu-id="44b6d-129">235</span><span class="sxs-lookup"><span data-stu-id="44b6d-129">150</span></span>| <span data-ttu-id="44b6d-130">USD</span><span class="sxs-lookup"><span data-stu-id="44b6d-130">USD</span></span>|


<span data-ttu-id="44b6d-131">Quando desativar o **Título Padrão** como a dimensão de definição de preços e o motor de definição de preços do Project Service procurar um preço, só irá utilizar o valor **Unidade Organizacional** do contexto de entrada.</span><span class="sxs-lookup"><span data-stu-id="44b6d-131">When you turn off **Standard Title** as the pricing dimension, and the Project Service pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="44b6d-132">Se a **Unidade Organizacional** do contexto de entrada for "Contoso US", o resultado será não determinístico porque as duas linhas corresponderão.</span><span class="sxs-lookup"><span data-stu-id="44b6d-132">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="44b6d-133">Para evitar este cenário, quando cria registos de **Preço da Função**, o Project Service valida que a combinação de dimensões é exclusiva.</span><span class="sxs-lookup"><span data-stu-id="44b6d-133">To avoid this scenario, when you create **Role Price** records, Project Service validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="44b6d-134">Se a dimensão for desativada após a criação dos registos de **Preço da Função**, esta restrição poderá ser violada.</span><span class="sxs-lookup"><span data-stu-id="44b6d-134">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="44b6d-135">Consequentemente, é necessário que, antes de desativar uma dimensão, elimine todas as linhas de **Preço da Função** e **Margem de Lucro do Preço da Função** que tenham esse valor de dimensão preenchido.</span><span class="sxs-lookup"><span data-stu-id="44b6d-135">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]