---
title: Importar uma estimativa para um item de contrato baseado no projeto
description: Este tópico fornece informações sobre como importar estimativas financeiras de um projeto para um item de contrato.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9ac367baba4529e86a42d812b7d9b2550812e297
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/20/2020
ms.locfileid: "4082637"
---
# <a name="importing-an-estimate-to-a-project-based-contract-line"></a>Importar uma estimativa para um item de contrato baseado no projeto

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

No Dynamics 365 Project Operations, pode importar estimativas de um projeto para um item de contrato baseado em projeto.

1. Verifique se o campo **Projeto** no item de contrato baseado em projeto foi preenchido.
2. No separador **Detalhes do Item de Contrato** , na subgrelha, selecione **Importar a partir da Estimativa do Projeto**. Abre-se uma página de diálogo com opções de resumo. As opções de resumo disponíveis são **Classe de Transação** , **Categoria** , **Função** e **Tarefa do Projeto**.
3. Baseada na seleção do resumo, é copiada a estimativa a partir do projeto para todas as classes de transações e tarefas incluídas neste item de contrato. Para verificar quais as classes de transações incluídas, no separador **Geral** no item de contrato baseado no projeto e verifique os valores **Incluir Tempo** , **Incluir Despesas** e **Incluir Taxas**. 
4. Para ver que tarefas estão incluídas, selecione o separador **Tarefas Faturáveis** no item de contrato. Com base nas tarefas associadas que têm o campo **Classes de Transações Incluídas** definidas como **Sim** , todas as estimativas para essas combinações de tarefas e classe de transação são importadas para o item de contrato.

Quando importa estimativas, o sistema assume a predefinição dos preços baseado nas listas de preços do projeto anexadas ao contrato e o tipo de faturação configurado no item de contrato. Se uma tarefa, função ou categoria for configurada no item de contrato como não faturável, a linha de estimativa importada será não faturável e não será somada ao valor contratado do item de contrato.

Quando um item de contrato tem detalhes de linha, os campos **Valor do Contrato** e **Imposto Estimado** no item de contrato são resumidos e não podem ser editados.

Quando são selecionadas várias opções de resumo, o sistema tenta resumir-se por todas as opções selecionadas. A produção de resumo resulta em mais itens de contrato importados do que se selecionar apenas uma opção de resumo.

Por exemplo, se o projeto tiver as seguintes linhas de estimativa para despesas:

| Tarefa | Categoria | Data | Quantidade | Preço unitário | Montante |
| --- | --- | --- | --- | --- | --- |
| Tarefa A | Tarifa aérea | 10/1/2020 | 4 | 400 | 1600 |
| Tarefa B | Hotel | 10/1/2020 | 4 | 200 | 800 |
| Tarefa C | Hotel | 11/1/2020 | 2 | 200 | 400 |

Quando o utilizador seleciona para resumir pela **Classe Transação** , serão importadas as seguintes informações:

| Tarefa | Categoria | Data | Quantidade | Preço unitário | Montante |
| --- | --- | --- | --- | --- | --- |
| &nbsp; | &nbsp; | 10/1/2020 | 3.34 | 840 | 2800 |

Quando o utilizador seleciona para resumir pela **Classe Transação** e **Categoria** , serão importadas as seguintes informações:

| Tarefa | Categoria | Data | Quantidade | Preço unitário | Montante |
| --- | --- | --- | --- | --- | --- |
| Tarefa A | Tarifa aérea | 10/1/2020 | 4 | 400 | 1600 |
| &nbsp;| Hotel | 10/1/2020 | 6 | 200 | 1200 |

Quando o utilizador seleciona para resumir pela **Classe Transação** , **Categoria** e **Tarefa do Nó de Folha** serão importadas as seguintes informações. Note que este resultado é o mesmo que está no projeto:

| Tarefa | Categoria | Data | Quantidade | Preço unitário | Montante |
| --- | --- | --- | --- | --- | --- |
| Tarefa A | Tarifa aérea | 10/1/2020 | 4 | 400 | 1600 |
| Tarefa B | Hotel | 10/1/2020 | 4 | 200 | 800 |
| Tarefa C | Hotel | 11/1/2020 | 2 | 200 | 400 |