---
title: Gerir estimativas de receitas
description: Este tópico fornece informações sobre como gerir e trabalhar com estimativas de receitas para projetos.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b63346f56db8b906e5aa45940465bdb18e3df480
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279017"
---
# <a name="manage-revenue-estimates"></a><span data-ttu-id="ce500-103">Gerir estimativas de receitas</span><span class="sxs-lookup"><span data-stu-id="ce500-103">Manage revenue estimates</span></span>

<span data-ttu-id="ce500-104">_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_</span><span class="sxs-lookup"><span data-stu-id="ce500-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="ce500-105">É possível criar, calcular, publicar, reverter ou eliminar estimativas de receitas.</span><span class="sxs-lookup"><span data-stu-id="ce500-105">You can create, calculate, post, reverse, or eliminate revenue estimates.</span></span> <span data-ttu-id="ce500-106">Pode fazê-lo manualmente ou utilizando um processo periódico.</span><span class="sxs-lookup"><span data-stu-id="ce500-106">You can do this either manually or by using a periodic process.</span></span> <span data-ttu-id="ce500-107">Este tópico fornece informações sobre como gerir e trabalhar com estimativas de receitas para projetos.</span><span class="sxs-lookup"><span data-stu-id="ce500-107">This topic provides information about how to work with revenue estimates for projects.</span></span>

### <a name="manage-revenue-estimates-manually"></a><span data-ttu-id="ce500-108">Gerir estimativas de receitas manualmente</span><span class="sxs-lookup"><span data-stu-id="ce500-108">Manage revenue estimates manually</span></span>

<span data-ttu-id="ce500-109">No projeto de estimativa de receitas de preço fixo ou na página **Inquérito de estimativa** (**Gestão de projetos e contabilística** > **Relatórios e inquéritos** > **Estimativas de inquéritos e relatórios**), selecione **Estimativas**.</span><span class="sxs-lookup"><span data-stu-id="ce500-109">On the fixed price revenue estimate project or the **Estimate inquiry** page (**Project management and accounting** > **Reports and inquiries** > **Estimates inquiries and reports**), select **Estimates**.</span></span>

### <a name="manage-revenue-estimates-using-a-periodic-process"></a><span data-ttu-id="ce500-110">Gerir estimativas de receitas utilizando um processo periódico</span><span class="sxs-lookup"><span data-stu-id="ce500-110">Manage revenue estimates using a periodic process</span></span>

<span data-ttu-id="ce500-111">Vá a **Gestão de projetos e contabilística** > **Periódicas** > **Estimativas** e selecione o processo correspondente.</span><span class="sxs-lookup"><span data-stu-id="ce500-111">Go to **Project management and accounting** > **Periodic** > **Estimates** and select the corresponding process.</span></span>

## <a name="create-a-revenue-estimate"></a><span data-ttu-id="ce500-112">Criar uma estimativa de receitas</span><span class="sxs-lookup"><span data-stu-id="ce500-112">Create a revenue estimate</span></span>

<span data-ttu-id="ce500-113">Conclua os seguintes passos para criar uma estimativa de receita.</span><span class="sxs-lookup"><span data-stu-id="ce500-113">Complete the following steps to create a revenue estimate.</span></span> 

