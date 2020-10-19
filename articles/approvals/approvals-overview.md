---
title: Descrição geral das aprovações
description: Este tópico fornece informação sobre como trabalhar com aprovações no Project Operations.
author: stsporen
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 37994422e9146765076fdbb77f5c763b4f1d0802
ms.sourcegitcommit: 2cf93d8bf0be5b61a739195a41334c34d910e9ba
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961180"
---
# <a name="approvals-overview"></a><span data-ttu-id="65f00-103">Descrição geral das aprovações</span><span class="sxs-lookup"><span data-stu-id="65f00-103">Approvals overview</span></span>

<span data-ttu-id="65f00-104">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="65f00-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="65f00-105">As submissões de Tempo e Despesa passam por um fluxo de trabalho de aprovação.</span><span class="sxs-lookup"><span data-stu-id="65f00-105">Time and Expense submissions move through an approval workflow.</span></span> <span data-ttu-id="65f00-106">Após a aprovação das entradas, as transações são registadas em valores reais ou o tempo é reservado na agenda.</span><span class="sxs-lookup"><span data-stu-id="65f00-106">After the entries are approved, transactions are recorded in actuals or time is booked in the schedule.</span></span>

## <a name="approvals-workflow"></a><span data-ttu-id="65f00-107">Fluxo de trabalho de aprovações</span><span class="sxs-lookup"><span data-stu-id="65f00-107">Approvals workflow</span></span>
<span data-ttu-id="65f00-108">Quando cria e envia uma entrada de hora ou despesa, é criada uma entrada de aprovação.</span><span class="sxs-lookup"><span data-stu-id="65f00-108">When you create and submit a time or expense entry, an approval entry is created.</span></span> <span data-ttu-id="65f00-109">O Aprovador do projeto ou o seu gestor analisa e aprova a sua entrada.</span><span class="sxs-lookup"><span data-stu-id="65f00-109">The Project approver or your manager reviews and approves your entry.</span></span> <span data-ttu-id="65f00-110">Se a entrada estiver relacionada com um projeto, quando for aprovada, serão criados os valores reais.</span><span class="sxs-lookup"><span data-stu-id="65f00-110">If the entry is related to a project, when it's approved, the actuals will be created.</span></span> <span data-ttu-id="65f00-111">Isto permite monitorizar o custo e a faturação.</span><span class="sxs-lookup"><span data-stu-id="65f00-111">This allows the cost and billing to be tracked.</span></span> 

## <a name="approve-an-entry"></a><span data-ttu-id="65f00-112">Aprovar uma entrada</span><span class="sxs-lookup"><span data-stu-id="65f00-112">Approve an entry</span></span>
<span data-ttu-id="65f00-113">O formulário **Aprovações** permite-lhe alternar entre diferentes vistas para poder ver os diferentes tipos de aprovação.</span><span class="sxs-lookup"><span data-stu-id="65f00-113">The **Approvals** form allows you to switch between different views so that you can view the different types of approvals.</span></span>
  
1. <span data-ttu-id="65f00-114">Vá para o formulário **Aprovações** e selecione **Despesas**, **Tempo** ou **Recuperações**.</span><span class="sxs-lookup"><span data-stu-id="65f00-114">Go to the **Approvals** form and select **Expenses**, **Time**, or **Recalls**.</span></span>
2. <span data-ttu-id="65f00-115">Reveja cada aprovação e selecione as que pretende aprovar.</span><span class="sxs-lookup"><span data-stu-id="65f00-115">Review each approval, and select the ones you want to approve.</span></span>
3. <span data-ttu-id="65f00-116">Selecione **Aprovar** para aprovar as entradas selecionadas.</span><span class="sxs-lookup"><span data-stu-id="65f00-116">Select **Approve** to approve the selected entries.</span></span>
<span data-ttu-id="65f00-117">O sistema processará estas entradas e criará os valores reais ou uma reserva.</span><span class="sxs-lookup"><span data-stu-id="65f00-117">The system will process these entries and create actuals or a booking.</span></span>

## <a name="reject-an-entry"></a><span data-ttu-id="65f00-118">Rejeitar uma entrada</span><span class="sxs-lookup"><span data-stu-id="65f00-118">Reject an entry</span></span>
<span data-ttu-id="65f00-119">Como Aprovador do projeto, poderá ter de enviar uma entrada de volta para um utilizador para correção.</span><span class="sxs-lookup"><span data-stu-id="65f00-119">As the Project approver, you may have to send an entry back to a user for correction.</span></span>
  
