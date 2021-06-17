---
title: Gerir uma fatura pró-forma do projeto
description: Este tópico fornece informações sobre como trabalhar com faturas pró-forma em projetos.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: dc069d7007bdc58140a33c7a2ebae7ef9d1e84ff
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003870"
---
# <a name="manage-a-proforma-project-invoice"></a>Gerir uma fatura pró-forma do projeto 

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

No Dynamics 365 Project Operations, as faturas pró-forma são criadas como uma extensão às faturas no Dynamics 365 Sales. No entanto, existem muitas diferenças no processo de faturação entre o Sales e Project Operations no que diz respeito à faturação. Por exemplo, não é possível criar uma nova fatura a partir da página **Lista de Faturas** no Project Operations, mas é possível fazê-lo no Sales. Estas diferenças e extensões estão em vigor para suportar processos de faturação para projetos que são diferentes de uma fatura típica para uma encomenda de vendas.

> [!IMPORTANT]
> Devido às diferenças, não utilize faturas no Sales e Project Operations alternadamente.

## <a name="invoice-header"></a>Cabeçalho da fatura

As seguintes informações estão disponíveis num cabeçalho de fatura pró-forma no Project Operations.

| Campo | Localização | Descrição | Impacto a jusante |
| --- | --- | --- | --- |
| **ID da Fatura** | Separador **Resumo** | O ID gerado automaticamente quando uma fatura pró-forma é criada. Um campo só de leitura que está bloqueado da edição. | Este campo é utilizado como referência para cada fatura pró-forma. |
| **Nome** | Separador **Resumo** | Definir o nome do contrato do projeto por predefinição. Este campo pode ser editado pelo utilizador. | &nbsp;  |
| **Moeda** | Separador **Resumo** | Definir a moeda do contrato do projeto por predefinição. Um campo só de leitura que está bloqueado da edição. |&nbsp; |
| **Lista de preços** | Separador **Resumo** | Definir a lista de preços do contrato do projeto por predefinição. Um campo só de leitura que está bloqueado da edição. | &nbsp; |
| **Oportunidade** | Separador **Resumo** | A referência à oportunidade associada. Um campo só de leitura que está bloqueado da edição. | &nbsp;  |
| **Contrato** | Separador **Resumo** | A referência ao contrato do projeto associado. Um campo só de leitura que está bloqueado da edição. | &nbsp; |
| **Cliente** | Separador **Resumo** | A referência ao contrato do projeto associado. Um campo só de leitura que está bloqueado da edição. |&nbsp;  |
| **Descrição** | Separador **Resumo** | O campo de texto que descreve a fatura. Este campo pode ser editado pelo utilizador. | &nbsp; |
| **Faturar a** e campos relacionados | **Separador Resumo** | As predefinições são definidas pelo cliente do contrato do projeto. Este campo pode ser editado pelo utilizador.  | &nbsp; |
| **Status** | Separador **Resumo** | Define as seguintes opções: **Ativa**, **Fechada**, **Paga** e **Cancelada** e podem ser editadas pelo utilizador. | Os estados não suportados para o Project Operations incluem **Fechadas** e **Canceladas**. </br> O estado é definido para **Ativa** quando a fatura é criada. </br>O estado só deve ser definido para **Paga** após a confirmação da fatura. |
| **Estado da Fatura do Projeto** | Separador **Resumo** | Define as seguintes opções: **Rascunho**, **Em análise** e **Confirmada** e podem ser editadas pelo utilizador. | Tanto nos estados **Rascunho** como **Em análise**, a fatura pode ser editada. A fatura não pode ser editada depois de confirmada. |
| **Montante Detalhado** | Separador **Resumo** | A soma dos montantes em todas as linhas de fatura após adiantamentos e deduções. Um campo só de leitura que está bloqueado da edição. | Este campo é usado para calcular o montante final. |
| **Desconto (%)** | Separador **Resumo** | Este campo pode ser editado para introduzir uma percentagem de desconto. Este campo não é suportado pela funcionalidade do Project Operations. | Este é um campo não suportado. |
| **Montante de Desconto** | Separador **Resumo** | Este campo pode ser editado para introduzir o montante do desconto. Este campo não é suportado pela funcionalidade do Project Operations. | Este é um campo não suportado. |
| **Montante antes de transporte** | **Separador Resumo** | O montante total da fatura após descontos é aplicado. Um campo só de leitura que está bloqueado da edição. | Este campo é usado para calcular o montante final. |
| **Montante do Transporte** | Separador **Resumo** | Este campo pode ser editado para introduzir o montante do transporte. Este campo não é suportado pela funcionalidade do Project Operations. | Este é um campo não suportado. |
| **Imposto Total** | Separador **Resumo** | O imposto total de todas as linhas de fatura na fatura. Um campo só de leitura que está bloqueado da edição. | Nenhum. |
| **Montante Total** | Separador **Resumo** | A soma do montante após descontos e impostos. | A soma é o montante que o cliente precisa de pagar. |
## <a name="project-based-invoice-lines"></a>Linhas de fatura baseadas em projetos

