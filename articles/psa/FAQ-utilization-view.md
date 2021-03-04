---
title: Ver a utilização faturável para recursos
description: Este tópico fornece informações sobre a vista de utilização de recursos.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 4516c562e7eaf35c5fef638183967eef5a033b11
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146407"
---
# <a name="view-chargeable-utilization-for-resources"></a><span data-ttu-id="e3dd6-103">Ver a utilização faturável para recursos</span><span class="sxs-lookup"><span data-stu-id="e3dd6-103">View chargeable utilization for resources</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]
 
<span data-ttu-id="e3dd6-104">A **Vista de Utilização** na página **Utilização de Recursos do Project Service** mostra a utilização faturável de cada recurso reservável.</span><span class="sxs-lookup"><span data-stu-id="e3dd6-104">The **Utilization View** on the **Project Service Resource Utilization** page shows the chargeable utilization for each bookable resource.</span></span> <span data-ttu-id="e3dd6-105">Como a vista é baseada no quadro da agenda, irá encontrar muitas das mesmas funções.</span><span class="sxs-lookup"><span data-stu-id="e3dd6-105">Because the view is based on the schedule board, you’ll find many of the same functions.</span></span>

> ![Captura de ecrã da Vista de Utilização](media/FAQ-utilization-1.png)
 

<span data-ttu-id="e3dd6-107">O cálculo de utilização faturável funciona da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="e3dd6-107">The chargeable utilization calculation works as follows:</span></span>

   <span data-ttu-id="e3dd6-108">Utilização faturável = (Horas reais faturáveis) / (capacidade do recurso)</span><span class="sxs-lookup"><span data-stu-id="e3dd6-108">Chargeable utilization = (Chargeable actual hours) / (resource capacity)</span></span>

<span data-ttu-id="e3dd6-109">As células representam a utilização faturável calculada durante o período selecionado (dias, semanas ou meses).</span><span class="sxs-lookup"><span data-stu-id="e3dd6-109">The cells represent the calculated chargeable utilization for the selected period (days, weeks, or months).</span></span>

<span data-ttu-id="e3dd6-110">As cores em cada uma das células mostram a utilização faturável para um recurso em comparação com a sua utilização faturável de destino.</span><span class="sxs-lookup"><span data-stu-id="e3dd6-110">The colors in each cell show the chargeable utilization for a resource as compared to their target chargeable utilization.</span></span> 

<span data-ttu-id="e3dd6-111">A utilização de destino pode ser definida na função predefinida do recurso ou no recurso individual propriamente dito.</span><span class="sxs-lookup"><span data-stu-id="e3dd6-111">The target utilization can be set on the resource’s default role or on the individual resource itself.</span></span> <span data-ttu-id="e3dd6-112">O cálculo examina a pessoa pelo destino em primeiro lugar e, em seguida, para a função predefinida do recurso.</span><span class="sxs-lookup"><span data-stu-id="e3dd6-112">The calculation looks at the individual for the target first, and then to the resource’s default role.</span></span>

## <a name="set-target-on-a-resource"></a><span data-ttu-id="e3dd6-113">Definir destino num recurso</span><span class="sxs-lookup"><span data-stu-id="e3dd6-113">Set target on a resource</span></span>

1. <span data-ttu-id="e3dd6-114">Aceda a **Recursos** \> **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="e3dd6-114">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="e3dd6-115">Selecione um recurso para abrir o registo.</span><span class="sxs-lookup"><span data-stu-id="e3dd6-115">Select a resource to open the record.</span></span> 
3. <span data-ttu-id="e3dd6-116">No separador **Project Service**, pode definir a utilização de destino do recurso.</span><span class="sxs-lookup"><span data-stu-id="e3dd6-116">On the **Project Service** tab, you can set the resource’s target utilization.</span></span>

