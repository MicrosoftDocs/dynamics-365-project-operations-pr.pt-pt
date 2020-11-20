---
title: Por que motivo é que não é possível eliminar registos da entidade Valores Reais?
description: Este tópico fornece informações sobre por que não pode eliminar registos da entidade Valores Reais.
author: JPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/6/2018
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
ms.openlocfilehash: b9b45e3ae0cd9273af4d2a5cd9cce30502c0aa78
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127172"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a><span data-ttu-id="4ce10-103">Por que motivo é que não é possível eliminar registos da entidade Valores Reais?</span><span class="sxs-lookup"><span data-stu-id="4ce10-103">Why can’t I delete records from the Actuals entity?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="4ce10-104">O Project Service Automation (PSA) não permite eliminar valores reais, porque estes servem de fonte de verdade para as transações que têm implicações financeiras nos sistemas a jusante, como o razão geral.</span><span class="sxs-lookup"><span data-stu-id="4ce10-104">Project Service Automation (PSA) doesn't allow you to delete actuals because they serve as the source of truth for transactions that have financial implications to downstream systems, such as the general ledger.</span></span> <span data-ttu-id="4ce10-105">Se for possível eliminar os valores reais, a integridade das transações de relatórios financeiros poderá ser questionável.</span><span class="sxs-lookup"><span data-stu-id="4ce10-105">If actuals could be deleted, the integrity of the financial reporting transactions could be questioned.</span></span> <span data-ttu-id="4ce10-106">Para estabelecer um registo de auditoria, os clientes devem utilizar diários para criar transações de compensação.</span><span class="sxs-lookup"><span data-stu-id="4ce10-106">To establish an audit trail, customers should use journals to create compensating transactions.</span></span>

