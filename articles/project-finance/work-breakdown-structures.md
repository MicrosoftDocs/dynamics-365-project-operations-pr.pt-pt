---
title: Descrição geral das estruturas hierárquicas do trabalho
description: Uma estrutura hierárquica do trabalho (WBS) é uma descrição do trabalho que será concluído para um projeto. É uma hierarquia das tarefas que representa a compreensão da equipa do projeto sobre a composição do trabalho, bem como a dimensão, o custo e a duração de cada componente ou tarefa.
author: KimANelson
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWorkBreakdownStructure
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23861
ms.assetid: 241a0464-0056-4a69-b468-0afbe2d5f3ae
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 954965ee947cbce9d1ae686d281a5fed25a78245
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754547"
---
# <a name="work-breakdown-structures-overview"></a>Descrição geral das estruturas hierárquicas do trabalho

[!include [banner](../includes/banner.md)]

Uma estrutura hierárquica do trabalho (WBS) é uma descrição do trabalho que será concluído para um projeto. É uma hierarquia das tarefas que representa a compreensão da equipa do projeto sobre a composição do trabalho, bem como a dimensão, o custo e a duração de cada componente ou tarefa. Uma WBS tem três grandes finalidades:

-   Descrever a estrutura ou a composição do trabalho em tarefas.
-   Agendar o trabalho do projeto.
-   Estimar o custo de cada tarefa.

O grau de detalhe numa WBS depende do nível de precisão exigido nas estimativas e do nível de monitorização que é necessário em relação a essas estimativas. Normalmente, os projetos com muito baixa tolerância de derrapagem na agenda ou no custo necessitam de uma WBS mais detalhada, e de uma monitorização diligente do progresso do trabalho e do custo em relação à WBS. Este tipo de projeto é comum nos setores da construção e da engenharia. 

Em contraste, os projetos em setores como os meios de comunicação e publicidade, software e infraestrutura de TI tendem a ser únicos, e a produtividade está relacionada com a experiência e a competência do indivíduo que está a executar a tarefa. Por isso, estes setores utilizam uma WBS para obterem uma aproximação do tamanho de um projeto, não para monitorizar o progresso desse projeto em detalhe. 

A criação de uma WBS é um processo intensivo que normalmente é feito durante um longo período, e que requer a colaboração e a informação de uma grande variedade de pessoas. Este tópico descreve como pode utilizar as melhorias da WBS para satisfazer os seus requisitos para estimativas e monitorização.

## <a name="prerequisites-for-creating-a-wbs"></a>Pré-requisitos para criar uma WBS
Para criar uma WBS, tem de ser capaz de criar uma agenda de trabalho e estimar o custo do trabalho.

### <a name="prerequisites-for-creating-a-work-schedule"></a>Pré-requisitos para criar uma agenda de trabalho

Para utilizar todas as capacidades de agendamento das funcionalidades da WBS, execute a seguinte configuração:

1.  Configure um calendário predefinido e um calendário de projeto:
    1.  Clique em **Gestão de projetos e contabilística** &gt; **Configurar** &gt; **Parâmetros da gestão de projetos e contabilística** &gt; **Agendamento**. No campo **Calendário de trabalho predefinido**, especifique um calendário predefinido. Este será o calendário de trabalho predefinido para qualquer novo projeto que seja criado.
    2.  Pode alterar o calendário predefinido para um projeto específico. Clique na página de detalhes do projeto e, em seguida, no Separador Rápido **Equipa do projeto e agendamento**, atualize o campo **Calendário de agendamento** ao selecionar outro calendário.

2.  Configure dias de trabalho padrão e o horário de trabalho. O calendário que definir como calendário de trabalho para o seu projeto será utilizado na WBS para determinar as seguintes informações:

-   Dias úteis e feriados
-   O número de horas de trabalho num dia

Para configurar os dias úteis e o horário de trabalho para um calendário, ou para criar um novo calendário, clique em **Administração da organização** &gt; **Comum** &gt; **Calendários**.

### <a name="prerequisites-for-estimating-the-cost-of-work"></a>Pré-requisitos para estimar o custo do trabalho

Para utilizar as capacidades de estimativa de custo total da WBS, deve configurar os custos e os preços de venda para os trabalhadores, categorias de mão de obra, despesas e tarifas, e itens.

