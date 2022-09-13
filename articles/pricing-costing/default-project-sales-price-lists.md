---
title: Lista de preços predefinida
description: Este artigo fornece informações sobre vendas e listas de preços de custo predefinidos no Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 50dbf74e31b9eb8d63c378e5fd718dc17c9691f4
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410277"
---
# <a name="default-price-lists"></a>Lista de preços predefinida

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

## <a name="sales-price-lists"></a>Listas de preços de venda

Cada cotação e contrato de projeto no Dynamics 365 Project Operations contém uma lista de preços de venda padrão. 

### <a name="price-list-default-on-project-quotes"></a>A lista de preços é assumida como predefinição nas propostas de projeto
O sistema completa o seguinte processo para determinar qual a lista de preços a assumir a predefinição numa proposta de projeto:

1. O sistema analisa as listas de preços que estão anexadas às listas de preços do projeto da conta. 
1. Se não houver listas de preços de projeto anexadas ao registo da conta, o sistema analisa as listas de preços de vendas anexadas aos parâmetros de projeto que correspondem à moeda da proposta de projeto.
1. Em seguida, o sistema verifica a efetividade da data das listas de preços que correspondem ao intervalo de datas da proposta de projeto. Especificamente, a data em que a proposta foi criada.
1. Se existirem várias listas de preços que são efetivas para a data da proposta do projeto, todas as listas de preços assumem a predefinição na proposta do projeto.
1. Se não houver listas de preços em vigor para a data da proposta do projeto, não há uma lista de preços do projeto predefinida na proposta do projeto. Uma mensagem de aviso ocorrerá na proposta do projeto. A mensagem indica que os valores reais e estimativas no projeto não terão preço porque não existem listas de preços do projeto anexadas.

### <a name="price-list-default-on-project-contracts"></a>A lista de preços assume a predefinição nos contratos de projeto 
O sistema completa o seguinte processo para determinar qual a lista de preços a assumir a predefinição num contrato de projeto:

1. Se o contrato for criado a partir de uma proposta, as listas de preços do projeto na proposta são copiadas separadamente e anexadas ao contrato de projeto.
1. Se o contrato for criado de raiz, o sistema analisa as listas de preços que estão anexadas às listas de preços do projeto da conta. Se não houver listas de preços de projeto anexadas ao registo da conta, o sistema analisa as listas de preços de vendas anexadas aos parâmetros de projeto que correspondem à moeda do contrato de projeto.
1. Em seguida, o sistema verifica a efetividade da data das listas de preços que correspondem ao intervalo de datas do contrato de projeto. Especificamente, a data em que o contrato foi criado.
1. Se existirem várias listas de preços que são efetivas para a data do contrato do projeto, todas as listas de preços assumem a predefinição no contrato do projeto.
1. Se não houver listas de preços em vigor para a data do contrato do projeto, não há listas de preços do projeto predefinidas no contrato do projeto. Uma mensagem de aviso ocorrerá no contrato do projeto. A mensagem indica que os valores reais e estimativas no projeto não terão preço porque não existem listas de preços do projeto anexadas.

## <a name="cost-price-lists"></a>Listas de preços de custo

As listas de preços de custo não assumem a predefinição de nenhuma entidade no Project Operations. A determinação da lista de preços de custo a utilizar para os custos do projeto é sempre feita por transação. O sistema completa o seguinte processo para determinar qual a lista de preços a usar para custos de projeto:

1. O sistema analisa as listas de preços que estão anexadas à unidade de organização contratante do projeto.
1. Em seguida, o sistema analisa então a efetividade da data das listas de preços que correspondem ao contexto estimado ou contexto real de entrada.

    - O *Contexto estimado* refere-se a qualquer um dos três contextos de estimativa no Project Operations:

        - Linha de estimativa do projeto
        - Detalhe de linha de proposta
        - Detalhe de item de contrato

    - O *Contexto real* refere-se a qualquer uma das origens reais no Project Operations:

       - Linhas de entrada do diário que são criadas manualmente ou linhas de correção do dirário que são criadas num diário de correção
       - Linhas do diário que são criadas durante a submissão de registos de tempo, despesas ou utilização de materiais
       - Detalhe de linha de fatura

    Quando o Project Operations faz a correspondência da efectividade de data da linha do diário de entrada ou do detalhe da linha de fatura no *contexto real*, utiliza o campo **Data da transação**.

    - Se várias listas de preços forem efetivas para a data do contexto de estimativa de entrada ou contexto real, a lista de preços criada mais recentemente é selecionada.
    - Se não forem anexadas listas de preços à unidade da organização contratante do projeto, o sistema analisa as listas de preços de custo que estão anexadas aos parâmetros de projeto que correspondem à moeda do projeto.

## <a name="enable-multi-currency-cost-price-list"></a>Ativar lista de preços de custo com várias moedas

Esta definição pode ser encontrada em **Definições** \> **Parâmetros**. O valor predefinido é **Não**.

Quando esta definição está ativada (ou seja, o valor está definido como **Sim**), o sistema comporta-se da seguinte forma:

- Permite que as listas de preços de custo em qualquer moeda sejam associadas à unidade organizacional. Por exemplo, é possível anexar uma lista de preços de custo na moeda EUR a uma unidade organizacional na moeda USD. O sistema continuará a validar se as listas de preços de custo que estão anexadas a uma unidade organizacional não têm sobreposição de efetividade de datas.
- Valida que as listas de preços de custo anexadas aos parâmetros do projeto não têm sobreposição de efetividade de datas, mesmo que tenham moedas diferentes. Este comportamento é diferente do comportamento predefinido (ou seja, o comportamento quando o valor está definido como **Não**). No comportamento predefinido, apenas as listas de preços de custo que têm a **mesma** moeda são validadas para a não sobreposição de efetividade de datas.
- Para um contexto de transações a receber, determina a lista de preços de custo com base apenas na efetividade de data. Este comportamento é diferente do comportamento predefinido, em que o sistema selecciona a lista de preços de custo que corresponde à moeda do projeto e à efetividade da data.

Devido a estas alterações de comportamento, os clientes do Project Operations irão conseguir manter uma lista de preços de custo global que será relevante para toda a empresa. Não terão de ter listas de preços em cada moeda de operações. A lista de preços global terá data de efeitividade e irá permitir configurar taxas de custo em qualquer moeda para uma combinação específica de valores da dimensão de definição de preços. A moeda da lista de preços de custo é apenas utilizada para introduzir valores predefinidos quando os registos dos itens **Preços de função**, **Preços de categoria** e **Lista de preços** são criados. Não será utilizado para determinar a lista de preços.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
