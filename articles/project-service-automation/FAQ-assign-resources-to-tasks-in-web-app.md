---
title: Como atribuir um recurso reservável a uma tarefa na aplicação Web
description: Uma descrição geral das maneiras pelas quais pode atribuir recursos reserváveis.
author: JohnPBurrows
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 2.x on platform version 9.x
ms.assetid: 9db35b39-8dfc-4989-9160-fd841fe0ae5a
ms.author: john.burrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 521ea73c948619816d3cd06d72140fcc85366397
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754632"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a>Como atribuir um recurso reservável a uma tarefa na aplicação Web (aplicação Project Service v2.x)?

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Existem duas formas de atribuir um recurso a uma tarefa no Project Service. Pode reservar um recurso como um membro da equipa e, em seguida, atribui-lo a uma tarefa Alternativamente, pode criar um membro da equipa genérico através de atribuição de função de tarefas, gerar uma equipa e, em seguida, cumprir os requisitos de cópia de segurança com um recurso nomeado.

Tenha em atenção que se pretende atribuir um recurso reservável a uma tarefa, membro da equipa do recurso reservável tem de ter reservas disponíveis suficientes. O estado da reserva tem de ser Tipo de Submissão Reserva Forçada e em estado Submetida. Se existirem reservas suficientes para o recurso, o Project Service remove a atribuição e apresenta a seguinte mensagem de erro:

*Não é possível atribuir recursos à tarefa – os seguintes recursos não têm horas suficientes reservadas para o projeto*

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a>Reservd um recurso como um membro da equipa e, em seguida, atribua o recurso a uma tarefa

Com este método, adiciona um recurso à equipa do projeto e, em seguida, atribui tarefas ao recurso na agenda do projeto. Eis como fazê-lo:
1.  Na grelha de membro da equipa, adicione um membro da equipa novo selecionando **Novo**.
2.  No ecrã Criação Rápida de Membro da Equipa, selecione o nome de recurso reservável e defina uma função.
3.  Selecione as datas **De** e **Para**.

    > [!div class="mx-imgBorder"] 
    > ![Captura de ecrã da adição de membro da equipa](media/FAQ-Resources-to-Tasks2-1.png "Captura de ecrã da adição de membro da equipa")
 
4.  Escolha um dos seguintes métodos de alocação para o agendamento do recurso:
    - **Capacidade Total** reserva a capacidade total do recurso para as datas de e para especificadas.
    - **Capacidade de Percentagem** reserva o recurso para a percentagem de capacidade do recurso para as datas de e para especificadas.
    - **Distribuir Igualmente por Horas** reserva o recurso para um número especificado de horas distribuindo-as uniformemente por dia ao longo das datas de e para especificadas.
    - **Carregamento no Início Por Horas** reserva o recurso para um número especificado de horas carregando inicialmente as horas por dia ao longo das datas de e para especificadas.

    Não selecione **Nenhum** porque adiciona o recurso à equipa do projeto, mas não cria quaisquer reservas que absorvam a capacidade do recurso.
5.  Selecione **Guardar**.

    Tenha em atenção que as horas da reserva têm de ser suficientes para abranger as horas de esforço e os intervalos de datas das tarefas a que atribui este recurso. Se não estiverem em alinhamento, não pode atribuir o recurso para a tarefa.

6.  Na estrutura hierárquica do trabalho (WBS) para a tarefa, clique no menu suspenso da célula do recurso. Então: 

    1. Selecione **Adicionar**.
    2. Selecione o menu suspenso em **Recursos** e selecione o membro da equipa que adicionou acima.
    3. Selecione **OK**. Agora, o membro da equipa está atribuído à tarefa.

    > [!div class="mx-imgBorder"] 
    > ![Captura de ecrã da adição de recursos com WBS](media/FAQ-Resources-to-Tasks2-2.png "Captura de ecrã da adição de recursos com WBS")
 
Na grelha de membro da equipa, verá o agregado das horas atribuídas ao recurso em Horas Atribuídas. Serão menos ou iguais às horas reservadas para o recurso. 

> [!div class="mx-imgBorder"] 
> ![Captura de ecrã das horas atribuídas a um recurso](media/FAQ-Resources-to-Tasks2-3.png "Captura de ecrã das horas atribuídas a um recurso")
 
