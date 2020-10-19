---
title: Reservas versus atribuições
description: Este tópico fornece informações sobre as diferenças entre as reservas de recursos e as atribuições de recursos.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fa99783e52dbcdeaf80bbfd03df0f458f86b5e99
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896025"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="4dc6d-103">Reservas versus atribuições</span><span class="sxs-lookup"><span data-stu-id="4dc6d-103">Bookings vs assignments</span></span>

<span data-ttu-id="4dc6d-104">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="4dc6d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4dc6d-105">As reservas são a alocação fixa ou flexível de recursos a um projeto.</span><span class="sxs-lookup"><span data-stu-id="4dc6d-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="4dc6d-106">As reservas fixas consomem a capacidade de um recurso.</span><span class="sxs-lookup"><span data-stu-id="4dc6d-106">Hard bookings consume a resource's capacity.</span></span> 

<span data-ttu-id="4dc6d-107">As atribuições são a atribuição de recursos às tarefas de projeto na agenda do projeto.</span><span class="sxs-lookup"><span data-stu-id="4dc6d-107">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="4dc6d-108">Os recursos podem ser reais ou genéricos.</span><span class="sxs-lookup"><span data-stu-id="4dc6d-108">The resources can be real or generic.</span></span> 

<span data-ttu-id="4dc6d-109">Idealmente, no caso dos recursos reais, as reservas e atribuições devem concordar, porque não diferem.</span><span class="sxs-lookup"><span data-stu-id="4dc6d-109">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="4dc6d-110">No entanto, o Microsoft Dynamics Project Operations não impõe este contrato.</span><span class="sxs-lookup"><span data-stu-id="4dc6d-110">However, Microsoft Dynamics Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="4dc6d-111">A vista **Reconciliação** mostra um gestor de projeto em que as reservas e as atribuições de um recurso não concordam.</span><span class="sxs-lookup"><span data-stu-id="4dc6d-111">The **Reconciliation** view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>
