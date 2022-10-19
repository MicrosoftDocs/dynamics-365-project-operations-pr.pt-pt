---
title: Processo de conversão do agendamento de projetos do Project Service Automation para o Project Operations
description: Este artigo fornece uma descrição geral das alterações de caraterísticas para o Microsoft Dynamics 365 Project Service Automation para o Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/07/2022
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 84a40fcc9a8561c4ade0be175b08f701f3196508
ms.sourcegitcommit: 28004d38800782540fa5642d41f8fe0f6e2d9fa5
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/08/2022
ms.locfileid: "9642583"
---
# <a name="project-service-automation-to-project-operations-project-scheduling-conversion-process"></a>Processo de conversão do agendamento de projetos do Project Service Automation para o Project Operations

Depois de um projeto ter sido atualizada com êxito do Microsoft Dynamics 365 Project Service Automation 3.X para o Dynamics 365 Project Operations Lite, não é possível editar tarefas de projeto na estrutura hierárquica do trabalho (WBS) da grelha de tarefas. Os clientes poderão rever as WBSs na grelha de monitorização onde foram adicionados novos campos para fornecerem todos os detalhes relacionados com a tarefa. Para projetos onde são necessárias edições à WBS, pode converter seletivamente projetos elegíveis na nova experiência de agendamento do Project for the Web.

## <a name="project-conversion-process"></a>Processo de conversão de projetos

Para converter um projeto, siga estes passos.

1. Abra a página principal do projeto e selecione **Converter** no Painel de Ações.
1. Na caixa de mensagem de confirmação, selecione **OK** para iniciar a conversão do projeto. Ocorrem as seguintes ações:

    1. Uma barra de mensagens que aparece na página principal do projeto afirma: "A agenda do projeto está a ser convertida. Não pode efetuar alterações ao projeto até que a conversão seja concluída."
    1. É redirecionado para a lista de projetos.

    Após a conversão do projeto ser concluída, ocorrem as seguintes ações:

    1. O gestor de projeto atribuído recebe uma notificação no lado direito da aplicação.
    1. A barra de mensagens que afirma que a conversão está em curso é removida.
    1. O separador **Agenda** mostra a nova experiência de agendamento com o Project for the Web. Qualquer utilizador que tenha as licenças e os direitos de acesso apropriados pode editar a WBS.
    1. O campo **Motor de agendamento** é atualizado para **Project for the Web**.
    1. O botão **Converter** é removido do Painel de Ações.

> [!IMPORTANT]
> Não é permitida a conversão em massa de projetos. Qualquer tentativa de atualizar um grande volume de projetos ao mesmo tempo será limitada. Esta limitação ajuda a assegurar um elevado desempenho para todos os clientes.

## <a name="manual-tasks-vs-automatic-tasks"></a>Tarefas manuais vs. tarefas automáticas

Quando um ambiente é atualizado do Project Service Automation para o Project Operations, todas as tarefas na WBS são consideradas agendadas automaticamente. O conceito de tarefas agendadas manualmente não está disponível em Project for the Web. No entanto, pode definir o comportamento de agendamento preferido para os projetos utilizando a definição do [modo de agendamento](/project-management/scheduling-modes.md) quando criar novos projetos.

## <a name="restricted-operations-for-pre-conversion-projects"></a>Operações restritas para projetos de pré-conversão

Esta secção descreve as diferenças funcionais que pode esperar quando os projetos não foram convertidos.

### <a name="copy-project"></a>Copiar projeto

A operação **Copiar** só é suportada em projetos convertidos. Não é possível copiar projetos atualizados antes da conversão.

### <a name="move-project"></a>Mover projeto

Uma alteração à data de início de um projeto não irá mover proporcionalmente o início das tarefas, a menos que o projeto tenha sido convertido.

## <a name="frequently-asked-questions"></a>Perguntas mais frequentes

### <a name="what-are-the-differences-between-converted-projects-and-new-projects-that-are-created-after-the-upgrade-has-been-completed"></a>Quais são as diferenças entre projetos convertidos e novos projetos criados após a atualização ter sido concluída?

Para projetos convertidos após o ambiente ter sido atualizado, será definida um sinalizador que instrua a agenda a respeitar apenas o calendário do projeto. Este comportamento corresponde ao comportamento no Project Service Automation. No entanto, o sinalizador não será definido para novos projetos criados após a atualização. Por conseguinte, a agenda irá respeitar as horas de expediente dos recursos quando estes estiverem atribuídos a uma tarefa.

### <a name="what-should-i-do-if-my-project-fails-to-be-converted"></a>O que devo fazer se a conversão do meu projeto falhar?

Se o projeto não conseguir ser convertido, o primeiro passo é rever os registos de erro para identificar quaisquer problemas comuns relacionados com a sua WBS. Se os registos não indicarem um erro específico sobre o qual possa agir, contacte o Suporte ao Cliente para que o seu caso possa ser revisto melhor.

### <a name="how-are-business-closures-handled-in-project-for-the-web"></a>Como é que os encerramentos de negócio são resolvidos no Project for the Web?

O Project for the Web não respeita os encerramentos de negócio definidos pela empresa ao nível da organização. No entanto, irá respeitar outros tipos de dias de folga que estão definidos num determinado modelo de horas de expediente.

### <a name="what-are-the-limitations-of-project-for-the-web"></a>Quais são as limitações do Project for the Web?

Defina [Criar uma estrutura hierárquica do trabalho: Limitações do Projeto](/project-management/create-wbs#project-limitations.md).

### <a name="can-i-expect-changes-to-my-cost-and-sales-estimates"></a>Posso esperar alterações às minhas estimativas de custo e vendas?

Em casos raros em que os contornos de atribuição de recursos são recalculados ou em que se enquadram num limite de data diferente do projeto de origem, poderá ver diferenças nas estimativas de vendas e custos. Como parte do processo de atualização de versão, espera-se que os clientes testem um conjunto de amostra de projetos representativo, para que possam compreender quaisquer alterações de agendamento potenciais.
