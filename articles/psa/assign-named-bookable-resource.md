---
title: Reservar recursos reserváveis nomeados para uma equipa do projeto e atribuir tarefas
description: Este artigo fornece informações sobre como reservar recursos nomeados para as equipas do projeto e atribuí-las a tarefas.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 61c9b47088e836c0a9c78477adf891df3d14853b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919338"
---
# <a name="book-named-bookable-resources-to-a-project-team-and-assign-tasks"></a>Reservar recursos reserváveis nomeados para uma equipa do projeto e atribuir tarefas 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Pode adicionar um recurso nomeado à sua equipa do projeto, reservando-o diretamente para a equipa. Para o fazer, conclua os seguintes passos.

1. No Project Service Automation, aceda a **Projetos** e selecione para abrir o projeto que está a reservar.
2. Na página **Projeto**, no separador **Equipa**, clique em **Novo**. 

![Adicionar um membro da equipa a partir do separador equipa.](media/RM-how-to-1.png)

3. Na caixa de diálogo **Criação Rápida de Membro de Equipa do Projeto**, selecione o recurso reservável. O campo **Função** será preenchido com a função predefinida do recurso se tiver atribuído um. Poderá alterar a função, se for necessário. 
4. Selecione as datas de início e fim, em que o recurso será necessário e selecione o método de alocação da capacidade do recurso. 
5. Se pretender que o membro da equipa seja um aprovador do projeto, selecione **Sim** no campo **Aprovador do Projeto**. Isto significa que o membro da equipa pode aprovar as entradas de tempo e despesas submetidas para este projeto. 
6. Clique em **Guardar**.

![Adicionar um membro da equipa no formulário criação rápida.](media/RM-how-to-2.png)


Agora, pode atribuir o recurso reservado a tarefas no projeto. Na página **Projeto**, clique no separador **Agenda** para atribuir tarefas ao novo recurso. O seletor de recursos que é iniciado a partir do campo **Recursos** na grelha de tarefas irá mostrar os membros da equipa que pode selecionar.

![Atribuir um membro da equipa a uma tarefa no separador agenda.](media/RM-how-to-3.png)

Na versão 3 do Project Service Automation (PSA), as reservas de recursos e as atribuições de tarefas não estão totalmente ligadas. Isto significa que, quando utiliza o seletor de recursos na agenda, pode atribuir tarefas a membros da equipa durante mais horas do que as reservas deles cobrem no projeto.
Pode ver as diferenças entre as reservas e as atribuições de membros da equipa no separador **Equipa** ou no separador **Reconciliação de Recursos**. Também pode reconciliar as diferenças entre as reservas e as atribuições de recursos a um nível mais detalhado.

![Separador Reconciliação de recursos.](media/RM-how-to-4.png)

Também pode utilizar o seletor de recursos no separador **Agenda** para procurar e selecionar recursos reserváveis que ainda não fazem parte da equipa do projeto. Estes são mostrados no seletor de recursos como **Outros Recursos**.

![Atribuir um recurso de um membro não pertencente à equipa a uma tarefa.](media/RM-how-to-5.png)

Quando efetua este procedimento, o recurso é adicionado à equipa do projeto e atribuído à tarefa, mas não são geradas reservas.

![Membro da equipa com atribuições e sem reservas.](media/RM-how-to-6.png)

Pode utilizar a capacidade de expansão da reserva do separador **Reconciliação** ou o **Quadro da Agenda** para reservar a capacidade do recurso para o projeto.

![Expandir reservas para um membro da equipa no separador reconciliação de recursos.](media/RM-how-to-7.png)

Depois de um membro da equipa ficar reservado no seu projeto, pode manter as reservas ou utilizar o Quadro da Agenda diretamente para gerir as respetivas reservas.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
