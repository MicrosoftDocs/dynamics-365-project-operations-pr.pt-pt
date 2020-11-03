---
title: Relatórios de despesas e vários aprovadores
description: Este tópico fornece informações sobre relatórios de despesas que requerem aprovação por mais de uma pessoa.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 548673541cee5ce598721f94415c0444995c8325
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082407"
---
# <a name="expense-reports-and-multiple-approvers"></a><span data-ttu-id="52d35-103">Relatórios de despesas e vários aprovadores</span><span class="sxs-lookup"><span data-stu-id="52d35-103">Expense reports and multiple approvers</span></span>

<span data-ttu-id="52d35-104">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="52d35-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="52d35-105">Dependendo das políticas de aprovação de despesas da sua organização, mais de uma pessoa poderá ter de aprovar um relatório de despesas apresentado.</span><span class="sxs-lookup"><span data-stu-id="52d35-105">Depending on your organization's expense approval policies, more than one person might have to approve a submitted expense report.</span></span> <span data-ttu-id="52d35-106">Quando configurar o processo de fluxo de trabalho para aprovação de relatórios de despesas, pode adicionar elementos de fluxo de trabalho que incluem tarefas ou passos para um ou mais aprovadores de relatórios de despesas.</span><span class="sxs-lookup"><span data-stu-id="52d35-106">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="52d35-107">Por exemplo, pode exigir que todos os relatórios de despesas sejam aprovados por duas pessoas distintas, o gestor do empregado que apresentou o relatório e o coordenador das Contas a pagar.</span><span class="sxs-lookup"><span data-stu-id="52d35-107">For example, you might require that all expense reports be approved by two separate people, the manager of the employee who submitted the report and the Accounts payable coordinator.</span></span>

<span data-ttu-id="52d35-108">Se decidir exigir vários aprovadores de relatórios de despesas, pode adicionar os elementos do fluxo de trabalho de uma das seguintes formas:</span><span class="sxs-lookup"><span data-stu-id="52d35-108">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="52d35-109">Adicione um elemento de aprovação que tenha um passo.</span><span class="sxs-lookup"><span data-stu-id="52d35-109">Add one approval element that has one step.</span></span> <span data-ttu-id="52d35-110">Por exemplo, o passo pode exigir que um relatório de despesas seja atribuído a um grupo de utilizadores e que seja aprovado por 50% dos membros do grupo de utilizadores.</span><span class="sxs-lookup"><span data-stu-id="52d35-110">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="52d35-111">Adicione um elemento de aprovação que tenha múltiplos passos.</span><span class="sxs-lookup"><span data-stu-id="52d35-111">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="52d35-112">Por exemplo, o elemento de aprovação pode ter os seguintes passos:</span><span class="sxs-lookup"><span data-stu-id="52d35-112">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="52d35-113">O gestor do empregado que apresentou o relatório de despesas aprova-o.</span><span class="sxs-lookup"><span data-stu-id="52d35-113">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="52d35-114">O funcionários responsável pelas contas a pagar verifica os recibos e os itens de relatório de despesas.</span><span class="sxs-lookup"><span data-stu-id="52d35-114">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="52d35-115">O proprietário do orçamento aprova o relatório de despesas.</span><span class="sxs-lookup"><span data-stu-id="52d35-115">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="52d35-116">Adicione vários elementos de aprovação, cada um dos quais com um passo.</span><span class="sxs-lookup"><span data-stu-id="52d35-116">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="52d35-117">Por exemplo, pode adicionar um elemento de aprovação separado para cada uma das seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="52d35-117">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="52d35-118">O gestor do funcionário aprova o relatório de despesas.</span><span class="sxs-lookup"><span data-stu-id="52d35-118">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="52d35-119">O proprietário do orçamento aprova o relatório de despesas.</span><span class="sxs-lookup"><span data-stu-id="52d35-119">The budget owner approves the expense report.</span></span>
