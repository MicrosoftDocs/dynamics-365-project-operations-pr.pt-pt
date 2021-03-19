---
title: Importar estimativas de um projeto para a linha de proposta baseada no projeto
description: Este tópico fornece informações sobre como importar estimativas de um projeto para uma linha de proposta.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b32ac22188922a56fa13ea67e0ead77b9b045d9f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278342"
---
# <a name="import-estimates-for-a-project-to-a-project-based-quote-line"></a>Importar estimativas de um projeto para a linha de proposta baseada no projeto

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_


Se um projeto for criado durante a fase de pré-venda, poderá selecionar para importar a estimativa financeira a partir do projeto para a linha de proposta baseada no projeto.

1. Certifique-se de que a linha de proposta baseada em projetos tem a informação do projeto no campo **Projeto**.
2. No separador **Detalhes de linha de proposta**, selecione **Importar a partir da Estimativa do Projeto**.
3. Na caixa de diálogo que é aberta, selecione uma das seguintes opções de resumo:

  - **Classe de transação**
  - **Categoria**
  - **Função** 
  - **Tarefa de projeto**

Baseada na sua seleção, é copiada a estimativa a partir do projeto para todas as classes de transações incluídas nesta linha de proposta. Para verificar quais as classes de transações incluídas, selecione o separador **Geral** na linha de proposta baseada no projeto e verifique os valores de **Incluir Tempo**, **Incluir Despesas** e **Incluir Taxas**.

Quando importa estimativas, o sistema assumirá por predefinição os preços baseado nas listas de preços do projeto anexadas à proposta e o tipo de faturação configurado na linha de proposta baseada no projeto. Se uma função ou categoria for configurada na linha de proposta baseada no projeto como não faturável, a linha de estimativa importada será definida como não faturável e não será somada ao valor proposto da linha de proposta.

Quando uma linha de proposta tem detalhes de linha, os campos **Valor da Proposta** e **Imposto Estimado** na linha de proposta são resumidos e não podem ser editados.

Quando são selecionadas várias opções de resumo, o sistema tenta resumir-se por todas as opções selecionadas. O resultado é que as linhas de proposta importadas será mais do que se selecionar apenas uma opção de resumo.

Por exemplo, se o projeto tiver as seguintes linhas de estimativa para despesas.

| Tarefa | Categoria | Data | Quantidade | Preço unitário | Montante |
| --- | --- | --- | --- | --- | --- |
| Tarefa A | Tarifa aérea | 10/1/2020 | 4 | 400 | 1600 |
| Tarefa B | Hotel | 10/1/2020 | 4 | 200 | 800 |
| Tarefa C | Hotel | 11/1/2020 | 2 | 200 | 400 |

Quando o utilizador seleciona para resumir pela classe Transação, serão importadas as seguintes informações.

| Tarefa | Categoria | Data | Quantidade | Preço unitário | Montante |
| --- | --- | --- | --- | --- | --- |
| | | 10/1/2020 | 3.34 | 840 | 2800 |

Quando o utilizador seleciona para resumir pela classe Transação e Categoria, serão importadas as seguintes informações.

| Tarefa | Categoria | Data | Quantidade | Preço unitário | Montante |
| --- | --- | --- | --- | --- | --- |
| Tarefa A | Tarifa aérea | 10/1/2020 | 4 | 400 | 1600 |
| | Hotel | 10/1/2020 | 6 | 200 | 1200 |

Quando o utilizador seleciona para resumir pela classe Transação, Categoria e Tarefa do Nó de Folha serão importadas as seguintes informações. Note que este resultado é o mesmo que estava no projeto.

| Tarefa | Categoria | Data | Quantidade | Preço unitário | Montante |
| --- | --- | --- | --- | --- | --- |
| Tarefa A | Tarifa aérea | 10/1/2020 | 4 | 400 | 1600 |
| Tarefa B | Hotel | 10/1/2020 | 4 | 200 | 800 |
| Tarefa C | Hotel | 11/1/2020 | 2 | 200 | 400 |


[!INCLUDE[footer-include](../includes/footer-banner.md)]