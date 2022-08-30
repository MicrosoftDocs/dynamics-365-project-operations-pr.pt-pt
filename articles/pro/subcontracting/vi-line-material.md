---
title: Linhas de fatura do fornecedor para produtos
description: Este artigo explica como gravar linhas de fatura de fornecedores para produtos e utilizar os diferentes campos para gravar compras de produtos a fornecedores.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d38a447c576c095a7bbe2f5ed84342a88bf69a9b
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261573"
---
# <a name="vendor-invoice-lines-for-products"></a>Linhas de fatura do fornecedor para produtos

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

Uma fatura de fornecedor no Microsoft Dynamics 365 Project Operations pode ter linhas de fatura de fornecedor para produtos (também referidos como materiais). Os gestores do projeto podem utilizar linhas de fatura de fornecedores para produtos para gravar os custos dos produtos que foram adquiridos em projetos.

As linhas de fatura de fornecedor para produtos podem ou não referir-se a item de subcontrato para materiais. Se uma linha de fatura de fornecedor se referir a um subcontrato, os gestores do projeto poderão fazer corresponder e verificar os produtos que estão a ser faturados pelo fornecedor, em relação à utilização de produtos adquiridos que são registados e aprovados pelos gestores do projeto.

A tabela seguinte fornece informações sobre os campos nas linhas da fatura de fornecedor para produtos.

| Campo | Description | Impacto funcional |
| --- | --- | --- |
| Name | O nome da linha da fatura de fornecedor, para ajudar na identificação. | Este nome será apresentado como a primeira coluna em todas as procuras baseadas em linhas de fatura de fornecedor. |
| Description | Uma breve descrição dos produtos que estão a ser faturados pelo fornecedor na linha da fatura do fornecedor. | None |
| Subcontrato | O subcontrato em que os produtos foram encomendados originalmente. | Quando um subcontrato é selecionado para a fatura do fornecedor, todas as linhas na fatura do fornecedor herdam essa seleção. Uma fatura de fornecedor não pode ter linhas de fatura de fornecedor que se referem a subcontratos diferentes. |
| Item de subcontrato | A linha de subcontrato em que os produtos foram encomendados. A lista de itens de subcontrato que podem ser selecionadas está limitada às linhas no subcontrato selecionado. | Quando uma linha de subcontrato é selecionada numa linha de fatura de fornecedor para produtos, os valores predefinidos para os campos **Projeto**, **Tarefa** e **Produto** são introduzidos a partir dos campos correspondentes no item de subcontrato. Se o item de subcontrato selecionado tiver valores nos campos **Projeto**, **Tarefa** e **Produto**, os valores dos campos correspondentes na linha de fatura do fornecedor não diferem desses valores. |
| Data da transação | A data em que o valor real do custo da linha de fatura do fornecedor será registado no projeto. | None|
| Classe de transação | Quando os produtos são faturados, este campo deve estar definido como **Material**. | O valor **Material** indica que a linha de fatura de fornecedor está a ser utilizada para gravar o montante da fatura dos materiais que foram adquiridos. |
| Project | O nome do projeto em que os produtos que estão a ser faturados foram utilizados. | Este campo é obrigatório e não pode ficar em branco. |
| Tarefa | O nome da tarefa do projeto em que os produtos que estão a ser faturados foram utilizados. Este campo só está disponível se um projeto estiver selecionado. A seleção de uma tarefa de projeto é opcional. | Se este campo ficar em branco, o gestor do projeto pode faer corresponder a linha de fatura do fornecedor ao produto comprado que é utilizado em qualquer tarefa do projeto. Se a linha de fatura do fornecedor não referir um item de subcontrato e este campo ficar em branco, o valor real do custo criado pela linha de fatura de fornecedor não será associado a nenhum valor real de vendas não faturado. Neste caso, se a faturação baseada em tarefas estiver configurada, os custos não poderão ser faturados ao cliente final. |
| Selecionar produto | Selecione se o produto que está a ser faturado é um produto existente a partir do catálogo ou um produto acrescentado manualmente. | O valor predefinido é inserido a partir da linha de subcontrato quando uma linha de subcontrato está selecionada. |
| Produto | Selecione o produto do catálogo. Se o produto for um produto acrescentado manualmente, introduza o nome do produto. | Este campo é utilizado para inserir preços de compra predefinidos para produtos existentes. |
| Quantidade | Introduza a quantidade de material que está a ser faturado pelo fornecedor nesta linha de fatura. | None |
| Grupo de unidades | Selecione o grupo de unidades da unidade da quantidade que está a ser faturada. | None |
| Unidade | O valor predefinido é a unidade base do grupo de unidades que está selecionado. Pode alterar este valor para pagamento em qualquer unidade do grupo de unidades selecionada. | A combinação dos valores **Produto** e **Unidade** será utilizada como predefinição ou o valor calculado para o campo **Preço unitário** da linha da fatura de fornecedor. |
| Preço unitário | O preço unitário predefinido utiliza a combinação dos valores **Produto** e **Unidade** da lista de preços do projeto aplicável à data de transação da linha de fatura do fornecedor. | None |
| Subtotal | Este campo apenas de leitura é calculado como *Quantidade* &times; *Preço unitário*, caso sejam introduzidos os valores tanto no campo **Quantidade** como no campo **Preço unitário**. Se um ou ambos os campos estiverem em branco, pode introduzir um valor neste campo. | None |
| Imposto sobre vendas | Introduza o montante do imposto sobre vendas. | None |
| Montante total | O montante total do linha de fatura do fornecedor, incluindo impostos. Este campo é calculado como *Subtotal* + *Imposto sobre vendas*. | None |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
