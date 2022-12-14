---
title: Novidades de outubro de 2022 - Project Operations para cenários baseados em recursos/itens não existentes em stock
description: Este artigo fornece informação sobre as atualizações de qualidade que estão disponíveis na versão de outubro de 2022 do Microsoft Dynamics 365 Project Operations para cenários baseados em recursos/sem stock.
author: ramagadu
ms.date: 11/17/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 392a12d6954c2390e5bad8e8e36cf58b7a1d0749
ms.sourcegitcommit: 1f162707ac342343fb5390fb9ae335e4cea4f3f2
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806628"
---
# <a name="whats-new-october-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades de outubro de 2022 - Project Operations para cenários baseados em recursos/itens não existentes em stock

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

Este artigo aplica-se aos seguintes componentes e versões do Microsoft Dynamics 365 Project Operations:

- Project Operations num ambiente Dataverse, versão 4.57.0.176
- Gestão de projetos e contabilidade num ambiente do Dynamics 365 Finance versão 10.0.30

## <a name="features-included-in-this-release"></a>Funcionalidades incluídas nesta versão

| Área de funcionalidades | Nome da funcionalidade | Mais informações |
| --- | --- | --- |
| Planeamento e Monitorização de Projetos | **Agendamento Externo do Project Operations**<br>O modo de agendamento externo permite aos clientes criar, atualizar e eliminar entidades de forma nativa relacionadas com as estruturas hierárquicas de trabalho (WBS) utilizando APIs do Dataverse nativas, sem os limites atuais impostos pelo Project for the Web. | [Agendamento Externo](/dynamics365/project-operations/project-management/external-scheduling) |
| Implementação e Configuração | <p>**Permitir que os clientes escolham o tipo de implementação**<br>As atualizações condicionados por produto (PDUs) do Project Operations são utilizadas para instalar automaticamente uma solução de Escrita dupla do Project Operations quando as soluções de Escrita dupla central e de orquestração estão instaladas no ambiente.</p><p>Esta caraterística introduz um novo parâmetro **Comportamento da atualização de versão da solução** nos parâmetros do Projeto. Quando este parâmetro estiver definido como **Só Lite**, as PDUs deixarão de instalar automaticamente uma solução de Escrita dupla do Project Operations, mesmo que as soluções de Escrita dupla central e de orquestração estejam instaladas no ambiente. Este comportamento irá beneficiar clientes que pretendam utilizar soluções de Escrita dupla para integrar ordens de venda em aplicações de finanças e operações, mas que pretendem utilizar o Project Operations num modo Lite (ou seja, sem integração com aplicações de finanças e operações).</p> | |
| Faturação e Preços | <p>**Conversão de moeda para transação de venda não faturada de despesas em Ambientes integrados**<br>Para clientes que utilizem o Project Operations integrado com aplicações de finanças e operações (ou seja, no tipo de implementação de recurso/não stock), as taxas de câmbio são normalmente tratadas em aplicações de finanças e operações. No entanto, se for necessário definir um preço para a categoria de despesas utilizando o método de cálculo de preços "ao custo" ou "margem de lucro para além do custo" quando o cliente é faturado, a taxa de câmbio que é utilizada para calcular o montante de vendas utiliza a taxa de câmbio no Dataverse, não as taxas de câmbio das aplicações de finanças e operações.</p><p>Esta caraterística introduz um novo parâmetro **Comportamento da conversão de moeda** nos parâmetros do Projeto. Quando este parâmetro está definido como **Expandido com contingência**, os montantes de vendas não faturados em transações de despesas são calculados utilizando as taxas de câmbio das aplicações de finanças e operações.</p> | |

## <a name="project-operations-dual-write-maps-updates"></a>Atualizações de mapas de escrita dupla do Project Operations

Não existem atualizações para os mapas de escrita dupla do Project Operations nesta versão. Para obter uma lista atual e as versões dos mapas de escrita dupla do Project Operations, consulte [Versões do mapa de escrita dupla do Project Operations](../environment/resource-dual-write-maps.md).

