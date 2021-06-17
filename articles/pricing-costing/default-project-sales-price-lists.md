---
title: Lista de preços predefinida
description: Este tópico fornece informação sobre as listas de preços de custos e vendas predefinidas no Project Operations.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c204a8f0364a4be39974b101e834d4465b99f769
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000495"
---
# <a name="default-price-lists"></a>Lista de preços predefinida

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

## <a name="sales-price-lists"></a>Listas de preços de venda

Cada cotação e contrato de projeto no Dynamics 365 Project Operations contém uma lista de preços de venda padrão. 

### <a name="price-list-default-on-project-quotes"></a>A lista de preços é assumida como predefinição nas propostas de projeto
O sistema completa o seguinte processo para determinar qual a lista de preços a assumir a predefinição numa proposta de projeto:

1. O sistema analisa as listas de preços que estão anexadas às listas de preços do projeto da conta. 
2. Se houver listas de preços de projeto anexadas ao registo da conta, o sistema analisa as listas de preços de vendas anexadas aos parâmetros de projeto que correspondem à moeda da proposta de projeto.
3. Em seguida, o sistema verifica a efetividade da data das listas de preços que correspondem ao intervalo de datas da proposta de projeto. Especificamente, a data em que a proposta foi criada.
4. Se existirem várias listas de preços que são efetivas para a data da proposta do projeto, todas as listas de preços assumem a predefinição na proposta do projeto.
5. Se não houver listas de preços em vigor para a data da proposta do projeto, não há uma lista de preços do projeto predefinida na proposta do projeto. Uma mensagem de aviso ocorrerá na proposta do projeto. A mensagem indica que os valores reais e estimativas no projeto não terão preço porque não existem listas de preços do projeto anexadas.

### <a name="price-list-default-on-project-contracts"></a>A lista de preços assume a predefinição nos contratos de projeto 
O sistema completa o seguinte processo para determinar qual a lista de preços a assumir a predefinição num contrato de projeto:

1. Se o contrato for criado a partir de uma proposta, as listas de preços do projeto na proposta são copiadas separadamente e anexadas ao contrato de projeto.
2. Se o contrato for criado de raiz, o sistema analisa as listas de preços que estão anexadas às listas de preços do projeto da conta. Se não houver listas de preços de projeto anexadas ao registo da conta, o sistema analisa as listas de preços de vendas anexadas aos parâmetros de projeto que correspondem à moeda do contrato de projeto.
4. Em seguida, o sistema verifica a efetividade da data das listas de preços que correspondem ao intervalo de datas do contrato de projeto. Especificamente, a data em que o contrato foi criado.
5. Se existirem várias listas de preços que são efetivas para a data do contrato do projeto, todas as listas de preços assumem a predefinição no contrato do projeto.
6. Se não houver listas de preços em vigor para a data do contrato do projeto, não há listas de preços do projeto predefinidas no contrato do projeto. Uma mensagem de aviso ocorrerá no contrato do projeto. A mensagem indica que os valores reais e estimativas no projeto não terão preço porque não existem listas de preços do projeto anexadas.

## <a name="cost-price-lists"></a>Listas de preços de custo

As listas de preços de custo não assumem a predefinição de nenhuma entidade no Project Operations. A determinação da lista de preços de custo a utilizar para os custos do projeto é sempre feita no momento. O sistema completa o seguinte processo para determinar qual a lista de preços a usar para custos de projeto:

1. O sistema analisa primeiro as listas de preços que estão anexadas à unidade de organização contratante do projeto.
2. O sistema analisa então a efetividade da data das listas de preços que correspondem à data da estimativa de entrada ou linha real. Nesta situação, a *linha de estimativa* refere-se aos três contextos de estimativa no Project Operations:

    - Linha de estimativa do projeto
    - Detalhe de linha de proposta
    - Detalhe de item de contrato
  
3. Se existirem várias listas de preços que são efetivas para a data na estimativa de entrada ou real, a lista de preços criada mais recentemente é selecionada.
4. Se não houver listas de preços anexadas à unidade da organização contratante do projeto, o sistema analisa as listas de preços de custo anexadas aos parâmetros de projeto que correspondem à moeda do projeto.
5. Em seguida, o sistema analisa então a efetividade da data das listas de preços que correspondem à data da estimativa de entrada ou linha real. 
6. Se existirem várias listas de preços que são efetivas para a data na estimativa de entrada ou real, a lista de preços criada mais recentemente é selecionada.
7. Se não houver listas de preços de custo anexadas aos parâmetros do projeto que correspondam à moeda e à data efetiva, o sistema predefine a taxa de custo para zero (0) na estimativa de entrada ou na linha real.


[!INCLUDE[footer-include](../includes/footer-banner.md)]