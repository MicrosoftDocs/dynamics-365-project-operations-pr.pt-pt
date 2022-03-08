---
title: Conceitos chave – Conceitos chave
description: Este tópico fornece informações sobre os conceitos chave de contratos de projeto no Project Operations.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fa00bd5b4a1179f38d5dfb63a47b39eec69c6ecf
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642152"
---
# <a name="project-contracts---key-concepts"></a>Conceitos chave – Conceitos chave

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Este tópico fornece os conceitos-chave de que deve estar ciente antes de começar a usar contratos de Projeto no Dynamics 365 Project Operations:

## <a name="owning-company"></a>Empresa Proprietária

A empresa proprietária é a entidade legal do módulo **Gestão de projetos e contabilística** para o Project Operations do Dynamics 365 Finance. A empresa proprietária representa a entidade legal que irá contabilizar o custo e as receitas que advêm de um negócio.

## <a name="contracting-unit"></a>Unidade de Contratação

A unidade de contratação representa a divisão ou a prática proprietária da entrega do projeto. Pode configurar os custos de recursos para cada unidade de contratação. Quando especificar o custo do recurso para um recurso, também poderá configurar diferentes taxas de custo para os recursos. Esta unidade de contratação empresta estes recursos de outras divisões ou práticas dentro da empresa. As taxas de custo para os recursos são referidas como preços de transferência, empréstimos de recursos ou preços de câmbio. Quando configura as taxas de custo a emprestar a recursos de outras divisões, use a moeda da divisão prestadora.

## <a name="cost-currency"></a>Moeda de Custo

A moeda de custo é a moeda em que os custos são reportados no ecrã. Esta moeda deriva da moeda anexada ao campo **Unidade de Contratação** no contrato e no projeto. Os custos podem ser registados em qualquer moeda para um projeto. No entanto, existe uma conversão da moeda em que os custos foram registados para a moeda de custo do projeto quando mostrada no ecrã.

Como as taxas de câmbio na plataforma Common Data Service (CDS) não podem ter vigência, os totais no ecrã para o custo podem mudar ao longo do tempo se atualizar as taxas de câmbio de moeda. No entanto, os custos tal como registados na base de dados permanecem inalterados, uma vez que os montantes são armazenados na moeda em que foram incorridos.

## <a name="sales-currency"></a>Moeda de Venda

A moeda de venda no Project Operations é a moeda em que os montantes de venda estimados e reais são registados e mostrados. A moeda das vendas é também a moeda em que o cliente é faturado para o negócio. Num contrato de projeto, a moeda de venda assume por predefinição o registo de cliente ou de conta, e pode ser alterada durante a criação do contrato. Quando um contrato é criado fechando uma proposta como ganha, a moeda do contrato assume a predefinição da moeda na proposta.

Quando cria um contrato de projeto de raiz, o campo **Moeda de Vendas** não pode ser editado. As listas de preços de produtos e projetos assumem por predefinição com base nesta moeda no contrato.

Ao contrário dos custos, os valores de venda só podem ser registados na moeda de vendas.

## <a name="billing-method"></a>Método de Faturação

Normalmente, existem dois tipos de modelos de contratação para projetos, taxas fixas e baseados no consumo. Estes modelos estão representados no Project Operations como métodos de faturação com dois valores possíveis:

- Tempo e Material: um modelo de contratação baseado no consumo em que cada custo incorrido é suportado pelas receitas correspondentes. À medida que estima ou incorre em mais custos, as vendas estimadas e reais correspondentes também aumentarão. Especifique limites a não exceder nos itens de contrato que têm este método de faturação que cobre as receitas reais. As receitas estimadas não são afetadas por limites a não exceder.
- Preço Fixo: um modelo de contratação de taxa fixa que indica que os valores de venda serão independentes dos custos incorridos. O valor de vendas é fixo e não é alterado à medida que estima ou incorre em mais custos.

## <a name="project-price-lists"></a>Listas de Preços de projetos

As listas de preços do projeto são utilizadas para assumir por predefinição os preços, e não taxas de custo, para o tempo, as despesas e outros componentes relacionados com o projeto. Pode haver várias listas de preços. Cada lista de preços tem a sua própria data de efetividade para cada contrato de projeto. A sobreposição da data efetiva em listas de preços de projeto não é suportada no Project Operations.

Quando um contrato de projeto é criado ganhando uma proposta de projeto, as listas de preços do projeto são copiadas com o nome do contrato e data incluída. Copiar estas informações constitui preços personalizados para componentes de projeto neste contrato de projeto.

## <a name="transaction-classes"></a>Classes de Transação

O Project Operations suporta quatro tipos de classes de transações:

- Tempo
- Despesa
- Material
- Taxa

Os valores de custos e vendas podem ser estimados e incorridos nas classes Tempo, Despesa e Transação de material. A tarifa é uma classe de transações só de receitas.

## <a name="work-entities-and-billing-entities"></a>Entidades de trabalho e entidades de Faturação

As entidades que representam o trabalho são projetos e tarefas. As entidades que representam os aspetos de faturação são itens de contrato. Pode associar diferentes entidades de trabalho a opções de faturação ao associá-las a itens de contrato.

## <a name="multi-customer-deals"></a>Negócios para vários clientes

Os negócios com vários clientes têm mais de um cliente para faturar num negócio. Os exemplos comuns incluem:

- Empresas OEM e seus parceiros: Parceiros e revendedores vendem um produto com alguns serviços de valor acrescentado, normalmente envolvendo um determinado negócio com um cliente. O OEM oferece-se para financiar uma parte do projeto. 

- Projetos do setor público: vários departamentos da administração pública local concordam em financiar um projeto e são faturados de acordo com uma divisão acordada previamente. Por exemplo, um agrupamento escolar ou a administração pública local concordam financiar a construção de uma piscina.

## <a name="invoice-schedules"></a>Agendas de Faturação

As agendas de faturação são específicas de cada item de contrato e são necessários para que a faturação automática funcione. As agendas de faturação são criadas com base em determinadas datas de início e de fim, e frequência da fatura. As agendas de faturação são utilizadas na fase de contrato quando o processo automático de criação de faturas está configurado. Quando um contrato de projeto é criado a partir de uma proposta, a agenda de faturação é copiada para o contrato de projeto a partir da proposta.

## <a name="changes-from-dynamics-365-sales-orders"></a>Alterações das Encomendas do Dynamics 365 Sales

Os contratos do Project Operations são criados em Encomendas no Dynamics 365 Sales. No entanto, existem desvios e diferenças importantes na funcionalidade. Os contratos têm um formulário e elementos de IU, regras de negócio, lógica de negócio em plug-ins e scripts do lado do cliente próprios que as tornam únicos das Encomendas. Por estas razões, não use uma encomenda de Vendas e um contrato do Project Operations alternadamente.
