---
title: Valores Reais
description: Este artigo fornece informações sobre como trabalhar com valores reais no Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 02/22/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 2551b7d6d20df170c913e302e734583135265529
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924812"
---
# <a name="actuals"></a>Valores Reais

_**Aplica-se a:** Project Operations para cenários baseados em recursos/não armazenados, implementação leve - negócio para faturação pró-forma_

Os valores reais representam os progressos financeiros e de programação revistos e aprovados num projeto. São criados quando as entradas de hora, despesas e utilização de material, entradas de diário e faturas são aprovadas.

> [!IMPORTANT]
> Os valores reais não devem ser editados nem eliminados do sistema. Caso contrário, a integridade financeira e qualquer integração com outros sistemas financeiros e de contabilidade poderá ser afetada negativamente. O Microsoft Dynamics 365 Project Operations permite-lhe utilizar a reversão e substituição de valores reais para editar valores reais em vários pontos do ciclo de vida dos processos de negócio dos seus projetos.

## <a name="recording-actuals-based-on-project-events"></a>Registar valores reais com base em eventos de projeto

O Project Operations regista as transações financeiras que ocorrem durante o ciclo de vida de cativação do projeto como valores reais. A criação de valores reais em vários eventos no ciclo de vida varia, dependendo se a cativação do projeto utiliza o modelo de faturação de tempo e materiais ou o modelo de faturação de preço fixo, quer se mantenha na fase de pré-venda ou se é um projeto interno.

Os artigos seguintes explicam o impacto na tabela Valores Reais em vários eventos para diferentes variações:

- [Impacto do valor real numa cativação de tempo e materiais](ActualsonTM.md)
- [Impacto real numa cativação de preço fixo](ActualonFP.md)
- [Impacto real durante a fase de pré-venda de uma cativação](ActualonPreSales.md)
- [Impacto dos valores reais para um projeto interno](ActualonInternal.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
