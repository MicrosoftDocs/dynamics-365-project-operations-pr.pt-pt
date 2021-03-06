---
title: Expandir entradas de hora
description: Este tópico fornece informações sobre como os programadores são capazes de expandir o controlo da entrada de hora.
author: stsporen
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 93f411ad7c86beefcc35e7799a03987dacdcd62b
ms.sourcegitcommit: 5a29adce48133e09f051929e8544d6c2c93c025d
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/02/2020
ms.locfileid: "3930894"
---
# <a name="extending-time-entries"></a>Expandir entradas de hora

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

O Dynamics 365 Project Operations inclui um controlo personalizado de hora expansível. Isto controlo inclui as seguintes funcionalidades:

- Introduzir o tempo horizontalmente ao longo de uma semana
- Totais por dia, linha ou semana
- Copiar linhas ou semanas
- Entrada de hora através de HH:mm ou HH.hh (converte-se automaticamente para HH.hh)
- Importar a partir de atribuições, reservas ou compromissos

É possível expandir as entradas de hora em duas áreas:
- [Adicionar entradas de hora personalizadas para o seu uso próprio](#add)
- [Personalizar o controlo Entrada de Hora semanalmente](#customize)

## <a name="add-custom-time-entries-for-your-own-use"></a><a name="add"></a>Adicione entradas de hora personalizadas para o seu uso próprio.

As entradas de hora são uma entidade central que foi concebida para ser utilizada para vários cenários. Na segunda fase do lançamento de abril de 2020, foi introduzida a solução central TESA, que fornece uma entidade **Definições** e um novo direito de acesso **Utilizador de Entrada de Hora**. Também foram incluídos os novos campos, **msdyn_start** e **msdyn_end**, que têm uma relação direta com **msdyn_duration**. A nova entidade, o direito de acesso e os campos permitem uma abordagem mais unificada ao tempo através de vários produtos.


### <a name="time-source-entity"></a>Entidade de Origem de Hora
| Campo | Descrição | 
|-------|------------|
| Nome  | O nome da entrada Origem da Hora utilizado como valor de seleção durante a criação da entrada de hora. |
| Origem da Hora Predefinida [Origem da Hora: isdefault] | Por predefinição, só pode ser marcada uma Origem de Hora na origem da hora predefinida. Esta capacidade permite que as entradas assuma por predefinição uma origem de hora, se não for especificada uma. |
|Tipo de Origem de Hora [Origem da Hora: sourcetype] | O tipo de origem é uma opção (Tipo de Origem de Entrada de Hora) que permite a associação da origem de hora a uma aplicação. Serão adicionados valores adicionais a este conjunto de opções à medida que forem adicionadas aplicações adicionais. Note que a Microsoft reserva os valores superiores a 190.000.000.|


### <a name="time-entries-and-the-time-source-entity"></a>Entradas de hora e a Entidade de Origem de Hora
Cada entrada de hora é associada a um registo de origem de hora. Este registo determina como e que aplicações devem processar a entrada de hora.

As entradas de hora são sempre um bloco de tempo contíguo com o início, o fim e a duração associados.

A lógica atualizará automaticamente o registo de entrada de hora nas seguintes situações:

- Se dois dos três campos seguintes forem fornecidos, o terceiro é calculado automaticamente 

    - **msdyn_start**
    - **msdyn_end**
    - **msdyn_duration**

- Os campos **msdyn_start** e **msdyn_end** são sensíveis ao fuso horário.
- As entradas de hora criadas apenas com **msdyn_date** e **msdyn_duration** especificadas começarão à meia-noite, e **msdyn_start** e **msdyn_end** serão atualizados em conformidade.

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



## <a name="customize-the-weekly-time-entry-control"></a><a name="customize"></a>Personalizar o controlo Entrada de Hora semanalmente
Os programadores podem adicionar campos e pesquisas adicionais a outras entidades, bem como implementar regras de negócio personalizadas para apoiar os seus cenários de negócio.

### <a name="add-custom-fields-with-lookups-to-other-entities"></a>Adicionar campos personalizados com pesquisas a outras entidades
Existem três passos principais para adicionar um campo personalizado à grelha de entrada de hora semanal.

- Adicione o campo personalizado à caixa de diálogo de criação rápida.
- Configure a grelha para mostrar o campo personalizado.
- Adicione o campo personalizado ao fluxo de tarefas de edição de linhas ou ao fluxo de tarefas de edição de células.

Também deve garantir que o novo campo tenha as validações necessárias no fluxo de tarefas de edição de linhas ou células. Como parte deste passo, tem de bloquear o campo com base no estado de entrada de hora.

#### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Adicionar o campo personalizado à caixa de diálogo de criação rápida
Tem de adicionar o campo personalizado à caixa de diálogo **Criação Rápida de Entrada de Hora**. Em seguida, os utilizadores podem introduzir um valor quando adicionam entradas de hora ao selecionar **Novo**.

#### <a name="configure-the-grid-to-show-the-custom-field"></a>Configurar a grelha para mostrar o campo personalizado
Existem duas maneiras para adicionar um campo personalizado à grelha de entrada de hora semanal:

  - Personalizar uma vista e adicionar um campo personalizado
  - Criar uma nova entrada de hora personalizada predefinida 


**Personalizar uma vista e adicionar um campo personalizado**

Pode personalizar a vista **As Minhas Entradas de Hora Semanais** e adicionar o campo personalizado à mesma. Pode escolher a posição e o tamanho do campo personalizado na grelha editando essas propriedades na vista.

**Criar uma nova entrada de hora personalizada predefinida** 

Esta vista deve conter os campos **Descrição** e **Comentários Externos**, além das colunas que pretende ter na grelha. 

1. Escolha a posição, o tamanho e a sequência de ordenação predefinida da grelha ao editar essas propriedades na vista. 
2. Configure o controlo personalizado para esta vista para que seja um controlo **Grelha de Entrada de Hora**. 
3. Adicione este controlo à vista e selecione-o para Web, telefone e tablet. 
4. Configure os parâmetros para a grelha de entrada de hora semanal. Defina o campo **Data de Início** para **msdyn_date**, defina o campo **Duração** para **msdyn_duration** e defina o campo **Estado** para **msdyn_entrystatus**. 
5. Para a vista predefinida, o campo **Estado de Lista Só de Leitura** é definido como **192350002,192350003,192350004** o campo **Fluxo de Tarefas de Edição de Linhas** é definido como **msdyn_timeentryrowedit** e o campo **Fluxo de Tarefas de Edição de Células** é definido como **msdyn_timeentryedit**. 
6. Pode personalizar estes campos para adicionar ou remover o estado só de leitura ou para utilizar uma experiência baseada em tarefas diferente (TBX) para a edição de linhas ou células. Estes campos devem estar vinculados a um valor estático.


> [!NOTE] 
> Ambas as opções irão remover algumas filtragens fornecidas com o programa nas entidades **Projeto** e **Tarefa do Projeto** para que todas as vistas de pesquisa das entidades sejam visíveis. Fornecidas com o programa, apenas as vistas de pesquisa relevantes são visíveis.
Tem de determinar o fluxo de tarefas apropriado para o campo personalizado. Provavelmente, se adicionou o campo à grelha, deve entrar no fluxo de tarefas de edição de linhas que é utilizado para os campos que se aplicam a toda a linha de entradas de tempo. Se o campo personalizado tiver um valor exclusivo todos os dias, tal como um campo personalizado para **Hora de Fim**, este deverá entrar no fluxo de tarefas de edição de células.

Para adicionar o campo personalizado a um fluxo de tarefas, arraste um elemento **Campo** para a posição apropriada na página e, em seguida, defina as propriedades do campo. Defina a propriedade **Origem** como **Entrada de Hora** e defina a propriedade **Campo de Dados** como o campo personalizado. A propriedade **Campo** especifica o nome a apresentar na página de TBX. Selecione **Aplicar** para guardar as suas alterações no campo e, em seguida, selecione **Atualizar** para guardar as suas alterações à página.

Para utilizar uma nova página de TBX personalizada, crie um novo processo. Defina a categoria como **Fluxo do Processo de Negócio**, defina a entidade como **Entrada de Tempo** e defina o tipo de processo de negócio como **Executar processo como fluxo de tarefas**. Em **Propriedades**, a propriedade **Nome da página** deve ser definida como o nome a apresentar da página. Adicione todos os campos relevantes à página de TBX. Guarde e ative o processo e, em seguida, atualize a propriedade de controlo personalizado para o fluxo de tarefas relevante para o valor **Nome** no processo.

### <a name="add-new-option-set-values"></a>Adicionar novos valores do conjunto de opções
Para adicionar valores do conjunto de opções a um campo fornecido com o programa, abra a página de edição para o campo e, em seguida, em **Tipo**, selecione **Editar** junto do conjunto de opções. Em seguida, adicione uma nova opção que tenha uma etiqueta e cor personalizadas. Se pretender adicionar um novo estado de entrada de tempo, o campo fornecido com o programa é denominado **Estado de Entrada**, e não **Estado**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Designar um novo estado de entrada de tempo como só de leitura
Para designar um novo estado de entrada de hora como só de leitura, adicione o novo valor de entrada de hora à propriedade **Estado de Lista Só de Leitura**. A parte editável da grelha de entrada de tempo será bloqueada para as linhas que tenham o novo estado.
Em seguida, adicione regras de negócio para bloquear todos os campos nas páginas de TBX **Editar Linha de Entrada de Tempo** e **Editar Entrada de Tempo**. Pode aceder às regras de negócio para estas páginas abrindo o editor de fluxo do processo de negócio para a página e, em seguida, selecionando **Regras de Negócio**. Pode adicionar o novo estado à condição nas regras de negócio existentes ou pode adicionar uma nova regra de negócio para o novo estado.

### <a name="add-custom-validation-rules"></a>Adicionar regras de validação personalizadas
Existem dois tipos de regras de validação que pode adicionar para a experiência de grelha de entrada de hora semanal:

- Regras de negócio do lado do cliente que funcionam em caixas de diálogo de criação rápida e em páginas TBX.
- Validações de plug-ins do lado do servidor aplicáveis a todas as atualizações de entrada de hora.

#### <a name="business-rules"></a>Regras de negócio
Utilize regras de negócio para bloquear e desbloquear campos, introduzir valores predefinidos nos campos e definir validações que requerem informações apenas do registo de entrada de tempo atual. Pode aceder às regras de negócio para uma página de TBX abrindo o editor de fluxo do processo de negócio para a página e, em seguida, selecionando **Regras de Negócio**. Em seguida, pode editar as regras de negócio existentes ou adicionar uma nova regra de negócio. Para obter ainda mais validações personalizadas, pode utilizar uma regra de negócio para executar JavaScript.

#### <a name="plug-in-validations"></a>Validações de plug-ins
Deve utilizar validações de plug-ins para quaisquer validações que exijam mais contexto do que o disponível num registo de entrada de tempo único ou para as validações que pretende executar nas atualizações inline na grelha. Para concluir a validação, crie um plug-in personalizado na entidade **Entrada de Tempo**.
