---
title: Novidades de julho de 2022 - Project Operations para cenários baseados em recursos/não armazenados
description: Este artigo fornece informação sobre as atualizações de qualidade que estão disponíveis na versão de julho de 2022 do Microsoft Dynamics 365 Project Operations para cenários baseados em recursos/sem stock.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: e63b29741dbaa400a2176ff8b4c35c6d64dfeab4
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 09/02/2022
ms.locfileid: "9403966"
---
# <a name="whats-new-july-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades de julho de 2022 - Project Operations para cenários baseados em recursos/não armazenados

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

Este artigo aplica-se aos seguintes componentes e versões do Microsoft Dynamics 365 Project Operations:

- Project Operations num ambiente Dataverse, versão 4.44.0.22
- Gestão de projetos e contabilidade num ambiente do Dynamics 365 Finance versão 10.0.28

## <a name="project-operations-dual-write-maps-updates"></a>Atualizações de mapas de escrita dupla do Project Operations

Não existem atualizações para os mapas de escrita dupla do Project Operations nesta versão. Para obter uma lista atual e as versões dos mapas de escrita dupla do Project Operations, consulte [Versões do mapa de escrita dupla do Project Operations](../environment/resource-dual-write-maps.md).

Execute sempre a versão mais recente do mapa no seu ambiente e ative todos os mapas de tabelas relacionados à medida que atualiza a sua solução do Project Operations Dataverse e a versão da solução Finance. Algumas funcionalidades e capacidades podem não funcionar corretamente se a versão mais recente do mapa não estiver ativada. Pode ver a versão ativa do mapa na coluna **Versão** na página **Escrita Dupla**. Para ativar uma nova versão do mapa, selecione **Versões do mapa de tabela** , selecione a versão mais recente e, em seguida, guarde a versão selecionada. Se tiver personalizado um mapa de tabela de origem, volte a aplicar as alterações. Para mais informações, consulte [Gestão do ciclo de vida da aplicação](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se ocorrer um problema quando iniciar o mapa, siga as instruções na secção [Problema de colunas de tabela em falta em mapas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) do guia de resolução de problemas do serviço Escrita dupla.

## <a name="quality-updates"></a>Atualizações de qualidade

### <a name="project-operations-on-dataverse"></a>Project Operations no Dataverse

| Área de funcionalidades | Número de referência | Atualização de qualidade |
| --- | --- | --- |
| Implementação e Configuração | 2761472 | Foi resolvido um erro de instalação do Project Operations. |
| Faturação e Preços | 2746940 | O nome do item de subcontrato deve ter um comprimento máximo de 100 caracteres. |
| Faturação e Preços | 2739162 | Os clientes têm de conseguir ver os botões do friso na vista de grelha dos valores reais. |
| Planeamento e Monitorização de Projetos | 2730318 | Validação atualizada para caracteres não suportados no assunto do projeto. |
| Faturação e Preços | 2705361 | Os valores reais de vendas faturados do marco têm de ser incluídos nos campos de deteção de movimentos do projeto. |
| Faturação e Preços | 2675880 | Impeça que um projeto seja associado a um item de contrato que não seja baseado em trabalho. |
| Faturação e Preços | 2664396 | Se uma proposta de lista de preços for guardada sem uma asserção, tem de haver um erro que declara que a asserção não pode estar vazia. |
| Faturação e Preços | 2184019 | O separador **Faturação baseada em tarefas** não deve ser apresentado para projetos que não tenham contrato ou proposta de suporte. |
| Tempo e Despesa | 2754459 | Quando o agendamento recorrente do fluxo de cloudestiver inactivo, mostre o banner e ignore o processamento assíncrono. |
| Faturação e Preços | 2724391 | É lançada uma excepção errada quando falta uma regra de faturação dividida de contratos do projeto num valor de cliente. |
| Faturação e Preços | 2708638 | O registo não foi encontrado durante a pesquisa utilizando a pesquisa de grelha nas Utilizações de material e Aprovações para Utilizações de material.|
| Faturação e Preços | 2686977 | Impeça a validação da linha de fatura durante a criação da fatura. |
| Faturação e Preços | 2683032 | A cópia de funções e categorias carregáveis não ultrapassa os 5000 dados.|
| Faturação e Preços | 2673363 | A % de consumo de custos no Projeto é danificada quando as estimativas de Esforço e de Despesa e os valores reais existem para um projeto. |

### <a name="project-management-and-accounting-in-finance"></a>Gestão de projetos e contabilística em Finanças

Para obter informações sobre as correções de erros incluídas nesta atualização, inicie sessão no Microsoft Dynamics Lifecycle Services (LCS) e consulte o [Artigo BDC](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Funcionalidades ligadas por predefinição na próxima versão

A tabela que se segue lista as funcionalidades que estão ativadas por predefinição na versão 10.0.29. A maioria das funcionalidades que foram ativadas automaticamente podem ser desativadas na [Gestão de funcionalidades](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). No futuro, algumas funcionalidades que foram automaticamente ativadas podem ser removidas da Gestão de funcionalidades e tornar-se obrigatórias. Esta alteração assegura que os clientes estão a utilizar a funcionalidade atual, para que os melhoramentos possam basear-se na funcionalidade atual à medida que são adicionados. As funcionalidades nunca serão ativadas automaticamente em menos de um ano, a menos que sejam determinadas como essenciais.

| Nome da funcionalidade | Data de ativação | Funcionalidade adicionada | Estado de funcionalidade | Módulo |
| --- | --- | --- |--- |--- |
| Ativar o ajuste da transação de hora com base na alteração da alocação da regra de atribuição de fundos | 16 de setembro de 2022 | 7 de outubro de 2020 | Ativada por predefinição | Gestão de projetos e contabilística |
| Funcionalidade de reversão de fatura de pagamento antecipado da nota de encomenda | 16 de setembro de 2022 | 6 de outubro de 2021 | Ativada por predefinição | Gestão de projetos e contabilística |
| Eliminar linhas de proposta de fatura quando utilizar o Project Operations para cenários baseados em recursos/ sem stock | 16 de setembro de 2022 | 6 de outubro de 2021 | Ativada por predefinição | Gestão de projetos e contabilística |
| Ajustar a gestão contabilística numa transação do projeto publicada | 16 de setembro de 2022 | 10 de maio de 2020 | Ativada por predefinição | Gestão de projetos e contabilística |
| Ativar a configuração de gestão contabilística predefinida para o projeto | 16 de setembro de 2022 | 19 de fevereiro de 2020 | Ativada por predefinição | Gestão de projetos e contabilística |
| Ativar vários itens de contrato para um projeto | 16 de setembro de 2022 | 29 de junho de 2020 | Ativada por predefinição | Gestão de projetos e contabilística |
| Tornar o diário Hora do Projeto só de leitura se o estado da aprovação atual não permitir a edição | 16 de setembro de 2022 | 6 de outubro de 2021 | Ativada por predefinição | Gestão de projetos e contabilística |
| Ativar a sincronização de linhas de vendas a partir de linhas de compra quando as linhas de compra são atualizadas e o parâmetro de gestão de alterações na ordem de compra está ativado | 16 de setembro de 2022 | 7 de outubro de 2020 | Ativada por predefinição | Gestão de projetos e contabilística |
| Ativar o Project Operations no Dynamics 365 Customer Engagement | 16 de setembro de 2022 | 29 de junho de 2020 | Ativada por predefinição | Gestão de projetos e contabilística |
| Funcionalidade de reversão de transações de projeto | 16 de setembro de 2022 | 13 de julho de 2020 | Ativada por predefinição | Gestão de projetos e contabilística |

## <a name="features-that-become-mandatory-in-the-upcoming-release"></a>Funcionalidades que se tornam obrigatórias na próxima versão

A tabela que se segue lista as funcionalidades que serão obrigatórias a partir da versão 10.0.29.

| Nome da funcionalidade | Data de ativação | Funcionalidade adicionada | Estado de funcionalidade | Módulo |
| --- | --- | --- | --- | --- |
| Calcular o valor empenhado na origem de fundos sem arredondamento da taxa de câmbio | 16 de setembro de 2022 | 14 de junho de 2020 | Obrigatório | Gestão de projetos e contabilística |
| Ativar a publicação de ajustes do projeto com a mesma conta de razão que a transação original | 16 de setembro de 2022 | 14 de junho de 2020 | Obrigatório | Gestão de projetos e contabilística |
| Detalhe do montante do contrato do projeto cometido | 16 de setembro de 2022 | 31 de agosto de 2019 | Obrigatório | Gestão de projetos e contabilística |
| Ativar a ordenação por recurso durante a criação de propostas de fatura do projeto | 16 de setembro de 2022 | 31 de agosto de 2019 | Obrigatório | Gestão de projetos e contabilística |
