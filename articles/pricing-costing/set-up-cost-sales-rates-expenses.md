---
title: Configurar taxas de custo e de vendas para despesas
description: Este tópico fornece informações sobre como configurar taxas de custo e de vendas para categorias de transações e despesas.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b518c9eda00bef4d342dd66677344af516012749
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180296"
---
# <a name="set-up-cost-and-sales-rates-for-expenses"></a>Configurar taxas de custo e de vendas para despesas

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

Pode configurar preços de custo e de vendas para categorias de transações no Dynamics 365 Project Operations. Dado que os preços de custo e de vendas são projetados para Despesas, cada categoria de transação que os inclua, deve também ser configurada como uma categoria de despesas. Esta configuração garante precisão na funcionalidade a jusante. Os preços de custo e de vendas das categorias de transações só podem ser listados numa moeda, que deve ser a moeda no cabeçalho da lista de preços.

Para configurar as taxas de custo e de vendas para categorias de transações, complete os seguintes passos. 

1. Crie uma lista de preços com base no cabeçalho da lista de preços. 
2. No menu **Categoria de Preços**, no menu da subgrelha, selecione **+ Preço da Nova Categoria**. 
3. Na página **Criação Rápida**, insira a categoria de transação e a unidade para as quais está a criar o novo preço.

A tabela a seguir lista os campos no separador **Geral** e a página **Criação Rápida** de uma linha de preço de categoria que deve ter em mente à medida que cria preços de categoria numa lista de preços de vendas ou de custos.

| Campo | Localização | Descrição | Impacto a jusante |
| --- | --- | --- | --- |
| Categoria de Transação | Separador **Geral** e páginas **Criação Rápida** | Selecione a categoria de transação para a qual está a criar um preço de vendas ou de custo. | A categoria de transação na estimativa de entrada ou real para Despesas será igualada contra esta linha para assumir a predefinição da taxa de custo ou de vendas da categoria de transação. |
| Agenda de Unidades | Separador **Geral** e páginas **Criação Rápida** | A agenda da unidade assume a predefinição da agenda da unidade da categoria de transação. | Este campo não tem impacto a jusante. |
| Unidade | Separador **Geral** e páginas **Criação Rápida** | Selecione a unidade para a qual as taxas estão a ser configuradas. | A unidade na estimativa de entrada ou real é igualada com a unidade nesta linha para assumir a predefinição da taxa na estimativa ou real de despesas. |
| Método de Definição de Preços | Separador **Geral** e páginas **Criação Rápida** | Os valores possíveis do campo **Método de Definição de Preços** são **Preço por Unidade**, **Custo** e **Margem de Lucro Sobre o Custo**. | Durante a configuração do preço, a seleção de **Preço Por Unidade** bloqueia o campo **Percentagem** na linha de preço da categoria. Se **A custo** for selecionado, os campos **Preço** e **Percentagem** são bloqueados na lista de preços de vendas. A seleção de **Margem de Lucro Sobre o Custo** bloqueia o campo **Preço** na lista de preços de vendas. Numa linha real de entrada de despesas, o método de definição de preços **A custo** ou **Margem de Lucro Sobre o Custo** resulta na correspondente linha de vendas não faturada a ser atribuída um preço igual ao preço sobre o custo real ou calculado como uma margem de lucro acima do preço. |
| Preço | Separador **Geral** e páginas **Criação Rápida** | Configurar uma taxa por unidade para a categoria de transação e a combinação de unidades. Por exemplo, a taxa de quilometragem é de 10 USD por milha e 8 USD por quilómetro. | A taxa de quilometragem será a taxa que assume a predefinição no preço ou custo por unidade da estimativa de entrada ou linha real para uma classe de transação de despesas.|
| Percentagem | Separador **Geral** e páginas **Criação Rápida** | Configurar percentagem sobre o custo para a categoria de transação e a combinação de unidades. Por exemplo, a taxa de vendas de tarifa aérea deve ser marcada em 10 por cento acima do custo das despesas com tarifas aéreas incorridas. | Esta percentagem da margem de lucro sobre o custo é aplicável apenas à lista de preços de vendas quando o método de definição de preços selecionado é **Margem de Lucro Sobre o Custo**. |
| Moeda | Separador **Geral** e páginas **Criação Rápida** | Por predefinição, este valor cambial provém da moeda no cabeçalho da lista de preços. Para o preço da categoria de transação, a moeda não pode ser substituída. | Esta moeda assume a predefinição no preço por unidade de entrada de linha real para a classe de transação de despesas para custo e vendas. |

## <a name="pricing-methods-for-expenses"></a>Método de definição de preços para despesas

Ao configurar preços de categoria que só são relevantes no contexto da definição de preços de despesas, pode utilizar um dos seguintes três métodos de definição de preços:

- **Preço unitário**
- **A custo**
- **Margem de Lucro Sobre o Custo**

### <a name="price-per-unit"></a>Preço unitário
Quando este método de definição de preços é selecionado numa linha de preços de categoria que está ligada a uma lista de preços de vendas, o preço assume a predefinição para a categoria e a combinação de unidade tanto na estimativa como no real. A estimativa refere-se às linhas de estimativa do projeto para despesas, ao detalhe da linha da proposta e ao detalhe do item contrato para despesas.

### <a name="at-cost"></a>A custo
Quando este método de definição de preços é selecionado na linha de preços de categoria que está ligada a uma lista de preços de vendas, o preço assume a predefinição para a categoria e a combinação de unidade apenas para o real das despesas. Por exemplo, valores reais de vendas não faturadas para a classe de transação de despesas. O preço unitário é definido no valor real das vendas não faturadas a partir do preço unitário sobre o custo real para essa despesa. Assumir a predefinição do preço com base no custo não é feito nas estimativas do projeto para despesas ou na linha de proposta e detalhes do item de contrato para despesas.

### <a name="markup-over-cost"></a>Margem de Lucro Sobre o Custo
Quando este método de definição de preços é selecionado na linha de preços de categoria que está ligada a uma lista de preços de vendas, o preço assume a predefinição para a categoria e a combinação de unidade apenas para um real das despesas. Por exemplo, valores reais de vendas não faturadas para a classe de transação de despesas. Este preço unitário é definido no valor real de vendas não faturadas para um valor calculado a partir do preço unitário sobre o custo real para essa despesa após a aplicação da percentagem de margem definida. Assumir a predefinição do preço com base no custo não é feito nas estimativas do projeto para despesas ou na linha de proposta e detalhes do item de contrato para despesas.
