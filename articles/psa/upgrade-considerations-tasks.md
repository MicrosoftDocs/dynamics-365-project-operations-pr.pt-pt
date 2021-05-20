---
title: Considerações sobre atualização para a estrutura hierárquica do trabalho
description: Este tópico fornece informações sobre a atualização da estrutura hierárquica do trabalho do Project Service Automation 2.x para 3.x.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
author: ruhercul
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
ms.openlocfilehash: d31ca60b267063e9cadf544468ece501353950fa
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/27/2021
ms.locfileid: "5951358"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a>Considerações sobre atualização para a estrutura hierárquica do trabalho

[!include [banner](../includes/psa-now-project-operations.md)]

Este tópico fornece informações sobre a atualização da estrutura hierárquica do trabalho do Project Service Automation 2.x para 3.x. Este tópico define o estado de funcionamento de um projeto no Project Service Automation (PSA) necessário para uma atualização bem-sucedida. Há também informações sobre as condições de bloqueio comuns que causarão falhas na atualização. Para obter mais informações sobre como definir tarefas do projeto e as suas funções numa agenda do projeto, consulte [Agendas do projeto](project-creating.md).

## <a name="key-entities"></a>Entidades principais
Para uma estrutura hierárquica do trabalho precisa que já esteja carregada com recursos, são necessárias as seguintes entidades:

- [Projeto](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)
- [Equipa do Projeto](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)
- [Tarefa de Projeto](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)
- [Atribuições de Recursos](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)
- [Dependência de Tarefa de Projeto](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)
- [Recursos Reserváveis](/dynamics365/customerengagement/on-premises/developer/entities/bookableresource)

Para definir uma estrutura hierárquica do trabalho carregada por recurso, deve concluir os seguintes passos:

1. Crie um projeto. Para obter mais informações sobre como criar um projeto, consulte [msdyn_project](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).
2. Crie uma ou mais tarefas. Para obter mais informações sobre como criar uma tarefa, consulte [msdyn_projecttask](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).
3. Defina as dependências da tarefa. Para mais informações, consulte [Dependência de Tarefas do Projeto](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).
4. Atribua membros da equipa do projeto ao projeto. Para obter mais informações, consulte [msdyn_projectteam](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).
5. Atribua membros da equipa do projeto às tarefas. Para obter mais informações, consulte [msdyn_resourceassignment](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).

## <a name="project-team-relationships"></a>Relações da equipa do projeto

Para garantir uma atualização bem-sucedida, as seguintes relações devem ser mantidas corretamente:
- Todos os membros da equipa do projeto devem estar associados a um recurso reservável.
- Todos os membros da equipa do projeto devem estar associados ao mesmo projeto. 

## <a name="project-task-relationships"></a>Relações de tarefas do projeto
Para garantir uma atualização bem-sucedida, as seguintes relações devem ser mantidas corretamente:

- Todas as tarefas relacionadas devem ser associadas ao mesmo projeto.
- Todas as tarefas de linha devem ter uma tarefa principal.
- Todas as tarefas devem ter um projeto principal.

### <a name="valid-conditions"></a>Condições válidas

- Todas as durações de tarefa devem ser maiores ou iguais a (>=) uma hora e inferiores a 1.800.000 minutos (1250 dias).*
- Todas as tarefas devem ter uma data de início não anterior a 2000/01/01.*
- Todas as tarefas devem ter uma data de início, de no máximo 17 anos a partir do dia atual.*
- Todas as tarefas devem ter uma data de início anterior ou igual à data de conclusão.
- Todos os tipos de transação nas classificações (Despesa, Material, Imposto e Tempo) devem ter valores para **Unidade Predefinida** e **Grupo de Unidades**.
- Os formatos de data com letras devem ser evitados.

### <a name="potential-mitigation-steps"></a>Passos potenciais de mitigação
- Utilize a Localização Avançada para identificar tarefas de Projeto que não contenham um ID de Projeto.
- Utilize a Localização Avançada para identificar tarefas de Projeto em que a duração agendada seja superior a > 1.800.000.
- Antes de efetuar alterações a dados, deve investigar eventuais personalizações associadas à entidade que poderão ter levado à obtenção dos dados num estado incorreto. Estas personalizações devem ser resolvidas antes de prosseguir com quaisquer atualizações relacionadas com os dados.
- Para as tarefas identificadas que ficaram órfãs, considere a possibilidade de eliminar estas tarefas se não forem necessárias ou se elas tiverem de ser associadas ao projeto principal correto.
- Para qualquer tarefa na qual a duração seja superior a 1.250 dias, considere adicionar várias tarefas para representar a duração total, se possível.

> [!NOTE]
> Os itens anotados com um asterisco (\*) têm limites porque a gestão das relações com os clientes (CRM) oferece suporte a apenas 7320 expansões de recorrência. Deve permanecer abaixo deste limite.

## <a name="resource-assignment-relationships"></a>Relações de Atribuição de Recursos
Para garantir uma atualização bem-sucedida, as seguintes relações devem ser mantidas corretamente:

- Todas as Atribuições de Recursos numa estrutura hierárquica do trabalho devem estar relacionadas com o mesmo projeto.
- Todas as Atribuições de Recursos numa estrutura hierárquica do trabalho devem ser associadas aos membros da equipa do projeto no mesmo projeto.

### <a name="potential-mitigation-steps"></a>Passos potenciais de mitigação
- Identifique todas as tarefas que estejam fora das condições descritas acima.  
- Todas as Atribuições de Recursos que já não sejam válidas devem ser eliminadas.

## <a name="project-task-dependency-relationships"></a>Relações de dependência de tarefas do projeto
Para garantir uma atualização bem-sucedida, as seguintes relações devem ser mantidas corretamente:

- Todas as dependências de tarefa do projeto devem estar relacionadas com o mesmo projeto.
- Uma tarefa não pode ter a mesma dependência referenciada mais de uma vez.


[!INCLUDE[footer-include](../includes/footer-banner.md)]