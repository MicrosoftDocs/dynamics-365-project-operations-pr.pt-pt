---
title: Configurar componentes faturáveis de um item de contrato do projeto
description: Este artigo fornece informações sobre componentes incluídos, faturáveis e não faturáveis em itens de contrato.
author: rumant
ms.date: 10/12/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 175b25dbcc43a5954fbbf2d54efdd73e19395907
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928308"
---
# <a name="configure-chargeable-components-of-a-project-contract-line"></a>Configurar componentes faturáveis de um item de contrato do projeto

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

Um item de contrato baseado em projeto tem o conceito de componentes incluídos e componentes faturáveis.

Os componentes incluídos estão sujeitos ao método de faturação, às divisões de clientes, aos limites a não exceder e às definições de frequência de faturação definidas no item de contrato baseado em projeto.

Um subconjunto dos componentes incluídos pode ser marcado como faturável atualizando o campo **Tipo de Faturação**.

Os componentes faturáveis podem ser definidos nas categorias de funções e transações.

Para um item de contrato de projeto, a capacidade de faturação definida numa função aplica-se apenas à classe de transação **Tempo**. Se **Incluir Tempo** estiver definido para **Não** num item de contrato de projeto, o separador **Funções faturáveis** não está disponível.

A capacidade de faturação definida nas categorias de transação de um item de contrato de projeto aplica-se apenas à classe de transação **Despesa**. Se **Incluir Despesas** estiver definido para **Não** num item de contrato de projeto, o separador **Categorias Faturáveis** não está disponível.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Atualizar uma função de projeto como faturável ou não faturável

Uma função pode ser faturável ou não faturável num item de contrato baseado em projetos específico.

No separador **Funções faturáveis** de um item de contrato baseada em projeto, na subgrelha **Categorias Faturáveis**, no campo **Tipo de Faturação**, atualize o tipo de faturação para uma função.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Atualizar uma categoria de transação como faturável ou não faturável

Uma categoria de transação pode ser faturável ou não faturável num item de contrato baseado em projetos específico.

No separador **Categorias Faturáveis** de um item de contrato baseada em projeto, na subgrelha **Categorias Faturáveis**, no campo **Tipo de Faturação**, atualize o tipo de faturação para uma transação.

### <a name="resolve-chargeability"></a>Resolver a capacidade de faturação

Uma estimativa ou um valor real criado para tempo apenas será considerado faturável se tempo for incluído no item de contrato, e se a Função for configurada como faturável no item de contrato.

Uma estimativa ou um valor real criado para despesas apenas será considerado faturável se despesa for incluída no item de contrato, e se as categoria de transação for configurada como faturável no item de contrato.

| Inclui tempo | Inclui despesa | Função | Categoria | Tarefa |
| --- | --- | --- | --- | --- |
| Sim | Sim | Faturável | Faturável | Faturação num valor real de tempo: Faturável </br>Tipo de faturação num valor real de despesas: Faturável |
| Sim | Sim | Não Faturável | Faturável | Faturação num valor real de tempo: Não Faturável </br>Tipo de faturação num valor real de despesas: Faturável |
| Sim | Sim | Não Faturável | Não Faturável | Faturação num valor real de tempo: Não Faturável </br>Tipo de faturação num valor real de despesas: Não Faturável |
| No | Sim | Não pode ser definido | Faturável | Faturação num valor real de tempo: Não disponível </br>Tipo de faturação num valor real de despesas: Faturável |
| No | Sim | Não pode ser definido | Não Faturável | Faturação num valor real de tempo: Não disponível </br>Tipo de faturação num valor real de despesas: Não faturável |
| Sim | No | Faturável | Não pode ser definido | Faturação num valor real de tempo: Faturável </br>Tipo de faturação num valor real de despesas: Não disponível |
| Sim | No | Não Faturável | Não pode ser definido | Faturação num valor real de tempo: Não faturável </br> Tipo de faturação num valor real de despesas: Não disponível |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
