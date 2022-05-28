---
title: Transações comerciais no Project Operations
description: Este tópico fornece uma visão geral do conceito de transações comerciais no Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 01/31/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2022-01-31
ms.openlocfilehash: 0c6fe583af0dcaa62204b35c1093746b13b6e00e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582218"
---
# <a name="business-transactions-in-project-operations"></a>Transações comerciais no Project Operations

_**Aplica-se a:** Project Operations para cenários baseados em recursos/não armazenados, implementação leve - negócio para faturação pró-forma_

No Microsoft Dynamics 365 Project Operations, a *transação comercial* é um conceito abstrato que não é representado por nenhuma entidade. No entanto, alguns campos e processos comuns nas entidades foram concebidos para utilizarem o conceito de transações comerciais. As seguintes entidades utilizam esta abstração:

- Detalhes de linha de proposta
- Detalhes de item de contrato
- Linhas de estimativa
- Linhas do diário
- Valores Reais

Destas entidades, os detalhes de linha de proposta, os detalhes de item de contrato e as linhas de estimativa são mapeados para a *fase de estimativa* no ciclo de vida do projeto. As entidades Linhas do diário e Valores reais são mapeadas para a *fase de execução* no ciclo de vida do projeto.

O Project Operations trata os registos destas cinco entidades como transações comerciais. A única distinção é que os registos nas entidades que são mapeadas para a fase de estimativa (Detalhes de linha de proposta, detalhes do item de contrato e Linhas de estimativa) são considerados *previsões financeiras*, ao passo que os registos nas entidades que são mapeadas para a fase de execução (Linhas do diário e Valores reais) são considerados *factos financeiros* que já ocorreram.

Para mais informações, consulte [Estimativas](../project-management/estimating-projects-overview.md) e [Valores Reais](actuals-overview.md).

## <a name="concepts-that-are-unique-to-business-transactions"></a>Conceitos que são exclusivos para as transações comerciais

Os seguintes conceitos são exclusivos para o conceito de transações comerciais:

- Tipo de transação
- Classe de transação
- Origem da transação
- Ligação da transação

### <a name="transaction-type"></a>Tipo de transação

O tipo de transação representa o tempo e o contexto do impacto financeiro num projeto. É definido por um conjunto de opções que tem os seguintes valores suportados no Project Operations:

- Custo
- Contrato do projeto
- Vendas não faturadas
- Vendas faturadas
- Vendas interorganizacionais
- Custo de unidade de atribuição de recursos

### <a name="transaction-class"></a>Classe de transação

A classe de transação representa os diferentes tipos de custos incorridos nos projetos. É definido por um conjunto de opções que tem os seguintes valores suportados no Project Operations:

- Tempo
- Despesa
- Material
- Taxa
- Marco
- Imposto

> [!NOTE]
> Normalmente, o valor **Marco** é utilizado pela lógica de negócio para a faturação de preço fixo no Project Operations.

### <a name="transaction-origin"></a>Origem da transação

A origem da transação é uma entidade que armazena a origem de cada transação de negócio para o ajudar com a capacidade de relatórios e monitorização. À medida que a execução do projeto é iniciada, cada transação comercial cria outra transação comercial que irá, por sua vez, criar outra transação comercial, e assim por diante.

### <a name="transaction-connection"></a>Ligação da transação

A ligação da transação é uma entidade que armazena a relação entre duas transações comerciais semelhantes, tais como o custo e os valores reais de vendas relacionados, ou reversões de transações acionados por atividades de faturação, como a confirmação ou correção de faturas.

Em conjunto, as entidades Origem da transação e Ligação da transação ajudam-no a monitorizar as relações entre as transações comerciais e as ações que causaram uma transação comercial específica a ser criada.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
