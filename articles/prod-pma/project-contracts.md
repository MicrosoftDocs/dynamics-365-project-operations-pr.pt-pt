---
title: Contratos de projeto
description: Este item fornece exemplos dos contratos de projeto que pode criar para vários tipos de projetos e fontes de financiamento, e como pode gerir contratos e faturar os clientes do projeto.
author: Yowelle
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: johnmichalak
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 14ff17bb070a44d8f3962e08f67d4c95bd8a26f9
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919660"
---
# <a name="project-contracts"></a>Contratos de projeto

[!include [banner](../includes/banner.md)]

Este item fornece exemplos dos contratos de projeto que pode criar para vários tipos de projetos e fontes de financiamento, e como pode gerir contratos e faturar os clientes do projeto.

O tipo de projeto que cria para um contrato de projeto determina o método que é utilizado para faturar os clientes do projeto. Pode alterar um contrato de projeto e o projeto relacionado, mas não pode alterar o tipo de projeto. 

Ao utilizar um contrato de projeto, pode faturar um ou mais projetos ao mesmo tempo. O contrato de projeto também ajuda a garantir um procedimento de faturação consistente para cada subprojecto numa estrutura de projetos. 

Cada projeto que será faturado tem de estar associado a um contrato de projeto. As definições para um contrato de projeto aplicam-se a todos os projetos e subprojetos associados a esse contrato de projeto. 

Um contrato de projeto pode especificar uma ou mais fontes de financiamento. Portanto, pode dividir a faturação entre vários financiadores, configurar limites de financiamento para as fontes de financiamento não serem faturadas mais do que um montante especificado e configurar regras de financiamento para cobrar gastos.

## <a name="funding-for-project-contracts"></a>Financiamento para contratos de projeto
Alguns contratos de projeto especificam que várias partes partilham a responsabilidade de financiamento dos custos de projeto. Seguem-se alguns exemplos:

-   Um grande cliente com múltiplas divisões solicita que o financiamento de um projeto seja dividido por divisão.
-   A sua empresa partilha os custos de um grande projeto com uma organização externa.
-   Um projeto rodoviário é cofinanciado por dois municípios.
-   Um projeto de ponte é financiado por uma subvenção do governo e uma empresa privada.

No Dynamics 365 Finance, pode dividir a faturação de uma única transação ou de um projeto completo entre vários clientes, bolsas ou organizações. 

Nos projetos com múltiplos financiadores, todas as partes que contribuem para o financiamento de um projeto de financiamento avançado são chamadas fontes de financiamento. Depois de um cliente, organização ou subvenção ser definido como fonte de financiamento, pode ser atribuído a uma ou mais regras de financiamento. As regras de financiamento contêm os critérios que determinam a forma como os encargos são atribuídos às várias fontes de financiamento para um projeto. 

Uma vez que os itens armazenados, como os que aparecem nas requisições de compra e nas notas de encomenda, não podem ser divididos, o montante do custo não pode ser dividido entre várias fontes de financiamento no momento da distribuição. Por conseguinte, o valor da fonte de financiamento mantém-se em 0 (zero) até a saída de stock ser lançada. Quando a saída de stock é lançada, o montante do custo é distribuído de acordo com as regras de distribuição da conta para o projeto.

Seguem-se alguns passos que pode dar para facilitar a divisão da faturação entre várias fontes de financiamento:

-   Especifique que todas as transações introduzidas para um projeto utilizam a mesma moeda de venda que o contrato de projeto.
-   Configure limites de financiamento para uma fonte de financiamento não ser faturada mais do que um montante especificado para um projeto.
-   Configure as regras de financiamento e os limites de financiamento para cada trabalhador, item, categoria, grupo de categorias e tipo de transação (ou para todos os tipos de transações).
-   Selecione as datas de início e fim opcionais para definir o período em que cada regra de financiamento é válida.
-   Especifique a percentagem pela qual cada fonte de financiamento é responsável.
-   Especifique qual a fonte de financiamento responsável pela arredondamento das diferenças que são causadas pelos cálculos da alocação de financiamento.
-   Configure regras que determinem como os custos do projeto são faturados aos clientes externos e cobrados às organizações internas.
-   Registe as transações numa conta de financiamento retido até poder ser obtido financiamento adicional ou até decidir suportar os custos internamente.

