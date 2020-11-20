---
title: Corresponder um recibo à uma despesa com OCR
description: Este tópico fornece informações sobre o processamento de reconhecimento de caracteres óticos (OCR) para obter recibos.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 55f63c8c092942b73a55c9d86d867bca600f42e5
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124337"
---
# <a name="match-a-receipt-to-an-expense-using-ocr"></a><span data-ttu-id="28d9b-103">Corresponder um recibo à uma despesa com OCR</span><span class="sxs-lookup"><span data-stu-id="28d9b-103">Match a receipt to an expense using OCR</span></span>

<span data-ttu-id="28d9b-104">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="28d9b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="28d9b-105">A entrada de despesas foi reforçada através da introdução do processamento de reconhecimento de caracteres óticos (OCR) para obter receitas.</span><span class="sxs-lookup"><span data-stu-id="28d9b-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="28d9b-106">Esta funcionalidade destina-se a melhorar a experiência do utilizador ao criar relatórios de despesas.</span><span class="sxs-lookup"><span data-stu-id="28d9b-106">This functionality is designed to improve the user experience when creating expense reports.</span></span>

## <a name="key-features"></a><span data-ttu-id="28d9b-107">Funcionalidades principais</span><span class="sxs-lookup"><span data-stu-id="28d9b-107">Key features</span></span>

- <span data-ttu-id="28d9b-108">O sistema extrai o nome do comerciante, a data e o valor total dos recibos.</span><span class="sxs-lookup"><span data-stu-id="28d9b-108">The system extracts the merchant name, date, and total amount from receipts.</span></span>
- <span data-ttu-id="28d9b-109">O sistema tentará combinar recibos não ligados a transações de despesas não associadas.</span><span class="sxs-lookup"><span data-stu-id="28d9b-109">The system will try to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="28d9b-110">Pode criar transações de despesas inseridas manualmente a partir de recibos.</span><span class="sxs-lookup"><span data-stu-id="28d9b-110">You can create manually entered expense transactions from receipts.</span></span>

## <a name="attach-receipts-to-an-expense-report"></a><span data-ttu-id="28d9b-111">Anexar recibos a um relatório de despesas</span><span class="sxs-lookup"><span data-stu-id="28d9b-111">Attach receipts to an expense report</span></span>

<span data-ttu-id="28d9b-112">Para anexar automaticamente recibos que incluam transações de cartões de crédito quando um relatório de despesas é criado, siga os passos seguintes.</span><span class="sxs-lookup"><span data-stu-id="28d9b-112">To automatically attach receipts that include credit card transactions when an expense report is created, complete the following steps.</span></span>

  1. <span data-ttu-id="28d9b-113">Abra área de trabalho da **gestão de despesas**.</span><span class="sxs-lookup"><span data-stu-id="28d9b-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="28d9b-114">No separador **Recibos**, verifique se existem recibos não anexados.</span><span class="sxs-lookup"><span data-stu-id="28d9b-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="28d9b-115">Também pode carregar recibos no separador **Recibos**.</span><span class="sxs-lookup"><span data-stu-id="28d9b-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="28d9b-116">No separador **Despesas**, verifique se existem despesas não anexadas.</span><span class="sxs-lookup"><span data-stu-id="28d9b-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="28d9b-117">Normalmente, o Administrador de despesas importa estas despesas do cartão de crédito do prestador.</span><span class="sxs-lookup"><span data-stu-id="28d9b-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="28d9b-118">Selecione **novo relatório de despesas**.</span><span class="sxs-lookup"><span data-stu-id="28d9b-118">Select **New expense report**.</span></span> <span data-ttu-id="28d9b-119">Note que agora também pode incluir despesas e recibos quando criar um relatório de despesas.</span><span class="sxs-lookup"><span data-stu-id="28d9b-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="28d9b-120">Se adicionar despesas e recibos, é desencadeada uma correspondência automática dos recibos com as despesas.</span><span class="sxs-lookup"><span data-stu-id="28d9b-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

## <a name="create-or-match-receipts-to-an-expense-report"></a><span data-ttu-id="28d9b-121">Criar ou fazer corresponder recibos a um relatório de despesas</span><span class="sxs-lookup"><span data-stu-id="28d9b-121">Create or match receipts to an expense report</span></span>
<span data-ttu-id="28d9b-122">Para criar uma despesa, ou fazer corresponder a uma despesa de um recibo, complete os seguintes passos.</span><span class="sxs-lookup"><span data-stu-id="28d9b-122">To create an expense, or match an expense from a receipt, complete the following steps.</span></span>

  1. <span data-ttu-id="28d9b-123">Num relatório de despesas, no separador **Recibos**, anexe um recibo selecionando **Adicionar recibos**.</span><span class="sxs-lookup"><span data-stu-id="28d9b-123">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="28d9b-124">Por baixo da imagem carregada do recibo, observe as opções **Criar** e **Corresponder**.</span><span class="sxs-lookup"><span data-stu-id="28d9b-124">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="28d9b-125">Selecione **Criar** para criar uma transação de despesas inserida manualmente e preencher os valores extraídos do recibo.</span><span class="sxs-lookup"><span data-stu-id="28d9b-125">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="28d9b-126">Se selecionar **Corresponder**, o sistema tenta corresponder uma despesa existente ao recibo.</span><span class="sxs-lookup"><span data-stu-id="28d9b-126">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="28d9b-127">Instalação</span><span class="sxs-lookup"><span data-stu-id="28d9b-127">Installation</span></span>

