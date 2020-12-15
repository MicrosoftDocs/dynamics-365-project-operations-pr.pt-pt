---
title: Relatórios de despesas reformulados
description: Este tópico fornece informações sobre a experiência reformulada e reinventada para a introdução de relatórios de despesas no Microsoft Dynamics 365 Finance. A nova experiência simplifica o processo de conclusão dos relatórios de despesas e diminui o tempo que é necessário.
author: ryansandness
manager: AnnBe
ms.date: 06/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2019-6-30
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: f2acd9eab52629b0baeb82a399993fbc6337c722
ms.sourcegitcommit: 13a4e58eddbb0f81aca07c1ff452c420dbd8a68f
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 11/30/2020
ms.locfileid: "4650153"
---
# <a name="redesigned-expense-reports"></a>Relatórios de despesas reformulados
[!include[banner](../includes/banner.md)]

A entrada do relatório de despesas foi redesenhado para simplificar o processo de preencher relatórios de despesas e diminuir o tempo necessário. Seguem-se os principais componentes da nova experiência de despesas:

- Uma nova área de trabalho de gestão de despesas que permite aceder às despesas do seu delegado.
- Uma nova experiência de correspondência de recibos para mostrar melhor os recibos a nível do cabeçalho e simplificar o processo de anexação de recibos às linhas de despesa.
- Uma nova grelha só de leitura que permite ver muito mais linhas de despesa e colunas de dados adicionais. Agora pode ver todas as linhas discriminadas e divididas, juntamente com as respetivas despesas principais.
- Um painel simplificado para editar despesas.
- Mensagens de erro, aviso e política reformuladas para ajuda a garantir que tem o contexto correto para compreender qual é o problema, e como resolvê-lo. A Microsoft removeu muitas mensagens que apareciam antes dos utilizadores terem a oportunidade de completar as suas tarefas e resolver os problemas, como a mensagem de discriminação incompleta.
- Uma nova página para especificar quais os campos que são necessários pela sua organização, quais os campos opcionais e quais os campos que não devem ser capturados. Esta página ajudará a reduzir o número de campos que os utilizadores têm de definir.
- Um novo aspeto e funcionalidade dos relatórios de despesas para os relatórios já não parecerem como se fossem concebidos para contabilistas.

Para ativar a nova experiência, utilize a área de trabalho **Gestão de funcionalidades** para ativar a funcionalidade **Relatórios de despesas reinventados**. Quando ativa esta funcionalidade, ocorrem as seguintes ações:

- A área de trabalho de despesas existente é substituída pela nova área de trabalho.
- Um novo item de menu para visibilidade do campo de despesas é adicionado.
- Não são removidos itens de menu existentes para relatórios de despesas (a página existente) ou campos de relatório de despesas.
- Fluxos de trabalho e quaisquer aprovações ainda o levam à página de relatórios de despesas existentes.

## <a name="getting-started-video-for-new-users"></a>Vídeo de introdução para novos utilizadores

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE2Y7gO]

A [Experiência de despesas no vídeo Dynamics 365 for Finance and Operations](https://youtu.be/Ocy-MsTvEE0) (mostrado acima) está incluída na lista de reprodução [Finance and Operations](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) disponível no YouTube.

## <a name="new-features"></a>Novas funcionalidades

| Nova funcionalidade | Descrição |
|---|----|
| Visibilidade do campo de despesas | Uma nova página de configuração permite especificar quais os campos que devem ser desativados para uma organização, quais os campos que devem ser obrigatórios e quais os campos recomendados. |
| Campos necessários | A nova configuração simples permite tornar alguns campos obrigatórios sem ter de utilizar o quadro da política. |
| Campos opcionais | É adicionada uma segunda página para campos opcionais. Desta forma, os colaboradores não se sentirão como se tivessem de definir os campos, mas os campos ainda estão facilmente acessíveis. |
| Adicionar recibos não anexados | A capacidade para adicionar recibos não anexados ao relatório de despesas é mais visível a partir da área de trabalho e no relatório de despesas. |
| Mensagens melhoradas | Existe melhor visibilidade das linhas de despesas que têm avisos ou erros. |
| Redução das mensagens na barra de mensagens| O número de mensagens do Infolog foi reduzido e foi feito um esforço para evitar que aparecessem mensagens duplicadas em muitos casos. |
| Ações comuns agrupadas | A interface foi limpa com a inclusão de um novo botão de ações para a maioria das ações comuns a nível da linha, e a adição de um botão de reticências (...) para o cabeçalho e outras ações menos frequentes. |
| Nova área de trabalho para aumentar a visibilidade | Uma nova área de trabalho unifica as funcionalidades e as ligações que permitem aos utilizadores moverem-se para diferentes áreas. |
| Adicionar as despesas e recibos existentes durante a criação de despesas | Quando cria relatórios de despesas, pode adicionar todos recibos ou despesas, ou os selecionados. |
| Calculadora de taxa de câmbio | É adicionada uma calculadora de taxa de câmbio que permite calcular a taxa de câmbio das transações multidivisa de despesas correntes. |
| Guardar e adicionar novas linhas de despesa | Os botões **Guardar** e **Novo** estão disponíveis quando são introduzidas novas despesas para o ajudar a introduzir rapidamente linhas de despesa. |
| Melhor visibilidade sobre as linhas divididas e discriminadas | As linhas discriminadas e divididas são adicionadas diretamente à lista de despesas para aumentar a visibilidade e ajudá-lo a determinar facilmente se existem erros de políticas ou outros. |
| Mostrar recibos durante a discriminação | Os recibos podem ser mostrados durante a discriminação. |

A versão inicial está focada em cenários de introdução de despesas. Qualquer cenário de revisão ou aprovação de relatório de despesas continuará a utilizar a página de introdução de despesas existente.

As seguintes funcionalidades estão presentes na página existente, mas ainda não estão presentes na nova página. Estas funcionalidades serão reintroduzidas ao longo dos vários lançamentos seguintes:

- Aprovações
- Aprovações de contas a pagar e a capacidade para editar a contabilidade
- Vários pontos de entrada
- Integração de requisição de viagem
- Entidade de dados para a visibilidade do campo de despesas
- Introdução para subsídio diário
- Fluxo de trabalho a nível da linha
- Suporte do aprovador provisório
- Discriminação avançada
