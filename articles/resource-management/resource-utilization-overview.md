---
title: Descrição geral da utilização de recursos
description: Este tópico fornece informações sobre a vista de utilização de recursos no Project Operations.
author: ruhercul
ms.date: 11/05/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: e24bbb33cdf34426d4e7fff21b68fcaea2fcef5e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8587140"
---
# <a name="resource-utilization-overview"></a>Descrição geral da utilização de recursos

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

Os recursos podem ter uma utilização faturável de destino. Esta utilização de destino é definida como um atributo na função predefinida de um recurso ou definida no registo do recurso reservável individual. Os cálculos de utilização baseiam-se nas horas reais que os recursos reportaram através da utilização de entradas de tempo aprovadas.

As fórmulas que se seguem são utilizadas para calcular a utilização:

  - Utilização faturável = Horas reais faturáveis ÷ Capacidade do recurso
  - Utilização não faturável = Tempo real com ID do tipo de faturação = Não faturável, Grátis ou Não disponível ÷ Capacidade do recurso
  - Interno = Tempo real sem contrato de vendas ÷ Capacidade do recurso
  - Capacidade do recurso = Horas de trabalho de recursos – Fora do escritório – Dias de descanso

Pode localizar a vista **Utilização de Recursos** no painel **Recursos**.

Cada célula da grelha representa a percentagem de utilização faturável do recurso num período, tal como um dia, uma semana ou um mês. As fórmulas que se seguem são utilizadas para colorir as células:

  - **Verde**: Utilização faturável >= Utilização de destino do recurso
  - **Amarelo**: Utilização de destino – 20 < = Utilização faturável < Utilização de destino
  - **Vermelho**: Utilização faturável < Utilização de destino – 20

Uma vez a vista **Utilização de Recursos** é baseada no Quadro da Agenda, pode utilizar as capacidades de filtragem do Quadro da Agenda para filtrar os resultados.

A grelha requer que defina uma utilização de destino na função ou no recurso individual. Para efetuar esta configuração, aceda a **Recursos** > **Funções do recurso**.

Além disso, deve ser atribuída uma função predefinida a cada recurso reservável. Aceda a **Recursos** > **Recursos**. No separador **Project Service**, verifique se está definida uma função de recurso e se o campo **É Predefinição** está definido como **Sim**. Pode adicionar funções adicionais em que **É Predefinição** = **Não**. A função em que **É Predefinição** = **Sim** é utilizada para avaliar a utilização do recurso relativamente ao alvo dessa função.

No separador **Project Service**, também pode definir uma utilização de destino individual para o recurso. Em seguida, o cálculo da utilização utiliza essa utilização de destino para avaliar o destino do recurso em vez do destino da função predefinida do recurso.

A utilização é apenas mostrada para um recurso se esse recurso tiver aprovado, um tempo faturável durante o período mostrado na grelha.


[!INCLUDE[footer-include](../includes/footer-banner.md)]