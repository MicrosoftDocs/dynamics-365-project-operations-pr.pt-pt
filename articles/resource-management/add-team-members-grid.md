---
title: Adicionar membros da equipa a partir da grelha Membro da equipa
description: Este tópico fornece informações sobre como pode gerir os recursos dos membros da equipa.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: de73dac28046ec98ed201e129be6511f894223fd
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121547"
---
# <a name="add-team-members-from-the-team-member-grid"></a>Adicionar membros da equipa a partir da grelha Membro da equipa

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

O Dynamics 365 Project Operations inclui um dashboard Gestor de recursos que fornece uma descrição geral visual da procura e utilização de recursos em toda a organização. Pode utilizar os gráficos neste dashboard para visualizar as seguintes informações:

- **Procura de recursos:** o gráfico **Pedido de Recursos Ativos** mostra os recursos que foram submetidos. Os recursos são agregados por uma função ou projeto.
- **Procura de recursos não submetidos:** o gráfico **Procura de Recursos Não Atribuídos** mostra todos os requisitos de recursos que não foram submetidos. Este gráfico ajuda os Gestores de recursos a visualizarem a procura que não é firme e que pode ser submetida através de um pedido de recurso.
- **Utilização faturável para a semana passada**: o gráfico **Utilização por Função** mostra a percentagem da utilização faturável real da organização por função relativamente à utilização faturável de destino por função.

    > [!NOTE]
    > Para disponibilizar o gráfico **Utilização por Função**, crie uma tarefa que execute o fluxo de trabalho **UpdateRoleUtilization**. Esta tarefa periódica é executada a cada sete dias para calcular a utilização faturável nos sete dias anteriores. Os resultados são agregados por função.

## <a name="manage-project-team-members"></a>Gerir membros da equipa do projeto

Os gestores de projeto podem utilizar o dashboard Gestor de recursos para gerir os recursos nos projetos. Por exemplo, podem adicionar um membro da equipa diretamente a um projeto e reservar um membro da equipa para cumprir os requisitos de recursos que foram capturados por um recurso genérico.

### <a name="add-a-team-member-directly-to-a-project"></a>Adicionar um membro da equipa diretamente a um projeto

Para adicionar um membro da equipa diretamente a um projeto, no formulário **Projetos**, no separador **Equipa**, selecione **Novo**. É apresentada a caixa de diálogo **Criação Rápida: Membro da Equipa do Projeto**. Nesta caixa de diálogo, pode efetuar estas tarefas:

- **Reservar um recurso nomeado**: no campo **Recurso Reservável**, selecione o nome do recurso. Em seguida, selecione a função, defina o período e selecione um método de alocação. O recurso nomeado que selecionou é adicionado ao projeto utilizando o método de alocação selecionado e o calendário de recursos.
- **Adicionar um recurso genérico**: deixe o campo **Recurso reservável** em branco e, em seguida, selecione a função, defina o período e selecione o método de alocação preferencial. É adicionado um recurso genérico à equipa como marcador de posição. O marcador de posição contém o padrão de procura que é utilizado para reservar os recursos nomeados na equipa. O requisito é efetuado de acordo com o calendário do projeto.
- **Adicionar um recurso nomeado à equipa sem consumir capacidade do recurso**: no campo **Recurso Reservável**, selecione um recurso. Selecione o período e selecione **Nenhum** como método de alocação. O recurso é adicionado à equipa, mas a capacidade do recurso não é consumida através de uma reserva.

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a>Reservar um membro da equipa para cumprir os requisitos de recursos para um recurso genérico

Nas Project Operations, pode reservar um recurso genérico numa equipa de projeto. Também pode especificar a função, a capacidade necessária e como essa capacidade é distribuída. Para o requisito de recurso, pode especificar atributos que estão associados ao recurso genérico. Estes atributos incluem as competências necessárias, a unidade organizacional preferencial e os recursos preferenciais.

Conclua os passos seguintes para especificar as competências necessárias num recurso genérico para um programador.

