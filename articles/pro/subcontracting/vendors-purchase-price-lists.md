---
title: Gestão da lista de preços de compra e de fornecedor no Project Operations
description: Este tópico fornece informações que o ajudarão a criar e manter os dados do fornecedor e as listas de preços de compra para subcontratação.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cf62ef8eb87ac2bc138e63c7f92132e00451df6d7766291a8399a94a070799ab
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994155"
---
# <a name="vendor-and-purchase-price-list-management-in-project-operations"></a>Gestão da lista de preços de compra e de fornecedor no Project Operations

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

## <a name="vendors-in-project-operations"></a>Fornecedores no Project Operations

No Microsoft Dynamics 365 Project Operations, as contas de fornecedor têm um tipo de relação de **Fornecedor** ou **Prestador**. Pode selecionar apenas um registo de conta que tenha um destes tipos de relação como fornecedor num subcontrato.

Pode associar uma ou mais listas de preços de compra a um registo de fornecedor. No entanto, cada lista de preços de compra associada a um registo de fornecedor deve ter uma data efetiva distinta. O Project Operations não suporta datas efetivas sobrepostas para listas de preços de compra.

Por predefinição, os seguintes campos e conceitos num registo de fornecedor são utilizados para qualquer subcontrato criado para o fornecedor:

- Prazos de pagamento
- Contacto para faturação
- Contacto principal

    > [!NOTE]
    > Por predefinição, o contacto principal do fornecedor é utilizado como gestor de conta do fornecedor do subcontrato.

- Moeda
- Listas de preços de compra atuais

## <a name="purchase-price-lists-in-project-operations"></a>Listas de preços de compra no Project Operations

Uma lista de preços onde o campo **Contexto** está definido como **Compra** é considerada uma lista de preços de compra. As listas de preços de compra podem ser definidas para representar um catálogo de taxas de compra para tempo, despesas e materiais. As listas de preços de compra assemelham-se às listas de preços de venda e custos no Project Operations. Os seguintes conceitos aplicam-se às listas de preços de compra da mesma forma que se aplicam às listas de preços de venda e custos:

- **Data efetiva** - As listas de preços de compra têm uma data efetiva. A data efetiva é representada pelos campos de data de início e data de fim em cada lista de preços. O tempo entre a data de início e a data de fim é o período de data efetiva.
- **Moeda** – A moeda no cabeçalho da tabela de preços é usada como a moeda em que os preços de compra são expressos para mão-de-obra, categorias de despesas e produtos no catálogo.
- **Unidade de tempo predefinida** – A unidade de tempo predefinida exprime os preços de mão-de-obra para compras. O campo de unidade de tempo numa lista de preços é utilizado apenas para fornecer um valor predefinido. Esse valor pode ser alterado nas linhas de preço de função individual.

As listas de preços de compra podem ser anexadas aos registos dos fornecedores como associações conhecidas como listas de preços do projeto. Estas listas de preços são usadas para introduzir preços predefinidos em itens de subcontrato. Por predefinição, quando várias listas de preços de compra são anexadas a um registo de fornecedor, a lista de preços mais atual é usada para subcontratos que são criados para o fornecedor. Apenas as listas de preços em que o campo **Contexto** está definido como **Compra** podem ser anexadas aos registos do fornecedor.

### <a name="subcontract-specific-purchase-price-lists"></a>Listas de preços de compra específicas de subcontratos

As listas de preços de compra também podem ser anexadas aos subcontratos como associações conhecidas como listas de preços do projeto. Estas listas de preços são usadas para introduzir preços predefinidos em itens de subcontrato. Por predefinição, quando várias listas de preços de compra são anexadas a um subcontrato, cada uma deve ter uma data efetiva distinta. O Project Operations não suporta listas de preços de compra que têm uma data efetiva sobreposta. Apenas as listas de preços em que o campo **Contexto** está definido como **Compra** podem ser anexadas aos subcontratos.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]