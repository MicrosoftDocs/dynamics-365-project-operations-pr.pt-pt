---
title: Recuperar entradas de tempo ou despesa aprovadas
description: Este tópico fornece informações sobre como recuperar uma transação de tempo ou despesa aprovada anteriormente.
author: rumant
ms.custom: ''
ms.author: rumant
ms.date: 03/08/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 71f75c1c516ca6e652baf311aa14e0c3fd4ba81e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998200"
---
# <a name="recall-approved-time-or-expense-entries"></a><span data-ttu-id="622be-103">Recuperar entradas de tempo ou despesa aprovadas</span><span class="sxs-lookup"><span data-stu-id="622be-103">Recall approved time or expense entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="622be-104">Um membro da equipa do projeto ou outra pessoa que submeta uma entrada de tempo ou despesa pode recuperar a entrada de tempo ou de despesa depois de a mesma ter sido aprovada.</span><span class="sxs-lookup"><span data-stu-id="622be-104">A project team member or an other person who submits a time or expense entry can recall that time or expense entry after it has been approved.</span></span> <span data-ttu-id="622be-105">O processo para recuperar uma entrada de tempo ou despesa aprovada tem dois passos:</span><span class="sxs-lookup"><span data-stu-id="622be-105">The process for recalling an approved time or expense entry has two steps:</span></span>

1. <span data-ttu-id="622be-106">Um submissor pede uma recuperação.</span><span class="sxs-lookup"><span data-stu-id="622be-106">A submitter requests a recall.</span></span>
2. <span data-ttu-id="622be-107">Um aprovador aprova a recuperação.</span><span class="sxs-lookup"><span data-stu-id="622be-107">An approver approves the recall.</span></span>

## <a name="request-a-recall"></a><span data-ttu-id="622be-108">Pedir uma recuperação</span><span class="sxs-lookup"><span data-stu-id="622be-108">Request a recall</span></span>

<span data-ttu-id="622be-109">Siga estes passos para pedir uma recuperação de uma entrada de tempo ou de despesa aprovada.</span><span class="sxs-lookup"><span data-stu-id="622be-109">Follow these steps to request a recall of an approved time or expense entry.</span></span>

1. <span data-ttu-id="622be-110">Para as entradas de tempo, aceda a **Projetos** \> **O Meu Trabalho** \> **Entrada de Tempo**.</span><span class="sxs-lookup"><span data-stu-id="622be-110">For time entries, go to **Projects** \> **My Work** \> **Time Entry**.</span></span>

    <span data-ttu-id="622be-111">–ou–</span><span class="sxs-lookup"><span data-stu-id="622be-111">–or–</span></span>

    <span data-ttu-id="622be-112">Para as entradas de despesa, aceda a **Projetos** \> **O Meu Trabalho** \> **Despesas**.</span><span class="sxs-lookup"><span data-stu-id="622be-112">For expense entries, go to **Projects** \> **My Work** \> **Expenses**.</span></span>

2. <span data-ttu-id="622be-113">Para as entradas de tempo, selecione todas as entradas de tempo para uma combinação específica de um projeto e uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="622be-113">For time entries, select all the time entries for a specific combination of a project and a task.</span></span> <span data-ttu-id="622be-114">Alternativamente, na grelha, selecione as células individuais para o tempo numa data específica para um projeto específico.</span><span class="sxs-lookup"><span data-stu-id="622be-114">Alternatively, in the grid, select the individual cells for time on a specific date for a specific project.</span></span>

    <span data-ttu-id="622be-115">–ou–</span><span class="sxs-lookup"><span data-stu-id="622be-115">–or–</span></span>

    <span data-ttu-id="622be-116">Para as entradas de despesa, selecione a linha para a entrada de despesa a recuperar.</span><span class="sxs-lookup"><span data-stu-id="622be-116">For expense entries, select the row for the expense entry to recall.</span></span>

