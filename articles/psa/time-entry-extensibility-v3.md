---
title: Personalizar entrada de tempo semanal
description: Este tópico fornece informações sobre como implementar regras de negócio personalizadas que suportam as práticas de uma organização.
author: stsporen
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 07/09/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: f1c8e150500334e87b25a1c8d04cf28c7b7beaeb
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5282077"
---
# <a name="customize-weekly-time-entry"></a>Personalizar entrada de hora semanal 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

No Microsoft Dynamics 365 Project Service Automation, versão 3.3, a Microsoft introduziu uma grelha moderna que permite que os recursos do projeto introduzam rapidamente tempo por até uma semana de cada vez. A nova grelha de entrada de tempo semanal pode mostrar o total de entradas por data, por linha ou por semana. Os recursos podem fazer cópias das entradas de tempo dentro da semana e também copiar em massa as semanas anteriores. Os personalizadores de sistemas podem personalizar a vista adicionando campos, adicionando pesquisas a outras entidades e implementando regras de negócio personalizadas para suportar as práticas da organização.

A entrada de tempo e a nova grelha de tempo semanal são acedidas através do mapa do site. A experiência de entrada de tempo personalizada não extensível que fazia parte das versões anteriores do PSA foi substituída pela grelha de entrada de tempo semanal extensível e também por uma experiência alternativa na grelha e no calendário só de leitura. Devido a esta alteração, os utilizadores podem introduzir horas em montantes semanais.

## <a name="page-layout"></a>Esquema de página
A nova grelha de entrada de tempo semanal é um controlo personalizado que tem uma barra de ferramentas e duas secções principais **Dimensões** e **Duração**. A barra de ferramentas inclui um botão que só é aplicável a este controlo personalizado para a grelha de entrada de tempo. Por outro lado, os botões no Painel de Ação, na parte superior da página, aplicam-se aos três tipos de controlos suportados com a entrada de tempo: o controlo de entrada de tempo semanal, o controlo só de leitura e o controlo de calendário.

### <a name="dimensions"></a>Dimensões
A secção **Dimensões** mostra, como os cabeçalhos de coluna, todas as dimensões nas quais é possível introduzir o tempo. As seguintes dimensões são suportadas imediatamente:

- Projeto
- Tarefa de Projeto
- Função
- Tipo
- Estado da Entrada

A secção **Dimensões** não permite a edição inline. Esta seção é apoiada por uma vista que permite que campos personalizados sejam adicionados à grelha de entrada de tempo semanal. Para obter informações sobre como adicionar campos personalizados, consulte a secção "Extensibilidade" posteriormente neste tópico.

### <a name="duration"></a>Duração
A secção Duração mostra os dias da semana como cabeçalhos de coluna. Esta secção permite a edição inline. Após a criação de uma linha de entrada de tempo com as dimensões apropriadas, os utilizadores podem introduzir rapidamente, inline, a quantidade de tempo que gastaram nessas dimensões.

## <a name="create-a-new-time-entry"></a>Criar uma nova entrada de tempo
Para criar uma nova entrada de tempo na grelha de entrada de tempo, selecione **Novo**. É apresentada a caixa de diálogo **Criação Rápida de Entrada de Tempo**. Nesta caixa de diálogo, os utilizadores podem selecionar a data de entrada de tempo e, em seguida, introduzir dados para as dimensões **Projeto**, **Tarefa do Projeto**, **Função** e **Duração** em minutos, horas ou dias, introduzindo **h**, **m** ou **d**, juntamente com o número. Os utilizadores também podem introduzir uma descrição e comentários que podem ser partilhados externamente durante a entrada de tempo. Quando os utilizadores guardam as suas alterações, são apresentados os valores introduzidos relativamente às dimensões na secção **Dimensões**. As informações de duração introduzidas no campos **Duração** aparecem na data para a qual a entrada de tempo foi criada.

Os campos de pesquisa são apoiados por vistas do sistema. Por exemplo, depois de um utilizador introduzir um projeto, o campo **Tarefa do Projeto** é definido como a vista **Copiar** por predefinição. Para criar entradas de tempo para tarefas que não estão atribuídas a um utilizador, selecione **Alterar Vista** na caixa de diálogo de pesquisa e, em seguida, selecione a vista **Todas as Tarefas do Projeto Ativas**.

