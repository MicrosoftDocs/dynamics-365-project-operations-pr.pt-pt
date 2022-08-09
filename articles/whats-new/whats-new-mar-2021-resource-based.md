---
title: Novidades em março de 2021 – Project Operations para cenários baseados em Recursos/Não Armazenados
description: Este artigo fornece informações sobre as atualizações de qualidade disponíveis na versão de março de 2021 do Project Operations para cenários baseados em recursos/itens não existentes em stock.
author: sigitac
ms.date: 03/03/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: e93b4eaad98267f163bad4aff3e4fdcc661e2ab0
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028286"
---
# <a name="whats-new-march-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novidades em março de 2021 – Project Operations para cenários baseados em Recursos/Não Armazenados

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

Este artigo aplica-se aos seguintes componentes e versões do Dynamics 365 Project Operations:

- Project Operations na versão 4.8.0.91 do ambiente Dataverse 
- Gestão de projetos e contabilidade no ambiente do Dynamics 365 Finance versão 10.0.16 

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

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Gestão de projetos e contabilidade no Dynamics 365 Finance

Para mais informações, ver [Novidades em janeiro de 2021 – Project Operations para cenários baseados em Recursos/Não Armazenados](whats-new-jan-2021-resource-based.md).

## <a name="regulatory-updates"></a>Atualizações regulamentares

Para obter informações sobre atualizações regulamentares para as aplicações de finanças e operações, consulte [Atualizações regulamentares](/dynamics365/finance/localizations/regulatory-updates). Outra forma de aprender sobre as atualizações regulamentares é fazer login em LCS ver as atualizações regulamentares planeadas usando a ferramenta de pesquisa de problemas. A pesquisa Emitir permite pesquisar por país, tipo de funcionalidade e versão.


[!INCLUDE[footer-include](../includes/footer-banner.md)]