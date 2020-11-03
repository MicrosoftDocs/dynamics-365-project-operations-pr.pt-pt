---
title: Determinar o tipo de implementação
description: Este tópico fornece informações que o vão ajudar a determinar o tipo de implementação correto do Project Operations para a sua empresa.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 564f2878553fe3904a7c47c7e80a3b57c763a3b2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082408"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="44814-103">Determinar o tipo de implementação</span><span class="sxs-lookup"><span data-stu-id="44814-103">Determine your deployment type</span></span>

<span data-ttu-id="44814-104">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="44814-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="44814-105">Depois de adquirir a licença, comece aqui para determinar o melhor modelo de implementação do Dynamics 365 Project Operations através do [Fluxo de instalação guiado](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="44814-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="44814-106">Depois de concluir o Fluxo de instalação guiado, será direcionado para o portal de gestão correto para concluir a sua instalação.</span><span class="sxs-lookup"><span data-stu-id="44814-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="44814-107">Consulte os detalhes da implementação para concluir a instalação.</span><span class="sxs-lookup"><span data-stu-id="44814-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="44814-108">Clientes existentes do Dynamics que utilizam o Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="44814-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="44814-109">O Project Operations inclui as capacidades que foram enviadas com o Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="44814-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="44814-110">Será lançado um caminho de atualização para estes clientes no futuro.</span><span class="sxs-lookup"><span data-stu-id="44814-110">An upgrade path will be released for these customers in the future.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="44814-111">Clientes existentes do Dynamics 365 Finance que utilizam a Gestão de projetos e contabilística</span><span class="sxs-lookup"><span data-stu-id="44814-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="44814-112">Os clientes existentes do Finance que utilizam a funcionalidade Gestão de projetos e contabilística podem continuar a utilizá-lo tal como está.</span><span class="sxs-lookup"><span data-stu-id="44814-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use this as is.</span></span> <span data-ttu-id="44814-113">Consulte [Project Operations para cenários de encomenda em stock/de produção](#pma).</span><span class="sxs-lookup"><span data-stu-id="44814-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-types"></a><span data-ttu-id="44814-114">Tipo de implementação</span><span class="sxs-lookup"><span data-stu-id="44814-114">Deployment types</span></span>
<span data-ttu-id="44814-115">O Project Operations suporta várias opções de implementação à medida dos seus requisitos.</span><span class="sxs-lookup"><span data-stu-id="44814-115">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="44814-116">Quer seja um cliente novo ou existente do Dynamics 365, o Project Operations suporta as suas necessidades.</span><span class="sxs-lookup"><span data-stu-id="44814-116">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="44814-117">O nosso [Questionário de implementação](https://aka.ms/provisionprojectoperations) ajudará a determinar a implementação certa.</span><span class="sxs-lookup"><span data-stu-id="44814-117">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="44814-118">Os resultados vão guiá-lo para um dos seguintes tipos de implementação:</span><span class="sxs-lookup"><span data-stu-id="44814-118">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="44814-119">Implementação leve - oportunidade potencial para fatura pró-forma</span><span class="sxs-lookup"><span data-stu-id="44814-119">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="44814-120">Project Operations para cenários baseados em recursos/não em stock</span><span class="sxs-lookup"><span data-stu-id="44814-120">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="44814-121">Project Operations para cenários de encomenda em stock/de produção</span><span class="sxs-lookup"><span data-stu-id="44814-121">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="44814-122">O Project Operations suporta cenários de encomenda em stock/de produção e cenários não armazenados/baseados em recursos no mesmo ambiente através de configurações a nível da entidade jurídica.</span><span class="sxs-lookup"><span data-stu-id="44814-122">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="44814-123">Por exemplo, a Contoso pode utilizar as capacidades de encomenda de abastecimento/produção nas suas instalações de fabrico dos EUA (Entidade legal = Contoso Manufacturing United States).</span><span class="sxs-lookup"><span data-stu-id="44814-123">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="44814-124">A Contoso pode utilizar as capacidades de não abastecimento/baseadas em recursos nas suas instalações de manutenção da Contoso Robotics Arms no Reino Unido (Entidade legal = Contoso Robotics United Kingdom).</span><span class="sxs-lookup"><span data-stu-id="44814-124">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="44814-125">Implementação leve - oportunidade potencial para fatura pró-forma</span><span class="sxs-lookup"><span data-stu-id="44814-125">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="44814-126">A implementação leve inclui as seguintes capacidades:</span><span class="sxs-lookup"><span data-stu-id="44814-126">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="44814-127">Planeamento de projetos com o Microsoft Project para a Web</span><span class="sxs-lookup"><span data-stu-id="44814-127">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="44814-128">Preços multidimensionais</span><span class="sxs-lookup"><span data-stu-id="44814-128">Multi-dimensional pricing</span></span>
- <span data-ttu-id="44814-129">Gestão de Recursos Unificados</span><span class="sxs-lookup"><span data-stu-id="44814-129">Unified Resource Management</span></span>
- <span data-ttu-id="44814-130">Monitorização do Tempo</span><span class="sxs-lookup"><span data-stu-id="44814-130">Time Tracking</span></span>
- <span data-ttu-id="44814-131">Despesas Básicas</span><span class="sxs-lookup"><span data-stu-id="44814-131">Basic Expense</span></span>
- <span data-ttu-id="44814-132">Proposta de Fatura</span><span class="sxs-lookup"><span data-stu-id="44814-132">Invoice Proposal</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="44814-133">Passos de implementação</span><span class="sxs-lookup"><span data-stu-id="44814-133">Deployment steps</span></span>
<span data-ttu-id="44814-134">Determine o melhor modelo de implementação do Project Operations através do [Questionário de implementação](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="44814-134">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="44814-135">Para esta implementação, consulte [Inscrever-se em subscrições de pré-visualização](lite-preview-subscription-sign-up.md) e [Aprovisionar novo ambiente](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="44814-135">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="44814-136">Project Operations para cenários baseados em recursos/não em stock</span><span class="sxs-lookup"><span data-stu-id="44814-136">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="44814-137">O Project Operations para cenários baseados em recursos/não em stock incluem as seguintes capacidades:</span><span class="sxs-lookup"><span data-stu-id="44814-137">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
  
- <span data-ttu-id="44814-138">Planeamento de projetos com o Microsoft Project para a Web</span><span class="sxs-lookup"><span data-stu-id="44814-138">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="44814-139">Preços multidimensionais</span><span class="sxs-lookup"><span data-stu-id="44814-139">Multi-dimensional pricing</span></span>
- <span data-ttu-id="44814-140">Gestão de Recursos Unificados</span><span class="sxs-lookup"><span data-stu-id="44814-140">Unified Resource Management</span></span>
- <span data-ttu-id="44814-141">Monitorização do Tempo</span><span class="sxs-lookup"><span data-stu-id="44814-141">Time Tracking</span></span>
- <span data-ttu-id="44814-142">Despesas Básicas</span><span class="sxs-lookup"><span data-stu-id="44814-142">Basic Expense</span></span>
- <span data-ttu-id="44814-143">Despesa Total</span><span class="sxs-lookup"><span data-stu-id="44814-143">Full Expense</span></span>
- <span data-ttu-id="44814-144">OCR de recibos</span><span class="sxs-lookup"><span data-stu-id="44814-144">Receipt OCR</span></span>
- <span data-ttu-id="44814-145">Faturação Completa</span><span class="sxs-lookup"><span data-stu-id="44814-145">Full Invoicing</span></span>
- <span data-ttu-id="44814-146">Reconhecimento de Receitas</span><span class="sxs-lookup"><span data-stu-id="44814-146">Revenue Recognition</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="44814-147">Passos de implementação</span><span class="sxs-lookup"><span data-stu-id="44814-147">Deployment steps</span></span>
<span data-ttu-id="44814-148">Determine o melhor modelo de implementação do Project Operations através do [Questionário de implementação](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="44814-148">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="44814-149">Para esta implementação, consulte [Inscrever-se em subscrições de pré-visualização](resource-sign-up-preview-subscription.md) e [Aprovisionar novo ambiente](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="44814-149">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="44814-150">Project Operations para cenários de encomenda em stock/de produção</span><span class="sxs-lookup"><span data-stu-id="44814-150">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="44814-151">Planeamento de projetos com WBS</span><span class="sxs-lookup"><span data-stu-id="44814-151">Project planning using WBS</span></span>
- <span data-ttu-id="44814-152">Gestão de Recursos</span><span class="sxs-lookup"><span data-stu-id="44814-152">Resource Management</span></span>
- <span data-ttu-id="44814-153">Monitorização do Tempo</span><span class="sxs-lookup"><span data-stu-id="44814-153">Time Tracking</span></span>
- <span data-ttu-id="44814-154">Despesa Total</span><span class="sxs-lookup"><span data-stu-id="44814-154">Full Expense</span></span>
- <span data-ttu-id="44814-155">OCR de recibos</span><span class="sxs-lookup"><span data-stu-id="44814-155">Receipt OCR</span></span>
- <span data-ttu-id="44814-156">Faturação Completa</span><span class="sxs-lookup"><span data-stu-id="44814-156">Full Invoicing</span></span>
- <span data-ttu-id="44814-157">Reconhecimento de Receitas</span><span class="sxs-lookup"><span data-stu-id="44814-157">Revenue Recognition</span></span>
- <span data-ttu-id="44814-158">Ordens de Produção</span><span class="sxs-lookup"><span data-stu-id="44814-158">Production Orders</span></span>
- <span data-ttu-id="44814-159">Suporte para materiais</span><span class="sxs-lookup"><span data-stu-id="44814-159">Materials support</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="44814-160">Passos de implementação</span><span class="sxs-lookup"><span data-stu-id="44814-160">Deployment steps</span></span>
<span data-ttu-id="44814-161">Determine o melhor modelo de implementação do Project Operations através do [Questionário de implementação](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="44814-161">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="44814-162">Para esta implementação, consulte [Inscrever-se em subscrições de pré-visualização](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) e [Aprovisionar novo ambiente](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="44814-162">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 

