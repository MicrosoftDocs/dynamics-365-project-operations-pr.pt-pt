---
title: Navegar na interface de utilizador
description: Este tópico fornece informações sobre a Gestão de projetos no Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: deedfe0c6601fd09e09460034c9a0db936b6566e
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127532"
---
# <a name="navigating-the-user-interface"></a><span data-ttu-id="68b13-103">Navegar na interface de utilizador</span><span class="sxs-lookup"><span data-stu-id="68b13-103">Navigating the user interface</span></span>

<span data-ttu-id="68b13-104">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="68b13-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="overview"></a><span data-ttu-id="68b13-105">Descrição geral</span><span class="sxs-lookup"><span data-stu-id="68b13-105">Overview</span></span>

<span data-ttu-id="68b13-106">O formulário do projeto principal é separado em vários separadores.</span><span class="sxs-lookup"><span data-stu-id="68b13-106">The main project form is separated into several tabs.</span></span> <span data-ttu-id="68b13-107">Cada separador representa um nível de detalhe diferente no projeto.</span><span class="sxs-lookup"><span data-stu-id="68b13-107">Each tab represents a different level of detail within the project.</span></span>

- <span data-ttu-id="68b13-108">**Resumo**: fornece uma descrição do projeto e agrega tanto o desempenho do projeto planeado e real.</span><span class="sxs-lookup"><span data-stu-id="68b13-108">**Summary**: Provides a description of the project and aggregates both the planned and actual project performance.</span></span>

    ![Separador e campos de Resumo](media/navigation7.png)

- <span data-ttu-id="68b13-110">**Tarefas**: fornece os detalhes relativos à estrutura hierárquica do trabalho representada por uma vista de grelha, vista de quadro e um gráfico gantt.</span><span class="sxs-lookup"><span data-stu-id="68b13-110">**Tasks**: Provides the details regarding the work breakdown structure represented by a grid view, board view, and a gantt.</span></span>

    ![Separador e campos de Tarefa](media/navigation8.png)

- <span data-ttu-id="68b13-112">**Equipa**: fornece detalhes sobre os participantes do projeto.</span><span class="sxs-lookup"><span data-stu-id="68b13-112">**Team**: Provides details regarding the project participants.</span></span> <span data-ttu-id="68b13-113">O esforço atribuído de cada membro da equipa também é resumido nesta vista.</span><span class="sxs-lookup"><span data-stu-id="68b13-113">The assigned effort of each team member is also summarized in this view.</span></span>

    ![Separador e campos de Equipa](media/navigation9.png)

- <span data-ttu-id="68b13-115">**Atribuições de recursos**: fornece uma vista faseada no tempo do esforço de cada recurso num projeto.</span><span class="sxs-lookup"><span data-stu-id="68b13-115">**Resource assignments**: Provides a time-phased view of the effort for each resource on a project.</span></span>

    ![Separador e campos de Atribuições de recursos](media/navigation10.png)

- <span data-ttu-id="68b13-117">**Reconciliação de recursos**: fornece uma vista faseada no tempo das diferenças entre as atribuições de cada recurso nomeado e as suas reservas.</span><span class="sxs-lookup"><span data-stu-id="68b13-117">**Resource reconciliation**: Provides a time-phased view of the differences between the assignments of each named resource and their bookings.</span></span>

    ![Separador e campos de Reconciliação de recursos](media/navigation11.png)

- <span data-ttu-id="68b13-119">**Estimativas**: fornece uma vista faseada no tempo das estimativas de vendas e de custo de um projeto.</span><span class="sxs-lookup"><span data-stu-id="68b13-119">**Estimates**: Provides a time-phased view of the cost and sales estimates of a project.</span></span>

    ![Separador e campos de Estimativas](media/navigation12.png)

- <span data-ttu-id="68b13-121">**Monitorização**: fornece uma vista que mostra o progresso das tarefas na estrutura hierárquica do trabalho em termos de esforço, custo e vendas.</span><span class="sxs-lookup"><span data-stu-id="68b13-121">**Tracking**: Provides a view that shows the progress of tasks in the work breakdown structure for effort, cost, and sales.</span></span>

    ![Separador e campos de Monitorização](media/navigation13.png)

- <span data-ttu-id="68b13-123">**Vendas**: fornece ligações avançadas às propostas e contratos associados ao projeto.</span><span class="sxs-lookup"><span data-stu-id="68b13-123">**Sales**: Provides deep links to quotes and contracts associated with the project.</span></span>

- <span data-ttu-id="68b13-124">**Estimativas de Despesas**: fornece uma grelha que define as despesas do projeto baseadas nas categorias de despesas organizacionais.</span><span class="sxs-lookup"><span data-stu-id="68b13-124">**Expense Estimates**: Provides a grid that defines project expenses based upon organizational expense categories.</span></span>

    ![Separador e campos de Estimativas de despesas](media/navigation14.png)

