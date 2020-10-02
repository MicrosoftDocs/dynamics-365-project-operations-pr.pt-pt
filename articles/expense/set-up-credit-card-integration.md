---
title: Configurar integração de cartão de crédito
description: Este tópico explica como importar e manter as transações de cartões de crédito relacionados com despesas.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 483775e1334a281026dbfaf214d06d235255f13e
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896835"
---
# <a name="set-up-credit-card-integration"></a><span data-ttu-id="ce746-103">Configurar integração de cartão de crédito</span><span class="sxs-lookup"><span data-stu-id="ce746-103">Set up credit card integration</span></span>

<span data-ttu-id="ce746-104">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="ce746-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ce746-105">As transações de cartões de crédito relacionadas com despesas podem ser configuradas de modo a que sejam automaticamente importadas num horário recorrente.</span><span class="sxs-lookup"><span data-stu-id="ce746-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="ce746-106">Em alternativa, as transações podem ser importadas manualmente conforme são necessárias.</span><span class="sxs-lookup"><span data-stu-id="ce746-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="ce746-107">As transações de cartões de crédito são importadas através da entidade de dados de transações de cartões de crédito.</span><span class="sxs-lookup"><span data-stu-id="ce746-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="ce746-108">Importar transações de cartões de crédito</span><span class="sxs-lookup"><span data-stu-id="ce746-108">Import credit card transactions</span></span>

1. <span data-ttu-id="ce746-109">Na página de **transações de cartões de crédito**, selecione **Importar transações**.</span><span class="sxs-lookup"><span data-stu-id="ce746-109">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="ce746-110">Se estiver a abrir a gestão de dados pela primeira vez, o sistema deve atualizar a lista de entidades de dados antes de poder continuar.</span><span class="sxs-lookup"><span data-stu-id="ce746-110">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="ce746-111">No campo **Nome**, introduza uma descrição única da tarefa de importação.</span><span class="sxs-lookup"><span data-stu-id="ce746-111">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="ce746-112">No campo **formato de dados de origem**, selecione o formato do ficheiro que contém as transações de cartão de crédito a importar.</span><span class="sxs-lookup"><span data-stu-id="ce746-112">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="ce746-113">Selecione **Carregar** e, em seguida, encontre e selecione o ficheiro para importar.</span><span class="sxs-lookup"><span data-stu-id="ce746-113">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="ce746-114">Depois de o ficheiro ter sido carregado, validar o mapeamento do ficheiro de transações de cartões de crédito e as colunas da entidade de dados de transações de cartões de Crédito, selecionando a ligação **Ver mapa** no mosaico.</span><span class="sxs-lookup"><span data-stu-id="ce746-114">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="ce746-115">Se houver erros de mapeamento, ou se tiver de alterar o mapeamento, faça as alterações de mapeamento a partir do separador de **Visualização de mapeamento** ou do separador **Detalhes do mapeamento**.</span><span class="sxs-lookup"><span data-stu-id="ce746-115">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="ce746-116">Para automatizar as transações de cartões de crédito, selecione **Criar tarefa de dados recorrente**.</span><span class="sxs-lookup"><span data-stu-id="ce746-116">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="ce746-117">Em seguida, pode definir a periodicidade que define a frequência com que as transações com cartão de crédito devem ser importadas.</span><span class="sxs-lookup"><span data-stu-id="ce746-117">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="ce746-118">Quando tiver terminado, selecione **OK**.</span><span class="sxs-lookup"><span data-stu-id="ce746-118">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="ce746-119">Para importar o ficheiro selecionado agora, selecione **Importar**.</span><span class="sxs-lookup"><span data-stu-id="ce746-119">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="ce746-120">Se ocorrerem erros durante a importação, pode ver o registo de execução ou os dados de teste para ver os erros que deve corrigir para ajudar a garantir uma importação bem sucedida.</span><span class="sxs-lookup"><span data-stu-id="ce746-120">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="ce746-121">Se tiver de importar mais do que um formato de ficheiro, deve criar tarefas de importação separadas para cada tipo de formato.</span><span class="sxs-lookup"><span data-stu-id="ce746-121">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="ce746-122">Voltar a atribuir as transações de cartões de crédito para funcionários despedidos</span><span class="sxs-lookup"><span data-stu-id="ce746-122">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="ce746-123">Após terminar um registo de funcionário, a conta Active Directory Domain Services (AD DS) do funcionário é desativada.</span><span class="sxs-lookup"><span data-stu-id="ce746-123">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="ce746-124">No entanto, pode haver transações ativas de cartões de crédito que ainda devem ser gastas e reembolsadas.</span><span class="sxs-lookup"><span data-stu-id="ce746-124">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="ce746-125">A partir da página de **transações de cartões de crédito**, pode reatribuir o funcionário a qualquer transação de cartão de crédito onde o funcionário associado tenha sido despedido.</span><span class="sxs-lookup"><span data-stu-id="ce746-125">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="ce746-126">Selecione uma ou mais transações de cartões de crédito e, em seguida, selecione **Reatribuir transações**.</span><span class="sxs-lookup"><span data-stu-id="ce746-126">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="ce746-127">Em seguida, pode selecionar outro funcionário para atribuir as transações do cartão de crédito.</span><span class="sxs-lookup"><span data-stu-id="ce746-127">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="ce746-128">Após a reatribuição das transações de cartões de crédito, podem ser selecionadas para um relatório de despesas e pagas através do processo habitual de reembolso do relatório de despesas.</span><span class="sxs-lookup"><span data-stu-id="ce746-128">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>
