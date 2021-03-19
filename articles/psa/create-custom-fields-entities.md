---
title: Criar campos e entidades personalizados
description: Este tópico explica como criar conjuntos de opções e entidades na sua própria solução na plataforma Power Apps.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: c58745a46e84a40b90fbb3cbf89b10e293588fc3
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290552"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="0052a-103">Criar campos e entidades personalizados</span><span class="sxs-lookup"><span data-stu-id="0052a-103">Create custom fields and entities</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="0052a-104">Conclua os seguintes passos sempre que pretender criar um conjunto de opções ou uma entidade personalizada na plataforma Power Apps.</span><span class="sxs-lookup"><span data-stu-id="0052a-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="0052a-105">Os procedimentos existentes neste tópico devem ser concluídos utilizando a interface Web do Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="0052a-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0052a-106">Recomendamos que efetue todas as alterações de dimensões de definição de preços personalizadas numa solução separada.</span><span class="sxs-lookup"><span data-stu-id="0052a-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="0052a-107">Essa melhor prática importante fornece flexibilidade no futuro para atualizar ou remover as alterações, conforme necessário, ajudará na reutilização do seu trabalho e facilita a portabilidade destas alterações para outra instância.</span><span class="sxs-lookup"><span data-stu-id="0052a-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="0052a-108">Depois de ter efetuado todas as alterações necessárias, exporte esta solução como uma **Solução Gerida** e importe-a para outras instâncias para reutilizar a configuração de preços.</span><span class="sxs-lookup"><span data-stu-id="0052a-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="0052a-109">Criar campos personalizados e conjuntos de opções na solução de dimensão de definição de preços</span><span class="sxs-lookup"><span data-stu-id="0052a-109">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="0052a-110">Uma dimensão de definição de preços pode ser uma conjunto de opções ou uma entidade.</span><span class="sxs-lookup"><span data-stu-id="0052a-110">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="0052a-111">Ambos têm de ser criados na solução de definição de preços.</span><span class="sxs-lookup"><span data-stu-id="0052a-111">Both must be created in your pricing solution.</span></span> <span data-ttu-id="0052a-112">Os passos neste procedimento explicam como criar dimensões baseadas em entidades e dimensões baseadas em conjuntos de opções.</span><span class="sxs-lookup"><span data-stu-id="0052a-112">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="0052a-113">Dimensões baseadas em entidades</span><span class="sxs-lookup"><span data-stu-id="0052a-113">Entity-based dimensions</span></span>

1. <span data-ttu-id="0052a-114">Em PSA, clique em **Definições** > **Soluções** e, em seguida, faça clique duplo nas dimensões de preços do **\<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="0052a-114">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="0052a-115">No Explorador de Soluções, no painel de navegação esquerdo, selecione **Entidades**.</span><span class="sxs-lookup"><span data-stu-id="0052a-115">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="0052a-116">Clique em **Novo** para criar uma nova entidade chamada **Título Padrão**.</span><span class="sxs-lookup"><span data-stu-id="0052a-116">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="0052a-117">Introduza as informações necessárias restantes e clique em **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="0052a-117">Enter the remaining required information, and then click **Save**.</span></span>

> ![Definição da entidade de título padrão](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="0052a-119">Dimensões baseadas em conjuntos de opções</span><span class="sxs-lookup"><span data-stu-id="0052a-119">Option set-based dimensions</span></span> 
<span data-ttu-id="0052a-120">Pode criar duas dimensões baseadas em conjuntos de opções.</span><span class="sxs-lookup"><span data-stu-id="0052a-120">You can create two option set-based dimensions.</span></span> <span data-ttu-id="0052a-121">Utilize **Localização do Trabalho do Recurso** para monitorizar o preço do trabalho da localização **Principal** e o trabalho **No Local** e utilize **Horas de Trabalho do Recurso** com os valores **Normais** e **Horas Extraordinárias** para aplicar uma margem de lucro quando o trabalho estiver concluído.</span><span class="sxs-lookup"><span data-stu-id="0052a-121">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="0052a-122">Em PSA, clique em **Definições** > **Soluções** e, em seguida, faça clique duplo nas dimensões de preços do **\<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="0052a-122">In PSA, click **Settings** > **Solutions**, and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="0052a-123">No Explorador de Soluções, no painel de navegação esquerdo, selecione  **Conjuntos de Opções**.</span><span class="sxs-lookup"><span data-stu-id="0052a-123">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="0052a-124">Clique em **Novo** para criar um novo conjunto de opções, introduza as informações necessárias restantes e, em seguida, clique em **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="0052a-124">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="0052a-125">Dimensão de definição de preços baseada em conjuntos de opções denominada Localização de Trabalho do Recurso</span><span class="sxs-lookup"><span data-stu-id="0052a-125">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="0052a-126">Dimensão de definição de preços baseada em conjuntos de opções denominada Horas de Trabalho do Recurso</span><span class="sxs-lookup"><span data-stu-id="0052a-126">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="0052a-127">Criar dados para as dimensões baseadas em entidades</span><span class="sxs-lookup"><span data-stu-id="0052a-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="0052a-128">Pode criar manualmente dados para as dimensões baseadas em entidades ou através da utilização de chamadas de importação ou de serviço do Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="0052a-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="0052a-129">Utilize os passos indicados neste procedimento para criar dois títulos padrão, o **Engenheiro de Sistemas** e o **Engenheiro de Sistemas Sénior** a partir da dimensão baseada em entidades, **Título Padrão**.</span><span class="sxs-lookup"><span data-stu-id="0052a-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="0052a-130">Se os dados que pretende criar forem pequenos, como no exemplo seguinte, pode utilizar um formulário padrão.</span><span class="sxs-lookup"><span data-stu-id="0052a-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="0052a-131">No PSA, clique em **Localização Avançada**.</span><span class="sxs-lookup"><span data-stu-id="0052a-131">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="0052a-132">Selecione a entidade **Título Padrão** e, em seguida, clique em **Resultados**.</span><span class="sxs-lookup"><span data-stu-id="0052a-132">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="0052a-133">Serão mostradas todas as linhas na entidade **Título Padrão**.</span><span class="sxs-lookup"><span data-stu-id="0052a-133">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="0052a-134">Clique em **Novo**.</span><span class="sxs-lookup"><span data-stu-id="0052a-134">Click **New**.</span></span> <span data-ttu-id="0052a-135">No campo **Nome**, introduza "Engenheiro de Sistemas" e clique em **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="0052a-135">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="0052a-136">Feche o formulário.</span><span class="sxs-lookup"><span data-stu-id="0052a-136">Close the form.</span></span> 
4. <span data-ttu-id="0052a-137">Repita os passos 1 a 3 para criar outro título padrão para o "Engenheiro de Sistemas Sénior".</span><span class="sxs-lookup"><span data-stu-id="0052a-137">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="0052a-138">Dados de Exemplo para a Entidade Título Padrão</span><span class="sxs-lookup"><span data-stu-id="0052a-138">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]