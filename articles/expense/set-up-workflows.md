---
title: Configurar fluxos de trabalho para a gestão de despesas
description: Pode configurar um processo de fluxo de trabalho usado para rever e aprovar documentos de viagem e despesas.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: af6463b07e282ae1ff6aa7dc1a540ff7c8cc318a
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127712"
---
# <a name="set-up-workflows-for-expense-management"></a>Configurar fluxos de trabalho para a gestão de despesas

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

Pode configurar um processo de fluxo de trabalho usado para rever e aprovar documentos de viagem e despesas. Pode definir fluxos de trabalho para relatórios de despesas, requisições de viagem e pedidos de adiantamento de dinheiro.

Um fluxo de trabalho representa um processo de negócio e define como um documento flui através do sistema. O fluxo de trabalho também indica quem deve completar uma tarefa ou aprovar um documento. Existem vários benefícios ao usar o sistema de fluxo de trabalho na sua organização:

- **Processos consistentes**: Pode definir o processo de aprovação de documentos específicos, como requisições de compras e relatórios de despesas. A utilização do sistema de fluxo de trabalho ajuda a garantir que os documentos são processados e aprovados de forma consistente e eficiente.
- **Visibilidade do processo**: Pode acompanhar o estado, o histórico e as métricas de desempenho de uma instância específica de fluxo de trabalho. Isto ajuda-o a determinar se devem ser feitas alterações ao fluxo de trabalho para melhorar a eficiência.
- **Lista de trabalho centralizada**: Os utilizadores podem visualizar uma lista de trabalho centralizada para visualizar as tarefas e aprovações de fluxo de trabalho que lhes são atribuídas. 

## <a name="workflow-types"></a>Tipos de fluxo de trabalho

A tabela seguinte lista os tipos de fluxos de trabalho que pode criar em **Gestão de despesas**.


|              <strong>Tipo</strong>              |                   <strong>Use este tipo para</strong>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <strong>Aprovar automaticamente relatórios de despesas</strong> |            Criar aprovação de fluxos de trabalho para relatórios de despesas.             |
|  <strong>Publicar automaticamente relatórios de despesas</strong>   |        Criar automaticamente a publicação de fluxos de trabalho para relatórios de despesas.        |
|       <strong>Item de linha de despesa</strong>        |     Criar aprovação de fluxos de trabalho para itens de linha nos relatórios de despesas.      |
| <strong>Publicação automática de item de linha de despesas</strong> | Criar publicação automática de fluxos de trabalho para itens de linha nos relatórios de despesas. |
|       <strong>Requisição de viagens</strong>       |          Criar aprovação de fluxos de trabalho para requisições de viagem.           |
|      <strong>Pedido de adiantamento de dinheiro</strong>      |         Criar aprovação de fluxos de trabalho para pedidos de adiantamento de dinheiro.          |
|        <strong>Recuperação da taxa de IVA</strong>        | Criar aprovação de fluxos de trabalho para a recuperação do imposto sobre o valor acrescentado (IVA).  |
