---
title: Estimar um item de contrato baseado no projeto – lite
description: Este tópico fornece informações sobre a estimativa de um item de contrato baseado em projetos.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2d0d8309fcb4300e33ed2f5933259f99ad7e0d6a
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180431"
---
# <a name="estimate-a-projectbased-contract-line---lite"></a><span data-ttu-id="2af53-103">Estimar um item de contrato baseado no projeto – lite</span><span class="sxs-lookup"><span data-stu-id="2af53-103">Estimate a project–based contract line - lite</span></span>

<span data-ttu-id="2af53-104">_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_</span><span class="sxs-lookup"><span data-stu-id="2af53-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2af53-105">No Dynamics 365 Project Operations, um item de contrato baseado em projetos tem detalhes que ajudam a estimar o custo e as receitas potenciais do trabalho envolvido para entregar o item de contrato.</span><span class="sxs-lookup"><span data-stu-id="2af53-105">In Dynamics 365 Project Operations, a project-based contract line has details that help estimate the cost and potential revenue of the work involved to deliver the contract line.</span></span>

<span data-ttu-id="2af53-106">Para estimar um item de contrato baseado em projetos, aceda ao separador **Detalhe do Item de Contrato** no **Item de Contrato** baseado em projetos.</span><span class="sxs-lookup"><span data-stu-id="2af53-106">To estimate a project-based contract line, go to the **Contract Line Detail** tab on the project-based **Contract Line**.</span></span>  <span data-ttu-id="2af53-107">Existem duas formas de criar uma estimativa num item de contrato baseado em projetos:</span><span class="sxs-lookup"><span data-stu-id="2af53-107">There are two ways to create an estimate on a project-based contract line:</span></span>

   - <span data-ttu-id="2af53-108">Crie uma estimativa diretamente no item de contrato adicionando manualmente detalhes do item de contrato.</span><span class="sxs-lookup"><span data-stu-id="2af53-108">Create an estimate directly on the contract line by manually adding contract line details.</span></span>
   - <span data-ttu-id="2af53-109">Crie um projeto e um plano de projeto e, em seguida, associe o projeto e as tarefas ao item de contrato do projeto.</span><span class="sxs-lookup"><span data-stu-id="2af53-109">Create a project and a project plan, and then associate the project and tasks to the project's contract line.</span></span> <span data-ttu-id="2af53-110">Isto permite o processo através do qual pode importar a estimativa do plano de projeto para o item de contrato com base nos componentes incluídos no item de contrato.</span><span class="sxs-lookup"><span data-stu-id="2af53-110">This enables the process by which you can import the project plan estimate into the contract line based on the components included on the contract line.</span></span>

## <a name="create-an-estimation-directly-on-a-projectbased-contract-line"></a><span data-ttu-id="2af53-111">Criar uma estimativa diretamente num item de contrato baseado no projeto</span><span class="sxs-lookup"><span data-stu-id="2af53-111">Create an estimation directly on a project–based contract line</span></span>

1. <span data-ttu-id="2af53-112">Vá para o item de contrato e selecione o separador **Detalhe do Item de Contrato**. Os itens que cria neste separador são resumidos e exibidos como o **Valor Contratado** para este **Item de Contrato**.</span><span class="sxs-lookup"><span data-stu-id="2af53-112">Go to the contract line and select the **Contract Line Detail** tab. The lines you create on this tab are summarized and display as the **Contracted Value** for this **Contract Line**.</span></span> 
2. <span data-ttu-id="2af53-113">Na subgrelha **Detalhes do Item de Contrato**, selecione **+ Novo Detalhe de Item de Contrato**.</span><span class="sxs-lookup"><span data-stu-id="2af53-113">In the **Contract Line Details** subgrid, select **+ New Contract Line Detail**.</span></span> <span data-ttu-id="2af53-114">Abre-se um controlador de deslize de criação rápida.</span><span class="sxs-lookup"><span data-stu-id="2af53-114">A quick-create slider opens.</span></span> <span data-ttu-id="2af53-115">Os seguintes campos estão disponíveis no formulário **Detalhes do Item de Contrato**:</span><span class="sxs-lookup"><span data-stu-id="2af53-115">The following fields are available on the **Contract Line Details** form:</span></span>

