---
title: Gerir o registo de tarefas pendentes de faturação
description: Este tópico fornece informações sobre como ver e trabalhar com tarefas pendentes de faturação no Project Operations.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ec77f3911a460b96414a61bc44ea254f1b7da660
ms.sourcegitcommit: f8edff6422b82fdf2cea897faa6abb51e2c0c3c8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/21/2020
ms.locfileid: "4088056"
---
# <a name="manage-the-billing-backlog"></a>Gerir o registo de tarefas pendentes de faturação

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

O Dynamics 365 Project Operations tem duas vistas dedicadas para o ajudar a trabalhar e gerir as tarefas pendentes de faturação. São **Marcos de Preço Fixo** e **Tarefas Pendentes de Faturação de Tempo e Material** Para selecionar uma vista, na área **Vendas** do Project Operations, na página de navegação à esquerda, selecione **Faturação**. As ligações às tarefas pendentes de faturação estão guardadas lá.

## <a name="fixed-price-milestones"></a>Marcos de Preço Fixo

Esta vista enumera todos os marcos de preço fixo em todas os itens de contrato de projeto no sistema. Os marcos únicos ou múltiplos podem ser marcados como **Pronto a Faturar** ou **Não Pronto a Faturar** a partir desta vista. Quando assinala um marco como **Pronto a Faturar** , o marco fica disponível para uma rascunha de fatura.

Quando os itens de contrato de vários clientes têm um método de faturação de preço fixo, é criado um marco para cada cliente no item de contrato. O utilizador cria um marco e esse marco é dividido em registos de marcos específicos de clientes internamente, de acordo com a percentagem de faturação dividida definida para cada cliente no item de contrato. Na vista **Marcos de Preço Fixo** , verá registos de marcos específicos do cliente individuais. Cada um destes registos de marcos pode ser marcado como **Pronto a Faturar** separadamente desta vista. Quando uma ou mais das divisões de marcos relacionados são marcados como **Prontos a Faturar** , o cabeçalho passa para um estado de **Em Progresso** de **Não Iniciado**. Quando todas as divisões de marcos tiverem sido faturadas, o estado do marco do cabeçalho torna-se **Concluído**.

É mostrado um marco numa fatura de rascunho nesta vista com o estado de faturação de **Fatura de Cliente Criada**. Quando a fatura de rascunho for confirmada, o estado da faturação neste registo é atualizado para **Fatura Publicada**. A atualização deste valor de estado utilizando código personalizado não é recomendada. O Project Operations não funcionará corretamente se estes valores de estado forem atualizados com código personalizado.

## <a name="time-and-material-billing-backlog"></a>Registo de Tarefas Pendentes de Faturação de Tempo e Material

Esta vista lista todos os valores reais de vendas não faturados que não foram faturados em todos os contratos de projeto no sistema. Os valores reais de vendas não faturados únicos ou múltiplos podem ser marcados como **Pronto a Faturar** ou **Não Pronto a Faturar** a partir desta vista. A marcação de um valor real de vendas não faturado como **Pronto a Faturar** disponibiliza-o para ser colocado numa fatura de rascunho.

Os valores reais de vendas não faturados que tenham um estado **A Não Exceder** de **Falhado** não podem ser marcados como **Pronto a Faturar**. Se estes valores reais precisarem de ser marcados como tal, reponha o estado em outros valores reais no item de contrato que são cometidos e, em seguida, avalie o estado **A Não Exceder**.

No caso de itens de contrato com vários clientes que tenham um método de faturação de tempo e material, quando o tempo e as despesas são aprovados, é criado um valor real de vendas não faturado para cada cliente no item de contrato, de acordo com a percentagem de faturação dividida definida para cada cliente no item de contrato. Na vista **Tarefas Pendentes de Faturação de Tempo e Material** , verá estes valores reais de vendas não faturados específicos do cliente. Cada um destes registos de valores reais de vendas não faturados pode ser marcado como **Pronto a Faturar** separadamente desta vista.

É mostrado um valor real de vendas não faturado numa fatura de rascunho nesta vista com um **Estado de Faturação** de **Fatura de Cliente Criada**. Quando a fatura de rascunho for confirmada, o estado da faturação neste registo é atualizado para **Fatura de Cliente Publicada**. A atualização deste valor quando se encontra neste estado utilizando código personalizado não é recomendada. O Project Operations não funcionará corretamente quando estes valores de estado forem atualizados com código personalizado.
