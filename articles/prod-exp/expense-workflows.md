---
title: Configurar fluxos de trabalho de gestão de Despesas
description: Pode configurar um processo de fluxo de trabalho usado para rever e aprovar documentos de viagem e despesas.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0af23ed2cf172e4c90de72f5db389c349303c039
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082558"
---
# <a name="set-up-expense-management-workflows"></a>Configurar fluxos de trabalho de gestão de Despesas

[!include [banner](../includes/banner.md)]

Pode configurar um processo de fluxo de trabalho usado para rever e aprovar documentos de viagem e despesas. Os documentos para os quais os fluxos de trabalho podem ser definidos para incluir relatórios de despesas, requisições de viagem e pedidos de adiantamento de dinheiro.

Um fluxo de trabalho representa um processo de negócio. Define como um documento flui através do sistema e indica quem deve completar uma tarefa ou aprovar um documento. Existem vários benefícios ao usar o sistema de fluxo de trabalho na sua organização:

-   **Processos consistentes** – Pode definir o processo de aprovação de documentos específicos, como requisições de compras e relatórios de despesas. A utilização do sistema de fluxo de trabalho ajuda a garantir que os documentos são processados e aprovados de forma consistente e eficiente.

-   Visibilidade do processo – Pode acompanhar o estado, o histórico e as métricas de desempenho de uma instância específica de fluxo de trabalho. Isto ajuda-o a determinar se devem ser feitas alterações ao fluxo de trabalho para melhorar a eficiência.

-   Lista de trabalho centralizada – Os utilizadores podem visualizar uma lista de trabalho centralizada para visualizar as tarefas e aprovações de fluxo de trabalho que lhes são atribuídas. 

**Os tipos de fluxos de trabalho que pode criar**

A tabela seguinte lista os tipos de fluxos de trabalho que pode criar em **Despesas**.


|              <strong>Tipo</strong>              |                   <strong>Use este tipo para</strong>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <strong>Relatório de despesas</strong>         |            Criar aprovação de fluxos de trabalho para relatórios de despesas.             |
|  <strong>Publicar automaticamente relatórios de despesas</strong>   |        Criar automaticamente a publicação de fluxos de trabalho para relatórios de despesas.        |
|       <strong>Item de linha de despesa</strong>        |     Criar aprovação de fluxos de trabalho para itens de linha nos relatórios de despesas.      |
| <strong>Publicação automática de item de linha de despesas</strong> | Criar publicação automática de fluxos de trabalho para itens de linha nos relatórios de despesas. |
|       <strong>Requisição de viagens</strong>       |          Criar aprovação de fluxos de trabalho para requisições de viagem.           |
|      <strong>Pedido de adiantamento de dinheiro</strong>      |         Criar aprovação de fluxos de trabalho para pedidos de adiantamento de dinheiro.          |
|        <strong>Recuperação da taxa de IVA</strong>        | Criar aprovação de fluxos de trabalho para a recuperação do imposto sobre o valor acrescentado (IVA).  |