1. No formulário **Projetos**, no separador **Equipa**, selecione **Novo** para reservar um recurso genérico.
2. Na vista **Todos os Membros da Equipa**, na coluna **Requisito de Recurso**, selecione a ligação para adicionar as competências necessárias para o recurso genérico.
3. No formulário **Requisito de Recurso** apresentado, na grelha **Competências**, selecione as reticências (**...**) e, em seguida, selecione **Adicionar Nova Característica de Requisito** para adicionar as competências necessárias para o programador.
4. Na caixa de diálogo **Criação Rápida: Característica de Requisito**, no campo **Característica**, selecione a competência necessária.
5. No campo **Valor de classificação**, selecione o nível de proficiência para essa competência. 
6. No campo **Requisito de Recurso**, defina o requisito como os recursos de origem a partir de unidades organizacionais ou até mesmo de recursos nomeados. Quando tiver terminado, selecione **Guardar**.
7. No formulário **Requisito de Recurso**, selecione **Reservar** para cumprir o requisito de recurso. Também pode selecionar o recurso genérico na grelha **Todos os Membros da Equipa** e, em seguida, selecione **Reservar**.

    > [!NOTE]
    > Neste exemplo, existem 40 horas necessárias, mas não existem horas reservadas reais, porque os recursos genéricos não têm reservas. Além disso, não existem horas atribuídas, porque o recurso genérico foi adicionado diretamente à equipa, em vez de ser adicionado através da atribuição de tarefas.

    No formulário **Assistente de Agendamento**, pode filtrar os recursos disponíveis de acordo com os requisitos especificados no requisito de recurso. Os recursos são ordenados de acordo com os parâmetros de ordenação especificados no Quadro da Agenda.

   Alguns dos filtros mais utilizados são:

    - **Características juntamente com uma classificação**: filtrar por competências, certificações e outras qualidades de recursos, para além das classificações de proficiência.
    - **Funções**: filtrar pelas funções predefinidas atribuídas aos recursos reserváveis.
    - **Unidades organizacionais**: filtrar recursos reserváveis pelas unidades organizacionais às quais estão atribuídos.

8. Se não estiver satisfeito com os resultados da pesquisa inicial de requisitos, pode alterar os critérios de filtro. Expanda o painel **Vista de Filtro** à esquerda e, em seguida, selecione **Pesquisar** para localizar recursos adicionais. Para alterar a forma como os resultados são ordenados, selecione **Ordenar**.
9. Selecione recursos de acordo com a procura especificada no requisito, conforme indicado na parte superior da grelha. Pode limpar a seleção de células na grelha e deixar a capacidade do recurso aberta. Só é possível selecionar um recurso de cada vez como está reservado.
10. Selecione **Reservar** para reservar o recurso selecionado e deixar o Quadro da Agenda aberto, para que possa selecionar recursos adicionais. Em alternativa, selecione **Reservar e Sair** para reservar o recurso selecionado e fechar o Quadro da Agenda.
11. Volte à vista **Todos os Membros da Equipa**. Na grelha, note que o recurso genérico foi substituído pelo recurso nomeado e as 40 horas estão listadas como reservadas para esse recurso.

    > [!NOTE]
    > Não são apresentadas as horas atribuídas, porque estavam reservadas diretamente na equipa. Não foram reservadas através da atribuição de tarefas.

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a>Atribuir recursos genéricos a tarefas e gerar requisitos de recursos

No Project Operations, é possível criar tarefas e, em seguida, atribuir-lhes recursos genéricos. Em seguida, a Procura de recursos recursos pode ser representada por marcadores de posição enquanto estima a agenda e os números financeiros. Em seguida, pode gerar requisitos de recursos para os recursos genéricos e cumpri-los.

1. No formulário **Projetos**, no separador **Agenda**, selecione **Adicionar** para criar uma tarefa.
2. No campo **Recursos**, selecione o símbolo **Seletor de Recursos**. O Seletor de Recursos é apresentado e mostra os membros da equipa existentes para o projeto.
3. Introduza o nome do novo recurso genérico e, em seguida, selecione **Criar**.
4. Na caixa de diálogo **Criação Rápida: Membro da Equipa do Projeto** que é apresentada, no campo **Função**, selecione a função para o recurso genérico. 
5. No campo **Unidade de Atribuição de Recursos**, selecione a unidade organizacional para o recurso genérico. Em seguida, selecione **Guardar**. Agora, o membro da equipa genérico está atribuído à tarefa.

   No separador **Equipa**, verá o novo membro da equipa genérico. Tenha em atenção que apenas tem horas atribuídas. Estas horas são a soma de todas as tarefas que estão atribuídas ao membro da equipa genérico. O membro da equipa genérico ainda não tem horas ou um requisito de recurso necessário.

