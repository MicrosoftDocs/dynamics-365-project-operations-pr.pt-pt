---
title: Modelos de projeto
description: Este tópico fornece informações sobre como utilizar modelos de projeto para configuração rápida do projeto.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 1bb82a312114e9814f5ce65a1698455582fd252e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082566"
---
# <a name="project-templates"></a><span data-ttu-id="989bf-103">Modelos de projeto</span><span class="sxs-lookup"><span data-stu-id="989bf-103">Project templates</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="989bf-104">Um modelo de projeto é uma estrutura predefinida que o ajuda a iniciar um projeto de forma rápida e fácil.</span><span class="sxs-lookup"><span data-stu-id="989bf-104">A project template is a predefined framework that helps you quickly and easily start a project.</span></span> <span data-ttu-id="989bf-105">Pode utilizar um modelo predefinido para criar um novo projeto com um único clique.</span><span class="sxs-lookup"><span data-stu-id="989bf-105">You can use a predefined template to create a new project with a single click.</span></span> <span data-ttu-id="989bf-106">Quanto aos projetos, deve definir os pré-requisitos para os modelos de projeto.</span><span class="sxs-lookup"><span data-stu-id="989bf-106">As for projects, you must define the prerequisites for project templates.</span></span> <span data-ttu-id="989bf-107">Tem de definir um calendário de projeto para cada modelo de projeto, e as funções e listas de preços devem ser predefinidas na organização, para que os componentes do modelo tenham dados úteis.</span><span class="sxs-lookup"><span data-stu-id="989bf-107">You must define a project calendar for each project template, and roles and price lists must be predefined in the organization, so that the components of the template have useful data.</span></span>

<span data-ttu-id="989bf-108">Um modelo de projeto consiste em três componentes: uma agenda, estimativas do projeto e membros da equipa do projeto.</span><span class="sxs-lookup"><span data-stu-id="989bf-108">A project template consists of three components: a schedule, project estimates, and project team members.</span></span>

## <a name="schedule"></a><span data-ttu-id="989bf-109">Agendar</span><span class="sxs-lookup"><span data-stu-id="989bf-109">Schedule</span></span>

<span data-ttu-id="989bf-110">Uma agenda num modelo de projeto tem o mesmo conjunto de elementos como uma agenda num projeto.</span><span class="sxs-lookup"><span data-stu-id="989bf-110">A schedule in a project template has the same set of elements as a schedule in a project.</span></span> <span data-ttu-id="989bf-111">Pode criar uma hierarquia de tarefas, associar funções às tarefas, definir atributos da agenda e definir dependências.</span><span class="sxs-lookup"><span data-stu-id="989bf-111">You can create a task hierarchy, associate roles with tasks, define schedule attributes, and set dependencies.</span></span> <span data-ttu-id="989bf-112">Uma agenda num modelo de projeto também suporta modos de tarefas para cada tarefa.</span><span class="sxs-lookup"><span data-stu-id="989bf-112">A schedule in a project template also supports task modes for each task.</span></span> <span data-ttu-id="989bf-113">Consequentemente, suporta o motor de agendamento.</span><span class="sxs-lookup"><span data-stu-id="989bf-113">Therefore, it supports the scheduling engine.</span></span> <span data-ttu-id="989bf-114">Tem de associar um calendário do projeto ao projeto.</span><span class="sxs-lookup"><span data-stu-id="989bf-114">You must associate a project calendar with the project.</span></span> <span data-ttu-id="989bf-115">Quando cria uma agenda de trabalho, não há diferença entre um modelo de projeto e um projeto.</span><span class="sxs-lookup"><span data-stu-id="989bf-115">When you create a work schedule, there is no difference between a project template and a project.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="989bf-116">Estimativas do projeto</span><span class="sxs-lookup"><span data-stu-id="989bf-116">Project estimates</span></span>

<span data-ttu-id="989bf-117">As estimativas de projeto num modelo de projeto funcionam da mesma maneira que as estimativas de projeto num projeto.</span><span class="sxs-lookup"><span data-stu-id="989bf-117">Project estimates in a project template work the same way as project estimates in a project.</span></span> <span data-ttu-id="989bf-118">No entanto, os preços de custo e venda são extraídos das listas de preços de custo e venda predefinidas que são definidas nos parâmetros.</span><span class="sxs-lookup"><span data-stu-id="989bf-118">However, the cost and sales prices are pulled from the default cost and sales price lists that are defined in the parameters.</span></span>

## <a name="creating-a-project-from-a-template"></a><span data-ttu-id="989bf-119">Criar um projeto a partir de um modelo</span><span class="sxs-lookup"><span data-stu-id="989bf-119">Creating a project from a template</span></span>
 
<span data-ttu-id="989bf-120">Existem várias formas de criar um projeto a partir de um modelo de projeto:</span><span class="sxs-lookup"><span data-stu-id="989bf-120">There are several ways to create a project from a project template:</span></span>

- <span data-ttu-id="989bf-121">Ao criar um projeto a partir de uma proposta, pode selecionar um modelo de projeto na caixa de diálogo **Criação Rápida: Projeto**.</span><span class="sxs-lookup"><span data-stu-id="989bf-121">When you create a project from a quote, you can select a project template in the **Quick Create: Project** dialog box.</span></span>

