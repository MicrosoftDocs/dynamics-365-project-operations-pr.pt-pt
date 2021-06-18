---
title: Descrição geral da gestão de projetos e contabilística
description: A funcionalidade de gestão de projetos e contabilística pode ser utilizada em vários setores para prestar um serviço, produzir um produto ou obter um resultado.
author: Yowelle
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjTable; ProjProjectManagementWorkspace
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a6d3b9eb97fce836e5b2310714d8f731b2c09e6c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008145"
---
# <a name="project-management-and-accounting-overview"></a>Descrição geral da gestão de projetos e contabilística

[!include [banner](../includes/banner.md)]

A funcionalidade de gestão de projetos e contabilística pode ser utilizada em vários setores para prestar um serviço, produzir um produto ou obter um resultado.  

Um projeto é um conjunto de atividades que foi concebido para prestar um serviço, produzir um produto ou alcançar um resultado. Os projetos consomem recursos e geram resultados financeiros sob a forma de receitas ou ativos.

## <a name="projects-across-industries"></a>Projetos em todos os setores
A funcionalidade de gestão de projetos e contabilística pode ser utilizada em vários setores, como é mostrado na seguinte ilustração.

[![Projetos em todos os setores](./media/projects-accross-industries.jpg)](./media/projects-accross-industries.jpg) 

Num centro de atendimento, pode ser utilizado um bilhete para descrever o conjunto de ações que são necessárias para resolver uma chamada. As empresas de consultoria, tais como as organizações de gestão ou consultoria técnica, ou as agências de publicidade, referem-se às suas atividades como projetos. No marketing, uma campanha representa um conjunto de trabalhos que têm de ser entregues. Na indústria baseada em projetos, um pedido de produção relaciona os vários trabalhos que têm de ser feitos para produzir alguns produtos acabados. Seja qual for o nome utilizado para eles, estes projetos envolvem recursos, agendas e custos, e a funcionalidade de gestão de projetos e contabilística podem ajudar no planeamento, na execução e na análise destes projetos.

## <a name="project-phases"></a>Fases do projeto
Apesar de o seguinte fluxo de processo se destinar a projetos externos, ou projetos que são concluídos para um ou mais clientes, a funcionalidade também se aplica aos projetos internos só de custos. 

![3 fases de um projeto](./media/3-stages-of-a-project.png) 

Tal como é mostrado na ilustração anterior, a gestão de projetos e contabilística pode ser dividida em três fases:

1.  Iniciar
2.  Executar
3.  Analisar

## <a name="initiate-the-project"></a>Iniciar o projeto
Durante o início do projeto, ocorrem vários processos chave. Pode utilizar uma cotação do projeto para comunicar a estimativa de mão-de-obra, despesas e materiais ao cliente. Pode registar os termos, os limites e os acordos de faturação num contrato de projeto. Pode utilizar uma estrutura hierárquica trabalho (WBS) para planear e fazer uma estimativa do trabalho. Pode configurar as previsões e os orçamentos para orientar a execução do projeto. A seguinte ilustração mostra a estrutura de um projeto.[![estrutura de projeto](./media/project-structure1.jpg)](./media/project-structure1.jpg)  

### <a name="create-project-quotations"></a>Criar cotações de projeto

Na fase inicial de vendas de um projeto, uma cotação do projeto permite-lhe fornecer a um cliente uma oferta não vinculativa. Uma cotação pode incluir elementos como os itens e os serviços que são cotados, informações básicas de contacto, acordos comerciais especiais e descontos, e possíveis impostos e sobretaxas.

Também pode emitir uma carta de garantia para uma transação de cotação do projeto entre a sua organização e o cliente. Após a criação da cotação do projeto, pode criar o pedido de carta da garantia para o cliente e submetê-lo ao banco. Depois de o banco aprovar o pedido, a carta de garantia é emitida para o cliente. 

Para mais informações, consulte [Cotações do projeto](project-quotations.md).

### <a name="create-project-contracts"></a>Criar contratos do projeto

Quando celebra um contrato com um cliente ou outra fonte de financiamento para concluir um projeto, primeiro tem de criar um contrato de projeto. Depois, quando cria o projeto, tem de atribuí-lo ao contrato correspondente. O tipo de projeto que cria para um contrato de projeto determina o método que é utilizado para faturar os clientes do projeto. Pode modificar um contrato de projeto e o projeto relacionado, mas não pode alterar o tipo de projeto. Para obter mais informações sobre os tipos de projeto, consulte a secção "Criar projetos".

Para mais informações sobre contratos de projeto, consulte [Contratos de projeto](project-contracts.md).

### <a name="create-work-breakdown-structures"></a>Criar estruturas hierárquicas do trabalho

O grau de detalhe numa WBS depende do nível de precisão exigido nas estimativas e do nível de monitorização que é necessário em relação a essas estimativas. Normalmente, os projetos com muito baixa tolerância de derrapagem na agenda ou no custo necessitam de uma WBS mais detalhada, e também necessitam de uma monitorização diligente do progresso do trabalho e do custo em relação à WBS. 

Para mais informações, consulte [Descrição geral das estruturas hierárquicas do trabalho](work-breakdown-structures.md).

### <a name="create-project-forecasts-and-budgets"></a>Criar previsões e orçamentos de projetos

