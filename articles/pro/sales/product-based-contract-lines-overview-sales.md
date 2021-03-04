---
title: Descrição geral dos itens de contrato baseados em produtos – lite
description: Este tópico fornece informações sobre itens de contrato baseados em produtos.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: eb09140eae5383b882db73195d0360a836ece791
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177885"
---
# <a name="product-based-contract-lines-overview---lite"></a>Descrição geral dos itens de contrato baseados em produtos – lite

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

Pode criar itens de contrato baseados em produtos no Dynamics 365 Project Operations. Os itens de contrato baseados em produtos podem ser linhas criadas manualmente ou podem ser itens do catálogo de produtos.

## <a name="product-catalog"></a>Catálogo de produtos

Os produtos no catálogo de produtos têm uma unidade e um grupo de unidades predefinidos. Se vários produtos partilharem o mesmo conjunto de atributos, pode criar uma família de produtos que também tenha esses atributos. Todos os produtos de uma família de produtos herdam o mesmo conjunto de atributos.

Por exemplo, uma empresa vende licenças de subscrição para diferentes tipos de software. Todo o software de subscrição possui os seguintes dois atributos:

- Número de utilizadores
- Duração da subscrição (em meses)

Para manter este tipo de catálogo, crie uma família de produtos que se chama **Software de Subscrição**. Adicione os atributos, **Número de utilizadores** e **Duração da subscrição** à família de produtos. Em seguida, adicione produtos individuais à família de produtos **Software de Subscrição**.

## <a name="add-product-catalog-items-to-a-project-contract"></a>Adicionar itens do catálogo de produtos a um Contrato do projeto

Os contratos do projeto e do contrato do projeto têm secções para dois tipos de linha, baseadas em projetos e baseadas em produtos. As linhas baseadas em produtos incluem todos os produtos e unidades na lista de preços do produto no contrato. Os produtos que não fazem parte da lista de preços de um contrato podem ser adicionados.

Pode selecionar produtos de outras listas de preços, ou diretamente do catálogo de produtos. Quando seleciona produtos diretamente a partir de um catálogo de produtos, a lista de preços predefinida desse produto é utilizada para o preço de venda do produto. Se não for definida uma lista de preços predefinida, o preço é definido como 0 (zero).

Se um item de contrato for baseado num catálogo de produtos, pode definir manualmente o preço de venda diretamente no item. Um item de contrato tem o campo **Definir preço** com os dois valores:

- **Definir preço manualmente**
- **Utilizar predefinição**

Se definir o campo como **Definir preço**, para **Definir preço manualmente**, o preço predefinido não é definido. Introduza um preço para o produto no item de contrato. Se definir o campo para **Utilizar predefinição**, o preço de vendas predefinido é utilizado e o campo não pode ser editado.

Depois de instalar o Project Operations, os preços de venda predefinidos são introduzidos nos itens baseados em produtos num contrato. O campo **Definir preço** é definido para **Definir preço manualmente**, para que possa editar o preço predefinido nos itens de contrato. Esta é uma definição manual específica do Project Operations ao comportamento de linhas baseadas em produtos no Dynamics 365 Sales.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]