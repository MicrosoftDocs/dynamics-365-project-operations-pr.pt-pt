---
title: Novidades em março de 2021 – Project Operations para cenários baseados em Recursos/Não Armazenados
description: Este tópico fornece informações sobre as atualizações de qualidade disponíveis na versão de março de 2021 do Project Operations para cenários baseados em Recursos/Não Armazenados.
author: sigitac
manager: tfehr
ms.date: 03/03/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4d114ee64bd26d3271a1c72a7404c0f7035c2b61
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948073"
---
# <a name="whats-new-march-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades em março de 2021 – Project Operations para cenários baseados em Recursos/Não Armazenados

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

Este tópico aplica-se aos seguintes componentes e versões do Dynamics 365 Project Operations:

- Project Operations na versão 4.8.0.91 do ambiente Dataverse 
- Gestão de projetos e contabilística na versão 10.0.16 do ambiente Dynamics 365 Finance 

## <a name="quality-updates"></a>Atualizações de qualidade

### <a name="project-operations-on-dataverse"></a>Project Operations no Dataverse


| **Área de funcionalidades** | **Número de referência** | **Atualização de qualidade** |
| --- | --- | --- |
| Faturação e preços | 2133873 | Definiu o visor do símbolo da **moeda de preço de venda** unitária na grelha de **estimativas de despesas**. |
| Faturação e preços | 2174616 | Quando uma proposta é ganha, a lista de preços personalizados do contrato é referenciada em detalhes do item de contrato que são copiados da proposta. |
| Gestão de oportunidades | 2167475 | Montante fixo do imposto na fatura de correção que originou uma entrada efetiva não faturada. |
| Gestão de oportunidades | 2176285 | O montante do imposto não deve ser copiado dos detalhes do item de contrato de venda/cotação para os detalhes do item de contrato/cotação de custos. |
| Gestão de oportunidades | 2188079 | A regra de faturação dividida não deve ser criada para contratos que não sejam baseados no trabalho. |
| Planeamento e deteção de movimentos | 2125274 | **Atributo do Mapa de Escrita Dupla do Projeto** para **Mapeamento da Data de Início do Projeto** atualizado de **msdyn\_taskearlieststart** para **msdyn\_actualstart**. |
| Planeamento e deteção de movimentos | 2138853 | Função de cópia do projeto atualizada para garantir linhas de estimativa de despesas que as tarefas de referência são copiadas para o projeto de destino. |
| Planeamento e deteção de movimentos | 2154306 | Problemas solucionados com a supressão das estimativas de despesas no Project Operations para cenários baseados em recursos. |
| Planeamento e deteção de movimentos | 2173259 | Função de cópia do projeto atualizada para garantir que não exibe mensagem de erro **A copiar WBS** em certos cenários. |
| Tempo e Despesa | 2148910 | Problema de exibição solucionado com a página de **Editar entrada** na grelha de **Entrada de tempo**. |
| Tempo e Despesa | 2159798 | Controlos apertados para garantir que as entradas de despesas aprovadas não podem ser editadas. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Gestão de projetos e contabilística no Dynamics 365 Finance

Para mais informações, ver [Novidades em janeiro de 2021 – Project Operations para cenários baseados em Recursos/Não Armazenados](whats-new-jan-2021-resource-based.md).

## <a name="regulatory-updates"></a>Atualizações regulamentares

Para obter informações sobre atualizações regulamentares para aplicações Finance and Operations, consulte [Atualizações regulamentares](/dynamics365/finance/localizations/regulatory-updates). Outra forma de aprender sobre as atualizações regulamentares é fazer login em LCS ver as atualizações regulamentares planeadas usando a ferramenta de pesquisa de problemas. A pesquisa Emitir permite pesquisar por país, tipo de funcionalidade e versão.


[!INCLUDE[footer-include](../includes/footer-banner.md)]