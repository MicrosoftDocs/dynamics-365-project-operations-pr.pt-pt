---
title: Porque é que o preço padrão é zero em custos de valores reais?
description: Resolução de problemas de porque é que o preço padrão é 0 para custos de valores reais.
author: rumant
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 635fe6dfb547e8b9f96ca1786912309a770e24c2
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146272"
---
# <a name="why-is-the-price-defaulting-to-zero-on-time-cost-actuals"></a>Porque é que o preço padrão é zero em custos de valores reais?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Este FAQ é aplicável aos valores reais onde a classe de transação está definida como Tempo e tipo de transação como Custos. As seguintes três verificações irão ajudá-lo a resolver o motivo pelo qual os preços estão como padrão a 0 para custos em valores reais.
 
## <a name="check-1-identify-the-cost-price-list-for-the-project"></a>Verificação 1: identificar a lista de preços de custos do projeto

Localize o projeto no campo do projeto e, em seguida, aceda à página do projeto. Clique na hiperligação de unidade de contratação no campo. Na página Unidade de Contratação, verifique se a unidade de contratação tem uma lista de preços na grelha de Listas de Preços de Custos.

Se existir mais de uma lista de preços, localizou o problema. O Project Service suporta apenas uma lista de preços por unidade organizacional. Remova todas as listas de preços desta entidade até que exista apenas uma lista de preços anexada na grelha de Listas de Preços de Custo da Unidade Organizacional.

Se não houver nenhuma lista de preços anexada à Unidade Organizacional, tome nota da moeda da Unidade organizacional. Aceda ao Project Service e, em seguida, vá a Parâmetros e abra o separador Listas de Preços. Verifique se existem listas de preços com contexto definido como Custo e moeda que corresponde à da Unidade Organizacional.
 
Se não houver nenhuma lista de preços que corresponda a esses critérios, localizou o problema. Certifique-se de que tem, pelo menos, uma lista de preços cujo contexto está definido como Custo e cuja moeda corresponde à da Unidade Organizacional.

Se existir mais de uma lista de preços que correspondam a esses critérios, continue a ler este documento para efetuar mais verificações.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-cost-actual"></a>Verificação 2: qualquer uma das listas de preços identificadas acima é válida para a data específica dos custos em valores reais?

Para o Project Service ter em consideração uma lista de preços para o preço padrão, essa lista de preços deve ser aplicável para a data nos custos em valores reais. Verifique o seguinte para ver se a(s) lista(s) de preços identificada(s) acima é/são aplicável(eis):

- Verifique se as datas de início e de fim do separador geral para as listas de preços associadas não estão vazias. Se as datas de início e de fim das listas de preços identificadas acima estão vazias, localizou o problema. 
- Anote o campo de data de início nos seus custos em valores reais e verifique se qualquer uma das listas de preços identificadas é aplicável para essa data. Por exemplo, a data de custos em valores reais deve estar dentro da data de início e data de fim na lista de preços. 
    - Se não houver nenhuma lista de preços que abranja essa data nos custos em valores reais, localizou o problema. Modifique as datas de início e de fim da lista de preços para assegurar que a lista de preços abrange a data de custos em valores reais. 
    - Se houver mais do que uma lista de preços que abranja essa data nos custos em valores reais, localizou o problema. Pode corrigir isto editando as datas de início e de fim da(s) lista(s) de preços para que exista apenas uma lista de preços que abranja a data de custos em valores reais. 
    - Se tiver apenas uma lista de preços que abrange essa data do custo de tempo em valores reais, mova para a verificação seguinte no documento.
Depois de efetuadas as correções necessárias, recrie a entrada de tempo, aprove-a e verifique se os custos em valores reais mostram um preço válido.

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-cost-actual"></a>Verificação 3: existe um preço na lista de preços para as dimensões de preços nos custos em valores reais?

Se tiver concluído com êxito a Verificação 1 e 2, deverá agora ter apenas uma lista de preços que é aplicável para a data de custos em valores reais. Abra a Lista de Preços e vá para o separador de Preços de Função. Certifique-se de que existe uma linha na grelha para as dimensões de preços no custo de tempo em valores reais.

Se não houver nenhuma linha na grelha de preços para as dimensões de preço nos custos em valores reais, então, localizou o problema. Crie uma linha na grelha de Preços de funções para as dimensões de preço nos seus custos em valores reais. Feito isto, recrie a entrada de tempo, aprove-a e verifique se os custos em valores reais mostram um preço válido.
 
Se ainda não visualizar um preço válido nas seus custos de valores reais depois de seguir as três verificações acima, submeta um pedido de suporte.





[!INCLUDE[footer-include](../includes/footer-banner.md)]