3. <span data-ttu-id="622be-117">Selecione **Recuperar**.</span><span class="sxs-lookup"><span data-stu-id="622be-117">Select **Recall**.</span></span> <span data-ttu-id="622be-118">É apresentada uma caixa de diálogo de confirmação.</span><span class="sxs-lookup"><span data-stu-id="622be-118">A confirmation dialog box appears.</span></span> <span data-ttu-id="622be-119">Se as entradas de tempo e despesa selecionadas já tiverem sido aprovadas, é-lhe pedido que introduza um motivo para a recuperação.</span><span class="sxs-lookup"><span data-stu-id="622be-119">If the selected time and expense entries were already approved, you're prompted to enter a reason for the recall.</span></span>
4. <span data-ttu-id="622be-120">Introduza um motivo para a recuperação e, em seguida, selecione **OK** para confirmar a operação.</span><span class="sxs-lookup"><span data-stu-id="622be-120">Enter a reason for the recall, and then select **OK** to confirm the operation.</span></span> <span data-ttu-id="622be-121">O sistema envia a pessoa que aprovou as entradas de um pedido para aprovar a recuperação.</span><span class="sxs-lookup"><span data-stu-id="622be-121">The system sends the person who approved the entries a request to approve the recall.</span></span>

> [!NOTE]
> <span data-ttu-id="622be-122">Apesar de as entradas de tempo e de despesa aprovadas poderem ser recuperadas, se um tempo ou uma despesa aprovado já tiver sido faturado ao cliente, não é possível criar um pedido de recuperação.</span><span class="sxs-lookup"><span data-stu-id="622be-122">Although approved time and expense entries can be recalled, if an approved time or expense has already been invoiced to the customer, a recall request can't be created.</span></span> <span data-ttu-id="622be-123">Um utilizador que tenta criar um pedido de recuperação receberá uma mensagem que indica que não é possível recuperar o tempo ou a despesa porque já foi faturado.</span><span class="sxs-lookup"><span data-stu-id="622be-123">A user who tries to create a recall request will receive a message that states that the time or expense can't be recalled because it was already invoiced.</span></span>

## <a name="approve-or-reject-a-recall-request"></a><span data-ttu-id="622be-124">Aprovar ou rejeitar um pedido de recuperação</span><span class="sxs-lookup"><span data-stu-id="622be-124">Approve or reject a recall request</span></span>

<span data-ttu-id="622be-125">Siga estes passos para aprovar ou rejeitar um pedido de recuperação.</span><span class="sxs-lookup"><span data-stu-id="622be-125">Follow these steps to approve or reject a recall request.</span></span>

1. <span data-ttu-id="622be-126">Aceda a **Projetos** \> **O Meu Trabalho** \> **Aprovações**.</span><span class="sxs-lookup"><span data-stu-id="622be-126">Go to **Projects** \> **My Work** \> **Approvals**.</span></span>
2. <span data-ttu-id="622be-127">Na página da lista de **Aprovações**, altere a vista para **Pedidos de recuperação para aprovação**.</span><span class="sxs-lookup"><span data-stu-id="622be-127">On the **Approvals** list page, change the view to **Recall requests for approval**.</span></span> <span data-ttu-id="622be-128">É apresentada uma lista de pedidos de recuperação submetidos.</span><span class="sxs-lookup"><span data-stu-id="622be-128">A list of submitted recall requests is shown.</span></span>
3. <span data-ttu-id="622be-129">Selecione uma ou mais entradas e, em seguida, selecione **Aprovar** ou **Rejeitar**.</span><span class="sxs-lookup"><span data-stu-id="622be-129">Select one or more entries, and then select either **Approve** or **Reject**.</span></span>
4. <span data-ttu-id="622be-130">Se tiver selecionado **Aprovar**, receberá uma mensagem de aviso que explica o impacto da aprovação.</span><span class="sxs-lookup"><span data-stu-id="622be-130">If you selected **Approve**, you receive a warning message that explains the impact of the approval.</span></span> <span data-ttu-id="622be-131">Selecione **OK** para confirmar a operação.</span><span class="sxs-lookup"><span data-stu-id="622be-131">Select **OK** to confirm the operation.</span></span> <span data-ttu-id="622be-132">O pedido de recuperação é aprovado.</span><span class="sxs-lookup"><span data-stu-id="622be-132">The recall request is approved.</span></span>

    <span data-ttu-id="622be-133">–ou–</span><span class="sxs-lookup"><span data-stu-id="622be-133">–or–</span></span>

    <span data-ttu-id="622be-134">Se tiver selecionado **Rejeitar**, o pedido de recuperação é rejeitado.</span><span class="sxs-lookup"><span data-stu-id="622be-134">If you selected **Reject**, the recall request is rejected.</span></span>

