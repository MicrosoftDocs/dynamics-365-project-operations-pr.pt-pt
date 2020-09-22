---
title: Criar campos e entidades personalizados
description: Este tópico explica como criar conjuntos de opções e entidades na sua própria solução na plataforma Power Apps.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/26/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: fb160bfd-e037-4a21-a968-3ff2e6e16481
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 7ee30e3bb6b8034ef226e2e9181195685355011f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754601"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="03afd-103">Criar campos e entidades personalizados</span><span class="sxs-lookup"><span data-stu-id="03afd-103">Create custom fields and entities</span></span> 

<span data-ttu-id="03afd-104">Conclua os seguintes passos sempre que pretender criar um conjunto de opções ou uma entidade personalizada na plataforma Power Apps.</span><span class="sxs-lookup"><span data-stu-id="03afd-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="03afd-105">Os procedimentos existentes neste tópico devem ser concluídos utilizando a interface Web do Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="03afd-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="03afd-106">Recomendamos que efetue todas as alterações de dimensões de definição de preços personalizadas numa solução separada.</span><span class="sxs-lookup"><span data-stu-id="03afd-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="03afd-107">Essa melhor prática importante fornece flexibilidade no futuro para atualizar ou remover as alterações, conforme necessário, ajudará na reutilização do seu trabalho e facilita a portabilidade destas alterações para outra instância.</span><span class="sxs-lookup"><span data-stu-id="03afd-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="03afd-108">Depois de ter efetuado todas as alterações necessárias, exporte esta solução como uma **Solução Gerida** e importe-a para outras instâncias para reutilizar a configuração de preços.</span><span class="sxs-lookup"><span data-stu-id="03afd-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="03afd-109">Criar uma solução personalizada para dimensões de definição de preços</span><span class="sxs-lookup"><span data-stu-id="03afd-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="03afd-110">No PSA, clique em **Definições** > **Soluções** e, em seguida, clique em **Novo** para criar uma nova solução.</span><span class="sxs-lookup"><span data-stu-id="03afd-110">In PSA, click **Settings** > **Solutions**, and then click **New** to create a new solution.</span></span> 
2. <span data-ttu-id="03afd-111">Atribua um nome à solução, **\<o nome da sua organização > dimensões de definição de preços**, introduza as informações necessárias restantes e, em seguida, clique em **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="03afd-111">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then click **Save**.</span></span>