> ![Caixa de diálogo Criação Rápida: Projeto](media/project-11.png)

- <span data-ttu-id="989bf-123">Quando cria um projeto selecionando **Novo Projeto** , a página **Projeto** aparece antes de o registo ser guardado.</span><span class="sxs-lookup"><span data-stu-id="989bf-123">When you create a project by selecting **New Project** , the **Project** page appears before the record is saved.</span></span> <span data-ttu-id="989bf-124">No campo **Selecionar um Modelo** , selecione um dos modelos de projeto predefinidos na organização.</span><span class="sxs-lookup"><span data-stu-id="989bf-124">In the **Pick a Template** field, select one of the predefined project templates in the organization.</span></span>
- <span data-ttu-id="989bf-125">Utilize **Criar Projeto a partir de um Modelo** na página **Entidade Modelo**.</span><span class="sxs-lookup"><span data-stu-id="989bf-125">Use **Create Project from a Template** on the **Template Entity** page.</span></span>

## <a name="copying-components-of-template-to-project"></a><span data-ttu-id="989bf-126">Copiar componentes de um modelo para um projeto</span><span class="sxs-lookup"><span data-stu-id="989bf-126">Copying components of template to project</span></span>

<span data-ttu-id="989bf-127">Quando copia os componentes de um modelo de projeto para um projeto, algumas substituições podem ocorrer, consoante as definições no projeto.</span><span class="sxs-lookup"><span data-stu-id="989bf-127">When you copy the components of a project template to a project, a few overrides can occur, depending on the settings in the project.</span></span>

### <a name="copying-the-schedule"></a><span data-ttu-id="989bf-128">Copiar a agenda</span><span class="sxs-lookup"><span data-stu-id="989bf-128">Copying the schedule</span></span>

<span data-ttu-id="989bf-129">Quando copia a agenda a partir de um modelo de projeto, se o projeto tiver um calendário do projeto diferente do modelo, as horas de trabalho do calendário do projeto serão aplicadas à agenda da tarefa.</span><span class="sxs-lookup"><span data-stu-id="989bf-129">When you copy the schedule from a project template, if the project has a different project calendar than the template, work hours from the project's calendar are applied to the task schedule.</span></span> <span data-ttu-id="989bf-130">Desta forma, a agenda é ajustada para corresponder ao calendário do projeto subjacente.</span><span class="sxs-lookup"><span data-stu-id="989bf-130">In this way, the schedule is adjusted to match the backing project calendar.</span></span> <span data-ttu-id="989bf-131">Da mesma forma, a primeira tarefa na agenda assume a data de início do projeto e a agenda do resto da hierarquia é atualizada com base na duração e nas dependências especificadas no modelo.</span><span class="sxs-lookup"><span data-stu-id="989bf-131">Similarly, the first task on the schedule takes the project's start date, and the schedule of the rest of the hierarchy is updated based on the duration and dependencies that are specified in the template.</span></span> 

### <a name="copying-project-estimates"></a><span data-ttu-id="989bf-132">Copiar estimativas do projeto</span><span class="sxs-lookup"><span data-stu-id="989bf-132">Copying project estimates</span></span> 

<span data-ttu-id="989bf-133">Quando copia em linhas de estimativa do projeto, as listas de preços são atualizadas.</span><span class="sxs-lookup"><span data-stu-id="989bf-133">When you copy across project estimate lines, the price lists are updated.</span></span> <span data-ttu-id="989bf-134">Para a lista de preços de custo, estas atualizações baseiam-se na unidade proprietária do projeto.</span><span class="sxs-lookup"><span data-stu-id="989bf-134">For the cost price list, these updates are based on the owning unit of the project.</span></span> <span data-ttu-id="989bf-135">Para a lista de preços de venda, baseiam-se no cliente.</span><span class="sxs-lookup"><span data-stu-id="989bf-135">For the sales price list, they are based on the customer.</span></span> <span data-ttu-id="989bf-136">Para projetos associados a uma entidade de vendas, o custo unitário e os preços de venda são determinados com base nestas listas de preços.</span><span class="sxs-lookup"><span data-stu-id="989bf-136">For projects that are associated with a sales entity, the unit cost and sales prices are determined based on these price lists.</span></span>

### <a name="copying-a-project-team"></a><span data-ttu-id="989bf-137">Copiar uma equipa do projeto</span><span class="sxs-lookup"><span data-stu-id="989bf-137">Copying a project team</span></span>

<span data-ttu-id="989bf-138">Quando uma equipa do projeto é copiada de um modelo de projeto para um projeto, os recursos genéricos são copiados, juntamente com as competências e proficiências definidas no modelo.</span><span class="sxs-lookup"><span data-stu-id="989bf-138">When a project team is copied from a project template to a project, the generic resources are copied, together with the skills and proficiencies that are defined in the template.</span></span> <span data-ttu-id="989bf-139">As atribuições de recursos genéricos também são mantidas como no modelo do projeto.</span><span class="sxs-lookup"><span data-stu-id="989bf-139">Generic resource assignments are also maintained as they were in the project template.</span></span> <span data-ttu-id="989bf-140">Os recursos nomeados não são suportados em modelos de projeto.</span><span class="sxs-lookup"><span data-stu-id="989bf-140">Named resources aren't supported in project templates.</span></span>
