---
title: Estimar vendas e custos do projeto quando um recurso reservável preenche várias funções num projeto
description: Este tópico explica como usar as dimensões dos preços para suportar as estimativas de preços e custos para um recurso que preenche várias funções num projeto.
author: rumant
manager: tfehr
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: da17f0f58623128d51fda0f5529182cd37ea41b9
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531523"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-on-a-project"></a>Estimar vendas e custos do projeto quando um recurso reservável preenche várias funções num projeto 

_**Aplica-se a:** Project Operations para cenários baseados em Recursos/Não Stock, implementação Lite – negócio para faturação pró-forma, Project Operations para cenários baseados em Stock/Produção_ 

As empresas baseadas em projetos têm muitas vezes a necessidade que um recurso preencha várias funções num projeto. Cada função pode ter o preço e o custo definidos de forma diferente. Isto significa que o tempo do mesmo recurso num projeto poderia obter uma estimativa financeira diferente, dependendo da conta e das taxas de custo para cada função. Pode configurar os valores no registo do membro da equipa para o recurso nomeado com diferentes definições manuais em cada uma das tarefas a que o membro da equipa está atribuído.

O exemplo que se segue explica como a simples definição manual de um valor permite que um recurso tenha múltiplas funções num projeto com diferentes taxas de custo e fatura.

## <a name="create-tasks"></a>Criar tarefas
Para criar tarefas, é necessário adicionar tarefas, bem como tarefas de resumo, após as quais necessita de atribuir a tarefa antes de adicionar a duração da tarefa. 

### <a name="add-tasks-and-summary-tasks"></a>Adicionar tarefas e tarefas de resumo
Para adicionar uma tarefa, conclua os seguintes passos.

1. Vá a **Projetos** e abra o projeto ao qual pretende adicionar tarefas.
2. Selecione **Adicionar nova tarefa**. Nomeie a tarefa e, em seguida, prima **Enter**.
3. Introduza outro nome de tarefa e pressione **Enter**. Repita isto até ter uma lista completa de tarefas.
3. Para avançar tarefas em tarefas de **Resumo**, selecione os três pontos verticais pelo nome da tarefa e, em seguida, selecione **Criar subtarefas**. 

  > [!TIP]
  > Para selecionar mais do que uma tarefa, selecione uma tarefa, prima e mantenha premido **Ctrl** e, em seguida, selecione outra tarefa.
  >
  > Também pode escolher **Promover subtarefa** para retirar tarefas das tarefas de **Resumo**.

### <a name="assign-tasks"></a>Atribuir tarefas

Conclua os seguintes passos para atribuir tarefas.

1. Na coluna **Atribuída a** para uma tarefa, selecione o ícone da pessoa.
2. Escolha um membro da equipa na lista ou introduza texto para procurar um nome.

### <a name="add-task-duration-and-columns"></a>Adicionar duração de tarefa e colunas

É muitas vezes mais fácil começar a criar o seu projeto com duração. Conclua os seguintes passos para adicionar uma duração de tarefa.

1. Na coluna **Duração** para uma tarefa, digite o número de dias que acha que levará para realizar a tarefa. Se pretender utilizar uma unidade de tempo diferente, insira um número mais a palavra **horas**, **semanas** ou **meses**.
2. Se quiser que a sua tarefa apareça como um marco em forma de diamante na vista **Linha cronológica**, na coluna **Duração**, insira **0 dias**.
3. Prima **Enter** para ir ao campo **Duração** da próxima tarefa e continuar a introduzir durações.

  > [!NOTE]
  > Não pode introduzir uma duração para tarefas de resumo.

Pode adicionar colunas ao seu projeto para fornecer mais detalhes. Para isso, selecione **Adicionar coluna**. 

