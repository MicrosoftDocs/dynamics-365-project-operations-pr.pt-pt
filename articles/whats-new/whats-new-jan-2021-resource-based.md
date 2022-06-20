---
title: Novidades em janeiro de 2021 – Project Operations para cenários baseados em Recursos/Não Armazenados
description: Este artigo fornece informações sobre as atualizações de qualidade disponíveis na versão de janeiro de 2021 do Project Operations para cenários baseados em recursos/itens não existentes em stock.
author: sigitac
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: cd20ba47a45593e7694234b4f58aecd79b1c3736
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910690"
---
# <a name="whats-new-january-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades em janeiro de 2021 – Project Operations para cenários baseados em Recursos/Não Armazenados

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_


Este artigo aplica-se aos seguintes componentes e versões do Dynamics 365 Project Operations:

  - Project Operations na versão 4.6.0.154 do ambiente Dataverse
  - Gestão de projetos e contabilidade no ambiente do Dynamics 365 Finance versão 10.0.16

## <a name="quality-updates"></a>Atualizações de qualidade

### <a name="project-operations-on-dataverse"></a>Project Operations no Dataverse

| **Área de funcionalidades** | **Número de referência** | **Atualização de qualidade** |
| --- | --- | --- |
| **Implementação e configuração** | 2106818 | Solucionou o renomear de recurso web que estava a causar problemas relacionados com a personalização de uma página. |
| **Faturação e Preços** | 2091908 | Solucionou a visibilidade das opções **Bloqueio de preços** e **Usar preços atuais** na página **Fatura** quando o Project Operations é instalado juntamente com Dynamics 365 Field Service. |
| **Faturação e Preços** | 2103058 | **Totais dos projetos** atualizados para lidar com valores nulos pelo custo real de uma tarefa. |
| **Faturação e Preços** | 2116100 | Melhoria das mensagens de erro utilizadas com a funcionalidade, **Entradas Correta em valores reais**. |
| **Faturação e Preços** | 2116129 | Melhoria da visibilidade da estimativa de despesa no separador **Estimativas** na página **projetos**. |
| **Faturação e Preços** | 2119112 | Agregação fixa das vendas efetivas e do custo real quando são utilizadas taxas de câmbio diferentes. |
| **Faturação e Preços** | 2134705 | Corrigiu o erro, "Não é possível ler propriedade **getResourceString** de indefinido" quando a página **Fatura** é aberta e o Field Service é instalado. |
| **Gestão de oportunidades** | 2022195 | A grelha de faturação baseada em tarefas na página do **Projeto** inclui um ícone que indica que existe uma linha de contrato ou cotação ligada a essa tarefa. |
| **Gestão de oportunidades** | 2029135 | Corrigiu o erro do processo de negócio que ocorre quando um utilizador tenta abrir uma linha de fatura numa fatura confirmada que tem um valor antecipado faturado. |
| **Gestão de oportunidades** | 2040713 | Corrigiu o erro de script que ocorre ao criar uma fatura a partir de um contrato e o Field Service é instalado. |
| **Planeamento e Monitorização de Projetos** | 2090202 | Regras comerciais marcadas que já não são usadas como **Preteridas**. |
| **Tempo e Despesa** | 2091249 | Controlos mais apertados para que os utilizadores não possam alterar a tarefa numa entrada de tempo que tenha sido aprovada ou submetida. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Gestão de projetos e contabilidade no Dynamics 365 Finance