Pode utilizar a previsão se a sua organização tiver uma perspetiva operacional, e se concentrar nas receitas e nos custos provenientes de transações específicas. No entanto, se a sua organização se concentrar mais nos montantes financeiros, pode usar a orçamentação. Cada método tem as suas vantagens. Para mais informações, consulte [Previsões e orçamentos de projetos](project-forecasts-budgets.md).

### <a name="create-projects"></a>Criar projetos

Pode criar seis tipos de projeto no Finance. Cada tipo de projeto é configurado de forma diferente para os custos e o reconhecimento de receitas. O tipo de projeto que escolher depende da finalidade do projeto. A tabela seguinte descreve a utilização típica de cada tipo de projeto.
                                                                                                            
<table>
  <tr>
    <td>Tipo de projeto</th>
    <td>Descrição</th>
  </tr>
  <tr>
    <td>Tempo e material</td>
    <td>Nos projetos de Tempo e material, o cliente é faturado por todos os custos incorridos num projeto. Estes custos incluem os custos por horas, despesas, itens e taxas.</td>
  </tr>
  <tr>
    <td>Preço fixo</td>
    <td>Nos Projetos de preço fixo, as faturas são compostas por transações em conta. Um projeto de preço fixo é faturado de acordo com uma agenda de faturação que se baseia num contrato de projeto. As receitas de um projeto de preço fixo podem ser calculadas e lançadas em todo o projeto através do método de percentagem concluída. Em alternativa, as receitas podem ser calculadas e lançadas quando o projeto estiver concluído, através do método de contrato concluído. As empresas podem muitas vezes beneficiar da utilização do valor do trabalho em curso (WIP) para calcular o grau de conclusão de um projeto ou grupo de projetos.</td>
  </tr>
  <tr>
    <td>Investimento</td>
    <td>Os projetos de investimento são projetos que não produzem ganhos imediatos. Normalmente, são utilizados para projetos internos a longo prazo onde os custos têm de ser capitalizados. Só os custos de itens, horas e despesas podem ser registados num projeto de Investimento. Os custos num Projeto de investimento são monitorizados e controlados através da funcionalidade de estimativa. Os Projetos de investimento podem ser configurados com uma capitalização máxima opcional. À medida que um Projeto de investimento progride, vá registando os seus custos em contas WIP, onde os custos são mantidos até o projeto estar concluído. Quando o projeto é eliminado, transfere o valor WIP para um ativo fixo, uma conta do livro razão ou um novo projeto. <br></br> <strong>NOTA:</strong> as transações em Projetos de investimento não são mostradas na página <strong>Lançar custos<strong>, <strong>Acumular receitas</strong> ou <strong>Criar propostas de fatura</strong>.</td>
  </tr>
  <tr>
    <td>Projeto de custos</td>
    <td>Tal como os Projetos de investimento, normalmente os Projetos de custos são utilizados para monitorizar os projetos internos, e só as horas, as despesas e os itens podem ser registados para eles. No entanto, os Projetos de custos são normalmente de menor duração do que os Projetos de investimento. Além disso, ao contrário dos projetos de investimento, os projetos de custos não podem ser capitalizados para contas de balanço. Em vez disso, as suas transações de projetos são lançadas apenas nas contas de resultados. <br></br> <strong>NOTA:</strong> as transações em Projetos de custos não são refletidas na página <strong>Lançar custos</strong>, <strong>Acumular receitas</strong> ou <strong>Criar propostas de fatura</strong>. Como normalmente os projetos de custos são utilizados para monitorizar projetos internos, normalmente não têm de estar associados a uma conta de cliente. No entanto, se a sua configuração exigir a criação de requisitos de itens para notas de encomenda, tem de associar o Projeto de custos a um cliente. Esta associação é necessária, porque os requisitos de item são geridos como linhas de encomenda de vendas, e o sistema requer que seja especificado um cliente. No entanto, esta configuração não fará com que sejam criados os requisitos de itens automaticamente a partir de uma nota de encomenda. Para os Projetos de custos, a definição <strong>Criar requisito de item</strong> é ignorada. Se precisar de um requisito de artigo num Projeto de custos, pode criá-lo manualmente, desde que um cliente esteja associado ao projeto.</td>
  </tr>
  <tr>
    <td>Interna</td>
    <td>Os projetos internos são utilizados para monitorizar os custos num projeto interno da organização. Os projetos internos podem fornecer uma ferramenta de planeamento para gerir o consumo de recursos. <br></br><strong>NOTA:<strong> as transações em projetos internos não são refletidas na página <strong>Acumular receitas</strong> ou <strong>Criar propostas de fatura</strong>.</td>
  </tr>
  <tr>
    <td>Time</td>
    <td>Os projetos de tempo são utilizados para monitorizar o tempo que está associado a atividades não cobráveis e não produtivas, como um projeto para monitorizar a ausência por doença dos trabalhadores. As transações em projetos de tempo não são lançadas no livro razão. Em vez disso, são incluídas nos relatórios de utilização dos trabalhadores. Só as transações de horas podem ser registadas em Projetos de tempo. Utilize um diário de horas ou uma folha de horas para registar estas horas no projeto. Depois de registadas as horas, aparecem como transações de projeto, mas não têm transações de vouchers correspondentes. <br></br><strong>NOTA:</strong> as transações em Projetos de tempo não são refletidas na página <strong>Lançar custos</strong>, <strong>Acumular receitas</strong> ou <strong>Criar propostas de fatura</strong>.</td>
  </tr>