No Project Operations, há sempre uma linha de fatura para cada item de contrato do projeto. A linha de fatura é criada mesmo que não existam valores reais. As seguintes informações estão disponíveis numa linha de fatura pró-forma.

| Campo | Localização | Descrição | Impacto a jusante |
| --- | --- | --- | --- |
| **ID da Fatura** | Separador **Geral** | A referência ao ID da fatura. Um campo só de leitura que está bloqueado da edição. | A ligação do ID da fatura pode ser utilizado para navegar de volta para o cabeçalho da fatura. |
| **Nome** | Separador **Geral** | O nome da linha de fatura definida por predefinição a partir do nome do item de contrato. Este campo pode ser editado pelo utilizador. | &nbsp; |
| **Project** | Separador **Geral** | O projeto no item de contrato do projeto relacionado. Um campo só de leitura que está bloqueado da edição. | A ligação do projeto pode ser usada para navegar para o projeto. |
| **Método de Faturação** | Separador **Geral** | O método de faturação no item de contrato do projeto relacionado. Um campo só de leitura que está bloqueado da edição. | &nbsp; |
| **Montante de Item de Contrato** | Separador **Geral** | O montante do contrato no item de contrato do projeto relacionado. Um campo só de leitura que está bloqueado da edição. | &nbsp; |
| **Faturado até à Data** | Separador **Geral** | A soma dos montantes em todos os detalhes da linha de fatura desta fatura. Um campo só de leitura que está bloqueado da edição. | &nbsp; |
| **Montante** | Separador **Geral** | A soma dos montantes em todos os detalhes da linha de fatura faturável desta fatura. Um campo só de leitura que está bloqueado da edição. | Este campo é usado para calcular o montante final no cabeçalho da fatura. |
| **Imposto** | Separador **Geral** | A soma dos montantes de impostos em todos os detalhes da linha de fatura desta linha de fatura. Um campo só de leitura que está bloqueado da edição. | Este campo é usado para calcular o montante de impostos final no cabeçalho da fatura. |
| **Montante Total** | Separador **Geral** | A soma dos montantes totais (**Imposto + Montantes**) em todos os detalhes da linha de fatura faturável desta linha de fatura. Um campo só de leitura que está bloqueado da edição. | Este campo é usado para calcular o montante final no cabeçalho da fatura. |


## <a name="invoice-line-details"></a>Detalhes de linha de fatura

Cada linha de fatura numa fatura do projeto inclui detalhes da linha de fatura. Estes detalhes de linha estão relacionados com os valores reais de vendas e marcos não faturados relacionados com o item de contrato referenciada pela linha de fatura. Todas estas transações estão marcadas como **Pronto a Faturar**.

Para uma linha de **Fatura de tempo e material**, os detalhes da linha de fatura são agrupados na página **Faturável**, **Não faturável** e **Grátis** na página **Linha de fatura**. Os detalhes da **Linha de Fatura Faturável** somam ao total da linha de fatura. Valores reais **grátis** e **não faturáveis** não somam o total da linha de fatura.

