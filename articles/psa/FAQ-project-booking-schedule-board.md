---
title: Criar uma reserva de projeto no quadro da Agenda
description: Este tópico fornece informações sobre como criar uma reserva de projeto a partir do quadro da agenda.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: 693f4c4be1371bae232f636a5e168e889e81b09c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578032"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a>Criar uma reserva de projeto no quadro da Agenda

[!include [banner](../includes/psa-now-project-operations.md)]

Pode reservar um recurso para um projeto diretamente no separador **Equipa** do projeto ou através da geração de um requisito de recurso de uma atribuição de membro da equipa genérico e, em seguida, preenchendo o requisito gerado com um membro da equipa do projeto.

Também é possível reservar um recurso para um projeto diretamente do quadro da Agenda. Existem três formas de o fazer:

- **Reservar a partir de um requisito de recurso gerado:** pode gerar um requisito de recurso depois de criar um recurso genérico e atribuir tarefas num projeto.

- **Reservar a partir do requisito principal:** os requisitos principais são mostrados no quadro da Agenda no separador **Projeto**. 

- **Reservar a partir de um requisito de recurso novo:** pode criar um requisito de recurso do zero e associá-lo a um projeto. No quadro da Agenda, o requisito de recurso é mostrado no separador **Abrir Requisitos**.

## <a name="book-from-a-generated-resource-requirement"></a>Reservar a partir de um requisito de recurso gerado

Pode criar um recurso genérico e atribuí-lo a uma ou mais tarefas dentro de um projeto. Em seguida, pode gerar um requisito de recurso a partir do membro da equipa genérico. 

1.  No quadro da Agenda, este recurso será mostrado no separador **Abrir Requisitos**. Também poderá ter de utilizar os filtros de coluna na grelha se tiver muitos requisitos abertos. 

    ![Abrir o separador Requisitos no quadro Agenda.](media/FAQ-Project-Booking-Schedule-Board-1.png "Captura de ecrã da tabela de reservas e atribuições")

2. Selecione o requisito. O separador **Localizar Disponibilidade** será apresentado na parte superior da linha selecionada.
 
3. Quando selecionar o separador, o modo de Assistente de Agenda do quadro da agenda é aberto e, em seguida, filtra os recursos disponíveis que cumprem o requisito de recurso. Depois disso, pode reservar um recurso.

4. Também pode arrastar e largar a linha selecionada da parte inferior do quadro da Agenda numa célula de recurso na grelha acima. Quando for largado, abre o painel **Criar Reserva de Recursos** à direita.

    Selecionar **Reservar** reserva o recurso para a equipa do projeto.

![Painel Criar Reserva de Recursos.](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a>Reservar a partir do Requisito Principal

Criar um projeto no Project Service automaticamente cria um requisito de recursos denominado o Requisito Principal. Este é um requisito vazio que é utilizado para reservar rapidamente um recurso com quadro da Agenda sem a geração de um requisito ou a criação de um do zero. Visto que o requisito está vazio, terá de especificar as datas, bem como o método de alocação e as horas, se aplicável. 

1. Para reservar um recurso com o Requisito Principal, no quadro da Agenda, selecione o separador **Projeto**. Se tiver vários projetos, poderá ter de utilizar o filtro de colunas no **Projeto**.

   ![Filtros de colunas no quadro Agenda.](media/FAQ-Project-Booking-Schedule-Board-2.png "Captura de ecrã da tabela de reservas e atribuições")

2. Selecione o requisito que só tem o nome do projeto como o respetivo nome e uma duração de zero (0).

3. Selecione o separador **Localizar Disponibilidade** que é apresentado na linha. Isto coloca o quadro da Agenda no modo do Assistente de Agenda e mostra os recursos disponíveis que podem ser reservados para o projeto.

4. Como um **Requisito Principal** é um requisito vazio com duração zero (0), terá de definir a duração no painel **Criar Reserva de Recursos** quando selecionar e reservar um recurso.

5. Também pode selecionar o **Requisito Principal do Projeto** na parte inferior da quadro da Agenda e arraste e largue-o num recurso para reservá-lo.
 
    Como o **Requisito Principal** é um requisito vazio com duração zero (0), terá de definir a duração no painel **Criar Reserva de Recursos** quando selecionar e reservar um recurso.
 
    Quando reserva um recurso através do **Requisito Principal** no quadro da Agenda, adiciona-o à equipa do projeto sem quaisquer atribuições.
 
## <a name="book-from-a-new-resource-requirement"></a>Reservar a partir de um requisito de recurso novo
Conclua os seguintes passos para reservar a partir de um novo requisito de recurso. 

1. Aceda a **Requisitos de Recursos** e, em seguida, selecione **Novo** para criar um novo requisito de recurso.

2. No separador **Projeto**, selecione um projeto para associar o requisito ao projeto.
 
    No quadro da Agenda, este novo requisito é apresentado como um **Requisito Aberto** que pode preencher.

3. Reserve o recurso para adicioná-lo à equipa do projeto.

4. Agora que o recurso está reservado, tem de atribuir tarefas manualmente.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
