---
title: Descrição geral das aprovações
description: Este tópico fornece informação sobre como trabalhar com aprovações no Project Operations.
author: stsporen
ms.date: 03/31/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.custom: intro-internal
ms.openlocfilehash: 9148c9f55e8664850c38aebbc9c4bbaa243475ad
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368670"
---
# <a name="approvals-overview"></a><span data-ttu-id="8c652-103">Descrição geral das aprovações</span><span class="sxs-lookup"><span data-stu-id="8c652-103">Approvals overview</span></span>

<span data-ttu-id="8c652-104">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="8c652-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8c652-105">O tempo, as despesas e as submissões de utilização do material passam por um fluxo de trabalho de aprovação.</span><span class="sxs-lookup"><span data-stu-id="8c652-105">Time, expense, and material usage submissions move through an approval workflow.</span></span> <span data-ttu-id="8c652-106">Após a aprovação das entradas, as transações são registadas em valores reais ou o tempo é reservado na agenda.</span><span class="sxs-lookup"><span data-stu-id="8c652-106">After the entries are approved, transactions are recorded in actuals or time is booked in the schedule.</span></span>

## <a name="approvals-workflow"></a><span data-ttu-id="8c652-107">Fluxo de trabalho de aprovações</span><span class="sxs-lookup"><span data-stu-id="8c652-107">Approvals workflow</span></span>
<span data-ttu-id="8c652-108">Quando cria e envia uma entrada de tempo, despesa ou utilização material, é criado um registo de aprovação.</span><span class="sxs-lookup"><span data-stu-id="8c652-108">When you create and submit a time, expense, or material usage entry, an approval record is created.</span></span> <span data-ttu-id="8c652-109">O aprovador ou gestor do projeto analisa e aprova a entrada.</span><span class="sxs-lookup"><span data-stu-id="8c652-109">The project approver or manager reviews and approves the entry.</span></span> <span data-ttu-id="8c652-110">Se a entrada estiver relacionada com um projeto, os valores reais serão criados quando for aprovado.</span><span class="sxs-lookup"><span data-stu-id="8c652-110">If the entry is related to a project, the actuals will be created when it's approved.</span></span> <span data-ttu-id="8c652-111">Isto permite monitorizar o custo e a faturação.</span><span class="sxs-lookup"><span data-stu-id="8c652-111">This allows the cost and billing to be tracked.</span></span>

## <a name="approve-an-entry"></a><span data-ttu-id="8c652-112">Aprovar uma entrada</span><span class="sxs-lookup"><span data-stu-id="8c652-112">Approve an entry</span></span>
<span data-ttu-id="8c652-113">A página **Aprovações** permite-lhe alternar entre diferentes pontos de vista para que possa ver os diferentes tipos de aprovações.</span><span class="sxs-lookup"><span data-stu-id="8c652-113">The **Approvals** page allows you to switch between different views so that you can view the different types of approvals.</span></span>
  
1. <span data-ttu-id="8c652-114">Aceda à página **Aprovações** e selecione **Despesas**, **Tempo**, **Utilização do Material** ou **Recordações**.</span><span class="sxs-lookup"><span data-stu-id="8c652-114">Go to the **Approvals** page and select **Expenses**, **Time**, **Material Usage**, or **Recalls**.</span></span>
2. <span data-ttu-id="8c652-115">Reveja cada aprovação e selecione as que pretende aprovar.</span><span class="sxs-lookup"><span data-stu-id="8c652-115">Review each approval, and select the ones you want to approve.</span></span>
3. <span data-ttu-id="8c652-116">Selecione **Aprovar** para aprovar as entradas selecionadas.</span><span class="sxs-lookup"><span data-stu-id="8c652-116">Select **Approve** to approve the selected entries.</span></span>
<span data-ttu-id="8c652-117">O sistema processa estas entradas e cria valores reais.</span><span class="sxs-lookup"><span data-stu-id="8c652-117">The system processes these entries and create actuals.</span></span>

## <a name="reject-an-entry"></a><span data-ttu-id="8c652-118">Rejeitar uma entrada</span><span class="sxs-lookup"><span data-stu-id="8c652-118">Reject an entry</span></span>
<span data-ttu-id="8c652-119">Como Aprovador do projeto, poderá ter de enviar uma entrada de volta para um utilizador para correção.</span><span class="sxs-lookup"><span data-stu-id="8c652-119">As the Project approver, you may have to send an entry back to a user for correction.</span></span>
  
1. <span data-ttu-id="8c652-120">Vá à página **Aprovações** e selecione a entrada a rejeitar.</span><span class="sxs-lookup"><span data-stu-id="8c652-120">Go to the **Approvals** page and select the entry to reject.</span></span> 
2. <span data-ttu-id="8c652-121">Selecione **Rejeitar**.</span><span class="sxs-lookup"><span data-stu-id="8c652-121">Select **Reject**.</span></span>
3. <span data-ttu-id="8c652-122">Opcional, adicione um comentário na caixa de diálogo **Comentários de rejeição** para informar o utilizador porque é que a entrada está a ser rejeitada.</span><span class="sxs-lookup"><span data-stu-id="8c652-122">Optional, add a comment in the **Rejection Comments** dialog box to inform the user why the entry is being rejected.</span></span>
4. <span data-ttu-id="8c652-123">Selecione **OK**.</span><span class="sxs-lookup"><span data-stu-id="8c652-123">Select **OK**.</span></span> <span data-ttu-id="8c652-124">A entrada será devolvida ao utilizador.</span><span class="sxs-lookup"><span data-stu-id="8c652-124">The entry will be returned to the user.</span></span>
  
