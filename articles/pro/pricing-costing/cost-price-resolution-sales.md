---
title: Resolução dos preços de custo em estimativas e valores reais – lite
description: Este tópico fornece informações sobre a resolução dos preços de custo em estimativas e valores reais.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d2afaa2231f4044dbcbfa24b91aec39289275a91
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764608"
---
# <a name="resolve-cost-prices-on-estimates-and-actuals---lite"></a>Resolução dos preços de custo em estimativas e valores reais – lite

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

Para resolver os preços de custo e a lista de preços de custos para estimativas e valores reais, o sistema utiliza as informações nos campos **Data**, **Moeda** e **Unidade Contratante** do projeto relacionado. Após a resolução da lista de preços de custo, a aplicação resolve a taxa de custo.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Resolver as taxas de custo em linhas de valores reais e de estimativa para Tempo

As linhas de estimativa para Tempo referem-se aos detalhes de item de contrato e de proposta para tempo e atribuições de recursos num projeto.

Após a conclusão de uma lista de preços de custos, os campos **Função** e **Unidade de atribuição de recurso** na linha estimada de Tempo são comparados com as linhas de preços de função na tabela de preços. Esta equivalência pressupõe que está a usar as dimensões de preços padrão para o custo da mão de obra. Se tiver configurado o sistema para corresponder campos em vez de, ou para além de **Função** e **Unidade de Atribuição de Recursos**, uma combinação diferente será usada para obter uma linha de preços de função correspondente. Se a aplicação encontrar uma linha de preço de função que tenha uma taxa de custo para a combinação **Função** e **Unidade de Atribuição de Recursos**, essa é a taxa de custo predefinida. Se a aplicação não conseguir corresponder os valores **Função** e **Unidade de Atribuição de Recursos**, obtém linhas de preço de função com uma função correspondente, mas valores nulos da **Unidade de Atribuição de Recursos**. Depois de ter um registo de preço de função correspondente, a taxa de custo assume a predefinição desse registo. 

> [!NOTE]
> Se configurou uma priorização diferente de **Função** e **Unidade de Atribuição de Recursos**, ou se tiver outras dimensões que tenham maior prioridade, este comportamento mudará em conformidade. O sistema obtém os registos de preços de função com valores que correspondem a cada um dos valores da dimensão dos preços na ordem de prioridade com linhas que têm valores nulos para que essas dimensões sejam as últimas.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Resolver as taxas de custo em linhas de valores reais e de estimativa para Despesa

As linhas de estimativa para Despesa referem-se aos detalhes de item de contrato e de proposta para despesas e as linhas de estimativa de despesa num projeto.

Após a conclusão de uma lista de preços de custos, o sistema utiliza uma combinação dos campos **Categoria** e **Unidade** na linha estimada de despesas para corresponder às linhas **Categoria de preço** na lista de preços resolvidas. Se o sistema encontrar uma linha de preço de categoria que tenha uma taxa de custo para a combinação de campos **Categoria** e **Unidade**, essa taxa de custo assume a predefinição. Se o sistema não conseguir equivaler os valores **Categoria** e **Unidade**, ou se for capaz de encontrar uma linha de preço de categoria correspondente, mas o método de preços não for **Preço Por unidade**, a taxa de custos passa a zero(0).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]