---
title: Efetuar reserva flexível de requisitos
description: Este tópico fornece informações sobre como reservar requisitos de forma flexível.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 95f064e0f83d2052ac4ae9673b4fcdcd16a2574246d3320e1ed3798cd6ff062b
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007025"
---
# <a name="soft-book-requirements"></a>Efetuar reserva flexível de requisitos

[!include [banner](../includes/psa-now-project-operations.md)]

Um requisito de recurso pode ser reservado de forma fixa. Uma reserva fixa cria uma proposta que consome a capacidade de um recurso. Em seguida, a proposta é enviada para o requerente para aprovação. Uma reserva flexível adiciona provisoriamente um recurso a uma equipa do projeto e tem um estado diferente no Quadro da Agenda, mas não consome a capacidade do recurso. Para efetuar uma reserva flexível de um recurso do Quadro da Agenda, defina o campo **Estado de Reserva** como **Flexível**.

![Estado da reserva definido como Flexível.](media/Resource-Management-image77.png)

Quando o separador **Equipa** se encontra na vista **Membros da Equipa Nomeados**, o recurso é apresentado nesse ponto. As horas reservadas de forma flexível são reportadas na coluna **Horas com Reserva Flexível**.

![Horas reservadas de forma flexível na vista Membros da Equipa Nomeados.](media/Resource-Management-image78.png)

Os membros da equipa reservados de forma flexível podem ser atribuídos às tarefas.

![Membro da equipa reservado de forma flexível atribuído a uma tarefa.](media/Resource-Management-image79.png)

No separador **Reconciliação**, não são mostradas reservas para um recurso com reserva flexível, porque o separador **Reconciliação** só considera as reservas fixas.

![Recurso reservado de forma flexível sem reservas no separador Reconciliação.](media/Resource-Management-image80.png)

> [!NOTE]
> Não é possível efetuar uma reserva flexível de um recurso a partir de um requisito gerado a partir de um membro da equipa genérico.

No Quadro da Agenda, é utilizada uma cor diferente para as reservas flexíveis de um recurso.

![Reservas flexíveis no Quadro da Agenda.](media/Resource-Management-image81.png)

Para converter uma reserva flexível numa reserva fixa, no Quadro da Agenda, clique com o botão direito do rato na reserva flexível e selecione **Alterar Estado** \> **Reserva Fixa** \> **Fixa**.

![Alterar o estado de reserva para Fixa.](media/Resource-Management-image82.png)

A reserva é alterada e o estado é alterado no Quadro da Agenda. Uma vez que o estado de reserva é **Fixa**, o recurso é mostrado como reservado e a sua capacidade e disponibilidade são ajustadas.

Pode utilizar o mesmo método para cancelar uma reserva fixa ou uma reserva flexível a partir do Quadro da Agenda.

Para converter um recurso com reserva flexível em fixa no separador **Equipa**, selecione o recurso e, em seguida, selecione **Confirmar**.

![Comando Confirmar.](media/Resource-Management-image83.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]