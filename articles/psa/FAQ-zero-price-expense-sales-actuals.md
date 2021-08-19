---
title: Porque é que o preço padrão é zero em despesas de vendas em valores reais?
description: As seguintes três verificações irão ajudá-lo a resolver o motivo pelo qual os preços estão como padrão a 0 para despesas de vendas em valores reais.
author: rumant
ms.prod: ''
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 6e477b7d5973398d50c6be03469d1c0a792b1b3323522329bc33cba755104968
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 08/06/2021
ms.locfileid: "7000815"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-sales-actuals"></a>Porque é que o preço padrão é zero em despesas de vendas em valores reais?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Este FAQ é aplicável às despesas de valores reais onde a classe de transação está definida como Despesa e tipo de transação como Vendas Não Faturadas. As seguintes três verificações irão ajudá-lo a resolver o motivo pelo qual os preços (taxa de cobrança) estão como padrão a 0 nas despesas de vendas em valores reais.

## <a name="check-1-identify-the-sales-price-list-for-project"></a>Verificação 1: identificar a lista de preços de vendas do projeto

Localize o projeto no campo do projeto do valor real e aceda à página do projeto. Em seguida, vá ao separador Vendas. Na grelha de Itens de Contrato do Projeto, clique na ligação no campo Contrato do Projeto. Abre a página de Contrato do Projeto. Na página Contrato do Projeto, vá para o separador Listas de Preços do Projeto. Verifique se existe, pelo menos, uma lista de preços anexada aqui.

Se não houver nenhuma lista de preços anexada na grelha de Listas de Preços do Contrato do Projeto:

- Anexe uma lista de preços à grelha de Listas de Preços do Projeto. As listas de preços permitidas a ser anexadas aqui deverão ter o campo de contexto definido como Vendas e o campo de moeda na lista de preços deve corresponder ao campo no contrato do projeto. Depois de efetuadas as correções necessárias, recrie a entrada de despesa, aprove-a e verifique se as vendas em valores reais não faturadas mostram um preço válido.
- Se tiver uma ou mais listas de preços anexadas na grelha de Listas de Preços do Contrato do Projeto, vá para a Verificação 2.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-expense-actual"></a>Verificação 2: qualquer uma das listas de preços identificadas acima é válida para a data específica das despesas em valores reais?

Para o Project Service ter em consideração uma lista de preços para o preço padrão, essa lista de preços deve ser aplicável para a data nas despesas em valores reais. Verifique o seguinte para ver se a(s) lista(s) de preços identificada(s) acima é/são aplicável(eis):

- Comece por verificar se as datas de início e de fim do separador geral para as listas de preços associadas não estão vazias. Se as datas de início e de fim nas listas de preços identificadas acima estão vazias, localizou o problema. 
- Anote o campo de data de início nas suas despesas em valores reais e verifique se qualquer uma das listas de preços identificadas é aplicável para essa data. Por exemplo, a data de despesas em valores reais deve estar dentro da data de início e data de fim na lista de preços. 
    - Se não houver nenhuma lista de preços que abranja essa data nas despesas em valores reais, localizou o problema. Modifique as datas de início e de fim da lista de preços para assegurar que a lista de preços abrange a data de despesas em valores reais. 
    - Se houver mais do que uma lista de preços que abranja essa data nas despesas em valores reais, localizou o problema. Editar as datas de início e de fim da(s) lista(s) de preços para que exista apenas uma lista de preços que abranja a data de despesas em valores reais. 
    - Se tiver apenas uma lista de preços que abrange essa data das despesas em valores reais, vá para a Verificação 3.
Depois de efetuadas as correções necessárias, recrie a entrada de despesa, aprove-a e verifique se as vendas em valores reais não faturadas mostram um preço válido.

## <a name="check-3-is-there-a-valid-price-for-the-expense-category-in-the-applicable-project-price-list"></a>Verificação 3: existe um preço válido para a categoria de despesas na lista de preços aplicável ao projeto? 

Se tiver concluído com êxito a Verificação 1 e 2, deverá agora ter apenas uma lista de preços de projeto que é aplicável para a data de despesas em valores reais. Abra a Lista de Preços do Projeto e vá para o separador Categoria de Preços. Certifique-se de que existe uma linha na grelha para a categoria de despesas específica nas Despesas em valores reais.
 
- Se não houver nenhuma linha, localizou o problema. Crie uma linha na grelha de Categoria de preços para a categoria nas suas despesas em valores reais. Depois, recrie uma entrada de despesas, aprove-a e verifique se as vendas não faturadas em valores reais mostram um preço válido. 
- Se existir uma linha para a categoria de despesas na grelha de preços de categoria, verifique se tem um preço válido.

Para compreender o que é um preço válido, utilize estes métodos:

- Se o campo Método de Preços na linha de preços de Categoria está definido A Custo, então, a taxa de unidades nas suas Despesas de vendas em valores reais será predefinida para o valor na entrada Despesas.
- Se o campo Método de Preços na Linha de Preços da Categoria estiver definido como Percentagem de Margem de Lucro, então, verifique se o campo Percentagem é definido como um valor válido. A taxa de unidades nas suas Despesas de vendas em valores reais é predefinida aplicando esta percentagem de margem de lucro ao preço na entrada Despesas.
- Se o campo Método de Preços na Linha de Preços da Categoria estiver definido Preço por Unidade, então, verifique se o campo Preço é definido como um valor válido. A taxa de unidades nas suas Despesas de vendas em valores reais será predefinido para o montante de moeda especificado no campo Preços.

Se a configuração de preços para a categoria de despesas não for válida, então, localizou o problema. A solução é editar a linha de preços de categoria com um preço válido para a categoria de despesas de acordo com as regras acima. Feito isto, recrie uma entrada de despesas, aprove-a e depois verifique se as vendas não faturadas em valores reais mostram um preço válido.

Se ainda não visualizar um preço válido nas suas despesas em valores reais depois de efetuar as três verificações acima, submeta um pedido de suporte.




[!INCLUDE[footer-include](../includes/footer-banner.md)]