</table>


### <a name="assign-workers-categories-and-resources"></a>Atribuir trabalhadores, categorias e recursos

Pode agendar os recursos dos trabalhadores baseado nos requisitos e na agenda de um projeto, ou nas competências e na disponibilidade dos trabalhadores. Ao utilizar as capacidades de agendamento de recursos, pode implementar os trabalhadores da sua organização de forma eficiente e eficaz. Poderá localizar rapidamente os trabalhadores mais qualificados que estão disponíveis para trabalhar no seu projeto. Também poderá ver facilmente como esses trabalhadores poderão ser utilizados de forma mais eficaz durante o projeto. 

Seguem-se algumas das formas de utilizar a funcionalidade de agendamento de recursos:

-   Utilize a informação sobre os atributos de um trabalhador, como a formação, as competências, as certificações e experiência no projeto, para o fazer corresponder aos requisitos de um projeto.
-   Utilize as informações sobre a disponibilidade e o calendário de um trabalhador para fazer a correspondência da agenda do trabalhador com o calendário do projeto.
-   Reveja a capacidade de cada trabalhador e determine como essa capacidade está a ser utilizada. Por exemplo, se um trabalhador estiver a ser subutilizado, o trabalhador pode ser atribuído a um projeto que se enquadre na sua disponibilidade e atributos.
-   Reveja a disponibilidade de um trabalhador para assegurar que não existem conflitos de calendário com as atribuições do trabalhador.
-   Reveja a informação sobre a utilização dos trabalhadores numa vista de resumo (por exemplo, por departamento ou por trabalhador) ou uma vista detalhada (por exemplo, por trabalhadores num departamento ou por detalhe semanal para cada trabalhador).
-   Modifique as atribuições de recursos para várias unidades de tempo, como dia, semana ou mês, para otimizar a forma como os trabalhadores são utilizados.

## <a name="execute-the-project"></a>Executar o projeto
Durante a execução do projeto, os membros ou os gestores da equipa registam o trabalho e as despesas incorridos, através de folhas de horas, relatórios de despesas e outros documentos empresariais. Os gestores de projetos têm ferramentas que lhes permitem monitorizar o consumo dos montantes orçamentados para o projeto. Os gestores de projetos também podem encomendar, escolher ou adquirir materiais para projetos através de notas de encomenda e outros documentos empresariais. As faturas são preparadas e aprovadas para que os clientes possam ser faturados para o trabalho em curso. Finalmente, as receitas são reconhecidas durante este processo para afetarem as finanças da organização.

### <a name="manage-work-breakdown-structures"></a>Gerir estruturas hierárquicas do trabalho

Uma WBS é uma descrição do trabalho que será concluído para um projeto. Uma WBS é uma hierarquia de tarefas. Representa não apenas o trabalho para cada tarefa, mas também o tamanho, o custo e a duração da tarefa. 

Para mais informações, consulte [Descrição geral das estruturas hierárquicas do trabalho](work-breakdown-structures.md).

### <a name="manage-project-forecasts-and-budgets"></a>Gerir previsões e orçamentos de projetos

Existem duas formas de gerir e controlar os seus projetos: previsões de projetos e orçamentos de projetos. Pode utilizar a previsão se a sua organização tiver uma perspetiva operacional, e se concentrar nas receitas e nos custos provenientes de transações específicas. No entanto, se a sua organização se concentrar mais nos montantes financeiros, pode usar a orçamentação.

Para mais informações, consulte [Previsões e orçamentos de projetos](project-forecasts-budgets.md).

### <a name="create-production-orders"></a>Criar ordens de produção

Uma ordem de produção relacionada com o projeto pode ser associada a uma ordem de venda ou a um requisito de item através do método do item acabado ou do método do item consumido. Além disso, se a ordem de produção foi criada manualmente, não existe qualquer associação entre a ordem de produção e a ordem de venda ou requisito do item (sem ligação à ordem). No entanto, se a ordem de produção foi criada automaticamente para cumprir uma ordem de venda ou um requisito de item, existe uma associação entre a ordem de produção e a ordem de venda ou o requisito de artigo (associação à ordem). 

Baseado nas combinações destes fatores, utilize um dos seguintes métodos:

- **Item concluído/ligação à encomenda** – Ligar o projeto a uma ordem de venda ou a um requisito de item. Quando utiliza este método, os custos do projeto reais são lançados quando a ordem de venda é faturada ou quando o recibo de entrega for atualizado para o requisito do item. O custo é lançado como um item acabado.
- **Item acabado/sem ligação à ordem** – Os custos reais não podem ser lançados até o ciclo de produção de um item ter o estado **Terminado**. O custo do item acabado é lançado como uma única transação.
- **Item consumido/ligação à encomenda** – Ligar o projeto a um requisito de item. Ao utilizar este método, pode ver os custos do projeto reais quando a produção tem o estado **Iniciado** ou é reportada como terminada. Os custos são lançados como várias transações de itens do projeto para matérias-primas e horas consumidas para produção. Quando o recibo de entrega é atualizado para o requisito de item, não são lançados custos do projeto. Também pode definir o nível na hierarquia da lista de materiais (BOM) em que os projetos na produção são monitorizados.
- *<strong><em>Item consumido/sem ligação à encomenda</em></strong>* – Ligar o projeto a um requisito de item. Ao utilizar este método, pode ver os custos do projeto reais quando a produção tem o estado <strong>Iniciado</strong> ou é reportada como terminada. Os custos são lançados como várias transações de itens do projeto para matérias-primas e horas consumidas para a produção. Também pode definir o nível na hierarquia BOM em que os projetos na produção são monitorizados.

