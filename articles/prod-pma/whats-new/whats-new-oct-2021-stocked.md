---
title: Novidades ou alterações no Project Operations, outubro de 2021, para cenários baseados em produção/armazenados
description: Este tópico fornece informações sobre as atualizações de qualidade que estão disponíveis na versão de outubro de 2021 do Project Operations para cenários baseados em produção/armazenados.
author: andchoi
ms.date: 11/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: 03491ccab855e48819fccf4c9d2b584fd87cb4ba
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8576054"
---
# <a name="whats-new-or-changed-in-project-operations-october-2021-for-stockedproduction-based-scenarios"></a>Novidades ou alterações no Project Operations, outubro de 2021, para cenários baseados em produção/armazenados

_**Aplica-se a:** Project Operations para cenários baseados em stock/produção_

Este tópico aplica-se aos seguintes componentes e versões do Microsoft Dynamics 365 Project Operations:

- Gestão de projetos e contabilidade num ambiente do Dynamics 365 Finance versão 10.0.22
 
## <a name="quality-updates"></a>Atualizações de qualidade

| Área de funcionalidades | Número de referência | Atualização de qualidade |
|--------------|------------------|----------------|
| Gestão de projetos e contabilística | [557017](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557017) | Os montantes de trabalhos de projeto em processamento (WIP) e de receitas acumuladas não são corretamente revertidos quando uma fatura de cliente interempresa é publicada. |
| Gestão de projetos e contabilística | [558232](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558232) | A funcionalidade **Impedir encerramento do projeto se existirem transações abertas** não funciona. |
| Gestão de projetos e contabilística | [559271](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559271) | A classificação de faturação numa fatura de texto livre não é preenchida automaticamente em dimensões de projetos quando essa funcionalidade está ativada. |
| Gestão de projetos e contabilística | [574013](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574013) | Em cenários não interempresa, os montantes WIP e de receitas acumuladas não são corretamente revertidos quando a fatura do projeto é publicada. |
| Gestão de projetos e contabilística | [577857](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577857) | Os valores de débito e de crédito são alternado quando os suplementos do Microsoft Excel é utilizado com o Diário de despesas do projeto e o campo **Tipo de conta de desfasamento** está definido como **Projeto**. |
| Gestão de projetos e contabilística | [577972](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577972) | O montante que é publicado em transações de projetos é sobrestimado numa nota de encomenda de projeto que inclui itens em armazém e que tem valores de impostos não dedutíveis quando **UseTax** está marcado. |
| Gestão de projetos e contabilística | [581216](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581216) | O sistema divide o montante entre os relatórios de lucro e de perda do projeto e os relatórios WIP do projeto. |
| Gestão de projetos e contabilística | [582065](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582065) | O inventário disponível está incorreto depois de um requisito de produto parcialmente devolvido ser ajustado. |
| Gestão de projetos e contabilística | [582682](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582682) | Os nomes de recursos são duplicados no Project Operations quando são editados no Microsoft Project. |
| Gestão de projetos e contabilística | [583873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583873) | Os relatórios de despesas interempresa que possuam custos pendentes de faturas de fornecedor interempresa de Contas a Pagar são publicados pela primeira vez no tipo de publicação **Custo de WIP do projeto**. No entanto, durante o processamento, os custos relacionados com a estimativa são publicados no tipo de publicação **Custo do projeto** em vez do tipo de publicação **Custo interempresa** esperado. |
| Gestão de projetos e contabilística | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Os resultados de retenção de fornecedores em transações de despesas de projeto não são mostrados. |
| Gestão de projetos e contabilística | [587453](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587453) | A folha de horas tem de arredondar o montante da transação na moeda da transação para um número especificado de casas decimais em todas as distribuições contabilísticas e entradas gerais de alocação de diário. |
| Gestão de projetos e contabilística | [589409](https://fix.lcs.dynamics.com/Issue/Details/?bugId=589409) | As quantidades de requisitos de itens do projeto são automaticamente atualizadas quando as encomendas planeadas são confirmadas. |
| Gestão de projetos e contabilística | [590206](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590206) | O número do voucher, o saldo do fornecedor do tipo de transação e o número da conta não podem ser revertidos na fatura de pré-pagamento de uma nota de encomenda. |
| Gestão de projetos e contabilística | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | A fatura do fornecedor interempresa é quebrada quando a integração de faturas de fornecedor é ativada. |
| Gestão de projetos e contabilística | [593335](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593335) | Quando cria um Diário de despesas do projeto, o montante do custo é mostrado no campo **Crédito**. |
| Gestão de projetos e contabilística | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Os termos de pagamento nas faturas do projeto não funcionam como esperado. |
| Gestão de projetos e contabilística | [593565](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593565) | Os vouchers da folha de horas podem ser reutilizados quando a sequência de números for configurada como contínua. |
| Gestão de projetos e contabilística | [593652](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593652) | FRANÇA: A lógica de **Montante da retenção manual** não corresponde à lógica de **Montante da retenção automática** na proposta de fatura do contrato do Projeto. |
| Gestão de projetos e contabilística | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Quando a retenção de fornecedor é libertada, a publicação do voucher tem linhas adicionais incorretas. |
| Gestão de projetos e contabilística | [596650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596650) | Quando o campo **Data da fatura** na página **Criar proposta de fatura** é alterado, poderá ocorrer o seguinte erro: "Referência de objeto não definida como uma instância de um objeto." |
| Gestão de projetos e contabilística | [597679](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597679) | Um erro ocorre quando tenta aprovar uma folha de horas do fluxo de trabalho **TSLine** e há uma política de folha de horas para sábado e domingo. |
| Gestão de projetos e contabilística | [597801](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597801) | O tipo de item de projeto de saldo inicial é excluído de **Resumos de transações da proposta de fatura** quando o total da fatura da proposta de fatura é calculado. |
| Gestão de projetos e contabilística | [597886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597886) | Se o custo de consumo numa encomenda de produção de projeto for 0 (zero), o seguinte erro ocorre quando tenta estimar: "Tentativa de divisão por zero." |
| Gestão de projetos e contabilística | [598706](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598706) | A aplicação móvel Folha de Horas do Projeto para Android deixa de responder. O problema está relacionado com **TimeEntryDataManager ArgumentNullException**. |
| Gestão de projetos e contabilística | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | O diário de integração do Project Operations falha quando o publica, porque faltam dimensões a uma conta. No entanto, a conta a que faltam as dimensões não é a conta em que está a publicar. |
| Gestão de projetos e contabilística | [598929](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598929) | O filtro **ToDate** nas pesquisas não é limpo quando é removido da caixa de diálogo **Selecionar** na página **Custo da publicação**. |
| Gestão de projetos e contabilística | [599757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=599757) | **Repor todas a distribuição** falha e mostra um erro para as folhas de horas que são criadas para um projeto do tipo **Apenas tempo**. |
| Gestão de projetos e contabilística | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | O separador **Projeto** não é editável numa fatura pendente de fornecedor quando a categoria de aprovisionamento é atribuída ao item. |
| Gestão de projetos e contabilística | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | O painel de navegação está em falta se não estiver a iniciar sessão no Project Operations Dataverse. |
| Gestão de projetos e contabilística | [546467](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546467) | Para as transações de ajuste de projetos interempresa, existem problemas na empresa de destino. |
| Gestão de projetos e contabilística | [563579](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563579) | Os custos consolidados para um projeto calculam a quantidade e o preço de custo errados se a nota de encomenda for processada pelo **Processo de final de ano de nota de encomenda** no livro razão Geral. |
| Gestão de projetos e contabilística | [581454](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581454) | Quando uma encomenda de produção de projeto que tenha encomendas de qualidade é reportada como terminada, ocorre o seguinte erro: "Nenhuma transação virtual marcada com transação de inventário." |
| Gestão de projetos e contabilística | [596408](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596408) | Quando uma fatura de Contas a pagar relacionada com um projeto é publicada, ocorre o seguinte erro: "Projeto de texto enumerado – custo – item não existe." |
| Gestão de projetos e contabilística | [597237](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597237) | Os custos indiretos duplicam quando acumula receitas manualmente. |
| Gestão de projetos e contabilística | [601198](https://fix.lcs.dynamics.com/Issue/Details/?bugId=601198) | As receitas acumuladas e a publicação WIP não produzem transações. |
| Gestão de projetos e contabilística | [602095](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602095) | A ativação do preço pendente falha num item de custo padrão quando existe uma nota de encomenda de projeto. |
| Gestão de projetos e contabilística | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | O valor WIP invertido da publicação de uma fatura é diferente do valor WIP original publicado a partir de uma entrada de hora. |
| Gestão de projetos e contabilística | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Existe um problema de publicação para receitas faturadas de projeto em casos em que a retenção é aplicada, onde as transações de um voucher não têm um saldo correto. |
| Gestão de projetos e contabilística | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | A criação de uma estimativa após a publicação de uma proposta de fatura bloqueia a importação de linhas de correção no Project Operations. |
| Gestão de projetos e contabilística | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | A modificação de um registo de marco totalmente faturado não deve ser possível. |
| Gestão de projetos e contabilística | [611389](https://fix.lcs.dynamics.com/Issue/Details/?bugId=611389) | Quando são utilizadas cobranças automáticas, a fatura do cliente interempresa para uma folha de horas não pode ser publicada e é mostrada uma mensagem de erro. |
| Gestão de projetos e contabilística | [612991](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612991) | O endereço de um subprojeto não é atualizado corretamente. |
| Gestão de projetos e contabilística | [613418](https://fix.lcs.dynamics.com/Issue/Details/?bugId=613418) | O preço de custo dos requisitos de item é atualizado com o preço de compra das notas de encomenda consolidadas. |
| Gestão de projetos e contabilística | [614145](https://fix.lcs.dynamics.com/Issue/Details/?bugId=614145) | O custo publicado não é correto após a atualização do preço de compra e o parâmetro **Ativar gestão de alterações** ser ativada. |
| Viagem e Despesa | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Todas as despesas do utilizador podem ser vistas quando procura uma categoria na aplicação móvel Despesas. |
| Viagem e Despesa | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Montantes incorretos das transações de fornecedores e imposto sobre vendas publicados a partir de uma despesa criada a partir de uma transação de cartão de crédito. |
| Viagem e Despesa | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Uma mensagem de aviso irrelevante é mostrada quando atualiza as páginas do relatório de despesas. |
| Viagem e Despesa | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | O aprovador provisório errado é utilizado quando elimina um aprovador provisório e, em seguida, volta a submeter através do fluxo de trabalho. |
| Viagem e Despesa | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Ocorre um erro de publicação relacionado com a configuração de quilometragem. |
| Viagem e Despesa | [620773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620773) | A distribuição não atualiza a entidade jurídica quando uma transação não anexada é adicionada novamente ao relatório de despesas numa despesa interempresa. |

### <a name="regulatory-updates"></a>Atualizações regulamentares

Para obter informações sobre atualizações regulamentares para as aplicações de Finanças e Operações, consulte [Atualizações regulamentares](/dynamics365/finance/localizations/regulatory-updates). Também pode iniciar sessão nos Microsoft Dynamics Lifecycle Services (LCS) e utilizar a ferramenta de Pesquisa de problemas para ver as atualizações regulamentares planeadas. A Pesquisa de problemas permite pesquisar por país ou região, tipo de funcionalidade e versão.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
