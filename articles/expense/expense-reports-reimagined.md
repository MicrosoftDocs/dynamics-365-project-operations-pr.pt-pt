---
title: Relatórios de despesas reinventados
description: Este tópico fornece informações sobre a experiência reformulada e reinventada para a introdução de relatórios de despesas.
author: suvaidya
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: cd0d415b9cc85bac91de8fb9427da290ae0c6108
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897150"
---
# <a name="expense-reports-reimagined"></a>Relatórios de despesas reinventados

A introdução de relatórios de despesas foi reformulada para simplificar o processo e reduzir o tempo necessário para concluir um relatório. Seguem-se os principais componentes da nova experiência de despesas:

- Uma nova área de trabalho de gestão de despesas que permite aceder às despesas do seu delegado.
- Uma nova experiência de correspondência de recibos para mostrar melhor os recibos a nível do cabeçalho e simplificar o processo de anexação de recibos às linhas de despesa.
- Uma nova grelha só de leitura que permite ver muito mais linhas de despesa e colunas de dados adicionais. Agora pode ver todas as linhas discriminadas e divididas, juntamente com as respetivas despesas principais.
- Um painel simplificado para editar despesas.
- Mensagens de erro, aviso e política reformuladas para fornecer o contexto e a compreensão corretos do problema, e como resolvê-lo. Removemos várias das mensagens que apareciam antes de os utilizadores poderem concluir as suas tarefas e resolver os problemas.
- Uma nova página para especificar os campos obrigatórios, os campos opcionais e os campos que não devem ser incluídos. Esta página ajuda a reduzir o número de campos que têm de ser definidos.
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
| Melhor visibilidade sobre as linhas divididas e discriminadas | As linhas discriminadas e divididas são adicionadas diretamente à lista de despesas para aumentar a visibilidade e ajudá-lo a determinar facilmente se existem erros. |
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
