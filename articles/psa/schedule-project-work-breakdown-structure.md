---
title: Agendar um projeto com uma estrutura hierárquica do trabalho
description: Como agendar um projeto com uma estrutura hierárquica do trabalho no Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: a00e39f78890426721a49cd569ba8ce4accb30a9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5282707"
---
# <a name="schedule-a-project-with-a-work-breakdown-structure-project-service"></a>Agendar um projeto com uma estrutura hierárquica do trabalho (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Um agenda do projeto comunica que tem de ser efetuado, que recursos irão efetuar o trabalho e o intervalo de tempo durante o qual o trabalho tem de ser concluído. A agenda do projeto reflete todo o trabalho associado à entrega do projeto a tempo. Um dos primeiros passos na fase de inicialização do projeto é definir uma agenda do projeto. Para estabelecer uma agenda do projeto, tem de criar uma estrutura hierárquica do trabalho.  
  
 Crie uma estrutura do projeto com estrutura hierárquica do trabalho, o que ajuda a:  
  
- Dividir o trabalho em tarefas geríveis  
  
- Estimar o tempo necessário para concluir uma tarefa  
  
- Definir as dependências e a duração da tarefa  
  
- Determinar as funções necessárias para concluir cada tarefa  
  
  A agenda do projeto na estrutura hierárquica do trabalho tem um aspeto e funcionalidade familiares, incluindo um gráfico Gantt interativo.  
  
## <a name="create-a-work-breakdown-structure-for-a-project"></a>Criar uma estrutura hierárquica do trabalho para um projeto  
 Crie uma estrutura hierárquica do trabalho para representar a sequência de tarefas num projeto. A estrutura hierárquica do trabalho inclui tarefas, requisitos para cada tarefa, bem como as informações do custo e das receitas. Na estrutura hierárquica do trabalho, poderá adicionar:  
  
-   A sequência de tarefas numa hierarquia  
  
-   Outras tarefas, se existirem, que tenham de ser concluídas antes de uma tarefa poder ser iniciada  
  
-   A data de início, a data de fim e a duração de uma tarefa  
  
-   O número de horas necessárias para uma tarefa  
  
-   Quaisquer competências e educação dos trabalhadores necessárias  
  
-   Os trabalhadores atribuídos a uma tarefa  
  
-   Receitas e custos estimados  
  
## <a name="task-types"></a>Tipos de tarefa  
Utilize os seguintes tipos de tarefa quando criar a sua estrutura hierárquica do trabalho:  

| | | 
|---------------------------------------|-----------------------------------------------------------------| 
| **Nó de raiz do projeto** | A tarefa de resumo de nível superior do projeto. Todas as outras tarefas do projeto são aí criadas. O nome da tarefa de raiz é o nome do projeto. O esforço, as datas e a duração do nó de raiz baseiam-se nos valores da hierarquia abaixo dele. Não pode editar as propriedades do nó de raiz nem eliminar o nó de raiz. | 
| **Tarefas de resumo ou contentor** | Uma tarefa de resumo é uma tarefa com subpastas. Uma tarefa de resumo não tem qualquer esforço de trabalho ou custo próprio. O esforço e o custo do trabalho são um rollup das respetivas subtarefas. Pode alterar o nome de uma tarefa de resumo, mas não poderá alterar o esforço, as datas ou a duração, porque estes são calculados automaticamente. Ao eliminar uma tarefa de resumo elimina a tarefa e todas as suas subtarefas.|  
| **Tarefas de nós de folha** | Uma tarefa de nós de folha representa o trabalho mais detalhado no projeto. Tem um esforço calculado, um número planeado de recursos, datas de início e de fim planeadas, e uma duração.|

  
## <a name="task-hierarchy"></a>Hierarquia de tarefas  
 Estão disponíveis as seguintes opções ao criação uma hierarquia de tarefas:  
  
- **Adicionar tarefa**.   Poderá adicionar uma tarefa numa posição à escolha na hierarquia de tarefas. Se não selecionar uma posição, a sua nova tarefa é apresentada no final.  
  
- **Avançar tarefa**.   Avance uma tarefa para a converter numa subordinada da tarefa diretamente acima.  
  
- **Diminuir avanço da tarefa**.   Diminua o avanço de uma tarefa para deixar de ser uma subtarefa do tarefa principal original.  
  
- **Mover para cima e Mover para baixo**.   Mova para cima e para baixo as tarefas na hierarquia da respetiva tarefa principal. Mover para cima ou para baixo uma tarefa não produz efeitos no respetivo esforço, custo, datas ou duração.  
  
## <a name="task-attributes"></a>Atributos da tarefa  
 O nome de uma tarefa descreve o trabalho que tem de ser concluído. Utilize vários atributos da tarefa para descrever a agenda e os requisitos de pessoal para a tarefa.  
  
