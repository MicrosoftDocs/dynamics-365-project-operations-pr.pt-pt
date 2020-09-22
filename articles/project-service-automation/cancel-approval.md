---
title: Cancelar entradas de tempo e despesa aprovadas anteriormente
description: Este tópico fornece informações sobre como cancelar uma transação de tempo e despesa aprovada do projeto.
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 2fc74aba2a837b7cdff55385ffa20d78c2678bb7
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754450"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a><span data-ttu-id="e8a18-103">Cancelar entradas de tempo ou despesa aprovadas anteriormente</span><span class="sxs-lookup"><span data-stu-id="e8a18-103">Cancel previously approved time or expense entries</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="e8a18-104">Na versão mais recente do Dynamics 365 Project Service Automation, os aprovadores podem cancelar as entradas de tempo ou despesa que anteriormente aprovaram.</span><span class="sxs-lookup"><span data-stu-id="e8a18-104">In the latest version of Dynamics 365 Project Service Automation, approvers can cancel time or expense entries that they previously approved.</span></span>

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a><span data-ttu-id="e8a18-105">Cancelar uma entrada de tempo ou despesa aprovada anteriormente</span><span class="sxs-lookup"><span data-stu-id="e8a18-105">Cancel a previously approved time or expense entry</span></span>

<span data-ttu-id="e8a18-106">Siga estes passos para cancelar uma entrada de tempo ou de despesa que tenha aprovado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="e8a18-106">Follow these steps to cancel a time or expense entry that you previously approved.</span></span>

1. <span data-ttu-id="e8a18-107">Aceda a **Projetos** \> **O Meu Trabalho** \> **Aprovações**.</span><span class="sxs-lookup"><span data-stu-id="e8a18-107">Go to **Projects** \> **My Work** \> **Approvals**.</span></span>
2. <span data-ttu-id="e8a18-108">Na página da lista de **Aprovações**, altere a vista para **As minhas aprovações passadas**.</span><span class="sxs-lookup"><span data-stu-id="e8a18-108">On the **Approvals** list page, change the view to **My past approvals**.</span></span> <span data-ttu-id="e8a18-109">É apresentada uma lista das entradas de tempo e despesa que aprovou anteriormente.</span><span class="sxs-lookup"><span data-stu-id="e8a18-109">A list of the time and expense entries that you previously approved is shown.</span></span>
3. <span data-ttu-id="e8a18-110">Selecione uma ou mais entradas e, em seguida, selecione **Cancelar aprovação**.</span><span class="sxs-lookup"><span data-stu-id="e8a18-110">Select one or more entries, and then select **Cancel approval**.</span></span> <span data-ttu-id="e8a18-111">Recebe uma mensagem de aviso.</span><span class="sxs-lookup"><span data-stu-id="e8a18-111">You receive a warning message.</span></span>
4. <span data-ttu-id="e8a18-112">Para cancelar a aprovação, selecione **OK**.</span><span class="sxs-lookup"><span data-stu-id="e8a18-112">Select **OK** to cancel the approval.</span></span>

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a><span data-ttu-id="e8a18-113">Compreender o impacto de cancelar uma aprovação de uma entrada de tempo ou despesa</span><span class="sxs-lookup"><span data-stu-id="e8a18-113">Understand the impact of canceling a time or expense entry approval</span></span>

<span data-ttu-id="e8a18-114">Quando uma aprovação é cancelada, existe um impacto operacional e um impacto financeiro.</span><span class="sxs-lookup"><span data-stu-id="e8a18-114">When an approval is canceled, there is both operational impact and financial impact.</span></span>

### <a name="operational-impact"></a><span data-ttu-id="e8a18-115">Impacto operacional</span><span class="sxs-lookup"><span data-stu-id="e8a18-115">Operational impact</span></span>

<span data-ttu-id="e8a18-116">No lado das operações, quando uma aprovação é cancelada, o estado do registo é reposto para **Rascunho** e a aprovação já não aparece na vista **As minhas aprovações passadas**.</span><span class="sxs-lookup"><span data-stu-id="e8a18-116">On the operations side, when an approval is canceled, the status of the record is reset to **Draft**, and the approval no longer appears in the **My past approvals** view.</span></span> <span data-ttu-id="e8a18-117">Em vez disso, a aprovação cancelada aparece na vista **Entradas de tempo para aprovação** ou na vista **Entradas de despesa para aprovação**, dependendo de se trata de uma entrada de tempo ou de uma entrada de despesa.</span><span class="sxs-lookup"><span data-stu-id="e8a18-117">Instead, the canceled approval appears in either the **Time entries for approval** view or the **Expense entries for approval** view, depending on whether it was a time entry or an expense entry.</span></span> <span data-ttu-id="e8a18-118">Além disso, o estado da entrada de tempo ou de despesa relacionada é alterado para **Submetido**, para que a entrada relacionada seja consistente com as aprovações que têm o estado **Rascunho**.</span><span class="sxs-lookup"><span data-stu-id="e8a18-118">Additionally, the status of the related time or expense entry is changed to **Submitted**, so that the related entry is consistent with approvals that have a status of **Draft**.</span></span>

