---
title: Efetuar reserva flexível de um recurso
description: Este tópico fornece informações sobre como agendar provisoriamente ou efetuar uma reserva flexível de membros da equipa do projeto.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/25/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.app:
- ProjectOperations
ms.openlocfilehash: 2675096085fc4c673d15741042ffc1b82ed3de8b
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146452"
---
# <a name="soft-book-a-resource"></a>Efetuar reserva flexível de um recurso

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

É possível agendar temporariamente ou efetuar uma "reserva flexível" de um recurso para uma equipa de projeto para mostrar que pretende atribuir o recurso ao projeto. Reservas flexíveis não consomem a capacidade disponível de um recurso e é possível atribuir membros da equipa flexíveis a tarefas do projeto. No entanto, uma vez que a reserva flexível não consome a capacidade de um recurso, pode ainda efetuar uma "reserva fixa" do recurso para outras tarefas dentro do mesmo período. Os recursos genéricos não podem ser reservados de forma flexível, nem será possível uma reserva flexível cumprir um pedido de recurso genérico.

Os membros da equipa do projeto reservados de forma flexível são listados no separador **Equipa** da página **Projeto**, com as respetivas horas com reserva flexível apresentadas na coluna **Horas com Reserva Flexível** na vista **Membros da Equipa Nomeados**. Os membros da equipa reservados de forma flexível também estão listados no quadro da Agenda. Visto que são reservados de forma flexível, o quadro da Agenda não mostra qualquer consumo de capacidade para estes recursos. O tempo reservado de forma flexível não é apresentado no separador **Reconciliação**, nem é mostrado no campo **Reservas Alargadas** no separador **Reconciliação** do quadro da Agenda. 

Existem duas formas de efetuar uma reserva flexível de um membro da equipa para um projeto: diretamente a partir do quadro da Agenda ou ao adicionar o membro da equipa no separador **Equipa**. 

## <a name="soft-book-from-the-schedule-board"></a>Efetue uma reserva flexível no quadro da Agenda
Conclua os seguintes passos para reservar flexivelmente um recurso a partir do quadro da Agenda. 

1. Abra o quadro de Agenda e, no painel **Requisitos de Reserva**, selecione o separador **Projeto**.
2. Localize o projeto em que pretende efetuar a reserva flexível de um recurso. Se houver um grande número de projetos na lista, selecione o cabeçalho da coluna **Projeto** e utilize o filtro para procurar um ou mais projetos.
3. Selecione o projeto e, em seguida, arraste e largue-o na grelha de tempo do recurso.
5. No painel **Criar Reserva de Recursos**, ajuste as datas de início e de fim, defina o **Estado de Reserva** para **Flexível** e, em seguida, defina as horas. 
6. Clique em **Reservar**. Agora o recurso é apresentado no separador **Equipa** como um recurso para o projeto. Na vista **Membro de Equipa Nomeado** verá as horas com reserva flexível na coluna **Horas com Reserva Flexível**.

> [!NOTE]
> Agora pode atribuir a reserva flexível às tarefas no separador **Agenda**. No separador **Reconciliação**, o recurso mostra um deficit de reserva relativo à atribuição de tarefa, uma vez que o separador **Reconciliação** só considera reservas fixas. Pode utilizar a funcionalidade **Reservas Alargadas** para reservar de forma fixa o recurso e, dessa forma, eliminar o deficit de reservas fixas contra as atribuições de recursos. Terá de cancelar manualmente a reserva flexível para o recurso através de **Manter Reservas**.

## <a name="soft-book-on-the-team-tab"></a>Efetue uma reserva flexível no separador Equipa

Pode adicionar membros da equipa diretamente no separador **Equipa** e, em seguida, alterar o estado da reserva de **Fixa** para **Flexível** com **Manter Reservas**. Quando adiciona um membro da equipa desta forma, vai sempre resultar numa reserva fixa, a menos que selecione o método de alocação como **Nenhum**.

Para utilizar este método, conclua os seguintes passos.

1. Na página **Projeto**, no separador **Equipa**, clique em **Novo**.
2. Selecione o recurso reservável, a função e as datas de e a.
3. Selecione um método de alocação diferente de **Nenhum**.
4. Selecione **Guardar**. Verá o recurso na grelha de equipa e as respetivas horas indicadas na coluna **Horas com Reserva Fixa**.
5. Mantenha as reservas do recurso selecionando **Manter Reservas**.
6. Quando o quadro da Agenda se abrir, expanda o recurso para apresentar as reservas. A reserva será apresentada como **Fixa**.
7. Com o botão direito do rato, clique na reserva, e em **Alterar Estado**, selecione **Reserva Flexível** \> **Flexível**. O estado da reserva é agora **Flexível**.
8. Depois de fechar o quadro da Agenda, verá que as horas para o recurso foram movidas da coluna **Horas com Reserva Fixa** para **Horas com Reserva Flexível** na grelha do separador **Equipa**, quando está na vista **Membros da Equipa Nomeados**.

> [!NOTE]
> Quando utilizar **Manter Reservas** para alterar o estado de **Fixa** para **Flexível**, se efetuar uma reserva fixa de um recurso para a equipa e, em seguida, atribuir tarefas ao recurso, as atribuições das tarefas para esse recurso ficarão retidas. No entanto, no separador **Reconciliação**, o recurso terá uma deficiência de reserva, uma vez que apenas reservas fixas são consideradas ao reconciliar reservas versus atribuições. Pode utilizar a funcionalidade **Reservas Alargadas** no separador **Reconciliação** para reservar de forma fixa o recurso e, dessa forma, eliminar o deficit de reservas fixas contra as atribuições de recursos. Terá de cancelar manualmente a reserva flexível para o recurso através de **Manter Reservas**.

Quando estiver pronto para alterar um recurso de membro de equipa reservado de forma flexível para reserva fixa, faça o seguinte:

1. No quadro da Agenda, expanda o recurso para apresentar as reservas. Verá a reserva marcada como **Flexível**.
2. Com o botão direito na reserva e em **Alterar Estado**, selecione **Reserva Fixa** \> **Fixa**. O estado da reserva é agora **Fixa**.
3. Depois de fechar o quadro da Agenda, voltar ao projeto e abrir o separador **Equipa**, verá que as horas para o recurso foram movidas da coluna **Horas com Reserva Flexível** para **Horas com Reserva Fixa** no separador **Equipa**, quando está na vista **Membros da Equipa Nomeados**. Se o recurso foi atribuído a tarefas, estas já não apresentam um deficit de reserva no separador **Reconciliação**, uma vez que as reservas são agora fixas.

