---
title: Vários aprovadores no relatório de despesas
description: Este tópico fornece informações sobre relatórios de despesas que requerem aprovação por várias pessoas.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0fbe1c93c5359a6be493e3c4e1b27b06dbb48002
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271727"
---
# <a name="multiple-approvers-on-an-expense-report"></a><span data-ttu-id="d1d34-103">Vários aprovadores no relatório de despesas</span><span class="sxs-lookup"><span data-stu-id="d1d34-103">Multiple approvers on an expense report</span></span>

<span data-ttu-id="d1d34-104">Dependendo das políticas de aprovação de despesas da sua organização, mais de uma pessoa poderá ter de aprovar um relatório de despesas submetido por um funcionário.</span><span class="sxs-lookup"><span data-stu-id="d1d34-104">Depending on your organization's expense approval policies, more than one person might have to approve an expense report that is submitted by an employee.</span></span> <span data-ttu-id="d1d34-105">Quando configurar o processo de fluxo de trabalho para aprovação de relatórios de despesas, pode adicionar elementos de fluxo de trabalho que incluem tarefas ou passos para um ou mais aprovadores de relatórios de despesas.</span><span class="sxs-lookup"><span data-stu-id="d1d34-105">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="d1d34-106">Por exemplo, pode exigir que todos os relatórios de despesas sejam aprovados primeiro pelo o gestor do empregado que apresentou o relatório e, em seguida, pelo coordenador das Contas a pagar.</span><span class="sxs-lookup"><span data-stu-id="d1d34-106">For example, you might require that all expense reports be approved first by the manager of the employee who submitted the report and then by the Accounts payable coordinator.</span></span>

<span data-ttu-id="d1d34-107">Se decidir exigir vários aprovadores de relatórios de despesas, pode adicionar os elementos do fluxo de trabalho de uma das seguintes formas:</span><span class="sxs-lookup"><span data-stu-id="d1d34-107">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="d1d34-108">Adicione um elemento de aprovação que tenha um passo.</span><span class="sxs-lookup"><span data-stu-id="d1d34-108">Add one approval element that has one step.</span></span> <span data-ttu-id="d1d34-109">Por exemplo, o passo pode exigir que um relatório de despesas seja atribuído a um grupo de utilizadores e que seja aprovado por 50% dos membros do grupo de utilizadores.</span><span class="sxs-lookup"><span data-stu-id="d1d34-109">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="d1d34-110">Adicione um elemento de aprovação que tenha múltiplos passos.</span><span class="sxs-lookup"><span data-stu-id="d1d34-110">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="d1d34-111">Por exemplo, o elemento de aprovação pode ter os seguintes passos:</span><span class="sxs-lookup"><span data-stu-id="d1d34-111">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="d1d34-112">O gestor do empregado que apresentou o relatório de despesas aprova-o.</span><span class="sxs-lookup"><span data-stu-id="d1d34-112">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="d1d34-113">O funcionários responsável pelas contas a pagar verifica os recibos e os itens de relatório de despesas.</span><span class="sxs-lookup"><span data-stu-id="d1d34-113">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="d1d34-114">O proprietário do orçamento aprova o relatório de despesas.</span><span class="sxs-lookup"><span data-stu-id="d1d34-114">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="d1d34-115">Adicione vários elementos de aprovação, cada um dos quais com um passo.</span><span class="sxs-lookup"><span data-stu-id="d1d34-115">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="d1d34-116">Por exemplo, pode adicionar um elemento de aprovação separado para cada uma das seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="d1d34-116">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="d1d34-117">O gestor do funcionário aprova o relatório de despesas.</span><span class="sxs-lookup"><span data-stu-id="d1d34-117">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="d1d34-118">O proprietário do orçamento aprova o relatório de despesas.</span><span class="sxs-lookup"><span data-stu-id="d1d34-118">The budget owner approves the expense report.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]