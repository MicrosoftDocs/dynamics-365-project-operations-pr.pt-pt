---
title: Configurar a faturação de projetos entre empresas
description: Este tópico mostra como configuração a faturação de projetos entre duas empresas na sua organização.
author: Yowelle
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9df15cb3712356a164de3507f5dbc17a9ff9a652
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288393"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="37891-103">Configurar a faturação de projetos entre empresas</span><span class="sxs-lookup"><span data-stu-id="37891-103">Configure intercompany project invoicing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="37891-104">Este tópico mostra como configuração a faturação de projetos entre duas empresas na sua organização.</span><span class="sxs-lookup"><span data-stu-id="37891-104">This topic shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="37891-105">Esta tarefa utiliza o conjunto de dados USSI.</span><span class="sxs-lookup"><span data-stu-id="37891-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="37891-106">No painel de navegação, vá para **Módulos > Contas a pagar > Fornecedores > Todos os fornecedores**.</span><span class="sxs-lookup"><span data-stu-id="37891-106">In the navigation pane, go to **Modules > Accounts payable > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="37891-107">Na lista **Todos os fornecedores**, localize e selecione o registo pretendido.</span><span class="sxs-lookup"><span data-stu-id="37891-107">In the **All vendors** list, find and select the desired record.</span></span>
3. <span data-ttu-id="37891-108">No Painel de Ação, selecione **Geral**.</span><span class="sxs-lookup"><span data-stu-id="37891-108">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="37891-109">Selecione **Entre empresas**.</span><span class="sxs-lookup"><span data-stu-id="37891-109">Select **Intercompany**.</span></span>
5. <span data-ttu-id="37891-110">Defina **Ativo** como **Sim** para ativar o comércio entre empresas.</span><span class="sxs-lookup"><span data-stu-id="37891-110">Set **Active** to **Yes** to enable intercompany trading.</span></span>
6. <span data-ttu-id="37891-111">No campo **Empresa cliente**, introduza ou selecione um valor.</span><span class="sxs-lookup"><span data-stu-id="37891-111">In the **Customer company** field, enter or select a value.</span></span>
7. <span data-ttu-id="37891-112">No campo **A minha conta**, introduza ou selecione um valor.</span><span class="sxs-lookup"><span data-stu-id="37891-112">In the **My account** field, enter or select a value.</span></span>
8. <span data-ttu-id="37891-113">Selecione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="37891-113">Select **Save**.</span></span>
9. <span data-ttu-id="37891-114">Feche as páginas para voltar à home page.</span><span class="sxs-lookup"><span data-stu-id="37891-114">Close the pages to return to the home page.</span></span>
10. <span data-ttu-id="37891-115">No painel de navegação, vá para **Módulos > Gestão de projetos e contabilística > Configurar > Parâmetros da gestão de projetos e contabilística**.</span><span class="sxs-lookup"><span data-stu-id="37891-115">In the navigation pane, go to **Modules > Project management and accounting > Setup > Project management and accounting parameters**.</span></span>
11. <span data-ttu-id="37891-116">Selecione o separador **Entre empresas**.</span><span class="sxs-lookup"><span data-stu-id="37891-116">Select the **Intercompany** tab.</span></span>
12. <span data-ttu-id="37891-117">Desloque o controlo de deslize para **Sim** para ativar as folhas de horas e o agendamento de recursos entre empresas.</span><span class="sxs-lookup"><span data-stu-id="37891-117">Move the slider to **Yes** to enable intercompany resource scheduling and timesheets.</span></span>
13. <span data-ttu-id="37891-118">Na lista, marque a linha selecionada.</span><span class="sxs-lookup"><span data-stu-id="37891-118">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="37891-119">Selecione **Novo**.</span><span class="sxs-lookup"><span data-stu-id="37891-119">Select **New**.</span></span>
15. <span data-ttu-id="37891-120">No campo **Entidade jurídica tomadora**, introduza ou selecione um valor.</span><span class="sxs-lookup"><span data-stu-id="37891-120">In the **Borrowing legal entity** field, enter or select a value.</span></span>
16. <span data-ttu-id="37891-121">Selecione a caixa de verificação **Acumular receitas**.</span><span class="sxs-lookup"><span data-stu-id="37891-121">Select the **Accrue revenue** check box.</span></span>
17. <span data-ttu-id="37891-122">No campo **Categoria de folha de horas predefinida**, introduza ou selecione um valor.</span><span class="sxs-lookup"><span data-stu-id="37891-122">In the **Default timesheet category** field, enter or select a value.</span></span>
18. <span data-ttu-id="37891-123">No campo **Categoria de despesa predefinida**, introduza ou selecione um valor.</span><span class="sxs-lookup"><span data-stu-id="37891-123">In the **Default expense category** field, enter or select a value.</span></span>
19. <span data-ttu-id="37891-124">Selecione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="37891-124">Select **Save**.</span></span>
20. <span data-ttu-id="37891-125">Feche a página.</span><span class="sxs-lookup"><span data-stu-id="37891-125">Close the page.</span></span>
21. <span data-ttu-id="37891-126">No painel de navegação, vá para **Módulos > Gestão de projetos e contabilística > Configurar > Publicação > Configuração do lançamento no livro razão**.</span><span class="sxs-lookup"><span data-stu-id="37891-126">In the navigation pane, go to **Modules > Project management and accounting > Setup > Posting > Ledger posting setup**.</span></span>
22. <span data-ttu-id="37891-127">No campo **Tipos de conta do livro razão**, selecione uma opção.</span><span class="sxs-lookup"><span data-stu-id="37891-127">In the **Ledger account types** field, select an option.</span></span>
23. <span data-ttu-id="37891-128">Selecione **Novo**.</span><span class="sxs-lookup"><span data-stu-id="37891-128">Select **New**.</span></span>
24. <span data-ttu-id="37891-129">No campo **Conta principal** da nova linha, especifique os valores desejados.</span><span class="sxs-lookup"><span data-stu-id="37891-129">In the **Main account** field of the new row, specify the desired values.</span></span>
25. <span data-ttu-id="37891-130">Selecione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="37891-130">Select **Save**.</span></span>
26. <span data-ttu-id="37891-131">Feche a página.</span><span class="sxs-lookup"><span data-stu-id="37891-131">Close the page.</span></span>
27. <span data-ttu-id="37891-132">No painel de navegação, vá para **Módulos > Gestão de projetos e contabilística > Configurar > Preços > Preço de transferência**.</span><span class="sxs-lookup"><span data-stu-id="37891-132">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Transfer price**.</span></span>
28. <span data-ttu-id="37891-133">Selecione **Novo**.</span><span class="sxs-lookup"><span data-stu-id="37891-133">Select **New**.</span></span>
29. <span data-ttu-id="37891-134">No campo **Data efetiva**, introduza uma data.</span><span class="sxs-lookup"><span data-stu-id="37891-134">In the **Effective date** field, enter a date.</span></span>
30. <span data-ttu-id="37891-135">No campo **Entidade jurídica tomadora**, introduza ou selecione um valor.</span><span class="sxs-lookup"><span data-stu-id="37891-135">In the **Borrowing legal entity** field, enter or select a value.</span></span>
31. <span data-ttu-id="37891-136">No campo **Modelo de preço de transferência**, selecione uma opção.</span><span class="sxs-lookup"><span data-stu-id="37891-136">In the **Transfer price model** field, select an option.</span></span>
32. <span data-ttu-id="37891-137">No campo **Preços**, introduza um número.</span><span class="sxs-lookup"><span data-stu-id="37891-137">In the **Pricing** field, enter a number.</span></span>
33. <span data-ttu-id="37891-138">Selecione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="37891-138">Select **Save**.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]