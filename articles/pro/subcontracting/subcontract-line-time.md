---
title: Itens de subcontrato para tempo
description: Este tópico explica como registar itens de subcontrato para tempo e registar a compra de tempo de fornecedores.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 10ebe0fcc86b4652ac01e28108361df1f768b61d
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323880"
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

| **Campo** | **Descrição** |
| --- | --- |
| Nome | O nome do item de subcontrato. |
| Descrição | Uma breve descrição dos serviços que estão a ser comprados no item de subcontrato. | 
| Tipo da Linha | Este campo é um valor predefinido.  |
| Método de Faturação | Selecione o método de faturação. Com base no método de faturação do item de subcontrato referenciado, é disponibilizada uma agenda de faturação baseada em marcos para o método de faturação Preço Fixo. |
| Classe de Transação | Este campo é um valor predefinido que indica se o item de subcontrato está a ser utilizado para registar uma compra de tempo do subcontratante. |
| Função | A função dos recursos de subcontrato cujo tempo está a ser comprado. A função atribuída aos recursos de subcontrato determina o custo da compra. |
| Início Solicitado | A data em que os recursos de subcontrato são necessários para começar a trabalhar. A data solicitada é utilizada para escolher uma lista de preços do projeto a partir das listas de preços do projeto anexadas ao subcontrato. O custo da função no item de subcontrato assume o valor predefinido a partir dessa lista de preços. |
| Fim solicitado | A data em que termina a atribuição dos recursos de subcontrato. Esta data é utilizada para mostrar avisos quando um Gestor de Projeto utiliza esta capacidade para os requisitos de recursos que ocorrem depois desta data. |
| Quantidade Encomendada | O número de horas de Função compradas ao fornecedor. Este valor é utilizado para mostrar avisos quando um Gestor de Projeto ultrapassa esta capacidade para os requisitos de recursos. |
| Grupo de Unidades | O valor predefinido deste campo é o grupo de unidades Tempo e não pode ser alterado.  |
| Unidade | Este campo utiliza como predefinição a unidade base de horas do grupo de unidades Tempo. Pode alterar este valor para comprar qualquer unidade do grupo de unidades Tempo, como dia ou semana. A combinação de Função e Unidade é utilizada para calcular o preço unitário do item de subcontrato. |
| Preço Unitário | O preço unitário é predefinido a partir da combinação de Função e Unidade, a partir da lista de preços do projeto aplicável à data de início solicitada do item de subcontrato. Quando a lista de preços do projeto aplicável tem o preço configurado numa unidade diferente da unidade do item de subcontrato, o sistema utiliza a conversão de unidades para calcular o preço por unidade. |
| Subtotal | Este é um campo só de leitura que é calculado automaticamente como **Quantidade x Preço unitário** se existirem os valores de quantidade e de preço unitário. Se a quantidade, o preço unitário, ou ambos estiverem em branco, pode introduzir um valor no campo. |
| Imposto sobre Vendas |  Introduza o montante do imposto sobre vendas. |
| Montante Total | O montante total do item de subcontrato com os impostos. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
