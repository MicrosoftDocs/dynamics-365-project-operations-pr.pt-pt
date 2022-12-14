---
title: Configurar a conversão de moeda para calcular preços de vendas a partir de taxas de custo
description: Este artigo explica como configurar o comportamento da conversão de moeda que será utilizado no Microsoft Dynamics 365 Project Operations quando as transações de vendas são geradas a partir de transações de custo.
author: rumant
ms.date: 11/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3fa8077deb18f1a54e7f0f5e6dc4491a830df45b
ms.sourcegitcommit: 95e52fcf012a51229f3f6ae7dbf7b0fa56072a85
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 12/01/2022
ms.locfileid: "9816675"
---
# <a name="set-up-currency-conversion-to-calculate-sales-prices-from-cost-rates"></a>Configurar a conversão de moeda para calcular preços de vendas a partir de taxas de custo

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

No Microsoft Dynamics 365 Project Operations, os preços de vendas das categorias de despesas podem ser configurados como valores numéricos ou podem ser definidos de modo a serem calculados com base no custo incorrido.

Quando estão configurados para serem calculados com base no custo incorrido, estão disponíveis as seguintes opções:

- A custo
- Percentagem da margem de lucro sobre o custo

Nos cenários em que o custo de despesas é incorrido numa moeda diferente da moeda de venda do contrato do projeto, a conversão de moeda é necessária para calcular o preço de venda com base no custo.

## <a name="currency-conversion-behavior-that-uses-native-dataverse-exchange-rates"></a>Comportamento da conversão de moeda que utiliza taxas de câmbio do Dataverse nativas

Por predefinição, o Project Operations utiliza as taxas de câmbio de moeda armazenadas na tabela Moeda no Dataverse. Para configurar o Project Operations para utilizar taxas de câmbio nativas para calcular os preços de vendas a partir do custo, siga estes passos.

1. Aceda a **Project Operations \> Definições \> Parâmetros**.
1. Abra a página de detalhes **Parâmetro do Projeto**.
1. Defina o campo **Lógica de conversão de moeda** para um valor em branco.

## <a name="currency-conversion-behavior-that-uses-exchange-rates-from-finance-and-operations-apps"></a>Comportamento da conversão de moeda que utiliza taxas de câmbio de aplicações de finanças e operações

As taxas de câmbio na tabela Moeda que estão disponíveis nativas no Dataverse não são eficazes. Por conseguinte, poderão não ser sempre dimensionados para os requisitos que tem para o cálculo de preços de vendas das taxas de custo.

Pode utilizar taxas de câmbio do ambiente de finanças e operações para calcular o preço de vendas na moeda de venda a partir de uma taxa de custo na moeda de custo. Para configurar este comportamento da conversão de moeda, siga estes passos.

1. Na página **Parâmetros do projeto**, adicione o campo **Lógica da conversão de moeda**. Em seguida, guarde e publique a personalização.
1. Aceda a **Project Operations \> Definições \> Parâmetros**.
1. Abra a página de detalhes **Parâmetro do Projeto**. 
1. Defina o campo **Comportamento da conversão de moeda** como **Expandido com contingência para predefinição**.
1. Dê permissão de **Leitura Global** do direito de acesso de **Utilizador de aplicação de escrita dupla** para as tabelas seguintes:

    - msdyn\_currencyexchangerates
    - msdyn\_currencyexchangeratepairs
    - msdyn\_exchangeratetypes

1. No ambiente de finanças e operações, execute os seguintes mapas de escrita dupla com sincronização inicial:

    - Tipo de taxa de câmbio (msdyn\_exchangeratetypes)
    - Par de moeda de taxa de câmbio (msdyn\_currencyexchangeratepairs)
    - Taxas de Câmbio do CDS (msdyn\_currencyexchangerates)

Uma vez concluídas estas alterações, a escrita dupla irá disponibilizar as taxas de câmbio do ambiente de finanças e operações no Dataverse. Em seguida, o Project Operations irá utilizar essas taxas de câmbio para converter taxas de custo na moeda de venda do contrato.

> [!NOTE]
> Este comportamento da conversão de moeda aplica-se apenas ao cálculo dos preços de venda a partir das taxas de custo. Não será utilizado para calcular genericamente valores de moeda base. Os valores de moeda base irão sempre utilizar as taxas de câmbio do Dataverse nativas, independentemente de este procedimento ser ou não concluído.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
