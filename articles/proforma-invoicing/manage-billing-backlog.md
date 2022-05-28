---
title: Gerir registo de tarefas pendentes de faturação
description: Este tópico fornece informações sobre como ver e trabalhar com tarefas pendentes de faturação no Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 9837af0d3c0b2476edab35a53092cf95a44e5244
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600015"
---
# <a name="manage-billing-backlog"></a>Gerir registo de tarefas pendentes de faturação

_ **Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados

O Dynamics 365 Project Operations tem vistas dedicadas para ajudar a gerir o registo de tarefas pendentes de faturação. Para gerir o registo de tarefas pendentes de faturação, selecione as ligações na área **Vendas** em **Faturação**. 

Estão disponíveis as seguintes vistas:

- Sinais e Adiantamentos
- Sinais e Adiantamentos disponíveis
- Marcos de Preço Fixo
- Registo de Tarefas Pendentes de Faturação de Tempo e Material

## <a name="retainers-and-advances"></a>Sinais e Adiantamentos

A vista **Retentores e avanços** lista os retentores e os avanços em todos os contratos de projeto. Depois de faturar um sinal ou adiantamento, o montante do adiantamento fica disponível para utilização.

## <a name="available-retainers-and-advances"></a>Sinais e Adiantamentos disponíveis

A vista **Retentores e avanços disponíveis** lista todos os retentores e avanços disponíveis em todos os contratos de projeto. Depois de faturar um sinal ou adiantamento, o montante do adiantamento fica disponível para utilização e é adicionado à lista. Após a quantidade do retentor ou adiantamento ser usada completamente, é removida da lista.

## <a name="fixed-price-milestones"></a>Marcos de Preço Fixo

A vista **Marcos de preço fixo** lista todos os marcos de preço fixo em todos os itens de contrato de projeto. A partir desta vista, os marcos individuais ou múltiplos podem ser marcados como **Pronto para faturar** ou **Não prontos para faturar**. Marcar um marco como **Pronto a faturar** torna-o disponível para ser colocado numa fatura de rascunho.

Quando os itens de contrato de vários clientes têm um método de faturação de preço fixo, é criado um marco para cada cliente no item de contrato. Um marco pode ser criado e, em seguida, dividido em registos de marcos específicos do cliente. Esta divisão é interna e de acordo com a percentagem de faturação dividida definida para cada cliente no item de contrato. Na vista **Marcos de Preço Fixo**, verá os registos de marcos específicos do cliente individuais. Cada um destes registos de marcos pode ser marcado como **Pronto a Faturar** separadamente desta vista. Quando uma ou mais das divisões de marcos relacionadas são marcadas como **Pronto para faturar**, o estado do cabeçalho atualiza-se para **Em progresso** desde **Não iniciado**. Quando todas as divisões de marcos são faturadas, o estado do marco do cabeçalho atualiza-se para **Concluído**.

É mostrado um marco numa fatura de rascunho nesta vista com o estado de faturação de **Fatura de Cliente Criada**. Quando a fatura de rascunho é confirmada, o estado da faturação no registo é atualizado para **Fatura do Cliente Publicada**. 

> [!NOTE] 
> Não atualize este valor de estado utilizando código personalizado. O Project Operations não funciona corretamente quando estes valores de estado são atualizados com código personalizado.

## <a name="time-and-material-billing-backlog"></a>Registo de Tarefas Pendentes de Faturação de Tempo e Material

A vista **Registo de Tarefas Pendentes de Faturação de Tempo e Material** lista todas os valores reais de vendas não faturados em todos os contratos de projeto no sistema que não foram faturados. Os valores reais de vendas não faturados únicos ou múltiplos podem ser marcados como **Pronto a Faturar** ou **Não Pronto a Faturar** a partir desta vista. A marcação de um valor real de vendas não faturado como **Pronto a Faturar** disponibiliza-o para ser colocado numa fatura de rascunho.

Os valores reais de vendas não faturados com um estado **A Não Exceder** de **Falhado** não podem ser marcados como **Pronto a Faturar**. Se os valores reais precisarem de ser marcados como **Pronto a faturar**, reponha o estado noutros valores reais do item de contrato que são cometidos e, em seguida, reavalie o estado **A não exceder**.

Se os itens de contrato de vários clientes tiverem um método de faturação de tempo e material, quando o tempo e as despesas são aprovados, um valor real de vendas não faturado é criado para cada cliente no item de contrato, de acordo com a divisão de percentagem de faturação definida para cada um dos clientes. Na vista **Registo de Tarefas Pendentes de Faturação de Tempo e Material**, verá estes valores reais de vendas não faturados específicos do cliente. Cada um destes registos de valores reais de vendas não faturados pode ser marcado como **Pronto a Faturar** separadamente desta vista.

Um valor real de venda não faturada que está numa fatura de projeto é mostrada nesta vista com um estado de faturação de **fatura de cliente criada**. Quando a fatura de rascunho for confirmada, o estado da faturação neste registo é atualizado para **Fatura de Cliente Publicada**. 

> [!NOTE] 
> Não atualize este valor de estado utilizando código personalizado. O Project Operations não funciona corretamente quando estes valores de estado são atualizados com código personalizado.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
