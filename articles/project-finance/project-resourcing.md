---
title: Atribuição de recursos do projeto
description: Este tópico fornece informações sobre a atribuições de recursos do projeto.
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f9352465f83abe19097945dd34eada365cd03b8f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754472"
---
# <a name="project-resourcing"></a>Atribuição de recursos do projeto

[!include [banner](../includes/banner.md)]

Este tópico fornece informações sobre a atribuições de recursos do projeto.

Um desafio para os gestores de projetos e os gestores de recursos durante a fase de planeamento do projeto é a atribuição de recursos, onde têm de determinar e reservar o recurso correto para trabalhar num projeto. No Dynamics 365 Finance, as funcionalidades atribuição de recursos para projetos permitem definir funções que são tratadas como recursos temporários que podem ser reservados para um compromisso específico ou parte de um compromisso. Este tipo de atribuição de recursos permite aos gestores de projetos e aos gestores de recursos executar as seguintes tarefas:

- Definir uma função com as competências necessárias para facilitar a correspondência correspondência de recursos.
- Utilizar funções para definir uma agenda de compromissos inicial que se baseie nos recursos reservados.
- Estimar os custos e determinar um orçamento inicial, baseado nas funções e recursos atribuídos para um projeto.
- Utilizar funções para estimar o número de reservas de recursos que são necessárias para cada compromisso.
- Estimar o número de recursos necessários para todo o ciclo de vida de um projeto.
- Delinear uma estrutura hierárquica do trabalho (WBS) ao utilizar as atribuições de recursos iniciais.

