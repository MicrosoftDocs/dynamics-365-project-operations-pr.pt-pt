---
title: Gerir recursos
description: Este tópico fornece informações sobre como pode gerir recursos.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/13/2019
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
ms.openlocfilehash: 548595e3951f824e1c79a641d3f336e381fcaaf9
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4132347"
---
# <a name="manage-resources"></a>Gerir recursos

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

O Dynamics 365 Project Service Automation inclui um dashboard do gestor de recursos que fornece uma descrição geral visual da procura e utilização de recursos em toda a organização. Pode utilizar os gráficos neste dashboard para visualizar as seguintes informações:

- **Procura de recursos** – O gráfico **Pedido de Recursos Ativos** mostra os recursos que foram submetidos. Os recursos são agregados por uma função ou projeto.
- **Procura de recursos não submetidos** – O gráfico **Procura de Recursos Não Atribuídos** mostra todos os requisitos de recursos que não foram submetidos. Ajuda os gestores de recursos a visualizarem a procura que não é firme e que pode ser submetida através de um pedido de recurso.
- **Utilização faturável para a semana passada** – O gráfico **Utilização por Função** mostra a percentagem da utilização faturável real da organização por função relativamente à sua utilização faturável de destino por função.

    > [!NOTE]
    > Para disponibilizar o gráfico **Utilização por Função**, crie uma tarefa que execute o fluxo de trabalho UpdateRoleUtilization Esta tarefa periódica é executada a cada sete dias para calcular a utilização faturável nos sete dias anteriores. Os resultados são agregados por função.

## <a name="manage-project-team-members"></a>Gerir membros da equipa do projeto

Os gestores de projeto podem utilizar o dashboard do gestor de recursos para gerir os recursos nos projetos. Por exemplo, podem adicionar um membro da equipa diretamente a um projeto e reservar um membro da equipa para cumprir os requisitos de recursos que foram capturados por um recurso genérico.

### <a name="add-a-team-member-directly-to-a-project"></a>Adicionar um membro da equipa diretamente a um projeto

Para adicionar um membro da equipa diretamente a um projeto, na página **Projetos**, no separador **Equipa**, selecione **Novo**. É apresentada a caixa de diálogo **Criação Rápida: Membro da Equipa do Projeto**. Nesta caixa de diálogo, pode efetuar estas tarefas:

- **Reservar um recurso nomeado** – No campo **Recurso Reservável**, selecione o nome do recurso. Em seguida, selecione a função, defina o período e selecione um método de alocação. O recurso nomeado que selecionou é adicionado ao projeto utilizando o método de alocação selecionado e o calendário de recursos.
- **Adicionar um recurso genérico** – Deixe o campo **Recurso reservável** em branco e, em seguida, selecione a função, defina o período e selecione o método de alocação preferencial. Um recurso genérico é adicionado à equipa como um marcador de posição para manter o padrão de procura utilizado para reservar recursos nomeados na equipa. O requisito é efetuado de acordo com o calendário do projeto.
- **Adicionar um recurso nomeado à equipa sem consumir capacidade do recurso** – No campo **Recurso Reservável**, selecione um recurso. Em seguida, selecione o período e selecione **Nenhum** o método de alocação. O recurso é adicionado à equipa, mas a capacidade do recurso não é consumida através de uma reserva.

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a>Reservar um membro da equipa para cumprir os requisitos de recursos para um recurso genérico

No PSA, pode reservar um recurso genérico numa equipa do projeto e pode especificar a função, a capacidade necessária e a forma como essa capacidade é distribuída. No requisito de recurso, pode especificar atributos que estão associados ao recurso genérico. Estes atributos incluem as competências necessárias, a unidade organizacional preferencial e os recursos preferenciais.

Siga estes passos para especificar as competências necessárias num recurso genérico para um programador.

1. Na página **Projetos**, no separador **Equipa**, selecione **Novo** para reservar um recurso genérico.

    ![Recurso genérico reservado na equipa](media/Resource-Management-image9.png)

2. Na vista **Todos os Membros da Equipa**, na coluna **Requisito de Recurso**, selecione a ligação para adicionar as competências necessárias para o recurso genérico.

    ![Ligação de requisitos](media/Resource-Management-image10.png)

