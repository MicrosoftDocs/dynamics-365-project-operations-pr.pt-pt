---
title: Configurar componentes faturáveis de um item de contrato baseado em projetos
description: Este tópico fornece informações sobre componentes incluídos, faturáveis e não faturáveis em itens de contrato.
author: rumant
manager: Annbe
ms.date: 10/12/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: af97904b0171618cb15d060da9bc87fcf6bbabeb
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082341"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a>Configurar componentes faturáveis de um item de contrato baseado em projetos

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

Um item de contrato baseado em projeto tem o conceito de componentes incluídos e componentes faturáveis.

Os componentes incluídos estão sujeitos ao método de faturação, às divisões de clientes, aos limites a não exceder e às definições de frequência de faturação definidas no item de contrato baseado em projeto.

Um subconjunto dos componentes incluídos pode ser marcado como faturável atualizando o campo **Tipo de Faturação**.

Os componentes faturáveis podem ser definidos nas categorias de funções e transações.

Para um item de contrato de projeto, a capacidade de faturação definida numa função aplica-se apenas à classe de transação **Tempo**. Se **Incluir Tempo** estiver definido para **Não** num item de contrato de projeto, o separador **Funções faturáveis** não está disponível.

A capacidade de faturação definida nas categorias de transação de um item de contrato de projeto aplica-se apenas à classe de transação **Despesa**. Se **Incluir Despesas** estiver definido para **Não** num item de contrato de projeto, o separador **Categorias Faturáveis** não está disponível.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Atualizar uma função de projeto como faturável ou não faturável

Uma função pode ser faturável ou não faturável num item de contrato baseado em projetos específico.

No separador **Funções faturáveis** de um item de contrato baseado em projetos, na subgrelha **Categorias Faturáveis** , no campo **Tipo de Faturação** , atualize o tipo de faturação para uma função.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Atualizar uma categoria de transação como faturável ou não faturável

Uma categoria de transação pode ser faturável ou não faturável num item de contrato baseado em projetos específico.

No separador **Categorias Faturáveis** de um item de contrato baseado em projetos, na subgrelha **Categorias Faturáveis** , no campo **Tipo de Faturação** , atualize o tipo de faturação para uma transação.

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