---
title: Parâmetros de integração do Project Service Automation
description: Este tópico explica como configurar a forma como os dados predefinidos são introduzidos quando integra o Microsoft Dynamics 365 for Project Service Automation com o Microsoft Dynamics 365 Finance.
author: ruhercul
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: b58f34cb74be531a98518100158f39d74f136afc34444468d666cd4e9394af6f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 08/06/2021
ms.locfileid: "7005855"
---
# <a name="project-service-automation-integration-parameters"></a>Parâmetros de integração do Project Service Automation

[!include[banner](../includes/banner.md)]

Na página **Parâmetros de integração do Project Service Automation**, pode configurar a forma como os dados predefinidos são introduzidos quando integra o Dynamics 365 Project Service Automation com o Dynamics 365 Finance. Para os projetos serem sincronizados com êxito do Project Service Automation para o Finance, tem de configurar os seguintes campos.

Para abrir a página **Parâmetros de integração do Project Service Automation**, vá para **Gestão de projetos e contabilística** \> **Configurar** \> **Parâmetros de integração do Dynamics 365 for Project Service Automation**. 

> [!NOTE]
> - A integração de tarefas do projeto, as categorias de transações de despesas, as estimativas de horas, as estimativas de despesas e o bloqueio de funcionalidades estão disponíveis na versão 8.0.
> - A integração dos valores reais está disponível na versão 8.0.1 ou posterior.


| Tabulação                    | Campo                | Descrição |
|------------------------|----------------------|-------------|
| Geral                | Tipo de projeto predefinido | Selecione o tipo de projeto predefinido. Quando os projetos são sincronizados a partir do Project Service Automation, este valor é utilizado se não forneceu um valor predefinido no modelo de integração. Durante a sincronização, o campo **Tipo de projeto** dos novos projetos é definido com este valor. No entanto, o valor poderá ser atualizado quando os itens de contrato do projeto são sincronizados a partir do Project Service Automation. |
|                        | Categoria de tempo        | Selecione a categoria de tempo predefinida. Este valor é utilizado quando as estimativas de horas são sincronizadas a partir do Project Service Automation. Quando as estimativas de horas e os valores reais de hora são sincronizados a partir do Project Service Automation, o campo **Categoria** das novas previsões de horas do projeto no Finance é definido com este valor. |
|                        | Categoria de tarifa         | Selecione a categoria de tarifa predefinida. Este valor é utilizado quando os valores reais da tarifa são sincronizados a partir do Project Service Automation. Quando os valores reais de tarifa são sincronizados a partir do Project Service Automation, o campo **Categoria** das novas transações de tarifas no Finance é definido com este valor. |
| Valores predefinidos do grupo do projeto | Tipo de projeto         | Clique em **Novo** para adicionar uma linha onde pode selecionar o tipo de projeto para o qual definir o grupo de projeto predefinido. Um tipo de projeto específico só pode ser selecionado uma vez na configuração. |
|                        | Grupo do projeto        | Selecione o grupo do projeto predefinido para o tipo de projeto selecionado. Quando são sincronizados novos projetos a partir do Project Service Automation, o campo **Grupo do projeto** é estabelecido com o valor predefinido para o tipo de projeto, se não forneceu um valor predefinido no modelo de integração. |
| Valores predefinidos do tipo de faturação  | Tipo de faturação         | Clique em **Novo** para adicionar uma linha onde pode selecionar o tipo de faturação para o qual definir a propriedade de linha predefinida. Um tipo de faturação específico só pode ser selecionado uma vez na configuração. |
|                        | Propriedade da linha        | Selecione a propriedade da linha predefinida para o tipo de faturação selecionado. Quando são sincronizadas novas estimativas de horas, novas estimativas de despesas ou novos valores reais a partir do Project Service Automation, o campo **Propriedade da linha** é estabelecido para o valor predefinido para o tipo de faturação. |
| Bloqueio de funcionalidades  | Não aplicável       | Selecione a funcionalidade para desativar no Finance para projetos e contratos com origem no Project Service Automation. Por exemplo, pode desativar a capacidade de editar contratos e projetos, criar estruturas hierárquicas de trabalho e introduzir folhas de horas no Finance. Os campos relacionados com a contabilidade continuarão a estar ativados, mesmo que sejam indisponibilizados pela definição de parâmetros. Por predefinição, todas as funcionalidades estão ativadas. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]