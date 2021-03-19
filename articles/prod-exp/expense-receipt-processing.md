---
title: Processamento de recibos de despesas
description: Este tópico fornece informações sobre o processamento de reconhecimento de caracteres óticos (OCR) para obter recibos. Esta funcionalidade destina-se a melhorar a experiência do utilizador ao criar relatórios de despesas no Microsoft Dynamics 365 Finance.
author: stsporen
manager: AnnBe
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 57ef67412eb3c5795559e4f6d011e97c4d7a1338
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271817"
---
# <a name="expense-receipt-processing"></a><span data-ttu-id="39245-104">Processamento de recibos de despesas</span><span class="sxs-lookup"><span data-stu-id="39245-104">Expense receipt processing</span></span>

<span data-ttu-id="39245-105">A entrada de despesas foi reforçada através da introdução do processamento de reconhecimento de caracteres óticos (OCR) para obter receitas.</span><span class="sxs-lookup"><span data-stu-id="39245-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="39245-106">Esta funcionalidade destina-se a melhorar a experiência do utilizador ao criar relatórios de despesas.</span><span class="sxs-lookup"><span data-stu-id="39245-106">This feature is designed to improve the user experience when expense reports are created.</span></span>

## <a name="key-features"></a><span data-ttu-id="39245-107">Funcionalidades principais</span><span class="sxs-lookup"><span data-stu-id="39245-107">Key features</span></span>

- <span data-ttu-id="39245-108">O nome do comerciante, a data e o valor total são extraídos dos recibos.</span><span class="sxs-lookup"><span data-stu-id="39245-108">The merchant name, date, and total amount are extracted from receipts.</span></span>
- <span data-ttu-id="39245-109">A funcionalidade tenta combinar recibos não ligados a transações de despesas não associadas.</span><span class="sxs-lookup"><span data-stu-id="39245-109">The feature tries to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="39245-110">Os utilizadores podem criar transações de despesas inseridas manualmente a partir de recibos.</span><span class="sxs-lookup"><span data-stu-id="39245-110">Users can create manually entered expense transactions from receipts.</span></span>

## <a name="usage-examples"></a><span data-ttu-id="39245-111">Exemplos de utilização</span><span class="sxs-lookup"><span data-stu-id="39245-111">Usage examples</span></span>

<span data-ttu-id="39245-112">Para anexar automaticamente recibos que incluam transações de cartões de crédito quando um relatório de despesas é criado, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="39245-112">To automatically attach receipts that include credit card transactions when an expense report is created, do the following:</span></span>

  1. <span data-ttu-id="39245-113">Abra área de trabalho da **gestão de despesas**.</span><span class="sxs-lookup"><span data-stu-id="39245-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="39245-114">No separador **Recibos**, verifique se existem recibos não anexados.</span><span class="sxs-lookup"><span data-stu-id="39245-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="39245-115">Também pode carregar recibos no separador **Recibos**.</span><span class="sxs-lookup"><span data-stu-id="39245-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="39245-116">No separador **Despesas**, verifique se existem despesas não anexadas.</span><span class="sxs-lookup"><span data-stu-id="39245-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="39245-117">Normalmente, o Administrador de despesas importa estas despesas do cartão de crédito do prestador.</span><span class="sxs-lookup"><span data-stu-id="39245-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="39245-118">Selecione **novo relatório de despesas**.</span><span class="sxs-lookup"><span data-stu-id="39245-118">Select **New expense report**.</span></span> <span data-ttu-id="39245-119">Note que agora também pode incluir despesas e recibos quando criar um relatório de despesas.</span><span class="sxs-lookup"><span data-stu-id="39245-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="39245-120">Se adicionar despesas e recibos, é desencadeada uma correspondência automática dos recibos com as despesas.</span><span class="sxs-lookup"><span data-stu-id="39245-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

<span data-ttu-id="39245-121">Para criar uma despesa, ou fazer corresponder a uma despesa de um recibo, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="39245-121">To create an expense, or match an expense from a receipt, do the following:</span></span>

  1. <span data-ttu-id="39245-122">Num relatório de despesas, no separador **Recibos**, anexe um recibo selecionando **Adicionar recibos**.</span><span class="sxs-lookup"><span data-stu-id="39245-122">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="39245-123">Por baixo da imagem carregada do recibo, observe as opções **Criar** e **Corresponder**.</span><span class="sxs-lookup"><span data-stu-id="39245-123">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="39245-124">Selecione **Criar** para criar uma transação de despesas inserida manualmente e preencher os valores extraídos do recibo.</span><span class="sxs-lookup"><span data-stu-id="39245-124">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="39245-125">Se selecionar **Corresponder**, o sistema tenta corresponder uma despesa existente ao recibo.</span><span class="sxs-lookup"><span data-stu-id="39245-125">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="39245-126">Instalação</span><span class="sxs-lookup"><span data-stu-id="39245-126">Installation</span></span>

<span data-ttu-id="39245-127">Esta funcionalidade funciona em combinação com a funcionalidade **Relatórios de despesas reimaginados** para ajudar a simplificar a experiência de despesas.</span><span class="sxs-lookup"><span data-stu-id="39245-127">This feature works in combination with the **Expense reports re-imagined** feature to help simplify the expense experience.</span></span> <span data-ttu-id="39245-128">Esta funcionalidade está disponível apenas para ambientes Camada 2+, que são Sandbox e Produção.</span><span class="sxs-lookup"><span data-stu-id="39245-128">This feature is only available for Tier 2+ environments, which are Sandbox and Production.</span></span>

