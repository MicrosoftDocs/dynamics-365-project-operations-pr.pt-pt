---
title: Descrição geral do Project Service Automation
description: Este tópico fornece informações sobre a solução de integração do Dynamics 365 Project Service Automation com o Dynamics 365 Finance.
author: ruhercul
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: ruhercul
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1e1a963bccefd1552aab6e42d3b2d1dc63a82e8f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082545"
---
# <a name="project-service-automation-overview"></a>Descrição geral do Project Service Automation

[!include[banner](../includes/banner.md)]

A solução de integração do Project Service Automation para Finance utiliza a funcionalidade Integração de Dados para sincronizar os dados entre instâncias do Dynamics 365 Finance e do Dynamics 365 Project Service Automation via Common Data Service. Os modelos de integração disponíveis com a funcionalidade Integração de dados permitem o fluxo de projetos, contratos de projetos, projetos, itens de contrato do projeto, marcos de itens de contrato do projeto, tarefas do projeto, categorias de transações de despesas, estimativas de horas e estimativas de despesa do Project Service Automation para o Finance.

> [!NOTE]
> - Se estiver a utilizar a versão 7.3.0, tem de instalar o KB 4074835. Em seguida, poderá integrar projetos de preço fixo.
> - Se estiver a utilizar a versão 7.3.0 e estiver a transferir transações de tarifas a partir do Project Service Automation, terá de instalar o KB 4345320 para incluir essas tarifas na fatura do projeto.
> - Se estiver a utilizar a versão 8.0, poderá utilizar a integração de tarefas do projeto, as categorias de transações de despesas, as estimativas de horas, as estimativas de despesas e o bloqueio de funcionalidades.
> - Se estiver a utilizar a versão 8.0.1 ou posterior, poderá sincronizar os valores reais.

Antes de poder integrar o Project Service Automation Finance, tem de configurar os parâmetros de integração do Project Service Automation. Pata mais informações, consulte [Parâmetros de integração do Project Service Automation](PSA-parameters.md).

Esta solução de integração permite a sincronização direta nos seguintes cenários:

- Mantenha os contratos do projeto no Project Service Automation e sincronize-os diretamente do Project Service Automation para o Finance.
- Crie projetos no Project Service Automation e sincronize-os diretamente do Project Service Automation para o Finance.
- Mantenha os itens de contrato do projeto no Project Service Automation e sincronize-os diretamente do Project Service Automation para o Finance.
- Mantenha os marcos de itens de contrato do projeto no Project Service Automation e sincronize-os diretamente do Project Service Automation para o Finance.
- Mantenha as tarefas do projeto no Project Service Automation e sincronize-os diretamente do Project Service Automation para o Finance.
- Mantenha as categorias de transações de despesas no Finance e sincronize-os diretamente do Finance para o Project Service Automation.
- Crie estimativas de horas do projeto Project Service Automation e sincronize-as diretamente do Project Service Automation para o Finance.
- Crie estimativas de despesa do projeto Project Service Automation e sincronize-as diretamente do Project Service Automation para o Finance.
- Crie dados reais de tempo, despesa e tarifas no Project Service Automation, e crie transações do projeto no diário de integração do Project Service Automation para poderem ser lançados no Finance.

## <a name="data-synchronization"></a>Sincronização de dados

A seguinte ilustração mostra como os dados são sincronizados como parte da integração entre o Project Service Automation e o Finance.

> [!NOTE]
> Nem todos os modelos estão disponíveis atualmente. Os modelos serão lançados à medida que forem concluídos.

[![Integração do Project Service Automation com o Finance](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance"></a>Requisitos doe sistema para o Finance

Para utilizar a solução de integração do Project Service Automation para o Finance, tem de instalar o Enterprise edition 7.3 com Platform update 12 ou posterior.

## <a name="system-requirements-for-project-service-automation"></a>Requisitos de sistema para o Project Service Automation

Para utilizar a solução de integração do Project Service Automation para o Finance, tem de instalar os seguintes componentes:

- Dynamics 365 Project Service Automation versão 9.0.0.0 ou posterior
- Solução de perspetiva de venda para o Dynamics 365 Sales, versão 1.14.0.0 (v14) ou posterior
- Solução Project Service Automation para Finance para o Dynamics 365 Project Service Automation versão 1.0.0.0 ou posterior

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a>Instalar a solução de integração Project Service Automation para Finance na sua instância do Project Service Automation

Transfira a solução de integração Project Service Automation para Finance a partir do [Centro de Transferências da Microsoft](https://www.microsoft.com/download/details.aspx?id=57016) e siga as instruções incluídas com a solução.
