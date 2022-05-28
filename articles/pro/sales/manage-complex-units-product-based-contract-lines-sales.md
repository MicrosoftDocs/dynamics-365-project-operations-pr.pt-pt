---
title: Gerir unidades complexas para itens de contrato baseados em produtos – lite
description: Este tópico fornece informações sobre o suporte à venda de produtos baseados em subscrições.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 214593c5b3fbfc5194031af3d3bef59d01750099
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593994"
---
# <a name="manage-complex-units-for-product-based-contract-lines---lite"></a>Gerir unidades complexas para itens de contrato baseados em produtos – lite

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

O Dynamics 365 Project Operations utiliza fatores de quantidade para suportar a venda de produtos baseados em subscrições. Para produtos baseados em subscrições, a quantidade no contrato ou item de contrato do projeto é expressa como o número de meses do utilizador.

O preço do software de subscrição é armazenado no catálogo como o preço por utilizador, por mês. Durante o processo de vendas, o preço no item de contrato é, normalmente, o preço por utilizador e por mês negociado e descontado pelo agente de vendas. Cada negócio tem um número diferente de utilizadores e um número diferente de meses de subscrição. A quantidade utilizada para calcular o montante do item de contrato é um produto do número de utilizadores e do número de meses de subscrição.

Para suportar este tipo de venda, o Project Operations suporta o conceito de *fatores de quantidade*. Os fatores de quantidade dependem dos atributos do produto. Quando configura propriedades específicas para um produto, pode sinalizar um subconjunto dessas propriedades, ou todas as propriedades, como fatores de quantidade.

O Project Operations valida que apenas as propriedades numéricas ou as propriedades de produto que têm um tipo de dados numérico são sinalizadas como fatores de quantidade. Quando um produto com fatores de quantidade configurados é adicionado a um item de contrato, o campo **Quantidade** torna-se apenas de leitura. Depois de introduzir valores para propriedades de produto que são fatores de quantidade, o Project Operations calcula a quantidade do item de contrato.

Por exemplo, o Dynamics 365 Sales poderá ter as seguintes propriedades:

- **N.º de utilizadores**: O número de utilizadores.
- **N.º de Meses**: O número de meses da subscrição.
- **SKU do Produto**: A unidade de armazenamento (SKU) do produto.

O **N.º de Utilizadores** e **N.º de Meses** podem ser sinalizadas como fatores de quantidade editando as propriedades da linha de produto.

Para criar fatores de quantidade a partir de propriedades do produto, complete os seguintes passos.

1. No **Project Operations**, selecione **Produtos de Vendas**.
2. Abra o produto para o qual necessita de configurar fatores de quantidade. Certifique-se de que o produto já tem propriedades configuradas.
3. Na página **Informações do projeto**, selecione o separador **Fatores de Quantidade**.
4. Na subgrelha, selecione **+ Novo cálculo do campo**.
5. Introduza o nome do **Fator de Quantidade** e selecione o valor da propriedade que mapeia para o cálculo do campo.
6. Guarde e feche o formulário.
7. Repita os passos 2-6 para todas as propriedades que, em conjunto, compõem a quantidade do item de contrato baseado em produtos.

Com os fatores de quantidade configurados, quando o utilizador cria um item de contrato para este produto, a quantidade do item de contrato é bloqueado. A quantidade é então calculada como um produto dos valores de propriedade para esse item de contrato.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]