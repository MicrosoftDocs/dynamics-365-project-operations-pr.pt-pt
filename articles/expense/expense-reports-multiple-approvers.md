---
title: Relatórios de despesas e vários aprovadores
description: Este tópico fornece informações sobre relatórios de despesas que requerem aprovação por mais de uma pessoa.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 9b9826c89e9deb870adb053f82bd049906f56052
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276542"
---
# <a name="expense-reports-and-multiple-approvers"></a>Relatórios de despesas e vários aprovadores

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

Dependendo das políticas de aprovação de despesas da sua organização, mais de uma pessoa poderá ter de aprovar um relatório de despesas apresentado. Quando configurar o processo de fluxo de trabalho para aprovação de relatórios de despesas, pode adicionar elementos de fluxo de trabalho que incluem tarefas ou passos para um ou mais aprovadores de relatórios de despesas. Por exemplo, pode exigir que todos os relatórios de despesas sejam aprovados por duas pessoas distintas, o gestor do empregado que apresentou o relatório e o coordenador das Contas a pagar.

Se decidir exigir vários aprovadores de relatórios de despesas, pode adicionar os elementos do fluxo de trabalho de uma das seguintes formas:

- Adicione um elemento de aprovação que tenha um passo. Por exemplo, o passo pode exigir que um relatório de despesas seja atribuído a um grupo de utilizadores e que seja aprovado por 50% dos membros do grupo de utilizadores.
- Adicione um elemento de aprovação que tenha múltiplos passos. Por exemplo, o elemento de aprovação pode ter os seguintes passos:

    1. O gestor do empregado que apresentou o relatório de despesas aprova-o.
    2. O funcionários responsável pelas contas a pagar verifica os recibos e os itens de relatório de despesas.
    3. O proprietário do orçamento aprova o relatório de despesas.

- Adicione vários elementos de aprovação, cada um dos quais com um passo. Por exemplo, pode adicionar um elemento de aprovação separado para cada uma das seguintes etapas:

    1. O gestor do funcionário aprova o relatório de despesas.
    2. O proprietário do orçamento aprova o relatório de despesas.


[!INCLUDE[footer-include](../includes/footer-banner.md)]