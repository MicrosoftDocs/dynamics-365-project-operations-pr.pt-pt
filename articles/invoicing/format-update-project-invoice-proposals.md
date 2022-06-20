---
title: Gerir propostas de fatura do projeto
description: Este artigo fornece detalhes sobre o processamento de faturas voltadas para clientes com o Project Operations para cenários baseados em recursos/não abastecidos.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: ef6003499f1372a51d7d1606db6f5bf9722a369d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927848"
---
# <a name="manage-project-invoice-proposals"></a>Gerir propostas de fatura do projeto

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

As propostas de fatura do projeto podem ser processadas pelo seu departamento de faturação quando estiverem reunidas as duas condições seguintes:

  - O gestor do Projeto confirma a fatura proforma em Microsoft Dataverse.
  - Todas as transações de vendas não faturadas de tempo e material que estão incluídas na fatura proforma são publicadas através do diário Dynamics 365 **Integração do Project Operations**.

Utilize os passos seguintes para concluir uma proposta de fatura do projeto no Dynamics 365 Finance.

1. Reveja a informação de faturação para transações de tempo e material e publique o diário **Integração do Project Operations**.
2. Rever informações de faturação para marcos de faturação de preço fixo.
3. Rever e formatar uma proposta de fatura do projeto.
4. Publicar e Imprimir faturas do projeto.

## <a name="manage-billing-information-in-the-project-operations-integration-journal"></a>Gerir informação de faturação no diário Integração do Project Operations

Os projetos criados em Dataverse são revistos e publicados em Finanças pelo contabilista do Projeto. Para mais informações sobre o trabalho com o diário de Integração, ver [Diário de Integração no Project Operations](../project-accounting/project-operations-integration-journal.md).

Os valores reais dos custos e vendas não faturadas são adicionados ao diário de integração como linhas separadas:

  - O preço de custo unitário e o valor do custo no custo real da transação de custos reais do projeto em Dataverse.
  - O preço de venda unitário e o valor de venda de transações de vendas não faturadas assume a transação real de vendas não faturadas do projeto no Dataverse.

### <a name="billing-sales-tax"></a>Imposto sobre as vendas de faturação

O cálculo do imposto sobre as vendas para faturação é determinado pelo **grupo de impostos sobre vendas de faturação** e pela combinação de campo do **grupo de impostos sobre vendas de produtos de faturação** num registo de vendas não faturado na linha de diário de **integração do Project Operations**. O sistema predefine estes valores de campo com base em definições no separador **Finanças** na página de **parâmetros de gestão e contabilidade do Projeto**.

- **O método do grupo de tributação das vendas** determina a lógica de incumprimento do grupo de imposto sobre as vendas:
  
  - **Projeto**: Irá sempre assumir o grupo de imposto de venda do projeto. Pode rever ou alterar o grupo de imposto de faturação padrão num projeto, selecionando **Mostrar contabilidade padrão** na página **Todos os projetos**.
  - **Contrato do projeto**: Irá sempre assumir o grupo de imposto de venda do contrato do projeto. Pode rever ou alterar o grupo de imposto de faturação padrão num contrato de projeto, selecionando **Mostrar contabilidade padrão** na página **Contratos de projetos**.
  - **Cliente**: Irá sempre assumir o grupo de imposto de venda do cliente.
  - **Pesquisa**: Irá procurar em todas as entidades acima e selecionar o primeiro valor disponível. A pesquisa começa com a entidade do **Projeto**, depois com a entidade do **contrato do Projeto** e, finalmente, com a entidade **cliente**.

- **O método do grupo de tributação de item de vendas** determina a lógica de predefinição do grupo de imposto sobre os itens de vendas:
  
  - Por tempo, despesas e tipos de transações de taxas, o grupo de imposto de venda de artigos de faturação sempre por defeito da entidade da categoria **Projeto**.
  - Para os tipos de transações materiais, o grupo de imposto de venda de produtos de faturação apresenta predefinição com base no método do **grupo de imposto de venda de rubricas de produtos** estabelecido nos **parâmetros de gestão e contabilidade do Projeto**. O número do item predefine o grupo de imposto de venda de produtos da entidade de **produto Liberado**. A categoria predefine o grupo de imposto de venda de produtos da entidade de **categoria de projeto**.

### <a name="financial-dimensions"></a>Dimensões financeiras

