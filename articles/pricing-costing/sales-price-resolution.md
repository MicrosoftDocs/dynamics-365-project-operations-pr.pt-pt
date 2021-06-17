---
title: Resolver preços de venda para estimativas e valores reais
description: Este tópico fornece informações sobre como resolver taxas de venda para estimativas e valores reais.
author: rumant
ms.date: 04/07/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bf0d92c08cb32d7bddb72246623b608831ff883e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004860"
---
# <a name="resolve-sales-prices-for-estimates-and-actuals"></a>Resolver preços de venda para estimativas e valores reais

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

Quando os preços de venda de estimativas e reais são resolvidos no Dynamics 365 Project Operations, o sistema utiliza primeiro a data e a moeda da cotação ou contrato do projeto conexo para resolver a lista de preços de venda. Após a resolução da lista de preços de venda, o sistema resolve a taxa de vendas ou faturação.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-time"></a>Resolver as taxas de venda em linhas de valores reais e de estimativa para o tempo

No Project Operations, as linhas de estimativa para tempo são usadas para denotar os detalhes da linha de proposta e do item de contrato para o tempo e as atribuições de recursos no projeto.

Depois de uma lista de preços para vendas ser resolvida, o sistema completa os seguintes passos para assumir a predefinição da taxa de faturação.

1. O sistema utiliza os campos **Função**, **Empresa de Atribuição de Recursos** e **Unidade de Atribuição de Recursos** na linha de estimativa para o tempo, para corresponder às linhas de preços de função na lista de preços resolvidas. Esta correspondência pressupõe que estão a ser utilizadas dimensões de preços prontas a utilizar para as taxas de faturação. Se tiver preços configurados com base noutros campos em vez de, ou para além de, **Função**, **Empresa de Atribuição de Recursos** e **Unidade de Atribuição de Recursos**, esta é a combinação que será usada para obter uma linha de preços de função correspondente.
2. Se o sistema encontrar uma linha de preço de função que tenha uma taxa de faturação para a combinação de campos **Função**, **Empresa de Atribuição de Recursos** e **Unidade de Atribuição de Recursos**, essa taxa de faturação assume a predefinição.
3. Se o sistema não conseguir corresponder os valores de campo **Função**, **Empresa de Atribuição de Recursos** e **Unidade de Atribuição de Recursos**, obtém linhas de preço de função com uma função correspondente, mas valores nulos da **Unidade de Atribuição de Recursos**. Depois do sistema encontrar um registo de preço de função correspondente, irá assumir a predefinição da taxa de faturação desse registo. Esta correspondência assume uma configuração pronta a utilizar para a prioridade relativa de **Função** vs. **Unidade de Atribuição de Recursos** como uma dimensão de preços de venda.

> [!NOTE]
> Se configurou uma priorização diferente de **Função**, **Empresa de Atribuição de Recursos** e **Unidade de Atribuição de Recursos**, ou se tiver outras dimensões que tenham maior prioridade, este comportamento mudará em conformidade. O sistema obtém os registos de preços de função com valores correspondentes de cada um dos valores da dimensão dos preços na ordem de prioridade com linhas que têm valores nulos para que essas dimensões sejam as últimas.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Resolver as taxas de venda em linhas de valores reais e de estimativa para a despesa

No Project Operations, as linhas de estimativa para despesa são usadas para denotar os detalhes da linha de proposta e do item de contrato para despesas e as linhas de estimativa de despesas no projeto.

Depois de uma lista de preços para vendas ser resolvida, o sistema completa os seguintes passos para assumir a predefinição do preço de vendas da unidade.

1. O sistema utiliza a combinação de campos **Função** e **Unidade** na linha de estimativa para despesa, para corresponder às linhas de preços de categoria na lista de preços resolvidas.
2. Se o sistema encontrar uma linha de preço de categoria que tenha uma taxa de vendas para a combinação de campos **Categoria** e **Unidade**, essa taxa de vendas assume a predefinição.
3. Se o sistema encontrar uma linha de preços de categoria correspondente, o método de preços pode ser utilizado para assumir a predefinição do preço de venda. A tabela abaixo mostra o comportamento de assumir predefinição do preço da despesa no Project Operations.

    | Contexto | Método de definição de preços | Preço predefinido |
    | --- | --- | --- |
    | Estimativa | Preço unitário | Com base na linha de preços da categoria |
    | &nbsp; | A custo | 0.00 |
    | &nbsp; | Margem de Lucro Sobre o Custo | 0.00 |
    | Valor Real | Preço unitário | Com base na linha de preços da categoria |
    | &nbsp; | A custo | Com base no valor real do custo relacionado |
    | &nbsp; | Margem de Lucro Sobre o Custo | Ao aplicar uma margem de lucro como definida pela linha de preço da categoria na taxa de custo da unidade do valor real do custo relacionado |

4. Se o sistema não conseguir corresponder aos valores de campo **Categoria** e **Unidade**, a taxa de vendas assume a predefinição zero (0).

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-material"></a>Resolução de taxas de vendas em valores reais e em linhas de estimativa de material

No Project Operations, as linhas de estimativa de material são usadas para denotar a linha de proposta e os detalhes do item de contrato para os materiais e as linhas de estimativa de material do projeto.

Depois de uma lista de preços para vendas ser resolvida, o sistema completa os seguintes passos para assumir a predefinição do preço de vendas da unidade.

1. O sistema utiliza a combinação de campo **Produto** e **Unidade** na linha de estimativa do material para corresponder ao item da lista de preço na lista de preços que foi resolvida.
2. Se o sistema encontrar um item de lista de preços que tenha uma taxa de venda para a combinação de campo **Produto** e **Unidade** e o método de preços é o **Valor da moeda**, o preço de venda especificado na linha de preços é utilizado.
3. Se os valores dos campos **Produto** e **Unidade** não corresponderem, a taxa de vendas passa a zero.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
