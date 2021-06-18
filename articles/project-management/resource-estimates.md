---
title: Estimativas financeiras para tempo de recursos em projetos
description: Este tópico fornece informações sobre como as estimativas financeiras para o tempo são calculadas.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e79e33da618c4ab32b1ba13f33e50f60a550ff0b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010800"
---
# <a name="financial-estimates-for-resource-time-on-projects"></a>Estimativas financeiras para tempo de recursos em projetos

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

As estimativas financeiras do tempo são calculadas com base em três fatores: 

- O tipo de membro genérico ou nomeado da equipa atribuído a cada tarefa do nó de folha no plano do projeto. 
- O tipo ou complexidade do trabalho.
- A difusão do esforço para a atribuição do recurso na tarefa. 

Os dois primeiros fatores influenciam o custo unitário ou a taxa de faturação da atribuição de um recurso. O custo unitário ou a taxa de faturação de uma atribuição de recursos é determinado pelos atributos do recurso atribuído. Estes atributos incluem a unidade organizacional a que pertence o recurso e o papel padrão do recurso. Também pode adicionar atributos personalizados relevantes para o seu negócio para o recurso, como título padrão ou nível de experiência e fazê-los influenciar o custo unitário ou a taxa de fatura da atribuição.
Para além dos atributos do recurso, atributos de trabalho, como a tarefa, também podem influenciar a taxa de faturação unitária ou a taxa de custo da atribuição. Por exemplo, quando certas tarefas são mais complexas, a atribuição do recurso a essas tarefas específicas resulta num custo unitário ou taxa de faturação mais elevado do que em tarefas menos complexas.   

O terceiro fator fornece a quantidade de horas a essa taxa. Nos casos em que uma tarefa abrange dois períodos de preço, é provável que a primeira parte da atribuição de recursos para essa tarefa seja custeada e tenha um preço diferente da segunda parte da tarefa. A estimativa de esforço em cada atribuição de recursos é um valor complexo armazenado com a distribuição diária do esforço por dia.

Para obter instruções detalhadas sobre como configurar atributos personalizados de trabalho e recursos como dimensões de preços e custos, consulte [Vista geral das dimensões dos preços](../pricing-costing/pricing-dimensions-overview.md).

A estimativa financeira de cada atribuição de recursos é calculada como **taxa/hora para a atribuição multiplicada pelo número de horas.**  À semelhança da estimativa de esforço, a estimativa financeira para o custo e receitas de cada atribuição de recursos é um valor complexo armazenado com a distribuição diária do valor monetário por dia. 

## <a name="summarizing-financial-estimates-for-time"></a>Resumir estimativas financeiras para o tempo
Uma estimativa financeira do tempo numa tarefa de nó de folhas é a soma das estimativas financeiras de todas as atribuições de recursos para essa tarefa.

Uma estimativa financeira do tempo numa tarefa de resumo ou principal é a soma das estimativas financeiras de todas as tarefas de elementos subordinados. Este é o custo estimado da mão de obra no projeto. 

![Estimativas de Recursos](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a>Preço de custo e moeda de custo predefinidos

O preço de custo por defeito provém das tabelas de preços anexas à unidade de contratação do projeto. A moeda de custo de um projeto é sempre a moeda da unidade de contratação do projeto. Numa atribuição de recursos, a estimativa financeira do custo é armazenada na moeda de custo do projeto. Por vezes, a moeda em que a taxa de custo é fixada na tabela de preços é diferente da moeda de custo do projeto. Nestes casos, a aplicação converte a moeda em que o preço de custo é criado para a moeda do projeto. Na grelha de **Estimativas**, todas as estimativas de custos são apresentadas e resumidas na moeda de custo do projeto. 

## <a name="default-bill-rate-and-sales-currency"></a>Taxa de faturação e moeda de venda predefinidas

O preço de venda padrão provém das listas de preços do projeto anexadas ao contrato de projeto relacionado se o negócio for ganho, ou da proposta do projeto relacionado se o negócio ainda estiver na fase de pré-venda. A moeda de vendas do projeto é sempre a moeda da proposta de projeto ou do contrato do projeto. Numa atribuição de recursos, a estimativa financeira das vendas é armazenada na moeda de vendas do projeto. Ao contrário do custo, o preço de venda que está estabelecido na tabela de preços nunca pode ser diferente da moeda de venda do projeto. Não há nenhum cenário em que a conversão de moeda seja necessária. Na grelha de **Estimativas**, todas as estimativas de vendas são apresentadas e resumidas na moeda de venda do projeto. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
