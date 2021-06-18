---
title: Analisar o registo de tarefas de faturação nos projetos e contratos do projeto
description: Este tópico fornece informações sobre como analisar o tempo, as despesas e os registos de tarefas dos produtos e como marcá-los como prontos para faturação.
author: rumant
ms.custom: ''
ms.author: rumant
ms.date: 03/11/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: cec09ca39563e3faf0f3b2c10cf9bde3feb020b0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008550"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a><span data-ttu-id="eb7f0-103">Analisar o registo de tarefas de faturação nos projetos e contratos do projeto</span><span class="sxs-lookup"><span data-stu-id="eb7f0-103">Review the invoicing backlog on projects and project contracts</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="eb7f0-104">Quando uma transação está pronta para ter uma fatura criada e processada, a transação deve estar marcada como **Pronta para faturar**.</span><span class="sxs-lookup"><span data-stu-id="eb7f0-104">When a transaction is ready to have an invoice created and processed, the transaction should be marked **Ready to invoice**.</span></span> <span data-ttu-id="eb7f0-105">Este tópico descreve os tipos de transações que podem ser criadas.</span><span class="sxs-lookup"><span data-stu-id="eb7f0-105">This topic describes the types of transactions that can be created.</span></span>

## <a name="review-the-time-and-material-billing-backlog"></a><span data-ttu-id="eb7f0-106">Analisar o registo de tarefas de faturação de tempo e material</span><span class="sxs-lookup"><span data-stu-id="eb7f0-106">Review the time and material billing backlog</span></span>

<span data-ttu-id="eb7f0-107">Quando uma entrada de tempo ou despesa é submetida e aprovada para um projeto, o PSA cria um valor real do projeto.</span><span class="sxs-lookup"><span data-stu-id="eb7f0-107">When a time or expense entry is submitted and approved for a project, PSA creates a project actual.</span></span> <span data-ttu-id="eb7f0-108">Se a combinação do projeto e a classe de transação forem mapeadas para um item de contrato para um projeto de tempo e materiais, serão criados dois valores reais quando a entrada for aprovada:</span><span class="sxs-lookup"><span data-stu-id="eb7f0-108">If the combination of the project and the transaction class are mapped to a contract line for a time-and-materials project, two actuals are created when the entry is approved:</span></span>

- <span data-ttu-id="eb7f0-109">Custo real</span><span class="sxs-lookup"><span data-stu-id="eb7f0-109">Cost actual</span></span> 
- <span data-ttu-id="eb7f0-110">Valor real de vendas não faturadas</span><span class="sxs-lookup"><span data-stu-id="eb7f0-110">Unbilled sales actual</span></span>

<span data-ttu-id="eb7f0-111">Os valores reais de vendas não faturadas representam o registo de tarefas de faturação, sendo que o seu estado de faturação tem de ser definido como **Pronto para Faturar**.</span><span class="sxs-lookup"><span data-stu-id="eb7f0-111">Unbilled sales actuals represent the billing backlog, and their billing status must be set to **Ready to Invoice**.</span></span> <span data-ttu-id="eb7f0-112">Quando é criada uma fatura do projeto, os valores reais de vendas não faturadas marcados como **Prontos para Faturar** são copiados como detalhes de linha de fatura.</span><span class="sxs-lookup"><span data-stu-id="eb7f0-112">When a project invoice is created, unbilled sales actuals that are marked **Ready to Invoice** are copied over as invoice line details.</span></span>

<span data-ttu-id="eb7f0-113">Para analisar o registo de tarefas pendentes de faturação para tempo e materiais, aceda a **Vendas** \> **Faturação** \> **Registo de Tarefas Pendentes de Faturação de Tempo e Material**.</span><span class="sxs-lookup"><span data-stu-id="eb7f0-113">To review the billing backlog for time and materials, go to **Sales** \> **Billing** \> **Time and Material Billing Backlog**.</span></span> <span data-ttu-id="eb7f0-114">Selecione todos os valores reais de vendas não faturadas que estão prontos para serem faturados e, em seguida, selecione **Pronto para Faturar**.</span><span class="sxs-lookup"><span data-stu-id="eb7f0-114">Select all the unbilled sales actuals that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="eb7f0-115">O estado de faturação destes valores reais é alterado para **Pronto para Faturar**.</span><span class="sxs-lookup"><span data-stu-id="eb7f0-115">The billing status of these actuals is changed to **Ready to Invoice**.</span></span>

