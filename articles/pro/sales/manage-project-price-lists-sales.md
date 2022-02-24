---
title: Gerir listas de preços de projetos em propostas do projeto
description: Este tópico fornece informação sobre como trabalhar com listas de preços do projeto em propostas.
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 912d2fad33ac02c3ba980da7eeb88eef5c331230
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858622"
---
# <a name="manage-project-price-lists-on-project-quotes"></a>Gerir listas de preços de projetos em propostas do projeto 

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

As propostas do projeto foram concebidas para suportar várias listas de preços de venda em vigor em várias datas. Com o Dynamics 365 Project Operations, é adicionada uma nova entidade associada chamada **Listas de preços do projeto**. Esta entidade tem uma relação de 1 para muitos com uma proposta de projeto.

As listas de preços do projeto são usadas para o tempo de preço, material e transações de despesas num projeto. Quando uma proposta tem uma ou mais listas de preços do projeto, estas listas de preços são usadas para o preço do tempo, material, estimativas de despesas e valores reais em projetos que estão associados à proposta através da linha de proposta.

Quando não existem listas de preços do projeto numa proposta de projeto, receberá uma mensagem de aviso. A mensagem indica que, como não existem listas de preços do projeto, não se fixará o preço do seu trabalho e das suas despesas estimados e reais do projeto. Em vez disso, terão o preço zero (0) para os valores de venda.

## <a name="associate-or-disassociate-a-project-price-list-on-a-project-quote"></a>Associar ou desassociar uma lista de preços do projeto numa proposta de projeto

Para criar ou selecionar uma lista de preços específica para estimar o trabalho e as despesas baseados no projeto, conclua os seguintes passos.

1. Na proposta, selecione o separador **Preço do Projeto** e, na subgrelha, selecione **+ Adicionar Nova Lista de Preços do Projeto**.
2. Na página Criação Rápida, selecione uma lista de preços. A lista pendente mostra todas as listas de preços com o contexto definido como **Vendas** e a moeda corresponde à moeda na proposta.
4. Introduza uma descrição para a associação da lista de preços do projeto e selecione **Guardar e Fechar**.

É criada uma associação de listas de preços do projeto.

Pode repetir este processo se precisar de associar mais de uma lista de preços do projeto à proposta de projeto. Crie várias listas de preços do projeto apenas se tiver datas efetivas diferentes em cada uma das listas de preços do projeto associadas.

> [!NOTE]
> O Project Operations não suporta a sobreposição de datas efetivas das listas de preços do projeto. Se existirem várias listas de preços do projeto para uma transação com determinada data, o preço nessa transação será assumido por predefinição como zero (0).
Para remover uma associação de listas de preços do projeto, selecione a lista de preços do projeto e, em seguida, selecione **Eliminar Lista de Preços do Projeto de Proposta**. A lista de preços é removida das listas de preços do projeto da proposta, mas a própria lista de preços não é eliminada. Só a associação à proposta é eliminada.

## <a name="set-up-default-project-price-lists-on-a-quote"></a>Configurar listas de preços de projeto predefinidas numa proposta

As listas de preços do projeto podem ser configuradas para assumirem por predefinição uma proposta de projeto. Esta configuração assegura que todas as propostas na sua organização começam sempre com uma lista de preços predefinidos para esse período de preços.

### <a name="set-up-organizational-default-for-project-price-lists"></a>Configurar valor por predefinição organizacional para as listas de preços de projetos

1. Vá para **Definições** > **Geral** > **Parâmetros**.
2. Na página da lista **Parâmetros Ativos**, localize o registo e faça duplo clique para o abrir. 
3. Na página **Parâmetros**, selecione o separador **Lista de Preços**. Pode ver que a lista de preços predefinida é mostrada. Esta é uma lista d custos predefinida e as listas de preços de venda. Ter uma lista de preços de venda associada aqui para cada moeda em que vende vai assegurar que esta lista de preços de venda é assumida por predefinição em qualquer proposta que crie para os clientes que fazem transações nesta moeda.

### <a name="set-up-customer-specific-project-price-lists"></a>Configurar listas de preços de projetos específicas do cliente

As listas de preços do projeto específicas do cliente também podem ser configuradas quando tiver negociado um contrato de preços principal com os seus clientes.

Para configurar uma lista de preços do projeto específica do cliente, conclua os seguintes passos.

1. Na área **Vendas**, selecione **Clientes**.
2. Na lista das suas contas ativas, selecione e abra o registo de cliente para o qual tem uma lista de preços especiais.
3. No separador **Listas de Preços do Projeto**, pode criar uma nova associação de listas de preços para ter a lista de preços do projeto específica para este cliente.

## <a name="create-custom-pricing-on-a-project-quote"></a>Criar preços personalizados numa proposta de projeto

Depois de ter listas de preços de projeto predefinidas específicas do cliente e organizacionais, as suas propostas de projeto serão criadas automaticamente com estas associações de listas de preços de projeto. No entanto, em determinados casos, poderá ser necessário criar preços personalizados para uma proposta de projeto específica. 

1. No separador **Proposta do Projeto**, no separador **Lista de Preços do Projeto**, certifique-se na subgrelha que não está selecionado nenhum registo da lista de preços específico.
2. Selecione **Criar Lista de Preços Personalizada**. Isto fará cópias de todas as listas de preços padrão atualmente associadas à proposta e associará estas cópias à proposta. As associações existentes às listas de preços predefinidas serão removidas. O vendedor pode então começar a fazer edições aos preços nestas cópias. Estes preços alterados serão aplicáveis apenas a esta proposta de projeto.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
