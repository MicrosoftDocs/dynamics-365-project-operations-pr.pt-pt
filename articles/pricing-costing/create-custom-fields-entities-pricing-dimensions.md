---
title: Criar campos e entidades personalizados como dimensões de definição de preços
description: Este tópico fornece informações sobre como criar conjuntos de opções ou entidades personalizados.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 616bcd5758b434b45bd06aa1a026f32efc8b7f99
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130907"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="c5f3c-103">Criar campos e entidades personalizados como dimensões de definição de preços</span><span class="sxs-lookup"><span data-stu-id="c5f3c-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="c5f3c-104">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="c5f3c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c5f3c-105">Conclua os seguintes passos sempre que pretender criar um conjunto de opções ou uma entidade personalizada.</span><span class="sxs-lookup"><span data-stu-id="c5f3c-105">Complete the following steps any time that you want to create a custom option set or entity.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c5f3c-106">Recomendamos que efetue todas as alterações de dimensões de definição de preços personalizadas numa solução separada.</span><span class="sxs-lookup"><span data-stu-id="c5f3c-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="c5f3c-107">Essa melhor prática importante fornece flexibilidade no futuro para atualizar ou remover as alterações, conforme necessário, ajudará na reutilização do seu trabalho e facilita a portabilidade destas alterações para outra instância.</span><span class="sxs-lookup"><span data-stu-id="c5f3c-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="c5f3c-108">Depois de ter efetuado todas as alterações necessárias, exporte esta solução como uma **Solução Gerida** e importe-a para outras instâncias para reutilizar a configuração de preços.</span><span class="sxs-lookup"><span data-stu-id="c5f3c-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="c5f3c-109">Criar uma solução personalizada para dimensões de definição de preços</span><span class="sxs-lookup"><span data-stu-id="c5f3c-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="c5f3c-110">Aceda a **Definições** > **Soluções** e, em seguida, selecione **Novo** para criar uma nova solução.</span><span class="sxs-lookup"><span data-stu-id="c5f3c-110">Go to **Settings** > **Solutions**, and then select **New** to create a new solution.</span></span> 
2. <span data-ttu-id="c5f3c-111">Atribua um nome à solução, **\<your organization name> dimensões de definição de preços**, introduza as informações necessárias restantes e, em seguida, selecione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="c5f3c-111">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then select **Save**.</span></span>
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="c5f3c-112">Criar campos personalizados e conjuntos de opções na solução de dimensão de definição de preços</span><span class="sxs-lookup"><span data-stu-id="c5f3c-112">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="c5f3c-113">Uma dimensão de definição de preços pode ser uma conjunto de opções ou uma entidade.</span><span class="sxs-lookup"><span data-stu-id="c5f3c-113">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="c5f3c-114">Ambos têm de ser criados na solução de definição de preços.</span><span class="sxs-lookup"><span data-stu-id="c5f3c-114">Both must be created in your pricing solution.</span></span> <span data-ttu-id="c5f3c-115">Os passos neste procedimento explicam como criar dimensões baseadas em entidades e dimensões baseadas em conjuntos de opções.</span><span class="sxs-lookup"><span data-stu-id="c5f3c-115">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="c5f3c-116">Dimensões baseadas em entidades</span><span class="sxs-lookup"><span data-stu-id="c5f3c-116">Entity-based dimensions</span></span>

1. <span data-ttu-id="c5f3c-117">Aceda a **Definições** > **Soluções** e, de seguida, faça clique duplo nas dimensões de preços do **\<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="c5f3c-117">Go to **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="c5f3c-118">No Explorador de Soluções, no painel de navegação esquerdo, selecione **Entidades**.</span><span class="sxs-lookup"><span data-stu-id="c5f3c-118">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="c5f3c-119">Selecione **Novo** para criar uma nova entidade chamada **Título Padrão**.</span><span class="sxs-lookup"><span data-stu-id="c5f3c-119">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="c5f3c-120">Introduza as informações necessárias restantes e selecione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="c5f3c-120">Enter the remaining required information, and then select **Save**.</span></span>