### <a name="procure-products-and-services"></a>Adquirir produtos e serviços

A compra e venda de itens são atividades frequentes em muitos negócios focados em projetos.

#### <a name="purchase-orders-for-projects"></a>Notas de encomenda para projetos

O objetivo da nota de encomenda é determinar quando nota de encomenda é consumida e, portanto, quando os itens são cobrados num projeto.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Método</th>
<th>Objetivo</th>
<th>Consumo de itens</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Crie uma nota de encomenda diretamente.</td>
<td>Compre itens a um fornecedor externo para consumo num projeto. Pode criar a nota de encomenda das seguintes formas:
<ul>
<li>A partir do próprio projeto. Neste caso, o projeto já está definido para a nota de encomenda.</li>
<li>Ao navegar para a nota de encomenda do projeto. Tem de selecionar o fornecedor e o projeto para o qual pretende criar a nota de encomenda.</li>
</ul></td>
<td>Os itens são consumidos quando a fatura do fornecedor é atualizada.</td>
</tr>
<tr class="even">
<td>Crie uma nota de encomenda a partir de uma nota de encomenda.</td>
<td>Compre artigos quando criar uma ordem de venda a partir de um projeto.</td>
<td>Os itens são consumidos quando a ordem de venda é faturada ao cliente.</td>
</tr>
<tr class="odd">
<td>Crie uma nota de encomenda a partir de um requisito de item.</td>
<td>Compre itens quando criar uma requisito de item a partir de um projeto.</td>
<td>Os itens são consumidos quando o recibo de entrega do requisito de item é atualizado.</td>
</tr>
</tbody>
</table>

#### <a name="sales-orders-for-projects"></a>Ordens de vendas para projetos

Em gestão de projetos e contabilística, pode registar o consumo de itens de várias formas. Pode vender ou comprar itens de um projeto, ou reservar itens para um projeto. 

Pode encomendar itens do inventário da empresa para consumo num projeto. Em alternativa, pode comprar itens a um fornecedor externo. Os itens podem ser consumidos em todos os tipos de projeto, exceto Projetos de tempo. 

A forma como encomenda itens depende de onde os encomenda:

-   Para encomendar itens do inventário da empresa, tem de inserir a encomenda como requisito de item. Se utilizar a página **Requisitos de item**, pode configurar o requisito para que receber os itens como entregas parciais. Assim, pode adiar o consumo de uma quantidade de itens até os itens serem necessários.
-   Para encomendar itens a um fornecedor externo, tem de criar a encomenda como uma nota de encomenda na página **Nota de encomenda**.

> [!NOTE] 
> O recibo de entrega para uma ordem de venda relacionada com o projeto não pode ser cancelado se os itens já estiverem marcados para a embalagem. 

A tabela seguinte lista os métodos para encomendar itens e descreve como os itens são consumidos.

| Método            | Objetivo                                                                                                                                                        | Consumo de transações de itens                                                                                                                  |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| Ordem de venda       | Introduza uma transação diretamente num Projeto de tempo e material.                                                                                                   | As transações de itens são consumidas quando a fatura do cliente é lançada.                                                                               |
| Diário do inventário | Introduza e mantenha rapidamente registos de itens. Se, por exemplo, pretende introduzir um requisito de item baseado numa lista impressa, pode ser aplicado o diário de inventário. | As transações de itens são consumidas quando o diário é lançado.                                                                                        |
| Requisito de item  | Introduza os itens que não serão consumidos imediatamente. Este método permite-lhe monitorizar o número de itens que foram consumidos num único registo de requisito de item.    | As transações de itens são consumidas quando o recibo de entrega é atualizado. Por outras palavras, o requisito de item é criado quando o recibo de entrega é lançado. |
| Notas de encomenda   | Introduza as transações numa de três localizações, consoante o método de compra.                                                                              | As transações de itens são consumidas quando o recibo de entrega é atualizado, ou quando o cliente ou o fornecedor é faturado.                                      |

### <a name="process-project-invoices"></a>Processar faturas do projeto

O tipo de projeto determina o procedimento de faturação a aplicar. Só os dois tipos de projeto externos (Tempo e material e Preço fixo) podem ser faturados. Os Projetos de tempo e material e os Projetos de preço fixo estão sempre ligados a um contrato de projeto. 

Antes de criar uma fatura do cliente para um projeto, pode criar uma fatura preliminar ou uma proposta de fatura. Numa proposta de fatura, pode selecionar as transações de projeto a incluir numa fatura de projeto. Em seguida, pode rever os dados da fatura antes de lançar a fatura de projeto e enviá-la para o cliente ou outra fonte de financiamento. 


