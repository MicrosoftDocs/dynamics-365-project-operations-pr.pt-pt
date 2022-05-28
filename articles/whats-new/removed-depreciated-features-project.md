---
title: Funcionalidades removidas ou preteridas no Dynamics 365 Project Operations
description: Este tópico descreve funcionalidades que foram removidas ou que têm remoção prevista do Dynamics 365 Project Operations.
author: sigitac
ms.date: 03/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 61bb84b94274762636eb8532f09634db1109e969
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8601584"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-project-operations"></a>Funcionalidades removidas ou preteridas no Dynamics 365 Project Operations

_**Aplica-se a:** Project Operations para cenários baseados em Recursos/Não Stock, implementação Lite – negócio para faturação pró-forma e Project Operations para cenários baseados em Stock/Produção_

Este tópico descreve funcionalidades que foram removidas ou que têm remoção prevista do Dynamics 365 Project Operations.

- Uma funcionalidade *removida* já não está disponível no produto.
- Uma funcionalidade *preterida* não está em desenvolvimento ativo e pode ser removida numa futura atualização.

Esta lista destina-se a ajudá-lo a considerar estas mudanças e preterições para o seu próprio planeamento.

> [!NOTE]
> Informações detalhadas sobre objetos nas aplicações de finanças e operações podem ser encontradas nos [**Relatórios técnicos de referência técnicos**](/dynamics/s-e/global/axtechrefrep_61). Pode comparar as diferentes versões destes relatórios para aprender sobre objetos que mudaram ou foram removidos em cada versão das aplicações de finanças e operações.

## <a name="features-removed-or-deprecated-in-the-project-operations-march-2022-release"></a>Funcionalidades removidas ou preteridas na versão de março de 2022 do Project Operations

### <a name="project-management-and-accounting-always-create-adjustment-transaction-parameter"></a>Parâmetro de gestão de projetos e contabilidade "Criar sempre transações de ajuste"

| &nbsp; | &nbsp; |
|--------|--------|
| **Razão para a preterição/remoção** | São necessárias transações de ajuste para efeitos de auditoria. Após a desapreciação, este parâmetro estará oculto. O sistema vai sempre criar transações de ajuste, da mesma forma que o faz atualmente quando o parâmetro está definido como **Sim**. |
| **Substituído por outra funcionalidade?** | No |
| **Áreas de produto afetadas** | Aplicação |
| **Opção de implementação** | Project Operations para cenários de produção/em stock |
| **Status** | Preterido: até 1 de março de 2023, ocultaremos o parâmetro e alteraremos o comportamento do sistema para que as transações de ajuste sejam sempre criadas. |

### <a name="project-management-and-accounting-use-adjustment-date-as-new-project-date-parameter"></a>Parâmtero de gestão de projetos e contabilidade "Utilizar data de ajuste como nova data do projeto"

| &nbsp; | &nbsp; |
|--------|--------|
| **Razão para a preterição/remoção** | Este parâmetro foi utilizado originalmente para permitir ajustes quando um período fiscal fosse fechado. No entanto, já não é obrigatório, porque a data de contabilidade da transação pode ser alterada para a primeira data do período aberto, se estiver configurada. A data do projeto não deve ser alterada, porque representa a data em que a transação ocorreu. |
| **Substituído por outra funcionalidade?** | No |
| **Áreas de produto afetadas** | Aplicação |
| **Opção de implementação** | Project Operations para cenários de produção/em stock |
| **Status** | Preterido: até 1 de março de 2023, ocultaremos o parâmetro e alteraremos o comportamento do sistema para que a data do projeto nunca seja alterada nos ajustes. |

### <a name="resource-request-workflow-in-project-operations-for-stockedproduction-based-scenarios"></a>Fluxo de trabalho de pedido de recurso no Project Operations para cenários com stock/baseados na produção

| &nbsp; | &nbsp; |
|--------|--------|
| **Razão para a preterição/remoção** | Preterido devido a limitações de volume de transações e baixa utilização. |
| **Substituído por outra funcionalidade?** | No |
| **Áreas de produto afetadas** | Aplicação |
| **Opção de implementação** | Project Operations para cenários de produção/em stock |
| **Status** | Preterido: até 1 de março de 2023, a opção será desativada para pedir recursos para o projeto utilizando o fluxo de trabalho. |

### <a name="project-invoice-proposal-page-without-header-and-lines-views"></a>Página de proposta de fatura do projeto sem as vistas de cabeçalho e linhas

| &nbsp; | &nbsp; |
|--------|--------|
| **Razão para a preterição/remoção** | Preterido devido a melhoramentos à página que foi introduzida juntamente com a chave de funcionalidades **Usar a proposta de fatura do projeto e os formulários de diário de faturas com a vista de cabeçalho e linhas**. |
| **Substituído por outra funcionalidade?** | Sim |
| **Áreas de produto afetadas** | Aplicação |
| **Opção de implementação** | Project Operations para cenários de produção/com stock; Project Operations para cenários de recursos/sem stock |
| **Status** | Preterido: até 1 de março de 2023, a página anterior (legada) será desligada e a ligada a chave de funcionalidades **Utilizar a proposta de fatura do projeto e os formulários de diário de faturas com a vista de cabeçalho e linhas** por predefinição. |

## <a name="features-removed-or-deprecated-in-the-project-operations-december-2021-release"></a>Funcionalidades removidas ou preteridas na versão de dezembro de 2021 do Project Operations

### <a name="collaboration-workspaces"></a>Áreas de trabalho de colaboração

[Criar ou ligar a uma área de trabalho de colaboração (Projeto)](/dynamicsax-2012/appuser-itpro/create-or-link-to-a-collaboration-workspace-project)

| &nbsp; | &nbsp; |
|--------|--------|
| **Razão para a preterição/remoção** | Preterido devido a pouca utilização. Os clientes que utilizam o Project Operations para cenários de recursos/fora de stock podem tirar partido da [Colaboração com Grupos do Office](../project-management/collaboration-groups.md). |
| **Substituído por outra funcionalidade?** | No |
| **Áreas de produto afetadas** | Aplicação  |
| **Opção de implementação** | Project Operations para cenários de produção/em stock |
| **Status** | Preterido: até 1 de dezembro de 2022, pretendemos deixar de suportar áreas de trabalho de Colaboração. |