## <a name="edit-a-time-entry"></a>Editar uma entrada de tempo
Os detalhes de alguns campos na página de entrada de tempo, tal como **Descrição** e **Comentários Externos**, não são apresentados na grelha de entrada de tempo semanal. Em vez disso, um pequeno indicador triangular aparece nas células de duração que possuem estes detalhes adicionais. Selecione a célula e, em seguida, selecione **Editar Detalhes** para ver os dados no painel **Edição Rápida**. Para editar ou atualizar os detalhes de uma entrada de tempo específica que não faça parte da grelha de entrada de tempo semanal, os utilizadores têm de abrir o painel **Edição Rápida**.

## <a name="copy-a-time-entry-row"></a>Copiar uma linha de entrada de tempo
Após a criação da primeira linha de entrada, os utilizadores podem selecionar **Copiar Linha** para copiar a linha completa para uma nova linha. Quando uma linha é copiada desta forma, as dimensões e as durações também são copiadas. Os utilizadores também podem selecionar **Editar Linha** para atualizar valores de dimensão e durações inline na secção **Duração**.

## <a name="open-a-time-entry"></a>Abrir uma entrada de tempo
Para suportar a entrada ideal e rápida nos campos mais importantes, a grelha de entrada de tempo semanal mostra um subconjunto de dimensões e durações de tempo selecionadas. Para ver todos os detalhes de uma única entrada de tempo, em **Editar Entrada**, selecione **Abrir**.

## <a name="submit-a-time-entry"></a>Submeter uma entrada de tempo
Os utilizadores podem submeter uma única entrada de tempo ou um grupo de entradas de tempo selecionando um bloco de células ou uma linha de entrada de tempo inteira e, em seguida, selecionando **Submeter**. As entradas de tempo submetidas são apresentadas como pendentes de aprovação na página **Aprovação** dos aprovadores. Depois de as entradas de tempo serem submetidas com êxito, não é possível editá-las.

## <a name="recall-a-time-entry"></a>Recuperar uma entrada de tempo
Pode recuperar entradas de tempo que tenha submetido. Pode recuperar uma única entrada de tempo, um bloco de entradas de tempo ou uma linha inteira de entradas de tempo. As entradas de tempo recuperadas estão disponíveis para os recursos para edição.

## <a name="time-entry-status"></a>Estado de entrada de tempo
As novas entradas de tempo recebem automaticamente um estado de **Rascunho**. Quando uma entrada de tempo é submetida, o estado é atualizado para **Submetido**. Quando uma entrada de tempo submetida é aprovada, o estado é atualizado para **Aprovado**. Se uma entrada de tempo for rejeitada, o estado é atualizado para **Devolvido** e a entrada fica disponível para correção e nova submissão. Só é possível eliminar as entradas de tempo com o estado **Rascunho**.

## <a name="view-rejection-comments"></a>Ver comentários de rejeição
Quando uma entrada de tempo é rejeitada por um aprovador, o aprovador poderá adicionar comentários de rejeição para ajudar o recurso a compreender o motivo da rejeição. Para ver os comentários de rejeição para uma entrada de tempo, selecione **Abrir entrada**. Os comentários de rejeição serão mostrados na linha cronológica. Na linha cronológica, o recurso pode responder aos comentários de rejeição antes de o utilizador resubmeter a entrada.

## <a name="copy-week"></a>Copiar semana
Depois de terem sido criadas algumas entradas de tempo, os utilizadores podem selecionar **Copiar Semana** para criar entradas de tempo adicionais em massa. É apresentada a caixa de diálogo **Copiar**. Na secção **Do período**, utilize os campos **Data de Início** e **Data de Fim** para definir o intervalo de datas a partir do qual pretende copiar entradas de tempo. Na secção **Até ao Período**, no campo **Data de Início**, especifique a data para a qual as entradas de tempo são criadas. Em seguida, selecione **Copiar**. Para a data especificada no período "até", é criada uma cópia das entradas de tempo para o dia da semana correspondente no período "de". Por exemplo, a entrada de tempo de segunda-feira da semana passada é copiada para a segunda-feira da semana especificada como o período "até".

