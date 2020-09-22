---
title: Home page de dimensões de definição de preços e custos
description: Este tópico fornece uma descrição geral das dimensões de definição de preços.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 425d7bb8-9015-4f67-b9c9-cf3602e9afe8
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 2379d0d2e038f28a1a8df87a851e9bf7db7fe33f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754517"
---
# <a name="pricing-and-costing-dimensions-home-page"></a><span data-ttu-id="9626b-103">Home page de dimensões de definição de preços e custos</span><span class="sxs-lookup"><span data-stu-id="9626b-103">Pricing and costing dimensions home page</span></span>

<span data-ttu-id="9626b-104">As dimensões utilizadas nos recursos humanos para definir preços e custos enquadram-se em duas categorias:</span><span class="sxs-lookup"><span data-stu-id="9626b-104">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="9626b-105">Pessoas</span><span class="sxs-lookup"><span data-stu-id="9626b-105">People</span></span>
- <span data-ttu-id="9626b-106">Trabalho planeado</span><span class="sxs-lookup"><span data-stu-id="9626b-106">Planned work</span></span>

<span data-ttu-id="9626b-107">Por esse motivo, existem dois tipos de valores de dimensão de definição de preços disponíveis no Project Service Automation (PSA):</span><span class="sxs-lookup"><span data-stu-id="9626b-107">Because of this, there are two types of pricing dimension values available in Project Service Automation (PSA):</span></span> 

- <span data-ttu-id="9626b-108">**Conjuntos de opções** - Dimensões que são enumerações fixas para um conjunto de valores.</span><span class="sxs-lookup"><span data-stu-id="9626b-108">**Option sets** - Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="9626b-109">**Valores baseados em entidades** - Dimensões que podem ser um conjunto de valores variado.</span><span class="sxs-lookup"><span data-stu-id="9626b-109">**Entity-based values** - Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="9626b-110">Dimensões de definição de preços</span><span class="sxs-lookup"><span data-stu-id="9626b-110">Pricing dimensions</span></span>

<span data-ttu-id="9626b-111">O PSA é fornecido com um conjunto predefinido de dimensões de definição de preços.</span><span class="sxs-lookup"><span data-stu-id="9626b-111">PSA ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="9626b-112">Pode visualizá-lo acedendo a **Project Service** > **Parâmetros**.</span><span class="sxs-lookup"><span data-stu-id="9626b-112">You can view these by going to **Project Service** > **Parameters**.</span></span> <span data-ttu-id="9626b-113">No registo de parâmetro, no separador **Dimensões de definição de preços baseadas em montantes**, verifique se a função, **msdyn_resourcecategory** e a unidade organizacional de atribuição de recursos, **msdyn_organizationalunit** têm os campos **Aplicável às vendas** e **Aplicável ao custo** definidos como **Sim**.</span><span class="sxs-lookup"><span data-stu-id="9626b-113">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="9626b-114">Isto irá permitir-lhe configurar o preço e o custo de cada combinação de função e unidade organizacional.</span><span class="sxs-lookup"><span data-stu-id="9626b-114">This will allow you to set up the price and cost for each role and organizational unit combination.</span></span>