### <a name="option-set-based-dimensions"></a><span data-ttu-id="c5f3c-121">Dimensões baseadas em conjuntos de opções</span><span class="sxs-lookup"><span data-stu-id="c5f3c-121">Option set-based dimensions</span></span> 
<span data-ttu-id="c5f3c-122">Pode criar duas dimensões baseadas em conjuntos de opções.</span><span class="sxs-lookup"><span data-stu-id="c5f3c-122">You can create two option set-based dimensions.</span></span> <span data-ttu-id="c5f3c-123">Utilize **Localização do Trabalho do Recurso** para monitorizar o preço do trabalho da localização **Principal** e o trabalho **No Local** e utilize **Horas de Trabalho do Recurso** com os valores **Normais** e **Horas Extraordinárias** para aplicar uma margem de lucro quando o trabalho estiver concluído.</span><span class="sxs-lookup"><span data-stu-id="c5f3c-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="c5f3c-124">Aceda a **Definições** > **Soluções** e faça clique duplo nas dimensões de preços do **\<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="c5f3c-124">Go to **Settings** > **Solutions**, and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="c5f3c-125">No Explorador de Soluções, no painel de navegação esquerdo, selecione  **Conjuntos de Opções**.</span><span class="sxs-lookup"><span data-stu-id="c5f3c-125">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="c5f3c-126">Selecione **Novo** para criar um novo conjunto de opções, introduza as informações necessárias restantes e, em seguida, selecione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="c5f3c-126">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="c5f3c-127">Criar dados para as dimensões baseadas em entidades</span><span class="sxs-lookup"><span data-stu-id="c5f3c-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="c5f3c-128">Pode criar manualmente dados para as dimensões baseadas em entidades ou através da utilização de chamadas de importação ou de serviço do Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="c5f3c-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="c5f3c-129">Utilize os passos indicados neste procedimento para criar dois títulos padrão, o **Engenheiro de Sistemas** e o **Engenheiro de Sistemas Sénior** a partir da dimensão baseada em entidades, **Título Padrão**.</span><span class="sxs-lookup"><span data-stu-id="c5f3c-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="c5f3c-130">Se os dados que pretende criar forem pequenos, como no exemplo seguinte, pode utilizar um formulário padrão.</span><span class="sxs-lookup"><span data-stu-id="c5f3c-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="c5f3c-131">Selecione **Pesquisa avançada**, selecione o **Título padrão** da entidade e, em seguida, selecione **Resultados**.</span><span class="sxs-lookup"><span data-stu-id="c5f3c-131">Select **Advanced Find**, select the entity **Standard Title**, and then select **Results**.</span></span> <span data-ttu-id="c5f3c-132">Serão mostradas todas as linhas na entidade **Título Padrão**.</span><span class="sxs-lookup"><span data-stu-id="c5f3c-132">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="c5f3c-133">Selecione **Novo**, e no campo **Nome**, introduza "Engenheiro de Sistemas" e selecione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="c5f3c-133">Select **New**, and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
3. <span data-ttu-id="c5f3c-134">Fechar o formulário.</span><span class="sxs-lookup"><span data-stu-id="c5f3c-134">Close the form.</span></span> 
4. <span data-ttu-id="c5f3c-135">Repita os passos 1 a 3 para criar outro título padrão para o "Engenheiro de Sistemas Sénior".</span><span class="sxs-lookup"><span data-stu-id="c5f3c-135">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="c5f3c-136">Adicionar todas as entidades obrigatórias e componentes relacionados necessários à Solução de Dimensão de Definição de Preços</span><span class="sxs-lookup"><span data-stu-id="c5f3c-136">Add all required entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="c5f3c-137">Terá de adicionar as seguintes entidades à Solução de Definição de Preços.</span><span class="sxs-lookup"><span data-stu-id="c5f3c-137">You will need to add the following entities to your pricing solution.</span></span> <span data-ttu-id="c5f3c-138">Utilize os passos indicados neste procedimento para efetuar algumas alterações de esquema importantes na solução de definição de preços, para que as entidades tomem conhecimento das novas dimensões de definição de preços.</span><span class="sxs-lookup"><span data-stu-id="c5f3c-138">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="c5f3c-139">Selecione **Definições** > **Soluções** e faça clique duplo nas dimensões de preços do **\<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="c5f3c-139">Select **Settings** > **Solutions**, and double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="c5f3c-140">No Explorador de Soluções, no painel de navegação esquerdo, selecione **Adicionar Existente** > **Entidades**.</span><span class="sxs-lookup"><span data-stu-id="c5f3c-140">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="c5f3c-141">Na caixa de diálogo **Componentes da Solução**, selecione as seguintes entidades:</span><span class="sxs-lookup"><span data-stu-id="c5f3c-141">In the **Solution Components** dialog box, select the following entities:</span></span>

  - <span data-ttu-id="c5f3c-142">Real</span><span class="sxs-lookup"><span data-stu-id="c5f3c-142">Actual</span></span>
  - <span data-ttu-id="c5f3c-143">Recurso Reservável</span><span class="sxs-lookup"><span data-stu-id="c5f3c-143">Bookable Resource</span></span>
  - <span data-ttu-id="c5f3c-144">Linha de Estimativa</span><span class="sxs-lookup"><span data-stu-id="c5f3c-144">Estimate Line</span></span>
  - <span data-ttu-id="c5f3c-145">Detalhe de Linha de Fatura</span><span class="sxs-lookup"><span data-stu-id="c5f3c-145">Invoice Line Detail</span></span>
  - <span data-ttu-id="c5f3c-146">Linha do Diário</span><span class="sxs-lookup"><span data-stu-id="c5f3c-146">Journal Line</span></span>
  - <span data-ttu-id="c5f3c-147">Detalhe de Item de Contrato do Projeto</span><span class="sxs-lookup"><span data-stu-id="c5f3c-147">Project Contract Line Detail</span></span>
  - <span data-ttu-id="c5f3c-148">Membro da Equipa do Projeto</span><span class="sxs-lookup"><span data-stu-id="c5f3c-148">Project Team Member</span></span>
  - <span data-ttu-id="c5f3c-149">Detalhe de Linha de Proposta</span><span class="sxs-lookup"><span data-stu-id="c5f3c-149">Quote Line Detail</span></span>
  - <span data-ttu-id="c5f3c-150">Margem de Lucro do Preço da Função</span><span class="sxs-lookup"><span data-stu-id="c5f3c-150">Role Price Markup</span></span>
  - <span data-ttu-id="c5f3c-151">Preço da Função</span><span class="sxs-lookup"><span data-stu-id="c5f3c-151">Role Price</span></span> 
  - <span data-ttu-id="c5f3c-152">Entrada de Hora</span><span class="sxs-lookup"><span data-stu-id="c5f3c-152">Time Entry</span></span> 


> [!NOTE]
> <span data-ttu-id="c5f3c-153">Certifique-se de que inclui todos os formulários e vistas para cada uma das entidades selecionadas.</span><span class="sxs-lookup"><span data-stu-id="c5f3c-153">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="c5f3c-154">Quando lhe for pedido para incluir entidades dependentes relativas às entidades selecionadas acima, selecione **Não**.</span><span class="sxs-lookup"><span data-stu-id="c5f3c-154">When prompted to include any dependent entities for the entities selected above, select **No**.</span></span>

