---
title: Reservar métodos de alocação
description: Esta tópico fornece informações sobre como os métodos de atribuição de reservas funcionam nas Operações do Projeto.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: c2a964c18c7eae61c5a0239da3b18da31b6ad574
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082354"
---
# <a name="booking-allocation-methods"></a>Reservar métodos de alocação

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

Se adicionar um membro da equipa diretamente a um projeto no separador **Equipa** ou reservar um recurso para um projeto ou requisito a partir do quadro da Agenda, existem alguns métodos de alocação de reserva diferentes que pode utilizar. Este tópico explica como funciona cada método e quais os métodos que poderão resultar em excesso de reservas dos recursos.

## <a name="booking-allocation-methods"></a>Reservar métodos de alocação

Existem seis métodos de atribuição de reservas que pode utilizar:

- [Capacidade total](#full)
- [Capacidade restante](#remaining)
- [Capacidade percentual](#percentage)
- [Distribuir horas uniformemente](#evenly)
- [Carregar horas no início](#front)
- [Nenhuma](#none)

### <a name="full-capacity"></a><a name="full"></a>Capacidade total 
O método Capacidade Total reserva a capacidade total do recurso para as datas de e para especificadas. Por exemplo, se um recurso tiver um calendário definido como oito horas por dia de trabalho, cinco dias por semana, definir uma data de início e de fim que abrange cinco dias de trabalho irá reservar o recurso por 40 horas. A reserva é efetuada independentemente da restante capacidade do recurso. Se um recurso já estiver reservado durante esse período em outros projetos, as 40 horas são reservadas como horas adicionais, potencialmente levando a um excesso de reservas.

### <a name="remaining-capacity"></a><a name="remaining"></a>Capacidade restante
O método Capacidade Restante só está disponível quando reserva diretamente para um projeto utilizando o quadro da Agenda. Este método reserva a capacidade disponível do recurso dentro do intervalo de datas especificado. Por exemplo, se um recurso tiver capacidade para 40 horas por semana e já tiver sido reservado 10 horas, a reserva para a mesma semana resultará na reserva das 30 horas restantes de capacidade para essa semana.

### <a name="percentage-capacity"></a><a name="percentage"></a>Capacidade percentual
O método Capacidade de Percentagem reserva o recurso para a percentagem de capacidade para as datas de e para especificadas. Por exemplo, se um recurso tiver um calendário definido como oito horas por dia de trabalho, cinco dias por semana, definir uma data de início e de fim que abrange cinco dias de trabalho com 50% da capacidade irá reservar o recurso por 20 horas. As reservas individuais por dia são espalhadas igualmente durante o período, por exemplo, de quatro horas por dia. A reserva é efetuada independentemente da restante capacidade do recurso. Se o recurso já estiver reservado durante esse período em outros projetos, as 20 horas são reservadas como horas adicionais, potencialmente levando a um excesso de reservas.

### <a name="evenly-distribute-hours"></a><a name="evenly"></a>Distribuir horas uniformemente
O método Distribuir Horas Uniformemente reserva o recurso para um número especificado de horas distribuindo o tempo uniformemente por dia ao longo das datas de e para especificadas. Por exemplo, se reservou um recurso de 20 horas ao longo de um período de cinco dias, este método distribui as 20 horas uniformemente em quatro horas por dia. A reserva é efetuada independentemente da restante capacidade do recurso. Se o recurso já estiver reservado durante esse período em outros projetos, as 20 horas são reservadas como horas adicionais, potencialmente levando a um excesso de reservas.

### <a name="front-load-hours"></a><a name="front"></a>Carregar horas no início
O método Carregar Horas no Início reserva o recurso para um número especificado de horas carregando inicialmente as horas por dia ao longo das datas de e para especificadas. O Carregamento no Início consome a capacidade disponível do recurso por ordem "primeiro a chegar, primeiro a ser consumido". Por exemplo, se a agenda de trabalho do recurso é de oito horas por dia, cinco dias por semana, e não tem reservas atuais, reservar o recurso por 20 horas ao longo de um período de cinco dias de trabalho forma o seguinte padrão de reserva diária: 

|                           |    Dia 1    |    Dia 2    |    Dia 3    |    Dia 4    |    Dia 5    |    Total    |
|---------------------------|-------------|-------------|-------------|-------------|-------------|-------------|
|    **Reservas existentes**    |    0        |    0        |    0        |    0        |    0        |    0        |
|    **Nova reserva**          |    8        |    8        |    4        |    0        |    0        |    20       |

O método de carregamento no início leva em consideração reservas existentes e capacidade disponível. Por exemplo, se o mesmo recurso já tiver 20 horas de reservas da semana de trabalho, as novas reservas consomem a capacidade restante da seguinte forma:

|                     | Dia 1 | Dia 2 | Dia 3 | Dia 4 | Dia 5 | Total |
|---------------------|-------|-------|-------|-------|-------|-------|
| **Reservas existentes** | 8     | 8     | 4     | 0     | 0     | 20    |
| **Nova reserva**       | 0     | 0     | 4     | 8     | 8     | 20    |

Como a capacidade disponível é considerada, poderá obter uma mensagem de erro se o recurso não tiver qualquer capacidade restante que possa ser absorvida pela reserva. Com este método, não é possível reservar em excesso.

### <a name="none"></a><a name="none"></a>Nenhum
O método Nenhum só está disponível quando reservar a partir do separador **Equipa** dentro de um projeto. Este método adiciona o recurso como um membro da equipa do projeto, mas não cria quaisquer reservas que absorvam a capacidade do recurso. Este método é utilizado quando o membro da equipa gestor do projeto padrão é adicionado quando um projeto é criado. O utilizador gestor de projeto que criou o projeto é adicionado por predefinição ao projeto, para que o registo de entidade do projeto tenha um proprietário e haja um aprovador no projeto. Como este utilizador não possui reservas, se pretender reservar o recurso, pode eliminá-lo e adicioná-lo novamente utilizando um método de alocação diferente, ou adicionar o recurso às tarefas e, em seguida, utilizar **Reservas Alargadas** no separador **Reconciliação** para criar reservas para atribuições.

## <a name="allocation-methods-that-lead-to-overbooking"></a>Métodos de alocação que levam ao excesso de reservas
Em resumo, os seguintes métodos de alocação levam ao excesso de reservas se o recurso já está empenhado em outros projetos (ou para outras ordens de intervenção ou entidades agendáveis):

- Capacidade Total
- Capacidade Percentual
- Distribuir Horas Uniformemente

Quando utiliza um destes três métodos de alocação, não será notificado que o recurso está com excesso de reservas. Para corrigir o excesso de reservas, terá de utilizar o quadro da Agenda.
