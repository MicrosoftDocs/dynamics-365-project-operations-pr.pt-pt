---
title: Analisar recursos propostos
description: Este tópico fornece informações sobre como propor recursos do projeto.
author: ruhercul
manager: AnnBe
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 54a0924da17eac86e2fa400540e629f6d803aa35
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401187"
---
# <a name="review-proposed-resources"></a>Analisar recursos propostos

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

Os gestores de recursos podem propor um recurso ao gestor de projeto utilizando um pedido de recurso.

1. A partir da grelha de pedido ou do próprio pedido, selecione **Localizar Recursos**.
2. Na página **Assistente da Agenda**, selecione o recurso e, em seguida, no painel **Criar Reserva de Recursos**, no campo **Estado da Reserva**, selecione **Reservar**.

Ocorrem as seguintes atualizações de estado:

- Na página **Assistente da Agenda**, os indicadores de estado são atualizados para indicar que a reserva é proposta, e não reservada de forma fixa.
- No pedido de recurso, o estado é alterado para **Necessita de Revisão**.
- No separador **Equipa** do projeto, o valor **Estado do Pedido** do membro da equipa genérico é alterado para **Necessita de Revisão**.

O gestor de projeto pode aceitar ou rejeitar a proposta.

Quando os gestores de recursos processam pedidos de recursos, podem utilizar qualquer uma das abordagens seguintes:

- Propor vários recursos para satisfazer a procura se não existir um único recurso disponível para cumprir as horas necessárias. Em seguida, as horas propostas são divididas entre vários recursos que podem satisfazer as horas necessárias. Neste cenário, as horas não podem ser sobrepostas.
- Propor menos recursos do que os necessários. Neste cenário, a capacidade do recurso proposto é inferior às horas necessárias que o requerente especificou. Consequentemente, quando o requerente aceita os recursos propostos, é criado um requisito de recurso não cumprido para capturar a procura restante.
- Reservar vários recursos para satisfazer a procura se não existir um único recurso disponível para concluir o trabalho.
- Reservar menos recursos do que os necessários. Nesse cenário, as horas reservadas são menores que as horas necessárias. O sistema orienta-o a propor recursos em vez de reservas, para que o requerente possa verificar e monitorizar a procura restante.

## <a name="resource-availability"></a>Disponibilidade do recurso

É importante que os gestores de recursos possam ver a disponibilidade de recursos e atualizar as reservas. Em alguns casos, não há uma procura formal (pedido de recurso), mas um gestor de recursos deve responder a uma procura não planeada que vem através de canais como e-mail, chamada telefónica ou mensagem instantânea. Os gestores de recursos utilizam o Quadro da Agenda para atualizar recursos e reservas.

As horas de trabalho dos recursos são utilizadas como base para calcular a disponibilidade de um recurso. As reservas de recursos consomem a capacidade dos recursos.

O Quadro da Agenda utiliza cores e sombreamento para mostrar reservas, disponibilidade e reservas em excesso, bem como o estado das reservas. Uma definição nas definições do Quadro da Agenda permite-lhe mostrar uma legenda.

Se uma seta a apontar para a direita aparecer ao lado de um recurso reservável individual no Quadro da Agenda, o recurso poderá ser expandido para mostrar os detalhes do trabalho em que o recurso está reservado.

Uma vez que o Dynamics 365 Project Operations utiliza o motor Universal Resource Scheduling, se tiver o Dynamics 365 Field Service instalado, pode ver os detalhes das reservas de recursos para projetos, ordens de intervenção e outras entidades para as quais expandiu o agendamento.

Para ver mais detalhes sobre um recurso individual, clique com o botão direito do rato para abrir o cartão do recurso.



[!INCLUDE[footer-include](../includes/footer-banner.md)]