> ![Captura de ecrã da utilização do separador Project Service para definir a utilização de destino](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a><span data-ttu-id="e3dd6-118">Definir utilização de destino numa função</span><span class="sxs-lookup"><span data-stu-id="e3dd6-118">Set target utilization on a role</span></span>

1. <span data-ttu-id="e3dd6-119">Aceda a **Recursos** \> **Funções do Recurso**.</span><span class="sxs-lookup"><span data-stu-id="e3dd6-119">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="e3dd6-120">Selecione uma função e abra o registo.</span><span class="sxs-lookup"><span data-stu-id="e3dd6-120">Select a role and open the record.</span></span> 
3. <span data-ttu-id="e3dd6-121">Defina a utilização de destino para a função.</span><span class="sxs-lookup"><span data-stu-id="e3dd6-121">Set the target utilization for the role.</span></span>

> ![Captura de ecrã da utilização de Funções de Recursos para definir a utilização de destino](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a><span data-ttu-id="e3dd6-123">Calcular a utilização faturável para um recurso</span><span class="sxs-lookup"><span data-stu-id="e3dd6-123">Calculate chargeable utilization for a resource</span></span>

<span data-ttu-id="e3dd6-124">Para calcular a utilização faturável de um recurso terá de concluir alguns pré-requisitos.</span><span class="sxs-lookup"><span data-stu-id="e3dd6-124">To calculate chargeable utilization for a resource, you will need to complete some pre-requisites.</span></span> 

### <a name="set-default-role-for-individual-resource"></a><span data-ttu-id="e3dd6-125">Definir função predefinida para recurso individual</span><span class="sxs-lookup"><span data-stu-id="e3dd6-125">Set default role for individual resource</span></span>

<span data-ttu-id="e3dd6-126">Em primeiro lugar, a utilização de destino tem ser definida no recurso individual ou nas funções do recurso.</span><span class="sxs-lookup"><span data-stu-id="e3dd6-126">First, the target utilization must be set on either the individual resource or on resource roles.</span></span> <span data-ttu-id="e3dd6-127">Se estiver a utilizar funções de recursos para destinos, cada recurso individual tem de ter uma função predefinida.</span><span class="sxs-lookup"><span data-stu-id="e3dd6-127">If you are using resource roles for targets, each individual resource must have a default role.</span></span> 

1. <span data-ttu-id="e3dd6-128">Para definir isto, aceda a **Recursos** \> **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="e3dd6-128">To set this, go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="e3dd6-129">Selecione um recurso, abra o registo e, em seguida, selecione o separador **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="e3dd6-129">Select a resource, open the record, and then select the **Project Service** tab.</span></span> 
3. <span data-ttu-id="e3dd6-130">Na grelha **Função do Recurso**, certifique-se de que existe uma função para o recurso e que **É Predefinição** está definido como **Sim**.</span><span class="sxs-lookup"><span data-stu-id="e3dd6-130">In the **Resource Role** grid, make sure there’s one role for the resource and **Is Default** is set to **Yes**.</span></span>
 
### <a name="change-billing-type-for-resource-role"></a><span data-ttu-id="e3dd6-131">Alterar o tipo de faturação para a função do recurso</span><span class="sxs-lookup"><span data-stu-id="e3dd6-131">Change billing type for resource role</span></span>

<span data-ttu-id="e3dd6-132">As funções de recursos têm de ser definidas para ter um tipo de faturação de **Faturável**.</span><span class="sxs-lookup"><span data-stu-id="e3dd6-132">The resource roles must be set to have a billing type of **Chargeable**.</span></span> 

1. <span data-ttu-id="e3dd6-133">Aceda a **Recursos** \> **Funções do Recurso**.</span><span class="sxs-lookup"><span data-stu-id="e3dd6-133">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="e3dd6-134">Abra o registo que pretende atualizar e defina o tipo de faturação predefinido como **Faturável**.</span><span class="sxs-lookup"><span data-stu-id="e3dd6-134">Open the record you want to update, and then set the billing type default to **Chargeable**.</span></span>

### <a name="set-working-hours-for-resource-role"></a><span data-ttu-id="e3dd6-135">Definir horas de trabalho para a função do recurso</span><span class="sxs-lookup"><span data-stu-id="e3dd6-135">Set working hours for resource role</span></span>
 
<span data-ttu-id="e3dd6-136">O recurso tem de ter horas de expediente para o cálculo de capacidade.</span><span class="sxs-lookup"><span data-stu-id="e3dd6-136">The resource must have working hours for the capacity calculation.</span></span> 

1. <span data-ttu-id="e3dd6-137">Aceda a **Recursos** \> **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="e3dd6-137">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="e3dd6-138">Selecione um recurso para abrir o registo e, em seguida, selecione **Mostrar Horas de Trabalho**.</span><span class="sxs-lookup"><span data-stu-id="e3dd6-138">Select a resource to open the record, and then select **Show Work Hours**.</span></span> 
3. <span data-ttu-id="e3dd6-139">Pode atualizar em massa a lista de recursos ao aplicar um **Modelo de Horas de Trabalho** a partir da vista de **Lista de Recursos**.</span><span class="sxs-lookup"><span data-stu-id="e3dd6-139">You can bulk-update the list of resources by applying a **Work Hour Template** from the **Resource List** view.</span></span>

## <a name="troubleshooting-chargeable-actual-hours"></a><span data-ttu-id="e3dd6-140">Resolução de problemas de horas reais faturáveis</span><span class="sxs-lookup"><span data-stu-id="e3dd6-140">Troubleshooting chargeable actual hours</span></span>

<span data-ttu-id="e3dd6-141">As horas reais faturáveis são obtidas a partir da entidade **Valores Reais**.</span><span class="sxs-lookup"><span data-stu-id="e3dd6-141">The chargeable actual hours are sourced from the **Actuals** entity.</span></span> <span data-ttu-id="e3dd6-142">Os valores reais com uma faturação de tipo **Faturável** estão incluídos no cálculo e, por este motivo, deve ter projetos nos quais os valores reais são faturáveis.</span><span class="sxs-lookup"><span data-stu-id="e3dd6-142">Actuals with a billing type of **Chargeable** are included in the calculation and, for this reason, you must have projects where the actuals that are chargeable.</span></span>

<span data-ttu-id="e3dd6-143">Se não está a ver utilização faturável, eis alguns aspetos que pode verificar:</span><span class="sxs-lookup"><span data-stu-id="e3dd6-143">If you are not seeing chargeable utilization, here are some things you can check:</span></span>

- <span data-ttu-id="e3dd6-144">A capacidade é definida nas horas de trabalho dos recursos.</span><span class="sxs-lookup"><span data-stu-id="e3dd6-144">The resource has working hours defined for capacity.</span></span>
- <span data-ttu-id="e3dd6-145">O recurso tem uma utilização de destino definida individualmente ou tem uma função padrão atribuída.</span><span class="sxs-lookup"><span data-stu-id="e3dd6-145">The resource has either an individually defined utilization target or has a default role assigned to it.</span></span> <span data-ttu-id="e3dd6-146">A função tem uma utilização de destino definida.</span><span class="sxs-lookup"><span data-stu-id="e3dd6-146">The role has a utilization target defined for it.</span></span>
- <span data-ttu-id="e3dd6-147">Os valores reais têm um tipo de faturação **Faturável** para o período para o qual está à espera de um cálculo de utilização.</span><span class="sxs-lookup"><span data-stu-id="e3dd6-147">Actuals have a billing type of **Chargeable** for the period you are expecting a utilization calculation for.</span></span> <span data-ttu-id="e3dd6-148">Verifique o seguinte se estiver a ver valores reais com tipos de faturação diferentes de faturável:</span><span class="sxs-lookup"><span data-stu-id="e3dd6-148">Check the following if you are seeing actuals with billing types other than chargeable:</span></span>

  - <span data-ttu-id="e3dd6-149">A função utilizada nos valores reais tem um tipo de faturação padrão diferente de faturável.</span><span class="sxs-lookup"><span data-stu-id="e3dd6-149">The role used on the actual has a default billing type of something other than chargeable.</span></span>
  - <span data-ttu-id="e3dd6-150">A função do item de contrato do projeto que apoia o projeto foi definida como não faturável.</span><span class="sxs-lookup"><span data-stu-id="e3dd6-150">The role on the project contract line backing the project has been set to non-chargeable.</span></span>
  - <span data-ttu-id="e3dd6-151">O projeto não tem um item de contrato associado.</span><span class="sxs-lookup"><span data-stu-id="e3dd6-151">The project does not have an associated contract line.</span></span>

