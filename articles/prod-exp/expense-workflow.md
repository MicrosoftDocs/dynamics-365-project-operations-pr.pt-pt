---
title: Fluxo de trabalho de gestão de despesas
description: Este tópico explica como pode utilizar o sistema de fluxo de trabalho no Microsoft Dynamics 365 Finance, para configurar um processo de revisão para relatórios de despesas na gestão de Despesas.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5207be92cb58d8ab2658096b3e0f3fc81d73d91e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082559"
---
# <a name="expense-management-workflow"></a><span data-ttu-id="a6d35-103">Fluxo de trabalho de gestão de despesas</span><span class="sxs-lookup"><span data-stu-id="a6d35-103">Expense management workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a6d35-104">Pode utilizar o sistema de fluxo de trabalho para configurar um processo de revisão para relatórios de despesas na gestão de Despesas.</span><span class="sxs-lookup"><span data-stu-id="a6d35-104">You can use the workflow system to set up a review process for expense reports in Expense management.</span></span> <span data-ttu-id="a6d35-105">Pode configurar um fluxo de trabalho que utilize os seguintes critérios para determinar quem aprova relatórios de despesas:</span><span class="sxs-lookup"><span data-stu-id="a6d35-105">You can set up a workflow that uses the following criteria to determine who approves expense reports:</span></span>

- <span data-ttu-id="a6d35-106">A hierarquia de relatórios de funcionários e os limites de aprovação predefinidos</span><span class="sxs-lookup"><span data-stu-id="a6d35-106">The employee reporting hierarchy and predefined approval limits</span></span>
- <span data-ttu-id="a6d35-107">Aprovação a vários níveis que suporta aprovadores provisórios e um aprovador final</span><span class="sxs-lookup"><span data-stu-id="a6d35-107">Multi-level approval that supports interim approvers and a final approver</span></span>
- <span data-ttu-id="a6d35-108">Dimensões financeiras e responsabilidade do projeto</span><span class="sxs-lookup"><span data-stu-id="a6d35-108">Financial dimensions and project responsibility</span></span>
- <span data-ttu-id="a6d35-109">Atribuição a utilizadores ou grupos de utilizadores específicos</span><span class="sxs-lookup"><span data-stu-id="a6d35-109">Assignment to specific users or user groups</span></span>

<span data-ttu-id="a6d35-110">Podem ser criadas aprovações de fluxos de trabalho para relatórios de despesas, requisições de viagens, adiantamentos de dinheiro e recuperação do imposto sobre o valor acrescentado (IVA).</span><span class="sxs-lookup"><span data-stu-id="a6d35-110">Workflow approvals can be created for expense reports, travel requisitions, cash advances, and value-added tax (VAT) recovery.</span></span>

<span data-ttu-id="a6d35-111">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="a6d35-111">**Example**</span></span>

<span data-ttu-id="a6d35-112">O processo que se segue é um exemplo do fluxo de trabalho de gestão de despesas para um relatório de despesas.</span><span class="sxs-lookup"><span data-stu-id="a6d35-112">The following process is an example of the expense management workflow for an expense report.</span></span>

1. <span data-ttu-id="a6d35-113">Um empregado cria e guarda um relatório de despesas.</span><span class="sxs-lookup"><span data-stu-id="a6d35-113">An employee creates and saves an expense report.</span></span>
2. <span data-ttu-id="a6d35-114">O funcionário submete o relatório de despesas para aprovação.</span><span class="sxs-lookup"><span data-stu-id="a6d35-114">The employee submits the expense report for approval.</span></span> <span data-ttu-id="a6d35-115">O aprovador é identificado com base nas regras definidas aquando da configuração do fluxo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a6d35-115">The approver is identified based on the rules that were defined when the workflow was set up.</span></span>
3. <span data-ttu-id="a6d35-116">O aprovador recebe uma notificação de que um relatório de despesas está pronto para aprovação.</span><span class="sxs-lookup"><span data-stu-id="a6d35-116">The approver receives a notification that an expense report is ready for approval.</span></span> <span data-ttu-id="a6d35-117">O aprovador revê o relatório de despesas e verifica que estão reunidas as seguintes condições:</span><span class="sxs-lookup"><span data-stu-id="a6d35-117">The approver reviews the expense report and verifies that the following conditions are met:</span></span>

    - <span data-ttu-id="a6d35-118">As despesas não violam nenhuma política de despesas.</span><span class="sxs-lookup"><span data-stu-id="a6d35-118">The expenses don't violate any expense policies.</span></span> <span data-ttu-id="a6d35-119">Se uma despesa violar uma política, o aprovador verifica que o relatório de despesas inclui uma justificação comercial válida.</span><span class="sxs-lookup"><span data-stu-id="a6d35-119">If an expense violates a policy, the approver verifies that the expense report includes a valid business justification.</span></span>
    - <span data-ttu-id="a6d35-120">Os recibos eletrónicos são anexados ao relatório de despesas.</span><span class="sxs-lookup"><span data-stu-id="a6d35-120">Electronic receipts are attached to the expense report.</span></span>

4. <span data-ttu-id="a6d35-121">O aprovador aprova o relatório de despesas.</span><span class="sxs-lookup"><span data-stu-id="a6d35-121">The approver approves the expense report.</span></span>
5. <span data-ttu-id="a6d35-122">O relatório de despesas é atribuído ao coordenador de Contas a pagar para publicação.</span><span class="sxs-lookup"><span data-stu-id="a6d35-122">The expense report is assigned to the Accounts payable coordinator for posting.</span></span>
6. <span data-ttu-id="a6d35-123">Ocorre um dos seguintes passos, dependendo se a publicação automática é configurada:</span><span class="sxs-lookup"><span data-stu-id="a6d35-123">One of the following steps occurs, depending on whether automatic posting is configured:</span></span>

    - <span data-ttu-id="a6d35-124">Se o registo automático for configurado, o relatório de despesas é processado para pagamento, e o estado do relatório de despesas é atualizado.</span><span class="sxs-lookup"><span data-stu-id="a6d35-124">If automatic posting is configured, the expense report is processed for payment, and the status of the expense report is updated.</span></span>
    - <span data-ttu-id="a6d35-125">Se a publicação automática não estiver configurada, o coordenador das Contas a pagar verifica que todos os recibos originais foram apresentados e que os recibos estão alinhados com as despesas do relatório de despesas.</span><span class="sxs-lookup"><span data-stu-id="a6d35-125">If automatic posting isn't configured, the Accounts payable coordinator verifies that all original receipts have been submitted, and that the receipts are aligned with the expenses on the expense report.</span></span> <span data-ttu-id="a6d35-126">Todos os códigos fiscais inscritos no relatório de despesas devem também ser verificados como corretos.</span><span class="sxs-lookup"><span data-stu-id="a6d35-126">All tax codes that are entered on the expense report must also be verified as correct.</span></span>

<span data-ttu-id="a6d35-127">Após a verificação destes requisitos, o relatório de despesas é publicado.</span><span class="sxs-lookup"><span data-stu-id="a6d35-127">After these requirements are verified, the expense report is posted.</span></span>

<span data-ttu-id="a6d35-128">Após o relatório de despesas ser publicado, o pagamento é autorizado para o relatório de despesas, e o empregado é reembolsado.</span><span class="sxs-lookup"><span data-stu-id="a6d35-128">After the expense report is posted, payment is authorized for the expense report, and the employee is reimbursed.</span></span>
