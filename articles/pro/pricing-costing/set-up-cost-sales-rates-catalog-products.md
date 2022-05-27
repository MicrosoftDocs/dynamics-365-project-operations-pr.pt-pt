---
title: Configurar taxas de custo e de venda para produtos de catálogo – lite
description: Este tópico fornece informações sobre como configurar taxas de custo e de vendas para itens num catálogo de produtos.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 12e09d99e9832c93c3aea34ec0d4488cdf6b02fa
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8576836"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Configurar taxas de custo e de venda para produtos de catálogo – lite

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_


Definir preços para artigos de catálogo de produtos em Dynamics 365 Project Operations é o mesmo que no Dynamics 365 Sales.

No Project Operations, os produtos não podem ser estimados ou utilizados em projetos, pelo que os preços do catálogo de produtos não precisam de ser definidos nas listas de preços do projeto para cotações e contratos.

Utilize o campo **preço do produto** de uma cotação, contrato ou conta para configurar os preços do catálogo de produtos. Não estabeleça preços de catálogo de produtos nas listas de preços do projeto. As listas de preços do projeto são exclusivas do Project Operations. A lógica de negócio específica da aplicação copia as listas de preços de uma cotação para um contrato. O resultado é uma lista de preços específica do contrato. A operação de cópia pode atrasar o processo de ganho da proposta se a lista de preços do projeto na proposta ficar demasiado grande. As listas de preços do produto não são copiadas para criar listas de preços personalizadas em contratos. Como não há cópias envolvidas, o desempenho do processo de citação não é afetado.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]