Para obter mais informações sobre como processar faturas de projeto, consulte [Faturação de projetos](/dynamics365/finance/accounts-payable/project-invoicing).


### <a name="calculate-the-cost-to-complete-a-project"></a>Calcular o custo para concluir um projeto

Quando cria uma estimativa, pode escolher o método utilizado para calcular o custo para concluir o projeto. Selecione um método no campo **Método Custo para conclusão** na página **Criar estimativa**. O método que escolher é aplicado separadamente a cada linha de custo na estimativa de custo. Enquanto uma linha tiver o estado **Criado**, poderá alterar o método que lhe é aplicado na página **Estimativa de custo**. 

A tabela seguinte descreve os métodos de cálculo do custo para a conclusão de um projeto.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Método</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Custo total – real</td>
<td>Os custos estimados têm de ser introduzidos manualmente. Após a conclusão da coluna <strong>Custo total</strong> ou <strong>Quantidade total</strong> na página <strong>Estimativa de custo</strong>, os custos reais são subtraídos aos totais introduzidos pelo utilizador. O resultado é o custo para a conclusão do projeto. Normalmente, o progresso dos custos não é monitorizado com base, por exemplo, no número de estadas e refeições em hotéis que são registadas em cada período. Em vez disso, A monitorização normalmente baseia-se numa comparação com o montante total de horas estimadas. Esta abordagem não requer um modelo de previsão, e o custo total ou a quantidade total podem ser alterados manualmente. Quando um valor é introduzido na coluna <strong>Custo total</strong>ou <strong>Quantidade total</strong>, o Finance compara este valor com as transações reais que são lançadas no período e, em seguida, diminui o valor na coluna <strong>Quantidade para conclusão</strong> ou <strong>Custo para conclusão</strong>.</td>
</tr>
<tr class="even">
<td>Orçamento total – real</td>
<td>Os custos reais são comparados com o modelo de previsão que seleciona para determinar o custo. Este método utiliza um modelo orçamental total que inclui transações previstas. Para obter uma vista mais precisa do projeto, pode ajustar o modelo orçamental quando o projeto estiver em curso. Se tiver de ajustar a previsão, siga este processo geral:
<ol>
<li>Copie as transações de previsão para outro modelo de previsão.</li>
<li>Compare as transações de previsão com as transações reais.</li>
<li>Mantenha, diminua ou aumente as estimativas para o próximo período.</li>
</ol>
O Finance não diminui automaticamente as estimativas previstas. Portanto, é uma boa ideia manter um modelo de previsão original no Projeto de preço fixo para estabelecer uma linha de base para comparação quando o projeto for concluído. 
<br></br> <strong>NOTA:</strong> quando selecionar este método, utilize pelo menos dois modelos de previsão. Um modelo deve conter a previsão original. Para o outro modelo, deve copiar transações de previsão a partir de outro modelo. Este método é válido apenas para os Projetos de preço fixo e Projetos de investimento.</td>
</tr>
<tr class="odd">
<td>Orçamento restante</td>
<td>Este método utiliza um modelo orçamental restante para calcular o custo para conclusão do projeto. Quando utiliza este método, os custos reais e os montantes previstos no modelo orçamental restante são adicionados em conjunto. O resultado é um custo total. Antes de utilizar este método, deve ser configurado um modelo orçamental restante para deduzir as transações com base nas transações reais que registadas no sistema. Na página <strong>Modelos de previsão</strong>, certifique-se de que os campos estão marcados no grupo <strong>Redução automática da previsão</strong>. Normalmente, um orçamento restante é copiado a partir de um orçamento original. À medida que as transações são introduzidas, as transações no orçamento restante são diminuídas. À medida que o projeto avança, se determinar que o orçamento restante tem de ser ajustado, cobre as transações de previsão para o orçamento restante. <br></br> <strong>NOTA:</strong> este método só pode ser aplicado se um modelo de previsão for anexado à estimativa.</td>
</tr>
<tr class="even">
<td>Como estimativa anterior</td>
<td>Aplica-se o mesmo método de estimativa utilizado no período anterior. Este método requer um modelo de previsão se o período anterior requeria de um modelo de previsão.</td>
</tr>
<tr class="odd">
<td>Definir custo para conclusão como zero</td>
<td>Normalmente, este método é usado antes de a estimativa de projeto ser eliminada. Este método corresponde às estimativas totais com as transações reais que foram lançadas e limpa a coluna <strong>Custo para conclusão</strong>. A percentagem de conclusão resultante é sempre de 100%. O campo <strong>Previsão</strong> não é selecionado para cada linha de custo que cria, e a estimativa total é copiada a partir da estimativa de custos anterior. O consumo real para a estimativa do período é deduzido do custo para conclusão do projeto. Este método não requer um modelo de previsão.</td>
</tr>
<tr class="even">
<td>Do modelo de custo</td>
<td>É aplicado o método de custo para conclusão que é configurado no modelo de custo que está associado à estimativa de projeto selecionada.</td>
</tr>
</tbody>
</table>

## <a name="analyze-the-project"></a>Analisar o projeto
No seu nível mais básico, um projeto é utilizado para agrupar transações que registam custos e, em seguida, lançar estes custos no razão geral. 