Execute sempre a versão mais recente do mapa no seu ambiente e ative todos os mapas de tabelas relacionados à medida que atualiza a sua solução do Project Operations Dataverse e a versão da solução Finance. Algumas funcionalidades e capacidades podem não funcionar corretamente se a versão mais recente do mapa não estiver ativada. Pode ver a versão ativa do mapa na coluna **Versão** na página **Escrita Dupla**. Para ativar uma nova versão do mapa, selecione **Versões do mapa de tabela** , selecione a versão mais recente e, em seguida, guarde a versão selecionada. Se tiver personalizado um mapa de tabela de origem, volte a aplicar as alterações. Para mais informações, consulte [Gestão do ciclo de vida da aplicação](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se ocorrer um problema quando iniciar o mapa, siga as instruções na secção [Problema de colunas de tabela em falta em mapas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) do guia de resolução de problemas do serviço Escrita dupla.

## <a name="quality-updates"></a>Atualizações de qualidade

### <a name="project-operations-on-dataverse"></a>Project Operations no Dataverse

| Área de funcionalidades | Número de referência | Atualização de qualidade |
| --- | --- | --- |
| Faturação e Preços | 2316317 | O sistema permite a criação de faturas sem transações faturáveis. |
| Faturação e Preços | 2737300 | Valide a disponibilidade do campo **Cliente** antes de o formulário ser acedido. |
| Faturação e Preços | 2744948 | Adicione um verificação nula para o método Faturação. |
| Faturação e Preços | 2763515 | Identificador do erro de referência nula quando o contrato de vendas da fatura está em falta. |
| Faturação e Preços | 2844301 | A criação de faturas em lote falha devido a um erro. |
| Faturação e Preços | 2845869 | Armazenamento incorreto do Serviço da Organização. |
| Faturação e Preços | 2853729 | Os detalhes da Função e do Preço são atualizados quando o tipo Faturação é modificado. |
| Faturação e Preços | 2940350 | Quando o preço dos valores reais é definido, apenas as listas de preços devem ser introduzidas automaticamente. |
| Implementação e Configuração | 3001206 | A entidade msdyn\_replaylogheader está a impedir atualizações de versão de Organizações de Clientes. |
| Gestão de oportunidades | 2755582 | Identificador de exceções de referência nula no Assistente da Regra de Divisão de Faturação. |
| Gestão de oportunidades | 2761477 | Quando a faturação dividida, a eliminação de um marco (cabeçalho) deixa marcos órfãos. |
| Gestão de oportunidades | 2767595 | Quando um registo de utilização de materiais é aberto no formulário principal, o recurso Reservável para o registo é alterado para o utilizador atualmente com sessão iniciada. |
| Planeamento e Monitorização de Projetos | 2790384 | O tempo limite do OperationSet Pendente é demasiado curto. |
| Planeamento e Monitorização de Projetos | 2957840 | Não é possível guardar tarefas e não é possível adicionar colunas à página **Tarefas** no Project Operations Integrado. |
| Gestão de Recursos | 2751560 | Unidades de Organização Preferenciais Inconsistentes em Requisito de Recursos. |
| Subcontratos | 2853245 | A correspondência de valores reais da Linha de Fatura do Fornecedor não atualiza o estado de verificação se um item de contrato já estiver associado à linha de fatura do fornecedor. |
| Subcontratos | 2907231 | A fase do processo de faturas do fornecedor não pode avançar. |
| Tempo e Despesa | 2867363 | Os registos não saem da vista Ausências/Férias para Aprovação quando são colocadas em fila para aprovação. |
| Tempo e Despesa | 2894405 | TESA: o diretório POC não utilizado está a causar problemas de conformidade. |

### <a name="project-management-and-accounting-in-finance"></a>Gestão de projetos e contabilística em Finanças

Para obter informações sobre as correções de erros incluídas nesta atualização, inicie sessão no Microsoft Dynamics Lifecycle Services e consulte o [Artigo BDC](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468).