[![Ciclo de vida do projeto](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg)

À medida que o planeamento do projeto avança, os recursos planeados podem ser substituídos por recursos de pessoal. O gestor de projetos também pode retroceder e atualizar as reservas de atribuição de recursos durante qualquer fase do projeto.

## <a name="set-up-project-resources"></a>Configurar recursos do projeto
Tem de configurar um calendário e associá-lo a um empregado ou a um trabalhador. O calendário é utilizado para agendar o projeto e o tempo de trabalho dos recursos que estão reservados para o projeto. Durante a configuração do calendário, os gestores de projetos podem nivelar os recursos como parte da otimização dos recursos. Baseado na agenda do calendário, podem ser colocadas restrições nos recursos. Pode configurar um calendário na página **Calendários**.

Quando configura um trabalhador como um recurso do projeto, pode selecionar entre os trabalhadores que trabalham na empresa para a qual está a configurar recursos. Em alternativa, poderá selecionar trabalhadores de outras empresas na sua organização. Estes trabalhadores são conhecidos como recursos entre empresas.

Os seguintes procedimentos explicam como configurar um trabalhador como recurso de projeto na sua empresa e como configurar um recurso de projeto entre empresas.

### <a name="set-up-a-worker-as-a-project-resource"></a>Configurar um trabalhador como recurso do projeto

1. Na página **Trabalhadores**, na lista **Trabalhadores**, selecione o trabalhador que está a adicionar como recurso do projeto e abra o registo do trabalhador.
2. No Painel de Ação, selecione **Projeto** &gt; **Configurar** &gt; **Configuração do projeto**.
3. Selecione um calendário e, em seguida, feche a página.

Também pode especificar projetos predefinidos para um recurso como um tipo de pré-atribuição. As pré-atribuições podem ser utilizadas quando o gestor de recursos ou o gestor de projetos sabe antecipadamente em que projetos o recurso irá trabalhar. As pré-atribuições também podem basear-se no pedido de um patrocinador ou cliente do projeto. Para pré-atribuir um projeto, na página **Atribuir projetos**, no separador **Projetos**, na lista **Projetos restantes**, selecione o projeto adequado.

### <a name="set-up-an-intercompany-resource"></a>Configurar um recurso entre empresas

Quando configura um trabalhador como um recurso entre empresas, tem de concluir a configuração tanto na empresa prestadora como na empresa tomadora.

**Na empresa prestadora**

1. No Finance, verifique se a empresa prestadora está selecionada e, em seguida, conclua o procedimento na secção anterior: "Configurar um trabalhador como recurso do projeto".
2. Na página **Gestão contabilística entre empresas**, selecione **Novo**.
3. No campo **ID da entidade jurídica**, selecione a empresa prestadora. Preencha os campos restantes conforme adequado e, em seguida, selecione **Guardar**.
4. Na página **Preço de transferência**, selecione **Novo**.
5. No campo **Entidade jurídica tomadora**, selecione a empresa adequada.
6. Para emprestar à empresa tomadora apenas o recurso que criou no início desta secção, no campo **Recurso**, selecione o nome do recurso que criou. Para disponibilizar todos os recursos na empresa prestadora à empresa tomadora, deixe o campo **Recursos** em branco.
7. Na página **Parâmetros da gestão de projetos e contabilística**, no separador **Entre empresas**, defina a opção **Ativar as folhas de horas e o agendamento de recursos entre empresas** para **Sim**.

**Na empresa tomadora**

- Na página **Lista de recursos**, no filtro de pesquisa, insira o nome do recurso que criou para a empresa prestadora para verificar se o nome está incluído na lista de recursos da empresa tomadora.

## <a name="manage-resource-competencies"></a>Gerir competências de recursos
As competências dos recursos são uma parte essencial da gestão de recursos. As competências podem ser utilizadas como base para determinar os recursos com o equilíbrio certo de aptidões, formação, certificação e experiência no projeto. Deve configurar estas informações para cada recurso e atualizá-las regularmente. Desta forma, pode maximizar as capacidades quando é feita a correspondência de competências de recursos específicas durante a atribuição de recursos do projeto.

[![Exemplos de aptidões, certificações, formação e experiência no projeto](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg)

Os seguintes procedimentos explicam como configurar algumas das competências para um recurso.

Para configurar as competências para um trabalhador, pode utilizar a página da lista **Trabalhadores** em Recursos Humanos ou a página da lista **Recursos** em Gestão de projetos e contabilística. Para os seguintes procedimentos, é utilizada a página da lista **Trabalhadores** em Recursos Humanos.

### <a name="set-up-competencies-certificates"></a>Configurar competências: Certificados

1. Na página da lista **Trabalhadores**, selecione a linha para o trabalhador ao qual pretende adicionar informações do certificado.
2. No Painel de Ação, no separador **Trabalhador**, no grupo **Competências**, selecione **Certificados**.
3. Selecione **Novo** e, no campo **Tipo e certificado**, selecione **PMP**.
4. No campo **Data de início**, selecione **1/10/2015** e selecione **Guardar**.

### <a name="set-up-competencies-skills"></a>Configurar competências: Aptidões

1. Na página da lista **Trabalhadores**, certifique-se de que o trabalhador que utilizou no procedimento anterior ainda está selecionado. Em seguida, no Painel de Ação, no separador **Trabalhador**, no grupo **Competências**, selecione **Aptidões**.
2. Selecione **Novo**.
3. No campo **Aptidão**, selecione **Gestão de projetos**.
4. No campo **Nível**, selecione **5 Especialista**.
5. No campo **Data do nível**, selecione **1-/14/2014**.
6. No campo **Anos de experiência**, introduza **10**.
7. Selecione **Guardar** e feche a página.

## <a name="create-a-new-project"></a>Criar um novo projeto
1. Na página **Gestão de projetos**, selecione **Novo projeto** e introduza os seguintes valores:

    - **Tipo de projeto:** Tempo e material
    - **Nome do projeto:** Fase de Atualização 2 XYZ
    - **Grupo do projeto:** TM\_WIP
    - **ID de contrato do projeto:** 00000002

2. Selecione **Criar projeto**.

### <a name="assign-a-resource-to-a-project"></a>Atribuir um recurso a um projeto

1. Na página **Trabalhadores**, na lista **Trabalhadores**, selecione o registo para o trabalhador para o qual configurou anteriormente competências, e abra o registo do trabalhador.
2. No Painel de Ação, no separador **Projeto**, no grupo **Configurar**, selecione **Atribuir projetos**.
3. Na página **Atribuições de projetos de validação de recursos**, no separador **Projetos**, no campo **Adicionar o projeto aos projetos selecionados**, filtre pelo projeto **Fase de Atualização 2 XYZ**.
4. No painel de **Projetos restantes**, selecione um projeto e, em seguida, selecione o botão de seta para adicioná-lo ao painel **Projetos selecionados**.

Também pode atribuir categorias para um recurso, conforme necessário. O tipo de categoria é **Custo** ou **Receitas**. O tipo de categoria é determinado pela sua organização. Se não forem atribuídas categorias a um recurso, o Finance procura a categoria predefinida nos preços por hora para custos e receitas.

### <a name="set-up-project-resource-and-role-characteristics"></a>Configurar características de recursos e funções do projeto

Um gestor de projetos pode utilizar a funcionalidade de atribuição de recursos do projeto para criar as funções necessárias para o projeto. As funções podem ser utilizadas se os recursos confirmados ainda forem desconhecidos quando os recursos estão a ser reservados. As funções podem ser reservadas temporariamente como recursos planeados para poder continuar as fases de planeamento do projeto.

[![Exemplo de uma função](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Cenário:** a Contoso foi contratado para concluir um Projeto de tempo e material que tem um estatuto de projeto aprovado. O gestor de projetos junior ainda está a concluir o âmbito do projeto. O gestor de recursos está neste momento a identificar os recursos específicos que serão reservados para trabalhar no novo projeto. Dada a natureza crítica do projeto, o patrocinador do projeto solicitou o gestor de projeto sénior como uma das funções. O gestor de recursos tem de adquirir o novo recurso e definir a função no sistema no caso de o gestor de projeto júnior necessitar de informações dos recursos durante o planeamento do projeto.

Os passos seguintes mostram como o gestor de recursos pode configurar a função de gestor de projetos Sénior e associar características de recursos a ele. Mais tarde, a função pode ser utilizada para procurar recursos disponíveis que correspondam às competências de recursos necessárias.

1. Na página **Configurar funções**, selecione **Novo** e introduza os seguintes valores:

    - **ID de função:** Gestor de Projetos Sénior
    - **Descrição:** Gestor de Projetos Sénior

2. Selecione **Criar**.
3. Selecione a função **Gestor de Projetos Sénior** e, em seguida, selecione **Configurar características**.
4. No campo **Tipo de características**, selecione **Aptidão**.
5. No campo **Características disponíveis**, introduza a aptidão a procurar.
6. No campo **Tipo de característica**, selecione **Certificado**.
7. No campo **Características disponíveis**, introduza o tipo de certificado a procurar.

### <a name="assign-a-project-resource-to-a-project"></a>Atribuir um recurso de projeto a um projeto

1. Na página **Todos os projetos**, selecione o projeto **Fase de Atualização 2 XYZ**.
2. No separador **Equipa do projeto e agendamento**, selecione **Adicionar**.
3. No campo **Função**, selecione **Membro da equipa**.
4. Selecione **Reservar no calendário**.
5. Na página **Disponibilidade do recurso**, selecione **Ver definições**.
6. Na página **'Ajustar definições da vista**, introduza os seguintes valores:

    - **Formato para a vista de intervalo de datas:** Dia
    - **Apresentar descrições de disponibilidade:** Sim
    - **Apresentar capacidade restante:** Sim

7. Na lista de recursos, selecione um recurso.
8. Selecione **Reserva Fixa** e **Capacidade Total**.


### <a name="assign-a-resource-to-a-default-role"></a>Atribuir um recurso a uma função predefinida

Para ajudar os gestores de projetos ou recursos, podem desagregar mais nos recursos que podem ser reservados para um projeto. Pode associar uma função predefinida a um recurso existente ou a um recurso adquirido recentemente. Por exemplo, quando o Daniel foi contratado, tinha experiência e aptidões para preencher a função Analista de negócios. O gestor de recursos atribuiu esta função como função predefinida de Daniel. Por isso, o gestor de recursos adicionou Daniel a um conjunto de analistas de negócios que estão disponíveis para trabalhar em projetos.

Durante a reserva de recursos, os gestores de projetos podem filtrar os recursos da função que estão disponíveis para trabalhar em projetos. Podem utilizar esta informação como um critério quando executam a análise de decisões de vários critérios durante a execução dos recursos. Podem ainda adicionar outras características de recursos ao filtro para procurar recursos com aptidões, formação e experiência específicas para um determinado projeto.

**Cenário:** foi iniciado um projeto aprovado e a função de de gestor de projetos Sénior foi reservada como recurso planeado durante a fase de planeamento do projeto. O gestor de recursos adquiriu agora um recurso para executar a função Gestor de projetos sénior.

1. Na página **Lista de recursos**, selecione **Daniel Goldschmidt**.
2. Na página **Função do recurso**, selecione **Novo** e introduza os seguintes valores:

    - **Data Efetiva:** Introduza a data atual.
    - **Expiração:** introduza **Nunca**.
    - **Função:** introduza **Gestor de Projetos Sénior**.

3. Selecione **Guardar** e feche a página.
4. No separador **Competências**, adicione a aptidão **ProjectMgmt** e o certificado **PMP**.

## <a name="set-up-role-based-pricing"></a>Configurar os preços baseados em funções
Todos os custos, vendas e preços de transferência podem ser configurados para funções.

1. Na página **Preço de venda (hora)**, selecione **Novo** e introduza uma data efetiva.
2. Na coluna **Função**, selecione uma função.
3. Na coluna **Preços**, introduza um preço para a função de recurso selecionada.

## <a name="form-a-project-team"></a>Formar uma equipa de projeto
Para utilizar as funções previamente configuradas num projeto, um gestor de projetos tem de associar as funções ao projeto. Podem ser atribuídas várias funções para um projeto. Para evitar confusões, estas funções são etiquetadas automaticamente durante a reserva. Por exemplo, se o gestor de projetos necessitar de três engenheiros de software, são geradas automaticamente três funções de Engenheiro de software com **Engenheiro de software 1**, **Engenheiro de software 2** e **Engenheiro de software 3** como etiquetas. Se a função tinha características de função definidas anteriormente, são aplicadas como um filtro durante as pesquisas de um recurso. Podem ser adicionadas características adicionais conforme seja necessário para refinar ainda mais a pesquisa.

As definições de visualização também podem ser personalizadas para oferecem uma melhor visão da disponibilidade dos recursos. Existem opções para mostrar a disponibilidade horária, diária, semanal, mensal, trimestral e anual. Também existe uma opção para mostrar a capacidade disponível e restante nos recursos. Esta opção é útil para a gestão do tempo, quando está a estimar o tempo disponível para as atividades ou disponibilidade de recursos.

O gestor do projetos pode selecionar uma função na página e, em seguida, se estiver disponível um recurso que se ajusta ao requisito, selecione para reservar um recurso para preencher a função. Note que os recursos não têm de ser reservados neste momento na fase de planeamento. Quando cria uma WBS, pode substituir as funções por recursos com pessoal para o projeto. Se as funções forem substituídas por recursos com pessoal na WBS, a configuração do recurso atualiza automaticamente a listagem e o agendamento da equipa do projeto.

[![Lista da equipa do projeto que inclui as funções e os recursos reais](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

O gestor de projetos tem várias opções para reservar um recurso para um projeto, tais como **Capacidade restante**, **Capacidade total**, **Capacidade Percentual** e **Especificar horas**. Estas opções de reserva podem ser canceladas em qualquer altura se as atribuições de recursos forem alteradas. São suportados dois tipos de reserva:

- **Reserva Fixa** – A reserva de recursos foi aprovada e confirmada para trabalhar no compromisso durante o período especificado.
- **Reserva flexível** – As reservas de recursos forem definidas provisoriamente para trabalharem no compromisso durante o período especificado.

O procedimento seguinte explica como criar uma equipa do projeto.

### <a name="create-a-project-team"></a>Criar uma equipa de projeto

1. Na página da lista **Todos os projetos**, selecione um projeto e, em seguida, selecione **Editar**.
2. No separador **Equipa do projeto e agendamento**, no campo **Data de fim da agenda**, introduza a data de início da agenda acrescida de um mês. Por exemplo, se a data de início da agenda for 24 de junho de 2017 (24/06/2017), introduza **24/07/2017**.
3. Selecione **Adicionar**.
4. No painel **Adicionar funções ao projeto**, no campo **Função**, selecione **Gestor de Projetos Sénior**.
5. Selecione **Competências necessárias**.
6. Na página **Escolha características**, as características que definiu anteriormente para a função Gestor de projetos sénior são selecionadas por predefinição. Selecione **OK**.
7. Na página **Adicionar funções ao projeto**, no campo **Número de recursos**, introduza **1**.
8. No campo **Recursos**, a pesquisa mostra todos os recursos que têm as competências necessárias. Selecione **Daniel Goldschmidt** e, em seguida, selecione **Criar**.
9. Na página **Projeto**, selecione **Adicionar**.
10. No painel **Adicionar funções ao projeto**, no campo **Função**, selecione **Membro da equipa**. No campo **Número de recursos**, introduza **5**.
11. Selecione **Criar**.
12. Na página **Projetos**, selecione **Concluir recurso**.

## <a name="resource-capacity-synchronization"></a>Sincronização da capacidade dos recursos
Os processos para a sincronização de recursos ajudam a garantir que a informação para o calendário e o calendário base passam para o agendamento de recursos do projeto. Se o calendário for alterado, os processos fazem as atualizações necessárias ao agendamento dos recursos do projeto. Os processos também ajudam a melhorar o desempenho, porque a informação dos recursos do calendário é sincronizada com antecedência. Por isso, as atualizações da informação de agendamento de recursos são mais rápidas. Recomendamos que agende os processos em lote em vez de individualmente. Caso contrário, existe o risco de alguém esquecer as datas inclusivas quando a informação foi sincronizada pela última vez. Se não forem utilizadas datas inclusivas, poderão ocorrer lacunas durante a sincronização de datas.

![Sincronização do calendário](./media/projectresourcing04-1024x471.jpg)

### <a name="synchronize-resource-capacity-roll-ups"></a>Sincronizar acumulações de capacidade dos recursos

O processo de sincronização foi concebido para sincronizar todas as informações do calendário de recursos. Estas informações incluem as informações base do calendário sobre quaisquer alterações à tabela de capacidade do Calendário de recursos do projeto. Se forem adicionados novos recursos no projeto, a sincronização ajuda a garantir que a informação do calendário atualizada está disponível. Esta sincronização pode ser feita em qualquer altura.

Recomendamos que utilize um lote. As opções estão disponíveis durante a sincronização das reservas de capacidade.

1. Selecione **Gestão de projetos e contabilística** &gt; **Periódico** &gt; **Sincronização da capacidade** &gt; **Sincronizar acumulações de capacidade dos recursos**.
2. Defina as opções na seguinte tabela.

    | Opção      | Descrição |
    |-------------|-------------|
    | Código de período | Opcionalmente, selecione o código do intervalo de datas do Razão geral para definir as datas de início e fim para o processo de sincronização para acumulações de capacidade de recursos. |
    | Data de início  | Introduza a data de início para o processo de sincronização para acumulações de capacidade de recursos. |
    | Data de fim    | Introduza a data de fim para o processo de sincronização para acumulações de capacidade de recursos. |

[![Processo de sincronização](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)

## <a name="set-up-roles-on-wbs-templates"></a>Configurar funções em modelos de WBS
Os gestores de projetos podem configurar modelos de WBS que podem aplicar quando criam uma WBS para novos projetos. Os gestores de projetos podem adicionar funções quando criam um modelo. Utilize o seguinte procedimento para atribuir uma função a um modelo de WBS.

1. Selecione **Gestão de projetos e contabilística** &gt; **Configurar** &gt; **Projetos** &gt; **Modelos de estrutura hierárquica do trabalho**.
2. Selecione **Detalhes** para um modelo de WBS selecionado.
3. Selecione uma tarefa na lista e, em seguida, no campo **Função**, selecione uma função a atribuir à tarefa.

### <a name="work-with-a-wbs"></a>Trabalhar com uma WBS

Pode criar uma nova WBS ou copiar uma WBS a partir de um modelo de WBS existente. Um gestor de projetos pode gerir facilmente os recursos ao atribuir funções a novas tarefas na WBS. As funções podem ser substituídas após a aquisição de um recurso ou depois de recurso confirmado para trabalhar na tarefa ser identificado. Esta flexibilidade permite que os gestores de projetos executem as seguintes tarefas:

- Identificar o número de recursos necessários para os pacotes de trabalho da WBS.
- Estimar os custos do projeto.
- Determinar um orçamento preliminar.
- Estimar a duração da atividade, baseado nas funções e nos recursos.
- Desenvolver alguns planos de gestão de projetos, baseado na informação do projeto disponível.

Foram adicionadas opções adicionais na WBS para melhorar a utilização da funcionalidade de atribuição de recursos.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Opção</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Atribuições de recursos</td>
<td>Veja os recursos atribuídos, as datas, o número de horas e o tipo de reserva para as tarefas na WBS.</td>
</tr>
<tr class="even">
<td>Gerar automaticamente a equipa</td>
<td>Adicione automaticamente os recursos planeados ao utilizar funções associadas a uma tarefa. O Finance sugere automaticamente recursos planeados através da análise de decisão de vários critérios baseada em funções. Depois de definidas as funções e o esforço (horas) para as tarefas numa WBS, e depois de a estrutura ter sido libertada, selecione <strong>Gerar automaticamente a equipa</strong>. O número necessário de recursos planeados é adicionado à WBS e ao separador <strong>Agendamento do projeto e da equipa</strong>.</td>
</tr>
<tr class="odd">
<td>Recurso (lista pendente)</td>
<td>Na página <strong>Iniciar atribuição de recursos</strong>, pode selecionar recursos para reserva fixa ou reserva flexível, baseado na duração especificada. Pode ajustar as definições de vista para ver e definir a duração das atividades dos recursos. Pode selecionar e atribuir recursos a nível do pacote de trabalho ao utilizar as seguintes opções:
<ul>
<li><strong>Aceitar</strong> – Confirmar alterações ao recurso atribuído a uma tarefa.</li>
<li><strong>Cancelar</strong> – Cancelar as alterações ao recurso atribuído a uma tarefa.</li>
<li><strong>Atribuir automaticamente</strong> – É selecionado automaticamente um recurso com pessoal disponível que tenha uma função de correspondência, e atribuído à tarefa selecionada.</li>
</ul></td>
</tr>
</tbody>
</table>

1. Na página **Todos os projetos**, selecione o projeto **Fase de Atualização 2 XYZ**.
2. Selecione **Plano** &gt; **Atividades** &gt; **Estrutura hierárquica do trabalho**.
3. Selecione **Novo** para adicionar as seguintes atividades de nível um à WBS:

    - A iniciar
    - Planeamento
    - A executar
    - Monitorização e Controlo
    - Fechar

4. Defina as datas e o esforço (horas), como mostra a seguinte ilustração.

    [![Definir as datas e o esforço](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Selecione a linha da tarefa **A iniciar** e, em seguida, no campo **Função**, selecione **Gestor de Projetos Sénior**.
6. Selecione **Publicar**.
7. Na mesma linha, no campo **Recursos**, selecione **Daniel Goldschmidt** e, em seguida, selecione **Aceitar**.
8. Selecione a linha de tarefa **Planeamento** e, em seguida, no campo **Função**, selecione **Analista de negócios**.
9. Selecione **Publicar** e, em seguida, selecione **Gerar automaticamente a equipa**.
10. Na caixa de mensagem apresentada, selecione **Sim**.
11. No campo **Recursos**, verifique se o valor é **Analista de negócios 1**.
12. Para o recurso **Analista de negócios 1** abra a pesquisa e selecione **Iniciar atribuições de recursos**. Em seguida, selecione um trabalhador para a tarefa.
13. Selecione **Atribuição flexível** &gt; **Capacidade Total**.

    > [!NOTE] 
    > Não receberá um aviso de que o recurso especificado é agora 2, porque o número de recursos permanece 1.

14. Na página **Estrutura hierárquica do trabalho**, valide a atribuição de recursos na WBS e selecione **Guardar**.

## <a name="resource-fulfillment-for-planned-resources"></a>Execução de recursos para recursos planeados
Um gestor de projeto pode planear as funções de recursos necessárias para um projeto. O gestor de recursos verá estes recursos planeados como pedidos na página **Execução de recursos** e poderá atribuir recursos reais.

1. Na página **Todos os projetos**, selecione o projeto **Fase de Atualização 2 XYZ**.
2. Selecione **Projeto** e, em seguida, selecione **Editar**.
3. No separador **Equipa do projeto e agendamento**, selecione **Adicionar**.
4. Na caixa de diálogo **Adicionar funções**, selecione a função **Programador de software**.
5. Selecione **Criar** e feche a página do projeto.
6. Na página **Execução de recursos**, selecione **Programador de software 1** para o projeto **Fase de Atualização 2 XYZ**.
7. Selecione um trabalhador e, em seguida, selecione **Atribuir**.
8. Verifique se a linha para **Programador de software 1** foi removida para o projeto **Fase de Atualização 2 XYZ**.
9. No separador **Equipa do projeto e agendamento**, para o projeto **Fase de Atualização 2 XYZ**, verifique se o trabalhador que selecionou no passo anterior foi adicionado como **Programador de software**.

## <a name="requests-for-project-resources"></a>Pedidos de recursos do projeto
A funcionalidade para o agendamento de recursos do projeto só permite que os gestores de recursos distribuam recursos com pessoal em compromissos ou projetos. Para ativar esta funcionalidade, execute as seguintes tarefas ou verifique se foram concluídas:

- Configurar sequências de números.
- Configurar os fluxos de trabalho de gestão de projetos e contabilística.
- Ativar os fluxos de trabalho de pedido de recursos.

Após a conclusão das tarefas anteriores, pode concluir as seguintes tarefas, conforme necessário:

- Criar um pedido de recurso a partir de um recurso com pessoal com reserva flexível.
- Monitorizar pedidos de recursos.
- Executar pedidos de recursos.
- Pedir um recurso com pessoal de uma WBS.
- ReservAr recursos para um projeto sem ter um pedido de recurso com pessoal.

## <a name="monitor-project-teams"></a>Monitorizar equipas do projeto
1. Na página **Todos os projetos**, selecione a ligação **ID do Projeto** para o projeto **Fase de Atualização 2 XYZ**.
2. No Separador Rápido **Equipa do projeto e agendamento**, verifique se os recursos do projeto que são listados estão corretos.
