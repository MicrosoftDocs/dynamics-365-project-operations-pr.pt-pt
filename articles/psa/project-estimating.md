---
title: Custos e receita do projeto
description: Este tópico fornece informações sobre a estimativa de custos e receitas do projeto.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 279c1119d334a7f60906e33b3fc7ca22ff9a360d
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148342"
---
# <a name="project-costs-and-revenue"></a>Custos e receita do projeto

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

As estimativas do projeto fornecem a vista financeira do trabalho estimado e agendado na agenda do projeto. O separador **Estimativas** na página **Projetos** mostra o impacto sobre o custo e a receita do trabalho que está a planear. Também fornece informações sobre muitas dimensões predefinidas. 

> ![Separador Estimativas](media/project-5.png)

## <a name="cost-and-sales-values-of-the-project"></a>Valores das vendas e do custo do projeto

As listas de preços definem o custo e as taxas de faturação para as funções num projeto. Pode determinar o impacto sobre o custo e a receita do trabalho, com base nas funções associadas ao nome da posição e no recurso nomeado atribuído a uma tarefa. Se existirem tarefas que não tenham quaisquer atribuições (genéricas ou nomeadas), não poderá obter estimativas de custo ou vendas. Os valores de custo e de vendas consideram a data definida nas listas de preços.

### <a name="default-cost-price"></a>Preço de custo predefinido  

Cada projeto pertence a uma organização. Esta organização é mostrada no campo **Unidade de Contratação** no projeto. A lista de preços associada à unidade de contratação é utilizada para determinar o preço de custo unitário. Para determinar os preços de custo corretos nas funções para a data definida nas linhas de estimativa, procure a combinação de função, unidade e unidade organizacional na lista de preços de custo. 

Para que os preços de custo possam ser calculados, todas as tarefas têm de ser atribuídas a um recurso. Todas as tarefas não atribuídas terão um preço de custo de 0,00.

Se a combinação de função, unidade e unidade organizacional não devolver um preço de custo a partir da lista de preços da unidade de contratação, o sistema ignora a unidade. Em vez disso, procura a combinação de apenas função e unidade organizacional. Se for encontrado um preço de custo, os fatores de conversão serão utilizados para convertê-lo na unidade selecionada na linha de estimativa.

Se a combinação de função e unidade organizacional não devolver um preço de custo, o sistema ignora a unidade organizacional. Em vez disso, procura a combinação de função e unidade para definir o preço predefinido (após qualquer conversão ser aplicada).

Se o sistema não encontrar o preço para a função, o preço de custo na linha de estimativa é definido como um valor predefinido de **0,00**. Todos os montantes de custo nas linhas de estimativa de custos do projeto são registados na moeda da unidade de contratação.

> [!NOTE]
> Por predefinição, o Microsoft Dynamics 365 armazena montantes de custo na moeda base. No entanto, os montantes de custo mostrados no separador **Estimativas** encontram-se na moeda da unidade de contratação.  

### <a name="default-sales-price"></a>Preço de venda predefinido 

A lista de preços de venda é determinada pela entidade de vendas à qual o projeto está anexado ou pelo cliente do projeto. Quando uma entidade de vendas, tal como uma oportunidade, proposta ou contrato, está associada ao projeto, o preço de venda da entidade de vendas é determinado pela lista de preços associada à proposta ou ao contrato. Se a proposta ou o contrato tiver uma lista de preços personalizada, essa lista de preços será utilizada como a lista de preços de venda predefinida para as estimativas do projeto. Se não houver uma associação com entidades de vendas, a lista de preços de venda predefinida dos parâmetros será utilizada como a lista de preços de venda predefinida do projeto correspondida pela moeda do cliente que está definida no projeto.

Cada linha de estimativa tem uma unidade de atribuição de recursos associada. A unidade de atribuição de recursos indica a unidade organizacional da qual os recursos são reservados para concluir a tarefa. Para determinar o preço de venda para as funções associadas, procure a combinação de função, unidade e unidade de atribuição de recursos na lista de preços de venda. Se não existirem atribuições na tarefa, o preço de venda da tarefa é 0,00.

Se a combinação de função, unidade e unidade de atribuição de recursos não devolver um preço de venda a partir da lista de preços de venda, o sistema ignora a unidade. Em vez disso, procura a combinação de apenas função e unidade de atribuição de recursos. Se for encontrado um preço de venda, os fatores de conversão serão utilizados para convertê-lo na unidade selecionada na linha de estimativa de vendas. 

