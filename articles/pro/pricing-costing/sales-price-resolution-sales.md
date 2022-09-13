---
title: Determinar preços de venda para estimativas e valores reais de projeto
description: Este artigo fornece informações sobre a forma como os preços de venda para estimativas e valores reais do projeto são determinados.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 6504302578d1eb3d00c717ea93cd4c4212acb4e7
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410133"
---
# <a name="determine-sales-prices-for-project-estimates-and-actuals"></a>Determinar preços de venda para estimativas e valores reais de projeto

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

Para determinar os preços de venda de estimativas e valores reais no Microsoft Dynamics 365 Project Operations, o sistema utiliza primeiro a data e a moeda na estimativa recebida ou no contexto real para determinar a lista de preços de venda. Especificamente no contexto real, o sistema utiliza o campo **Data das transações** para determinar a lista de preços aplicável. Após a determinação da lista de preços de venda, o sistema determina a venda ou taxa de faturação.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-time"></a>Determinar as taxas de venda em linhas de valores reais e de estimativa para a Hora

O contexto de estimativa **Hora** refere-se a:

- Detalhes de linha de proposta para **Hora**.
- Detalhes do item de contrato para **Hora**.
- Atribuições de recurso num projeto.

O contexto real para **Hora** refere-se a:

- Entradas e Correções de entradas de diário para **Hora**.
- Entradas de diário que são criadas quando uma entrada de hora é submetida.
- Detalhes da linha de fatura para **Hora**. 

Depois de uma lista de preços para vendas ser determinada, o sistema completa os seguintes passos para introduzir a taxa de faturação predefinida.

1. O sistema faz corresponder a combinação dos campos **Função** e **Unidade de atribuibuição de recursos** na estimativa ou contexto atual para **Hora** em relação às linhas de preço de função na lista de preços. Esta correspondência pressupõe que está a utilizar as dimensões de preços prontas a utilizar para as taxas de faturação. Se configurou preços com base noutros campos em vez de, ou para além de, **Função** e **Unidade de atribuição de recursos**, esta combinação de campos é usada para obter uma linha de preços de função correspondente.
1. Se o sistema encontrar uma linha de preço de função que tenha uma taxa de faturação para a combinação de campos **Função** e **Unidade de atribuição de recursos**, essa taxa de faturação é usada como a taxa de faturação predefinida.
1. Se o sistema não conseguir corresponder os valores **Função**, **Unidade de atribuição de Recursos**, obtém linhas de preços de função que têm valores correspondentes ao campo **Função**, mas valores nulos para o campo **Unidade de atribuição de recursos**. Depois do sistema encontrar um registo de preço de função correspondente, a taxa de faturação desse registo será usada como a taxa de faturação predefinida. Esta correspondência assume uma configuração pronta a utilizar para a prioridade relativa de **Função** versus a **Unidade de atribuição de recursos** como uma dimensão de preços de venda.

> [!NOTE]
> Se configurou uma priorização diferente dos campos **Função** e **Unidade de atribuição de recursos**, ou se tiver outras dimensões que tenham maior prioridade, o comportamento anterior irá mudar em conformidade. O sistema obtém dados de preços de função que têm valores que correspondem a cada valor de dimensão de preços por ordem de prioridade. As linhas que têm valores nulos para essas dimensões são as últimas.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Determinar taxas de venda em linhas de valores reais e de estimativa para Despesa

O contexto de estimativa **Despesa** refere-se a:

- Detalhes de linha de proposta para **Despesa**.
- Detalhes de item de contrato para **Despesa**.
- Linhas de estimativas de despesa num projeto.

O contexto real **Despesa** refere-se a:

- Entradas e Correções de entradas de diário para **Despesa**.
- Entradas de diário que são criadas quando uma entrada de despesa é submetida.
- Detalhes de item de fatura para **Despesa**. 

Depois de uma lista de preços para vendas ser determinada, o sistema completa os seguintes passos para introduzir o preço de venda unitário predefinido.

1. O sistema faz corresponder a combinação dos campos **Categoria** e **Unidade** na linha de estimativa para **Despesa** em relação às linhas de preços de categoria na lista de preços.
1. Se o sistema encontrar uma linha de preço de categoria que tenha uma taxa de vendas para a combinação **Categoria** e **Unidade**, essa taxa de vendas é usada como a taxa de vendas predefinida.
1. Se o sistema encontrar uma linha de preços de categoria correspondente, o método de preços pode ser utilizado para introduzir o preço de venda predefinido. A tabela abaixo mostra o comportamento predefinido de preços de despesa no Project Operations.

    | Contexto | Método de definição de preços | Preço predefinido |
    | --- | --- | --- |
    | Estimativa | Preço unitário | Com base na linha de preços da categoria. |
    |        | A custo | 0.00 |
    |        | Margem de Lucro Sobre o Custo | 0.00 |
    | Valor Real | Preço unitário | Com base na linha de preços da categoria. |
    |        | A custo | Com base no valor real do custo relacionado. |
    |        | Margem de Lucro Sobre o Custo | É aplicada uma margem de lucro, como definido pela linha de preço da categoria, na taxa de custo unitário do valor de custo real relacionado. |

1. Se o sistema não conseguir corresponder os valores **Categoria** e **Unidade**, a taxa de vendas é definida como **0** (zero) por predefinição.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-material"></a>Determinação de taxas de vendas em valores reais e em linhas de estimativa de Material

O contexto de estimativa **Material** refere-se a:

- Detalhes de linha de proposta para **Material**.
- Detalhes de item de contrato para **Material**.
- Linhas de estimativas de material num projeto.

O contexto real **Material** refere-se a:

- Entradas e Correções de entradas de diário para **Material**.
- Entradas de diário que são criadas quando o registo de utilização de Material é submetido.
- Detalhes de item de fatura para **Material**. 

Depois de uma lista de preços para vendas ser determinada, o sistema completa os seguintes passos para introduzir o preço de venda unitário predefinido.

1. O sistema faz corresponder a combinação dos campos **Produto** e **Unidade** na linha de estimativa para **Material** em relação às linhas de item da lista de preços para a lista de preços.
1. Se o sistema encontrar um item de lista de preços que tenha uma taxa de venda para a combinação de campo **Produto** e **Unidade** e se o método de preços é o **Montante em moeda**, o preço de venda especificado na linha de preços é utilizado. 
1. Se os valores dos campos **Produto** e **Unidade** não corresponderem ou se o método de definição de preços for diferente do **Montante em moeda**, a taxa de vendas é definida como **0** (zero) por predefinição. Este comportamento ocorre porque o Project Operations suportam apenas o método de definição de preços **Montante em moeda** para os materiais utilizados num projeto.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
