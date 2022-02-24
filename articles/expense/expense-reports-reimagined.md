---
title: Relatórios de despesas reinventados
description: Este tópico explica a experiência redesenhada e reimaginada para a entrada no relatório de despesas.
author: suvaidya
manager: AnnBe
ms.date: 03/26/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 79e6a407689813f8c87fdffba0cda84df10d3b83
ms.sourcegitcommit: 46726e5c8c994735c1e570e08d6ed8f9c9341319
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 03/26/2021
ms.locfileid: "5717709"
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

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4IQFM]

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
| Adicionar as despesas e recibos existentes durante a criação de despesas | Quando criar relatórios de despesas, pode adicionar todas as despesas ou selecionar despesas não associadas. As despesas não anexadas são despesas que foram importadas do feed do cartão de crédito corporativo ou despesas que foram criadas manualmente pelo utilizador, mas que não foram anexadas a um relatório de despesas.|
| Calculadora de taxa de câmbio | É adicionada uma calculadora de taxa de câmbio que permite calcular a taxa de câmbio das transações multidivisa de despesas correntes. |
| Guardar e adicionar novas linhas de despesa | Os botões **Guardar** e **Novo** estão disponíveis quando são introduzidas novas despesas para o ajudar a introduzir rapidamente linhas de despesa. |
| Melhor visibilidade sobre as linhas divididas e discriminadas | As linhas discriminadas e divididas são adicionadas diretamente à lista de despesas para aumentar a visibilidade e ajudá-lo a determinar facilmente se existem erros. |
| Mostrar recibos durante a discriminação | Os recibos podem ser mostrados durante a discriminação. |
| Seleção de adiantamento de tesouraria | Selecione um ou mais adiantamentos em dinheiro para cumprir uma única transação de despesas. |
| Saldo de adiantamento de tesouraria | Reveja o saldo antecipado em tempo real quando criar uma entrada de despesas contra adiantamentos aprovados e pagos em dinheiro. |

A versão inicial está focada em cenários de introdução de despesas. Qualquer cenário de revisão ou aprovação de relatório de despesas continuará a utilizar a página de introdução de despesas existente.

As seguintes funcionalidades não são suportadas no espaço de trabalho de despesas reimaginadas:

- Integração de requisição de viagem
- Entrada de despesas per diem
- Suporte do aprovador provisório
- Capacidade de ver a história do fluxo de trabalho


[!INCLUDE[footer-include](../includes/footer-banner.md)]
