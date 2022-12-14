---
title: Conceitos exclusivos de propostas baseadas em projetos
description: Este artigo fornece informações sobre propostas de projeto no Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/02/2022
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 89867cfbe92f47d58b16da40b62d3d9dd6a15b64
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824342"
---
# <a name="concepts-unique-to-project-based-quotes"></a>Conceitos exclusivos de propostas baseadas em projetos

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

Antes de começar a utilizar propostas de projeto no Microsoft Dynamics 365 Project Operations, deve estar ciente dos seguintes conceitos-chave.

## <a name="owning-company"></a>Empresa proprietária

A empresa proprietária representa a entidade legal que é a detentora da entrega do projeto. O cliente na proposta deverá ser um cliente válido nessa entidade legal em aplicações de finanças e operações. A moeda da empresa proprietária e a moeda da unidade de contratação selecionada numa proposta baseada em projeto têm de corresponder.

## <a name="contracting-unit"></a>Unidade de contratação

Uma unidade de contratação representa a divisão ou a prática proprietária da entrega do projeto. Pode configurar os custos de recursos para cada unidade de contratação. Quando especifica os custos do recurso para um recurso numa unidade de contratação, pode configurar diferentes taxas de custo para os recursos que a unidade de contratação toma emprestados, ou para outras divisões ou práticas na empresa. Estas taxas de custo são referidas como preços de transferência, empréstimos de recursos ou preços de câmbio. Quando configura o custo dos recursos tomadores de outras divisões, pode configurar as taxas de custo na moeda da divisão prestadora.

## <a name="cost-currency"></a>Moeda de custo

A moeda de custo no Project Operations é a moeda em que os custos são reportados. Esta moeda deriva da moeda que está anexada ao campo **Unidade de contratação** na proposta, contrato e projeto. Os custos para um projeto podem ser registados em qualquer moeda. No entanto, existe conversão da moeda em que os custos foram registados para a moeda de custo do projeto.

Como as taxas de câmbio na plataforma do Dataverse não podem ter vigência, os totais no ecrã para o custo poderão mudar ao longo do tempo se atualizar as taxas de câmbio de moeda. No entanto, os custos que estão registados na base de dados permanecem inalterados, uma vez que os montantes são armazenados na moeda em que foram incorridos.

## <a name="sales-currency"></a>Moeda de venda

A moeda de venda no Project Operations é a moeda em que os montantes de venda estimados e reais são registados e mostrados. Também é a moeda em que o cliente é faturado para o negócio. Para uma proposta de projeto, uma moeda de venda é predefinida do registo de cliente ou de conta, e pode ser alterada quando a proposta é criada. No entanto, a moeda de venda não pode ser alterada depois de a proposta ser guardada. As listas de preços de produto e de projetos são definidas com base na moeda de venda da proposta.

Ao contrário dos custos, os valores de venda **só** podem ser registados na moeda de vendas.

## <a name="billing-method"></a>Método de faturação

Normalmente, os projetos têm taxas fixas e modelos de contratação baseados no consumo. No Project Operations, o modelo de contratação de um projeto é representado pelo método de faturação. O método de faturação tem dois valores: tempo e material e preço fixo.

- **Tempo e material** — trata-se de um modelo de contratação baseado no consumo em que cada custo incorrido é suportado pelas receitas correspondentes. À medida que estima ou incorre em mais custos, as vendas estimadas e reais correspondentes também aumentarão. Pode especificar limites a não exceder nas linhas de proposta que têm este método de faturação. Desta forma, pode limitar a receita real. As receitas estimadas não são afetadas por limites a não exceder.
- **Preço fixo** – um modelo de contratação de taxa fixa onde os valores de venda são independentes dos custos incorridos. O valor de vendas é fixo e não é alterado à medida que estima ou incorre em mais custos.

## <a name="project-price-lists"></a>Listas de preços de projetos