-   Para configurar o custo e o preço venda das categorias de mão de obra, despesa e tarifas, clique em **Gestão de projetos e contabilística** &gt; **Configurar** &gt; **Preços**.
-   Para configurar o custo e o preço de venda dos itens, utilize a página **Acordos comerciais** para cada item na página da lista **Produtos lançados** na Gestão da informação do produto.

## <a name="creating-a-wbs"></a>Criar um WBS
A criação de uma WBS implica três atividades:

1.  **Decomposição do trabalho** – Crie uma hierarquia do trabalho em partes ou tarefas geríveis.
2.  **Agenda de trabalho** – Faça uma estimativa do tempo necessário para concluir uma tarefa, definir as interdependências das tarefas e selecionar as datas de início e de fim das tarefas.
3.  **Estimativa de custos** – Estime os custos de cada tarefa.

As secções seguintes abordam a forma como as capacidades da WBS podem ajudar em cada uma destas atividades.

### <a name="work-decomposition"></a>Decomposição do trabalho

Normalmente, a criação de uma hierarquia ou decomposição do trabalho é o primeiro passo no processo de criação de uma WBS. A funcionalidade WBS suporta as seguintes construções básicas para a decomposição ou hierarquia do trabalho. 

**Tarefa raiz do projeto** A tarefa raiz do projeto é a tarefa de resumo de alto nível de um projeto. Todas as outras tarefas do projeto são criadas sob essa. O nome da tarefa raiz é sempre definido como o nome do projeto. O esforço, as datas e a duração do nó raiz resumem os valores das tarefas sob a tarefa raiz. Não pode modificar as propriedades do nó raiz nem eliminá-lo.

**Tarefas de resumo ou contentor** Uma tarefa de resumo é uma tarefa com subtarefas ou tarefas constituintes sob ela. Uma tarefa de resumo não tem qualquer esforço de trabalho ou custo próprio. Em vez disso, o custo e o esforço do trabalho de uma tarefa de resumo são a soma do custo e do esforço do trabalho das suas tarefas constituintes. A primeira data de início das tarefas constituintes é utilizada como data de início da tarefa de resumo e a última data de fim das tarefas constituintes é utilizada como data de fim. Pode modificar o nome de uma tarefa de resumo, mas não pode modificar as propriedades de agendamento do esforço, datas e duração. Se eliminar uma tarefa de resumo, também eliminará todas as suas tarefas constituintes. 

**Tarefas do nó de folha** Uma tarefa de nó de folha representa o pacote de trabalho mais granular do projeto. Um nó de folha tem um esforço estimado, um número de recursos planeado, uma data de início e de fim planeadas, e uma duração. 

Pode concluir as seguintes operações hierárquicas para permitir a criação de uma decomposição ou hierarquia de trabalho para um projeto. 

**Nova tarefa** Qualquer nova tarefa que criar é adicionada automaticamente sob o nó raiz e é atribuído automaticamente um número de WBS à tarefa. O número de WBS representa o nível da tarefa na hierarquia. Para as tarefas no primeiro nível sob a tarefa raiz do projeto, é utilizado um esquema de numeração de 1, 2, 3 e assim por diante. Para tarefas sob primeiro nível, é utilizado um esquema de numeração 1.1, 1.2, 1.3 e assim por diante. Para cada nível que é adicionado sob um nível anterior, é adicionada uma nova série de pontos de números. 

Atualmente, não é possível personalizar a numeração da WBS. 

**Avançar tarefa** Quando avança uma tarefa, torna-se uma subordinada da tarefa que a antecede. O número da WBS da nova tarefa subordinada é recalculada automaticamente com base no número da WBS da nova principal. A tarefa principal é agora uma tarefa de resumo ou contentor, e torna-se uma acumulação das suas tarefas constituintes. 

> [!NOTE] 
> Quando avança tarefas sob uma tarefa que era um nó de folha antes da operação de avanço, a tarefa de resumo criada recentemente perde as suas próprias datas, esforço e número de recursos. Utiliza agora um resumo dos valores das suas novas tarefas constituintes. 

**Diminuir avanço da tarefa** Quando diminui o avanço de uma tarefa, já não é uma tarefa constituinte da sua principal. O número da WBS desta tarefa é recalculado automaticamente para refletir o novo nível da tarefa na hierarquia. O esforço, o custo e as datas da tarefa principal da tarefa anterior são recalculados para excluir essa tarefa. 

