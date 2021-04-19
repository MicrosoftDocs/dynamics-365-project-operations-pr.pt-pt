---
title: Monitorização de custo do projeto
description: Este tópico fornece informações sobre como o Project Operations acompanha o progresso contra o custo da mão de obra e gastos num projeto.
author: rumant
manager: AnnBe
ms.date: 03/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 28cb692c61ae4137a28973dc1bd70ffd989dd535
ms.sourcegitcommit: a1f9f92546ab5d8d8e5a4710ce4c96414ea55d14
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 03/24/2021
ms.locfileid: "5711076"
---
# <a name="labor-cost-tracking-on-projects"></a>Monitorização de custos de mão de obra em projetos

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

Dynamics 365 Project Operations rastreia as estimativas de mão de obra e gastos na granularidade mais baixa exigida no plano do projeto. A estimativa financeira do custo da mão de obra baseia-se no esforço planeado e nos recursos genéricos ou nomeados que são atribuídos a cada tarefa de nó de folhas no plano do projeto. Quando o projeto começa e as pessoas começam a reportar tempo em várias tarefas do projeto, o gasto real em mão de obra é resumido, o que inicia um cálculo das projeções.

## <a name="labor-cost-tracking-view"></a>Vista de monitorização de custo de mão de obra

Na página **Projetos**, no separador **Monitorização**, pode selecionar **Monitorização** > **Custo** para abrir a vista de **Monitorização de custo** e ver o progresso do gasto de mão de obra em cada tarefa no plano do projeto. Esta perspetiva também compara o custo real da mão de obra gasto numa tarefa com o custo de mão de obra planeada da tarefa. O Project Operations utiliza as seguintes fórmulas para calcular as métricas do custo da mão de obra:

- **Custo previsto**: Custo estimado de todas as atribuições de recursos em cada tarefa do nó folha
- **Custo real**: Soma de todos os custos reais pelo tempo registado na tarefa
- **Percentagem de consumo de custos**: Custo real ÷ Estimativa de custos na conclusão
- **Custo restante**: Estimativa de custo na conclusão – Custo real
- **Custo na conclusão**: Custo restante – Custo real
- **Variação de custo**: Custo planificado – Estimativa de custo na conclusão

Cada tarefa apresenta uma projeção do desvio de custo na tarefa. Se a estimativa de custos na conclusão for superior ao custo previsto, prevê-se que a tarefa ultrapasse o orçamento. Se a estimativa de custos na conclusão for inferior ao custo previsto, prevê-se que a tarefa termine abaixo do orçamento.

>[!NOTE]
> O Project Operations só mostra os custos de mão de obra na página do **Projeto** no separador **Monitorização**. Embora os materiais e despesas possam ser estimados e rastreados para consumo, estes custos não estão incluídos nos custos indicados no separador **Monitorização**. Este separador destina-se a funcionar apenas para tornar a projetar os custos da mão de obra através da nova projeção do esforço.
Todos os montantes de custos apresentados são convertidos para a moeda de custo do projeto a partir da moeda de preço do projeto utilizada para determinar a taxa de custo. A moeda de custo do projeto é a moeda da unidade de contratação do projeto. Os valores de custo estimados para o tempo que são mostrados no separador **Estimativas** na página do **Projeto** podem não somar o custo planeado no separador **Monitorização**. A razão desta discrepância deve-se às diferenças de como o custo estimado é resumido na grelha de **Estimativas** e como o custo planeado é calculado na rede de **Monitorização**. 
>
> - O separador **Estimativa** calcula o custo estimado utilizando a mesma moeda da taxa de custo na tabela de preços. Em seguida, o custo estimado na moeda da lista de preços é convertido para o custo estimado na moeda de custo do projeto. O custo estimado na moeda do projeto é apresentado arredondado para 2 casas decimais. Em nenhum momento durante esta conversão é aplicada a precisão cambial. 
> - No separador **Monitorização**, o cálculo de custos previsto segue uma ordem de cálculo ligeiramente diferente que envolve a aplicação da precisão da moeda em duas fases: 
   ><ol>
   ><li>O valor estimado do custo na moeda da lista de preços é convertido para a moeda base (conversão 1).</li>
   ><li>O valor estimado do custo na moeda base é convertido para a moeda do projeto (conversão 2). </li>
   ></ol>
   >A precisão da moeda é aplicada em ambas as etapas para obter um custo planeado (no separador **Monitorização**) que se desvia ligeiramente do custo estimado (na vista **tempo - vista faseada** no separador **Estimativas**). 
   