1. <span data-ttu-id="ce500-114">Vá a **Gestão de projetos e contabilística** > **Periódica** > **Estimativas**.</span><span class="sxs-lookup"><span data-stu-id="ce500-114">Go to **Project management and accounting** > **Periodic** > **Estimates**.</span></span>
2. <span data-ttu-id="ce500-115">Selecione **Novo**.</span><span class="sxs-lookup"><span data-stu-id="ce500-115">Select **New**.</span></span> <span data-ttu-id="ce500-116">Na página **Criação de estimativa**, selecione os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="ce500-116">On the **Estimate creation** page, select the following parameters:</span></span>

   - <span data-ttu-id="ce500-117">**Código de período**: este código determina a frequência com que as estimativas são publicadas.</span><span class="sxs-lookup"><span data-stu-id="ce500-117">**Period code**: This code determines how frequently estimates are posted.</span></span>
   - <span data-ttu-id="ce500-118">**Data de estimativa**: a data em que a estimativa é processada.</span><span class="sxs-lookup"><span data-stu-id="ce500-118">**Estimate date**: The date the estimate is processed.</span></span>
   - <span data-ttu-id="ce500-119">**Contínua**: selecione esta caixa de verificação para criar estimativas apenas se as estimativas forem publicadas no período anterior, ou se a estimativa for a primeira estimativa que foi criada.</span><span class="sxs-lookup"><span data-stu-id="ce500-119">**Continuous**: Select this check box to create estimates only if estimates were posted in the previous period, or if the estimate is the first estimate that has been created.</span></span> <span data-ttu-id="ce500-120">Se esta não for selecionada, as estimativas são criadas mesmo que as estimativas não tenham sido publicadas no período anterior.</span><span class="sxs-lookup"><span data-stu-id="ce500-120">If this is not selected, estimates are created even if estimates were not posted in the previous period.</span></span>
   - <span data-ttu-id="ce500-121">**Método de custo para conclusão**: defina como estimar o restante trabalho do projeto.</span><span class="sxs-lookup"><span data-stu-id="ce500-121">**Cost to complete method**: Define how to estimate the remaining project work.</span></span> <span data-ttu-id="ce500-122">Para obter mais informações, consulte [Métodos de custo para conclusão](cost-complete-methods.md).</span><span class="sxs-lookup"><span data-stu-id="ce500-122">For more information, see [Cost to complete methods](cost-complete-methods.md).</span></span>
   - <span data-ttu-id="ce500-123">**Método de conclusão**: selecione um método de conclusão a partir das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="ce500-123">**Completion method**: Select a completion method from the following options:</span></span>
     - <span data-ttu-id="ce500-124">**Automático**: a percentagem de conclusão é calculada automaticamente e com base nas linhas de custo incluídas no cálculo.</span><span class="sxs-lookup"><span data-stu-id="ce500-124">**Automatic**: The completion percentage is calculated automatically and based on the cost lines included in the calculation.</span></span> <span data-ttu-id="ce500-125">O modelo de custo define as linhas de custo que estão incluídas.</span><span class="sxs-lookup"><span data-stu-id="ce500-125">The cost template defines the cost lines that are included.</span></span>
     - <span data-ttu-id="ce500-126">**Manual**: a percentagem de conclusão é igual à percentagem de conclusão da última estimativa.</span><span class="sxs-lookup"><span data-stu-id="ce500-126">**Manual**: The completion percentage equals the completion percentage of the last estimate.</span></span> <span data-ttu-id="ce500-127">Após a criação da estimativa, pode alterar o **Cálculo manual** na página **Estimativas**.</span><span class="sxs-lookup"><span data-stu-id="ce500-127">After the estimate is created, you can change the **Manual calculation** on the **Estimates** page.</span></span>
     - <span data-ttu-id="ce500-128">**Modelo Do custo**: uma combinação dos métodos automáticos e manuais.</span><span class="sxs-lookup"><span data-stu-id="ce500-128">**From cost template**: A combination of the automatic and manual methods.</span></span> <span data-ttu-id="ce500-129">Esta opção é definida automaticamente ou manualmente, dependendo do valor predefinido no modelo de custos.</span><span class="sxs-lookup"><span data-stu-id="ce500-129">This option is set automatically or manually, depending on the default value in the cost template.</span></span>
   - <span data-ttu-id="ce500-130">**Modelo de previsão**: selecione um modelo de previsão para a estimativa.</span><span class="sxs-lookup"><span data-stu-id="ce500-130">**Forecast model**: Select a forecast model for the estimate.</span></span>
   - <span data-ttu-id="ce500-131">**Imprimir lista de estimativas**: crie e mostre uma lista de estimativas.</span><span class="sxs-lookup"><span data-stu-id="ce500-131">**Print estimate list**: Create and show an estimate list.</span></span> <span data-ttu-id="ce500-132">A lista contém o estado da função atual.</span><span class="sxs-lookup"><span data-stu-id="ce500-132">The list contains the status of the current function.</span></span> <span data-ttu-id="ce500-133">Pode imprimir qualquer aviso sobre a estimativa do relatório.</span><span class="sxs-lookup"><span data-stu-id="ce500-133">You can print any warnings about the estimate on the report.</span></span> <span data-ttu-id="ce500-134">As seguintes condições fazem com que as advertências apareçam na lista de estimativas:</span><span class="sxs-lookup"><span data-stu-id="ce500-134">The following conditions cause warnings to appear in the estimate list:</span></span>
     - <span data-ttu-id="ce500-135">Uma percentagem de conclusão superior a 100 por cento.</span><span class="sxs-lookup"><span data-stu-id="ce500-135">A completion percentage of more than 100 percent.</span></span>
     - <span data-ttu-id="ce500-136">Uma percentagem de conclusão inferior a zero por cento.</span><span class="sxs-lookup"><span data-stu-id="ce500-136">A completion percentage less than zero percent.</span></span>
     - <span data-ttu-id="ce500-137">Um montante negativo na coluna **Para concluir**.</span><span class="sxs-lookup"><span data-stu-id="ce500-137">A negative amount in the **To complete** column.</span></span>
     - <span data-ttu-id="ce500-138">Uma estimativa sem o valor do contrato correspondente.</span><span class="sxs-lookup"><span data-stu-id="ce500-138">An estimate with no corresponding contract amount.</span></span>
     - <span data-ttu-id="ce500-139">Uma estimativa sem estimativa de custos anexada.</span><span class="sxs-lookup"><span data-stu-id="ce500-139">An estimate with no attached cost estimate.</span></span>
   - <span data-ttu-id="ce500-140">**Mostrar Registo de Informações**: selecione esta opção para receber uma mensagem que contenha informações sobre os projetos de estimativa que foram processados quando o trabalho foi executado.</span><span class="sxs-lookup"><span data-stu-id="ce500-140">**Show Infolog**: Select this option to receive a message that contains information about the estimate projects that were processed when the job was run.</span></span>