<span data-ttu-id="39245-129">Para utilizar estas capacidades de despesas avançadas, instale o suplemento do Serviço de Gestão de Despesas para o Microsoft Dynamics 365 Finance, e ligue as funcionalidades na sua instância.</span><span class="sxs-lookup"><span data-stu-id="39245-129">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="39245-130">Pode aceder ao suplemento do seu projeto em Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="39245-130">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="39245-131">Iniciar sessão no LCS e abrir o ambiente desejado.</span><span class="sxs-lookup"><span data-stu-id="39245-131">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="39245-132">Aceda a **Todos os detalhes**.</span><span class="sxs-lookup"><span data-stu-id="39245-132">Go to **Full details**.</span></span>
3. <span data-ttu-id="39245-133">Selecione **Manter** ou desloque-se para baixo para FastTab dos **Suplementos do ambiente**.</span><span class="sxs-lookup"><span data-stu-id="39245-133">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="39245-134">Selecione **Instalar um novo suplemento**.</span><span class="sxs-lookup"><span data-stu-id="39245-134">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="39245-135">Selecione **Serviço de Gestão de Despesas**.</span><span class="sxs-lookup"><span data-stu-id="39245-135">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="39245-136">Siga o guia de instalação e concorde com os termos e condições.</span><span class="sxs-lookup"><span data-stu-id="39245-136">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="39245-137">Selecione **Instalar**.</span><span class="sxs-lookup"><span data-stu-id="39245-137">Select **Install**.</span></span>

<span data-ttu-id="39245-138">Na área de trabalho de **Gestão de recursos**, ligue as seguintes funcionalidades:</span><span class="sxs-lookup"><span data-stu-id="39245-138">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="39245-139">Relatórios de despesas reinventados</span><span class="sxs-lookup"><span data-stu-id="39245-139">Expense reports re-imagined</span></span>
- <span data-ttu-id="39245-140">Correspondência automática e criar despesas a partir do recibo</span><span class="sxs-lookup"><span data-stu-id="39245-140">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="39245-141">Quando liga estas funcionalidades, ocorrem as seguintes ações:</span><span class="sxs-lookup"><span data-stu-id="39245-141">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="39245-142">A área de trabalho existente de **gestão de despesas** é substituída pela nova área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="39245-142">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="39245-143">Um novo item de menu para visibilidade do campo de despesas é adicionado.</span><span class="sxs-lookup"><span data-stu-id="39245-143">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="39245-144">Pode ainda abrir a página de **relatórios de despesas** anteriores ao aceder a **Gestão de Despesas > As minhas despesas > Relatórios de despesas**.</span><span class="sxs-lookup"><span data-stu-id="39245-144">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="39245-145">Fluxos de trabalho e quaisquer aprovações ainda o levam à página de relatórios de despesas existentes.</span><span class="sxs-lookup"><span data-stu-id="39245-145">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="39245-146">Os recibos serão processados através do Microsoft Azure Cognitive Services, e os metadados serão extraídos e adicionados.</span><span class="sxs-lookup"><span data-stu-id="39245-146">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="39245-147">Uma opção é adicionada que lhe permite criar um relatório de despesas que inclui recibos não anexados.</span><span class="sxs-lookup"><span data-stu-id="39245-147">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="39245-148">Uma opção que é adicionada aos relatórios de despesas permite criar uma linha de despesas a partir de um recibo, ou tenta combinar um recibo existente com uma linha de despesas existente.</span><span class="sxs-lookup"><span data-stu-id="39245-148">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

<span data-ttu-id="39245-149">Para obter mais informações sobre os relatórios de despesas reimaginados, consulte [Relatórios de despesas reimaginados](ExpenseWorkspaceNew.md).</span><span class="sxs-lookup"><span data-stu-id="39245-149">For more information about the Expense reports re-imagined feature, see [Expense reports reimagined](ExpenseWorkspaceNew.md).</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="39245-150">Perguntas mais frequentes</span><span class="sxs-lookup"><span data-stu-id="39245-150">Frequently asked questions</span></span>

<span data-ttu-id="39245-151">**A Microsoft usa os meus dados para os seus modelos?**</span><span class="sxs-lookup"><span data-stu-id="39245-151">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="39245-152">Não, a Microsoft construiu um modelo de aprendizagem automática geral para o seu serviço de processamento de recibos.</span><span class="sxs-lookup"><span data-stu-id="39245-152">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="39245-153">Este modelo não se baseia nos recibos que envia.</span><span class="sxs-lookup"><span data-stu-id="39245-153">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="39245-154">**Onde é que esta funcionalidade está disponível e processada?**</span><span class="sxs-lookup"><span data-stu-id="39245-154">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="39245-155">Atualmente, os Estados Unidos são compatíveis.</span><span class="sxs-lookup"><span data-stu-id="39245-155">Currently, the United States is supported.</span></span>

<span data-ttu-id="39245-156">**Para onde vão os meus recibos?**</span><span class="sxs-lookup"><span data-stu-id="39245-156">**Where do my receipts go?**</span></span>

<span data-ttu-id="39245-157">A contabilidade entrará em contacto com os Serviços Cognitivos para extrair os dados de campo.</span><span class="sxs-lookup"><span data-stu-id="39245-157">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="39245-158">Os Serviços Cognitivos conservarão uma cópia do seu recibo durante 24 horas enquanto ocorre o processamento.</span><span class="sxs-lookup"><span data-stu-id="39245-158">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="39245-159">Após o processamento estar concluído, os Serviços Cognitivos removerão o recibo.</span><span class="sxs-lookup"><span data-stu-id="39245-159">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="39245-160">Os recibos ainda estão guardados na Contabilidade.</span><span class="sxs-lookup"><span data-stu-id="39245-160">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="39245-161">Para obter mais informações, consulte [Ativar o compreensão do recibo com a nova capacidade do Reconhecedor de Formato](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="39245-161">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]