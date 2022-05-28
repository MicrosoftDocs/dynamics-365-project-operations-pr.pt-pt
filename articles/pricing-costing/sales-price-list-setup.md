---
title: Configurar uma lista de preços de vendas
description: Este tópico fornece informação sobre as listas de preços de vendas para preços do projeto.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: cb4153e05359c17c1536e06f220e21465be899fb
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582678"
---
# <a name="set-up-a-sales-price-list"></a>Configurar uma lista de preços de vendas

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

Para obter propostas e contratos do projeto, uma lista de preços do projeto tem um padrão de substituição de preços diferente da lista de preços de produtos. Num item de proposta baseado no catálogo de produtos, pode substituir o preço por funções e categorias diretamente na linha de proposta, porque cada linha de proposta aponta para exatamente um item de catálogo. No entanto, numa linha de proposta com base em projetos, não pode substituir o preço por funções e categorias diretamente na linha de proposta. Pode usar a lista de preços do projeto para trabalhar com os dois padrões distintos de definição manual.

> [!NOTE]
> Recomendamos que tenha uma lista de preços separada para os recursos do seu projeto e itens do catálogo, devido às diferenças de comportamento entre os dois quando os preços são substituídos.

Cada uma das seguintes entidades pode ter uma ou mais listas de preços de venda associadas para a definição de preços do projeto:

- Cliente (conta) 
- Oportunidade 
- Proposta 
- Contrato do Projeto

A associação destas entidades com uma lista de preços é indicada pelas listas de preços do projeto. Pode associar uma ou mais listas de preços às entidades de vendas Cliente, Oportunidade, Proposta e Contrato do Projeto.

Uma lista de preços predefinida do projeto não é introduzida automaticamente num registo de cliente. No entanto, pode anexar manualmente uma lista de preços do projeto ao registo de cliente. No entanto, deverá anexar manualmente uma lista de preços do projeto quando tiver um contrato de preços personalizado com o cliente. 

Quando uma lista de preços do projeto é associada a uma entidade de vendas, as seguintes informações são validadas:

- A lista de preços tem um contexto de **Vendas**. 
- A moeda da lista de preços corresponde com a moeda do cliente. 

Num contrato do projeto, a seguinte ordem de precedência é usada para definir automaticamente as listas de preços relacionadas com os projetos:

1. Proposta
2. Oportunidade
3. Cliente 
4. Definições globais 

Quando uma lista de preços do projeto é introduzida por predefinição, o sistema valida que a moeda corresponde com a moeda do cliente e que as listas de preços predefinidas que foram introduzidas têm um contexto de **Vendas**.

Pode associar várias listas de preços do projeto às entidades Cliente, Oportunidade, Proposta e Contrato do Projeto. Esta capacidade suporta preços predefinidos específicos de data para um contrato do projeto de execução demorada, onde poderá necessitar de mais de uma lista de preços para contabilizar as atualizações de preços que ocorrem devido à inflação. No entanto, se as listas de preços associadas è entidade Cliente, Oportunidade, Proposta ou Contrato do Projeto tiverem a data efetiva sobreposta, os preços predefinidos poderão estar incorretos. Consequentemente, deve certificar-se de que as listas de preços do projeto que têm a data efetiva sobreposta não estão associadas a essas entidades.


[!INCLUDE[footer-include](../includes/footer-banner.md)]