---
title: Novidades de maio de 2022 - Project Operations para cenários baseados em recursos/não armazenados
description: Este artigo fornece informação sobre as atualizações de qualidade que estão disponíveis na versão de maio de 2022 do Microsoft Dynamics 365 Project Operations para cenários baseados em recursos/sem stock.
author: sigitac
ms.date: 05/02/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: beb75fc4b721d52cddbdaf2d20194218cefced5e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921408"
---
# <a name="whats-new-may-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades de maio de 2022 - Project Operations para cenários baseados em recursos/não armazenados

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

Este artigo aplica-se aos seguintes componentes e versões do Microsoft Dynamics 365 Project Operations:

- Project Operations num ambiente Dataverse, versão 4.42.0.70
- Gestão de projetos e contabilidade num ambiente do Dynamics 365 Finance versão 10.0.26

## <a name="project-operations-dual-write-maps-updates"></a>Atualizações de mapas de escrita dupla do Project Operations

Não existem atualizações para os mapas de escrita dupla do Project Operations nesta versão. Para obter uma lista atual e as versões dos mapas de escrita dupla do Project Operations, consulte [Versões do mapa de escrita dupla do Project Operations](../environment/resource-dual-write-maps.md).

Execute sempre a versão mais recente do mapa no seu ambiente e ative todos os mapas de tabelas relacionados à medida que atualiza a sua solução do Project Operations Dataverse e a versão da solução Finance. Algumas funcionalidades e capacidades podem não funcionar corretamente se a versão mais recente do mapa não estiver ativada. Pode ver a versão ativa do mapa na coluna **Versão** na página **Escrita Dupla**. Para ativar uma nova versão do mapa, selecione **Versões do mapa de tabela** , selecione a versão mais recente e, em seguida, guarde a versão selecionada. Se tiver personalizado um mapa de tabela de origem, volte a aplicar as alterações. Para mais informações, consulte [Gestão do ciclo de vida da aplicação](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se ocorrer um problema quando iniciar o mapa, siga as instruções na secção [Problema de colunas de tabela em falta em mapas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) do guia de resolução de problemas do serviço Escrita dupla.

## <a name="quality-updates"></a>Atualizações de qualidade
### <a name="project-operations-on-dataverse"></a>Project Operations no Dataverse

| Área de funcionalidades | Número de referência | Atualização de qualidade |
| --- | --- | --- |
| Gestão de recursos | 2634019 | Mensagens de erro melhoradas para validações de negócio ao adicionar membros de equipa genéricos como recursos. |
| Planeamento e monitorização de projetos | 2648515 | Atualizações restritas de **ownerid**, **estado** e **estado** no agendamento de entidades. |
| Faturação e preços | 2653167 | O separador decimal da grelha **Estimativas** tem de seguir as definições de formato nas **Opções pessoais**. |
| Faturação e preços| 2662251 | Valores nos campos predefinidos **Unidade corrigida** e **Grupo de unidades** quando criados registos em estimativas de materiais. |
| Faturação e preços| 2571408 | Os valores reais de vendas não faturados estão com um ID de fatura proforma quando é criado um rascunho de fatura. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Gestão de projetos e contabilidade no Dynamics 365 Finance

Para obter informações sobre as correções de erros incluídas nesta atualização, inicie sessão no Microsoft Dynamics Lifecycle Services (LCS) e consulte o [Artigo BDC](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
