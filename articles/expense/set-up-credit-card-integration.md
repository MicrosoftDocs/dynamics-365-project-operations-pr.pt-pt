---
title: Configurar integração de cartão de crédito
description: Este tópico explica como trabalhar com transações de cartões de crédito relacionados com despesas.
author: suvaidya
manager: AnnBe
ms.date: 04/02/2021
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
ms.openlocfilehash: 72ff98f5985af4362cde3c9914e0d20247f1f09a
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866697"
---
# <a name="set-up-credit-card-integration"></a><span data-ttu-id="483af-103">Configurar integração de cartão de crédito</span><span class="sxs-lookup"><span data-stu-id="483af-103">Set up credit card integration</span></span>

<span data-ttu-id="483af-104">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="483af-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="483af-105">As transações de cartões de crédito relacionadas com despesas podem ser configuradas de modo a que sejam automaticamente importadas num horário recorrente.</span><span class="sxs-lookup"><span data-stu-id="483af-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="483af-106">Em alternativa, as transações podem ser importadas manualmente conforme são necessárias.</span><span class="sxs-lookup"><span data-stu-id="483af-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="483af-107">As transações de cartões de crédito são importadas através da entidade de dados de transações de Cartões de crédito.</span><span class="sxs-lookup"><span data-stu-id="483af-107">The credit card transactions are imported through the credit card transactions data entity.</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="483af-108">Importar transações de cartões de crédito</span><span class="sxs-lookup"><span data-stu-id="483af-108">Import credit card transactions</span></span>

<span data-ttu-id="483af-109">Para importar transações de cartões de crédito, siga estes passos:</span><span class="sxs-lookup"><span data-stu-id="483af-109">To import credit card transactions, follow these steps:</span></span>

1. <span data-ttu-id="483af-110">Na página de **transações de cartões de crédito**, selecione **Importar transações**.</span><span class="sxs-lookup"><span data-stu-id="483af-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="483af-111">Se estiver a abrir a gestão de dados pela primeira vez, o sistema deve atualizar a lista de entidades de dados antes de poder continuar.</span><span class="sxs-lookup"><span data-stu-id="483af-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="483af-112">No campo **Nome**, insira uma descrição única para o trabalho de importação.</span><span class="sxs-lookup"><span data-stu-id="483af-112">In the **Name** field, enter a unique description for the import job.</span></span>
3. <span data-ttu-id="483af-113">No campo **formato de dados de origem**, selecione o formato do ficheiro que contém as transações de cartão de crédito a importar.</span><span class="sxs-lookup"><span data-stu-id="483af-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="483af-114">Selecione **Carregar** e, em seguida, encontre e selecione o ficheiro para importar.</span><span class="sxs-lookup"><span data-stu-id="483af-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="483af-115">Depois de o ficheiro ter sido carregado, validar o mapeamento do ficheiro de transações de cartões de crédito e as colunas da entidade de dados de transações de Cartões de crédito, selecionando a ligação **Ver mapa** no mosaico.</span><span class="sxs-lookup"><span data-stu-id="483af-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="483af-116">Se houver erros de mapeamento, ou se tiver de alterar o mapeamento, faça as alterações de mapeamento a partir do separador de **Visualização de mapeamento** ou do separador **Detalhes do mapeamento**.</span><span class="sxs-lookup"><span data-stu-id="483af-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="483af-117">Para automatizar as transações de cartões de crédito, selecione **Criar tarefa de dados recorrente**.</span><span class="sxs-lookup"><span data-stu-id="483af-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="483af-118">Em seguida, pode definir a periodicidade que define a frequência com que as transações com cartão de crédito devem ser importadas.</span><span class="sxs-lookup"><span data-stu-id="483af-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="483af-119">Quando tiver terminado, selecione **OK**.</span><span class="sxs-lookup"><span data-stu-id="483af-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="483af-120">Para importar o ficheiro selecionado agora, selecione **Importar**.</span><span class="sxs-lookup"><span data-stu-id="483af-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="483af-121">Se ocorrerem erros durante a importação, pode ver o registo de execução ou os dados de teste para ver os erros que deve corrigir para ajudar a garantir uma importação bem sucedida.</span><span class="sxs-lookup"><span data-stu-id="483af-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help ensure a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="483af-122">Se precisar de importar mais de um formato de ficheiro, deve criar trabalhos de importação separados para cada tipo de formato.</span><span class="sxs-lookup"><span data-stu-id="483af-122">If you need to import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="483af-123">Voltar a atribuir as transações de cartões de crédito para funcionários despedidos</span><span class="sxs-lookup"><span data-stu-id="483af-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="483af-124">Após terminar um registo de funcionário, a conta Active Directory Domain Services (AD DS) do funcionário é desativada.</span><span class="sxs-lookup"><span data-stu-id="483af-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="483af-125">No entanto, pode haver transações ativas de cartões de crédito que ainda devem ser gastas e reembolsadas.</span><span class="sxs-lookup"><span data-stu-id="483af-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="483af-126">Na página de **Transações de cartões de crédito**, pode reatribuir o empregado para qualquer transação de cartão de crédito onde o empregado associado tenha sido despedido.</span><span class="sxs-lookup"><span data-stu-id="483af-126">On the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="483af-127">Selecione uma ou mais transações de cartões de crédito e, em seguida, selecione **Reatribuir transações**.</span><span class="sxs-lookup"><span data-stu-id="483af-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="483af-128">Em seguida, pode selecionar outro funcionário para atribuir as transações do cartão de crédito.</span><span class="sxs-lookup"><span data-stu-id="483af-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="483af-129">Após a reatribuição das transações de cartões de crédito, podem ser selecionadas para um relatório de despesas e pagas através do processo habitual de reembolso do relatório de despesas.</span><span class="sxs-lookup"><span data-stu-id="483af-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>

