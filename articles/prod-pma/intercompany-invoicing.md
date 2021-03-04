---
title: Faturação entre empresas
description: Este artigo fornece informações e exemplos sobre a faturação entre empresas para projetos.
author: Yowelle
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerInterCompany
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 94153
ms.assetid: 33e98da7-01c1-4369-923d-aa1c8326cb80
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4604708dbd7c835c8df1cf48f67e645952f49774
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082430"
---
# <a name="intercompany-invoicing"></a>Faturação entre empresas

[!include [banner](../includes/banner.md)]

Este artigo fornece informações e exemplos sobre a faturação entre empresas para projetos.

A sua organização pode ter múltiplas divisões, subsidiárias e outras entidades jurídicas que transferem produtos e serviços entre si para projetos. A entidade jurídica que presta o serviço ou produto é denominada *entidade jurídica prestadora* e a entidade jurídica que recebe o serviço ou produto é denominada *entidade jurídica tomadora*. 

A ilustração seguinte mostra um cenário típico em que duas entidades jurídicas, SI FR (entidade jurídica tomadora) e a SI USA (entidade jurídica prestadora) partilham recursos para entregar um projeto ao cliente A. Para este cenário, a SI FR é contratada para entregar o trabalho ao cliente A. 

[![Exemplo de faturação entre empresas](./media/interco.invoicing-01.jpg)](./media/interco.invoicing-01.jpg) 

O objetivo é tornar o controlo de custos, o reconhecimento de receitas, os impostos e o preço de transferência para transações de projetos entre empresas mais flexível e poderoso. Além disso, são fornecidas as seguintes funcionalidades:

-   Crie faturas de clientes para um projeto numa entidade jurídica tomadora através de folhas de horas, despesas e faturas de fornecedores entre empresas numa entidade jurídica prestadora.
-   Suporte de cálculos de impostos e custos indiretos.
-   Diferir o reconhecimento de receitas numa entidade jurídica prestadora e quando uma entidade jurídica tomadora deve reconhecer o custo.
-   Acumule as receitas do trabalho em curso (WIP) na entidade jurídica prestadora.
-   Defina os preços de transferência que podem basear-se em vários modelos de preços. Seguem-se alguns exemplos:
    -   **Quantidade** : a quantidade que introduz no campo **Preços** é o custo real por quantidade ou unidade.
    -   **Montante de encargos** : o preço/custo por transação, acrescido do montante dos encargos que introduz no campo **Preços**.
    -   **Percentagem de encargos** : o preço de transferência é o preço/custo por transação multiplicado pela percentagem de encargos que introduz no campo **Preços**.
    -   **Percentagem do preço de venda** : a percentagem do preço de venda que é transferido para a entidade jurídica prestadora.
    -   **Montante abaixo do preço de venda** : o montante que a entidade jurídica tomadora retém dos preços de venda antes de os transferir para a entidade jurídica prestadora.
    -   **Rácio de contribuição** : o número que introduzir no campo **Preços** é a relação de contribuição ratio, que é expresso como uma percentagem do preço de venda.

## <a name="example-1-set-up-parameters-for-intercompany-invoicing"></a>Exemplo 1: Configurar parâmetros para a faturação entre empresas
Neste exemplo, a USSI é uma entidade jurídica prestadora e os seus recursos estão a comunicar tempo a atribuir à entidade jurídica tomadora, a FRSI, que é proprietária do contrato com o cliente final. As horas e as despesas que os colaboradores da USSI comunicam podem ser incluídas na fatura do projeto que a FRSI gera. Além disso, existe uma terceira origem de transações que pode ter origem na entidade jurídica prestadora (USSI neste exemplo) quando presta serviços de fornecedores partilhados a subsidiárias (como a FRSI) e, em seguida, transfere esses custos para os projetos dentro dessas subsidiárias. Todos os documentos de faturação correspondentes e cálculos fiscais são preenchidos pelo Finance. 

Para este exemplo, a FRSI tem de ser um cliente na entidade jurídica USSI, e esta tem de ser um fornecedor na entidade jurídica FRSI. Em seguida, pode configurar uma relação entre empresas entre as duas entidades jurídicas. O seguinte procedimento mostra como configurar os parâmetros para ambas as entidades jurídicas poderem participar na faturação entre empresas.

