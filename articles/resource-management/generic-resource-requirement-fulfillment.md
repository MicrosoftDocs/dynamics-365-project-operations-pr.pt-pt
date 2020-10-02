---
title: Cumprimento dos requisitos genéricos de recursos
description: Este tópico fornece informações sobre a reserva de recursos nomeados para um requisito de recurso genérico.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 76dd47fa2451b5cb61298ff332d77bae646a288a
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897600"
---
# <a name="generic-resource-requirement-fulfillment"></a>Cumprimento dos requisitos genéricos de recursos

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

Pode reservar um recurso nomeado para substituir o recurso genérico que tem um requisito de recurso.

1. Na página **Projetos**, selecione o separador **Equipa**.
2. Selecione o recurso genérico que tem um requisito de recurso a partir da lista e, em seguida, selecione **Reservar**. Ou abra o requisito de recurso e, em seguida, selecione **Reservar**.
3. Na página **Assistente da Agenda**, selecione um recurso nomeado para reservar na sua equipa do projeto e, em seguida, selecione **Reservar**.

Quando a reserva é concluída e cumprida por um recurso nomeado, o recurso genérico é substituído pelo recurso nomeado.

As atribuições na agenda também são atualizadas com o recurso nomeado.

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a>Cumprir um recurso genérico com vários recursos nomeados
O cumprimento de um requisito para um recurso genérico com vários recursos nomeados é semelhante à atribuição de um único recurso nomeado. Por exemplo, existe uma tarefa com uma duração de cinco dias e 120 horas de esforço. Esta tarefa não pode ser concluída por um recurso que funciona num dia de oito horas normal numa semana de cinco dias. 

O requisito é de 120 horas de engenharia robótica em cinco dias, ou seja, 24 horas por dia.

Este é um exemplo de quando são necessários vários recursos nomeados para cumprir um pedido de recurso genérico. Terá de reservar vários recursos para cumprir o requisito.

A principal diferença neste cenário é que o recurso genérico permanece na equipa atribuída à tarefa, e os membros da equipa de recursos nomeados reservados não são atribuídos como parte da posição. O gestor de projeto pode atribuir o trabalho conforme adequado aos recursos nomeados. A vista **Reconciliação** pode ajudar um gestor de projeto a dividir as reservas em vários recursos em atribuições de tarefas. Isto não é efetuado automaticamente porque, em qualquer cenário mais complicado do que o exemplo simples acima, como, por exemplo, o local onde tem um grupo de tarefas que compõem o requisito ou a intenção de como o gestor de projeto pretende atribuir, precisa de ser assumida pelo sistema. Como o sistema não pode compreender a intenção, é provável que as suposições sejam diferentes das pretensões e um resultado incorreto ou imprevisível será obtido. O resultado previsível é que o recurso genérico permanece atribuído até que o gestor de projeto crie deliberadamente as atribuições, com a ajuda da vista **Reconciliação**.


