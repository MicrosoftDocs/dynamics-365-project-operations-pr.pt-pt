---
title: Reservas de recursos e como elas se relacionam com atribuições de tarefas
description: Este tópico fornece informações sobre como gerir recursos nomeados, reservas de recursos e atribuições de tarefas e como se relacionam.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 0e4eea87bfb059a3c0be8ccbd2914a4d6c3cf46b
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149962"
---
# <a name="resource-bookings-and-how-they-relate-to-task-assignments"></a>Reservas de recursos e como elas se relacionam com atribuições de tarefas

[!include [banner](../includes/psa-now-project-operations.md)]

Os recursos nomeados podem ser reservados para uma equipa do projeto e podem ter atribuídas tarefas de projeto de duas maneiras:

- O recurso pode ser reservado diretamente para um projeto e atribuído a tarefas do projeto.
- As tarefas podem ser atribuídas a um recurso genérico que, em seguida, é utilizado para localizar e substituir o genérico por um recurso nomeado. 

Em ambos os casos, o ato de reservar o recurso reserva a capacidade do recurso.

O gestor de projeto que planeia o projeto é o proprietário do plano do projeto e da agenda. Utilizando o recurso genérico para atribuição e, em seguida, gerando um pedido de recurso a partir do mesmo, o gestor de projeto pode reservar recursos para o projeto com contornos especificados no plano do projeto. Estes podem reservar recursos para um projeto e, em seguida, atribui-los a tarefas, no entanto não existe nenhuma forma de alinhamento dos contornos de reserva com os contornos das tarefas. As reservas não afetam a agenda do projeto.

Considere um projeto complexo com várias tarefas sobrepostas onde vários recursos do mesmo tipo necessitam de trabalhar em simultâneo. Se for dado um contorno a um recurso que é diferente do que o agregado das suas atribuições, é difícil modificar as tarefas para as adaptar ao contorno das reservas às discretas tarefas e os contornos originais.

No exemplo abaixo, o esforço total necessário requerido pelo mesmo recurso de um conjunto de quatro tarefas é de 62 horas ao longo de um período de duas semanas e existe um contorno específico. Se o recurso Fernando está marcado para 62 horas durante as mesmas duas semanas, mas com um contorno diferente, o requisito e as reservas estão alinhados.

| **Contornos da tarefa**    | **Horas totais** | Seg 4/6 | Ter 5/6 | Qua 6/6 | Qui 7/6 | Sex 8/6 | Sáb 9/6 | Dom 10/6 | Seg 11/6 | Ter 12/6 | Qua 6/13 | Qui 14/6 | Sex 15/6 |
|----------------------|-----------------|--------|--------|--------|--------|--------|--------|---------|---------|---------|---------|---------|---------|
| Tarefa 1               | 24              | 8      | 8      | 4      |        |        |        |         |         |         | 4       |         |         |
| Tarefa 2               | 16              |        |        | 4      | 4      |        |        |         | 8       |         |         |         |         |
| Tarefa 3               | 10              |        |        |        |        | 4      |        |         |         | 4       |         | 2       |         |
| Tarefa 4               | 12              |        |        |        |        |        |        |         |         |         | 4       |         | 8       |
|                      |                 |        |        |        |        |        |        |         |         |         |         |         |         |
| **Totais**           | 62              | 8      | 8      | 8      | 4      | 4      |        |         | 8       | 4       | 8       | 2       | 8       |
|                      |                 |        |        |        |        |        |        |         |         |         |         |

### <a name="bobs-availability"></a>Disponibilidade do Fernando
| **Reserva de recurso** | **Horas totais** | Seg 4/6 | Ter 5/6 | Qua 6/6 | Qui 7/6 | Sex 8/6 | Sáb 9/6 | Dom 10/6 | Seg 11/6 | Ter 12/6 | Qua 6/13 | Qui 14/6 | Sex 15/6 |
|------------------------|-----------------|--------|--------|--------|--------|--------|--------|---------|---------|---------|---------|---------|---------|
| Fernando                    | 62              | 4      | 4      | 8      | 8      | 8      |        |         | 4       | 4       | 8       | 8       | 6       |

No entanto, não existe nenhuma forma sistemática para atribuir o contorno das horas reservadas para tarefas numa base por dia. Se o gestor de projeto estiver disposto a alterar a agenda de projeto para atingir a disponibilidade do recurso, terá de remover a atribuição e rever todas as tarefas para corresponderem aos contornos da reserva.

No caso onde uma organização recebeu a tarefa de planeamento de planeamento de projeto para ambos o gestor de projeto e gestor de recursos, o gestor de projeto define a agenda e isso inclui os contornos do trabalho necessário. O gestor de recursos não deverá conseguir afetar a agenda sem o conhecimento do gestor de projeto alterando os contornos de esforço durante a reserva de recursos reais. Se o gestor de recursos está a preencher algo diferente do que o gestor de projeto solicitou, é necessário que entrem em acordo sobre que alterações são necessários na agenda do projeto.

Uma vez que as reservas e as atribuições não estão totalmente ligadas, é possível reservar contornos que são diferentes dos contornos de tarefa ou alterar as atribuições para resultar em circunstâncias nas quais as reservas e atribuições não estão alinhadas.

A **Vista de Reconciliação** permite ao gestor de projeto ver as reservas e atribuições de cada membro da equipa do projeto. A vista utiliza cores e sombreamento para mostrar quando não há correspondência entre a reserva de um membro da equipa e atribuições. Com base nestas informações, o gestor de projeto pode tomar medidas corretivas para expandir as reservas de recursos para casos em que não existem atribuições e nenhuma reserva ou cancelamento de reserva onde os recursos estão reservados mas não têm atribuições.

> [!NOTE]
> Se mover uma tarefa para a qual tenha sido você a criar os contornos, estes contornos não são mantidos. Os contornos são regenerados de acordo com o calendário do projeto para dar conta de alterações nas horas de trabalho e férias. Isto é propositado uma vez que o sistema não conhece o objetivo do contorno original e não pode determinar se faz sentido manter esse contorno num período de tempo novo. Uma vez que as reservas e as atribuições estão desligadas, as reservas retêm os contornos da reserva original. Neste caso, terá de cancelar e recusar para o novo contorno de atribuição.

