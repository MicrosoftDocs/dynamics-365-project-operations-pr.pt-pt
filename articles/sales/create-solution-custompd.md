---
title: Criar uma solução para dimensões de preços personalizadas
description: Este tópico fornece informações sobre como criar soluções para dimensões de preços personalizadas.
author: Rumant
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 86f4cd2c26ebfca621d1b226b571d220d3b2441e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010350"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="b0f8c-103">Criar uma solução para dimensões de preços personalizadas</span><span class="sxs-lookup"><span data-stu-id="b0f8c-103">Create a solution for custom pricing dimensions</span></span>

 <span data-ttu-id="b0f8c-104">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="b0f8c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span> 

>[!IMPORTANT]
><span data-ttu-id="b0f8c-105">Todas as alterações às dimensão de preços personalizados devem estar numa solução separada.</span><span class="sxs-lookup"><span data-stu-id="b0f8c-105">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="b0f8c-106">Esta melhor prática importante permite a flexibilidade para atualizar ou remover as alterações, conforme necessário, ajuda na reutilização do seu trabalho e facilita a portabilidade de alterações para outras instâncias.</span><span class="sxs-lookup"><span data-stu-id="b0f8c-106">This important best practice allows the flexibility to update or remove changes as needed, helps with re-use of your work, and makes it easier to port changes to other instances.</span></span> <span data-ttu-id="b0f8c-107">Depois de efetuar as alterações necessárias, exporte esta solução como uma solução **Gerida** e, em seguida, importe-a para outras instâncias para reutilização.</span><span class="sxs-lookup"><span data-stu-id="b0f8c-107">After you make the required changes, export this solution as a **Managed** solution, and then import into other instances for reuse.</span></span>

## <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="b0f8c-108">Criar uma solução para dimensões de preços personalizadas</span><span class="sxs-lookup"><span data-stu-id="b0f8c-108">Create a solution for custom pricing dimensions</span></span>

