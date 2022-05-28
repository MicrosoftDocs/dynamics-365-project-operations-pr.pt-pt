---
title: Criar e confirmar diários de entrada
description: Este tópico informações sobre como criar e confirmar os diários de entrada no Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 8cb768337bc197895a837670f93b99b132c97437
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584242"
---
# <a name="create-and-confirm-entry-journals"></a>Criar e confirmar diários de entrada

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

Pode utilizar diários de entrada para registar valores reais diretamente no Microsoft Dynamics 365 Project Operations. Quando utiliza os diários de entrada, não tem de introduzir o Tempo, as Despesas e a utilização de Materiais no Project Operations.

Um diário de entrada único permite-lhe criar várias linhas de diário múltiplas. Quando o diário é confirmado, uma linha do diário de entrada regista os valores atuais para os detalhes seguintes:

- O custo ou receita, dependendo do tipo de transações que foi selecionado.
- A classe de transação selecionada. As classes disponíveis são **Tempo**, **Despesas**, **Material**, **Adiantamento**, **Marcos** e **Imposto**.
- O projeto e/ou tarefa que está selecionada na linha do diário.

Siga estes passos para criar um diário de entrada no Project Operations.

1. Aceda a **Vendas** \> **Transações** \> **Diários.**
2. Na página da lista **Diários de entrada,** no Painel de Ação, selecione **Novo** para criar um diário.
3. Na página **Novo diário**, no campo **Descrição**, introduza uma descrição do mesmo.
4. Certifique-se de que o campo **Tipo de diário** está definido como **Entrada** e, em seguida, selecione **Guardar**. Depois de guardado o novo diário de entrada, deve aparecer um separador **Linhas do diário** na página do diário.
5. No separador **Linhas do diário**, na barra de ferramentas acima da grelha, selecione **Novo** para criar uma linha do diário de entrada.
6. Na caixa de diálogo **Criação rápida** para criar uma linha do diário de entrada, defina os campos conforme descrito na tabela seguinte.

    | Campo | Description | Impacto funcional |
    | --- | --- | --- |
    | Classe de Transação | A linha do diário pode ser classificada numa das seis classes de transação: **Tempo**, **Despesas**, **Material**, **Adiantamento**, **Marcos** ou **Imposto**. | A classe de transação **Imposto** foi preterida no Project Operations. <br> Se criar uma classe de transação **Imposto**, a mesma não será processada por faturas, custos ou cálculos de receitas. **Marcos** é uma classe de transações apenas de receitas. <br>A classe de transação **Adiantamento** representa um avanço recebido de um cliente. Deve sempre ser criado como um par de vendas faturadas e linhas de diário de vendas não faturadas. |
    | Tipo de Operação | Os tipos de transações **Custo**, **Vendas Interorganização** e **Custo unitário dos recursos** devem ser utilizados para o custo de gravação.<br> Os tipos de transação **Vendas não faturadas** e **Vendas faturadas** devem ser utilizados para gravar receitas. | A classe de transação **Adiantamento** funciona apenas com os tipos de transação **Vendas não faturadas** e **Vendas faturadas**.<br> A classe de transação **Marcos** funciona apenas com o tipo de transação **Vendas faturadas**. <br>Os tipos de transação **Vendas Interorganização** e **Custo unitário dos recursos** são aplicáveis apenas à classe de transação **Tempo** e estão apenas disponíveis nos diários de entrada no cenário de implementação Lite e não ao implementar o Project Operations nos cenários Recurso/Não Em Stock. |
    | Selecionar Produto | Quando uma classe de transação **Material** é selecionada, este campo permite-lhe especificar se a transação material para a qual está a criar a linha do diário é um produto existente ou um produto de sobreposição. | Se selecionar o **Produto de sobreposição**, pode introduzir um nome para o produto. |
    | Produto | Uma referência para o produto do catálogo. | |
    | Description | Uma descrição da linha do diário para facilitar a sua identificação. | Para linhas de diários de vendas não faturadas, o valor será utilizado como descrição quando os detalhes do linha de fatura forem criados. |
    | Descrição externa | Uma descrição da linha do diário que pode ser utilizada para partilhar com os intervenientes externos. | Para linhas de diários de vendas não faturadas, o valor será utilizado como descrição externa quando os detalhes do linha de fatura forem criados. Também pode aparecer na fatura que é enviada para o cliente. |
    | Tipo de Faturação | Um valor que indica se a linha do diário será contabilizada como componente imputável, complementar ou não imputável no projeto. | Num fluxo normal, o tipo de faturação deriva dos termos acordados que estão definidos no contrato. No entanto, quando gravar uma linha do diário, poderá inserir um valor neste campo. |
    | Data do documento | Utilize uma data em que a transação ocorreu. | |
    | Data de Início | Utilize a data em que a transação ocorreu. | Este campo é utilizado para comparação com a data de criação de faturas para transações do tipo **Vendas Não Faturadas**. Esta comparação irá ajudá-lo a decidir se a transação tem uma data futura ou passada. Só são adicionadas transações passadas à fatura. |
    | Data de Fim | Utilize a data em que a transação ocorreu. | |
    | Data de Gestão Contabilística | Utilize a data em que o impacto na gestão contabilística será registado. | |
    | Cliente do item de contrato | Por predefinição, se o item de contrato tiver apenas um cliente, este campo é definido com o cliente no item de contrato quando a linha do diário for guardada. Se o item de contrato tiver vários clientes, selecione o cliente correto no item de contrato. | Se o sistema não conseguir determinar o cliente do item de contrato na linha do diário, e se estiver em branco no valor real do tipo **Vendas não faturadas** que é criado a partir da linha do diário, o valor real não será faturado. |
    | Project | Selecione o projeto para gravar o valor real. | Com base no projeto, classe de transações e tarefa selecionados, o sistema tenta determinar o contrato, item de contrato e cliente de item de contrato. |
    | Tarefa | Selecione a tarefa para gravar o valor real. | Se tiver associado tarefas a linhas de contrato durante a configuração do contrato, o sistema irá utilizar a tarefa selecionada, juntamente com uma classe de projeto e transação, para determinar o contrato, item de contrato e cliente de item de contrato. |
    | Categoria de Transação | Selecione a categoria da transação para gravar o valor real. | Para as despesas, a categoria de transações selecionada determina o preço predefinido que será inserido na linha do diário quando este for guardado. |
    | Função | Este campo é relevante para as linhas de diário Tempo. Selecione a função do recurso que gastou tempo no projeto e/ou tarefa. | Para linhas do diário Tempo, se utilizar a configuração alternativa para a entrada dos custos de recurso predefinidas e taxas de faturação, a função selecionada é utilizada em conjunto com a unidade de recursos para determinar o preço predefinido que será inserido na linha do diário quando for guardado. Se utilizar uma configuração personalizada para a entrada de preços predefinidos, deve rever essa configuração para determinar se o campo **Função** é utilizado para inserir valores de preços predefinidos. |
    | Subcontrato | Se a linha do diário representar capacidade subcontratada ou despesas ou materiais subcontratados, selecione o subcontrato relevante. | Quando as linhas do diário de custos são registadas, o subcontrato selecionado irá determinar a lista de preços utilizada para introdução do custo unitário predefinido. |
    | Item de subcontrato | Se a linha do diário representar capacidade subcontratada ou despesas ou materiais subcontratados, selecione o item de subcontrato relevante. | Quando as linhas do diário de custos são registadas, o item de subcontrato selecionado irá assegurar que os cálculos de capacidade disponíveis no item de subcontrato estão corretamente calculados. |
    | Método de Montante | Por predefinição, este campo está definido como **Multiplicar quantidade pelo preço**. Quando este método for utilizado, o montante será calculado como *Quantidade* x *Preço*. O outro método suportado é o **Preço fixo**. Quando este método é utilizado, o preço será definido com o montante e a quantidade não será utilizada no cálculo. | |
    | Agenda de unidades e Unidade | Em conjunto, a agenda de unidades e a unidade identificam a unidade da quantidade. | A combinação da unidade com a categoria de transações é utilizada para introduzir os preços predefinidos das despesas. Na configuração predefinida do Project Operations, a combinação da unidade, função e unidade de recursos é utilizada para predefinir os preços por tempo. Se tiver uma configuração personalizada para a entrada de preços predefinidos, a mesma será utilizada juntamente com a unidade. A combinação do produto e da unidade é utilizada para introduzir os preços predefinidos dos materiais. |
    | Quantidade | Introduza a quantidade. | |
    | Preço | Se o preço ficar em branco quando a linha do diário for criada, os valores relevantes serão utilizados para introduzir os preços predefinidos, dependendo da classe de transação. Se um preço for inserido quando a linha do diário for criada, esse preço será utilizado. | |
    | Imposto | Introduza qualquer montante de imposto. | Dependendo do montante de imposto que foi inserido, o valor total será calculado como *Montante* + *Imposto*. |

