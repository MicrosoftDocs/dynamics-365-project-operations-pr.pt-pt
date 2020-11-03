---
title: Porque é que o preço padrão é zero em custos de valores reais?
description: Resolução de problemas de porque é que o preço padrão é 0 para custos de valores reais.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 44d4952b77ac0a541cdf8e3e55f202c9209efdf4
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082423"
---
# <a name="why-is-the-price-defaulting-to-zero-on-time-cost-actuals"></a><span data-ttu-id="f20be-103">Porque é que o preço padrão é zero em custos de valores reais?</span><span class="sxs-lookup"><span data-stu-id="f20be-103">Why is the price defaulting to zero on time cost actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="f20be-104">Este FAQ é aplicável aos valores reais onde a classe de transação está definida como Tempo e tipo de transação como Custos.</span><span class="sxs-lookup"><span data-stu-id="f20be-104">This FAQ applies to actuals where the transaction class is set to Time and transaction type is Cost.</span></span> <span data-ttu-id="f20be-105">As seguintes três verificações irão ajudá-lo a resolver o motivo pelo qual os preços estão como padrão a 0 para custos em valores reais.</span><span class="sxs-lookup"><span data-stu-id="f20be-105">The following three checks will help you troubleshoot why the price is defaulting to 0 on time cost actuals.</span></span>
 
## <a name="check-1-identify-the-cost-price-list-for-the-project"></a><span data-ttu-id="f20be-106">Verificação 1: identificar a lista de preços de custos do projeto</span><span class="sxs-lookup"><span data-stu-id="f20be-106">Check 1: Identify the cost price list for the project</span></span>

<span data-ttu-id="f20be-107">Localize o projeto no campo do projeto e, em seguida, aceda à página do projeto.</span><span class="sxs-lookup"><span data-stu-id="f20be-107">Find the project from the project field of the actual and then go to the project page.</span></span> <span data-ttu-id="f20be-108">Clique na hiperligação de unidade de contratação no campo.</span><span class="sxs-lookup"><span data-stu-id="f20be-108">Click on the contracting unit link in the field.</span></span> <span data-ttu-id="f20be-109">Na página Unidade de Contratação, verifique se a unidade de contratação tem uma lista de preços na grelha de Listas de Preços de Custos.</span><span class="sxs-lookup"><span data-stu-id="f20be-109">On the Contracting Unit page, check if the contracting unit has a price list in the Cost Price Lists grid.</span></span>

<span data-ttu-id="f20be-110">Se existir mais de uma lista de preços, localizou o problema.</span><span class="sxs-lookup"><span data-stu-id="f20be-110">If there is more than one price list, you have isolated the problem.</span></span> <span data-ttu-id="f20be-111">O Project Service suporta apenas uma lista de preços por unidade organizacional.</span><span class="sxs-lookup"><span data-stu-id="f20be-111">Project Service only supports one price list per organizational unit.</span></span> <span data-ttu-id="f20be-112">Remova todas as listas de preços desta entidade até que exista apenas uma lista de preços anexada na grelha de Listas de Preços de Custo da Unidade Organizacional.</span><span class="sxs-lookup"><span data-stu-id="f20be-112">Remove all prices lists from this entity until there is only one price list attached in the Cost Price Lists grid of the Organizational Unit.</span></span>

<span data-ttu-id="f20be-113">Se não houver nenhuma lista de preços anexada à Unidade Organizacional, tome nota da moeda da Unidade organizacional.</span><span class="sxs-lookup"><span data-stu-id="f20be-113">If there are no price lists attached to the Organizational Unit, make a note of the currency of the Organizational unit.</span></span> <span data-ttu-id="f20be-114">Aceda ao Project Service e, em seguida, vá a Parâmetros e abra o separador Listas de Preços. Verifique se existem listas de preços com contexto definido como Custo e moeda que corresponde à da Unidade Organizacional.</span><span class="sxs-lookup"><span data-stu-id="f20be-114">Go to the Project Service and then Parameters and open the Price Lists tab. Check if there are any price lists with context set to Cost and currency that matches the currency of the Organizational Unit.</span></span>
 
<span data-ttu-id="f20be-115">Se não houver nenhuma lista de preços que corresponda a esses critérios, localizou o problema.</span><span class="sxs-lookup"><span data-stu-id="f20be-115">If there are no price lists that match that criteria, you have isolated the problem.</span></span> <span data-ttu-id="f20be-116">Certifique-se de que tem, pelo menos, uma lista de preços cujo contexto está definido como Custo e cuja moeda corresponde à da Unidade Organizacional.</span><span class="sxs-lookup"><span data-stu-id="f20be-116">Make sure to have at least one price list whose context is set to Cost and whose currency matches the currency of the Organizational Unit.</span></span>

<span data-ttu-id="f20be-117">Se existir mais de uma lista de preços que correspondam a esses critérios, continue a ler este documento para efetuar mais verificações.</span><span class="sxs-lookup"><span data-stu-id="f20be-117">If there is more than one price list that match that criteria, continue reading this document to make more checks.</span></span>

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-cost-actual"></a><span data-ttu-id="f20be-118">Verificação 2: qualquer uma das listas de preços identificadas acima é válida para a data específica dos custos em valores reais?</span><span class="sxs-lookup"><span data-stu-id="f20be-118">Check 2: Are any of the price lists identified above valid for the specific date of the time cost actual?</span></span>

