---
title: Novidades de maio de 2021 - Project Operations para cenários baseados em recursos/não armazenados
description: Este artigo fornece informações sobre as atualizações de qualidade disponíveis na versão de maio de 2021 do Project Operations para cenários baseados em recursos/itens não existentes em stock.
author: sigitac
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 425b0eb78b5f03d4b0da9a792d6e33fc96adf060
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930424"
---
# <a name="whats-new-may-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades de maio de 2021 - Project Operations para cenários baseados em recursos/não armazenados

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

Este artigo aplica-se aos seguintes componentes e versões do Dynamics 365 Project Operations:

- Project Operations no ambiente do Dynamics 365 Dataverse, versão 4.10.0.186
- Gestão de projetos e contabilidade em ambientes de aplicações de Finanças e Operações versão 10.0.18

## <a name="features-included-in-this-release"></a>Funcionalidades incluídas nesta versão

Estão incluídas nesta versão as seguintes funcionalidades:

- [Modos de agendamento](../project-management/scheduling-modes.md): Os gestores de projeto podem definir se um projeto deve ser gerido utilizando o modo de agendamento de duração fixa, trabalho fixo ou unidades fixas.
- [Configurar quilometragem utilizando níveis de taxa de quilometragem](../expense/set-up-mileage.md): Atualizar os níveis de taxa de quilometragem para relatórios de despesas dos colaboradores.

## <a name="project-operations-dual-write-maps-updates"></a>Atualizações de mapas de escrita dupla do Project Operations

A lista que se segue mostra os mapas de escrita dupla que foram modificados ou adicionados na edição de maio 2021 do Project Operations.

| Mapa da entidade | Versão atualizada | Comentários |
| --- | --- | --- |
| Origem de financiamento do projeto (msdyn\_projectcontractsplitbillingrules) | 1.0.0.2 | Sincronização dos termos de pagamento do cliente do contrato de projeto. |
| Proposta de fatura do projeto V2 (faturas) | 1.0.0.3 | Sincronização dos termos de pagamento da fatura pró-forma. |
| Entidade de exportação de linhas de faturas de projeto de integração de projetos do Project Operations (msdyn\_projectvendorinvoicelines) | 1.0.0.1 | Atualizações de qualidade |
| Projetos V2 (msdyn\_projects) | 1.0.0.2 | Atualizações de qualidade |

