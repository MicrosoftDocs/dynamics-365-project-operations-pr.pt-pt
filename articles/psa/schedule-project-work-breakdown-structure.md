---
title: Agendar um projeto com uma estrutura hierárquica do trabalho
description: Como agendar um projeto com uma estrutura hierárquica do trabalho no Project Service
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
ms.openlocfilehash: 04f30f2f2ed93dd1525f1c86a7521cdbf39a77bc
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127892"
---
# <a name="schedule-a-project-with-a-work-breakdown-structure-project-service"></a><span data-ttu-id="21d72-103">Agendar um projeto com uma estrutura hierárquica do trabalho (Project Service)</span><span class="sxs-lookup"><span data-stu-id="21d72-103">Schedule a project with a work breakdown structure (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="21d72-104">Um agenda do projeto comunica que tem de ser efetuado, que recursos irão efetuar o trabalho e o intervalo de tempo durante o qual o trabalho tem de ser concluído.</span><span class="sxs-lookup"><span data-stu-id="21d72-104">A project schedule communicates what work needs to be performed, which resources will perform the work, and the timeframe in which that work needs to be completed.</span></span> <span data-ttu-id="21d72-105">A agenda do projeto reflete todo o trabalho associado à entrega do projeto a tempo.</span><span class="sxs-lookup"><span data-stu-id="21d72-105">The project schedule reflects all the work associated with delivering the project on time.</span></span> <span data-ttu-id="21d72-106">Um dos primeiros passos na fase de inicialização do projeto é definir uma agenda do projeto.</span><span class="sxs-lookup"><span data-stu-id="21d72-106">One of the first steps in the initiation phase of the project is to come up with a project schedule.</span></span> <span data-ttu-id="21d72-107">Para estabelecer uma agenda do projeto, tem de criar uma estrutura hierárquica do trabalho.</span><span class="sxs-lookup"><span data-stu-id="21d72-107">To establish a project schedule, you need to create a work breakdown structure.</span></span>  
  
 <span data-ttu-id="21d72-108">Crie uma estrutura do projeto com estrutura hierárquica do trabalho, o que ajuda a:</span><span class="sxs-lookup"><span data-stu-id="21d72-108">Create a project structure with a work breakdown structure, which helps you:</span></span>  
  
- <span data-ttu-id="21d72-109">Dividir o trabalho em tarefas geríveis</span><span class="sxs-lookup"><span data-stu-id="21d72-109">Break down work into manageable tasks</span></span>  
  
- <span data-ttu-id="21d72-110">Estimar o tempo necessário para concluir uma tarefa</span><span class="sxs-lookup"><span data-stu-id="21d72-110">Estimate the time required to complete a task</span></span>  
  
- <span data-ttu-id="21d72-111">Definir as dependências e a duração da tarefa</span><span class="sxs-lookup"><span data-stu-id="21d72-111">Set task dependencies and task duration</span></span>  
  
- <span data-ttu-id="21d72-112">Determinar as funções necessárias para concluir cada tarefa</span><span class="sxs-lookup"><span data-stu-id="21d72-112">Determine the roles required to complete each task</span></span>  
  
  <span data-ttu-id="21d72-113">A agenda do projeto na estrutura hierárquica do trabalho tem um aspeto e funcionalidade familiares, incluindo um gráfico Gantt interativo.</span><span class="sxs-lookup"><span data-stu-id="21d72-113">The project schedule in the work breakdown structure has a familiar look and feel, complete with an interactive Gantt chart.</span></span>  
  
## <a name="create-a-work-breakdown-structure-for-a-project"></a><span data-ttu-id="21d72-114">Criar uma estrutura hierárquica do trabalho para um projeto</span><span class="sxs-lookup"><span data-stu-id="21d72-114">Create a work breakdown structure for a project</span></span>  
 <span data-ttu-id="21d72-115">Crie uma estrutura hierárquica do trabalho para representar a sequência de tarefas num projeto.</span><span class="sxs-lookup"><span data-stu-id="21d72-115">Create a work breakdown structure to represent the sequence of tasks in a project.</span></span> <span data-ttu-id="21d72-116">A estrutura hierárquica do trabalho inclui tarefas, requisitos para cada tarefa, bem como as informações do custo e das receitas.</span><span class="sxs-lookup"><span data-stu-id="21d72-116">The work breakdown structure includes tasks, requirements for each task, and revenue and cost information.</span></span> <span data-ttu-id="21d72-117">Na estrutura hierárquica do trabalho, poderá adicionar:</span><span class="sxs-lookup"><span data-stu-id="21d72-117">In your work breakdown structure, you can add:</span></span>  
  
