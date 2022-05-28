---
title: Fechar uma proposta
description: Este tópico fornece informações sobre como fechar propostas no Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 25f5a515769b97e963b2a2ac8738884b3f0db2fb
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598594"
---
# <a name="close-a-quote"></a>Fechar uma proposta

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

Uma proposta de projeto pode ser fechada como Ganha ou Perdida. Uma vez que as funções de Ativação e Revisão não são suportadas em propostas no Microsoft Dynamics 365 Project Operations, pode fechar uma proposta de rascunho.

## <a name="close-a-quote-as-won"></a>Fechar uma proposta como Ganha

Fechar uma proposta de projeto como Ganha definirá o estado da proposta como **Fechada** e a razão do estado como **Ganha**. Fechar as propostas torna-as só de leitura e cria um contrato de projeto de rascunho com todas as informações da proposta. Como uma proposta fechada não pode ser reaberta, antes de fechar uma proposta, uma caixa de diálogo de confirmação confirmará as suas alterações.

O contrato de projeto criado a partir de uma proposta de projeto também é disponibilizado no módulo Gestão de projetos e contabilística do Project Operations. Se um contrato de projeto não for mapeado para um projeto em nenhuma das suas linhas, este contrato de projeto será disponibilizado como um contrato de projeto inativo e torna-se ativo assim que um projeto é mapeado para, pelo menos, um dos seus itens de contrato.

Se a proposta estiver anexada a uma oportunidade, quaisquer outras propostas de projeto na oportunidade são fechadas automaticamente como Perdidas.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Impacto financeiro de fechar uma proposta como Ganha

Se tiverem existido valores reais para o tempo registado num projeto enquanto ainda está anexado a uma proposta de rascunho, só o custo do tempo ou da despesa é registado. Depois de uma proposta ser fechada como Ganha, a aplicação irá refatorizar os custos ao inverter os valores reais do custo mais antigos e recriar novos custos reais. A aplicação irá processar estes valores reais de custos baseados no método de Faturação do item de contrato do projeto associado. Se os valores reais do custo referenciarem um item de contrato de tempo e material, o sistema criará automaticamente as vendas não faturadas correspondentes para quando a proposta estiver fechada e o contrato de projeto for criado. Se os valores reais do custo referenciam um item de contrato de preço fixo, a aplicação deixará de reprocessar os valores reais do custo baseado nas regras de faturação dividida para os clientes do contrato de projeto.

Todos os valores reais reprocessados estão disponíveis no módulo Gestão de projetos e contabilística para a Gestão contabilística do projeto rever, atualizar e lançar no Razão geral. 

## <a name="close-a-quote-as-lost"></a>Fechar uma proposta como Perdida

Fechar uma proposta de projeto como Perdida definirá o estado como **Fechada** e a razão do estado como **Perdida**. Fechar a proposta torna-a só de leitura. Como uma proposta fechada não pode ser reaberta e, antes de fechar uma proposta, uma caixa de diálogo de confirmação confirmará as suas alterações.

Se a proposta de projeto que está fechada como Perdida tem um projeto referenciado em qualquer uma das suas linhas, esse projeto também é marcado como Fechado e quaisquer reservas de recursos a partir desse dia são canceladas.

> [!NOTE]
> No Project Operations, fechar uma proposta como Ganha ou Perdida não afetará esse estado da Oportunidade, que permanecerá aberta até ser fechada manualmente.


[!INCLUDE[footer-include](../includes/footer-banner.md)]