| <span data-ttu-id="2af53-116">Campo</span><span class="sxs-lookup"><span data-stu-id="2af53-116">Field</span></span> | <span data-ttu-id="2af53-117">Localização</span><span class="sxs-lookup"><span data-stu-id="2af53-117">Location</span></span> | <span data-ttu-id="2af53-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="2af53-118">Description</span></span> | <span data-ttu-id="2af53-119">Impacto a jusante</span><span class="sxs-lookup"><span data-stu-id="2af53-119">Downstream impact</span></span> |
| --- | --- | --- | --- |
| <span data-ttu-id="2af53-120">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="2af53-120">**Description**</span></span> | <span data-ttu-id="2af53-121">**Criação Rápida**</span><span class="sxs-lookup"><span data-stu-id="2af53-121">**Quick Create**</span></span> | <span data-ttu-id="2af53-122">Uma descrição da estimativa específica.</span><span class="sxs-lookup"><span data-stu-id="2af53-122">A description of the specific estimate.</span></span> | <span data-ttu-id="2af53-123">Este campo assume a predefinição do detalhe do item de contrato relacionado para os custos que são automaticamente criados.</span><span class="sxs-lookup"><span data-stu-id="2af53-123">This field defaults to the related contract line detail for costs that are automatically created.</span></span> |
| <span data-ttu-id="2af53-124">**Classe de Transação**</span><span class="sxs-lookup"><span data-stu-id="2af53-124">**Transaction Class**</span></span> | <span data-ttu-id="2af53-125">**Criação Rápida**</span><span class="sxs-lookup"><span data-stu-id="2af53-125">**Quick Create**</span></span> | <span data-ttu-id="2af53-126">Esta lista pendente é uma lista de classes de transações incluídas no separador **Geral** do item de contrato baseado em projeto.</span><span class="sxs-lookup"><span data-stu-id="2af53-126">This drop-down is a list of transaction classes included on the **General** tab of the project-based contract line.</span></span> | <span data-ttu-id="2af53-127">Este campo assume a predefinição do detalhe do item de contrato relacionado para os custos que são automaticamente criados.</span><span class="sxs-lookup"><span data-stu-id="2af53-127">This field defaults to the related contract line detail for costs that are automatically created.</span></span> |
| <span data-ttu-id="2af53-128">**Função**</span><span class="sxs-lookup"><span data-stu-id="2af53-128">**Role**</span></span> | <span data-ttu-id="2af53-129">**Criação Rápida**</span><span class="sxs-lookup"><span data-stu-id="2af53-129">**Quick Create**</span></span> | <span data-ttu-id="2af53-130">A função da pessoa que está a realizar este trabalho ou a incorrer nesta despesa.</span><span class="sxs-lookup"><span data-stu-id="2af53-130">The role of the person who is performing this work or incurring this expense.</span></span> | <span data-ttu-id="2af53-131">Este campo assume a predefinição do detalhe do item de contrato relacionado para os custos que são automaticamente criados.</span><span class="sxs-lookup"><span data-stu-id="2af53-131">This field defaults to the related contract line detail for costs that are automatically created.</span></span> |
| <span data-ttu-id="2af53-132">**Categoria**</span><span class="sxs-lookup"><span data-stu-id="2af53-132">**Category**</span></span> | <span data-ttu-id="2af53-133">**Criação Rápida**</span><span class="sxs-lookup"><span data-stu-id="2af53-133">**Quick Create**</span></span> | <span data-ttu-id="2af53-134">A categoria do trabalho ou da despesa.</span><span class="sxs-lookup"><span data-stu-id="2af53-134">The category of the work or expense.</span></span> | <span data-ttu-id="2af53-135">Este campo assume a predefinição do detalhe do item de contrato relacionado para os custos que são automaticamente criados.</span><span class="sxs-lookup"><span data-stu-id="2af53-135">This field defaults to the related contract line detail for costs that are automatically created.</span></span> |
| <span data-ttu-id="2af53-136">**Data de Início**</span><span class="sxs-lookup"><span data-stu-id="2af53-136">**Start Date**</span></span> | <span data-ttu-id="2af53-137">**Criação Rápida**</span><span class="sxs-lookup"><span data-stu-id="2af53-137">**Quick Create**</span></span> | <span data-ttu-id="2af53-138">A data de início do trabalho.</span><span class="sxs-lookup"><span data-stu-id="2af53-138">The start date of the work.</span></span> | <span data-ttu-id="2af53-139">Este campo assume a predefinição do detalhe do item de contrato relacionado para os custos que são automaticamente criados.</span><span class="sxs-lookup"><span data-stu-id="2af53-139">This field defaults to the related contract line detail for costs that are automatically created.</span></span> |
| <span data-ttu-id="2af53-140">**Data de Fim**</span><span class="sxs-lookup"><span data-stu-id="2af53-140">**End Date**</span></span> | <span data-ttu-id="2af53-141">**Criação Rápida**</span><span class="sxs-lookup"><span data-stu-id="2af53-141">**Quick Create**</span></span> | <span data-ttu-id="2af53-142">A data de fim do trabalho.</span><span class="sxs-lookup"><span data-stu-id="2af53-142">The end date of the work.</span></span> | <span data-ttu-id="2af53-143">Este campo assume a predefinição do detalhe do item de contrato para o custo que é automaticamente criado.</span><span class="sxs-lookup"><span data-stu-id="2af53-143">This field defaults to the related contract line detail for the cost that is automatically created.</span></span> |
| <span data-ttu-id="2af53-144">**Unidade de Atribuição de Recursos**</span><span class="sxs-lookup"><span data-stu-id="2af53-144">**Resourcing Unit**</span></span> | <span data-ttu-id="2af53-145">**Criação Rápida**</span><span class="sxs-lookup"><span data-stu-id="2af53-145">**Quick Create**</span></span> | <span data-ttu-id="2af53-146">A unidade de atribuição de recursos que incorre neste custo e requer que o recurso trabalhe nele.</span><span class="sxs-lookup"><span data-stu-id="2af53-146">The resourcing unit that incurs this cost and provies the resource to work on it.</span></span> | <span data-ttu-id="2af53-147">Este campo assume a predefinição do detalhe do item de contrato relacionado para os custos que são automaticamente criados.</span><span class="sxs-lookup"><span data-stu-id="2af53-147">This field defaults to the related contract line detail for costs that are automatically created.</span></span> <span data-ttu-id="2af53-148">Este campo também é utilizado na obtenção do preço de custo.</span><span class="sxs-lookup"><span data-stu-id="2af53-148">This field is also used in cost price retrieval.</span></span> |
| <span data-ttu-id="2af53-149">**Agenda de unidades**</span><span class="sxs-lookup"><span data-stu-id="2af53-149">**Unit schedule**</span></span> | <span data-ttu-id="2af53-150">**Criação rápida**</span><span class="sxs-lookup"><span data-stu-id="2af53-150">**Quick create**</span></span> | <span data-ttu-id="2af53-151">O grupo de unidades do trabalho ou despesa.</span><span class="sxs-lookup"><span data-stu-id="2af53-151">The unit group of the work or expense.</span></span> <span data-ttu-id="2af53-152">As unidades pertencem a uma agenda de unidades ou a um grupo de unidades.</span><span class="sxs-lookup"><span data-stu-id="2af53-152">Units belong to a unit schedule or a group of units.</span></span> <span data-ttu-id="2af53-153">Por exemplo, *milhas* e *quilómetros (Kms)* são unidades que pertencem a um grupo de unidades que descrevem a distância.</span><span class="sxs-lookup"><span data-stu-id="2af53-153">For example, *miles* and *kilometers (Kms)* are units that belong to a group of units that describe distance.</span></span> | <span data-ttu-id="2af53-154">Este campo assume a predefinição do detalhe do item de contrato relacionado para os custos que são automaticamente criados.</span><span class="sxs-lookup"><span data-stu-id="2af53-154">This field defaults to the related contract line detail for costs that are automatically created.</span></span> |
| <span data-ttu-id="2af53-155">**Unidade**</span><span class="sxs-lookup"><span data-stu-id="2af53-155">**Unit**</span></span> | <span data-ttu-id="2af53-156">**Criação Rápida**</span><span class="sxs-lookup"><span data-stu-id="2af53-156">**Quick Create**</span></span> | <span data-ttu-id="2af53-157">A unidade do trabalho ou despesa.</span><span class="sxs-lookup"><span data-stu-id="2af53-157">The unit of work or expense.</span></span> | <span data-ttu-id="2af53-158">Este campo assume a predefinição do detalhe do item de contrato relacionado para os custos que são automaticamente criados.</span><span class="sxs-lookup"><span data-stu-id="2af53-158">This field defaults to the related contract line detail for costs that are automatically created.</span></span> |
| <span data-ttu-id="2af53-159">**Quantidade**</span><span class="sxs-lookup"><span data-stu-id="2af53-159">**Quantity**</span></span> | <span data-ttu-id="2af53-160">**Criação Rápida**</span><span class="sxs-lookup"><span data-stu-id="2af53-160">**Quick Create**</span></span> | <span data-ttu-id="2af53-161">A quantidade do trabalho ou despesa.</span><span class="sxs-lookup"><span data-stu-id="2af53-161">The quantity of work or expense.</span></span> | <span data-ttu-id="2af53-162">Este campo assume a predefinição do detalhe do item de contrato relacionado para os custos que são automaticamente criados.</span><span class="sxs-lookup"><span data-stu-id="2af53-162">This field defaults to the related contract line detail for costs that are automatically created.</span></span> |
| <span data-ttu-id="2af53-163">**Preço unitário**</span><span class="sxs-lookup"><span data-stu-id="2af53-163">**Unit price**</span></span> | <span data-ttu-id="2af53-164">**Criação Rápida**</span><span class="sxs-lookup"><span data-stu-id="2af53-164">**Quick Create**</span></span> | <span data-ttu-id="2af53-165">A taxa de faturação da função que está a desempenhar o trabalho ou o preço de vendas da categoria de despesas.</span><span class="sxs-lookup"><span data-stu-id="2af53-165">The bill rate of the role that is performing the work or the sales price of the expense category.</span></span> <span data-ttu-id="2af53-166">Este campo assume por predefinição o **Tempo** baseado na combinação da função e da unidade de atribuição de recursos na lista de preços do projeto em vigor para a data de início.</span><span class="sxs-lookup"><span data-stu-id="2af53-166">This field defaults for **Time** based on the role and resourcing unit combination on the project price list that is effective for the start date.</span></span> <span data-ttu-id="2af53-167">Para despesas, a predefinição deste campo é da configuração de preços para a categoria de transação na lista de preços do projeto que é efetiva para a data de início.</span><span class="sxs-lookup"><span data-stu-id="2af53-167">For expenses, this field's default is from the price setup for the transaction category in the project price list that is effective for the start date.</span></span> <span data-ttu-id="2af53-168">Se o método de cálculo de preços para a categoria de transação não for o **preço por unidade**, não existe valor predefinido e este campo é deixado em branco.</span><span class="sxs-lookup"><span data-stu-id="2af53-168">If the pricing method for the transaction category is not **price-per-unit**, there is no default, and this field is left blank.</span></span> | <span data-ttu-id="2af53-169">A taxa de custos da função que está a desempenhar o trabalho ou o custo por unidade da categoria de despesas.</span><span class="sxs-lookup"><span data-stu-id="2af53-169">The cost rate of the role that is performing the work, or the cost per unit of the expense category.</span></span> <span data-ttu-id="2af53-170">Este campo assume a predefinição **Tempo baseado na função** e na combinação da unidade de atribuição de recursos na linha de preços de função da lista de preços de custos anexada à unidade de contratação com efeito para a data de início.</span><span class="sxs-lookup"><span data-stu-id="2af53-170">This field defaults for **Time based on the role** and the resourcing unit combination on the role price line of the cost price list attached to the contracting unit effective for the start date.</span></span> <span data-ttu-id="2af53-171">Para despesas, a predefinição deste campo é baseada na linha de preços da categoria da lista de preços de custos anexada à unidade de contratação que é efetiva para a data de início.</span><span class="sxs-lookup"><span data-stu-id="2af53-171">For expenses, this field's default is based on the category price line of the cost price list attached to the contracting unit that is effective for the start date.</span></span> <span data-ttu-id="2af53-172">Se o método de cálculo de preços para a categoria de transação não for o preço por unidade, não existe valor predefinido e este campo é deixado em branco.</span><span class="sxs-lookup"><span data-stu-id="2af53-172">If the pricing method for the transaction category is not price-per-unit, there is no default and this field is left blank.</span></span> |
| <span data-ttu-id="2af53-173">**Imposto Estimado**</span><span class="sxs-lookup"><span data-stu-id="2af53-173">**Estimated Tax**</span></span> | <span data-ttu-id="2af53-174">**Criação Rápida**</span><span class="sxs-lookup"><span data-stu-id="2af53-174">**Quick Create**</span></span> | <span data-ttu-id="2af53-175">O imposto estimado para este trabalho ou despesa como entrada do utilizador.</span><span class="sxs-lookup"><span data-stu-id="2af53-175">The estimated tax for this work or expense as input by the user.</span></span> | <span data-ttu-id="2af53-176">O imposto estimado para este trabalho ou despesa como entrada do utilizador.</span><span class="sxs-lookup"><span data-stu-id="2af53-176">The estimated tax for this work or expense as input by the user.</span></span> |
| <span data-ttu-id="2af53-177">**Montante**</span><span class="sxs-lookup"><span data-stu-id="2af53-177">**Amount**</span></span> | <span data-ttu-id="2af53-178">**Criação Rápida**</span><span class="sxs-lookup"><span data-stu-id="2af53-178">**Quick Create**</span></span> | <span data-ttu-id="2af53-179">Este valor neste campo pode ser adicionado pelo utilizador se os campos **Quantidade** e **Preço** ficarem em branco.</span><span class="sxs-lookup"><span data-stu-id="2af53-179">This value in this field can be added by the user if the **Quantity** and **Price** fields are left blank.</span></span> <span data-ttu-id="2af53-180">Se **Quantidade** e **Preço** forem preenchidos, o campo **Montante** é apenas de leitura e é calculado como **(Quantidade \* Preço Unitário) + Imposto**.</span><span class="sxs-lookup"><span data-stu-id="2af53-180">If **Quantity** and **Price** are filled, the **Amount** field is read-only and is calculated as **(Quantity \* Unit price) + Tax**.</span></span> | &nbsp; |