> ![Criar uma solução personalizada para dimensões de definição de preços](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="03afd-113">Criar campos personalizados e conjuntos de opções na solução de dimensão de definição de preços</span><span class="sxs-lookup"><span data-stu-id="03afd-113">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="03afd-114">Uma dimensão de definição de preços pode ser uma conjunto de opções ou uma entidade.</span><span class="sxs-lookup"><span data-stu-id="03afd-114">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="03afd-115">Ambos têm de ser criados na solução de definição de preços.</span><span class="sxs-lookup"><span data-stu-id="03afd-115">Both must be created in your pricing solution.</span></span> <span data-ttu-id="03afd-116">Os passos neste procedimento explicam como criar dimensões baseadas em entidades e dimensões baseadas em conjuntos de opções.</span><span class="sxs-lookup"><span data-stu-id="03afd-116">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="03afd-117">Dimensões baseadas em entidades</span><span class="sxs-lookup"><span data-stu-id="03afd-117">Entity-based dimensions</span></span>

1. <span data-ttu-id="03afd-118">No PSA, clique em **Definições** > **Soluções** e faça duplo clique no **\<nome da sua organização> dimensões de definição de preços**.</span><span class="sxs-lookup"><span data-stu-id="03afd-118">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="03afd-119">No Explorador de Soluções, no painel de navegação esquerdo, selecione **Entidades**.</span><span class="sxs-lookup"><span data-stu-id="03afd-119">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="03afd-120">Clique em **Novo** para criar uma nova entidade chamada **Título Padrão**.</span><span class="sxs-lookup"><span data-stu-id="03afd-120">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="03afd-121">Introduza as informações necessárias restantes e clique em **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="03afd-121">Enter the remaining required information, and then click **Save**.</span></span>

> ![Definição da entidade de título padrão](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="03afd-123">Dimensões baseadas em conjuntos de opções</span><span class="sxs-lookup"><span data-stu-id="03afd-123">Option set-based dimensions</span></span> 
<span data-ttu-id="03afd-124">Pode criar duas dimensões baseadas em conjuntos de opções.</span><span class="sxs-lookup"><span data-stu-id="03afd-124">You can create two option set-based dimensions.</span></span> <span data-ttu-id="03afd-125">Utilize **Localização do Trabalho do Recurso** para monitorizar o preço do trabalho da localização **Principal** e o trabalho **No Local** e utilize **Horas de Trabalho do Recurso** com os valores **Normais** e **Horas Extraordinárias** para aplicar uma margem de lucro quando o trabalho estiver concluído.</span><span class="sxs-lookup"><span data-stu-id="03afd-125">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="03afd-126">No PSA, clique em **Definições** > **Soluções** e faça duplo clique no  **\<nome da sua organização> dimensões de definição de preços**.</span><span class="sxs-lookup"><span data-stu-id="03afd-126">In PSA, click **Settings** > **Solutions**, and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="03afd-127">No Explorador de Soluções, no painel de navegação esquerdo, selecione  **Conjuntos de Opções**.</span><span class="sxs-lookup"><span data-stu-id="03afd-127">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="03afd-128">Clique em **Novo** para criar um novo conjunto de opções, introduza as informações necessárias restantes e, em seguida, clique em **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="03afd-128">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="03afd-129">Dimensão de definição de preços baseada em conjuntos de opções denominada Localização de Trabalho do Recurso</span><span class="sxs-lookup"><span data-stu-id="03afd-129">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="03afd-130">Dimensão de definição de preços baseada em conjuntos de opções denominada Horas de Trabalho do Recurso</span><span class="sxs-lookup"><span data-stu-id="03afd-130">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="03afd-131">Criar dados para as dimensões baseadas em entidades</span><span class="sxs-lookup"><span data-stu-id="03afd-131">Create data for entity-based dimensions</span></span>

<span data-ttu-id="03afd-132">Pode criar manualmente dados para as dimensões baseadas em entidades ou através da utilização de chamadas de importação ou de serviço do Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="03afd-132">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="03afd-133">Utilize os passos indicados neste procedimento para criar dois títulos padrão, o **Engenheiro de Sistemas** e o **Engenheiro de Sistemas Sénior** a partir da dimensão baseada em entidades, **Título Padrão**.</span><span class="sxs-lookup"><span data-stu-id="03afd-133">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="03afd-134">Se os dados que pretende criar forem pequenos, como no exemplo seguinte, pode utilizar um formulário padrão.</span><span class="sxs-lookup"><span data-stu-id="03afd-134">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="03afd-135">No PSA, clique em **Localização Avançada**.</span><span class="sxs-lookup"><span data-stu-id="03afd-135">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="03afd-136">Selecione a entidade **Título Padrão** e, em seguida, clique em **Resultados**.</span><span class="sxs-lookup"><span data-stu-id="03afd-136">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="03afd-137">Serão mostradas todas as linhas na entidade **Título Padrão**.</span><span class="sxs-lookup"><span data-stu-id="03afd-137">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="03afd-138">Clique em **Novo**.</span><span class="sxs-lookup"><span data-stu-id="03afd-138">Click **New**.</span></span> <span data-ttu-id="03afd-139">No campo **Nome**, introduza "Engenheiro de Sistemas" e clique em **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="03afd-139">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="03afd-140">Feche o formulário.</span><span class="sxs-lookup"><span data-stu-id="03afd-140">Close the form.</span></span> 
4. <span data-ttu-id="03afd-141">Repita os passos 1 a 3 para criar outro título padrão para o "Engenheiro de Sistemas Sénior".</span><span class="sxs-lookup"><span data-stu-id="03afd-141">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="03afd-142">Dados de Exemplo para a Entidade Título Padrão</span><span class="sxs-lookup"><span data-stu-id="03afd-142">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)

## <a name="add-all-required-psa-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="03afd-143">Adicionar todas as entidades do PSA e componentes relacionados necessários à Solução de Dimensão de Definição de Preços</span><span class="sxs-lookup"><span data-stu-id="03afd-143">Add all required PSA entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="03afd-144">Terá de adicionar as seguintes entidades do Project Service à Solução de Definição de Preços.</span><span class="sxs-lookup"><span data-stu-id="03afd-144">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="03afd-145">Utilize os passos indicados neste procedimento para efetuar algumas alterações de esquema importantes na solução de definição de preços, para que as entidades tomem conhecimento das novas dimensões de definição de preços.</span><span class="sxs-lookup"><span data-stu-id="03afd-145">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="03afd-146">No PSA, clique em **Definições** > **Soluções** e faça duplo clique no **\<nome da sua organização> dimensões de definição de preços**.</span><span class="sxs-lookup"><span data-stu-id="03afd-146">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="03afd-147">No Explorador de Soluções, no painel de navegação esquerdo, selecione **Adicionar Existente** > **Entidades**.</span><span class="sxs-lookup"><span data-stu-id="03afd-147">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="03afd-148">Na caixa de diálogo **Componentes da Solução**, selecione as seguintes entidades:</span><span class="sxs-lookup"><span data-stu-id="03afd-148">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="03afd-149">Real</span><span class="sxs-lookup"><span data-stu-id="03afd-149">Actual</span></span>
- <span data-ttu-id="03afd-150">Recurso Reservável</span><span class="sxs-lookup"><span data-stu-id="03afd-150">Bookable Resource</span></span>
- <span data-ttu-id="03afd-151">Linha de Estimativa</span><span class="sxs-lookup"><span data-stu-id="03afd-151">Estimate Line</span></span>
- <span data-ttu-id="03afd-152">Detalhe de Linha de Fatura</span><span class="sxs-lookup"><span data-stu-id="03afd-152">Invoice Line Detail</span></span>
- <span data-ttu-id="03afd-153">Linha do Diário</span><span class="sxs-lookup"><span data-stu-id="03afd-153">Journal Line</span></span>
- <span data-ttu-id="03afd-154">Detalhe de Item de Contrato do Projeto</span><span class="sxs-lookup"><span data-stu-id="03afd-154">Project Contract Line Detail</span></span>
- <span data-ttu-id="03afd-155">Membro da Equipa do Projeto</span><span class="sxs-lookup"><span data-stu-id="03afd-155">Project Team Member</span></span>
- <span data-ttu-id="03afd-156">Detalhe de Item de Proposta</span><span class="sxs-lookup"><span data-stu-id="03afd-156">Quote Line Detail</span></span>
- <span data-ttu-id="03afd-157">Margem de Lucro do Preço da Função</span><span class="sxs-lookup"><span data-stu-id="03afd-157">Role Price Markup</span></span>
- <span data-ttu-id="03afd-158">Preço da Função</span><span class="sxs-lookup"><span data-stu-id="03afd-158">Role Price</span></span> 
- <span data-ttu-id="03afd-159">Entrada de Hora</span><span class="sxs-lookup"><span data-stu-id="03afd-159">Time Entry</span></span> 

> ![Adicionar as entidades existentes à solução de dimensões de definição de preços](media/Existing-entities-to-PD-solution.png)

> ![Selecionar componentes da solução](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="03afd-162">Certifique-se de que inclui todos os formulários e vistas para cada uma das entidades selecionadas.</span><span class="sxs-lookup"><span data-stu-id="03afd-162">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="03afd-163">Quando lhe for pedido para incluir entidades dependentes relativas às entidades selecionadas acima, clique em **Não**.</span><span class="sxs-lookup"><span data-stu-id="03afd-163">When prompted to include any dependent entities for the entities selected above, click **No**.</span></span>

> ![Não incluir todos os componentes relacionados](media/Do-not-include-required.png)


