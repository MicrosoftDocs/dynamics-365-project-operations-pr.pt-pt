---
title: Novidades de junho de 2021 - Project Operations para cenários baseados em recursos/não armazenados
description: Este artigo fornece informações sobre as atualizações de qualidade disponíveis na versão de junho de 2021 do Project Operations para cenários baseados em recursos/itens não existentes em stock.
author: sigitac
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fd745107fa6d50882ebea302d3d2ae0de21b79ad
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028276"
---
# <a name="whats-new-june-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades de junho de 2021 - Project Operations para cenários baseados em recursos/não armazenados

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

Este artigo aplica-se aos seguintes componentes e versões do Dynamics 365 Project Operations:

- Project Operations na versão de ambiente 4.11.0.156 ou 4.11.0.164 do Dynamics 365 Dataverse.
- Gestão de projetos e contabilidade em ambientes de aplicações de finanças e operações, versão 10.0.19.

## <a name="features-included-in-this-release"></a>Funcionalidades incluídas nesta versão

Estão incluídas nesta versão as seguintes funcionalidades:

- Capacidade para eliminar [Linhas da proposta de fatura do projeto para cenários de ajuste](../invoicing/correct-project-invoice-proposals.md).
- As linhas de despesas discriminadas refletem os nomes das subcategorias no relatório de despesas [Relatórios de Despesas Reinventados-Novas Funcionalidades](../expense/expense-reports-reimagined.md#new-features).
- O método de pagamento está disponível no novo painel de despesas ao criar uma nova despesa.
- Disponibilidade geral das APIs de Agenda do Projeto. Esta nova funcionalidade permite aos clientes executar programaticamente as operações para criar, atualizar e eliminar em tarefas de projeto, atribuições de recursos, dependências de tarefas e registos de membros da equipa do projeto. Para mais informações, consulte [Utilizar APIs de Agenda do Projeto para executar operações com as entidades de Agendamento](../project-management/schedule-api-preview.md).

## <a name="project-operations-dual-write-maps-updates"></a>Atualizações de mapas de escrita dupla do Project Operations

Não existem atualizações para os mapas de escrita dupla do Project Operations nesta versão. 

Para obter uma lista atual e as versões dos mapas de escrita dupla do Project Operations, consulte [Versões do mapa de escrita dupla do Project Operations](../environment/resource-dual-write-maps.md).

Execute sempre a versão mais recente do mapa no seu ambiente e ative todos os mapas de tabelas relacionados à medida que atualiza a sua solução do Project Operations Dataverse e a versão da solução das aplicações de finanças e operações. Certas funcionalidades e capacidades podem não funcionar corretamente se a versão mais recente do mapa não estiver ativada. Pode ver a versão ativa do mapa na página **Escrita dupla** na coluna **Versão**. Ative uma nova versão do mapa ao selecionar **Versões do mapa de tabelas**, selecionar a versão mais recente e, em seguida, guardar a versão selecionada. Se tiver personalizado um mapa de tabela fora da caixa, reaplique as alterações. Para mais informações, consulte [Gestão do ciclo de vida da aplicação](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se encontrar um problema ao iniciar o mapa, siga as instruções na secção [Problema de colunas de tabela em falta nos mapas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) do guia de resolução de problemas de escrita dupla.

## <a name="quality-updates"></a>Atualizações de qualidade

### <a name="project-operations-on-dataverse"></a>Project Operations no Dataverse

| **Área de funcionalidades** | **Número de referência** | **Atualização de qualidade** |
| --- | --- | --- |
| Faturação e Preços | 2281417 | Foi corrigido o problema relativa à falha da ação de criação automática de faturas através da agenda de faturação. |
| Faturação e Preços | 2287835 | Desempenho melhorado da confirmação de faturas. |
| Gestão de oportunidades | 2222555 | A exigibilidade das estimativas de material tem de ser copiada corretamente para os detalhes da linha de proposta ao utilizar **Importar a partir da Estimativa do Projeto**. |
| Gestão de oportunidades | 2223427 | As personalizações são agora permitidas para a ação **GenerateRetainersFromRetainerScheduleOptions**. |
| Gestão de oportunidades | 2277528 | Cálculo do valor de marco de faturação fixo para os itens de contrato do projeto com vários clientes. |
| Planeamento e Monitorização de Projetos | 2226110 | Foi corrigido o problema intermitente com a função **Gerar Requisito** na grelha **Equipa do Projeto**. |
| Planeamento e Monitorização de Projetos | 2208109 | Os utilizadores não podem criar um projeto numa moeda com tarefas relacionadas noutra moeda. |
| Planeamento e Monitorização de Projetos | 2258228 | A lista de campos permitidos para modificar com entidades **Agendamento** que utilizam a API de Agenda foi atualizada. |
| Planeamento e Monitorização de Projetos | 2293989 | O idioma correto e as definições regionais têm de ser transmitidos para a grelha **Tarefas do Projeto**. |
| Gestão de Recursos | 2220493 | Foi corrigida a experiência de utilizador na grelha **Tarefa** ao marcar rapidamente um pedido de recurso como concluído. |
| Gestão de Recursos | 2330496 | Foi corrigido o problema de carregamento **Quadro da Agenda**. (A atualização da qualidade está disponível na versão 4.11.0.164) |
| Tempo e Despesa | 2194431 | A grelha **Entrada de hora** tem de respeitar o início da semana conforme definido nas **Definições de sistema**. |
| Tempo e Despesa | 2277311 | Depois de eliminar o valor numa célula na grelha **Entrada de hora**, o cursor mantém-se na grelha. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Gestão de projetos e contabilidade no Dynamics 365 Finance

| Área de funcionalidades | Número de referência | Atualização de qualidade |
| --- | --- | --- |
| Gestão de projetos e contabilística | [552976](https://fix.lcs.dynamics.com/Issue/Details/?bugId=552976) | **Notas de formulário** e **Configuração de formulário** não estão visíveis em **Configuração da gestão de projetos** nas entidades jurídicas do Finance que estão integradas com o Project Operations. |
| Gestão de projetos e contabilística | [527970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527970) | A descrição predefinida para o IVA está em branco quando **Tipo de lançamento** = **Imposto sobre vendas** para os vouchers de faturas do projeto. |
| Gestão de projetos e contabilística | [565089](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565089) | As transações duplas são publicadas quando a faturação baseada em tarefas é utilizada no Dataverse com integração com o Project Operations. |
| Gestão de projetos e contabilística | [566869](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566869) | A percentagem concluída no reconhecimento de receitas é incorreta ao utilizar a integração do Project Operations. |
| Gestão de projetos e contabilística | [568107](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568107) | A acumulação de receitas é duplicada numa fatura de fornecedor pendente num cenário integrado do Project Operations. |
| Gestão de projetos e contabilística | [572370](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572370) | Não é possível lançar o diário de integração quando a regra do perfil de receitas está definida para a configuração **Grupo**. |
| Gestão de projetos e contabilística | [573596](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573596) | Uma fatura de compra não pode ser lançada para as notas de encomenda do projeto que tenham linhas com várias unidades de medida. |
| Gestão de projetos e contabilística | [573637](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573637) | A dimensão financeira predefinida num projeto não pode ser atualizada através da entidade de dados **V2** dos projetos. |
| Gestão de projetos e contabilística | [577211](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577211) | O processo em lote para criar estimativas do projeto demora demasiado tempo a concluir. |
| Gestão de projetos e contabilística | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | Eliminar um contrato também elimina o endereço associado ao cliente. |
| Viagem e despesa | [514930](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514930) | A condição de fluxo de trabalho de aprovação do relatório de despesas não é avaliada corretamente. |
| Viagem e despesa | [519304](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519304) | A política do relatório de despesas não está a avaliar corretamente o ID de projeto. |
| Viagem e despesa | [522463](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522463) | A ação **Dividir em pessoal para as transações de despesas entre empresas** não está a funcionar corretamente. |
| Viagem e despesa | [534702](https://fix.lcs.dynamics.com/Issue/Details/?bugId=534702) | As justificações da linha do relatório de despesas são eliminadas acidentalmente quando determinadas requisições de viagem são eliminadas. Isto ocorre quando o recID do relatório de despesas e a requisição de viagem são os mesmos. |
| Viagem e despesa | [544368](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544368) | Existe um problema na aplicação móvel Expense quando o campo **ID do Projeto** é obrigatório nas políticas de relatórios de despesa. |
| Viagem e despesa | [545331](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545331) | As despesas entre empresas associadas a um projeto não podem ser editadas. Em vez disso, é apresentada a seguinte mensagem de erro: "Referência de objeto não definida para uma instância de um objeto". |
| Viagem e despesa | [548659](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548659) | Após o lançamento do relatório de despesas, a moeda e o montante errados são listados no razão auxiliar do banco. |
| Viagem e despesa | [558336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558336) | Foram introduzidas melhorias na funcionalidade *Eliminar transações do cartão de crédito*.  |
| Viagem e despesa | [525070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525070) | O imposto sobre vendas incluído num relatório de despesas não é calculado de forma consistente quando é especificada uma moeda de relatório diferente numa entidade jurídica. |
| Viagem e despesa | [527779](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527779) | O desempenho é afetado ao adicionar uma nova despesa de viagem em dinheiro. |
| Viagem e despesa | [537841](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537841) | As regras da política de despesas não são acionadas num relatório de despesas. |
| Viagem e despesa | [566386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566386) | Carregar uma nova categoria partilhada através da Infraestrutura de Gestão de Dados remove todas as subcategorias para todas as categorias partilhadas. |
| Viagem e despesa | [574131](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574131) | Quando cria uma linha de despesa e, em seguida, seleciona uma categoria, aparece a seguinte mensagem de erro: "A combinação do DOM do grupo de impostos sobre vendas e o STD do grupo de impostos sobre vendas de artigos não é válida". |
| Viagem e despesa | [574900](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574900) | Existem problemas de sincronização na aplicação móvel Expense. |
