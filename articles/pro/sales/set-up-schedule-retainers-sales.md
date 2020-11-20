---
title: Configurar uma agenda de sinais – lite
description: Este tópico fornece informações sobre como configurar uma agenda de sinais no Project Operations.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5e0312b89d9969f140146b6aaaa9bdcfde702c0b
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181286"
---
# <a name="set-up-a-retainer-schedule---lite"></a>Configurar uma agenda de sinais – lite

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

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