3. Na página **Requisito de Recurso** que é apresentada, na grelha **Competências**, selecione as reticências (**...**) e, em seguida, selecione **Adicionar Nova Característica de Requisito** para adicionar as competências necessárias para o programador.

    ![Comando Adicionar Nova Característica de Requisito](media/Resource-Management-image11.png)

4. Na caixa de diálogo **Criação Rápida: Característica de Requisito** que é apresentada, no campo **Característica**, selecione a competência necessária. Em seguida, no campo **Valor de classificação**, selecione o nível de proficiência para essa competência. Por fim, no campo **Requisito de Recurso**, defina o requisito como os recursos de origem a partir de unidades organizacionais ou até mesmo de recursos nomeados. Quando tiver terminado, selecione **Guardar**.

    ![Caixa de diálogo Criação Rápida: Característica de Requisito](media/Resource-Management-image12.png)

5. Na página **Requisito de Recurso**, selecione **Reservar** para cumprir o requisito de recurso.

    ![Botão Reservar na página Requisito de Recurso](media/Resource-Management-image13.png)

    Também pode selecionar o recurso genérico na grelha **Todos os Membros da Equipa** e, em seguida, selecione **Reservar**.

    ![Botão Reservar acima da grelha Todos os Membros da Equipa](media/Resource-Management-image14.png)

    > [!NOTE]
    > Neste exemplo, existem 40 horas necessárias, mas não existem horas reservadas reais, porque os recursos genéricos não têm reservas. Além disso, não existem horas atribuídas, porque o recurso genérico foi adicionado diretamente à equipa. O mesmo não foi adicionado através da atribuição de tarefas.

    Na página **Assistente de Agendamento**, pode filtrar os recursos disponíveis de acordo com os requisitos especificados no requisito de recurso. Os recursos são ordenados de acordo com os parâmetros de ordenação especificados no Quadro da Agenda.

    ![Página Assistente de Agendamento](media/Resource-Management-image15.png)

    Seguem-se alguns filtros que são frequentemente utilizados:

    - **Características juntamente com uma classificação** – Filtrar por competências, certificações e outras qualidades de recursos, para além das classificações de proficiência.
    - **Funções** – Filtrar pelas funções predefinidas atribuídas aos recursos reserváveis.
    - **Unidades organizacionais** – Filtrar recursos reserváveis pelas unidades organizacionais às quais estão atribuídos.

6. Se não estiver satisfeito com os resultados da pesquisa inicial de requisitos, pode alterar os critérios de filtro. Expanda o painel **Vista de Filtro** à esquerda e, em seguida, selecione **Pesquisar** para localizar recursos adicionais.

    ![Painel Vista de Filtro](media/Resource-Management-image16.png)

7. Para alterar a forma como os resultados são ordenados, selecione **Ordenar**.

    ![Comando Ordenar](media/Resource-Management-image17.png)

8. Selecione recursos de acordo com a procura especificada no requisito, conforme indicado na parte superior da grelha. Pode limpar a seleção de células na grelha e deixar a capacidade do recurso aberta. Só é possível selecionar um recurso de cada vez como está reservado.

9. Selecione **Reservar** para reservar o recurso selecionado e deixar o Quadro da Agenda aberto, para que possa selecionar recursos adicionais. Em alternativa, selecione **Reservar e Sair** para reservar o recurso selecionado e fechar o Quadro da Agenda.

    ![Recurso a reservar](media/Resource-Management-image19.png)

    Recebe uma notificação sobre as horas reservadas. Os indicadores de procura mostram a quantidade de tempo de reserva satisfeita e a quantidade de tempo restante. Também pode ver a quantidade de capacidade do recurso selecionada que é consumida. Selecione **Expandir** para ver mais detalhes sobre as reservas de recursos.

9. Volte à vista **Todos os Membros da Equipa**. Na grelha, note que o recurso genérico foi substituído pelo recurso nomeado e as 40 horas estão listadas como reservadas para esse recurso.

    ![Grelha Todos os Membros da Equipa atualizada](media/Resource-Management-image20.png)

    > [!NOTE]
    > Não são apresentadas as horas atribuídas, porque estavam reservadas diretamente na equipa. Não foram reservadas através da atribuição de tarefas.

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a>Atribuir recursos genéricos a tarefas e gerar requisitos de recursos

No PSA, é possível criar tarefas e, em seguida, atribuir-lhes recursos genéricos. Desta forma, a procura de recursos pode ser representada por marcadores de posição enquanto estima a agenda e os números financeiros. Em seguida, pode gerar requisitos de recursos para os recursos genéricos e cumpri-los.

