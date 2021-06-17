---
title: Ligue os valores reais aos registos originais
description: Este tópico explica como ligar os valores reais aos registos originais, tais como entrada de tempo, entrada de despesas ou registos de utilização de materiais.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9fc49211f3c2c79e18f6dd18e9a687091793cad0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996760"
---
# <a name="link-actuals-to-original-records"></a>Ligue os valores reais aos registos originais

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_


No Dynamics 365 Project Operations, uma *transação comercial* é um conceito abstrato que não é representado por uma entidade. No entanto, alguns campos e processos comuns nas entidades foram concebidos para utilizarem o conceito de transações comerciais. As seguintes entidades utilizam este conceito:

- Detalhes de linha de proposta
- Detalhes de item de contrato
- Linhas de estimativa
- Linhas do diário
- Valores Reais

Destas entidades, os **Detalhes de linha de proposta**, **Detalhes de item de contrato** e **Linhas de estimativa** são mapeados para a fase de estimativa no ciclo de vida do projeto. As entidades **Linhas do diário** e **Valores reais** são mapeadas para a fase de execução no ciclo de vida do projeto.

O Project Operations reconhece os registos destas cinco entidades como transações comerciais. A única distinção é que os registos nas entidades que são mapeadas para a fase de estimativa são considerados previsões financeiras, ao passo que os registos nas entidades que são mapeadas para a fase de execução são considerados factos financeiros que já ocorreram.

## <a name="concepts-that-are-unique-to-business-transactions"></a>Conceitos que são exclusivos para as transações comerciais
Os seguintes conceitos são exclusivos para o conceito de transações comerciais:

- Tipo de transação
- Classe de transação
- Origem da transação
- Ligação da transação

### <a name="transaction-type"></a>Tipo de transação

O tipo de transação representa o tempo e o contexto do impacto financeiro num projeto. isto é representado por um conjunto de opções que tem os seguintes valores suportados no Project Operations:

  - Custo
  - Contrato do projeto
  - Vendas não faturadas
  - Vendas faturadas
  - Vendas interorganizacionais
  - Custo de unidade de atribuição de recursos

### <a name="transaction-class"></a>Classe de transação

A classe de transação representa os diferentes tipos de custos incorridos nos projetos. isto é representado por um conjunto de opções que tem os seguintes valores suportados no Project Operations:

  - Tempo
  - Despesa
  - Material
  - Taxa
  - Marco
  - Imposto

Normalmente, o valor **Marco** é utilizado pela lógica de negócio para a faturação de preço fixo no Project Operations.

### <a name="transaction-origin"></a>Origem da transação

**Origem da transação** é uma entidade que armazena a origem de cada transação comercial. À medida que um projeto começa, cada transação comercial dará origem a outra transação comercial que, por sua vez, irá criar outra e assim por diante. A entidade de origem de transações é projetada para armazenar dados sobre a origem de cada transação para ajudar no reporte e rastreabilidade. 

### <a name="transaction-connection"></a>Ligação da transação

A **ligação da transação** é uma entidade que armazena a relação entre duas transações comerciais semelhantes, tais como o custo e os valores reais de vendas relacionados, ou os estornos de transações acionados por atividades de faturação, como as correções ou a confirmação de faturas.

Em conjunto, a **Origem da transação** e a **Ligação da transação** ajudam-no a monitorizar as relações entre as transações comerciais e as ações que resultaram na criação de uma transação comercial específica.

### <a name="example-how-transaction-origin-works-with-transaction-connection"></a>Exemplo: como a Origem da transação funciona com a Ligação da transação

O exemplo que se segue mostra o processamento normal das entradas de tempo num ciclo de vida do projeto do Project Operations.

> ![Processamento completo do tempo num ciclo de vida do Project Service](media/basic-guide-17.png)
 
1. Uma submissão de entrada de tempo causa a criação de duas linhas do diário: uma para o custo e outra para as vendas não faturadas.
2. A eventual aprovação de uma entrada de tempo cria dois valores reais: um valor real para o custo e outro valor real para as vendas não faturadas.
3. Quando uma nova fatura do projeto é criada, a transação de linha da fatura é criada através da utilização de dados do valor real de vendas não faturadas. 
4. Quando a fatura é confirmada, são criados dois novos valores reais: um valor real de estorno de vendas não faturadas e um valor real de vendas faturadas.

Cada um destes eventos cria um registo nas entidades de **Origem da transação** e **Ligação da transação**. Estes novos registos ajudam a construir uma história de relações entre os registos que são criados através da entrada no tempo, linha de diário, detalhes reais e detalhes da linha de fatura.

A tabela seguinte mostra os registos na entidade **Origem da transação** para o fluxo de trabalho anterior.

| Evento                        | Origem                   | Tipo de origem                       | Transação                       | Tipo de transação         |
|------------------------------|--------------------------|-----------------------------------|-----------------------------------|--------------------------|
| Submissão da Entrada de Tempo        | GUID do registo de entrada de tempo   | Entrada de Hora                        | GUID do Registo de Linha do Diário (custo)   | Linha do Diário             |
| GUID do Registo de Entrada de Tempo       | Entrada de Hora               | GUID do Registo de Linha do Diário (vendas)  | Linha do Diário                      |                          |
| Aprovação do Tempo                | GUID do Registo de Linha do Diário | Linha do Diário                      | GUID do Registo de Vendas Não Faturadas        | Real                   |
| GUID do Registo de Entrada de Tempo       | Entrada de Hora               | GUID do Registo de Vendas Não Faturadas        | Real                            |                          |
| GUID do Registo de Linha do Diário     | Linha do Diário             | GUID do Registo do Valor Real de Custo           | Real                            |                          |
| GUID do Registo de Entrada de Tempo       | Entrada de Hora               | GUID do Registo do Valor Real de Custo           | Valor Real                            |                          |
| Criação de Faturas             | GUID do registo de entrada de tempo   | Entrada de Hora                        | GUID da Transação de Linha de Fatura     | Transação de Linha de Fatura |
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

A tabela seguinte mostra os registos na entidade **Ligação da transação** para o fluxo de trabalho anterior.

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