## <a name="post-wip-or-accruals"></a><span data-ttu-id="ce500-141">Pós-WIP ou acréscimos</span><span class="sxs-lookup"><span data-stu-id="ce500-141">Post WIP or accruals</span></span>

<span data-ttu-id="ce500-142">Após a avaliação das estimativas, estas são mantidas, diminuídas ou aumentadas.</span><span class="sxs-lookup"><span data-stu-id="ce500-142">After the estimates are evaluated, they are maintained, decreased, or increased.</span></span> <span data-ttu-id="ce500-143">Em seguida, pode publicar o WIP quando trabalhar com o princípio de avaliação do **Contrato concluído**, ou publicar os acréscimos quando trabalhar com o princípio de avaliação de **Percentagem de conclusão**.</span><span class="sxs-lookup"><span data-stu-id="ce500-143">You can then post the WIP when you work with the **Completed contract** assessment principle, or post the accruals when you work with the **Completed percentage** assessment principle.</span></span>
  
<span data-ttu-id="ce500-144">O estado do período de estimativa muda de **Criada** para **Publicada**.</span><span class="sxs-lookup"><span data-stu-id="ce500-144">The estimate period status changes from **Created** to **Posted**.</span></span>

## <a name="reverse-wip-or-accruals"></a><span data-ttu-id="ce500-145">Reverter WIP ou acréscimos</span><span class="sxs-lookup"><span data-stu-id="ce500-145">Reverse WIP or accruals</span></span>

<span data-ttu-id="ce500-146">Use a opção de reversão para creditar WIP ou acréscimos já publicados e, em seguida, crie estimativas para o período.</span><span class="sxs-lookup"><span data-stu-id="ce500-146">Use the reverse option to credit already posted WIP or accruals, and then create estimates for the period.</span></span>

> [!NOTE]
> <span data-ttu-id="ce500-147">Para inverter um período que se encontra entre outros períodos, reverta os períodos de estimativa necessários e, em seguida, volte a publicá-los.</span><span class="sxs-lookup"><span data-stu-id="ce500-147">To reverse a period that is in between other periods, reverse the necessary estimate periods and then repost them.</span></span> <span data-ttu-id="ce500-148">Como todos os períodos subsequentes dependem das estimativas do período anterior, não ignore quaisquer períodos.</span><span class="sxs-lookup"><span data-stu-id="ce500-148">Because all subsequent periods depend on the estimates from the previous period, don't skip any periods.</span></span>

## <a name="eliminate-the-estimate-project-and-finish-the-project"></a><span data-ttu-id="ce500-149">Elimine o projeto de estimativa e termine o projeto</span><span class="sxs-lookup"><span data-stu-id="ce500-149">Eliminate the estimate project and finish the project</span></span>

