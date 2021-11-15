---
title: Criar uma estrutura hierárquica do trabalho
description: Esta tópico explica como criar uma estrutura hierárquica do trabalho (WBS) incluindo os controlos básicos na nova interface de agendamento.
author: ruhercul
ms.date: 06/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: f77450d0d754606dd336072248012fea462510a4
ms.sourcegitcommit: a12d21c7cab296f5b6a3181d76a06f57dee1267c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/19/2021
ms.locfileid: "7655431"
---
# <a name="create-a-work-breakdown-structure-wbs"></a>Criar uma estrutura hierárquica do trabalho (WBS)

Uma agenda do projeto comunica qual trabalho deve ser concluído, quais recursos farão o trabalho e o tempo durante o qual o trabalho deve ser terminado. A agenda reflete todo o trabalho associado à entrega do projeto a tempo. Em Dynamics 365 Project Operations, você cria um programa de projeto por:

  - Dividir o trabalho em tarefas geríveis.
  - Estimar o tempo necessário para fazer cada tarefa.
  - Definir dependências de tarefa.
  - Definir durações de tarefa.
  - Estimar os recursos genéricos que farão as tarefas. 

A agenda do projeto é criada no separador **Agenda** da página do **Projeto**.

## <a name="tasks"></a>Tarefas

O primeiro passo para criar uma agenda do projeto é dividir o trabalho em partes geríveis. A agenda no Project Operations suporta as seguintes funcionalidades:

- Tarefas de resumo ou contentor
- Tarefas de nós de folha

### <a name="summary-tasks"></a>Resumo de tarefas

As tarefas resumidas podem armazenar outras tarefas de resumo ou de nó de folha. Não têm esforço de trabalho nem custo próprio. Em vez disso, o esforço e o custo do trabalho são um rollup do esforço e do custo do trabalho das tarefas do contentor. A data de início da tarefa de resumo é a data de início das tarefas de contentor e a data de fim é a data de fim das tarefas de contentor. O nome de uma tarefa de resumo pode ser editado, mas as propriedades de agendamento, incluindo esforço, datas e duração não podem ser editadas. Se eliminar uma tarefa de resumo, também eliminará todas as suas tarefas de contentor.

### <a name="leaf-node-tasks"></a>Tarefas de nós de folha

As tarefas de nós de folha representam o trabalho mais granular no projeto. Têm um esforço estimado, recursos, datas de início e de fim planeadas e uma duração.

## <a name="create-a-task-hierarchy"></a>Criar uma hierarquia de tarefas

### <a name="add-a-task"></a>Adicionar uma tarefa

Concluir os seguintes passos para adicionar uma ou mais tarefas.

1. Ir a **Projetos** e selecionar e abrir o registo do projeto para o qual pretende criar uma agenda. 
2. Selecionar o separador **Tarefas**. 
3. Selecionar **Adicionar nova tarefa**, inserir um nome para a tarefa e, em seguida, premir Enter.
2. Introduza outro nome de tarefa e prima Enter novamente até ter uma lista completa de tarefas.

### <a name="manage-hierarchy-of-a-task"></a>Gerir a hierarquia de uma tarefa

Quando uma tarefa é avançada, esta passa a ser um elemento subordinado da tarefa que está diretamente acima da mesma. O ID da agenda da tarefa é, em seguida, recalculado para que se baseie no ID da agenda do novo elemento principal e segue o esquema de numeração de tópicos. A tarefa do elemento principal é agora uma tarefa sumária. Consequentemente, passa a ser um rollup de suas tarefas subordinadas. Quando uma tarefa é promovida, deixa de ser um elemento subordinado da tarefa que era o seu elemento principal. O ID da agenda é então recalculado para refletir a profundidade e a posição atualizadas da tarefa na hierarquia. O esforço, o custo e as datas da tarefa principal anterior são recalculados para que não incluam esta tarefa.

Conclua os seguintes passos para avançar ou promover uma tarefa.

1. Na página **Projeto**, no separador **Tarefas** em **Tarefas de resumo**, selecione os três pontos verticais pelo nome da tarefa e, em seguida, selecione **Criar subtarefa**. 
2. Selecione a tarefa para avançar ou promover. Para selecionar mais do que uma tarefa, selecione uma tarefa, prima e mantenha premido Ctrl e, em seguida, selecione tarefas adicionais.
2. Selecione **Avançar** ou **promover subtarefa** para mover tarefas para baixo ou para fora das tarefas de resumo.

### <a name="move-tasks-up-and-down"></a>Mover tarefas para cima e para baixo

As tarefas podem ser mudadas para qualquer nível na estrutura hierárquica de trabalho de uma de duas maneiras:

- Selecione mais uma tarefa e arraste-as para o local pretendido.
- Selecione uma ou mais tarefas, clique à direita e selecione **Cortar**, selecione a célula de destino na agenda e, em seguida, clique à direita e selecione **Colar**.

## <a name="task-attributes"></a>Atributos da tarefa

O nome de uma tarefa descreve o trabalho que tem de ser concluído. No Project Operations, os atributos associados a uma tarefa descrevem o agendamento da tarefa e as necessidades de definição de pessoal da mesma.

## <a name="schedule-attributes"></a>Agendar atributos