-   <span data-ttu-id="21d72-118">A sequência de tarefas numa hierarquia</span><span class="sxs-lookup"><span data-stu-id="21d72-118">The sequence of tasks in a hierarchy</span></span>  
  
-   <span data-ttu-id="21d72-119">Outras tarefas, se existirem, que tenham de ser concluídas antes de uma tarefa poder ser iniciada</span><span class="sxs-lookup"><span data-stu-id="21d72-119">Other tasks, if any, that must be completed before a task can be started</span></span>  
  
-   <span data-ttu-id="21d72-120">A data de início, a data de fim e a duração de uma tarefa</span><span class="sxs-lookup"><span data-stu-id="21d72-120">The starting date, ending date, and duration of a task</span></span>  
  
-   <span data-ttu-id="21d72-121">O número de horas necessárias para uma tarefa</span><span class="sxs-lookup"><span data-stu-id="21d72-121">The number of hours required for a task</span></span>  
  
-   <span data-ttu-id="21d72-122">Quaisquer competências e educação dos trabalhadores necessárias</span><span class="sxs-lookup"><span data-stu-id="21d72-122">Any required worker skills and education</span></span>  
  
-   <span data-ttu-id="21d72-123">Os trabalhadores atribuídos a uma tarefa</span><span class="sxs-lookup"><span data-stu-id="21d72-123">The workers who are assigned to a task</span></span>  
  
-   <span data-ttu-id="21d72-124">Receitas e custos estimados</span><span class="sxs-lookup"><span data-stu-id="21d72-124">Estimated revenue and costs</span></span>  
  
## <a name="task-types"></a><span data-ttu-id="21d72-125">Tipos de tarefa</span><span class="sxs-lookup"><span data-stu-id="21d72-125">Task types</span></span>  
<span data-ttu-id="21d72-126">Utilize os seguintes tipos de tarefa quando criar a sua estrutura hierárquica do trabalho:</span><span class="sxs-lookup"><span data-stu-id="21d72-126">You’ll use the following types of tasks when creating your work breakdown structure:</span></span>  

