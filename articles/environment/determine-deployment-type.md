---
title: Tipo de implementação
description: Este tópico fornece informações que o vão ajudar a determinar o tipo de implementação correto do Project Operations para a sua empresa.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: c3cf378caae4510482a8ee6771bf2e6decfe3b48
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949018"
---
# <a name="deployment-types"></a><span data-ttu-id="bbee3-103">Tipo de implementação</span><span class="sxs-lookup"><span data-stu-id="bbee3-103">Deployment types</span></span>

<span data-ttu-id="bbee3-104">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="bbee3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bbee3-105">Depois de adquirir a licença, comece aqui para determinar o melhor modelo de implementação do Dynamics 365 Project Operations através do [Fluxo de instalação guiado](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="bbee3-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="bbee3-106">Depois de concluir o Fluxo de instalação guiado, será direcionado para o portal de gestão correto para concluir a sua instalação.</span><span class="sxs-lookup"><span data-stu-id="bbee3-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="bbee3-107">Consulte os detalhes da implementação abaixo para concluir a instalação.</span><span class="sxs-lookup"><span data-stu-id="bbee3-107">See the deployment details below to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="bbee3-108">Clientes existentes do Dynamics que utilizam o Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="bbee3-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="bbee3-109">O Project Operations inclui as capacidades que foram enviadas com o Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="bbee3-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="bbee3-110">Será lançado um caminho de atualização para estes clientes no futuro.</span><span class="sxs-lookup"><span data-stu-id="bbee3-110">An upgrade path will be released for these customers in the future.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="bbee3-111">Clientes existentes do Dynamics 365 Finance que utilizam a Gestão de projetos e contabilística</span><span class="sxs-lookup"><span data-stu-id="bbee3-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="bbee3-112">Os clientes existentes do Finance que utilizam a funcionalidade Gestão de projetos e contabilística podem continuar a utilizá-lo tal como está.</span><span class="sxs-lookup"><span data-stu-id="bbee3-112">Existing customers of Finance who use the Project management and accounting functionality can continue use this as is.</span></span> <span data-ttu-id="bbee3-113">Consulte [Project Operations para cenários de encomenda em stock/de produção](#pma).</span><span class="sxs-lookup"><span data-stu-id="bbee3-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>

<span data-ttu-id="bbee3-114">O Project Operations suporta várias opções de implementação à medida dos seus requisitos.</span><span class="sxs-lookup"><span data-stu-id="bbee3-114">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="bbee3-115">Quer seja um cliente novo ou existente do Dynamics 365, o Project Operations suporta as suas necessidades.</span><span class="sxs-lookup"><span data-stu-id="bbee3-115">Whether you are a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="bbee3-116">O nosso [Questionário de implementação](https://aka.ms/provisionprojectoperations) ajudará a determinar a implementação certa.</span><span class="sxs-lookup"><span data-stu-id="bbee3-116">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="bbee3-117">Os resultados vão guiá-lo para um dos seguintes tipos de implementação:</span><span class="sxs-lookup"><span data-stu-id="bbee3-117">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="bbee3-118">Implementação leve - oportunidade potencial para fatura pró-forma</span><span class="sxs-lookup"><span data-stu-id="bbee3-118">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="bbee3-119">Project Operations para cenários baseados em recursos/não em stock</span><span class="sxs-lookup"><span data-stu-id="bbee3-119">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="bbee3-120">Project Operations para cenários de encomenda em stock/de produção</span><span class="sxs-lookup"><span data-stu-id="bbee3-120">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="bbee3-121">O Project Operations suporta cenários de encomenda em stock/de produção e cenários não armazenados/baseados em recursos no mesmo ambiente através de configurações a nível da entidade jurídica.</span><span class="sxs-lookup"><span data-stu-id="bbee3-121">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="bbee3-122">Por exemplo, a Contoso pode tirar partido das capacidades de encomenda em stock/de produção nas suas instalações de produção nos E.U.A. (Entidade legal = Contoso Manufacturing United States) e capacidades não armazenadas/baseadas em recursos nas instalações de serviços da Contoso Robotics Arms no Reino Unido (Entidade legal = Contoso Robotics United Kingdom).</span><span class="sxs-lookup"><span data-stu-id="bbee3-122">For example, Contoso can leverage stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States) and non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

## <a name="a-namelitelite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="bbee3-123"><a name="lite"><a/>Implementação leve - oportunidade potencial para fatura pró-forma</span><span class="sxs-lookup"><span data-stu-id="bbee3-123"><a name="lite"><a/>Lite deployment - deal to proforma invoicing</span></span>
<span data-ttu-id="bbee3-124">A implementação leve inclui as seguintes capacidades:</span><span class="sxs-lookup"><span data-stu-id="bbee3-124">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="bbee3-125">Planeamento de projetos com o Microsoft Project para a Web</span><span class="sxs-lookup"><span data-stu-id="bbee3-125">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="bbee3-126">Preços multidimensionais</span><span class="sxs-lookup"><span data-stu-id="bbee3-126">Multi-dimensional pricing</span></span>
- <span data-ttu-id="bbee3-127">Gestão de Recursos Unificados</span><span class="sxs-lookup"><span data-stu-id="bbee3-127">Unified Resource Management</span></span>
- <span data-ttu-id="bbee3-128">Monitorização do Tempo</span><span class="sxs-lookup"><span data-stu-id="bbee3-128">Time Tracking</span></span>
- <span data-ttu-id="bbee3-129">Despesas Básicas</span><span class="sxs-lookup"><span data-stu-id="bbee3-129">Basic Expense</span></span>
- <span data-ttu-id="bbee3-130">Proposta de Fatura</span><span class="sxs-lookup"><span data-stu-id="bbee3-130">Invoice Proposal</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="bbee3-131">Passos de implementação:</span><span class="sxs-lookup"><span data-stu-id="bbee3-131">Deployment steps:</span></span>
<span data-ttu-id="bbee3-132">Determine o melhor modelo de implementação do Project Operations através do [Questionário de implementação](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="bbee3-132">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="bbee3-133">Para esta implementação, consulte [Inscrever-se em subscrições de pré-visualização](lite-preview-subscription-sign-up.md) e [Aprovisionar novo ambiente](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="bbee3-133">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


## <a name="a-nameintegratedproject-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="bbee3-134"><a name="integrated"><a/>Project Operations para cenários baseados em recursos/não em stock</span><span class="sxs-lookup"><span data-stu-id="bbee3-134"><a name="integrated"><a/>Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="bbee3-135">O Project Operations para cenários baseados em recursos/não em stock incluem as seguintes capacidades:</span><span class="sxs-lookup"><span data-stu-id="bbee3-135">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
  
- <span data-ttu-id="bbee3-136">Planeamento de projetos com o Microsoft Project para a Web</span><span class="sxs-lookup"><span data-stu-id="bbee3-136">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="bbee3-137">Preços multidimensionais</span><span class="sxs-lookup"><span data-stu-id="bbee3-137">Multi-dimensional pricing</span></span>
- <span data-ttu-id="bbee3-138">Gestão de Recursos Unificados</span><span class="sxs-lookup"><span data-stu-id="bbee3-138">Unified Resource Management</span></span>
- <span data-ttu-id="bbee3-139">Monitorização do Tempo</span><span class="sxs-lookup"><span data-stu-id="bbee3-139">Time Tracking</span></span>
- <span data-ttu-id="bbee3-140">Despesas Básicas</span><span class="sxs-lookup"><span data-stu-id="bbee3-140">Basic Expense</span></span>
- <span data-ttu-id="bbee3-141">Despesa Total</span><span class="sxs-lookup"><span data-stu-id="bbee3-141">Full Expense</span></span>
- <span data-ttu-id="bbee3-142">OCR de recibos</span><span class="sxs-lookup"><span data-stu-id="bbee3-142">Receipt OCR</span></span>
- <span data-ttu-id="bbee3-143">Faturação Completa</span><span class="sxs-lookup"><span data-stu-id="bbee3-143">Full Invoicing</span></span>
- <span data-ttu-id="bbee3-144">Reconhecimento de Receitas</span><span class="sxs-lookup"><span data-stu-id="bbee3-144">Revenue Recognition</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="bbee3-145">Passos de implementação:</span><span class="sxs-lookup"><span data-stu-id="bbee3-145">Deployment steps:</span></span>
<span data-ttu-id="bbee3-146">Determine o melhor modelo de implementação do Project Operations através do [Questionário de implementação](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="bbee3-146">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="bbee3-147">Para esta implementação, consulte [Inscrever-se em subscrições de pré-visualização](resource-sign-up-preview-subscription.md) e [Aprovisionar novo ambiente](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="bbee3-147">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


## <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="bbee3-148">Project Operations para cenários de encomenda em stock/de produção</span><span class="sxs-lookup"><span data-stu-id="bbee3-148">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="bbee3-149">Planeamento de projetos com WBS</span><span class="sxs-lookup"><span data-stu-id="bbee3-149">Project planning using WBS</span></span>
- <span data-ttu-id="bbee3-150">Gestão de Recursos</span><span class="sxs-lookup"><span data-stu-id="bbee3-150">Resource Management</span></span>
- <span data-ttu-id="bbee3-151">Monitorização do Tempo</span><span class="sxs-lookup"><span data-stu-id="bbee3-151">Time Tracking</span></span>
- <span data-ttu-id="bbee3-152">Despesa Total</span><span class="sxs-lookup"><span data-stu-id="bbee3-152">Full Expense</span></span>
- <span data-ttu-id="bbee3-153">OCR de recibos</span><span class="sxs-lookup"><span data-stu-id="bbee3-153">Receipt OCR</span></span>
- <span data-ttu-id="bbee3-154">Faturação Completa</span><span class="sxs-lookup"><span data-stu-id="bbee3-154">Full Invoicing</span></span>
- <span data-ttu-id="bbee3-155">Reconhecimento de Receitas</span><span class="sxs-lookup"><span data-stu-id="bbee3-155">Revenue Recognition</span></span>
- <span data-ttu-id="bbee3-156">Ordens de Produção</span><span class="sxs-lookup"><span data-stu-id="bbee3-156">Production Orders</span></span>
- <span data-ttu-id="bbee3-157">Suporte para materiais</span><span class="sxs-lookup"><span data-stu-id="bbee3-157">Materials support</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="bbee3-158">Passos de implementação:</span><span class="sxs-lookup"><span data-stu-id="bbee3-158">Deployment steps:</span></span>
<span data-ttu-id="bbee3-159">Determine o melhor modelo de implementação do Project Operations através do [Questionário de implementação](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="bbee3-159">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="bbee3-160">Para esta implementação, consulte [Inscrever-se em subscrições de pré-visualização](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) e [Aprovisionar novo ambiente](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="bbee3-160">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 



