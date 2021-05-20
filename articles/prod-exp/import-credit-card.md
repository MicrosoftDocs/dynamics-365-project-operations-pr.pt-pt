---
title: Importar e manter transações de cartões de crédito
description: Este tópico explica como importar e manter as transações de cartões de crédito relacionados com despesas. Estas transações podem ser configuradas de modo a que sejam automaticamente importadas numa agenda recorrente, ou podem ser importadas manualmente conforme são necessárias.
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: c434356c08e8490931bd60ea5b10fe2706cb0f51
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/27/2021
ms.locfileid: "5951088"
---
# <a name="import-and-maintain-credit-card-transactions"></a><span data-ttu-id="b4c35-104">Importar e manter transações de cartões de crédito</span><span class="sxs-lookup"><span data-stu-id="b4c35-104">Import and maintain credit card transactions</span></span>

<span data-ttu-id="b4c35-105">As transações de cartões de crédito relacionadas com despesas podem ser configuradas de modo a que sejam automaticamente importadas num horário recorrente.</span><span class="sxs-lookup"><span data-stu-id="b4c35-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="b4c35-106">Em alternativa, as transações podem ser importadas manualmente conforme são necessárias.</span><span class="sxs-lookup"><span data-stu-id="b4c35-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="b4c35-107">As transações de cartões de crédito são importadas através da entidade de dados de transações de cartões de crédito.</span><span class="sxs-lookup"><span data-stu-id="b4c35-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

<span data-ttu-id="b4c35-108">Para obter mais informações sobre entidades de dados, consulte [Entidades de dados](/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).</span><span class="sxs-lookup"><span data-stu-id="b4c35-108">For more information about data entities, see [Data entities](/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="b4c35-109">Importar transações de cartões de crédito</span><span class="sxs-lookup"><span data-stu-id="b4c35-109">Import credit card transactions</span></span>

1. <span data-ttu-id="b4c35-110">Na página de **transações de cartões de crédito**, selecione **Importar transações**.</span><span class="sxs-lookup"><span data-stu-id="b4c35-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="b4c35-111">Se estiver a abrir a gestão de dados pela primeira vez, o sistema deve atualizar a lista de entidades de dados antes de poder continuar.</span><span class="sxs-lookup"><span data-stu-id="b4c35-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="b4c35-112">No campo **Nome**, introduza uma descrição única da tarefa de importação.</span><span class="sxs-lookup"><span data-stu-id="b4c35-112">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="b4c35-113">No campo **formato de dados de origem**, selecione o formato do ficheiro que contém as transações de cartão de crédito a importar.</span><span class="sxs-lookup"><span data-stu-id="b4c35-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="b4c35-114">Selecione **Carregar** e, em seguida, encontre e selecione o ficheiro para importar.</span><span class="sxs-lookup"><span data-stu-id="b4c35-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="b4c35-115">Depois de o ficheiro ter sido carregado, validar o mapeamento do ficheiro de transações de cartões de crédito e as colunas da entidade de dados de transações de cartões de Crédito, selecionando a ligação **Ver mapa** no mosaico.</span><span class="sxs-lookup"><span data-stu-id="b4c35-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="b4c35-116">Se houver erros de mapeamento, ou se tiver de alterar o mapeamento, faça as alterações de mapeamento a partir do separador de **Visualização de mapeamento** ou do separador **Detalhes do mapeamento**.</span><span class="sxs-lookup"><span data-stu-id="b4c35-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="b4c35-117">Para automatizar as transações de cartões de crédito, selecione **Criar tarefa de dados recorrente**.</span><span class="sxs-lookup"><span data-stu-id="b4c35-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="b4c35-118">Em seguida, pode definir a periodicidade que define a frequência com que as transações com cartão de crédito devem ser importadas.</span><span class="sxs-lookup"><span data-stu-id="b4c35-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="b4c35-119">Quando tiver terminado, selecione **OK**.</span><span class="sxs-lookup"><span data-stu-id="b4c35-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="b4c35-120">Para importar o ficheiro selecionado agora, selecione **Importar**.</span><span class="sxs-lookup"><span data-stu-id="b4c35-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="b4c35-121">Se ocorrerem erros durante a importação, pode ver o registo de execução ou os dados de teste para ver os erros que deve corrigir para ajudar a garantir uma importação bem sucedida.</span><span class="sxs-lookup"><span data-stu-id="b4c35-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="b4c35-122">Se tiver de importar mais do que um formato de ficheiro, deve criar tarefas de importação separadas para cada tipo de formato.</span><span class="sxs-lookup"><span data-stu-id="b4c35-122">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="b4c35-123">Voltar a atribuir as transações de cartões de crédito para funcionários despedidos</span><span class="sxs-lookup"><span data-stu-id="b4c35-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="b4c35-124">Após terminar um registo de funcionário, a conta Active Directory Domain Services (AD DS) do funcionário é desativada.</span><span class="sxs-lookup"><span data-stu-id="b4c35-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="b4c35-125">No entanto, pode haver transações ativas de cartões de crédito que ainda devem ser gastas e reembolsadas.</span><span class="sxs-lookup"><span data-stu-id="b4c35-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="b4c35-126">A partir da página de **transações de cartões de crédito**, pode reatribuir o funcionário a qualquer transação de cartão de crédito onde o funcionário associado tenha sido despedido.</span><span class="sxs-lookup"><span data-stu-id="b4c35-126">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="b4c35-127">Selecione uma ou mais transações de cartões de crédito e, em seguida, selecione **Reatribuir transações**.</span><span class="sxs-lookup"><span data-stu-id="b4c35-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="b4c35-128">Em seguida, pode selecionar outro funcionário para atribuir as transações do cartão de crédito.</span><span class="sxs-lookup"><span data-stu-id="b4c35-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="b4c35-129">Após a reatribuição das transações de cartões de crédito, podem ser selecionadas para um relatório de despesas e pagas através do processo habitual de reembolso do relatório de despesas.</span><span class="sxs-lookup"><span data-stu-id="b4c35-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]