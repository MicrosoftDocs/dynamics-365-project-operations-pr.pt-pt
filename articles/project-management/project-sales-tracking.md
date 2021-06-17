---
title: Monitorização das vendas do projeto
description: Este tópico fornece informações sobre como o Project Operations acompanha o progresso contra as receitas da mão de obra num projeto.
author: rumant
ms.date: 03/24/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3f9873dc3e709453a56cb53273b35cc1cd312127
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996985"
---
# <a name="project-sales-tracking"></a>Monitorização das vendas do projeto

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

Dynamics 365 Project Operations monitoriza as estimativas de mão de obra e receitas na granularidade mais baixa exigida num plano do projeto. A estimativa da receita da mão de obra baseia-se no esforço planeado e nos recursos genéricos ou nomeados que são atribuídos a cada tarefa de nó de folhas no plano do projeto. Quando o projeto começa e as pessoas começam a reportar tempo em várias tarefas do projeto, a receita real em mão de obra é resumido, o que inicia um cálculo das projeções.

## <a name="labor-revenue-tracking-view"></a>Vista de monitorização de receita de mão de obra

Na página **Projetos**, no separador **Monitorização**, pode selecionar **Monitorização** > **Custo** para abrir a vista de **Monitorização**. Ou, pode selecionar **Usar** > **Taxa de faturação** para abrir a vista **Monitorização de receita**, que mostra o progresso da receita da mão de obra em cada tarefa no plano do projeto. Esta perspetiva também compara a receita real da mão de obra gasta numa tarefa com a receita de mão de obra planeada da tarefa. O Project Operations utiliza as seguintes fórmulas para calcular as métricas da receita da mão de obra:

- **Receita prevista**: Valores de vendas estimados de todas as atribuições de recursos em cada tarefa do nó folha
- **Receita real**: Soma de todos os valores reais de vendas não faturadas pelo tempo registado na tarefa
- **Receitas faturáveis%** : Receita real ÷ Estimativa de receita na conclusão
- **Receitas restantes** : Estimativa de receita na conclusão – Receita real
- **Receitas estimadas na conclusão**: Receita restante + Receita real
- **Variação de receita**: Receita planificada – Receita estimada na conclusão


> [!NOTE]
> O Project Operations só mostra as receitas de mão de obra na página do **Projeto** no separador **Monitorização**. Embora os materiais e despesas possam ser estimados e rastreados para consumo, estas receitas não estão incluídas nas receitas indicadas no separador **Monitorização**. Este separador destina-se a funcionar apenas para tornar a projetar as receitas da mão de obra através da nova projeção do esforço.  
> Todos os montantes das receitas apresentados são convertidos para a moeda de custo do projeto. A moeda de custo do projeto é a moeda da unidade de contratação do projeto. Para os projetos de preço fixo, os números de receitas na vista **monitorização de receitas da mão de obra** não são relevantes porque as vendas não faturadas não são registadas na aprovação do tempo.
> Os valores estimados de vendas para o tempo que são mostrados no separador **Estimativa** do projeto podem não somar o valor de receitas previsto no separador **Monitorização**. A origem desta discrepância deve-se a duas razões possíveis:
><ol>
   ><li> O separador <b>Estimativas</b> mostra receitas estimadas na moeda de venda, enquanto o separador <b>Monitorização</b> mostra as receitas planeadas convertidas para a moeda de custo. </li>
   ><li> Quando as vendas estimadas são convertidas para a moeda contratual, conforme indicado no separador <b>Estimativas</b>, para a moeda do projeto, a conversão envolve etapas que podem resultar em alguma perda de precisão: </li>
><ol>
><li> O valor estimado das vendas na moeda do contrato é primeiro convertido para a moeda base (conversão 1).</li>
><li> O valor estimado das vendas na moeda base é convertido para a moeda do projeto (conversão 2). </li>
></ol>
></ol>
> A precisão cambial é aplicada em ambas as etapas, o que resulta num desvio das receitas previstas na moeda do projeto das vendas previstas na moeda contratual.
   