| | | 
|---------------------------------------|-----------------------------------------------------------------| 
| <span data-ttu-id="21d72-127">**Nó de raiz do projeto**</span><span class="sxs-lookup"><span data-stu-id="21d72-127">**Project root node**</span></span> | <span data-ttu-id="21d72-128">A tarefa de resumo de nível superior do projeto.</span><span class="sxs-lookup"><span data-stu-id="21d72-128">The top-level summary task for the project.</span></span> <span data-ttu-id="21d72-129">Todas as outras tarefas do projeto são aí criadas.</span><span class="sxs-lookup"><span data-stu-id="21d72-129">All other project tasks are created under it.</span></span> <span data-ttu-id="21d72-130">O nome da tarefa de raiz é o nome do projeto.</span><span class="sxs-lookup"><span data-stu-id="21d72-130">The name of the root task is the project name.</span></span> <span data-ttu-id="21d72-131">O esforço, as datas e a duração do nó de raiz baseiam-se nos valores da hierarquia abaixo dele.</span><span class="sxs-lookup"><span data-stu-id="21d72-131">The effort, dates, and duration of the root node are based on the values on the hierarchy below it.</span></span> <span data-ttu-id="21d72-132">Não pode editar as propriedades do nó de raiz nem eliminar o nó de raiz.</span><span class="sxs-lookup"><span data-stu-id="21d72-132">You can’t edit root node properties or delete the root node.</span></span> | 
| <span data-ttu-id="21d72-133">**Tarefas de resumo ou contentor**</span><span class="sxs-lookup"><span data-stu-id="21d72-133">**Summary or container tasks**</span></span> | <span data-ttu-id="21d72-134">Uma tarefa de resumo é uma tarefa com subpastas.</span><span class="sxs-lookup"><span data-stu-id="21d72-134">A summary task is a task that has sub-tasks under it.</span></span> <span data-ttu-id="21d72-135">Uma tarefa de resumo não tem qualquer esforço de trabalho ou custo próprio.</span><span class="sxs-lookup"><span data-stu-id="21d72-135">A summary task doesn’t have any work effort or cost of its own.</span></span> <span data-ttu-id="21d72-136">O esforço e o custo do trabalho são um rollup das respetivas subtarefas.</span><span class="sxs-lookup"><span data-stu-id="21d72-136">Its work effort and cost are a rollup of its sub-tasks.</span></span> <span data-ttu-id="21d72-137">Pode alterar o nome de uma tarefa de resumo, mas não poderá alterar o esforço, as datas ou a duração, porque estes são calculados automaticamente.</span><span class="sxs-lookup"><span data-stu-id="21d72-137">You can change the name of a summary task, but you can’t change the effort, dates, or duration, because those are automatically calculated.</span></span> <span data-ttu-id="21d72-138">Ao eliminar uma tarefa de resumo elimina a tarefa e todas as suas subtarefas.</span><span class="sxs-lookup"><span data-stu-id="21d72-138">Deleting a summary task deletes the task and all of its sub-tasks.</span></span>|  
| <span data-ttu-id="21d72-139">**Tarefas de nós de folha**</span><span class="sxs-lookup"><span data-stu-id="21d72-139">**Leaf node tasks**</span></span> | <span data-ttu-id="21d72-140">Uma tarefa de nós de folha representa o trabalho mais detalhado no projeto.</span><span class="sxs-lookup"><span data-stu-id="21d72-140">A leaf node task represents the most detailed work on the project.</span></span> <span data-ttu-id="21d72-141">Tem um esforço calculado, um número planeado de recursos, datas de início e de fim planeadas, e uma duração.</span><span class="sxs-lookup"><span data-stu-id="21d72-141">It has an estimated effort, a planned number of resources, planned start and end dates, and a duration.</span></span>|

  
## <a name="task-hierarchy"></a><span data-ttu-id="21d72-142">Hierarquia de tarefas</span><span class="sxs-lookup"><span data-stu-id="21d72-142">Task hierarchy</span></span>  
 <span data-ttu-id="21d72-143">Estão disponíveis as seguintes opções ao criação uma hierarquia de tarefas:</span><span class="sxs-lookup"><span data-stu-id="21d72-143">You have the following options when creating a task hierarchy:</span></span>  
  
- <span data-ttu-id="21d72-144">**Adicionar tarefa**.</span><span class="sxs-lookup"><span data-stu-id="21d72-144">**Add task**.</span></span>   <span data-ttu-id="21d72-145">Poderá adicionar uma tarefa numa posição à escolha na hierarquia de tarefas.</span><span class="sxs-lookup"><span data-stu-id="21d72-145">You can add a task at a position you choose in the task hierarchy.</span></span> <span data-ttu-id="21d72-146">Se não selecionar uma posição, a sua nova tarefa é apresentada no final.</span><span class="sxs-lookup"><span data-stu-id="21d72-146">If you don’t select a position, your new task appears at the end.</span></span>  
  
- <span data-ttu-id="21d72-147">**Avançar tarefa**.</span><span class="sxs-lookup"><span data-stu-id="21d72-147">**Indent task**.</span></span>   <span data-ttu-id="21d72-148">Avance uma tarefa para a converter numa subordinada da tarefa diretamente acima.</span><span class="sxs-lookup"><span data-stu-id="21d72-148">Indent a task to make it a child of the task directly above it.</span></span>  
  
- <span data-ttu-id="21d72-149">**Diminuir avanço da tarefa**.</span><span class="sxs-lookup"><span data-stu-id="21d72-149">**Outdent task**.</span></span>   <span data-ttu-id="21d72-150">Diminua o avanço de uma tarefa para deixar de ser uma subtarefa do tarefa principal original.</span><span class="sxs-lookup"><span data-stu-id="21d72-150">Outdent a task to make it so it’s no longer a sub-task of its original parent task.</span></span>  
  
