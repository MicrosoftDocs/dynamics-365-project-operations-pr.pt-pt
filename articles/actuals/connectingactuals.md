---
title: Ligações de transações - Ligar valores reais de diferentes tipos de transações
description: Este tópico explica como uma ligação de transação é utilizada para ligar valores reais de tipos diferentes para ajudar a controlar a rentabilidade, o atraso de faturação e os cálculos de receitas faturados versus não faturados.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2e8d75a69e27619e6a21f0fe61e2c656e94017b0
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580792"
---
# <a name="transaction-connections---link-actuals-of-different-transaction-types"></a>Ligações de transações - Ligar valores reais de diferentes tipos de transações

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

Os registos de ligação de transações são criados para ligar valores reais de tipos diferentes à medida que o tempo, despesas ou utilização de material se move no ciclo de vida da fase de proposta ou pré-venda para a fase de contrato, aprovações e/ou revocações, faturação e potencial crédito ou faturação corretiva.

O exemplo que se segue mostra o processamento normal das entradas de tempo num ciclo de vida do projeto do Project Operations.

> ![Processar entradas de tempo no Project Operations.](media/basic-guide-17.png)

O processamento de entradas de tempo num ciclo de vida do Project Operations segue estes passos: 

1. A submissão de uma entrada de tempo causa a criação de duas linhas do diário: uma para o custo e outra para as vendas não faturadas. 
2. A eventual aprovação de uma entrada de tempo causa a criação de dois valores reais: um para o custo e outro para as vendas não faturadas. Estes 2 valores reais estão associados através de ligações de transações.
3. Quando o utilizador cria uma fatura do projeto, a transação de linha da fatura é criada através da utilização de dados do valor real de vendas não faturadas.
4. Quando a fatura é confirmada, são criados dois novos valores reais: uma reversão de vendas não faturadas e um valor real de vendas faturadas. A reversão de vendas não faturadas e as vendas não faturadas originais são ligadas utilizando as ligações de transações de reversão. As vendas faturadas e os valores reais de vendas não faturados originais também estão ligados para mostrar as ligações entre as receitas que, antes, era um atraso ou uma receita em progresso (WIP) do que é agora receita faturada.   

Cada evento no fluxo de trabalho de processamento aciona a criação de registos na tabela **Ligação de transação**. Isto ajuda a criar um rastreio das relações entre os registos criados ao longo das entradas de tempo, linhas do diário, valores reais e detalhes da linha da fatura.

A tabela seguinte mostra os registos na entidade **Ligação da transação** para o fluxo de trabalho anterior.

|Evento                   |Transação 1                 |Função da transação 1 |Tipo de transação 1       |Transação 2          |Função da transação 2 |Tipo de transação 2 |
|------------------------|------------------------------|---------------|-----------------------------|-----------------------------|-------------------|-------------------|
|Submissão da Entrada de Tempo   |GUID da Linha do Diário (vendas)     |Vendas Não Faturadas |msdyn_journalline            |GUID da Linha do Diário (custo)     |Custo            |msdyn_journalline  |
|Aprovação do Tempo           |GUID do Valor Real Não Faturado (vendas)  |Vendas Não Faturadas |msdyn_actual                 |GUID do valor real de custo (custo)       |Custo            |msdyn_actual       |
|Criação de Faturas        |GUID do Detalhe de Linha de Fatura      |Vendas Faturadas   |msdyn_invoicelinetransaction |GUID do Valor Real de Vendas Não Faturadas   |Vendas Não Faturadas  |msdyn_actual       |
|Confirmação de Faturas    |GUID do Valor Real de Estorno         |Estorno      |msdyn_actual                 |GUID de vendas não faturadas originais |Original        |msdyn_actual       |
|                        |GUID de Vendas Faturadas             |Vendas Faturadas   |msdyn_actual                 |GUID do Valor Real de Vendas Não Faturadas   |Vendas Não Faturadas  |msdyn_actual       |
|Correção de Faturas de Rascunho |GUID da Transação de Linha de Fatura|Substituição      |msdyn_invoicelinetransaction |GUID de Vendas Faturadas            |Original        |msdyn_actual       |
|Confirmar Correção de Faturas|GUID de Estorno de Vendas Faturadas  |Estorno      |msdyn_actual                 |GUID de Vendas Faturadas            |Original        |msdyn_actual       |
|                        |Novo GUID de vendas não faturadas |Substituição            |msdyn_actual                 |GUID de Vendas Faturadas            |Original        |msdyn_actual       |


A ilustração seguinte mostra as ligações criadas entre tipos diferentes de valores reais em vários eventos utilizando o exemplo de entradas de tempo Project Operations.

> ![Como os valores reais de diferentes tipos são associados entre si no Project Operations.](media/TransactionConnections.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
