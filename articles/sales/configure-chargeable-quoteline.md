---
title: Configurar os componentes faturáveis de uma linha de proposta baseada em projetos
description: Este tópico fornece informações sobre componentes incluídos, faturáveis e não faturáveis nas linhas de proposta baseadas em projetos.
author: rumant
manager: Annbe
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 36765ab3687a8aaf3ae4a631516a1d61c14e981e
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642557"
---
# <a name="configure-the-chargeable-components-of-a-project-based-quote-line"></a>Configurar os componentes faturáveis de uma linha de proposta baseada em projetos

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

Uma linha de proposta baseada em projetos pode ter incluído componentes e componentes faturáveis.

Os componentes incluídos estão sujeitos ao método de faturação, às divisões de clientes, aos limites a não exceder e às definições de frequência de faturação definidas na linha de proposta baseada em projetos.
Um subconjunto dos componentes incluídos pode ser marcado como faturável utilizando o **Tipo de Faturação**. Pode selecionar uma das seguintes opções no campo **Tipo de Faturação** no contexto de uma linha de proposta:

   - Faturável
   - Não faturável

Os componentes faturáveis podem ser definidos nas categorias de funções e transações.

A capacidade de cobrança definida em funções para uma linha de proposta de projeto aplica-se apenas à classe de transação **Tempo**. Se uma linha de proposta do projeto tiver **Incluir Tempo** = **Não**, o separador **Funções Faturáveis** não está disponível.

A capacidade de cobrança definida em categorias de transação para uma linha de proposta de projeto aplica-se apenas à classe de transação **Despesa**. Se uma linha de proposta do projeto tiver **Incluir Despesas** = **Não**, o separador **Categorias Faturáveis** não está disponível.

## <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Atualizar uma função de projeto como faturável ou não faturável
Uma função pode ser faturável ou não faturável numa linha de proposta baseada em projetos. O tipo de faturação de uma função pode ser configurado no separador **Funções Faturáveis** de uma linha de proposta baseada em projetos. Para isso, atualize **Tipo de Faturação** na subgrelha **Funções Faturáveis**. 

## <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Atualizar uma categoria de transação como faturável ou não faturável
Uma categoria de transação pode ser faturável ou não faturável numa linha de proposta baseada em projetos. O tipo de faturação de uma transação pode ser configurado no separador **Categorias Faturáveis** de uma linha de proposta baseada em projetos. Para isso, atualize o campo **Tipo de Faturação** na subgrelha **Categorias Faturáveis**. 

## <a name="resolve-chargeability"></a>Resolver a capacidade de faturação

Uma estimativa ou um valor real criado para tempo só será considerado faturável se o tempo for incluído na linha de proposta e se a função for configurada como faturável.
Uma estimativa ou um valor real criado para uma despesa só será considerado faturável se a despesa for incluída na linha de proposta e se a categoria de transação for configurada como faturável na linha de proposta. A tabela a seguir mostra como a capacidade de cobrança assume a predefinição em cada valor real. As predefinições baseiam-se nos componentes incluídos e no tipo de faturação que é configurado na linha de proposta.

| Inclui tempo | Inclui despesa | Função | Categoria | Tarefa |
| --- | --- | --- | --- | --- |
| Sim | Sim | Faturável | Faturável | Faturação num valor real de tempo: Faturável </br>Tipo de faturação num valor real de despesas: Faturável |
| Sim | Sim | Não Faturável | Faturável | Faturação num valor real de tempo: Não Faturável </br>Tipo de faturação num valor real de despesas: Faturável |
| Sim | Sim | Não Faturável | Não Faturável | Faturação num valor real de tempo: Não Faturável </br>Tipo de faturação num valor real de despesas: Não Faturável |
| No | Sim | Não pode ser definido | Faturável | Faturação num valor real de tempo: Não disponível </br>Tipo de faturação num valor real de despesas: Faturável |
| No | Sim | Não pode ser definido | Não Faturável | Faturação num valor real de tempo: Não disponível </br>Tipo de faturação num valor real de despesas: Não faturável |
| Sim | No | Faturável | Não pode ser definido | Faturação num valor real de tempo: Faturável </br>Tipo de faturação num valor real de despesas: Não disponível |
| Sim | No | Não Faturável | Não pode ser definido | Faturação num valor real de tempo: Não faturável </br> Tipo de faturação num valor real de despesas: Não disponível |
