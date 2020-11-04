---
title: Principais conceitos
description: Este tópico fornece informações sobre os principais conceitos para a gestão de recursos no Project Service Automation.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 1e5e78bbeb1086fada799cf7ac66173e5a563e2d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082628"
---
# <a name="key-concepts"></a>Principais conceitos

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

A tabela seguinte define os principais conceitos que são utilizados na aplicação Dynamics 365 Project Service Automation.

| Conceito                    | Definição |
|----------------------------|------------|
| Membro da equipa do projeto        | Como parte da equipa do projeto, um membro da equipa do projeto pode ser um recurso nomeado que tem reservas, um recurso nomeado que não tem reservas ou um recurso genérico. Os recursos genéricos não têm reservas, são locais no projeto e não têm restrições de capacidade entre os projetos. |
| Recurso genérico do projeto   | Um marcador de posição do recurso que lhe permite formar uma equipa e definir uma equipa para um plano do projeto sem ter de conhecer o recurso nomeado. O calendário do projeto é utilizado como o calendário do recurso genérico. Os recursos genéricos podem ser adicionados a uma equipa do projeto e atribuídos às tarefas. |
| Horas reservadas               | As horas dos recursos são reservadas de forma fixa num projeto para ajudar a garantir que o trabalho do projeto fica concluído. As horas reservadas são consumidas a partir da capacidade geral do recurso. As reservas são apenas para os recursos nomeados, não para os recursos genéricos. |
| Horas atribuídas             | As horas dos recursos são atribuídas às tarefas na agenda do projeto. As atribuições podem ser para recursos nomeados ou recursos genéricos. As atribuições podem ser independentes das reservas. |
| Horas necessárias             | A capacidade necessária, mas ainda não cumprida por um recurso nomeado. As horas necessárias são relevantes apenas para membros da equipa genéricos que geraram requisitos de recursos. |
| Procura                     | A carga de trabalho atual e recebida. No Project Service Automation, a procura é mostrada como requisitos ou pedidos de recursos. |
| Requisito de recurso       | Uma entidade que é utilizada para capturar horas necessárias, datas de início e fim, competências, geografia e outras dimensões de definição de preços dos recursos necessários. Os requisitos de recursos são gerados a partir de membros da equipa do projeto ou criados individualmente. |
| Pedido de recurso           | Uma entidade que é utilizada como um "envelope" para transportar o requisito de recurso que deve ser cumprido por um gestor de recursos. |
| Função predefinida do recurso      | A função na qual um recurso está agrupado para cálculo de utilização. Presume-se que o recurso tenha as competências necessárias para a função e cumpra a utilização de destino para essa função. |
| Unidade organizacional de recursos | A unidade organizacional à qual um recurso está atribuído. |
| Contorno                    | Tarefa, requisito ou horas de atribuição, conforme são divididos numa distribuição diária. Por exemplo, uma tarefa de cinco dias e 40 horas pode ser contornada em oito horas por dia durante cinco dias. |
| Vista de reconciliação        | Uma vista que mostra as reservas e as atribuições para cada membro da equipa do projeto. Esta vista permite que o gestor de projeto procure qualquer incompatibilidade entre reservas e atribuições e tome as ações corretivas se ocorrer alguma incompatibilidade. |
| Horas de trabalho                 | Uma entidade que é utilizada para identificar a capacidade do recurso, bem como as horas de trabalho e de descanso. Esta entidade também é referida como o calendário de recurso. |