> [!NOTE]
> <span data-ttu-id="622be-135">Como quando uma nova recuperação é pedida, quando uma recuperação é aprovada, o sistema verifica a existência de qualquer atividade de faturação nas entradas de tempo ou despesa.</span><span class="sxs-lookup"><span data-stu-id="622be-135">As when a recall is requested, when a recall is approved, the system checks for any invoicing activity on the time or expense entries.</span></span> <span data-ttu-id="622be-136">Se uma entrada já tiver sido faturada, ou se estiver numa fatura de rascunho, o aprovador receberá uma mensagem de erro que indica que não é possível aprovar o tempo ou a despesa para a recuperação, porque já estava faturado.</span><span class="sxs-lookup"><span data-stu-id="622be-136">If an entry was already invoiced, or if it's on a draft invoice, the approver will receive an error message that states that the time or expense can't be approved for recall, because it was already invoiced.</span></span>

## <a name="impact-of-a-recall-request"></a><span data-ttu-id="622be-137">Impacto de um pedido de recuperação</span><span class="sxs-lookup"><span data-stu-id="622be-137">Impact of a recall request</span></span>

<span data-ttu-id="622be-138">Quando uma aprovação é recuperada, existe um impacto operacional e um impacto financeiro.</span><span class="sxs-lookup"><span data-stu-id="622be-138">When an approval is recalled, there is both operational impact and financial impact.</span></span>

### <a name="operational-impact"></a><span data-ttu-id="622be-139">Impacto operacional</span><span class="sxs-lookup"><span data-stu-id="622be-139">Operational impact</span></span>

<span data-ttu-id="622be-140">Se um pedido de recuperação for aprovado, o registo de aprovação é marcado como **Rejeitado**.</span><span class="sxs-lookup"><span data-stu-id="622be-140">If a recall request is approved, the approval record is marked as **Rejected**.</span></span> <span data-ttu-id="622be-141">O estado da entrada é alterado para **Devolvido** ou **Rejeitado**, dependendo de se é uma entrada de tempo ou uma entrada de despesa.</span><span class="sxs-lookup"><span data-stu-id="622be-141">The status of the entry is changed to either **Returned** or **Rejected**, depending on whether it's a time entry or an expense entry.</span></span>

<span data-ttu-id="622be-142">O membro da equipa do projeto pode ver as entradas, editá-las e, em seguida, voltar a submetê-las ou eliminá-las por completo.</span><span class="sxs-lookup"><span data-stu-id="622be-142">The project team member can view entries, edit and then resubmit entries, or delete entries entirely.</span></span>

<span data-ttu-id="622be-143">Se um pedido de recuperação for rejeitado, o estado da entrada permanece **Aprovado** e a entrada não pode ser editada pelo membro da equipa do projeto ou pelo aprovador do projeto.</span><span class="sxs-lookup"><span data-stu-id="622be-143">If a recall request is rejected, the status of the entry remains **Approved**, and the entry can't be edited by the project team member or the approver for the project.</span></span>

### <a name="financial-impact"></a><span data-ttu-id="622be-144">Impacto financeiro</span><span class="sxs-lookup"><span data-stu-id="622be-144">Financial impact</span></span>

<span data-ttu-id="622be-145">Se um pedido de recuperação for aprovado, os valores reais correspondentes de custo e vendas são atualizados da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="622be-145">If a recall request is approved, the corresponding actuals for cost and sales are updated in the following manner:</span></span>

