---
title: Atualizar um projeto
description: Este tópico fornece informações sobre como atualizar projetos no Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 5c9cd0c7c6886bd454c5f2ef2ae7f20d1707293f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897826"
---
# <a name="update-a-project"></a>Atualizar um projeto

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

Abaixo é apresentado um resumo dos campos que podem ser atualizados num projeto depois de ser criado e quaisquer implicações aplicáveis das atualizações.

## <a name="project-detail-fields"></a>Campos de detalhe do projeto

- **Nome**: o título do projeto.
- **Descrição**: uma descrição geral do projeto.
- **Cliente**: a empresa à qual o projeto será entregue.
- **Modelo de calendário**: o horário de trabalho do projeto. Quando o campo é alterado, toda a agenda é recalculada.
- **Moeda**: a moeda para o projeto. Este campo assume por predefinição a moeda definida na unidade de contratação. Quando a unidade de contratação é atualizada, o campo também é atualizado.
- **Unidade de Contratação**: a unidade organizacional que representa o grupo ou a divisão da empresa, responsável principalmente pela vitória da venda e gestão da entrega de trabalho e serviços ao cliente. 
- **Gestor de Projeto**: o membro da equipa do projeto que tem autoridade para rever e aprovar entradas de tempo e despesas.

## <a name="estimate-fields"></a>Campos de estimativa

- **Data de Início Estimada**: a data em que o projeto começará. Quando este campo for atualizado, quaisquer tarefas no projeto serão movidas proporcionalmente com a nova data de início.
- **Data de Fim**: a data agendada para o final do projeto.
- **Esforço**: o esforço estimado do projeto. Quando as tarefas são adicionadas ao projeto, este campo já não é editável.
- **Custo Estimado da Mão de Obra**: o custo da mão de obra estimado do projeto. Quando os custos de mão de obra são adicionados ao projeto, este campo já não é editável.
- **Despesas Estimadas**: as despesas estimadas do projeto. Quando as despesas são adicionadas ao projeto, este campo já não é editável.

## <a name="project-actual-fields"></a>Campos reais do projeto
- **Início Real**: a data em que o projeto começou.
- **Fim Real**: para ser atualizado quando um projeto for concluído.

## <a name="project-status-fields"></a>Campos de estado do projeto

- **Estado Geral do Projeto**: o estado global do projeto fornecido pelo Gestor de projeto.
- **Comentários**: uma narrativa sobre o estado atual do projeto fornecido pelo Gestor de projeto.