**Mover para cima e Mover para baixo** Quando clica em **Mover para cima** e **Mover para baixo**, pode alterar a posição de uma tarefa na sua hierarquia principal. A posição de uma tarefa não afeta o esforço, o custo, as datas ou a duração da tarefa. No entanto, o número da WBS da tarefa é recalculado automaticamente para refletir a nova posição da tarefa.

### <a name="schedule-estimation"></a>Estimativa da agenda

Normalmente, a estimativa da agenda é o segundo passo na criação de uma WBS. Como melhor prática, deve concluir a estimativa da agenda depois de criar as tarefas. A página **estrutura hierárquica do trabalho** no Finance tem duas secções. O painel superior destina-se à estimativa da agenda e o painel inferior inclui um separador **Estimativa de custos e receitas** que pode utilizar na estimativa de custos. 
**Dependências de tarefas** Numa WBS, pode criar uma relação antecessora entre tarefas. Quando atribui tarefas antecessoras a uma tarefa, essa tarefa só pode ser iniciada depois de todas as suas tarefas antecessoras terem sido concluídas. A data de início planeada da tarefa é definida automaticamente para a data mais recente de todas as suas antecessoras. 

**Agendamento de tarefas** Os seguintes fatores determinam o agendamento das tarefas do nó de folha:

-   Antecessores
-   Esforço
-   O número de recursos
-   Dadas de início e de fim

A data de início de uma tarefa de nó de folha que não tenha antecessores é definida automaticamente para a data de início de agendamento do projeto. A duração de uma tarefa de nós de folha é sempre calculada como o número de dias de trabalho entre as datas de início e de fim. 

*<strong><em>Regras de agendamento</em></strong>* Quando a assistência de agendamento automático está ativada, são aplicáveis as seguintes regras ao agendamento de tarefas para as tarefas de nó de folha:

-   As datas de início e de fim de uma tarefa têm de ser dias de trabalho de acordo com o calendário de agendamento do projeto.
-   A data de início de uma tarefa com antecessores é definida automaticamente para a data de fim mais recente dos respetivos antecessores.
-   O esforço para uma tarefa é calculado automaticamente da seguinte forma:

Número de pessoas × Duração × Número de horas num dia de trabalho padrão no calendário do projeto. 

Em alguns casos, poderá querer afastar-se destas regras. Pode desativar o agendamento automático para evitar que o Finance defina ou corrija automaticamente quaisquer propriedades das tarefas do nó de folha. Quando introduz informações para uma tarefa que causa uma violação de quaisquer regras de agendamento, é mostrado um ícone de erro de agendamento para a tarefa. Se não quiser que sejam apresentados erros de agendamento, clique em **São mostrados erros de agendamento** para desativar a funcionalidade. 

> [!NOTE] 
> Os valores para uma tarefa de resumo ou contentor continuam a ser calculados como a soma dos valores das tarefas constituintes, independentemente de a assistência do agendamento automático estar ativada ou desativada. 

**Corrigir erros de agendamento** Quando a assistência do agendamento automático está ativada, não é provável que ocorram erros de agendamento. No entanto, se desativar a assistência de agendamento automático e, depois, voltar a ativá-la mais tarde, poderão aparecer os ícones de erro de agendamento na WBS. 

**Corrigir erros de agendamento por tarefa** Quando faz duplo clique no ícone de erro de agendamento para uma tarefa específica, uma caixa de diálogo apresenta todos os erros de agendamento dessa tarefa. Pode decidir quais os erros de agendamento corrigir para a tarefa. 

**Corrigir todos os erros de agendamento** Se pretende que o Finance corrija todos os erros de agendamento na WBS, no Painel de Ação, clique em **Corrigir todas as discrepâncias de agendamento**. 

> [!NOTE] 
> Esta funcionalidade pode causar modificações significativas na WBS. Os erros são corrigidos pela seguinte ordem:

1.  O esforço estimado em todas as tarefas é modificado para ser igual à capacidade definida no calendário do projeto.
2.  A data de início de cada tarefa é modificada para a tarefa começar depois de concluídas todas as suas tarefas antecessoras.
3.  A data de início de cada tarefa é modificada para remover lacunas nas datas de início das tarefas antecessoras.

### <a name="cost-estimation"></a>Estimativa de custos

Tal como mencionado anteriormente neste documento, introduza a estimativa de custo para cada tarefa do nó de folha através do separador **Custos e receitas estimados** no painel inferior da página **Estrutura hierárquica do trabalho**. 

