---
title: Descrição geral do assistente da agenda
description: Este tópico fornece informações sobre como trabalhar com o Assistente da agenda para reservar recursos.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: da551e805f395e466952df1dbb7d193bdddba358
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908464"
---
# <a name="schedule-assistant-overview"></a>Descrição geral do assistente da agenda

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

O Assistente da agenda é utilizado para reservar recursos baseado nos requisitos definidos pelo Gestor de projeto. O assistente da agenda baseia-se nos parâmetros fornecidos no requisito do recurso para localizar o recurso. O Assistente da agenda recomenda recursos que correspondam aos requisitos relevantes, tais como janelas de tempo ou competências necessárias.

Após a identificação dos recursos adequados, o Gestor de recursos ou o Gestor de projeto pode reservar o recurso para o trabalho.

## <a name="prerequisites"></a>Pré-requisitos

O Assistente da agenda faz parte da solução do Universal Resource Scheduling. Esta solução é incluída e instalada com o Dynamics 365 Project Operations, Dynamics 365 Field Service e Dynamics 365 Customer Service.

## <a name="matching-requirements-and-resources"></a>Requisitos e recursos correspondentes

Um requisito de recursos gerados baseia-se em detalhes como:

-   Características
-   Funções
-   Unidades de negócio
-   Preferências de recurso
-   Perfis de esforço
-   Fuso horário

O Assistente da agenda utiliza estes detalhes para filtrar recursos.

## <a name="launch-the-schedule-assistant"></a>Iniciar o Assistente da agenda

O assistente da agenda pode ser iniciado de duas formas. Se estiver a utilizar o modo híbrido, na grelha de membro de equipa pode selecionar qualquer membro da equipa com um requisito de recurso não concluído e, em seguida, selecione **Reservar**. Se estiver a utilizar o modo central, o Gestor de recursos localiza e seleciona o recurso.

## <a name="schedule-assistant-filters"></a>Filtro do assistente da agenda

Após a execução do Assistente da agenda, os detalhes do requisito do recurso são apresentados como valores filtrados no painel esquerdo. O Gestor de recursos ou o Gestor de projeto pode otimizar os resultados ao ajustar os filtros para satisfazer as necessidades de agendamento.

O painel de filtro mostra opções relacionadas com o trabalho, incluindo:

-   Início e fim do trabalho
-   Características
-   Funções
-   Unidades organizacionais
-   Empresa de recursos
-   Tipos de recursos
-   Recursos preferenciais