![Registo de tarefas pendentes de faturação de tempo e material](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a><span data-ttu-id="eb7f0-117">Analisar o registo de tarefas pendentes de faturação de produtos</span><span class="sxs-lookup"><span data-stu-id="eb7f0-117">Review the product billing backlog</span></span>

<span data-ttu-id="eb7f0-118">No PSA, quando um contrato do projeto tem itens de contrato baseados em produtos, esses itens são considerados para faturação sempre que é criada uma fatura para o contrato do projeto.</span><span class="sxs-lookup"><span data-stu-id="eb7f0-118">In PSA, when a project contract has product-based contract lines, those lines are considered for invoicing whenever an invoice is created for the project contract.</span></span> <span data-ttu-id="eb7f0-119">Qualquer produto que tenha itens de contrato marcados como **Pronto para Faturar** é copiado para a fatura do projeto como linhas de fatura do projeto.</span><span class="sxs-lookup"><span data-stu-id="eb7f0-119">Any product that has contract lines that are marked **Ready to Invoice** is copied over to the project invoice as project invoice lines.</span></span>

<span data-ttu-id="eb7f0-120">Para analisar o registo de tarefas pendentes de faturação de produtos, aceda a **Vendas** \> **Faturação** \> **Registo de Tarefas Pendentes de Faturação de Produtos**.</span><span class="sxs-lookup"><span data-stu-id="eb7f0-120">To review the billing backlog for products, go to **Sales** \> **Billing** \> **Product Billing Backlog**.</span></span> <span data-ttu-id="eb7f0-121">Selecione todos os itens de contrato baseados em produtos que estão prontos para serem faturados e, em seguida, selecione **Pronto para Faturar**.</span><span class="sxs-lookup"><span data-stu-id="eb7f0-121">Select all the product-based contract lines that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="eb7f0-122">O estado de faturação destes itens é alterado para **Pronto para Faturar**.</span><span class="sxs-lookup"><span data-stu-id="eb7f0-122">The billing status of these lines is changed to **Ready to Invoice**.</span></span>

![Registo de tarefas pendentes de faturação de produtos](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a><span data-ttu-id="eb7f0-124">Analisar marcos de faturação em contratos de preço fixo</span><span class="sxs-lookup"><span data-stu-id="eb7f0-124">Review billing milestones on fixed-price contracts</span></span>

<span data-ttu-id="eb7f0-125">Cada item de contrato do projeto com um método de faturação de preço fixo tem de definir os marcos do contrato.</span><span class="sxs-lookup"><span data-stu-id="eb7f0-125">Each project contract line that has a fixed-price billing method must define contract milestones.</span></span> <span data-ttu-id="eb7f0-126">Estes marcos do contrato só podem ser faturados se estiverem marcados como **Pronto para Faturar**.</span><span class="sxs-lookup"><span data-stu-id="eb7f0-126">These contract milestones can be invoiced only if they are marked **Ready to Invoice**.</span></span> 

<span data-ttu-id="eb7f0-127">Para analisar os marcos de faturação, aceda a **Vendas** \> **Faturação** \> **Marcos de Preço Fixo**.</span><span class="sxs-lookup"><span data-stu-id="eb7f0-127">To review billing milestones, go to **Sales** \> **Billing** \> **Fixed Price Milestones**.</span></span> <span data-ttu-id="eb7f0-128">Selecione os marcos que estão prontos para serem faturados e, em seguida, selecione **Pronto para faturar**.</span><span class="sxs-lookup"><span data-stu-id="eb7f0-128">Select the milestones that are ready to be invoiced, and then select **Ready to invoice**.</span></span> <span data-ttu-id="eb7f0-129">O estado de faturação destes marcos é alterado para **Pronto para Faturar**.</span><span class="sxs-lookup"><span data-stu-id="eb7f0-129">The billing status of these milestones is changed to **Ready to Invoice**.</span></span>

![Marcos de preço fixo](media/FPBacklog.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]