> [!NOTE] 
> Não pode modificar a estimativa de custo para uma tarefa de resumo ou de contentor. A estimativa de custo para uma tarefa de resumo é igual à soma da estimativa de custo das suas tarefas de nó de folha. O custo total estimado para cada tarefa é calculado como a soma dos montantes de custo estimado para os seguintes tipos de transação:

-   Mão de Obra
-   Item ou material
-   Despesas

É utilizado um tipo de transação **Tarifa** para estimar as receitas baseadas na tarifa. Este tipo de transação não tem um componente de custo, pelo que não é tido em consideração quando os custos são estimados. 

Um tipo de transação **Na conta** é utilizado para registar o valor das vendas contratadas num tipo de projeto de valor fixo. Este tipo de transação também não é tido consideração quando os custos são estimados. 

Quando faz a estimativa de custos da mão de obra, material e despesas para cada tarefa, tem de atribuir uma categoria de projeto ao custo estimado. 

**Estimativa dos custos de mão de obra** Para cada tarefa de nó de folha, atribua um esforço de trabalho em horas e uma categoria predefinida. Por isso, quando configura uma agenda para uma tarefa, a estimativa de custo da mão de obra para essa tarefa é adicionada automaticamente na categoria predefinida para a mão de obra. Esta estimativa de custos é apresentada no separador **Estimativa de custos e receitas** na grelha **Detalhes da linha** para essa tarefa. Se necessitar de mais estimativas de custos da mão de obra, pode adicioná-las neste separador. Se aumentar ou diminuir as horas na estimativa de custos da mão de obra, a agenda da tarefa é recalculada automaticamente. 

**Estimativa de despesas e custos de materiais** O separador **Estimativa de despesas e custos de materiais** também permite estimar as despesas e os custos de material para uma tarefa, se necessitar de estimativas. 

O custo e o preço de venda para cada linha de estimativa de mão de obra ou despesas baseia-se na configuração definida para cada categoria nas tabelas de preços da em **Gestão de projetos e contabilística** &gt; **Configurar** &gt; **Preços**. Para os itens, o custo e o preço de venda são adicionados por predefinição a partir do item ou dos contratos comerciais na página da lista **Produtos lançados** na Gestão da informação do produto.

## <a name="tracking-progress-on-the-wbs"></a>Monitoriza o progresso na WBS
Alguns setores de atividade monitoriza o progresso de um projeto em relação a uma WBS a um nível muito granular, enquanto outros monitorizam o progresso a um nível mais elevado da WBS. Esta secção descreve como pode utilizar a monitorização da WBS para os seus requisitos do projeto. 

O Finance têm três vistas para a WBS de um projeto: vista de Planeamento, vista de Monitorização do esforço e vista de Monitorização de custos.

### <a name="planning-view"></a>Vista de planeamento

A Vista de planeamento apresenta a estimativa planeada ou da linha de base da informação da agenda e dos custos. Apesar de não existirem funcionalidades para monitorizar a versão e a linha de base para a WBS de um projeto, os valores nesta vista pretendem representar a versão da linha de base. As secções Estimativa da agenda e Estimativa de custos deste tópico descreve esta vista e como é utilizada para criar uma WBS.

### <a name="effort-tracking-view"></a>Visto de controlo do esforço

A vista Monitorização do esforço apresenta a monitorização do progresso para as tarefas na WBS. Compara as horas de esforço reais acumuladas para uma tarefa com as horas de esforço planeadas. As seguintes fórmulas fornecem os valores na vista Monitorização do esforço:

-   Percentagem do progresso = Esforço real até à data ÷ Esforço planeado para a tarefa
-   Esforço restante (também conhecido como Estimativa para conclusão \[ETC\]) = Esforço planeado – Esforço real até à data
-   Estimativa na conclusão (EAC) = Esforço restante + Esforço real até à data
-   Desvio do esforço projetado = Esforço planeado – EAC

A vista Monitorização do esforço apresenta uma projeção do desvio do esforço para a tarefa, baseado no facto de a EAC ser inferior ou superior ao esforço planeado:

-   Se a EAC for superior ao esforço planeado, a tarefa está projetada para demorar mais tempo do que planeado originalmente e está atrasada.
-   Se a EAC for inferior ao esforço planeado, a tarefa está projetada para demorar menos tempo do planeado originalmente e está adiantada.

