---
title: Entrada de despesas (lite)
description: Este tópico fornece informações sobre como trabalhar com a entrada de despesas numa implementação leve.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 536c961593599df8e7e2986f92259b0e690eae8b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121097"
---
# <a name="expense-entry-lite"></a><span data-ttu-id="c3d98-103">Entrada de despesas (lite)</span><span class="sxs-lookup"><span data-stu-id="c3d98-103">Expense entry (lite)</span></span>

<span data-ttu-id="c3d98-104">_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_</span><span class="sxs-lookup"><span data-stu-id="c3d98-104">_**Applies to:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c3d98-105">A gestão de despesas básica ou leve é a capacidade de registar as despesas simples.</span><span class="sxs-lookup"><span data-stu-id="c3d98-105">Basic, or lite, expense management is the capability to record simple expenses.</span></span> <span data-ttu-id="c3d98-106">Pode registar as despesas num projeto e, em seguida, o aprovador do projeto irá revê-los e aprová-los.</span><span class="sxs-lookup"><span data-stu-id="c3d98-106">You can record expenses against a project, and then the project approver will review and approve them.</span></span>

<span data-ttu-id="c3d98-107">Para mais informações sobre as capacidades de despesas no Dynamics 365 Project Operations, consulte [Descrição geral da despesa](expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c3d98-107">For more information about expense capabilities in Dynamics 365 Project Operations, see [Expense overview](expense-overview.md).</span></span>

## <a name="capture-a-basic-expense"></a><span data-ttu-id="c3d98-108">Capturar uma despesa básica</span><span class="sxs-lookup"><span data-stu-id="c3d98-108">Capture a basic expense</span></span>

<span data-ttu-id="c3d98-109">Pode capturar as suas despesas para poder submetê-las ao aprovador.</span><span class="sxs-lookup"><span data-stu-id="c3d98-109">You can capture your expenses so that you can submit them to the approver.</span></span>

1. <span data-ttu-id="c3d98-110">Vá para **Despesas** e selecione **Novo**.</span><span class="sxs-lookup"><span data-stu-id="c3d98-110">Go to **Expenses**, and select **New**.</span></span>
2. <span data-ttu-id="c3d98-111">Na página **Nova Despesa**, introduza as informações da despesa necessárias e, em seguida, selecione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="c3d98-111">On the **New Expense** page, enter the required expense information, and then select **Save**.</span></span>

## <a name="submit-a-basic-expense"></a><span data-ttu-id="c3d98-112">Submeter uma despesa básica</span><span class="sxs-lookup"><span data-stu-id="c3d98-112">Submit a basic expense</span></span>

<span data-ttu-id="c3d98-113">Depois de concluir a captura de todas as suas despesas, e quando estiver pronto para aprová-las, tem de submetê-las.</span><span class="sxs-lookup"><span data-stu-id="c3d98-113">After you've finished capturing all your expenses, and you're ready to have them approved, you must submit them.</span></span>

1. <span data-ttu-id="c3d98-114">Vá para **Despesas** e selecione uma despesa.</span><span class="sxs-lookup"><span data-stu-id="c3d98-114">Go to **Expenses**, and select an expense.</span></span> <span data-ttu-id="c3d98-115">Ou selecione todas as despesas através da caixa de verificação no cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="c3d98-115">Or, select all the expenses by using the check box on the header.</span></span>
2. <span data-ttu-id="c3d98-116">Selecione **Submeter**.</span><span class="sxs-lookup"><span data-stu-id="c3d98-116">Select **Submit**.</span></span> <span data-ttu-id="c3d98-117">O sistema processa as entradas selecionadas e, em seguida, cria pedidos de aprovação de despesas.</span><span class="sxs-lookup"><span data-stu-id="c3d98-117">The system processes the selected entries and then creates expense approval requests.</span></span>

## <a name="recall-a-basic-expense"></a><span data-ttu-id="c3d98-118">Recuperar uma despesa básica</span><span class="sxs-lookup"><span data-stu-id="c3d98-118">Recall a basic expense</span></span>

<span data-ttu-id="c3d98-119">Quando submete uma despesa por engano, podes recuperá-la.</span><span class="sxs-lookup"><span data-stu-id="c3d98-119">When you submit an expense by mistake, you can recall it.</span></span> <span data-ttu-id="c3d98-120">O tempo necessário para recuperar uma entrada de despesa depende da sua fase de aprovação.</span><span class="sxs-lookup"><span data-stu-id="c3d98-120">The time that is required to recall an expense entry depends on its approval stage.</span></span>  <span data-ttu-id="c3d98-121">Se o aprovador ainda não tiver aprovado a entrada, a recuperação poderá ocorrer imediatamente.</span><span class="sxs-lookup"><span data-stu-id="c3d98-121">If the approver hasn't yet approved the entry, the recall can occur immediately.</span></span> <span data-ttu-id="c3d98-122">No entanto, se a entrada já tiver sido aprovada, é pedido ao aprovador para aprovar a recuperação e reverter as transações.</span><span class="sxs-lookup"><span data-stu-id="c3d98-122">However, if the entry has already been approved, the approver is asked to approve the recall and reverse the transactions.</span></span>

1. <span data-ttu-id="c3d98-123">Vá para **Despesas** e, depois, na lista de despesas, selecione a despesa a recuperar.</span><span class="sxs-lookup"><span data-stu-id="c3d98-123">Go to **Expenses**, and then, in the list of expenses, select the expense to recall.</span></span>
2. <span data-ttu-id="c3d98-124">Selecione **Recuperar**.</span><span class="sxs-lookup"><span data-stu-id="c3d98-124">Select **Recall**.</span></span> <span data-ttu-id="c3d98-125">Se a entrada de despesa ainda não tiver sido aprovada, o sistema recupera-a imediatamente.</span><span class="sxs-lookup"><span data-stu-id="c3d98-125">If the expense entry hasn't yet been approved, the system immediately recalls it.</span></span> <span data-ttu-id="c3d98-126">Se a entrada de despesa já tiver sido aprovada, é criado um pedido de recuperação para notificar o aprovador que pretende reverter a despesa.</span><span class="sxs-lookup"><span data-stu-id="c3d98-126">If the expense entry has already been approved, a recall request is created to notify the approver that you want to reverse the expense.</span></span> <span data-ttu-id="c3d98-127">Em seguida, o aprovador confirmará que a reversão pode ser feita e a entrada será devolvida.</span><span class="sxs-lookup"><span data-stu-id="c3d98-127">The approver will then confirm that the reversal can be done, and the entry will be returned.</span></span>

## <a name="delete-a-basic-expense"></a><span data-ttu-id="c3d98-128">Eliminar uma despesa básica</span><span class="sxs-lookup"><span data-stu-id="c3d98-128">Delete a basic expense</span></span>

<span data-ttu-id="c3d98-129">As despesas que ainda não foram submetidas podem ser eliminadas.</span><span class="sxs-lookup"><span data-stu-id="c3d98-129">Expenses that haven't yet been submitted can be deleted.</span></span> <span data-ttu-id="c3d98-130">Para eliminar uma despesa que já foi submetida, primeiro tem de recuperá-la.</span><span class="sxs-lookup"><span data-stu-id="c3d98-130">To delete an expense that has already been submitted, you must first recall it.</span></span>

## <a name="see-also"></a><span data-ttu-id="c3d98-131">Consulte também</span><span class="sxs-lookup"><span data-stu-id="c3d98-131">See also</span></span>

- [<span data-ttu-id="c3d98-132">Descrição geral das aprovações</span><span class="sxs-lookup"><span data-stu-id="c3d98-132">Approvals overview</span></span>](../approvals/approvals-overview.md)