### <a name="schedule-attributes"></a>Agendar atributos

 - Atribua valores a **Horas de Esforço**, **Número de recursos**, **Data de início**, **Data de fim** e **Duração** para determinar a agenda da tarefa. 
 - **Esforço** é uma estimativa das horas que demora a concluir a tarefa.
 - **Número de recursos** é uma estimativa que o gestor do projeto coloca na tarefa para ajudar a determinar a melhor agenda possível. 
 - **Duração** (dias) indica o número de dias de trabalho que demorará a concluir a tarefa.  
  
### <a name="staffing-attributes"></a>Atributos do pessoal

 - **Função**, **Unidade organizacional do recurso**, **Número de recursos** e **Recursos** descrevem os requisitos de pessoal para a tarefa. 
 - **Função** descreve o tipo de recurso necessário para executar a tarefa. 
 - **Unidade organizacional do recurso** indica a unidade organizacional na qual os recursos devem receber pessoal para essa tarefa; isto também tem impacto na estimativa de custo e vendas da tarefa, uma vez que é contabilizado para quando determinar o preço de venda da unidade do recurso. 
 - **Recursos** contém um recurso genérico ou um recurso nomeado quando é encontrado um.  
  
## <a name="task-dependencies"></a>Dependências de tarefa  
 Poderá criar relações de antecessora entre uma ou mais tarefas na estrutura hierárquica do trabalho. Pode definir um ou mais valores para o campo antecessor nas tarefas para indicar as tarefas das quais irá depender. Quando atribui um valor antecessor a uma tarefa, a tarefa só pode ser iniciado quando todas as tarefas antecessoras forem concluídas. A definição desta dependência numa tarefa resulta no recálculo da data de início planeado da tarefa como o último final de todas as antecessoras. Os impactos relacionados com a antecessora numa agenda não estão limitados pelo modo de tarefa definido na tarefa.  
  
## <a name="task-mode"></a>Modo de tarefa  
 O modo de tarefa é um dos mais importantes fatores que determinam as tarefas de nós de folha de agendamento. Existem dois modos de tarefa para cada tarefa: modo de agendamento automático e modo de agendamento manual.  
  
-   **Agendamento automático**.   Quando define o modo de tarefa como Agendado Automaticamente, o motor de agendamento da tarefa utiliza as regras de agendamento nos seguintes atributos da tarefa para determinar a agenda para a tarefa:  
  
    -   Antecessores  
  
    -   Esforço  
  
    -   Número de recursos  
  
    -   Dadas de início e de fim  
  
-   **Regras de agendamento**.   A data de início de uma tarefa de nós de folha não tem predefinições de antecessores para a data de início de agendamento do projeto. A duração de uma tarefa de nós de folha é sempre calculada como o número de dias de trabalho entre as datas de início e de fim. Quando uma tarefa é agendada automaticamente, o motor de agendamento segue as regras abaixo:  
  
    -   As datas de início e de fim de uma tarefa têm de ser sempre dias úteis de acordo com o calendário de agendamento do projeto  
  
    -   A data de início de uma tarefa com antecessores assume por predefinição a data de fim mais recente dos respetivos antecessores  
  
    -   Esforço = número de pessoas * Duração * horas num dia útil padrão do calendário do projeto  
  
-   **Agendamento manual**.   Em alguns casos, poderá querer afastar-se destas regras. Nestes casos, poderá definir o modo de tarefa para a tarefa ser agendada manualmente. Desta forma, o motor de agendamento para o cálculo dos valores para outros atributos de agendamento. A definição de antecessores em tarefas tem sempre impacto na data de início da tarefa dependente.  
  
## <a name="create-a-work-breakdown-structure"></a>Criar uma estrutura hierárquica do trabalho  
  
1.  Vá para **Project Service > Projetos**.  
  
2.  Clique no projeto em que pretende trabalhar.  
  
3.  Na barra na parte superior do ecrã, selecione a seta para baixo junto ao nome do projeto e, em seguida, clique em estrutura hierárquica do trabalho.  
  
4.  Para adicionar uma tarefa, clique em **Adicionar Tarefa**. Preencha os campos para a tarefa e clique e **Guardar**.  
  
5.  Continue a adicionar tarefas até a estrutura hierárquica do trabalho estar concluída. Enquanto cria a estrutura hierárquica do trabalho, pode fazer o seguinte para organizar as suas tarefas:  
  
    -   Selecione uma tarefa e clique em **Avançar** para movê-la para outra tarefa ou clique em Diminuir Avanço para a mover para fora de um nível.  
  
    -   Selecione uma tarefa e clique em **Mover para Cima** ou **Mover para Baixo** para a mover para cima ou para baixo na lista.  
  
    -   Clique em **Ocultar Gantt** para ocultar o gráfico Gantt e clique em **Mostrar Gantt** para o apresentar novamente.  
  
    -   Selecione um período de tempo diferente para o gráfico Gantt em **Escala Temporal**.  
  
6.  Para adicionar as funções especificadas na estrutura hierárquica do trabalho aos membros da equipa do projeto, clique em **Gerar Equipa do Projeto**.  
  
7.  Clique em **Guardar** no canto inferior direito do ecrã quando concluir as alterações.  
  
### <a name="see-also"></a>Consulte Também  
 [Manual do gestor de projeto](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]