---
title: Resolução de preços de venda para estimativas e valores reais
description: Este tópico fornece informações sobre a resolução dos preços de venda em estimativas e valores reais.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c8972bd7710735e9acdbf951079f2da24a00bd7f
ms.sourcegitcommit: f8edff6422b82fdf2cea897faa6abb51e2c0c3c8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/21/2020
ms.locfileid: "4088052"
---
# <a name="resolving-sales-prices-for-estimates-and-actuals"></a>Resolução de preços de venda para estimativas e valores reais

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

Quando os preços de venda em estimativas e valores reais são resolvidos no Dynamics 365 Project Operations, o sistema utiliza primeiro a data e a moeda da proposta ou contrato de projeto relacionado para resolver a lista de preços de venda. Após a resolução da lista de preços de venda, o sistema resolve a taxa de vendas ou faturação.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-time"></a>Resolver as taxas de venda em linhas de valores reais e de estimativa para o tempo

No Project Operations, as linhas de estimativa para tempo são usadas para denotar os detalhes da linha de proposta e do item de contrato para o tempo e as atribuições de recursos no projeto.

Depois de uma lista de preços para vendas ser resolvida, o sistema completa os seguintes passos para assumir a predefinição da taxa de faturação.

1. O sistema utiliza os campos **Função** e **Unidade de Atribuição de Recursos** na linha de estimativa para o tempo, para corresponder às linhas de preços de função na lista de preços resolvidas. Esta correspondência pressupõe que estão a ser utilizadas dimensões de preços prontas a utilizar para as taxas de faturação. Se tiver preços configurados com base noutros campos em vez de, ou para além de, **Função** e **Unidade de Atribuição de Recursos** , esta é a combinação que será usada para obter uma linha de preços de função correspondente.
2. Se o sistema encontrar uma linha de preço de função que tenha uma taxa de faturação para a combinação de campos **Função** e **Unidade de Atribuição de Recursos** , essa taxa de faturação assume a predefinição.
3. Se o sistema não conseguir corresponder os valores de campo **Função** e **Unidade de Atribuição de Recursos** , obtém linhas de preço de função com uma função correspondente, mas valores nulos da **Unidade de Atribuição de Recursos**. Depois do sistema encontrar um registo de preço de função correspondente, irá assumir a predefinição da taxa de faturação desse registo. Esta correspondência assume uma configuração pronta a utilizar para a prioridade relativa de **Função** vs. **Unidade de Atribuição de Recursos** como uma dimensão de preços de venda.

> [!NOTE]
> Se configurar uma priorização diferente de **Função** e **Unidade de Atribuição de Recursos** , ou se tiver outras dimensões que tenham maior prioridade, este comportamento mudará em conformidade. O sistema obtém os registos de preços de função com valores correspondentes de cada um dos valores da dimensão dos preços na ordem de prioridade com linhas que têm valores nulos para que essas dimensões sejam as últimas.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Resolver as taxas de venda em linhas de valores reais e de estimativa para a despesa

No Project Operations, as linhas de estimativa para despesa são usadas para denotar os detalhes da linha de proposta e do item de contrato para despesas e as linhas de estimativa de despesas no projeto.

Depois de uma lista de preços para vendas ser resolvida, o sistema completa os seguintes passos para assumir a predefinição do preço de vendas da unidade.

1. O sistema utiliza a combinação de campos **Função** e **Unidade** na linha de estimativa para despesa, para corresponder às linhas de preços de categoria na lista de preços resolvidas.
2. Se o sistema encontrar uma linha de preço de categoria que tenha uma taxa de vendas para a combinação de campos **Categoria** e **Unidade** , essa taxa de vendas assume a predefinição.
3. Se o sistema encontrar uma linha de preços de categoria correspondente, o método de preços pode ser utilizado para assumir a predefinição do preço de venda. A tabela abaixo mostra o comportamento de assumir predefinição do preço da despesa no Project Operations.

    | Contexto | Método de definição de preços | Preço predefinido |
    | --- | --- | --- |
    | Estimativa | Preço unitário | Com base na linha de preços da categoria |
    | &nbsp; | A custo | 0.00 |
    | &nbsp; | Margem de Lucro Sobre o Custo | 0.00 |
    | Valor Real | Preço unitário | Com base na linha de preços da categoria |
    | &nbsp; | A custo | Com base no valor real do custo relacionado |
    | &nbsp; | Margem de Lucro Sobre o Custo | Aplicar uma margem de lucro como definida pela linha de preço da categoria na taxa de custo da unidade do valor real do custo relacionado |

4. Se o sistema não conseguir corresponder aos valores de campo **Categoria** e **Unidade** , a taxa de vendas assume a predefinição zero (0).