---
title: Apresentar estimativas de trabalho para um projeto durante o processo de vendas
description: Como apresentar estimativas de trabalho para um projeto durante o processo de vendas no Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: ddb7f8c0ff8c7fd7e51edb42f9d227f2b91a811b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082454"
---
# <a name="provide-work-estimates-for-a-project-during-the-sales-process-project-service"></a><span data-ttu-id="124a3-103">Apresentar estimativas de trabalho para um projeto durante o processo de vendas (Project Service)</span><span class="sxs-lookup"><span data-stu-id="124a3-103">Provide work estimates for a project during the sales process (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="124a3-104">Durante o processo de vendas, poderá determinar as estimativas de vendas de raiz com as linhas de proposta.</span><span class="sxs-lookup"><span data-stu-id="124a3-104">During the sales process, you can work out sales estimates from the ground up with quote lines.</span></span> <span data-ttu-id="124a3-105">As capacidades do [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] no [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] oferecem uma forma mais científica e determinística de criar as estimativas de vendas ao dividir os itens de trabalho e ao associar os atributos relevantes que contribuem para as estimativas do projeto na estrutura hierárquica do trabalho.</span><span class="sxs-lookup"><span data-stu-id="124a3-105">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] provide a more scientific and deterministic way of coming up with sales estimates by breaking down work items and associating relevant attributes that contribute toward the estimates for the project in the work breakdown structure.</span></span>  
  
 <span data-ttu-id="124a3-106">Quando ganha a venda, pode utilizar a estrutura hierárquica do trabalho associada no plano do projeto ao refiná-lo conforme for necessário para concluir o projeto com êxito.</span><span class="sxs-lookup"><span data-stu-id="124a3-106">Once you win the sale, you can use the associated work breakdown structure in your project plan, refining it as necessary for successful completion of your project.</span></span>  
  
## <a name="link-a-project-to-a-quote-line"></a><span data-ttu-id="124a3-107">Associar um projeto a uma linha de proposta</span><span class="sxs-lookup"><span data-stu-id="124a3-107">Link a project to a quote line</span></span>  
 <span data-ttu-id="124a3-108">Quando cria uma linha de proposta baseada no projeto, pode criar um novo projeto a partir da linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="124a3-108">When creating a project-based quote line, you can create a new project from the quote line.</span></span> <span data-ttu-id="124a3-109">Poderá utilizar os modelos de projeto, que são planos de projeto padrão pré-configurados e estimativas financeiras comuns à sua organização, ou uma cópia de um plano do projeto e estimativas de um projeto passado.</span><span class="sxs-lookup"><span data-stu-id="124a3-109">You can then use project templates, which are either pre-configured standard project plans and financial estimates common to your organization, or a copy of a project plan and estimates from a past project.</span></span> <span data-ttu-id="124a3-110">Quando cria um projeto, a escolha de um modelo de projeto fornece uma base para refinar o plano do projeto, as estimativas e os requisitos da função.</span><span class="sxs-lookup"><span data-stu-id="124a3-110">When you create a project, choosing a project template provides a basis to refine the project plan, estimates, and role requirements.</span></span> <span data-ttu-id="124a3-111">Ao criar o projeto a partir da proposta, o projeto é associado automaticamente à linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="124a3-111">By creating your project from the quote, the project is automatically associated with the quote line.</span></span>  
  
## <a name="project-estimate-components"></a><span data-ttu-id="124a3-112">Componentes da estimativa do projeto</span><span class="sxs-lookup"><span data-stu-id="124a3-112">Project estimate components</span></span>  
 <span data-ttu-id="124a3-113">A estrutura hierárquica do trabalho num projeto fornece uma forma de dividir o trabalho em tarefas, manter de uma hierarquia de tarefas e atribuir uma estimativa do esforço necessário para concluir cada tarefa.</span><span class="sxs-lookup"><span data-stu-id="124a3-113">The work breakdown structure in a project provides a way to break down work into tasks, maintain a hierarchy of tasks, and assign an estimate of effort required to complete each task.</span></span> <span data-ttu-id="124a3-114">Também poderá associar funções a uma tarefa para indicar uma estimativa do tipo de recurso necessário para concluir uma tarefa e uma agenda.</span><span class="sxs-lookup"><span data-stu-id="124a3-114">You can also associate roles to a task to indicate an estimate of the type of resource required to complete a task and a schedule.</span></span>  
  
 <span data-ttu-id="124a3-115">A estrutura hierárquica do trabalho ajuda a determinar o esforço do trabalho e as estimativas de agenda.</span><span class="sxs-lookup"><span data-stu-id="124a3-115">The work breakdown structure helps you determine work effort and schedule estimates.</span></span> <span data-ttu-id="124a3-116">Por predefinição, o projeto utiliza listas de preços predefinidas que definiu anteriormente.</span><span class="sxs-lookup"><span data-stu-id="124a3-116">By default, the project uses default price lists that you defined earlier.</span></span> <span data-ttu-id="124a3-117">O custo e os preços de vendas definidos nas listas de preços ajudam a determinar as estimativas financeiras para a divisão hierárquica do trabalho do projeto.</span><span class="sxs-lookup"><span data-stu-id="124a3-117">The cost and sales prices defined in the price lists help determine financial estimates for the project’s work breakdown.</span></span>  
  
 <span data-ttu-id="124a3-118">Se o projeto estiver associado a uma proposta, e esta tiver uma lista de preços diferente da predefinição, é utilizada a lista de preços da proposta para as estimativas.</span><span class="sxs-lookup"><span data-stu-id="124a3-118">If your project is associated with a quote, and the quote has a different price list from the default, the quote’s price list is used for financial estimates.</span></span>  
  
## <a name="import-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="124a3-119">Importar estimativas de um projeto para uma proposta</span><span class="sxs-lookup"><span data-stu-id="124a3-119">Import estimates from a project into a quote</span></span>  
 <span data-ttu-id="124a3-120">Quando tiver as estimativas do projeto no projeto, poderá importá-las para linha de proposta:</span><span class="sxs-lookup"><span data-stu-id="124a3-120">Once you have project estimates in the project, you can import these estimates into the quote line:</span></span>  
  
-   <span data-ttu-id="124a3-121">Em **Detalhes de Linha de Proposta** , clique em **Importar a partir da estimativa**.</span><span class="sxs-lookup"><span data-stu-id="124a3-121">In **Quote Line Details** , click **Import from estimates**.</span></span> 

-   <span data-ttu-id="124a3-122">Selecione se pretende importar as estimativas do projeto resumidas por nível de nó da estrutura hierárquica do trabalho, tipo de transação ou função.</span><span class="sxs-lookup"><span data-stu-id="124a3-122">Select whether to import project estimates summarized by transaction type, role, or work breakdown structure node level.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="124a3-123">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="124a3-123">See Also</span></span>  
 [<span data-ttu-id="124a3-124">Guia do Gestor de Projeto</span><span class="sxs-lookup"><span data-stu-id="124a3-124">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
