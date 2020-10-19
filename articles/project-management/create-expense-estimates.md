---
title: Estimativas de despesas
description: Este tópico fornece informações sobre como definir ou estimar as despesas baseadas em projetos.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2afe4ff2f84fc5426c409e6314da73b11a4de281
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908472"
---
# <a name="expense-estimates"></a><span data-ttu-id="0c38f-103">Estimativas de despesas</span><span class="sxs-lookup"><span data-stu-id="0c38f-103">Expense estimates</span></span>
<span data-ttu-id="0c38f-104">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="0c38f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0c38f-105">Juntamente com a definição das estimativas baseadas em recursos, o Dynamics 365 Project Operations permite aos Gestores de projetos definir despesas baseadas em projetos para cada projeto.</span><span class="sxs-lookup"><span data-stu-id="0c38f-105">Along with defining resource-based estimates, Dynamics 365 Project Operations allows Project managers to define project-based expenses for each project.</span></span> <span data-ttu-id="0c38f-106">Cada item de despesa pode ser associado a uma tarefa de projeto ou categoria de despesa específica.</span><span class="sxs-lookup"><span data-stu-id="0c38f-106">Each expense item can be associated with a specific project task or expense category.</span></span> <span data-ttu-id="0c38f-107">Normalmente, as categorias de despesas são definidas a nível organizacional.</span><span class="sxs-lookup"><span data-stu-id="0c38f-107">Expense categories are typically defined at the organizational level.</span></span> <span data-ttu-id="0c38f-108">Normalmente, os preços para cada categoria de despesa são definidos na seguinte hierarquia:</span><span class="sxs-lookup"><span data-stu-id="0c38f-108">Pricing for each expense category is typically defined in the following hierarchy:</span></span>

- <span data-ttu-id="0c38f-109">Organização</span><span class="sxs-lookup"><span data-stu-id="0c38f-109">Organization</span></span>
- <span data-ttu-id="0c38f-110">Cliente</span><span class="sxs-lookup"><span data-stu-id="0c38f-110">Customer</span></span>
- <span data-ttu-id="0c38f-111">Proposta/contrato</span><span class="sxs-lookup"><span data-stu-id="0c38f-111">Quote/contract</span></span>

<span data-ttu-id="0c38f-112">Execute os seguintes passos para ver, adicionar ou eliminar uma despesa do projeto.</span><span class="sxs-lookup"><span data-stu-id="0c38f-112">Complete the following steps to view, add, or delete a project expense.</span></span>

1. <span data-ttu-id="0c38f-113">Vá para **Projetos** e selecione o projeto em que pretende trabalhar.</span><span class="sxs-lookup"><span data-stu-id="0c38f-113">Go to **Projects**, and select the project you want to work on.</span></span>
2. <span data-ttu-id="0c38f-114">Selecione o separador **Estimativas do Projeto** e consulte a lista de despesas do projeto.</span><span class="sxs-lookup"><span data-stu-id="0c38f-114">Select the **Project Estimates** tab and view the list of project expenses.</span></span>
3. <span data-ttu-id="0c38f-115">Selecione **Nova Despesa** para adicionar uma despesa.</span><span class="sxs-lookup"><span data-stu-id="0c38f-115">Select **New Expense** to add an expense.</span></span> <span data-ttu-id="0c38f-116">Também pode selecionar uma despesa a eliminar e, em seguida, selecionar **Eliminar Despesa**.</span><span class="sxs-lookup"><span data-stu-id="0c38f-116">Or, select an expense to delete, and then select **Delete Expense**.</span></span>

<span data-ttu-id="0c38f-117">Os seguintes atributos são definidos para cada item da linha de despesa:</span><span class="sxs-lookup"><span data-stu-id="0c38f-117">The following attributes are defined for each expense line item:</span></span>

- <span data-ttu-id="0c38f-118">**Categoria**: os agrupamentos comuns utilizados para descrever todas as despesas incorridas num projeto.</span><span class="sxs-lookup"><span data-stu-id="0c38f-118">**Category**: The common groupings used to describe all expenses incurred on a project.</span></span>
- <span data-ttu-id="0c38f-119">**Data de Início**: a data em que se prevê que a despesa seja incorrida.</span><span class="sxs-lookup"><span data-stu-id="0c38f-119">**Start Date**: The date when the expense is forecasted to be incurred.</span></span>
- <span data-ttu-id="0c38f-120">**Quantidade**: número estimado de itens de despesa para uma categoria específica.</span><span class="sxs-lookup"><span data-stu-id="0c38f-120">**Quantity**: The estimated number of expense items for a specific category.</span></span>
- <span data-ttu-id="0c38f-121">**Preço do Custo Unitário**: o preço unitário utilizado para calcular o custo da despesa.</span><span class="sxs-lookup"><span data-stu-id="0c38f-121">**Unit Cost Price**: The unit price used to calculate to cost of the expense.</span></span>
- <span data-ttu-id="0c38f-122">**Preço de Venda Unitário**: o preço unitário utilizado para calcular os preços de venda da despesa.</span><span class="sxs-lookup"><span data-stu-id="0c38f-122">**Unit Sales Price**: The unit price used to calculate the sale prices of the expense.</span></span>

