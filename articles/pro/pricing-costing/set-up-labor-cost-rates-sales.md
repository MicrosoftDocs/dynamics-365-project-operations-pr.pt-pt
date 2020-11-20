---
title: Configurar taxas de custo de mão de obra – lite
description: Este tópico fornece informações sobre como configurar taxas de custo de mão de obra no Project Operations.
author: rumant
manager: Annbe
ms.date: 10/12/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2e79dde867833fb952349c073ce8975381029dcf
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180742"
---
# <a name="set-up-labor-cost-rates---lite"></a>Configurar taxas de custo de mão de obra – lite

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

Cada lista de preços tem um conjunto de taxas de mão de obra (preços de função) que se alinham com o conteúdo e a data de efetividade da lista de preços.

1. Crie uma lista de preços e, no separador **Preço de Função**, na subgrelha, selecione **Nova Função**.
2. Na página **Criação Rápida**, selecione a função e a unidade de organização.
3. Introduza quaisquer outras informações de campo necessárias.

A tabela a seguir inclui alguns dos campos que são importantes na criação de taxas de mão de obra numa lista de preços de custo.

| Campo | Localização | Descrição | Impacto a jusante |
| --- | --- | --- | --- |
| Função | Separador **Geral** e páginas **Criação Rápida** | Selecione a função a que a taxa de custo se aplica. | A função na estimativa de entrada ou real será igualada contra esta linha para assumir a predefinição do custo da função. |
| Unidade de Atribuição de Recursos | Separador **Geral** e páginas **Criação Rápida** | Selecione a unidade organizacional ou divisão da empresa de onde esta função será utilizada. Por exemplo, um programador da divisão de Robótica da Fabrikam India ou um programador da divisão de Software da Fabrikam USA. | A unidade de atribuição de recursos na estimativa de entrada ou real será igualada contra esta linha para assumir a predefinição do custo da função. |
| Preço | Separador **Geral** e páginas **Criação Rápida** | Configurar a taxa de custo para a função, a empresa de atribuição de recursos e a combinação de unidade de atribuição de recursos. Por exemplo, um programador da Fabrikam India custa 1000 INR ou um programador da Fabrikam USA custa 150 USD. | O preço é a taxa de custo que assume a predefinição no custo por unidade da estimativa de entrada ou linha real para a classe de transação **Tempo**. |
| Moeda | Separador **Geral** e páginas **Criação Rápida** | Por predefinição, o valor cambial provém da moeda no cabeçalho da lista de preços de custo, mas pode ser substituído. Por exemplo, um programador da Fabrikam India custa 1000 INR. Um programador da Fabrikam USA custa 150 USD. | Esta moeda assume no custo por unidade linha de custo real de entrada para a classe de transação **Tempo**. Numa estimativa do projeto, o valor cambial é convertido para a moeda do projeto e indicado na vista faseada por Tempo da estimativa. |
| Agenda de Unidades | Separador **Geral** e páginas **Criação Rápida** | A agenda de unidade assume a predefinição Tempo e não pode ser alterada na entidade de preço Função porque é usado para expressar taxas por unidades de tempo. | Não existe impacto a jusante. |
| Unidade | Separador **Geral** e páginas **Criação Rápida** | Por predefinição, o valor provém do campo **Unidade de Tempo** no cabeçalho da lista de preços de custo. O valor pode ser substituído. Por exemplo, um programador da Fabrikam India custa 1000 INR por **Dia na Índia**. Um programador da Fabrikam USA custa 150 USD por **Dia nos EUA**. | O sistema utiliza o sistema de unidades e a conversão em unidades base para calcular um custo por unidade para calcular o preço predefinido por unidade numa estimativa de entrada ou numa linha real. Por exemplo, uma estimativa é de 10 **Dias na Índia** no valor de trabalho para um programador na Índia, e a unidade **Dia na Índia** é definido como 10 horas. Ao definir o custo dessa linha de estimativa, a aplicação calcula o custo unitário na estimativa como: 1000 INR / 10 horas = 100 INR por hora, o que é convertido em USD e mostrado como o custo unitário na página **Estimativas do Projeto**. |

