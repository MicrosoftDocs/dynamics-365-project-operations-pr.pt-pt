---
title: Novidades ou alterações na Versão da Atualização 32 do Project Service Automation, V3
description: Este tópico lista as funcionalidades e correções disponíveis no Project Service Automation V3, Versão da Atualização 32, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 11bf451ef4f24e2301ffde4f86a556a8a4fe30b0
ms.sourcegitcommit: 886102894244887d72e5a6213071e8d8a52c9d48
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/01/2021
ms.locfileid: "6129680"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a><span data-ttu-id="ed138-103">Novidades ou alterações na Versão da Atualização 32 do Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="ed138-103">What's new or changed in Project Service Automation Update Release 32, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="ed138-104">Temos o prazer de anunciar a atualização mais recente para a aplicação Microsoft Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="ed138-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="ed138-105">Esta versão inclui algumas melhorias importantes na qualidade, desempenho e utilização.</span><span class="sxs-lookup"><span data-stu-id="ed138-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="ed138-106">É compatível com o Dynamics 365, versão 9.x.</span><span class="sxs-lookup"><span data-stu-id="ed138-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="ed138-107">Para atualizar para esta versão, visite a página de soluções online do Centro de Administração do Dynamics 365 e instale a atualização.</span><span class="sxs-lookup"><span data-stu-id="ed138-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="ed138-108">Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="ed138-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="ed138-109">Este tópico lista as funcionalidades e correções novas ou alteradas para o Project Service Automation V3, Versão da Atualização 32.</span><span class="sxs-lookup"><span data-stu-id="ed138-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 32.</span></span> <span data-ttu-id="ed138-110">Esta versão tem um número de compilação V3.10.53.108 e está geralmente disponível através de uma atualização automática em junho de 2021.</span><span class="sxs-lookup"><span data-stu-id="ed138-110">This version has a build number of V3.10.53.108 and is generally available through a self-update in June 2021.</span></span>

## <a name="update-release-32"></a><span data-ttu-id="ed138-111">Versão da Atualização 32</span><span class="sxs-lookup"><span data-stu-id="ed138-111">Update Release 32</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="ed138-112">Correções de erros</span><span class="sxs-lookup"><span data-stu-id="ed138-112">Bug fixes</span></span>

#### <a name="general"></a><span data-ttu-id="ed138-113">Geral</span><span class="sxs-lookup"><span data-stu-id="ed138-113">General</span></span>

- <span data-ttu-id="ed138-114">Quando uma atualização principal falha, apenas os principais pontos de entrada da aplicação devem ser bloqueados, para garantir que as entidades partilhadas ainda estão acessíveis.</span><span class="sxs-lookup"><span data-stu-id="ed138-114">When a major upgrade fails, only the main application entry points should be blocked, to ensure that shared entities are still accessible.</span></span>

#### <a name="time-and-expense"></a><span data-ttu-id="ed138-115">Tempo e Despesa</span><span class="sxs-lookup"><span data-stu-id="ed138-115">Time and Expense</span></span>

<span data-ttu-id="ed138-116">Foram corrigidos os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="ed138-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="ed138-117">**TimeEntriesImportFromResourceAsignment** não mantém as horas de início e fim do setor de perfil de atribuição de recursos.</span><span class="sxs-lookup"><span data-stu-id="ed138-117">**TimeEntriesImportFromResourceAssignment** doesn't maintain the start and end times of the resource assignment contour slice.</span></span>
- <span data-ttu-id="ed138-118">Quando seleciona **Abrir Entrada** na grelha **Entrada de Hora**, poderá ser impedido de selecionar outras formas.</span><span class="sxs-lookup"><span data-stu-id="ed138-118">When you select **Open Entry** on the **Time Entry** grid, you might be prevented from selecting other forms.</span></span>
- <span data-ttu-id="ed138-119">Enquanto importa atribuições para entradas de tempo, a consulta de código do cliente pode gerar um URL longo que falha a consulta.</span><span class="sxs-lookup"><span data-stu-id="ed138-119">While you import assignments to time entries, the client code query could generate a long URL that fails the query.</span></span>
- <span data-ttu-id="ed138-120">Na grelha **Entrada de Hora**, depois de um valor ser eliminado de uma célula, o foco não permanece na grelha.</span><span class="sxs-lookup"><span data-stu-id="ed138-120">In the **Time Entry** grid, after a value is deleted from a cell, the focus doesn't remain in the grid.</span></span>
- <span data-ttu-id="ed138-121">O botão **Rejeitar** foi removido da vista **Processamento de aprovações** para aprovações modernas.</span><span class="sxs-lookup"><span data-stu-id="ed138-121">The **Reject** button has been removed from the **Processing approvals** view for modern approvals.</span></span>
- <span data-ttu-id="ed138-122">A estabilidade e o desempenho da aprovação em massa de entradas de tempo são afetados por impasses e por uma falha no processamento adequado de personalizações relacionadas com a entidade **Entrada de Tempo**.</span><span class="sxs-lookup"><span data-stu-id="ed138-122">The stability and performance of time entry bulk approval are affected by deadlocks and a failure to appropriately handle customizations that are related to the **Time Entry** entity.</span></span>