1. Na página **Projetos**, no separador **Agenda**, selecione **Adicionar** para criar uma tarefa.

    ![Nova tarefa criada](media/Resource-Management-image21.png)

2. No campo **Recursos**, selecione o símbolo **Seletor de Recursos**. O Seletor de Recursos é apresentado e mostra os membros da equipa existentes para o projeto.

    ![Seletor de Recursos](media/Resource-Management-image22.png)

3. Introduza o nome do novo recurso genérico e, em seguida, selecione **Criar**.

    ![Nome de um novo recurso genérico introduzido](media/Resource-Management-image23.png)

4. Na caixa de diálogo **Criação Rápida: Membro da Equipa do Projeto** que é apresentada, no campo **Função**, selecione a função para o recurso genérico. No campo **Unidade de Atribuição de Recursos**, selecione a unidade organizacional para o recurso genérico. Em seguida, selecione **Guardar**.

    ![Caixa de diálogo Criação Rápida: Membro da Equipa do Projeto](media/Resource-Management-image24.png)

    Agora, o membro da equipa genérico está atribuído à tarefa.

    ![Membro da equipa genérico atribuído à tarefa](media/Resource-Management-image25.png)

    No separador **Equipa**, verá o novo membro da equipa genérico. Tenha em atenção que apenas tem horas atribuídas. Estas horas são a soma de todas as tarefas que estão atribuídas ao membro da equipa genérico. O membro da equipa genérico ainda não tem horas ou um requisito de recurso necessário.

    ![Membro da equipa genérico no separador Equipa](media/Resource-Management-image26.png)

5. Agora, pode atribuir o membro da equipa genérico a outras tarefas utilizando o Seletor de Recursos.

    ![Membro da equipa genérico no Seletor de Recursos](media/Resource-Management-image27.png)

    Quando tiver terminado a atribuição do recurso genérico às tarefas, poderá gerar um requisito de recurso para o recurso genérico.

5. No separador **Equipa**, selecione o recurso genérico e, em seguida, selecione **Gerar Requisito**.

    ![Comando Gerar Requisito](media/Resource-Management-image28.png)

    Quando o requisito for gerado, o membro da equipa genérico terá as horas necessárias e uma ligação para o requisito de recurso.

    ![Ligação Requisito de recurso](media/Resource-Management-image29.png)

    Depois de reservar um recurso nomeado, o recurso genérico é removido da equipa e é substituído pelo recurso nomeado.

    ![Recurso genérico substituído pelo recurso nomeado](media/Resource-Management-image30.png)

    No separador **Agenda**, as atribuições de recursos genéricos são removidas e substituídas pelo recurso nomeado.

    ![Atribuições de recursos genéricos substituídas pelo recurso nomeado no separador Agenda](media/Resource-Management-image31.png)

    > [!NOTE]
    > Este comportamento só ocorre quando um recurso nomeado é totalmente reservado para o requisito de recurso genérico. Quando um recurso nomeado substitui parcialmente o requisito de recurso genérico ou os vários recursos nomeados substituem o requisito de recurso genérico, o recurso genérico permanece atribuído à tarefa.

    Na ilustração seguinte, foi planeada uma tarefa de 80 horas para uma duração de cinco dias (16 horas por dia durante cinco dias) e atribuída ao recurso genérico com o nome **Funcional**.

    ![Tarefa de oitenta horas e cinco dias atribuída ao recurso genérico Funcional](media/Resource-Management-image32.png)

    Quando gera o requisito, dura 80 horas em cinco dias.

    ![Requisito gerado durante 80 horas durante cinco dias](media/Resource-Management-image33.png)

    Visto que os recursos disponíveis só funcionam oito horas por dia, são necessários dois recursos para cumprir o requisito.

    ![Segundo recurso](media/Resource-Management-image35.png)

    No separador **Equipa**, pode ver que o recurso genérico não tem horas necessárias, mas as horas atribuídas continuam a aparecer juntamente com os dois recursos nomeados que compõem o cumprimento.

    ![Dois recursos nomeados no separador Equipa](media/Resource-Management-image36.png)

    No separador **Agenda**, o recurso genérico permanece atribuído à tarefa.

    ![Recursos genéricos no separador Agenda](media/Resource-Management-image37.png)