- <span data-ttu-id="21d72-151">**Mover para cima e Mover para baixo**.</span><span class="sxs-lookup"><span data-stu-id="21d72-151">**Move up and Move down**.</span></span>   <span data-ttu-id="21d72-152">Mova para cima e para baixo as tarefas na hierarquia da respetiva tarefa principal.</span><span class="sxs-lookup"><span data-stu-id="21d72-152">Move tasks up and down in the hierarchy of its parent task.</span></span> <span data-ttu-id="21d72-153">Mover para cima ou para baixo uma tarefa não produz efeitos no respetivo esforço, custo, datas ou duração.</span><span class="sxs-lookup"><span data-stu-id="21d72-153">Moving a task up or down has no effect on its effort, cost, dates, or duration.</span></span>  
  
## <a name="task-attributes"></a><span data-ttu-id="21d72-154">Atributos da tarefa</span><span class="sxs-lookup"><span data-stu-id="21d72-154">Task attributes</span></span>  
 <span data-ttu-id="21d72-155">O nome de uma tarefa descreve o trabalho que tem de ser concluído.</span><span class="sxs-lookup"><span data-stu-id="21d72-155">A task’s name describes the work that needs to be completed.</span></span> <span data-ttu-id="21d72-156">Utilize vários atributos da tarefa para descrever a agenda e os requisitos de pessoal para a tarefa.</span><span class="sxs-lookup"><span data-stu-id="21d72-156">You use various task attributes to describe the schedule and staffing requirements for the task.</span></span>  
  
### <a name="schedule-attributes"></a><span data-ttu-id="21d72-157">Agendar atributos</span><span class="sxs-lookup"><span data-stu-id="21d72-157">Schedule attributes</span></span>

 - <span data-ttu-id="21d72-158">Atribua valores a **Horas de Esforço**, **Número de recursos**, **Data de início**, **Data de fim** e **Duração** para determinar a agenda da tarefa.</span><span class="sxs-lookup"><span data-stu-id="21d72-158">Assign values to **Effort hours**, **Number of resources**, **Start date**, **End date**, and **Duration** to determine the schedule for the task.</span></span> 
 - <span data-ttu-id="21d72-159">**Esforço** é uma estimativa das horas que demora a concluir a tarefa.</span><span class="sxs-lookup"><span data-stu-id="21d72-159">**Effort** is an estimate of the hours it takes to complete the task.</span></span>
 - <span data-ttu-id="21d72-160">**Número de recursos** é uma estimativa que o gestor do projeto coloca na tarefa para ajudar a determinar a melhor agenda possível.</span><span class="sxs-lookup"><span data-stu-id="21d72-160">**Number of resources** is an estimate that the project manager puts in the task to help come up with the best possible schedule.</span></span> 
 - <span data-ttu-id="21d72-161">**Duração** (dias) indica o número de dias de trabalho que demorará a concluir a tarefa.</span><span class="sxs-lookup"><span data-stu-id="21d72-161">**Duration** (in days) indicates the number of work days it will take to complete the task.</span></span>  
  
### <a name="staffing-attributes"></a><span data-ttu-id="21d72-162">Atributos do pessoal</span><span class="sxs-lookup"><span data-stu-id="21d72-162">Staffing attributes</span></span>

 - <span data-ttu-id="21d72-163">**Função**, **Unidade organizacional do recurso**, **Número de recursos** e **Recursos** descrevem os requisitos de pessoal para a tarefa.</span><span class="sxs-lookup"><span data-stu-id="21d72-163">**Role**, **Resource organizational unit**, **Number of resources**, and **Resources** describe the staffing requirements for the task.</span></span> 
 - <span data-ttu-id="21d72-164">**Função** descreve o tipo de recurso necessário para executar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="21d72-164">**Role** describes the type of resource needed to perform the task.</span></span> 
 - <span data-ttu-id="21d72-165">**Unidade organizacional do recurso** indica a unidade organizacional na qual os recursos devem receber pessoal para essa tarefa; isto também tem impacto na estimativa de custo e vendas da tarefa, uma vez que é contabilizado para quando determinar o preço de venda da unidade do recurso.</span><span class="sxs-lookup"><span data-stu-id="21d72-165">**Resource organizational unit** indicates the organizational unit from which resources should be staffed for that task; this also impacts the cost and sales estimate of the task, since this is accounted for when determining the unit sales price for the resource.</span></span> 
 - <span data-ttu-id="21d72-166">**Recursos** contém um recurso genérico ou um recurso nomeado quando é encontrado um.</span><span class="sxs-lookup"><span data-stu-id="21d72-166">**Resources** holds a generic resource or a named resource when one is found.</span></span>  
  