Os atributos **Esforço**, **Data de início**, **Data de fim** e **Duração** definem a agenda para a tarefa.

A tabela a seguir mostra atributos de agenda adicionais.

| **Nome a apresentar final** | **Descrição final** |
| --- | --- |
| Esforço Concluído (Horas) | Trabalho concluído para a tarefa em horas. |
| Duração | Apresenta a duração em dias para a tarefa. |
| Esforço Total | Trabalho total para a tarefa em horas. |
| Conclusão | Data e Hora de conclusão. |
| % Concluída | A percentagem da tarefa que está concluída. |
| Registo do Projeto | O quadro de tarefas pode ser agrupado por registo, para que cada registo tenha uma coluna própria. |
| Esforço Restante (Horas) | O trabalho restante para a tarefa em horas. |
| Iniciar | Data e hora de início. |
| Nome | O nome da tarefa. |
| ID | O ID da tarefa na estrutura hierárquica do trabalho. |

Como Administrador, pode definir campos personalizados na entidade de tarefa. No entanto, os campos não podem ser exibidos na grelha de programação. Para ver os seus campos personalizados, adicione-os à página de detalhes de **Tarefa do projeto**.

## <a name="staffing-attributes"></a>Atributos do pessoal

Os atributos de definição de pessoal são acedidos através do campo **Recursos** na agenda. Pode procurar um recurso existente ou selecionar **Criar** e, no painel **Criação Rápida**, adicionar um membro da equipa do projeto como um novo recurso.

Os campos **Função**, **Unidade de Atribuição de Recursos** e **Nome da Posição** são utilizados para descrever as necessidades de definição de pessoal para a tarefa. Estes atributos de definição de pessoal, juntamente com o agendamento da tarefa são utilizados para localizar os recursos disponíveis para efetuar esta tarefa.

   - **Função**: Especifique o tipo de recurso que é necessário para efetuar a tarefa.
   - **Unidade de atribuição de recursos**: Especifique a unidade a partir da qual os recursos para a tarefa devem ser atribuídos. Este atributo afeta o custo e a estimativa de vendas para a tarefa se o custo e a taxa de faturação do recurso forem definidos com base nas unidades de atribuição de recursos.
   - **Nome da posição**: Introduza um nome para o recurso genérico que serve como marcador de posição para o recurso que, por fim, fará o trabalho.

O campo **Recursos** contém o nome da posição do recurso genérico ou um recurso nomeado quando é encontrado um.

O campo **Categoria** contém os valores que indicam um tipo mais amplo de trabalho no qual a tarefa pode ser agrupada. Este campo não afeta o agendamento nem a definição de pessoal. Em vez disso, o campo é usado apenas para reportar.

## <a name="task-dependencies"></a>Dependências de tarefa

Pode utilizar a agenda no Project Operations para criar relações antecessoras entre tarefas. O campo **Antecessor** utiliza um ou mais valores para indicar as tarefas de que uma tarefa depende. Quando os valores antecessores são atribuídos a uma tarefa, a tarefa pode ser iniciada apenas depois de todas as tarefas antecessoras terem sido concluídas. Devido à dependência, a data de início planeada da tarefa é reposta para a data em que as tarefas antecessoras são concluídas.

O modo de tarefa não tem efeito nas atualizações efetuadas nas datas de início e de fim das tarefas antecessoras/dependentes.

## <a name="accessibility-and-keyboard-shortcuts"></a>Atalhos de teclado e acessibilidade

A grelha **Agenda** é totalmente acessível e pode ser utilizada com leitores de ecrã, tais como o Narrator, o JAWS ou o NVDA. Pode percorrer a área de grelha através da utilização das teclas de seta (como no Microsoft Excel), pode utilizar a tecla de tabulação para avançar através dos elementos da interface de utilizador interativa e pode utilizar a tecla de seta para baixo, a tecla Enter ou a Barra de Espaço para selecionar e abrir os menus pendentes.

## <a name="project-limitations"></a>Limitações do projeto 
Se estiver a utilizar a estrutura hierárquica do trabalho no Project Operations, deve estar ciente das seguintes limitações. Estes limites são aplicáveis aos projetos e às tarefas. Para mais informações, consulte [Limites e limiares do Project for the web](/project-for-the-web/project-for-the-web-limits-and-boundaries).

| **Campo**                                          |  **Limite**           |
|----------------------------------------------------|----------------------|
| Total de tarefas máximo para um projeto                  | 500                  |
| Duração total máxima para um projeto               | 3650 dias (10 anos) |
| Total de recursos máximo para um projeto              | 235                  |
| Total de ligações máximo (apenas a sucessora) para um projeto | 600                  |
| Total de campos personalizados máximo para um projeto          | 10                   |

**Limitações de tarefas**

| **Campo**                               |   **Limite**           |
|-----------------------------------------|-----------------------|
| Nível máximo da hierarquia                 | 10 níveis             |
| Máximo de ligações (sucessora + antecessora) | 20                    |
| Duração máxima da tarefa da folha           | 1250 dias             |
| Duração máxima de uma tarefa de resumo      | 3650 dias (10 anos)  |
| Máximo de recursos atribuídos a uma tarefa    | 20 recursos          |
| Intervalo de datas suportado para uma tarefa         | 1/1/2000 - 31/12/2149 |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
