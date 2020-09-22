---
title: Reservar recursos nomeados a partir de requisitos de recursos
description: Este tópico fornece informações sobre a reserva de recursos nomeados para um requisito de recurso genérico.
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 83ac2056-313e-4f90-8297-238fd4d25ef9
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: eab280cd1a670cc2a6ed0ae02cde7ba9bf7d601d
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754497"
---
# <a name="book-named-resources-from-resource-requirements"></a>Reservar recursos nomeados a partir de requisitos de recursos

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Pode reservar um recurso nomeado para substituir o recurso genérico que tem um requisito de recurso.

1. No Project Service Automation (PSA), na página **Projetos**, clique no separador **Equipa**.
2. Selecione o recurso genérico que tem um requisito de recurso a partir da lista e, em seguida, clique em **Reservar**. Ou abra o requisito de recurso e, em seguida, clique em **Reservar**.


![Reservar um membro da equipa genérico](media/RM-how-to-14.png)


3. Na página **Assistente da Agenda**, selecione um recurso nomeado para reservar na sua equipa do projeto e, em seguida, clique em **Reservar**.

![Reservar um membro da equipa genérico utilizando o assistente da agenda](media/RM-how-to-15.png)

Quando a reserva é concluída e cumprida por um recurso nomeado, o recurso genérico é substituído pelo recurso nomeado.

![Membro da equipa nomeado que substitui um membro da equipa genérico](media/RM-how-to-16.png)

As atribuições na agenda também são atualizadas com o recurso nomeado.

![Membro da equipa nomeado atribuído a tarefas do projeto](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a>Cumprir um recurso genérico com vários recursos nomeados
O cumprimento de um requisito para um recurso genérico com vários recursos nomeados é semelhante à atribuição de um único recurso nomeado. Por exemplo, existe uma tarefa com uma duração de cinco dias e 120 horas de esforço. Esta tarefa não pode ser concluída por um recurso que funciona num dia de oito horas normal numa semana de cinco dias. 

![Uma tarefa que necessita de 120 horas de esforço durante cinco dias](media/RM-how-to-21.png)

O requisito é de 120 horas de engenharia robótica em cinco dias, ou seja, 24 horas por dia.

![Requisito por dia](media/RM-how-to-22.png)

Este é um exemplo de quando são necessários vários recursos nomeados para cumprir um pedido de recurso genérico. Terá de reservar vários recursos para cumprir o requisito.

![Reservar vários recursos para cumprir o requisito](media/RM-how-to-23.png)

A principal diferença neste cenário é que o recurso genérico permanece na equipa atribuída à tarefa, e os membros da equipa de recursos nomeados reservados não são atribuídos como parte da posição. O gestor de projeto pode atribuir o trabalho conforme adequado aos recursos nomeados. A vista **Reconciliação** pode ajudar um gestor de projeto a dividir as reservas em vários recursos em atribuições de tarefas. Isto não é efetuado automaticamente porque, em qualquer cenário mais complicado do que o exemplo simples acima, como, por exemplo, o local onde tem um grupo de tarefas que compõem o requisito, a intenção de como o gestor de projeto pretende atribuir, precisa de ser assumida pelo sistema. Uma vez que o sistema não consegue compreender as intenções, é provável que as suposições sejam diferentes das pretendidas e irá acontecer um resultado incorreto ou imprevisível. O resultado previsível é que o recurso genérico permanece atribuído até que o gestor de projeto crie deliberadamente as atribuições, com a ajuda da vista **Reconciliação**.


