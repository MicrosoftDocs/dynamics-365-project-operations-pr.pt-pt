---
title: Novidades de junho de 2022 - Project Operations para cenários baseados em recursos/não armazenados
description: Este artigo fornece informação sobre as atualizações de qualidade que estão disponíveis na versão de junho de 2022 do Microsoft Dynamics 365 Project Operations para cenários baseados em recursos/sem stock.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fde1f0be42eecfc5ee809cb9b2191d3aeae57131
ms.sourcegitcommit: 51745acac29dfacba43a4003d86baff4d6ca2fb8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/14/2022
ms.locfileid: "8959464"
---
# <a name="whats-new-june-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades de junho de 2022 - Project Operations para cenários baseados em recursos/não armazenados

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

Este artigo aplica-se aos seguintes componentes e versões do Microsoft Dynamics 365 Project Operations:

- Project Operations num ambiente Dataverse, versão 4.43.0.77
- Gestão de projetos e contabilidade num ambiente do Dynamics 365 Finance versão 10.0.27

## <a name="project-operations-dual-write-maps-updates"></a>Atualizações de mapas de escrita dupla do Project Operations

A tabela seguinte mostra os mapas de escrita dupla que foram modificados ou adicionados na versão de junho de 2022 do Project Operations.

| Mapa da entidade | Versão atualizada | Comentários |
| --- | --- | --- |
| Entidade de exportação de faturas de projeto de integração de projetos do Project Operations (msdyn_projectvendorinvoices) | 1.0.0.1 | Preterido o campo legado e mapeado para o novo campo para monitoração do estado de faturas de fornecedor. |

Execute sempre a versão mais recente do mapa no seu ambiente e ative todos os mapas de tabelas relacionados à medida que atualiza a sua solução do Project Operations Dataverse e a versão da solução Finance. Algumas funcionalidades e capacidades podem não funcionar corretamente se a versão mais recente do mapa não estiver ativada. Pode ver a versão ativa do mapa na coluna **Versão** na página **Escrita Dupla**. Para ativar uma nova versão do mapa, selecione **Versões do mapa de tabela** , selecione a versão mais recente e, em seguida, guarde a versão selecionada. Se tiver personalizado um mapa de tabela de origem, volte a aplicar as alterações. Para mais informações, consulte [Gestão do ciclo de vida da aplicação](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se ocorrer um problema quando iniciar o mapa, siga as instruções na secção [Problema de colunas de tabela em falta em mapas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) do guia de resolução de problemas do serviço Escrita dupla.

## <a name="quality-updates"></a>Atualizações de qualidade

### <a name="project-operations-on-dataverse"></a>Project Operations no Dataverse

| Área de funcionalidades | Número de referência | Atualização de qualidade |
| --- | --- | --- |
| Subcontratos | 2708885 | Corrigida a mensagem de erro que aparecia quando um utilizador criava um registo de cabeçalho de reserva de recursos reservável onde nenhum recurso reservável foi preenchido. |
| Planeamento e monitorização de projetos | 2629441 | Corrigida a lógica de acionamento do fluxo de trabalho para ajudar a impedir um ciclo infinito quando as tarefas do projeto são atualizadas. |
| Tempo e despesa | 2641209 | As importações de entrada de tempo a partir de atribuições/reservas têm de reter uma referência de recurso reservável. |
| Planeamento e monitorização de projetos | 2651148 | O cabeçalho de documentos do projeto tem de ser protegido.|
| Planeamento e monitorização de projetos | 2653145 | Validações adicionadas para garantir que não é possível criar um registo de projeto que tenha carateres não válidos no mesmo. |
| Tempo e despesa | 2654710 | Corrigida a filtragem na página **Aprovações**. |
| Faturação e preços | 2667805 | Validações adicionadas para ajudar a impedir a criação de valores reais de vendas faturados se não existirem valores reais de vendas não faturados. |
| Faturação e preços | 2668378 | Validações adicionadas para ajudar a impedir a adição de uma dimensão de preços personalizada, a menos que um nome lógico e um nome de campo sejam preenchidos. |
| Subcontratos | 2677485 | Atualizada a versão de destino do mapa de escrita dupla de faturas de fornecedor. |
| Tempo e despesa | 2700428 | Melhorada a lógica de aprovações para garantir que outros conjuntos de aprovações para o projeto podem ser processados, mesmo que um dos conjuntos de aprovações esteja preso em tarefas de sistema. |

### <a name="project-management-and-accounting-in-finance"></a>Gestão de projetos e contabilística em Finanças

Para obter informações sobre as correções de erros incluídas nesta atualização, inicie sessão no Microsoft Dynamics Lifecycle Services (LCS) e consulte o [Artigo BDC](https://fix.lcs.dynamics.com/Issue/Details?bugId=673271).