O PSA não atribui ambos os recursos à tarefa, pois esse comportamento produziria uma agenda menos previsível. Neste exemplo simples, é fácil dividir as horas igualmente entre dois recursos. No entanto, em cenários mais complexos que envolvam várias tarefas e vários recursos, o PSA teria de dar suposições sobre como deve alocar as reservas que são recebidas para vários recursos em várias tarefas.

Consequentemente, nestes cenários, o gestor de projeto é responsável pela análise de várias reservas e pela atribuição das mesmas, conforme necessário. Para alocar as reservas, o gestor de projeto atribui as tarefas dos recursos genéricos aos recursos nomeados e, em seguida, utiliza a vista **Reconciliação** para garantir que a alocação funciona com as reservas.

### <a name="edit-a-resource-requirement"></a>Editar um requisito de recurso

Depois de criar um requisito de recurso, um gestor de projeto ou um gestor de recursos poderá pretender editar os detalhes para refinar os critérios de pesquisa quando o Quadro da Agenda for utilizado. Para editar o requisito de recurso, siga estes passos.

1. Na página **Projetos**, no separador **Equipa**, selecione a ligação para qualquer requisito num recurso genérico.
2. Na página **Requisito de Recurso** que aparece, pode atualizar vários atributos. Seguem-se alguns exemplos:

    - Nome
    - Da Data
    - À Data
    - Duração
    - Tipo de Recurso

Na página **Requisito de Recurso**, o gestor de projeto ou o gestor de recursos também podem definir as seguintes informações:

- Competências
- Funções
- Preferências de recurso
- Unidade organizacional preferencial

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a>Atualizar as reservas de recursos depois de estarem reservados num projeto

Depois de ter adicionado um recurso genérico ou nomeado a uma equipa do projeto, pode alterar as reservas do recurso.

1. Na página **Projetos**, no separador **Equipa**, selecione um membro da equipa e, em seguida, selecione **Manter Reservas**.

    ![Quadro da Agenda aberto para o membro da equipa selecionado](media/Resource-Management-image40.png)

    O Quadro da Agenda é apresentado e mostra as reservas do membro da equipa do projeto. Expanda o registo do membro da equipa para ver as horas que foram reservadas para este projeto e outros projetos que estão a consumir a capacidade do membro da equipa.

2. Selecione e arraste a reserva para expandir ou reduzir o seu tamanho. É apresentada a caixa de diálogo **Criar Reserva de Recursos** que lhe permite ajustar a reserva.

    ![Caixa de diálogo Criar Reserva de Recursos](media/Resource-Management-image41.png)

3. Clique com o botão direito do rato na reserva. Em seguida, pode utilizar o menu de atalho para concluir as seguintes ações:

    - Altere o estado da reserva.
    - Edite a reserva.
    - Substitua um recurso na equipa do projeto.

### <a name="change-the-booking-status"></a>Alterar o estado da reserva

Pode alterar qualquer estado da reserva predefinido ou personalizado.

![Comando Alterar Estado](media/Resource-Management-image42.png)

Os seguintes estados estão incluídos no PSA:

- **Cancelado** – Este estado cancela a reserva de um recurso e liberta a capacidade do recurso.
- **Reserva Fixa** – Este estado consome a capacidade de um recurso. Normalmente, uma reserva tem este estado quando abre **Manter Reservas** a partir da grelha **Todos os Membros da Equipa** na página **Projetos**.
- **Reserva Flexível** – Este estado adiciona um recurso a uma equipa, mas não consome a capacidade do recurso. Indica que o recurso foi reservado para trabalho potencial, mas ainda tem capacidade se for necessário em outras tarefas. Na vista da disponibilidade geral do recurso, as reservas flexíveis têm um estado diferente das reservas fixas.
- **Proposto** – Este estado representa a proposta do gestor de recursos ou do gestor de projeto para um recurso. As propostas não consomem a capacidade de um recurso e o recurso não é adicionado à equipa do projeto. Para efetuar a reserva fixa do recurso na equipa, o gestor de projeto tem de aceitar a proposta.

### <a name="submit-resource-requests"></a>Submeter pedidos de recursos

Os pedidos de recursos são utilizados para transportar a procura (requisito de recurso) que tem de ser cumprida por um gestor de recursos. No caso de um recurso genérico que já esteja na equipa, pode submeter diretamente um pedido de recurso. Um pedido de recurso pode ser cumprido de duas formas:

- O gestor de recursos cumpre diretamente o pedido. Neste caso, o recurso genérico é substituído por uma reserva fixa que tem um recurso nomeado.
- O gestor de recursos propõe um recurso ao gestor de projeto e o gestor de projeto aprova ou rejeita o recurso proposto.

#### <a name="direct-fulfillment-of-resource-requests"></a>Cumprimento direto de pedidos de recursos

Quando um requisito de recurso é gerado, um gestor de projeto pode submeter um pedido de recurso para um recurso genérico selecionando o recurso e, em seguida, selecionando **Submeter Pedido**.

![Botão Submeter Pedido](media/Resource-Management-image45.png)

Os comentários sobre o recurso podem ser fornecidos ao gestor de recursos que está a cumprir o pedido. Depois de o pedido ser submetido, o campo **Estado** para o membro da equipa é alterado para **Submetido**.

![Introduzir comentários opcionais](media/Resource-Management-image46.png)

Quando o gestor de recursos cumpre o pedido, o membro da equipa genérico é substituído pelo recurso nomeado na grelha **Todos os Membros da Equipa**.

![Membro da equipa genérico substituído pelo recurso nomeado na grelha Todos os Membros da Equipa](media/Resource-Management-image47.png)

#### <a name="use-a-resource-proposal-for-resource-requests"></a>Utilizar uma proposta de recursos para pedidos de recursos

Em vez de reservar diretamente um recurso num pedido de recurso, um gestor de recursos pode propor um recurso ao gestor de projeto. Um gestor de recursos poderá utilizar esta opção quando não estiver disponível uma correspondência exata para os requisitos. Quando um gestor de recursos propõe um recurso, o gestor de projeto vê que o campo **Estado** do membro da equipa genérico é alterado para **Necessita de Revisão**.

![Estado do membro da equipa genérico alterado para Necessita de Revisão](media/Resource-Management-image48.png)

Para ver o recurso proposto juntamente com uma visualização do efeito da reserva da proposta, faça duplo clique no membro da equipa que tem o estado **Necessita de Revisão**. Em seguida, selecione o separador **Recursos Propostos**.

![Separador Recursos Propostos](media/Resource-Management-image49.png)

Selecione **Aceitar Todas as Propostas** para aceitar todos os recursos propostos ou **Rejeitar Todas as Propostas** para rejeitá-los. Se aceitar os recursos propostos, estes serão reservados de forma fixa no projeto como membros da equipa e substituem os recursos genéricos.

> [!NOTE]
> Tem de aceitar ou rejeitar todos os recursos propostos. Não é possível aceitá-los ou rejeitá-los parcialmente.

### <a name="substitute-a-resource-on-the-project-team"></a>Substituir um recurso na equipa do projeto

Por vezes, um gestor de projeto tem de substituir um membro da equipa reservado num projeto.

1. Na página **Projetos**, no separador **Equipa**, selecione o recurso que necessita de um substituto e, em seguida, selecione **Manter Reservas**.
2. Expanda o recurso para ver os projetos aos quais está atribuído.

    ![Recurso expandido para mostrar os projetos atribuídos](media/Resource-Management-image50.png)

3. Clique com o botão direito do rato no projeto e selecione **Substituir Recurso**.
4. Se souber o recurso que pretende substituir pelo recurso atual, selecione ou escreva o nome e, em seguida, selecione **Reatribuir**.

    ![Especificar um recurso substituto](media/Resource-Management-image51.png)

    Em alternativa, siga estes passos para procurar um recurso:

    1. Selecione **Localizar Substituição**.

        ![Procurar um recurso substituto](media/Resource-Management-image52.png)

        O Assistente da Agenda devolve uma lista de substitutos disponíveis. No Assistente da Agenda, pode filtrar ainda mais os recursos disponíveis para localizar um substituto adequado.

        ![Lista de substitutos disponíveis](media/Resource-Management-image53.png)

    2. Para substituir o recurso, selecione o recurso pretendido e, em seguida, selecione **Substituir**.

        ![Recurso substituto selecionado](media/Resource-Management-image54.png)

    As reservas e as atribuições são substituídas pelo novo recurso.

    ![Reservas e atribuições substituídas pelo novo recurso](media/Resource-Management-image55.png)

