---
title: Recuperar entradas de tempo ou despesa aprovadas
description: Este tópico fornece informações sobre como recuperar uma transação de tempo ou despesa aprovada anteriormente.
author: rumant
ms.custom: ''
ms.author: rumant
ms.date: 03/08/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 457aebb00851a1db3e4aa1068f6a825759b8f2e3
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578814"
---
# <a name="recall-approved-time-or-expense-entries"></a>Recuperar entradas de tempo ou despesa aprovadas

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Um membro da equipa do projeto ou outra pessoa que submeta uma entrada de tempo ou despesa pode recuperar a entrada de tempo ou de despesa depois de a mesma ter sido aprovada. O processo para recuperar uma entrada de tempo ou despesa aprovada tem dois passos:

1. Um submissor pede uma recuperação.
2. Um aprovador aprova a recuperação.

## <a name="request-a-recall"></a>Pedir uma recuperação

Siga estes passos para pedir uma recuperação de uma entrada de tempo ou de despesa aprovada.

1. Para as entradas de tempo, aceda a **Projetos** \> **O Meu Trabalho** \> **Entrada de Tempo**.

    –ou–

    Para as entradas de despesa, aceda a **Projetos** \> **O Meu Trabalho** \> **Despesas**.

2. Para as entradas de tempo, selecione todas as entradas de tempo para uma combinação específica de um projeto e uma tarefa. Alternativamente, na grelha, selecione as células individuais para o tempo numa data específica para um projeto específico.

    –ou–

    Para as entradas de despesa, selecione a linha para a entrada de despesa a recuperar.

3. Selecione **Recuperar**. É apresentada uma caixa de diálogo de confirmação. Se as entradas de tempo e despesa selecionadas já tiverem sido aprovadas, é-lhe pedido que introduza um motivo para a recuperação.
4. Introduza um motivo para a recuperação e, em seguida, selecione **OK** para confirmar a operação. O sistema envia a pessoa que aprovou as entradas de um pedido para aprovar a recuperação.

> [!NOTE]
> Apesar de as entradas de tempo e de despesa aprovadas poderem ser recuperadas, se um tempo ou uma despesa aprovado já tiver sido faturado ao cliente, não é possível criar um pedido de recuperação. Um utilizador que tenta criar um pedido de recuperação receberá uma mensagem que indica que não é possível recuperar o tempo ou a despesa porque já foi faturado.

## <a name="approve-or-reject-a-recall-request"></a>Aprovar ou rejeitar um pedido de recuperação

Siga estes passos para aprovar ou rejeitar um pedido de recuperação.

1. Aceda a **Projetos** \> **O Meu Trabalho** \> **Aprovações**.
2. Na página da lista de **Aprovações**, altere a vista para **Pedidos de recuperação para aprovação**. É apresentada uma lista de pedidos de recuperação submetidos.
3. Selecione uma ou mais entradas e, em seguida, selecione **Aprovar** ou **Rejeitar**.
4. Se tiver selecionado **Aprovar**, receberá uma mensagem de aviso que explica o impacto da aprovação. Selecione **OK** para confirmar a operação. O pedido de recuperação é aprovado.

    –ou–

    Se tiver selecionado **Rejeitar**, o pedido de recuperação é rejeitado.

> [!NOTE]
> Como quando uma nova recuperação é pedida, quando uma recuperação é aprovada, o sistema verifica a existência de qualquer atividade de faturação nas entradas de tempo ou despesa. Se uma entrada já tiver sido faturada, ou se estiver numa fatura de rascunho, o aprovador receberá uma mensagem de erro que indica que não é possível aprovar o tempo ou a despesa para a recuperação, porque já estava faturado.

## <a name="impact-of-a-recall-request"></a>Impacto de um pedido de recuperação

Quando uma aprovação é recuperada, existe um impacto operacional e um impacto financeiro.

### <a name="operational-impact"></a>Impacto operacional

Se um pedido de recuperação for aprovado, o registo de aprovação é marcado como **Rejeitado**. O estado da entrada é alterado para **Devolvido** ou **Rejeitado**, dependendo de se é uma entrada de tempo ou uma entrada de despesa.

O membro da equipa do projeto pode ver as entradas, editá-las e, em seguida, voltar a submetê-las ou eliminá-las por completo.

Se um pedido de recuperação for rejeitado, o estado da entrada permanece **Aprovado** e a entrada não pode ser editada pelo membro da equipa do projeto ou pelo aprovador do projeto.

### <a name="financial-impact"></a>Impacto financeiro

Se um pedido de recuperação for aprovado, os valores reais correspondentes de custo e vendas são atualizados da seguinte forma:

- O campo **Estado do Ajuste** é atualizado para **Ajustado**.
- O campo **Estado de Faturação** é atualizado para **Cancelado**.

Em seguida, as entradas de estorno são criadas na tabela Valores Reais. Para criar entradas de estorno, o sistema copia os valores dos campos a partir dos valores reais originais. Os únicos valores que não são copiados são os valores de quantidade. Em vez disso, estes valores são revertidos. Os valores reais estornados são criados para os valores reais de **Custo** e **Vendas Não Faturadas**. O campo **Estado de Ajuste** nos valores reais estornados é definido como **Não ajustável** e o campo **Estado da faturação** é definido como **Cancelado**. Devido a estas alterações, as despesas registadas e o registo de tarefas de receita no projeto já não serão responsáveis pelos valores que estes valores reais representam.

Se um pedido de recuperação for rejeitado, não haverá um impacto financeiro no projeto.

## <a name="changes-to-time-entry-records"></a>Alterações nos registos de entrada de tempo

A ilustração seguinte mostra as alterações que ocorrem para as entradas de tempo aprovadas quando são canceladas.

![Transições de estado de Entrada de Tempo.](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-entry-records"></a>Alterações nos registos de entrada de despesa

A ilustração seguinte mostra as alterações que ocorrem para as entradas de despesa aprovadas quando são canceladas.

![Transições de estado de Entrada de Despesa.](media/ExpenseEntryStateTransitions.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
