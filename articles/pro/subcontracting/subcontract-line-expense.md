---
title: Itens de subcontrato para as categorias de despesas
description: Este artigo explica como gravar itens de subcontrato para despesas e utilizar os campos para gravar a compra de tempo por parte dos fornecedores.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0b02a8aa0fce7bcb52374c0755d4bb85db16dad3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921040"
---
#  <a name="subcontract-lines-for-expense-categories"></a>Itens de subcontrato para as categorias de despesas

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

Um subcontrato no Dynamics 365 Project Operations pode ter um item para categorias de despesas. Os itens de subcontrato para categorias de despesas permitem que um Gestor de Projeto compre categorias de serviços ou produtos de fornecedores para os quais é possível efetuar a cobrança num projeto.

Execute os seguintes passos para criar um item de subcontrato para as categorias de despesas no Project Operations.

1. No painel de navegação, selecione **Subcontratos** e abra o subcontrato com o qual pretende trabalhar.
2. No separador **Itens de Subcontrato**, selecione **Novo** para criar um novo item.
3. Na página **Criação Rápida**, no campo **Classe de Transação**, selecione **Despesa** e introduza ou selecione quaisquer outras informações necessárias do campo.

A tabela seguinte fornece informações sobre os campos na página de detalhes **Item de subcontrato** e na página **Criação Rápida**.

| **Campo** | **Descrição** | **Impacto funcional** |
| --- | --- | --- |
| Nome | Nome do item de subcontrato para ajudar na identificação. | Será mostrada como a primeira coluna em todas as procuras baseadas em itens de subcontrato. |
| Descrição | Uma breve descrição das categorias de despesas que estão a ser compradas no item de subcontrato. | Nenhuma |
|Tipo da Linha | Este campo tem um valor predefinido de **Baseado na quantidade**. |Nenhuma |
| Método de Faturação | Trata-se de um conjunto de opções que representa os dois modelos de contratação principais suportados pelo Project Operations: **Preço Fixo** e **Horas e Material**. | Uma agenda de faturação baseada em marcos é disponibilizada para itens de subcontrato quando o método de faturação Preço Fixo é selecionado. |
| Classe de Transação | Este campo tem um valor predefinido de **Hora**. Para criar itens de subcontrato para a compra de produtos, defina o campo **Classe de Transação** como **Despesa**.  | Isto indica que o item de subcontrato está a ser utilizado para registar a compra de uma categoria de despesas a utilizar em projetos. |
| Categoria de Transação | Mostra uma lista de categorias de transações ativas no sistema. |Nenhuma |
| Início Solicitado | Introduza a data em que as categorias da compra devem ser disponibilizadas pelo fornecedor. | O início pedido é utilizado para escolher uma lista de preços do projeto a partir das listas de preços de projetos anexadas ao subcontrato. O custo da categoria no item de subcontrato provém dessa lista de preços. |
| Fim Pedido | Introduza a data em que as categorias da compra deixariam de ser necessárias. | Será utilizada para mostrar avisos quando um gestor de projeto está a associar este item de subcontrato a estimativas de despesas específicas no projeto que são necessárias após esta data. |
| Quantidade Encomendada | Quantidade da categoria a comprar ao fornecedor. | Será utilizada para mostrar avisos quando um gestor de projeto excede esta quantidade.|
| Grupo de Unidades | O valor predefinido baseia-se no grupo de unidades predefinido configurado para a categoria selecionada. |Nenhuma |
| Unidade | A predefinição baseia-se na unidade predefinida configurada para a categoria selecionada.  | A combinação de **Categoria** e **Unidade** será utilizada como predefinição ou calculada para o preço unitário do item de subcontrato.  |
| Preço Unitário | O valor predefinido utiliza a combinação de **Categoria** e **Unidade** dos preços de categoria relacionados com a lista de preços do projeto, aplicável ao início pedido do item de subcontrato. |Nenhuma |
| Subtotal | É um campo apenas de leitura que é calculado como Quantidade X Preço unitário, caso sejam introduzidos os valores da quantidade e do preço unitário. Se um ou ambos os campos estiverem em branco, pode introduzir um valor neste campo. |Nenhuma |
| Imposto sobre Vendas | Introduza o montante do imposto sobre vendas. |Nenhuma |
| Montante Total | O montante total do item de subcontrato com os impostos. Este campo é calculado como Subtotal + Imposto sobre vendas. |Nenhuma |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
