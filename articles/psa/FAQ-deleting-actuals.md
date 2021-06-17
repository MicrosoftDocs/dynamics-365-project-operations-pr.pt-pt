---
title: Por que motivo é que não é possível eliminar registos da entidade Valores Reais?
description: Este tópico fornece informações sobre por que não pode eliminar registos da entidade Valores Reais.
author: JPBurrows
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
ms.openlocfilehash: 434be93cedb4772616b1e6d5cbe15fc715eed19a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993115"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a>Por que motivo é que não é possível eliminar registos da entidade Valores Reais?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

O Project Service Automation (PSA) não permite eliminar valores reais, porque estes servem de fonte de verdade para as transações que têm implicações financeiras nos sistemas a jusante, como o razão geral. Se for possível eliminar os valores reais, a integridade das transações de relatórios financeiros poderá ser questionável. Para estabelecer um registo de auditoria, os clientes devem utilizar diários para criar transações de compensação.



[!INCLUDE[footer-include](../includes/footer-banner.md)]