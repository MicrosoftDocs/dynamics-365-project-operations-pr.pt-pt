---
title: Controlar o estado de um projeto
description: Como monitorizar o estado de um projeto no Project Service
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
ms.openlocfilehash: e9c8b594d468016264d0b4d9745597a35f55e50e
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149602"
---
# <a name="track-a-projects-status-project-service"></a><span data-ttu-id="c2559-103">Monitorizar o estado de um projeto (Project Service)</span><span class="sxs-lookup"><span data-stu-id="c2559-103">Track a project’s status (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="c2559-104">Utilize as capacidades do [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] para controlar o progresso de um projeto do cliente.</span><span class="sxs-lookup"><span data-stu-id="c2559-104">Use the [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] to track the progress of a client’s project.</span></span>  

<span data-ttu-id="c2559-105">À medida que cativação progride, as fases do projeto refletem a fase da cativação:</span><span class="sxs-lookup"><span data-stu-id="c2559-105">As the engagement progresses, the project stages update to reflect the stage of the engagement:</span></span>  


|              |                                                                                                                                                                                                                                                                                                  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   <span data-ttu-id="c2559-106">**Novo**</span><span class="sxs-lookup"><span data-stu-id="c2559-106">**New**</span></span>    | <span data-ttu-id="c2559-107">Quando cria um projeto, a fase é definida como **Novo**.</span><span class="sxs-lookup"><span data-stu-id="c2559-107">When you create a project, the stage is set to **New**.</span></span> <span data-ttu-id="c2559-108">Se tiver criado o projeto a partir de um modelo, nesta fase o projeto pode ter uma agenda, estimativas e dados da equipa.</span><span class="sxs-lookup"><span data-stu-id="c2559-108">If you created the project from a template, at this stage the project may have a schedule, estimates, and team data.</span></span> <span data-ttu-id="c2559-109">Caso contrário, será o esquema do projeto e terá de introduzir manualmente os restantes componentes do projeto.</span><span class="sxs-lookup"><span data-stu-id="c2559-109">Otherwise, it will be the outline of the project and you need to manually enter the rest of the project components.</span></span> |
|  <span data-ttu-id="c2559-110">**Proposta**</span><span class="sxs-lookup"><span data-stu-id="c2559-110">**Quote**</span></span>   |      <span data-ttu-id="c2559-111">Quando associa um projeto a uma proposta ou o cria a partir de uma proposta, a fase de projeto é definida como **Proposta** e datas de início e de fim estimadas também são atualizadas.</span><span class="sxs-lookup"><span data-stu-id="c2559-111">When you associate a project to a quote or create it from a quote, the project stage is set to **Quote**, and the estimated start and end datesare updated as well.</span></span> <span data-ttu-id="c2559-112">Quando o projeto está na fase de proposta, os detalhes da proposta são apresentados no separador **Vendas** na página **Projeto**.</span><span class="sxs-lookup"><span data-stu-id="c2559-112">When the project is in the quote stage, details on the quote display on the **Sales** tab on the **Project** page.</span></span>      |
|   <span data-ttu-id="c2559-113">**Planear**</span><span class="sxs-lookup"><span data-stu-id="c2559-113">**Plan**</span></span>   |                                     <span data-ttu-id="c2559-114">Quando ganha uma proposta associada a um projeto e quando a cativação progride para a fase de contrato, a fase do projeto é atualizada para **Plano**.</span><span class="sxs-lookup"><span data-stu-id="c2559-114">When you win a quote associated with a project, and when the engagement progresses to the contract stage, the project stage updates to **Plan**.</span></span> <span data-ttu-id="c2559-115">Os detalhes do contrato são apresentados no separador **Vendas** na página **Projeto**.</span><span class="sxs-lookup"><span data-stu-id="c2559-115">Contract details display on the **Sales** tab on the **Project** page.</span></span>                                      |
| <span data-ttu-id="c2559-116">**Concluída**</span><span class="sxs-lookup"><span data-stu-id="c2559-116">**Complete**</span></span> |                    <span data-ttu-id="c2559-117">Quando o trabalho do projeto é concluído, pode mudar a fase para **Concluído**.</span><span class="sxs-lookup"><span data-stu-id="c2559-117">When the project work is complete, you can flip the stage to **Complete**.</span></span> <span data-ttu-id="c2559-118">Quando a fase do projeto é definida como concluído, entende-se que o trabalho está 100% concluído, mas o projeto é mantido aberto para serem registadas quaisquer horas ou despesas pendentes.</span><span class="sxs-lookup"><span data-stu-id="c2559-118">When the project stage is set to complete, it’s understood that the work is 100% complete but the project is kept open for any pending time or expense entries to be recorded.</span></span>                     |
|  <span data-ttu-id="c2559-119">**Fechar**</span><span class="sxs-lookup"><span data-stu-id="c2559-119">**Close**</span></span>   |           <span data-ttu-id="c2559-120">Depois de registadas todas as transações no projeto e não espera que sejam registadas mais, pode definir manualmente a fase como **Fecho**.</span><span class="sxs-lookup"><span data-stu-id="c2559-120">When all transactions have been recorded on the project and you don't expect any more to be logged, you can manually set the stage to **Close**.</span></span> <span data-ttu-id="c2559-121">Quando o projeto é definido como **Fecho**, não é possível registar mais transações no projeto e este passa a ser só de leitura.</span><span class="sxs-lookup"><span data-stu-id="c2559-121">When the project is set to **Close**, you can’t log any more transactions on the project and the project will be read only.</span></span>           |

## <a name="to-track-a-projects-status"></a><span data-ttu-id="c2559-122">Para controlar o estado de um projeto</span><span class="sxs-lookup"><span data-stu-id="c2559-122">To track a project’s status</span></span>  

1.  <span data-ttu-id="c2559-123">Vá para **Project Service > Projetos**.</span><span class="sxs-lookup"><span data-stu-id="c2559-123">Go to **Project Service > Projects**.</span></span>  

2.  <span data-ttu-id="c2559-124">Clique no projeto em que pretende trabalhar.</span><span class="sxs-lookup"><span data-stu-id="c2559-124">Click the project you want to work on.</span></span>  

3.  <span data-ttu-id="c2559-125">Na barra na parte superior do ecrã, selecione a seta para baixo junto ao nome do projeto e, em seguida, clique em **Monitorização do Projeto**.</span><span class="sxs-lookup"><span data-stu-id="c2559-125">In the bar across the top of the screen, select the down arrow next to the project name, and then click **Project Tracking**.</span></span>  

4.  <span data-ttu-id="c2559-126">Selecione **Controlo do Esforço** ou **Controlo dos Custos** na lista pendente acima da lista de tarefas.</span><span class="sxs-lookup"><span data-stu-id="c2559-126">Select **Effort Tracking** or **Cost Tracking** in the drop-down list above the task list.</span></span>  

5.  <span data-ttu-id="c2559-127">Faça duplo clique em qualquer tarefa para editá-la.</span><span class="sxs-lookup"><span data-stu-id="c2559-127">Double-click any task to edit it.</span></span> <span data-ttu-id="c2559-128">Também pode mover ou redimensionar as barras no gráfico Gantt para alterar o tempo e o progresso de uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="c2559-128">You can also move or resize the bars in the Gantt chart to change the time and progress for a task.</span></span>  

### <a name="see-also"></a><span data-ttu-id="c2559-129">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="c2559-129">See Also</span></span>  
 [<span data-ttu-id="c2559-130">Guia do Gestor de Projeto</span><span class="sxs-lookup"><span data-stu-id="c2559-130">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
