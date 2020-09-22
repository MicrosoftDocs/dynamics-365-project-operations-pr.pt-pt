---
title: Configurar funções de recursos
description: Como configurar funções de recursos no Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 0a180069-17d9-40fd-b4af-9b8d50f373ea
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 6a32ec4380e847b897931b6691fa8f9784d0cee7
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754500"
---
# <a name="configure-resource-roles-project-service"></a><span data-ttu-id="ec424-103">Configurar funções de recursos (Project Service)</span><span class="sxs-lookup"><span data-stu-id="ec424-103">Configure resource roles (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="ec424-104">As funções têm um papel importante no planeamento do projeto, na determinação dos requisitos dos recursos ou nos custos de um projeto.</span><span class="sxs-lookup"><span data-stu-id="ec424-104">Roles play an important part in project planning, when determining resource requirements or costs of a project.</span></span> <span data-ttu-id="ec424-105">Para cada função que os seus projetos precisarem, tem de criar uma função do recurso e associar as competências e as proficiências a essa função.</span><span class="sxs-lookup"><span data-stu-id="ec424-105">For each role your projects require, you need to create a resource role and associate skills and proficiencies to that role.</span></span> <span data-ttu-id="ec424-106">Por exemplo, poderá querer criar funções para programador, gestor de projetos ou técnico de testes de jogos.</span><span class="sxs-lookup"><span data-stu-id="ec424-106">For example, you might want to create roles for developer, project manager, or game tester.</span></span> <span data-ttu-id="ec424-107">Também pode definir os níveis de proficiência e competências necessários para a função.</span><span class="sxs-lookup"><span data-stu-id="ec424-107">You’ll also set the skills and proficiency levels required for the role.</span></span>  
  
 <span data-ttu-id="ec424-108">Configure as funções de recursos para assegurar a estimativa do projeto real para a sua organização.</span><span class="sxs-lookup"><span data-stu-id="ec424-108">Configure resource roles to ensure effective project estimation for your organization.</span></span>  <span data-ttu-id="ec424-109">Certifique-se também de que define com precisão o tipo de faturação.</span><span class="sxs-lookup"><span data-stu-id="ec424-109">Also make sure you accurately set the billing type.</span></span> <span data-ttu-id="ec424-110">Um item definido com um tipo de faturação não faturável não é mostrado nas linhas do contrato ou da proposta.</span><span class="sxs-lookup"><span data-stu-id="ec424-110">An item set with a non-chargeable billing type doesn’t show up on contract or quote lines.</span></span>  
  
 <span data-ttu-id="ec424-111">Depois de configurar as funções de recursos, pode configurar o custo e os preços de venda com uma lista de preços.</span><span class="sxs-lookup"><span data-stu-id="ec424-111">Once you’ve set up resource roles, you can set up cost and sales prices with a price list.</span></span>  
  
 <span data-ttu-id="ec424-112">Para cada função que pretende adicionar, efetue o seguinte:</span><span class="sxs-lookup"><span data-stu-id="ec424-112">For each role you want to add, do the following:</span></span>  
  
1.  <span data-ttu-id="ec424-113">Vá para **Project Service > Funções de Recursos**.</span><span class="sxs-lookup"><span data-stu-id="ec424-113">Go to **Project Service > Resource Roles**.</span></span>  
  
2.  <span data-ttu-id="ec424-114">Clique em **Novo**.</span><span class="sxs-lookup"><span data-stu-id="ec424-114">Click **New**.</span></span>  
  
3.  <span data-ttu-id="ec424-115">Na área **Geral**, introduza o nome da função em **Nome** e preencha os outros campos conforme for necessário.</span><span class="sxs-lookup"><span data-stu-id="ec424-115">In the **General** area, enter a name for the role in **Name**, and then fill in the other fields as necessary.</span></span>  
  
4.  <span data-ttu-id="ec424-116">Clique em **Guardar** para criar o registo para poder continuar a editá-lo.</span><span class="sxs-lookup"><span data-stu-id="ec424-116">Click **Save** to create the record so you can continue editing it.</span></span>  
  
5.  <span data-ttu-id="ec424-117">Na área **Competências**, clique em **+** para adicionar uma competência.</span><span class="sxs-lookup"><span data-stu-id="ec424-117">In the **Skills** area, click **+** to add a skill.</span></span>  
  
6.  <span data-ttu-id="ec424-118">No painel **Requisito de competência da função**, clique no campo **Competência**, clique no botão **Procurar** e, em seguida, selecione uma competência.</span><span class="sxs-lookup"><span data-stu-id="ec424-118">In the **Role competency requirement** pane, click in the **Skill** field, click the **Search** button, and then select a skill.</span></span>  
  
7.  <span data-ttu-id="ec424-119">Selecione uma proficiência para essa competência e clique em **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="ec424-119">Select a proficiency for that skill, and then click **Save**.</span></span>  
  
8.  <span data-ttu-id="ec424-120">Continue a adicionar competências conforme for necessário.</span><span class="sxs-lookup"><span data-stu-id="ec424-120">Continue adding skills as necessary.</span></span> <span data-ttu-id="ec424-121">Quando terminar, clique em **Guardar** no canto inferior direito do ecrã.</span><span class="sxs-lookup"><span data-stu-id="ec424-121">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
9. <span data-ttu-id="ec424-122">Para disponibilizar esta função do recurso para os projetos utilizarem, clique em **Ativar**.</span><span class="sxs-lookup"><span data-stu-id="ec424-122">To make this resource role available for projects to use, click **Activate**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="ec424-123">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="ec424-123">See Also</span></span>  
 [<span data-ttu-id="ec424-124">Configurar recursos</span><span class="sxs-lookup"><span data-stu-id="ec424-124">Set up resources</span></span>](../project-service/set-up-resources.md)
