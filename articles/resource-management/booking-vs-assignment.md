---
title: Reservas versus atribuições
description: Este tópico fornece informações sobre as diferenças entre as reservas de recursos e as atribuições de recursos.
author: ruhercul
manager: Annbe
ms.date: 01/08/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3aaf8dcbae0a5762879c2b1223eba3bdc33af1a7
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279917"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="bf8b8-103">Reservas versus atribuições</span><span class="sxs-lookup"><span data-stu-id="bf8b8-103">Bookings vs assignments</span></span>

<span data-ttu-id="bf8b8-104">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="bf8b8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="bf8b8-105">As reservas são a alocação fixa ou flexível de recursos a um projeto.</span><span class="sxs-lookup"><span data-stu-id="bf8b8-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="bf8b8-106">As reservas fixas consomem a capacidade de um recurso.</span><span class="sxs-lookup"><span data-stu-id="bf8b8-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="bf8b8-107">As reservas representam conceitos organizacionais para as equipas, para que possam compreender como os recursos serão envolvidos em vários projetos.</span><span class="sxs-lookup"><span data-stu-id="bf8b8-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="bf8b8-108">Dynamics 365 Project Operations considera as reservas um conceito de nível de projeto.</span><span class="sxs-lookup"><span data-stu-id="bf8b8-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="bf8b8-109">Ao contrários das reservas, as atribuições são a alocação de recursos às tarefas de projeto na agenda do projeto.</span><span class="sxs-lookup"><span data-stu-id="bf8b8-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="bf8b8-110">Os recursos podem ser nomeados ou genéricos.</span><span class="sxs-lookup"><span data-stu-id="bf8b8-110">The resources can be named or generic.</span></span>  <span data-ttu-id="bf8b8-111">Quando um requisito de recursos é derivado das atribuições de tarefas do projeto, o Project Operations usa os contornos de esforço da atribuição de recursos para construir os contornos dos detalhes dos requisitos de recursos.</span><span class="sxs-lookup"><span data-stu-id="bf8b8-111">When a resource requirement is derived from the project task assignments, Project Operations uses the effort contours of the resources assignment to build the contours of the resource requirement details.</span></span> <span data-ttu-id="bf8b8-112">No entanto, não é mantida uma referência para as atribuições de recursos.</span><span class="sxs-lookup"><span data-stu-id="bf8b8-112">However, a refence to the resource assignments isn't maintained.</span></span> <span data-ttu-id="bf8b8-113">As atualizações às reservas derivadas do requisito de recursos não atualizam nenhuma atribuição de recursos.</span><span class="sxs-lookup"><span data-stu-id="bf8b8-113">Updates to the bookings derived from the resource requirement don't update any resource assignments.</span></span>

<span data-ttu-id="bf8b8-114">Normalmente, a soma das reservas para um recurso será igual à soma das atribuições do recurso numa ou muitas tarefas.</span><span class="sxs-lookup"><span data-stu-id="bf8b8-114">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="bf8b8-115">No entanto, o Project Operations não impõe este contrato.</span><span class="sxs-lookup"><span data-stu-id="bf8b8-115">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="bf8b8-116">A vista de **Reconciliação** mostra o Gestor de projeto em que as reservas e as atribuições de um recurso não concordam.</span><span class="sxs-lookup"><span data-stu-id="bf8b8-116">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]