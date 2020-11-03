---
title: Configurar taxas de custo e de venda para produtos de catálogo
description: Este tópico fornece informações sobre como configurar taxas de custo e de vendas para itens num catálogo de produtos.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5178a9143536bf4b2573403125325017861cdd5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082471"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products"></a>Configurar taxas de custo e de venda para produtos de catálogo

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_


A configuração de preços para itens de catálogo de produtos no Dynamics 365 Project Operations é a mesma que no Dynamics 365 Sales.

Como os produtos não podem ser estimados ou utilizados em projetos no Project Operations, não há necessidade de definir preços do catálogo de produtos nas listas de preços do projeto para propostas e contratos.

Os preços do catálogo de produtos devem ser configurados no campo **Preço do Produto** de uma proposta, contrato ou conta. Não configure preços de catálogo de produtos nas listas de preços do projeto para estas entidades. As listas de preços do projeto são exclusivas do Project Operations. Existe uma lógica de negócio específica para aplicações que copia as listas de preços de uma proposta para um contrato. O resultado é uma lista de preços específica do contrato. A operação de cópia pode atrasar o processo de ganho da proposta se a lista de preços do projeto na proposta ficar demasiado grande. As listas de preços do produto não são copiadas para criar listas de preços personalizadas em contratos. Isto significa que as listas de preços do produto não têm impacto no desempenho do processo de ganho das propostas.
