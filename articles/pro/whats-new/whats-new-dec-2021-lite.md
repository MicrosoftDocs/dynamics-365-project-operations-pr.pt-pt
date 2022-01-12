---
title: Novidades de dezembro de 2021 – Implementação do Project Operations Lite
description: Este tópico fornece informações sobre as atualizações de qualidade que estão disponíveis na versão de dezembro de 2021 da implementação do Project Operations Lite.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0432e2d4970c352e91cca589987bbdace57c6eaf
ms.sourcegitcommit: 9d20e7738cce195d344f5925a115741a1ce3ca36
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 12/21/2021
ms.locfileid: "7942991"
---
# <a name="whats-new-december-2021---project-operations-lite-deployment"></a>Novidades de dezembro de 2021 – Implementação do Project Operations Lite

_Aplica-se a: Implementação lite – negócio para faturação pró-forma_

Este tópico aplica-se aos seguintes componentes e versões do Microsoft Dynamics 365 Project Operations:

- Project Operations num ambiente Dataverse, versão 4.27.0.195, 4.27.0.242


## <a name="features-included-in-this-release"></a>Funcionalidades incluídas nesta versão

### <a name="subcontract-management"></a>Gestão de subcontratos 

- [Subcontratar membros da equipa do projeto](../subcontracting/subcontracting-project-team-members.md): um gestor de projeto pode criar membros da equipa nomeados ou genéricos com subcontratos e itens de subcontrato para afetar a criação da equipa e a estimativa.
- [Opções de subcontratação para membros da equipa do projeto](../subcontracting/subcon-options.md): ao fazer escolhas de criação da equipa para membros da equipa do projeto nomeados ou genéricos, o gestor do projeto pode rever os subcontratos existentes ou criar novos subcontratos para um ou mais membros da equipa do projeto. 
- [Estimativa de custos das atribuições de recursos subcontratadas](../subcontracting/costing-subcon-ra.md): a estimativa de custos do projeto terá em conta as atribuições de recursos subcontratadas e terão o custo da utilização das tabelas de preços de compra associadas a subcontratos. 
- [Configurar Quadro da Agenda para mostrar trabalhadores contratados e capacidade subcontratada](../subcontracting/configure-sb-subcon.md): o Quadro da Agenda no Project Operations pode agora ser configurado para procurar e sugerir o tipo de trabalhador contratado de recursos reserváveis e capacidade subcontratada, juntamente com os colaboradores. Esta configuração pode ser aplicada quando pesquisa recursos no contexto de dotar de colaboradores para um requisito específico do projeto ou quando pesquisa fora do contexto de um requisito do projeto.
- [Dotar de colaboradores um projeto com trabalhadores contratados e capacidade subcontratada](../subcontracting/staffing-cw.md): os trabalhadores contratados podem agora ser reservados em projetos que tiram partido das experiências do quadro da agenda.
- [Tempo de gravação, despesas e utilização de material em projetos para componentes subcontratados](../subcontracting/recording-subcon-actuals.md): os trabalhadores contratados podem registar tempo e despesas, e os membros da equipa de projeto também podem registar a utilização de materiais adquiridos através de um subcontrato num projeto. Isto resultará na gravação de custos precisos em projetos que utilizem capacidade ou materiais comprados.
- [Transições de estado num subcontrato](../subcontracting/subcon-states.md): os subcontratos podem ser confirmados para concluir a negociação com o fornecedor, fechados para indicar a conclusão da entrega, ou cancelados para indicar a rescisão do contrato com o fornecedor antes da conclusão da entrega.

### <a name="task-planning"></a>Planeamento de Tarefas
- Resolução de problemas melhorada para administradores de sistema. Quando um utilizador não pode abrir um projeto, o administrador pode rever erros não relacionados com licenças gerados a partir do Project for the Web em [Registos de agendamento do projeto](../../project-management/schedule-api-logs.md).
- [Utilizar listas de verificação de tarefas no Microsoft Project for the Web](https://support.microsoft.com/en-us/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c). No Microsoft Project for the web, pode adicionar uma lista de verificação a uma tarefa para monitorizar itens específicos.

## <a name="quality-updates"></a>Atualizações de qualidade

| **Área de funcionalidades** | **Número de referência** | **Atualização de qualidade** |
| --- | --- | --- |
| Planeamento e deteção de movimentos | 2392596 | As APIs da Agenda agora permitem atualizações aos campos **Esforço restante**, **Esforço concluído** e **% Completo**. |
| Planeamento e deteção de movimentos | 2478497 | Os campos **Número de Atividade** e **ID da Tarefa** de APIs da Agenda podem estar em branco na entrada porque o sistema irá preenchê-los usando numeração automatizada.|
| Tempo e Despesa | 2468135 | O número de tentativas de aprovação é reduzido de cinco para três. |
| Tempo e Despesa | 2468188 | Corrigido o problema com texto de registo que excedia ao comprimento máximo no atributo **notetext** da entidade **anotação**. |
