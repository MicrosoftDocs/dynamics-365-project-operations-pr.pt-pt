---
title: Cancelar a aprovação de entradas de tempo anteriormente aprovadas
description: Este artigo explica como um gestor de projeto pode cancelar a aprovação de entradas de tempo, despesas ou utilização de material previamente aprovadas.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 08c2248a5fcfc9b7569871a76bc09234ffd172c7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930470"
---
# <a name="cancel-the-approval-of-previously-approved-entries"></a>Cancelar a aprovação de entradas de tempo anteriormente aprovadas

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

Um gestor de projeto ou aprovador que tenha anteriormente aprovado entradas de tempo, despesas ou utilização de material pode cancelar a sua aprovação dessas entradas. 

Siga estes passos para cancelar a aprovação de uma entrada de tempo, despesa ou utilização de material anteriormente aprovada.

1. Aceda a **Projetos** \> **O Meu Trabalho** \> **Aprovações**.
2. A página de lista **Aprovações** mostra todas as entradas de tempo que aguardam aprovação. Altere a vista para **As minhas aprovações anteriores**.
3. Selecione as aprovações de tempo, despesa ou material a cancelar. Em seguida, no Painel de Ações, selecione **Cancelar Aprovação**.
4. Na caixa de mensagem de confirmação que aparece, selecione **OK** para confirmar a operação.

> [!IMPORTANT]
> Não é possível cancelar a aprovação de uma entrada anteriormente aprovada de tempo, despesas ou utilização de material que já tenha sido faturada ao cliente. Se tentar, recebe uma mensagem que indica que não a aprovação não pode ser cancelada porque já foi faturado. Neste caso, só pode cancelar a aprovação se for utilizada uma fatura corretiva para emitir um crédito total ou reembolsar o cliente na fatura original.

## <a name="impact-of-canceling-the-approval-of-a-previously-approved-entry"></a>Impacto de cancelar a aprovação de uma entrada anteriormente aprovada

Quando uma aprovação é cancelada, existe um impacto operacional e um impacto financeiro.

### <a name="operational-impact"></a>Impacto operacional

Se a aprovação de uma entrada for cancelada, o registo de aprovação está marcado como **Submetido**. O estado da entrada é alterado para **Submetido**. Nesta fase, um membro da equipa do projeto pode revocar a entrada sem submeter um pedido de revocação.

O aprovador pode alterar os valores **Quantidade a faturar** e o **Tipo de faturação** e, em seguida, aprovar a entrada mais uma vez.

### <a name="financial-impact"></a>Impacto financeiro

Se a aprovação de uma entrada for cancelada, os valores reais correspondentes de custo e vendas são atualizados da seguinte forma:

- O campo **Estado do Ajuste** é atualizado para **Ajustado**.
- O campo **Estado de Faturação** é atualizado para **Cancelado**.

Em seguida, as entradas de estorno são criadas na tabela Valores Reais. Para criar entradas de estorno, o sistema copia os valores dos campos a partir dos valores reais originais. Os únicos valores que não são copiados são os valores de quantidade. Em vez disso, estes valores são revertidos. Os valores reais estornados são criados para os valores reais de **Custo** e **Vendas Não Faturadas**. O campo **Estado de Ajuste** nos valores reais estornados é definido como **Não ajustável** e o campo **Estado da faturação** é definido como **Cancelado**. Devido a estas alterações, as despesas registadas e o registo de tarefas de receita no projeto já não serão responsáveis pelos valores que estes valores reais representam.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
