---
title: Analisar recursos propostos
description: Este tópico fornece informações sobre como propor recursos do projeto.
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
ms.openlocfilehash: ad5cbdeb5fe05e6115eb024833a8d58b626ea4c9
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082371"
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

## <a name="billable-utilization"></a>Utilização faturável

Os recursos podem ter uma utilização faturável de destino. Esta utilização de destino é definida como um atributo na função predefinida de um recurso ou definida no registo do recurso reservável individual. Os cálculos de utilização baseiam-se nas horas reais que os recursos reportaram através da utilização de entradas de tempo aprovadas.

As fórmulas que se seguem são utilizadas para calcular a utilização:

- Utilização faturável = Horas reais faturáveis ÷ Capacidade do recurso
- Utilização não faturável = Tempo real com ID do tipo de faturação = Não faturável, Grátis ou Não disponível ÷ Capacidade do recurso
- Interno = Tempo real sem contrato de vendas ÷ Capacidade do recurso
- Capacidade do recurso = Horas de trabalho de recursos – Fora do escritório – Dias de descanso

Pode localizar a vista **Utilização de Recursos** no painel **Recursos**.

Cada célula da grelha representa a percentagem de utilização faturável do recurso num período, tal como um dia, uma semana ou um mês. As fórmulas que se seguem são utilizadas para colorir as células:

- **Verde:** Utilização faturável \>= Utilização de destino do recurso
- **Amarelo:** Utilização de destino – 20 \<= Utilização faturável \< Utilização de destino
- **Vermelho:** Utilização faturável \< Utilização de destino – 20

Uma vez a vista **Utilização de Recursos** é baseada no Quadro da Agenda, pode utilizar as capacidades de filtragem do Quadro da Agenda para filtrar os resultados.

A grelha requer que defina uma utilização de destino na função ou no recurso individual. Para efetuar esta configuração, aceda a **Recursos** \> **Funções do recurso**.

Além disso, deve ser atribuída uma função predefinida a cada recurso reservável. Aceda a **Recursos** \> **Recursos**. No separador **Project Service**, verifique se está definida uma função de recurso e se o campo **É Predefinição** está definido como **Sim**. Pode adicionar funções adicionais em que **É Predefinição = Não**. A função em que **É Predefinição = Sim** é utilizada para avaliar a utilização do recurso relativamente ao alvo dessa função.

No separador **Project Service**, também pode definir uma utilização de destino individual para o recurso. Em seguida, o cálculo da utilização utiliza essa utilização de destino para avaliar o destino do recurso em vez do destino da função predefinida do recurso.

A utilização é mostrada para um recurso apenas se esse recurso tiver aprovado, um tempo faturável durante o período mostrado na grelha.

## <a name="resource-availability"></a>Disponibilidade do recurso

É importante que os gestores de recursos possam ver a disponibilidade de recursos e atualizar as reservas. Em alguns casos, não há uma procura formal (pedido de recurso), mas um gestor de recursos deve responder a uma procura não planeada que vem através de canais como e-mail, chamada telefónica ou mensagem instantânea. Os gestores de recursos utilizam o Quadro da Agenda para atualizar recursos e reservas.

As horas de trabalho dos recursos são utilizadas como base para calcular a disponibilidade de um recurso. As reservas de recursos consomem a capacidade dos recursos.

O Quadro da Agenda utiliza cores e sombreamento para mostrar reservas, disponibilidade e reservas em excesso, bem como o estado das reservas. Uma definição nas definições do Quadro da Agenda permite-lhe mostrar uma legenda.

Se uma seta a apontar para a direita aparecer ao lado de um recurso reservável individual no Quadro da Agenda, o recurso poderá ser expandido para mostrar os detalhes do trabalho em que o recurso está reservado.

Uma vez que o Dynamics 365 Project Operations utiliza o motor Universal Resource Scheduling, se tiver o Dynamics 365 Field Service instalado, pode ver os detalhes das reservas de recursos para projetos, ordens de intervenção e outras entidades para as quais expandiu o agendamento.

Para ver mais detalhes sobre um recurso individual, clique com o botão direito do rato para abrir o cartão do recurso.

