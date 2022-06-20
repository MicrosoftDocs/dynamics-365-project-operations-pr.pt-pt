---
title: Conceitos-chave de subcontratação
description: Este artigo explica alguns dos principais conceitos que se aplicam à subcontratação no Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 08/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0ac84d132a2d62528d97ed3776a78062a589a380
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927710"
---
# <a name="key-concepts-in-subcontracting"></a>Conceitos-chave de subcontratação

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

Este artigo explica alguns dos principais conceitos que deve ter em conta antes de começar a utilizar a funcionalidade de subcontratação no Microsoft Dynamics 365 Project Operations.

## <a name="contracting-unit-on-the-subcontract"></a>Unidade de contratação no subcontrato

A unidade de contratação representa a divisão ou prática que detém a entrega do projeto final. A unidade de contratação é também a divisão que entra na relação contratual com o fornecedor.

## <a name="purchase-currency"></a>Moeda da compra

No Project Operations, a moeda de compra é a moeda em que o subcontrato é criado. É também a moeda em que os custos do subcontratante num projeto são registados. A moeda de compra pode diferir da moeda do projeto e a moeda do projeto pode, por sua vez, diferir da moeda de venda.

## <a name="billing-methods-on-subcontract-lines"></a>Métodos de faturação em linhas de subcontratação

Para os projetos, existem tipicamente modelos de contratação com base em taxas fixas e de consumo. O Project Operations suporta estes métodos de faturação nos contextos de venda e compra. Para uma compra, os métodos de faturação funcionam da seguinte forma:

- **Tempo e Material** – Quando um item de subcontrato utiliza o método de faturação **Tempo e Material**, o custo do tempo é registado no projeto à medida que os subcontratantes trabalham nesse projeto e registam o tempo. Estas transações de custos de subcontratantes são associadas aos itens de linha nas faturas do fornecedor. Neste modelo, os gestores de projeto que utilizam o Project Operations podem combinar e verificar as linhas de fatura do fornecedor com o tempo do subcontratante que é registado e aprovado. Após a conclusão da verificação, os custos reais anteriores que foram registados após a aprovação são invertidos e os novos custos reais que são baseados na fatura do fornecedor são criados no projeto.
- **Preço Fixo** – Neste modelo de contratação de taxa fixa, as faturas do fornecedor baseiam-se em marcos fixos. No entanto, os recursos subcontratados também podem comunicar o tempo. Depois, o tempo é revisto e aprovado pelo gestor do projeto. Quando é aprovado, o Project Operations cria custos temporários reais no projeto. Depois de o fornecedor enviar uma fatura para um marco, o gestor do projeto pode associar os custos anteriormente registados ao marco. Quando a verificação estiver concluída, os custos reais são invertidos e o custo baseado em marcos é registado.

## <a name="project-price-lists-on-subcontracts"></a>Listas de preços de projeto nos subcontratos

As listas de preços do projeto são listas de preços que são usadas para configurar preços de compra para o tempo, despesas e outros componentes relacionados com o projeto. Podem existir várias listas de preços, podendo cada uma delas ter o seu próprio subcontrato efetivo para a data no Project Operations. O Project Operations não suporta datas efetivas sobrepostas nas listas de preços do projeto para um subcontrato.

## <a name="transaction-classes-on-subcontracts"></a>Classes de transação nos subcontratos

O Project Operations suporta quatro tipos de classes de transações:

- Tempo
- Despesa
- Material
- Taxa

Os custos de compra só podem ser estimados e incorridos nas classes de transação **Tempo**, **Despesa** e **Material**. A **taxa** é uma classe de transação apenas de receitas e não está disponível no conteúdo da compra.

## <a name="purchase-pricing-dimensions"></a>Dimensões de preços de compras

As dimensões dos preços permitem-lhe decidir quais os atributos utilizados para a configuração do preço de compra e transações atempadas predefinidas. No que diz respeito à compra, o Project Operations suporta apenas conjuntos de dimensão fixa para a configuração e predefinição do preço de compra. Para a configuração e predefinição do preço de compra em itens de subcontrato e transações de tempo de subcontrato, os atributos são **Função** e **Recurso Reservável**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
