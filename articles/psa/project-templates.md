---
title: Modelos de projeto
description: Este tópico fornece informações sobre como utilizar modelos de projeto para configuração rápida do projeto.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 1bb82a312114e9814f5ce65a1698455582fd252e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082566"
---
# <a name="project-templates"></a>Modelos de projeto 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Um modelo de projeto é uma estrutura predefinida que o ajuda a iniciar um projeto de forma rápida e fácil. Pode utilizar um modelo predefinido para criar um novo projeto com um único clique. Quanto aos projetos, deve definir os pré-requisitos para os modelos de projeto. Tem de definir um calendário de projeto para cada modelo de projeto, e as funções e listas de preços devem ser predefinidas na organização, para que os componentes do modelo tenham dados úteis.

Um modelo de projeto consiste em três componentes: uma agenda, estimativas do projeto e membros da equipa do projeto.

## <a name="schedule"></a>Agendar

Uma agenda num modelo de projeto tem o mesmo conjunto de elementos como uma agenda num projeto. Pode criar uma hierarquia de tarefas, associar funções às tarefas, definir atributos da agenda e definir dependências. Uma agenda num modelo de projeto também suporta modos de tarefas para cada tarefa. Consequentemente, suporta o motor de agendamento. Tem de associar um calendário do projeto ao projeto. Quando cria uma agenda de trabalho, não há diferença entre um modelo de projeto e um projeto.

## <a name="project-estimates"></a>Estimativas do projeto

As estimativas de projeto num modelo de projeto funcionam da mesma maneira que as estimativas de projeto num projeto. No entanto, os preços de custo e venda são extraídos das listas de preços de custo e venda predefinidas que são definidas nos parâmetros.

## <a name="creating-a-project-from-a-template"></a>Criar um projeto a partir de um modelo
 
Existem várias formas de criar um projeto a partir de um modelo de projeto:

- Ao criar um projeto a partir de uma proposta, pode selecionar um modelo de projeto na caixa de diálogo **Criação Rápida: Projeto**.

> ![Caixa de diálogo Criação Rápida: Projeto](media/project-11.png)

- Quando cria um projeto selecionando **Novo Projeto** , a página **Projeto** aparece antes de o registo ser guardado. No campo **Selecionar um Modelo** , selecione um dos modelos de projeto predefinidos na organização.
- Utilize **Criar Projeto a partir de um Modelo** na página **Entidade Modelo**.

## <a name="copying-components-of-template-to-project"></a>Copiar componentes de um modelo para um projeto

Quando copia os componentes de um modelo de projeto para um projeto, algumas substituições podem ocorrer, consoante as definições no projeto.

### <a name="copying-the-schedule"></a>Copiar a agenda

Quando copia a agenda a partir de um modelo de projeto, se o projeto tiver um calendário do projeto diferente do modelo, as horas de trabalho do calendário do projeto serão aplicadas à agenda da tarefa. Desta forma, a agenda é ajustada para corresponder ao calendário do projeto subjacente. Da mesma forma, a primeira tarefa na agenda assume a data de início do projeto e a agenda do resto da hierarquia é atualizada com base na duração e nas dependências especificadas no modelo. 

### <a name="copying-project-estimates"></a>Copiar estimativas do projeto 

Quando copia em linhas de estimativa do projeto, as listas de preços são atualizadas. Para a lista de preços de custo, estas atualizações baseiam-se na unidade proprietária do projeto. Para a lista de preços de venda, baseiam-se no cliente. Para projetos associados a uma entidade de vendas, o custo unitário e os preços de venda são determinados com base nestas listas de preços.

### <a name="copying-a-project-team"></a>Copiar uma equipa do projeto

Quando uma equipa do projeto é copiada de um modelo de projeto para um projeto, os recursos genéricos são copiados, juntamente com as competências e proficiências definidas no modelo. As atribuições de recursos genéricos também são mantidas como no modelo do projeto. Os recursos nomeados não são suportados em modelos de projeto.