<span data-ttu-id="e8a18-119">Como aprovador, pode editar alguns dos campos de uma aprovação com um estado de **Rascunho**.</span><span class="sxs-lookup"><span data-stu-id="e8a18-119">As an approver, you can edit some of the fields of an approval that has a status of **Draft**.</span></span> <span data-ttu-id="e8a18-120">Estes campos incluem o **Tipo de Faturação** e **Horas Faturáveis para Entradas de Tempo**.</span><span class="sxs-lookup"><span data-stu-id="e8a18-120">These fields include **Billing Type** and **Billable Hours for Time Entries**.</span></span> <span data-ttu-id="e8a18-121">Depois de efetuar as alterações, pode aprovar novamente o registo.</span><span class="sxs-lookup"><span data-stu-id="e8a18-121">After you make changes, you can approve the record again.</span></span> <span data-ttu-id="e8a18-122">Em alternativa, pode rejeitar a entrada.</span><span class="sxs-lookup"><span data-stu-id="e8a18-122">Alternatively, you can reject the entry.</span></span> <span data-ttu-id="e8a18-123">Se rejeitar a aprovação de uma entrada de tempo, o estado da entrada é alterado para **Devolvido**.</span><span class="sxs-lookup"><span data-stu-id="e8a18-123">If you reject the approval of a time entry, the status of the entry is changed to **Returned**.</span></span> <span data-ttu-id="e8a18-124">Se rejeitar a aprovação de uma entrada de despesa, o estado é alterado para **Rejeitado**.</span><span class="sxs-lookup"><span data-stu-id="e8a18-124">If you reject the approval of an expense entry, the status is changed to **Rejected**.</span></span> <span data-ttu-id="e8a18-125">Funcionalmente, ambas as entradas devolvidas e rejeitadas têm o mesmo comportamento que uma entrada com o estado de **Rascunho**.</span><span class="sxs-lookup"><span data-stu-id="e8a18-125">Functionally, both returned and rejected entries behave the same as an entry that has a status of **Draft**.</span></span> <span data-ttu-id="e8a18-126">Um membro da equipa do projeto pode efetuar quaisquer alterações necessárias na entrada e, em seguida, submetê-la novamente para aprovação ou eliminar a entrada totalmente.</span><span class="sxs-lookup"><span data-stu-id="e8a18-126">A project team member can either make any required changes to the entry and then resubmit it for approval, or delete the entry entirely.</span></span>

### <a name="financial-impact"></a><span data-ttu-id="e8a18-127">Impacto financeiro</span><span class="sxs-lookup"><span data-stu-id="e8a18-127">Financial impact</span></span>

<span data-ttu-id="e8a18-128">Um projeto também é afetado financeiramente quando uma aprovação é cancelada.</span><span class="sxs-lookup"><span data-stu-id="e8a18-128">A project is also affected financially when an approval is canceled.</span></span> <span data-ttu-id="e8a18-129">Primeiro, os valores reais correspondentes de custo e vendas são atualizados da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="e8a18-129">First, the corresponding actuals for cost and sales are updated in the following manner:</span></span>

- <span data-ttu-id="e8a18-130">O estado do ajuste é definido como **Ajustado**.</span><span class="sxs-lookup"><span data-stu-id="e8a18-130">The adjustment status is set to **Adjusted**.</span></span>
- <span data-ttu-id="e8a18-131">O estado de faturação é definido como **Cancelado**.</span><span class="sxs-lookup"><span data-stu-id="e8a18-131">The billing status is set to **Canceled**.</span></span>

<span data-ttu-id="e8a18-132">Em seguida, as entradas de estorno são criadas na tabela Valores Reais.</span><span class="sxs-lookup"><span data-stu-id="e8a18-132">Next, reversal entries are created in the Actuals table.</span></span> <span data-ttu-id="e8a18-133">Para criar entradas de estorno, o sistema copia os valores dos campos a partir dos valores reais originais.</span><span class="sxs-lookup"><span data-stu-id="e8a18-133">To create reversal entries, the system copies over the field values from the original actuals.</span></span> <span data-ttu-id="e8a18-134">Os únicos valores que não são copiados são os valores de quantidade.</span><span class="sxs-lookup"><span data-stu-id="e8a18-134">The only values that aren't copied over are the quantity values.</span></span> <span data-ttu-id="e8a18-135">Em vez disso, estes valores são revertidos.</span><span class="sxs-lookup"><span data-stu-id="e8a18-135">These values are reversed instead.</span></span> <span data-ttu-id="e8a18-136">Os valores reais estornados são criados para os valores reais de **Custo** e **Vendas Não Faturadas**.</span><span class="sxs-lookup"><span data-stu-id="e8a18-136">Reversed actuals are created for both **Cost** and **Unbilled Sales** actuals.</span></span> <span data-ttu-id="e8a18-137">O campo **Estado de Ajuste** nos valores reais estornados é definido como **Não ajustável** e o estado da faturação é definido como **Cancelado**.</span><span class="sxs-lookup"><span data-stu-id="e8a18-137">The **Adjustment Status** field on the reversed actuals is set to **Unadjustable**, and the billing status is set to **Canceled**.</span></span>

<span data-ttu-id="e8a18-138">Depois de estas alterações serem efetuadas, o valor que é registado como gasto no projeto e o registo de tarefas pendentes de receita no projeto contabilizarão mais os valores que estes valores reais representam.</span><span class="sxs-lookup"><span data-stu-id="e8a18-138">After these changes are made, the amount that is recorded as spent on the project and the revenue backlog on the project will longer account for the amounts that these actuals represent.</span></span>