## <a name="transfer-pricing-and-costs-for-resources-outside-of-your-division-or-legal-entity"></a>Preços de transferência e custos para recursos fora da sua divisão ou entidade legal

Em empresas baseadas em projetos, é comum usar funcionários de diferentes entidades jurídicas ou divisões em projetos. Um projeto pode ser executado por uma entidade legal, mas os colaboradores ou consultores que trabalham no projeto podem vir da mesma entidade legal ou de outra, ou pode haver uma combinação de ambos. No Dynamics 365 Project Operations, a entidade legal que detém a entrega do projeto é a **Empresa Proprietária** e a divisão que detém a entrega é a **Unidade Contratante**. Outras entidades jurídicas que fornecem recursos são as **Empresas de Atribuição de Recursos** e divisões que fornecem recursos são as **Unidades de Atribuições de Recursos**. Na maioria dos países, as empresas são obrigadas a garantir que a entidade ou divisão legal de atribuição de recursos cobre à empresa proprietária e a unidade contratante pela utilização dos recursos.

Por exemplo, a corporação Fabrikam deve garantir que a Fabrikam India-Robotics tenha um cartão de taxa de custo negociado com a Fabrikam US-Robotics ou a Fabrikam UK-Robotics.

Um programador da Fabrikam India-Robotic cobra 100 $ quando emprestado à Fabrikam US-Robotics e 150 $ quando emprestado à Fabrikam U-Robotics.

### <a name="set-up-costs-for-outside-resources"></a>Configurar custos para recursos externos

1. Crie uma lista de preços de custos chamada *Taxas de custo da Fabrikam US-Robotics* e definir um intervalo de data eficaz.
2. Na lista de preços de custo, configure taxas utilizando informações da tabela seguinte. 

| Função | Empresa de Recursos | Unidade de Atribuição de Recursos | Taxa de custo |
| --- | --- | --- | --- |
| Programador | Fabrikam India | Fabrikam India-Robotics | 100€ |
| Programador | Fabrikam Philippines | Fabrikam Philippines-Robotics | 90 $ |
| Programador | Fabrikam US | Fabrikam US-Robotics | 150 $ |

3. Anexe esta lista de preços de custos à unidade de organização Fabrikam US-Robotics.

### <a name="set-up-transfer-pricing-for-a-resource-in-the-appropriate-currency"></a>Configurar preços de transferência para um recurso na moeda adequada 

No Project Operations, os preços dos recursos podem ser criados em qualquer moeda. A moeda assume a predefinição do que está no cabeçalho da lista de preços, mas pode ser alterada.

Utilizando o exemplo para o preço de transferência configurado, as informações podem ser alteradas para:

A corporação Fabrikam deve garantir que a Fabrikam India-Robotics tenha uma taxa de custo negociado com a Fabrikam US-Robotics ou a Fabrikam UK-Robotics.

Um programador da Fabrikam India-Robotics cobra 5000 INR quando emprestado à Fabrikam US-Robotics e 5500 INR quando emprestado à Fabrikam UK-Robotics.

Na lista de preços de custos da Fabrikam US-Robotics, as taxas de custo podem ser expressas como:

| Função | Empresa de Recursos | Custo |
| --- | --- | --- |
| Programador | Fabrikam India | 5000 INR |
| Programador | Fabrikam US | 115 USD |

Na lista de preços de custos da Fabrikam UK-Robotics, as taxas de custo podem ser expressas abaixo:

| Função | Empresa de recursos | Custo |
| --- | --- | --- |
| Programador | Fabrikam India | 5500 INR |
| Programador | Fabrikam UK | 115 GBP |

A lista de preços de custos pode fornecer taxas de mão de obra em várias moedas. Ao gerar uma estimativa de custos no projeto, o Project Operations converterá estas taxas de custo na moeda do projeto e exibi-la-á ao utilizador. Quando uma entrada de tempo é aprovada e um custo real é criado, o custo real tem o preço real na moeda dessa linha de preço de função correspondente na lista de preços de custo. Os custos reais de um único projeto podem ser registados em várias moedas. No entanto, ao efetuar o rollup ou resumir os custos reais da mão de obra a nível do projeto, o Project Operations converterá todos os montantes do custo da mão de obra na moeda do projeto, o que o utilizador pode visualizar.