**Reprojeção do esforço do gestor de projeto** Ocasionalmente, o gestor de projetos ou outra pessoa que está a monitorizar o progresso de um projeto terá de rever as estimativas originais de uma tarefa. A tarefa pode estar a mover-se mais depressa ou mais devagar do que era inicialmente antecipado por várias razões. Por exemplo, o âmbito foi reduzido ou os trabalhadores têm menos experiência do que o inicialmente previsto. As projeções são a perceção das estimativas por parte de um gestor de projeto, baseada no estado atual de um projeto. Regra geral, não deve alterar os números da linha de base, porque uma linha de base do projeto representa um documento bem publicado para a agenda e a estimativa de custo do projeto acordadas por todos os intervenientes no projeto. 

Os gestores de projetos podem modificar o esforço nas tarefas de duas formas:

-   Modificar o esforço restante que é definido automaticamente para atualizar o esforço restante real na tarefa.
-   Modificar a percentagem do progresso que é definida automaticamente para atualizar o progresso real na tarefa.

Estas duas abordagens causam um recálculo da ETC, da EAC e da percentagem de progresso da tarefa e o desvio do esforço projetado na tarefa. A EAC, a ETC e a percentagem de progresso das tarefas de resumo também são recalculadas, e é atualizado o desvio do respetivo esforço projetado. 

**Esforço modificado nas tarefas de resumo** Pode modificar o esforço nas tarefas de resumo ou contentor. Independentemente de modificar estes valores ao utilizar o esforço restante ou a percentagem de progresso nas tarefas de resumo, os cálculos ocorrem automaticamente pela seguinte ordem:

1.  A EAC, a ETC e a percentagem de progresso na tarefa são calculadas.
2.  A nova EAC é distribuída para as tarefas subordinadas na mesma proporção que o montante da EAC original.
3.  É calculada a nova EAC em cada tarefa do nó de folha.
4.  O esforço restante e a percentagem do progresso são recalculados para todas as tarefas subordinadas afetadas, com base no novo valor da EAC. O desvio do esforço das tarefas também é recalculado.
5.  A EAC das tarefas de resumo também é recalculada a partir dos nós de folha.

Clique em **Expandir para o nível** na vista Monitorização do esforço para definir o nível a rastrear e manter a sua WBS. A WBS é expandida automaticamente para esse nível na vista Monitorização do esforço sempre que o abre.

### <a name="cost-tracking-view"></a>Vista Controlo dos custos

A vista Monitorização do custo apresenta a monitorização do consumo de custos para uma tarefa. Nesta vista, o custo real que foi gasto em relação a uma tarefa até à data é comparado com o custo planeado para a tarefa. As seguintes fórmulas fornecem os valores na vista Monitorização do custo:

-   Percentagem do custo consumido = Custo real até à data ÷ Custo planeado até à tarefa
-   Custo para conclusão (CTC) = Custo planeado – Custo real até à data
-   Estimativa na conclusão (EAC) = CTC + Custo real até à data
-   Desvio de custo projetado = Custo planeado – EAC

A vista Monitorização do custo apresenta uma projeção do desvio do custo para a tarefa, baseado no facto de a EAC ser inferior ou superior ao custo planeado:

-   Se a EAC for superior ao custo planeado, a tarefa está projetada para utilizar mais dinheiro do que planeado originalmente e está acima do orçamento.
-   Se a EAC for inferior ao custo planeado, a tarefa está projetada para utilizar menos dinheiro do que planeado originalmente e está abaixo do orçamento.

**Reprojeção de custos do gestor de projeto** Os gestores de projetos têm de utilizar o CTC para rever a estimativa de custos original numa tarefa. O gestor de projetos pode modificar o valor CTC ao custo necessário para concluir a tarefa. Se modificar o valor CTC, o CTC, a EAC e percentagem de custos consumidos, bem como o desvio de custos projetado numa tarefa, são recalculados. A EAC, a ETC e a percentagem de custos consumidos nas tarefas de resumo também são recalculadas, e é atualizado o desvio do respetivo custo projetado. 

> [!NOTE] 
> Quando revê o esforço para uma tarefa da WBS na vista Monitorização do esforço, o CTC, a EAC, a percentagem de custos consumidos e o desvio de custos projetado são todos recalculados na vista Monitorização dos custos. No entanto, as revisões de custos não afetam os valores da vista Monitorização do esforço, porque o custo por tipo de transação (mão de obra, material ou despesa) ou categoria de projeto não é revisto. 

