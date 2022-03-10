---
title: Copiar listas de preços
description: Este tópico fornece informação sobre como copiar listas de preços no Project Operations.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ad09bdce563a48843b3ed96e7aaabd9c0d5960336b9e1c74fddb9b61f760f4cd
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003740"
---
# <a name="copy-price-lists"></a>Copiar listas de preços

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

Pode criar cópias das listas de preços no Dynamics 365 Project Operations. Por exemplo, pode criar listas de preços para o próximo ano usando uma lista de preços do ano em curso.  Ou, pode copiar uma lista de preços para as taxas de faturação e de preços de venda das listas de preços para o custo. 

Para fazer uma cópia da lista de preços, complete os seguintes passos.

1. Abra a lista de preços que pretende copiar e selecione **Copiar**.
2. Insira todas as informações necessárias para copiar a lista de preços. A tabela a seguir mostra considerações a ter em mente ao introduzir informações.

| Campo | Descrição | Impacto a jusante |
| --- | --- | --- |
| Nome | O nome da lista de preços de origem com a **-cópia** anexado. | A lista de preços inclui este valor em todas as páginas da lista e opções pendente. |
| Contexto | Insira o contexto que deseja para a lista de preços de destino. | Uma lista de preços com o contexto definido para **Custos** é usada para pesquisar o preço para estimativas de custos e custos reais. Uma lista de preços com o contexto definido para **Vendas** é usada para pesquisar o preço para estimativas de vendas e vendas reais. Apenas as listas de preços que têm o contexto definido para **Vendas** podem ser anexadas a uma lista de preços para um cliente, propostas ou contratos. |
| Data de Início | A data de início do período em que se encontra a lista de preços é efetiva. | Juntamento com **Data de Fim**, este campo é utilizado para determinar qual a lista de preços aplicável a uma determinada estimativa ou linha real. |
| Data de Fim | A data de fim do período em que se encontra a lista de preços é efetiva. | Juntamento com **Data de Início**, este campo é utilizado para determinar qual a lista de preços aplicável a uma determinada estimativa ou linha real. |
| Moeda | A moeda da lista de preços de origem. Isto pode ser alterado. | Quando isto é alterado, todas as linhas de preços resultantes para mão de obra, despesas e itens de catálogo de produtos são convertidas para a moeda de destino da lista de preços durante a cópia. |
| Unidade de Tempo | A moeda da lista de preços de origem. Isto pode ser alterado. | Quando isto é alterado, todas as linhas de preços resultantes para mão de obra são convertidas para a unidade de destino da lista de preços durante a cópia. É utilizada a conversão da configuração da unidade para a unidade de tempo da lista de preços de origem e a unidade de tempo da lista de preços de destino. |
| Descrição | Uma descrição da lista de preços de origem com **-cópia** anexado. Este é um campo de texto e permite-lhe ter uma descrição de várias linhas da lista de preços. | Este campo é mostrado nas vistas **Associadas** na lista de preços em várias entidades que têm listas de preços relacionadas. |

3. Guarde a lista de preços. 

## <a name="update-a-price-list-by-applying-a-mark-up-to-all-the-prices"></a>Atualize uma lista de preços aplicando uma margem de lucro a todos os preços

1. Nos separadores **Função**, **Categoria** e **Item de Lista de Preços** de uma lista de preços, pode selecionar **Atualizar Preços** para aplicar uma margem de lucro para todos os preços na subgrelha. 
2. Na página de diálogo que abre, introduza uma margem de lucro. Também pode introduzir uma percentagem de margem de lucro negativa para diminuir os preços em uma certa percentagem. 
3. Selecione **OK** na página de diálogo e, em seguida, verifique se os preços na subgrelha refletem as alterações efetuadas.


[!INCLUDE[footer-include](../includes/footer-banner.md)]