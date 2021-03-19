---
title: Atribuir um recurso a uma tarefa
description: Este tópico fornece informações sobre como atribuir recursos a tarefas.
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
ms.openlocfilehash: 486371df2de8b400f200dbf38e66cb5e2dec7ae7
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286262"
---
# <a name="assign-a-resource-to-a-task"></a>Atribuir um recurso a uma tarefa

[!include [banner](../includes/psa-now-project-operations.md)]

Existem três formas de atribuir um recurso a uma tarefa no Microsoft Dynamics 365 Project Service Automation.

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a>Reservar um recurso como um membro da equipa e, em seguida, atribuir o recurso a uma tarefa

Pode adicionar um recurso à equipa do projeto e, em seguida, atribuir o recurso a tarefas na agenda do projeto.

1. No separador **Membro da Equipa**, adicione um membro da equipa novo selecionando **Novo**. 

2. Abre-se o painel **Criação Rápida de Membros da Equipa**, onde pode selecionar o nome de recurso reservável e definir uma função. 

    Escolha um dos seguintes métodos de alocação para a reserva do recurso:

    - **Capacidade Total** reserva a capacidade total do recurso para as datas de e para especificadas.
    - **Capacidade de Percentagem** reserva o recurso para a percentagem de capacidade do recurso para as datas de e para especificadas.
    - **Distribuir Igualmente por Horas** reserva o recurso para um número especificado de horas distribuindo-as uniformemente por dia ao longo das datas de e para especificadas.
    - **Carregamento no Início Por Horas** reserva o recurso para um número especificado de horas carregando inicialmente as horas por dia ao longo das datas de e para especificadas.
    - **Nenhum** adiciona o recurso à equipa, mas não cria quaisquer reservas que absorvam a sua capacidade.

3. Na grelha **Agenda** para uma tarefa, selecione o ícone **Recurso** na célula de recursos e, em seguida, em **Membros da Equipa**, selecione o membro da equipa que acabou de adicionar. 

> [!NOTE]
> Nos separadores **Membro da Equipa** e **Reconciliação**, o recurso mostra as horas reservadas e as horas atribuídas. As horas devem ser iguais, mas não têm de ser, uma vez que as reservas e as atribuições não estão totalmente ligadas. O separador **Reconciliação** oferece-lhe detalhes quando forem diferentes, por exemplo, quando atribui a um recurso mais horas mais do que as que reservou. Se necessário, poderá corrigir as informações através da expansão das reservas do recurso ou da alteração da atribuição.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Criar um membro da equipa genérico através de atribuição da tarefa

Quando cria um membro da equipa genérico através de atribuição da tarefa, cria um marcador de posição ou recurso genérico que descreve as características do recurso nomeado que, em última análise, pretende que funcione nas tarefas. Em seguida, gera um requisito (ou submete um pedido utilizando o requisito) que é utilizado para procurar e reservar o recurso nomeado.

1. Na grelha **Agenda** para uma tarefa, selecione o ícone **Recurso** na célula de recurso.

2. Escreva um nome para servir como o nome do recurso de marcador de posição. Por exemplo, Gestor do Programa.

3. Selecione **Criar** e no campo **Criação Rápida de Membro da Equipa do Projeto**, defina a função do recurso genérico.

4. Pode continuar a atribuir tarefas a este recurso de marcador de posição selecionando o recurso no **Seletor de Recursos** para a tarefa. Estão listados em **Membros da Equipa**.

5. Quando tiver terminado a atribuição de recurso genérico, selecione-o no separador **Equipa** e selecione **Gerar Requisito** para criar um requisito de recurso para o recurso genérico.

6. Selecione **Reservar** para o recurso genérico. Em seguida, pode utilizar o quadro da Agenda para localizar e reservar um recurso real. Também é possível enviar o requisito para preenchimento por um gestor de recursos.

7. Quando o recurso genérico é preenchido com um recurso nomeado, o recurso genérico é removido da equipa e as atribuições de tarefas para o recurso genérico são atribuídas ao recurso nomeado que preencheu o requisito de recurso genérico do recurso.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Atribuir um recurso nomeado da lista de todos os recursos reserváveis

Pode utilizar a caixa de pesquisa no **Seletor de Recursos** para procurar todos os recursos reserváveis e atribui-los a uma tarefa.

Os recursos atribuídos desta forma são adicionados à equipa sem quaisquer reservas. Isto é semelhante à adição de um membro da equipa e à seleção de Nenhum como o método de alocação. O recurso é apresentado nos separadores **Equipa** e **Reconciliação** como recursos com atribuições apenas e um deficit de reserva. Reserve-os se quiser utilizar a sua disponibilidade.

1. Na grelha **Agenda** para uma tarefa, selecione o ícone **Recurso** na célula de recurso.

2. Comece a escrever um nome. Os resultados da pesquisa para o nome são apresentados no **Seletor de Recursos** em **Outros Recursos**.

3. Selecione o recurso que pretende atribuir à tarefa.



[!INCLUDE[footer-include](../includes/footer-banner.md)]