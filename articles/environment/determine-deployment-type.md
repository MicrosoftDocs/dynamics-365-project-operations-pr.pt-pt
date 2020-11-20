---
title: Determinar o tipo de implementação
description: Este tópico fornece informações que o vão ajudar a determinar o tipo de implementação correto do Project Operations para a sua empresa.
author: stsporen
manager: Annbe
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: e9d3a5d8e6e1daafac72a3b4c0380b679d1869bd
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401232"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="b3a63-103">Determinar o tipo de implementação</span><span class="sxs-lookup"><span data-stu-id="b3a63-103">Determine your deployment type</span></span>

<span data-ttu-id="b3a63-104">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="b3a63-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b3a63-105">Depois de adquirir a licença, comece aqui para determinar o melhor modelo de implementação do Dynamics 365 Project Operations através do [Fluxo de instalação guiado](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="b3a63-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="b3a63-106">Depois de concluir o Fluxo de instalação guiado, será direcionado para o portal de gestão correto para concluir a sua instalação.</span><span class="sxs-lookup"><span data-stu-id="b3a63-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="b3a63-107">Consulte os detalhes da implementação para concluir a instalação.</span><span class="sxs-lookup"><span data-stu-id="b3a63-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="b3a63-108">Clientes existentes do Dynamics que utilizam o Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="b3a63-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="b3a63-109">O Project Operations inclui as capacidades que foram enviadas com o Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="b3a63-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="b3a63-110">Será lançada um percurso de atualização de versão para estes clientes na vaga 1 da versão de 2021.</span><span class="sxs-lookup"><span data-stu-id="b3a63-110">An upgrade path will be released for these customers in the 2021 release wave 1.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="b3a63-111">Clientes existentes do Dynamics 365 Finance que utilizam a Gestão de projetos e contabilística</span><span class="sxs-lookup"><span data-stu-id="b3a63-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="b3a63-112">Os clientes existentes d Finance que utilizam a funcionalidade de Gestão e contabilidade de projetos podem continuar a usá-lo como está.</span><span class="sxs-lookup"><span data-stu-id="b3a63-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use it as is.</span></span> <span data-ttu-id="b3a63-113">Consulte [Project Operations para cenários de encomenda em stock/de produção](#pma).</span><span class="sxs-lookup"><span data-stu-id="b3a63-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-types"></a><span data-ttu-id="b3a63-114">Tipo de implementação</span><span class="sxs-lookup"><span data-stu-id="b3a63-114">Deployment types</span></span>
<span data-ttu-id="b3a63-115">O Project Operations suporta várias opções de implementação à medida dos seus requisitos.</span><span class="sxs-lookup"><span data-stu-id="b3a63-115">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="b3a63-116">Quer seja um cliente novo ou existente do Dynamics 365, o Project Operations suporta as suas necessidades.</span><span class="sxs-lookup"><span data-stu-id="b3a63-116">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="b3a63-117">O nosso [Questionário de implementação](https://aka.ms/provisionprojectoperations) ajudará a determinar a implementação certa.</span><span class="sxs-lookup"><span data-stu-id="b3a63-117">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="b3a63-118">Os resultados vão guiá-lo para um dos seguintes tipos de implementação:</span><span class="sxs-lookup"><span data-stu-id="b3a63-118">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="b3a63-119">Implementação leve - oportunidade potencial para fatura pró-forma</span><span class="sxs-lookup"><span data-stu-id="b3a63-119">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="b3a63-120">Project Operations para cenários baseados em recursos/não em stock</span><span class="sxs-lookup"><span data-stu-id="b3a63-120">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="b3a63-121">Project Operations para cenários de encomenda em stock/de produção</span><span class="sxs-lookup"><span data-stu-id="b3a63-121">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="b3a63-122">O Project Operations suporta cenários de encomenda em stock/de produção e cenários não armazenados/baseados em recursos no mesmo ambiente através de configurações a nível da entidade jurídica.</span><span class="sxs-lookup"><span data-stu-id="b3a63-122">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="b3a63-123">Por exemplo, a Contoso pode utilizar as capacidades de encomenda de abastecimento/produção nas suas instalações de fabrico dos EUA (Entidade legal = Contoso Manufacturing United States).</span><span class="sxs-lookup"><span data-stu-id="b3a63-123">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="b3a63-124">A Contoso pode utilizar as capacidades de não abastecimento/baseadas em recursos nas suas instalações de manutenção da Contoso Robotics Arms no Reino Unido (Entidade legal = Contoso Robotics United Kingdom).</span><span class="sxs-lookup"><span data-stu-id="b3a63-124">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="b3a63-125">Implementação leve - oportunidade potencial para fatura pró-forma</span><span class="sxs-lookup"><span data-stu-id="b3a63-125">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="b3a63-126">A implementação leve inclui as seguintes capacidades:</span><span class="sxs-lookup"><span data-stu-id="b3a63-126">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="b3a63-127">Processo de vendas para projetos que alarga experiências de aplicação do Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="b3a63-127">Sales process for projects that extends Dynamics 365 Sales application experiences</span></span>
- <span data-ttu-id="b3a63-128">Planeamento de projetos com o Microsoft Project para a Web</span><span class="sxs-lookup"><span data-stu-id="b3a63-128">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="b3a63-129">Preços multidimensionais</span><span class="sxs-lookup"><span data-stu-id="b3a63-129">Multi-dimensional pricing</span></span>
- <span data-ttu-id="b3a63-130">Gestão de recursos unificados</span><span class="sxs-lookup"><span data-stu-id="b3a63-130">Unified resource management</span></span>
- <span data-ttu-id="b3a63-131">Monitorização do tempo</span><span class="sxs-lookup"><span data-stu-id="b3a63-131">Time tracking</span></span>
- <span data-ttu-id="b3a63-132">Despesas básicas</span><span class="sxs-lookup"><span data-stu-id="b3a63-132">Basic expense</span></span>
- <span data-ttu-id="b3a63-133">Faturação pró-forma e virada para o cliente</span><span class="sxs-lookup"><span data-stu-id="b3a63-133">Proforma and customer-facing invoicing</span></span> 

#### <a name="deployment-steps"></a><span data-ttu-id="b3a63-134">Passos de implementação</span><span class="sxs-lookup"><span data-stu-id="b3a63-134">Deployment steps</span></span>
<span data-ttu-id="b3a63-135">Determine o melhor modelo de implementação do Project Operations através do [Questionário de implementação](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="b3a63-135">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="b3a63-136">Para esta implementação, consulte [Inscrever-se em subscrições de pré-visualização](lite-preview-subscription-sign-up.md) e [Aprovisionar novo ambiente](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="b3a63-136">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="b3a63-137">Project Operations para cenários baseados em recursos/não em stock</span><span class="sxs-lookup"><span data-stu-id="b3a63-137">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="b3a63-138">O Project Operations para cenários baseados em recursos/não em stock incluem as seguintes capacidades:</span><span class="sxs-lookup"><span data-stu-id="b3a63-138">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
 
- <span data-ttu-id="b3a63-139">Processo de vendas para projetos que alarga a aplicação do Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="b3a63-139">Sales process for projects that extends the Dynamics 365 Sales application</span></span>
- <span data-ttu-id="b3a63-140">Planeamento de projetos com o Microsoft Project para a Web</span><span class="sxs-lookup"><span data-stu-id="b3a63-140">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="b3a63-141">Preços multidimensionais</span><span class="sxs-lookup"><span data-stu-id="b3a63-141">Multi-dimensional pricing</span></span>
- <span data-ttu-id="b3a63-142">Gestão de recursos unificados</span><span class="sxs-lookup"><span data-stu-id="b3a63-142">Unified resource management</span></span>
- <span data-ttu-id="b3a63-143">Monitorização do tempo</span><span class="sxs-lookup"><span data-stu-id="b3a63-143">Time tracking</span></span>
- <span data-ttu-id="b3a63-144">Despesas básicas</span><span class="sxs-lookup"><span data-stu-id="b3a63-144">Basic expense</span></span>
- <span data-ttu-id="b3a63-145">Despesa total</span><span class="sxs-lookup"><span data-stu-id="b3a63-145">Full expense</span></span>
- <span data-ttu-id="b3a63-146">OCR de recibos</span><span class="sxs-lookup"><span data-stu-id="b3a63-146">Receipt OCR</span></span>
- <span data-ttu-id="b3a63-147">Faturação pró-forma e virada para o cliente</span><span class="sxs-lookup"><span data-stu-id="b3a63-147">Proforma and customer-facing invoicing</span></span> 
- <span data-ttu-id="b3a63-148">Reconhecimento de receitas para projetos</span><span class="sxs-lookup"><span data-stu-id="b3a63-148">Revenue recognition for projects</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="b3a63-149">Passos de implementação</span><span class="sxs-lookup"><span data-stu-id="b3a63-149">Deployment steps</span></span>
<span data-ttu-id="b3a63-150">Determine o melhor modelo de implementação do Project Operations através do [Questionário de implementação](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="b3a63-150">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="b3a63-151">Para esta implementação, consulte [Inscrever-se em subscrições de pré-visualização](resource-sign-up-preview-subscription.md) e [Aprovisionar novo ambiente](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="b3a63-151">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="b3a63-152">Project Operations para cenários de encomenda em stock/de produção</span><span class="sxs-lookup"><span data-stu-id="b3a63-152">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="b3a63-153">Planeamento de projetos com WBS</span><span class="sxs-lookup"><span data-stu-id="b3a63-153">Project planning using WBS</span></span>
- <span data-ttu-id="b3a63-154">Gestão de Recursos</span><span class="sxs-lookup"><span data-stu-id="b3a63-154">Resource Management</span></span>
- <span data-ttu-id="b3a63-155">Monitorização do Tempo</span><span class="sxs-lookup"><span data-stu-id="b3a63-155">Time Tracking</span></span>
- <span data-ttu-id="b3a63-156">Despesa Total</span><span class="sxs-lookup"><span data-stu-id="b3a63-156">Full Expense</span></span>
- <span data-ttu-id="b3a63-157">OCR de recibos</span><span class="sxs-lookup"><span data-stu-id="b3a63-157">Receipt OCR</span></span>
- <span data-ttu-id="b3a63-158">Faturação Completa</span><span class="sxs-lookup"><span data-stu-id="b3a63-158">Full Invoicing</span></span>
- <span data-ttu-id="b3a63-159">Reconhecimento de Receitas</span><span class="sxs-lookup"><span data-stu-id="b3a63-159">Revenue Recognition</span></span>
- <span data-ttu-id="b3a63-160">Ordens de Produção</span><span class="sxs-lookup"><span data-stu-id="b3a63-160">Production Orders</span></span>
- <span data-ttu-id="b3a63-161">Suporte para materiais</span><span class="sxs-lookup"><span data-stu-id="b3a63-161">Materials support</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="b3a63-162">Passos de implementação</span><span class="sxs-lookup"><span data-stu-id="b3a63-162">Deployment steps</span></span>
<span data-ttu-id="b3a63-163">Determine o melhor modelo de implementação do Project Operations através do [Questionário de implementação](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="b3a63-163">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="b3a63-164">Para esta implementação, consulte [Inscrever-se em subscrições de pré-visualização](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) e [Aprovisionar novo ambiente](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="b3a63-164">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 

