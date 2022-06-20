---
title: Configurar a integração do Project Operations por entidade legal
description: Este artigo fornece informações sobre configurar a integração por entidade legal no Project Operations.
author: sigitac
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3f33e641ee0932655282618c99a26e2603660059
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914692"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a>Configurar a integração do Project Operations por entidade legal 

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

Este artigo orienta-o ao longo dos passos necessários para configurar o Dynamics 365 Project Operations por entidade legal.

## <a name="enable-feature-keys-in-dynamics-365-finance"></a>Ativar chaves de funcionalidade no Dynamics 365 Finance

Complete os seguintes passos para ativar as funcionalidades necessárias.

1. No Dynamics 365 Finance, aceda à área de trabalho **Gestão de funcionalidades**.
2. Na **Lista de funcionalidades**, encontre e ative as seguintes funcionalidades:
  
    - **Ativar vários itens de contrato para um projeto**
    - **Ativar o Project Operations no Dynamics 365 Customer Engagement**

> [!NOTE]
> Se não vir as **Chaves de funcionalidades** listadas, verifique se a sua versão do Finance cumpre o requisito mínimo de versão (versão 10.0.13 com todas as atualizações de qualidade aplicadas ou superior). Selecione **Verificar se há atualizações** para atualizar a lista de funcionalidades.

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a>Definir o cenário de implementação do Project Operations para uma entidade legal

Pode ativar o Project Operations no Dynamics 365 Customer Engagement num nível de entidade legal. Pode ter uma entidade legal utilizando o Project Operations no Dynamics 365 Customer Engagement para cenários baseados em recursos/sem stock. No mesmo ambiente, pode ter outra entidade legal a utilizar o Project Operations para cenários de abastecimento/produção.

1. No Dynamics 365 Finance, aceda a **Gestão de projetos e contabilidade** > **Configuração** > **Parâmetros de gestão de projetos e contabilidade**.
2. Na lista de entidades legais disponíveis, selecione entidades nas quais estarão ativados vários itens de contrato e o Project Operations no Dynamics 365 Customer Engagement. Deixe as entidades legais que utilizarão o Project Operations para cenários de encomenda de armazenamento/produção não selecionados.

> [!NOTE]
> Uma entidade legal só pode ser selecionada se não tiver projetos existentes.

## <a name="configure-project-management-and-accounting-parameters"></a>Configurar os parâmetros de Gestão de projetos e contabilística

Cada entidade legal que utiliza o Project Operations no Dynamics 365 Customer Engagement necessita de um conjunto de parâmetros predefinidos. Estes parâmetros estão configurados no separador **Project Operations** na página **Parâmetros da Gestão de projetos e contabilística**. Os parâmetros são:

  - **Predefinições do tipo de faturação**: O Project Operations utilizam um conjunto fixo de predefinições do tipo de faturação que devem ser mapeados para as propriedades de linha Finanças. Criar um registo para cada tipo de faturação: **Não especificado**, **Faturável**, **Não faturável**, **Complementar** e **Não disponível**.
  - **Predefinições de categoria do projeto**: Selecione as categorias de projeto predefinidas a utilizar para cada tipo de transação. Estas predefinições serão utilizadas no **Diário de Integração do Project Operations** e em estimativas onde não é especificada nenhuma categoria de transação para o valor real do projeto.
  - **Previsões**: Selecione o modelo de previsão a utilizar para estimativas de tempo e despesas.


[!INCLUDE[footer-include](../includes/footer-banner.md)]