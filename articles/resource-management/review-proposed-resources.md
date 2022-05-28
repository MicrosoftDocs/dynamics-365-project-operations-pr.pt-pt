---
title: Analisar recursos propostos
description: Este tópico fornece informações sobre como propor recursos do projeto.
author: ruhercul
ms.date: 08/18/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3d2ab3ba9e5b18a2b42acaa2dc51ad94b8189274
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584978"
---
# <a name="review-proposed-resources"></a>Analisar recursos propostos

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

Os gestores de recursos podem propor um recurso ao gestor de projeto utilizando um pedido de recurso.

Para analisar os recursos propostos, siga estes passos:

1. Na grelha **Pedido**, ou no próprio pedido, selecione **Localizar Recursos**.
2. Na página **Assistente da Agenda**, selecione o recurso e confirme se todas as horas propostas estão incluídas na reserva proposta.
3. No painel **Criar Reserva de Recurso**, defina o campo **Estado de Reserva** como **Proposto** e, em seguida, selecione **Reservar**.

    > [!NOTE]
    > A definição do **Estado de Reserva** como **Proposto** não faz uma reserva fixa do recurso nem substitui o recurso genérico pelo membro da equipa nomeado.

    Ocorrem as seguintes atualizações de estado:

    - Na página **Assistente da Agenda**, os indicadores de estado são atualizados para indicar que a reserva é proposta, e não reservada de forma fixa.
    - No pedido de recurso, o estado é alterado para **Necessita de Revisão**.
    - No separador **Equipa** do projeto, o valor **Estado do Pedido** do membro da equipa genérico é alterado para **Necessita de Revisão**.

O gestor de projeto pode aceitar ou rejeitar a proposta.

Quando os gestores de recursos processam pedidos de recursos, podem utilizar qualquer uma das abordagens seguintes:

- Propor vários recursos para satisfazer a procura se não existir um único recurso disponível para cumprir as horas necessárias. Em seguida, as horas propostas são divididas entre vários recursos que podem satisfazer as horas necessárias. Neste cenário, as horas não podem ser sobrepostas.
- Propor menos recursos do que os necessários. Neste cenário, a capacidade do recurso proposto é inferior às horas necessárias que o requerente especificou. Quando o requerente aceita os recursos propostos, é criado um requisito de recurso não cumprido para capturar a procura restante.
- Reservar vários recursos para satisfazer a procura se não existir um único recurso disponível para concluir o trabalho.
- Reserve menos recursos do que os necessários. Nesse cenário, as horas reservadas são menores que as horas necessárias. O sistema orienta-o a propor recursos em vez de reservas, para que o requerente possa verificar e monitorizar a procura restante.

## <a name="resource-availability"></a>Disponibilidade do recurso

Os gestores de recursos têm de conseguir ver a disponibilidade de recursos e atualizar as reservas. Em alguns casos, não existe uma procura formal (pedido de recurso). No entanto, um gestor de recursos deve responder a uma procura não planeada proveniente de outros canais, como e-mails, chamadas telefónicas ou mensagens instantâneas. Os gestores de recursos utilizam o **Quadro da Agenda** para atualizar os recursos e as reservas.

As horas de trabalho dos recursos são utilizadas como base para calcular a disponibilidade de um recurso. As reservas de recursos consomem a capacidade dos recursos.

O **Quadro da Agenda** utiliza cores e sombreados para mostrar as reservas, a disponibilidade, as reservas em excesso e o estado das reservas. Uma definição no **Quadro da Agenda** permite-lhe apresentar uma legenda.

Se uma seta a apontar para a direita aparecer ao lado de um recurso reservável individual no **Quadro da Agenda**, o recurso poderá ser expandido para mostrar os detalhes do trabalho em que o recurso está reservado.

Uma vez que o Dynamics 365 Project Operations utiliza o motor de Universal Resource Scheduling, se tiver o Dynamics 365 Field Service instalado, pode ver os detalhes das reservas de recursos para projetos, ordens de intervenção e outras entidades para as quais expandiu o agendamento.

Para ver mais detalhes sobre um recurso individual, clique com o botão direito do rato para abrir o cartão do recurso.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