Execute sempre a versão mais recente do mapa no seu ambiente e ative todos os mapas de tabelas relacionados à medida que atualiza a sua solução do Project Operations Dataverse e a versão da solução das aplicações de finanças e operações. Certas funcionalidades e capacidades podem não funcionar corretamente se a versão mais recente do mapa não estiver ativada. Pode ver a versão ativa do mapa na coluna **Versão** na página **Escrita Dupla**. Para ativar uma nova versão do mapa, selecione **Versões do mapa de tabela** , selecione a versão mais recente e, em seguida, guarde a versão selecionada. Se tiver personalizado um mapa de tabela fora da caixa, reaplique as alterações. Para mais informações, consulte [Gestão do ciclo de vida da aplicação](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se encontrar algum problema com o início do mapa, siga as instruções na secção [Problema com colunas de tabelas desaparecidas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) do guia de resolução de problemas de escrita dupla.

## <a name="quality-updates"></a>Atualizações de qualidade

### <a name="project-operations-on-dataverse"></a>Project Operations no Dataverse

| **Área de funcionalidades** | **Número de referência** | **Atualização de qualidade** |
| --- | --- | --- |
| Faturação e Preços | 2227635 | Os valores nos campos **Grupo de unidades** e **Unidade** predefinidos a partir do produto na grelha **Estimativas de Material**. |
| Faturação e Preços | 2234127 | O campo **ID da Tarefa** integra-se agora corretamente nos valores reais do projeto do Dataverse quando uma fatura do fornecedor é publicada. |
| Faturação e Preços | 2235564 | Guardar a entrada de diário garante que a moeda apresentada na entrada de diário corresponde à moeda predefinida da linha após guardar. |
| Faturação e Preços | 2246671 | Efetuar uma transação não faturável durante a faturação inverte o registo original de vendas não faturadas e cria um novo registo de vendas não faturadas como não faturáveis. |
| Faturação e Preços | 2264042 | A correção válida da fatura não deve ser bloqueada se houver um detalhe de correção de fatura que não seja válido no ambiente. |
| Faturação e Preços | 2146367 | O mapeamento de escrita dupla do cabeçalho da fatura do projeto é alargado para incluir os termos de pagamento. |
|   Gestão de oportunidades | 2086888 | Não adicione funções nem categorias que estão desativadas antes de copiar uma proposta para funções e categorias faturáveis de uma proposta recentemente copiada. |
|   Gestão de oportunidades | 2234376 | Os campos só de leitura estão acinzentados na grelha **Estimativas de Material**. |
|   Gestão de oportunidades | 2238337 | Uma proposta baseada num contacto pode ser guardada mesmo que não esteja associada a uma lista de preços do projeto. |
|   Gestão de oportunidades | 2239810 | Fechar uma proposta como perdida também fecha o projeto associado e cancela quaisquer reservas. |
| Planeamento e Monitorização de Projetos | 2099559 | Adicionou validações adicionais para o funcionamento do sistema antes da abertura da grelha **Tarefas do projeto**. |
| Planeamento e Monitorização de Projetos | 2178987 | Corrigiu um erro transitório que ocorre ao selecionar **Fase Seguinte** na página **Projeto**. |
| Gestão de Recursos | 2224817 | A funcionalidade para alargar as reservas está predefinida para o estado correto da reserva. |
| Entrada de hora | 2202476 | A página **Entrada de Hora** utiliza agora o controlo da grelha de reação e corrige problemas como o desalinhamento da grelha. |
| Entrada de hora | 2223377 | A entrada de hora é oculta na secção **Relacionado** na página **Recurso Reservado** para evitar confusões com a capacidade de utilização. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Gestão de projetos e contabilidade no Dynamics 365 Finance

| Área de funcionalidades | Número de referência | Atualização de qualidade |
| --- | --- | --- |
| Gestão de projetos e contabilística | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | Project Operations para cenários baseados no Recurso: Não pode converter uma proposta a ganhar por causa de um erro de integração. |
| Gestão de projetos e contabilística | [546604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546604) | Project Operations: Ocorre um erro quando tenta associar uma linha de contrato a um ID de Projeto devido à verificação de itens de contrato sobrepostas e tipos de transação. |
| Gestão de projetos e contabilística | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | **ProjCDSProjectContractEntity** define o endereço de fatura de origem de financiamento de um cliente diferente. |
| Viagem e Despesa | [480451](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480451) | Pode ocorrer um erro de publicação relacionado com a configuração da quilometragem. |
| Viagem e Despesa | [522084](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522084) | A funcionalidade **Dividir a pessoal** não está a funcionar para transações de despesas em moeda estrangeira. |
| Viagem e Despesa | [523938](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523938) | Os valores da lista pendente de categorias de despesas estão a apresentar categorias incorretas para os delegados, independentemente de serem um recurso. |
| Viagem e Despesa | [539266](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539266) | Não é possível guardar um relatório de despesas interempresa por causa de um erro de **validação de Recurso/Categoria**. |
| Viagem e Despesa | [532610](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532610) | O cálculo errado da taxa de quilometragem no relatório de despesas tem linhas divididas. |
| Viagem e Despesa | [537404](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537404) | Não é possível publicar um relatório de despesas interempresa quando o imposto de venda está incluído e o tipo de conta offset no método de pagamento é **Trabalhador**. |
| Viagem e Despesa | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | A entidade de dados **TrvRequisitionLine** da reversão e o índice único estão associados. |
| Viagem e Despesa | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | O relatório de despesas suporta a criação e atualização da linha de documentos de origem. |
| Viagem e Despesa | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | É apresentado um diário de sublivro razão incorreto num cenário interempresa se o imposto de venda for colocado na entidade jurídica de destino. |
| Viagem e Despesa | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | Project Operations: A estimativa de despesas não é eliminada do Finance quando é eliminada do Dataverse. |
| Viagem e Despesa | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | Quando a categoria de despesas não é uma categoria do projeto, as dimensões financeiras que são selecionadas na página **Despesas** não são copiadas para o relatório de despesas. |
