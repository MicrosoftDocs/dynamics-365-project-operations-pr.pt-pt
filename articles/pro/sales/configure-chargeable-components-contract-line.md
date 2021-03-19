---
title: Configurar componentes faturáveis de um item de contrato baseado em projetos – lite
description: Este tópico fornece informações sobre como adicionar componentes faturáveis a itens de contrato no Project Operations.
author: rumant
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cf3f2a28fc992d6444b35d6ffa0c3f6cadcf16ea
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273932"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line---lite"></a>Configurar componentes faturáveis de um item de contrato baseado em projetos – lite

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

Um item de contrato baseado em projeto tem componentes *incluídos* e componentes *faturáveis*.

Os componentes incluídos são componentes que estão sujeitos a:

  - Método de faturação e divisões de clientes
  - Limites a não exceder 
  - Definições de frequência de fatura definidas no item de contrato baseado em projeto

Um subconjunto dos componentes incluídos pode ser marcado como faturável utilizando o campo **Tipo de Faturação**. O campo **Tipo de Faturação** é um conjunto de opções que permite os seguintes valores no contexto de um item de contrato:

  - Faturável
  - Não faturável

Os componentes faturáveis podem ser definidos nas categorias de tarefas, funções e transações.

A capacidade de faturação é definida em tarefas para um item de contrato de projeto e aplica-se a todas as classes de transação incluídas no item. Se o campo **Incluir Tarefas** num item de contrato estiver em branco ou definido para **Todo o projeto**, o separador **Tarefas faturáveis** não estará disponível.

A capacidade de faturação definida nas funções de um item de contrato de projeto aplica-se apenas à classe de transação **Tempo**. Se o campo **Incluir Tempo** num item de contrato estiver definido para **Não**, o separador **Funções faturáveis** não estará disponível.

A capacidade de faturação definida nas categorias de transação de um item de contrato de projeto aplica-se apenas à classe de transação **Despesa**. Se o campo **Incluir Despesas** estiver definido para **Não**, o separador **Categorias faturáveis** não estará disponível.

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a>Atualizar uma tarefa de projeto como faturável ou não faturável

Uma tarefa do projeto pode ser faturável ou não faturável num item de contrato específico que torna possível a seguinte configuração:

Se um item de contrato baseado em projeto incluir **Tempo** e uma determinada tarefa, **T1** é associado a ela como faturável. Se houver um segundo item de contrato que inclua **Despesas**, pode associar a tarefa T1 ao item de contrato como não faturável. O resultado é que todo o tempo registado na tarefa é faturado e todas as despesas são não faturáveis.

O tipo de faturação de uma tarefa pode ser configurado no separador **Tarefas Faturáveis** de um item de contrato, atualizando o campo **Tipo de Faturação** na subgrelha de tarefas do item de contrato. Em alternativa, pode atualizar o campo **Tipo de Faturação** na subgrelha da configuração de Faturação da tarefa de itens de contrato associados a uma tarefa.

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a>Atualizar uma função de projeto como faturável ou não faturável

Uma função pode ser faturável ou não faturável num item de contrato específico.

O tipo de faturação de uma função pode ser configurado no separador **Funções faturáveis** de um item de contrato. Para isso, atualize o campo **Tipo de Faturação** na subgrelha **Funções Faturáveis**.

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a>Atualizar uma categoria de transação como faturável ou não faturável

Uma categoria de transação pode ser faturável ou não faturável num item de contrato específico.

O tipo de faturação de uma transação pode ser configurado no separador **Categorias faturáveis** de um item de contrato baseado em projeto. Para isso, atualize o campo **Tipo de Faturação** na subgrelha **Categorias Faturáveis**.

### <a name="resolve-chargeability"></a>Resolver a capacidade de faturação

Uma estimativa ou um valor real criado para tempo apenas será considerado faturável se **Tempo** for incluído no item de contrato, e se **Tarefa** e **Função** forem configuradas como faturáveis no item de contrato.

Uma estimativa ou um valor real criado para despesas apenas é considerado faturável se **Despesa** for incluído no item de contrato, e se as categorias **Tarefa** e **Transação** forem configuradas como faturáveis no item de contrato.


| Inclui Tempo | Inclui Despesa | Inclui Tarefas | Função           | Categoria       | Tarefa                                                                                                      |
|---------------|------------------|----------------|----------------|----------------|-----------------------------------------------------------------------------------------------------------|
| Sim           | Sim              | Todo o projeto | Faturável     | Faturável     | Faturação num valor real de Tempo: **Faturável** </br> Tipo de faturação em valor real de Despesas: **Faturável**           |
| Sim           | Sim              | Tarefas selecionadas | Faturável     | Faturável     | Faturação num valor real de Tempo: **Faturável** </br> Tipo de faturação em valor real de Despesas: **Faturável**           |
| Sim           | Sim              | Tarefas selecionadas | Não faturável | Faturável     | Faturação num valor real de Tempo: **Não Faturável** </br> Tipo de faturação em valor real de Despesas: **Faturável**       |
| Sim           | Sim              | Tarefas selecionadas | Faturável     | Faturável     | Faturação num valor real de Tempo: **Não Faturável** </br> Tipo de faturação em valor real de Despesas: **Não Faturável** |
| Sim           | Sim              | Tarefas selecionadas | Não faturável | Faturável     | Faturação num valor real de Tempo: **Não Faturável** </br> Tipo de faturação em valor real de Despesas: **Não Faturável** |
| Sim           | Sim              | Tarefas selecionadas | Não faturável | Não faturável | Faturação num valor real de Tempo: **Não Faturável** </br> Tipo de faturação em valor real de Despesas: **Não Faturável** |
| No            | Sim              | Todo o projeto | Não pode ser definido   | Faturável     | Faturação num valor real de Tempo: **Não disponível**</br>Tipo de faturação em valor real de Despesas: **Faturável**          |
| No            | Sim              | Todo o projeto | Não pode ser definido   | Não faturável | Faturação num valor real de Tempo: **Não disponível**</br> Tipo de faturação em valor real de Despesas: **Não Faturável**     |
| Sim           | No               | Todo o projeto | Faturável     | Não pode ser definido   | Faturação num valor real de Tempo: **Faturável** </br> Tipo de faturação em valor real de Despesas: **Não disponível**        |
| Sim           | No               | Todo o projeto | Não faturável | Não pode ser definido   | Faturação num valor real de Tempo: **Não Faturável** </br>Tipo de faturação em valor real de Despesas: **Não disponível**   |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]