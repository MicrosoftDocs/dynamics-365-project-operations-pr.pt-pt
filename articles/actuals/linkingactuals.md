---
title: Origens das transações - Ligar valores reais à origem
description: Este artigo explica como o conceito de origem de transações é utilizado para ligar valores reais a relatórios de origem originais, tais como entradas de tempo, entrada de despesas ou registos de utilização de materiais.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f1beff392ddd449a930d38016ca6083fea97953b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921316"
---
# <a name="transaction-origins---link-actuals-to-their-source"></a>Origens das transações - Ligar valores reais à origem

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

Os relatórios de origem das transações são criados para ligar valores reais à origem, tais como entradas de tempo, entradas de despesas, registos de utilização de materiais e faturas do projeto.

O exemplo que se segue mostra o processamento normal das entradas de tempo num ciclo de vida do projeto do Project Operations.

> ![Processar entradas de tempo no Project Operations.](media/basic-guide-17.png)
 
1. A submissão de uma entrada de tempo causa a criação de duas linhas do diário: uma para o custo e outra para as vendas não faturadas.
2. A eventual aprovação de uma entrada de tempo causa a criação de dois valores reais: um para o custo e outro para as vendas não faturadas.
3. Quando o utilizador cria uma fatura do projeto, a transação de linha da fatura é criada através da utilização de dados do valor real de vendas não faturadas.
4. Quando a fatura é confirmada, são criados dois novos valores reais: um estorno de vendas não faturadas e um valor real de vendas faturadas.

Cada evento neste fluxo de trabalho de processamento aciona a criação de registos na entidade Origem da transação para ajudar a criar um rastreio de relações entre estes registos criados na entrada de tempo, na linha do diário, valor real e nos detalhes de linha de fatura.

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
| GUID da Fatura de Correção      | Fatura                  | GUID do Valor Real de Vendas Não Faturadas Novas    | Valor Real                            |                          |


A ilustração seguinte mostra as ligações criadas entre tipos diferentes de valores reais e as suas origens em vários eventos utilizando o exemplo de entradas de tempo Project Operations.

> ![Como os valores reais estão associados a registos de origem no Project Operations.](media/TransactionOrigins.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
