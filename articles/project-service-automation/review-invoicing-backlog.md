---
title: Analisar o registo de tarefas de faturação nos projetos e contratos do projeto
description: Este tópico fornece informações sobre como analisar o tempo, as despesas e os registos de tarefas dos produtos e como marcá-los como prontos para faturação.
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 03/11/2019
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 2.x and 3.x
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: db15ea136b9939c0a0631936bcadab538bf2dd4a
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754585"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a><span data-ttu-id="729c7-103">Analisar o registo de tarefas de faturação nos projetos e contratos do projeto</span><span class="sxs-lookup"><span data-stu-id="729c7-103">Review the invoicing backlog on projects and project contracts</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="729c7-104">Quando uma transação está pronta para ter uma fatura criada e processada, a transação deve estar marcada como **Pronta para faturar**.</span><span class="sxs-lookup"><span data-stu-id="729c7-104">When a transaction is ready to have an invoice created and processed, the transaction should be marked **Ready to invoice**.</span></span> <span data-ttu-id="729c7-105">Este tópico descreve os tipos de transações que podem ser criadas.</span><span class="sxs-lookup"><span data-stu-id="729c7-105">This topic describes the types of transactions that can be created.</span></span>

## <a name="review-the-time-and-material-billing-backlog"></a><span data-ttu-id="729c7-106">Analisar o registo de tarefas de faturação de tempo e material</span><span class="sxs-lookup"><span data-stu-id="729c7-106">Review the time and material billing backlog</span></span>

<span data-ttu-id="729c7-107">Quando uma entrada de tempo ou despesa é submetida e aprovada para um projeto, o PSA cria um valor real do projeto.</span><span class="sxs-lookup"><span data-stu-id="729c7-107">When a time or expense entry is submitted and approved for a project, PSA creates a project actual.</span></span> <span data-ttu-id="729c7-108">Se a combinação do projeto e a classe de transação forem mapeadas para um item de contrato para um projeto de tempo e materiais, serão criados dois valores reais quando a entrada for aprovada:</span><span class="sxs-lookup"><span data-stu-id="729c7-108">If the combination of the project and the transaction class are mapped to a contract line for a time-and-materials project, two actuals are created when the entry is approved:</span></span>

- <span data-ttu-id="729c7-109">Custo real</span><span class="sxs-lookup"><span data-stu-id="729c7-109">Cost actual</span></span> 
- <span data-ttu-id="729c7-110">Valor real de vendas não faturadas</span><span class="sxs-lookup"><span data-stu-id="729c7-110">Unbilled sales actual</span></span>

<span data-ttu-id="729c7-111">Os valores reais de vendas não faturadas representam o registo de tarefas de faturação, sendo que o seu estado de faturação tem de ser definido como **Pronto para Faturar**.</span><span class="sxs-lookup"><span data-stu-id="729c7-111">Unbilled sales actuals represent the billing backlog, and their billing status must be set to **Ready to Invoice**.</span></span> <span data-ttu-id="729c7-112">Quando é criada uma fatura do projeto, os valores reais de vendas não faturadas marcados como **Prontos para Faturar** são copiados como detalhes de linha de fatura.</span><span class="sxs-lookup"><span data-stu-id="729c7-112">When a project invoice is created, unbilled sales actuals that are marked **Ready to Invoice** are copied over as invoice line details.</span></span>

<span data-ttu-id="729c7-113">Para analisar o registo de tarefas pendentes de faturação para tempo e materiais, aceda a **Vendas** \> **Faturação** \> **Registo de Tarefas Pendentes de Faturação de Tempo e Material**.</span><span class="sxs-lookup"><span data-stu-id="729c7-113">To review the billing backlog for time and materials, go to **Sales** \> **Billing** \> **Time and Material Billing Backlog**.</span></span> <span data-ttu-id="729c7-114">Selecione todos os valores reais de vendas não faturadas que estão prontos para serem faturados e, em seguida, selecione **Pronto para Faturar**.</span><span class="sxs-lookup"><span data-stu-id="729c7-114">Select all the unbilled sales actuals that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="729c7-115">O estado de faturação destes valores reais é alterado para **Pronto para Faturar**.</span><span class="sxs-lookup"><span data-stu-id="729c7-115">The billing status of these actuals is changed to **Ready to Invoice**.</span></span>

