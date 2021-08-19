---
title: Progresso e consumo de custo do projeto
description: Este tópico fornece informações sobre a monitorização do progresso e o consumo de custo do projeto.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 08/21/2020
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
ms.openlocfilehash: 8bde19fbf1dd9f0c760455ecb7f7f2bd14a358d441bf024ec0cdefa42866f53e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987180"
---
# <a name="project-progress-and-cost-consumption"></a>Progresso e consumo de custo do projeto

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

A necessidade de monitorizar o progresso relativamente a uma agenda varia de acordo com o setor. Alguns setores monitorizam a um nível granular, ao passo que outros setores monitoram a um nível superior. Este tópico mostra como agendar para satisfazer os requisitos da sua organização.

## <a name="effort-tracking-view"></a>Visto de controlo do esforço

A vista **Controlo do Esforço** monitoriza o progresso das tarefas na agenda. Esta vista compara as horas de esforço reais de uma tarefa com as horas de esforço planeadas para essa tarefa. O Project Service Automation utiliza as seguintes fórmulas para calcular as métricas de monitorização:

Inicialmente na criação de tarefas: O custo previsto será definido para o custo estimado ao completar. Uma vez que os Atuais são registados na tarefa, o seguinte será o cálculo na vista de Monitorização para Esforço

- Percentagem de progresso = Esforço real gasto até à data = Estimativa na conclusão (EAC) 
- Estimativa para conclusão (ETC) = Estimativa na conclusão (EAC) – Esforço real gasto até à data 
- EAC = Esforço restante + Esforço real gasto até à data 
- Desvio do esforço projetado = Esforço planeado – EAC

O Project Service Automation mostra uma projeção do desvio do esforço na tarefa. Se a EAC for superior ao esforço planeado, a tarefa é projetada para levar mais tempo do que o planeado originalmente. Consequentemente, está atrasada. Se a EAC for inferior ao esforço planeado, a tarefa é projetada para levar menos tempo do que o planeado originalmente. Consequentemente, está adiantada.

## <a name="reprojecting-effort"></a>Reprojetar o esforço

É comum que um gestor de projeto reveja as estimativas originais de uma tarefa. As reprojeções do projeto são a perceção de estimativas de um gestor de projeto, dado o estado atual de um projeto. No entanto, não recomendamos que os gestores de projeto alterem os valores da linha de base, porque a linha de base do projeto representa a fonte de verdade estabelecida para a agenda e a estimativa de custo do projeto acordadas por todos os intervenientes.

Existem duas formas de um gestor de projeto poder reprojetar o esforço nas tarefas:

- Substitua a ETC predefinida por uma nova estimativa do esforço real restante na tarefa. 
- Substitua a percentagem de progresso predefinida por uma nova estimativa do verdadeiro progresso na tarefa.

Cada uma destas abordagens causa um recálculo da ETC, da EAC e da percentagem de progresso da tarefa e o desvio do esforço projetado numa tarefa. A EAC, a ETC e a percentagem de progresso das tarefas de resumo também são recalculadas e produzem uma nova projeção de variância do esforço.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Reprojeção do esforço em tarefas de resumo

O esforço em tarefas de resumo ou tarefas de contentor pode ser reprojetado. Independentemente de o utilizador reprojetar utilizando o esforço restante ou a percentagem de progresso nas tarefas de resumo, o seguinte conjunto de cálculos começa:

- A EAC, a ETC e a percentagem de progresso na tarefa são calculadas.
- A nova EAC é distribuída para as tarefas subordinadas na mesma proporção que a EAC original na tarefa.
- A nova EAC em cada uma das tarefas individuais até às tarefas do nó de folha é calculada. 
- As tarefas subordinadas afetadas até ao nó de folha têm a ETC e a percentagem de progresso recalculada com base no valor da EAC. Isto resulta numa nova projeção para o desvio do esforço da tarefa. 
- As EACs das tarefas de resumo até ao nó raiz são recalculadas.

### <a name="cost-tracking-view"></a>Vista Controlo dos custos 

A vista **Controlo dos custos** compara o custo real gasto numa tarefa com o custo planeado. 

> [!NOTE]
> Esta vista mostra apenas os custos de mão de obra e não inclui os custos das estimativas de despesas. 

O Project Service Automation utiliza as seguintes fórmulas para calcular as métricas de monitorização:

Quando uma tarefa é criada, o custo previsto é igual ao custo estimado aquando da conclusão. Depois dos Atuais serem registados na tarefa, o seguinte é calculado na vista **Monitorização** para o custo:

 - Percentagem do custo consumido = Custo real gasto até à data ÷ Custo estimado na conclusão para a tarefa
 - Custo para conclusão (CTC) = Custo estimado na conclusão – Custo real gasto até à data
 - Custo estimado na conclusão = CTC + Custo real gasto até à data
 - Variância de custos projetados = Custo planeado – Custo estimado na conclusão

Uma projeção do desvio de custo é mostrada na tarefa. Se o custo estimado na conclusão for superior ao custo planeado, a tarefa é projetada para custar mais do que o planeado originalmente. Portanto, está acima do orçamento. Se o custo Estimado na conclusão for inferior ao custo planeado, a tarefa é projetada para custar menos do que o planeado originalmente e está dentro do orçamento.

## <a name="project-managers-reprojection-of-cost"></a>Reprojeção de custos do gestor de projeto

Quando o esforço é reprojetado, o CTC, o Custo estimado na conclusão, a percentagem do custo consumido e o desvio de custo projetado são todos recalculados na vista **Controlo dos custos**.

## <a name="project-status-summary"></a>Resumo do estado do projeto

Os dados de monitorização nas vistas **Controlo do esforço** e **Controlo dos custos** mostram o progresso e o consumo de custo no nó raiz do projeto, nas tarefas de resumo e nos níveis de tarefas dos nós de folha. A secção **Estado** na página **Entidade do Projeto** mostra um resumo do estado do nível do projeto.

## <a name="status-summary-fields"></a>Campos Resumo do estado

O campo **Estado Geral do Projeto** é um campo editável que mostra o estado geral do projeto. Utiliza a codificação de cores, tal como verde, amarela e vermelha, para indicar um risco de aumento. O campo **Comentários** permite que o gestor de projeto introduza comentários específicos sobre o estado. O campo **Estado atualizado em** não é editável e o valor é um carimbo de data/hora que indica quando o estado foi atualizado pela última vez.

Os campos **Desempenho de Agendamento** e **Desempenho de Custos** são definidos a partir da data de monitorização. Quando os desvios da agenda e de custo do nó raiz na vista **Controlo do esforço** são positivos, é possível definir estes campos como **Adiantado**. Quando os desvios da agenda e de custo do nó raiz são negativos, é possível defini-los como **Atrasado**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]