## <a name="reconcile-team-member-bookings-and-assignments"></a>Reconciliar reservas e atribuições de membros da equipa

Quanto aos membros da equipa, as reservas e as atribuições têm uma ligação fraca. Por outras palavras, os recursos podem ter atribuições, mas não reservas, ou podem ter reservas, mas não atribuições. Idealmente, as reservas e atribuições devem ser alinhadas, para que os recursos tenham capacidade comprometida para executar as atribuições de tarefas. No entanto, as reservas podem basear-se na disponibilidade e as temporizações das tarefas podem mudar à medida que o projeto continua. Portanto, a ligação fraca de reservas e atribuições fornece flexibilidade.

O PSA tem um separador **Reconciliação** que permite que os gestores de projeto reconciliem os reservas de membros da equipa e as respetivas atribuições para as equipas do projeto.

![Separador Reconciliação](media/Resource-Management-image56.png)

O separador **Reconciliação** mostra as reservas e as atribuições até ao nível da atribuição de tarefas individuais para cada membro da equipa. Mostra horas nas células que representam períodos de meses a dias.

O separador também mostra um total líquido global para o projeto, juntamente com uma coluna total.

Para cada recurso, o separador calcula a diferença entre as reservas do membro da equipa e um rollup das atribuições de tarefas do membro da equipa. O ideal é que esta diferença seja 0 (zero). Por outras palavras, não deve haver diferença entre as reservas e as atribuições. As diferenças são coloridas e sombreadas para chamar a atenção para duas condições:

- **Falta de reserva** – Uma falta de reserva ocorre quando um recurso tem mais atribuições do que reservas. Como essa capacidade não foi reservada, um gestor de projeto pode querer corrigir esta condição, expandindo as reservas do recurso para cobrir o deficit.
- **Reservas em excesso** – As reservas em excesso ocorrem quando um recurso foi reservado para o projeto, mas ainda não foi atribuído às tarefas. Esta condição poderá ser aceitável nos casos em que o recurso esteve reservado para o projeto antes da atribuição de tarefas. No entanto, em outros casos, o recurso não está planeado para ser atribuído a tarefas. Nestes casos, o gestor de projeto deverá considerar o cancelamento das reservas do recurso, para que a capacidade possa ser utilizada para outro projeto.

Em alguns casos, quando visualiza o tempo num nível superior ao nível do dia (por exemplo, o nível de mês), poderá ver uma diferença líquida de zero para um recurso (por outras palavras, reservas = atribuições). No entanto, se visualizar o tempo no nível da semana, poderá ver que existem atribuições de zero horas e reservas de 40 horas na primeira semana, mas atribuições de 40 horas e reservas de zero horas na segunda semana. Globalmente, as reservas e as atribuições são reconciliadas, mas diferem de uma semana para a seguinte.

Quando visualiza o tempo em níveis superiores, as células no separador **Reconciliação** têm um indicador para informá-lo de que existem diferenças em níveis inferiores. Ao clicar duas vezes numa célula, pode ampliar para ver a diferença. Em seguida, pode clicar com o botão direito do rato para reduzir. Ao selecionar um recurso e, em seguida, utilizar o controlo **Diferença seguinte** na barra de ferramentas de grelha, pode ir para a próxima diferença entre as reservas e as atribuições para esse recurso. Em seguida, pode utilizar o controlo **Diferença anterior** para voltar. Também pode desativar o indicador de diferença e o comportamento de navegação em **Definições**.

![Indicador de diferença](media/Resource-Management-image57.png)

Se tiver atribuições de tarefas para um recurso, mas não tiver reservas, na página **Projetos**, no separador **Reconciliação**, selecione a falta de reserva e, em seguida, selecione **Expandir Reserva**. É apresentada a caixa de diálogo **Falta de Reserva** e mostra a reserva necessária para resolver a falta do recurso. Também mostra as reservas existentes do recurso em todos os projetos ou outras entidades agendáveis. Se selecionar **OK** para criar a reserva para o recurso, independentemente da disponibilidade do recurso, poderá causar uma reserva em excesso.

![Caixa de diálogo Expandir Reserva](media/Resource-Management-image58.png)

Em seguida, o gestor de projeto ou o gestor de recursos pode utilizar o Quadro da Agenda para gerir qualquer situação em que um recurso tenha uma reserva em excesso além da sua capacidade.