6. Agora, pode atribuir o membro da equipa genérico a outras tarefas utilizando o Seletor de Recursos.

   Quando tiver terminado a atribuição do recurso genérico às tarefas, poderá gerar um requisito de recurso para o recurso genérico.

7. No separador **Equipa**, selecione o recurso genérico e, em seguida, selecione **Gerar Requisito**. Quando o requisito for gerado, o membro da equipa genérico terá as horas necessárias e uma ligação para o requisito de recurso.

  Depois de reservar um recurso nomeado, o recurso genérico é removido da equipa e é substituído pelo recurso nomeado. No separador **Agenda**, as atribuições de recursos genéricos são removidas e substituídas pelo recurso nomeado.

  > [!NOTE]
  > Este comportamento só ocorre quando um recurso nomeado é totalmente reservado para o requisito de recurso genérico. Quando um recurso nomeado substitui parcialmente o requisito de recurso genérico ou os vários recursos nomeados substituem o requisito de recurso genérico, o recurso genérico permanece atribuído à tarefa.

O Project Operations não atribui ambos os recursos à tarefa, pois esse comportamento produziria uma agenda menos previsível. Neste exemplo simples, é fácil dividir as horas igualmente entre dois recursos. No entanto, em cenários mais complexos que envolvam várias tarefas e vários recursos, o PSA teria de dar suposições sobre como deve alocar as reservas que são recebidas para vários recursos em várias tarefas.

Consequentemente, nestes cenários, o Gestor de projeto é responsável pela análise de várias reservas e pela atribuição das mesmas, conforme necessário. Para alocar as reservas, o Gestor de projeto atribui as tarefas dos recursos genéricos aos recursos nomeados e, em seguida, utiliza a vista **Reconciliação** para garantir que a alocação funciona com as reservas.

### <a name="edit-a-resource-requirement"></a>Editar um requisito de recurso

Depois de criar um requisito de recurso, um Gestor de projeto ou um Gestor de recursos poderá pretender editar os detalhes para refinar os critérios de pesquisa quando o Quadro da Agenda for utilizado. Para editar o requisito de recurso, siga estes passos.

1. No formulário **Projetos**, no separador **Equipa**, selecione a ligação para qualquer requisito num recurso genérico.
2. No formulário **Requisito de Recurso** que aparece, introduza as informações necessárias no campo

   No formulário **Requisito de Recurso**, o Gestor de projeto ou o Gestor de recursos também pode definir as competências, as funções, as preferências de recursos e a unidade organizacional preferida.

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a>Atualizar as reservas de recursos depois de estarem reservados num projeto

Depois de ter adicionado um recurso genérico ou nomeado a uma equipa do projeto, pode alterar as reservas do recurso.

1. No formulário **Projetos**, no separador **Equipa**, selecione um membro da equipa e, em seguida, selecione **Manter Reservas**.
 
   O Quadro da Agenda é apresentado e mostra as reservas do membro da equipa do projeto. Expanda o registo do membro da equipa para ver as horas que foram reservadas para este projeto e outros projetos que estão a consumir a capacidade do membro da equipa.

2. Selecione e arraste a reserva para expandir ou reduzir o seu tamanho. É apresentada a caixa de diálogo **Criar Reserva de Recursos** que lhe permite ajustar a reserva.
3. Clique com o botão direito do rato na reserva. Em seguida, pode utilizar o menu de atalho para concluir as seguintes ações:

    - Alterar o estado da reserva
    - Editar a reserva
    - Substituir um recurso na equipa do projeto

### <a name="change-the-booking-status"></a>Alterar o estado da reserva

Pode alterar qualquer estado da reserva predefinido ou personalizado.

Os seguintes estados estão incluídos no Project Operations:

- **Cancelado**: cancela a reserva de um recurso e liberta a capacidade do recurso.
- **Reserva Fixa**: consome a capacidade de um recurso. Normalmente, uma reserva tem este estado quando abre **Manter Reservas** a partir da grelha **Todos os Membros da Equipa** no formulário **Projetos**.
- **Reserva Flexível**: adiciona um recurso a uma equipa, mas não consome a capacidade do recurso. Este estado indica que o recurso foi reservado para trabalho potencial, mas ainda tem capacidade se for necessário em outras tarefas. Na vista da disponibilidade geral do recurso, as reservas flexíveis têm um estado diferente das reservas fixas.
- **Proposto**: representa a proposta de um Gestor de recursos ou Gestor de projeto para um recurso. As propostas não consomem a capacidade de um recurso e o recurso não é adicionado à equipa do projeto. Para efetuar a reserva fixa do recurso na equipa, o Gestor de projeto tem de aceitar a proposta.

### <a name="submit-resource-requests"></a>Submeter pedidos de recurso

Os pedidos de recursos são utilizados para transportar a procura, ou requisito de recurso, que tem de ser cumprida por um Gestor de recursos. No caso de um recurso genérico que já esteja na equipa, pode submeter diretamente um pedido de recurso. Um pedido de recurso pode ser cumprido de duas formas:

- O Gestor de recursos cumpre diretamente o pedido. Neste caso, o recurso genérico é substituído por uma reserva fixa que tem um recurso nomeado.
- O Gestor de recursos propõe um recurso ao Gestor de projeto e o Gestor de projeto aprova ou rejeita o recurso proposto.

#### <a name="direct-fulfillment-of-resource-requests"></a>Cumprimento direto de pedidos de recursos

Quando um requisito de recurso é gerado, um Gestor de projeto pode submeter um pedido de recurso para um recurso genérico selecionando o recurso e, em seguida, selecionando **Submeter Pedido**. Os comentários sobre o recurso podem ser fornecidos ao Gestor de recursos que está a cumprir o pedido. Depois de o pedido ser submetido, o campo **Estado** para o membro da equipa é alterado para **Submetido**. Quando o Gestor de recursos cumpre o pedido, o membro da equipa genérico é substituído pelo recurso nomeado na grelha **Todos os Membros da Equipa**.

#### <a name="use-a-resource-proposal-for-resource-requests"></a>Utilizar uma proposta de recursos para pedidos de recursos

Em vez de reservar diretamente um recurso num pedido de recurso, um Gestor de recursos pode propor um recurso ao Gestor de projeto. Um Gestor de recursos poderá utilizar esta opção quando não estiver disponível uma correspondência exata para os requisitos. Quando um Gestor de recursos propõe um recurso, o Gestor de projeto vê que o campo **Estado** do membro da equipa genérico é alterado para **Necessita de Revisão**.

Pode ver o recurso proposto juntamente com uma visualização do efeito da reserva da proposta. 

1. Faça duplo clique no membro da equipa que tem o estado **Necessita de Revisão**. 
2. Selecione o separador **Recursos Propostos**.
3. Selecione **Aceitar Todas as Propostas** para aceitar todos os recursos propostos ou **Rejeitar Todas as Propostas** para rejeitá-los. Se aceitar os recursos propostos, estes serão reservados de forma fixa no projeto como membros da equipa e substituem os recursos genéricos.

> [!NOTE]
> Tem de aceitar ou rejeitar todos os recursos propostos. Não é possível aceitá-los ou rejeitá-los parcialmente.

### <a name="substitute-a-resource-on-the-project-team"></a>Substituir um recurso na equipa do projeto

Por vezes, um Gestor de projeto tem de substituir um membro da equipa reservado num projeto.

1. No formulário **Projetos**, no separador **Equipa**, selecione o recurso que necessita de um substituto e, em seguida, selecione **Manter Reservas**.
2. Expanda o recurso para ver os projetos aos quais está atribuído.
3. Clique com o botão direito do rato no projeto e selecione **Substituir Recurso**.
4. Se souber o recurso que pretende substituir pelo recurso atual, selecione ou escreva o nome e, em seguida, selecione **Reatribuir**.

Ou, se precisar de procurar um recurso, conclua os seguintes passos.

1. Selecione **Localizar Substituição**.

   O Assistente da Agenda devolve uma lista de substitutos disponíveis. No Assistente da Agenda, pode filtrar ainda mais os recursos disponíveis para localizar um substituto adequado.