## <a name="import"></a>Importar
O mesmo processo básico é utilizado para importar reservas, atribuições e trocas. Os utilizadores podem especificar o intervalo de datas a partir do qual as reservas são importadas. Em seguida, tem de selecionar explicitamente as reservas que devem ser copiadas para as entradas de tempo de rascunho. Na versão anterior, as entradas de tempo sugeridas apareceram na grelha e no calendário e foram perdidas quando a sessão foi atualizada.

## <a name="extensibility"></a>Extensibilidade
### <a name="add-custom-fields-that-have-lookups-to-other-entities"></a>Adicionar campos personalizados que tenham pesquisas a outras entidades
Existem três passos principais para adicionar um campo personalizado à grelha de entrada de tempo semanal.

1.  Adicione o campo personalizado à caixa de diálogo de criação rápida.
2.  Configure a grelha para mostrar o campo personalizado.
3.  Adicione o campo personalizado ao fluxo de tarefas de edição de linhas ou ao fluxo de tarefas de edição de células, conforme adequado.

Também deve garantir que o novo campo tenha as validações necessárias no fluxo de tarefas de edição de linhas ou células. Como parte deste passo, tem de bloquear o campo com base no estado de entrada de tempo.

#### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Adicionar o campo personalizado à caixa de diálogo de criação rápida
Tem de adicionar o campo personalizado à caixa de diálogo Criação Rápida de Entrada de Tempo. para que os utilizadores possam introduzir um valor para o mesmo quando adicionarem entradas de tempo utilizando o botão **Novo**.

#### <a name="configure-the-grid-to-show-the-custom-field"></a>Configurar a grelha para mostrar o campo personalizado
Existem duas maneiras para adicionar um campo personalizado à grelha de entrada de tempo semanal. A primeira opção é personalizar a vista **As Minhas Entradas de Tempo Semanais** e adicionar o campo personalizado à mesma. Pode escolher a posição e o tamanho do campo personalizado na grelha editando essas propriedades na vista.

A segunda opção é criar uma nova vista de entrada de tempo personalizada e defini-la como a vista predefinida. Esta vista deve conter os campos **Descrição** e **Comentários Externos**, além das colunas que pretende ter na grelha. Pode escolher a posição, o tamanho e a sequência de ordenação predefinida da grelha editando essas propriedades na vista. Em seguida, configure o controlo personalizado para esta vista para que seja um controlo **Grelha de Entrada de Tempo**. Adicione este controlo à vista e selecione-o para Web, telefone e tablet. Em seguida, configure os parâmetros para a grelha de entrada de tempo semanal. Defina o campo **Data de Início** para **msdyn_date**, defina o campo **Duração** para **msdyn_duration** e defina o campo **Estado** para **msdyn_entrystatus**. Para a vista predefinida, o campo **Estado de Lista Só de Leitura** é definido como **192350002,192350003,192350004** o campo **Fluxo de Tarefas de Edição de Linhas** é definido como **msdyn_timeentryrowedit** e o campo **Fluxo de Tarefas de Edição de Células** é definido como **msdyn_timeentryedit**. Pode personalizar estes campos para adicionar ou remover o estado só de leitura ou para utilizar uma experiência baseada em tarefas diferente (TBX) para a edição de linhas ou células. Estes campos devem estar vinculados a um valor estático.

#### <a name="add-the-custom-field-to-the-appropriate-edit-task-flow"></a>Adicionar o campo personalizado ao fluxo de tarefas de edição apropriado
As páginas de TBX que são utilizadas para edição podem ser encontradas em **Processos**. As páginas predefinidas são **Project Service - Editar Linha de Entrada de Tempo** e **Project Service - Editar Entrada de Tempo**. Pode editar estas páginas predefinidas ou criar novas páginas de TBX personalizadas.

> [!NOTE] 
> Ambas as opções irão remover algumas filtragens fornecidas com o programa nas entidades **Projeto** e **Tarefa do Projeto**, para que todas as vistas de pesquisa das entidades sejam visíveis. Fornecidas com o programa, apenas as vistas de pesquisa relevantes são visíveis.

Tem de determinar o fluxo de tarefas apropriado para o campo personalizado. Provavelmente, se adicionou o campo à grelha, deve entrar no fluxo de tarefas de edição de linhas que é utilizado para os campos que se aplicam a toda a linha de entradas de tempo. Se o campo personalizado tiver um valor exclusivo todos os dias, tal como um campo personalizado para **Hora de Fim**, este deverá entrar no fluxo de tarefas de edição de células.