## <a name="grid-controls"></a><span data-ttu-id="68b13-126">Controlos da grelha</span><span class="sxs-lookup"><span data-stu-id="68b13-126">Grid controls</span></span>

<span data-ttu-id="68b13-127">Segue-se uma breve descrição geral dos controlos típicos encontrados nos vários separadores de planeamento de projetos.</span><span class="sxs-lookup"><span data-stu-id="68b13-127">The follow is a brief overview of the typical controls found on the various project planning tabs.</span></span>

### <a name="refresh"></a><span data-ttu-id="68b13-128">Actualizar</span><span class="sxs-lookup"><span data-stu-id="68b13-128">Refresh</span></span>

<span data-ttu-id="68b13-129">**Atualizar**: obtém os dados mais recentes do servidor se tiverem ocorrido alterações após o carregamento da grelha.</span><span class="sxs-lookup"><span data-stu-id="68b13-129">**Refresh**: Retrieves the latest data from the server if any changes occurred after the grid was loaded.</span></span>

![Botão Atualizar](media/navigation7.png)

### <a name="group-by"></a><span data-ttu-id="68b13-131">Agrupar por</span><span class="sxs-lookup"><span data-stu-id="68b13-131">Group by</span></span>

<span data-ttu-id="68b13-132">**Agrupar por**: atualiza o agrupamento das linhas na grelha para refletir os recursos, as funções ou as categorias com base nas necessidades do utilizador.</span><span class="sxs-lookup"><span data-stu-id="68b13-132">**Group by**: Updates the grouping of the rows in the grid to reflect either resources, roles, or categories based on the user's needs.</span></span>

![Botão Agrupar por](media/navigation6.png)

### <a name="previousnext"></a><span data-ttu-id="68b13-134">Anterior/Seguinte</span><span class="sxs-lookup"><span data-stu-id="68b13-134">Previous/Next</span></span>

<span data-ttu-id="68b13-135">**Anterior**/**Seguinte**: atualize os períodos visíveis nas grelhas faseadas no tempo.</span><span class="sxs-lookup"><span data-stu-id="68b13-135">**Previous**/**Next**: Update the visible time periods on the time-phased grids.</span></span>

![Botões Anterior e Seguinte](media/navigation2.png)

### <a name="timescale"></a><span data-ttu-id="68b13-137">Horário</span><span class="sxs-lookup"><span data-stu-id="68b13-137">Timescale</span></span>

<span data-ttu-id="68b13-138">**Horário**: alterar a agregação dos dados faseados no tempo entre dias, semanas, meses e anos.</span><span class="sxs-lookup"><span data-stu-id="68b13-138">**Timescale**: Change the aggregation of the time-phased data between days, weeks, months, and years.</span></span>

![Botão Horário](media/navigation3.png)

### <a name="expand"></a><span data-ttu-id="68b13-140">Expandir</span><span class="sxs-lookup"><span data-stu-id="68b13-140">Expand</span></span>

<span data-ttu-id="68b13-141">**Expandir**: tornar a grelha visível em ecrã inteiro para fornecer mais capacidade para ver funções adicionais.</span><span class="sxs-lookup"><span data-stu-id="68b13-141">**Expand**: Render the visible grid to full screen providing more ability to see additional roles.</span></span>

![botão Expandir](media/navigation4.png)

### <a name="time-phase-by"></a><span data-ttu-id="68b13-143">Faseamento no tempo por</span><span class="sxs-lookup"><span data-stu-id="68b13-143">Time-phase by</span></span>

<span data-ttu-id="68b13-144">**Faseamento no tempo por**: atualizar o agrupamento de linhas na grelha para refletir as estimativas de custos para as estimativas de vendas.</span><span class="sxs-lookup"><span data-stu-id="68b13-144">**Time-phase by**: Update the grouping of the rows in the grid to reflect cost estimates for sales estimates.</span></span> <span data-ttu-id="68b13-145">Este controlo também se aplica ao script de estimativa e à grelha de monitorização.</span><span class="sxs-lookup"><span data-stu-id="68b13-145">This control also applies to the estimate script and the tracking grid.</span></span>

![Botão Faseamento no tempo por](media/navigation0.png)

### <a name="add-column"></a><span data-ttu-id="68b13-147">Adicionar coluna</span><span class="sxs-lookup"><span data-stu-id="68b13-147">Add column</span></span>

<span data-ttu-id="68b13-148">**Adicionar coluna**: permite ao utilizador definir as colunas visíveis na grelha.</span><span class="sxs-lookup"><span data-stu-id="68b13-148">**Add column**: Allows the user to define the visible columns in the grid.</span></span> <span data-ttu-id="68b13-149">Só as colunas de configuração inicial podem ser adicionadas às grelhas no formulário **Planeamento de projeto**.</span><span class="sxs-lookup"><span data-stu-id="68b13-149">Only out-of-the-box columns can be added to the grids in the **Project Planning** form.</span></span>

![Botão Adicionar coluna](media/navigation5.png)