As dimensões financeiras dos registos de vendas não faturados no diário **Integração do Project Operations** assume a entidade do **Projeto**. As dimensões financeiras podem ser revistas e ajustadas selecionando **Valores de Distribuição**. Se precisar de alterar as dimensões financeiras do registo de vendas não faturado após a publicação do diário Integração, mas antes de a fatura Proforma ser confirmada, vá a **Todos os projetos** > **Gerir** > **Transações publicadas**, selecione a transação e, em seguida, selecione **Processo** > **Ajustar contabilidade**.

### <a name="exchange-rates"></a>Taxas de câmbio

A moeda de transação não faturada em Dataverse é utilizada como moeda de transação em Finanças e convertida em moeda contabilística da empresa utilizando taxas de câmbio definidas em Finanças.


## <a name="manage-the-financial-attributes-of-billing-milestones"></a>Gerir os atributos financeiros dos marcos da faturação 

As linhas de contrato de projeto utilizando o método de faturação de preço fixo são faturadas através de [marcos de preço fixo](../sales/invoice-schedules-contract-line.md#create-a-fixed-price-invoice-schedule-for-a-contract-line). O contabilista do Projeto pode rever os marcos da faturação nas Finanças indo a **gestão e contabilidade de projeto** > **Todos os projetos** > **Gerir** > **transações em conta**.

### <a name="billing-sales-tax"></a>Imposto sobre as vendas de faturação

Os valores do **grupo de tributação de vendas** e do **grupo de imposto sobre as vendas de produto** predefinem as definições quando um novo marco de faturação é criado em Dataverse. O sistema predefine os valores para estes campos com base em definições no separador **Financeiro** na página de **parâmetros de gestão e contabilidade do Projeto**.

- O **método do grupo de tributação das vendas** determina a lógica predefinida do **grupo de imposto sobre as vendas**:

    - **Projeto** Irá sempre assumir o grupo de imposto de venda do projeto. Pode rever ou alterar o grupo de imposto de vendas padrão num projeto, selecionando **Mostrar contabilidade padrão** na página **Todos os projetos**.
    - **Contrato do projeto** irá sempre assumir o grupo de imposto de venda do contrato do projeto. Pode rever ou alterar o grupo de imposto de faturação padrão num contrato de projeto, selecionando **Mostrar contabilidade padrão** na página **Contratos de projetos**.
    - **Cliente** irá sempre assumir o grupo de imposto de venda do cliente.
    - **Pesquisa** irá procurar em todas as entidades nesta lista e selecionar o primeiro valor disponível. A pesquisa começa com a entidade do **Projeto**, depois com a entidade do **contrato do Projeto** e, depois, com a entidade **cliente**.

- O **grupo de imposto sobre as vendas de pontos de venda de preço fixo** é utilizado como o valor predefinido no campo do **grupo de imposto de venda de artigos** para o marco da faturação. O contabilista pode rever e modificar este valor na página de **transações em conta**. O sistema utiliza o valor da transação em conta ao criar uma linha de proposta de fatura do projeto.
 

### <a name="financial-dimensions"></a>Dimensões financeiras

As dimensões financeiras padrão para o marco da faturação de preço fixo são definidas nas linhas de contrato do Projeto. Vá aos **contratos do Projeto** > **Mostrar contabilidade padrão** e no separador **Linhas de contrato**, selecione **linha de contrato de preço** e, em seguida, defina os valores de dimensão financeira que pretende usar como padrão.

O contabilista do Projeto pode editar a informação sobre o imposto sobre as vendas e as dimensões financeiras sobre os marcos da fatura até que a proposta de fatura do Projeto seja criada.


## <a name="create-project-invoice-proposals"></a>Criar propostas de fatura do projeto

As propostas de fatura do projeto podem ser revistas no módulo de **gestão e contabilidade do projeto** indo a **Faturas de projeto** > **Propostas de fatura de projeto**.

O cabeçalho da proposta de fatura do Projeto é criado nas Finanças quando a fatura Proforma é confirmada em Dataverse. Para uma reconciliação mais fácil, o sistema define o número da proposta de fatura do Projeto nas Finanças para o mesmo número que o ID da fatura Proforma em Dataverse. Como as faturas proforma não são necessariamente confirmadas na mesma ordem em que são criadas, a sequência de números de proposta de fatura do Projeto em Finanças deve permitir alterações para números cada vez mais baixos. Configure as sequências de números utilizando os seguintes passos:

1. Em Finanças, aceda às **Administração de organização** > **Sequências de números** > **Sequências de números**.
2. No filtro **Área**, selecione **Projetos**.
3. No filtro **Referência**, selecione **Proposta de Fatura**.
4. Utilize o campo **Empresa** para filtrar cada entidade jurídica com a integração de Project Operations Dataverse habilitada.
5. Abra os **detalhes da sequência de números** e no separador **geral**:

    - **Permitir alterações no utilizador: Para um número mais baixo** = **Sim**
    - **Permitir alterações no utilizador: Para um número mais alto** = **Sim**

As linhas de proposta de fatura do projeto são adicionadas pelo sistema utilizando o processo periódico **Importar tabela de teste** (**Gestão de projetos e contabilidade** > **Periódico** > **Integração do Project Operations** > **Importar da tabela de teste**). Este processo pode ser executado manualmente ou utilizando um agendamento periódico. O sistema não vai adicionar linhas ao documento de proposta de fatura até que todas as linhas estejam prontas para serem faturadas. As transações de tempo e material só estão prontas para serem faturadas quando forem publicadas através do diário **Integração do Project Operations**.

## <a name="format-and-print-invoice-proposals"></a>Formatar e imprimir propostas de fatura

O contabilista do Projeto pode personalizar uma impressão de fatura do projeto utilizando a página de **Formatar proposta de fatura** e imprimir capacidades de gestão.

### <a name="format-invoice-proposals"></a>Formatar propostas de fatura

A página de **formatar propostas de fatura** permite que as transações de agrupamento personalizados apareçam na fatura do projeto do cliente.

1. Na página de **proposta de fatura do projeto**, selecione **Imprimir** > **Proposta de fatura do formato**.
2. Selecione **Novo** para criar um novo agrupamento para a impressão de fatura do Projeto.
3. No campo **Detalhe/Resumo** selecione opções para este agrupamento:

    - Selecione **Detalhes** para imprimir os detalhes da transação da fatura do cliente.
    - Selecione **Resumo** para imprimir o resumo da transação da fatura do cliente.

> [!NOTE]
> A seleção no campo **Detalhe/Resumo** na página de **proposta de fatura formato** substitui a opção selecionada no campo **formato de fatura** da página **propostas de Fatura** para imprimir uma fatura detalhada ou uma fatura resumida.

- Selecione as linhas de transação para incluir nesta secção o separador de **transações disponíveis** e selecione **Incluir transações** para as mover para o separador de **transações selecionadas**.
- Selecione **Mover para cima** e **Mover para baixo** para alterar a ordem das secções.
- Selecione **Imprimir a pré-visualização** para pré-visualizar a fatura formatada.

### <a name="print-management"></a>Gestão de impressão

A gestão de impressão utiliza diferentes ficheiros de relatório para imprimir, especificar destinos e personalizar texto de rodapé para a fatura. A gestão de impressão pode ser configurada ao nível do módulo, no entanto estas definições podem ser ultrapassadas para uma proposta específica de cliente, contrato ou fatura. Para aceder a esta função na página de **proposta de fatura do Projeto**, selecione **Imprimir** > **gestão de impressão**.

A configuração da gestão da impressão é apresentada como uma vista de árvore, onde cada nível de nó exibe os documentos disponíveis para ajustar. Pode atribuir impressões personalizadas no módulo, cliente, contrato ou nível de documento de proposta de fatura. Para modificar a impressão original do documento, expanda o nó desejado e selecione **item Original**. No campo **Formato de relatório**, selecione o formato de relatório a utilizar para impressão. Pode utilizar formatos de relatório personalizados utilizando o [quadro de Gestão de Documentos empresariais](/dynamics365/fin-ops-core/dev-itpro/analytics/er-business-document-management).

## <a name="post-invoice-proposals"></a>Publicar propostas de fatura

Depois de a fatura ter sido revista e editada, e as linhas de proposta de fatura serem satisfatórias, verifique os totais da fatura e o imposto sobre as vendas. No grupo **Detalhes**, selecione **Totais** e, em seguida, selecione **Publicar** para publicar a fatura.

Para ver a fatura antes de publicar, limpe a caixa de verificação de **Publicação**. **Pró forma** será impresso na fatura para significar que é uma fatura de amostra. Para imprimir a fatura, selecione a caixa de verificação **Imprimir fatura**.

Além da página de **propostas de fatura**, as propostas de fatura podem também ser publicadas através da execução do trabalho periódico, **publicar propostas de fatura**. Para encontrar este trabalho, vá à **gestão de projetos e contabilidade** > **Periódico** > **Faturas do projeto** > **Publicar propostas de fatura**.

Esta página mostra todas as propostas de fatura que estão prontas para publicar. Pode agendar propostas de fatura de publicação selecionando **Lote**. Defina o **parâmetro de processamento do Lote** para **Sim** e defina a periodicidade do processamento do lote selecionando **Periodicidade**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
