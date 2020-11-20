---
title: Definições do projeto
description: Este tópico fornece informações sobre as definições de gestão do projeto.
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
ms.openlocfilehash: b2cda6bfd7f152ee948cf49fab91aed475968a09
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123122"
---
# <a name="project-settings"></a><span data-ttu-id="447f7-103">Definições do projeto</span><span class="sxs-lookup"><span data-stu-id="447f7-103">Project settings</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="447f7-104">Utilize as seguintes definições para aceder às funcionalidades de planeamento do projeto.</span><span class="sxs-lookup"><span data-stu-id="447f7-104">Use the following settings to access the project planning features.</span></span>

## <a name="work-template"></a><span data-ttu-id="447f7-105">Modelo de trabalho</span><span class="sxs-lookup"><span data-stu-id="447f7-105">Work template</span></span>

<span data-ttu-id="447f7-106">Para criar uma agenda de projeto, cria um modelo de calendário do projeto que define o número de horas de trabalho por dia e todos os encerramentos de companhia.</span><span class="sxs-lookup"><span data-stu-id="447f7-106">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="447f7-107">Para criar um modelo de calendário do projeto, associe um modelo de trabalho ao campo **Modelo de calendário** do projeto.</span><span class="sxs-lookup"><span data-stu-id="447f7-107">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="447f7-108">Siga estes passos para criar um modelo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="447f7-108">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="447f7-109">No PSA, no painel de navegação esquerdo, clique em **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="447f7-109">In PSA, in the left navigation pane, click **Resources**.</span></span> 
2. <span data-ttu-id="447f7-110">Na página da lista de **Recursos**, abra o registo de utilizador e selecione **Mostrar Horas de Trabalho**.</span><span class="sxs-lookup"><span data-stu-id="447f7-110">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="447f7-111">Certifique-se de que permite pop-ups na página do browser.</span><span class="sxs-lookup"><span data-stu-id="447f7-111">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="447f7-112">Isto permite-lhe ver as horas de trabalho definidas para o recurso.</span><span class="sxs-lookup"><span data-stu-id="447f7-112">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="447f7-113">No separador **Vista Mensal**, clique em **Configurar**.</span><span class="sxs-lookup"><span data-stu-id="447f7-113">On the **Monthly View** tab, click **Set Up**.</span></span> <span data-ttu-id="447f7-114">É apresentada uma lista de três opções:</span><span class="sxs-lookup"><span data-stu-id="447f7-114">A list of three options appears:</span></span> 

  - <span data-ttu-id="447f7-115">Nova Agenda Semanal</span><span class="sxs-lookup"><span data-stu-id="447f7-115">New Weekly Schedule</span></span>
  - <span data-ttu-id="447f7-116">Agenda de Trabalho Para Um Dia</span><span class="sxs-lookup"><span data-stu-id="447f7-116">Work Schedule for One Day</span></span>
  - <span data-ttu-id="447f7-117">Intervalo</span><span class="sxs-lookup"><span data-stu-id="447f7-117">Time Off</span></span>

> ![Configurar opções](media/project-13.png)

4. <span data-ttu-id="447f7-119">Selecione **Nova Agenda Semanal** e, em seguida, defina as opções para esta agenda de recursos.</span><span class="sxs-lookup"><span data-stu-id="447f7-119">Select **New Weekly Schedule**, and then set the options for this resource schedule.</span></span> <span data-ttu-id="447f7-120">É possível definir uma agenda semanal periódica, os parâmetros de hora diária, os encerramentos de companhia e muito mais.</span><span class="sxs-lookup"><span data-stu-id="447f7-120">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="447f7-121">Defina o intervalo de datas, selecione **Guardar** e clique em **Fechar**.</span><span class="sxs-lookup"><span data-stu-id="447f7-121">Set the date range, select **Save**, and then click **Close**.</span></span> 
6. <span data-ttu-id="447f7-122">Volte à página da lista de **Recursos** e selecione o recurso para o qual define as horas de trabalho.</span><span class="sxs-lookup"><span data-stu-id="447f7-122">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="447f7-123">Selecione **Definir Calendário Como** para definir o modelo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="447f7-123">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="447f7-124">Na caixa de diálogo **Modelo de Trabalho**, introduza um nome para o modelo de trabalho e selecione **Aplicar**.</span><span class="sxs-lookup"><span data-stu-id="447f7-124">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="447f7-125">Agora, pode associar o modelo de trabalho a um modelo de calendário do projeto.</span><span class="sxs-lookup"><span data-stu-id="447f7-125">You can now associate the work template with a project calendar template.</span></span>

