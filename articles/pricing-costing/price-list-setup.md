---
title: Configurar listas de preços
description: Este tópico fornece informações sobre como configurar listas de preços de custos e vendas.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 578f5641659a5d05785781afe7055fe4449cf799
ms.sourcegitcommit: f8edff6422b82fdf2cea897faa6abb51e2c0c3c8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/21/2020
ms.locfileid: "4088057"
---
# <a name="set-up-price-lists"></a>Configurar listas de preços

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

As listas de preços no Dynamics 365 Project Operations representam um catálogo de taxas. As taxas expressam custos, vendas e taxas de faturação. Dependendo se a lista de preços expressa taxas de custo ou de vendas e taxas de faturação, o contexto da lista de preços é **Vendas** ou **Custos**.

As seguintes extensões são específicas para o Project Operations e são aplicadas às listas de preços do Dynamics 365 Sales.

- **Contexto** : Este campo tem os valores suportados **Custos** e **Vendas**. O valor **Compra** não é suportado. Defina o contexto para **Custos** para criar uma lista de preços de custos ou defina o contexto para **Vendas** para uma lista de preços de vendas. As listas de preços de custos resolvem o preço do tipo de custo nos registos de estimativa e real. As listas de preços de vendas resolvem o preço em registos de estimativa e reais de tipos de vendas não faturados e faturados.
- **Unidade de Tempo** : Esta é a unidade de tempo predefinida para a qual o preço é configurado na tabela **Preço de função** relacionado para esta lista de preços.
- **Entidade Lista de Preços** : Este campo oculto é para o Project Operations diferenciar listas de preços que são específicos de proposta ou de contrato daqueles que são padrão e globalmente aplicáveis.

## <a name="price-list-header"></a>Cabeçalho da lista de preços

A tabela seguinte inclui os campos no separador **Geral** de uma lista de preços que são exclusivos do Project Operations ou têm alterações significativas no comportamento das listas de preços no Sales.

| Campo | Localização | Relevância, finalidade e orientação | Impacto a jusante |
| --- | --- | --- | --- |
| Nome | Separador **Geral** e formulários **Criação Rápida** | A identidade da lista de preços. | A lista de preços é mostrada com este valor em todas as páginas da lista e opções pendente.|
| Contexto | Separador **Geral** e formulários **Criação Rápida** | Este campo pode ser definido como **Custos** ou **Vendas**. | Uma lista de preços definida para **Custos** é usada para pesquisar o preço para estimativas de custos e custos reais. Uma lista de preços definida para **Vendas** é usada para pesquisar o preço para estimativas de vendas e vendas reais. Apenas as listas de preços que têm o contexto definido para **Vendas** podem ser anexadas às listas de preços do projeto para clientes, propostas de projeto e contratos de projeto. |
| Data de Início | Separador **Geral** e formulários **Criação Rápida** | A data de início do período em que se encontra a lista de preços é efetiva. | Com o campo **Data de Fim** , este campo é utilizado para determinar qual a lista de preços aplicável a uma determinada estimativa ou linha real. |
| Data de Fim | Separador **Geral** e formulários **Criação Rápida** | A data de fim do período em que se encontra a lista de preços é efetiva. | Com o campo **Data de Início** , este campo é utilizado para determinar qual a lista de preços aplicável a uma determinada estimativa ou linha real. |
| Moeda | Separador **Geral** e formulários **Criação Rápida** | Este campo é utilizado assumir a predefinição da moeda em cada função, categoria ou linha de item da lista de preços relacionada com esta lista de preços. | Nas listas de preços **Vendas** , as funções, categorias ou linhas de item da lista de preços não podem ser criadas em nenhuma moeda que não seja esta moeda. Nas listas de preços **Custos** , pode criar uma linha de preço de função em qualquer moeda. A moeda aqui definida é usada como uma predefinição. A configuração do utilizador que está relacionada com os preços de função pode sobrepor-se a este valor para ativar a configuração da taxa de custo da mão de obra em qualquer moeda. As taxas de custos de categoria e os custos de item de lista de preços só podem ser definidos na moeda definida aqui. |
| Unidade de Tempo | Separador **Geral** e formulários **Criação Rápida** | Este campo é utilizado assumir a predefinição da unidade de tempo em cada linha de função relacionada com esta lista de preços. | Este valor de campo é utilizado apenas na configuração do preço da função relacionada. Nas listas de preços **Custos** e **Vendas** , pode criar uma linha de preço de função em qualquer unidade de tempo. A unidade de tempo aqui definida é usada como uma predefinição. A configuração do utilizador que está relacionada com os preços de função pode sobrepor-se a este valor para ativar a configuração da taxa de custo e faturação da mão de obra em qualquer unidade de tempo. |
| Descrição | Separador **Geral** e formulários **Criação Rápida** | Este campo de texto permite-lhe fornecer uma descrição de várias linhas da lista de preços. | Este campo é mostrado nas vistas **Associadas** na lista de preços em várias entidades que têm listas de preços relacionadas. |
