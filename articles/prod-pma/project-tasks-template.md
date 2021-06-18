---
title: Sincronizar tarefas do projetos diretamente do Project Service Automation para o Finance and Operations
description: Este tópico descreve o modelo e a tarefa subjacente que são utilizados para sincronizar as tarefas do projeto diretamente do Microsoft Dynamics 365 Project Service Automation para o Dynamics 365 Finance.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 16cd38f2f190414d7be9c93e8ab90d55006f47e1
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009990"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="a5c7f-103">Sincronizar tarefas do projetos diretamente do Project Service Automation para o Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a5c7f-103">Synchronize project tasks directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a5c7f-104">Este tópico descreve o modelo e a tarefa subjacente que são utilizados para sincronizar as tarefas do projeto diretamente do Dynamics 365 Project Service Automation para o Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="a5c7f-104">This topic describes the template and underlying task that are used to synchronize project tasks directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="a5c7f-105">A integração de tarefas do projeto, as categorias de transações de despesas, as estimativas de horas, as estimativas de despesas e o bloqueio de funcionalidades estão disponíveis na versão 8.0.</span><span class="sxs-lookup"><span data-stu-id="a5c7f-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="a5c7f-106">Se estiver a utilizar a Enterprise edition 7.3.0 depois de instalar o KB 4132657 e o KB 4132660, poderá utilizar os modelos para integrar tarefas de projeto, categorias de transações de despesas, estimativas de horas, estimativas de despesas e valores reais, e para configurar o bloqueio de funcionalidades.</span><span class="sxs-lookup"><span data-stu-id="a5c7f-106">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="a5c7f-107">Se tiver de repor as distribuições contabilísticas, recomendamos que também instale o KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="a5c7f-107">If you must reset the accounting distributions, we recommended that you also install KB 4131710.</span></span>
> - <span data-ttu-id="a5c7f-108">A integração dos valores reais está disponível na versão 8.0.1 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="a5c7f-108">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="a5c7f-109">Fluxo de dados para o Project Service Automation para o Finance</span><span class="sxs-lookup"><span data-stu-id="a5c7f-109">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="a5c7f-110">A solução de integração do Project Service Automation para Finance utiliza a funcionalidade Integração de Dados para sincronizar os dados entre instâncias do Project Service Automation e do Finance.</span><span class="sxs-lookup"><span data-stu-id="a5c7f-110">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="a5c7f-111">O modelo de integração que está disponível com a funcionalidade Integração de dados permite o fluxo de dados sobre as tarefas do projeto entre o Project Service Automation e o Finance.</span><span class="sxs-lookup"><span data-stu-id="a5c7f-111">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance.</span></span>

