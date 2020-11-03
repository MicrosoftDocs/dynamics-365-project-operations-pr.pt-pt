---
title: Conceitos chave da proposta de projeto
description: Este tópico fornece informações sobre como utilizar propostas de projeto no Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 64d2fd9bab9452d71e8cd194fbab70edadf00b93
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082328"
---
# <a name="project-quote-key-concepts"></a>Conceitos chave da proposta de projeto

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_


Seguem-se conceitos chave a ter em conta antes de começar a utilizar as propostas de projeto no Dynamics 365 Project Operations:

## <a name="contracting-unit"></a>Unidade de contratação

A unidade de contratação representa a divisão ou a prática proprietária da entrega do projeto. Pode configurar os custos de recursos para cada unidade de contratação. Quando especifica o custo do recurso para um recurso na unidade de contratação, também poderá configurar diferentes taxas de custo para os recursos que esta unidade de contratação toma emprestados, ou outra divisão ou práticas dentro da empresa. Estes são referidos como preços de transferência, empréstimos de recursos ou preços de câmbio. Quando configura o custo dos recursos tomadores de outras divisões, também pode optar por configurar essas taxas de custo na moeda da divisão prestadora.

## <a name="cost-currency"></a>Moeda de custo

A moeda de custo no Project Operations é a moeda em que os custos são reportados. Esta moeda deriva da moeda anexada ao campo **Unidade de contratação** na proposta, contrato e projeto. Os custos podem ser registados em qualquer moeda para um projeto. No entanto, existe uma conversão da moeda em que os custos foram registados para a moeda de custo do projeto.

Como as taxas de câmbio na plataforma CDS não podem ter vigência, os totais no ecrã para o custo podem mudar ao longo do tempo se atualizar as taxas de câmbio de moeda. No entanto, os custos registados na base de dados permanecem inalterados, uma vez que os montantes são armazenados na moeda em que foram incorridos.

## <a name="sales-currency"></a>Moeda de venda

A moeda de venda no Project Operations é a moeda em que os montantes de venda estimados e reais são registados e mostrados. Também é a moeda em que o cliente é faturado para o negócio. Numa proposta de projeto, a moeda de venda assume por predefinição o registo de cliente ou de conta, e pode ser alterada quando a proposta é criada. Depois de a proposta ser guardada, a moeda de venda não pode ser alterada. As listas de preços de produtos e projetos assumem por predefinição com base na moeda de venda da proposta.

Ao contrário dos custos, os valores de venda só podem ser registados na moeda de Vendas.

## <a name="billing-method"></a>Método de faturação

Normalmente, os projetos têm taxas fixas e modelos de contratação baseados no consumo. Isto é representado no Project Operations como **Método de Faturação** e tem dois valores, tempo e material, e preço fixo.

- **Tempo e material:** trata-se de um modelo de contrato baseado no consumo em que cada custo incorrido é suportado pelas receitas correspondentes. À medida que estima ou incorre em mais custos, as vendas estimadas e reais correspondentes também aumentarão. Pode especificar limites a não exceder nas linhas de proposta que têm este método de faturação. Isto definirá um máximo das receitas reais. As receitas estimadas não são afetadas por limites a não exceder.
- **Preço fixo:** trata-se de um modelo de contrato de taxa fixa que indica que os valores de venda serão independentes dos custos incorridos. O valor de vendas é fixo e não é alterado à medida que estima ou incorre em mais custos.

## <a name="project-price-lists"></a>Listas de preços de projetos

As listas de preços do projeto são listas de preços que são utilizadas para assumir por predefinição os preços, e não taxas de custo, para o tempo, as despesas e outros componentes relacionados com o projeto. Podem existir várias listas de preços, e cada lista pode ter a sua própria data efetiva para cada proposta de projeto. A sobreposição da data efetiva em listas de preços de projeto não é suportada no Project Operations.

## <a name="product-price-lists"></a>Listas de preços de produtos

As listas de preços do produto são listas de preços que são utilizadas para assumir por predefinição os preços, e não taxas de custo, para as listas baseadas em produtos numa proposta. Só existe uma lista de preços do produto por proposta.

## <a name="transaction-classes"></a>Classe de transação

O Project Operations suporta quatro tipos de classes de transações:

- Tempo
- Despesa
- Material
- Taxa

Os valores de custos e vendas podem ser estimados e incorridos nas classes Tempo, Despesa e Transação de material. A tarifa é uma classe de transações só de receitas.

## <a name="work-entities-and-billing-entities"></a>Entidades de trabalho e entidades de faturação

As entidades que representam o trabalho são Projetos e Tarefas. As entidades que representam a faturação são as Linhas de proposta e os Itens de contrato. Pode associar diferentes entidades de trabalho a opções de faturação ao associá-las a Linhas de proposta ou Itens de contrato.

## <a name="multi-customer-deals"></a>Negócios para vários clientes

Os negócios com vários clientes ocorrem quando existe mais de um cliente para faturar. Os exemplos comuns incluem:

- **Empresas OEM e os seus parceiros:** os parceiros e os revendedores vendem um produto com serviços de valor acrescentado. Normalmente, este é um cenário em que, durante um determinado negócio com um cliente, o OEM oferece-se para financiar uma parte do projeto. 

- **Projetos do setor público:** vários departamentos da administração pública local concordam em financiar um projeto e são faturados de acordo com uma divisão acordada previamente. Por exemplo, um agrupamento escolar e a cidade ou o departamento da administração pública local concordam financiar a construção de uma piscina.

## <a name="invoice-schedules"></a>Agendas de faturação

As agendas de faturação são específicas de cada linha de proposta e também são opcionais. As agendas de faturação são criadas com base em determinadas datas de início e de fim, e frequência da fatura. As agendas de faturação são utilizadas na fase de contrato quando o processo automático de criação de faturas está configurado. Na fase de proposta, as agendas são opcionais. Quando as agendas da faturação são criadas na fase **Proposta** , são copiadas para o contrato de projeto que é criado quando uma proposta de projeto é ganha.

## <a name="changes-from-dynamics-365-sales-quote"></a>Alterações da proposta do Dynamics 365 Sales:

As propostas do Project Operations são criadas nas propostas do Dynamics 365 Sales. No entanto, existem algumas diferenças importantes na funcionalidade que deve conhecer:

- As ações **Rever** e **Ativar** não são suportadas.
- As propostas do Project Operations têm dois tipos de linhas diferentes. Uma é para os projetos e a outra é para os produtos.
- As propostas do Project Operations têm um formulário e elementos de IU, regras de negócio, lógica de negócio em plug-ins e scripts do lado do cliente próprios que as tornam únicos nas propostas de Vendas.

Por estas razões, não é recomendado utilizar uma proposta do Sales e uma proposta do Project Operations indistintamente.