Para mais informações, consulte [Criar um projeto](https://support.microsoft.com/en-us/office/create-a-project-a5b5e823-fb2e-45fd-be00-7d84422d9749).

## <a name="set-up-the-role-and-organization-unit-for-a-generic-project-team-member"></a>Configure a função e a unidade da organização para um membro genérico da equipa de projeto
Complete os seguintes passos para criar uma função e unidade organizacional para um membro genérico da equipa.

1. Na página **Tarefas**, selecione a linha **Tarefa** para a **Tarefa A**. 
2. Em **Atribuir A**, selecione **Adicionar recurso genérico**. Isto abre a página **Criação Rápida do Membro da Equipa**.
3. Na página **Criação Rápida do Membro da Equipa**, especifique os atributos do membro da equipa genérico que pode executar esta tarefa.
4. Selecione a função e a unidade organizacional apropriadas e, em seguida, selecione **Guardar e Fechar**. Um membro da equipa genérico é criado e atribuído a esta tarefa. 
5. Repita os passos 1-4 para a **Tarefa B**. No entanto, a **Tarefa B** deve ter uma função diferente e uma unidade organizacional atribuída ao membro genérico da equipa do que a **Tarefa A**. 

## <a name="set-up-the-role-and-organization-unit-for-a-project-task"></a>Configure a função e a unidade da organização para uma tarefa de projeto
Complete os seguintes passos para criar uma função e unidade organizacional para uma tarefa.

1. Depois de criar a **Tarefa A**, selecione a tarefa e, em seguida, selecione o ícone **i** para abrir o painel **Detalhes da Tarefa**. 
2. No painel **Detalhes da Tarefa**, desloque-se para o fundo e selecione **Ver Detalhes** para abrir a página **Detalhes da Tarefa**.
3. Na página **Detalhes da Tarefa**, em **Função** e **Unidade Organizacional**, adicione os valores necessários para executar esta tarefa para o recurso. 

  > [!NOTE]
  > Se completar este cenário utilizando os dados de demonstração do Project Operations, selecione **Líder de Consultoria** para a função, e **Fabrikam US** como a unidade organizacional.

4. Selecione a **Tarefa B** e, em seguida, selecione a tarefa.
5. Selecione o ícone **i** para abrir o painel **Detalhes da Tarefa**. 
6. No painel **Detalhes da Tarefa**, desloque-se para o fundo e selecione **Ver detalhes** para abrir a página **Detalhes da Tarefa**.
7. Na página **Detalhes da Tarefa**, em **Função** e **Unidade Organizacional**, adicione os valores necessários de um recurso que executaria esta tarefa. Os valores na **Função** e na **Unidade Organizacional** para a **Tarefa B** devem ser diferentes dos da **Tarefa A**. 

  > [!NOTE]
  > Se completar este cenário utilizando os dados de demonstração do Project Operations, selecione **Técnico de Rede** para a função, e **Fabrikam US** como a unidade organizacional.

8. Guarde e feche a página **Detalhes da Tarefa**. 

## <a name="team-member-and-estimates-behavior"></a>Comportamento de membro da equipa e estimativa 
Para compreender o comportamento na grelha do **Membro da Equipa** e as estimativas, complete os seguintes passos.

1. Na grelha **Membro da Equipa**, selecione os dois membros genéricos da equipa e, em seguida, selecione **Gerar Requisitos**. Esta ação irá gerar requisitos de recursos. 
2. Selecione a linha de membro da equipa de **Líder de Consultoria** e, em seguida, selecione **Reservar**. O quadro da agenda abre com uma lista de recursos. Selecione um recurso e, em seguida, selecione **Reservar** para reservar o recurso para esse requisito.
3. Selecione a linha de membro da equipa de **Técnico de Rede** e, em seguida, selecione **Reservar**. O quadro da agenda abre com uma lista de recursos. Selecione o mesmo recurso que acima e, em seguida, selecione **Reservar** para reservar o recurso para esse requisito.

### <a name="team-member-grid"></a>Grelha Membro da Equipa 

Na grelha **Membro da Equipa**, os dois registos genéricos de membros da equipa são eliminados e substituídos por apenas um recurso. Há um conjunto de valores para esse recurso, que são um conjunto de valores predefinido para **Função** e **Unidade Organizacional**.

Quando expandires a linha para esse registo de membro da equipa, pode ver atribuições distintas no registo de membro da equipa para ambas as tarefas. Cada linha de atribuição tem valores específicos de tarefa para **Função** e **Unidade Organizacional**. 

### <a name="estimates-grid"></a>Grelha Estimativas 

Na grelha **Estimativas**, ambas as atribuições para o mesmo recurso têm um preço diferente. A atribuição do recurso na **Tarefa A** tem o preço utilizando o valor de atributo **Função** de **Líder de Consultoria**. A atribuição do mesmo recurso na **Tarefa B** tem o preço utilizando o valor de atributo **Função** de **Técnico de Rede**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]