1. <span data-ttu-id="65f00-120">Vá para o formulário **Aprovações** e selecione a entrada a rejeitar.</span><span class="sxs-lookup"><span data-stu-id="65f00-120">Go to the **Approvals** form and select the entry to reject.</span></span> 
2. <span data-ttu-id="65f00-121">Selecione **Rejeitar**.</span><span class="sxs-lookup"><span data-stu-id="65f00-121">Select **Reject**.</span></span>
3. <span data-ttu-id="65f00-122">Opcional - Adicione um comentário na caixa de diálogo **Comentários de Rejeição** para informar o utilizador por que motivo a entrada está a ser rejeitada.</span><span class="sxs-lookup"><span data-stu-id="65f00-122">Optional - Add a comment in the **Rejection Comments** dialog to inform the user why the entry is being rejected.</span></span>
4. <span data-ttu-id="65f00-123">Selecione **OK**.</span><span class="sxs-lookup"><span data-stu-id="65f00-123">Select **OK**.</span></span> <span data-ttu-id="65f00-124">A entrada será devolvida ao utilizador.</span><span class="sxs-lookup"><span data-stu-id="65f00-124">The entry will be returned to the user.</span></span>
  
## <a name="recall-entries"></a><span data-ttu-id="65f00-125">Recuperar entradas</span><span class="sxs-lookup"><span data-stu-id="65f00-125">Recall entries</span></span>
<span data-ttu-id="65f00-126">A dada altura, poderá ter de recuperar uma entrada submetida.</span><span class="sxs-lookup"><span data-stu-id="65f00-126">At some point, you might need to recall a submitted entry.</span></span> <span data-ttu-id="65f00-127">Se a entrada não tiver sido aprovada, será devolvida imediatamente.</span><span class="sxs-lookup"><span data-stu-id="65f00-127">If the entry has not been approved, it will be returned immediately.</span></span> <span data-ttu-id="65f00-128">No entanto, uma entrada aprovada pode ter um impacto material.</span><span class="sxs-lookup"><span data-stu-id="65f00-128">An approved entry however, may have a material impact.</span></span> <span data-ttu-id="65f00-129">O Aprovador do projeto tem de aprovar a recuperação para reverter a transação em Valores Reais.</span><span class="sxs-lookup"><span data-stu-id="65f00-129">The Project approver is required to approve the recall in order to reverse the transaction in Actuals.</span></span>

## <a name="specify-project-approvers"></a><span data-ttu-id="65f00-130">Especificar Aprovadores do projeto</span><span class="sxs-lookup"><span data-stu-id="65f00-130">Specify Project approvers</span></span>
<span data-ttu-id="65f00-131">Cada projeto tem vários membros da equipa do projeto.</span><span class="sxs-lookup"><span data-stu-id="65f00-131">Each project has a number of project team members.</span></span> <span data-ttu-id="65f00-132">Pode especificar os membros da equipa que também são Aprovadores do projeto.</span><span class="sxs-lookup"><span data-stu-id="65f00-132">You can specify which team members are also Project approvers.</span></span>

1. <span data-ttu-id="65f00-133">Vá para o formulário **Projetos** e abra o projeto a partir da lista.</span><span class="sxs-lookup"><span data-stu-id="65f00-133">Go to the **Projects** form and open the project from the list.</span></span>
2. <span data-ttu-id="65f00-134">No separador **Equipa**, selecione o membro da equipa que será Aprovador do projeto e, em seguida, selecione **Editar**.</span><span class="sxs-lookup"><span data-stu-id="65f00-134">On the **Team** tab, select the team member who will be a Project approver and then select **Edit**.</span></span>
3. <span data-ttu-id="65f00-135">Defina o campo **Aprovador do Projeto** como **Sim**.</span><span class="sxs-lookup"><span data-stu-id="65f00-135">Set the **Project Approver** field to **Yes**.</span></span>
4. <span data-ttu-id="65f00-136">Selecione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="65f00-136">Select **Save**.</span></span>
5. <span data-ttu-id="65f00-137">Repita os passos 2 a 4 para adicionar Aprovadores do projeto adicionais.</span><span class="sxs-lookup"><span data-stu-id="65f00-137">Repeat steps 2-4 to add additional Project approvers.</span></span>

## <a name="configure-the-users-manager"></a><span data-ttu-id="65f00-138">Configurar o gestor do utilizador</span><span class="sxs-lookup"><span data-stu-id="65f00-138">Configure the user's manager</span></span>

1. <span data-ttu-id="65f00-139">Aceda a **Definições** > **Segurança** > **Utilizadores**.</span><span class="sxs-lookup"><span data-stu-id="65f00-139">Go to **Settings** > **Security** > **Users**.</span></span>
2. <span data-ttu-id="65f00-140">Selecione o utilizador a quem está a atribuir um gestor e, na área **Informações da Organização**, selecione o gestor a partir da lista.</span><span class="sxs-lookup"><span data-stu-id="65f00-140">Select the user to whom you are assigning a manager and in the **Organization Information** area, select the manager from the list.</span></span> 
3. <span data-ttu-id="65f00-141">Selecione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="65f00-141">Select **Save**.</span></span>


