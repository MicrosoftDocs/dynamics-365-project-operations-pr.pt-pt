---
title: Criar campos e entidades personalizados como dimensões de definição de preços
description: Este tópico fornece informações sobre como criar conjuntos de opções ou entidades personalizados.
author: rumant
manager: AnnBe
ms.date: 11/18/2020
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
ms.openlocfilehash: fc5917856b8f28d36dc55593a68eba7823a00b36
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642827"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="390b4-103">Criar campos e entidades personalizados como dimensões de definição de preços</span><span class="sxs-lookup"><span data-stu-id="390b4-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="390b4-104">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="390b4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="390b4-105">Conclua os seguintes passos quando pretender criar um conjunto de opções ou uma entidade personalizados para utilizar como dimensão de preços.</span><span class="sxs-lookup"><span data-stu-id="390b4-105">Complete the following steps when you want to create a custom option set or entity for using it as a pricing dimension.</span></span> <span data-ttu-id="390b4-106">Para mais informações, consulte [Descrição geral de dimensões de preços](pricing-dimensions-overview.md).</span><span class="sxs-lookup"><span data-stu-id="390b4-106">For more information, see [Pricing dimensions overview](pricing-dimensions-overview.md).</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="390b4-107">Recomendamos que efetue todas as alterações de dimensões de definição de preços personalizadas numa solução separada.</span><span class="sxs-lookup"><span data-stu-id="390b4-107">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="390b4-108">Esta importante melhor prática proporciona flexibilidade no futuro para atualizar ou remover as alterações, se necessário.</span><span class="sxs-lookup"><span data-stu-id="390b4-108">This important best practice provides flexibility in the future to update or remove changes as needed.</span></span> <span data-ttu-id="390b4-109">Isto também ajudará na reutilização do seu trabalho e facilitará a portabilidade destas alterações para outra instância; depois de ter feito todas as alterações necessárias, exporte esta solução como **Solução gerida** e importe-a para outras instâncias para reutilizar a sua configuração de preços.</span><span class="sxs-lookup"><span data-stu-id="390b4-109">This will also help with re-use of your work and make it easier to port these changes to another instance After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="390b4-110">Criar campos personalizados e conjuntos de opções na solução de dimensão de definição de preços</span><span class="sxs-lookup"><span data-stu-id="390b4-110">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="390b4-111">Uma dimensão de definição de preços pode ser uma conjunto de opções ou uma entidade.</span><span class="sxs-lookup"><span data-stu-id="390b4-111">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="390b4-112">Ambos têm de ser criados na solução de definição de preços.</span><span class="sxs-lookup"><span data-stu-id="390b4-112">Both must be created in your pricing solution.</span></span> <span data-ttu-id="390b4-113">Os passos neste procedimento explicam como criar dimensões baseadas em entidades e dimensões baseadas em conjuntos de opções.</span><span class="sxs-lookup"><span data-stu-id="390b4-113">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="390b4-114">Dimensões baseadas em entidades</span><span class="sxs-lookup"><span data-stu-id="390b4-114">Entity-based dimensions</span></span>
<span data-ttu-id="390b4-115">Para criar dimensões baseadas em entidades, siga estes passos:</span><span class="sxs-lookup"><span data-stu-id="390b4-115">To create entity-based dimensions, follow these steps:</span></span>

1. <span data-ttu-id="390b4-116">Aceda a **Definições** > **Soluções** e, de seguida, faça clique duplo nas dimensões de preços do **\<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="390b4-116">Go to **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="390b4-117">No Explorador de Soluções, no painel de navegação esquerdo, selecione **Entidades**.</span><span class="sxs-lookup"><span data-stu-id="390b4-117">In Solution Explorer, in the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="390b4-118">Selecione **Novo** para criar uma nova entidade chamada **Título Padrão**.</span><span class="sxs-lookup"><span data-stu-id="390b4-118">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="390b4-119">Introduza as informações necessárias restantes e selecione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="390b4-119">Enter the remaining required information, and then select **Save**.</span></span>

> ![Definição da entidade de título padrão](media/Standard-Title-entity-definition.png)

### <a name="option-set-based-dimensions"></a><span data-ttu-id="390b4-121">Dimensões baseadas em conjuntos de opções</span><span class="sxs-lookup"><span data-stu-id="390b4-121">Option set-based dimensions</span></span> 
<span data-ttu-id="390b4-122">Pode criar duas dimensões baseadas em conjuntos de opções.</span><span class="sxs-lookup"><span data-stu-id="390b4-122">You can create two option set-based dimensions.</span></span> 

