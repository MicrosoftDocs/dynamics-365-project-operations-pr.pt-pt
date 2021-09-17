---
title: Itens de subcontrato para as categorias de despesas
description: Este tópico explica como registar itens de subcontrato para despesas e utilizar os campos para registar a compra de tempo de fornecedores.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9e8e7bb66063dab6db1ac8da1753913aee0ef3fc
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323835"
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

| **Campo** |  **Descrição** |
| ----------| ---------------- |
| Nome | O nome do item de subcontrato. |
| Descrição | Uma breve descrição das categorias de serviços ou produtos que estão a ser compradas no item de subcontrato. |
| Tipo da Linha | Este campo tem um valor predefinido de **Baseado na quantidade**.  |
| Método de Faturação | O método de faturação do item de subcontrato. Com base no método de faturação do item, é disponibilizada uma agenda de faturação baseada em marcos para o método de faturação de preço fixo.  |
| Classe de Transação | Este campo tem um valor predefinido de **Tempo**. Para criar itens de subcontrato para a compra de produtos, defina o campo **Classe de Transação** como **Despesa**. O valor deste campo indica que o item de subcontrato está a ser utilizado para registar uma compra de uma categoria de produtos ou serviços que serão utilizados em projetos. |
| Categoria de Transação | Selecione a categoria de transação. |
| Início Solicitado | A data em que as categorias de compras devem estar disponíveis no fornecedor. A data solicitada é utilizada para escolher uma lista de preços do projeto a partir das listas de preços do projeto anexadas ao subcontrato. O custo da categoria no item de subcontrato assume o valor predefinido a partir dessa lista de preços. |
| Fim solicitado | A data em que as categorias de compras já não serão necessárias. Esta data mostra um aviso quando um gestor de projeto associa este item de subcontrato a estimativas de despesas específicas nos projetos com data posterior à indicada. |
| Quantidade Encomendada | A quantidade da categoria que está a ser comprada ao fornecedor. Quando um gestor de projeto ultrapassa a quantidade comprada, ocorrerá um aviso.  |
| Grupo de Unidades | O valor predefinido deste campo é baseado no grupo de unidades predefinido que está configurado para a categoria selecionada. |
| Unidade | O valor predefinido deste campo é baseado na unidade predefinida que está configurada para a categoria selecionada. A combinação de categoria e unidade é utilizada para predefinir o preço unitário no item de subcontrato. |
| Preço Unitário | O valor do campo de preço unitário é predefinido a partir da combinação de categoria e unidade, a partir dos preços de categorias relacionados com a lista de preços do projeto aplicável ao início solicitado do item de subcontrato.  |
| Subtotal | Este campo só de leitura é calculado automaticamente como o preço unitário segundo a quantidade se existirem os valores de quantidade e de preço unitário. Se um ou ambos os campos estiverem vazios, pode introduzir um valor manualmente neste campo.  |
| Imposto sobre Vendas | Introduza o montante do imposto sobre vendas.  |
| Montante Total | O montante total do item de subcontrato com os impostos. Este campo é calculado como subtotal + imposto sobre vendas.  |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
