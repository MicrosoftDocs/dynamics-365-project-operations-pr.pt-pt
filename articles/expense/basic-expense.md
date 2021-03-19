---
title: Entrada de despesas (lite)
description: Este tópico fornece informações sobre como trabalhar com a entrada de despesas numa implementação leve.
author: stsporen
manager: AnnBe
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 539d0ba6be6f49a6f0509595a0776ef67135496d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276767"
---
# <a name="expense-entry-lite"></a><span data-ttu-id="eb70b-103">Entrada de despesas (lite)</span><span class="sxs-lookup"><span data-stu-id="eb70b-103">Expense entry (lite)</span></span>

<span data-ttu-id="eb70b-104">_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_</span><span class="sxs-lookup"><span data-stu-id="eb70b-104">_**Applies to:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="eb70b-105">A gestão de despesas básica ou leve é a capacidade de registar as despesas simples.</span><span class="sxs-lookup"><span data-stu-id="eb70b-105">Basic, or lite, expense management is the capability to record simple expenses.</span></span> <span data-ttu-id="eb70b-106">Pode registar as despesas num projeto e, em seguida, o aprovador do projeto irá revê-los e aprová-los.</span><span class="sxs-lookup"><span data-stu-id="eb70b-106">You can record expenses against a project, and then the project approver will review and approve them.</span></span>

