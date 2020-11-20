---
title: Novidades ou alterações no Project Service Automation versão 3
description: Este tópico inclui informações sobre o que há de novo e o que foi alterado no Project Service Automation versão 3.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
ms.topic: article
author: JohnPBurrows
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
ms.openlocfilehash: 46cbbc3ff3b0efcecd3cba30b265a782f6cdcf60
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120017"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3"></a>Novidades ou alterações no Project Service Automation versão 3
[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Este tópico inclui informações sobre as alterações feitas na UI (interface de utilizador), nas funcionalidades e na terminologia do Project Service Automation entre as versões 2 ou 1 e a versão 3.

## <a name="project-scheduling"></a>Agendamento de projetos
O agendamento de projetos, que era conhecido como WBS (estrutura hierárquica do trabalho) nas versões anteriores, foi renomeado para Agendar, e pode ser acedido clicando no separador **Agendar**. 

![Agendamento de projetos](media/psa-schedule-01.png)

A agenda agora tem uma nova superfície para interação que é moderna e acessível. No entanto, o motor de agendamento do Project Service Automation subjacente não foi alterado. Os botões de controlo no friso da grelha da agenda permitem interagir com a agenda de maneira semelhante à versão anterior do Project Service Automation. Outras alterações à agenda incluem:

- **Gráfico Gantt** - O gráfico Gantt já não está presente. Uma nova visualização do Gantt será oferecida numa atualização futura.
- **Cabeçalhos de coluna** - Pode ocultar os cabeçalhos das colunas na grelha clicando no indicador para baixo ao lado do título da coluna. 
- **Colunas** - É possível apresentar colunas ocultas clicando em **Adicionar coluna**. 
- **Categoria da transação** - Uma pesquisa por **Categoria de transação** foi adicionada à grelha da agenda e será apresentada por predefinição. 
 
## <a name="project-templates"></a>Modelos de projeto
As alterações a seguir foram realizadas na funcionalidade de modelo do projeto.

### <a name="create-a-project-template"></a>Criar um modelo de projeto 
Pode criar um modelo de projeto na versão 3 de maneira semelhante às das versões anteriores do Project Service Automation. O modelo pode conter apenas uma agenda, e esta pode incluir atribuições, mas não são obrigatórias. Se a agenda tiver atribuições, estas poderão ser apenas para recursos genéricos. É possível gerar requisitos de recursos para recursos genéricos, mas estes não poderão ser reservados com recursos reais no modelo. Não é possível reservar um recurso real para uma equipa num modelo. 

### <a name="create-a-template-from-an-existing-template"></a>Criar um modelo com base num modelo existente
Ao criar um modelo de projeto com base num modelo existente no Project Service Automation versão 3, ocorre o seguinte: 

- A agenda do projeto de origem é copiada para o modelo. 
- Os recursos genéricos são copiados para a equipa e todas as atribuições de recursos genéricos também são copiadas. Os requisitos para os recursos genéricos não são copiados. 

### <a name="create-a-template-from-an-existing-project"></a>Criar um modelo com base num projeto existente
Ao criar um modelo de projeto com base num projeto existente, ocorre o seguinte: 

- A agenda do projeto de origem é copiada para o modelo. 
- Os recursos genéricos são copiados para a equipa e todas as atribuições de recursos genéricos são preservadas. Os requisitos para os recursos genéricos não são copiados.    
- Os recursos nomeados, atribuídos ou não atribuídos, são removidos da equipa e substituídos por recursos genéricos.
- As informações do cliente são removidas, se houver. 
- As referências às propostas e aos contratos são removidas, se houver. 

### <a name="create-a-project-from-a-template"></a>Criar um projeto a partir de um modelo
No Project Service Automation versão 3, ao criar um novo projeto a partir de um modelo, ocorre o seguinte:

- A agenda, a equipa e as atribuições são copiadas para o novo projeto.   
- A data de início é a data da cópia ou a data selecionada pelo utilizador.   
- Para os membros da equipa genéricos com requisitos de recursos no modelo, os requisitos não são copiados nem gerados automaticamente. Será necessário gerá-los. 

## <a name="copy-a-project"></a>Copiar um projeto
No Project Service Automation versão 3, ao copiar um projeto, ocorre o seguinte: 

- A data de início estimada é copiada, mas pode ser alterada.  
- A agenda e as tarefas do projeto são copiadas. 
- Os recursos genéricos e as suas atribuições são copiados. Os requisitos de recursos para os recursos genéricos não são copiados. Deverá gerá-los novamente. 
- Os recursos reais e as suas atribuições não são copiados. Em vez disso, são substituídos por recursos genéricos. 
- Os valores reais não são copiados para o novo projeto. 

## <a name="move-a-scheduled-project"></a>Mover um projeto agendado
Ao mover a agenda de um projeto existente, ocorre o seguinte: 

- As datas da tarefa são movidas automaticamente para corresponder ao período da movimentação. 
- Os recursos genéricos atribuídos são preservados.   
- Se tiverem sido gerados antes de o projeto ser movido, os requisitos do recurso genérico continuarão os mesmos e não serão gerados de novo automaticamente. Deverá gerá-los novamente para refletir as novas atribuições devido à movimentação da tarefa. 
- As atribuições de recursos reais são alteradas para corresponder à movimentação de datas da tarefa. As reservas de recursos reais não são alteradas. Deverá alterar as reservas utilizando a vista de reconciliação. 
- Os recursos da equipa com reservas, mas sem atribuições, não são alterados. 
- Os valores reais não são movidos. 

## <a name="estimates"></a>Estimativas
As estimativas foram divididas em dois separadores, **Atribuição de recurso** e **Estimativas**. O separador **Atribuição de recurso** contém as estimativas de esforço e mostra as atribuições do recurso para as tarefas numa vista faseada no tempo. Pode editar as estimativas com base no que foi gerado pelo motor de agendamento.

![Separador de atribuições de recursos a mostrar estimativas de esforço e atribuições do recurso para as tarefas](media/resource-assignments-tab-02.png)

O separador **Estimativas** mostra os valores de custo e vendas das atribuições do recurso. Os valores são só de leitura. Agora, a definição de preços de custo e venda é derivada das atribuições do membro da equipa na agenda. Isto significa que, se houver uma tarefa sem nenhuma atribuição, ela será apresentada sob o registo não atribuído. Isto também significa que, sem **função**, que é uma dimensão de definição de preços predefinida, não haverá nenhuma estimativa de custo ou vendas se houver um cliente ou um contrato/uma proposta associado ao projeto. 

![Separador Estimativas a mostrar valores de custo e vendas](media/estimates-tab-03.png)
  
A categoria também é suportada em tarefas na vista da agenda. O agrupamento por categoria na vista faseada no tempo das estimativas fornecerá uma experiência melhor, especialmente quando tiver estimativas de despesa no seu projeto. As estimativas de despesa são introduzidas utilizando uma grelha num separador separado. 

As estimativas de despesa podem ser introduzidas na grelha do separador **Estimativas de despesas**. 

![Separador Estimativas de despesas a mostrar a grelha de estimativas de despesas](media/expense-estimates-tab-04.png)

## <a name="resource-management"></a>Gestão de recursos
No Project Service Automation versão 3, com a nova IU Unificada do Cliente e as alterações nas relações entre reservas e atribuições, a definição da equipa de um projeto com recursos genéricos ou reais foi alterada significativamente em comparação com as versões 2 e 1. Entretanto, os conceitos de recursos reserváveis, **real** e **genérico**, permanecem iguais, assim como os membros da equipa, os requisitos, as atribuições e as reservas.   

![Utilizando o seletor de recursos](media/resource-management-05.png)

### <a name="assign-a-real-bookable-resource"></a>Atribuir um recurso reservável real 
No Project Service Automation versão 3, as reservas e as atribuições de tarefas não estão tão entrelaçados como nas versões anteriores do Project Service Automation. Pode utilizar a grelha da equipa para reservar um membro da equipa **real**, de modo semelhante ao mercado.

Utilizando o seletor de recursos na agenda, pode selecionar o membro da equipa criado na vista da equipa e, em seguida, atribuir tarefas ao mesmo. É possível continuar a atribuir tarefas aos recursos, mesmo depois das suas reservas. Utilize o separador **Reconciliação** para reconciliar membros da equipa que possuem diferenças nas reservas e atribuições.

O seletor de recursos mostrará os membros da equipa para o projeto. Também pode utilizar o seletor de recursos para pesquisar e ver outros recursos reserváveis que não fazem parte da equipa do projeto. Pode atribuí-los a uma tarefa, e ele passarão a fazer parte da equipa do projeto. Deverá reservá-los utilizando o separador **Quadro da agenda** ou **Reconciliação**.

### <a name="assign-a-generic-bookable-resource-on-a-task-and-project-team-and-then-fulfill-with-a-real-resource-via-schedule-board"></a>Atribuir um recurso genérico reservável a uma tarefa e uma equipa do projeto e, em seguida, preencher com um recurso real por meio do Quadro da Agenda 
No Project Service Automation versão 3, a funcionalidade de geração de equipas não é utilizada para recursos genéricos. Em vez disso, pode criar e atribuir diretamente um recurso genérico com base na agenda, introduzindo o nome da posição do recurso genérico na célula de recurso da agenda. Ou pode selecionar o ícone de recurso na célula e, em seguida, utilizando o seletor de recursos, introduzir o nome do recurso genérico que pretende criar. Isto abrirá um painel de criação rápida que permite definir a função e a unidade organizacional do membro da equipa do recurso genérico. Depois de criar o recurso, este será atribuído à tarefa e poderá continuar a atribuir esse recurso genérico a outras tarefas na agenda.    
 
Quando tiver atribuído o recurso a todas as tarefas apropriadas, poderá gerar um requisito de recurso e, depois, cumpri-lo fazendo a reserva diretamente no **Quadro da Agenda** ou submetendo um pedido de recurso. Também é possível adicionar recursos genéricos diretamente à grelha do membro da equipa. 

Os recursos genéricos são adicionados à equipa do projeto sem nenhum requisito de recurso e com as datas de início/fim do projeto até que o requisito de recurso seja gerado. Para gerar um requisito, selecione o recurso genérico e clique em **Gerar**. A ligação de requisito é apresentada e as horas necessárias serão preenchidas com as horas atribuídas. Pode clicar na ligação para abrir e atualizar o requisito.
  
Quando a reserva for concluída e tiver sido totalmente cumprida por um recurso nomeado, o recurso genérico será substituído pelo recurso nomeado e a atribuição na agenda será atualizada com o recurso nomeado. 

Os recursos propostos para os requisitos são armazenados numa separador, em vez de uma secção separada.

### <a name="multiple-named-resources-fulfilling-a-generic-resource"></a>Vários recursos nomeados a cumprir um recurso genérico
Quando um requisito é cumprido com vários recursos, o recurso genérico permanece na equipa e atribuído à tarefa. Os membros da equipa nomeados que são reservados não são atribuídos como parte da posição. O gestor de projeto pode atribuir o trabalho, conforme apropriado, aos recursos reais.  A vista **Reconciliação** fornece uma discriminação das reservas entre vários recursos para diversas atribuições de tarefa. Isto não é feito automaticamente porque, em cenários mais complicados, como um em que tem um grupo de tarefas a compor o requisito, a maneira como o gestor de projeto quer fazer a atribuição deve ser considerada. Como o sistema não pode compreender a intenção, as suposições provavelmente serão diferentes das pretensões e um resultado incorreto ou imprevisível será obtido. O resultado previsível é que o recurso genérico permaneça atribuído até que o gestor de projeto atribua deliberadamente os recursos utilizando a vista **Reconciliação**.

### <a name="reconciliation"></a>Reconciliação
O separador **Reconciliação** mostra as reservas e todas as atribuições de cada membro da equipa do projeto. A vista mostra as horas em células que podem representar pontos no tempo, desde meses até dias. Esta vista permite que os gestores de projeto reconciliem as reservas dos membros da equipa e as suas atribuições para a equipa do projeto. Isto é útil porque as reservas e as atribuições de tarefa não estão totalmente ligadas, o que permite uma maior flexibilidade ao planear um projeto. 

![Separador Reconciliação a mostrar as reservas e as atribuições dos membros da equipa do projeto](media/resource-reconciliation-tab-06.png)

Para cada recurso, a vista calcula a diferença entre as reservas de um membro da equipa e o rollup das atribuições de tarefas desse membro e apresenta as duas diferenças a seguir, que podem ocorrer com reservas e atribuições num projeto: 

- **Falta de reserva** - As faltas de reserva ocorrem quando um recurso tem mais atribuições do que reservas. Como esta capacidade não foi reservada, um gestor de projeto pode corrigir esta condição expandindo as reservas do recurso para cobrir o deficit. 
- **Reservas em excesso** - As reservas em excesso ocorrem quando um recurso é reservado para o projeto, mas não é atribuído a tarefas.  Esta condição pode ser aceitável se, por exemplo, o recurso tiver sido reservado antes da atribuição de tarefas. Entretanto, em outros casos, talvez não haja um plano de atribuição do recurso, e o gestor de projeto pode considerar o cancelamento das reservas do recurso para permitir que a capacidade seja utilizada em outro projeto. 

Quando tem atribuições de tarefas para um recurso, mas nenhuma reserva (uma falta de reserva), é possível selecionar a falta de reserva agregada e clicar em **Expandir reserva**. Aqui, é possível verificar a reserva necessária para resolver a falta do recurso e a sua disponibilidade. 
 
## <a name="time-and-expense"></a>Tempo e despesa
Esta secção inclui informações sobre as alterações de tempo, despesas e aprovações no Project Service Automation versão 3. Como parte da solução Dynamics 365 Project Service Automation, o recurso **Entrada de tempo** foi atualizado para aproveitar a arquitetura da Interface Unificada. Isto permite a entrega de uma interface de utilizador consistente e uniforme que segue um design responsivo para uma visualização ideal em qualquer tamanho de ecrã ou dispositivo. 

### <a name="landing-page"></a>Página de destino
A experiência de entrada de tempo personalizada não extensível foi preterida na versão 3. Em vez disso, agora há uma experiência de grelha nativa extensível e acessível. Pode aceder à funcionalidade de entrada de tempo utilizando o mapa do site à esquerda. Com esta alteração, já não poderá introduzir o tempo para uma semana de uma só vez. Em vez disso, deverá criar uma entrada de tempo para cada dia na grelha. Após a criação de algumas entradas de tempo, os utilizadores poderão criar entradas de tempo em massa com a função **Copiar** explicada mais adiante neste tópico. 

![Página de destino de entrada de tempo](media/time-entry-landing-page-07.png)
 
### <a name="create-new-time-entries"></a>Criar novas entradas de tempo 
Clique em **Novo** no friso para abrir uma página de criação rápida de entrada de tempo, na qual deve introduzir a duração em minutos, horas ou dias. Para fazer isso, basta começar a introduzir h, m ou d juntamente com a quantidade.  

![Criação rápida de entrada de tempo](media/quick-create-time-entry-08.png)

Os campos de pesquisa são apoiados por vistas do sistema. Por exemplo, depois de introduzir informações do projeto, o campo **Tarefa do projeto** é definido, por predefinição, como a vista **As Minhas Tarefas do Projeto em Aberto**. Para criar entradas de tempo para as tarefas que não foram atribuídas ao utilizador, clique em **Alterar vista** na pesquisa e selecione **Todas as tarefas do projeto Ativas**. Depois de a entrada de tempo ser criada e apresentada na grelha, pode editar todos os valores de linha diretamente na grelha.  

### <a name="bulk-createcopy"></a>Criar/copiar em massa 
Após criar algumas entradas de tempo, é possível utilizar a funcionalidade de cópia para criar entradas de tempo adicionais em massa. Clique em **Copiar** para abrir a caixa de diálogo **Copiar**. Em **Do período: Data de Início**, defina o intervalo de datas do qual os períodos de tempo devem ser copiados. Em **Até ao período: Data de Início**, especifique a data em que as entradas devem ser criadas. Clique em **Copiar** para copiar as entradas de tempo no dia da semana correspondente indicado em **Até ao Período**. Por exemplo, a entrada de tempo de segunda-feira da semana passada será copiada na segunda-feira da semana indicada em **Até ao Período**. 

![Copiar entradas de tempo em massa](media/bulk-copy-time-entry-09.png)
 
### <a name="import-data"></a>Importar dados 
As atribuições e as trocas seguem o mesmo padrão da IU, o que permite que o utilizador especifique o intervalo de datas quando as reservas precisam de ser importadas. Em seguida, deve selecionar explicitamente as reservas que devem ser copiadas nas entradas de tempo de **Rascunho**. Na versão 3, já não é possível ver o padrão de entradas de tempo **Sugerido** na grelha e no calendário.  

### <a name="change-in-calendar-control"></a>Alteração no controlo de calendário
Na versão 3, deixámos o controlo de calendário personalizado e passamos a utilizar o Calendário UC para apresentar as entradas de tempo da semana. Neste calendário, pode visualizar dia, semana e mês. 

> [!NOTE]
> Uma limitação do Calendário é que este controlo não oferece suporte a ações em itens de calendário individuais. Por exemplo, não poderá selecionar um ou mais itens de calendário e submeter ou eliminar esses itens. Ao clicar num item de calendário, a página da **entidade Entrada de tempo** será aberta para realizar ações adicionais. 

### <a name="extensibility"></a>Extensibilidade
**Capturar dados em campos personalizados apenas de entidades de entrada de tempo e despesa** - A entrada de tempo utiliza uma grelha editável, uma grelha só de leitura e controlos de calendário da plataforma. Todos esses controlos são nativos e, por isso, oferecem suporte a personalizações. No Project Service Automation versão 3, pode adicionar outros campos personalizados, configurar campos de pesquisa e apoiá-los com vistas personalizadas. Também é possível definir uma lógica de negócio personalizada com base em valores selecionados de campos personalizados.  

**Capturar dados em campos personalizados de entradas de tempo e despesa e propagá-los por entidades que suportam o fluxo de submissão e aprovação** - O processamento típico de entradas de tempo é apresentado no diagrama a seguir.

![Processo do fluxo de entrada de tempo](media/process-time-entries-10.png)

Se os requisitos de negócios estipularem que as entidades de tempo e despesa devem capturar as dimensões de definição de preços personalizadas e propagar os valores definidos por um recurso de tempo e entrada na dimensão de definição de preços personalizada para todas as entidades no gráfico anterior, consulte [Configurar campos personalizados como dimensões de definição de preços](set-up-pricing-dimensions.md).

Para dar suporte aos requisitos de negócios nos quais as entidades de tempo e despesa devem capturar as dimensões personalizadas que não são de preço e propagar os valores, pode utilizar a configuração de dimensões de definição de preços e indicar as dimensões personalizadas como dimensões de definição de preços sem custo ou taxa de faturação. Outro cenário seria a adição de um campo personalizado a cada uma das entidades utilizando o mesmo nome de campo em todas as entidades. Podem ser criados plug-ins personalizados para relacionar os registos nas entidades que estão a participar no fluxo de submissão/aprovação utilizando as entidades de origem e ligação da transação.  

### <a name="delegate-time-and-expense-entry"></a>Delegar entradas de tempo e despesa
A plataforma Common Data Service não oferece suporte à representação de um utilizador por outro, o que significa que, no Project Service Automation versão 3, não há suporte para a entrada delegada de tempo e despesa. No entanto, parceiros e clientes utilizaram uma solução alternativa para ativar o suporte para experiências de entrada de tempo delegada na versão 3. Esta solução é apenas uma alternativa, e não uma solução completa. Por isso, é importante entender as suas limitações e utilizar esta abordagem apenas se as limitações forem aceitáveis. 

> [!IMPORTANT]
> Estas informações só devem ser consideradas como uma sugestão diretriz para a implementação personalizada por um parceiro/cliente. A equipa do produto não oferecerá suporte formal para esta funcionalidade por meio de nenhum dos nossos canais de suporte.

### <a name="customization-details"></a>Detalhes da personalização 
A personalização permite que adicione um **Recurso reservável** para criar e editar experiências, o que possibilita que um utilizador atue como delegado, alterando o campo **Reserva de recurso** para outro utilizador para o qual as entradas de tempo e despesa precisam de ser registadas. Os passos a seguir abordam a delegação da entrada de tempo. Estas mesmas informações aplicam-se à delegação da entrada de despesa. 
 
1.  Certifique-se de que o utilizador delegado possua acesso de segurança global para os projetos e as tarefas dos projetos. 
1.  Como o **Recurso reservável**, que é um campo na entidade **Entrada de tempo**, não é exposto na página **Criação rápida**, é necessário adicioná-lo.

    -ou-

    Crie uma vista personalizada que inclua a coluna **Recurso reservável** para visualizar apenas as entradas de tempo criadas para o recurso. Publique as personalizações no designer de módulo de aplicação para que esta visualização apareça sob **Seletor de vistas** na página **Entradas de tempo**. Existem dois plug-ins que tratam da definição do gestor para entradas de tempo que não são do projeto:

    - PreValidateTimeEntryCreate
    - PreValidateTimeEntryUpdate
 
1. Crie um plug-in para substituir o campo **Gestor** pelo gestor do utilizador atribuído no campo **Recurso reservável**. Utilize a mesma **Fase de execução** que o plug-in OOB (fora da banda) (pré-validação) e utilize uma **Ordem de execução** que seja superior à dos plug-ins OOB (maior que 1). Isto garantirá que o plug-in personalizado seja executado depois dos plug-ins OOB.  
 
### <a name="end-user-experience"></a>Experiência do utilizador final
1.  Ao criar uma entrada de tempo na página de criação rápida, introduza os detalhes do Projeto e da Tarefa do projeto e, em seguida, selecione o utilizador no campo **Recurso reservável** para o qual as entradas de tempo devem ser registadas. 
2.  Por predefinição, este campo utiliza como predefinição o utilizador com sessão iniciada; entretanto, considerando que o utilizador substituiu este campo, a entrada de tempo será criada para o **Recurso reservável** escolhido.
3.  Quando submete as entradas de tempo que criou para estes registros, elas são colocadas em fila para o aprovador do projeto, conforme esperado. 
4.  Quando recupera as entradas de tempo do outro utilizador, estas serão devolvidas a um estado de **Rascunho**, com o campo **Recurso reservável** definido para outro utilizador. 
5.  Opcionalmente, pode mudar para a vista personalizada para filtrar as entradas de tempo do outro utilizador. 
 
### <a name="limitations"></a>Limitações
As funcionalidades **Copiar** e **Importar** funcionam apenas no contexto do utilizador com sessão iniciada. Isto significa que não é possível copiar ou importar entradas de tempo que tenham sido criadas para o utilizador com sessão iniciada como recurso reservável.

As entradas de tempo que não são para um projeto serão encaminhadas para aprovação para o gestor do recurso reservável apenas se o passo 4 da secção **Detalhes da Personalização** acima tiver sido concluído. Caso contrário, as entradas de tempo que não são do projeto do outro utilizador serão encaminhadas incorretamente para o gestor do utilizador com sessão iniciada. 

### <a name="other-changes"></a>Outras alterações 
A funcionalidade **Reservas e Tarefas** foi removida. 

## <a name="multidimensional-pricing"></a>Definição de preços multidimensional
Para maximizar a flexibilidade e satisfazer diferentes requisitos de negócios, o Project Service Automation versão 3 oferece suporte à aplicação discreta de conjuntos de dimensão de definição de preços para o custo e as taxas de faturação. Os valores de dimensão podem ser definidos como predefinidos e, em seguida, propagados pelo processo de definição de custo e preços, desde a criação de perfis do recurso até à entrada de tempo e os valores reais do projeto. A configuração específica do cliente e a sua modificação ou extensão utilizam a infraestrutura de personalização padrão.

O Project Service Automation é fornecido com um conjunto predefinido de dimensões de definição de preços, funções e unidades de recurso, e permite a configuração de preços e custos para cada combinação de Função e Unidade organizacional.

Para os clientes do Project Service Automation que pretendem continuar a utilizar estes campos fornecidos com o programa como dimensões de definição de preços na versão 3, não haverá nenhuma alteração relevante. Pode continuar a utilizar o Project Service Automation normalmente. Entretanto, se precisar de definir o preço ou os custos dos seus recursos utilizando outros atributos adicionais, a versão 3 permite adicionar as suas próprias dimensões de definição de preços personalizadas ao Project Service Automation. A extensão das dimensões de definição de preços personalizadas é uma experiência de configuração complicada. 

## <a name="quotes-and-contracts"></a>Propostas e contratos
No Project Service Automation versão 3, os aspetos de configuração e gestão de propostas e contratos foram alterados. As secções a seguir incluem informações mais detalhadas.

### <a name="set-up-chargeability-options"></a>Configurar opções de exigibilidade
Nas versões 1 e 2, a configuração de exigibilidade para funções e categorias de propostas e contratos específicos era efetuada utilizando a vista **Exigibilidade**, que estava na navegação superior de uma linha de proposta ou um item de contrato. Este também era o local em que podia configurar os preços para essas funções e categorias de Despesa.

A partir da versão 3, a configuração de opções de exigibilidade por função e categoria de Despesa será feita no nível da linha de proposta ou item de contrato. A configuração de preços é separada da configuração de Exigibilidade. É possível encontrar **Funções faturáveis** e **Categorias faturáveis** como separadores das páginas **Linha de proposta** e **Item de contrato** sem ter de utilizar a navegação superior.

![Funções faturáveis](media/chargeable-12.png)
 
A configuração de Funções faturáveis e Categorias faturáveis também utiliza o controlo de grelha editável e fornecido com o programa. Para cada função e cada categoria, as opções com suporte para o tipo de faturação durante a fase de Criação de Propostas e Contratação permanecem inalteradas em relação às versões anteriores como **Faturável** e **Não Faturável**. **Grátis** não é um tipo suportado durante a fase de Criação de Propostas ou Contratação. **Grátis** tem suporte apenas durante a aprovação de Tempo ou Despesas.  
 
### <a name="create-and-edit-custom-pricing-for-a-project-service-automation-quote-and-project-contract"></a>Criar e editar a definição de preços personalizada para uma proposta e um contrato de projeto do Project Service Automation
Nas versões 1 e 2, a utilização de uma lista de preços personalizada para propostas e contratos específicos era efetuada por meio de **Editar preços** na vista **Exigibilidade**. A vista **Exigibilidade** estava localizada na navegação superior de uma linha de proposta ou um item de contrato. Este também era o local em que podia configurar as opções de exigibilidade para as categorias de despesas e funções.

A partir da versão 3, a criação e a utilização de uma lista de preços de projeto personalizada numa proposta ou num contrato do projeto do Project Service Automation foram separadas da configuração de exigibilidade. Os contratos de proposta e projeto do Project Service Automation possuem um novo separador denominado **Listas de preços do projeto**. Este separador mostra uma vista associada de todas as Listas de preços do projeto que foram anexadas à proposta ou ao contrato do projeto do Project Service Automation. Para criar uma lista de preços personalizada com base numa lista de preços existente que já está associada a uma proposta ou um contrato do projeto, clique em **Criar lista de preços personalizada**. Isto criará uma cópia de todas as listas de preços associadas e anexá-las-á à Proposta ou ao contrato. Agora, é possível abrir a lista de preços e editar o preço da categoria da função ou da despesa, de modo a que essas alterações de preço sejam aplicadas apenas a esta proposta ou a este contrato. 
  
O gráfico a seguir é anterior à criação das listas de preços personalizadas.

![Antes das listas de preços personalizadas](media/before-custom-price-lists-13.png)

O gráfico a seguir é posterior à criação das listas de preços personalizadas.

![Depois das listas de preços personalizadas](media/after-custom-price-lists-14.png)

> [!NOTE]
> Um pequeno atraso pode ocorrer entre clicar em **Criar Lista de Preços Personalizada** e a lista de preços personalizada ser criada. É recomendável atualizar a grelha, em vez de clicar várias vezes. Uma lista de preços personalizada será criada se o nome da lista de preços associada tiver o nome da proposta ou o nome do contrato do projeto anexado.
