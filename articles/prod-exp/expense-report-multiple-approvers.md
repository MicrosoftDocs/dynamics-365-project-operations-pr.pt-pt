---
title: Vários aprovadores no relatório de despesas
description: Este tópico fornece informações sobre relatórios de despesas que requerem aprovação por várias pessoas.
author: saraschi2
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c745dda957fab5acc464b9d1c774fcdc783cde40
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005265"
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


[!INCLUDE[footer-include](../includes/footer-banner.md)]