Normalmente, estas transações são o resultado de documentos empresariais, tais como folhas de horas, relatórios de despesas, faturas de fornecedores ou transações do inventário. Normalmente, o ciclo de vida de um projeto começa com estimativas, previsões e orçamentos que ajudam a planear e antecipar o trabalho e o impacto financeiro do projeto. À medida que analisa um projeto, pode avaliar não só as transações que ocorreram durante o projeto, mas também a precisão das suas estimativas e previsões, as taxas de utilização dos membros da equipa do projeto e o sucesso global do projeto.

### <a name="analyze-cash-flow"></a>Analisar o fluxo de caixa

Utilize a monitorização do fluxo de caixa para rever os fluxos de caixa previstos e os fluxos de caixa reais de um projeto. Pode rever fluxos de caixa enquanto um projeto está em curso ou ver os fluxos de caixa de um projeto concluído. 

Ao monitorizar os fluxos de caixa, pode avaliar um único projeto, utilizar os relatórios para ver vários projetos e transferir fluxos de caixa do projeto para as previsões de fluxo de caixa no razão geral.

#### <a name="cash-inflow-forecasting"></a>Previsão de entrada de caixa

Baseado na sua configuração, pode prever as entradas de caixa de um projeto selecionado. Por exemplo, se a data do projeto for 5 de março de 2012, e faturar em 31 de março de 2012, veja como pode prever a data de vencimento e a data de pagamento de vendas esperada:

-   **Data do projeto:** 5 de março de 2012.
-   **Data da fatura:** 31 de março de 2012. Esta data é determinada com base na frequência da fatura. Para este exemplo, defina a frequência da fatura para o mês atual. Assim, todas as transações que são lançadas no mês de março são faturadas no último dia do mês.
-   **Data de vencimento:** 14 de abril de 2012. Esta data é determinada com base nos termos de pagamento que foram definidos para o projeto. Para este exemplo, selecionou as condições de pagamento de 14 dias. Assim, são adicionados 14 dias à data da fatura para chegar à data de vencimento de 14 de abril de 2012.
-   **Data de pagamento de vendas prevista:** 27 de abril de 2012. Esta data é calculada ao adicionar o número de dias no campo **Dias de reserva geral** na página **Parâmetros da Gestão de projetos e contabilística** ao número de dias no campo **Dias de reserva individual** na página **Contratos do projeto** e, em seguida, adicionar o total ao número de dias no campo **Data de vencimento**. Para este exemplo, introduziu **3** no campo **Dias de reserva geral** e **10** no campo **Dias de reserva individual**. Assim, são adicionados 13 dias à data de vencimento para chegar a uma data de pagamento esperada de 27 de abril de 2012.

Os dias de reserva geral podem substituir os dias de reserva individual ou ser adicionados aos dias de reserva individual:

-   Para utilizar os dias de reserva geral como substituição dos dias de reserva individual, introduza o número médio de dias entre a data de vencimento e a data de pagamento real para os clientes.
-   Para adicionar os dias de reserva geral aos dias de reserva individual, no campo **Dias de reserva geral**, introduza a sua estimativa para o número de dias entre o dia em que o cliente envia o pagamento e o dia em que a sua organização recebe o pagamento.

Configure os dias de reserva individual no contrato do projeto. Os dias são calculados com base na data de vencimento da fatura de venda e na experiência da sua organização com o padrão de pagamento de um cliente.

#### <a name="actual-cash-inflow"></a>Entrada de caixa real

A entrada de caixa real assemelha-se à previsão, mas pode iniciar os seus cálculos a partir da primeira data da fatura. Segue-se um exemplo:

-   **Data da fatura:** 2 de março de 2012.
-   **Data de vencimento:** 16 de março de 2012. Os termos de pagamento são definidas para 14 dias.
-   **Data de pagamento de vendas prevista:** 29 de março de 2012. O cálculo inclui três dias de reserva geral e 10 dias de reserva individual.

#### <a name="cost-forecasting"></a>Previsão de custos

Com base nos dias definidos, a data de pagamento do custo pode diferir da data do projeto. Neste caso, a data de pagamento do custo é calculada ao adicionar o número de dias a partir da data do projeto ao número de dias nos termos de pagamento. 

Por exemplo, a data do projeto da transação é 5 de março de 2012 e são definidos os seguintes termos de pagamento:

-   **Horas:** Mês atual (**M**)
-   **Despesas:** 14 dias (**D14**)
-   **Itens :** 30 dias (**D30**)

Com base nestas definições, segue-se a data de pagamento do custo para cada tipo de transação:

-   **Horas:** 31 de março de 2012, que é o último dia do mês selecionado.
-   **Despesas:** 19 de março de 2012, que é 14 dias após a data da transação.
-   **Itens:** 4 de abril de 2012, que é 30 dias após a data da transação.

> [!NOTE] 
> A data de vencimento da nota de encomenda baseia-se na transação do fornecedor quando a nota de encomenda do projeto é criada. A data de vencimento não é determinada por quaisquer predefinições. 

A data de pagamento do custo não é calculada em dias de reserva. Após a conclusão de um projeto, quando são concluídos todos os custos e a faturação, o custo e as vendas são lançados nas contas de resultados. 