Se a combinação de função e unidade de atribuição de recursos não devolver um preço de venda a partir da lista de preços de venda, o sistema ignora a unidade de atribuição de recursos. Em vez disso, procura a combinação de função e unidade para definir o preço predefinido (após qualquer conversão ser aplicada).

Se o sistema não encontrar um preço para a função, o preço de venda na linha de estimativa é definido como um valor predefinido de **0,00**.

O separador **Estimativas** tem uma vista de grelha que mostra as linhas de estimativa. A grelha inclui colunas para a unidade, o preço de custo total e o preço de venda total, conforme mostrado na ilustração seguinte. 

> ![Vista de grelha no separador Estimativas](media/project-6.png)

## <a name="time-phased-view-of-project-estimates"></a>Vista faseada no tempo das estimativas do projeto

A vista faseada no tempo das estimativas do projeto mostra os dados de estimativa a partir da vista de grelha na linha cronológica, numa escala temporal selecionada. Por predefinição, os dados de estimativa são articulados na dimensão **Função**.

> ![Vista faseada no tempo para estimativas do projeto](media/project-7.png)

## <a name="allocating-estimated-effort-based-on-the-task-mode"></a>Alocar o esforço estimado com base no modo de tarefa

Na vista faseada no tempo, distribui o esforço total estimado para a tarefa através da alocação de horas de esforço por um período de tempo unitário na escala temporal selecionada. O modo de tarefa determina a forma como o esforço é alocado ao longo da duração da tarefa. Os dois tipos de alocação são **Uniforme** e **Baseada nas horas de trabalho**.

### <a name="work-hours-based-allocation"></a>Alocação baseada nas horas de trabalho
 
No modo de tarefa de agendamento automático, as horas predefinidas diárias para os recursos de tarefas são definidas com a taxa horária de trabalho completa. Este comportamento aplica-se quando o esforço é alocado, dividindo-o pela duração da tarefa na vista faseada no tempo. Por exemplo, se estimar que uma tarefa será concluída por um recurso na escala temporal **Dia**, o esforço alocado por dia não excederá as horas de trabalho por dia definidas no calendário do projeto. Consequentemente, a alocação do esforço assegura sempre que os recursos têm uma estimativa de utilização durante todo o dia.

### <a name="even-allocation"></a>Alocação uniforme

No modo de tarefa agendada manualmente, as horas de trabalho do calendário do projeto não são utilizadas. Em vez disso, a agenda da tarefa baseia-se na intervenção do utilizador. Para estas tarefas, a alocação do esforço por período de tempo unitário na escala temporal selecionada não tem qualquer fator de limitação. O esforço total na tarefa é dividido e alocado equitativamente para cada período de tempo unitário na escala temporal selecionada. Desta forma, o modo de tarefa definido na tarefa determina a distribuição do esforço ou a alocação do esforço por período de tempo unitário nas estimativas faseadas no tempo.

## <a name="grouping-and-time-phasing-options"></a>Opções de agrupamento e faseamento no tempo

A vista faseada no tempo mostra a distribuição do esforço, do custo e das estimativas de venda baseadas no dia, semana, mês ou ano. Por predefinição, os dados de estimativa são articulados na dimensão **Função**. No entanto, pode utilizar a opção **Agrupar Por** para articular duas outras dimensões: **Categoria** e **Recurso**.

Na vista de grelha e na vista faseada no tempo, pode selecionar os campos que são mostrados. Os totais para cada bloco de tempo são mostrados na parte inferior do projeto. Mostram o total estimado do esforço, custo e vendas para o dia, semana, mês ou ano. O preço de custo e o preço de venda predefinidos são efetivos para a data. Por outras palavras, são alterados para cada recurso, com base na vista faseada no tempo que selecionar.

## <a name="expense-estimates"></a>Estimativas de despesas

O botão **Adicionar uma Estimativa de Despesa Nova** na vista de grelha permite-lhe registar quaisquer despesas incorridas no projeto, mas que não estão diretamente relacionadas com a mão de obra. Pode registar as estimativas de despesas para uma tarefa específica ou para todo o projeto. Selecione as categorias de despesa e a data provisória em que espera incorrer na despesa. Se a lista de preços de custo e a lista de preços de venda associadas tiverem preços predefinidos (ou percentagens de margem de lucro definidas para as categorias de despesa), estes serão introduzidos automaticamente na linha de estimativa quando a associação ocorrer.
