---
title: Reconciliar reservas e atribuições
description: Este tópico fornece informações sobre os valores reais.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 11/27/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 614352ba-dbd8-4fa5-8225-d54f9ec0e218
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 27fc7b6abb4c9a7a761059a2f392f13bc0dd14f9
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754617"
---
# <a name="reconcile-bookings-and-assignments"></a>Reconciliar reservas e atribuições

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

As reservas de projetos e as atribuições de tarefas de um membro da equipa do projeto têm uma ligação fraca. Consequentemente, um recurso pode ter atribuições de tarefas que não correspondem a reservas e reservas que não correspondem a atribuições de tarefas. Idealmente, as reservas e atribuições de projetos são alinhadas, de modo que os recursos tenham capacidade comprometida para executar as suas atribuições de tarefas. No entanto, a realidade é que as reservas podem ocorrer com base na disponibilidade, sendo que as temporizações das tarefas podem ser alteradas à medida que o projeto continua ao longo do ciclo de vida. Consequentemente, a ligação fraca permite flexibilidade.

Devido à ligação fraca de reservas de projetos e atribuições de tarefas, é incluído um separador **Reconciliação** na entidade do Projeto. Este separador ajuda os gestores de projeto a reconciliar as reservas dos membros da equipa e as suas atribuições para a equipa do projeto.

Para cada membro da equipa nomeado, o separador **Reconciliação** mostra reservas e atribuições até à atribuição de tarefas individuais. Mostra horas nas células que podem representar períodos de meses a dias.

No campo **Escala temporal**, pode selecionar **Mês**, **Semana** ou **Dia**. Por predefinição, está selecionado **Semana**. No entanto, pode alterar o valor predefinido selecionando o botão **Definições**. Quando o separador **Reconciliação** é aberto, mostra a data atual, mas pode utilizar o controlo de calendário para avançar ou retroceder no tempo. Quando um projeto tem uma data de início no futuro, o separador mostra essa data quando é aberto. O controlo de calendário também tem opções que lhe permitem mover para as datas de início e de fim do projeto.

Pode utilizar os controlos de expansão em cada recurso para mostrar os detalhes das reservas do recurso. Também pode expandir as atribuições de cada recurso para o nível da tarefa individual.

A parte inferior do separador **Reconciliação** mostra um total líquido global para o projeto e o separador também inclui uma coluna de total. Para cada recurso, o separador faz a diferença entre as reservas de um membro da equipa no projeto e o rollup das atribuições de tarefas desse membro da equipa. O ideal é que a diferença seja 0 (zero). Por outras palavras, não deve haver diferença entre as reservas do recurso e as atribuições de tarefas. Quaisquer diferenças são indicadas por cor e sombreamento para destacar duas condições:

- **Falta de reserva** – As faltas de reserva ocorrem quando um recurso tem mais atribuições do que reservas. Como esta capacidade não foi reservada, um gestor de projeto pode corrigir esta condição, expandindo as reservas do recurso para cobrir a falta.
- **Reservas em excesso** – As reservas em excesso ocorrem quando um recurso foi reservado para o projeto, mas ainda não foi atribuído às tarefas. Esta condição poderá ser aceitável se, por exemplo, o recurso tiver sido reservado antes de a atribuição de tarefas ocorrer. No entanto, em outros casos, o recurso pode não estar planeado para ser atribuído. Nestes casos, o gestor de projeto deverá considerar o cancelamento das reservas do recurso, para que a capacidade possa ser utilizada para outro projeto.

> [!NOTE]
> A legenda para estas condições poderá estar oculta para deixar mais espaço para a grelha. Neste caso, pode tornar a legenda visível selecionando o botão **Definições**.

Em alguns casos, quando o campo **Escala temporal** está definido como um nível superior a **Dia**, as diferenças podem ser calculadas como 0 (zero). Por exemplo, no nível **Mês**, a diferença líquida de um recurso poderá ser 0 (zero) para indicar que as reservas são iguais às atribuições. No entanto, se observar o nível **Semana**, poderá ver que existem atribuições de 0 (zero) horas e reservas de 40 horas na primeira semana do mês, e atribuições de 40 horas e reservas de 0 (zero) horas na segunda semana do mês. Apesar de o total de reservas e atribuições para o mês serem iguais, são diferentes por semana.

Quando visualiza níveis de tempo superiores, o separador **Reconciliação** mostra um indicador de célula para notificá-lo de que existem diferenças em níveis de tempo inferiores. Por exemplo, na ilustração seguinte, é apresentado um indicador de célula na célula para o mês de outubro de 2018 relativamente ao recurso com o nome Gabriela Gomes. Consequentemente, pode ver que, apesar de as reservas e as atribuições do recurso serem iguais quando são agregadas no nível **Mês**, não correspondem nos níveis inferiores.

