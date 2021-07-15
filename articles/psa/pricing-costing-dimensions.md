---
title: Home page de dimensões de definição de preços e custos
description: Este tópico fornece uma descrição geral das dimensões de definição de preços.
author: rumant
ms.custom:
- dyn365-projectservice
- intro-internal
ms.date: 10/01/2020
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
ms.openlocfilehash: 5c8c28839f5e7b3259afbea4ab400d0c4fca95fd
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368895"
---
# <a name="pricing-and-costing-dimensions-home-page"></a><span data-ttu-id="cee59-103">Home page de dimensões de definição de preços e custos</span><span class="sxs-lookup"><span data-stu-id="cee59-103">Pricing and costing dimensions home page</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="cee59-104">As dimensões utilizadas para definir os preços do trabalho e os custos em organizações baseadas em projetos são influenciadas pelos seguintes atributos:</span><span class="sxs-lookup"><span data-stu-id="cee59-104">The dimensions used to set labor pricing and costing in project-based organizations are influenced by the following attributes:</span></span>

- <span data-ttu-id="cee59-105">Pessoas com trabalho semelhante à sua experiência, função ou geografia</span><span class="sxs-lookup"><span data-stu-id="cee59-105">People doing work similar to their experience, role, or geography</span></span>
- <span data-ttu-id="cee59-106">Trabalho a realizar semelhante à sua complexidade ou hora do dia</span><span class="sxs-lookup"><span data-stu-id="cee59-106">Work to be performed similar to its complexity or time of day</span></span>

<span data-ttu-id="cee59-107">Dada a natureza típica destes attrubutes do trabalho e das pessoas necessárias para realizar o trabalho, existem dois tipos de valores de dimensão de preços disponíveis no Project Service Automation:</span><span class="sxs-lookup"><span data-stu-id="cee59-107">Given the typical nature of these attrubutes of the work and the people required to perform the work, there are two types of pricing dimension values available in Project Service Automation:</span></span> 

- <span data-ttu-id="cee59-108">**Conjuntos de opções** – atributos que são enumerações fixas para um conjunto de valores.</span><span class="sxs-lookup"><span data-stu-id="cee59-108">**Option sets** - Attributes that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="cee59-109">**Valores baseados em entidades** – atributos que podem ter um conjunto de valores variado que são finitos mas podem mudar ao longo do tempo.</span><span class="sxs-lookup"><span data-stu-id="cee59-109">**Entity-based values** - Attributes that can have a varied set of values that are finite but can change over time.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="cee59-110">Dimensões de preços</span><span class="sxs-lookup"><span data-stu-id="cee59-110">Pricing dimensions</span></span>

<span data-ttu-id="cee59-111">O PSA é fornecido com um conjunto predefinido de dimensões de definição de preços.</span><span class="sxs-lookup"><span data-stu-id="cee59-111">PSA ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="cee59-112">Pode visualizá-lo acedendo a **Project Service** > **Parâmetros**.</span><span class="sxs-lookup"><span data-stu-id="cee59-112">You can view these by going to **Project Service** > **Parameters**.</span></span> <span data-ttu-id="cee59-113">No registo de parâmetro, no separador **Dimensões de definição de preços baseadas em montantes**, verifique se a função, **msdyn_resourcecategory** e a unidade organizacional de atribuição de recursos, **msdyn_organizationalunit** têm os campos **Aplicável às vendas** e **Aplicável ao custo** definidos como **Sim**.</span><span class="sxs-lookup"><span data-stu-id="cee59-113">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="cee59-114">Isto irá permitir-lhe configurar o preço e o custo de cada combinação de função e unidade organizacional.</span><span class="sxs-lookup"><span data-stu-id="cee59-114">This will allow you to set up the price and cost for each role and organizational unit combination.</span></span>