## <a name="delete-credit-card-transactions"></a><span data-ttu-id="483af-130">Eliminar transações de cartões de crédito</span><span class="sxs-lookup"><span data-stu-id="483af-130">Delete credit card transactions</span></span> 

<span data-ttu-id="483af-131">Por vezes, após a importação de transações com cartão de crédito, certas transações podem ter de ser eliminadas.</span><span class="sxs-lookup"><span data-stu-id="483af-131">Sometimes, after credit card transactions are imported, certain transactions may need to be deleted.</span></span> <span data-ttu-id="483af-132">Isto pode ser porque as transações são duplicadas ou porque os dados podem não ser precisos.</span><span class="sxs-lookup"><span data-stu-id="483af-132">This could be because the transactions are duplicates or because the data might isn't accurate.</span></span> <span data-ttu-id="483af-133">Os administradores podem utilizar a função **Eliminar as transações de cartões de crédito** para selecionar e eliminar transações de cartões de crédito que estejam **não anexadas** a um relatório de despesas.</span><span class="sxs-lookup"><span data-stu-id="483af-133">Admins can use the **"Delete credit card transactions"** feature to select and delete credit card transactions that are **not attached** to an expense report.</span></span> 

1. <span data-ttu-id="483af-134">Ir a **Tarefas periódicas** > **Eliminar transações de cartões de crédito**.</span><span class="sxs-lookup"><span data-stu-id="483af-134">Go to **Periodic tasks** > **Delete credit card transactions**.</span></span>
2. <span data-ttu-id="483af-135">Selecione **Filtrar** e forneça informações para identificar os registos a incluir.</span><span class="sxs-lookup"><span data-stu-id="483af-135">Select **Filter** and provide information to identify the records to include.</span></span>
3. <span data-ttu-id="483af-136">Selecione **Ok** para eliminar os registos.</span><span class="sxs-lookup"><span data-stu-id="483af-136">Select **OK** to delete the records.</span></span> 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
