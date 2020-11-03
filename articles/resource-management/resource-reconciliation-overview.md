---
title: Descrição geral da reconciliação de recursos
description: Este tópico fornece informações sobre como assegurar que as reservas de recursos e as atribuições aos projetos estão alinhadas.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e2b16a6e1c48769ed4d903e546804ba1c4e1c4fa
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082346"
---
# <a name="resource-reconciliation-overview"></a>Descrição geral da reconciliação de recursos

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

Quanto aos membros da equipa, as reservas e as atribuições têm uma ligação fraca. Por outras palavras, os recursos podem ter atribuições, mas não reservas, ou podem ter reservas, mas não atribuições. Idealmente, as reservas e atribuições devem ser alinhadas, para que os recursos tenham capacidade comprometida para executar as atribuições de tarefas. No entanto, as reservas podem basear-se na disponibilidade e as temporizações das tarefas podem mudar à medida que o projeto continua. Portanto, a ligação fraca de reservas e atribuições fornece flexibilidade.

O separador **Reconciliação** no formulário **Projeto** permite que os gestores de projeto reconciliem os reservas de membros da equipa e as respetivas atribuições para as equipas do projeto.

O separador **Reconciliação** também mostra as reservas e as atribuições até ao nível da atribuição de tarefas individuais para cada membro da equipa. As horas são mostradas nas células que representam períodos de meses a dias.

O separador também mostra um total líquido global para o projeto, juntamente com uma coluna **Total**.

Para cada recurso, o separador calcula a diferença entre as reservas do membro da equipa e um rollup das atribuições de tarefas do membro da equipa. O ideal é que esta diferença seja 0 (zero). Por outras palavras, não deve haver diferença entre as reservas e as atribuições. As diferenças são coloridas e sombreadas para chamar a atenção para duas condições:

- **Falta de reserva** – Uma falta de reserva ocorre quando um recurso tem mais atribuições do que reservas. Como essa capacidade não foi reservada, um gestor de projeto pode querer corrigir esta condição, expandindo as reservas do recurso para cobrir o deficit.
- **Reservas em excesso** – As reservas em excesso ocorrem quando um recurso foi reservado para o projeto, mas ainda não foi atribuído às tarefas. Esta condição poderá ser aceitável nos casos em que o recurso esteve reservado para o projeto antes da atribuição de tarefas. No entanto, em outros casos, o recurso não está planeado para ser atribuído a tarefas. Nestes casos, o gestor de projeto deverá considerar o cancelamento das reservas do recurso, para que a capacidade possa ser utilizada para outro projeto.

Em alguns casos, quando visualiza o tempo num nível superior ao nível do dia (por exemplo, o nível de mês), poderá ver uma diferença líquida de zero para um recurso (por outras palavras, reservas = atribuições). No entanto, se visualizar o tempo no nível da semana, poderá ver que existem atribuições de zero horas e reservas de 40 horas na primeira semana, mas atribuições de 40 horas e reservas de zero horas na segunda semana. Globalmente, as reservas e as atribuições são reconciliadas, mas diferem de uma semana para a seguinte.

Quando visualiza o tempo em níveis superiores, as células no separador **Reconciliação** têm um indicador para informá-lo de que existem diferenças em níveis inferiores. Ao clicar duas vezes numa célula, pode ampliar para ver a diferença. Em seguida, pode clicar com o botão direito do rato para reduzir. Ao selecionar um recurso e, em seguida, utilizar o controlo **Diferença seguinte** na barra de ferramentas de grelha, pode ir para a próxima diferença entre as reservas e as atribuições para esse recurso. Em seguida, pode utilizar o controlo **Diferença anterior** para voltar. Também pode desativar o indicador de diferença e o comportamento de navegação em **Definições**.


Se tiver atribuições de tarefas para um recurso, mas não tiver reservas, na página **Projetos** , no separador **Reconciliação** , selecione a falta de reserva e, em seguida, selecione **Expandir Reserva**. É apresentada a caixa de diálogo **Falta de Reserva** e mostra a reserva necessária para resolver a falta do recurso. Também mostra as reservas existentes do recurso em todos os projetos ou outras entidades agendáveis. Se selecionar **OK** para criar a reserva para o recurso, independentemente da disponibilidade do recurso, poderá causar uma reserva em excesso.

Em seguida, o gestor de projeto ou o gestor de recursos pode utilizar o Quadro da Agenda para gerir qualquer situação em que um recurso tenha uma reserva em excesso além da sua capacidade.

