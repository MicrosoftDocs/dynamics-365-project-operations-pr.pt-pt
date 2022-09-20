---
title: Determinar taxas de custo para estimativas e valores reais com base no projeto
description: Este artigo fornece informações sobre a forma como as taxas de custo para estimativas e valores reais com base no projeto são determinadas.
author: rumant
ms.date: 9/12/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 822a7bd8ae87d4fd4044d8b46347bfe1b4ca13ca
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475293"
---
# <a name="determine-cost-rates-for-project-based-estimates-and-actuals"></a>Determinar taxas de custo para estimativas e valores reais com base no projeto

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

Para determinar os preços de custo de estimativas e valores reais no Microsoft Dynamics 365 Project Operations, o sistema utiliza primeiro a data e a moeda na estimativa recebida ou no contexto real para determinar a lista de preços de venda. Especificamente no contexto real, o sistema utiliza o campo **Data das transações** para determinar a lista de preços aplicável. O valor **Data de transação** da estimativa ou valor real de entrada é comparado com os valores **Início efetivo (independente do fuso horário)** e **Fim efetivo (independente do fuso horário)** na lista de preços. Após a determinação da lista de preços de custo, o sistema determina a taxa de custo.

## <a name="determining-cost-rates-in-estimate-and-actual-contexts-for-time"></a>Determinação das taxas de custo nos contextos de estimativa e de valores reais para Hora

O contexto de estimativa **Hora** refere-se a:

- Detalhes de linha de proposta para **Hora**.
- Detalhes do item de contrato para **Hora**.
- Atribuições de recurso num projeto.

O contexto real para **Hora** refere-se a:

- Entradas e Correções de entradas de diário para **Hora**.
- Entradas de diário que são criadas quando uma entrada de hora é submetida.

Depois de uma lista de preços de custo ser determinada, o sistema termina os seguintes passos para introduzir a taxa de custo predefinida.

1. O sistema faz corresponder a combinação dos campos **Função**, **Empresa de atribuição de recursos** e **Unidade de atribuição de recursos** na estimativa ou contexto atual para **Hora** em relação às linhas de preço de função na lista de preços. Esta correspondência pressupõe que está a usar as dimensões de preços standard para o custo da mão de obra. Se tiver configurado o sistema para corresponder campos em vez de, ou para além de, **Função**, **Empresa de atribuição de recursos** e **Unidade de atribuição de recursos**, uma combinação diferente é usada para obter uma linha de preços de função correspondente.
1. Se o sistema encontrar uma linha de preço de função que tenha uma taxa de custo para a combinação **Função**, **Empresa de atribuição de recursos** e **Unidade de atribuição de recursos**, essa é a taxa de custo é utilizada como a taxa de custo predefinida.
1. Se o sistema não conseguir corresponder os valores de **Função**, **Empresa de atribuição de recursos** e **Unidade de atribuição de recursos**, remove a dimensão que tem a prioridade mais baixa, pesquisa linhas de preço de função que correspondem aos outros dois valores de dimensão e continuar a remover dimensões progressivamente até que uma linha de preço de função correspondente seja encontrada. A taxa de custo desse regist será utilizada como taxa de custo predefinida. Se o sistema não encontrar uma linha de preço de função correspondente, o preço será definido como **0** (zero) por predefinição.

> [!NOTE]
> Se configurou uma priorização diferente dos campos **Função** e **Unidade de atribuição de recursos**, ou se tiver outras dimensões que tenham maior prioridade, o comportamento anterior irá mudar em conformidade. O sistema obtém dados de preços de função que têm valores que correspondem a cada valor de dimensão de preços por ordem de prioridade. As linhas que têm valores nulos para essas dimensões são as últimas.

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Determinação de taxas de custo nas linhas de valores reais e estimativa para Despesa

O contexto de estimativa **Despesa** refere-se a:

- Detalhes de linha de proposta para **Despesa**.
- Detalhes de item de contrato para **Despesa**.
- Estimativas de despesa num projeto.

O contexto real **Despesa** refere-se a:

- Entradas e Correções de entradas de diário para **Despesa**.
- Entradas de diário que são criadas quando uma entrada de despesa é submetida.

Depois de uma lista de preços de custo ser determinada, o sistema termina os seguintes passos para introduzir a taxa de custo predefinida.

1. O sistema faz corresponder a combinação dos campos **Categoria** e **Unidade** na estimativa ou contexto atual para **Despesa** em relação às linhas de preço de categoria na lista de preços.
1. Se o sistema encontrar uma linha de preço de categoria que tenha uma taxa de custo para a combinação **Categoria** e **Unidade**, essa taxa de custo é usada como a taxa de custo predefinida.
1. Se o sistema não conseguir corresponder os valores **Categoria** e **Unidade**, o preço é definido como **0** (zero) por predefinição.
1. No contexto de estimativa, se o sistema não conseguir corresponder uma linha de preço de categoria, mas o método de definição de preços é diferente de **Preço unitário**, a taxa de custo é definida como **0** (zero) por predefinição.

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-material"></a>Determinação de taxas de custo em linhas de valores reais e de estimativa para Material

O contexto de estimativa **Material** refere-se a:

- Detalhes de linha de proposta para **Material**.
- Detalhes de item de contrato para **Material**.
- Estimativas de material num projeto.

O contexto real **Material** refere-se a:

- Entradas e Correções de entradas de diário para **Material**.
- Entradas de diário que são criadas quando o registo de utilização de Material é submetido.

Depois de uma lista de preços de custo ser determinada, o sistema termina os seguintes passos para introduzir a taxa de custo predefinida.

1. O sistema usa a combinação dos campos **Produto** e **Unidade** na estimativa ou contexto atual para **Material** em relação às linhas de item da lista preços na lista de preços.
1. Se o sistema encontrar uma linha de item da lista de preços que tenha uma taxa de custo para a combinação **Produto** e **Unidade**, essa taxa de custo é usada como a taxa de custo predefinida.
1. Se o sistema não conseguir corresponder os valores de **Produto** e **Unidade**, o custo unitário é definido como **0** (zero) por predefinição.
1. No contexto de estimativa ou de valor real, se o sistema não conseguir corresponder uma linha de item da lista de preços, mas o método de definição de preços é diferente de **Montante da moeda**, o custo unitário é definido como **0** (zero) por predefinição. Este comportamento ocorre porque o Project Operations suportam apenas o método de definição de preços **Montante em moeda** para os materiais utilizados num projeto.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
