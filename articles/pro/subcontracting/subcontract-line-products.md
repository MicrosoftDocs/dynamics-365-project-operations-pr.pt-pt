---
title: Itens de subcontrato para produtos
description: Este tópico explica como registar itens de subcontrato para produtos e utilizar os diversos campos para registar as compras de produtos aos fornecedores.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c0ddc39638ae9830eacc57f3e1def75aa36e6553
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323700"
---
# <a name="subcontract-lines-for-products"></a>Itens de subcontrato para produtos

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

Um subcontrato no Dynamics 365 Project Operations pode ter um item de subcontrato para produtos. Estes itens permitem que um Gestor de Projeto compre produtos aos fornecedores que depois podem utilizar nas tarefas de projeto.

Execute os seguintes passos para criar um item de subcontrato para produtos no Project Operations.

1. Na página de navegação, selecione **Subcontratos** e, em seguida, abra o subcontrato com o qual pretende trabalhar. 
2. No separador **Itens de Subcontrato**, selecione **+ Novo** para criar um novo item de subcontrato.
3. Na página **Criação Rápida**, no campo **Classe de Transação**, selecione **Material** e introduza ou selecione as informações necessárias do campo. 
4. Selecione **Guardar**.

A tabela seguinte fornece informações sobre os campos na página **Detalhes de item de subcontrato** e na página **Criação rápida**, uma vez que são relevantes para a compra de produtos.

| Campo | Descrição |
| ----- | ----------- |
| Nome | O nome do item de subcontrato. |
| Descrição | Uma breve descrição dos produtos que estão a ser encomendados no item de subcontrato. |
| Tipo da Linha | O valor predefinido deste campo é **Baseado na quantidade**. |
| Método de Faturação |  O método de faturação do item de subcontrato. Está disponível uma agenda de faturação baseada em marcos para os métodos de faturação de preço fixo. |
| Classe de Transação | O valor predefinido deste campo é **Tempo**. Para criar itens de subcontrato para a compra de produtos, no campo **Classe de Transação**, selecione **Material**. Esta seleção indica que o item de subcontrato é utilizado para registar uma compra de produtos que serão utilizados em projetos. |
| Selecionar Produto | Selecione se o produto que está a ser comprado faz parte do catálogo de produtos ou se é um produto acrescentado manualmente. |
| Produto | Selecione um produto ativo do catálogo. Este campo só está disponível quando **Selecionar Produto** está definido como **Existente**. |
| Produto Acrescentado Manualmente | Introduza o nome do produto acrescentado manualmente. Este campo só está disponível quando **Selecionar Produto** está definido como **Acrescentado Manualmente**.  |
| Data de Entrega Pretendida | Selecione a data de entrega necessária para os produtos. Esta data é também utilizada para escolher uma lista de preços do projeto a partir das listas de preços do projeto anexadas ao subcontrato. O custo do produto no item de subcontrato assume o valor predefinido a partir dessa lista de preços. |
| Data de entrega contratada | Selecione a data de entrega dos produtos, conforme acordado no contrato.  |
| Quantidade Encomendada | Introduza a quantidade de produto que está a ser comprada ao fornecedor. Se um Gestor de Projeto ultrapassar esta quantidade, ocorrerá um aviso. |
| Grupo de Unidades | Este valor é predefinido apenas para os produtos de catálogo. Quando as opções **Produto** e **Data de entrega pretendida** estão selecionadas, o sistema escolhe a lista de preços aplicável com base na data de entrega. Os itens da lista de preços relacionados são consultados para o produto correspondente. Os valores de unidade e de grupo de unidades são predefinidos a partir da configuração no registo do item da lista de preços. |
| Unidade | Este valor é predefinido para a configuração da unidade no registo do item da lista de preços. Se necessário, pode alterar para outra unidade. A combinação de produto e unidade é utilizada para predefinir o preço unitário no item de subcontrato para os produtos de catálogo existentes. |
| Preço Unitário | O preço unitário é predefinido utilizando a combinação de produto e unidade a partir dos itens da lista de preços relacionados com a lista de preços do projeto aplicável à data de entrega pretendida do item de subcontrato.  |
| Subtotal | Este campo só de leitura é calculado como Quantidade x Preço Unitário, se existirem valores introduzidos em ambos os campos. Se o campo **Quantidade**, o campo **Preço unitário**, ou ambos estiverem vazios, pode introduzir um valor manualmente.  |
| Imposto sobre Vendas | Introduza o valor do imposto sobre vendas. |
| Montante Total | Este campo calculado mostra o montante total do item de subcontrato depois de incluir os impostos. O valor neste campo é calculado como subtotal + imposto. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
