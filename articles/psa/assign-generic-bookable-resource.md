---
title: Atribuir recursos reserváveis genéricos a uma equipa de tarefas e projetos
description: Este tópico fornece informações sobre a reserva de recursos genéricos para equipas de tarefas e projetos.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: 5b4c47513b96310745fd2cdb296988a57df0e966
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291408"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a><span data-ttu-id="8e7fa-103">Atribuir recursos reserváveis genéricos a uma tarefa e gerar requisitos de recursos</span><span class="sxs-lookup"><span data-stu-id="8e7fa-103">Assign generic bookable resources to a task and generate resource requirements</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="8e7fa-104">Além da reserva e da atribuição de recursos nomeados ou reais ao seu projeto, pode atribuir recursos genéricos a tarefas do projeto.</span><span class="sxs-lookup"><span data-stu-id="8e7fa-104">In addition to booking and assigning named or real resources to your project, you can assign generic resources to project tasks.</span></span> <span data-ttu-id="8e7fa-105">Estes recursos podem servir como marcadores de posição para os recursos nomeados até estar pronto para definir a equipa para o seu projeto com os recursos nomeados.</span><span class="sxs-lookup"><span data-stu-id="8e7fa-105">These resources can serve as placeholders for named resources until you are ready to staff your project with named resources.</span></span> 

1. <span data-ttu-id="8e7fa-106">No Project Service Automation (PSA), abra a página **Projeto** e no separador **Agenda**, introduza o nome da posição do recurso genérico na célula **Recurso** da agenda.</span><span class="sxs-lookup"><span data-stu-id="8e7fa-106">In Project Service Automation (PSA), open the **Project** page and on the **Schedule** tab, enter the position name of the generic resource in the **Resource** cell of the schedule.</span></span> <span data-ttu-id="8e7fa-107">Alternativamente, clique no ícone **Recurso** na célula para abrir o seletor de recursos e, em seguida, introduza o nome do recurso genérico que pretende criar.</span><span class="sxs-lookup"><span data-stu-id="8e7fa-107">Or, click the **Resource** icon in the cell to open the resource picker and then enter the name of the generic resource that you want to create.</span></span>

![Criar e atribuir um membro da equipa genérico](media/RM-how-to-9.png)

<span data-ttu-id="8e7fa-109">Isto irá abrir o painel **Criação Rápida: Membro da Equipa do Projeto**.</span><span class="sxs-lookup"><span data-stu-id="8e7fa-109">This will open the **Quick Create: Project Team Member** panel.</span></span> 

2. <span data-ttu-id="8e7fa-110">Introduza a função e a unidade organizacional do membro da equipa de recurso genérico e, em seguida, clique em **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="8e7fa-110">Enter the role and organization unit of the generic resource team member and then click **Save**.</span></span>

![Criação rápida de membros da equipa genéricos](media/RM-how-to-10.png)

3. <span data-ttu-id="8e7fa-112">Depois de ter criado o novo membro da equipa de recurso genérico, o mesmo é atribuído à tarefa.</span><span class="sxs-lookup"><span data-stu-id="8e7fa-112">After you have created the new generic resource team member, it is assigned to the task.</span></span> <span data-ttu-id="8e7fa-113">Pode continuar a atribuir esse recurso genérico a outras tarefas na agenda de tarefas.</span><span class="sxs-lookup"><span data-stu-id="8e7fa-113">You can continue to assign that generic resource to other tasks in the task schedule.</span></span>

![Atribuir um membro da equipa genérico existente a tarefas](media/RM-how-to-11.png)

4. <span data-ttu-id="8e7fa-115">Depois de ter atribuído o recurso genérico, pode gerar um requisito de recurso e cumpri-lo, reservando diretamente ou submetendo um pedido de recurso a um gestor de recursos.</span><span class="sxs-lookup"><span data-stu-id="8e7fa-115">After you have assigned the generic resource, you can generate a resource requirement and fulfill it by directly booking or submitting a resource request to a resource manager.</span></span>

![Gerar um requisito para um membro da equipa genérico](media/RM-how-to-12.png)

<span data-ttu-id="8e7fa-117">Na grelha de membros da equipa, além de poder utilizar o seletor de recursos conforme mencionado acima, pode adicionar recursos genéricos diretamente.</span><span class="sxs-lookup"><span data-stu-id="8e7fa-117">On the team member grid, in addition to being able to use the resource picker as mentioned above, you can add generic resources directly.</span></span> <span data-ttu-id="8e7fa-118">Os recursos são adicionados com um requisito de recurso baseado no método de datas de início/fim e alocação especificado no painel **Criação Rápida: Membro da Equipa do Projeto**.</span><span class="sxs-lookup"><span data-stu-id="8e7fa-118">The resources are added with a resource requirement that is based on the start/end dates and allocation method specified in the **Quick Create: Project Team Member** panel.</span></span>

<span data-ttu-id="8e7fa-119">Pode ver uma diferença se adicionar o membro da equipa genérico diretamente e, em seguida, atribuir mais tarefas ao recurso genérico do que o necessário para cobrir as horas.</span><span class="sxs-lookup"><span data-stu-id="8e7fa-119">You can see a difference if you add the generic team member directly and then assign more tasks to the generic resource than they have required hours to cover.</span></span> <span data-ttu-id="8e7fa-120">Clique em **Gerar Requisito** para regenerar o requisito para equilibrar as horas necessárias com as atribuições.</span><span class="sxs-lookup"><span data-stu-id="8e7fa-120">Click **Generate Requirement** to regenerate the requirement to balance the required hours against assignments.</span></span>

<span data-ttu-id="8e7fa-121">Também pode clicar na ligação **Requisito de recurso** na grelha de equipa para abrir o requisito e adicionar competências, recursos preferenciais, etc.</span><span class="sxs-lookup"><span data-stu-id="8e7fa-121">You can also click the **Resource requirement** link in the team grid to open the requirement and add skills, preferred resources, etc.</span></span>

![Requisito de recurso](media/RM-how-to-13.png)



[!INCLUDE[footer-include](../includes/footer-banner.md)]