---
title: Configurar taxas de custo e de venda para materiais
description: Este tópico fornece informações sobre como configurar os custos e taxas de venda dos materiais utilizados em projetos.
author: rumant
ms.date: 03/21/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 1b1b679f15662d922804deefb6372adcdf4d4839
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8576882"
---
# <a name="set-up-cost-and-sales-rates-for-materials"></a>Configurar taxas de custo e de venda para materiais

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

Pode configurar preços de custo e de venda para produtos no Dynamics 365 Project Operations. Os preços de custo e de venda dos produtos só podem ser listados numa moeda, que deve ser a moeda no cabeçalho da tabela de preços.

Para configurar as taxas de custo e de venda dos produtos, complete os seguintes passos. 

1. Vá a **Vendas** > **Clientes** > **Listas de Preços** e selecione **Novo** para criar uma nova lista de preços. 
2. Nos **Itens da lista de preços** no menu da subgrelha, selecione **Novo item da lista de preços**. 
3. Na página **Criação rápida**, insira o produto e a unidade para a qual está a criar o novo preço.

Para mais informações sobre como definir preços para itens de catálogo, consulte [Definir preços de produtos com listas de preços e itens da lista de preços](/dynamics365/sales/create-price-lists-price-list-items-define-pricing-products) e [Precisão decimal na moeda e nos preços](/dynamics365/sales/decimal-precision-currency-pricing).
> [!NOTE]
> O Dynamics 365 Project Operations não suporta todos os métodos de definição de preços de produtos como o Dynamics 365 Sales. O único método de definição de preços suportado para produtos a utilizar em projetos é *Montante em moeda*.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
