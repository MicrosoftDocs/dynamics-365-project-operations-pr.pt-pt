---
title: Novidades de abril de 2021 - Project Operations para cenários baseados em recursos/não armazenados
description: Este tópico fornece informações sobre as atualizações de qualidade disponíveis no lançamento de abril de 2021 da implementação leve do Project Operations para cenários baseados em recursos/não armazenados.
author: sigitac
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 07622ed798fd8d70e0ce5cc42297bd5056402474
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589118"
---
# <a name="whats-new-april-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades de abril de 2021 - Project Operations para cenários baseados em recursos/não armazenados

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

Este tópico aplica-se aos seguintes componentes e versões do Dynamics 365 Project Operations:

- Project Operations na versão 4.9.0.221 do ambiente Dataverse
- Gestão de projetos e contabilidade no ambiente do Dynamics 365 Finance versão 10.0.17

## <a name="features-included-in-this-release"></a>Funcionalidades incluídas nesta versão

Estão incluídas nesta versão as seguintes funcionalidades:

- Materiais não armazenados para projetos. As capacidades-chave incluem:
  - Estimar e definir preços de materiais não armazenados durante o ciclo de vendas de um projeto. Para mais informações ver [Configurar taxas de custo e de venda para produtos de catálogo - leve](../pro/pricing-costing/set-up-cost-sales-rates-catalog-products.md).
  - Monitorização da utilização de materiais não armazenados durante a entrega do projeto. Para obter mais informações, consulte [Registar utilização de material em projetos e tarefas de projeto](../material/material-usage-log.md).
  - A faturação utilizou custos materiais não armazenados. Para obter mais informações, consulte [Gerir o registo de tarefas pendentes de faturação](../proforma-invoicing/manage-billing-backlog.md).
  - Para obter informações sobre como configurar esta funcionalidade, consulte [Configurar materiais não armazenados e faturas pendentes do fornecedor](../procurement/configure-materials-nonstocked.md)
- Faturação baseada em tarefas: Adicionou a capacidade de associar tarefas de projeto com itens de contrato de projeto, submetendo-as assim ao mesmo método de faturação, frequência de fatura e clientes como os do item de contrato. Esta associação garante faturação precisa, contabilística, estimativa de receitas e reconhecimento para trabalhar de acordo com esta configuração em tarefas do projeto.
- As novas APIs no Dynamics 365 Dataverse permitem criar, atualizar e eliminar operações com **Entidades de agendamento**. Para mais informações, ver [Utilizar APIs de Agenda para realizar operações com entidades de agendamento](../project-management/schedule-api-preview.md).

## <a name="project-operations-dual-write-maps-updates"></a>Atualizações de mapas de escrita dupla do Project Operations

A lista que se segue mostra os mapas de dupla escrita que foram modificados ou adicionados na edição de abril 2021 do Project Operations.

| **Mapa da entidade** | **Versão atualizada** | **Comentários** |
| --- | --- | --- |
| Valores reais de integração com o Project Operations (msdyn\_actuals) | 1.0.0.14 | Mapa modificado para sincronizar os valores reais do projeto do material. |
| Entidade de integração com o Project Operations para estimativas de despesa (msdyn\_estimateslines) | 1.0.0.2 | Adicionada sincronização de item de contrato do projeto às aplicações Finanças e Operações para suporte de faturação baseada em tarefas. |
| Entidade de integração com o Project Operations para estimativas de horas (msdyn\_resourceassignments) | 1.0.0.5 | Adicionada sincronização de item de contrato do projeto às aplicações Finanças e Operações para suporte de faturação baseada em tarefas. |
| Tabela de integração do Project Operations para estimativas de materiais (msdyn\_estimatelines) | 1.0.0.0 | Novo mapa de tabela para sincronizar estimativas de material a partir do Dataverse para as aplicações de Finanças e Operações. |
| Entidade de exportação de faturas de projeto de integração de projetos do Project Operations (msdyn\_projectvendorinvoices) | 1.0.0.0 | Novo mapa de tabela para sincronizar cabeçalhos das faturas de fornecedor a partir das aplicações de Finanças e Operações para o Dataverse. |
| Entidade de exportação de linhas de faturas de projeto de integração de projetos do Project Operations (msdyn\_projectvendorinvoicelines) | 1.0.0.0 | Novo mapa de tabela para sincronizar linhas das faturas de fornecedor a partir das aplicações de Finanças e Operações para o Dataverse. |