Para determinar o grupo fiscal a associar a uma transação, é procurada no projeto uma atribuição de grupo fiscal. Se não tiver sido feita nenhuma atribuição de grupos fiscais a nível do projeto, é procurado o contrato de projeto.

### <a name="example-multiple-funding-sources-simple"></a>Exemplo: Múltiplas fontes de financiamento (simples)

O quadro seguinte fornece cenários para gerir a alocação de financiamento entre múltiplas fontes de financiamento. Estes cenários baseiam-se nos seguintes pressupostos:

-   As definições prioritárias são tidas em conta na alocação de fundos antes de serem aplicados outros critérios de regras de financiamento.
-   Não foi especificado nenhum intervalo de datas para definir o período d durante o qual a regra de financiamento é válida.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Cenário</strong></td>
<td><strong>Fonte de financiamento</strong></td>
<td><strong>Percentagem de alocação</strong></td>
<td><strong>Prioridade da alocação</strong></td>
</tr>
<tr class="even">
<td>Pretende alocar custos a uma fonte de financiamento até os seus fundos serem esgotados, alocar custos a uma segunda fonte de financiamento até os seus fundos serem esgotados e, finalmente, alocar os custos restantes a uma terceira fonte de financiamento.</td>
<td><ul>
<li>Fonte de financiamento 1</li>
<li>Fonte de financiamento 2</li>
<li>Fonte de financiamento 3</li>
</ul></td>
<td><ul>
<li>100%</li>
<li>100%</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
<li>3</li>
</ul></td>
</tr>
<tr class="odd">
<td>Pretende alocar 75% dos custos a uma fonte de financiamento e 25% a uma segunda fonte de financiamento. Quando qualquer uma dessas fontes de financiamento se esgotar, quer pagar os custos restantes de uma terceira fonte de financiamento.</td>
<td><ul>
<li>Fonte de financiamento 1</li>
<li>Fonte de financiamento 2</li>
<li>Fonte de financiamento 3</li>
</ul></td>
<td><ul>
<li>75%</li>
<li>25%</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
<tr class="even">
<td>Pretende alocar 75% dos custos a uma fonte de financiamento e 25% a uma segunda fonte de financiamento. Quando qualquer uma dessas fontes de financiamento se esgotar, quer dividir os custos restantes entre uma terceira fonte de financiamento e uma quarta fonte de financiamento.</td>
<td><ul>
<li>Fonte de financiamento 1</li>
<li>Fonte de financiamento 2</li>
<li>Fonte de financiamento 3</li>
<li>Fonte de financiamento 4</li>
</ul></td>
<td><ul>
<li>75%</li>
<li>25%</li>
<li>50%</li>
<li>50%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
<li>2</li>
</ul></td>
</tr>
<tr class="odd">
<td>Pretende alocar os primeiros 25% dos custos a uma fonte de financiamento e o restante a uma segunda fonte de financiamento.</td>
<td><ul>
<li>Fonte de financiamento 1</li>
<li>Fonte de financiamento 2</li>
</ul></td>
<td><ul>
<li>25%</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a>Exemplo: Múltiplas fontes de financiamento (complexo)

Tem três fontes de financiamento que pretende utilizar pela seguinte ordem:

1.  Utilize a fonte de financiamento 2 e a fonte de financiamento 3 equitativamente até a fonte de financiamento 2 estar esgotada.
2.  Continue a utilizar a fonte de financiamento 3 até estar esgotada.
3.  Utilize a fonte de financiamento 1 depois de esgotada a fonte de financiamento 3.

Para atingir este objetivo, tem de efetuar o seguinte:

-   Configure limites de financiamento para a fonte de financiamento 2 e a fonte de financiamento 3, para os respetivos montantes.
-   Crie as seguintes regras de financiamento:
    -   Regra 1 (Prioridade 1): Alocar 50% das transações à fonte de financiamento 2 e 50% à fonte de financiamento 3.
    -   Regra 2 (Prioridade 2): Alocar 100% das transações à fonte de financiamento 3.
    -   Regra 3 (Prioridade 3): Alocar 100% das transações à fonte de financiamento 1.

