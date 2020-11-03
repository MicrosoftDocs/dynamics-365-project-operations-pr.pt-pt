---
title: Por que motivo é que não é possível eliminar registos da entidade Valores Reais?
description: Este tópico fornece informações sobre por que não pode eliminar registos da entidade Valores Reais.
author: JPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: f47e7ccd46642dc6129fbb3beac3c9490160d046
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082530"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a>Por que motivo é que não é possível eliminar registos da entidade Valores Reais?

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

O Project Service Automation (PSA) não permite eliminar valores reais, porque estes servem de fonte de verdade para as transações que têm implicações financeiras nos sistemas a jusante, como o razão geral. Se for possível eliminar os valores reais, a integridade das transações de relatórios financeiros poderá ser questionável. Para estabelecer um registo de auditoria, os clientes devem utilizar diários para criar transações de compensação.