As listas de preços do projeto são listas de preços que são utilizadas para introduzir preços predefinidos, e não taxas de custo, para o tempo, as despesas e outros componentes relacionados com o projeto. Podem existir várias listas de preços, e cada lista pode ter a sua própria data efetiva para cada proposta de projeto. O Project Operations não suporta datas efetivas sobrepostas para listas de preços de projeto.

## <a name="product-price-lists"></a>Listas de preços de produtos

As listas de preços do produto são listas de preços que são utilizadas para introduzir preços predefinidos, e não taxas de custo, para as listas baseadas em produtos numa proposta. Só existe uma lista de preços do produto por proposta.

## <a name="transaction-classes"></a>Classe de transação

O Project Operations suporta quatro tipos de classes de transações:

- Tempo
- Despesa
- Material
- Taxa

Os valores de custos e vendas podem ser estimados e incorridos nas classes de transação **Tempo**, **Despesa** e **Material**. **Honorários** é uma classe de transações só de receitas.

## <a name="work-entities-and-billing-entities"></a>Entidades de trabalho e entidades de faturação

Projetos e Tarefas são entidades que representam o trabalho. As Linhas de proposta e os Itens de contrato são entidades que representam faturação. Pode associar diferentes entidades de trabalho a opções de faturação ao associá-las a Linhas de proposta ou Itens de contrato.

## <a name="multi-customer-deals"></a>Negócios para vários clientes

Os negócios com vários clientes ocorrem quando existe mais de um cliente por fatura. Eis alguns exemplos típicos:

- **Empresas de fabricante de equipamento original (OEM) e os seus parceiros:** — Os parceiros e os revendedores vendem um produto que inclui serviços de valor acrescentado. Durante um negócio com um cliente, o OEM, normalmente, oferece-se para financiar parte do projeto.
- **Projetos do setor público** — Vários departamentos da administração pública local concordam em financiar um projeto e são faturados de acordo com uma divisão acordada previamente. Por exemplo, um agrupamento escolar e a cidade ou o departamento da administração pública local concordam financiar a construção de uma piscina.

## <a name="invoice-schedules"></a>Agendas de faturação

As agendas de faturação são específicas de cada linha de proposta e são opcionais. As agendas de faturação são criadas com base em datas de início e de fim específicas e uma frequência da fatura. São utilizadas durante a fase de contrato, quando o processo automático de criação de faturas é configurado. Durante a fase de proposta, as agendas de fatura são opcionais. Se forem criadas durante a fase de proposta, são copiadas para o contrato de projeto que é criado quando uma proposta de projeto é ganha.

## <a name="differences-from-dynamics-365-sales-quotes"></a>Diferenças das propostas do Dynamics 365 Sales

As propostas do Project Operations são criadas em propostas do Dynamics 365 Sales. No entanto, existem algumas diferenças importantes na funcionalidade que deve conhecer:

- As propostas do Project Operations têm dois tipos diferentes de itens: um para projetos e outro para produtos.
- As propostas do Project Operations têm a sua própria página e elementos da interface de utilizador (IU), regras de negócio, lógica de negócio em plug-ins e scripts do lado do cliente próprios que as tornam distintos nas propostas do Sales.
- No Sales, pode anexar várias encomendas a uma única proposta de vendas. No Project Operations, pode anexar apenas um contrato de projeto a uma proposta do projeto.
- Quando ganha uma proposta de vendas, a oportunidade relacionada pode permanecer aberta. Depois de uma proposta de projeto ser ganha, a oportunidade relacionada é fechada.
- Uma proposta de vendas não inclui alguns campos e conceitos incluídos numa proposta de projeto. Os campos incluem **Unidade de Contratação**, **Gestor de Contas** e **Nome do Contacto para Faturação**.
- As propostas do Sales e do projeto são identificadas por um campo **Tipo** baseado no conjunto de opções. Para uma proposta de vendas, o valor deste campo é **Baseado em item**. Para uma proposta do projeto, valor é **Baseado em trabalho**.

Devido a estas diferenças, não recomendamos que utilize propostas do Sale e do Project Operations alternadamente.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