1. Configure a FRSI como um cliente na entidade jurídica USSI e crie a USSI como fornecedor na entidade jurídica FRSI. Existem três pontos de entrada para os passos necessários para esta tarefa.

   | Passo |                                                       Ponto de entrada                                                        |                                                                                                                                                                                               Descrição                                                                                                                                                                                               |
   |------|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |  A   | Na USSI, clique em <strong>Contas a receber</strong> &gt; <strong>Clientes</strong> &gt; <strong>Todos os clientes</strong>. |                                                                                                                                                                  Crie um novo registo de cliente para a FRSI e selecione o grupo de clientes.                                                                                                                                                                  |
   |  N   |    Na FRSI, clique em <strong>Contas a pagar</strong> &gt; <strong>Fornecedores</strong> &gt; <strong>Todos os fornecedores</strong>.     |                                                                                                                                                                    Crie um novo registo de fornecedor para a USSI e selecione o grupo de fornecedores.                                                                                                                                                                    |
   |  C   |                                  Na FRSI, abra o registo de fornecedor que acabou de criar.                                  | No Painel de Ação, no separador <strong>Geral</strong>, no grupo <strong>Configurar</strong>, clique em <strong>Entre empresas</strong>. Na página <strong>Entre empresas</strong>, no separador <strong>Relação comercial</strong>, defina o controlo de deslize <strong>Ativo</strong> como <strong>Sim</strong>. No campo <strong>Empresa do cliente</strong>, selecione o registo de cliente que criou no passo A. |


2. Clique em **Gestão de projetos e contabilística** &gt; **Configurar** &gt; **Parâmetros de gestão de projetos e contabilística** e clique no separador **Entre empresas**. A forma como configura os parâmetros depende se é a entidade jurídica tomadora ou a entidade jurídica prestadora.
   -   Se for a entidade jurídica tomadora , selecione a categoria de compras que deve ser usada para fazer a correspondência com as faturas do fornecedor, que são geradas automaticamente.
   -   Se for a entidade jurídica prestadora, para cada entidade tomadora, selecione uma categoria de projeto predefinida para cada tipo de transação. As categorias de projeto são utilizadas para a configuração fiscal quando a categoria faturada nas transações entre empresas existe apenas na entidade jurídica tomadora. Pode optar por acumular as receitas para as transações entre empresas. Esta acumulação é feita quando as transações são lançadas e, depois, é invertida quando a fatura entre empresas é lançada.

3. Clique em **Gestão de projetos e contabilística** &gt; **Configurar** &gt; **Preços** &gt; **Preço de transferência**.
4. Selecione uma moeda, tipo de transação e modelo de preço de transferência. A moeda que é utilizada na fatura é a moeda que está configurada no registo de cliente para a entidade jurídica tomadora na entidade jurídica prestadora. A moeda é utilizada para fazer a correspondência com as entradas na tabela de preços de transferência.
5. Clique em **Razão Geral** &gt; **Configuração do lançamento** &gt; **Gestão contabilística entre empresas** e configure uma relação para a USSI e a FRSI.

## <a name="example-2-create-and-post-an-intercompany-timesheet"></a>Exemplo 2: Criar e lançar uma folha de horas entre empresas
A USSI, a entidade jurídica prestadora, tem de criar e lançar a folha de horas para um projeto da FRSI, a entidade jurídica tomadora. Existem dois pontos de entrada para os passos necessários para esta tarefa.

| Passo | Ponto de entrada                                                                       | Descrição                                                                                                                                                                                       |
|------|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Gestão de projetos e contabilística** &gt; **Folhas de horas** &gt; **Todas as folhas de horas** | Crie uma nova folha de horas. Na linha da folha de horas, no campo **Entidade jurídica** , selecione **FRSI**. No campo **ID de Projeto** , selecione o projeto na FRSI. Introduza as horas para cada dia da semana. |
| N    | Página **Folha de horas**                                                                | Depois da execução do fluxo de trabalho, lance a folha de horas e anote o número do voucher.                                                                                                               |

