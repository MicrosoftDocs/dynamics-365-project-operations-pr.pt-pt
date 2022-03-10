---
title: Integração de escrita dupla no Project Operations
description: Este tópico fornece uma visão geral da integração de escrita dupla no Project Operations.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: b65c40e8aaa9524c1c634738dadd23f21e86e2ec095c47bc849467c8806addbc
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007925"
---
# <a name="project-operations-dual-write-integration-overview"></a>Visão geral da Integração de escrita dupla no Project Operations

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

O Project Operations utiliza [capacidades de dupla escrita](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) para sincronizar dados através de Microsoft Dataverse e Dynamics 365 Finance.

A seguinte ilustração mostra como os dados são sincronizados como parte desta integração entre Dataverse e finanças.

![Visão geral dos fluxos de dados do Project Operations.](./media/ProjectOperationsFlows.jpg)

O Project Operations no Dataverse fornece uma interface de utilizador moderna (UI) e fácil extensibilidade sem código/código baixo utilizando as capacidades Power Platform. Gestores de projetos, gestores de recursos, membros da equipa do projeto, e outras personalidades de front-office, realizam as suas atividades no Project Operations no Dataverse.

O Project Operations em Finanças proporciona apoio à contabilidade do projeto e ao reconhecimento de receitas. O Project Operations liga-se ao quadro financeiro das Finanças para o cálculo do imposto sobre as vendas, as taxas de câmbio, o reporte de dimensão financeira e muito mais. As experiências de contabilista do Projeto são maioritariamente baseadas em Finanças.

A integração do Project Operations consiste na seguinte integração de componentes:


- [Configuração do Project Operations e integração de dados de configuração](resource-dual-write-setup-integration.md) 
- [Valores reais e estimativas de Projeto](resource-dual-write-estimates-actuals.md)
- [Faturas do Projeto](resource-dual-write-project-invoice.md)
- [Gestão de despesas](resource-dual-write-expense.md)
- [Fatura de fornecedor](resource-dual-write-vendor-invoice.md)
