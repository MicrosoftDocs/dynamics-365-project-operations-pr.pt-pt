---
title: Vários aprovadores no relatório de despesas
description: Este tópico fornece informações sobre relatórios de despesas que requerem aprovação por várias pessoas.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b6d07f00fd6c1ba2d860787665d95f95f7b1a89
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960621"
---
# <a name="multiple-approvers-on-an-expense-report"></a>Vários aprovadores no relatório de despesas

Dependendo das políticas de aprovação de despesas da sua organização, mais de uma pessoa poderá ter de aprovar um relatório de despesas submetido por um funcionário. Quando configurar o processo de fluxo de trabalho para aprovação de relatórios de despesas, pode adicionar elementos de fluxo de trabalho que incluem tarefas ou passos para um ou mais aprovadores de relatórios de despesas. Por exemplo, pode exigir que todos os relatórios de despesas sejam aprovados primeiro pelo o gestor do empregado que apresentou o relatório e, em seguida, pelo coordenador das Contas a pagar.

Se decidir exigir vários aprovadores de relatórios de despesas, pode adicionar os elementos do fluxo de trabalho de uma das seguintes formas:

- Adicione um elemento de aprovação que tenha um passo. Por exemplo, o passo pode exigir que um relatório de despesas seja atribuído a um grupo de utilizadores e que seja aprovado por 50% dos membros do grupo de utilizadores.
- Adicione um elemento de aprovação que tenha múltiplos passos. Por exemplo, o elemento de aprovação pode ter os seguintes passos:

    1. O gestor do empregado que apresentou o relatório de despesas aprova-o.
    2. O funcionários responsável pelas contas a pagar verifica os recibos e os itens de relatório de despesas.
    3. O proprietário do orçamento aprova o relatório de despesas.

- Adicione vários elementos de aprovação, cada um dos quais com um passo. Por exemplo, pode adicionar um elemento de aprovação separado para cada uma das seguintes etapas:

    1. O gestor do funcionário aprova o relatório de despesas.
    2. O proprietário do orçamento aprova o relatório de despesas.
