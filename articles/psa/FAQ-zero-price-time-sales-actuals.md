---
title: Porque é que o preço padrão é zero em vendas de valores reais?
description: Resolução de problemas de porque é que o preço padrão é 0 em vendas de valores reais.
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
ms.openlocfilehash: 5f72e0db94392a35fee9fdcf2c4adb8a08feef13
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146227"
---
# <a name="why-is-price-defaulting-to-zero-on-time-sales-actuals"></a>Porque é que o preço padrão é zero em vendas de valores reais?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Este FAQ é aplicável ao valores reais onde a classe de transação está definida como Tempo e tipo de transação como Vendas Não Faturadas. As seguintes três verificações irão ajudá-lo a resolver o motivo pelo qual os preços (taxa de cobrança) estão como padrão a 0 no tempo de vendas de valores reais.

## <a name="check-1-identify-the-sales-price-list-for-the-project"></a>Verificação 1: identificar a lista de preços de vendas do projeto

Localize o projeto no campo do projeto do valor real e aceda à página do projeto. Em seguida, vá ao separador Vendas e na grelha de Itens de Contrato do Projeto, clique na ligação no campo Contrato do Projeto. Abre a página de Contrato do projeto. Na página Contrato do Projeto, vá para o separador Listas de Preços do Projeto. Verifique se existe, pelo menos, uma lista de preços anexada aqui. Se não houver nenhuma lista de preços anexada na grelha de Listas de Preços do Contrato do Projeto, localizou o problema. Anexe uma lista de preços à grelha de Listas de Preços do Projeto. As listas de preços permitidas a ser anexadas aqui deverão ter o campo de contexto definido como Vendas e o campo de moeda na lista de preços deve corresponder ao campo no contrato do projeto. Depois de efetuadas as correções necessárias, recrie a entrada de tempo, aprove-a e verifique se as vendas em valores reais não faturadas mostram um preço válido. 

Se tiver uma ou mais listas de preços anexadas na grelha de Listas de Preços do Contrato do Projeto, vá para a verificação seguinte no documento.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-sales-actual"></a>Verificação 2: qualquer uma das listas de preços identificadas acima é válida para a data específica das vendas em valores reais?

Para o Project Service ter em consideração uma lista de preços para o preço padrão, essa lista de preços deve ser aplicável para a data nas vendas em valores reais. Verifique o seguinte para ver se a(s) lista(s) de preços identificada(s) acima é/são aplicável(eis):
- Verifique se as datas de início e de fim do separador geral para as listas de preços associadas não estão vazias. Se as datas de início e de fim das listas de preços identificadas acima estão vazias, localizou o problema. 
- Anote o campo de data de início nas suas vendas em valores reais e verifique se qualquer uma das listas de preços identificadas é aplicável para essa data. Por exemplo, a data de vendas em valores reais deve estar dentro da data de início e data de fim na lista de preços. 
    - Se não houver nenhuma lista de preços que abranja essa data nas vendas de valor real, localizou o problema. Modifique as datas de início e de fim da lista de preços para assegurar que a lista de preços abrange a data de vendas de valores reais. 
    - Se houver mais do que uma lista de preços que abranja essa data nas vendas de valores reais, localizou o problema. Pode corrigir isto editando as datas de início e de fim da(s) lista(s) de preços para que exista apenas uma lista de preços que abranja a data de vendas de valores reais. 
    - Se tiver apenas uma lista de preços que abrange essa data das vendas de valores reais, vá para a Verificação 3.
Depois de efetuadas as correções necessárias, recrie a entrada de tempo, aprove-a e verifique se as vendas de valores reais mostram um preço válido.

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-sales-actual"></a>Verificação 3: existe um preço na lista de preços para as dimensões de preços nas vendas de valores reais?

Se tiver concluído com êxito a Verificação 1 e 2, deverá agora ter apenas uma lista de preços que é aplicável para a data de vendas de valores reais. Abra a Lista de Preços e navegue para o separador de Preços de Função. Certifique-se de que existe uma linha na grelha para as dimensões de preços nas vendas de Tempo em valores reais.

Se não houver nenhuma linha na grelha de preços para as dimensões de preço nas vendas de valores reais, então, localizou o problema. Crie uma linha na grelha de Preços de funções para as dimensões de preço nas suas vendas de valores reais. Feito isto, recrie a entrada de tempo, aprove-a e verifique se as vendas de valores reais mostram um preço válido.

Se ainda não visualizar um preço válido nas suas vendas de valores reais depois de seguir as três verificações acima, submeta um pedido de suporte. 



[!INCLUDE[footer-include](../includes/footer-banner.md)]