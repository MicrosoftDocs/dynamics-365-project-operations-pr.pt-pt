---
title: Custo dos itens de contrato baseados em produtos – lite
description: Este tópico fornece informações sobre como criar
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9458a57863244a68359f57185325c03a46bd6569
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003555"
---
# <a name="cost-product-based-contract-lines---lite"></a>Custo dos itens de contrato baseados em produtos – lite

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_


As linhas de contrato baseadas no produto Dynamics 365 Project Operations incluem o campo **Preço de custo**, que armazena o preço de custo do produto para cálculos de rendibilidade a jusante.

Quando uma linha de contrato baseada em produtos é criada para um produto de catálogo, o custo da linha assume o campo **Custo padrão** no catálogo de produtos. O campo **Custo Padrão** no catálogo de produtos está configurado na moeda base da Organização. Quando o custo unitário assume a predefinição no item de contrato, é convertido na moeda de venda do contrato.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Custo unitário num item de contrato baseado em produtos

Ter um custo unitário num item de contrato baseado em produtos permite custos diferentes para produtos para cada venda de uma unidade. Embora nem sempre seja necessário, existem certos cenários em que o custo do produto pode ser descontado para o cliente pelo fornecedor. Considere o seguinte cenário:

A Fabrikam Robotics está a instalar braços robóticos nas linhas de montagem da Adatum Corporation. A Fabrikam presta serviços de instalação, mas os braços robóticos são da Trey Research. Se a instalação de braços robóticos na Adatum Corporation abrir uma nova indústria vertical para a Trey Research, pode oferecer um desconto especial para este negócio à Fabrikam. Neste caso, a Fabrikam cria uma linha de contrato baseada em produtos para braços robóticos. É celebrado um custo por unidade para este contrato. O custo é diferente do custo dos braços robóticos da Trey Research.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]