## <a name="cancel-approval"></a><span data-ttu-id="8c652-125">Cancelar a aprovação</span><span class="sxs-lookup"><span data-stu-id="8c652-125">Cancel approval</span></span>
<span data-ttu-id="8c652-126">Nalguns casos, poderá ter de cancelar uma entrada previamente aprovada.</span><span class="sxs-lookup"><span data-stu-id="8c652-126">In some cases, you might need to cancel a previously approved entry.</span></span> <span data-ttu-id="8c652-127">O cancelamento de uma entrada previamente aprovada terá um impacto financeiro.</span><span class="sxs-lookup"><span data-stu-id="8c652-127">Canceling a previously approved entry will have a financial impact.</span></span> 

## <a name="approving-recall-requests"></a><span data-ttu-id="8c652-128">Aprovar pedidos de recuperação</span><span class="sxs-lookup"><span data-stu-id="8c652-128">Approving recall requests</span></span>
<span data-ttu-id="8c652-129">Nalguns casos, um consultor pode precisar de recuperar uma entrada previamente aprovada.</span><span class="sxs-lookup"><span data-stu-id="8c652-129">In some cases, a consultant may need to recall a previously approved entry.</span></span> <span data-ttu-id="8c652-130">O cancelamento de uma entrada previamente aprovada terá um impacto financeiro.</span><span class="sxs-lookup"><span data-stu-id="8c652-130">Canceling a previously approved entry will have a financial impact.</span></span> <span data-ttu-id="8c652-131">O aprovador do projeto é obrigado a aprovar a retirada para inverter a transação em Valores reais.</span><span class="sxs-lookup"><span data-stu-id="8c652-131">The project approver is required to approve the recall to reverse the transaction in Actuals.</span></span>

## <a name="specify-project-approvers"></a><span data-ttu-id="8c652-132">Especificar Aprovadores do projeto</span><span class="sxs-lookup"><span data-stu-id="8c652-132">Specify Project approvers</span></span>
<span data-ttu-id="8c652-133">Cada projeto tem vários membros da equipa do projeto.</span><span class="sxs-lookup"><span data-stu-id="8c652-133">Each project has a number of project team members.</span></span> <span data-ttu-id="8c652-134">Pode especificar os membros da equipa que também são Aprovadores do projeto.</span><span class="sxs-lookup"><span data-stu-id="8c652-134">You can specify which team members are also Project approvers.</span></span>

1. <span data-ttu-id="8c652-135">Vá à página **Projetos** e abra o projeto a partir da lista.</span><span class="sxs-lookup"><span data-stu-id="8c652-135">Go to the **Projects** page and open the project from the list.</span></span>
2. <span data-ttu-id="8c652-136">No separador **Equipa**, selecione o membro da equipa que será Aprovador do projeto e, em seguida, selecione **Editar**.</span><span class="sxs-lookup"><span data-stu-id="8c652-136">On the **Team** tab, select the team member who will be a Project approver and then select **Edit**.</span></span>
3. <span data-ttu-id="8c652-137">Defina o campo **Aprovador do Projeto** como **Sim**.</span><span class="sxs-lookup"><span data-stu-id="8c652-137">Set the **Project Approver** field to **Yes**.</span></span>
4. <span data-ttu-id="8c652-138">Selecione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="8c652-138">Select **Save**.</span></span>
5. <span data-ttu-id="8c652-139">Repita os passos 2 a 4 para adicionar Aprovadores do projeto adicionais.</span><span class="sxs-lookup"><span data-stu-id="8c652-139">Repeat steps 2-4 to add additional Project approvers.</span></span>

## <a name="configure-the-users-manager"></a><span data-ttu-id="8c652-140">Configurar o gestor do utilizador</span><span class="sxs-lookup"><span data-stu-id="8c652-140">Configure the user's manager</span></span>

1. <span data-ttu-id="8c652-141">Aceda a **Definições** > **Segurança** > **Utilizadores**.</span><span class="sxs-lookup"><span data-stu-id="8c652-141">Go to **Settings** > **Security** > **Users**.</span></span>
2. <span data-ttu-id="8c652-142">Selecione o utilizador a quem está a atribuir um gestor e, na área **Informações da Organização**, selecione o gestor a partir da lista.</span><span class="sxs-lookup"><span data-stu-id="8c652-142">Select the user to whom you are assigning a manager and in the **Organization Information** area, select the manager from the list.</span></span> 
3. <span data-ttu-id="8c652-143">Selecione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="8c652-143">Select **Save**.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
