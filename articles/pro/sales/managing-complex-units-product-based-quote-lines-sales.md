---
title: Gerir unidades complexas, tais como por utilizador, por mês para linhas de proposta baseadas em produtos – lite
description: Este artigo fornece informações sobre a gestão de unidades complexas para linhas de proposta baseadas em produtos.
author: rumant
ms.date: 10/06/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 88173468cd2e898331c4aa0a398792d9a0f3df10
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929918"
---
# <a name="managing-complex-units-such-as-per-user-per-month-for-product-based-quote-lines---lite"></a>Gerir unidades complexas, tais como por utilizador, por mês para linhas de proposta baseadas em produtos – lite

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

O Dynamics 365 Project Operations utiliza fatores de quantidade para suportar a venda de produtos baseados em subscrições. Para produtos baseados em subscrições, a quantidade na proposta ou item de contrato do projeto é expressa como o número de meses do utilizador.

Normalmente, o preço do software de subscrição é armazenado no catálogo como o preço por utilizador, por mês. Durante o processo de vendas, o preço na linha de proposta é, normalmente, o preço por utilizador e por mês negociado e descontado pelo agente de vendas de TI. Cada negócio tem um número diferente de utilizadores e um número diferente de meses de subscrição. A quantidade utilizada para calcular a linha de proposta é um produto do número de utilizadores e do número de meses de subscrição.

Para suportar este tipo de venda, o Project Operations introduziu o conceito de fatores de quantidade. Os fatores de quantidade dependem dos atributos do produto no Dynamics 365. Quando configura propriedades específicas para um produto, o Project Operations permite-lhe sinalizar um subconjunto de todas as propriedades, como fatores de quantidade.

O Project Operations valida que apenas as propriedades numéricas ou as propriedades de produto que têm um tipo de dados numérico são sinalizadas como fatores de quantidade. Quando adiciona um produto com fatores de quantidade a uma linha de proposta, o campo **Quantidade** torna-se só de leitura. Depois de introduzir valores para propriedades de produto que são fatores de quantidade, o Project Operations calcula a quantidade da linha de proposta.

Por exemplo, o Dynamics 365 Sales poderá ter as seguintes propriedades:

- **N.º de utilizadores**: O número de utilizadores
- **N.º de Meses**: O número de meses da subscrição
- **SKU do Produto**

Pode sinalizar o **N.º de Utilizadores** e **N.º de Meses** como fatores de quantidade editando as propriedades da linha de produto.

Para criar Fatores de quantidade a partir das Propriedades do produto, siga estes passos:

1. No painel de navegação esquerdo do Project Operations, vá para **Vendas** > **Produtos**.
2. Abra o produto para o qual precisa de configurar fatores de quantidade. Certifique-se de que o produto tem propriedades já configuradas.
3. Na página **Informações do Projeto** para o Produto, selecione o separador **Fatores de Quantidade**.
4. Na subgrelha, selecione **+ Novo cálculo do campo**.
5. Introduza o nome do Fator de Quantidade e selecione o valor da propriedade que mapeia para o cálculo do campo.
6. Guarde e feche o formulário. Repita estes passos para todas as propriedades a utilizar para calcular a quantidade da linha de proposta baseada no produto.

Quando cria uma linha de proposta baseada em produtos para um produto, a quantidade da linha de proposta será bloqueada. A quantidade será calculada como um produto dos valores de propriedade que introduzir para essa linha de proposta.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]