---
title: Reservas versus atribuições
description: Este tópico fornece informações sobre as diferenças entre as reservas de recursos e as atribuições de recursos.
author: ruhercul
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8fe6937dfdfe137f28917c16da1d7dc6155284ae
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130232"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="81da3-103">Reservas versus atribuições</span><span class="sxs-lookup"><span data-stu-id="81da3-103">Bookings vs assignments</span></span>

<span data-ttu-id="81da3-104">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="81da3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="81da3-105">As reservas são a alocação fixa ou flexível de recursos a um projeto.</span><span class="sxs-lookup"><span data-stu-id="81da3-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="81da3-106">As reservas fixas consomem a capacidade de um recurso.</span><span class="sxs-lookup"><span data-stu-id="81da3-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="81da3-107">As reservas representam conceitos organizacionais para as equipas, para que possam compreender como os recursos serão envolvidos em vários projetos.</span><span class="sxs-lookup"><span data-stu-id="81da3-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="81da3-108">O Dynamics 365 Project Operations considera as reservas um conceito ao nível do projeto.</span><span class="sxs-lookup"><span data-stu-id="81da3-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="81da3-109">Ao contrários das reservas, as atribuições são a alocação de recursos às tarefas de projeto na agenda do projeto.</span><span class="sxs-lookup"><span data-stu-id="81da3-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="81da3-110">Os recursos podem ser nomeados ou genéricos.</span><span class="sxs-lookup"><span data-stu-id="81da3-110">The resources can be named or generic.</span></span> 

<span data-ttu-id="81da3-111">Normalmente, a soma das reservas para um recurso será igual à soma das atribuições do recurso numa ou muitas tarefas.</span><span class="sxs-lookup"><span data-stu-id="81da3-111">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="81da3-112">No entanto, o Project Operations não impõe este contrato.</span><span class="sxs-lookup"><span data-stu-id="81da3-112">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="81da3-113">A vista de **Reconciliação** mostra o Gestor de projeto em que as reservas e as atribuições de um recurso não concordam.</span><span class="sxs-lookup"><span data-stu-id="81da3-113">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>
