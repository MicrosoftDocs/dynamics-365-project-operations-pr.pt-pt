---
title: Linhas da fatura do fornecedor para categorias de despesa
description: Este tópico explica como gravar linhas de fatura do fornecedor para categorias de despesas.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 209460680c9e5c2e39f98ba5c48aa18992775db1
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579550"
---
# <a name="vendor-invoice-lines-for-expense-categories"></a>Linhas da fatura do fornecedor para categorias de despesa

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

Uma fatura de fornecedor no Microsoft Dynamics 365 Project Operations pode ter linhas de fatura de fornecedor para categorias de despesas. Os gestores de projetos podem utilizar linhas de fatura dos fornecedores para categorias de despesas para gravar os custos dos serviços adquiridos como categorias de despesas.

As linhas de fatura de fornecedor para categorias de despesas podem ou não referir-se item de subcontrato para categorias de despesas. Se uma linha de fatura de fornecedor para categorias de despesas se referir a um subcontrato, os gestores do projeto poderão fazer corresponder e verificar as despesas que estão a ser faturadas pelo fornecedor, em relação às despesas são registadas nestas categorias de despesas e aprovadas pelos gestores do projeto no projeto.

A tabela seguinte fornece informações sobre os campos nas linhas da fatura de fornecedor para categorias de despesas.

| Campo | Description | Impacto funcional |
| --- | --- | --- |
| Name | O nome da linha da fatura de fornecedor, para ajudar na identificação. | Este nome será apresentado como a primeira coluna em todas as procuras baseadas em linhas de fatura de fornecedor. |
| Description | Uma breve descrição dos serviços que estão a ser faturados pelo fornecedor na linha da fatura do fornecedor. | None |
| Subcontrato | O subcontrato em que os serviços foram encomendados originalmente. | Quando um subcontrato é selecionado para a fatura do fornecedor, todas as linhas na fatura do fornecedor herdam essa seleção. Uma fatura de fornecedor não pode ter linhas de fatura de fornecedor que se referem a subcontratos diferentes. |
| Item de subcontrato | O item de subcontrato em que os serviços foram encomendados. A lista de itens de subcontrato que podem ser selecionadas está limitada às linhas no subcontrato selecionado. | Quando uma linha de subcontrato é selecionada numa linha de fatura de fornecedor para categorias de despesas, os valores predefinidos para os campos **Projeto**, **Tarefa** e **Categoria de transação** são introduzidos a partir dos campos correspondentes no item de subcontrato. Se o item de subcontrato selecionado tiver valores nos campos **Projeto**, **Tarefa do projeto** e **Categoria de transação**, os valores dos campos correspondentes na linha de fatura do fornecedor não diferem desses valores. |
| Data da transação | A data em que o valor real do custo da linha de fatura do fornecedor será registado no projeto. |None |
| Classe de transação | Selecione **Despesas** para gravar uma fatura de fornecedor para uma categoria de despesas. | O valor **Despesa** indica que a linha de fatura de fornecedor está a ser utilizada para gravar o montante da fatura dos serviços que foram adquiridos como categorias de despesas. |
| Project | O nome do projeto em que os serviços que estão a ser faturados foram utilizados. | Este campo é obrigatório e não pode ficar em branco. |
| Tarefa | O nome da tarefa do projeto em que os serviços que estão a ser faturados foram utilizados. Este campo só está disponível se um projeto estiver selecionado. A seleção de uma tarefa de projeto é opcional. | Se este campo ficar em branco, o gestor do projeto pode fazer corresponder a linha de fatura do fornecedor a despesas que estão registadas em qualquer tarefa do projeto. Se a linha de fatura do fornecedor não referir um item de subcontrato e este campo ficar em branco, o valor real do custo criado pela linha de fatura de fornecedor não será associado a nenhum valor real de vendas não faturado. Neste caso, se a faturação baseada em tarefas estiver configurada, os custos poderão não ser faturados ao cliente final. |
| Categoria de transação | A categoria de transações que está a ser faturada. Tem de ser criada uma categoria de despesas correspondente para a categoria de transação selecionada. | A combinação dos valores **Categoria de transação** e **Unidade** será utilizada como predefinição ou o valor calculado para o campo **Preço unitário** da linha da fatura de fornecedor. |
| Quantidade | Introduza a quantidade que está a ser faturada pelo fornecedor na linha de fatura. |None|
| Grupo de unidades | É inserido um valor predefinido com base no grupo de unidades da categoria de transação selecionada. | None |
| Unidade | O valor predefinido é a unidade base do grupo de unidades que está selecionado. Pode alterar este valor para compra de qualquer unidade do grupo de unidades. | A combinação dos valores **Categoria de transação** e **Unidade** será utilizada como predefinição ou o valor calculado para o campo **Preço unitário** da linha da fatura de fornecedor. |
| Preço unitário | O preço unitário predefinido utiliza a combinação dos valores **Categoria de transação** e **Unidade** da lista de preços do projeto aplicável à data de transação da linha de fatura do fornecedor. | Se o preço da lista de preços do projeto aplicável estiver definido numa unidade diferente da unidade na linha de fatura do fornecedor, o sistema utiliza a conversão de unidade para calcular o preço por unidade. |
| Subtotal | Este campo apenas de leitura é calculado como *Quantidade* &times; *Preço unitário*, caso sejam introduzidos os valores tanto no campo **Quantidade** como no campo **Preço unitário**. Se um ou ambos os campos estiverem em branco, pode introduzir um valor neste campo.| None |
| Imposto sobre vendas | Introduza o montante do imposto sobre vendas. | None |
| Montante total | O montante total do linha de fatura do fornecedor, incluindo impostos. Este campo é calculado como *Subtotal* + *Imposto sobre vendas*. | None |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
