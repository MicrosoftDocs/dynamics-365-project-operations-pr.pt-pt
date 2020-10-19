---
title: Atualizar um projeto
description: Este tópico fornece informações sobre como atualizar projetos no Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 5c9cd0c7c6886bd454c5f2ef2ae7f20d1707293f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897826"
---
# <a name="update-a-project"></a><span data-ttu-id="5fed6-103">Atualizar um projeto</span><span class="sxs-lookup"><span data-stu-id="5fed6-103">Update a project</span></span>

<span data-ttu-id="5fed6-104">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="5fed6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5fed6-105">Abaixo é apresentado um resumo dos campos que podem ser atualizados num projeto depois de ser criado e quaisquer implicações aplicáveis das atualizações.</span><span class="sxs-lookup"><span data-stu-id="5fed6-105">Below is a summary of the fields that can be updated on a project after it has been created and any applicable implications of the updates.</span></span>

## <a name="project-detail-fields"></a><span data-ttu-id="5fed6-106">Campos de detalhe do projeto</span><span class="sxs-lookup"><span data-stu-id="5fed6-106">Project detail fields</span></span>

- <span data-ttu-id="5fed6-107">**Nome**: o título do projeto.</span><span class="sxs-lookup"><span data-stu-id="5fed6-107">**Name**: The title of the project.</span></span>
- <span data-ttu-id="5fed6-108">**Descrição**: uma descrição geral do projeto.</span><span class="sxs-lookup"><span data-stu-id="5fed6-108">**Description**: An overview of the project.</span></span>
- <span data-ttu-id="5fed6-109">**Cliente**: a empresa à qual o projeto será entregue.</span><span class="sxs-lookup"><span data-stu-id="5fed6-109">**Customer**: The company the project will be delivered to.</span></span>
- <span data-ttu-id="5fed6-110">**Modelo de calendário**: o horário de trabalho do projeto.</span><span class="sxs-lookup"><span data-stu-id="5fed6-110">**Calendar template**: The working hours of the project.</span></span> <span data-ttu-id="5fed6-111">Quando o campo é alterado, toda a agenda é recalculada.</span><span class="sxs-lookup"><span data-stu-id="5fed6-111">When the field is changed, the entire schedule is recalculated.</span></span>
- <span data-ttu-id="5fed6-112">**Moeda**: a moeda para o projeto.</span><span class="sxs-lookup"><span data-stu-id="5fed6-112">**Currency**: The currency for the project.</span></span> <span data-ttu-id="5fed6-113">Este campo assume por predefinição a moeda definida na unidade de contratação.</span><span class="sxs-lookup"><span data-stu-id="5fed6-113">This field defaults based on the currency defined in the contracting unit.</span></span> <span data-ttu-id="5fed6-114">Quando a unidade de contratação é atualizada, o campo também é atualizado.</span><span class="sxs-lookup"><span data-stu-id="5fed6-114">When the contracting unit is updated, the field is also updated.</span></span>
- <span data-ttu-id="5fed6-115">**Unidade de Contratação**: a unidade organizacional que representa o grupo ou a divisão da empresa, responsável principalmente pela vitória da venda e gestão da entrega de trabalho e serviços ao cliente.</span><span class="sxs-lookup"><span data-stu-id="5fed6-115">**Contracting Unit**: The organizational unit that represents the company group or division that is primarily responsible for winning the sale and managing the delivery of work and services to the customer.</span></span> 
- <span data-ttu-id="5fed6-116">**Gestor de Projeto**: o membro da equipa do projeto que tem autoridade para rever e aprovar entradas de tempo e despesas.</span><span class="sxs-lookup"><span data-stu-id="5fed6-116">**Project Manager**: The project team member who has the authority to review and approve time entries and expenses.</span></span>

## <a name="estimate-fields"></a><span data-ttu-id="5fed6-117">Campos de estimativa</span><span class="sxs-lookup"><span data-stu-id="5fed6-117">Estimate fields</span></span>

- <span data-ttu-id="5fed6-118">**Data de Início Estimada**: a data em que o projeto começará.</span><span class="sxs-lookup"><span data-stu-id="5fed6-118">**Estimated Start Date**: The date that the project will begin.</span></span> <span data-ttu-id="5fed6-119">Quando este campo for atualizado, quaisquer tarefas no projeto serão movidas proporcionalmente com a nova data de início.</span><span class="sxs-lookup"><span data-stu-id="5fed6-119">When this field is updated, any tasks on the project will move proportionately with the start new start date.</span></span>
- <span data-ttu-id="5fed6-120">**Data de Fim**: a data agendada para o final do projeto.</span><span class="sxs-lookup"><span data-stu-id="5fed6-120">**Finish Date**: The date that the project is scheduled to end.</span></span>
- <span data-ttu-id="5fed6-121">**Esforço**: o esforço estimado do projeto.</span><span class="sxs-lookup"><span data-stu-id="5fed6-121">**Effort**: The estimated effort of the project.</span></span> <span data-ttu-id="5fed6-122">Quando as tarefas são adicionadas ao projeto, este campo já não é editável.</span><span class="sxs-lookup"><span data-stu-id="5fed6-122">When tasks are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="5fed6-123">**Custo Estimado da Mão de Obra**: o custo da mão de obra estimado do projeto.</span><span class="sxs-lookup"><span data-stu-id="5fed6-123">**Estimated Labor Cost**: The estimated labor cost of the project.</span></span> <span data-ttu-id="5fed6-124">Quando os custos de mão de obra são adicionados ao projeto, este campo já não é editável.</span><span class="sxs-lookup"><span data-stu-id="5fed6-124">When labor costs are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="5fed6-125">**Despesas Estimadas**: as despesas estimadas do projeto.</span><span class="sxs-lookup"><span data-stu-id="5fed6-125">**Estimated Expenses**: The estimated expenses of the project.</span></span> <span data-ttu-id="5fed6-126">Quando as despesas são adicionadas ao projeto, este campo já não é editável.</span><span class="sxs-lookup"><span data-stu-id="5fed6-126">When expenses are added to the project, this field is no longer editable.</span></span>

## <a name="project-actual-fields"></a><span data-ttu-id="5fed6-127">Campos reais do projeto</span><span class="sxs-lookup"><span data-stu-id="5fed6-127">Project actual fields</span></span>
- <span data-ttu-id="5fed6-128">**Início Real**: a data em que o projeto começou.</span><span class="sxs-lookup"><span data-stu-id="5fed6-128">**Actual Start**: The date that the project started.</span></span>
- <span data-ttu-id="5fed6-129">**Fim Real**: para ser atualizado quando um projeto for concluído.</span><span class="sxs-lookup"><span data-stu-id="5fed6-129">**Actual Finish**: To be updated when a project has been completed.</span></span>

## <a name="project-status-fields"></a><span data-ttu-id="5fed6-130">Campos de estado do projeto</span><span class="sxs-lookup"><span data-stu-id="5fed6-130">Project status fields</span></span>

- <span data-ttu-id="5fed6-131">**Estado Geral do Projeto**: o estado global do projeto fornecido pelo Gestor de projeto.</span><span class="sxs-lookup"><span data-stu-id="5fed6-131">**Overall Project Status**: The overall project health provided by the Project manager.</span></span>
- <span data-ttu-id="5fed6-132">**Comentários**: uma narrativa sobre o estado atual do projeto fornecido pelo Gestor de projeto.</span><span class="sxs-lookup"><span data-stu-id="5fed6-132">**Comments**: A narrative regarding the current health of the project provided by the Project manager.</span></span>

