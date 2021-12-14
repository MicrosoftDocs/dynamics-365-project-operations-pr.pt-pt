---
title: Novidades ou alterações no Project Operations, setembro de 2021, para cenários baseados em produção/armazenados
description: Este tópico fornece informações sobre as atualizações de qualidade que estão disponíveis na versão de setembro de 2021 do Project Operations para cenários baseados em produção/armazenados.
author: andchoi
ms.date: 11/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: andchoi
ms.openlocfilehash: 7016d702719b2d432ec929aaca8d609ebf6e996b
ms.sourcegitcommit: abdd6cb3461ebb12fd2ca7ea78439c29aecd0a94
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 11/16/2021
ms.locfileid: "7815854"
---
# <a name="whats-new-or-changed-in-project-operations-september-2021-for-stockedproduction-based-scenarios"></a>Novidades ou alterações no Project Operations, setembro de 2021, para cenários baseados em produção/armazenados

_**Aplica-se a:** Project Operations para cenários baseados em stock/produção_

Este tópico aplica-se aos seguintes componentes e versões do Microsoft Dynamics 365 Project Operations:

- Gestão de projetos e contabilidade de num ambiente do Dynamics 365 Finance versão 10.0.21
 
## <a name="quality-updates"></a>Atualizações de qualidade

