---
title: Novidades em novembro de 2021 – Project Operations para cenários baseados em Recursos/Não Stock
description: Este tópico fornece informações sobre as atualizações de qualidade disponíveis na versão de novembro de 2021 do Project Operations para cenários baseados em recursos/itens não existentes em stock.
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 20f277bc9b6f571c0144eaaa867bb97c0cf30ddb
ms.sourcegitcommit: 04ebe764afa22742b3fbf8f12af31e8eea93682e
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 11/23/2021
ms.locfileid: "7827340"
---
# <a name="whats-new-november-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades em novembro de 2021 – Project Operations para cenários baseados em Recursos/Não Stock

*Aplica-se A: Project Operations para cenários baseados em recursos/não armazenados*

Este tópico aplica-se aos seguintes componentes e versões do Microsoft Dynamics 365 Project Operations:

- Project Operations num ambiente Dataverse, versão 4.26.0.145, 4.26.0.148, or 4.26.0.150
- Gestão de projetos e contabilidade de num ambiente do Dynamics 365 Finance versão 10.0.22

## <a name="features-included-in-this-release"></a>Funcionalidades incluídas nesta versão

Estão incluídas nesta versão as seguintes funcionalidades:

- As interfaces de programação de aplicações (APIs) do Agendamento de Projetos suportam agora a capacidade de criar e eliminar buckets do Projeto.

## <a name="project-operations-dual-write-maps-updates"></a>Atualizações de mapas de escrita dupla do Project Operations

Não existem atualizações para os mapas de escrita dupla do Project Operations nesta versão. Para obter uma lista atual e as versões dos mapas de escrita dupla do Project Operations, consulte [Versões do mapa de escrita dupla do Project Operations](/dynamics365/project-operations/environment/resource-dual-write-maps).

Execute sempre a versão mais recente do mapa no seu ambiente e ative todos os mapas de tabelas relacionados à medida que atualiza a sua solução do Project Operations Dataverse e a versão da solução Finance. Algumas funcionalidades e capacidades podem não funcionar corretamente se a versão mais recente do mapa não estiver ativada. Pode ver a versão ativa do mapa na coluna **Versão** na página **Escrita Dupla**. Para ativar uma nova versão do mapa, selecione **Versões do mapa de tabela** , selecione a versão mais recente e, em seguida, guarde a versão selecionada. Se tiver personalizado um mapa de tabela de origem, volte a aplicar as alterações. Para mais informações, consulte [Gestão do ciclo de vida da aplicação](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se ocorrer um problema quando iniciar o mapa, siga as instruções na secção [Problema de colunas de tabela em falta em mapas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) do guia de resolução de problemas do serviço Escrita dupla.

## <a name="quality-updates"></a>Atualizações de qualidade

### <a name="project-operations-in-dataverse"></a>Project Operations no Dataverse

| Área de funcionalidades | Número de referência | Atualização de qualidade |
| --- | --- | --- |
| Faturação e Preços | 2240080 | O campo **Termos de pagamento** não deve ser duplicado na fatura pro forma. |
| Faturação e Preços | 2358236 | A correção de faturas tem de permitir correções que tenham linhas de preço zero. |
| Gestão de Recursos | 2410072 | Permita a configuração de um recurso que está atribuído à tarefa como gestor de projetos. |
| Faturação e Preços | 2430234 | Corrija um problema de cálculo de desempenho de custo. |
| Tempo e Despesa | 2436978 | Permite que a hora ser introduzida no formato hh:mm. |
| Faturação e Preços | 2448623 | Permita que as listas de preços sejam atualizadas depois de associadas a uma unidade organizacional. |
| Tempo e Despesa | 2460396 | Deixe que uma entrada de tempo seja eliminada limpando a célula. |
| Faturação e Preços | 2467386 | Permita que um projeto que tenha uma tarefa seja eliminado, mesmo quando a tarefa está associada a uma cotação ganha. |
| Tempo e Despesa | 2461744 | A vista **A minha aprovação com falhas** contém apenas as aprovações de projetos na fase **Submetido**. |
| Tempo e Despesa | 2464082 | Remova a ligação das aprovações do projeto para o conjunto de aprovações quando o estado de destino for correspondido. |
| Tempo e Despesa | 2468108 | O trabalho de Agendamento não deve definir um estado de **Processamento** para o conjunto de aprovações. |
| Tempo e Despesa | 2471503 | Elimine os conjuntos de aprovações com sete dias de idade. |
| Faturação e Preços | 2480687 | A referência da linha de cotação não deve ser removida quando um marco da linha de cotação é criado. |

### <a name="project-management-and-accounting-in-finance"></a>Gestão de projetos e contabilística em Finanças

| Área de funcionalidades | Número de referência | Atualização de qualidade |
| --- | --- | --- |
| Gestão de projetos e contabilística | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Os montantes de fornecedor retidos em transações de despesas de projeto não são apresentados na lista de transações. |
| Gestão de projetos e contabilística | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | A fatura do fornecedor interempresa é quebrada quando a integração de faturas de fornecedor é ativada. |
| Gestão de projetos e contabilística | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Os termos de pagamento nas faturas do projeto não funcionam como esperado. |
| Gestão de projetos e contabilística | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Quando a retenção de fornecedor é libertada, a publicação do voucher tem linhas adicionais que estão incorretas. |
| Gestão de projetos e contabilística | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Quando o diário de integração do Project Operations é publicado, falha devido a dimensões em falta de uma conta a que não está a ser publicada. |
| Gestão de projetos e contabilística | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | O separador **Projeto** não é editável numa fatura pendente de fornecedor quando a categoria de aprovisionamento é atribuída ao item. |
| Gestão de projetos e contabilística | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | O painel de navegação está em falta se não estiver a iniciar sessão no Project Operations Dataverse. |
| Gestão de projetos e contabilística | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Quando publica receitas de uma fatura de projeto num caso em que a retenção é aplicada, um erro ocorre porque as transações no voucher não têm um saldo correto. |
| Gestão de projetos e contabilística | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | A criação de uma estimativa depois de publicar uma proposta de fatura bloqueia as linhas de correção da importação. |
| Gestão de projetos e contabilística | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | A modificação de um registo de marco totalmente faturado não deve ser possível. |
| Viagem e Despesa | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Todos os relatórios de despesas estão visíveis quando procura uma categoria na aplicação móvel Despesas. |
| Viagem e Despesa | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Montantes incorretos das transações de fornecedores e imposto sobre vendas publicados a partir de uma despesa criada a partir de uma transação de cartão de crédito. |
| Viagem e Despesa | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Uma mensagem de aviso irrelevante ocorre quando atualiza a página **Relatório de despesas**. |
| Viagem e Despesa | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | O aprovador provisório errado é utilizado quando elimina um aprovador provisório e, em seguida, volta a submeter um relatório de despesas através do fluxo de trabalho. |
| Viagem e Despesa | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Ocorre um erro de publicação relacionado com a configuração de quilometragem. |
