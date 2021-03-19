---
title: Sincronizar tarefas do projetos diretamente do Project Service Automation para o Finance and Operations
description: Este tópico descreve o modelo e a tarefa subjacente que são utilizados para sincronizar as tarefas do projeto diretamente do Microsoft Dynamics 365 Project Service Automation para o Dynamics 365 Finance.
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 7cc9ee9de576549c132e14c333a1000c22a55236
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288933"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a>Sincronizar tarefas do projetos diretamente do Project Service Automation para o Finance and Operations

[!include[banner](../includes/banner.md)]

Este tópico descreve o modelo e a tarefa subjacente que são utilizados para sincronizar as tarefas do projeto diretamente do Dynamics 365 Project Service Automation para o Dynamics 365 Finance.

> [!NOTE]
> - A integração de tarefas do projeto, as categorias de transações de despesas, as estimativas de horas, as estimativas de despesas e o bloqueio de funcionalidades estão disponíveis na versão 8.0.
> - Se estiver a utilizar a Enterprise edition 7.3.0 depois de instalar o KB 4132657 e o KB 4132660, poderá utilizar os modelos para integrar tarefas de projeto, categorias de transações de despesas, estimativas de horas, estimativas de despesas e valores reais, e para configurar o bloqueio de funcionalidades. Se tiver de repor as distribuições contabilísticas, recomendamos que também instale o KB 4131710.
> - A integração dos valores reais está disponível na versão 8.0.1 ou posterior.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Fluxo de dados para o Project Service Automation para o Finance

A solução de integração do Project Service Automation para Finance utiliza a funcionalidade Integração de Dados para sincronizar os dados entre instâncias do Project Service Automation e do Finance. O modelo de integração que está disponível com a funcionalidade Integração de dados permite o fluxo de dados sobre as tarefas do projeto entre o Project Service Automation e o Finance.

A seguinte ilustração mostra como os dados são sincronizados entre o Project Service Automation e o Finance.

[![Fluxo de dados para a integração do Project Service Automation com o Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>Modelo e tarefa

Para aceder ao modelo, no centro de administração do Microsoft Power Apps, selecione **Projetos** e, em seguida, no canto superior direito, selecione **Novo projeto** para selecionar modelos públicos.

O modelo seguinte e a tarefa subjacente são utilizados para sincronizar as tarefas do projeto do Project Service Automation para o Finance:

- **Nome do modelo na Integração de dados:** tarefas do projeto (PSA para Fin and Ops)
- **Nome da tarefa no projeto:** Tarefas do projeto

Antes de poder ocorrer a sincronização das tarefas do projeto, é necessário sincronizar os contratos de projeto e os projetos.

## <a name="entity-set"></a>Conjunto de entidades

| Project Service Automation | Finanças                             |
|----------------------------|-------------------------------------|
| Tarefas do Projeto              | Entidade de integração para a tarefa de projeto |

## <a name="entity-flow"></a>Fluxo de entidades

As tarefas do projeto são geridas no Project Service Automation e sincronizadas com o Finance como atividades de projeto.

## <a name="prerequisites-and-mapping-setup"></a>Pré-requisitos e configuração do mapeamento

Antes de poder ocorrer a sincronização das tarefas do projeto, é necessário sincronizar os contratos de projeto e os projetos.

## <a name="power-query"></a>Power Query

Tem de utilizar o Microsoft Power Query para Excel para filtrar os dados se esta condição se verificar:

- Tem registos específicos de recursos numa tarefa de projeto.

Se tiver de utilizar o Power Query, siga esta diretriz:

- O modelo Tarefas de projeto (PSA para Fin and Ops) tem um filtro predefinido que exclui os registos específicos do recurso de uma tarefa do projeto ao definir o filtro em **IsLineTask** como **False**. Se criar o seu próprio modelo, terá de adicionar este filtro.

## <a name="template-mapping-in-data-integration"></a>Mapeamento de modelos na Integração de dados

A seguinte ilustração mostra um exemplo dos mapeamentos de tarefas do modelo na Integração de Dados. O mapeamento mostra as informações do campo que serão sincronizadas do Project Service Automation para Finance.

[![Mapeamento de modelos](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]