---
title: Novidades de agosto de 2021 - Implementação leve do Project Operations
description: Este tópico fornece informações sobre as atualizações de qualidade disponíveis na versão de agosto de 2021 da implementação leve do Project Operations.
author: sigitac
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e1e0842edaa6153a4780bc799d8df3b6ebb12bba
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323520"
---
# <a name="whats-new-august-2021---project-operations-lite-deployment"></a>Novidades de agosto de 2021 - Implementação leve do Project Operations

_Aplica-se a: Implementação lite – negócio para faturação pró-forma_

Este tópico aplica-se aos seguintes componentes e versões do Dynamics 365 Project Operations:

  - Project Operations na versão 4.13.0.152 do ambiente Dataverse

## <a name="features-included-in-this-release"></a>Funcionalidades incluídas nesta versão

Estão incluídas nesta versão as seguintes funcionalidades:

- **Conjuntos de aprovações**: Os conjuntos de aprovações agrupam os pedidos de aprovação de utilização de tempo, despesa ou material em subconjuntos menores de operações. Este agrupamento permite que as aprovações sejam processadas por projeto, numa ordem específica, e permite repetições e sequenciações. O agrupamento de pedidos melhora a fiabilidade e a rastreabilidade do processamento de aprovações no caso de grandes volumes de aprovações. Para mais informações, consulte [Conjuntos de aprovações](../../approvals/approval-sets.md).

## <a name="quality-updates"></a>Atualizações de qualidade

### <a name="project-operations-on-dataverse"></a>Project Operations no Dataverse

| **Área de funcionalidades** | **Número de referência** | **Atualização de qualidade** |
| --- | --- | --- |
| Faturação e preços | 2295625 | O nome do marco deve ser copiado da agenda de faturação para o detalhe da linha de fatura. |
| Faturação e preços | 2316323 | O desconto não deve ser editável numa fatura pró-forma no Project Operations para cenários baseados em recursos. |
| Gestão de oportunidades | 2338619 | As regras de negócio **Oportunidade** e **Proposta** só devem ser invocadas nas páginas. |
| Gestão de recursos | 2316523 | A utilização de **Enviar Pedido** a partir de um requisito de recurso que tem uma função anexada não deve apresentar um erro. |
| Gestão de recursos | 2326885 | A criação de um requisito de recurso através de um projeto não deve apresentar um erro. |
| Tempo e despesa | 2335584 | Fluxos de tarefas preteridos na entrada de hora. |
| Tempo e despesa | 2336884 | O botão de entrada de hora **Copiar Semana** deve funcionar para algo mais do que apenas o utilizador atual. |