## <a name="task-dependencies"></a><span data-ttu-id="21d72-167">Dependências de tarefa</span><span class="sxs-lookup"><span data-stu-id="21d72-167">Task dependencies</span></span>  
 <span data-ttu-id="21d72-168">Poderá criar relações de antecessora entre uma ou mais tarefas na estrutura hierárquica do trabalho.</span><span class="sxs-lookup"><span data-stu-id="21d72-168">You can create predecessor relationships between one or more tasks in the work breakdown structure.</span></span> <span data-ttu-id="21d72-169">Pode definir um ou mais valores para o campo antecessor nas tarefas para indicar as tarefas das quais irá depender.</span><span class="sxs-lookup"><span data-stu-id="21d72-169">You can set one or more values for the predecessor field on tasks to indicate the tasks that it will be dependent on.</span></span> <span data-ttu-id="21d72-170">Quando atribui um valor antecessor a uma tarefa, a tarefa só pode ser iniciado quando todas as tarefas antecessoras forem concluídas.</span><span class="sxs-lookup"><span data-stu-id="21d72-170">When you assign a predecessor value to a task, the task can only start when all the predecessor tasks have completed.</span></span> <span data-ttu-id="21d72-171">A definição desta dependência numa tarefa resulta no recálculo da data de início planeado da tarefa como o último final de todas as antecessoras.</span><span class="sxs-lookup"><span data-stu-id="21d72-171">Setting this dependency on a task will result in the recalculation of the planned start date of the task as the latest end of all of its predecessors.</span></span> <span data-ttu-id="21d72-172">Os impactos relacionados com a antecessora numa agenda não estão limitados pelo modo de tarefa definido na tarefa.</span><span class="sxs-lookup"><span data-stu-id="21d72-172">Predecessor-related impacts on a schedule are not limited by the task mode defined on the task.</span></span>  
  
## <a name="task-mode"></a><span data-ttu-id="21d72-173">Modo de tarefa</span><span class="sxs-lookup"><span data-stu-id="21d72-173">Task mode</span></span>  
 <span data-ttu-id="21d72-174">O modo de tarefa é um dos mais importantes fatores que determinam as tarefas de nós de folha de agendamento.</span><span class="sxs-lookup"><span data-stu-id="21d72-174">Task mode is one of the important factors that determine scheduling leaf node tasks.</span></span> <span data-ttu-id="21d72-175">Existem dois modos de tarefa para cada tarefa: modo de agendamento automático e modo de agendamento manual.</span><span class="sxs-lookup"><span data-stu-id="21d72-175">There are two task modes for every task: auto scheduling mode and manual scheduling mode.</span></span>  
  
-   <span data-ttu-id="21d72-176">**Agendamento automático**.</span><span class="sxs-lookup"><span data-stu-id="21d72-176">**Auto scheduling**.</span></span>   <span data-ttu-id="21d72-177">Quando define o modo de tarefa como Agendado Automaticamente, o motor de agendamento da tarefa utiliza as regras de agendamento nos seguintes atributos da tarefa para determinar a agenda para a tarefa:</span><span class="sxs-lookup"><span data-stu-id="21d72-177">When you set the task mode to Automatically Scheduled, the task scheduling engine uses the scheduling rules on the following task attributes to determine the schedule for the task:</span></span>  
  
    -   <span data-ttu-id="21d72-178">Antecessores</span><span class="sxs-lookup"><span data-stu-id="21d72-178">Predecessors</span></span>  
  
    -   <span data-ttu-id="21d72-179">Esforço</span><span class="sxs-lookup"><span data-stu-id="21d72-179">Effort</span></span>  
  
    -   <span data-ttu-id="21d72-180">Número de recursos</span><span class="sxs-lookup"><span data-stu-id="21d72-180">Number of resources</span></span>  
  
    -   <span data-ttu-id="21d72-181">Dadas de início e de fim</span><span class="sxs-lookup"><span data-stu-id="21d72-181">Start and end dates</span></span>  
  