<span data-ttu-id="eb70b-107">Para obter mais informações sobre as capacidades de despesas no Dynamics 365 Project Operations, consulte [Descrição geral de Despesas](expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="eb70b-107">For more information about expense capabilities in Dynamics 365 Project Operations, see [Expense overview](expense-overview.md).</span></span>

## <a name="capture-a-basic-expense"></a><span data-ttu-id="eb70b-108">Capturar uma despesa básica</span><span class="sxs-lookup"><span data-stu-id="eb70b-108">Capture a basic expense</span></span>

<span data-ttu-id="eb70b-109">Pode capturar as suas despesas para poder submetê-las ao aprovador.</span><span class="sxs-lookup"><span data-stu-id="eb70b-109">You can capture your expenses so that you can submit them to the approver.</span></span>

1. <span data-ttu-id="eb70b-110">Vá para **Despesas** e selecione **Novo**.</span><span class="sxs-lookup"><span data-stu-id="eb70b-110">Go to **Expenses**, and select **New**.</span></span>
2. <span data-ttu-id="eb70b-111">Na página **Nova Despesa**, introduza as informações da despesa necessárias e, em seguida, selecione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="eb70b-111">On the **New Expense** page, enter the required expense information, and then select **Save**.</span></span>

## <a name="submit-a-basic-expense"></a><span data-ttu-id="eb70b-112">Submeter uma despesa básica</span><span class="sxs-lookup"><span data-stu-id="eb70b-112">Submit a basic expense</span></span>

<span data-ttu-id="eb70b-113">Depois de concluir a captura de todas as suas despesas, e quando estiver pronto para aprová-las, tem de submetê-las.</span><span class="sxs-lookup"><span data-stu-id="eb70b-113">After you've finished capturing all your expenses, and you're ready to have them approved, you must submit them.</span></span>

1. <span data-ttu-id="eb70b-114">Vá para **Despesas** e selecione uma despesa.</span><span class="sxs-lookup"><span data-stu-id="eb70b-114">Go to **Expenses**, and select an expense.</span></span> <span data-ttu-id="eb70b-115">Ou selecione todas as despesas através da caixa de verificação no cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="eb70b-115">Or, select all the expenses by using the check box on the header.</span></span>
2. <span data-ttu-id="eb70b-116">Selecione **Submeter**.</span><span class="sxs-lookup"><span data-stu-id="eb70b-116">Select **Submit**.</span></span> <span data-ttu-id="eb70b-117">O sistema processa as entradas selecionadas e, em seguida, cria pedidos de aprovação de despesas.</span><span class="sxs-lookup"><span data-stu-id="eb70b-117">The system processes the selected entries and then creates expense approval requests.</span></span>

## <a name="add-an-attachment"></a><span data-ttu-id="eb70b-118">Adicionar um anexo</span><span class="sxs-lookup"><span data-stu-id="eb70b-118">Add an attachment</span></span>

<span data-ttu-id="eb70b-119">Poderá ter de fornecer ao aprovador documentação adicional sobre as suas despesas.</span><span class="sxs-lookup"><span data-stu-id="eb70b-119">You may have to provide the approver with additional documentation about your expense.</span></span> <span data-ttu-id="eb70b-120">Pode anexar um recibo na linha cronológica da entrada de despesas.</span><span class="sxs-lookup"><span data-stu-id="eb70b-120">You can attach a receipt in the timeline of the expense entry.</span></span> <span data-ttu-id="eb70b-121">Selecione **Editar** e a secção **Linha Cronológica** e, em seguida, selecione o ícone de clipe de papel para anexar o seu recibo.</span><span class="sxs-lookup"><span data-stu-id="eb70b-121">Select **Edit** and in the **Timeline** section, and then select the paperclip icon to attach your receipt.</span></span>

## <a name="recall-a-basic-expense"></a><span data-ttu-id="eb70b-122">Recuperar uma despesa básica</span><span class="sxs-lookup"><span data-stu-id="eb70b-122">Recall a basic expense</span></span>

<span data-ttu-id="eb70b-123">Quando submete uma despesa por engano, podes recuperá-la.</span><span class="sxs-lookup"><span data-stu-id="eb70b-123">When you submit an expense by mistake, you can recall it.</span></span> <span data-ttu-id="eb70b-124">O tempo necessário para recuperar uma entrada de despesa depende da sua fase de aprovação.</span><span class="sxs-lookup"><span data-stu-id="eb70b-124">The time that is required to recall an expense entry depends on its approval stage.</span></span>  <span data-ttu-id="eb70b-125">Se o aprovador ainda não tiver aprovado a entrada, a recuperação poderá ocorrer imediatamente.</span><span class="sxs-lookup"><span data-stu-id="eb70b-125">If the approver hasn't yet approved the entry, the recall can occur immediately.</span></span> <span data-ttu-id="eb70b-126">No entanto, se a entrada já tiver sido aprovada, é pedido ao aprovador para aprovar a recuperação e reverter as transações.</span><span class="sxs-lookup"><span data-stu-id="eb70b-126">However, if the entry has already been approved, the approver is asked to approve the recall and reverse the transactions.</span></span>

1. <span data-ttu-id="eb70b-127">Vá para **Despesas** e, depois, na lista de despesas, selecione a despesa a recuperar.</span><span class="sxs-lookup"><span data-stu-id="eb70b-127">Go to **Expenses**, and then, in the list of expenses, select the expense to recall.</span></span>
2. <span data-ttu-id="eb70b-128">Selecione **Recuperar**.</span><span class="sxs-lookup"><span data-stu-id="eb70b-128">Select **Recall**.</span></span> <span data-ttu-id="eb70b-129">Se a entrada de despesa ainda não tiver sido aprovada, o sistema recupera-a imediatamente.</span><span class="sxs-lookup"><span data-stu-id="eb70b-129">If the expense entry hasn't yet been approved, the system immediately recalls it.</span></span> <span data-ttu-id="eb70b-130">Se a entrada de despesa já tiver sido aprovada, é criado um pedido de recuperação para notificar o aprovador que pretende reverter a despesa.</span><span class="sxs-lookup"><span data-stu-id="eb70b-130">If the expense entry has already been approved, a recall request is created to notify the approver that you want to reverse the expense.</span></span> <span data-ttu-id="eb70b-131">Em seguida, o aprovador confirmará que a reversão pode ser feita e a entrada será devolvida.</span><span class="sxs-lookup"><span data-stu-id="eb70b-131">The approver will then confirm that the reversal can be done, and the entry will be returned.</span></span>

## <a name="delete-a-basic-expense"></a><span data-ttu-id="eb70b-132">Eliminar uma despesa básica</span><span class="sxs-lookup"><span data-stu-id="eb70b-132">Delete a basic expense</span></span>

<span data-ttu-id="eb70b-133">As despesas que ainda não foram submetidas podem ser eliminadas.</span><span class="sxs-lookup"><span data-stu-id="eb70b-133">Expenses that haven't yet been submitted can be deleted.</span></span> <span data-ttu-id="eb70b-134">Para eliminar uma despesa que já foi submetida, primeiro tem de recuperá-la.</span><span class="sxs-lookup"><span data-stu-id="eb70b-134">To delete an expense that has already been submitted, you must first recall it.</span></span>

## <a name="see-also"></a><span data-ttu-id="eb70b-135">Consulte também</span><span class="sxs-lookup"><span data-stu-id="eb70b-135">See also</span></span>

- [<span data-ttu-id="eb70b-136">Descrição geral das aprovações</span><span class="sxs-lookup"><span data-stu-id="eb70b-136">Approvals overview</span></span>](../approvals/approvals-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]