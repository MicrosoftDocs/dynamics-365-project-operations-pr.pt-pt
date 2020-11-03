---
title: Listas de preços de projetos
description: Este tópico fornece informações sobre a entidade da lista de preços do Projeto.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1a69cf51ca8cde8260f4136cf1b2e936f99b112a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082630"
---
# <a name="project-price-lists"></a>Listas de preços de projetos

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

O Dynamics 365 Project Operations alarga a entidade da lista de preços no Dynamics 365 Sales. 

## <a name="key-entities"></a>Entidades principais

Uma lista de preços inclui as informações fornecidas por quatro entidades diferentes:

- **Lista de Preços** : Esta entidade armazena informações sobre o contexto, a moeda, a data efetiva e a unidade de tempo para o tempo de definição de preços. O contexto mostra se a lista de preços expressa taxas de custo ou taxas de venda. 
- **Moeda** : Esta entidade armazena a moeda de preços da lista de preços. 
- **Data** : Esta entidade é utilizada quando o sistema tenta introduzir um preço predefinido numa transação. Uma lista de preços que tem a data efetiva que inclui a data da transação é selecionada. Se for encontrada mais de uma lista de preços efetiva para a data da transação e for anexada à proposta, ao contrato ou à unidade organizacional relacionada, nenhum preço será predefinido. 
- **Tempo** : Esta entidade armazena a unidade de tempo em que os preços são expressos, tais como taxas diárias ou horárias. 

A entidade Lista de preços tem três tabelas relacionadas que armazenam preços:

  - **Preço da Função** : Esta tabela armazena uma taxa para uma combinação de valores de funções e unidades organizacionais, sendo utilizada para configurar preços baseados em funções para os recursos humanos.
  - **Preço da Categoria de Transação** : Esta tabela armazena preços por categoria de transação e é utilizada para configurar preços da categoria de despesa.
  - **Itens da Lista de Preços** : Esta tabela armazena preços para produtos de catálogos.
 
A lista de preços é um cartão de taxas. Um cartão de taxas é uma combinação da entidade Lista de Preços e linhas relacionadas nas tabelas Preço da Função, Preço da Categoria de Transação e Itens da Lista de Preços.

## <a name="resource-roles"></a>Funções do recurso

O termo *função do recurso* refere-se a um conjunto de qualificações, competências e certificações que uma pessoa tem de ter para executar um conjunto de tarefas específicas num projeto.

O tempo dos recursos humanos é proposto com base na função que um recurso preenche num projeto específico. Para o tempo dos recursos humanos, os custos e a faturação são baseados na função do recurso. O tempo pode ser o preço definido em qualquer unidade no grupo de unidades **Tempo**.

O grupo de unidades **Tempo** é criado quando instala Operações de projeto. Tem uma unidade de **Hora** predefinida. Não é possível eliminar, mudar o nome ou editar os atributos do grupo de unidades **Tempo** ou da unidade **Hora**. No entanto, pode adicionar outras unidades ao grupo de unidades **Tempo**. Se tentar eliminar o grupo de unidades **Tempo** ou a unidade **Hora** , poderá causar falhas na lógica de negócio.
 
## <a name="transaction-categories-and-expense-categories"></a>Categorias de transação e categorias de despesa

As despesas de viagem e outras despesas incorridas pelos consultores de projeto são faturadas ao cliente. Os preços das categorias de despesa é completado utilizando as listas de preços. A tarifa aérea, o hotel e o aluguer do automóvel são exemplos de categorias de despesa. Cada linha da lista de preços para despesas especifica os preços para uma categoria de despesa específica. Os três métodos seguintes são utilizados para as categorias de despesas de preço:

- **De custo** : O custo das despesas é faturado ao cliente e não é aplicada nenhuma margem de lucro.
- **Percentagem da margem de lucro** : A percentagem sobre o custo real é faturada ao cliente. 
- **Preço unitário** : Um preço de faturação é definido para cada unidade da categoria de despesa. O montante que é faturado a um cliente é calculado com base no número de unidades de despesa que o consultor reporta. A quilometragem utiliza o método de definição de preços por preço unitário. Por exemplo, a categoria de despesa Quilometragem pode ser configurada para 30 dólares norte-americanos (USD) por dia ou 2 USD por milha. Quando um consultor reporta a quilometragem num projeto, o montante a faturar é calculado com base no número de milhas reportadas pelo consultor.
 
## <a name="project-sales-pricing-and-overrides"></a>Substituições e definição de preços de vendas do projeto

Para obter propostas e contratos do projeto, uma lista de preços do projeto tem um padrão de substituição de preços diferente da lista de preços de produtos. Num item de proposta baseado no catálogo de produtos, pode substituir o preço por funções e categorias diretamente na linha de proposta, porque cada linha de proposta aponta para exatamente um item de catálogo. No entanto, numa linha de proposta com base em projetos, não pode substituir o preço por funções e categorias diretamente na linha de proposta. Use a lista de preços do projeto para suportar os dois padrões distintos de definição manual.

