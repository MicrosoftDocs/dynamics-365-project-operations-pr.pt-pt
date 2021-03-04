---
title: Gerir fusos horários
description: Quando um projeto é criado, o seu fuso horário baseia-se no fuso horário definido no modelo de horas de trabalho aplicado.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 278b226c88c2f441262eb5be0504f34a1964848c
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119837"
---
# <a name="manage-time-zones"></a>Gerir fusos horários

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_


## <a name="projects"></a>Projetos

Quando um projeto é criado, o fuso horário baseia-se no fuso horário definido no modelo de horas de trabalho aplicado. No **Projeto**, as datas são sempre relativas ao fuso horário do utilizador que tem sessão iniciada em cada separador, exceto o separador **Tarefa**. Quando visualizar a estrutura hierárquica do trabalho, as datas serão sempre apresentadas no fuso horário do projeto.

## <a name="tasks"></a>Tarefas

Quando uma tarefa é criada, a hora de início, a hora de fim e as horas/dia são controlados pelas horas de trabalho do projeto. Por exemplo, se for criada uma tarefa com um projeto cujo fuso horário é -8 PST e tiver as seguintes horas de trabalho: 9:00 às 17:00, segunda a sexta-feira, qualquer tarefa criada sem atribuição respeitará a hora de início e a hora de fim do calendário do projeto.

## <a name="manage-resources-with-time-zones"></a>Gerir recursos com fusos horários

Para obter resultados precisos e previsíveis ao utilizar **Expandir Reserva**, existem dois pré-requisitos chave que têm de ser cumpridos:  

- O utilizador tem de configurar o fuso horário do dispositivo para fazer corresponder ao fuso horário definido nas **Definições de Personalização** do sistema.
 
  ![Definições de fuso horário no Windows 10](media/reconcile-assignments-03.png)

  ![Definições de fuso horário nas definições de personalização](media/reconcile-assignments-04.png)
 
- O recurso reservável tem de ter, pelo menos, um minuto de tempo de trabalho que se sobrepõe aos contornos que são utilizados para definir a extensão solicitada. Por exemplo, os seguintes recursos com horas de trabalho que se situam entre as 9:00 e as 19:00 horas. 

  ![Comparação entre os contornos de recursos](media/reconcile-assignments-05.png)

A tabela seguinte mostra:

- Um modelo de calendário de projeto
- Recurso A: este recurso tem o mesmo calendário e está no mesmo fuso horário que o projeto. A hora de início das reservas será 9h00.
- Recurso B: este recurso está localizado num fuso horário diferente daquele do projeto e começa às 7:00 no seu fuso horário. No entanto, as reservas começarão às 9h00, uma vez que se trata da hora de início mais antiga do contorno da atribuição.
- Recursos C e D: os recursos estão localizados em fusos horários diferentes, entre si e do projeto, e as suas reservas não começam antes das respetivas horas de início disponíveis.

|Entidade  |Calendário  |
|-|-|
|Modelo de calendário de projeto   | ![calendário do projeto](media/reconcile-assignments-06.png) |
|Recurso A  | ![Calendário do Recurso A](media/reconcile-assignments-06.png) |
|Recurso B  |  ![Calendário do Recurso B](media/reconcile-assignments-07.png) |
|Recurso C  |  ![Calendário do Recurso C](media/reconcile-assignments-08.png) |
|Recurso D  | ![Calendário do Recurso D](media/reconcile-assignments-09.png)  |
 
Quando navega para a vista **Reconciliação**, são apresentadas as atribuições de recursos e as faltas de reservas associadas.

![Vista de reconciliação antes da extensão](media/reconcile-assignments-10.png)

Após a utilização da funcionalidade Expandir Reserva para cada recurso, as reservas são expandidas com êxito para cada recurso porque as horas de trabalho de cada recurso sobrepõem-se aos perfis da escassez.

![Vista de reconciliação após a extensão da reserva](media/reconcile-assignments-11.png) 

Note que um olhar mais atento aos detalhes das reservas mostra diferenças na hora de início das reservas. As reservas não começam antes da hora de início do perfil da atribuição e não antes da hora de início disponível do recurso.

![Novas reservas dos recursos no quadro da agenda](media/reconcile-assignments-12.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]