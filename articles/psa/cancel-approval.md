---
title: Cancelar entradas de tempo e despesa aprovadas anteriormente
description: Este tópico fornece informações sobre como cancelar uma transação de tempo e despesa aprovada do projeto.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: ea42c6755b4b48d986e385879607d659c57f483d
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150592"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a>Cancelar entradas de tempo ou despesa aprovadas anteriormente

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Na versão mais recente do Dynamics 365 Project Service Automation, os aprovadores podem cancelar as entradas de tempo ou despesa que anteriormente aprovaram.

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a>Cancelar uma entrada de tempo ou despesa aprovada anteriormente

Siga estes passos para cancelar uma entrada de tempo ou de despesa que tenha aprovado anteriormente.

1. Aceda a **Projetos** \> **O Meu Trabalho** \> **Aprovações**.
2. Na página da lista de **Aprovações**, altere a vista para **As minhas aprovações passadas**. É apresentada uma lista das entradas de tempo e despesa que aprovou anteriormente.
3. Selecione uma ou mais entradas e, em seguida, selecione **Cancelar aprovação**. Recebe uma mensagem de aviso.
4. Para cancelar a aprovação, selecione **OK**.

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a>Compreender o impacto de cancelar uma aprovação de uma entrada de tempo ou despesa

Quando uma aprovação é cancelada, existe um impacto operacional e um impacto financeiro.

### <a name="operational-impact"></a>Impacto operacional

No lado das operações, quando uma aprovação é cancelada, o estado do registo é reposto para **Rascunho** e a aprovação já não aparece na vista **As minhas aprovações passadas**. Em vez disso, a aprovação cancelada aparece na vista **Entradas de tempo para aprovação** ou na vista **Entradas de despesa para aprovação**, dependendo de se trata de uma entrada de tempo ou de uma entrada de despesa. Além disso, o estado da entrada de tempo ou de despesa relacionada é alterado para **Submetido**, para que a entrada relacionada seja consistente com as aprovações que têm o estado **Rascunho**.

Como aprovador, pode editar alguns dos campos de uma aprovação com um estado de **Rascunho**. Estes campos incluem o **Tipo de Faturação** e **Horas Faturáveis para Entradas de Tempo**. Depois de efetuar as alterações, pode aprovar novamente o registo. Em alternativa, pode rejeitar a entrada. Se rejeitar a aprovação de uma entrada de tempo, o estado da entrada é alterado para **Devolvido**. Se rejeitar a aprovação de uma entrada de despesa, o estado é alterado para **Rejeitado**. Funcionalmente, ambas as entradas devolvidas e rejeitadas têm o mesmo comportamento que uma entrada com o estado de **Rascunho**. Um membro da equipa do projeto pode efetuar quaisquer alterações necessárias na entrada e, em seguida, submetê-la novamente para aprovação ou eliminar a entrada totalmente.

### <a name="financial-impact"></a>Impacto financeiro

Um projeto também é afetado financeiramente quando uma aprovação é cancelada. Primeiro, os valores reais correspondentes de custo e vendas são atualizados da seguinte forma:

- O estado do ajuste é definido como **Ajustado**.
- O estado de faturação é definido como **Cancelado**.

Em seguida, as entradas de estorno são criadas na tabela Valores Reais. Para criar entradas de estorno, o sistema copia os valores dos campos a partir dos valores reais originais. Os únicos valores que não são copiados são os valores de quantidade. Em vez disso, estes valores são revertidos. Os valores reais estornados são criados para os valores reais de **Custo** e **Vendas Não Faturadas**. O campo **Estado de Ajuste** nos valores reais estornados é definido como **Não ajustável** e o estado da faturação é definido como **Cancelado**.

Depois de estas alterações serem efetuadas, o valor que é registado como gasto no projeto e o registo de tarefas pendentes de receita no projeto contabilizarão mais os valores que estes valores reais representam.


[!INCLUDE[footer-include](../includes/footer-banner.md)]