2. Para substituir o recurso, selecione o recurso pretendido e, em seguida, selecione **Substituir**.   

   As reservas e as atribuições são substituídas pelo novo recurso.

## <a name="reconcile-team-member-bookings-and-assignments"></a>Reconciliar reservas e atribuições de membros da equipa

Quanto aos membros da equipa, as reservas e as atribuições têm uma ligação fraca. Por outras palavras, os recursos podem ter atribuições, mas não reservas, ou podem ter reservas, mas não atribuições. Idealmente, as reservas e atribuições devem ser alinhadas, para que os recursos tenham capacidade comprometida para executar as atribuições de tarefas. No entanto, as reservas podem basear-se na disponibilidade e as temporizações das tarefas podem mudar à medida que o projeto continua. Portanto, a ligação fraca de reservas e atribuições fornece flexibilidade.

O Project Operations tem um separador **Reconciliação** que permite que os Gestores de projeto reconciliar as reservas de membros da equipa e as respetivas atribuições para as equipas do projeto.

O separador **Reconciliação** mostra as reservas e as atribuições até ao nível da atribuição de tarefas individuais para cada membro da equipa. Mostra horas nas células que representam períodos de meses a dias.

O separador também mostra um total líquido global para o projeto, juntamente com uma coluna total.

Para cada recurso, o separador calcula a diferença entre as reservas do membro da equipa e um rollup das atribuições de tarefas do membro da equipa. O ideal é que esta diferença seja 0 (zero). Por outras palavras, não deve haver diferença entre as reservas e as atribuições. As diferenças são coloridas e sombreadas para chamar a atenção para duas condições:

- **Falta de reserva**: ocorre quando um recurso tem mais atribuições do que reservas. Como essa capacidade não foi reservada, um Gestor de projeto pode querer corrigir esta condição, expandindo as reservas do recurso para cobrir o deficit.
- **Reservas em excesso**: ocorre quando um recurso foi reservado para o projeto, mas ainda não foi atribuído às tarefas. Esta condição poderá ser aceitável nos casos em que o recurso esteve reservado para o projeto antes da atribuição de tarefas. No entanto, em outros casos, o recurso não está planeado para ser atribuído a tarefas. Nestes casos, o Gestor de projeto deverá considerar o cancelamento das reservas do recurso, para que a capacidade possa ser utilizada para outro projeto.

Em alguns casos, quando visualiza o tempo num nível superior a nível do dia, por exemplo, o nível de mês, poderá ver uma diferença líquida de zero para um recurso. Por outras palavras, reservas = atribuições. No entanto, se visualizar o tempo no nível da semana, poderá ver que existem atribuições de zero horas e reservas de 40 horas na primeira semana, mas atribuições de 40 horas e reservas de zero horas na segunda semana. Globalmente, as reservas e as atribuições são reconciliadas, mas diferem de uma semana para a seguinte.

Quando visualiza o tempo em níveis superiores, as células no separador **Reconciliação** têm um indicador para informá-lo de que existem diferenças em níveis inferiores. Faça duplo clique numa célula para ampliar e ver a diferença. Em seguida, pode clicar com o botão direito do rato para reduzir. Ao selecionar um recurso e, em seguida, selecionar **Diferença seguinte** na barra de ferramentas de grelha, pode ir para a próxima diferença entre as reservas e as atribuições para esse recurso. Selecione **Diferença anterior** para retroceder. Também pode desativar o indicador de diferença e o comportamento de navegação em **Definições**.

Se tiver atribuições de tarefas para um recurso, mas não tiver reservas, no formulário **Projetos**, no separador **Reconciliação**, selecione a falta de reserva e, em seguida, selecione **Expandir Reserva**. É apresentada a caixa de diálogo **Falta de Reserva** e mostra a reserva necessária para resolver a falta do recurso. A caixa de diálogo também mostra as reservas existentes do recurso em todos os projetos ou outras entidades agendáveis. Se selecionar **OK** para criar a reserva para o recurso, independentemente da disponibilidade do recurso, poderá causar uma reserva em excesso.

Em seguida, o Gestor de projeto ou o Gestor de recursos pode utilizar o Quadro da Agenda para gerir qualquer situação em que um recurso tenha uma reserva em excesso além da sua capacidade.
