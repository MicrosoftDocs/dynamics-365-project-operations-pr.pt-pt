---
title: Linhas de proposta baseadas em produtos
description: Este artigo fornece informações sobre linhas de proposta baseadas em produtos.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
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
ms.reviewer: johnmichalak
ms.openlocfilehash: a5385e1bb0f18a7cc1d23f4e46c86d8340ba951d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922696"
---
# <a name="product-based-quote-lines"></a>Linhas de proposta baseadas em produtos

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


É possível criar linhas de proposta baseadas em produtos no Dynamics 365 Project Service Automation. As linhas de proposta baseadas em produtos podem ser linhas "acrescentadas manualmente" ou podem ser itens do catálogo de produtos.

## <a name="product-catalog"></a>Catálogo de produtos

Os produtos existentes num catálogo de produtos do Dynamics 365 têm uma unidade e um grupo de unidades predefinidos. Se vários produtos partilharem o mesmo conjunto de atributos, pode criar uma família de produtos que também tenha esses atributos. Todos os produtos de uma família de produtos herdam o mesmo conjunto de atributos.

Por exemplo, uma empresa vende licenças de subscrição para uma variedade de softwares. Todo o software de subscrição possui os seguintes dois atributos:

- Número de utilizadores 
- Duração da subscrição (em meses)

Uma boa forma de manter este tipo de catálogo consiste em criar uma família de produtos denominada **Software de Subscrição** e com o **Número de utilizadores** e **Duração da subscrição** como atributos. Em seguida, pode adicionar produtos individuais, tais como **Dynamics 365 Sales** ou **Dynamics 365 Field Service** à família de produtos **Software de Subscrição**.

## <a name="adding-product-catalog-items-to-a-project-quote"></a>Adicionar itens do catálogo de produtos a uma proposta do projeto

As páginas da proposta do projeto e do contrato do projeto têm secções para dois tipos de linha: linhas baseadas em projetos e linhas baseadas em produtos. Quanto às linhas baseadas em produtos, o Dynamics 365 é utilizado para adicionar itens de um catálogo de produtos a uma proposta. A lista pendente na linha de proposta ou no item de contrato do projeto inclui todos os produtos e unidades existentes na lista de preços do produto anexada à proposta ou ao contrato do projeto. Também pode adicionar produtos que não fazem parte da lista de preços do produto da proposta.

Além disso, pode selecionar produtos de outras listas de preços ou pode selecionar produtos diretamente a partir do catálogo de produtos. Quando seleciona produtos diretamente a partir de um catálogo de produtos, a lista de preços predefinida desse produto é utilizada para obter o preço de venda do produto. Se não for definida uma lista de preços predefinida, o preço é definido como 0 (zero).

Se uma linha de proposta for baseada num catálogo de produtos, pode definir manualmente o preço de venda diretamente na linha de proposta. Tenha em atenção que uma linha de proposta no Dynamics 365 tem um campo **Definição de Preços**. Estão disponíveis dois valores:

- Definir preço manualmente  
- Utilizar predefinição

Se definir este campo como **Definir preço manualmente**, o Dynamics 365 não define um preço predefinido. Tem de introduzir um preço para o produto na linha de proposta. Se definir este campo para **Utilizar predefinição**, o Dynamics 365 utiliza o preço de venda predefinido e bloqueia o campo para impedir a edição.

Depois de instalar o PSA, os preços de venda predefinidos são introduzidos nos itens baseados em produtos numa proposta. O campo **Definição de Preços** é definido para **Definir preço manualmente**, para que possa editar o preço predefinido nas linhas de proposta.

> ![Definir preço manualmente.](media/basic-guide-10.png)
 
## <a name="quantity-factors-for-products"></a>Fatores de quantidade para produtos

O PSA utiliza fatores de quantidade para suportar a venda de produtos baseados em subscrições. Para produtos baseados em subscrições, a quantidade na proposta ou item de contrato do projeto é expressa como o número de meses do utilizador.

Normalmente, o preço do software de subscrição é armazenado no catálogo como o preço por utilizador, por mês. No entanto, pode utilizar outras descrições de tempo. Durante o processo de vendas, o preço na linha de proposta é, normalmente, o preço por utilizador e por mês negociado e descontado pelo agente de vendas de TI. Cada negócio tem um número diferente de utilizadores e um número diferente de meses de subscrição. A quantidade que é utilizada para calcular o montante da linha de proposta é um produto do número de utilizadores e do número de meses de subscrição.

Para suportar este tipo de venda, o PSA introduziu o conceito de fatores de quantidade. Os fatores de quantidade dependem dos atributos do produto no Dynamics 365. Quando configura propriedades específicas para um produto, o PSA permite-lhe sinalizar um subconjunto dessas propriedades, ou todas as propriedades, como fatores de quantidade.

O PSA valida que apenas as propriedades numéricas ou as propriedades de produto que têm um tipo de dados numérico são sinalizadas como fatores de quantidade. Quando um produto para o qual os fatores de quantidade estão configurados é adicionado a uma linha de proposta, o campo **Quantidade** na linha da proposta passa a ser um campo só de leitura. Depois de introduzir valores para propriedades de produto que são fatores de quantidade, o PSA calcula a quantidade da linha de proposta.

Por exemplo, o Dynamics 365 poderá ter as seguintes propriedades: 

- **N.º de utilizadores** - O número de utilizadores 
- **N.º de Meses** - O número de meses da subscrição
- **SKU do Produto** 

As propriedades **N.º de Utilizadores** e **N.º de Meses** podem ser sinalizadas como fatores de quantidade editando as propriedades da linha de produto. 

> ![Sinalizar N.º de Utilizadores e N.º de Meses como fatores de qualidade.](media/basic-guide-11.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
