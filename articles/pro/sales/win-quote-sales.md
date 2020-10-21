---
title: Fechar propostas
description: Este tópico fornece informações sobre como fechar uma proposta no Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cc3b2cdeb1ac46b7d927c1f96e94e9154d3eebf8
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896205"
---
# <a name="close-quotes"></a>Fechar propostas 

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

Uma proposta de projeto pode ser fechada como Ganha ou Perdida. As operações Ativar e Rever em propostas não são suportadas no Microsoft Dynamics 365 Project Operations, pelo que uma proposta de rascunho pode ser fechada.

## <a name="close-a-quote-as-won"></a>Fechar uma proposta como Ganha

Fechar uma proposta de projeto como Ganha fechará a proposta com o estado definido como Fechado e a razão do estado definida como Ganha. Fechar a proposta torna a proposta de projeto só de leitura e cria um contrato de projeto de rascunho que contém as informações da proposta. Como uma proposta fechada não pode ser reaberta, existe uma caixa de diálogo de confirmação antes de as alterações serem feitas, uma vez que uma proposta fechada não pode ser reaberta e as alterações são irreversíveis.

Se a proposta estiver anexada a uma oportunidade, quaisquer outras propostas de projeto na oportunidade são fechadas automaticamente como Perdidas.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Impacto financeiro de fechar uma proposta como Ganha

Se tiverem existido valores reais para o tempo registado num projeto enquanto ainda está anexado a uma proposta de rascunho, só o custo do tempo ou da despesa é registado. Depois de uma proposta ser fechada como Ganha, a aplicação irá refatorizar os custos ao inverter os valores reais do custo mais antigos e recriar novos custos reais. A aplicação irá processar estes valores reais de custos baseados no método de Faturação do item de contrato do projeto associado. Se os valores reais do custo referenciarem um item de contrato de tempo e material, o sistema criará automaticamente as vendas não faturadas correspondentes para quando a proposta estiver fechada e o contrato de projeto for criado. Se os valores reais do custo referenciam um item de contrato de preço fixo, a aplicação deixará de reprocessar os valores reais do custo baseado nas regras de faturação dividida para os clientes do contrato de projeto.

## <a name="closing-a-quote-as-lost"></a>Fechar uma proposta como perdida:

Fechar uma proposta de projeto como Perdida definirá o estado como Fechada e a razão do estado como Perdida. Fechar a proposta faz com que a proposta de projeto seja só de leitura. Como uma proposta fechada não pode ser reaberta e, antes de fechar uma proposta, uma caixa de diálogo de confirmação confirmará as suas alterações.

Se a proposta de projeto que está fechada como Perdida tem um projeto referenciado em qualquer uma das suas linhas, esse projeto também é marcado como Fechado e quaisquer reservas de recursos a partir desse dia são canceladas.

> [!NOTE]
> No Project Operations, fechar uma proposta como Ganha ou Perdida não afetará esse estado da Oportunidade, que permanecerá aberta até ser fechada manualmente.