## <a name="reprojecting-costs-on-leaf-node-tasks"></a>Reprojetar os custos nas tarefas do nó folha

Os custos de mão de obra numa tarefa de nó de folha não podem ser reprojetados diretamente no separador **Monitorização** na página do **Projeto**. No entanto, pode utilizar a vista **Esforço de monitorização** para reprojetar o esforço restante numa tarefa. Isto provoca um recálculo do custo remanescente da tarefa. Segue-se uma descrição de como isto funciona.

1. Um gestor de projeto pode reprojetar esforço em tarefas atualizando o valor padrão no campo **Esforço Restante** com uma nova estimativa do esforço restante na tarefa. A reprojeção provoca um recalcular da estimativa de esforço da tarefa na conclusão (EAC), percentagem de progresso e variação de esforço projetada numa tarefa. A EAC, estimativa de concusão (ETC) e a percentagem de progresso das tarefas de resumo também são recalculadas e produzem uma nova projeção de variância do esforço.
2. Com base no novo valor para o esforço restante na tarefa, o sistema calcula o custo remanescente na vista de **Monitorização de custos**. Para calcular o custo remanescente com base no esforço remanescente, o sistema calcula primeiro o custo médio de uma hora de esforço na tarefa como custo planeado ou esforço planeado. O custo previsto é a soma do custo de todas as atribuições de recursos na tarefa. O custo médio por hora é utilizado para calcular o custo remanescente para o esforço remanescente recentemente projetado na tarefa.
3. O custo em percentagem completa e de consumo de custos na tarefa do nó folha é recalculado.
4. O custo em valor completo das tarefas de resumo até ao nó raiz é recalculado.

## <a name="reprojecting-costs-on-summary-tasks"></a>Reprojetar os custos nas tarefas de resumo

Pode reprojetar os custos de mão de obra em tarefas de resumo ou tarefas de contentores. No entanto, não pode reprojetar custos de mão de obra diretamente numa tarefa de resumo de projeto no separador **Monitorização** na página **Projeto**. Semelhantes às tarefas do nó de folhas, o resumo reprojetar e as tarefas do contentor podem ser feitas utilizando a vista **Monitorização de esforço**. Nesta vista, pode reprojetar o esforço restante numa tarefa de resumo que provoque um recálculo do custo remanescente na tarefa de resumo. Segue-se uma descrição de como isto funciona.

1. Um gestor de projeto pode reprojetar esforço em tarefas de resumo atualizando o valor padrão do esforço restante com uma nova estimativa do esforço restante na tarefa. Esta atualização provoca um recalcular da estimativa de resumo da tarefa na conclusão (EAC), percentagem de progresso e variação de esforço projetada numa tarefa. A EAC, a ETC e a percentagem de progresso das tarefas de resumo também são recalculadas e produzem uma nova projeção de variância do esforço.
2. Com base no novo valor para o esforço restante na tarefa de resumo, o sistema calcula o custo remanescente na vista de **Monitorização de custos**. Para calcular o custo remanescente com base no esforço remanescente, o sistema calcula primeiro o custo médio de uma hora de esforço na tarefa de resumo como custo planeado ou esforço planeado. O custo médio por hora é utilizado para calcular o custo do novo esforço remanescente projetado na tarefa de resumo.
3. O custo em percentagem completa e de consumo de custos na tarefa de resumo é recalculado.
4. O novo custo na conclusão é distribuído para as tarefas de elemento subordinado na mesma proporção que o custo planificado tinha na tarefa.
5. O novo custo com valor completo em cada uma das tarefas individuais até às tarefas do nó de folha é calculado. Com base neste valor, as tarefas de elemento subordinado afetadas até aos nós das folhas terão o seu custo remanescente e a percentagem de consumo de custos recalculadas com base no custo pelo valor total. Este valor resulta numa nova projeção para o desvio de custo da tarefa. 


O campo **Desempenho de custo** pode ser definido a partir dos dados de monitorização. Quando a variação de custos para o nó raiz na vista **Monitorização de custo** é negativa, pode definir este campo como **Abaixo do orçamento**. Quando a variação de custo para o nó de raiz é positiva, pode definir o valor como **Acima do orçamento**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
