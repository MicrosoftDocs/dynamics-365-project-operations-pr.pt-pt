---
title: Gerir listas de preços de projetos em contratos do projeto
description: Este artigo fornece informações sobre gerir listas de preços de projeto em contratos de projeto.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 23b9e6f9bc3e4bc3fb03de62064644dd58da34c7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926192"
---
# <a name="manage-project-price-lists-on-project-contracts"></a>Gerir listas de preços de projetos em contratos do projeto

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

Os contratos de Projeto no Dynamics 365 Project Operations destinam-se a suportar várias listas de preços de vendas efetivas de data num contrato. No Project Operations, existe uma nova entidade associada chamada **Listas de Preços do Projeto**. Esta entidade tem uma relação de um para muitos com um contrato de projeto.

As listas de preços do projeto são usadas para o tempo de preço, material e transações de despesas num projeto. Quando um contrato tem uma ou mais listas de preços do projeto, estas listas de preços são usadas para o preço do tempo, material, estimativas de despesas e valores reais em projetos que estão associados ao contrato através do item de contrato.

Quando não há listas de preços do projeto num contrato de projeto, verá uma mensagem de aviso de que não há listas de preços do projeto e as suas estimativas, trabalhos reais de projeto, material e despesas registadas não serão avaliadas. Não haverá preço para os valores de venda.

## <a name="associate-or-unassociate-a-project-price-list-on-a-project-contract"></a>Associado ou não associado a uma lista de preços do projeto num contrato de projeto

### <a name="create-or-associate-a-specific-price-list-for-estimating-project-based-work-material-and-expenses"></a>Criar ou associar uma lista de preços específica para calcular trabalho, material e despesas baseadas em projetos

1. No contrato do projeto, selecione o separador **Listas de Preços do Projeto**.
2. Na subgrelha, selecione **+ Adicionar Nova Lista de Preços do Projeto**.
3. No controlador de deslize **Criação Rápida**, selecione uma lista de preços. 

  A lista pendente mostra todas as listas de preços que têm o contexto definido para **Vendas**, onde a moeda na lista de preços corresponde à moeda do contrato.
  
4. Introduza uma descrição para a associação da lista de preços do projeto, selecione **Guardar** e, em seguida, feche o controlador de deslize **Criação Rápida**.

   É criada uma associação de listas de preços do projeto.
   
5. Repita os passos 1-4 para associar mais do que uma lista de preços do projeto ao contrato do projeto. Só crie várias listas de preços do projeto se tiver uma data diferente em cada uma das listas de preços do projeto associada.

> [!NOTE]
> O Project Operations não suporta a sobreposição da efetividade da data das listas de preços do projeto. Se houver várias listas de preços de projeto para uma transação com uma determinada data, o preço dessa transação assumirá a predefinição zero.

### <a name="remove-a-project-price-list-association"></a>Remover uma associação de lista de preços de projeto

- Selecione a lista de preços do projeto e, em seguida, selecione **Eliminar Lista de Preços do Projeto do Contrato** na subgrelha. 

  A lista de preços é removida das listas de preços do projeto no contrato. A lista de preços em si não será eliminada. Só a associação ao contrato será eliminada.

## <a name="set-up-automatic-defaulting-of-project-price-lists-on-a-contract"></a>Configurar a predefinição automática das listas de preços do projeto num contrato

Uma lista de preços do projeto pode ser configurada como a lista de preços do projeto padrão. Esta configuração garante que todos os contratos da sua organização começam sempre com uma lista de preços padrão do projeto para esse período de preços.

### <a name="set-up-the-organizational-default-for-project-price-lists"></a>Configurar a predefinição organizacional para listas de preços do projeto

1. Vá a **Definições** > **Geral** e, em seguida, selecione **Parâmetros**.
2. Na página da lista de **Parâmetros Ativos**, selecione e clique duas vezes no registo para o abrir. Ao clicar duas vezes, certifique-se de que não está a clicar num valor de campo que seja hiperligação. 
3. Na página **Parâmetros Ativos**, selecione o separador **Lista de Preços**. Uma subgrelha mostra uma lista de listas de preços predefinidos. Esta é uma lista das listas de preços de custos e vendas padrão. Ter uma lista de preços de **Vendas** associada aqui para cada moeda que vende garante que a lista de preços de venda é a predefinida em qualquer contrato que cria para clientes que efetuam transações nesta moeda.

### <a name="set-up-a-customer-specific-project-price-list"></a>Configurar uma lista de preços de projeto específica do cliente

Também pode configurar listas de preços específicas do projeto quando negociou um contrato de preços principal com os seus clientes.

1. Aceda a **Vendas** > **Clientes**.
2. A partir da lista de contas ativas, selecione o cliente para quem tem uma lista de preços especiais.
3. Selecione o registo do cliente para o abrir e, em seguida, selecione o separador **Listas de Preços do Projeto**. Uma subgrelha mostra uma lista de listas de preços do projeto específicas para este cliente. 
4. Crie aqui uma nova associação de preços para ter uma lista de preços de projeto específica para este cliente.

## <a name="custom-pricing-on-a-project-contract"></a>Preços personalizados num contrato de projeto

Depois de ter listas de preços de projetos específicos e organizacionais, os seus contratos de projeto serão criados automaticamente com estas associações de preços do projeto. No entanto, as listas de preços do projeto num contrato de projeto são sempre copiadas com a data e o nome do contrato que lhes são anexados. Os gestores de conta e de projetos podem então começar a fazer edições a preços nestas cópias. Estes preços alterados só serão aplicáveis a este contrato de projeto.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
