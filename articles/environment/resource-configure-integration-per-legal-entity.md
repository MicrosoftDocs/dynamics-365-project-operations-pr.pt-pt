---
title: Configurar a integração do Project Operations por entidade legal
description: Este tópico fornece informações sobre como configurar integração por entidade legal no Project Operations.
author: sigitac
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: fc3f5be1318d482ece9a6e9e4fadc3cf628ff79577776e679f32cef7c0b2fc8f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6999420"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a>Configurar a integração do Project Operations por entidade legal 

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

Este tópico percorre os passos necessários para configurar o Dynamics 365 Project Operations por entidade legal.

## <a name="enable-feature-keys-in-dynamics-365-finance"></a>Ativar chaves de funcionalidades no Dynamics 365 Finance

Complete os seguintes passos para ativar as funcionalidades necessárias.

1. No Dynamics 365 Finance, vá para a área de trabalho **Gestão de Funcionalidades**.
2. Na **Lista de funcionalidades**, encontre e ative as seguintes funcionalidades:
  
    - **Ativar vários itens de contrato para um projeto**
    - **Ativar o Project Operations no Dynamics 365 Customer Engagement**

> [!NOTE]
> Se não vir as **Chaves de funcionalidades** listadas, verifique se a sua versão do Finance cumpre o requisito mínimo de versão (versão 10.0.13 com todas as atualizações de qualidade aplicadas ou superior). Selecione **Verificar se há atualizações** para atualizar a lista de funcionalidades.

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a>Definir o cenário de implementação do Project Operations para uma entidade legal

Pode ativar o Project Operations no Dynamics 365 Customer Engagement ao nível da entidade legal. Pode ter uma entidade legal a usar o Project Operations no Dynamics 365 Customer Engagement para cenários baseados em recursos/não abastecidos. No mesmo ambiente, pode ter outra entidade legal a utilizar o Project Operations para cenários de abastecimento/produção.

1. No Dynamics 365 Finance, vá para **Gestão de projetos e contabilística** > **Configurar** > **Parâmetros globais da Gestão de projetos e contabilística**.
2. Na lista de entidades legais disponíveis, serão ativadas vários itens de contrato e o Project Operations nas funcionalidades do Dynamics 365 Customer Engagement. Deixe as entidades legais que utilizarão o Project Operations para cenários de encomenda de armazenamento/produção não selecionados.

> [!NOTE]
> Uma entidade legal só pode ser selecionada se não tiver projetos existentes.

## <a name="configure-project-management-and-accounting-parameters"></a>Configurar os parâmetros de Gestão de projetos e contabilística

Cada entidade legal que utiliza o Project Operations no Dynamics 365 Customer Engagement necessita de um conjunto de parâmetros predefinidos. Estes parâmetros estão configurados no separador **Project Operations** na página **Parâmetros da Gestão de projetos e contabilística**. Os parâmetros são:

  - **Predefinições do tipo de faturação**: O Project Operations utilizam um conjunto fixo de predefinições do tipo de faturação que devem ser mapeados para as propriedades de linha Finanças. Criar um registo para cada tipo de faturação: **Não especificado**, **Faturável**, **Não faturável**, **Complementar** e **Não disponível**.
  - **Predefinições de categoria do projeto**: Selecione as categorias de projeto predefinidas a utilizar para cada tipo de transação. Estas predefinições serão utilizadas no **Diário de Integração do Project Operations** e em estimativas onde não é especificada nenhuma categoria de transação para o valor real do projeto.
  - **Previsões**: Selecione o modelo de previsão a utilizar para estimativas de tempo e despesas.


[!INCLUDE[footer-include](../includes/footer-banner.md)]