- <span data-ttu-id="622be-146">O campo **Estado do Ajuste** é atualizado para **Ajustado**.</span><span class="sxs-lookup"><span data-stu-id="622be-146">The **Adjustment Status** field is updated to **Adjusted**.</span></span>
- <span data-ttu-id="622be-147">O campo **Estado de Faturação** é atualizado para **Cancelado**.</span><span class="sxs-lookup"><span data-stu-id="622be-147">The **Billing Status** field is updated to **Canceled**.</span></span>

<span data-ttu-id="622be-148">Em seguida, as entradas de estorno são criadas na tabela Valores Reais.</span><span class="sxs-lookup"><span data-stu-id="622be-148">Next, reversal entries are created in the Actuals table.</span></span> <span data-ttu-id="622be-149">Para criar entradas de estorno, o sistema copia os valores dos campos a partir dos valores reais originais.</span><span class="sxs-lookup"><span data-stu-id="622be-149">To create reversal entries, the system copies over the field values from the original actuals.</span></span> <span data-ttu-id="622be-150">Os únicos valores que não são copiados são os valores de quantidade.</span><span class="sxs-lookup"><span data-stu-id="622be-150">The only values that aren't copied over are the quantity values.</span></span> <span data-ttu-id="622be-151">Em vez disso, estes valores são revertidos.</span><span class="sxs-lookup"><span data-stu-id="622be-151">These values are reversed instead.</span></span> <span data-ttu-id="622be-152">Os valores reais estornados são criados para os valores reais de **Custo** e **Vendas Não Faturadas**.</span><span class="sxs-lookup"><span data-stu-id="622be-152">Reversed actuals are created for both **Cost** and **Unbilled Sales** actuals.</span></span> <span data-ttu-id="622be-153">O campo **Estado de Ajuste** nos valores reais estornados é definido como **Não ajustável** e o campo **Estado da faturação** é definido como **Cancelado**.</span><span class="sxs-lookup"><span data-stu-id="622be-153">The **Adjustment Status** field on the reversed actuals is set to **Unadjustable**, and the **Billing status** field is set to **Canceled**.</span></span> <span data-ttu-id="622be-154">Devido a estas alterações, as despesas registadas e o registo de tarefas de receita no projeto já não serão responsáveis pelos valores que estes valores reais representam.</span><span class="sxs-lookup"><span data-stu-id="622be-154">Because of these changes, the recorded spending and the revenue backlog on the project will no longer account for the amounts that these actuals represent.</span></span>

<span data-ttu-id="622be-155">Se um pedido de recuperação for rejeitado, não haverá um impacto financeiro no projeto.</span><span class="sxs-lookup"><span data-stu-id="622be-155">If a recall request is rejected, there is no financial impact on the project.</span></span>

## <a name="changes-to-time-entry-records"></a><span data-ttu-id="622be-156">Alterações nos registos de entrada de tempo</span><span class="sxs-lookup"><span data-stu-id="622be-156">Changes to time entry records</span></span>

<span data-ttu-id="622be-157">A ilustração seguinte mostra as alterações que ocorrem para as entradas de tempo aprovadas quando são canceladas.</span><span class="sxs-lookup"><span data-stu-id="622be-157">The following illustration shows the changes that occur for approved time entries when they are recalled.</span></span>

![Transições de estado de Entrada de Tempo](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-entry-records"></a><span data-ttu-id="622be-159">Alterações nos registos de entrada de despesa</span><span class="sxs-lookup"><span data-stu-id="622be-159">Changes to expense entry records</span></span>

<span data-ttu-id="622be-160">A ilustração seguinte mostra as alterações que ocorrem para as entradas de despesa aprovadas quando são canceladas.</span><span class="sxs-lookup"><span data-stu-id="622be-160">The following illustration shows the changes that occur for approved expense entries when they are recalled.</span></span>

![Transições de estado de Entrada de Despesa](media/ExpenseEntryStateTransitions.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]