Se a tarefa que estiver a tentar atribuir ao recurso iniciar após a data de fim das reservas dos recursos, o recurso não aparecerá no menu suspenso.

Tenha em atenção que pode atribuir um recurso a mais horas do que as respetivas horas reservadas se o recurso tiver alguma capacidade restante não atribuída. Neste caso, o recurso será apenas parcialmente atribuído até às reservas. Pode ver estas horas tarefas nãos atribuídas restantes adicionando a coluna de Horas com Falta de Recursos à estrutura hierárquica do trabalho.

Se os recursos são atribuídos às respetivas horas reservadas (as respetivas horas reservadas são iguais às suas horas atribuídas), verá a seguinte mensagem de erro ao tentar atribuir-lhes mais tarefas:

*Não é possível atribuir recursos à tarefa – os seguintes recursos não têm horas suficientes reservadas para o projeto.*

Além disso, o membro da equipa gestor do projeto predefinido que é adicionado à equipa quando cria o projeto é adicionado sem quaisquer reservas e não pode ser atribuído a qualquer tarefa. Eles não aparecerão no menu suspenso de recursos para tarefas.

Se pretender atribuir este recurso, será necessário removê-las da equipa e adicioná-las novamente com um método de alocação diferente de Nenhum. A razão pela qual são adicionados à equipa aquando da criação do projeto é para que um projeto tenha, pelo menos, uma aprovador de projeto por predefinição.

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a>Criar um membro da equipa genérico através de atribuição de funções em tarefas

Este método assegura que os recursos têm reservas suficientes para tarefas. Em primeiro lugar, cria um marcador de posição ou recurso genérico que descreve as características do recurso nomeado que, em última análise, pretende que trabalhe nas tarefas ao gerar uma equipa depois de atribuir funções a tarefas. Eis como fazê-lo:

1. Na estrutura hierárquica do trabalho, selecione uma tarefa.
2. Selecione o ícone do menu suspenso **Função Atribuída** na célula do recurso.
3. Selecione o menu suspenso **Função** e selecione a função para o recurso genérico.
4. Selecione **OK**.

    > [!div class="mx-imgBorder"] 
    > ![Captura de ecrã da utilização de WBS para adicionar recurso](media/FAQ-Resources-to-Tasks2-4.png "Captura de ecrã da utilização de WBS para adicionar recurso")
 
Quando tiver concluído a atribuição de funções às tarefas no WBS, selecione **Gerar Equipa do Projeto**. O Project Service cria a quantidade mínima de membros da equipa genéricos com base nas funções, unidades de organização e calendário do projeto ao agregar as atribuições de tarefas.

> [!div class="mx-imgBorder"] 
> ![Captura de ecrã da geração da equipa do projeto](media/FAQ-Resources-to-Tasks2-5.png "Captura de ecrã da geração da equipa do projeto")
 
Na grelha Membro da Equipa, verá recursos do tipo Recurso Genérico com o nome da função e posição. Se forem necessários dois recursos para uma função concluir o trabalho, a funcionalidade Gerar Equipa cria dois membros da equipa e utiliza o nome de posição para os diferenciar.

> [!div class="mx-imgBorder"] 
> ![Captura de ecrã da adição de dois recursos genéricos](media/FAQ-Resources-to-Tasks2-6.png "Captura de ecrã da adição de dois recursos genéricos")
 
Pode abrir o requisito de recursos de cópia de segurança do membro da equipa genérico selecionando a ligação em Requisito de Recurso.

> [!div class="mx-imgBorder"] 
> ![Captura de ecrã da abertura de suporte do requisito de recurso](media/FAQ-Resources-to-Tasks2-7.png "Captura de ecrã da abertura de suporte do requisito de recurso")

Selecione **Reservar** para o recurso genérico e, em seguida, pode utilizar o quadro da agenda para localizar e reservar um recurso real. Também é possível enviar o requisito para preenchimento por um gestor de recursos selecionando **Enviar Pedido**.

Quando o recurso genérico é preenchido com um recurso nomeado, o recurso genérico é removido da equipa e as atribuições de tarefas para o recurso genérico são atribuídas ao recurso nomeado que preencheu o requisito de recurso genérico do recurso.
 

