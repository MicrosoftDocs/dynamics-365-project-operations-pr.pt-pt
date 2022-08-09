---
title: Novidades em fevereiro de 2021 – Project Operations para cenários baseados em Recursos/Não Armazenados
description: Este artigo fornece informações sobre as atualizações de qualidade disponíveis na versão de fevereiro de 2021 do Project Operations para cenários baseados em recursos/itens não existentes em stock.
author: sigitac
ms.date: 02/08/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1fe1e59a0a3674752fe62525349a50f00e11089b
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029636"
---
# <a name="whats-new-february-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades em fevereiro de 2021 – Project Operations para cenários baseados em Recursos/Não Armazenados

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

Este artigo aplica-se aos seguintes componentes e versões do Dynamics 365 Project Operations:

- Project Operations no ambiente Dataverse 4.7.0.95
- Gestão de projetos e contabilidade no ambiente do Dynamics 365 Finance versão 10.0.16 

## <a name="quality-updates"></a>Atualizações de qualidade

### <a name="project-operations-on-dataverse"></a>Project Operations no Dataverse

| **Área de funcionalidades** | **Número de referência** | **Atualização de qualidade** |
| --- | --- | --- |
| **Faturação e Preços** | 2053736 | Os detalhes da linha de fatura passam a estar acessíveis através **Fatura** > **Informação relacionada**. |
| **Faturação e Preços** | 2122613 | As ações **Ativar** e **Desativar** foram removidas das entidades da associação **Lista de preços**. |
| **Faturação e Preços** | 2128606 | Resolveu o problema com **ullReferenceException** no plug-in **GetEstimatesForProject**. |
| **Implementação e configuração** | 2139346 | Resolveu o problema com a importação não gerida da solução **Dynamics365ProjectOperationsDualWrite**. |
| **Implementação e configuração** | 2140569 | A solução de projeto não deve ser instalada nos ambientes Equipas Dataverse. |
| **Implementação e configuração** | 2086991 | Localização restrita de personalização de recursos web. |
| **Gestão de oportunidades** | 2136794 | Apresenta a mensagem de erro correta quando os processos **Confirmar fatura** ou **Marcar fatura como paga** falham. |
| **Gestão de oportunidades** | 2139330 | A alteração do gestor do Projeto num projeto não deve repor a empresa proprietária de volta ao valor predefinido. |
| **Gestão de oportunidades** | 2146376 | O valor do imposto corrigido num valor real não faturável é criado a partir da confirmação da fatura. |
| **Planeamento e Monitorização de Projetos** | 2099879 | A implementação do ambiente Dataverse deve criar uma categoria de transação padrão com um ID estático e não gerar aleatoriamente um por ambiente. |
| **Planeamento e Monitorização de Projetos** | 2128577 | Fixou os privilégios do utilizador do Project Service para atualizar a categoria de transação numa atribuição de recursos. |
| **Planeamento e Monitorização de Projetos** | 2164035 | Problemas solucionados com a função **Copiar**. |
| **Entrada de hora** | 2129161 | São aplicadas restrições mais apertadas para garantir que os utilizadores não podem alterar e atualizar uma entrada de tempo que tenha sido submetida ou aprovada. |
| **Entrada de hora** | 2103572 | A aprovação do tempo para as entradas no tempo não-projeto não deve estar à procura de um papel aprovador do projeto. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Gestão de projetos e contabilidade no Dynamics 365 Finance 

Para mais informações sobre gestão de projetos e contabilidade no Dynamics 365 Finance, consulte [Novidades de janeiro de 2021 - Project Operations para cenários baseados em recursos/sem stock](whats-new-jan-2021-resource-based.md).


## <a name="regulatory-updates"></a>Atualizações regulamentares

Para obter informações sobre atualizações regulamentares para as aplicações de finanças e operações, consulte [Atualizações regulamentares](/dynamics365/finance/localizations/regulatory-updates). Outra forma de aprender sobre as atualizações regulamentares é fazer login em Lifecycle Services (LCS) e ver as atualizações regulamentares planeadas usando a ferramenta de pesquisa de problemas. A pesquisa Emitir permite pesquisar por país, tipo de funcionalidade e versão.


[!INCLUDE[footer-include](../includes/footer-banner.md)]