---
title: Linhas de fatura do fornecedor para marcos
description: Este artigo explica como criar linhas de fatura de fornecedor para marcos num subcontrato.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 212d68c32e712ac2349d1670f9e799bcc5144148
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931344"
---
# <a name="vendor-invoice-lines-for-milestones"></a>Linhas de fatura do fornecedor para marcos

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

Uma fatura de fornecedor no Microsoft Dynamics 365 Project Operations pode ter linhas de fatura de fornecedor para marcos que estão definidos numa linha de subcontrato. Os gestores do projeto podem utilizar linhas de fatura do fornecedor para marcos para gravar os custos dos serviços obtidos como custos baseados em marcos incorridos com serviços ou produtos obtidos para o projeto.

Os linhas de fatura do fornecedor para marcos têm sempre de se referir a um subcontrata que tenha um método de faturação de preço fixo. Quando uma linha de fatura de fornecedor para marcos se referir a um item de subcontrato, os gestores do projeto poderão fazer corresponder e verificar os custos subjacentes de tempo, despesas ou materiais que se referem a esse item de subcontrato relativamente ao marco que está a ser faturado pelo fornecedor.

A tabela seguinte fornece informações sobre os campos nas linhas da fatura de fornecedor para marcos.

| Campo | Description | Impacto funcional |
| --- | --- | --- |
| Name | O nome da linha da fatura de fornecedor, para ajudar na identificação. | Este nome será apresentado como a primeira coluna em todas as procuras baseadas em linhas de fatura de fornecedor. |
| Description | Uma breve descrição dos serviços que estão a ser faturados pelo fornecedor na linha da fatura do fornecedor. | None |
| Subcontrato | O subcontrato em que os serviços foram encomendados originalmente. | Quando um subcontrato é selecionado para a fatura do fornecedor, todas as linhas na fatura do fornecedor herdam essa seleção. Uma fatura de fornecedor não pode ter linhas de fatura de fornecedor que se referem a subcontratos diferentes. |
| Item de subcontrato | O item de subcontrato em que os serviços foram encomendados. A lista de itens de subcontrato que podem ser selecionadas está limitada às linhas no subcontrato selecionado. | Quando um item de subcontrato é selecionada num linha de fatura de fornecedor para marcos, os campos **Função** e **Categoria de transação**, assim como campos relacionados com produtos, são irrelevantes e não estão disponíveis. Os campos **Quantidade**, **Unidade** e **Grupo de unidades** também não são relevantes para os campos de fatura do fornecedor baseados em marcos. |
| Data da transação | A data em que o valor real do custo da linha de fatura do fornecedor será registado no projeto. | None |
| Classe de transação | Selecione **Marcos** para gravar uma fatura de fornecedor para um marco concluído que foi definido num item de subcontrato. | None |
| Marco | Selecione o marco definido no item de subcontrato relacionado que está marcado como **Pronto para faturar**. | Os marcos de item de subcontrato que têm um estado de **Pronto para faturar** podem ser selecionados numa linha de fatura do fornecedor. |
| Project | O nome do projeto em que os serviços que estão a ser faturados foram utilizados. | Este campo é obrigatório e não pode ficar em branco. |
| Tarefa | O nome da tarefa do projeto em que os serviços que estão a ser faturados foram utilizados. Este campo só está disponível se um projeto estiver selecionado. A seleção de uma tarefa de projeto é opcional. | Se este campo ficar em branco, o gestor do projeto pode fazer corresponder a linha de fatura do fornecedor à classe de transações no item de subcontrato relacionado que está registado em qualquer tarefa do projeto. Se a linha de fatura do fornecedor não referir um item de subcontrato e este campo ficar em branco, o valor real do custo criado pela linha de fatura de fornecedor não será associado a nenhum valor real de vendas não faturado. Neste caso, se a faturação baseada em tarefas estiver configurada, os custos poderão não ser faturados ao cliente final. |
| Montante do marco | Introduza o valor do marco definido no item de subcontrato que está pronto para ser faturado. | None |
| Imposto sobre vendas | Introduza o montante do imposto sobre vendas. | None |
| Montante total | O montante total do linha de fatura do fornecedor, incluindo impostos. Este campo é calculado como *Montante do marco* + *Imposto sobre vendas*. | None |

> [!NOTE]
> Quando um fornecedor de uma linha de fatura que referencia um marco de item de subcontrato é criado, o estado do marco de subcontrato é atualizado para **Fatura de fornecedor criada**. Em seguida, quando a fatura do fornecedor é confirmada, o estado do marco de item de subcontrato é atualizado para **Fatura do fornecedor confirmada**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
