---
title: Criar soluções personalizadas para dimensões de preços
description: Este tópico explica como criar uma solução personalizada ao criar dimensões de preços personalizados.
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
ms.openlocfilehash: 3810df9b875d017a8d639b5253b96275571898f3
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144653"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a><span data-ttu-id="47709-103">Criar soluções personalizadas para dimensões de preços</span><span class="sxs-lookup"><span data-stu-id="47709-103">Create custom solutions for pricing dimensions</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

> [!IMPORTANT]
> <span data-ttu-id="47709-104">Todas as alterações às dimensão de preços personalizados devem estar numa solução separada.</span><span class="sxs-lookup"><span data-stu-id="47709-104">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="47709-105">Essa melhor prática importante fornece flexibilidade no futuro para atualizar ou remover as alterações, conforme necessário, ajudará na reutilização do seu trabalho e facilita a portabilidade destas alterações para outra instância.</span><span class="sxs-lookup"><span data-stu-id="47709-105">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="47709-106">Depois de efetuar todas as alterações necessárias, exporte esta solução como uma **Solução Gerida** e importe-a para outras instâncias para reutilizar a configuração de preços.</span><span class="sxs-lookup"><span data-stu-id="47709-106">After you make the required changes, export this solution as a **Managed solution**, and import it into other instances to reuse your pricing setup.</span></span>

1. <span data-ttu-id="47709-107">Selecione **Definições** > **Soluções** e, em seguida, selecione **Nova**.</span><span class="sxs-lookup"><span data-stu-id="47709-107">Select **Settings** > **Solutions**, and then select **New**.</span></span> 
2. <span data-ttu-id="47709-108">Atribua um nome à solução, **\<your organization name> dimensões de definição de preços**, introduza as informações necessárias restantes e, em seguida, selecione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="47709-108">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then select **Save**.</span></span>

> ![Criar uma solução personalizada para dimensões de definição de preços](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="47709-110">Adicionar todas as entidades obrigatórias e componentes relacionados necessários à Solução de dimensão de preços</span><span class="sxs-lookup"><span data-stu-id="47709-110">Add all required entities and related components to the Pricing dimension solution</span></span>
<span data-ttu-id="47709-111">Terá de adicionar as seguintes entidades do Project Service à Solução de Definição de Preços.</span><span class="sxs-lookup"><span data-stu-id="47709-111">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="47709-112">Conclua os passos indicados neste procedimento para efetuar algumas alterações de esquema importantes na solução de definição de preços, para que as entidades tomem conhecimento das novas dimensões de preços.</span><span class="sxs-lookup"><span data-stu-id="47709-112">Complete the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="47709-113">Selecione **Definições** > **Soluções** e, de seguida, faça clique duplo nas dimensões de preços do **\<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="47709-113">Select **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="47709-114">No Explorador de Soluções, no painel de navegação esquerdo, selecione **Adicionar Existente** > **Entidades**.</span><span class="sxs-lookup"><span data-stu-id="47709-114">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="47709-115">Na caixa de diálogo **Componentes da Solução**, selecione as seguintes entidades:</span><span class="sxs-lookup"><span data-stu-id="47709-115">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="47709-116">Valor Real</span><span class="sxs-lookup"><span data-stu-id="47709-116">Actual</span></span>
- <span data-ttu-id="47709-117">Recurso Reservável</span><span class="sxs-lookup"><span data-stu-id="47709-117">Bookable Resource</span></span>
- <span data-ttu-id="47709-118">Linha de Estimativa</span><span class="sxs-lookup"><span data-stu-id="47709-118">Estimate Line</span></span>
- <span data-ttu-id="47709-119">Tarefa de Projeto</span><span class="sxs-lookup"><span data-stu-id="47709-119">Project Task</span></span>
- <span data-ttu-id="47709-120">Detalhe de Linha de Fatura</span><span class="sxs-lookup"><span data-stu-id="47709-120">Invoice Line Detail</span></span>
- <span data-ttu-id="47709-121">Linha do Diário</span><span class="sxs-lookup"><span data-stu-id="47709-121">Journal Line</span></span>
- <span data-ttu-id="47709-122">Detalhe de Item de Contrato do Projeto</span><span class="sxs-lookup"><span data-stu-id="47709-122">Project Contract Line Detail</span></span>
- <span data-ttu-id="47709-123">Membro da Equipa do Projeto</span><span class="sxs-lookup"><span data-stu-id="47709-123">Project Team Member</span></span>
- <span data-ttu-id="47709-124">Detalhe de Item de Proposta</span><span class="sxs-lookup"><span data-stu-id="47709-124">Quote Line Detail</span></span>
- <span data-ttu-id="47709-125">Margem de Lucro do Preço da Função</span><span class="sxs-lookup"><span data-stu-id="47709-125">Role Price Markup</span></span>
- <span data-ttu-id="47709-126">Preço da Função</span><span class="sxs-lookup"><span data-stu-id="47709-126">Role Price</span></span> 
- <span data-ttu-id="47709-127">Entrada de Hora</span><span class="sxs-lookup"><span data-stu-id="47709-127">Time Entry</span></span> 

> ![Adicionar as entidades existentes à solução de dimensões de definição de preços](media/Existing-entities-to-PD-solution.png)

> ![Selecionar componentes da solução](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="47709-130">Certifique-se de que inclui todos os formulários e vistas para cada uma das entidades selecionadas.</span><span class="sxs-lookup"><span data-stu-id="47709-130">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="47709-131">Quando lhe for pedido para incluir entidades dependentes relativas às entidades selecionadas, selecione **Não**.</span><span class="sxs-lookup"><span data-stu-id="47709-131">When prompted to include any dependent entities for the selected entities, select **No**.</span></span>

> ![Não incluir todos os componentes relacionados](media/Do-not-include-required.png)


