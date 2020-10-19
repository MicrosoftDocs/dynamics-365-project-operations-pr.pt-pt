---
title: Custo das linhas de proposta baseadas em produtos
description: Este tópico fornece informações sobre como aplicar um preço de custo a uma linha de proposta baseada em produtos.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 17b377eab5bcbc1a2327cb3ff87cc75d8de40953
ms.sourcegitcommit: a0f80d024a5d3112a39781815bd31d0c05ddaf6f
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 09/30/2020
ms.locfileid: "3906286"
---
# <a name="costing-product-based-quote-lines"></a>Custo das linhas de proposta baseadas em produtos

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_


As linhas de proposta baseadas em produtos no Dynamics 365 Project Operations também têm um campo **Preço de Custo**. Este campo é utilizado para monitorizar o preço de custo do produto na linha de proposta e para os cálculos de rentabilidade a jusante.

Quando uma linha de proposta baseada em produtos é criada para um produto do catálogo, o custo da linha de proposta baseado em produtos assume por predefinição o valor do campo **Custo Padrão** no catálogo de produtos. O campo de custo padrão no catálogo de produtos está configurado na moeda base da Organização. O custo unitário predefinido na linha da proposta baseada em produtos é convertido para a moeda de venda na proposta.

## <a name="unit-cost-on-a-product-based-quote-line"></a>Custo unitário numa linha de proposta baseada em produtos

Ter um custo unitário numa linha de proposta baseada em produtos tem como objetivo permitir custos diferentes para um produto para cada venda. Este não é um cenário típico, mas por vezes o custo do produto pode ser descontado pelo fornecedor, dependendo do cliente da venda final.

Por exemplo:

A Fabrikam Robotics está a instalar braços robóticos nas linhas de montagem da A Datum Corporation. A Fabrikam presta serviços de instalação, mas os braços robóticos são adquiridos à Trey robotics. Se a instalação de braços robóticos na A Datum Corporation abrir uma nova indústria vertical para os braços robóticos da Trey, a Trey pode oferecer um desconto especial para este negócio à Fabrikam.

Neste caso, a Fabrikam criará uma linha de proposta baseada em produtos para a Robotic Arms e introduzirá um custo unitário especial para esta proposta. Este custo é diferente do custo padrão da Trey Robotic Arms.