## <a name="resource-roles"></a><span data-ttu-id="447f7-126">Funções do recurso</span><span class="sxs-lookup"><span data-stu-id="447f7-126">Resource roles</span></span>

<span data-ttu-id="447f7-127">O termo *função do recurso* refere-se ao conjunto de qualificações, competências e certificações que uma pessoa tem de ter para executar um conjunto de tarefas específicas num projeto.</span><span class="sxs-lookup"><span data-stu-id="447f7-127">The term *resource role* refers to the set of skills, competencies, and certifications that a person must have to perform a specific set of tasks on a project.</span></span> <span data-ttu-id="447f7-128">O PSA permite-lhe contabilizar e faturar o tempo de um recurso com base na função à qual o recurso está associado.</span><span class="sxs-lookup"><span data-stu-id="447f7-128">PSA lets you cost and bill a resource's time based on the role that the resource is associated with.</span></span> <span data-ttu-id="447f7-129">Cada organização tem de configurar estas funções utilizando a navegação à esquerda no menu **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="447f7-129">Every organization must set up these roles by using the left navigation on the **Project Service** menu.</span></span>

<span data-ttu-id="447f7-130">Cada organização tem de configurar estas funções na página **Categorias de Recurso Ativas**.</span><span class="sxs-lookup"><span data-stu-id="447f7-130">Every organization must set up these roles on the **Active Resource Categories** page.</span></span> <span data-ttu-id="447f7-131">Para abrir esta página, no painel de navegação esquerdo, selecione **Funções do Recurso**.</span><span class="sxs-lookup"><span data-stu-id="447f7-131">To open this page, in the left navigation pane, select **Resource Roles**.</span></span>

## <a name="price-lists"></a><span data-ttu-id="447f7-132">Listas de preços</span><span class="sxs-lookup"><span data-stu-id="447f7-132">Price lists</span></span>

<span data-ttu-id="447f7-133">As listas de preços permitem definir preços de custo e vendas para funções de recursos, categorias de despesa, produtos e outros elementos numa organização.</span><span class="sxs-lookup"><span data-stu-id="447f7-133">Price lists let you set cost and sales prices for resource roles, expense categories, products, and other elements in an organization.</span></span> <span data-ttu-id="447f7-134">Antes de definir estimativas financeiras para o trabalho que deve ser entregue para um projeto, deve criar uma lista de preços de custo e venda subjacente.</span><span class="sxs-lookup"><span data-stu-id="447f7-134">Before you set financial estimates for the work that must be delivered for a project, you should create a backing cost and sales price list.</span></span> <span data-ttu-id="447f7-135">Na secção de parâmetros, também deverá configurar uma lista de preços de custo e de venda predefinida que se aplique a todos os projetos criados na organização.</span><span class="sxs-lookup"><span data-stu-id="447f7-135">In the parameters section, you should also set up a default cost and sales price list that applies to all projects that are created in the organization.</span></span> <span data-ttu-id="447f7-136">Na página **Parâmetros do Projeto Ativos**, certifique-se de que configurou uma lista de preços de custo e venda predefinida.</span><span class="sxs-lookup"><span data-stu-id="447f7-136">On the **Active Project Parameters** page, make sure that you set up a default cost and sales price list.</span></span>
