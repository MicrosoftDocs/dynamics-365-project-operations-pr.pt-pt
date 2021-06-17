---
title: Configurar Project Service Automation
description: Passos de configuração do Project Service
author: ruhercul
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
ms.openlocfilehash: ef1724bb92e62ae21472e133fff0978c4faeeffa
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002860"
---
# <a name="configure-project-service"></a><span data-ttu-id="04b75-103">Configurar o Project Service</span><span class="sxs-lookup"><span data-stu-id="04b75-103">Configure Project Service</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="04b75-104">Antes de poder utilizar as funcionalidades de automatização do [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] no [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] para gerir as suas contas, projetos e recursos, tem de completar alguns passos de configuração para assegurar que a solução do [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] corresponde às necessidades da organização.</span><span class="sxs-lookup"><span data-stu-id="04b75-104">Before you can use the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automation capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] to manage your accounts, projects, and resources, you need to complete a few configuration steps to ensure the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] solution matches your organization’s needs.</span></span> <span data-ttu-id="04b75-105">Estes passos incluem:</span><span class="sxs-lookup"><span data-stu-id="04b75-105">These steps include:</span></span>  
  
-   <span data-ttu-id="04b75-106">[Configurar unidades de tempo](../psa/set-up-time-units.md).</span><span class="sxs-lookup"><span data-stu-id="04b75-106">[Set up time units](../psa/set-up-time-units.md).</span></span> <span data-ttu-id="04b75-107">Configure as unidades de tempo no catálogo de produtos que utilizará como base para agendar e faturar os seus projetos.</span><span class="sxs-lookup"><span data-stu-id="04b75-107">Configure the time units in the product catalog that you’ll use as a base for scheduling and billing your projects.</span></span>  
  
-   <span data-ttu-id="04b75-108">[Configurar moedas e taxas de câmbio](../psa/set-up-currencies-exchange-rates.md).</span><span class="sxs-lookup"><span data-stu-id="04b75-108">[Set up currencies and exchange rates](../psa/set-up-currencies-exchange-rates.md).</span></span> <span data-ttu-id="04b75-109">Configure as moedas a utilizar para os seus projetos.</span><span class="sxs-lookup"><span data-stu-id="04b75-109">Set up the currencies to use for your projects.</span></span>  
  
-   <span data-ttu-id="04b75-110">[Criar unidades organizacionais](../psa/create-organizational-units.md).</span><span class="sxs-lookup"><span data-stu-id="04b75-110">[Create organizational units](../psa/create-organizational-units.md).</span></span> <span data-ttu-id="04b75-111">Configure os grupos que a sua empresa utiliza para dividir o negócio, quer por região, função de negócio ou outra divisão lógica.</span><span class="sxs-lookup"><span data-stu-id="04b75-111">Set up the groups that your company uses to divide its business, whether by geography, business function, or other logical division.</span></span>  
  
-   <span data-ttu-id="04b75-112">[Configurar frequências de fatura](../psa/set-up-invoice-frequencies.md).</span><span class="sxs-lookup"><span data-stu-id="04b75-112">[Set up invoice frequencies](../psa/set-up-invoice-frequencies.md).</span></span> <span data-ttu-id="04b75-113">Configure os períodos de tempo que pretende utilizar para faturar os seus clientes.</span><span class="sxs-lookup"><span data-stu-id="04b75-113">Set up time periods that you want to use for billing your clients.</span></span>  
  
-   <span data-ttu-id="04b75-114">[Configurar categorias de transação](../psa/configure-transaction-categories.md).</span><span class="sxs-lookup"><span data-stu-id="04b75-114">[Configure transaction categories](../psa/configure-transaction-categories.md).</span></span> <span data-ttu-id="04b75-115">Configure as categorias de transação às quais os seus consultores podem cobrar as despesas faturáveis e não faturáveis.</span><span class="sxs-lookup"><span data-stu-id="04b75-115">Set up transaction categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="04b75-116">[Configurar categorias de despesas](../psa/configure-expense-categories.md).</span><span class="sxs-lookup"><span data-stu-id="04b75-116">[Configure expense categories](../psa/configure-expense-categories.md).</span></span> <span data-ttu-id="04b75-117">Configure as categorias às quais os seus consultores podem cobrar as despesas faturáveis e não faturáveis.</span><span class="sxs-lookup"><span data-stu-id="04b75-117">Set up the categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="04b75-118">[Criar itens do catálogo de produtos](../psa/create-product-catalog-items.md).</span><span class="sxs-lookup"><span data-stu-id="04b75-118">[Create product catalog items](../psa/create-product-catalog-items.md).</span></span> <span data-ttu-id="04b75-119">Adicione os produtos que vende, como as licenças de software, ao catálogo de produtos.</span><span class="sxs-lookup"><span data-stu-id="04b75-119">Add the products you sell, such as software licenses, to the product catalog.</span></span>  
  
-   <span data-ttu-id="04b75-120">[Criar uma lista de preços](../psa/create-price-list.md).</span><span class="sxs-lookup"><span data-stu-id="04b75-120">[Create a price list](../psa/create-price-list.md).</span></span> <span data-ttu-id="04b75-121">Configure diferentes listas de preços consoante quanto pretende cobrar aos clientes para cada função que o projeto necessite.</span><span class="sxs-lookup"><span data-stu-id="04b75-121">Configure different price lists, depending on how much you want to charge your clients for each role their project requires.</span></span>  
  
-   <span data-ttu-id="04b75-122">[Configurar recursos](../psa/set-up-resources.md).</span><span class="sxs-lookup"><span data-stu-id="04b75-122">[Set up resources](../psa/set-up-resources.md).</span></span> <span data-ttu-id="04b75-123">Adicione as competências, proficiências, funções de recursos e outras informações de recursos que irá necessitar para os seus projetos.</span><span class="sxs-lookup"><span data-stu-id="04b75-123">Add the skills, proficiencies, resource roles, and other resource information that you’ll need for your projects.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="04b75-124">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="04b75-124">See Also</span></span>  
 <span data-ttu-id="04b75-125">[Descrição Geral do Project Service Automation](../psa/overview.md) </span><span class="sxs-lookup"><span data-stu-id="04b75-125">[Overview of Project Service Automation](../psa/overview.md) </span></span>  
 <span data-ttu-id="04b75-126">[Configurar Project Service Automation](../psa/configure.md) </span><span class="sxs-lookup"><span data-stu-id="04b75-126">[Configure Project Service Automation](../psa/configure.md) </span></span>  
 <span data-ttu-id="04b75-127">[Guia do Gestor de Contas](../psa/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="04b75-127">[Account Manager Guide](../psa/account-manager-guide.md) </span></span>  
 <span data-ttu-id="04b75-128">[Guia do Gestor de Projeto](../psa/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="04b75-128">[Project Manager Guide](../psa/project-manager-guide.md) </span></span>  
 <span data-ttu-id="04b75-129">[Guia do Resource Manager](../psa/resource-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="04b75-129">[Resource Manager Guide](../psa/resource-manager-guide.md) </span></span>  
 [<span data-ttu-id="04b75-130">Guia de Tempo, Despesa e Colaboração</span><span class="sxs-lookup"><span data-stu-id="04b75-130">Time, Expense, and Collaboration Guid</span></span>](../psa/time-expense-collaboration-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]