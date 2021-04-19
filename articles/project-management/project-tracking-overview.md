---
title: Monitorização do esforço do projeto
description: Este tópico fornece informações sobre como monitorizar o esforço e progresso e do trabalho.
author: ruhercul
manager: AnnBe
ms.date: 03/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: ead8821c8861ded1e7afd5c192af414f758edef9
ms.sourcegitcommit: a1f9f92546ab5d8d8e5a4710ce4c96414ea55d14
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 03/24/2021
ms.locfileid: "5710954"
---
# <a name="project-effort-tracking"></a>Monitorização do esforço do projeto

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

A necessidade de monitorizar o progresso relativamente a uma agenda varia de acordo com o setor. Alguns setores monitorizam a um nível granular, ao passo que outros setores monitoram a um nível superior. Este tópico mostra como agendar para satisfazer os requisitos da sua organização.

## <a name="effort-tracking-view"></a>Visto de controlo do esforço

A vista **Controlo do Esforço** monitoriza o progresso das tarefas na agenda ao comparar as horas de esforço reais gastas numa tarefa com as horas de esforço planeadas da tarefa. O Dynamics 365 Project Operations utiliza as seguintes fórmulas para calcular as métricas de monitorização:

- **Percentagem de progresso**: Esforço real gasto até à data ÷ Estimativa na conclusão (EAC) 
- **Esforço restante**: Esforço estimado na conclusão – Esforço real gasto até à data 
- **EAC**: Esforço restante + Esforço real gasto até à data 
- **Desvio do esforço projetado** Esforço planeado – EAC

O Project Operations mostra uma projeção do desvio do esforço na tarefa. Se a EAC for superior ao esforço planeado, a tarefa está projetada para demorar mais tempo do que planeado originalmente e está atrasada. Se a EAC for inferior ao esforço planeado, a tarefa está projetada para demorar menos tempo do planeado originalmente e está adiantada.

## <a name="reprojecting-effort-on-leaf-node-tasks"></a>Reprojetar esforço nas tarefas do nó folha

Os gestores de projeto revêm as estimativas originais de uma tarefa. As reprojeções do projeto são a perceção de estimativas de um gestor de projeto, dado o estado atual de um projeto. No entanto, não recomendamos que os gestores de projetos mudem os números de esforço planeados. Isto porque o esforço planeado do projeto representa a fonte de verdade estabelecida para o calendário do projeto e estimativa de custos e todos os intervenientes no projeto concordaram com ele.

Um gestor de projeto pode reprojetar esforço em tarefas atualizando o valor padrão do **esforço restante** com uma nova estimativa do esforço restante na tarefa. Esta atualização provoca um recalcular da estimativa da tarefa na conclusão (EAC), percentagem de progresso e variação de esforço projetada numa tarefa. A EAC, a ETC e a percentagem de progresso das tarefas de resumo também são recalculadas e produzem uma nova projeção de variância do esforço.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Reprojeção do esforço em tarefas de resumo

O esforço em tarefas de resumo ou tarefas de contentor pode ser reprojetado. Os gestores de projetos podem atualizar o esforço remanescente nas tarefas resumidas. A atualização do esforço remanescente desencadeia o seguinte conjunto de cálculos na aplicação:

- A EAC e a percentagem de progresso na tarefa são calculadas.
- A nova EAC é distribuída para as tarefas subordinadas na mesma proporção que a EAC original na tarefa.
- A nova EAC em cada uma das tarefas individuais até às tarefas do nó de folha é calculada. 
- As tarefas subordinadas afetadas até ao nó de folha têm a sua percentagem de progresso recalculada com base no valor da EAC. Isto resulta numa nova projeção para o desvio do esforço da tarefa. 
- As EACs das tarefas de resumo até ao nó raiz são recalculadas.


## <a name="project-status-summary"></a>Resumo do estado do projeto

Os dados de monitorização nas vistas **Controlo do esforço** e **Controlo dos custos** mostram o progresso e o consumo de custo no nó raiz do projeto, nas tarefas de resumo e nos níveis de tarefas dos nós de folha. A secção **Estado** na página **Entidade do Projeto** mostra um resumo do estado do nível do projeto.

## <a name="status-summary-fields"></a>Campos Resumo do estado

O campo **Estado Geral do Projeto** é um campo editável que mostra o estado geral do projeto. Utiliza a codificação de cores, tal como verde, amarela e vermelha, para indicar um risco de aumento. O campo **Comentários** permite que o gestor de projeto introduza comentários específicos sobre o estado. O campo **Estado atualizado em** não é editável e o valor é um carimbo de data/hora que indica quando o estado foi atualizado pela última vez.

Os campos **Desempenho de Agendamento** e **Desempenho de Custos** são definidos a partir da data de monitorização. Quando os desvios da agenda e de custo do nó raiz na vista **Controlo do esforço** são positivos, é possível definir estes campos como **Adiantado**. Quando os desvios da agenda e de custo do nó raiz são negativos, é possível defini-los como **Atrasado**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