## <a name="reprojecting-revenues-on-leaf-node-tasks"></a>Reprojetar as receitas nas tarefas do nó folha

As receitas de mão de obra numa tarefa de nó de folha não podem ser reprojetadas diretamente no separador **Monitorização** na página do **Projeto**. No entanto, pode utilizar a vista **Esforço de monitorização** para reprojetar o esforço restante numa tarefa. Isto provoca um recálculo da receita remanescente da tarefa. Segue-se uma descrição de como isto funciona.

1. Um gestor de projeto pode reprojetar esforço em tarefas atualizando o valor padrão no campo **Esforço Restante** com uma nova estimativa do esforço restante na tarefa. A reprojeção provoca um recalcular da estimativa de esforço da tarefa na conclusão (EAC), percentagem de progresso e variação de esforço projetada numa tarefa. A EAC, estimativa de concusão (ETC) e a percentagem de progresso das tarefas de resumo também são recalculadas e produzem uma nova projeção de variância do esforço.
2. Com base no novo valor para o esforço restante na tarefa, o sistema calcula a receita remanescente na vista de **Monitorização de receitas**. Para calcular a receita remanescente com base no esforço remanescente, o sistema calcula primeiro a receita média de uma hora de esforço na tarefa de resumo como receita planeada ou esforço planeado. A receita prevista é a soma da receita de todas as atribuições de recursos na tarefa. A receita média por hora é utilizada para calcular a receita remanescente para o esforço remanescente recentemente projetado na tarefa.
3. A receita estimada na conclusão e de consumo de receita na tarefa do nó folha é recalculada.
4. A receita em valor completo das tarefas de resumo até ao nó raiz é recalculada.

## <a name="reprojecting-revenues-on-summary-tasks"></a>Reprojetar as receitas nas tarefas de resumo

Pode reprojetar as receitas de mão de obra em tarefas de resumo ou tarefas de contentores. No entanto, não pode reprojetar receitas de mão de obra diretamente numa tarefa de resumo de projeto no separador **Monitorização** na página **Projeto**. Semelhantes às tarefas do nó de folhas, o resumo reprojetar e as tarefas do contentor podem ser feitas utilizando a vista **Monitorização de esforço**. Nesta vista, pode reprojetar o esforço restante numa tarefa de resumo que provoque um recálculo da receita remanescente na tarefa de resumo. Segue-se uma descrição de como isto funciona.

1. Um gestor de projeto pode reprojetar esforço em tarefas atualizando o valor padrão no campo **Esforço Restante** com uma nova estimativa do **esforço restante** na tarefa. A reprojeção provoca um recalcular da estimativa da tarefa na conclusão (EAC), percentagem de progresso e variação de esforço projetada numa tarefa. A EAC, a ETC e a percentagem de progresso das tarefas de resumo também são recalculadas e produzem uma nova projeção de variância do esforço.
2. Com base no novo valor no campo **esforço restante** na tarefa, o sistema calcula a receita remanescente na vista de **Monitorização de receitas**. Para calcular a receita remanescente com base no esforço remanescente, o sistema calcula primeiro a receita média de uma hora de esforço na tarefa de resumo como receita planeada ou esforço planeado. A receita prevista é a soma da receita de todas as atribuições de recursos na tarefa. Esta receita média por hora é então utilizada para calcular a receita do esforço remanescente recentemente projetado na tarefa.
3. A receita estimada na conclusão e de percentagens de consumo de receita na tarefa de resumo é recalculada.
4. O novo valor da receita estimada na conclusão é distribuído para as tarefas de elemento subordinado na mesma proporção que a receita planificada tinha na tarefa.
5. A nova receita estimada na conclusão em cada uma das tarefas individuais até às tarefas do nó de folha é calculada. Com base neste valor, as tarefas de elemento subordinado afetadas até aos nós das folhas terão a sua receita remanescente e a percentagem de consumo de receitas recalculadas com base na receita pelo valor total. Isto resulta numa nova projeção para o desvio da receita da tarefa. 
6. A receita em valor completo das tarefas de resumo até ao nó raiz é recalculada.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

