---
title: FAQ de gestão de recursos
description: Este tópico fornece respostas às perguntas mais frequentes sobre a gestão de recursos.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: d335a12a9b478bff63b6c93809c89dac9718a4be
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144382"
---
# <a name="resource-management-faq"></a><span data-ttu-id="65e65-103">FAQ de gestão de recursos</span><span class="sxs-lookup"><span data-stu-id="65e65-103">Resource management FAQ</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a><span data-ttu-id="65e65-104">Qual é a diferença entre um membro da equipa e um requisito de recurso?</span><span class="sxs-lookup"><span data-stu-id="65e65-104">What is the difference between a team member and a resource requirement?</span></span>

<span data-ttu-id="65e65-105">Um membro da equipa do projeto pode ser atribuído a tarefas, reservado ou reservado em excesso e definido como aprovador.</span><span class="sxs-lookup"><span data-stu-id="65e65-105">A project team member can be assigned to tasks, booked or overbooked, and set as an approver.</span></span> <span data-ttu-id="65e65-106">Um requisito de recurso pode existir sem um membro da equipa do projeto, como uma nota de procura de rascunho.</span><span class="sxs-lookup"><span data-stu-id="65e65-106">A resource requirement can exist without a project team member, as a draft note of demand.</span></span> 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a><span data-ttu-id="65e65-107">Qual é a diferença entre as horas propostas e as horas reservadas de forma flexível?</span><span class="sxs-lookup"><span data-stu-id="65e65-107">What is the difference between proposed and soft-booked hours?</span></span>

<span data-ttu-id="65e65-108">As horas propostas e as horas reservadas de forma flexível diferem em visibilidade.</span><span class="sxs-lookup"><span data-stu-id="65e65-108">Proposed hours and soft-booked hours differ in visibility.</span></span> <span data-ttu-id="65e65-109">As horas propostas são visíveis apenas para os gestores de recursos e o gestor de projeto que iniciaram a procura utilizando um pedido de recurso.</span><span class="sxs-lookup"><span data-stu-id="65e65-109">Proposed hours are visible only to resource managers and the project manager who initiated the demand by using a resource request.</span></span> <span data-ttu-id="65e65-110">As horas reservadas de forma flexível são visíveis a qualquer pessoa que tenha acesso ao Quadro da Agenda.</span><span class="sxs-lookup"><span data-stu-id="65e65-110">Soft-booked hours are visible to anyone who has access to the Schedule Board.</span></span>

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a><span data-ttu-id="65e65-111">Como posso ver as horas reservadas de forma flexível para os recursos numa equipa?</span><span class="sxs-lookup"><span data-stu-id="65e65-111">How can I see the soft-booked hours for resources on a team?</span></span>

<span data-ttu-id="65e65-112">As reservas flexíveis podem ser efetuadas quando reserva um requisito de recurso.</span><span class="sxs-lookup"><span data-stu-id="65e65-112">Soft bookings can made when you book a resource requirement.</span></span> <span data-ttu-id="65e65-113">Os recursos que são reservados de forma flexível numa equipa do projeto aparecem como membros da equipa que possuem horas reservadas de forma flexível.</span><span class="sxs-lookup"><span data-stu-id="65e65-113">Resources that are soft-booked on a project team appear as team members who have soft-booked hours.</span></span> <span data-ttu-id="65e65-114">Também aparecem no Quadro da Agenda.</span><span class="sxs-lookup"><span data-stu-id="65e65-114">They also appear on the Schedule Board.</span></span>

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a><span data-ttu-id="65e65-115">Como posso alterar as horas necessárias e as datas de início e de fim, para um recurso (genérico ou nomeado) que reservei?</span><span class="sxs-lookup"><span data-stu-id="65e65-115">How do I change the required hours, and the start and end dates, for a resource (generic or named) that I booked?</span></span>

<span data-ttu-id="65e65-116">Depois de os recursos serem reservados, selecione **Manter Reservas** para efetuar as alterações necessárias.</span><span class="sxs-lookup"><span data-stu-id="65e65-116">After resources are booked, select **Maintain Bookings** to make any changes that are required.</span></span>

## <a name="what-resources-types-does-project-service-automation-support"></a><span data-ttu-id="65e65-117">Que tipos de recursos suporta o Project Service Automation?</span><span class="sxs-lookup"><span data-stu-id="65e65-117">What resources types does Project Service Automation support?</span></span>

<span data-ttu-id="65e65-118">O **Utilizador** e o **Contacto** são os únicos tipos de recursos suportados no Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="65e65-118">**User** and **Contact** are the only resource types that are supported in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="65e65-119">Apesar de poder criar outros tipos de recursos (por exemplo, **Equipamento** e **Grupo**), nenhum caso de utilização completo é suportado por eles.</span><span class="sxs-lookup"><span data-stu-id="65e65-119">Although you can create other types of resources (for example, **Equipment** and **Group**), no end-to-end use case is supported for them.</span></span>

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a><span data-ttu-id="65e65-120">Qual é a diferença entre uma atribuição e uma reserva?</span><span class="sxs-lookup"><span data-stu-id="65e65-120">What is the difference between an assignment and a booking?</span></span>

<span data-ttu-id="65e65-121">As atribuições são a atribuição de recursos às tarefas de projeto na agenda do projeto.</span><span class="sxs-lookup"><span data-stu-id="65e65-121">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="65e65-122">Os recursos podem ser recursos reais ou genéricos.</span><span class="sxs-lookup"><span data-stu-id="65e65-122">The resources can be either real or generic resources.</span></span> <span data-ttu-id="65e65-123">As reservas são a alocação fixa ou flexível de recursos a um projeto.</span><span class="sxs-lookup"><span data-stu-id="65e65-123">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="65e65-124">As reservas fixas consomem a capacidade de um recurso.</span><span class="sxs-lookup"><span data-stu-id="65e65-124">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="65e65-125">Idealmente, no caso dos recursos reais, as reservas e atribuições devem concordar, porque não diferem.</span><span class="sxs-lookup"><span data-stu-id="65e65-125">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="65e65-126">No entanto, o PSA não impõe este contrato.</span><span class="sxs-lookup"><span data-stu-id="65e65-126">However, PSA doesn't enforce this agreement.</span></span> <span data-ttu-id="65e65-127">A vista de Reconciliação mostra um gestor de projeto em que as reservas e as atribuições de um recurso não concordam.</span><span class="sxs-lookup"><span data-stu-id="65e65-127">The Reconciliation view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>