<span data-ttu-id="28d9b-128">Para utilizar estas capacidades de despesas avançadas, instale o suplemento do Serviço de Gestão de Despesas para o Microsoft Dynamics 365 Finance, e ligue as funcionalidades na sua instância.</span><span class="sxs-lookup"><span data-stu-id="28d9b-128">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="28d9b-129">Pode aceder ao suplemento do seu projeto em Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="28d9b-129">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="28d9b-130">Iniciar sessão no LCS e abrir o ambiente desejado.</span><span class="sxs-lookup"><span data-stu-id="28d9b-130">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="28d9b-131">Aceda a **Todos os detalhes**.</span><span class="sxs-lookup"><span data-stu-id="28d9b-131">Go to **Full details**.</span></span>
3. <span data-ttu-id="28d9b-132">Selecione **Manter** ou desloque-se para baixo para FastTab dos **Suplementos do ambiente**.</span><span class="sxs-lookup"><span data-stu-id="28d9b-132">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="28d9b-133">Selecione **Instalar um novo suplemento**.</span><span class="sxs-lookup"><span data-stu-id="28d9b-133">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="28d9b-134">Selecione **Serviço de Gestão de Despesas**.</span><span class="sxs-lookup"><span data-stu-id="28d9b-134">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="28d9b-135">Siga o guia de instalação e concorde com os termos e condições.</span><span class="sxs-lookup"><span data-stu-id="28d9b-135">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="28d9b-136">Selecione **Instalar**.</span><span class="sxs-lookup"><span data-stu-id="28d9b-136">Select **Install**.</span></span>

<span data-ttu-id="28d9b-137">Na área de trabalho de **Gestão de recursos**, ligue as seguintes funcionalidades:</span><span class="sxs-lookup"><span data-stu-id="28d9b-137">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="28d9b-138">Relatórios de despesas reinventados</span><span class="sxs-lookup"><span data-stu-id="28d9b-138">Expense reports re-imagined</span></span>
- <span data-ttu-id="28d9b-139">Correspondência automática e criar despesas a partir do recibo</span><span class="sxs-lookup"><span data-stu-id="28d9b-139">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="28d9b-140">Quando liga estas funcionalidades, ocorrem as seguintes ações:</span><span class="sxs-lookup"><span data-stu-id="28d9b-140">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="28d9b-141">A área de trabalho existente de **gestão de despesas** é substituída pela nova área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="28d9b-141">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="28d9b-142">Um novo item de menu para visibilidade do campo de despesas é adicionado.</span><span class="sxs-lookup"><span data-stu-id="28d9b-142">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="28d9b-143">Pode ainda abrir a página de **relatórios de despesas** anteriores ao aceder a **Gestão de Despesas > As minhas despesas > Relatórios de despesas**.</span><span class="sxs-lookup"><span data-stu-id="28d9b-143">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="28d9b-144">Fluxos de trabalho e quaisquer aprovações ainda o levam à página de relatórios de despesas existentes.</span><span class="sxs-lookup"><span data-stu-id="28d9b-144">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="28d9b-145">Os recibos serão processados através do Microsoft Azure Cognitive Services, e os metadados serão extraídos e adicionados.</span><span class="sxs-lookup"><span data-stu-id="28d9b-145">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="28d9b-146">Uma opção é adicionada que lhe permite criar um relatório de despesas que inclui recibos não anexados.</span><span class="sxs-lookup"><span data-stu-id="28d9b-146">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="28d9b-147">Uma opção que é adicionada aos relatórios de despesas permite criar uma linha de despesas a partir de um recibo, ou tenta combinar um recibo existente com uma linha de despesas existente.</span><span class="sxs-lookup"><span data-stu-id="28d9b-147">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="28d9b-148">Perguntas mais frequentes</span><span class="sxs-lookup"><span data-stu-id="28d9b-148">Frequently asked questions</span></span>

<span data-ttu-id="28d9b-149">**A Microsoft usa os meus dados para os seus modelos?**</span><span class="sxs-lookup"><span data-stu-id="28d9b-149">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="28d9b-150">Não, a Microsoft construiu um modelo de aprendizagem automática geral para o seu serviço de processamento de recibos.</span><span class="sxs-lookup"><span data-stu-id="28d9b-150">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="28d9b-151">Este modelo não se baseia nos recibos que envia.</span><span class="sxs-lookup"><span data-stu-id="28d9b-151">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="28d9b-152">**Onde é que esta funcionalidade está disponível e processada?**</span><span class="sxs-lookup"><span data-stu-id="28d9b-152">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="28d9b-153">Atualmente, os Estados Unidos são compatíveis.</span><span class="sxs-lookup"><span data-stu-id="28d9b-153">Currently, the United States is supported.</span></span>

<span data-ttu-id="28d9b-154">**Para onde vão os meus recibos?**</span><span class="sxs-lookup"><span data-stu-id="28d9b-154">**Where do my receipts go?**</span></span>

<span data-ttu-id="28d9b-155">A contabilidade entrará em contacto com os Serviços Cognitivos para extrair os dados de campo.</span><span class="sxs-lookup"><span data-stu-id="28d9b-155">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="28d9b-156">Os Serviços Cognitivos conservarão uma cópia do seu recibo durante 24 horas enquanto ocorre o processamento.</span><span class="sxs-lookup"><span data-stu-id="28d9b-156">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="28d9b-157">Após o processamento estar concluído, os Serviços Cognitivos removerão o recibo.</span><span class="sxs-lookup"><span data-stu-id="28d9b-157">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="28d9b-158">Os recibos ainda estão guardados na Contabilidade.</span><span class="sxs-lookup"><span data-stu-id="28d9b-158">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="28d9b-159">Para obter mais informações, consulte [Ativar o compreensão do recibo com a nova capacidade do Reconhecedor de Formato](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="28d9b-159">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>