Para uma linha de **fatura de preço fixo**, os detalhes da linha de fatura são criados a partir de marcos que são marcados como **Prontos a faturar** no item de contrato relacionado. Após a criação do detalhe da linha de fatura a partir de um marco, o estado de faturação do marco é atualizado para **Fatura do Cliente Criada**.

### <a name="edit-invoice-line-details"></a>Editar detalhes de linha de fatura

Os seguintes campos estão disponíveis num detalhe da linha de fatura que é suportada por um valor real de venda não faturada:

| Campo | Descrição | Impacto a jusante |
| --- | --- | --- |
| **Linha de fatura** | Uma referência ao **ID de Linha da Fatura**. Campo só de leitura bloqueado para edição. | Esta ligação do ID da fatura pode ser utilizada para navegar de volta para o cabeçalho da fatura. |
| **Descrição** | Uma descrição do detalhe da linha de fatura. Configurar por predefinição o campo **Comentários Internos** em **Entrada de Tempo** e do campo **Descrição** na **Entrada de Despesas**. O campo pode ser editado pelo utilizador.| &nbsp; |
| **Descrição Externa** | Uma descrição do detalhe da linha de fatura. Configurar por predefinição o campo **Comentários Externos** em **Entrada de Tempo** e campo **Descrição** na **Entrada de Despesas**. O campo pode ser editado pelo utilizador. | Esta descrição pode ser usada para determinar o que deve estar na fatura impressa que será enviada ao cliente. No Project Operations, uma fatura pró-forma não tem todas as funcionalidades necessárias para configurar definições de impressão para uma fatura. |
| **Data de Início** | Predefinido a partir do valor real de origem. Um campo só de leitura que está bloqueado da edição. | Este campo pode ser editado num novo detalhe da linha de fatura que não é apoiado por um valor real de origem. |
| **Project** | Predefinido a partir do valor real de origem. Um campo só de leitura que está bloqueado da edição. | Predefinido para o projeto no item de contrato relacionado. |
| **Tarefa** | Predefinido a partir do valor real de origem. Um campo só de leitura que está bloqueado da edição. | O campo pode ser editado num novo detalhe da linha de fatura que não é apoiado por um valor real de origem. Uma lista pendente mostra todas as tarefas associadas ao item de contrato do projeto relacionado.  |
| **Categoria de transação** | Predefinido a partir do valor real de origem. Um campo só de leitura que está bloqueado da edição. | O campo pode ser editado num novo detalhe da linha de fatura que não é apoiado por uma origem real. |
| **Função** | Predefinido a partir do valor real de origem. Um campo só de leitura que está bloqueado da edição. | O campo pode ser editado num novo detalhe da linha de fatura que não é apoiado por um valor real de origem. |
| **Recurso Reservável** | Predefinido a partir do valor real de origem. Um campo só de leitura que está bloqueado da edição. | O campo pode ser editado num novo detalhe da linha de fatura que não é apoiado por uma origem real. |
| **Unidade de Atribuição de Recursos** | Predefinido a partir do valor real de origem. Um campo só de leitura que está bloqueado da edição. | O campo pode ser editado num novo detalhe da linha de fatura que não é apoiado por um valor real de origem. |
| **Quantidade** | Predefinido a partir do valor real de origem. Um campo só de leitura que está bloqueado da edição. | O campo pode ser editado num novo detalhe da linha de fatura que não é apoiado por um valor real de origem. |
| **Agenda de Unidades** | Para o detalhe da linha de fatura para tempo, este é sempre definido para tempo e não pode ser editado. Para despesas, este é predefinido a partir do valor real da despesa de origem. Um campo só de leitura que está bloqueado da edição. | Predefinido para **Tempo** num novo detalhe da linha de fatura que não é apoiado por um valor real. |
| **Unidade** | Predefinido a partir do valor real de origem. Um campo só de leitura que está bloqueado da edição. | O campo pode ser editado num novo detalhe da linha de fatura que não é apoiado por um valor real de origem |
| **Preço** | Predefinido a partir do valor real de origem. Um campo só de leitura que está bloqueado da edição. | O campo pode ser editado num novo detalhe da linha de fatura que não é apoiado por um valor real de origem. Se não for introduzido qualquer valor, é predefinido depois de **Guardar**. |
| **Moeda** | Predefinido a partir do valor real de origem. Um campo só de leitura que está bloqueado da edição. | Predefinido a partir do cabeçalho da fatura ao criar um novo detalhe de fatura sem suporte de valor real.  Um campo só de leitura que está bloqueado da edição. |
| **Montante** | Predefinido a partir do valor real de origem. Um campo só de leitura que está bloqueado da edição. | Calculado como **Quantidade \* Preço** ao criar um novo detalhe de fatura sem um valor real de suporte. É calculado depois de **Guardar**. Um campo só de leitura que está bloqueado da edição. |
| **Imposto** | Predefinido a partir do valor real de origem. O campo pode ser editado pelo utilizador | O campo pode ser editado pelo utilizador ao criar um novo detalhe de linha de fatura sem um valor real de suporte. |
| **Montante Total** | Um campo calculado, calculado como **Montante + Imposto**. Um campo só de leitura que está bloqueado da edição. | &nbsp; |
| **Tipo de Faturação** | Predefinido a partir do valor real de origem. O campo pode ser editado pelo utilizador. | Selecionar **Faturável** adiciona a linha ao total da linha de fatura. **Grátis** e **Não Faturável** irá excluí-la do total da linha de fatura. |
| **Selecionar Produto** | Marcado por predefinição a partir da fonte real, este é um campo de apenas leitura. | Quando cria um novo detalhe de linha de fatura sem um suporte real, este campo pode ser editado. |
| **Produto** | Marcado por predefinição a partir da fonte real, este é um campo de apenas leitura. | Quando cria um novo detalhe de linha de fatura sem um suporte real, este campo pode ser editado se o campo **Selecionar produto** estiver definido para o **produto existente**. |
| **Nome do Produto** | Marcado por predefinição a partir da fonte real, este é um campo de apenas leitura. | Num novo detalhe da linha de fatura, onde o ID do produto é selecionado a partir do catálogo, este campo é definido para o nome do produto. Para acrescentar manualmente no produto, o campo está definido para acrescentar manualmente em nome. |
| **Descrição de acrescentar manualmente** | Marcado por predefinição a partir da fonte real, este campo é de apenas leitura. | Quando cria um novo detalhe de linha de fatura sem um suporte real, pode acrescentar manualmente uma descrição para o produto. |
| **Tipo de Transação** | Predefinido a partir do valor real de origem. Um campo só de leitura que está bloqueado da edição. | Predefinido para **Vendas Faturadas** e bloqueado ao criar um novo **Detalhe da linha de fatura** sem um valor real de suporte.  |
| **Classe de Transação** | Predefinido a partir do valor real de origem. Um campo só de leitura que está bloqueado da edição. | Definido por predefinição com base no facto de o utilizador optar por criar um detalhe de linha de fatura **tempo**, **despesa**, **material** ou **taxa**, ao mesmo tempo que cria um novo **detalhe da linha fatura** sem suporte real. Bloqueado de edição. |

Os seguintes campos estão disponíveis num detalhe da linha de fatura que é suportada por marco:

| Campo | Descrição | Impacto a jusante |
| --- | --- | --- |
| **Linha de fatura** | Referência ao **ID de Linha da Fatura**. Um campo só de leitura que está bloqueado da edição. | A ligação do ID da fatura pode ser utilizada para navegar de volta para o cabeçalho da fatura. |
| **Descrição** | Descrição do detalhe da linha de fatura. Predefinido a partir da descrição do marco de origem. | &nbsp; |
|**Descrição Externa** | Descrição do detalhe da linha de fatura que é predefinido a partir da descrição do marco de origem. | Este campo pode ser usado para determinar o que deve estar na fatura impressa que será enviada ao cliente. Uma fatura pró-forma no Project Operations não tem todas as funcionalidades necessárias para configurar definições de impressão para uma fatura. |
| **Data de Início** | Predefinido a partir da data do **Marco** no marco de origem. Um campo só de leitura que está bloqueado da edição. | &nbsp; |
| **Project** | Predefinido a partir do marco de origem. Um campo só de leitura que está bloqueado da edição. | &nbsp; |
| **Tarefa** | Predefinido a partir do marco de origem. Um campo só de leitura que está bloqueado da edição. | &nbsp; |
| **Categoria de transação** | Um campo só de leitura que está bloqueado da edição. | &nbsp; |
| **Função** | Um campo só de leitura que está bloqueado da edição. | &nbsp; |
| **Recurso Reservável** | Um campo só de leitura que está bloqueado da edição. | &nbsp; |
| **Unidade de Atribuição de Recursos** | Um campo só de leitura que está bloqueado da edição. | &nbsp; |
| **Agenda de Unidades** | Um campo só de leitura que está bloqueado da edição. | &nbsp; |
| **Unidade** | Um campo só de leitura que está bloqueado da edição. | &nbsp; |
| **Preço** | Predefinido a partir do montante sobre o marco de origem. Um campo só de leitura que está bloqueado da edição. | &nbsp; |
| **Moeda** | Predefinido a partir do marco de origem. Um campo só de leitura que está bloqueado da edição. |&nbsp; |
| **Montante** | Predefinido a partir do montante sobre o marco de origem. Um campo só de leitura que está bloqueado da edição. | &nbsp; |
| **Imposto** | Predefinido a partir do montante do imposto sobre o marco de origem. Um campo só de leitura que está bloqueado da edição. | &nbsp; |
| **Montante Total** | Predefinido a partir do valor total do marco de origem. O campo pode ser editado pelo utilizador | &nbsp; |
| **Tipo de Faturação** | Sempre predefinido como **Faturável**. Um campo só de leitura que está bloqueado da edição. | &nbsp; |
| **Tipo de Transação** | Predefinido a partir do marco de origem. Um campo só de leitura que está bloqueado da edição. | &nbsp; |
| **Classe de Transação** | Predefinido a partir do marco de origem. Um campo só de leitura que está bloqueado da edição. | &nbsp; |