## <a name="update-prices-on-contract-line-details"></a><span data-ttu-id="2af53-181">Atualizar os preços nos detalhes do item de contrato</span><span class="sxs-lookup"><span data-stu-id="2af53-181">Update prices on contract line details</span></span>

<span data-ttu-id="2af53-182">Se alterar os preços na lista de preços do projeto que está anexada ao contrato ou à lista de preços de custo da unidade contratante, pode atualizar os preços nos detalhes do item de contrato individual para refletir a alteração.</span><span class="sxs-lookup"><span data-stu-id="2af53-182">If you change prices on the project price list that is attached to the contract or the cost price list of the contracting unit, you can refresh the prices on the individual contract line details to reflect the change.</span></span> <span data-ttu-id="2af53-183">Na página **Contrato**, selecione **Recalcular**.</span><span class="sxs-lookup"><span data-stu-id="2af53-183">On the **Contract** page, select **Recalculate**.</span></span> <span data-ttu-id="2af53-184">Um aviso abre para informá-lo que os preços de todas os itens de contrato deste contrato são repostos.</span><span class="sxs-lookup"><span data-stu-id="2af53-184">A warning opens to inform you that prices for all contract lines on this contract are reset.</span></span> <span data-ttu-id="2af53-185">Selecione **Sim** para atualizar os preços tanto para as vendas como para os detalhes do item de contrato de custos.</span><span class="sxs-lookup"><span data-stu-id="2af53-185">Select **Yes** to refresh prices for both sales and cost contract line details.</span></span>

