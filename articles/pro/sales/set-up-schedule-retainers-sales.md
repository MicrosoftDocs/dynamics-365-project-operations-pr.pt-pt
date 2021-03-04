---
title: Configurar uma agenda de sinais
description: Este tópico fornece informações sobre como configurar uma agenda de sinais no Project Operations.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1c264b544660cf7a0b116f09b6bd7c94fcf0457e
ms.sourcegitcommit: 250270409412ba4cad95fbd4c345a80d3d2b3e53
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 11/21/2020
ms.locfileid: "4596386"
---
# <a name="set-up-a-retainer-schedule"></a>Configurar uma agenda de sinais

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

As agendas de sinais são configuradas na página do **Contrato de Projeto** no Dynamics 365 Project Operations.

1. Na página **Contrato de Projeto**, no separador **Adiantamentos e Sinais**, selecione **Configurar a agenda de sinais**.
2. Na página de diálogo que abre, são apresentados os campos listados na tabela seguinte. A tabela dá uma ideia de como os valores introduzidos impactam ou influenciam a agenda de sinais que será criada.

| Campo | Descrição | Impacto a jusante |
| --- | --- | --- |
| Cliente do Contrato do Projeto | O cliente no contrato que será faturado por este sinal ou adiantamento. | Se tiver vários clientes no contrato e precisar de faturar cada um deles por um montante de sinal ou de adiantamento específico, crie manualmente uma fatura para cada cliente. |
| Início de agendamento de sinal | Introduza a data início da agenda de sinais. | Esta data pode não ser a data em que o primeiro sinal ou adiantamento é criado. A data em que o primeiro sinal ou adiantamento é também influenciado pela frequência da fatura. |
| Final de agendamento de sinal | Introduza a data de fim da agenda de sinais. | Esta data pode não ser a data em que o último sinal ou adiantamento é criado. A data em que o último sinal ou adiantamento é também influenciado pela frequência da fatura. |
| Número de sinais para criar | Quando introduz o número de sinais a criar, o sistema utiliza a data de início e a frequência para criar o número neste campo. | Quando este campo é atualizado manualmente, o sistema ignora o valor no campo **Fim da Agenda de Sinais** e cria o número específico de sinais ou adiantamentos. |
| Frequência da Fatura | Com que frequência a aplicação irá criar sinais e adiantamentos. | Este valor influencia diretamente o número de sinais e adiantamentos e as datas criadas. |
| Montante Total | O montante total é o montante que é dividido nos pagamentos do sinal individual ou do adiantamento que serão criados. | Este campo não tem impacto a jusante. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]