---
title: Configurar categorias do projeto
description: Este tópico fornece informações sobre como configurar categorias de projetos.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 3698b68b5dd0460343d26af0fcea5b9a56be4083
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131942"
---
# <a name="configure-project-categories"></a><span data-ttu-id="5dee1-103">Configurar categorias do projeto</span><span class="sxs-lookup"><span data-stu-id="5dee1-103">Configure project categories</span></span>

<span data-ttu-id="5dee1-104">_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_</span><span class="sxs-lookup"><span data-stu-id="5dee1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="5dee1-105">O Project Operations oferece funcionalidades robustas para categorizar as receitas e as despesas nos projetos.</span><span class="sxs-lookup"><span data-stu-id="5dee1-105">Project Operations offers robust capabilities for categorizing revenue and expenses on projects.</span></span> <span data-ttu-id="5dee1-106">As categorias fornecem a capacidade de reportar e analisar transações de projetos, e impulsionar o lançamento no razão geral.</span><span class="sxs-lookup"><span data-stu-id="5dee1-106">Categories provide the ability to report on and analyze project transactions, and drive posting to the general ledger.</span></span>

<span data-ttu-id="5dee1-107">O diagrama seguinte ilustra a correlação entre categorias de transações, categorias partilhadas e categorias de projetos.</span><span class="sxs-lookup"><span data-stu-id="5dee1-107">The following diagram illustrates the correlation between transaction categories, shared categories, and project categories.</span></span> 

<span data-ttu-id="5dee1-108">As categorias de transações são o agrupamento básico para transações de projetos.</span><span class="sxs-lookup"><span data-stu-id="5dee1-108">Transaction categories are the basic grouping for project transactions.</span></span> <span data-ttu-id="5dee1-109">Nesse agrupamento, existe um conjunto de categorias partilhadas que podem ser partilhadas entre aplicações e módulos.</span><span class="sxs-lookup"><span data-stu-id="5dee1-109">Within that grouping, there is a set of shared categories that can be shared across applications and modules.</span></span> <span data-ttu-id="5dee1-110">Entrando ainda mais nos detalhes, as categorias de projetos são o nível mais granular das categorias.</span><span class="sxs-lookup"><span data-stu-id="5dee1-110">Getting even further into specifics, project categories are the most granular level of categories.</span></span> <span data-ttu-id="5dee1-111">As categorias de projetos são específicas da entidade jurídica, do módulo e da aplicação.</span><span class="sxs-lookup"><span data-stu-id="5dee1-111">Project categories are specific to legal entity, module, and application.</span></span>

![Correlação entre categorias de transações, categorias partilhadas e categorias de projetos](media/project-categories.png)

## <a name="transaction-categories"></a><span data-ttu-id="5dee1-113">Categorias de transações</span><span class="sxs-lookup"><span data-stu-id="5dee1-113">Transaction categories</span></span>

<span data-ttu-id="5dee1-114">As categorias de transações representam o agrupamento básico para as transações de projetos e não são específicas da empresa ou do tipo de transação.</span><span class="sxs-lookup"><span data-stu-id="5dee1-114">Transaction categories represent the basic grouping for project transactions and are not company or transaction type-specific.</span></span> <span data-ttu-id="5dee1-115">Por exemplo, a Contoso Robotics utiliza as categorias Design, Viagem, Instalação e Transação de Serviços para agrupar as Transações do projeto.</span><span class="sxs-lookup"><span data-stu-id="5dee1-115">For example, Contoso Robotics uses Design, Travel, Installation, and Service Transaction categories to group Project transactions.</span></span>

<span data-ttu-id="5dee1-116">As categorias de transações são definidas no módulo Project Operations.</span><span class="sxs-lookup"><span data-stu-id="5dee1-116">Transaction categories are defined in the Project Operations module.</span></span> 
1. <span data-ttu-id="5dee1-117">Vá para **Definições** \> **Categorias de Transação** para abrir o formulário.</span><span class="sxs-lookup"><span data-stu-id="5dee1-117">Go to **Settings** \> **Transaction Categories** to open the form.</span></span> 
2. <span data-ttu-id="5dee1-118">Crie uma nova categoria de transação ao selecionar **Novo** ou ao selecionar **Importar do Excel**.</span><span class="sxs-lookup"><span data-stu-id="5dee1-118">Create a new transaction category either by selecting **New** or by selecting **Import from Excel**.</span></span>

## <a name="shared-categories"></a><span data-ttu-id="5dee1-119">Categorias partilhadas</span><span class="sxs-lookup"><span data-stu-id="5dee1-119">Shared categories</span></span>