> [!NOTE]
> Recomendamos que tenha uma lista de preços separada para os recursos do seu projeto e itens do catálogo, devido às diferenças de comportamento entre os dois quando os preços são substituídos.

Cada uma das seguintes entidades pode ter uma ou mais listas de preços de venda associadas para a definição de preços do projeto:

- Cliente (conta) 
- Oportunidade 
- Proposta 
- Contrato do Projeto

A associação destas entidades com uma lista de preços é indicada pelas listas de preços do projeto. Pode associar uma ou mais listas de preços às entidades de vendas Cliente, Oportunidade, Proposta e Contrato do Projeto.

Uma lista de preços predefinida do projeto não é introduzida automaticamente num registo de cliente. No entanto, pode anexar manualmente uma lista de preços do projeto ao registo de cliente. No entanto, deverá anexar manualmente uma lista de preços do projeto quando tiver um contrato de preços personalizado com o cliente. 

Quando uma lista de preços do projeto é associada a uma entidade de vendas, as seguintes informações são validadas:

- A lista de preços tem um contexto de **Vendas**. 
- A moeda da lista de preços corresponde com a moeda do cliente. 

Num contrato do projeto, a seguinte ordem de precedência para definir automaticamente as listas de preços relacionadas com os projetos:

1. Proposta
2. Oportunidade
3. Cliente 
4. Definições globais 

Quando uma lista de preços do projeto é introduzida por predefinição, o sistema valida que a moeda corresponde com a moeda do cliente e que as listas de preços predefinidas que foram introduzidas têm um contexto de **Vendas**.

Pode associar várias listas de preços do projeto às entidades Cliente, Oportunidade, Proposta e Contrato do Projeto. Esta capacidade suporta preços predefinidos específicos de data para um contrato do projeto de execução demorada, onde poderá necessitar de mais de uma lista de preços para contabilizar as atualizações de preços que ocorrem devido à inflação. No entanto, se as listas de preços associadas è entidade Cliente, Oportunidade, Proposta ou Contrato do Projeto tiverem a data efetiva sobreposta, os preços predefinidos poderão estar incorretos. Consequentemente, deve certificar-se de que as listas de preços do projeto que têm a data efetiva sobreposta não estão associadas a essas entidades.

### <a name="deal-specific-price-overrides"></a>Substituição de preços específica de um negócio

É possível criar substituições específicas de um negócio para os preços selecionados nas listas de preços do projeto que são introduzidas por predefinição numa proposta ou contrato do projeto.

Por predefinição, um contrato do projeto obtém sempre uma cópia da lista de preços de vendas principal em vez de uma ligação direta para a mesma. Este comportamento ajuda a garantir que os contratos de preços efetuados com um cliente para uma declaração de trabalho (SOW) não sejam alterados se a lista de preços principal for alterada.

No entanto, numa proposta, pode utilizar uma lista de preços principal. Em alternativa, pode copiar uma lista de preços principal e editá-la para criar uma lista de preços personalizada que só se aplica a essa proposta. Para criar uma nova lista de preços específica de uma proposta, na página **Proposta** , selecione **Criar lista de preços personalizada**. Pode aceder à lista de preços do projeto específica do negócio a partir da proposta. 

Quando cria uma lista de preços do projeto personalizada, só são copiados os componentes do projeto da lista de preços. Por outras palavras, uma nova lista de preços criada como cópia da lista de preços do projeto existente que está anexada à proposta e esta nova lista de preços só tem preços de função e preços de categoria de transação relacionados.
  
## <a name="tracking-costs"></a>Controlo dos custos

As Operações do projeto monitorizam os custos da utilização de tempo de recursos humanos em projetos. Também monitoriza os custos de outras despesas incorridas durante o projeto, tais como as despesas de viagem.

Assim como as taxas de faturação, as taxas de custo de recursos humanos também são configuradas utilizando listas de preços. Eis as principais diferenças no comportamento da lista de preços de custo e da lista de preços de vendas:

- A taxa de custo de um recurso não pode ser substituída num determinado projeto, contrato ou proposta. No entanto, as taxas de faturação podem ser substituídas por negócio se forem efetuadas alterações específicas da natureza do negócio. 

- A seguinte ordem é utilizada para resolver uma lista de preços de custo:

    1. A lista de preços de custo associada à unidade organizacional.
    2. A lista de preços de custo é anexada aos parâmetros das operações do projeto. Visto que as listas de preços de custo em muitas moedas diferentes podem ser anexadas aos parâmetros, uma correspondência de moeda é completada entre a moeda da unidade organizacional de contratação do projeto, o contrato ou a proposta e a moeda da lista de preços de custo.
    3. Quanto às despesas, os métodos de definição de preços de custo e margem de lucro sobre o custo não se aplicam às listas de preços de custo. Mesmo que estes métodos de definição de preços sejam utilizados em linhas da lista de preços de custo para configurar os custos da categoria de transação, o sistema ignora-os e não é introduzido nenhum preço de custo predefinido.
