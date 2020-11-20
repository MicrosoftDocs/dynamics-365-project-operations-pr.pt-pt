---
title: Estimativas de recursos
description: Este tópico fornece informações sobre como as estimativas de recursos são calculadas no Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 454b8931db53739a7bc19364911109802a1ed087
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127388"
---
# <a name="resource-estimates"></a>Estimativas de recursos

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

As estimativas de recursos provêm de um esforço faseado no tempo que é definido na estrutura hierárquica do trabalho, juntamente com as dimensões de preços aplicáveis. Tipicamente, o cálculo é **tarifa/hora para cada função x horas**. O esforço faseado no tempo para cada recurso é armazenado no registo de atribuição de recursos. Os preços são armazenados numa lista de preços predefinida. A conversão de unidades é aplicada com base na lista de preços aplicável.

![Estimativas de Recursos](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a>Preço de custo e moeda de custo predefinidos

Os preços de custos são assumidos por predefinição a partir da Unidade Organizacional.

## <a name="default-bill-rate-and-sales-currency"></a>Taxa de faturação e moeda de venda predefinidas

Os preços de venda são aplicados uma vez por negócio. A hierarquia para assumir por predefinição a lista de preços de venda é a seguinte:

1. Organização
2. Cliente
3. Proposta/contrato
