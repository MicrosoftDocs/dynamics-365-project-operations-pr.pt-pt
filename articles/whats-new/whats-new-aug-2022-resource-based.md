---
title: Novidades de agosto de 2022 - Project Operations para cenários baseados em recursos/não armazenados
description: Este artigo fornece informação sobre as atualizações de qualidade que estão disponíveis na versão de agosto de 2022 do Microsoft Dynamics 365 Project Operations para cenários baseados em recursos/sem stock.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 4042dca72a33f48e04e51af2a3cfd2da83146afd
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 09/02/2022
ms.locfileid: "9403871"
---
# <a name="whats-new-august-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades de agosto de 2022 - Project Operations para cenários baseados em recursos/não armazenados

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

Este artigo aplica-se aos seguintes componentes e versões do Microsoft Dynamics 365 Project Operations:

- Project Operations num ambiente Dataverse, versão 4.45.0.53
- Gestão de projetos e contabilidade num ambiente do Dynamics 365 Finance versão 10.0.28

## <a name="project-operations-dual-write-maps-updates"></a>Atualizações de mapas de escrita dupla do Project Operations

Não existem atualizações para os mapas de escrita dupla do Project Operations nesta versão. Para obter uma lista atual e as versões dos mapas de escrita dupla do Project Operations, consulte [Versões do mapa de escrita dupla do Project Operations](../environment/resource-dual-write-maps.md).

Execute sempre a versão mais recente do mapa no seu ambiente e ative todos os mapas de tabelas relacionados à medida que atualiza a sua solução do Project Operations Dataverse e a versão da solução Finance. Algumas funcionalidades e capacidades podem não funcionar corretamente se a versão mais recente do mapa não estiver ativada. Pode ver a versão ativa do mapa na coluna **Versão** na página **Escrita Dupla**. Para ativar uma nova versão do mapa, selecione **Versões do mapa de tabela** , selecione a versão mais recente e, em seguida, guarde a versão selecionada. Se tiver personalizado um mapa de tabela de origem, volte a aplicar as alterações. Para mais informações, consulte [Gestão do ciclo de vida da aplicação](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Se ocorrer um problema quando iniciar o mapa, siga as instruções na secção [Problema de colunas de tabela em falta em mapas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) do guia de resolução de problemas do serviço Escrita dupla.

## <a name="quality-updates"></a>Atualizações de qualidade

### <a name="project-operations-on-dataverse"></a>Project Operations no Dataverse

| Área de funcionalidades | Número de referência | Atualização de qualidade |
| --- | --- | --- |
| Gestão de oportunidades | 2762089 | O processamento de erros ao fechar o contrato como perdido se guardar automaticamente estiver desativado na organização.|
|Planeamento e Monitorização de Projetos | 2767841 | A telemetria atualiza a entidade de Projeto de Criar ou Atualizar cenários.|
|Faturação e Preços | 2771072 | Tratamento de exceção de referência nula durante uma proposta ganha.|
|Faturação e Preços | 2844181 |Falha na obtenção de um ID de correlação e bloqueio da criação de uma fatura.|
|Faturação e Preços | 2852836 | Valores reais entre empresas em falta para Despesas entre empresas criadas e aprovadas no CE.|


### <a name="project-management-and-accounting-in-finance"></a>Gestão de projetos e contabilística em Finanças

Para obter informações sobre as correções de erros incluídas nesta atualização, inicie sessão no Microsoft Dynamics Lifecycle Services (LCS) e consulte o [Artigo BDC](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).
