---
title: Por que motivo é que não é possível eliminar registos da entidade Valores Reais?
description: Este tópico fornece informações sobre por que não pode eliminar registos da entidade Valores Reais.
author: JPBurrows
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 11/6/2018
ms.topic: article
ms.prod: Project Service
ms.technology: Applies to all versions of Project Service
ms.assetid: ff504c34-7337-474f-89e8-d8afdd1e0a98
ms.author: Jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 5817940933c161dccac0fe549fabacbe57e7077a
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754489"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a><span data-ttu-id="1e372-103">Por que motivo é que não é possível eliminar registos da entidade Valores Reais?</span><span class="sxs-lookup"><span data-stu-id="1e372-103">Why can’t I delete records from the Actuals entity?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="1e372-104">O Project Service Automation (PSA) não permite eliminar valores reais, porque estes servem de fonte de verdade para as transações que têm implicações financeiras nos sistemas a jusante, como o razão geral.</span><span class="sxs-lookup"><span data-stu-id="1e372-104">Project Service Automation (PSA) doesn't allow you to delete actuals because they serve as the source of truth for transactions that have financial implications to downstream systems, such as the general ledger.</span></span> <span data-ttu-id="1e372-105">Se for possível eliminar os valores reais, a integridade das transações de relatórios financeiros poderá ser questionável.</span><span class="sxs-lookup"><span data-stu-id="1e372-105">If actuals could be deleted, the integrity of the financial reporting transactions could be questioned.</span></span> <span data-ttu-id="1e372-106">Para estabelecer um registo de auditoria, os clientes devem utilizar diários para criar transações de compensação.</span><span class="sxs-lookup"><span data-stu-id="1e372-106">To establish an audit trail, customers should use journals to create compensating transactions.</span></span>

