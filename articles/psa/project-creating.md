---
title: Agendas do projeto
description: Este tópico fornece informações sobre como criar uma agenda.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 3/01/2019
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
ms.openlocfilehash: 2877f12a9ea3d288c4cf41f406cd8ca3e6cee821
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148432"
---
# <a name="project-schedules"></a>Agendas do projeto 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Uma agenda do projeto comunica qual trabalho deve ser concluído, quais recursos farão o trabalho e o tempo durante o qual o trabalho deve ser concluído. Reflete todo o trabalho associado à entrega do projeto a tempo. No Dynamics 365 Project Service Automation, pode criar uma agenda do projeto dividindo o trabalho em tarefas geríveis, estimando o tempo necessário para realizar cada tarefa, definindo dependências entre tarefas, definindo a duração das tarefas e estimando os recursos genéricos que irão efetuar as tarefas. A agenda do projeto é criada no separador **Agenda** da página do projeto.
 
## <a name="tasks"></a>Tarefas

O primeiro passo para criar uma agenda do projeto é dividir o trabalho em partes geríveis. A agenda no PSA suporta as seguintes funcionalidades:

- Nó de raiz do projeto
- Tarefas de resumo ou contentor
- Tarefas de nós de folha

### <a name="project-root-node"></a>Nó de raiz do projeto

O nó raiz do projeto é a tarefa de resumo de nível superior do projeto. Todas as outras tarefas do projeto são aí criadas. O nome do nó raiz é sempre definido como o nome do projeto. O esforço, as datas e a duração do nó raiz são resumidos com base nos valores da hierarquia abaixo dele. Pode editar as propriedades do nó raiz. Também não é possível eliminar o nó raiz.

### <a name="summary-or-container-tasks"></a>Tarefas de resumo ou contentor 

As tarefas de resumo têm subtarefas ou tarefas de contentor. Não têm esforço de trabalho nem custo próprio. Em vez disso, o esforço e o custo do trabalho são um rollup do esforço e do custo do trabalho das tarefas do contentor. A data de início da tarefa de resumo é a data de início das tarefas de contentor e a data de fim é a data de fim das tarefas de contentor. O nome de uma tarefa de resumo pode ser editado, mas as propriedades de agendamento (esforço, datas e duração) não podem ser editadas. Se eliminar uma tarefa de resumo, também eliminará todas as suas tarefas de contentor.

### <a name="leaf-node-tasks"></a>Tarefas de nós de folha

As tarefas de nós de folha representam o trabalho mais granular no projeto. Têm um esforço estimado, recursos, datas de início e de fim planeadas e uma duração.
 
## <a name="creating-a-task-hierarchy"></a>Criar uma hierarquia de tarefas

Pode criar uma hierarquia de tarefas utilizando as seguintes opções:

- Botão **Adicionar tarefa**
- Botão **Avançar tarefa**
- Botão **Diminuir avanço da tarefa**
- Botões **Mover para cima** e **Mover para baixo**
- Atalhos de teclado e acessibilidade

### <a name="add-task"></a>Adicionar tarefa

O botão **Adicionar tarefa** permite-lhe criar uma nova tarefa na hierarquia. Se não selecionar uma posição, a tarefa é inserida no final. 

Um ID da agenda é atribuído a cada tarefa. O ID da agenda representa a profundidade e a posição da tarefa na hierarquia. Utiliza a numeração de tópicos. Para tarefas no primeiro nível no nó raiz do projeto, é utilizado um esquema de numeração de 1, 2, 3 e assim por diante. Para tarefas no primeiro nível, é utilizado um esquema de numeração 1.1, 1.2, 1.3 e assim por diante.

### <a name="indent-task"></a>Avançar tarefa

Quando uma tarefa é avançada, esta passa a ser um elemento subordinado da tarefa que está diretamente acima da mesma. O ID da agenda da tarefa é, em seguida, recalculado para que se baseie no ID da agenda do novo elemento principal e segue o esquema de numeração de tópicos. A tarefa principal é agora uma tarefa de resumo ou uma tarefa de contentor. Consequentemente, passa a ser um rollup de suas tarefas subordinadas.

### <a name="outdent-task"></a>Diminuir avanço da tarefa 

Quando o avanço de uma tarefa é diminuído, deixa de ser um elemento subordinado da tarefa que era o seu elemento principal. O ID da agenda é então recalculado para refletir a profundidade e a posição atualizadas da tarefa na hierarquia. O esforço, o custo e as datas da tarefa principal anterior são recalculados para que não incluam esta tarefa.

### <a name="move-up-and-move-down"></a>Mover para cima e Mover para baixo 

Os botões **Mover para cima** e **Mover para baixo** alteram a posição de uma tarefa na respetiva hierarquia principal. As alterações deste tipo não afetam o esforço, o custo, as datas ou a duração da tarefa. Apenas o ID da agenda da tarefa é afetado. O ID da agenda é recalculado para refletir a nova posição da tarefa na lista do elemento principal das tarefas subordinadas.

### <a name="accessibility-and-keyboard-shortcuts"></a>Atalhos de teclado e acessibilidade

A grelha **Agenda** é totalmente acessível e pode ser utilizada com leitores de ecrã, tais como o Narrator, o JAWS ou o NVDA. Pode percorrer a área de grelha através da utilização das teclas de seta (como no Microsoft Excel), pode utilizar a tecla de tabulação para avançar através dos elementos da IU interativa e pode utilizar a tecla de seta para baixo, a tecla Enter ou a Barra de Espaço para selecionar e invocar os menus pendentes. Os cabeçalhos de coluna também são interativos. Pode ocultar e mostrar colunas, utilizar a tecla de tabulação e as teclas de seta para percorrer os cabeçalhos de coluna e utilizar os botões de ação na barra de ferramentas. Além disso, pode utilizar os seguintes atalhos de teclado:

- **Atualizar**: ALT+SHIFT+F5
- **Adicionar**: ALT+SHIFT+Insert
- **Eliminar**: ALT+SHIFT+Delete
- **Mover para cima/baixo**: ALT+SHIFT+setas para cima/para baixo
- **Avançar/diminuir avanço**: ALT_SHIFT+setas para a esquerda/direita
- **Expandir/fechar hierarquias**: ALT+SHIFT+teclas mais/menos

## <a name="task-attributes"></a>Atributos da tarefa

O nome de uma tarefa descreve o trabalho que tem de ser concluído. No PSA, os atributos que estão associados a uma tarefa descrevem o agendamento da tarefa e as necessidades de definição de pessoal da mesma.

> ![Atributos da tarefa](media/project-2.png)
 
### <a name="schedule-attributes"></a>Agendar atributos

Os atributos **Esforço**, **Data de início**, **Data de fim** e **Duração** definem a agenda para a tarefa.

Os atributos da agenda adicionais incluem:

- **Horas de esforço**: introduza uma estimativa das horas necessárias para concluir a tarefa. 
- **Duração**: especifique o número de dias de trabalho que são necessários para concluir a tarefa.
- **ID da agenda**: o ID gerado automaticamente é utilizado para ordenar tarefas na hierarquia. As dependências entre as tarefas gerem a ordem real na qual as tarefas são trabalhadas.
 
### <a name="staffing-attributes"></a>Atributos do pessoal

Os atributos de definição de pessoal são acedidos através do campo **Recursos** na agenda. Pode procurar um recurso existente ou clicar em **Criar** e, no painel **Criação Rápida**, adicionar um membro da equipa do projeto como um novo recurso.

Os campos **Função**, **Unidade de Atribuição de Recursos** e **Nome da Posição** são utilizados para descrever as necessidades de definição de pessoal para a tarefa. Estes atributos de definição de pessoal juntamente com o agendamento da tarefa são utilizados para localizar os recursos disponíveis para efetuar esta tarefa.

**Função** - Especifique o tipo de recurso que é necessário para efetuar a tarefa.

**Unidade de atribuição de recursos** - Especifique a unidade a partir da qual os recursos para a tarefa devem ser atribuídos. Este atributo afeta o custo e a estimativa de vendas para a tarefa se o custo e a taxa de faturação do recurso forem definidos com base nas unidades de atribuição de recursos.

**Nome da posição** – Introduza um nome amigável para o recurso genérico que serve como marcador de posição para o recurso que, por fim, fará o trabalho.

O campo **Recursos** contém o nome da posição do recurso genérico ou um recurso nomeado quando é encontrado um.

O campo **Categoria** contém os valores que indicam um tipo mais amplo de trabalho no qual a tarefa pode ser agrupada. Este campo não afeta o agendamento nem a definição de pessoal. É utilizado apenas para relatórios.

### <a name="task-dependencies"></a>Dependências de tarefa 

Pode utilizar a agenda no PSA para criar relações antecessoras entre tarefas. O campo **Antecessor** em **Tarefas** utiliza um ou mais valores para indicar as tarefas de que uma tarefa depende. Quando os valores antecessores são atribuídos a uma tarefa, a tarefa pode ser iniciada apenas depois de todas as tarefas antecessoras terem sido concluídas. Devido à dependência, a data de início planeada da tarefa é reposta para a data em que as tarefas antecessoras são concluídas.

O modo de tarefa não tem efeito nas atualizações efetuadas nas datas de início e de fim das tarefas antecessoras/dependentes.

## <a name="task-mode"></a>Modo de tarefa 

O modo de tarefa determina o agendamento de tarefas de nós de folha. O PSA suporta dois modos de tarefa para cada tarefa: agendamento automático e agendamento manual.

### <a name="auto-scheduling"></a>Agendamento automático 
 
Quando o modo de tarefa é definido como **Agendado Automaticamente** para uma tarefa, o motor de agendamento da tarefa utiliza as regras de agendamento nos atributos da tarefa para determinar a agenda para a tarefa.

#### <a name="scheduling-rules"></a>Regras de agendamento

Por predefinição, se a tarefa de nós de folha não tiver antecessores, a sua data de início é definida como a data de início agendada do projeto. A duração de uma tarefa de nós de folha é sempre calculada como o número de dias de trabalho entre as datas de início e de fim. Quando uma tarefa é agendada automaticamente, o motor de agendamento segue estas regras:

- As datas de início e de fim da tarefa têm de ser dias de trabalho de acordo com o calendário de agendamento do projeto. 
- Para qualquer tarefa que possua tarefas antecessoras, a data de início é automaticamente definida como a data de fim mais recente dos seus antecessores.
- O esforço é calculado através da utilização desta fórmula: número de pessoas × duração × horas num dia de trabalho padrão no calendário do projeto.

### <a name="manual-scheduling"></a>Agendamento manual

Se as regras do agendamento automático não corresponderem aos seus requisitos, pode definir o modo de tarefa para que a tarefa seja **Agendada Manualmente**. Esta definição para o motor de agendamento para o cálculo dos valores de outros atributos de agendamento. Independentemente do modo de tarefa, se definir os antecessores nas tarefas, afeta sempre a data de início da tarefa dependente.