![Reservas e atribuições não correspondidas](media/reconcile-assignments-01.JPG)

Faça duplo clique numa célula para ampliar o nível inferior seguinte e ver a diferença. Por exemplo, se clicar duas vezes na diferença de outubro de 2018 para Gabriela Gomes, irá desagregar para o nível **Semana**. Pode ver que o recurso tem reservas de 16 horas, mas não atribuições nas duas primeiras semanas de outubro e 16 horas de atribuições, mas não reservas na terceira semana de outubro.

![Reservas e atribuições não correspondidas](media/reconcile-assignments-02.JPG)

Pode clicar com o botão direito do rato numa célula para reduzir o nível superior seguinte. Também é possível desativar o indicador de célula selecionando o botão **Definições**. 

Também pode utilizar os botões **Anterior** e **Seguinte** acima da grelha para percorrer qualquer diferença no seu projeto. Para utilizar estes botões, primeiro tem de selecionar um recurso. Selecione **Seguinte** para ir para a próxima diferença entre as reservas e as atribuições para esse recurso. Selecione **Anterior** para ir para a diferença anterior.

Nas situações em que tem atribuições de tarefas para um recurso, mas não há reservas, é possível selecionar a falta de reserva e, em seguida, selecione **Expandir Reserva**. Em seguida, pode ver a reserva necessária para resolver a falta do recurso. Também pode ver as reservas do recurso no projeto atual e noutros projetos. Selecione **OK** para criar a reserva para o recurso sem considerar a disponibilidade atual. O gestor de projeto ou o gestor de recursos pode utilizar o Quadro da Agenda para gerir situações em que um recurso ficou com excesso de reservas além da capacidade, porque as suas reservas foram expandidas.

## <a name="managing-with-time-zones"></a>Gerir com fusos horários
Para assegurar resultados exatos e previsíveis ao utilizar Expandir Reserva, existem dois pré-requisitos chave que têm de ser satisfeitos:  

- O utilizador tem de configurar o fuso horário do dispositivo para corresponder ao fuso horário definido nas Definições de Personalização do seu sistema.
 
  ![Definições de fuso horário no Windows 10](media/reconcile-assignments-03.png)

  ![Definições de fuso horário nas definições de personalização](media/reconcile-assignments-04.png)
 
- O Recurso Agendável tem de ter, pelo menos, um minuto de tempo de trabalho que se sobrepõe aos contornos que são utilizados para definir a extensão solicitada. Por exemplo, o exemplo seguinte mostra a revisão de recursos com horas de trabalho que caem entre as 9h00 e as 19h00. 

  ![Comparação entre os contornos de recursos](media/reconcile-assignments-05.png)

A tabela seguinte mostra:

- Um modelo de calendário de projeto.
- Recurso A: este recurso tem o mesmo calendário e está no mesmo fuso horário que o projeto. A hora de início das reservas será 9h00.
- Recurso B: este recurso encontra-se num fuso horário diferente do do projeto e, por conseguinte, começa às 7h00 no fuso horário correspondente. No entanto, as reservas começarão às 9h00, uma vez que se trata da hora de início mais antiga do contorno da atribuição.
- Recursos C e D: os recursos também estão localizados em fusos horários diferentes, ambos diferentes uns dos outros e do projeto, e as respetivas reservas começam depois das respetivas horas de início disponíveis.

|Entidade  |Calendário  |
|-|-|
|Modelo de calendário de projeto   | ![calendário do projeto](media/reconcile-assignments-06.png) |
|Recurso A  | ![Calendário do Recurso A](media/reconcile-assignments-06.png) |
|Recurso B  |  ![Calendário do Recurso B](media/reconcile-assignments-07.png) |
|Recurso C  |  ![Calendário do Recurso C](media/reconcile-assignments-08.png) |
|Recurso D  | ![Calendário do Recurso D](media/reconcile-assignments-09.png)  |
 
Quando navega para a vista de reconciliação, as atribuições de recursos e as respetivas escassezes de reserva são apresentadas.
 ![Vista de reconciliação antes da extensão](media/reconcile-assignments-10.png)

Depois de a funcionalidade Expandir Reserva ter sido executada em cada recurso, as reservas são expandidas com êxito para cada recurso. Isto porque as horas de trabalho de cada recurso estão sobrepostas aos contornos da escassez.
 ![Vista de reconciliação após a extensão da reserva](media/reconcile-assignments-11.png) 

No entanto, uma análise mais detalhada dos detalhes das reservas mostra diferenças na hora de início das reservas. As reservas serão iniciadas nunca antes da hora de início do contorno da atribuição e nunca antes da hora de início disponível do recurso.
 ![Novas reservas dos recursos no quadro da agenda](media/reconcile-assignments-12.png)
