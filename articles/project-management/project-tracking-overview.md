---
title: Descrição geral da monitorização do projeto
description: Este tópico fornece informações sobre como monitorizar o progresso e o consumo de custo do projeto.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: f159ecac53b824ef208221bb14958923fb5da63b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127377"
---
# <a name="project-tracking-overview"></a>Descrição geral da monitorização do projeto

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

A necessidade de monitorizar o progresso relativamente a uma agenda varia de acordo com o setor. Alguns setores monitorizam a um nível granular, ao passo que outros setores monitoram a um nível superior. Este tópico mostra como agendar para satisfazer os requisitos da sua organização.

## <a name="effort-tracking-view"></a>Visto de controlo do esforço

A vista **Controlo do Esforço** monitoriza o progresso das tarefas na agenda ao comparar as horas de esforço reais gastas numa tarefa com as horas de esforço planeadas da tarefa. O Dynamics 365 Project Operations utiliza as seguintes fórmulas para calcular as métricas de monitorização:

- **Percentagem de progresso**: Esforço real gasto até à data ÷ Estimativa na conclusão (EAC) 
- **Estimativa para conclusão (ETC)** Esforço planeado – Esforço real gasto até à data 
- **EAC**: Esforço restante + Esforço real gasto até à data 
- **Desvio do esforço projetado** Esforço planeado – EAC

O Project Operations mostra uma projeção do desvio do esforço na tarefa. Se a EAC for superior ao esforço planeado, a tarefa está projetada para demorar mais tempo do que planeado originalmente e está atrasada. Se a EAC for inferior ao esforço planeado, a tarefa está projetada para demorar menos tempo do planeado originalmente e está adiantada.

## <a name="reprojecting-effort"></a>Reprojetar o esforço

Os gestores de projeto revêm as estimativas originais de uma tarefa. As reprojeções do projeto são a perceção de estimativas de um gestor de projeto, dado o estado atual de um projeto. No entanto, não recomendamos que os gestores de projetos alterem os valores da linha de base. Isto porque a linha de base do projeto representa a fonte de verdade estabelecida para a agenda e a estimativa de custo do projeto acordadas por todos os intervenientes.

Existem duas formas de um gestor de projeto poder reprojetar o esforço nas tarefas:

- Substitua a ETC predefinida por uma nova estimativa do esforço real restante na tarefa. 
- Substitua a percentagem de progresso predefinida por uma nova estimativa do verdadeiro progresso na tarefa.

Cada abordagem causa um recálculo da ETC, da EAC, da percentagem de progresso da tarefa e do desvio do esforço projetado numa tarefa. A EAC, a ETC e a percentagem de progresso das tarefas de resumo também são recalculadas e produzem uma nova projeção de variância do esforço.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Reprojeção do esforço em tarefas de resumo

O esforço em tarefas de resumo ou tarefas de contentor pode ser reprojetado. Independentemente de o utilizador reprojetar utilizando o esforço restante ou a percentagem de progresso nas tarefas de resumo, o seguinte conjunto de cálculos começa:

- A EAC, a ETC e a percentagem de progresso na tarefa são calculadas.
- A nova EAC é distribuída para as tarefas subordinadas na mesma proporção que a EAC original na tarefa.
- A nova EAC em cada uma das tarefas individuais até às tarefas do nó de folha é calculada. 
- As tarefas subordinadas afetadas até ao nó de folha têm a ETC e a percentagem de progresso recalculada com base no valor da EAC. Isto resulta numa nova projeção para o desvio do esforço da tarefa. 
- As EACs das tarefas de resumo até ao nó raiz são recalculadas.

### <a name="cost-tracking-view"></a>Vista Controlo dos custos 

A vista **Controlo dos custos** compara o custo real gasto numa tarefa com o custo planeado numa tarefa. 

> [!NOTE]
> Esta vista mostra apenas os custos de mão de obra e não inclui os custos das estimativas de despesas. O Project Operations utiliza as seguintes fórmulas para calcular as métricas de monitorização:

- **Percentagem do custo consumido**: Custo real gasto até à data ÷ Custo estimado na conclusão
- **Custo para conclusão (CTC)**: Custo planeado – Custo real gasto até à data
- **EAC**: Custo Restante + Custo real gasto até à data
- **Desvio de custo projetado**: Custo planeado – EAC

Uma projeção do desvio de custo é mostrada na tarefa. Se a EAC for superior ao custo planeado, a tarefa é projetada para custar mais do que o planeado originalmente. Portanto, está acima do orçamento. Se a EAC for inferior ao custo planeado, a tarefa é projetada para custar menos do que o planeado originalmente. Portanto, está abaixo do orçamento.

## <a name="project-managers-reprojection-of-cost"></a>Reprojeção de custos do gestor de projeto

Quando o esforço é reprojetado, o CTC, a EAC, a percentagem do custo consumido e o desvio de custo projetado são todos recalculados na vista **Controlo dos custos**.

## <a name="project-status-summary"></a>Resumo do estado do projeto

Os dados de monitorização nas vistas **Controlo do esforço** e **Controlo dos custos** mostram o progresso e o consumo de custo no nó raiz do projeto, nas tarefas de resumo e nos níveis de tarefas dos nós de folha. A secção **Estado** na página **Entidade do Projeto** mostra um resumo do estado do nível do projeto.

## <a name="status-summary-fields"></a>Campos Resumo do estado

O campo **Estado Geral do Projeto** é um campo editável que mostra o estado geral do projeto. Utiliza a codificação de cores, tal como verde, amarela e vermelha, para indicar um risco de aumento. O campo **Comentários** permite que o gestor de projeto introduza comentários específicos sobre o estado. O campo **Estado atualizado em** não é editável e o valor é um carimbo de data/hora que indica quando o estado foi atualizado pela última vez.

Os campos **Desempenho de Agendamento** e **Desempenho de Custos** são definidos a partir da data de monitorização. Quando os desvios da agenda e de custo do nó raiz na vista **Controlo do esforço** são positivos, é possível definir estes campos como **Adiantado**. Quando os desvios da agenda e de custo do nó raiz são negativos, é possível defini-los como **Atrasado**.
