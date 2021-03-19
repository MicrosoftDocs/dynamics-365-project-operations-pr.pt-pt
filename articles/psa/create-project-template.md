---
title: Criar um modelo de projeto
description: Como criar um modelo do projeto no Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: e8a9b75aa0721c6e7c85c2bca8796bf9f2c6d3db
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285137"
---
# <a name="create-a-project-template-project-service"></a><span data-ttu-id="ca07b-103">Criar um modelo de projeto (Project Service)</span><span class="sxs-lookup"><span data-stu-id="ca07b-103">Create a project template (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="ca07b-104">Os modelos de projeto poupam tempo se a sua empresa apresenta propostas em tipos semelhantes de projetos.</span><span class="sxs-lookup"><span data-stu-id="ca07b-104">Project templates save you time if your company regularly bids on similar types of projects.</span></span> <span data-ttu-id="ca07b-105">Fornecem um conjunto de funções padrão e as horas estimadas para um tipo de projeto.</span><span class="sxs-lookup"><span data-stu-id="ca07b-105">They provide a standard set of roles and estimated hours for a type of project.</span></span> <span data-ttu-id="ca07b-106">Os gestores de contas e os gestores de projetos podem criar projetos com num modelo de design ou copiar o modelo e assumir um.</span><span class="sxs-lookup"><span data-stu-id="ca07b-106">Account managers and project managers can create projects based on a project template, or they can copy the template and make one of their own.</span></span>  
  
## <a name="components-of-project-template"></a><span data-ttu-id="ca07b-107">Componentes do modelo de projeto</span><span class="sxs-lookup"><span data-stu-id="ca07b-107">Components of project template</span></span>
 <span data-ttu-id="ca07b-108">Um modelo de projeto é composto por três componentes:</span><span class="sxs-lookup"><span data-stu-id="ca07b-108">A project template consists of three components:</span></span>  
  
- <span data-ttu-id="ca07b-109">**Estrutura hierárquica do trabalho**: Uma estrutura hierárquica do trabalho num modelo de projeto tem o mesmo conjunto de elementos que no projeto.</span><span class="sxs-lookup"><span data-stu-id="ca07b-109">**Work breakdown structure**: A work breakdown structure in a project template has the same set of elements as in the project.</span></span> <span data-ttu-id="ca07b-110">Pode criar uma hierarquia de tarefas, associar funções à tarefa, definir atributos da agenda, definir dependências e ver todos os dados no gráfico Gantt.</span><span class="sxs-lookup"><span data-stu-id="ca07b-110">You can create a task hierarchy, associate roles to task, define schedule attributes, set dependencies and view all the data in the Gantt.</span></span> <span data-ttu-id="ca07b-111">A estrutura hierárquica do trabalho nos modelos de projeto também suportam modos de tarefa para cada tarefa.</span><span class="sxs-lookup"><span data-stu-id="ca07b-111">The work breakdown structure in project templates also support task modes for each task.</span></span> <span data-ttu-id="ca07b-112">Não existem diferença entre um modelo de projeto e um projeto ao criar a agenda de trabalho.</span><span class="sxs-lookup"><span data-stu-id="ca07b-112">There is no difference between a project template and a project when creating work schedule.</span></span>  
  
- <span data-ttu-id="ca07b-113">**Estimativas do projeto**: As estimativas do projeto em funcionam da mesma forma que nos projetos, à exceção das listas de preços, que para assumir por predefinição o custo e os preços de vendas, são sempre as listas de preços de venda e o custo definidos nos parâmetros do [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="ca07b-113">**Project estimates**: Project estimates in templates work the same way as they do in projects, except the price lists for defaulting the cost and sales prices are always the default cost and sales price lists defined in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] parameters.</span></span> <span data-ttu-id="ca07b-114">A restante funcionalidade é igual à de um projeto.</span><span class="sxs-lookup"><span data-stu-id="ca07b-114">The rest of the functionality is the same as in a project.</span></span>  
  
- <span data-ttu-id="ca07b-115">**Formação da equipa do projeto**: Ao formar uma equipa do projeto para um modelo de projeto, não é possível reservar um recurso nomeado num modelo.</span><span class="sxs-lookup"><span data-stu-id="ca07b-115">**Project team formation**: When forming a project team for a project template, you can’t book a named resource in a template.</span></span> <span data-ttu-id="ca07b-116">Pode utilizar **Gerar Equipa do Projeto** estrutura hierárquica do trabalho para gerar um conjunto de recursos genéricos.</span><span class="sxs-lookup"><span data-stu-id="ca07b-116">You can use **Generate Project Team** in the work breakdown structure to generate a set of generic resources.</span></span> <span data-ttu-id="ca07b-117">Também pode especificar as competências e as proficiências necessárias para os recursos genéricos.</span><span class="sxs-lookup"><span data-stu-id="ca07b-117">You can also specify required skills and proficiencies for generic resources.</span></span> <span data-ttu-id="ca07b-118">Não pode substituir um recurso genérico por um recurso reservável nos modelos do projeto.</span><span class="sxs-lookup"><span data-stu-id="ca07b-118">You can’t substitute a generic resource with a bookable resource in project templates.</span></span>  
  
