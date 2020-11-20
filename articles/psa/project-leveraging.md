---
title: Estimativas e projetos de vendas
description: Este tópico fornece informações sobre como tirar partido da agenda e das estimativas no processo de vendas.
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: d8bb380519759659dc1b4151b62228a626ee7a26
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120692"
---
# <a name="sales-estimates-and-projects"></a><span data-ttu-id="d22db-103">Estimativas e projetos de vendas</span><span class="sxs-lookup"><span data-stu-id="d22db-103">Sales estimates and projects</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="d22db-104">Durante o processo de vendas, pode criar estimativas de vendas associando um projeto a uma proposta de vendas.</span><span class="sxs-lookup"><span data-stu-id="d22db-104">During the sales process, you can create sales estimates by linking a project to a sales quote.</span></span> <span data-ttu-id="d22db-105">Deste modo, a estimativa determinística pode ocorrer durante o processo de vendas, para tirar partido das capacidades de agendamento e estimativa do projeto.</span><span class="sxs-lookup"><span data-stu-id="d22db-105">In this way, deterministic estimation can occur during the sales process, to take advantage of project scheduling and estimation capabilities.</span></span> <span data-ttu-id="d22db-106">Se a venda for concluída, a agenda utilizada para fins de estimativa de vendas poderá ser utilizada como base para um refinamento adicional do plano do projeto.</span><span class="sxs-lookup"><span data-stu-id="d22db-106">If the sale goes through, the schedule that was used for sales estimation purposes can be used as the basis for further refinement of the project plan.</span></span>

## <a name="linking-a-project-to-a-quote-line"></a><span data-ttu-id="d22db-107">Associar um projeto a uma linha de proposta</span><span class="sxs-lookup"><span data-stu-id="d22db-107">Linking a project to a quote line</span></span>

<span data-ttu-id="d22db-108">Quando cria uma linha de proposta baseada em projetos, pode criar um novo projeto ou associar um projeto existente na página **Linha de Proposta**.</span><span class="sxs-lookup"><span data-stu-id="d22db-108">When you create a project-based quote line, you can create a new project or associate an existing project pn the **Quote Line** page.</span></span> 

> ![Formulário de linha de proposta](media/project-8.png)
 
<span data-ttu-id="d22db-110">Quando cria um novo projeto a partir dos detalhes de linha de proposta, pode tirar partido dos modelos de projeto.</span><span class="sxs-lookup"><span data-stu-id="d22db-110">When you create a new project from the quote line details, you can take advantage of project templates.</span></span> <span data-ttu-id="d22db-111">Os modelos de projeto são projetos de modelo que representam planos do projeto padrão e estimativas financeiras que são típicos de uma organização.</span><span class="sxs-lookup"><span data-stu-id="d22db-111">Project templates are model projects that represent standard project plans and financial estimates that are typical in an organization.</span></span> <span data-ttu-id="d22db-112">Também podem representar cópias de planos e estimativas de projeto a partir de projetos passados.</span><span class="sxs-lookup"><span data-stu-id="d22db-112">They can also represent copies of project plans and estimates from past projects.</span></span>

> ![Detalhes de linha de proposta](media/project-9.png)
  
<span data-ttu-id="d22db-114">Quando cria o projeto a partir da proposta, o projeto é associado automaticamente à linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="d22db-114">When you create the project from the quote, the project is automatically associated with the quote line.</span></span>

## <a name="components-of-estimates-in-a-project"></a><span data-ttu-id="d22db-115">Componentes de estimativas num projeto</span><span class="sxs-lookup"><span data-stu-id="d22db-115">Components of estimates in a project</span></span>

<span data-ttu-id="d22db-116">Uma agenda permite-lhe dividir o trabalho em tarefas, manter uma hierarquia das tarefas, determinar quais os recursos necessários para concluir uma tarefa e atribuir uma estimativa do esforço necessário para concluir uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="d22db-116">A schedule lets you divide work into tasks, maintain a hierarchy of tasks, determine what resources are required to complete a task, and assign an estimate of the effort that is required to complete a task.</span></span>

<span data-ttu-id="d22db-117">Pode definir o esforço de trabalho e agendar estimativas utilizando os campos no separador **Agenda** da página **Projeto**.</span><span class="sxs-lookup"><span data-stu-id="d22db-117">You can define the work effort and schedule estimates by using the fields on the **Schedule** tab of the **Project** page.</span></span> <span data-ttu-id="d22db-118">Uma vez que uma lista de preços está associada ao projeto, as estimativas financeiras são calculadas através da utilização de preços de custo e de venda que são definidos na lista de preços.</span><span class="sxs-lookup"><span data-stu-id="d22db-118">Because a price list is associated with the project, financial estimates are calculated by using cost and sales prices that are defined in the price list.</span></span>

## <a name="importing-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="d22db-119">Importar estimativas de um projeto para uma proposta</span><span class="sxs-lookup"><span data-stu-id="d22db-119">Importing estimates from a project into a quote</span></span>

<span data-ttu-id="d22db-120">Depois de definir as estimativas do projeto, pode importá-las para a linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="d22db-120">After you define project estimates, you can import them into the quote line.</span></span> <span data-ttu-id="d22db-121">Na página **Detalhes de Linha de Proposta**, selecione **Importar a partir da estimativa** a partir de estimativas no friso para resumir as estimativas de projeto por tipo de transação, função ou nível de tarefa.</span><span class="sxs-lookup"><span data-stu-id="d22db-121">On the **Quote Line Details** page, select **Import from estimates** on the ribbon to summarize project estimates by transaction type, role, or task level.</span></span>
