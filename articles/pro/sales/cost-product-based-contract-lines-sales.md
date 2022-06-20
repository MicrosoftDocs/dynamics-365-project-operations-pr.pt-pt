---
title: Custo dos itens de contrato baseados em produtos – lite
description: Este artigo fornece informações sobre a criação
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a63ad12c081d19efde02303bf626184f8586d4a2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922926"
---
# <a name="cost-product-based-contract-lines---lite"></a>Custo dos itens de contrato baseados em produtos – lite

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_


As linhas de contrato baseadas no produto Dynamics 365 Project Operations incluem o campo **Preço de custo**, que armazena o preço de custo do produto para cálculos de rendibilidade a jusante.

Quando uma linha de contrato baseada em produtos é criada para um produto de catálogo, o custo da linha assume o campo **Custo padrão** no catálogo de produtos. O campo **Custo Padrão** no catálogo de produtos está configurado na moeda base da Organização. Quando o custo unitário assume a predefinição no item de contrato, é convertido na moeda de venda do contrato.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Custo unitário num item de contrato baseado em produtos

Ter um custo unitário num item de contrato baseado em produtos permite custos diferentes para produtos para cada venda de uma unidade. Embora nem sempre seja necessário, existem certos cenários em que o custo do produto pode ser descontado para o cliente pelo fornecedor. Considere o seguinte cenário:

A Fabrikam Robotics está a instalar braços robóticos nas linhas de montagem da Adatum Corporation. A Fabrikam presta serviços de instalação, mas os braços robóticos são da Trey Research. Se a instalação de braços robóticos na Adatum Corporation abrir uma nova indústria vertical para a Trey Research, pode oferecer um desconto especial para este negócio à Fabrikam. Neste caso, a Fabrikam cria uma linha de contrato baseada em produtos para braços robóticos. É celebrado um custo por unidade para este contrato. O custo é diferente do custo dos braços robóticos da Trey Research.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]