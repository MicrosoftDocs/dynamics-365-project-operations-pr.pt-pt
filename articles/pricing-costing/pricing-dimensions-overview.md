---
title: Descrição geral das dimensões de preços
description: Este tópico fornece informações sobre as dimensões dos preços no Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 6b1ebdc97ec4704ba256acb521c0f2e7c474940b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082511"
---
# <a name="pricing-dimensions-overview"></a><span data-ttu-id="92b98-103">Descrição geral das dimensões de preços</span><span class="sxs-lookup"><span data-stu-id="92b98-103">Pricing dimensions overview</span></span>

<span data-ttu-id="92b98-104">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="92b98-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="92b98-105">As dimensões utilizadas nos recursos humanos para definir preços e custos enquadram-se em duas categorias:</span><span class="sxs-lookup"><span data-stu-id="92b98-105">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="92b98-106">Pessoas</span><span class="sxs-lookup"><span data-stu-id="92b98-106">People</span></span>
- <span data-ttu-id="92b98-107">Trabalho planeado</span><span class="sxs-lookup"><span data-stu-id="92b98-107">Planned work</span></span>

<span data-ttu-id="92b98-108">Por esse motivo, existem dois tipos de valores de dimensão de definição de preços disponíveis:</span><span class="sxs-lookup"><span data-stu-id="92b98-108">Because of this, there are two types of pricing dimension values available:</span></span>

- <span data-ttu-id="92b98-109">**Conjuntos de opções** : Dimensões que são enumerações fixas para um conjunto de valores.</span><span class="sxs-lookup"><span data-stu-id="92b98-109">**Option sets** : Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="92b98-110">**Valores baseados em entidades** : Dimensões que podem ser um conjunto de valores variado.</span><span class="sxs-lookup"><span data-stu-id="92b98-110">**Entity-based values** : Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="92b98-111">Dimensões de definição de preços</span><span class="sxs-lookup"><span data-stu-id="92b98-111">Pricing dimensions</span></span>

<span data-ttu-id="92b98-112">Dynamics 365 Project Operations envia com um conjunto padrão de dimensões de preços.</span><span class="sxs-lookup"><span data-stu-id="92b98-112">Dynamics 365 Project Operations ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="92b98-113">Pode visualizar estas dimensões de preços ao aceder a **Operações do projeto** > **Parâmetros**.</span><span class="sxs-lookup"><span data-stu-id="92b98-113">You can view these pricing dimensions by going to **Project Operations** > **Parameters**.</span></span> <span data-ttu-id="92b98-114">No registo de parâmetro, no separador **Dimensões de definição de preços baseadas em montantes** , verifique se a função, **msdyn_resourcecategory** e a unidade organizacional de atribuição de recursos, **msdyn_organizationalunit** têm os campos **Aplicável às vendas** e **Aplicável ao custo** definidos como **Sim**.</span><span class="sxs-lookup"><span data-stu-id="92b98-114">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="92b98-115">Com estes campos ativados, pode configurar o preço e o custo de cada combinação de função e unidade organizacional.</span><span class="sxs-lookup"><span data-stu-id="92b98-115">With these fields enabled, you can set up the price and cost for each role and organizational unit combination.</span></span>

<span data-ttu-id="92b98-116">Se precisar de definir o preço ou o custo dos seus recursos utilizando atributos adicionais, poderá criar campos, entidades e dimensões personalizados.</span><span class="sxs-lookup"><span data-stu-id="92b98-116">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span>

## <a name="pricing-human-resource-time"></a><span data-ttu-id="92b98-117">Definir preço do tempo dos recursos humanos</span><span class="sxs-lookup"><span data-stu-id="92b98-117">Pricing human resource time</span></span>
<span data-ttu-id="92b98-118">A forma como uma organização define o preço do tempo de um recurso humano é, normalmente, uma consideração estratégica importante que afeta diretamente a rentabilidade da organização.</span><span class="sxs-lookup"><span data-stu-id="92b98-118">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="92b98-119">Trabalhe com as equipas de finanças e pratique os chefes quando a sua organização estiver pronta para identificar como pretende definir taxas de faturação e custo para o tempo de recursos humanos.</span><span class="sxs-lookup"><span data-stu-id="92b98-119">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="92b98-120">As outras considerações para definição de preços incluem a reutilização de campos ou entidades que, no momento, não são dimensões de definição de preços, mas que se aplicam como uma dimensão de definição de preços para a sua organização.</span><span class="sxs-lookup"><span data-stu-id="92b98-120">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="92b98-121">Campos como **Categoria de Transação** ( **msdyn_transactioncategory** ) e **Recurso Reservável** ( **bookableresource** ) são exemplos de dimensões candidatas.</span><span class="sxs-lookup"><span data-stu-id="92b98-121">Fields like **Transaction Category** ( **msdyn_transactioncategory** ) and **Bookable Resource** ( **bookableresource** ) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="92b98-122">Considere se a dimensão de definição de preços deve ser uma tabela ou um conjunto de opções.</span><span class="sxs-lookup"><span data-stu-id="92b98-122">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="92b98-123">Se prever alterações nos valores de uma dimensão que excederão 10 ou 12 e necessitar de atributos adicionais nestes valores, poderá criar uma entidade em vez de um conjunto de opções.</span><span class="sxs-lookup"><span data-stu-id="92b98-123">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="92b98-124">A manutenção de um conjunto de opções, como a adição ou a remoção de valores, requer um administrador ou programador, ao passo que a adição de novas linhas a uma tabela pode ser efetuada pela maior parte dos utilizadores.</span><span class="sxs-lookup"><span data-stu-id="92b98-124">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="92b98-125">O exemplo que se segue mostra taxas de faturação que são configuradas com base na função e na unidade organizacional de atribuição de recursos à qual o recurso pertence.</span><span class="sxs-lookup"><span data-stu-id="92b98-125">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="92b98-126">Normalmente, as taxas de custo baseiam-se na faixa salarial do funcionário e na unidade organizacional à qual pertencem.</span><span class="sxs-lookup"><span data-stu-id="92b98-126">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="92b98-127">Neste exemplo, as tabelas de taxas de faturação e taxas de custo terão o seguinte aspeto:</span><span class="sxs-lookup"><span data-stu-id="92b98-127">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="92b98-128">**Taxas de faturação de exemplo**</span><span class="sxs-lookup"><span data-stu-id="92b98-128">**Sample bill rates**</span></span>

