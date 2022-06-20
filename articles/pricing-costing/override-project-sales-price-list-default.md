---
title: Substituir listas de preços de vendas do projeto
description: Este artigo fornece informações sobre a criação de listas de preços de vendas personalizadas.
author: rumant
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 8d0a769f415679b08f3228fcb14fbbbd37533ebc
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911932"
---
# <a name="override-project-sales-price-lists"></a>Substituir listas de preços de vendas do projeto

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

## <a name="customer-specific-project-price-lists"></a>Listas de preços de projeto específicas do cliente

Os contratos de preços específicos do cliente podem ser configurados como listas de preços do projeto num registo de conta no Dynamics 365 Project Operations.

Para configurar uma lista de preços de projeto específica do cliente, na área **Vendas**, navegue para o registo da conta.

1. Abra a página de lista **Contas**.
2. Localize e clique duas vezes num registo de cliente para abrir a página de detalhes da **Conta**.
3. No separador **Listas de preços do Projeto**, selecione **+ Nova Lista de preços do Projeto**.
4. Na página **Nova Lista de Preços do Projeto**, selecione uma lista de preços a partir da lista pendente. Apenas listas de preços que tenham o contexto definido para **Vendas** e cuja moeda corresponda à moeda da conta estão incluídas.
5. Nomeie a associação e, em seguida, selecione **Guardar**. É criada uma lista de preços de projeto específica do cliente. Esta lista de preços será utilizada para os preços de projeto predefinidos em propostas de projetos ou contratos criados para este cliente, sempre que a data criada do contrato de proposta ou projeto se insere na data da efetividade da lista de preços.

## <a name="custom-pricing-on-project-quotes"></a>Preços personalizados em propostas de projeto

Nas propostas de projeto, pode ter preços de projeto que começam com uma lista de preços padrão predefinida que assume a predefinição do cliente ou dos parâmetros do projeto.

Quando precisa de preços personalizados para trabalhos relacionados com projetos numa determinada proposta, pode obtê-los a partir da entidade associada às listas de preços de projeto.

Complete os seguintes passos para configurar preços de projeto específicos da proposta.

1. Abra a proposta do projeto e selecione o separador **Listas de Preços do Projeto**.
2. Na subgrelha, selecione **Criar preços personalizados**.

Todas as listas de preços do projeto que estão anexadas à proposta são copiadas para novas listas de preços. Os nomes das novas listas de preços refletem o nome da proposta com um carimbo de data/hora para quando estas listas de preços foram criadas.

Pode utilizar cada uma dessas listas de preços e atualizar os preços de mão de obra (preço de função) e despesas (preço de categoria). Estes preços só serão aplicáveis a esta proposta de projeto.

## <a name="price-lists-on-a-project-contract"></a>Listas de preços num contrato do projeto

Num contrato do projeto, os preços do projeto assumem sempre a predefinição de uma lista de preços personalizada com o nome do contrato e o carimbo de data/hora criado anexado ao nome. Isto é verdade se o contrato foi criado quando a proposta foi ganha ou se o contrato foi criado de raiz. Se necessário, pode remover esta associação à lista de preços personalizada e associar uma lista de preços padrão ao contrato do projeto.

Quando associar uma lista de preços padrão às listas de preços do projeto na proposta ou no contrato, quaisquer alterações efetuadas aos preços na lista de preços terão impacto em todas as propostas e contratos que utilizem a lista de preços.


[!INCLUDE[footer-include](../includes/footer-banner.md)]