Esta configuração funciona porque as transações são comparadas com as regras e os limites para determinar se alguma delas se aplica à transação. Se não forem aplicáveis regras ou limites específicos à transação, aplica-se a regra Todas as transações. A regra Todas as transações corresponde a todas as transações. 

Se for encontrada uma regra que corresponda a uma transação, a percentagem que foi alocada nessa regra é aplicada primeiro, mas só depois de verificadas as correspondências tendo em conta quaisquer limites que tenham sido configurados. Se tiver sido atingido um limite e os fundos de uma fonte de financiamento estiverem esgotados, a regra de financiamento que está associada ao limite de financiamento é ignorada, e o programa verifica a regra seguinte aplicável. 

Em alguns casos, só parte de uma transação pode ser alocada de acordo com uma regra. Isto pode acontecer porque é atingido um limite quando a transação é alocada. Neste caso, só é alocado um determinado montante de acordo com essa regra, como 50% a cada fonte de financiamento. É o caso da regra 1, descrita anteriormente nesta secção. O restante é alocado de acordo com a regra seguinte na sequência. 

A tabela seguinte examina este cenário em maior detalhe.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Foco</strong></td>
<td><strong>Detalhes</strong></td>
</tr>
<tr class="even">
<td>Regras de financiamento</td>
<td><ul>
<li>Regra 1 (Prioridade 1): Todas as transações. Alocar fonte de financiamento 2 a 50% e a fonte de financiamento 3 a 50%.</li>
<li>Regra 2 (Prioridade 2): Todas as transações. Alocar fonte de financiamento 3 a 100%.</li>
<li>Regra 3 (Prioridade 2): Todas as transações. Alocar fonte de financiamento 1 a 100%.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Limites de financiamento</td>
<td><ul>
<li>Limite da fonte de financiamento 1 = 10.000,00</li>
<li>Limite da fonte de financiamento 2 = 500,00</li>
<li>Limite da fonte de financiamento 3 = 750,00</li>
</ul></td>
</tr>
<tr class="even">
<td>Transação 1</td>
<td><strong>Montante da transação:</strong> 100,00<strong>Financiamento:</strong> A transação é paga apenas de acordo com a regra 1, porque a transação é paga totalmente após a aplicação da regra 1. A transação é financiada igualmente entre a fonte de financiamento 2 e a fonte de financiamento 3.
<ul>
<li>Fonte de financiamento 2: 50,00</li>
<li>Fonte de financiamento 3: 50,00</li>
</ul></td>
</tr>
<tr class="odd">
<td>Transação 2</td>
<td><strong>Montante da transação:</strong> 5.000,00<strong>Financiamento:</strong> A transação é paga de acordo com as três regras. <strong>Regra 1</strong>
<ul>
<li>Fonte de financiamento 2: 450,00</li>
<li>Fonte de financiamento 3: 450,00</li>
</ul>
<strong>Regra 2</strong>
<ul>
<li>Fonte de financiamento 3: 250,00 (= 750,00 – 50,00 – 450,00)</li>
</ul>
<strong>Regra 3</strong>
<ul>
<li>Fonte de financiamento 1: 3.850,00 (= 5.000,00 – 450,00 – 450,00 – 250,00)</li>
</ul></td>
</tr>
<tr class="even">
<td>Total de fundos distribuídos por cada fonte de financiamento</td>
<td><ul>
<li>Fonte de financiamento 1: 3.850,00</li>
<li>Fonte de financiamento 2: 500,00</li>
<li>Fonte de financiamento 3: 750,00</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a>Regras de faturação
Quando negoceia um contrato de projeto com um cliente, define como e quando pode faturar o cliente pelo trabalho num projeto. Depois de configurar o contrato de projeto e o projeto, pode configurar regras de faturação para o projeto. As regras de faturação baseiam-se nos termos do projeto especificados no contrato do projeto. As regras de faturação que pode criar dependem dos termos do contrato de projeto e do tipo de projeto, como o Tempo e material ou Preço fixo, que associa à regra de faturação. Pode criar mais de uma regra de faturação para um contrato de projeto. Também pode atribuir uma regra de faturação a vários projetos que estão associados ao mesmo contrato de projeto e têm termos de faturação semelhantes. 

Pode configurar os seguintes tipos de regras de faturação:

