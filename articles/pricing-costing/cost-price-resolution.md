---
title: Resolução dos preços de custo para estimativas e valores reais
description: Este tópico fornece informações sobre a resolução dos preços de custo para estimativas e valores reais.
author: rumant
ms.date: 04/09/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d81b521acbfd97127cf056bd41a3249c01108374
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001395"
---
# <a name="resolving-cost-prices-for-estimates-and-actuals"></a>Resolução dos preços de custo para estimativas e valores reais

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

Para resolver os preços de custo e a lista de preços de custos para estimativas e valores reais, o sistema utiliza as informações nos campos **Data**, **Moeda** e **Unidade Contratante** do projeto relacionado. Após a resolução da lista de preços de custo, a aplicação resolve a taxa de custo.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Resolver as taxas de custo em linhas de valores reais e de estimativa para Tempo

As linhas de estimativa para Tempo referem-se aos detalhes de item de contrato e de proposta para tempo e atribuições de recursos num projeto.

Após uma lista de preços de custo ser resolvida, o sistema utiliza os campos **Função**, **Empresa de Atribuição de Recursos** e **Unidade de Atribuição de Recursos** na linha de estimativa para Tempo, para corresponder às linhas de preço de função na lista de preços. Esta correspondência pressupõe que está a utilizar dimensões de preços prontas a utilizar para o custo da mão de obra. Se tiver configurado o sistema para corresponder campos em vez de, ou para além de, **Função**, **Empresa de Atribuição de Recursos** e **Unidade de Atribuição de Recursos**, uma combinação diferente será usada para obter uma linha de preços de função correspondente. Se a aplicação encontrar uma linha de preço de função que tenha uma taxa de custo para a combinação **Função**, **Empresa de Atribuição de Recursos** e **Unidade de Atribuição de Recursos**, essa é a taxa de custo predefinida. Se a aplicação não corresponder exatamente à combinação de **Função**, **Empresa de recursos** e **Unidade de recursos**, irá recuperar linhas de preço de função com um valor de função correspondente, mas terá valores nulos para **Unidade de recursos** e **Empresa de recursos**. Após um registo de preço de função correspondente ao valor do preço da função ser encontrado, a taxa de custos torna-se padrão desse registo. 

> [!NOTE]
> Se configurar uma priorização diferente de **Função**, **Empresa de Atribuição de Recursos** e **Unidade de Atribuição de Recursos**, ou se tiver outras dimensões que tenham maior prioridade, este comportamento mudará em conformidade. O sistema recupera os registos de preços de função com valores que correspondem a cada um dos valores de dimensão de preços por ordem prioritária com linhas que têm valores nulos para essas dimensões que vêm em último lugar na ordem prioritária.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Resolver as taxas de custo em linhas de valores reais e de estimativa para Despesa

As linhas de estimativa para Despesa referem-se aos detalhes de item de contrato e de proposta para despesas e as linhas de estimativa de despesa num projeto.

Após uma lista de preços de custo ser resolvida, o sistema utiliza uma combinação dos campos **Categoria** e **Unidade** na linha de estimativa para uma despesa, para corresponder às linhas **Preços de Categoria** na lista de preços resolvidas. Se o sistema encontrar uma linha de preço de categoria que tenha uma taxa de custo para a combinação de campos **Categoria** e **Unidade**, essa taxa de custo assume a predefinição. Se o sistema não conseguir corresponder os valores **Categoria** e **Unidade**, ou se for capaz de encontrar uma linha de preço de categoria correspondente, mas o método de preços não é **Preço Por Unidade**, a taxa de custo assume a predefinição zero (0).

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-material"></a>Resolução de taxas de custos em valores reais e em linhas de estimativa de material

As linhas de estimativa de material referem-se aos detalhes do item de contrato para os materiais e as linhas de estimativa de material de um projeto.

Depois de uma lista de preços de custos ser resolvida, o sistema utiliza uma combinação dos campos **produto** e **Unidade** na linha de estimativa para uma estimativa material que corresponda às linhas de **Itens da Lista de Preços** na lista de preços resolvidas. Se o sistema encontrar uma linha de preços do produto que tenha uma taxa de custo para a combinação de campo **Produto** e **Unidade**, a taxa de custo está em incumprimento. Se o sistema não conseguir corresponder aos valores do **Produto** e da **Unidade**, o custo unitário passa a zero. Esta predefinição também irá ocorrer se houver uma linha de item de lista de preços correspondente, mas o método de preços se basear num custo padrão ou no custo atual que não está definido no produto.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
