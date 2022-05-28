---
title: Métodos de alocação de reservas no Project Service Automation
description: Este tópico fornece informações sobre as diferentes formas de reservar alocações.
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
ms.openlocfilehash: f0f4f5c68698fbe88de968e65a65b316b10872d9
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8590130"
---
# <a name="booking-allocation-methods-in-project-service-automation"></a>Métodos de alocação de reservas no Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

Se adicionar um membro da equipa diretamente a um projeto no separador **Equipa** ou reservar um recurso para um projeto ou requisito a partir do quadro da Agenda, existem alguns métodos de alocação de reserva diferentes que pode utilizar. Este tópico explica como funciona cada método e quais os métodos que poderão resultar em excesso de reservas dos recursos.

## <a name="full-capacity"></a>Capacidade Total 
O método Capacidade Total reserva a capacidade total do recurso para as datas de e para especificadas. Por exemplo, se um recurso tiver um calendário definido como oito horas por dia de trabalho, cinco dias por semana, definir uma data de início e de fim que abrange cinco dias de trabalho irá reservar o recurso por 40 horas. A reserva é efetuada independentemente da restante capacidade do recurso. Se um recurso já estiver reservado durante esse período em outros projetos, as 40 horas são reservadas como horas adicionais, potencialmente levando a um excesso de reservas.

## <a name="remaining-capacity"></a>Capacidade Restante
O método Capacidade Restante só está disponível quando reserva diretamente para um projeto utilizando o quadro da Agenda. Este método reserva a capacidade disponível do recurso dentro do intervalo de datas especificado. Por exemplo, se um recurso tiver capacidade para 40 horas por semana e já tiver sido reservado 10 horas, a reserva para a mesma semana resultará na reserva das 30 horas restantes de capacidade para essa semana.

## <a name="percentage-capacity"></a>Capacidade Percentual
O método Capacidade de Percentagem reserva o recurso para a percentagem de capacidade para as datas de e para especificadas. Por exemplo, se um recurso tiver um calendário definido como oito horas por dia de trabalho, cinco dias por semana, definir uma data de início e de fim que abrange cinco dias de trabalho com 50% da capacidade irá reservar o recurso por 20 horas. As reservas individuais por dia são espalhadas igualmente durante o período, por exemplo, de quatro horas por dia. A reserva é efetuada independentemente da restante capacidade do recurso. Se o recurso já estiver reservado durante esse período em outros projetos, as 20 horas são reservadas como horas adicionais, potencialmente levando a um excesso de reservas.

## <a name="evenly-distribute-hours"></a>Distribuir Horas Uniformemente
O método Distribuir Horas Uniformemente reserva o recurso para um número especificado de horas distribuindo o tempo uniformemente por dia ao longo das datas de e para especificadas. Por exemplo, se reservou um recurso de 20 horas ao longo de um período de cinco dias, este método distribui as 20 horas uniformemente em quatro horas por dia. A reserva é efetuada independentemente da restante capacidade do recurso. Se o recurso já estiver reservado durante esse período em outros projetos, as 20 horas são reservadas como horas adicionais, potencialmente levando a um excesso de reservas.

## <a name="front-load-hours"></a>Carregar Horas no Início
O método Carregar Horas no Início reserva o recurso para um número especificado de horas carregando inicialmente as horas por dia ao longo das datas de e para especificadas. O Carregamento no Início consome a capacidade disponível do recurso por ordem "primeiro a chegar, primeiro a ser consumido". Por exemplo, se a agenda de trabalho do recurso é de oito horas por dia, cinco dias por semana, e não tem reservas atuais, reservar o recurso por 20 horas ao longo de um período de cinco dias de trabalho forma o seguinte padrão de reserva diária: 

|         Reservas          |    Dia 1    |    Dia 2    |    Dia 3    |    Dia 4    |    Dia 5    |    Total    |
|---------------------------|-------------|-------------|-------------|-------------|-------------|-------------|
|    Reservas existentes    |    0        |    0        |    0        |    0        |    0        |    0        |
|    Nova reserva          |    8        |    8        |    4        |    0        |    0        |    20       |

O método de carregamento no início leva em consideração reservas existentes e capacidade disponível. Por exemplo, se o mesmo recurso já tiver 20 horas de reservas da semana de trabalho, as novas reservas consomem a capacidade restante da seguinte forma:

|   Reservas          | Dia 1 | Dia 2 | Dia 3 | Dia 4 | Dia 5 | Total |
|---------------------|-------|-------|-------|-------|-------|-------|
| Reservas existentes | 8     | 8     | 4     | 0     | 0     | 20    |
| Nova reserva       | 0     | 0     | 4     | 8     | 8     | 20    |

Como a capacidade disponível é considerada, poderá obter uma mensagem de erro se o recurso não tiver qualquer capacidade restante que possa ser absorvida pela reserva. Com este método, não é possível reservar em excesso.

## <a name="none"></a>Nenhum
O método Nenhum só está disponível quando reservar a partir do separador **Equipa** dentro de um projeto. Este método adiciona o recurso como um membro da equipa do projeto, mas não cria quaisquer reservas que absorvam a capacidade do recurso. Este método é utilizado quando o membro da equipa gestor do projeto padrão é adicionado quando um projeto é criado. O utilizador gestor de projeto que criou o projeto é adicionado por predefinição ao projeto, para que o registo de entidade do projeto tenha um proprietário e haja um aprovador no projeto. Como este utilizador não possui reservas, se pretender reservar o recurso, pode eliminá-lo e adicioná-lo novamente utilizando um método de alocação diferente, ou adicionar o recurso às tarefas e, em seguida, utilizar **Reservas Alargadas** no separador **Reconciliação** para criar reservas para atribuições.

## <a name="allocation-methods-that-lead-to-overbooking"></a>Métodos de alocação que levam ao excesso de reservas
Em resumo, os seguintes métodos de alocação levam ao excesso de reservas se o recurso já está empenhado em outros projetos (ou para outras ordens de intervenção ou entidades agendáveis):

- Capacidade Total
- Capacidade Percentual
- Distribuir Horas Uniformemente

Quando utiliza um destes três métodos de alocação, não será notificado que o recurso está com excesso de reservas. Para corrigir o excesso de reservas, terá de utilizar o quadro da Agenda.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
