---
title: Configurar fluxos de trabalho para a gestão de despesas
description: Pode configurar um processo de fluxo de trabalho usado para rever e aprovar documentos de viagem e despesas.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: dfc5945f32bb8d4073fc31499979ba279fef66a4
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896565"
---
# <a name="set-up-workflows-for-expense-management"></a><span data-ttu-id="b933f-103">Configurar fluxos de trabalho para a gestão de despesas</span><span class="sxs-lookup"><span data-stu-id="b933f-103">Set up workflows for Expense management</span></span>

<span data-ttu-id="b933f-104">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="b933f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b933f-105">Pode configurar um processo de fluxo de trabalho usado para rever e aprovar documentos de viagem e despesas.</span><span class="sxs-lookup"><span data-stu-id="b933f-105">You can set up a workflow process to review and approve travel and expense documents.</span></span> <span data-ttu-id="b933f-106">Pode definir fluxos de trabalho para relatórios de despesas, requisições de viagem e pedidos de adiantamento de dinheiro.</span><span class="sxs-lookup"><span data-stu-id="b933f-106">You can define workflows for expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="b933f-107">Um fluxo de trabalho representa um processo de negócio e define como um documento flui através do sistema.</span><span class="sxs-lookup"><span data-stu-id="b933f-107">A workflow represents a business process and defines how a document flows through the system.</span></span> <span data-ttu-id="b933f-108">O fluxo de trabalho também indica quem deve completar uma tarefa ou aprovar um documento.</span><span class="sxs-lookup"><span data-stu-id="b933f-108">The workflow also indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="b933f-109">Existem vários benefícios ao usar o sistema de fluxo de trabalho na sua organização:</span><span class="sxs-lookup"><span data-stu-id="b933f-109">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="b933f-110">**Processos consistentes**: Pode definir o processo de aprovação de documentos específicos, como requisições de compras e relatórios de despesas.</span><span class="sxs-lookup"><span data-stu-id="b933f-110">**Consistent processes**: You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="b933f-111">A utilização do sistema de fluxo de trabalho ajuda a garantir que os documentos são processados e aprovados de forma consistente e eficiente.</span><span class="sxs-lookup"><span data-stu-id="b933f-111">Using the workflow system helps ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="b933f-112">**Visibilidade do processo**: Pode acompanhar o estado, o histórico e as métricas de desempenho de uma instância específica de fluxo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="b933f-112">**Process visibility**: You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="b933f-113">Isto ajuda-o a determinar se devem ser feitas alterações ao fluxo de trabalho para melhorar a eficiência.</span><span class="sxs-lookup"><span data-stu-id="b933f-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="b933f-114">**Lista de trabalho centralizada**: Os utilizadores podem visualizar uma lista de trabalho centralizada para visualizar as tarefas e aprovações de fluxo de trabalho que lhes são atribuídas.</span><span class="sxs-lookup"><span data-stu-id="b933f-114">**Centralized work list**: Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

## <a name="workflow-types"></a><span data-ttu-id="b933f-115">Tipos de fluxo de trabalho</span><span class="sxs-lookup"><span data-stu-id="b933f-115">Workflow types</span></span>

<span data-ttu-id="b933f-116">A tabela seguinte lista os tipos de fluxos de trabalho que pode criar em **Gestão de despesas**.</span><span class="sxs-lookup"><span data-stu-id="b933f-116">The following table lists the types of workflows that you can create in **Expense Management**.</span></span>


|              <span data-ttu-id="b933f-117"><strong>Tipo</strong></span><span class="sxs-lookup"><span data-stu-id="b933f-117"><strong>Type</strong></span></span>              |                   <span data-ttu-id="b933f-118"><strong>Use este tipo para</strong></span><span class="sxs-lookup"><span data-stu-id="b933f-118"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <span data-ttu-id="b933f-119"><strong>Aprovar automaticamente relatórios de despesas</strong></span><span class="sxs-lookup"><span data-stu-id="b933f-119"><strong>Expense report auto approval</strong></span></span> |            <span data-ttu-id="b933f-120">Criar aprovação de fluxos de trabalho para relatórios de despesas.</span><span class="sxs-lookup"><span data-stu-id="b933f-120">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="b933f-121"><strong>Publicar automaticamente relatórios de despesas</strong></span><span class="sxs-lookup"><span data-stu-id="b933f-121"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="b933f-122">Criar automaticamente a publicação de fluxos de trabalho para relatórios de despesas.</span><span class="sxs-lookup"><span data-stu-id="b933f-122">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="b933f-123"><strong>Item de linha de despesa</strong></span><span class="sxs-lookup"><span data-stu-id="b933f-123"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="b933f-124">Criar aprovação de fluxos de trabalho para itens de linha nos relatórios de despesas.</span><span class="sxs-lookup"><span data-stu-id="b933f-124">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="b933f-125"><strong>Publicação automática de item de linha de despesas</strong></span><span class="sxs-lookup"><span data-stu-id="b933f-125"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="b933f-126">Criar publicação automática de fluxos de trabalho para itens de linha nos relatórios de despesas.</span><span class="sxs-lookup"><span data-stu-id="b933f-126">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="b933f-127"><strong>Requisição de viagens</strong></span><span class="sxs-lookup"><span data-stu-id="b933f-127"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="b933f-128">Criar aprovação de fluxos de trabalho para requisições de viagem.</span><span class="sxs-lookup"><span data-stu-id="b933f-128">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="b933f-129"><strong>Pedido de adiantamento de dinheiro</strong></span><span class="sxs-lookup"><span data-stu-id="b933f-129"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="b933f-130">Criar aprovação de fluxos de trabalho para pedidos de adiantamento de dinheiro.</span><span class="sxs-lookup"><span data-stu-id="b933f-130">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="b933f-131"><strong>Recuperação da taxa de IVA</strong></span><span class="sxs-lookup"><span data-stu-id="b933f-131"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="b933f-132">Criar aprovação de fluxos de trabalho para a recuperação do imposto sobre o valor acrescentado (IVA).</span><span class="sxs-lookup"><span data-stu-id="b933f-132">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |