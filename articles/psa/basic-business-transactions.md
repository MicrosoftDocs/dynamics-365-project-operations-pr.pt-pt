---
title: Transações comerciais
description: Este tópico fornece informações sobre transações comerciais.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 7c1fd7046783b98b7c2e823b2c2eb8bbdfb232fc
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583359"
---
# <a name="business-transactions"></a>Transações comerciais

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

No Dynamics 365 Project Service Automation, a *transação comercial* é um conceito abstrato que não é representado por nenhuma entidade. No entanto, alguns campos e processos comuns nas entidades foram concebidos para utilizarem o conceito de transações comerciais. As seguintes entidades utilizam esta abstração:

- Detalhes de linha de proposta
- Detalhes de item de contrato
- Linhas de estimativa
- Linhas do diário
- Valores Reais

Destas entidades, os Detalhes de linha de proposta, os Detalhes de item de contrato e as Linhas de estimativa são mapeados para a fase de estimativa no ciclo de vida do projeto. As entidades Linhas do diário e Valores reais são mapeadas para a fase de execução no ciclo de vida do projeto.

O PSA trata os registos destas cinco entidades como transações comerciais. A única distinção é que os registos nas entidades que são mapeadas para a fase de estimativa são considerados previsões financeiras, ao passo que os registos nas entidades que são mapeadas para a fase de execução são considerados factos financeiros que já ocorreram.

Para mais informações, consulte [Estimativas](estimates.md) e [Valores Reais](actuals.md).

## <a name="concepts-that-are-unique-to-business-transactions"></a>Conceitos que são exclusivos para as transações comerciais
Os seguintes conceitos são exclusivos para o conceito de transações comerciais:

- Tipo de transação
- Classe de transação
- Origem da transação
- Ligação da transação

### <a name="transaction-type"></a>Tipo de transação

O tipo de transação representa o tempo e o contexto do impacto financeiro num projeto. É representado por um conjunto de opções que tem os seguintes valores suportados no PSA:
- Custo
- Contrato do projeto
- Vendas não faturadas
- Vendas faturadas
- Vendas interorganizacionais
- Custo de unidade de atribuição de recursos

### <a name="transaction-class"></a>Classe de transação

A classe de transação representa os diferentes tipos de custos incorridos nos projetos. É representado por um conjunto de opções que tem os seguintes valores suportados no PSA:

- Time
- Despesa
- Material
- Taxa
- Marco
- Imposto

Normalmente o valor **Marco** é utilizado pela lógica de negócio para a faturação de preço fixo no PSA.

### <a name="transaction-origin"></a>Origem da transação

Origem da transação é uma entidade que armazena a origem de cada transação comercial. À medida que a execução do projeto avança, cada transação comercial dá origem a outra transação comercial, que por sua vez criará outra, e assim sucessivamente. A entidade Origem da transação foi concebida para armazenar os dados sobre a origem de cada transação para ajudar na geração de relatórios e na rastreabilidade. 

### <a name="transaction-connection"></a>Ligação da transação

A ligação da transação é uma entidade que armazena a relação entre duas transações comerciais semelhantes, tais como o custo e os valores reais de vendas relacionados, ou os estornos de transações acionados por atividades de faturação, como as correções ou a confirmação de faturas.

Em conjunto, a Origem da transação e a Ligação da transação ajudam-no a monitorizar as relações entre as transações comerciais e as ações que resultaram na criação de uma transação comercial específica.

### <a name="example-how-transaction-origin-works-with-transaction-connection"></a>Exemplo: como a Origem da transação funciona com a Ligação da transação

O exemplo que se segue mostra o processamento normal das entradas de tempo num ciclo de vida do projeto do PSA.

> ![Processamento completo do tempo num ciclo de vida do Project Service.](media/basic-guide-17.png)
 
1. A submissão de uma entrada de tempo causa a criação de duas linhas do diário: uma para o custo e outra para as vendas não faturadas.
2. A eventual aprovação de uma entrada de tempo causa a criação de dois valores reais: um para o custo e outro para as vendas não faturadas.
3. Quando o utilizador cria uma fatura do projeto, a transação de linha da fatura é criada através da utilização de dados do valor real de vendas não faturadas. 
4. Quando a fatura é confirmada, são criados dois novos valores reais: um estorno de vendas não faturadas e um valor real de vendas faturadas.

Cada um destes eventos aciona a criação de registos nas entidades Origem da transação e Ligação da transação para ajudar a criar um rastreio de relações entre estes registos criados na entrada de tempo, na linha do diário, nos valores reais e nos detalhes de linha de fatura.

A tabela seguinte mostra os registos na entidade Origem da transação para o fluxo de trabalho anterior.

| Evento                        | Origem                   | Tipo de origem                       | Transação                       | Tipo de transação         |
|------------------------------|--------------------------|-----------------------------------|-----------------------------------|--------------------------|
| Submissão da Entrada de Tempo        | GUID do Registo de Entrada de Tempo   | Entrada de Hora                        | GUID do Registo de Linha do Diário (custo)   | Linha do Diário             |
| GUID do Registo de Entrada de Tempo       | Entrada de Hora               | GUID do Registo de Linha do Diário (vendas)  | Linha do Diário                      |                          |
| Aprovação do Tempo                | GUID do Registo de Linha do Diário | Linha do Diário                      | GUID do Registo de Vendas Não Faturadas        | Real                   |
| GUID do Registo de Entrada de Tempo       | Entrada de Hora               | GUID do Registo de Vendas Não Faturadas        | Real                            |                          |
| GUID do Registo de Linha do Diário     | Linha do Diário             | GUID do Registo do Valor Real de Custo           | Real                            |                          |
| GUID do Registo de Entrada de Tempo       | Entrada de Hora               | GUID do Registo do Valor Real de Custo           | Real                            |                          |
| Criação de Faturas             | GUID do Registo de Entrada de Tempo   | Entrada de Hora                        | GUID da Transação de Linha de Fatura     | Transação de Linha de Fatura |
| GUID do Registo de Linha do Diário     | Linha do Diário             | GUID da Transação de Linha de Fatura     | Transação de Linha de Fatura          |                          |
| Confirmação de Faturas         | GUID da Linha de Fatura        | Linha de Fatura                      | GUID do Registo de Vendas Faturadas          | Real                   |
| GUID da fatura                 | Fatura                  | GUID do Registo de Vendas Faturadas          | Real                            |                          |
| GUID do Detalhe de Linha de Fatura     | Detalhe de Linha de Fatura      | GUID do Registo de Vendas Faturadas          | Real                            |                          |
| GUID do Registo de Entrada de Tempo       | Entrada de Hora               | GUID do Registo de Vendas Faturadas          | Real                            |                          |
| GUID do Registo de Linha do Diário     | Linha do Diário             | GUID do Registo de Vendas Faturadas          | Real                            |                          |
| GUID do Registo de Entrada de Tempo       | Entrada de Hora               | GUID do Estorno de Vendas Não Faturadas      | Real                            |                          |
| GUID do Registo de Linha do Diário     | Linha do Diário             | GUID do Estorno de Vendas Não Faturadas      | Real                            |                          |
| Correção de Faturas de Rascunho     | GUID do ILD antigo             | Transação de Linha de Fatura          | GUID do ILD de correção               | Transação de Linha de Fatura |
| GUID do IL antigo                  | Linha de Fatura             | GUID do ILD de correção               | Transação de Linha de Fatura          |                          |
| GUID da fatura antiga             | Fatura                  | GUID do ILD de correção               | Transação de Linha de Fatura          |                          |
| GUID do Registo de Entrada de Tempo       | Entrada de Hora               | GUID do ILD de correção               | Transação de Linha de Fatura          |                          |
| GUID do Registo de Linha do Diário     | Linha do Diário             | GUID do ILD de correção               | Transação de Linha de Fatura          |                          |
| Correção de faturas confirmada | GUID do ILD antigo             | Transação de Linha de Fatura          | GUID do valor real de vendas faturadas estornadas | Real                   |
| GUID do IL antigo                  | Linha de Fatura             | GUID do valor real de vendas faturadas estornadas | Real                            |                          |
| GUID da fatura antiga             | Fatura                  | GUID do valor real de vendas faturadas estornadas | Real                            |                          |
| GUID do Registo de Entrada de Tempo       | Entrada de Hora               | GUID do valor real de vendas faturadas estornadas | Real                            |                          |
| GUID do Registo de Linha do Diário     | Linha do Diário             | GUID do valor real de vendas faturadas estornadas | Real                            |                          |
| GUID do ILD antigo                 | Transação de Linha de Fatura | GUID do Valor Real de Vendas Não Faturadas Novas    | Real                            |                          |
| GUID do IL antigo                  | Linha de Fatura             | GUID do Valor Real de Vendas Não Faturadas Novas    | Real                            |                          |
| GUID da fatura antiga             | Fatura                  | GUID do Valor Real de Vendas Não Faturadas Novas    | Real                            |                          |
| GUID do Registo de Entrada de Tempo       | Entrada de Hora               | GUID do Valor Real de Vendas Não Faturadas Novas    | Real                            |                          |
| GUID do Registo de Linha do Diário     | Linha do Diário             | GUID do Valor Real de Vendas Não Faturadas Novas    | Real                            |                          |
| GUID do ILD de correção          | Transação de Linha de Fatura | GUID do Valor Real de Vendas Não Faturadas Novas    | Real                            |                          |
| GUID do IL de correção           | Linha de Fatura             | GUID do Valor Real de Vendas Não Faturadas Novas    | Real                            |                          |
| GUID da Fatura de Correção      | Fatura                  | GUID do Valor Real de Vendas Não Faturadas Novas    | Real                            |                          |

A tabela seguinte mostra os registos na entidade Ligação da transação para o fluxo de trabalho anterior.

| Evento                          | Transação 1                 | Função da transação 1 | Tipo de transação 1           | Transação 2                | Função da transação 2 | Tipo de transação 2 |
|--------------------------------|-------------------------------|--------------------|------------------------------|------------------------------|--------------------|--------------------|
| Submissão da Entrada de Tempo          | GUID da Linha do Diário (vendas)     | Vendas Não Faturadas     | msdyn_journalline            | GUID da Linha do Diário (custo)     | Custo               | msdyn_journalline  |
| Aprovação do Tempo                  | GUID do Valor Real Não Faturado (vendas)  | Vendas Não Faturadas     | msdyn_actual                 | GUID do valor real de custo (custo)       | Custo               | msdyn_actual       |
| Criação de Faturas               | GUID do Detalhe de Linha de Fatura      | Vendas Faturadas       | msdyn_invoicelinetransaction | GUID do Valor Real de Vendas Não Faturadas   | Vendas Não Faturadas     | msdyn_actual       |
| Confirmação de Faturas           | GUID do Valor Real de Estorno         | Estorno          | msdyn_actual                 | GUID de vendas não faturadas originais | Original           | msdyn_actual       |
| GUID de Vendas Faturadas              | Vendas Faturadas                  | msdyn_actual       | GUID do Valor Real de Vendas Não Faturadas   | Vendas Não Faturadas               | msdyn_actual       |                    |
| Correção de Faturas de Rascunho       | GUID da Transação de Linha de Fatura | Substituição          | msdyn_invoicelinetransaction | GUID de Vendas Faturadas            | Original           | msdyn_actual       |
| Confirmar Correção de Faturas     | GUID de Estorno de Vendas Faturadas    | Estorno          | msdyn_actual                 | GUID de Vendas Faturadas            | Original           | msdyn_actual       |
| GUID do Valor Real de Vendas Não Faturadas Novas | Substituição                     | msdyn_actual       | GUID de Vendas Faturadas            | Original                     | msdyn_actual       |                    |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