Quando todas as faturas de vendas e fornecedores são concluídas, pode ver a relação entre os campos na página **Fluxo de caixa** e os campos na página **Extratos do projeto**.

:::row:::
    :::column:::
        #### <a name="cash-flow-page"></a>Página de fluxo de caixa
        - Entradas de caixa 
        - Saídas de caixa
        - Fluxos de caixa líquidos
    :::column-end:::
    :::column:::
        #### <a name="project-statements-page"></a>Página de extratos do projeto
        - Receita
        - Custo total
        - Margem bruta
    :::column-end:::
:::row-end:::

### <a name="review-costs"></a>Rever custos

Pode monitorizar os custos em que a sua organização incorre durante um projeto na página **Controlo de custos**. Ao comparar os custos orçamentados originais para o projeto com os custos reais atuais e os custos consolidados, poderá determinar se o projeto está a cumprir o orçamento, a excedê-lo ou abaixo. 

> [!NOTE] 
> Quando utiliza a página **Controlo de custos** para ver o estado atual dos custos do projeto, utilize os modelos de previsão que foram selecionados para o orçamento original e restante. Se selecionar outros modelos de previsão quando calcular os custos, os resultados do cálculo não serão exatos.

#### <a name="viewing-the-remaining-budgeted-amounts"></a>Ver os montantes orçamentados restantes

Se **Orçamento restante** for selecionado como método de controlo de custos na página **Parâmetros da gestão de projetos e contabilística**, a página **Controlo de custos** calcula custos que não foram lançados como reais ou marcados como consolidados. Especificamente, os montantes no separador **Geral** no painel inferior da página **Controlo de custos** são calculados das seguintes formas:

-   **Custo real** – o montante total que foi gasto no projeto para a linha de custo selecionada. O montante real do custo é calculado na página **Atualizações do livro razão**.
-   **Custo consolidado** – o montante adicional das despesas que a entidade jurídica se comprometeu a pagar. Os montantes dos custos consolidados específicos são calculados na página **Custos consolidados**.
-   **Orçamento restante** – o montante do montante orçamentado original que ainda está disponível para a linha de custo selecionada. O montante orçamental restante é calculado na página **Pré-visualização do razão geral**.
-   **Custo total** – a soma do custo real, custo consolidado e montantes orçamentais restantes.

Na página **Controlo de custos**, no separador **Desvio**, pode ver uma comparação do custo total esperado com o orçamento original. Esta comparação mostra quaisquer diferenças entre estes montantes. Portanto, pode ver onde os dados não coincidem. Os montantes do desvio são calculados das seguintes formas:

-   **Orçamento original** – o montante originalmente orçamentado para a linha de custo selecionada. O montante orçamental original é calculado na página **Pré-visualização do razão geral**.
-   **Custo total** – a soma do custo real, custo comprometido e orçamento restante, conforme comunicado no separador **Geral**.
-   **Desvio** – a diferença entre o custo total e o orçamento original.
-   **Desvio baseado na quantidade** – a diferença total entre a previsão original e a previsão total. Esta diferença pode ser expressa matematicamente como (Quantidade total prevista) × (Preço médio original – Preço médio total). Este cálculo aplica-se apenas às horas do projeto.
-   **Desvio baseado no preço** – a diferença total entre a previsão original e a previsão total. Esta diferença pode ser expressa matematicamente como (Preço previsto original) × (Quantidade prevista original – Quantidade prevista total). Este cálculo aplica-se apenas às horas do projeto.

#### <a name="viewing-the-total-budgeted-amounts"></a>Ver os montantes orçamentados totais

Se **Orçamento total** for selecionado como método de controlo de custos na página **Parâmetros da gestão de projetos e contabilística**, a página **Controlo de custos** calcula os custos reais e os custos totais do projeto para o ajudar a detetar qualquer diferença entre os dois. Especificamente, na página **Controlo de custos**, os montantes nas colunas no painel inferior no separador **Geral** são calculados das seguintes formas:

-   **Custo total orçamentado** – o montante total orçamentado para a linha de custo selecionada.
-   **Custo real** – o montante total dos custos que foram incorridos no projeto até à data para as linhas de custo selecionadas.
-   **Custo consolidado** – o montante total que foi consolidado para a linha de custo selecionada.
-   **Desvio** – a diferença entre a soma dos custos reais e consolidados, e o custo total. O desvio mostra se têm de ser especificados custos adicionais para o orçamento total.

Na página **Controlo de custos**, no separador **Desvio**, pode ver a diferença entre o orçamento total e o orçamento original ao analisar os seguintes campos:

-   **Orçamento original** – o montante originalmente orçamentado para a linha de custo. O orçamento original é calculado na página **Pré-visualização do razão geral**.
-   **Custo total orçamentado** – o custo total originalmente orçamentado para a linha de custo. O Custo total orçamentado é calculado na página **Pré-visualização do razão geral**.
-   **Desvio** – o desvio em relação à linha de custo. Este montante é calculado ao subtrair o custo total do orçamento original.
-   **Desvio baseado na quantidade** – a diferença total entre o orçamento original e o orçamento total. Este montante é calculado ao subtrair o total de horas orçamentadas das horas orçamentadas originais e, em seguida, multiplicar a diferença pelo preço de custo orçamentado original. Esta diferença pode ser expressa matematicamente como (Preço de custo orçamentado original) × (Horas orçamentadas originais – Total de horas orçamentadas). Este cálculo aplica-se apenas às horas do projeto.
-   **Desvio baseado no preço** – este montante é calculado ao subtrair o total de horas orçamentadas das horas orçamentadas originais e, em seguida, multiplicar a diferença pelo número total de horas consumidas. Esta diferença pode ser expressa matematicamente como (Total de horas consumidas) × (Horas orçamentadas originais – Total de horas orçamentadas). Este cálculo aplica-se apenas às horas do projeto.