| **Área de funcionalidades** | **Número de referência** | **Atualização de qualidade** |
| --- | --- | --- |
| **Gestão de projetos e contabilística** | [478667](https://fix.lcs.dynamics.com/Issue/Details/?bugId=478667) | Valor do contrato incorreto na página de **Em conta** para um projeto de preço fixo com múltiplas fontes de financiamento. |
| **Gestão de projetos e contabilística** | [480260](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480260) | O marcador de posição **Invoiceproposal.PSAnfRefProjId** não está a apresentar o ID do Projeto para o fluxo de trabalho **Rever as propostas de fatura do projeto**. |
| **Gestão de projetos e contabilística** | [481227](https://fix.lcs.dynamics.com/Issue/Details/?bugId=481227) | A data de desconto em dinheiro errada é usada ao publicar propostas de fatura do projeto. |
| **Gestão de projetos e contabilística** | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558) | Remoção e leitura de atribuição de recursos no Project Operations duplica as entradas de previsão do projeto em Finanças. |
| **Gestão de projetos e contabilística** | [484468](https://fix.lcs.dynamics.com/Issue/Details/?bugId=484468) | No Project Operations não é possível criar estimativas de projeto Dataverse sem ter uma linha de contrato no projeto. |
| **Gestão de projetos e contabilística** | [485871](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485871) | A dimensão financeira de uma transação de despesas de projeto não é sincronizada com o voucher relacionado e a distribuição contabilística do relatório de despesas quando os custos são registados no Saldo. |
| **Gestão de projetos e contabilística** | [488382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488382) | O filtro para o **estado da fatura** em transações de projetos publicadas para projetos de preço fixo não funciona. |
| **Gestão de projetos e contabilística** | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | A eliminação da estimativa inversa não está a funcionar na secção **Periódica**. |
| **Gestão de projetos e contabilística** | [509989](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509989) | As linhas de proposta de fatura podem ser eliminadas no Project Operations quando estão integradas com Dataverse. |
| **Gestão de projetos e contabilística** | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041) | Impedir a ativação da funcionalidade de vários itens de contrato sem a integração do Dataverse. |
| **Gestão de projetos e contabilística** | [510527](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510527) | Quando a faturação em-conta é igual a lucros e perdas, a receita faturada é listada como zero na página de Estimativas. |
| **Gestão de projetos e contabilística** | [514167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514167) | As correções de faturas não funcionam em ambientes integrados. |
| **Gestão de projetos e contabilística** | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | Ao publicar WIP - a publicação do valor de vendas na faturação do projeto interempresa, é selecionada a conta errada. |
| **Gestão de projetos e contabilística** | [514385](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514385) | No Project Operations, as dependências das tarefas de estimativa em Dataverse não podem ser atualizadas. |
| **Gestão de projetos e contabilística** | [515258](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515258) | A eliminação repetida de diários de integração do Project Operations em Finanças leva à perda de dados. |
| **Gestão de projetos e contabilística** | [519716](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519716) | Ocorre o seguinte erro ao publicar um projeto de proposta de fatura, "A transação não equilibra na moeda de reporte quando a fatura antecipada deduzida é adicionada de volta". |
| **Gestão de projetos e contabilística** | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | O ID errado do projeto está incluído nas deduções após a atualização do contrato de projeto em Project Operations. |
| **Gestão de projetos e contabilística** | [522799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522799) | A estimativa e o reconhecimento de receitas não podem ser concluídos quando o Project Operations estiver ativado. |
| **Gestão de projetos e contabilística** | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | No Project Operations, a remoção de um projeto de um contrato não repõe o projeto padrão no contrato. |
| **Gestão de projetos e contabilística** | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | No Project Operations, numa fatura interempresa, as linhas de despesas erradas aparecem na lista de **Adicionar linha**. |
| **Viagem e Despesa** | [515334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515334) | As linhas de despesas não podem ser publicadas porque falta a configuração de horas na linha do contrato. |
| **Viagem e Despesa** | [437673](https://fix.lcs.dynamics.com/Issue/Details/?bugId=437673) | Quando a validação do projeto/categoria é obrigatória, as categorias de despesas associadas ao projeto não são visíveis no relatório de despesas. |
| **Viagem e Despesa** | [441256](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441256) | O saldo adiantado não é atualizado quando um relatório de despesas é publicado por linha. |
| **Viagem e Despesa** | [465396](https://fix.lcs.dynamics.com/Issue/Details/?bugId=465396) | O trabalho de **Atualizar informação de pagamento** falha após reverter as liquidações em que uma fatura foi liquidada com duas ou mais operações de pagamento. |
| **Viagem e Despesa** | [472892](https://fix.lcs.dynamics.com/Issue/Details/?bugId=472892) | Ocorre um problema com o cálculo da redução de refeição do último dia para a categoria de despesas diárias. |
| **Viagem e Despesa** | [477714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=477714) | O relatório **tipo de despesa por empregado** não mostra despesas em item se a primeira ligação de um utilizador estiver no idioma es-MX. |
| **Viagem e Despesa** | [487516](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487516) | O pagamento do fornecedor por uma fatura de relatório de despesas está a usar a conta sumária errada para a publicação de liquidação. |
| **Viagem e Despesa** | [487531](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487531) | Quando um relatório de despesa publicado com **Permitir o agrupamento de transações com base na conta de pagamento de desfasamento** e **Corrigir data contabilística ao publicar** ativados, as datas contabilísticas não são agrupadas na tabela **Distribuição contabilística**, o que tem impacto nos registos fiscais das vendas. |
| **Viagem e Despesa** | [488292](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488292) | O mapeamento da subcategoria de despesas é removido quando a caixa de verificação de despesas é limpa e selecionada novamente. |
| **Viagem e Despesa** | [506175](https://fix.lcs.dynamics.com/Issue/Details/?bugId=506175) | Um relatório de despesas interempresa não pode ser criado se o ID do projeto for adicionado ao nível do cabeçalho. |
| **Viagem e Despesa** | [509491](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509491) | Existe um problema com os pagamentos de despesas quando o valor da despesa é superior ao montante do adiantamento em dinheiro. |
| **Viagem e Despesa** | [509556](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509556) | O campo **ID do projeto** num relatório de despesas interempresa está vazio se a função de utilizador for atribuída a uma organização específica. |
| **Viagem e Despesa** | [518186](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518186) | A categoria de despesas está bloqueada ao adicionar uma nova linha de despesas. |
| **Viagem e Despesa** | [520914](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520914) | Discriminar linhas do relatório de despesas que já estão divididas resulta num preço incompleto de Contas a pagar\Voucher de livro-razão geral. Por causa da duplicação de **TRVEXPTRANS.SOURCEDOCUMENTLINE**, o Explorador de origem contabilística também está avariado. |
| **Viagem e Despesa** | [521768](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521768) | O índice adicionado na tabela **TRVREQUISITIONLINE** para a qual o cliente tem duplicados, resulta num erro durante a atualização. |
| **Viagem e Despesa** | [525106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525106) | No Project Operations, o tempo com tarefas interempresa em Dataverse não pode ser criado ou aprovado. |

## <a name="regulatory-updates"></a>Atualizações regulamentares

Para obter informações sobre atualizações regulamentares para as aplicações de Finanças e Operações, consulte [Atualizações regulamentares](/dynamics365/finance/localizations/regulatory-updates). Também pode iniciar sessão no LCS e ver as atualizações regulamentares planeadas utilizando a ferramenta de pesquisa Emitir. A pesquisa Emitir permite pesquisar por país, tipo de funcionalidade e versão.


[!INCLUDE[footer-include](../includes/footer-banner.md)]