<span data-ttu-id="5dee1-120">O Dynamics 365 utiliza o conceito de Categorias partilhadas para categorizar as despesas em diferentes aplicações, como o Dynamics 365 Finance, Dynamics 365 Supply Chain e Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="5dee1-120">Dynamics 365 uses the Shared categories concept to categorize expenses in different applications, such as Dynamics 365 Finance, Dynamics 365 Supply Chain, and Dynamics 365 Project Operations.</span></span> <span data-ttu-id="5dee1-121">Para cada Categoria de transação criada, o Project Operations cria automaticamente quatro Categorias partilhadas relacionadas: Horas, Despesa, Taxas e Item.</span><span class="sxs-lookup"><span data-stu-id="5dee1-121">For each Transaction category created, Project Operations automatically creates four related Shared categories: Hours, Expense, Fees, and Item.</span></span> <span data-ttu-id="5dee1-122">Pode rever e ajustar as categorias partilhadas em **Gestão de projetos e contabilística** \> **Configurar** \> **Categorias** \> **Categorias Partilhadas**.</span><span class="sxs-lookup"><span data-stu-id="5dee1-122">You can review and adjust the shared categories by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Shared Categories**.</span></span>

## <a name="project-categories"></a><span data-ttu-id="5dee1-123">Categorias do projeto</span><span class="sxs-lookup"><span data-stu-id="5dee1-123">Project categories</span></span>

<span data-ttu-id="5dee1-124">As categorias de projetos representam o nível mais granular de configuração de categorias e têm de ser configuradas separadamente, e para cada empresa, por um Contabilista de projetos.</span><span class="sxs-lookup"><span data-stu-id="5dee1-124">Project categories represent most granular level of category configuration and must be configured separately, and for each company, by a Project accountant.</span></span>

1. <span data-ttu-id="5dee1-125">Vá para **Gestão de projetos e contabilística** \> **Configurar** \> **Categorias** \> **Categorias do projeto**.</span><span class="sxs-lookup"><span data-stu-id="5dee1-125">Go to **Project Management and Accounting** \> **Setup** \> **Categories** \> **Project categories**.</span></span>
2. <span data-ttu-id="5dee1-126">Selecione **Novo**.</span><span class="sxs-lookup"><span data-stu-id="5dee1-126">Select **New**.</span></span>
3. <span data-ttu-id="5dee1-127">Selecione o **ID da Categoria** da Categoria partilhada que criou na secção anterior.</span><span class="sxs-lookup"><span data-stu-id="5dee1-127">Select the **Category ID** of the Shared category you created in the previous section.</span></span> <span data-ttu-id="5dee1-128">O Project Operations permite utilizar apenas as categorias partilhadas que estão associadas às categorias de transações.</span><span class="sxs-lookup"><span data-stu-id="5dee1-128">Project Operations allows using only those shared categories that are associated with transaction categories.</span></span>
4. <span data-ttu-id="5dee1-129">Selecione um grupo de categorias.</span><span class="sxs-lookup"><span data-stu-id="5dee1-129">Select a category group.</span></span>

## <a name="category-groups"></a><span data-ttu-id="5dee1-130">Grupos de categorias</span><span class="sxs-lookup"><span data-stu-id="5dee1-130">Category groups</span></span>

<span data-ttu-id="5dee1-131">Os grupos de categorias são utilizados para partilhar as propriedades, principalmente perfis de lançamento, entre Categorias de projetos relacionadas.</span><span class="sxs-lookup"><span data-stu-id="5dee1-131">Category groups are used to share properties, primarily posting profiles, between related Project categories.</span></span> <span data-ttu-id="5dee1-132">Tem de haver pelo menos um grupo de categorias para cada tipo de transação e cada categoria de projeto é atribuída a um grupo.</span><span class="sxs-lookup"><span data-stu-id="5dee1-132">There must be at least one category group for each transaction type and each project category is assigned a group.</span></span>

<span data-ttu-id="5dee1-133">As especificações de lançamento no Project Operations são definidas pelas regras do perfil de custos e receitas, pelas categorias de projetos e pelos grupos de categorias.</span><span class="sxs-lookup"><span data-stu-id="5dee1-133">The posting specifications in Project Operations are defined by the project cost and revenue profile rules, project categories, and category groups.</span></span> <span data-ttu-id="5dee1-134">Pode configurar grupos de categorias em **Gestão de projetos e contabilística** \> **Configurar** \> **Categorias** \> **Grupos de categorias**.</span><span class="sxs-lookup"><span data-stu-id="5dee1-134">You can set up category groups by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Category groups**.</span></span>