1.  <span data-ttu-id="b0f8c-109">Selecione **Definições** > **Soluções** e, em seguida, selecione **Nova**.</span><span class="sxs-lookup"><span data-stu-id="b0f8c-109">Select **Settings** > **Solutions**, and then select **New**.</span></span>
2.  <span data-ttu-id="b0f8c-110">Nomeie a solução, *Dimensões de preços de <your organization name>*.</span><span class="sxs-lookup"><span data-stu-id="b0f8c-110">Name the solution, *<your organization name> pricing dimensions*.</span></span>
3. <span data-ttu-id="b0f8c-111">Introduza as informações necessárias restantes e selecione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="b0f8c-111">Enter the remaining required information, and then select **Save**.</span></span>

  ![Criação de uma solução de dimensões de preços personalizadas](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="b0f8c-113">Adicionar todas as entidades obrigatórias e componentes relacionados necessários à Solução de dimensão de preços</span><span class="sxs-lookup"><span data-stu-id="b0f8c-113">Add all required entities and related components to the Pricing dimension solution</span></span>

<span data-ttu-id="b0f8c-114">Adicione as seguintes entidades do Project Service à sua solução de preços para fazer alterações importantes na solução de preços.</span><span class="sxs-lookup"><span data-stu-id="b0f8c-114">Add the following Project Service entities to your pricing solution to make important schema changes in the pricing solution.</span></span> <span data-ttu-id="b0f8c-115">Depois de concluído este procedimento, as entidades reconhecerão as novas dimensões de preços.</span><span class="sxs-lookup"><span data-stu-id="b0f8c-115">After you have completed this procedure, the entities will recognize the new pricing dimensions.</span></span>

1.  <span data-ttu-id="b0f8c-116">Selecione **Definições** > **Soluções** e faça duplo clique no **<*nome da sua organização*> dimensões de preços**.</span><span class="sxs-lookup"><span data-stu-id="b0f8c-116">Select **Settings** > **Solutions**, and then double-click **<*your organization name*> pricing dimensions**.</span></span>
2.  <span data-ttu-id="b0f8c-117">No Explorador de Soluções, no painel de navegação esquerdo, selecione **Adicionar Existente** > **Entidades**.</span><span class="sxs-lookup"><span data-stu-id="b0f8c-117">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3.  <span data-ttu-id="b0f8c-118">Na caixa de diálogo **Componentes da Solução**, selecione as seguintes entidades:</span><span class="sxs-lookup"><span data-stu-id="b0f8c-118">In the **Solution Components** dialog box, select the following entities:</span></span>
 
   - <span data-ttu-id="b0f8c-119">**Valor Real**</span><span class="sxs-lookup"><span data-stu-id="b0f8c-119">**Actual**</span></span>
   - <span data-ttu-id="b0f8c-120">**Recurso Reservável**</span><span class="sxs-lookup"><span data-stu-id="b0f8c-120">**Bookable Resource**</span></span>
   - <span data-ttu-id="b0f8c-121">**Linha de Estimativa**</span><span class="sxs-lookup"><span data-stu-id="b0f8c-121">**Estimate Line**</span></span>
   - <span data-ttu-id="b0f8c-122">**Tarefa de Projeto**</span><span class="sxs-lookup"><span data-stu-id="b0f8c-122">**Project Task**</span></span>
   - <span data-ttu-id="b0f8c-123">**Detalhe de Linha de Fatura**</span><span class="sxs-lookup"><span data-stu-id="b0f8c-123">**Invoice Line Detail**</span></span>
   - <span data-ttu-id="b0f8c-124">**Linha do Diário**</span><span class="sxs-lookup"><span data-stu-id="b0f8c-124">**Journal Line**</span></span>
   - <span data-ttu-id="b0f8c-125">**Detalhe de Item de Contrato do Projeto**</span><span class="sxs-lookup"><span data-stu-id="b0f8c-125">**Project Contract Line Detail**</span></span>
   - <span data-ttu-id="b0f8c-126">**Membro da Equipa do Projeto**</span><span class="sxs-lookup"><span data-stu-id="b0f8c-126">**Project Team Member**</span></span>
   - <span data-ttu-id="b0f8c-127">**Detalhe de Item de Proposta**</span><span class="sxs-lookup"><span data-stu-id="b0f8c-127">**Quote Line Detail**</span></span>
   - <span data-ttu-id="b0f8c-128">**Margem de Lucro do Preço da Função**</span><span class="sxs-lookup"><span data-stu-id="b0f8c-128">**Role Price Markup**</span></span>
   - <span data-ttu-id="b0f8c-129">**Preço da Função**</span><span class="sxs-lookup"><span data-stu-id="b0f8c-129">**Role Price**</span></span>
   - <span data-ttu-id="b0f8c-130">**Entrada de Hora**</span><span class="sxs-lookup"><span data-stu-id="b0f8c-130">**Time Entry**</span></span>
 
   ![Adicionar solução de dimensão de preços personalizados de entidades existentes](./media/Existing-entities-to-PD-solution.png)
 
 4. <span data-ttu-id="b0f8c-132">Para cada entidade, reveja os componentes a ser adicionados e a lista final de ativos de entidade para cada entidade.</span><span class="sxs-lookup"><span data-stu-id="b0f8c-132">For each entity, review the components being added and the final list of entity assets for each entity.</span></span> 

   >[!NOTE]
   > <span data-ttu-id="b0f8c-133">Inclua todos os formulários e vistas para cada uma das entidades selecionadas.</span><span class="sxs-lookup"><span data-stu-id="b0f8c-133">Include all forms and views for each of the selected entities.</span></span>

  ![Entidades adicionadas](./media/solution-component-selection.png)


5.  <span data-ttu-id="b0f8c-135">Quando solicitado para incluir quaisquer entidades dependentes para as entidades selecionadas, selecione **Não, não incluir componentes necessários.**</span><span class="sxs-lookup"><span data-stu-id="b0f8c-135">When prompted to include any dependent entities for the selected entities, select **No, do not include required components.**</span></span>

    ![Incluindo entidades dependentes](./media/Do-not-include-required.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]