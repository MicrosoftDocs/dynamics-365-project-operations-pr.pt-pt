---
title: Atribuir recursos reserváveis genéricos a uma equipa de tarefas e projetos
description: Este tópico fornece informações sobre a reserva de recursos genéricos para equipas de tarefas e projetos.
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: f461fbd3-1fce-4aeb-a896-a6d14453a5a4
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 82478e2cf97ab03e80e9f5fbb662b3603d5905b9
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754631"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a><span data-ttu-id="20921-103">Atribuir recursos reserváveis genéricos a uma tarefa e gerar requisitos de recursos</span><span class="sxs-lookup"><span data-stu-id="20921-103">Assign generic bookable resources to a task and generate resource requirements</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="20921-104">Além da reserva e da atribuição de recursos nomeados ou reais ao seu projeto, pode atribuir recursos genéricos a tarefas do projeto.</span><span class="sxs-lookup"><span data-stu-id="20921-104">In addition to booking and assigning named or real resources to your project, you can assign generic resources to project tasks.</span></span> <span data-ttu-id="20921-105">Estes recursos podem servir como marcadores de posição para os recursos nomeados até estar pronto para definir a equipa para o seu projeto com os recursos nomeados.</span><span class="sxs-lookup"><span data-stu-id="20921-105">These resources can serve as placeholders for named resources until you are ready to staff your project with named resources.</span></span> 

1. <span data-ttu-id="20921-106">No Project Service Automation (PSA), abra a página **Projeto** e no separador **Agenda**, introduza o nome da posição do recurso genérico na célula **Recurso** da agenda.</span><span class="sxs-lookup"><span data-stu-id="20921-106">In Project Service Automation (PSA), open the **Project** page and on the **Schedule** tab, enter the position name of the generic resource in the **Resource** cell of the schedule.</span></span> <span data-ttu-id="20921-107">Alternativamente, clique no ícone **Recurso** na célula para abrir o seletor de recursos e, em seguida, introduza o nome do recurso genérico que pretende criar.</span><span class="sxs-lookup"><span data-stu-id="20921-107">Or, click the **Resource** icon in the cell to open the resource picker and then enter the name of the generic resource that you want to create.</span></span>

![Criar e atribuir um membro da equipa genérico](media/RM-how-to-9.png)

<span data-ttu-id="20921-109">Isto irá abrir o painel **Criação Rápida: Membro da Equipa do Projeto**.</span><span class="sxs-lookup"><span data-stu-id="20921-109">This will open the **Quick Create: Project Team Member** panel.</span></span> 

2. <span data-ttu-id="20921-110">Introduza a função e a unidade organizacional do membro da equipa de recurso genérico e, em seguida, clique em **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="20921-110">Enter the role and organization unit of the generic resource team member and then click **Save**.</span></span>

![Criação rápida de membros da equipa genéricos](media/RM-how-to-10.png)

3. <span data-ttu-id="20921-112">Depois de ter criado o novo membro da equipa de recurso genérico, o mesmo é atribuído à tarefa.</span><span class="sxs-lookup"><span data-stu-id="20921-112">After you have created the new generic resource team member, it is assigned to the task.</span></span> <span data-ttu-id="20921-113">Pode continuar a atribuir esse recurso genérico a outras tarefas na agenda de tarefas.</span><span class="sxs-lookup"><span data-stu-id="20921-113">You can continue to assign that generic resource to other tasks in the task schedule.</span></span>

![Atribuir um membro da equipa genérico existente a tarefas](media/RM-how-to-11.png)

4. <span data-ttu-id="20921-115">Depois de ter atribuído o recurso genérico, pode gerar um requisito de recurso e cumpri-lo, reservando diretamente ou submetendo um pedido de recurso a um gestor de recursos.</span><span class="sxs-lookup"><span data-stu-id="20921-115">After you have assigned the generic resource, you can generate a resource requirement and fulfill it by directly booking or submitting a resource request to a resource manager.</span></span>

![Gerar um requisito para um membro da equipa genérico](media/RM-how-to-12.png)

<span data-ttu-id="20921-117">Na grelha de membros da equipa, além de poder utilizar o seletor de recursos conforme mencionado acima, pode adicionar recursos genéricos diretamente.</span><span class="sxs-lookup"><span data-stu-id="20921-117">On the team member grid, in addition to being able to use the resource picker as mentioned above, you can add generic resources directly.</span></span> <span data-ttu-id="20921-118">Os recursos são adicionados com um requisito de recurso baseado no método de datas de início/fim e alocação especificado no painel **Criação Rápida: Membro da Equipa do Projeto**.</span><span class="sxs-lookup"><span data-stu-id="20921-118">The resources are added with a resource requirement that is based on the start/end dates and allocation method specified in the **Quick Create: Project Team Member** panel.</span></span>

<span data-ttu-id="20921-119">Pode ver uma diferença se adicionar o membro da equipa genérico diretamente e, em seguida, atribuir mais tarefas ao recurso genérico do que o necessário para cobrir as horas.</span><span class="sxs-lookup"><span data-stu-id="20921-119">You can see a difference if you add the generic team member directly and then assign more tasks to the generic resource than they have required hours to cover.</span></span> <span data-ttu-id="20921-120">Clique em **Gerar Requisito** para regenerar o requisito para equilibrar as horas necessárias com as atribuições.</span><span class="sxs-lookup"><span data-stu-id="20921-120">Click **Generate Requirement** to regenerate the requirement to balance the required hours against assignments.</span></span>

<span data-ttu-id="20921-121">Também pode clicar na ligação **Requisito de recurso** na grelha de equipa para abrir o requisito e adicionar competências, recursos preferenciais, etc.</span><span class="sxs-lookup"><span data-stu-id="20921-121">You can also click the **Resource requirement** link in the team grid to open the requirement and add skills, preferred resources, etc.</span></span>

![Requisito de recurso](media/RM-how-to-13.png)

