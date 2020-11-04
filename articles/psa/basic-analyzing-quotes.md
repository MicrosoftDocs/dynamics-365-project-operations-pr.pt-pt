---
title: Análise de propostas do projeto
description: Este tópico fornece informações sobre a análise de propostas do projeto.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 0d9cefafcce33297146cae81d9ba7e68ab79aeb6
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082520"
---
# <a name="analysis-of-project-quotes"></a>Análise de propostas do projeto

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

O Dynamics 365 Project Service Automation analisa as propostas do projeto para estimar a rentabilidade. Também analisa como a proposta está alinhada com as expectativas do cliente sobre a data de entrega ou a data de conclusão, bem como sobre o orçamento.

## <a name="profitability-analysis"></a>Análise de rentabilidade

O Project Service Automation analisa a rentabilidade utilizando a margem bruta e a margem bruta ajustada.

- As margens brutas são calculadas utilizando a seguinte fórmula:

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- A margem bruta ajustada é calculada utilizando a seguinte fórmula:

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

Se os valores para a margem bruta e a margem bruta ajustada forem diferentes por uma margem ampla, a maior parte do trabalho na proposta é classificada como não faturável.

## <a name="analysis-of-customer-expectations"></a>Análise das expectativas do cliente

Pode analisar as propostas e gerar gráficos para obter as expectativas do cliente sobre a agenda e o orçamento se introduzir valores nos seguintes campos:

- O campo **Data de entrega pretendida** no cabeçalho da proposta.
- O campo **Orçamento do cliente** para cada linha de proposta (para linhas baseadas em projetos e linhas baseadas em produtos).

A análise das expectativas do cliente sobre a agenda é efetuada comparando a data de fim mais recente do detalhe da linha de proposta com a data de entrega pretendida em todas as linhas de proposta na proposta.

A análise das expectativas do cliente sobre o orçamento é efetuada através da comparação da soma do orçamento total do cliente com o montante proposto em todas as linhas de proposta.