- <span data-ttu-id="390b4-123">Utilize **Localização de Trabalho de Recursos** para monitorizar o preço do trabalho de localização **Doméstica** e o trabalho **No local**.</span><span class="sxs-lookup"><span data-stu-id="390b4-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work.</span></span> 
- <span data-ttu-id="390b4-124">Utilize **Horas de trabalho de recursos** com valores **Regulares** e **Horas Extraordinárias** para aplicar uma margem de lucro quando o trabalho estiver concluído.</span><span class="sxs-lookup"><span data-stu-id="390b4-124">Use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when the work is complete.</span></span>

<span data-ttu-id="390b4-125">O gráfico a seguir proporciona uma vista da dimensão de **Localização de Trabalho de Recursos**.</span><span class="sxs-lookup"><span data-stu-id="390b4-125">The following graphic provides a view of the **Resource Work Location** dimension.</span></span> 

> ![Dimensão de definição de preços baseada em conjuntos de opções denominada Localização de Trabalho do Recurso](media/Option-set-PD-called-Resource-Work-Location.png)

<span data-ttu-id="390b4-127">O gráfico a seguir proporciona uma vista da dimensão de **Horas de Trabalho de Recursos**.</span><span class="sxs-lookup"><span data-stu-id="390b4-127">The following graphic provides a view of the **Resource Work Hours** dimension.</span></span> 

> ![Dimensão de definição de preços baseada em conjuntos de opções denominada Horas de Trabalho do Recurso](media/Option-set-PD-called-Resource-Work-Hours.png)

1. <span data-ttu-id="390b4-129">Aceda a **Definições** > **Soluções** e faça clique duplo nas dimensões de preços do **\<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="390b4-129">Go to **Settings** > **Solutions**, and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="390b4-130">No Explorador de Soluções, no painel de navegação esquerdo, selecione **Conjuntos de Opções**.</span><span class="sxs-lookup"><span data-stu-id="390b4-130">In Solution Explorer, in the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="390b4-131">Selecione **Novo** para criar um novo conjunto de opções, introduza as informações necessárias restantes e, em seguida, selecione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="390b4-131">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="390b4-132">Criar dados para as dimensões baseadas em entidades</span><span class="sxs-lookup"><span data-stu-id="390b4-132">Create data for entity-based dimensions</span></span>

<span data-ttu-id="390b4-133">Pode criar manualmente dados para as dimensões baseadas em entidades ou através da utilização de chamadas de importação ou de serviço do Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="390b4-133">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="390b4-134">Utilize os passos indicados neste procedimento para criar dois títulos padrão, o **Engenheiro de Sistemas** e o **Engenheiro de Sistemas Sénior** a partir da dimensão baseada em entidades, **Título Padrão**.</span><span class="sxs-lookup"><span data-stu-id="390b4-134">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="390b4-135">Se os dados que pretende criar forem pequenos, como no exemplo seguinte, pode utilizar um formulário padrão.</span><span class="sxs-lookup"><span data-stu-id="390b4-135">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="390b4-136">Selecione **Localização Avançada**.</span><span class="sxs-lookup"><span data-stu-id="390b4-136">Select **Advanced Find**.</span></span>
2. <span data-ttu-id="390b4-137">Selecione a entidade **Título Padrão** e, em seguida, selecione **Resultados**.</span><span class="sxs-lookup"><span data-stu-id="390b4-137">Select the entity **Standard Title**, and then select **Results**.</span></span> <span data-ttu-id="390b4-138">Serão mostradas todas as linhas na entidade **Título Padrão**.</span><span class="sxs-lookup"><span data-stu-id="390b4-138">All of the rows in the **Standard Title** entity will be shown.</span></span>
3. <span data-ttu-id="390b4-139">Selecione **Novo**, e no campo **Nome**, introduza "Engenheiro de Sistemas" e selecione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="390b4-139">Select **New**, and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
4. <span data-ttu-id="390b4-140">Feche a página.</span><span class="sxs-lookup"><span data-stu-id="390b4-140">Close the page.</span></span> 
5. <span data-ttu-id="390b4-141">Repita os passos 1 a 3 para criar outro título padrão para o "Engenheiro de Sistemas Sénior".</span><span class="sxs-lookup"><span data-stu-id="390b4-141">Repeat steps 1-3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![Dados de exemplo para a entidade Título Padrão](media/ST-data.png)
