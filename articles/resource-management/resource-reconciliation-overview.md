---
title: Descrição geral da reconciliação de recursos
description: Esta tópico fornece informações que o ajudarão a garantir que as reservas de recursos e atribuições para projetos estão alinhadas.
author: ruhercul
manager: AnnBe
ms.date: 01/08/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 8723cfad1e7cd07774e37023c5427b0a5833a554
ms.sourcegitcommit: cffc84187007b34211c90babef8af5152d4d92ea
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 01/12/2021
ms.locfileid: "4849638"
---
# <a name="resource-reconciliation-overview"></a>Descrição geral da reconciliação de recursos

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

Quanto aos membros da equipa, as reservas e as atribuições têm uma ligação fraca. Por outras palavras, os recursos podem ter atribuições e não ter reservas, ou podem ter reservas e não ter atribuições. Idealmente, as reservas e atribuições devem ser alinhadas, para que os recursos tenham capacidade comprometida para executar as atribuições de tarefas. No entanto, as reservas podem basear-se na disponibilidade e as temporizações das tarefas podem mudar à medida que o projeto continua. Portanto, a ligação fraca de reservas e atribuições fornece flexibilidade.

O separador **Reconciliação** na página **Projetos** permite que os gestores de projeto reconciliem as reservas de membros da equipa e as respetivas atribuições para as equipas do projeto.

O separador **Reconciliação** mostra as reservas e as atribuições até ao nível da atribuição de tarefas individuais para cada membro da equipa. As horas são apresentadas em células representam períodos de meses a dias. O separador também mostra um total líquido global para o projeto, juntamente com uma coluna **Total**.

Para cada recurso, o separador **Reconciliação** calcula a diferença entre as reservas do membro da equipa e um rollup das atribuições de tarefas desse membro da equipa. O ideal é que esta diferença seja 0 (zero). Por outras palavras, não deve haver diferença entre as reservas e as atribuições. As diferenças são coloridas e sombreadas para chamar a atenção para duas condições:

- **Falta de reserva** – Uma falta de reserva ocorre quando um recurso tem mais atribuições do que reservas. Como a capacidade não foi reservada, o gestor de projeto pode querer corrigir esta condição, expandindo as reservas do recurso para cobrir o deficit.
- **Reservas em excesso** – As reservas em excesso ocorrem quando um recurso foi reservado para o projeto, mas ainda não foi atribuído às tarefas. Esta condição poderá ser aceitável em casos em que o recurso esteve reservado para o projeto antes da atribuição de tarefas. No entanto, noutros casos, em que não exista um plano para atribuir o recurso às tarefas, o gestor do projeto deve considerar o cancelamento das reservas do recurso. Desta forma, a capacidade pode ser utilizada para outro projeto.

Em alguns casos, quando visualiza o tempo num nível superior ao nível do dia (por exemplo, o nível de mês), poderá ver uma diferença líquida de zero para um recurso (por outras palavras, reservas igual a atribuições). No entanto, se visualizar o tempo no nível da semana, poderá ver que existem atribuições de zero horas e reservas de 40 horas na primeira semana, mas atribuições de 40 horas e reservas de zero horas na segunda semana. Globalmente, as reservas e as atribuições são reconciliadas, mas diferem de uma semana para a seguinte.

Quando visualiza o tempo em níveis superiores, as células no separador **Reconciliação** têm um indicador para informá-lo de que existem diferenças em níveis inferiores. Ao tocar duas vezes numa célula, pode ampliar para ver a diferença. Em seguida, pode selecionar e manter (ou clicar com o botão direito do rato) para reduzir. Ao selecionar um recurso e, em seguida, utilizar o controlo **Diferença seguinte** na barra de ferramentas de grelha, pode ir para a próxima diferença entre as reservas e as atribuições para esse recurso. Em seguida, pode utilizar o controlo **Diferença anterior** para voltar. Também pode desativar o indicador de diferença e o comportamento de navegação em **Definições**.

Se tiver atribuições de tarefas para um recurso, mas não tiver reservas, selecione o atalho de reserva no separador **Reconciliação** da página **Projetos** e depois selecione **Prolongar reserva**. A caixa de diálogo **Prolongar reserva** que aparece, mostra a reserva requerida para resolver a falta do recurso. A caixa de diálogo também mostra as reservas existentes do recurso em todos os projetos ou outras entidades agendáveis. Se selecionar **OK** para criar a reserva para o recurso, independentemente da disponibilidade do recurso, poderá causar uma reserva em excesso.

As reservas que são criadas através da ação **Prolongar reserva** estão associadas à exigência do projeto primário. Quando uma extensão é iniciada, o requisito específico que deve ser estendido não pode ser determinado, porque o recurso pode estar associado a mais de um requisito para o projeto.

Em seguida, o gestor de projeto ou o gestor de recursos podem utilizar o quadro da agenda para gerir qualquer situação em que um recurso tenha uma reserva em excesso além da sua capacidade.
