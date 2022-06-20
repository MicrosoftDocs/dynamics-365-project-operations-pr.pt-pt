---
title: Configurar taxas de custo e de venda para materiais
description: Este artigo fornece informações sobre como configurar as taxas de custo e de vendas para materiais utilizados em projetos.
author: rumant
ms.date: 03/21/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0a7d84c2dcaa228e06add2f3cb06a530b29e0e35
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911794"
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