## <a name="confirm-an-entry-journal"></a>Confirmar um diário de entrada

Depois de inserir todas as linhas do diário num diário de entrada, pode confirmar o diário. Este processo irá gravar cada linha do diário como valores reais nos projetos apropriados.

Depois de um diário ser confirmado, já não é possível editá-lo nem a nenhuma das linhas.

## <a name="actuals-created-by-entry-journal-confirmation"></a>Valores reais criados pela confirmação do diário de entrada

Existem algumas diferenças principais entre os valores reais criados pela confirmação do diário de entrada e os valores reais que são criados durante a aprovação dos registos de utilização Tempo, Despesas e Materiais e confirmação de fatura no Project Operations:

- Os diários de entrada não utilizam ligações de transações para ligar o custo real às vendas não faturadas. Os valores reais criados quando os registos de utilização de Tempo, Despesas e Materiais são aprovados utilizam sempre ligações de transações para ligar o custo e os valores reais de vendas não faturadas.
- Os diários de entrada não utilizam origens de transações para ligar o custo real e as vendas reais não faturadas a nenhum registo proveniente. Os valores reais criados quando os registos de utilização de Tempo, Despesas e Materiais são aprovados utilizam sempre origens de transações para ligar o custo e os valores reais de vendas não faturadas à entrada de tempo proveniente.
- Quando os valores reais de vendas não faturados que são criados por confirmação do diário de entrada são faturados, os valores reais de vendas faturados criados durante a confirmação da fatura são associados aos valores reais de vendas não faturadas, de modo semelhante aos valores reais de vendas não faturadas criados quando os registos de utilização de Tempo, Despesas e Materiais são aprovados.
- As linhas do diário de entrada que são criadas para tempo e que são inseridas por recursos inter-organizacionais não fazem com que os valores reais dos tipos **Custo unitário dos recursos** e **Vendas Interorganização** sejam criados automaticamente. Estes valores reais têm de ser criados manualmente. Este comportamento é diferente do comportamento das entradas de tempo registadas pelos recursos interorganizacionais. Neste caso, quando o tempo é aprovado, a aplicação cria automaticamente os valores reais do tipo **Custo** no projeto e os valores reais dos tipos **Custo unitário dos recursos** e **Vendas interorganização** na divisão de propriedade do colaborador. Em seguida, utiliza ligações de transações para ligar esses valores reais e origens das transações, para as ligar à entrada de tempo proveniente.
- Quando os diários de entrada são confirmados, criam valores reais. No entanto, não é possível utilizar diários de correção para corrigir esses valores reais. Este comportamento é diferente do comportamento dos valores reais criados quando os registos de utilização de Tempo, Despesas e Materiais são aprovados. Neste caso, a aplicação permite-lhe utilizar diários de correção para corrigir os valores reais para corrigir erros, desde que esses valores reais ainda não tenham sido faturados. Se ja tiverem sido faturados, ainda pode corrigir um valor real se processar um crédito total desse valor real ao cliente.

> [!NOTE]
> Os diários de entrada não impõem regras de predefinição rígidas. Por conseguinte, utilize o menos possível estes diários de entra e tenha os cuidados necessários para garantir que não cria dados financeiros danificados no seu sistema. Sempre que possível, utilize os registos de utilização de Tempo, Despesas e Materiais, os marcos e a configuração de adiantamento nos contratos do projeto e o processo de confirmação da fatura do projeto em vez de criação de valores reais pelos diários de entrada.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