### <a name="create-new-invoice-line-details"></a>Criar novos detalhes de linha de fatura

Em linhas de fatura de tempo e material, pode criar novos detalhes da linha de fatura. Estes detalhes da linha de fatura não são apoiados por um valor real. Na linha de fatura de uma linha de fatura de tempo e material, pode selecionar **Novo** para criar um novo detalhe de linha de fatura para as classes de transações que estão incluídas no item de contrato.

## <a name="refresh-invoice-transactions"></a>Atualizar transações de fatura

Se tiver valores reais que chegaram após a criação da fatura, pode incluir estes valores reais na fatura.

1. Na **Vista de Registo de Tarefas Pendentes de Faturação**, marque os dados como **Pronto a Faturar**.   
2. Abra a fatura pró-forma de rascunho e, na faixa **Ações**, clique em **Atualizar Transações da Linha de Fatura**.

  Isto cria detalhes da linha de fatura para qualquer valor real que seja datado e marcado como **Pronto a Faturar**, mas não está incluído na fatura.

## <a name="product-based-invoice-lines"></a>Linhas de fatura baseadas em produtos

No Project Operations, pode criar linhas de fatura para produtos que não se aplicam a nenhum projeto ou a todos os projetos, juntamente com linhas de fatura baseadas em projetos. Estas linhas de fatura são criadas como itens de contrato baseados em produtos e depois de marcados como pronto a faturar, são adicionados como linhas de fatura baseadas em produtos.

Depois de ter adicionado linhas de fatura baseadas em produtos, não podem ser alteradas. Podem, no entanto, ser eliminadas da fatura pró-forma de rascunho.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