**Revisão da projeção dos custos em tarefas de resumo** Pode rever os custos nas tarefas de resumo, e os cálculos ocorrem automaticamente pela seguinte ordem:

1.  A EAC, o CTC e a percentagem de custos consumidos na tarefa são recalculados.
2.  A nova EAC é distribuída para as tarefas subordinadas na mesma proporção que a EAC original nas tarefas.
3.  É calculada a nova EAC para cada tarefa.
4.  Os CTS e a percentagem de custos consumidos são recalculados para as tarefas subordinadas afetadas, com base no valor da EAC. O desvio de custos das tarefas também é recalculado.
5.  A EAC para todas as tarefas de resumo é recalculada com base nesta alteração.

Clique em **Expandir para o nível** na vista Monitorização do custo para definir o nível a rastrear e manter a sua WBS. A WBS é expandida para esse nível na vista Monitorização do custo sempre que o abre.

### <a name="earned-value-management"></a>Gestão do valor ganho

Pode utilizar o método de valor ganho (EVM) para monitorizar o progresso de um projeto. Pode ver as métricas de valor ganhas no Centro de Funções do gestor de projetos. A componente de gráfico do valor ganho mostra os valores faseados no tempo do valor planeado e do custo real. O valor ganho a partir da data atual é mostrado como um ponto. Os dados faseados no tempo para o valor ganho não estão atualmente disponíveis. 

A fase de tempo no gráfico de valores ganhos é apresentado por semana ou por mês. Esta secção descreve os três pilares do EVM: valor planeado, valor ganho e custo real. 

**Valor planeado** O EVM estabelece que a linha de valor planeado representa a taxa a que a equipa do projeto planeou ganhar valor no projeto. 

O Finance utiliza a regra de ganhos de 0:100 quando traça o valor planeado. Segundo esta regra, o valor da tarefa é lançado para a tarefa a partir da respetiva data de fim. Nenhum valor é lançado enquanto a tarefa não for 100% concluída. 

Em Gestão de projetos e contabilística, introduza a data de fim dos nós de folha e o custo planeado dos mesmos. Quando o gráfico do valor planeado é apresentado por semana, o valor planeado é resumido por semana para todas as tarefas do nó de folha durante a duração do projeto. 

**Valor ganho** O EVM estabelece que a linha de valor ganho representa a taxa a que a equipa do projeto está realmente a ganhar valor no projeto. 

O Finance utiliza a regra de ganhos de 0:100 quando traça o valor ganho. Segundo esta regra, o valor da tarefa é lançado para a tarefa a partir da respetiva data de fim. Nenhum valor é lançado enquanto a tarefa não for 100% concluída. 

Quando o valor ganho é calculado, é considerada a percentagem de progresso de cada tarefa. Segundo a regra de ganhos de 0:100, só as tarefas que estão concluídas num determinado período são consideradas para o cálculo do valor ganho no final desse período. O valor ganho no projeto é calculado para todas as tarefas que foram concluídas quando o gráfico é criado. 

> [!NOTE] 
> Atualmente, o sistema para a monitorização da WBS não tem estruturas de dados para armazenar percentagens de progresso históricas em cada tarefa. Por isso, o valor ganho só pode ser comunicado a partir do momento em que o cubo é processado. Processe o cubo regularmente para atualizar os dados do valor ganho que são mostrados no Centro de Funções. 

**Custo real** A EVM estabelece que a linha de custo real representa a taxa a que o dinheiro está a ser gasta no projeto. 

As transações que são lançadas para um projeto são utilizadas para traçar a linha de custos real. Os custos são resumidos por data. Em seguida, estes dados são utilizados para criar o gráfico dos custos reais por semana ou por mês gráfico de valores ganhos.

### <a name="how-to-use-the-concepts-of-planned-value-earned-value-and-actual-cost"></a>Como utilizar os conceitos de valor planeado, valor ganho e custo real

**Desvio da agenda** Durante o planeamento, crie uma previsão para o trabalho numa linha cronológica. Por isso, o valor planeado é a taxa a que os planeadores de projetos pensavam que o trabalho seria concluído no projeto. Depois de um projeto estar em curso, o trabalho é concluído e o projeto ganha valor. Ao comparar o valor planeado com o valor ganho, pode ver como o trabalho num projeto está a progredir. O resultado desta comparação chama-se desvio da agenda. 