## <a name="access-contract-line-details-for-cost"></a><span data-ttu-id="2af53-186">Aceder aos detalhes do item de contrato para custo</span><span class="sxs-lookup"><span data-stu-id="2af53-186">Access contract line details for cost</span></span>

<span data-ttu-id="2af53-187">No separador **Detalhes do Item de Contrato**, selecione uma linha na grelha para apresentar ações na barra de ferramentas da subgrelha.</span><span class="sxs-lookup"><span data-stu-id="2af53-187">On the **Contract Line Details** tab, select a row in the grid to display actions on the toolbar of the subgrid.</span></span> <span data-ttu-id="2af53-188">A primeira ação na barra de ferramentas da subgrelha é **Abrir Detalhe do Custo**.</span><span class="sxs-lookup"><span data-stu-id="2af53-188">The first action on the subgrid tool bar is **Open Cost Detail**.</span></span> <span data-ttu-id="2af53-189">Para ver a taxa de custos e o montante relacionados para este detalhe do item de contrato, selecione **Abrir Detalhe do Custo**.</span><span class="sxs-lookup"><span data-stu-id="2af53-189">To see the related cost rate and amount for this contract line detail, select **Open Cost Detail**.</span></span> 

> [!NOTE]
> <span data-ttu-id="2af53-190">A alteração da empresa de atribuição de recursos, unidade de atribuição de recursos, quantidade, datas, função ou valores de categoria no detalhe do item de contrato para **Custo** também altera os valores correspondentes no detalhe do item de contrato para **Vendas**.</span><span class="sxs-lookup"><span data-stu-id="2af53-190">Changing the resourcing company, resourcing unit, quantity, dates, role, or category values on the contract line detail for **Cost** also changes the corresponding values on the contract line detail for **Sales**.</span></span>