-   **Unidade de entrega** – Faturar um cliente quando conclui uma unidade de entrega. Defina as unidades de entrega no contrato.
-   **Progresso** – Faturar um cliente quando conclui uma percentagem especificada do projeto. Pode configurar uma regra de faturação para calcular automaticamente a percentagem de trabalho concluído, ou pode calcular manualmente a percentagem de trabalho concluído e o montante a faturar o cliente.
-   **Marco** – Faturar um cliente pelo montante total de um marco de projeto quando o marco é atingido.
-   **Tarifa** – Faturar um cliente pelos seus serviços, acrescido de uma tarifa de gestão, que normalmente é uma percentagem do custo dos serviços.
-   **Tempo e material** – Faturar um cliente pelo valor do tempo e dos materiais que são utilizados num projeto.

Para todos os tipos de regras de faturação, pode especificar uma percentagem de retenção que é deduzida das faturas do cliente até um projeto atingir uma fase acordada. A percentagem de retenção de pagamentos é especificada no contrato de projeto. O montante é calculado e é subtraído do valor total das linhas numa fatura do cliente. 

Para as regras de faturação **Tempo e material** e **Progresso**, pode atribuir categorias faturáveis. As categorias faturáveis indicam as transações que devem ser incluídas nas faturas dos clientes. 

Quando estiver pronto para faturar o cliente, o montante da faturação do projeto é calculado com base nas regras de faturação e é gerada uma proposta de fatura do projeto. 

As secções seguintes fornecem exemplos que mostram como configurar e gerir as regras de faturação para um projeto.

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a>Exemplo: Criar uma regra de faturação baseada no número de unidades entregues

A sua organização celebra um contrato para fornecer um total de cinco sessões de formação aos colaboradores de um cliente por um custo de 10.000 por sessão de formação. Fature o cliente após cada sessão de formação. 

Quando configurar as regras de faturação do contrato, utilize os seguintes valores:

-   A unidade de entrega é uma sessão de formação.
-   O preço unitário é de 10.000 por sessão de formação.
-   O número total de unidades é de cinco sessões de formação.

Depois de concluir uma sessão de formação, pode criar uma fatura de 10.000, para a primeira unidade que foi entregue, e enviar a fatura ao cliente.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a>Exemplo: Criar uma regra de faturação baseada numa percentagem especificada de conclusão do projeto (cálculo manual)

A sua organização, uma empresa de consultoria de software, celebra um acordo com um cliente para desenvolver parte de um produto que o cliente está a desenvolver. A sua organização concorda entregar o código de software durante um período de seis meses. O cliente concorda pagar à sua organização um total de 100.000 pelo trabalho. Crie uma regra de faturação para faturar o cliente baseado na percentagem de trabalho que é concluída no projeto, conforme especificado no contrato.

-   No final do primeiro mês, encontra-se com o cliente para determinar a percentagem de trabalho concluído. Depois , com o o cliente rever o projeto, decide que o projeto está 15% concluído.
-   Crie uma fatura para 15.000 (15% de 100.000) e envie-a ao cliente.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a>Exemplo: Criar uma regra de faturação baseada numa percentagem especificada de conclusão do projeto (cálculo automático)

A sua organização, uma empresa de desenvolvimento de software, concorda desenvolver um pacote de cálculo das folhas de pagamento para um cliente por 30.000. O cliente concorda pagar à sua organização com base na percentagem de trabalho concluída. Estima que os custos do projeto são de 20.000. O contrato de projeto especifica as categorias de trabalho que utiliza no processo de faturação. Configura regras de faturação que calculam automaticamente os montantes da fatura para a percentagem de trabalho que está concluída para cada categoria. Crie um orçamento para cada categoria:

-   **Desenvolvimento** – Custo de 15.000 e receitas de 20.000
-   **Instalação** – Custo de 5.000 e receitas de 10.000

Quando cria uma fatura do cliente pela primeira vez, o montante da fatura é calculado automaticamente com base nas seguintes informações:

