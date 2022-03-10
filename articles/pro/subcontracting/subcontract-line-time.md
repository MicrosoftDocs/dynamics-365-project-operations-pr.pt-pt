---
title: Itens de subcontrato para tempo
description: Este tópico explica como registar itens de subcontrato para tempo e registar a compra de tempo de fornecedores.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 29b38ec9124502e4283b71d13434b1e0420bc413
ms.sourcegitcommit: 74a7e1c9c338fb8a4b0ad57c5560a88b6e02d0b2
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 09/23/2021
ms.locfileid: "7547258"
---
# <a name="subcontract-lines-for-time"></a>Itens de subcontrato para tempo

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

Um subcontrato no Dynamics 365 Project Operations pode ter um item de subcontrato para tempo. Os itens de subcontrato para tempo permitem que um Gestor de Projeto compre tempo de recursos do fornecedor para as tarefas do projeto e os requisitos de recursos da equipa.

Execute os seguintes passos para criar um item de subcontrato para tempo no Project Operations.

1. No painel de navegação, selecione **Subcontratos** e abra um subcontrato.
2. No separador **Itens de Subcontrato**, selecione **Novo** para criar um novo item de subcontrato.
3. Na página **Criação Rápida**, no campo **Classe de Transação**, selecione **Tempo**.
4. Introduza as informações do campo restantes e, em seguida, selecione **Guardar**.

  A tabela seguinte fornece informações sobre os campos nas páginas **Item de subcontrato** e **Criação Rápida**.

| **Campo** | **Descrição** | **Impacto funcional** |
| --- | --- | --- |
| Nome | Nome do item de subcontrato para ajudar na identificação. | Será mostrada como a primeira coluna em todas as procuras baseadas em itens de subcontrato. |
| Descrição | Uma breve descrição dos serviços que estão a ser comprados no item de subcontrato. |Nenhuma |
| Tipo da Linha |   Este campo tem um valor predefinido de **Baseado na quantidade**.| Nenhuma |
| Método de Faturação | Trata-se de um conjunto de opções que representa os dois modelos de contratação principais suportados pelo Project Operations: **Preço Fixo** e **Horas e Material**. | Com base no método de faturação selecionado, uma agenda de faturação baseada em marcos é disponibilizada para itens de subcontrato com o método de faturação Preço Fixo. |
| Classe de Transação | O valor predefinido é **Hora**. | Indica que o item de subcontrato está a ser utilizado para registar uma compra de horas do subcontratante. |
| Função | Selecione a função dos recursos do subcontrato cujas horas estão a ser compradas. | A função desempenhada pelos recursos do subcontrato determina o custo da compra. |
| Início Solicitado | Introduza a data em que os recursos do subcontratante têm de começar a trabalhar. | Isto é utilizado para escolher uma lista de preços do projeto a partir das listas de preços de projetos anexadas ao subcontrato. O custo da função no item de subcontrato provém dessa lista de preços. |
| Fim Pedido | Introduza a data em que a atribuição do recurso do subcontratante termina. | Será utilizada para mostrar avisos quando um gestor de projeto utiliza capacidade para os requisitos dos recursos que ocorrem após esta data. |
| Quantidade Encomendada | Introduza o número de horas da função que estão a ser compradas ao fornecedor. | Isto será utilizado para mostrar avisos quando um gestor de projeto excede esta capacidade para os requisitos dos recursos. |
| Grupo de Unidades | O valor predefinido é **Grupo de unidade de horas** e não pode ser alterado. | Nenhuma|
| Unidade | A predefinição para este campo é a unidade base de horas do **Grupo de unidades de horas**. Pode alterar este valor para comprar qualquer unidade do **Grupo de unidades de horas**, como dia ou semana. | A combinação de **Função** e **Unidade** será utilizada como predefinição ou calculada para o preço unitário do item de subcontrato. |
| Preço Unitário | O preço unitário predefinido utiliza a combinação de **Função** e **Unidade** da lista de preços do projeto aplicável à data de **Início Pedido** do item de subcontrato. | Quando a lista de preços do projeto aplicável tem o preço configurado numa unidade diferente da unidade do item de subcontrato, o sistema utiliza a conversão de unidades para calcular o preço por unidade. |
| Subtotal |    É um campo só de leitura que é calculado como Quantidade x Preço unitário, caso sejam introduzidos os valores da quantidade e do preço unitário. Se a quantidade, o preço unitário, ou ambos estiverem em branco, pode introduzir um valor no campo. | Nenhuma|
| Imposto sobre Vendas |   Introduza o montante do imposto sobre vendas. |Nenhuma |
| Montante Total | O montante total do item de subcontrato com os impostos. Este campo é calculado como Subtotal + Imposto sobre vendas.|Nenhuma |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