<span data-ttu-id="a5c7f-112">A seguinte ilustração mostra como os dados são sincronizados entre o Project Service Automation e o Finance.</span><span class="sxs-lookup"><span data-stu-id="a5c7f-112">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="a5c7f-113">[![Fluxo de dados para a integração do Project Service Automation com o Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="a5c7f-113">[![Data flow for Project Service Automation integration with Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="a5c7f-114">Modelo e tarefa</span><span class="sxs-lookup"><span data-stu-id="a5c7f-114">Template and task</span></span>

<span data-ttu-id="a5c7f-115">Para aceder ao modelo, no centro de administração do Microsoft Power Apps, selecione **Projetos** e, em seguida, no canto superior direito, selecione **Novo projeto** para selecionar modelos públicos.</span><span class="sxs-lookup"><span data-stu-id="a5c7f-115">To access the template, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="a5c7f-116">O modelo seguinte e a tarefa subjacente são utilizados para sincronizar as tarefas do projeto do Project Service Automation para o Finance:</span><span class="sxs-lookup"><span data-stu-id="a5c7f-116">The following template and underlying task are used to synchronize project tasks from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="a5c7f-117">**Nome do modelo na Integração de dados:** tarefas do projeto (PSA para Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="a5c7f-117">**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="a5c7f-118">**Nome da tarefa no projeto:** Tarefas do projeto</span><span class="sxs-lookup"><span data-stu-id="a5c7f-118">**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="a5c7f-119">Antes de poder ocorrer a sincronização das tarefas do projeto, é necessário sincronizar os contratos de projeto e os projetos.</span><span class="sxs-lookup"><span data-stu-id="a5c7f-119">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="a5c7f-120">Conjunto de entidades</span><span class="sxs-lookup"><span data-stu-id="a5c7f-120">Entity set</span></span>

| <span data-ttu-id="a5c7f-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="a5c7f-121">Project Service Automation</span></span> | <span data-ttu-id="a5c7f-122">Finanças</span><span class="sxs-lookup"><span data-stu-id="a5c7f-122">Finance</span></span>                             |
|----------------------------|-------------------------------------|
| <span data-ttu-id="a5c7f-123">Tarefas do Projeto</span><span class="sxs-lookup"><span data-stu-id="a5c7f-123">Project Tasks</span></span>              | <span data-ttu-id="a5c7f-124">Entidade de integração para a tarefa de projeto</span><span class="sxs-lookup"><span data-stu-id="a5c7f-124">Integration entity for project task</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="a5c7f-125">Fluxo de entidades</span><span class="sxs-lookup"><span data-stu-id="a5c7f-125">Entity flow</span></span>

<span data-ttu-id="a5c7f-126">As tarefas do projeto são geridas no Project Service Automation e sincronizadas com o Finance como atividades de projeto.</span><span class="sxs-lookup"><span data-stu-id="a5c7f-126">Project tasks are managed in Project Service Automation, and they are synchronized to Finance as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="a5c7f-127">Pré-requisitos e configuração do mapeamento</span><span class="sxs-lookup"><span data-stu-id="a5c7f-127">Prerequisites and mapping setup</span></span>

<span data-ttu-id="a5c7f-128">Antes de poder ocorrer a sincronização das tarefas do projeto, é necessário sincronizar os contratos de projeto e os projetos.</span><span class="sxs-lookup"><span data-stu-id="a5c7f-128">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="a5c7f-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="a5c7f-129">Power Query</span></span>

<span data-ttu-id="a5c7f-130">Tem de utilizar o Microsoft Power Query para Excel para filtrar os dados se esta condição se verificar:</span><span class="sxs-lookup"><span data-stu-id="a5c7f-130">You must use Microsoft Power Query for Excel to filter data if this condition is met:</span></span>

- <span data-ttu-id="a5c7f-131">Tem registos específicos de recursos numa tarefa de projeto.</span><span class="sxs-lookup"><span data-stu-id="a5c7f-131">You have resource-specific records in a project task.</span></span>

<span data-ttu-id="a5c7f-132">Se tiver de utilizar o Power Query, siga esta diretriz:</span><span class="sxs-lookup"><span data-stu-id="a5c7f-132">If you must use Power Query, follow this guideline:</span></span>

- <span data-ttu-id="a5c7f-133">O modelo Tarefas de projeto (PSA para Fin and Ops) tem um filtro predefinido que exclui os registos específicos do recurso de uma tarefa do projeto ao definir o filtro em **IsLineTask** como **False**.</span><span class="sxs-lookup"><span data-stu-id="a5c7f-133">The Project tasks (PSA to Fin and Ops) template has a default filter that excludes resource-specific records from a project task by setting the filter on **IsLineTask** to **False**.</span></span> <span data-ttu-id="a5c7f-134">Se criar o seu próprio modelo, terá de adicionar este filtro.</span><span class="sxs-lookup"><span data-stu-id="a5c7f-134">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="a5c7f-135">Mapeamento de modelos na Integração de dados</span><span class="sxs-lookup"><span data-stu-id="a5c7f-135">Template mapping in Data integration</span></span>

<span data-ttu-id="a5c7f-136">A seguinte ilustração mostra um exemplo dos mapeamentos de tarefas do modelo na Integração de Dados.</span><span class="sxs-lookup"><span data-stu-id="a5c7f-136">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="a5c7f-137">O mapeamento mostra as informações do campo que serão sincronizadas do Project Service Automation para Finance.</span><span class="sxs-lookup"><span data-stu-id="a5c7f-137">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="a5c7f-138">[![Mapeamento de modelos](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="a5c7f-138">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]