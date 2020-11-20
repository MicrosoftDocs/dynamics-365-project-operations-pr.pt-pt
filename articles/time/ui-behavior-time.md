---
title: Comportamento da IU de entrada de hora
description: Este tópico fornece informações sobre o comportamento da IU para Entrada de Hora.
author: stsporen
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 8719e2f9ee4867f17ed75142eca2115f61e37999
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124517"
---
# <a name="time-entry-ui-behavior"></a>Comportamento da IU de entrada de hora

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_


A grelha **Entrada de hora semanal** é um controlo personalizado que tem duas secções principais: **Dimensões** e **Duração**.

## <a name="dimensions"></a>Dimensões
A secção **Dimensões** mostra as dimensões nas quais é possível introduzir o tempo. As seguintes dimensões são suportadas imediatamente:

  - Project
  - Tarefa de Projeto
  - Função
  - Tipo
  - Estado da Entrada

A secção **Dimensões** não permite a edição inline. Esta seção é apoiada por uma vista que permite que campos personalizados sejam adicionados à grelha de entrada de tempo semanal.

## <a name="duration"></a>Duração
A secção Duração mostra os dias da semana como cabeçalhos de coluna. Esta secção permite a edição inline. Após a criação de uma linha de entrada de hora com as dimensões apropriadas, os utilizadores podem introduzir rapidamente a quantidade de tempo que gastaram nessas dimensões.

## <a name="create-a-new-time-entry"></a>Criar uma nova entrada de tempo

1. Na grelha de entradas de hora, selecione **Novo**. 
2. Na caixa de diálogo **Criação Rápida de Entrada de Hora**, selecione a data de entrada de hora.
3. Introduza dados para as dimensões **Projeto**, **Tarefa de Projeto**, **Função** e **Duração**. Estas informações devem ser adicionadas em minutos, horas ou dias ao digitar **h**, **m** ou **d**, a par do número. 
4. Introduza uma descrição da entrada e quaisquer comentários que possam ser partilhados externamente sobre a entrada de hora. 

Quando guarda a entrada, os valores introduzidos aparecem na secção **Dimensões**. As informações introduzidas no campo **Duração** aparecem na data para a qual a entrada de hora foi criada.

Os campos de pesquisa são apoiados por vistas do sistema. Por exemplo, depois de um utilizador introduzir um projeto, o campo **Tarefa do Projeto** é definido como a vista **Copiar** por predefinição. Para criar entradas de tempo para tarefas que não estão atribuídas a um utilizador, selecione **Alterar Vista** na caixa de diálogo de pesquisa e, em seguida, selecione a vista **Todas as Tarefas do Projeto Ativas**.

## <a name="edit-a-time-entry"></a>Editar uma entrada de tempo 
Os detalhes de alguns campos na página de entrada de tempo, tal como **Descrição** e **Comentários Externos**, não são apresentados na grelha de entrada de tempo semanal. Em vez disso, um pequeno indicador triangular aparece nas células de **Duração** que têm estes detalhes adicionais. 

1. Para editar uma entrada de hora, selecione a célula que pretende atualizar na entrada de hora.
2. Selecione **Editar Detalhes** para atualizar os dados no painel **Formulário Principal de Entrada da Hora**. 

## <a name="copy-a-time-entry-row"></a>Copiar uma linha de entrada de tempo
Após a criação da linha, pode selecionar **Copiar Linha** para copiar a linha completa para uma nova linha. Quando uma linha é copiada desta forma, as dimensões e as durações também são copiadas. Também podem selecionar **Editar Linha** para atualizar valores de dimensão e durações na secção **Duração**.

## <a name="open-a-time-entry-behavior"></a>Abrir um comportamento de entrada de hora
Para suportar a entrada ideal e rápida nos campos mais importantes, a grelha de entrada de hora semanal mostra um subconjunto de dimensões e durações de tempo selecionadas. Para ver todos os detalhes de uma única entrada de tempo, em **Editar Entrada**, selecione **Abrir**.

## <a name="submit-a-time-entry"></a>Submeter uma entrada de tempo
Pode submeter uma única entrada de hora ou um grupo de entradas de hora ao selecionar um bloco de células ou uma linha de entrada de hora inteira e, em seguida, selecionar **Submeter**. As entradas de tempo submetidas são apresentadas como pendentes de aprovação na página **Aprovação** dos aprovadores. Depois de as entradas de tempo serem submetidas com êxito, não é possível editá-las.

## <a name="recall-a-time-entry"></a>Recuperar uma entrada de tempo
Pode recuperar entradas de tempo que tenha submetido. Pode recuperar uma única entrada de tempo, um bloco de entradas de tempo ou uma linha inteira de entradas de tempo. As entradas de hora recuperadas podem ser editadas.

## <a name="time-entry-status"></a>Estado de entrada de tempo

- **Rascunho**: as novas entradas de hora recebem automaticamente o estado de **Rascunho**. Só é possível eliminar as entradas de tempo com o estado **Rascunho**.
- **Submetido**: quando uma entrada de hora é submetida, o estado é atualizado para **Submetido**. 
- **Aprovado**: quando uma entrada de hora submetida é aprovada, o estado é atualizado para **Aprovado**. 
- **Devolvido**: se uma entrada de hora for rejeitada, o estado é atualizado para **Devolvido** e a entrada fica disponível para correção e nova submissão. 

## <a name="view-rejection-comments"></a>Ver comentários de rejeição
Quando uma entrada de hora é rejeitada por um aprovador, o aprovador poderá adicionar comentários para ajudar o recurso a compreender o motivo da rejeição. Para ver os comentários de rejeição para uma entrada de tempo, selecione **Abrir entrada**. Os comentários de rejeição serão mostrados na linha cronológica. O utilizador pode responder aos comentários de rejeição antes de voltar a submeter a entrada.

## <a name="copy-week"></a>Copiar semana
Depois de criadas algumas entradas de hora, os utilizadores podem várias entradas de hora ao mesmo tempo.

1. No formulário **Entradas de Hora**, selecione **Copiar Semana** para criar entradas de hora adicionais em massa. 
2. Na caixa de diálogo **Copiar** na secção **Do período**, utilize os campos **Data de Início** e **Data de Fim** para definir o intervalo de datas a partir do qual pretende copiar entradas de hora. 
3. Na secção **Até ao Período**, no campo **Data de Início**, especifique a data para a qual as entradas de tempo são criadas. 
4. Selecione **Copiar**. Para a data especificada em **Até ao período**, é criada uma cópia das entradas de hora para o dia da semana correspondente em **Do período**. Por exemplo, a entrada de hora de segunda-feira da semana passada é copiada para a segunda-feira da semana especificada como **Ao período**.

## <a name="import"></a>Importação
O mesmo processo básico é utilizado para importar reservas, atribuições e trocas. Pode especificar o intervalo de datas a partir do qual as reservas são importadas e, em seguida, selecionar explicitamente as reservas que devem ser copiadas para entradas de hora de rascunho. 