Se o valor planeado para um período for superior ao valor ganho, o montante do trabalho que foi feito num projeto é inferior ao planeado. Por isso, o projeto está atrasado. Como o valor planeado e o valor ganho são expressos em termos monetários, o tempo de atraso no projeto também é apresentado como um valor monetário. 

Se o valor planeado para um período for inferior ao valor ganho, o montante do trabalho que foi feito num projeto é superior ao planeado. Por isso, o projeto está adiantado. A este prazo também é atribuído um valor monetário.

**Desvio de custos** Como o valor ganho utiliza o preço de custo como multiplicador, o valor ganho indica o custo do trabalho que é feito num projeto. À medida que um projeto progride, o registo de transações fornece um registo do dinheiro que é realmente gasto nesse projeto. Ao comparar o valor ganho com o custo real, pode ver o montante de dinheiro que está a ser gasto em relação ao valor que é ganho. O resultado desta comparação chama-se desvio de custos. 

Se o custo real que é gasto por um período for superior ao valor ganho, significa que foi gasto mais dinheiro do que ganho. Por isso, o projeto está acima do orçamento. 

Se o custo real que é gasto por um período for inferior ao valor ganho, significa que foi ganho mais dinheiro do que gasto. Por isso, o projeto está abaixo do orçamento.

## <a name="wbs-templates"></a>Modelos de WBS
Pode utilizar a funcionalidade de Modelos de WBS para criar modelos padrão para projetos. Se os projetos que a sua empresa oferece envolvem muito trabalho repetível, deve considerar a criação de um modelo de WBS. 

Pode criar um modelo de WBS a partir da WBS de um projeto existente para os conhecimentos e as melhores práticas que reuniu durante o planeamento desse projeto poderem ser reutilizados em projetos semelhantes no futuro. No entanto, por vezes poderá não fazer sentido guardar toda a WBS como um modelo. Por isso, também pode criar modelos a partir de partes da WBS para um projeto.

### <a name="saving-a-projects-wbs-as-a-template"></a>Guardar a WBS de um projeto como um modelo

Depois de criar um modelo, pode importá-lo para a WBS de um novo projeto sob o nó raiz, ou sob qualquer tarefa na WBS do projeto.

### <a name="importing-a-wbs-template-into-a-projects-wbs"></a>Importar um modelo de WBS para a WBS de um projeto

Quando importa tarefas, as tarefas no modelo são organizadas com base na data de início da tarefa sob a qual são importadas. Durante a importação, as relações antecessores nas tarefas do modelo são utilizadas para calcular as datas de início para as tarefas importadas. O calendário de trabalho padrão do projeto de destino é aplicado para calcular as datas finais das tarefas importadas para os dias de trabalho e as horas de trabalho padrão definidas no calendário de trabalho do projeto em curso serem mantidos. 

Os montantes dos custos e os preços de venda nas linhas de estimativa são aplicados para garantir que os preços que são específicos do projeto ou do contrato de projeto têm datas válidas.

### <a name="differences-between-a-projects-wbs-and-a-wbs-template"></a>Diferenças entre a WBS de um projeto e um modelo de WBS

-   As tarefas nos modelos de WBS não têm datas de início e datas de fim.

Os dias de trabalho e descanso não estão definidos para os modelos de WBS.

-   Os modelos de WBS utilizam sempre o calendário da agenda que está configurado como calendário predefinido para todos os projetos.

O calendário de agendamento predefinido é utilizado apenas para saber as horas num dia de trabalho normal.

-   As relações de antecessor não são copiadas para um modelo de WBS.

Como os modelos de WBS não têm datas, a lógica da data de início que se baseia na data de fim de uma antecessora não é obrigatória.

-   Uma linha de estimativa de custos de mão de obra é criada automaticamente quando uma tarefa é criada num modelo de WBS. O preço de venda e o montante do custo são copiados a partir do trabalhador selecionado.

Os custos de despesas e de itens podem ser criados manualmente, tal como na WBS de um projeto.

-   São apresentados erros de agendamento quando existem desvios em relação à seguinte fórmula:

Esforço = Número de recursos × Duração × Número de horas num dia de trabalho padrão 

Pode corrigir todos os erros de agendamento ao mesmo tempo ao clicar em **Corrigir todos os erros de agendamento**. 

Em alternativa, pode corrigir os erros de agendamento individualmente ao clicar no ícone de aviso para cada tarefa.



