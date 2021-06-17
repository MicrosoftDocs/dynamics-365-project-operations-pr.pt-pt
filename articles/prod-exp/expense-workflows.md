---
title: Configurar fluxos de trabalho de gestão de Despesas
description: Pode configurar um processo de fluxo de trabalho usado para rever e aprovar documentos de viagem e despesas.
author: ShylaThompson
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4070b4fb5109464abdabbce971688fb881dfcf2c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005130"
---
# <a name="set-up-expense-management-workflows"></a><span data-ttu-id="04a5f-103">Configurar fluxos de trabalho de gestão de Despesas</span><span class="sxs-lookup"><span data-stu-id="04a5f-103">Set up Expense management workflows</span></span>

<span data-ttu-id="04a5f-104">Pode configurar um processo de fluxo de trabalho usado para rever e aprovar documentos de viagem e despesas.</span><span class="sxs-lookup"><span data-stu-id="04a5f-104">You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="04a5f-105">Os documentos para os quais os fluxos de trabalho podem ser definidos para incluir relatórios de despesas, requisições de viagem e pedidos de adiantamento de dinheiro.</span><span class="sxs-lookup"><span data-stu-id="04a5f-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="04a5f-106">Um fluxo de trabalho representa um processo de negócio.</span><span class="sxs-lookup"><span data-stu-id="04a5f-106">A workflow represents a business process.</span></span> <span data-ttu-id="04a5f-107">Define como um documento flui através do sistema e indica quem deve completar uma tarefa ou aprovar um documento.</span><span class="sxs-lookup"><span data-stu-id="04a5f-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="04a5f-108">Existem vários benefícios ao usar o sistema de fluxo de trabalho na sua organização:</span><span class="sxs-lookup"><span data-stu-id="04a5f-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="04a5f-109">**Processos consistentes** – Pode definir o processo de aprovação de documentos específicos, como requisições de compras e relatórios de despesas.</span><span class="sxs-lookup"><span data-stu-id="04a5f-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="04a5f-110">A utilização do sistema de fluxo de trabalho ajuda a garantir que os documentos são processados e aprovados de forma consistente e eficiente.</span><span class="sxs-lookup"><span data-stu-id="04a5f-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="04a5f-111">Visibilidade do processo – Pode acompanhar o estado, o histórico e as métricas de desempenho de uma instância específica de fluxo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="04a5f-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="04a5f-112">Isto ajuda-o a determinar se devem ser feitas alterações ao fluxo de trabalho para melhorar a eficiência.</span><span class="sxs-lookup"><span data-stu-id="04a5f-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="04a5f-113">Lista de trabalho centralizada – Os utilizadores podem visualizar uma lista de trabalho centralizada para visualizar as tarefas e aprovações de fluxo de trabalho que lhes são atribuídas.</span><span class="sxs-lookup"><span data-stu-id="04a5f-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="04a5f-114">**Os tipos de fluxos de trabalho que pode criar**</span><span class="sxs-lookup"><span data-stu-id="04a5f-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="04a5f-115">A tabela seguinte lista os tipos de fluxos de trabalho que pode criar em **Despesas**.</span><span class="sxs-lookup"><span data-stu-id="04a5f-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>


|              <span data-ttu-id="04a5f-116"><strong>Tipo</strong></span><span class="sxs-lookup"><span data-stu-id="04a5f-116"><strong>Type</strong></span></span>              |                   <span data-ttu-id="04a5f-117"><strong>Use este tipo para</strong></span><span class="sxs-lookup"><span data-stu-id="04a5f-117"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <span data-ttu-id="04a5f-118"><strong>Relatório de despesas</strong></span><span class="sxs-lookup"><span data-stu-id="04a5f-118"><strong>Expense report</strong></span></span>         |            <span data-ttu-id="04a5f-119">Criar aprovação de fluxos de trabalho para relatórios de despesas.</span><span class="sxs-lookup"><span data-stu-id="04a5f-119">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="04a5f-120"><strong>Publicar automaticamente relatórios de despesas</strong></span><span class="sxs-lookup"><span data-stu-id="04a5f-120"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="04a5f-121">Criar automaticamente a publicação de fluxos de trabalho para relatórios de despesas.</span><span class="sxs-lookup"><span data-stu-id="04a5f-121">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="04a5f-122"><strong>Item de linha de despesa</strong></span><span class="sxs-lookup"><span data-stu-id="04a5f-122"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="04a5f-123">Criar aprovação de fluxos de trabalho para itens de linha nos relatórios de despesas.</span><span class="sxs-lookup"><span data-stu-id="04a5f-123">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="04a5f-124"><strong>Publicação automática de item de linha de despesas</strong></span><span class="sxs-lookup"><span data-stu-id="04a5f-124"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="04a5f-125">Criar publicação automática de fluxos de trabalho para itens de linha nos relatórios de despesas.</span><span class="sxs-lookup"><span data-stu-id="04a5f-125">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="04a5f-126"><strong>Requisição de viagens</strong></span><span class="sxs-lookup"><span data-stu-id="04a5f-126"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="04a5f-127">Criar aprovação de fluxos de trabalho para requisições de viagem.</span><span class="sxs-lookup"><span data-stu-id="04a5f-127">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="04a5f-128"><strong>Pedido de adiantamento de dinheiro</strong></span><span class="sxs-lookup"><span data-stu-id="04a5f-128"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="04a5f-129">Criar aprovação de fluxos de trabalho para pedidos de adiantamento de dinheiro.</span><span class="sxs-lookup"><span data-stu-id="04a5f-129">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="04a5f-130"><strong>Recuperação da taxa de IVA</strong></span><span class="sxs-lookup"><span data-stu-id="04a5f-130"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="04a5f-131">Criar aprovação de fluxos de trabalho para a recuperação do imposto sobre o valor acrescentado (IVA).</span><span class="sxs-lookup"><span data-stu-id="04a5f-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |



[!INCLUDE[footer-include](../includes/footer-banner.md)]