<span data-ttu-id="f20be-119">Para o Project Service ter em consideração uma lista de preços para o preço padrão, essa lista de preços deve ser aplicável para a data nos custos em valores reais.</span><span class="sxs-lookup"><span data-stu-id="f20be-119">For Project Service to consider a price list for defaulting price, that price list should be applicable for the date on the time cost actual.</span></span> <span data-ttu-id="f20be-120">Verifique o seguinte para ver se a(s) lista(s) de preços identificada(s) acima é/são aplicável(eis):</span><span class="sxs-lookup"><span data-stu-id="f20be-120">Check the following to see if the price list(s) identified above are applicable:</span></span>

- <span data-ttu-id="f20be-121">Verifique se as datas de início e de fim do separador geral para as listas de preços associadas não estão vazias.</span><span class="sxs-lookup"><span data-stu-id="f20be-121">Check if the start and end dates on the general tab for the price lists attached aren’t empty.</span></span> <span data-ttu-id="f20be-122">Se as datas de início e de fim das listas de preços identificadas acima estão vazias, localizou o problema.</span><span class="sxs-lookup"><span data-stu-id="f20be-122">If the start and end dates on price lists identified above are empty, you have isolated the problem.</span></span> 
- <span data-ttu-id="f20be-123">Anote o campo de data de início nos seus custos em valores reais e verifique se qualquer uma das listas de preços identificadas é aplicável para essa data.</span><span class="sxs-lookup"><span data-stu-id="f20be-123">Make a note of the start date field on your time cost actual and check if any of the price lists identified is applicable for that date.</span></span> <span data-ttu-id="f20be-124">Por exemplo, a data de custos em valores reais deve estar dentro da data de início e data de fim na lista de preços.</span><span class="sxs-lookup"><span data-stu-id="f20be-124">For example, the date of the time cost actual should fall within the start date and end date on the price list.</span></span> 
    - <span data-ttu-id="f20be-125">Se não houver nenhuma lista de preços que abranja essa data nos custos em valores reais, localizou o problema.</span><span class="sxs-lookup"><span data-stu-id="f20be-125">If there is no price list that covers that date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="f20be-126">Modifique as datas de início e de fim da lista de preços para assegurar que a lista de preços abrange a data de custos em valores reais.</span><span class="sxs-lookup"><span data-stu-id="f20be-126">Modify the start and end dates of the price list to ensure that the price list covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="f20be-127">Se houver mais do que uma lista de preços que abranja essa data nos custos em valores reais, localizou o problema.</span><span class="sxs-lookup"><span data-stu-id="f20be-127">If there is more than one price list that covers the date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="f20be-128">Pode corrigir isto editando as datas de início e de fim da(s) lista(s) de preços para que exista apenas uma lista de preços que abranja a data de custos em valores reais.</span><span class="sxs-lookup"><span data-stu-id="f20be-128">You can fix this by editing the start and end dates of the price list(s) so that there is only one price list that covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="f20be-129">Se tiver apenas uma lista de preços que abrange essa data do custo de tempo em valores reais, mova para a verificação seguinte no documento.</span><span class="sxs-lookup"><span data-stu-id="f20be-129">If there is only one price list that covers that date of the time cost actual, move to the next check in the document.</span></span>
<span data-ttu-id="f20be-130">Depois de efetuadas as correções necessárias, recrie a entrada de tempo, aprove-a e verifique se os custos em valores reais mostram um preço válido.</span><span class="sxs-lookup"><span data-stu-id="f20be-130">Once you’ve done made the required fixes, recreate a time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-cost-actual"></a><span data-ttu-id="f20be-131">Verificação 3: existe um preço na lista de preços para as dimensões de preços nos custos em valores reais?</span><span class="sxs-lookup"><span data-stu-id="f20be-131">Check 3: Is there a price in the price list for the pricing dimensions on the time cost actual?</span></span>

<span data-ttu-id="f20be-132">Se tiver concluído com êxito a Verificação 1 e 2, deverá agora ter apenas uma lista de preços que é aplicável para a data de custos em valores reais.</span><span class="sxs-lookup"><span data-stu-id="f20be-132">If you have successfully completed Check 1 and Check 2, you should now have only one price list that is applicable for the date of the time cost actual.</span></span> <span data-ttu-id="f20be-133">Abra a Lista de Preços e vá para o separador de Preços de Função. Certifique-se de que existe uma linha na grelha para as dimensões de preços no custo de tempo em valores reais.</span><span class="sxs-lookup"><span data-stu-id="f20be-133">Open this Price List and go to the Role Prices tab. Make sure that there is a row in the grid for the pricing dimensions on the time cost actual.</span></span>

<span data-ttu-id="f20be-134">Se não houver nenhuma linha na grelha de preços para as dimensões de preço nos custos em valores reais, então, localizou o problema.</span><span class="sxs-lookup"><span data-stu-id="f20be-134">If there is no row in the role price grid for the pricing dimensions on the time cost actual, then you have isolated the problem.</span></span> <span data-ttu-id="f20be-135">Crie uma linha na grelha de Preços de funções para as dimensões de preço nos seus custos em valores reais.</span><span class="sxs-lookup"><span data-stu-id="f20be-135">Create a row in the Role prices grid for the pricing dimensions on your time cost actual.</span></span> <span data-ttu-id="f20be-136">Feito isto, recrie a entrada de tempo, aprove-a e verifique se os custos em valores reais mostram um preço válido.</span><span class="sxs-lookup"><span data-stu-id="f20be-136">Once this is done, recreate time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>
 
<span data-ttu-id="f20be-137">Se ainda não visualizar um preço válido nas seus custos de valores reais depois de seguir as três verificações acima, submeta um pedido de suporte.</span><span class="sxs-lookup"><span data-stu-id="f20be-137">If you still don't see a valid price on your time cost actual after you’ve done the three checks above, please log a support ticket.</span></span>