#### <a name="project-planning"></a><span data-ttu-id="ed138-123">Planeamento de Projeto</span><span class="sxs-lookup"><span data-stu-id="ed138-123">Project Planning</span></span>

- <span data-ttu-id="ed138-124">Uma exceção de referência nula é gerada quando atualiza um projeto que tem um valor nulo no campo **Unidade de Contratação**.</span><span class="sxs-lookup"><span data-stu-id="ed138-124">A null reference exception is generated when you update a project that has a null value in the **Contracting Unit** field.</span></span>
- <span data-ttu-id="ed138-125">**Atualiza Totais do Projeto** calcula incorretamente o custo restante e as vendas restantes num projeto.</span><span class="sxs-lookup"><span data-stu-id="ed138-125">**Refresh Project Totals** incorrectly calculates the remaining cost and remaining sales on a project.</span></span>
- <span data-ttu-id="ed138-126">Os cálculos de preços redundantes afetam o desempenho relacionado com atualizações nos perfis de atribuição de recursos.</span><span class="sxs-lookup"><span data-stu-id="ed138-126">Redundant pricing calculations affect performance that is related to updates on resource assignment contours.</span></span>

#### <a name="resource-management"></a><span data-ttu-id="ed138-127">Gestão de Recursos</span><span class="sxs-lookup"><span data-stu-id="ed138-127">Resource Management</span></span>

<span data-ttu-id="ed138-128">O seguinte problema foi corrigido:</span><span class="sxs-lookup"><span data-stu-id="ed138-128">The following issue has been fixed:</span></span>

- <span data-ttu-id="ed138-129">Quando a capacidade de calendário de um recurso reservável é superior a 1, o Project Service Automation reconhece incorretamente a capacidade como 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="ed138-129">When a bookable resource's calendar capacity is more than 1, Project Service Automation incorrectly recognizes the capacity as 0 (zero).</span></span> <span data-ttu-id="ed138-130">Portanto, ocorre um ciclo infinito na vista da agenda.</span><span class="sxs-lookup"><span data-stu-id="ed138-130">Therefore, an infinite loop occurs in the schedule view.</span></span>

#### <a name="sales"></a><span data-ttu-id="ed138-131">Vendas</span><span class="sxs-lookup"><span data-stu-id="ed138-131">Sales</span></span>

<span data-ttu-id="ed138-132">Foram corrigidos os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="ed138-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="ed138-133">Quando uma linha do diário é criada com um tipo de transação personalizada, ocorre a seguinte exceção de referência nula: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.</span><span class="sxs-lookup"><span data-stu-id="ed138-133">When a journal line is created that has a custom transaction type, the following null reference exception occurs: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.</span></span>
- <span data-ttu-id="ed138-134">As funções e categorias que estão inativas antes de uma proposta ser copiada não devem ser adicionadas a funções e categorias faturáveis da proposta recentemente copiada.</span><span class="sxs-lookup"><span data-stu-id="ed138-134">Roles and categories that are inactivated before a quotation is copied should not be added to chargeable roles and categories of the newly copied quotation.</span></span>
- <span data-ttu-id="ed138-135">A data do documento e a data da gestão contabilística não estão alinhadas com a data de início que é fornecida no detalhe da linha de uma fatura que é criado diretamente numa fatura de rascunho.</span><span class="sxs-lookup"><span data-stu-id="ed138-135">The document date and accounting date aren't aligned with the start date that is provided on an invoice line detail that is created directly on a draft invoice.</span></span>
- <span data-ttu-id="ed138-136">As exceções de referência nulas são geradas em cenários relacionados com a inativação de funções e categorias antes de uma proposta ser copiada.</span><span class="sxs-lookup"><span data-stu-id="ed138-136">Null reference exceptions are generated in scenarios that are related to inactivation of roles and categories before a quotation is copied.</span></span>
- <span data-ttu-id="ed138-137">A ação **Atualizar Preços** na página **Projetos** não atualiza as estimativas de despesas e estimativas de materiais.</span><span class="sxs-lookup"><span data-stu-id="ed138-137">The **Update Prices** action on the **Projects** page doesn't update expense estimates and material estimates.</span></span>
