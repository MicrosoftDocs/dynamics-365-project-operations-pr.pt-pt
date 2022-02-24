---
title: Fechar uma proposta – lite
description: Este tópico fornece informações sobre como fechar uma proposta no Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6214e1b5bec5c9173a6b6e69578de14654da633e
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272297"
---
# <a name="close-a-quote---lite"></a>Fechar uma proposta – lite

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

Uma proposta de projeto pode ser fechada como Ganha ou Perdida. Um rascunho de cotação pode ser fechado porque as operações de Ativação e Revisão em cotações não são suportadas no Microsoft Dynamics 365 Project Operations.

## <a name="close-a-quote-as-won"></a>Fechar uma proposta como Ganha

Quando fecha uma citação do projeto como Ganho, o estado está definido para Fechado e o razão do estado é Ganho. Fechar a proposta torna a proposta de projeto só de leitura e cria um contrato de projeto de rascunho que contém as informações da proposta. Uma vez que uma cotação fechada não pode ser reaberta, um diálogo de confirmação confirmará as suas alterações.

Se a proposta estiver anexada a uma oportunidade, quaisquer outras propostas de projeto na oportunidade são fechadas automaticamente como Perdidas.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Impacto financeiro de fechar uma proposta como Ganha

Se houver algum tempo real num projeto enquanto ainda estiver anexado a um projeto de cotação, apenas o custo do tempo ou da despesa é registado. Depois de uma proposta ser fechada como Ganha, a aplicação irá refatorizar os custos ao inverter os valores reais do custo mais antigos e recriar novos custos reais. A aplicação irá processar estes valores reais de custos baseados no método de Faturação do item de contrato do projeto associado. Se os resultados de custo referem uma linha de contrato de tempo e material, os correspondentes resultados de vendas não faturados são criados para quando a cotação é fechada e o contrato do projeto é criado. Se os custos reais referem uma linha de contrato de preço fixo, a aplicação deixará de reprocessar os custos reais que se baseiam nas regras de faturação divididas para os clientes do contrato de projeto.

## <a name="closing-a-quote-as-lost"></a>Fechar uma proposta como perdida:

Quando fecha uma citação do projeto como Perdido, o estado está definido para Fechado e o razão do estado é Perdido. Fechar a proposta faz com que a proposta de projeto seja só de leitura. Como uma proposta fechada não pode ser reaberta e, antes de fechar uma proposta, uma caixa de diálogo de confirmação confirmará as suas alterações.

Se a citação do projeto que está fechada como Perdido refere um projeto em qualquer uma das suas linhas, esse projeto também é marcado como Perdido. Quaisquer reservas de recursos a partir desse dia são canceladas.

> [!NOTE]
> No Project Operations, fechar uma proposta como Ganha ou Perdida não afetará esse estado da Oportunidade, que permanecerá aberta até ser fechada manualmente.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]