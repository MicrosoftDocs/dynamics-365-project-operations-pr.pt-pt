---
title: Configurar os componentes faturáveis de uma linha de proposta
description: Este tópico fornece informações sobre a criação de componentes faturáveis e não faturáveis numa linha de proposta baseada em projetos.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e0b64d7edb21df127bf7544f044de7f3c496dfe3
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082525"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a>Configurar os componentes faturáveis de uma linha de proposta

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

Uma linha de proposta baseada em projeto tem o conceito de componentes *incluídos* e componentes *faturáveis*.

Os componentes incluídos estão sujeitos a:

  - Método de faturação e divisões de clientes
  - Limites a não exceder 
  - Definições de frequência de fatura definidas na linha de proposta baseada em projeto

Um subconjunto dos componentes incluídos pode ser marcado como faturável utilizando o campo **Tipo de Faturação**. O campo **Tipo de Faturação** é um conjunto de opções que permite os seguintes valores no contexto de uma linha de proposta:

  - Faturável
  - Não faturável

Os componentes faturáveis podem ser definidos nas categorias de tarefas, funções e transações.

A capacidade de faturação é definida nas tarefas para uma linha de proposta e aplica-se a todas as classes de transação incluídas na linha. Se o campo **Incluir Tarefas** for definido para **Todo o projeto** ou for deixado em branco, o separador **Tarefas Faturáveis** não está disponível.

A capacidade de faturação é definida nas funções de uma linha de proposta e aplica-se apenas à classe de transação **Tempo**. Se o campo **Incluir Tempo** estiver definido para **Não** numa linha de proposta, o separador **Funções Faturáveis** não está disponível.

A capacidade de faturação é definida nas categorias de transação de uma linha de proposta e aplica-se apenas à classe de transação **Despesa**. Se o campo **Incluir Despesas** estiver definido para **Não** numa linha de proposta, o separador **Categorias Faturáveis** não está disponível.

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a>Atualizar uma tarefa de projeto para faturável ou não faturável

Uma tarefa do projeto pode ser faturável ou não faturável no contexto de uma linha de proposta baseada em projeto específica que torna possível a seguinte configuração:

Se uma linha de proposta baseada em projeto inclui **Tempo** e a tarefa **T1** , a tarefa está associada à linha de proposta como faturável. Se houver uma segunda linha de proposta que inclua **Despesas** , pode associar a tarefa **T1** à linha de proposta como não faturável. O resultado é que todo o tempo registado na tarefa é faturado e todas as despesas registadas na tarefa são não faturáveis.

O tipo de faturação de uma tarefa pode ser configurado no separador **Tarefas Faturáveis** de uma linha de proposta baseada em projeto, atualizando o campo **Tipo de Faturação** na subgrelha **Tarefas da Linha de Proposta**. Em alternativa, pode atualizar o tipo de faturação para a tarefa de projeto no campo **Tipo de Faturação** na subgrelha na configuração de um projeto que mostra as linhas de propostas associados a uma tarefa.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Atualizar uma função de projeto como faturável ou não faturável

Uma função pode ser faturável ou não faturável no contexto de uma linha de proposta específica baseada em projetos.

O tipo de faturação de uma função pode ser configurado no separador **Funções Faturáveis** da linha de proposta, atualizando o campo **Tipo de Faturação** na subgrelha **Funções Faturáveis**.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Atualizar uma categoria de transação como faturável ou não faturável

Uma categoria de transação pode ser faturável ou não faturável numa linha de proposta específica.

O tipo de faturação de uma transação pode ser configurado no separador **Categorias Faturáveis** da linha de proposta, atualizando o campo **Tipo de Faturação** na subgrelha **Categorias Faturáveis**.

### <a name="resolve-chargeability"></a>Resolver a capacidade de faturação
Uma estimativa ou um valor real criado para tempo apenas será considerado faturável se **Tempo** for incluído na linha de proposta, e se **Tarefa** e **Função** forem configuradas como faturáveis na linha de proposta.

Uma estimativa ou um valor real criado para despesas só será considerado faturável se **Despesa** for incluído na linha de proposta, e se **Tarefa** e **Categoria de Transação** forem configuradas como faturáveis na linha de proposta.

| Inclui Tempo | Inclui Despesa | Tarefas Incluídas | Função | Categoria | Tarefa | Faturação |
| --- | --- | --- | --- | --- | --- | --- |
| Sim | Sim | Todo o projeto | Faturável | Faturável | Não pode ser definido | Faturação num valor real de tempo: Faturável </br>Tipo de faturação em valor real de despesas: Faturável |
| Sim | Sim | Apenas tarefas selecionadas | Faturável | Faturável | Faturável | Faturação num valor real de tempo: Faturável</br>Tipo de faturação em valor real de despesas: Faturável |
| Sim | Sim | Apenas tarefas selecionadas | Não faturável | Faturável | Faturável | Faturação num valor real de tempo: Não Faturável</br>Tipo de faturação em valor real de despesas: Faturável |
| Sim | Sim | Apenas tarefas selecionadas | Faturável | Faturável | Não Faturável | Faturação num valor real de tempo: Não Faturável</br> Tipo de faturação em valor real de despesas: Não Faturável |
| Sim | Sim | Apenas tarefas selecionadas | Não Faturável | Faturável | Não Faturável | Faturação num valor real de tempo: Não Faturável</br> Tipo de faturação em valor real de despesas: Não Faturável |
| Sim | Sim | Apenas tarefas selecionadas | Não Faturável | Não Faturável | Faturável | Faturação num valor real de tempo: Não Faturável</br> Tipo de faturação em valor real de despesas: Não Faturável |
| No | Sim | Todo o projeto | Não pode ser definido | Faturável | Não pode ser definido | Faturação num valor real de tempo: Não disponível </br>Tipo de faturação em valor real de despesas: Faturável |
| No | Sim | Todo o projeto | Não pode ser definido | Não faturável | Não pode ser definido | Faturação num valor real de tempo: Não disponível </br>Tipo de faturação em valor real de despesas: Não faturável |
| Sim | No | Todo o projeto | Faturável | Não pode ser definido | Não pode ser definido | Faturação num valor real de tempo: Faturável</br>Tipo de faturação em valor real de despesas: Não disponível |
| Sim | No | Todo o projeto | Não faturável | Não pode ser definido | Não pode ser definido | Faturação num valor real de tempo: Não faturável </br>Tipo de faturação em valor real de despesas: Não disponível |