![Captura de ecrã dos parâmetros do Project Service com "Aplicável às Vendas" destacado](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> <span data-ttu-id="9626b-116">Se tiver utilizado os campos de função e unidade organizacional fornecidos com o programa como dimensões de definição de preços anteriores à versão 3 do PSA, não haverá nenhuma alteração observável.</span><span class="sxs-lookup"><span data-stu-id="9626b-116">If you have been the using out-of-the box fields of role and organizational unit as pricing dimensions prior to version 3 of PSA, there will not be any observable change.</span></span> <span data-ttu-id="9626b-117">Pode continuar a utilizar o Project Service normalmente.</span><span class="sxs-lookup"><span data-stu-id="9626b-117">You can continue to use Project Service as usual.</span></span> 

<span data-ttu-id="9626b-118">Se precisar de definir o preço ou o custo dos seus recursos utilizando atributos adicionais, poderá criar campos, entidades e dimensões personalizados.</span><span class="sxs-lookup"><span data-stu-id="9626b-118">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="9626b-119">Para mais informações, consulte os seguintes tópicos, no entanto, note que tem de concluir os procedimentos na ordem listada abaixo:</span><span class="sxs-lookup"><span data-stu-id="9626b-119">For more information, see the following topics, however note that you must complete the procedures in the order listed below:</span></span>

- [<span data-ttu-id="9626b-120">Criar campos e entidades personalizados</span><span class="sxs-lookup"><span data-stu-id="9626b-120">Create custom fields and entities</span></span>](create-custom-fields-entities.md)
- [<span data-ttu-id="9626b-121">Adicionar campos personalizados às entidades de configuração de preços e transacionais</span><span class="sxs-lookup"><span data-stu-id="9626b-121">Add custom fields to price setup and transactional entities</span></span>](field-references.md)
- [<span data-ttu-id="9626b-122">Configurar campos personalizados como dimensões de definição de preços</span><span class="sxs-lookup"><span data-stu-id="9626b-122">Set up custom fields as pricing dimensions</span></span>](set-up-pricing-dimensions.md)
- [<span data-ttu-id="9626b-123">Atualizar atributos de plug-in para incluir novas dimensões de definição de preços</span><span class="sxs-lookup"><span data-stu-id="9626b-123">Update plug-in attributes to include new pricing dimensions</span></span>](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a><span data-ttu-id="9626b-124">Definir preço do tempo dos recursos humanos</span><span class="sxs-lookup"><span data-stu-id="9626b-124">Pricing human resource time</span></span>
<span data-ttu-id="9626b-125">A forma como uma organização define o preço do tempo de um recurso humano é, normalmente, uma consideração estratégica importante que afeta diretamente a rentabilidade da organização.</span><span class="sxs-lookup"><span data-stu-id="9626b-125">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="9626b-126">Trabalhe com as equipas de finanças e pratique os chefes quando a sua organização estiver pronta para identificar como pretende definir taxas de faturação e custo para o tempo de recursos humanos.</span><span class="sxs-lookup"><span data-stu-id="9626b-126">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="9626b-127">As outras considerações para definição de preços incluem a reutilização de campos ou entidades que, no momento, não são dimensões de definição de preços, mas que se aplicam como uma dimensão de definição de preços para a sua organização.</span><span class="sxs-lookup"><span data-stu-id="9626b-127">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="9626b-128">Campos como **Categoria de Transação** (**msdyn_transactioncategory**) e **Recurso Reservável** (**bookableresource**) são exemplos de dimensões candidatas.</span><span class="sxs-lookup"><span data-stu-id="9626b-128">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="9626b-129">Também deve considerar se a dimensão de definição de preços deve ser uma tabela ou um conjunto de opções.</span><span class="sxs-lookup"><span data-stu-id="9626b-129">You should also consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="9626b-130">Se prever alterações nos valores de uma dimensão que excederão 10 ou 12 e necessitar de atributos adicionais nestes valores, poderá criar uma entidade em vez de um conjunto de opções.</span><span class="sxs-lookup"><span data-stu-id="9626b-130">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="9626b-131">A manutenção de um conjunto de opções, como a adição ou a remoção de valores, requer um administrador ou programador, ao passo que a adição de novas linhas a uma tabela pode ser efetuada pela maior parte dos utilizadores.</span><span class="sxs-lookup"><span data-stu-id="9626b-131">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="9626b-132">O exemplo que se segue mostra taxas de faturação que são configuradas com base na função e na unidade organizacional de atribuição de recursos à qual o recurso pertence.</span><span class="sxs-lookup"><span data-stu-id="9626b-132">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="9626b-133">Normalmente, as taxas de custo baseiam-se na faixa salarial do funcionário e na unidade organizacional à qual pertencem.</span><span class="sxs-lookup"><span data-stu-id="9626b-133">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="9626b-134">Neste exemplo, as tabelas de taxas de faturação e taxas de custo terão o seguinte aspeto:</span><span class="sxs-lookup"><span data-stu-id="9626b-134">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="9626b-135">**Taxas de faturação de exemplo**</span><span class="sxs-lookup"><span data-stu-id="9626b-135">**Sample bill rates**</span></span>

| <span data-ttu-id="9626b-136">Função</span><span class="sxs-lookup"><span data-stu-id="9626b-136">Role</span></span>        | <span data-ttu-id="9626b-137">Unidade Organizacional</span><span class="sxs-lookup"><span data-stu-id="9626b-137">Org Unit</span></span>    |<span data-ttu-id="9626b-138">Unidade</span><span class="sxs-lookup"><span data-stu-id="9626b-138">Unit</span></span>      |<span data-ttu-id="9626b-139">Preço</span><span class="sxs-lookup"><span data-stu-id="9626b-139">Price</span></span>      |<span data-ttu-id="9626b-140">Moeda</span><span class="sxs-lookup"><span data-stu-id="9626b-140">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="9626b-141">Programador</span><span class="sxs-lookup"><span data-stu-id="9626b-141">Developer</span></span>   | <span data-ttu-id="9626b-142">Contoso EUA</span><span class="sxs-lookup"><span data-stu-id="9626b-142">Contoso US</span></span>  |<span data-ttu-id="9626b-143">Hour</span><span class="sxs-lookup"><span data-stu-id="9626b-143">Hour</span></span> | <span data-ttu-id="9626b-144">200</span><span class="sxs-lookup"><span data-stu-id="9626b-144">200</span></span>|<span data-ttu-id="9626b-145">USD</span><span class="sxs-lookup"><span data-stu-id="9626b-145">USD</span></span>     |
| <span data-ttu-id="9626b-146">Programador</span><span class="sxs-lookup"><span data-stu-id="9626b-146">Developer</span></span>   | <span data-ttu-id="9626b-147">Contoso India</span><span class="sxs-lookup"><span data-stu-id="9626b-147">Contoso India</span></span> |<span data-ttu-id="9626b-148">Hour</span><span class="sxs-lookup"><span data-stu-id="9626b-148">Hour</span></span>|   <span data-ttu-id="9626b-149">112</span><span class="sxs-lookup"><span data-stu-id="9626b-149">112</span></span>|<span data-ttu-id="9626b-150">USD</span><span class="sxs-lookup"><span data-stu-id="9626b-150">USD</span></span>     |


<span data-ttu-id="9626b-151">**Exemplo de taxas de custo**</span><span class="sxs-lookup"><span data-stu-id="9626b-151">**Sample cost rates**</span></span>

| <span data-ttu-id="9626b-152">Faixa salarial</span><span class="sxs-lookup"><span data-stu-id="9626b-152">Salary Band</span></span>     | <span data-ttu-id="9626b-153">Unidade Organizacional</span><span class="sxs-lookup"><span data-stu-id="9626b-153">Org Unit</span></span>    |<span data-ttu-id="9626b-154">Unidade</span><span class="sxs-lookup"><span data-stu-id="9626b-154">Unit</span></span>      |<span data-ttu-id="9626b-155">Preço</span><span class="sxs-lookup"><span data-stu-id="9626b-155">Price</span></span>      |<span data-ttu-id="9626b-156">Moeda</span><span class="sxs-lookup"><span data-stu-id="9626b-156">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="9626b-157">A minha empresa_Faixa 1</span><span class="sxs-lookup"><span data-stu-id="9626b-157">My company_Band1</span></span> | <span data-ttu-id="9626b-158">Contoso EUA</span><span class="sxs-lookup"><span data-stu-id="9626b-158">Contoso US</span></span>  |<span data-ttu-id="9626b-159">Hour</span><span class="sxs-lookup"><span data-stu-id="9626b-159">Hour</span></span> | <span data-ttu-id="9626b-160">145</span><span class="sxs-lookup"><span data-stu-id="9626b-160">145</span></span>|<span data-ttu-id="9626b-161">USD</span><span class="sxs-lookup"><span data-stu-id="9626b-161">USD</span></span>     |
| <span data-ttu-id="9626b-162">A minha empresa_Faixa 2</span><span class="sxs-lookup"><span data-stu-id="9626b-162">My company_Band2</span></span> | <span data-ttu-id="9626b-163">Contoso India</span><span class="sxs-lookup"><span data-stu-id="9626b-163">Contoso India</span></span> |<span data-ttu-id="9626b-164">Hour</span><span class="sxs-lookup"><span data-stu-id="9626b-164">Hour</span></span>|   <span data-ttu-id="9626b-165">67</span><span class="sxs-lookup"><span data-stu-id="9626b-165">67</span></span>|<span data-ttu-id="9626b-166">USD</span><span class="sxs-lookup"><span data-stu-id="9626b-166">USD</span></span>     |