Para adicionar o campo personalizado a um fluxo de tarefas, arraste um elemento de **Campo** para a posição apropriada na página e, em seguida, defina as respetivas propriedades. Defina a propriedade **Origem** como **Entrada de Tempo** e defina a propriedade **Campo de Dados** como o campo personalizado. A propriedade **Campo** especifica o nome a apresentar na página de TBX. Selecione **Aplicar** para guardar as alterações no campo. Em seguida, selecione **Atualizar** para guardar as alterações na página.

Para utilizar uma nova página de TBX personalizada, crie um novo processo. Defina a categoria como **Fluxo do Processo de Negócio**, defina a entidade como **Entrada de Tempo** e defina o tipo de processo de negócio como **Executar processo como fluxo de tarefas**. Em **Propriedades**, a propriedade **Nome da página** deve ser definida como o nome a apresentar da página. Adicione todos os campos relevantes à página de TBX. Guarde e ative o processo e, em seguida, atualize a propriedade de controlo personalizado para o fluxo de tarefas relevante para o valor **Nome** no processo.

### <a name="add-new-option-set-values"></a>Adicionar novos valores do conjunto de opções
Para adicionar valores do conjunto de opções a um campo fornecido com o programa, abra a página de edição para o campo e, em seguida, em **Tipo**, selecione **Editar** junto do conjunto de opções. Em seguida, adicione uma nova opção que tenha uma etiqueta e cor personalizadas. Se pretender adicionar um novo estado de entrada de tempo, o campo fornecido com o programa é denominado **Estado de Entrada**, e não **Estado**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Designar um novo estado de entrada de tempo como só de leitura
Para designar um novo estado de entrada de tempo como só de leitura, adicione o novo valor de entrada de tempo (o número, e não a etiqueta) à propriedade **Estado de Lista Só de Leitura**. A parte editável da grelha de entrada de tempo será bloqueada para as linhas que tenham o novo estado.
Em seguida, adicione regras de negócio para bloquear todos os campos nas páginas de TBX **Editar Linha de Entrada de Tempo** e **Editar Entrada de Tempo**. Pode aceder às regras de negócio para estas páginas abrindo o editor de fluxo do processo de negócio para a página e, em seguida, selecionando **Regras de Negócio**. Pode adicionar o novo estado à condição nas regras de negócio existentes ou pode adicionar uma nova regra de negócio para o novo estado.

### <a name="add-custom-validation-rules"></a>Adicionar regras de validação personalizadas
Existem dois tipos de regras de validação que pode adicionar à experiência de grelha de entrada de tempo semanal: • Regras de negócio do lado do cliente que funcionam em caixas de diálogo de criação rápida e em páginas de TBX • Validações de plug-ins do lado do servidor que se aplicam a todas as atualizações de entradas de tempo

#### <a name="business-rules"></a>Regras de negócio
Utilize regras de negócio para bloquear e desbloquear campos, introduzir valores predefinidos nos campos e definir validações que requerem informações apenas do registo de entrada de tempo atual. Pode aceder às regras de negócio para uma página de TBX abrindo o editor de fluxo do processo de negócio para a página e, em seguida, selecionando **Regras de Negócio**. Em seguida, pode editar as regras de negócio existentes ou adicionar uma nova regra de negócio. Para obter ainda mais validações personalizadas, pode utilizar uma regra de negócio para executar JavaScript.

#### <a name="plug-in-validations"></a>Validações de plug-ins
Deve utilizar validações de plug-ins para quaisquer validações que exijam mais contexto do que o disponível num registo de entrada de tempo único ou para as validações que pretende executar nas atualizações inline na grelha. Para concluir a validação, crie um plug-in personalizado na entidade **Entrada de Tempo**.

> [!IMPORTANT] 
> Atualmente, um problema conhecido nas páginas de TBX impede os utilizadores de corrigir informações e selecionar novamente Concluído quando uma atualização falha na validação de plug-in. Como solução alternativa, configure as validações de regras de negócio para evitar esta situação o máximo possível.


[!INCLUDE[footer-include](../includes/footer-banner.md)]