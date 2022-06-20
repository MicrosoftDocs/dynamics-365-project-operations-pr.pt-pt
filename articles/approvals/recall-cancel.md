---
title: Revocar entradas anteriormente aprovadas
description: Este artigo explica de que forma um membro da equipa do projeto pode pedir a revocação dos dados de tempo, despesas e utilização de materiais submetidos e aprovados anteriormente, bem como a forma como um gestor do projeto pode aprovar ou rejeitar pedidos de revocação.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 54fc7ac2301a4423ebf70b0b67ad489580c347b5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930378"
---
# <a name="recall-previously-approved-entries"></a>Revocar entradas anteriormente aprovadas

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

Um membro da equipa do projeto que submeta uma entrada de tempo ou utilização de material pode revocar essa entrada depois de a mesma ter sido aprovada. O processo de revocação tem dois passos principais:

1. Um submissor pede uma recuperação.
2. Um aprovador aprova o pedido de revocação.

## <a name="request-a-recall"></a>Pedir uma recuperação

Siga estes passos para pedir uma revocação de uma entrada de tempo, despesa ou utilização de material aprovada.

1. Siga um destes passos, dependendo do tipo de entrada que pretende revocar:

    - Para entradas de tempo, aceda a **Projetos** \> **O meu trabalho** \> **Entrada de tempo** e selecione todas as entradas de tempo para uma combinação específica de um projeto e uma tarefa. Alternativamente, na grelha, selecione as células individuais para o tempo numa data específica para um projeto específico.
    - Para entradas de despesa, aceda a **Projetos** \> **O meu trabalho** \> **Despesas** e selecione a linha para a entrada de despesa a revocar.
    - Para entradas de utilização de material, aceda a **Projetos** \> **O meu trabalho** \> **Registo de utilização de material** e selecione a linha para a entrada de utilização de material a revocar.

2. Selecione **Recuperar**. É apresentada uma caixa de diálogo de confirmação. Se as entradas de tempo, despesa e utilização de material selecionadas já tiverem sido aprovadas, é-lhe pedido que introduza um motivo para a revocação.
3. Introduza um motivo para a recuperação e, em seguida, selecione **OK** para confirmar a operação. O sistema envia a pessoa que aprovou as entradas de um pedido para aprovar a recuperação.

> [!IMPORTANT]
> Não é possível criar um pedido de revocação para uma entrada de utilização de tempo, despesas ou material aprovada que já tenha sido faturada ao cliente. Se tentar, recebe uma mensagem que indica que não é possível revocar o tempo, despesa ou utilização de material porque já foi faturado. Neste caso, só pode pedir uma revocação da entrada se for utilizada uma fatura corretiva para emitir um crédito total ou reembolsar o cliente na fatura original.

## <a name="approve-or-reject-a-recall-request"></a>Aprovar ou rejeitar um pedido de recuperação

Siga estes passos para aprovar ou rejeitar um pedido de recuperação.

1. Aceda a **Projetos** \> **O Meu Trabalho** \> **Aprovações**.
2. Na página da lista de **Aprovações**, altere a vista para **Pedidos de recuperação para aprovação**. É apresentada uma lista de pedidos de recuperação submetidos.
3. Selecione uma ou mais entradas e, em seguida, selecione **Aprovar** ou **Rejeitar**.
4. Se tiver selecionado **Aprovar**, receberá uma mensagem de aviso que explica o impacto da aprovação. Selecione **OK** para confirmar a operação. O pedido de recuperação é aprovado.

    –ou–

    Se tiver selecionado **Rejeitar**, o pedido de recuperação é rejeitado.

> [!IMPORTANT]
> Quando uma revocação é aprovada, tal como quando é pedida, o sistema verifica a existência de qualquer atividade de faturação nas entradas de tempo, despesa ou utilização de material. Se uma entrada já tiver sido faturada, ou se estiver numa fatura de rascunho, o aprovador recebe uma mensagem de erro que indica que não é possível aprovar o tempo ou a despesa para a revocação, porque já estava faturado. Neste caso, o aprovador pode aprovar a revocação apenas se uma fatura corretiva for utilizada para emitir um crédito total ou reembolsar o cliente na fatura original.

## <a name="impact-of-a-recall-request"></a>Impacto de um pedido de recuperação

Quando uma aprovação é recuperada, existe um impacto operacional e um impacto financeiro.

### <a name="operational-impact"></a>Impacto operacional

Se um pedido de recuperação for aprovado, o registo de aprovação é marcado como **Rejeitado**. O estado da entrada é alterado para **Devolvido** ou **Rejeitado**, dependendo se é uma entrada de tempo, despesa ou utilização de material.

O membro da equipa do projeto pode ver as entradas, editá-las e, em seguida, voltar a submetê-las ou eliminá-las na totalidade.

Se um pedido de recuperação for rejeitado, o estado da entrada permanece **Aprovado** e a entrada não pode ser editada pelo membro da equipa do projeto ou pelo aprovador do projeto.

### <a name="financial-impact"></a>Impacto financeiro

Se um pedido de recuperação for aprovado, os valores reais correspondentes de custo e vendas são atualizados da seguinte forma:

- O campo **Estado do Ajuste** é atualizado para **Ajustado**.
- O campo **Estado de Faturação** é atualizado para **Cancelado**.

Em seguida, as entradas de estorno são criadas na tabela Valores Reais. Para criar entradas de estorno, o sistema copia os valores dos campos a partir dos valores reais originais. Os únicos valores que não são copiados são os valores de quantidade. Em vez disso, estes valores são revertidos. Os valores reais estornados são criados para os valores reais de **Custo** e **Vendas Não Faturadas**. O campo **Estado de Ajuste** nos valores reais estornados é definido como **Não ajustável** e o campo **Estado da faturação** é definido como **Cancelado**. Devido a estas alterações, as despesas registadas e o registo de tarefas de receita no projeto já não serão responsáveis pelos valores que estes valores reais representam.

Se um pedido de recuperação for rejeitado, não haverá um impacto financeiro no projeto.

## <a name="changes-to-time-entry-records"></a>Alterações nos registos de entrada de tempo

A ilustração seguinte mostra as alterações que ocorrem para as entradas de tempo aprovadas e os registos de aprovação correspondentes quando são revocadas.

![Transições de estado de entrada de tempo.](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-and-material-usage-entry-records"></a>Alterações nos registos de entrada de despesa e utilização de material

A ilustração seguinte mostra as alterações que ocorrem para as entradas de despesas e utilização de material aprovadas e os registos de aprovação correspondentes quando são revocadas.

![Transições de estado de entrada de despesa.](media/ExpenseEntryStateTransitions.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
