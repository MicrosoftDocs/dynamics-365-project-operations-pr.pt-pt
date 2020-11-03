---
title: Custo dos itens de contrato baseados em produtos
description: Este tópico fornece informações sobre como criar
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7dfb9425174dddee52f9ee64f7a963e48a6bca70
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/20/2020
ms.locfileid: "4082635"
---
# <a name="costing-product-based-contract-lines"></a>Custo dos itens de contrato baseados em produtos

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_


Os itens de contrato baseados em produtos no Dynamics 365 Project Operations incluem o campo **Preço de Custo** , que armazena o preço de custo do produto para cálculos de rentabilidade a jusante.

Quando um item de contrato baseado em produtos é criado para um produto do catálogo, o custo do item de contrato baseado em produtos assume a predefinição o valor do campo **Custo Padrão** no catálogo de produtos. O campo **Custo Padrão** no catálogo de produtos está configurado na moeda base da Organização. Quando o custo unitário assume a predefinição no item de contrato, é convertido na moeda de venda do contrato.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Custo unitário num item de contrato baseado em produtos

Ter um custo unitário num item de contrato baseado em produtos permite custos diferentes para produtos para cada venda de uma unidade. Embora nem sempre seja necessário, existem certos cenários em que o custo do produto pode ser descontado para o cliente pelo fornecedor. Considere o seguinte cenário:

A Fabrikam Robotics está a instalar braços robóticos nas linhas de montagem da Adatum Corporation. A Fabrikam presta serviços de instalação, mas os braços robóticos são adquiridos à Trey Research. Se a instalação de braços robóticos na Adatum Corporation abrir uma nova indústria vertical para a Trey Research, pode oferecer um desconto especial para este negócio à Fabrikam. Neste caso, a Fabrikam cria um item de contrato baseado em produtos para Braços Robóticos e insere um custo por unidade para este contrato que é diferente do custo padrão dos braços robóticos da Trey Research.
