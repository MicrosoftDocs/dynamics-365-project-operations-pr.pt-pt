---
title: Agendamento externo
description: Este artigo fornece informações sobre o agendamento externo.
author: ruhercul
ms.date: 10/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 746fb3a7c812b2b387ec707e58796d02d2473847
ms.sourcegitcommit: b1a5b9bb8b826678fc52f1d5a3d199a71caccb0a
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 11/03/2022
ms.locfileid: "9736971"
---
# <a name="external-scheduling"></a>Agendamento externo

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

O modo de agendamento externo permite-lhe criar, atualizar e eliminar entidades de forma nativa relacionadas com estruturas hierárquicas de trabalho (WBSs), mas sem os limites atuais impostos pelo Microsoft Project for the Web. Também fornece validação limitada. Este modo só deve ser utilizado pelos seguintes clientes:

- Clientes que tenham as ferramentas necessárias para definir uma WBS fora da lógica de agendamento fornecida pelo Project Operations
- Clientes que têm de gerir a hierarquia de agendamento, as dependências ou a duração da tarefa

> [!IMPORTANT]
> Os dados que não estão corretamente introduzidos na entidades relacionadas com WBS poderão não ser processados na grelha de reconciliação de recursos, grelha de estimativas, grelha de monitorização ou grelha de atribuição de recursos.

## <a name="configuration"></a>Configuration

Esta caraterística está ativada por predefinição. No entanto, na página principal de origem para projetos, o campo relacionado não está visível por predefinição. Para ativar o campo, no Maker Portal, abra a página principal para entidade do projeto, selecione o campo **Motor de Agendamento** e, em seguida, altere o campo para **Visível por Predefinição**. Se não utilizar a página principal do projeto de origem, edite a página existente e adicione-lhe o campo **Motor de Agendamento**.

## <a name="settings"></a>Definições

Para utilizar o modo de agendamento externo, tem primeiro de criar um novo projeto e selecionar o motor de agendamento **Agendado Externamente** na lista pendente na página principal do projeto. Não é possível alterar este modo depois de ter sido configurado para um projeto.

## <a name="viewing-the-wbs"></a>Ver a WBS

Se um projeto for agendado externamente, o acesso ao Project for the Web é restringido para esse projeto. Para ver a WBS, tem de aceder à grelha de monitorização, onde é apresentada a WBS completa.

## <a name="creating-and-editing-the-wbs"></a>Criar e editar a WBS

Se o agendamento externo estiver ativado para um projeto, tem de definir os dados para todas as entidades relacionadas com a WBS, incluindo tarefas, membros da equipa, atribuições de recursos e dependências.

A seguinte ilustração mostra o modelo de dados para planeamento de projetos.

![Modelo de dados de planeamento de projetos.](media/projectplanningdatamodel.png)

## <a name="functional-limitations"></a>Limitações funcionais

As seguintes operações não são permitidas em projetos agendados externamente.

### <a name="project-planning"></a>Planeamento de projeto

- **Copiar projeto** – Esta operação não é suportada em projetos agendados externamente.
- **Mover projeto** – As alterações à data de início de um projeto não irão mover o início de tarefas ou atribuições de recursos na WBS.
- **Atualizar o Gestor de Projetos** – As alterações ao gestor de projetos na página principal do projeto não criam automaticamente um novo membro da equipa do projeto até que o projeto tenha sido convertido.
- **Atualizar o modelo de horário de trabalho do projeto** – As alterações ao modelo de horário de trabalho do projeto não irão recalcular a agenda do projeto.
- **Contornos da Atribuição de Recursos** – A criação de atribuições de recursos não atualizará automaticamente o campo **mdyn\_PlannedWork**. Este campo é utilizado para armazenar contornos para o esforço de atribuição de recursos. Se mostrar esforço faseado por tempo na grelha de atribuição de recursos ou na grelha de reconciliação de recursos, tem de definir contornos de atribuição de recursos válidos. Estes contornos têm de ser formatados corretamente para acionarem o cálculo de ambos os contornos de custo e os contornos de preços de vendas. Recomendamos que crie um projeto de teste que seja agendado pelo Project for the Web e, em seguida, reveja os dados associados para confirmar os requisitos e a formatação.

### <a name="resource-management"></a>Gestão de recursos

- **Cumprimento de recursos genéricos** – O cumprimento de recursos genéricos não é suportado para projetos agendados externamente. As tentativas de cumprir requisitos abertos ativos criará novos membros da equipa do projeto, mas não eliminará o membro da equipa genérico nem substituirá o membro da equipa genérico em quaisquer atribuições de recurso existentes.
- **Eliminar Membro da Equipa** – A eliminação de um membro da equipa não elimina automaticamente atribuições de recursos.

### <a name="quoting-and-contracting"></a>Propostas e contratação

- **Importar detalhes da Linha de Proposta e de Item de Contrato** – Quando os detalhes da proposta ou do item de contrato são importados de um projeto, a aplicação foi testada para suportar um máximo de apenas 500 tarefas na WBA, com base num limite de 20 atribuições por tarefa.

### <a name="actuals-and-invoicing"></a>Valores reais e faturação

- Apesar de não existirem alterações a validações existentes entre a WBS e as transações financeiras, é importante que esteja em conformidade com o modelo de dados de origem, para assegurar que todas as transações a jusante são executadas conforme esperado.