| <span data-ttu-id="92b98-129">Função</span><span class="sxs-lookup"><span data-stu-id="92b98-129">Role</span></span>        | <span data-ttu-id="92b98-130">Unidade Organizacional</span><span class="sxs-lookup"><span data-stu-id="92b98-130">Org Unit</span></span>    |<span data-ttu-id="92b98-131">Unidade</span><span class="sxs-lookup"><span data-stu-id="92b98-131">Unit</span></span>      |<span data-ttu-id="92b98-132">Preço</span><span class="sxs-lookup"><span data-stu-id="92b98-132">Price</span></span>      |<span data-ttu-id="92b98-133">Moeda</span><span class="sxs-lookup"><span data-stu-id="92b98-133">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="92b98-134">Programador</span><span class="sxs-lookup"><span data-stu-id="92b98-134">Developer</span></span>   | <span data-ttu-id="92b98-135">Contoso EUA</span><span class="sxs-lookup"><span data-stu-id="92b98-135">Contoso US</span></span>  |<span data-ttu-id="92b98-136">Hour</span><span class="sxs-lookup"><span data-stu-id="92b98-136">Hour</span></span> | <span data-ttu-id="92b98-137">200</span><span class="sxs-lookup"><span data-stu-id="92b98-137">200</span></span>|<span data-ttu-id="92b98-138">USD</span><span class="sxs-lookup"><span data-stu-id="92b98-138">USD</span></span>     |
| <span data-ttu-id="92b98-139">Programador</span><span class="sxs-lookup"><span data-stu-id="92b98-139">Developer</span></span>   | <span data-ttu-id="92b98-140">Contoso India</span><span class="sxs-lookup"><span data-stu-id="92b98-140">Contoso India</span></span> |<span data-ttu-id="92b98-141">Hour</span><span class="sxs-lookup"><span data-stu-id="92b98-141">Hour</span></span>|   <span data-ttu-id="92b98-142">112</span><span class="sxs-lookup"><span data-stu-id="92b98-142">112</span></span>|<span data-ttu-id="92b98-143">USD</span><span class="sxs-lookup"><span data-stu-id="92b98-143">USD</span></span>     |


<span data-ttu-id="92b98-144">**Exemplo de taxas de custo**</span><span class="sxs-lookup"><span data-stu-id="92b98-144">**Sample cost rates**</span></span>

| <span data-ttu-id="92b98-145">Faixa salarial</span><span class="sxs-lookup"><span data-stu-id="92b98-145">Salary Band</span></span>     | <span data-ttu-id="92b98-146">Unidade Organizacional</span><span class="sxs-lookup"><span data-stu-id="92b98-146">Org Unit</span></span>    |<span data-ttu-id="92b98-147">Unidade</span><span class="sxs-lookup"><span data-stu-id="92b98-147">Unit</span></span>      |<span data-ttu-id="92b98-148">Preço</span><span class="sxs-lookup"><span data-stu-id="92b98-148">Price</span></span>      |<span data-ttu-id="92b98-149">Moeda</span><span class="sxs-lookup"><span data-stu-id="92b98-149">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="92b98-150">A minha empresa_Faixa 1</span><span class="sxs-lookup"><span data-stu-id="92b98-150">My company_Band1</span></span> | <span data-ttu-id="92b98-151">Contoso EUA</span><span class="sxs-lookup"><span data-stu-id="92b98-151">Contoso US</span></span>  |<span data-ttu-id="92b98-152">Hour</span><span class="sxs-lookup"><span data-stu-id="92b98-152">Hour</span></span> | <span data-ttu-id="92b98-153">145</span><span class="sxs-lookup"><span data-stu-id="92b98-153">145</span></span>|<span data-ttu-id="92b98-154">USD</span><span class="sxs-lookup"><span data-stu-id="92b98-154">USD</span></span>     |
| <span data-ttu-id="92b98-155">A minha empresa_Faixa 2</span><span class="sxs-lookup"><span data-stu-id="92b98-155">My company_Band2</span></span> | <span data-ttu-id="92b98-156">Contoso India</span><span class="sxs-lookup"><span data-stu-id="92b98-156">Contoso India</span></span> |<span data-ttu-id="92b98-157">Hour</span><span class="sxs-lookup"><span data-stu-id="92b98-157">Hour</span></span>|   <span data-ttu-id="92b98-158">67</span><span class="sxs-lookup"><span data-stu-id="92b98-158">67</span></span>|<span data-ttu-id="92b98-159">USD</span><span class="sxs-lookup"><span data-stu-id="92b98-159">USD</span></span>     |