## <a name="create-a-project-from-a-template"></a><span data-ttu-id="ca07b-119">Criar um projeto a partir de um modelo</span><span class="sxs-lookup"><span data-stu-id="ca07b-119">Create a project from a template</span></span>  
 <span data-ttu-id="ca07b-120">Pode criar um projeto a partir de um modelo das seguintes formas:</span><span class="sxs-lookup"><span data-stu-id="ca07b-120">You can create a project from a template in these following ways:</span></span>  
  
-   <span data-ttu-id="ca07b-121">Ao criar um projeto a partir da cotação, pode escolher um modelo de projeto no formulário de criação rápida de projeto.</span><span class="sxs-lookup"><span data-stu-id="ca07b-121">When creating a project from the quote, you can choose a project template in the project quick create form.</span></span>  
  
-   <span data-ttu-id="ca07b-122">Ao criar um projeto clicando em **Novo Projeto**, o formulário do projeto é apresentado antes de guardar o registo.</span><span class="sxs-lookup"><span data-stu-id="ca07b-122">When creating a project by clicking **New Project**, the project form displays before you save the record.</span></span> <span data-ttu-id="ca07b-123">A partir daqui, poderá clicar no campo **Selecionar um modelo** para escolher na lista de modelos de projeto predefinidos na sua organização.</span><span class="sxs-lookup"><span data-stu-id="ca07b-123">From here, you can click **Pick a template** field to choose from the list of pre-defined project templates in your organization.</span></span>  
  
-   <span data-ttu-id="ca07b-124">Clique em **Criar projeto a partir de um modelo** na página **Modelo de Projeto** para criar um projeto a partir do modelo.</span><span class="sxs-lookup"><span data-stu-id="ca07b-124">Click **Create project from a template** on the **Project Template** page to create a project from the template.</span></span>  
  
## <a name="copying-components-of-a-template-to-a-project"></a><span data-ttu-id="ca07b-125">Copiar componentes de um modelo para um projeto</span><span class="sxs-lookup"><span data-stu-id="ca07b-125">Copying components of a template to a project</span></span>  
 <span data-ttu-id="ca07b-126">Quando copia os componentes de um modelo para um projeto, há alguns aspetos que deve conhecer.</span><span class="sxs-lookup"><span data-stu-id="ca07b-126">When you copy components of a template into a project, there are a few things you should know about.</span></span>  
  
 <span data-ttu-id="ca07b-127">**Copiar uma estrutura hierárquica do trabalho**: Quando copia a estrutura hierárquica do trabalho a partir de um modelo de projeto, se o projeto tiver um calendário do projeto diferente do modelo, as horas de trabalho do calendário do projeto serão aplicadas à agenda das tarefas.</span><span class="sxs-lookup"><span data-stu-id="ca07b-127">**Copying a work breakdown structure**: When you copy the work breakdown structure from a project template, if the project has a different project calendar than the template, the work hours from the project’s calendar will be applied to the schedule of tasks.</span></span> <span data-ttu-id="ca07b-128">Isto ajusta a agenda ao calendário do projeto de reserva.</span><span class="sxs-lookup"><span data-stu-id="ca07b-128">This adjusts the schedule to the backing project calendar.</span></span> <span data-ttu-id="ca07b-129">Da mesma forma, a primeira tarefa na estrutura hierárquica do trabalho assume a data de início do projeto, pelo que a restante agenda da hierarquia de tarefas é atualizada com base na duração e nas dependências especificadas na estrutura hierárquica do trabalho</span><span class="sxs-lookup"><span data-stu-id="ca07b-129">Similarly, the first task on the work breakdown structure takes the project’s start date, so the rest of the task hierarchy schedule is updated based on the duration and dependencies specified in the template’s work breakdown structure.</span></span>  
  
 <span data-ttu-id="ca07b-130">**Copiar estimativas do projeto**: Quando copia entre linhas de estimativa do projeto, as listas de preços são atualizadas com base na unidade proprietária do projeto para a lista de preços de custo e o cliente para a lista de preços de venda.</span><span class="sxs-lookup"><span data-stu-id="ca07b-130">**Copying project estimates**: When you copy across project estimate lines, price lists are updated based on the owning unit of the project for the cost price list and customer for the sales price list.</span></span> <span data-ttu-id="ca07b-131">O custo unitário e os preços de venda são determinadas com base nestas listas de preços nos projetos associados a uma entidade de vendas.</span><span class="sxs-lookup"><span data-stu-id="ca07b-131">The unit cost and sales prices are determined from these price lists on projects that are associated to a sales entity.</span></span>  
  
 <span data-ttu-id="ca07b-132">**Copiar uma equipa do projeto**: Quando copia a equipa do projeto do modelo para um projeto, os recursos genéricos são copiados com as competências e as proficiências definidas no modelo.</span><span class="sxs-lookup"><span data-stu-id="ca07b-132">**Copying a project team**: When you copy the project team from the template to a project, the generic resources are copied across, along with the skills and proficiencies defined in the template.</span></span> <span data-ttu-id="ca07b-133">As atribuições de recursos genéricos também são mantidas como no modelo do projeto.</span><span class="sxs-lookup"><span data-stu-id="ca07b-133">Generic resource assignments are also maintained as in the project template.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="ca07b-134">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="ca07b-134">See Also</span></span>  
 [<span data-ttu-id="ca07b-135">Guia do Gestor de Projeto</span><span class="sxs-lookup"><span data-stu-id="ca07b-135">Project Manager Guide</span></span>](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]