### <a name="analyze-utilization"></a>Analisar a utilização

A taxa de utilização é a percentagem de tempo em que um trabalhador realiza um trabalho faturado ou produtivo num período de trabalho específico. As horas faturáveis são as horas do trabalhador que podem ser cobradas a um cliente específico. 

A taxa de utilização de um trabalhador é calculada ao dividir o número de horas faturáveis pelo número de horas de trabalho num período específico. Por exemplo, se um trabalhador tiver 30 horas faturáveis num período, e o número de horas de trabalho no mesmo período for de 40, a taxa de utilização do trabalhador é de 75%. 

Quando calcula a taxa de utilização de um trabalhador, pode calcular a taxa faturável ou a taxa de eficiência:

-   **Taxa faturável** – a diferença entre as horas faturáveis e as horas não faturáveis, ou horas normais.
-   **Taxa de eficiência** – a diferença entre as horas produtivas e as horas não não produtivas, ou horas normais. As horas produtivas são as horas que o trabalhador dedica a contribuir para um projeto específico. Normalmente, as horas produtivas são cobradas aos clientes, exceto no caso dos projetos internos. As horas não produtivas nunca são cobradas a um cliente.

Calcule as taxas de utilização na página **Utilização de horas**. Os cálculos baseiam-se nas preferências predefinidas. Estas preferências também especificam como as horas são calculadas ao atribuir a **Utilização** ou a **Carga** a cada tipo de projeto. Isto aplica-se aos cálculos de taxas faturáveis e aos cálculos da taxa de eficiência.

-   **Utilização** – as horas comunicadas para o tipo de projeto selecionado são sempre consideradas para utilização faturável ou eficiente.
-   **Carga** – as horas comunicadas para o tipo de projeto selecionado são sempre consideradas para utilização não faturável ou não eficiente.
-   **De acordo com a propriedade da linha** – as propriedades da linha de uma transação de horas específica determinam se as horas são consideradas para a utilização faturável ou eficiente.
-   **Não incluído** – as horas não contabilizadas para o cálculo da utilização faturável ou de eficiência.

Na página **Utilização de horas**, para além da percentagem da taxa de utilização global para um trabalhador ou projeto, pode ver o número de horas que foram utilizadas para os cálculos da taxa de utilização para cada um dos seguintes tipos de horas:

-   **Horas não incluídas** – estas horas não estão incluídas na taxa de utilização de horas.
-   **Horas incluídas** – estas horas são calculadas ao adicionar as horas de utilização e as horas de carga. Estas horas são incluídas na taxa de utilização.
-   **Horas de carga** – se estiver a calcular uma taxa faturável, estas horas são as mesmas que as horas não cobráveis. Se estiver a calcular uma taxa de eficiência, estas horas são as mesmas que as horas não produtivas.
-   **Horas de utilização** – se estiver a calcular uma taxa faturável, estas horas são as mesmas que as horas cobráveis. Se estiver a calcular uma taxa de eficiência, estas horas são as mesmas que as horas produtivas.

Quando calcula a taxa de utilização para um trabalhador, pode utilizar as horas normais ou as horas incluídas. Se utilizar as horas incluídas, terá de assegurar que os trabalhadores registam todo o respetivo tempo de trabalho nos períodos da folha de horas, porque o cálculo é expresso como uma percentagem das horas que são introduzidas. Quando calcula a taxa de utilização de horas para um projeto, contrato de projeto, registo de cliente ou categoria, tem de utilizar as horas incluídas para o seu cálculo.

### <a name="review-project-statements"></a>Rever extratos do projeto

Pode criar um extrato do projeto para ver um instantâneo rápida do progresso de um projeto. Quando executa um extrato do projeto, pode especificar os critérios utilizados para calcular o extrato ao fazer seleções no separador **Geral** na página do **Extratos do projeto**. Pode selecionar para incluir ou excluir as seguintes informações:

-   Tipos de projeto
-   Tipos de Transação
-   Data do projeto/data do livro razão
-   Dados

Após o cálculo do extrato, pode ver as seguintes informações nos vários separadores na página **Extratos do projeto**:

-   **Geral** – informação geral sobre a estrutura básica de resultados do projeto.
-   **Resultados** – informação sobre as receitas acumuladas.
-   **WIP** – informação sobre os saldos de conta do WIP.
-   **Consumo** – informação sobre o consumo de horas, itens, despesas e transações de pagamento.
-   **Fatura** – informação sobre faturas e faturação em conta.
-   **Taxa Horária** – as tarifas horárias para as horas que são lançadas nas contas de receitas e custos.


[!INCLUDE[footer-include](../includes/footer-banner.md)]