---
title: Linhas de fatura do fornecedor para tempo
description: Este tópico explica como gravar linhas de fatura do fornecedor para os custos de tempo que os subcontratantes colocam.
author: rumant
ms.date: 03/15/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: ac598dff7b0b4a29ac0397a31130ada3b197fe44
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8597214"
---
# <a name="vendor-invoice-lines-for-time"></a>Linhas de fatura do fornecedor para tempo

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

Uma fatura de fornecedor no Microsoft Dynamics 365 Project Operations pode ter linhas de fatura de fornecedor pelo tempo. Os gestores do projeto podem utilizar linhas de fatura de fornecedores para o tempo para gravar os custos do tempo do subcontratante nos projetos.

As linhas de fatura de fornecedor para tempo podem ou não referir-se a item de subcontrato para tempo. Se uma linha de fatura de fornecedor para tempo se referir a um subcontrato, os gestores do projeto poderão fazer corresponder e verificar o tempo que está a ser faturado pelo fornecedor, em relação ao tempo que está registado pelo subcontratante e aprovado pelos gestores do projeto no projeto.

A tabela seguinte fornece informações sobre os campos nas linhas da fatura de fornecedor para tempo.

| Campo | Description | Impacto funcional |
| --- | --- | --- |
| Name | O nome da linha da fatura de fornecedor, para ajudar na identificação. | Este nome será apresentado como a primeira coluna em todas as procuras baseadas em linhas de fatura de fornecedor. |
| Description | Uma breve descrição dos serviços que estão a ser faturados pelo fornecedor na linha da fatura do fornecedor. | None |
| Subcontrato | O subcontrato em que os serviços foram encomendados originalmente. | Quando um subcontrato é selecionado para a fatura do fornecedor, todas as linhas na fatura do fornecedor herdam essa seleção. Uma fatura de fornecedor não pode ter linhas de fatura de fornecedor que se referem a subcontratos diferentes. |
| Item de subcontrato | O item de subcontrato em que os serviços foram encomendados. A lista de itens de subcontrato que podem ser selecionadas está limitada às linhas no subcontrato selecionado. | Quando uma linha de subcontrato é selecionada numa linha de fatura de fornecedor para tempo, os valores predefinidos para os campos **Projeto**, **Função** e **Recurso a reservar** são introduzidos a partir dos campos correspondentes no item de subcontrato. Se o item de subcontrato selecionado tiver valores nos campos **Projeto**, **Função** e **A reservar**, os valores dos campos correspondentes na linha de fatura do fornecedor não diferem desses valores. |
| Data da transação | A data em que o valor real do custo da linha de fatura do fornecedor será registado no projeto. | None |
| Classe de transação | O valor predefinido é **Hora**. | O valor **Tempo** indica que a linha de fatura de fornecedor está a ser utilizada para gravar o montante do tempo do subcontratante. |
| Project | O nome do projeto em que os serviços que estão a ser faturados foram utilizados. | Este campo é obrigatório e não pode ficar em branco. |
| Tarefa | O nome da tarefa do projeto em que os serviços que estão a ser faturados foram utilizados. Este campo só está disponível se um projeto estiver selecionado. A seleção de uma tarefa de projeto é opcional. | Se este campo ficar em branco, o gestor do projeto pode fazer corresponder a linha de fatura do fornecedor ao tempo que está registado pelos recursos do subcontratante em qualquer tarefa do projeto. Se a linha de fatura do fornecedor não referir um item de subcontrato e este campo ficar em branco, o valor real do custo criado pela linha de fatura de fornecedor não será associado a nenhum valor real de vendas não faturado. Neste caso, se a faturação baseada em tarefas estiver configurada, os custos poderão não ser faturados ao cliente final. |
| Função | A função dos recursos do subcontrato cujo tempo está a ser faturado. | Este campo especifica a função executada pelos recursos do subcontrato cujo tempo é faturado na fatura do fornecedor. |
| Recurso reservável | O nome do subcontratante cujo tempo está a ser faturado. A seleção de um recurso a reservar é opcional. | Se este campo ficar em branco, o gestor do projeto pode fazer corresponder a linha de fatura do fornecedor ao tempo que está registado por qualquer recurso que pertence ao fornecedor na linha da fatura do fornecedor. |
| Quantidade | Introduza o número de horas de tempo que está a ser faturado pelo fornecedor na linha da fatura. |None |
| Grupo de unidades | O valor predefinido é **Grupo de unidades de tempo** e não pode ser alterado. | None |
| Unidade | O valor predefinido é a unidade base de horas do grupo de unidades tempo. Pode alterar este valor para comprar qualquer unidade do grupo de unidades tempo, como dia ou semana. | A combinação dos valores **Função** e **Unidade** será utilizada como predefinição ou o valor calculado para o campo **Preço unitário** da linha da fatura de fornecedor. |
| Preço unitário | O preço unitário predefinido utiliza a combinação dos valores **Função** e **Unidade** da lista de preços do projeto aplicável à data de transação da linha de fatura do fornecedor. | Se o preço da lista de preços do projeto aplicável estiver definido numa unidade diferente da unidade na linha de fatura do fornecedor, o sistema utiliza a conversão de unidade para calcular o preço por unidade. |
| Subtotal | Este campo apenas de leitura é calculado como *Quantidade* &times; *Preço unitário*, caso sejam introduzidos os valores tanto no campo **Quantidade** como no campo **Preço unitário**. Se um ou ambos os campos estiverem em branco, pode introduzir um valor neste campo. | None |
| Imposto sobre vendas | Introduza o montante do imposto sobre vendas. | None |
| Montante total | O montante total do linha de fatura do fornecedor, incluindo impostos. Este campo é calculado como *Subtotal* + *Imposto sobre vendas*. | None |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