## <a name="currency-on-contract-line-details-for-cost-and-sales"></a><span data-ttu-id="2af53-191">Moeda em detalhes do item de contrato para custos e vendas</span><span class="sxs-lookup"><span data-stu-id="2af53-191">Currency on contract line details for cost and sales</span></span>

<span data-ttu-id="2af53-192">O detalhe do item de contrato para **Vendas** define a moeda predefinida da lista de preços do projeto que é eficaz para a data de início do detalhe do item de contrato.</span><span class="sxs-lookup"><span data-stu-id="2af53-192">The contract line detail for **Sales** sets the default currency from the project price list that is effective for the start date of the contract line detail.</span></span>

<span data-ttu-id="2af53-193">O detalhe do item de contrato para **Custo** define a moeda predefinida da lista de preços da unidade contratante do contrato que é eficaz para a data de início do detalhe do item de contrato para **Custo**.</span><span class="sxs-lookup"><span data-stu-id="2af53-193">The contract line detail for **Cost** sets the default currency from the price list of the contracting unit of the contract that is effective for the start date of the contract line detail for **Cost**.</span></span>

<span data-ttu-id="2af53-194">Os cálculos de rentabilidade convertem os montantes dos detalhes do item de contrato para **Custo** e **Vendas** na moeda base do ambiente para reportar as margens efetivas e estimadas globais do contrato.</span><span class="sxs-lookup"><span data-stu-id="2af53-194">Profitability calculations convert the amounts for the contract line details for **Cost** and **Sales** into the base currency of the environment to report the overall actual and estimated margins on the contract.</span></span>

> [!NOTE]
> <span data-ttu-id="2af53-195">Podem ocorrer erros de arredondamento de moeda e margens alteradas devido à falta de taxas de câmbio efetivas da data.</span><span class="sxs-lookup"><span data-stu-id="2af53-195">Currency rounding errors and changed margins could occur because of the lack of date effective exchange rates.</span></span> <span data-ttu-id="2af53-196">Utilize estes cálculos em contratos de projeto apenas como aproximações e não para relatórios estatutários ou outros que exijam maior precisão de arredondamento e sensibilização para a efetividade da data para as taxas de câmbio.</span><span class="sxs-lookup"><span data-stu-id="2af53-196">Use these calculations on project contracts only as approximations and not for actual statutory or other reporting that requires higher precision of rounding and awareness of date effectivity for exchange rates.</span></span>