![Registo de tarefas pendentes de faturação de tempo e material](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a><span data-ttu-id="729c7-117">Analisar o registo de tarefas pendentes de faturação de produtos</span><span class="sxs-lookup"><span data-stu-id="729c7-117">Review the product billing backlog</span></span>

<span data-ttu-id="729c7-118">No PSA, quando um contrato do projeto tem itens de contrato baseados em produtos, esses itens são considerados para faturação sempre que é criada uma fatura para o contrato do projeto.</span><span class="sxs-lookup"><span data-stu-id="729c7-118">In PSA, when a project contract has product-based contract lines, those lines are considered for invoicing whenever an invoice is created for the project contract.</span></span> <span data-ttu-id="729c7-119">Qualquer produto que tenha itens de contrato marcados como **Pronto para Faturar** é copiado para a fatura do projeto como linhas de fatura do projeto.</span><span class="sxs-lookup"><span data-stu-id="729c7-119">Any product that has contract lines that are marked **Ready to Invoice** is copied over to the project invoice as project invoice lines.</span></span>

<span data-ttu-id="729c7-120">Para analisar o registo de tarefas pendentes de faturação de produtos, aceda a **Vendas** \> **Faturação** \> **Registo de Tarefas Pendentes de Faturação de Produtos**.</span><span class="sxs-lookup"><span data-stu-id="729c7-120">To review the billing backlog for products, go to **Sales** \> **Billing** \> **Product Billing Backlog**.</span></span> <span data-ttu-id="729c7-121">Selecione todos os itens de contrato baseados em produtos que estão prontos para serem faturados e, em seguida, selecione **Pronto para Faturar**.</span><span class="sxs-lookup"><span data-stu-id="729c7-121">Select all the product-based contract lines that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="729c7-122">O estado de faturação destes itens é alterado para **Pronto para Faturar**.</span><span class="sxs-lookup"><span data-stu-id="729c7-122">The billing status of these lines is changed to **Ready to Invoice**.</span></span>

![Registo de tarefas pendentes de faturação de produtos](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a><span data-ttu-id="729c7-124">Analisar marcos de faturação em contratos de preço fixo</span><span class="sxs-lookup"><span data-stu-id="729c7-124">Review billing milestones on fixed-price contracts</span></span>

<span data-ttu-id="729c7-125">Cada item de contrato do projeto com um método de faturação de preço fixo tem de definir os marcos do contrato.</span><span class="sxs-lookup"><span data-stu-id="729c7-125">Each project contract line that has a fixed-price billing method must define contract milestones.</span></span> <span data-ttu-id="729c7-126">Estes marcos do contrato só podem ser faturados se estiverem marcados como **Pronto para Faturar**.</span><span class="sxs-lookup"><span data-stu-id="729c7-126">These contract milestones can be invoiced only if they are marked **Ready to Invoice**.</span></span> 

<span data-ttu-id="729c7-127">Para analisar os marcos de faturação, aceda a **Vendas** \> **Faturação** \> **Marcos de Preço Fixo**.</span><span class="sxs-lookup"><span data-stu-id="729c7-127">To review billing milestones, go to **Sales** \> **Billing** \> **Fixed Price Milestones**.</span></span> <span data-ttu-id="729c7-128">Selecione os marcos que estão prontos para serem faturados e, em seguida, selecione **Pronto para faturar**.</span><span class="sxs-lookup"><span data-stu-id="729c7-128">Select the milestones that are ready to be invoiced, and then select **Ready to invoice**.</span></span> <span data-ttu-id="729c7-129">O estado de faturação destes marcos é alterado para **Pronto para Faturar**.</span><span class="sxs-lookup"><span data-stu-id="729c7-129">The billing status of these milestones is changed to **Ready to Invoice**.</span></span>

![Marcos de preço fixo](media/FPBacklog.png)
