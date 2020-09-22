---
title: Configurar Project Service Automation
description: Passos de configuração do Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 56ba0b8d-808c-48d6-965f-abd74b49c2b4
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 52be4705e6ef983dcf421df5d1bfb5c6de8e9a30
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754519"
---
# <a name="configure-project-service"></a><span data-ttu-id="1ccf7-103">Configurar o Project Service</span><span class="sxs-lookup"><span data-stu-id="1ccf7-103">Configure Project Service</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="1ccf7-104">Antes de poder utilizar as funcionalidades de automatização do [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] no [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] para gerir as suas contas, projetos e recursos, tem de completar alguns passos de configuração para assegurar que a solução do [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] corresponde às necessidades da organização.</span><span class="sxs-lookup"><span data-stu-id="1ccf7-104">Before you can use the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automation capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] to manage your accounts, projects, and resources, you need to complete a few configuration steps to ensure the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] solution matches your organization’s needs.</span></span> <span data-ttu-id="1ccf7-105">Estes passos incluem:</span><span class="sxs-lookup"><span data-stu-id="1ccf7-105">These steps include:</span></span>  
  
-   <span data-ttu-id="1ccf7-106">[Configurar unidades de tempo](../project-service/set-up-time-units.md).</span><span class="sxs-lookup"><span data-stu-id="1ccf7-106">[Set up time units](../project-service/set-up-time-units.md).</span></span> <span data-ttu-id="1ccf7-107">Configure as unidades de tempo no catálogo de produtos que utilizará como base para agendar e faturar os seus projetos.</span><span class="sxs-lookup"><span data-stu-id="1ccf7-107">Configure the time units in the product catalog that you’ll use as a base for scheduling and billing your projects.</span></span>  
  
-   <span data-ttu-id="1ccf7-108">[Configurar moedas e taxas de câmbio](../project-service/set-up-currencies-exchange-rates.md).</span><span class="sxs-lookup"><span data-stu-id="1ccf7-108">[Set up currencies and exchange rates](../project-service/set-up-currencies-exchange-rates.md).</span></span> <span data-ttu-id="1ccf7-109">Configure as moedas a utilizar para os seus projetos.</span><span class="sxs-lookup"><span data-stu-id="1ccf7-109">Set up the currencies to use for your projects.</span></span>  
  
-   <span data-ttu-id="1ccf7-110">[Criar unidades organizacionais](../project-service/create-organizational-units.md).</span><span class="sxs-lookup"><span data-stu-id="1ccf7-110">[Create organizational units](../project-service/create-organizational-units.md).</span></span> <span data-ttu-id="1ccf7-111">Configure os grupos que a sua empresa utiliza para dividir o negócio, quer por região, função de negócio ou outra divisão lógica.</span><span class="sxs-lookup"><span data-stu-id="1ccf7-111">Set up the groups that your company uses to divide its business, whether by geography, business function, or other logical division.</span></span>  
  
-   <span data-ttu-id="1ccf7-112">[Configurar frequências de fatura](../project-service/set-up-invoice-frequencies.md).</span><span class="sxs-lookup"><span data-stu-id="1ccf7-112">[Set up invoice frequencies](../project-service/set-up-invoice-frequencies.md).</span></span> <span data-ttu-id="1ccf7-113">Configure os períodos de tempo que pretende utilizar para faturar os seus clientes.</span><span class="sxs-lookup"><span data-stu-id="1ccf7-113">Set up time periods that you want to use for billing your clients.</span></span>  
  
-   <span data-ttu-id="1ccf7-114">[Configurar categorias de transação](../project-service/configure-transaction-categories.md).</span><span class="sxs-lookup"><span data-stu-id="1ccf7-114">[Configure transaction categories](../project-service/configure-transaction-categories.md).</span></span> <span data-ttu-id="1ccf7-115">Configure as categorias de transação às quais os seus consultores podem cobrar as despesas faturáveis e não faturáveis.</span><span class="sxs-lookup"><span data-stu-id="1ccf7-115">Set up transaction categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="1ccf7-116">[Configurar categorias de despesas](../project-service/configure-expense-categories.md).</span><span class="sxs-lookup"><span data-stu-id="1ccf7-116">[Configure expense categories](../project-service/configure-expense-categories.md).</span></span> <span data-ttu-id="1ccf7-117">Configure as categorias às quais os seus consultores podem cobrar as despesas faturáveis e não faturáveis.</span><span class="sxs-lookup"><span data-stu-id="1ccf7-117">Set up the categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="1ccf7-118">[Criar itens do catálogo de produtos](../project-service/create-product-catalog-items.md).</span><span class="sxs-lookup"><span data-stu-id="1ccf7-118">[Create product catalog items](../project-service/create-product-catalog-items.md).</span></span> <span data-ttu-id="1ccf7-119">Adicione os produtos que vende, como as licenças de software, ao catálogo de produtos.</span><span class="sxs-lookup"><span data-stu-id="1ccf7-119">Add the products you sell, such as software licenses, to the product catalog.</span></span>  
  
-   <span data-ttu-id="1ccf7-120">[Criar uma lista de preços](../project-service/create-price-list.md).</span><span class="sxs-lookup"><span data-stu-id="1ccf7-120">[Create a price list](../project-service/create-price-list.md).</span></span> <span data-ttu-id="1ccf7-121">Configure diferentes listas de preços consoante quanto pretende cobrar aos clientes para cada função que o projeto necessite.</span><span class="sxs-lookup"><span data-stu-id="1ccf7-121">Configure different price lists, depending on how much you want to charge your clients for each role their project requires.</span></span>  
  
-   <span data-ttu-id="1ccf7-122">[Configurar recursos](../project-service/set-up-resources.md).</span><span class="sxs-lookup"><span data-stu-id="1ccf7-122">[Set up resources](../project-service/set-up-resources.md).</span></span> <span data-ttu-id="1ccf7-123">Adicione as competências, proficiências, funções de recursos e outras informações de recursos que irá necessitar para os seus projetos.</span><span class="sxs-lookup"><span data-stu-id="1ccf7-123">Add the skills, proficiencies, resource roles, and other resource information that you’ll need for your projects.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="1ccf7-124">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="1ccf7-124">See Also</span></span>  
 <span data-ttu-id="1ccf7-125">[Descrição Geral do Project Service Automation](../project-service/overview.md) </span><span class="sxs-lookup"><span data-stu-id="1ccf7-125">[Overview of Project Service Automation](../project-service/overview.md) </span></span>  
 <span data-ttu-id="1ccf7-126">[Configurar Project Service Automation](../project-service/configure.md) </span><span class="sxs-lookup"><span data-stu-id="1ccf7-126">[Configure Project Service Automation](../project-service/configure.md) </span></span>  
 <span data-ttu-id="1ccf7-127">[Guia do Gestor de Contas](../project-service/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="1ccf7-127">[Account Manager Guide](../project-service/account-manager-guide.md) </span></span>  
 <span data-ttu-id="1ccf7-128">[Guia do Gestor de Projeto](../project-service/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="1ccf7-128">[Project Manager Guide](../project-service/project-manager-guide.md) </span></span>  
 <span data-ttu-id="1ccf7-129">[Guia do Resource Manager](../project-service/resource-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="1ccf7-129">[Resource Manager Guide](../project-service/resource-manager-guide.md) </span></span>  
 [<span data-ttu-id="1ccf7-130">Guia de Tempo, Despesa e Colaboração</span><span class="sxs-lookup"><span data-stu-id="1ccf7-130">Time, Expense, and Collaboration Guid</span></span>](../project-service/time-expense-collaboration-guide.md)