-   <span data-ttu-id="21d72-182">**Regras de agendamento**.</span><span class="sxs-lookup"><span data-stu-id="21d72-182">**Scheduling rules**.</span></span>   <span data-ttu-id="21d72-183">A data de início de uma tarefa de nós de folha não tem predefinições de antecessores para a data de início de agendamento do projeto.</span><span class="sxs-lookup"><span data-stu-id="21d72-183">The start date of a leaf node task that does not have predecessors defaults to the project’s scheduling start date.</span></span> <span data-ttu-id="21d72-184">A duração de uma tarefa de nós de folha é sempre calculada como o número de dias de trabalho entre as datas de início e de fim.</span><span class="sxs-lookup"><span data-stu-id="21d72-184">The duration of a leaf node task is always calculated as the number of working days between its start and end dates.</span></span> <span data-ttu-id="21d72-185">Quando uma tarefa é agendada automaticamente, o motor de agendamento segue as regras abaixo:</span><span class="sxs-lookup"><span data-stu-id="21d72-185">When a task is automatically scheduled, the scheduling engine follows the rules below:</span></span>  
  
    -   <span data-ttu-id="21d72-186">As datas de início e de fim de uma tarefa têm de ser sempre dias úteis de acordo com o calendário de agendamento do projeto</span><span class="sxs-lookup"><span data-stu-id="21d72-186">Start and end dates of a task must always be working days according to the project’s scheduling calendar</span></span>  
  
    -   <span data-ttu-id="21d72-187">A data de início de uma tarefa com antecessores assume por predefinição a data de fim mais recente dos respetivos antecessores</span><span class="sxs-lookup"><span data-stu-id="21d72-187">The start date of a task that has predecessors defaults to the latest end date of its predecessors</span></span>  
  
    -   <span data-ttu-id="21d72-188">Esforço = número de pessoas \* Duração \* horas num dia útil padrão do calendário do projeto</span><span class="sxs-lookup"><span data-stu-id="21d72-188">Effort = Number of people \* Duration \* hours in a standard work day of the project calendar</span></span>  
  
-   <span data-ttu-id="21d72-189">**Agendamento manual**.</span><span class="sxs-lookup"><span data-stu-id="21d72-189">**Manual scheduling**.</span></span>   <span data-ttu-id="21d72-190">Em alguns casos, poderá querer afastar-se destas regras.</span><span class="sxs-lookup"><span data-stu-id="21d72-190">In some cases, you might want to deviate from these rules.</span></span> <span data-ttu-id="21d72-191">Nestes casos, poderá definir o modo de tarefa para a tarefa ser agendada manualmente.</span><span class="sxs-lookup"><span data-stu-id="21d72-191">In these cases, you can set the task mode for the task to be manually scheduled.</span></span> <span data-ttu-id="21d72-192">Desta forma, o motor de agendamento para o cálculo dos valores para outros atributos de agendamento.</span><span class="sxs-lookup"><span data-stu-id="21d72-192">This stops the scheduling engine from calculating the values for other scheduling attributes.</span></span> <span data-ttu-id="21d72-193">A definição de antecessores em tarefas tem sempre impacto na data de início da tarefa dependente.</span><span class="sxs-lookup"><span data-stu-id="21d72-193">Setting predecessors on tasks always impacts the dependent task’s start date.</span></span>  
  
## <a name="create-a-work-breakdown-structure"></a><span data-ttu-id="21d72-194">Criar uma estrutura hierárquica do trabalho</span><span class="sxs-lookup"><span data-stu-id="21d72-194">Create a work breakdown structure</span></span>  
  
