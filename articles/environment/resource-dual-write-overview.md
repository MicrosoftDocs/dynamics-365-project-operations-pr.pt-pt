---
title: Integração de escrita dupla no Project Operations
description: Este artigo fornece uma descrição geral da integração de escrita dupla do Project Operations.
author: sigitac
ms.date: 04/28/2021
ms.topic: overview
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d365a036f96ff4f7b14107b43e8c6b70df0b5362
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927986"
---
# <a name="project-operations-dual-write-integration-overview"></a>Visão geral da Integração de escrita dupla no Project Operations

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

O Project Operations usa [capacidades de escrita dupla](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) para sincronizar dados entre o Microsoft Dataverse o e o Dynamics 365 Finance.

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
