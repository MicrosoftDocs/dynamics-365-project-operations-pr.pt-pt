---
title: Descrição geral dos modos de gestão de recursos
description: Este tópico fornece informações sobre a funcionalidade de gestão de recursos no Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4d132bcbef5421202d2f4899091f0dc75166dd66
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949963"
---
# <a name="resource-management-modes-overview"></a><span data-ttu-id="73a1a-103">Descrição geral dos modos de gestão de recursos</span><span class="sxs-lookup"><span data-stu-id="73a1a-103">Resource management modes overview</span></span>

<span data-ttu-id="73a1a-104">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="73a1a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="73a1a-105">O Dynamics 365 Project Operations suporta dois modos para executar o fluxo de reserva global.</span><span class="sxs-lookup"><span data-stu-id="73a1a-105">Dynamics 365 Project Operations supports two modes in order for you to execute the overall booking flow.</span></span> <span data-ttu-id="73a1a-106">O modo de gestão é definido como um parâmetro de projeto e pode ser modificado se o seu negócio precisar de alteração.</span><span class="sxs-lookup"><span data-stu-id="73a1a-106">The mode of management is defined as a project parameter and can be modified if your business needs change.</span></span>    

## <a name="central-mode"></a><span data-ttu-id="73a1a-107">Modo central</span><span class="sxs-lookup"><span data-stu-id="73a1a-107">Central mode</span></span>
<span data-ttu-id="73a1a-108">Para as organizações que centralizam a alocação de recursos para projetos, o modo Central oferece uma forma de assegurar que os Gestores de projeto podem definir os requisitos de recursos a nível do projeto.</span><span class="sxs-lookup"><span data-stu-id="73a1a-108">For organizations who centralize the allocation for resources to projects, the Central mode provides a way to ensure Project managers can define resource requirements at the project level.</span></span> <span data-ttu-id="73a1a-109">A conclusão dos requisitos do recurso é delegada num Gestor de recursos.</span><span class="sxs-lookup"><span data-stu-id="73a1a-109">Fulfillment of the resource requirements is delegated to a Resource manager.</span></span> <span data-ttu-id="73a1a-110">Os gestores de projetos podem aceitar ou rejeitar recursos que são propostos pelo Gestor de recursos.</span><span class="sxs-lookup"><span data-stu-id="73a1a-110">Project managers can accept or reject resources that are proposed by the Resource manager.</span></span>

![Modo Central](./media/resource-management-central.png)

<span data-ttu-id="73a1a-112">Para gerir recursos com o modo Central, consulte:</span><span class="sxs-lookup"><span data-stu-id="73a1a-112">To manage resources with the Central mode, see:</span></span>

- [<span data-ttu-id="73a1a-113">Atribuir recursos reserváveis genéricos a uma tarefa e gerar requisitos de recursos</span><span class="sxs-lookup"><span data-stu-id="73a1a-113">Assign generic bookable resources to a task and generate resource requirements</span></span>](/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="73a1a-114">Reservar recursos nomeados a partir de requisitos de recursos</span><span class="sxs-lookup"><span data-stu-id="73a1a-114">Book named resources from resource requirements</span></span>](/dynamics365/project-service/book-named-resource)
- [<span data-ttu-id="73a1a-115">Submeter um pedido de recurso</span><span class="sxs-lookup"><span data-stu-id="73a1a-115">Submit a resource request</span></span>](/dynamics365/project-service/submit-resource-request)
- [<span data-ttu-id="73a1a-116">Concluir um pedido de recurso</span><span class="sxs-lookup"><span data-stu-id="73a1a-116">Fulfill a resource request</span></span>](/dynamics365/project-service/resource-management-fulfill-requests)
- [<span data-ttu-id="73a1a-117">Aceitar ou rejeitar um recurso de projeto proposto a partir de um pedido de recurso</span><span class="sxs-lookup"><span data-stu-id="73a1a-117">Accept or reject a proposed project resource from a resource request</span></span>](/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a><span data-ttu-id="73a1a-118">Modo híbrido</span><span class="sxs-lookup"><span data-stu-id="73a1a-118">Hybrid mode</span></span>
<span data-ttu-id="73a1a-119">Para as organizações que necessitam de flexibilidade na alocação de recursos, o modo híbrido conferem aos Gestores de projeto e aos Gestores de recursos a capacidade de reservar recursos.</span><span class="sxs-lookup"><span data-stu-id="73a1a-119">For organizations who require flexibility in the allocation of resources, the hybrid mode enables both Project managers and Resource managers the ability to book resources.</span></span>

![Modo Híbrido](./media/resource-management-hybrid.png)

<span data-ttu-id="73a1a-121">Além do processo do modo Central suportado, consulte os seguintes tópicos para gerir todos os outros fluxos de reservas suportados no modo Híbrido:</span><span class="sxs-lookup"><span data-stu-id="73a1a-121">In addition to the supported Central mode process, see the following topics to manage all other supported booking flows in the Hybrid mode:</span></span>

<span data-ttu-id="73a1a-122">Reservar um recurso diretamente para um projeto:</span><span class="sxs-lookup"><span data-stu-id="73a1a-122">Book a resource directly to a project:</span></span>
- [<span data-ttu-id="73a1a-123">Reservar recursos reserváveis nomeados para uma equipa do projeto e atribuir tarefas</span><span class="sxs-lookup"><span data-stu-id="73a1a-123">Book named bookable resources to a project team and assign tasks</span></span>](/dynamics365/project-service/assign-named-bookable-resource)

<span data-ttu-id="73a1a-124">Reservar um recurso a partir de um requisito de recurso:</span><span class="sxs-lookup"><span data-stu-id="73a1a-124">Book a resource from a resource requirement:</span></span>
- [<span data-ttu-id="73a1a-125">Atribuir recursos reserváveis genéricos a uma tarefa e gerar requisitos de recursos</span><span class="sxs-lookup"><span data-stu-id="73a1a-125">Assign generic bookable resources to a task and generate resource requirements</span></span>](/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="73a1a-126">Reservar recursos nomeados a partir de requisitos de recursos</span><span class="sxs-lookup"><span data-stu-id="73a1a-126">Book named resources from resource requirements</span></span>](/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]