---
title: Alterações de gestão de recursos (Project Service Automation 3.x)
description: Este tópico fornece informações sobre as alterações na área de gestão de Recursos.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 5f88d7309a5e1171629a72e749bfc01abb64c62a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5284777"
---
# <a name="resource-management-changes-project-service-automation-3x"></a>Alterações de gestão de recursos (Project Service Automation 3.x)

[!include [banner](../../includes/psa-now-project-operations.md)]

As secções deste tópico fornecem informações sobre as alterações efetuadas na área de gestão de Recursos do Dynamics 365 Project Service Automation, versão 3.x.

## <a name="project-estimates"></a>Estimativas do projeto

Em vez de se basear na entidade **msdyn\_projecttask** (**Tarefa do Projeto**), as estimativas do projeto são baseadas na entidade **msdyn\_resourceassignment** (**Atribuição de Recurso**). As atribuições de recursos tornaram-se a "fonte da verdade" para o agendamento e a definição de preços das tarefas.

## <a name="line-tasks"></a>Tarefas de linha

No PSA 3.x, as tarefas de linha são obsoletas (preteridas). Agora, as atribuições apontam para a tarefa inteira, em vez das tarefas de linha.

O exemplo a seguir mostra como uma tarefa denominada "Tarefa de teste" é atribuída aos membros da equipa A e B nas versões anteriores do PSA e no PSA 3.x.

- **Antes do PSA 3.x:**

    - Tarefa de teste

        - Tarefa de teste - Tarefa de linha 1

            - Atribuição a A

        - Tarefa de teste - Tarefa de linha 2

            - Atribuição a B

- **PSA 3.x:**

    - Tarefa de teste

        - Atribuição a A
        - Atribuição a B

## <a name="unassigned-assignment"></a>Atribuição não atribuída

No PSA 3.x, uma atribuição não atribuída é uma atribuição que é atribuída a um membro da equipa **NULL** e a um recurso **NULL**. As atribuições não atribuídas podem ocorrer em alguns cenários:

- Se uma tarefa tiver sido criada, mas ainda não tiver sido atribuída a nenhum membro da equipa, é sempre criada uma atribuição não atribuída. 
- Se todos os detentores de atribuição de uma tarefa forem removidos, uma atribuição não atribuída é recriada para essa tarefa.

## <a name="scheduling-fields-on-the-project-task-entity"></a>Campos de agendamento na entidade Tarefa do Projeto

Os campos na entidade **msdyn\_projecttask** foram preteridos ou movidos para a entidade **msdyn\_resourceassignment** ou são referenciados a partir da entidade **msdyn\_projectteam** (**Membro da Equipa do Projeto**).

| Campo preterido em msdyn\_projecttask (Tarefa do Projeto) | Novo campo em msdyn\_resourceassignment (Atribuição de Recurso) | Comentário |
|---|---|---|
| msdyn\_assignedresources | Nenhum | |
| msdyn\_assignedteammembers | Nenhum | |
| msdyn\_numberofresources | Nenhum | |
| msdyn\_scheduledhours | Nenhum | |
| msdyn\_effortcontour | msdyn\_plannedwork | O formato da estrutura de dados do JSON (JavaScript Object Notation) armazenado no campo foi alterado. |

## <a name="schedule-contour"></a>Contorno da agenda

O contorno da agenda é armazenado no campo **Trabalho Planeado** (**msdyn\_plannedwork**) de cada entidade **Atribuição de Recurso** (**msdyn\_resourceassignment**).

### <a name="structure"></a>Estrutura

A nova estrutura do contorno da agenda é constituída por intervalos de tempo flexíveis que são definidos para cada dia da agenda. Cada intervalo de tempo tem as seguintes propriedades:

- **Início** – O início das horas de trabalho para o dia, de acordo com o calendário do projeto.
- **Fim** – O fim das horas de trabalho para o dia, de acordo com o calendário do projeto.
- **Horas** – O número de horas que estão atribuídas no dia.

**Exemplo**

Este exemplo utiliza um calendário de projeto em que o dia de trabalho é das 9:00 às 17:00 no fuso horário UTC-8.

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a>Agendamento automático e agendamento manual

Se uma tarefa for agendada automaticamente, as horas serão antecipadas e a duração da tarefa poderá ser reduzida.

**Exemplo**

A tarefa a seguir é agendada automaticamente por 18 horas em três dias (3 de dezembro de 2018 a 5 de dezembro de 2018).

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

Se uma tarefa for agendada manualmente, as horas serão distribuídas uniformemente em todas as datas.

**Exemplo**

A tarefa a seguir é agendada manualmente por 18 horas em três dias (3 de dezembro de 2018 a 5 de dezembro de 2018).

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a>Unidade de atribuição

A unidade de atribuição foi preterida no PSA 3.x. Agora, as horas de esforço da tarefa estão igualmente divididas, por dia, entre todos os recursos atribuídos.

**Exemplo**

Neste exemplo, a tarefa é atribuída a dois recursos e é agendada automaticamente por 36 horas em três dias (3 de dezembro de 2018 a 5 de dezembro de 2018).

- Atribuição 1:

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- Atribuição 2:

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a>Dimensões de definição de preços

No PSA 3.x, os campos de dimensão de definição de preços específicos de recursos (como **Função** e **Unidade Organizacional**) foram removidos da entidade **msdyn\_projecttask**. Agora, estes campos podem ser obtidos a partir do membro da equipa do projeto correspondente (**msdyn\_projectteam**) da atribuição de recurso (**msdyn\_resourceassignment**) quando são geradas estimativas de projeto. Foi adicionado um novo campo, **msdyn\_organizationalunit**, à entidade **msdyn\_projectteam**.

| Campo preterido em msdyn\_projecttask (Tarefa do Projeto) | Campo do msdyn\_projectteam (Membro da Equipa do Projeto) que é utilizado em vez disso |
|---|---|
| msdyn\_resourcecategory | msdyn\_resourcecategory |
| msdyn\_organizationalunit | msdyn\_organizationalunit |

## <a name="contours"></a>Contornos

Os campos de contornos de preços e estimativas foram preteridos na entidade **msdyn\_projecttask**. Foram movidos para a entidade **msdyn\_resourceassignment**.

| Campo preterido em msdyn\_projecttask (Tarefa do Projeto) | Novo campo em msdyn\_resourceassignment (Atribuição de Recurso) |
|---|---|
| msdyn\_costestimatecontour | msdyn\_plannedcostcontour |
| msdyn\_salesestimatecontour | msdyn\_plannedsalescontour |

Os campos que se seguem foram adicionados à entidade **msdyn\_resourceassignment**:

* msdyn\_plannedcost
* msdyn\_plannedsales

Os campos que se seguem para custos e vendas planeados, reais e restantes não são alterados na entidade **msdyn\_projecttask**:

* msdyn\_plannedcost
* msdyn\_plannedsales
* msdyn\_actualcost
* msdyn\_actualsales
* msdyn\_remainingcost
* msdyn\_remainingsales


[!INCLUDE[footer-include](../../includes/footer-banner.md)]