1.  <span data-ttu-id="21d72-195">Vá para **Project Service > Projetos**.</span><span class="sxs-lookup"><span data-stu-id="21d72-195">Go to **Project Service > Projects**.</span></span>  
  
2.  <span data-ttu-id="21d72-196">Clique no projeto em que pretende trabalhar.</span><span class="sxs-lookup"><span data-stu-id="21d72-196">Click the project you want to work on.</span></span>  
  
3.  <span data-ttu-id="21d72-197">Na barra na parte superior do ecrã, selecione a seta para baixo junto ao nome do projeto e, em seguida, clique em estrutura hierárquica do trabalho.</span><span class="sxs-lookup"><span data-stu-id="21d72-197">In the bar across the top of the screen, select the down arrow next to the project name, and then click Work breakdown structure.</span></span>  
  
4.  <span data-ttu-id="21d72-198">Para adicionar uma tarefa, clique em **Adicionar Tarefa**.</span><span class="sxs-lookup"><span data-stu-id="21d72-198">To add a task, click **Add Task**.</span></span> <span data-ttu-id="21d72-199">Preencha os campos para a tarefa e clique e **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="21d72-199">Fill in the fields for the task, and then click **Save**.</span></span>  
  
5.  <span data-ttu-id="21d72-200">Continue a adicionar tarefas até a estrutura hierárquica do trabalho estar concluída.</span><span class="sxs-lookup"><span data-stu-id="21d72-200">Continue adding tasks until your work breakdown structure is complete.</span></span> <span data-ttu-id="21d72-201">Enquanto cria a estrutura hierárquica do trabalho, pode fazer o seguinte para organizar as suas tarefas:</span><span class="sxs-lookup"><span data-stu-id="21d72-201">While creating your work breakdown structure, you can do the following to organize your tasks:</span></span>  
  
    -   <span data-ttu-id="21d72-202">Selecione uma tarefa e clique em **Avançar** para movê-la para outra tarefa ou clique em Diminuir Avanço para a mover para fora de um nível.</span><span class="sxs-lookup"><span data-stu-id="21d72-202">Select a task and click **Indent** to move it under another task or click Outdent to move it out a level.</span></span>  
  
    -   <span data-ttu-id="21d72-203">Selecione uma tarefa e clique em **Mover para Cima** ou **Mover para Baixo** para a mover para cima ou para baixo na lista.</span><span class="sxs-lookup"><span data-stu-id="21d72-203">Select a task and click **Move Up** or **Move Down** to move it up or down in the list.</span></span>  
  
    -   <span data-ttu-id="21d72-204">Clique em **Ocultar Gantt** para ocultar o gráfico Gantt e clique em **Mostrar Gantt** para o apresentar novamente.</span><span class="sxs-lookup"><span data-stu-id="21d72-204">Click **Hide Gantt** to hide the Gantt chart, and click **Show Gantt** to display it again.</span></span>  
  
    -   <span data-ttu-id="21d72-205">Selecione um período de tempo diferente para o gráfico Gantt em **Escala Temporal**.</span><span class="sxs-lookup"><span data-stu-id="21d72-205">Select a different period of time for the Gantt chart in **Time Scale**.</span></span>  
  
6.  <span data-ttu-id="21d72-206">Para adicionar as funções especificadas na estrutura hierárquica do trabalho aos membros da equipa do projeto, clique em **Gerar Equipa do Projeto**.</span><span class="sxs-lookup"><span data-stu-id="21d72-206">To add the roles you specified in your work breakdown structure to your project’s team members, click **Generate Project Team**.</span></span>  
  
7.  <span data-ttu-id="21d72-207">Clique em **Guardar** no canto inferior direito do ecrã quando concluir as alterações.</span><span class="sxs-lookup"><span data-stu-id="21d72-207">Click **Save** at the bottom right corner of the screen when you’re done making changes.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="21d72-208">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="21d72-208">See Also</span></span>  
 [<span data-ttu-id="21d72-209">Manual do gestor de projeto</span><span class="sxs-lookup"><span data-stu-id="21d72-209">Project manager guide</span></span>](../psa/project-manager-guide.md)
