---
title: Itens de subcontrato para produtos
description: Este artigo explica como gravar itens de subcontrato para produtos e utilizar os vários campos para gravar compras de produtos a fornecedores.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 1ca042eaf95a5e252f00248e83efb959ab3ce801
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522857"
---
# <a name="subcontract-lines-for-products"></a>Itens de subcontrato para produtos

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

Um subcontrato no Dynamics 365 Project Operations pode ter um item de subcontrato para produtos. Estes itens permitem que um Gestor de Projeto compre produtos aos fornecedores que depois podem utilizar nas tarefas de projeto.

Execute os seguintes passos para criar um item de subcontrato para produtos no Project Operations.

1. Na página de navegação, selecione **Subcontratos** e, em seguida, abra o subcontrato com o qual pretende trabalhar. 
2. No separador **Itens de Subcontrato**, selecione **+ Novo** para criar um novo item de subcontrato.
3. Na página **Criação Rápida**, no campo **Classe de Transação**, selecione **Material** e introduza ou selecione as informações necessárias do campo. 
4. Selecione **Guardar**.

A tabela seguinte fornece informações sobre os campos na página **Detalhes de item de subcontrato** e na página **Criação rápida**, uma vez que são relevantes para a compra de produtos.

| Campo | Descrição | Impacto funcional|
| ----- | ----------- | ----------- |
| Nome | Nome do item de subcontrato para ajudar na identificação. |Será mostrada como a primeira coluna em todas as procuras baseadas em itens de subcontrato.
| Descrição | Uma breve descrição dos produtos que estão a ser encomendados no item de subcontrato. | Nenhuma |
| Tipo da Linha | Este campo tem um valor predefinido de **Baseado na quantidade**. |Nenhuma |
| Método de Faturação | Trata-se de um conjunto de opções que representa os dois modelos de contratação principais suportados pelo Project Operations: **Preço Fixo** e **Horas e Material**. | Com base no método de faturação selecionado, uma agenda de faturação baseada em marcos é disponibilizada para itens de subcontrato com o método de faturação Preço Fixo. |
| Classe de Transação |Este campo tem um valor predefinido de **Hora**. Para criar itens de subcontrato para a compra de produtos, defina o campo **Classe da Transação** como **Material**.  | Isto indica que o item de subcontrato está a ser utilizado para registar a compra de produtos a utilizar em projetos. |
| Selecionar Produto | Selecione se o produto que está a ser comprado faz parte do catálogo de produtos ou se é um produto acrescentado manualmente. |Nenhuma |
| Produto | Selecione um produto ativo do catálogo. Este campo só está disponível quando **Selecionar Produto** está definido como **Existente**. |A combinação de **Produto** e **Unidade** será utilizada como predefinição ou calculada para o preço unitário do item de subcontrato.
| Produto Acrescentado Manualmente | Introduza o nome do produto acrescentado manualmente. Este campo só está disponível quando **Selecionar Produto** está definido como **Acrescentado Manualmente**.  |O preço de compra não será preenchido automaticamente para produtos acrescentados manualmente.|
| Data de Entrega Pretendida | Introduza a data de entrega necessária para os produtos.| Esta data é também utilizada para escolher uma lista de preços do projeto a partir das listas de preços do projeto anexadas ao subcontrato. O custo do produto no item de subcontrato assume o valor predefinido a partir dessa lista de preços. |
| Data de entrega contratada | Introduza a data de entrega dos produtos acordada no contrato.  |Nenhuma|
| Quantidade Encomendada | Introduza a quantidade de produto que está a ser comprada ao fornecedor.| Será utilizada para mostrar avisos quando um gestor de projeto excede esta quantidade.|
| Grupo de Unidades | Este valor é predefinido apenas para os produtos de catálogo. |Quando as opções **Produto** e **Data de entrega pretendida** estão selecionadas, o sistema escolhe a lista de preços aplicável com base na data de entrega. Os itens da lista de preços relacionados são consultados para o produto correspondente. Os valores de unidade e de grupo de unidades são predefinidos a partir da configuração no registo do item da lista de preços. |
| Unidade | Por predefinição, este valor assume a unidade configurada no registo do item da lista de preços. Se necessário, pode alterar para outra unidade.| A combinação de produto e unidade é utilizada para predefinir o preço unitário no item de subcontrato para os produtos de catálogo existentes. |
| Preço Unitário | O preço unitário é predefinido utilizando a combinação de produto e unidade a partir dos itens da lista de preços relacionados com a lista de preços do projeto aplicável à data de entrega pretendida do item de subcontrato.  |Nenhuma |
| Subtotal | Este campo só de leitura é calculado como Quantidade x Preço Unitário, se existirem valores introduzidos em ambos os campos. Se o campo **Quantidade**, o campo **Preço unitário**, ou ambos estiverem vazios, pode introduzir um valor manualmente.  |Nenhuma |
| Imposto sobre Vendas | Introduza o valor do imposto sobre vendas. |Nenhuma |
| Montante Total | Este campo calculado mostra o montante total do item de subcontrato depois de incluir os impostos. O valor neste campo é calculado como Subtotal + Imposto. |Nenhuma |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