| Área de funcionalidades | Número de referência | Atualização de qualidade |
|---|---|---|
| Gestão de projetos e contabilística | [412077](https://fix.lcs.dynamics.com/Issue/Details/?bugId=412077) | Se a função de Gestor de compras for concedido a uma entidade com personalidade jurídica, também obtém acesso a todos os projetos em todas as entidades com personalidade jurídica. |
| Gestão de projetos e contabilística | [537214](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537214) | Um problema de arredondamento do Imposto sobre o Valor Acrescentado (IVA) ocorre enquanto uma nota de crédito é liquidada contra uma fatura original do projeto. |
| Gestão de projetos e contabilística | [538002](https://fix.lcs.dynamics.com/Issue/Details/?bugId=538002) | Utilize um orçamento de projeto alternativo para verificação de orçamento. |
| Gestão de projetos e contabilística | [546265](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546265) | O grupo de preços **Hora de preços de vendas** não é calculado na estrutura hierárquica do trabalho para quotizações de projetos. |
| Gestão de projetos e contabilística | [555604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=555604) | Falha na eliminação da estimativa quando a funcionalidade **Ativar moeda do contrato do projeto para o cálculo de estimativas** está ativada. |
| Gestão de projetos e contabilística | [563523](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563523) | A fatorização do imposto sobre as vendas por quantidade é adicionada ao montante do preço de vendas quando o imposto de utilização é usado no grupo de impostos sobre vendas do Diário de despesas do projeto. |
| Gestão de projetos e contabilística | [564701](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564701) | O imposto condicional não é calculado corretamente para o último pagamento quando a retenção de fornecedores e o pré-pagamento são aplicados a faturas de uma nota de encomenda. |
| Gestão de projetos e contabilística | [565642](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565642) | O rastreio de ajuste não funciona para Diários de saldo inicial. |
| Gestão de projetos e contabilística | [568814](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568814) | **A alocação da revisão do orçamento do projeto por período** é dividida por todos os períodos de orçamento. Quando a alocação é submetida, o registo não é limpo. |
| Gestão de projetos e contabilística | [569250](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569250) | As publicações de Trabalho em Processamento (WIP) no livro razão geral têm um montante incorreto. |
| Gestão de projetos e contabilística | [570731](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570371) | A aprovação do Diário de horas do projeto não funciona. |
| Gestão de projetos e contabilística | [571391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571391) | O preço de vendas de ajuste do projeto não é atualizado com custos indiretos quando o limite de financiamento não está marcado. |
| Gestão de projetos e contabilística | [575831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575831) | Um requisito de item não pode ser criado quando o cabeçalho da tabela Vendas é faturado e a ordem de encomenda de apoio para linhas existentes foi finalizada. |
| Gestão de projetos e contabilística | [578036](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578036) | O montante da retenção para uma regra de faturação que tem um marco para um projeto diferente não é publicado no ID do projeto correspondente que foi selecionado para o marco. Em vez disso, é publicado com o primeiro projeto. |
| Gestão de projetos e contabilística | [578327](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578327) | Quando seleciona **Dimensão financeira definida** numa proposta de fatura, ocorre o seguinte erro: "Não é possível lançar objeto do tipo "Dynamics.AX.Application.FormIntControl" para o tipo "Dynamics.AX.Application.FormStringControl"." |
| Gestão de projetos e contabilística | [581167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581167) | O relatório de **Faturas do projeto** salta linhas. |
| Gestão de projetos e contabilística | [581489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581489) | Ocorre um erro quando calcula o controlo de custos de um projeto de investimento. |
| Gestão de projetos e contabilística | [590357](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590357) | O método **ProjTable::InitFromCustTable - canDeletePostalAddress** causa um problema de desempenho. |
| Gestão de projetos e contabilística | [592493](https://fix.lcs.dynamics.com/Issue/Details/?bugId=592493) | A mensagem de erro deve ser mais clara do que "Erro inesperado." |
| Gestão de projetos e contabilística | [598810](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598810) | A tarefa de lote de publicação de Faturas do projeto processa e publica a proposta de fatura mesmo que as linhas da fatura não tenham sido geradas. |
| Gestão de projetos e contabilística | [574282](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574282) | Um problema de arredondamento ocorre quando a chave de configuração da licença do Sector público é desativada. Um custo ou preço de vendas incorreto é gerado nas horas da folha de cálculo para contratos que têm múltiplas origens fundadoras. |
| Gestão de projetos e contabilística | [577598](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577598) | O preço de vendas do projeto numa encomenda de compra de projeto faturada é calculado incorretamente quando o modelo de preço de vendas é **Razão de contribuição**. |
| Gestão de projetos e contabilística | [580784](https://fix.lcs.dynamics.com/Issue/Details/?bugId=580784) | O sistema não considera os dias ativos entre os quais calcula a taxa de trabalho efetiva para um trabalhador. |
| Gestão de projetos e contabilística | [584054](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584054) | Um erro de publicação ocorre na folha de horas interempresa devido ao seguinte erro de validação: "Nenhum parceiro comercial está configurado para entidade jurídica." |
| Gestão de projetos e contabilística | [586303](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586303) | A descrição de uma nota de encomenda que tenha uma categoria de despesas não é obtida na lista de transações de projeto publicada. |
| Gestão de projetos e contabilística | [590349](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590349) | Existe uma conversão incorreta em diários de item que são postados num projeto. |
| Gestão de projetos e contabilística | [557294](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557294) | Pode confirmar uma nota de encomenda mesmo que o limite de financiamento tenha sido ultrapassado. |
| Gestão de projetos e contabilística | [574162](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574162) | A secção **Correção/Cancelar fatura** numa fatura de texto livre desaparece quando um ID de projeto é selecionado. |
| Gestão de projetos e contabilística | [575425](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575425) | Há problemas de desempenho quando uma proposta de fatura de projeto é publicada a partir de uma encomenda de venda de projeto que inclui um item em armazém. |
| Gestão de projetos e contabilística | [575939](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575939) | As faturas de compra do projeto não podem ser publicadas porque ocorre o seguinte erro: "Função AccDistProcessorProjectExtension.createForProjectRevenueLine foi incorretamente chamada." |
| Gestão de projetos e contabilística | [578970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578970) | Atualização à criação de tarefas de lote de estimativa do projeto para suportar a execução de várias subtarefas. |
| Gestão de projetos e contabilística | [584519](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584519) | O estado de uma folha de horas não pode ser atualizada para **Rascunho** quando o fluxo de trabalho está preso num estado **Cancelado**. |
| Gestão de projetos e contabilística | [584757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584757) | Os montantes de retenção não são calculados na proposta de fatura de nota de crédito se existirem várias linhas. |
| Gestão de projetos e contabilística | [586034](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586034) | Quando tenta alterar o montante numa fatura gerada a partir de uma nota de encomenda, ocorre o seguinte erro: "As transações em voucher não equilibram conforme XX/XX/XXXX. (moeda contabilística: 0,00 - moeda de relatório: 0,01)". |
| Gestão de projetos e contabilística | [588714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588714) | Há um problema de desempenho quando uma proposta de fatura do projeto é publicada no modo de lote, por causa da união com **GeneralJournalAccountEntry**. |
| Gestão de projetos e contabilística | [588851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588851) | Há problemas de desempenho quando uma folha de horas é publicada. |
| Gestão de projetos e contabilística | [590535](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590535) | A hierarquia de estimativas de custos da estrutura hierárquica do trabalho não está corretamente alinhada depois de todas as tarefas serem expandidas ou após uma única tarefa ser expandida manualmente. |
| Gestão de projetos e contabilística | [593663](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593663) | O modelo Excel de cotação do projeto não pode ser adicionado ao menu **Abrir no Excel**. |
| Gestão de projetos e contabilística | [596669](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596669) | O número de isenção fiscal para uma entidade com personalidade jurídica não é incluída na fatura de projeto impressa. |
| Gestão de projetos e contabilística | [597563](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597563) | Nenhum dado financeiro é atualizado no erro da unidade de inventário quando um projeto é ajustado em relação às linhas de crédito. |
| Gestão de projetos e contabilística | [598109](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598109) | Depois de aplicar o BDC 461935, não pode publicar estimativas se mudar para sequências de números contínuos. |
| Gestão de projetos e contabilística | [598688](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598688) | **TimeEntryDataManager** faz com que a aplicação móvel da folha de horas do Projeto para Android deixe de responder. |
| Gestão de projetos e contabilística | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | O valor WIP invertido da publicação de uma fatura é diferente do valor WIP originalmente publicado a partir da entrada de hora. |
| Gestão de projetos e contabilística | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Em casos em que a retenção é aplicada, as transações de um voucher não têm um saldo correto quando as receitas faturadas de um projeto são publicadas. |
| Gestão de projetos e contabilística | [603320](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603320) | Quando a funcionalidade **Melhoria do desempenho de agendamento de recursos do projeto** está ativada, os valores decimais são incorretamente arredondados para a disponibilidade e capacidade dos recursos. |
| Gestão de projetos e contabilística | [607324](https://fix.lcs.dynamics.com/Issue/Details/?bugId=607324) | Quando a funcionalidade **Criar estimativas de projeto utilizando várias tarefas de lote** está ativada, a criação de estimativas num lote que tenha várias subtarefas funciona apenas durante o período atual. |
| Viagem e Despesa | [551911](https://fix.lcs.dynamics.com/Issue/Details/?bugId=551911) | Uma política de requisição de viagem é ignorada e o fluxo de trabalho é aprovado sem erros. |
| Viagem e Despesa | [563752](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563752) | <p>A aplicação Despesas de Mobilidade não guarda as seguintes informações na linha de despesas:</p><ul><li>O ID do projeto</li><li>Se as despesas forem faturáveis</li><li>O número da atividade</li></ul> |
| Viagem e Despesa | [569458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569458) | O campo **Recibos anexados** está definido como **Sim** mesmo que nenhum recibo seja anexado à linha de despesas. |
| Viagem e Despesa | [571334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571334) | Ocorre um erro quando altera a categoria de despesas para **Pessoal**. |
| Viagem e Despesa | [572783](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572783) | Não pode editar a despesa principal ou anexar um recibo depois de uma transação de cartão de crédito ser dividida numa despesas pessoal. |
| Viagem e Despesa | [574252](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574252) | A política de despesas para transações interempresa que têm um ID de projeto não funciona corretamente. |
| Viagem e Despesa | [574489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574489) | As informações de data publicada estão em falta para os relatórios de despesas publicados. |
| Viagem e Despesa | [574504](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574504) | Existem problemas de método de pagamento na aplicação móvel Despesas. |
| Viagem e Despesa | [584799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584799) | Uma requisição de viagem que foi criada para um trabalhador pode ser utilizada para o relatório de despesas de outro trabalhador antes da data delegada. |
| Viagem e Despesa | [586023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586023) | Quando cria uma despesa, as alterações aos valores de dimensão financeira não são atualizadas corretamente ao nível da distribuição contabilística na área de trabalho **Gestão de despesas**. |
| Viagem e Despesa | [586081](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586081) | O estado de aprovação da linha de despesas principal não é sincronizado com o estado de aprovação do fluxo de trabalho da linha discriminada. |
| Viagem e Despesa | [590544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590544) | Ocorre um erro se publicar um relatório de despesas e a recuperação de impostos estiver ativada. |
| Viagem e Despesa | [564851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564851) | Um delegado não pode eliminar documentos de despesas para um colaborador despedido. |
| Viagem e Despesa | [587306](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587306) | A eliminação de uma linha de despesas demora mais do que o esperado e afeta o desempenho. |
| Viagem e Despesa | [600455](https://fix.lcs.dynamics.com/Issue/Details/?bugId=600455) | **TrvExpTrans** cria um registo **TaxUncommitted** órfão porque apenas **SourceDocumentLine** é eliminado. |
| Viagem e Despesa | [609918](https://fix.lcs.dynamics.com/Issue/Details/?bugId=609918) | **ReleaseUpdateDB72_Expense.updateTrvExpTransProjTransId()** não honra **trvExpTrans.ReferenceDataAreaId** para criar a nova sequência de números. |

## <a name="regulatory-updates"></a>Atualizações regulamentares

Para obter informações sobre atualizações regulamentares para aplicações Finance and Operations, consulte [Atualizações regulamentares](/dynamics365/finance/localizations/regulatory-updates). Também pode iniciar sessão nos Microsoft Dynamics Lifecycle Services (LCS) e utilizar a ferramenta de Pesquisa de problemas para ver as atualizações regulamentares planeadas. A Pesquisa de problemas permite pesquisar por país ou região, tipo de funcionalidade e versão.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