Deve sempre executar a versão mais recente do mapa no seu ambiente e ativar todos os mapas de tabelas relacionados à medida que atualiza a sua solução do Project Operations Dataverse e a versão da solução Operations. Certas funcionalidades e capacidades podem não funcionar corretamente se a versão mais recente do mapa não estiver ativada. Pode ver a versão ativa do mapa na coluna **Versão** na página **Escrita Dupla**. Pode ativar uma nova versão do mapa selecionando **Versões do mapa de tabela** , selecionando a versão mais recente e, em seguida, guardar a versão selecionada. Se tiver personalizado um mapa de tabela fora da caixa, reaplique as alterações. Para mais informações, consulte [Gestão do ciclo de vida da aplicação](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se encontrar algum problema com o início do mapa, siga as instruções na secção [Problema com colunas de tabelas desaparecidas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) do guia de resolução de problemas de escrita dupla.

## <a name="quality-updates"></a>Atualizações de qualidade

### <a name="project-operations-in-dynamics-365-dataverse"></a>Project Operations no Dynamics 365 Dataverse

| **Área de funcionalidades** | **Número de referência** | **Atualização de qualidade** |
| --- | --- | --- |
| Faturação e preços | 2124532 | O botão **Fatura correta** é apresentado numa fatura pró-forma quando o valor do retentor ou o valor do retentor aplicado estão presentes na fatura original. O botão é apresentado apenas para ambientes com a versão 10.0.19 ou superior. |
| Faturação e preços | 2224568 | Lógica adicional para permitir personalizações que envolvem invocar o plug-in de confirmação da fatura. |
| Faturação e preços | 2101098 | Melhorou a lógica dos campos predefinidos para fatura pró-forma: **Fatura para endereço**, **Fatura a nome** e **Termos de pagamento** estão agora por defeito a partir do registo correspondente do cliente do contrato de projeto. |
| Faturação e preços | 2021413 | Atualizou os campos de **Custos reais** e **Vendas** na entidade **Tarefa** para incluir valores de venda de despesas não faturadas e faturadas em tarefas. |
| Faturação e preços | 2182110 | Ao copiar um contrato de projeto, o item de contrato ID é regenerado no contrato de projeto de destino para garantir que é único. |
| Gestão de oportunidades | 2186741 | Validações adicionais para garantir que o campo **Origem** e **tipo de transação** não podem ser atualizados nos detalhes da linha de proposta existentes. |
| Gestão de oportunidades | 2191353 | Os marcos não devem ser criados num item de contrato de tempo e material. |
| Gestão de oportunidades | 2216956 | Problemas solucionados com **Atualizar preços**. |
| Planeamento e deteção de movimentos | 2182979 | A função de cópia do projeto melhorou para garantir que as linhas de estimativa de despesas são copiadas do projeto original. |
| Planeamento e deteção de movimentos | 2184144 | A função de cópia do projeto melhorou para garantir que o nome da posição do recurso é copiado do projeto original. |
| Planeamento e deteção de movimentos | 2184799 | Cópia do projeto: Controlo apertado para garantir que a data de início estimada não pode ser alterada enquanto a cópia está em andamento. |
| Planeamento e deteção de movimentos | 2185134 | Cópia do projeto: A data de início estimada do projeto de destino está marcada para a data de hoje. |
| Planeamento e deteção de movimentos | 2196373 | Cópia do projeto: Certifique-se de que os registos do gestor do projeto e dos membros da equipa não são duplicados na equipa do projeto. |
| Planeamento e deteção de movimentos | 2211833 | Cópia do projeto: As atribuições de recursos são copiadas da tarefa do projeto de origem para o projeto de destino. |
| Planeamento e deteção de movimentos | 2186541 | Problemas solucionados na grelha de **Estimativas** ao agrupar por recurso. |
| Planeamento e deteção de movimentos | 2166906 | A categoria de transação a partir de uma tarefa deve ser copiada para a entidade de **Atribuição de recursos**. |
| Gestão de Recursos | 2125362 | Problemas solucionados com a criação de um membro genérico da equipa usando um método de atribuição baseado em horas. |
| Tempo e Despesa | 2113603 | Corrigiu o problema relacionado com a personalização com a remoção de atributos da página **Entrada de tempo**. O sistema verifica agora se o atributo existe na página antes de aceder aos mesmos utilizando um script. |
| Tempo e Despesa | 2204377 | As folhas de tempo copiadas devem aparecer automaticamente quando selecionar **Copiar semana** durante a entrada de tempo. |
| Tempo e Despesa | 2209059 | O campo **Estado** pode ser editado para entradas de tempo do Dynamics 365 Field Service. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Gestão de projetos e contabilidade no Dynamics 365 Finance

| **Área de funcionalidades** | **Número de referência** | **Atualização de qualidade** |
| --- | --- | --- |
| Gestão de projetos e contabilística | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | A eliminação da estimativa inversa não está a funcionar na secção **Periódica**.  |
| Gestão de projetos e contabilística | [509773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509773) | A função de **Ajustamento contabilístico** cria um problema com contas de livro razão que têm **Não permitir a entrada manual** selecionada. |
| Gestão de projetos e contabilística | [510728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=5109728) | Adicionou lógica comercial para processar faturas de correção, incluindo o valor do retentor ou o valor do retentor aplicado. |
| Gestão de projetos e contabilística | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | WIP-a publicação do valor de vendas na faturação do projeto interempresa escolhe uma conta inesperada. |
| Gestão de projetos e contabilística | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | Ao trabalhar com retentores em Operações de Projeto, alterar o projeto de incumprimento de um contrato após os pagamentos antecipados serem faturados causa problemas com deduções recebidas. |
| Gestão de projetos e contabilística | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | No Project Operations, a remoção de um projeto de um contrato deve repor o projeto padrão do contrato, se for necessário. |
| Gestão de projetos e contabilística | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | No Project Operations, as linhas de despesas erradas mostram na lista **Adicionar linha** na fatura interempresa. |
| Gestão de projetos e contabilística | [543968](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543968) | No Project Operations, a página **Contrato de compra** não é visível nas entidades legais de finanças que estejam integradas com o Project Operations. |
| Gestão de projetos e contabilística | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | Devido a um erro de integração de Dataverse, não se pode converter uma proposta a ganhar no Project Operations. |
| Gestão de projetos e contabilística | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | **ProjCDSProjectContractEntity** pode definir o endereço de fatura de fonte de financiamento de um cliente diferente.  |
| Gestão de projetos e contabilística | [557376](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557376) | No Project Operations não são selecionadas dimensões quando cria uma fatura de registo para uma transação. |
| Viagem e despesa | [441256](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441256) | O saldo adiantado não é atualizado para um relatório de despesas se for aprovado e colocado linha a linha. |
| Viagem e Despesa | [482041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482041) | Os impostos para relatórios de despesas interempresa não são calculados corretamente. |
| Viagem e Despesa | [483469](https://fix.lcs.dynamics.com/Issue/Details/?bugId=483469) | Campos adicionais relacionados com projetos são exibidos na página de **relatórios de despesas interempresa** reimaginadas. |
| Viagem e Despesa | [486592](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486592) | Ocorre uma mensagem de erro incorreta nos recibos do cabeçalho dos relatórios de despesas. |
| Viagem e Despesa | [487971](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487971) | Um relatório de despesas é incorretamente publicado num cenário interempresa se o imposto de venda for colocado na entidade jurídica de destino. |
| Viagem e Despesa | [505696](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505696) | As datas de submissão do relatório não são impressas em relatórios de despesas aprovados. |
| Viagem e Despesa | [508726](https://fix.lcs.dynamics.com/Issue/Details/?bugId=508726) | Os campos **Data aprovada** e **Data rejeitada** não são preenchidos após a aprovação de uma despesa. |
| Viagem e Despesa | [509913](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509913) | Uma requisição de viagem criada para um trabalhador pode ser usada para o relatório de despesas de outro trabalhador. |
| Viagem e Despesa | [518186](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518186) | As categorias de despesas são bloqueadas quando se adiciona uma nova linha de despesas. |
| Viagem e Despesa | [520914](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520914) | Separar em itens linhas de relatório de despesas já divididas resulta numa publicação incompleta do voucher Contas A pagar\Livro razão geral e interrompe o Explorador de Fontes Contabilísticas porque **TRVEXPTRANS. SOURCEDOCUMENTLINE** é duplicado. |
| Viagem e Despesa | [521943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521943) | A política de requisição de viagem não está a funcionar como esperado. |
| Viagem e Despesa | [522567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522567) | O nome da conta do fornecedor não aparece nas transações de projetos publicadas para relatórios de despesas. |
| Viagem e Despesa | [525106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525106) | No Project Operations não é possível aprovar o tempo com uma tarefa para um projeto de interempresa. |
| Viagem e Despesa | [526336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=526336) | A categoria de devolução antecipada de caixa não está a atualizar os saldos antecipados de caixa quando registados. |
| Viagem e Despesa | [527218](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527218) | O preço de venda é calculado incorretamente em relatórios de despesas que foram criados em moeda estrangeira utilizando transações de cartões de crédito importados e estão associados a um projeto. |
| Viagem e Despesa | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | Reverteu a entidade de dados **TrvRequisitionLine** e o índice único associado. |
| Viagem e Despesa | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | Instrumentação adicionada à geração **SOURCEDOCUMENTLINE**. |
| Viagem e Despesa | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | É apresentado um diário de sublivro razão num cenário interempresa se o imposto de venda for colocado na entidade jurídica de destino. |
| Viagem e Despesa | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | No Project Operations, as estimativas de despesas não são suprimidas das Finanças quando são eliminadas de Dataverse. |
| Viagem e Despesa | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | Quando uma categoria de despesas é uma categoria não-projeto, as dimensões financeiras selecionadas na página **Despesas** não são copiadas para o relatório de despesas. |