## <a name="example-3-create-and-post-an-intercompany-vendor-invoice"></a>Exemplo 3: Criar e lançar uma fatura de fornecedor entre empresas
A USSI, a entidade jurídica prestadora, tem de criar e lançar a fatura de fornecedor entre empresas para um projeto da FRSI, a entidade jurídica tomadora. Esta fatura de fornecedor representa a mão-de-obra subcontratada e as despesas realizadas por fornecedores que são pagos pela USSI. Existem dois pontos de entrada para os passos necessários para esta tarefa.

| Passo | Ponto de entrada                                                                                      | Descrição                                                                                                                                                                                                                                                                          |
|------|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Contas a pagar** &gt; **Faturas** &gt; **Faturas de fornecedor abertas** &gt; **Nova fatura de fornecedor** | Crie uma nova fatura de fornecedor e introduza os serviços que foram comprados em nome do projeto da FRSI.                                                                                                                                                                                  |
| N    | A página **Fatura de fornecedor**                                                                      | Introduza as linhas que representem os serviços subcontratados em nome da FRSI. No Separador Rápido **Detalhes da linha** , no separador **Projeto** para a linha de fatura, no campo **Empresa do projeto** , introduza **FRSI**. Introduza o projeto e a informação correspondente. Em seguida, lance a fatura do fornecedor. |

## <a name="example-4-create-and-post-the-intercompany-invoice"></a>Exemplo 4: Criar e lançar a fatura entre empresas
A USSI, a entidade jurídica prestadora, tem de criar e lançar a fatura entre empresas. Existem dois pontos de entrada para os passos necessários para esta tarefa.

| Passo | Ponto de entrada                                                                                             | Descrição                                                                                                                                      |
|------|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Gestão de projetos e contabilística** &gt; **Faturas do projeto** &gt; **Fatura do cliente entre empresas**  | Clique em **Novo** para abrir a página **Criar fatura entre empresas**.                                                                                  |
| N    | **Gestão de projetos e contabilística** &gt; **Faturas do projeto** &gt; **Faturas do cliente entre empresas** | Na página **Criar fatura entre empresas** , introduza a entidade jurídica, especifique a transação que deve ser incluída e clique em **Procurar**. |
| C    | **Gestão de projetos e contabilística** &gt; **Faturas do projeto** &gt; **Faturas do cliente entre empresas** | Selecione as transações a faturar ou clique em **Selecionar tudo** para faturar todas as transações na lista e, em seguida, clique em **OK**.                  |
| D    | A página **Fatura entre empresas**                                                                       | É mostrada a proposta de fatura do cliente entre empresas.                                                                                             |
| E    | A página **Fatura entre empresas**                                                                       | Clique em **Lançar**.                                                                                                                                  |

## <a name="example-5-post-the-vendor-invoice-and-invoice-the-customer"></a>Exemplo 5: Lançar a fatura do fornecedor e faturar o cliente
Quando a entidade jurídica de prestadora, a USSI, lança a fatura do cliente entre empresas, é criada uma fatura do fornecedor pendente correspondente na entidade jurídica prestadora, a FRSI. Após o lançamento desta fatura do fornecedor, a FRSI também fatura o cliente do projeto pelas horas que a USSI introduziu. Existem três pontos de entrada para os passos necessários para esta tarefa.

| Passo | Ponto de entrada                                                                                        | Descrição                                                                                                             |
|------|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| A    | **Contas a pagar** &gt; **Faturas** &gt; **Faturas do fornecedor pendentes**                            | Reveja a fatura para verificar se os valores da folha de horas estão incluídos e, em seguida, lance a fatura do fornecedor.                  |
| N    | **Gestão de projetos e contabilística** &gt; **Faturas do projeto** &gt; **Propostas de faturas do projeto** | Crie uma nova fatura do projeto para o projeto e verifique se as transações por hora que foram lançadas aparecem.            |
| C    | A página **Fatura do projeto**                                                                       | Selecione a fatura do projeto e, em seguida, clique em **Ver detalhes** para rever o custo e o montante da venda. Em seguida, lance a fatura. |


Para mais informações, consulte [Configurar a faturação de projetos entre empresas](tasks/configure-intercompany-project-invoicing.md).




[!INCLUDE[footer-include](../includes/footer-banner.md)]