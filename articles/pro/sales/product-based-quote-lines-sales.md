---
title: Descrição geral de linhas de proposta baseadas em produtos – lite
description: Este tópico fornece informações sobre trabalhar com linhas de proposta baseadas em produtos.
author: rumant
manager: Annbe
ms.date: 10/30/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 29d82637c6c8bb5b5cde7707d181d5b3d3b235c4
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272582"
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