<span data-ttu-id="ce500-150">O passo final no processo de estimativa é eliminar o projeto de estimativa e terminar o projeto de preço fixo quando a percentagem de conclusão chega aos 100 por cento.</span><span class="sxs-lookup"><span data-stu-id="ce500-150">The final step in the estimate process is to eliminate the estimate project and end the fixed price project when the percentage of completion reaches 100 percent.</span></span>

<span data-ttu-id="ce500-151">O seguinte ocorre quando executa a eliminação:</span><span class="sxs-lookup"><span data-stu-id="ce500-151">The following occurs when you run the elimination:</span></span>

- <span data-ttu-id="ce500-152">Para um projeto de preço fixo com contrato concluído, os valores WIP são limpos das contas de saldo e publica as contas de lucro e perda.</span><span class="sxs-lookup"><span data-stu-id="ce500-152">For a fixed price project with a completed contract, the WIP values clear from the balance accounts and post to the profit and loss accounts.</span></span>
- <span data-ttu-id="ce500-153">Para um projeto de preço fixo com uma percentagem de conclusão, os acréscimos são retirados das contas de lucro e perda.</span><span class="sxs-lookup"><span data-stu-id="ce500-153">For a fixed-price project with a completed percentage, the accruals are removed from the profit and loss accounts.</span></span>

<span data-ttu-id="ce500-154">A estimativa altera o estado para **Eliminado**.</span><span class="sxs-lookup"><span data-stu-id="ce500-154">The estimate changes the status to **Eliminated**.</span></span>

> [!NOTE]
> <span data-ttu-id="ce500-155">Em casos especiais, a percentagem pode estender-se para além dos 100 por cento.</span><span class="sxs-lookup"><span data-stu-id="ce500-155">In special cases, the percentage can extend beyond 100 percent.</span></span> <span data-ttu-id="ce500-156">Quando isso acontecer, reduza a percentagem de conclusão utilizando o **Método Definir custo para conclusão para zero** para chegar aos 100 por cento.</span><span class="sxs-lookup"><span data-stu-id="ce500-156">When this happens, reduce the percentage of completion by using the **Set cost to complete to zero method** to reach 100 percent.</span></span>

## <a name="reverse-elimination"></a><span data-ttu-id="ce500-157">Reverter eliminação</span><span class="sxs-lookup"><span data-stu-id="ce500-157">Reverse elimination</span></span>

1. <span data-ttu-id="ce500-158">Aceda a **Gestão de projetos e contabilística** > **Periódica** > **Estimativas** > **Reverter eliminação**.</span><span class="sxs-lookup"><span data-stu-id="ce500-158">Go to **Project management and accounting** > **Periodic** > **Estimates** > **Reverse elimination**.</span></span> 
2. <span data-ttu-id="ce500-159">No Painel de Ação, no separador **Processo**, no grupo **Manter**, selecione **Estimativa**.</span><span class="sxs-lookup"><span data-stu-id="ce500-159">On the Action Pane, on the **Process** tab, in the **Maintain** group, select **Estimate**.</span></span> 
3. <span data-ttu-id="ce500-160">Selecione **Reverter eliminação**.</span><span class="sxs-lookup"><span data-stu-id="ce500-160">Select **Reverse elimination**.</span></span>

<span data-ttu-id="ce500-161">Utilize esta página para reverter todas as eliminações com uma data de estimativa especificada e com um estado de estimativa de **Eliminada**.</span><span class="sxs-lookup"><span data-stu-id="ce500-161">Use this page to reverse all eliminations with a specified estimate date and with an estimate status of **Eliminated**.</span></span> <span data-ttu-id="ce500-162">O estado de transação muda depois de selecionar os campos apropriados.</span><span class="sxs-lookup"><span data-stu-id="ce500-162">The transaction status changes after you select the appropriate fields.</span></span>

<span data-ttu-id="ce500-163">Isto também altera automaticamente o estado do projeto para **Em processo** se a fase do projeto estiver definida para Concluída.</span><span class="sxs-lookup"><span data-stu-id="ce500-163">This also automatically changes the project status to **In process** if the project stage is set to finished.</span></span> <span data-ttu-id="ce500-164">O estado de estimativa do período de projeto volta a **Publicado**.</span><span class="sxs-lookup"><span data-stu-id="ce500-164">The estimate status of the project period changes back to **Posted**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]