-   Após um mês, o trabalhador do projeto submete uma folha de horas para o projeto. O custo das horas do trabalhador é de 5.000 para o desenvolvimento e 1.000 para a instalação. O trabalho de desenvolvimento está 33% concluído (5.000 custos reais/15.000 custos orçamentais) e o trabalho de instalação está 20% concluído (1.000 custos reais/5.000 custos orçamentais).
-   O montante da fatura de 8.667 é calculado automaticamente (33% de 20.000 + 20% de 10.000).
-   Crie uma fatura para 8.667 e envie-a ao cliente.

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a>Exemplo: Criar uma regra de faturação baseada em marcos acordados

A sua organização, uma empresa de consultoria de gestão, concorda em realizar pesquisas de mercado para um produto de consumo que o cliente planeia vender. O cliente concorda utilizar os seus serviços por um período de três meses, a partir de março, e concorda em pagar à sua organização 50.000. O projeto tem três marcos:

-   Marco 1: Recolher dados de consumidores – 31 de março
-   Marco 2: Analisar os dados dos consumidores – 30 de abril
-   Marco 3: Apresentar uma proposta de viabilidade do produto – 31 de maio

O cliente concorda pagar à sua organização 10.000 pelo primeiro marco, 20.000 pelo segundo marco e 20.000 pelo terceiro marco. 

Ao configurar o contrato de projeto, concorda faturar o cliente com base no marco que foi concluído. A configuração da regra de faturação inclui os seguintes passos:

-   Definir os marcos do projeto.
-   Definir o montante a faturar o cliente quando cada marco estiver concluído.

Quando o primeiro marco estiver concluído a 31 de março, marque o marco como concluído e, em seguida, crie uma fatura de 10.000 e envie-a para o cliente. Não pode criar uma fatura para um marco enquanto não tiver marcado o marco como concluído.

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a>Exemplo: Criar uma regra de faturação baseada nos serviços, acrescida de uma taxa de gestão

A sua organização, uma empresa de consultoria de gestão, concorda fazer um estudo de mercado para avaliar a viabilidade de um produto que o cliente, uma empresa de retalho, está a desenvolver. Os termos do acordo especificam que irá fornecer os serviços dos seus três principais consultores de gestão, que conduzirão o estudo em função do tempo e dos materiais. O cliente concorda pagar 100 por hora, acrescido de uma taxa de gestão de 10% para as horas de consultoria que são cobradas ao projeto. 

Quando configura o contrato de projeto, crie uma regra de faturação para adicionar uma taxa de gestão de 10% às horas de consultoria que são cobradas ao projeto. 

Quando cria uma fatura para o cliente, o cliente é faturado uma taxa de gestão de 10%, acrescida do custo das horas de consultoria. Por exemplo, se os três consultores trabalharam um total de 200 horas no projeto, é criada uma fatura de 22.000 com base no seguinte cálculo:

-   200 horas a 100 por hora = 20.000
-   10% de taxa de gestão = 2.000
-   Montante total da fatura = 22.000

Se as tarifas forem tributáveis para um cliente, e selecionar um grupo de impostos sobre vendas no contrato do projeto, o grupo de impostos sobre vendas é automaticamente inscrito numa regra de faturação de tarifas.

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a>Exemplo: Criar uma regra de faturação para o valor de tempo e materiais

A sua organização, uma empresa de consultoria de software, concorda fornecer cinco consultores técnicos para trabalharem num projeto de desenvolvimento de software para um cliente durante os próximos seis meses. O cliente concorda pagar 150 por cada hora de consultoria, acrescido do custo dos materiais de escritório. A sua organização envia uma fatura ao cliente no final de cada mês. 

Ao configurar o contrato de projeto, concorda faturar o cliente todos os meses pelo tempo e material no projeto. Crie uma regra de faturação que inclua as seguintes informações:

-   O período de contrato é de seis meses.
-   O tempo de consultoria é calculado a uma tarifa de 150 por hora.
-   Os materiais de escritório são faturados ao custo, e o custo total do projeto não pode exceder 10.000.
-   Crie uma fatura do cliente no final de cada mês de calendário durante o projeto.

Durante o primeiro mês, é registo um total de 800 horas pelos consultores do projeto. O custo dos materiais de escritório que são cobrados ao projeto é de 2.000. Assim, no final do mês, cria uma fatura pelos 122.000, que é calculada como 800 horas a 150 por hora, mais 2.000 para material de escritório.





[!INCLUDE[footer-include](../includes/footer-banner.md)]