---
title: Descrição geral de linhas de proposta baseadas em produtos – lite
description: Este tópico fornece informações sobre trabalhar com linhas de proposta baseadas em produtos.
author: rumant
ms.date: 10/30/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 8b904f9abd3d2505c5397906f63a5ae8ff4be41b
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369840"
---
# <a name="product-based-quote-lines-overview---lite"></a>Descrição geral de linhas de proposta baseadas em produtos – lite

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

É possível criar linhas de proposta baseadas em produtos no Dynamics 365 Project Operations. As linhas de proposta baseadas em produtos podem ser adicionadas manualmente ou podem ser itens do catálogo de produtos.

## <a name="product-catalog"></a>Catálogo de produtos

Cada produto no catálogo de produtos tem uma unidade e um grupo de unidades predefinidos. Se vários produtos partilharem o mesmo conjunto de atributos, pode criar uma família de produtos que partilhe esses atributos. 

Por exemplo, uma empresa vende licenças de subscrição para diferentes tipos de software. Todo o software de subscrição possui os seguintes dois atributos:

- Número de utilizadores
- Uma duração da subscrição medida em meses

Para manter este tipo de catálogo, crie uma família de produtos denominada **Software de Subscrição** e com o número de utilizadores e duração da subscrição como atributos. Em seguida, pode adicionar produtos individuais à família de produtos de **Software de Subscrição**.

## <a name="add-product-catalog-items-to-a-project-quote"></a>Adicionar itens do catálogo de produtos a uma proposta do projeto

As páginas **Proposta do Projeto** e **Contrato do Projeto** têm secções para linhas baseadas em projetos e linhas baseadas em produtos. Para linhas baseadas em produtos, a lista pendente na linha de proposta ou no item de contrato do projeto inclui todos os produtos e unidades existentes na lista de preços. Também pode adicionar produtos que não fazem parte da lista de preços do produto.

Além disso, pode selecionar produtos de outras listas de preços ou diretamente a partir do catálogo de produtos. Quando seleciona produtos diretamente a partir de um catálogo de produtos, a lista de preços predefinida desse produto é utilizada para obter o preço de venda do produto. Se não for definida uma lista de preços predefinida, o preço é definido como zero (0).

Quando uma linha de proposta for baseada num catálogo de produtos, pode definir manualmente o preço de venda diretamente na linha de proposta. Uma linha de proposta no campo de **Preços** com dois valores disponíveis:

- **Definir Preço Manualmente**
- **Utilizar Predefinição**

Se selecionar **Definir Preço Manualmente**, o preço predefinido não está definido. Em vez disso, tem de introduzir um preço para o produto na linha de proposta. Se selecionar **Utilizar Predefinição**, o preço de vendas predefinido é utilizado e o campo está bloqueado para edição.

Os preços de vendas predefinidos são introduzidos nas linhas baseadas em produtos de uma proposta. O campo **Preços** é definido para **Definir Preço Manualmente**, para que possa editar o preço predefinido nas linhas de proposta. Esta é uma definição manual específica do Project Operations do comportamento das linhas baseadas em produtos no Dynamics 365 Sales.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]