![Captura de ecrã dos parâmetros do Project Service com "Aplicável às Vendas" destacado](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> <span data-ttu-id="cee59-116">Se tiver utilizado os campos de função e unidade organizacional fornecidos com o programa como dimensões de definição de preços anteriores à versão 3 do PSA, não haverá nenhuma alteração observável.</span><span class="sxs-lookup"><span data-stu-id="cee59-116">If you have been the using out-of-the box fields of role and organizational unit as pricing dimensions prior to version 3 of PSA, there will not be any observable change.</span></span> <span data-ttu-id="cee59-117">Pode continuar a utilizar o Project Service normalmente.</span><span class="sxs-lookup"><span data-stu-id="cee59-117">You can continue to use Project Service as usual.</span></span> 

<span data-ttu-id="cee59-118">Se precisar de definir o preço ou o custo dos seus recursos utilizando atributos adicionais, poderá criar campos, entidades e dimensões personalizados.</span><span class="sxs-lookup"><span data-stu-id="cee59-118">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="cee59-119">Para mais informações, consulte os seguintes tópicos, no entanto, note que tem de concluir os procedimentos na ordem listada abaixo:</span><span class="sxs-lookup"><span data-stu-id="cee59-119">For more information, see the following topics, however note that you must complete the procedures in the order listed below:</span></span>

- [<span data-ttu-id="cee59-120">Criar campos e entidades personalizados</span><span class="sxs-lookup"><span data-stu-id="cee59-120">Create custom fields and entities</span></span>](create-custom-fields-entities.md)
- [<span data-ttu-id="cee59-121">Adicionar campos personalizados às entidades de configuração de preços e transacionais</span><span class="sxs-lookup"><span data-stu-id="cee59-121">Add custom fields to price setup and transactional entities</span></span>](field-references.md)
- [<span data-ttu-id="cee59-122">Configurar campos personalizados como dimensões de definição de preços</span><span class="sxs-lookup"><span data-stu-id="cee59-122">Set up custom fields as pricing dimensions</span></span>](set-up-pricing-dimensions.md)
- [<span data-ttu-id="cee59-123">Atualizar atributos de plug-in para incluir novas dimensões de definição de preços</span><span class="sxs-lookup"><span data-stu-id="cee59-123">Update plug-in attributes to include new pricing dimensions</span></span>](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a><span data-ttu-id="cee59-124">Definir preço do tempo dos recursos humanos</span><span class="sxs-lookup"><span data-stu-id="cee59-124">Pricing human resource time</span></span>
<span data-ttu-id="cee59-125">A forma como uma organização define o preço do tempo de um recurso humano é, normalmente, uma consideração estratégica importante que afeta diretamente a rentabilidade da organização.</span><span class="sxs-lookup"><span data-stu-id="cee59-125">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="cee59-126">Trabalhe com as equipas de finanças e pratique os chefes quando a sua organização estiver pronta para identificar como pretende definir taxas de faturação e custo para o tempo de recursos humanos.</span><span class="sxs-lookup"><span data-stu-id="cee59-126">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="cee59-127">As outras considerações para definição de preços incluem a reutilização de campos ou entidades que, no momento, não são dimensões de definição de preços, mas que se aplicam como uma dimensão de definição de preços para a sua organização.</span><span class="sxs-lookup"><span data-stu-id="cee59-127">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="cee59-128">Campos como **Categoria de Transação** (**msdyn_transactioncategory**) e **Recurso Reservável** (**bookableresource**) são exemplos de dimensões candidatas.</span><span class="sxs-lookup"><span data-stu-id="cee59-128">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="cee59-129">Considere se a dimensão de definição de preços deve ser uma tabela ou um conjunto de opções.</span><span class="sxs-lookup"><span data-stu-id="cee59-129">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="cee59-130">Se prever alterações nos valores de uma dimensão que excederão 10 ou 12 e necessitar de atributos adicionais nestes valores, criar uma entidade em vez de um conjunto de opções.</span><span class="sxs-lookup"><span data-stu-id="cee59-130">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, create an entity rather than an option set.</span></span> <span data-ttu-id="cee59-131">A manutenção de um conjunto de opções, como a adição ou a remoção de valores, requer um administrador ou programador, ao passo que a adição de novas linhas a uma tabela pode ser efetuada pela maior parte dos utilizadores empresariais.</span><span class="sxs-lookup"><span data-stu-id="cee59-131">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most business users.</span></span>

<span data-ttu-id="cee59-132">O exemplo que se segue mostra taxas de faturação que são configuradas com base na função e na unidade organizacional de atribuição de recursos à qual o recurso pertence.</span><span class="sxs-lookup"><span data-stu-id="cee59-132">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="cee59-133">Normalmente, as taxas de custo baseiam-se na faixa salarial do funcionário e na unidade organizacional à qual pertencem.</span><span class="sxs-lookup"><span data-stu-id="cee59-133">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="cee59-134">Neste exemplo, as tabelas de taxas de faturação e taxas de custo terão o seguinte aspeto:</span><span class="sxs-lookup"><span data-stu-id="cee59-134">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="cee59-135">**Taxas de faturação de exemplo**</span><span class="sxs-lookup"><span data-stu-id="cee59-135">**Sample bill rates**</span></span>

| <span data-ttu-id="cee59-136">Função</span><span class="sxs-lookup"><span data-stu-id="cee59-136">Role</span></span>        | <span data-ttu-id="cee59-137">Unidade Organizacional</span><span class="sxs-lookup"><span data-stu-id="cee59-137">Org Unit</span></span>    |<span data-ttu-id="cee59-138">Unidade</span><span class="sxs-lookup"><span data-stu-id="cee59-138">Unit</span></span>      |<span data-ttu-id="cee59-139">Preço</span><span class="sxs-lookup"><span data-stu-id="cee59-139">Price</span></span>      |<span data-ttu-id="cee59-140">Moeda</span><span class="sxs-lookup"><span data-stu-id="cee59-140">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="cee59-141">Programador</span><span class="sxs-lookup"><span data-stu-id="cee59-141">Developer</span></span>   | <span data-ttu-id="cee59-142">Contoso E.U.A.</span><span class="sxs-lookup"><span data-stu-id="cee59-142">Contoso US</span></span>  |<span data-ttu-id="cee59-143">Hora</span><span class="sxs-lookup"><span data-stu-id="cee59-143">Hour</span></span> | <span data-ttu-id="cee59-144">200</span><span class="sxs-lookup"><span data-stu-id="cee59-144">200</span></span>|<span data-ttu-id="cee59-145">USD</span><span class="sxs-lookup"><span data-stu-id="cee59-145">USD</span></span>     |
| <span data-ttu-id="cee59-146">Programador</span><span class="sxs-lookup"><span data-stu-id="cee59-146">Developer</span></span>   | <span data-ttu-id="cee59-147">Contoso India</span><span class="sxs-lookup"><span data-stu-id="cee59-147">Contoso India</span></span> |<span data-ttu-id="cee59-148">Hora</span><span class="sxs-lookup"><span data-stu-id="cee59-148">Hour</span></span>|   <span data-ttu-id="cee59-149">112</span><span class="sxs-lookup"><span data-stu-id="cee59-149">112</span></span>|<span data-ttu-id="cee59-150">USD</span><span class="sxs-lookup"><span data-stu-id="cee59-150">USD</span></span>     |


<span data-ttu-id="cee59-151">**Exemplo de taxas de custo**</span><span class="sxs-lookup"><span data-stu-id="cee59-151">**Sample cost rates**</span></span>

| <span data-ttu-id="cee59-152">Faixa salarial</span><span class="sxs-lookup"><span data-stu-id="cee59-152">Salary Band</span></span>     | <span data-ttu-id="cee59-153">Unidade Organizacional</span><span class="sxs-lookup"><span data-stu-id="cee59-153">Org Unit</span></span>    |<span data-ttu-id="cee59-154">Unidade</span><span class="sxs-lookup"><span data-stu-id="cee59-154">Unit</span></span>      |<span data-ttu-id="cee59-155">Preço</span><span class="sxs-lookup"><span data-stu-id="cee59-155">Price</span></span>      |<span data-ttu-id="cee59-156">Moeda</span><span class="sxs-lookup"><span data-stu-id="cee59-156">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="cee59-157">A minha empresa_Faixa 1</span><span class="sxs-lookup"><span data-stu-id="cee59-157">My company_Band1</span></span> | <span data-ttu-id="cee59-158">Contoso E.U.A.</span><span class="sxs-lookup"><span data-stu-id="cee59-158">Contoso US</span></span>  |<span data-ttu-id="cee59-159">Hora</span><span class="sxs-lookup"><span data-stu-id="cee59-159">Hour</span></span> | <span data-ttu-id="cee59-160">145</span><span class="sxs-lookup"><span data-stu-id="cee59-160">145</span></span>|<span data-ttu-id="cee59-161">USD</span><span class="sxs-lookup"><span data-stu-id="cee59-161">USD</span></span>     |
| <span data-ttu-id="cee59-162">A minha empresa_Faixa 2</span><span class="sxs-lookup"><span data-stu-id="cee59-162">My company_Band2</span></span> | <span data-ttu-id="cee59-163">Contoso India</span><span class="sxs-lookup"><span data-stu-id="cee59-163">Contoso India</span></span> |<span data-ttu-id="cee59-164">Hora</span><span class="sxs-lookup"><span data-stu-id="cee59-164">Hour</span></span>|   <span data-ttu-id="cee59-165">67</span><span class="sxs-lookup"><span data-stu-id="cee59-165">67</span></span>|<span data-ttu-id="cee59-166">USD</span><span class="sxs-lookup"><span data-stu-id="cee59-166">USD</span></span>     |


[!INCLUDE[footer-include](../includes/footer-banner.md)]