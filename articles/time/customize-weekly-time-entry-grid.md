---
title: Expandir entradas de hora
description: Este tópico fornece informações sobre como os programadores são capazes de expandir o controlo da entrada de hora.
author: stsporen
ms.date: 01/27/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 6b91aecd76950d2bd37192d634c80ea98d08034e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583000"
---
# <a name="extending-time-entries"></a>Expandir entradas de hora

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

Dynamics 365 Project Operations inclui um controlo personalizado de entrada de tempo extensível. Isto controlo inclui as seguintes funcionalidades:

- Introduzir o tempo horizontalmente ao longo de uma semana
- Totais por dia, linha ou semana
- Copiar linhas ou semanas
- Entrada de hora através de HH:mm ou HH.hh (converte-se automaticamente para HH.hh)
- Importar a partir de atribuições, reservas ou compromissos

É possível expandir as entradas de hora em duas áreas:
- [Adicionar entradas de hora personalizadas para o seu uso próprio](#add)
- [Personalizar o controlo Entrada de Hora semanalmente](#customize)

## <a name="add-custom-time-entries-for-your-own-use"></a><a name="add"></a>Adicione entradas de hora personalizadas para o seu uso próprio

As entradas de hora são uma entidade de núcleo utilizada em vários cenários. Na Vaga 1 de abril de 2020, foi introduzida a solução de núcleo TESA. A TESA fornece uma entidade **Definições** e um novo direito de acesso **Utilizador de Entrada de Hora**. Também foram incluídos os novos campos, **msdyn_start** e **msdyn_end**, que têm uma relação direta com **msdyn_duration**. A nova entidade, o direito de acesso e os campos permitem uma abordagem mais unificada ao tempo através de vários produtos.


### <a name="time-source-entity"></a>Entidade de origem de hora
| Campo | Descrição | 
|-------|------------|
| Nome  | O nome da entrada Origem da hora utilizado como valor de seleção ao criar entradas de hora. |
| Origem da Hora Predefinida [Origem da Hora: isdefault] | Por predefinição, só pode ser marcada uma Origem de Hora como predefinida. Isto permite que as entradas assuma por predefinição uma origem de hora, se não for especificada uma. |
|Tipo de Origem de Hora [Origem da Hora: sourcetype] | O tipo de origem é uma opção (Tipo de Origem de Entrada de Hora) que permite a associação da origem de hora a uma aplicação. A Microsoft reserva os valores superiores a 190.000.000.|


### <a name="time-entries-and-the-time-source-entity"></a>Entradas de hora e a entidade de origem de Hora
Cada entrada de hora é associada a um registo de origem de hora. Este registo determina quais as aplicações que devem processar a entrada de tempo e como.

As entradas de hora são sempre um bloco de tempo contíguo com o início, o fim e a duração associados.

A lógica atualizará automaticamente o registo de entrada de hora nas seguintes situações:

- Se dois dos três campos seguintes forem fornecidos, o terceiro é calculado automaticamente: 

    - **msdyn_start**
    - **msdyn_end**
    - **msdyn_duration**

- Os campos **msdyn_start** e **msdyn_end** são conscientes do fuso horário.
- As entradas de hora criadas apenas com **msdyn_date** e **msdyn_duration** especificadas começarão à meia-noite. Os campos **msdyn_start** e **msdyn_end** serão atualizados em conformidade.

#### <a name="time-entry-types"></a>Tipos de entrada de hora

Os registos de entrada de hora têm um tipo associado que define o comportamento no fluxo de submissão para a aplicação associada.

|Rótulo | valor|
|-----|-----|
|Em pausa   |192,355,000|
|Viagens | 192,355,001|
|Horas Extraordinárias   | 192,354,320|
|Trabalho   | 192,350,000|
|Ausência    | 192,350,001|
|Férias   | 192,350,002|


## <a name="customize-the-weekly-time-entry-control"></a><a name="customize"></a>Personalizar o controlo de entrada de Hora semanalmente
Os programadores podem adicionar campos e pesquisas adicionais a outras entidades, bem como implementar regras de negócio personalizadas para apoiar os seus cenários de negócio.

### <a name="add-custom-fields-with-lookups-to-other-entities"></a>Adicionar campos personalizados com pesquisas a outras entidades
Existem três passos principais para adicionar um campo personalizado à grelha de entrada de hora semanal.

1. Adicione o campo personalizado à caixa de diálogo **Criação rápida**.
2. Configure a grelha para mostrar o campo personalizado.
3. Adicione o campo personalizado à página **Edição de linha** ou **Edição da entrada de tempo**, conforme adequado.

Garanta também que o novo campo tem as validações necessárias na página **Edição de linha** ou **Edição da entrada de tempo**. Como parte desta tarefa, bloqueie o campo com base no estado de entrada de tempo.

Quando adiciona um campo personalizado à grelha **Entrada de tempo** e, em seguida, cria entradas de tempo diretamente na grelha, o campo personalizado dessas entradas é definido automaticamente de modo a corresponder à linha. 

### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Adicionar o campo personalizado à caixa de diálogo Criação rápida
Adicione o campo personalizado à caixa de diálogo **Criação Rápida: criar entrada de tempo**. Em seguida, os utilizadores podem introduzir um valor quando adicionam entradas de hora ao selecionar **Novo**.

### <a name="configure-the-grid-to-show-the-custom-field"></a>Configurar a grelha para mostrar o campo personalizado
Existem duas formas de adicionar um campo personalizado à grelha **Entrada de tempo semanal**.

- Personalize a vista **As minhas entradas de tempo semanais** e adicione o campo personalizado à mesma. Pode especificar a posição e o tamanho do campo personalizado na grelha, editando as propriedades na vista.
- Crie uma nova vista de entrada de tempo personalizada e defina-a como a vista predefinida. Esta vista deve conter os campos **Descrição** e **Comentários externos**, além das colunas que pretende ter na grelha a incluir. Pode especificar a posição, o tamanho e a sequência de ordenação predefinida da grelha editando as propriedades na vista. Em seguida, configure o controlo personalizado para esta vista para que seja um controlo **Grelha de Entrada de Tempo**. Adicione o controlo à vista e selecione-o para **Web**, **Telefone** e **Tablet**. Em seguida, configure os parâmetros para a grelha **Entrada de tempo semanal**. Defina o campo **Data de início** para **msdyn\_date**, defina o campo **Duração** para **msdyn\_duration** e defina o campo **Estado** para **msdyn\_entrystatus**. O campo **Lista de estado apenas de leitura** está definido para **192350002 (Aprovado)**, **192350003 (Submetido)**, ou **192350004 (Revocação Pedida)**.

### <a name="add-the-custom-field-to-the-appropriate-edit-page"></a>Adicionar o campo personalizado à pagina de edição apropriada
É possível encontrar as páginas utilizadas para editar uma entrada de tempo ou uma linha de entradas de tempo por baixo de **Formulários**. O botão **Editar entrada** na gralha abre a página **Editar entrada** e o botão **Editar linha** abre a página **Editar linha**. Pode editar estas páginas de modo a que incluam campos personalizados.

Ambas as opções removem algumas filtragens inovadoras fornecidas com as entidades **Projeto** e **Tarefa do Projeto**, para que todas as vistas de procura das entidades sejam visíveis. Fornecidas com o programa, apenas as vistas de pesquisa relevantes são visíveis.

Tem de determinar a página de tarefas apropriada para o campo personalizado. Provavelmente, se adicionou o campo à grelha, deve entrar na página **Editar linha** que é utilizado para os campos que se aplicam a toda a linha de entradas de tempo. Se o campo personalizado tiver um valor exclusivo na linha todos os dias, (por exemplo, se é um campo personalizado para a hora de fim), deve entrar na página **Editar entrada de tempo**.

Para adicionar o campo personalizado a uma página, arraste um elemento **Campo** para a posição apropriada na página e, em seguida, defina as respetivas propriedades.

### <a name="add-new-option-set-values"></a>Adicionar novos valores do conjunto de opções
Para adicionar os valores do conjunto de opções a um campo inovador, siga estes passos.

1. Abra a página de edição para o campo e, em seguida, por baixo de **Tipo**, selecione **Editar** junto do conjunto de opções.
2. Adicione uma nova opção que tenha uma etiqueta e cor personalizadas. Se pretender adicionar um novo estado de entrada de tempo, o campo inovador é denominado **Estado de Entrada**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Designar um novo estado de entrada de tempo como só de leitura
Para designar um novo estado de entrada de hora como só de leitura, adicione o novo valor de entrada de hora à propriedade **Estado de Lista Só de Leitura**. Certifique-se de que adiciona o número e não a etiqueta. A parte editável da grelha de entrada de tempo será agora bloqueada para as linhas que tenham o novo estado. Para definir a propriedade **Lista de estado apenas de leitura** de forma diferente para diferentes vistas **Entrada de tempo**, adicione a grelha **Entrada de tempo** numa secção da vista **Personalizar controlos** e configure os parâmetros conforme adequado.

Em seguida, adicione regras de negócio para bloquear todos os campos nas páginas **Editar linha** e **Editar entrada de tempo**. Para aceder às regras de negócio para estas páginas, abra o editor de formulários para cada página e, em seguida, selecione **Regras de Negócio**. Pode adicionar o novo estado à condição nas regras de negócio existentes ou pode adicionar uma nova regra de negócio para o novo estado.

### <a name="add-custom-validation-rules"></a>Adicionar regras de validação personalizadas
Pode adicionar dois tipos de regras de validação para a experiência de grelha **Entrada de tempo semanal**:

- Regras de negócio do lado do cliente que funcionam em páginas
- Validações de plug-in do lado do servidor aplicáveis a todas as atualizações de entrada de tempo

#### <a name="client-side-business-rules"></a>Regras de negócio do lado do cliente
Utilize regras de negócio para bloquear e desbloquear campos, introduzir valores predefinidos nos campos e definir validações que requerem informações apenas do registo de entrada de tempo atual. Para aceder às regras de negócio para uma página, abra o editor de formulários e, em seguida, selecione **Regras de Negócio**. Em seguida, pode editar as regras de negócio existentes ou adicionar uma nova regra de negócio.

#### <a name="server-side-plug-in-validations"></a>Validações de plug-in do lado do servidor
Deve utilizar validações de plug-ins para quaisquer validações que exijam mais contexto do que o disponível num registo de entrada de tempo único. Também devem ser usadas para quaisquer validações que queira executar em atualizações em linha na grelha. Para concluir as validações, crie um plug-in personalizado na entidade **Entrada de tempo**.

### <a name="limits"></a>Limites
Atualmente, a grelha **Entrada de tempo** tem um limite de tamanho de 500 linhas. Se houver mais de 500 linhas, as linhas não serão apresentadas. Não existe nenhuma forma de aumentar este limite de tamanho.

### <a name="copying-time-entries"></a>Copiar entradas de hora
Utilize **Copiar Colunas de Entradas de Hora** para definir a lista de campos a copiar durante a entrada de tempo. **Data** e **Duração** são campos necessários e não devem ser removidos da vista.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
