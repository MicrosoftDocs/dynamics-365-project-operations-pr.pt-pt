---
title: Analisar o registo de tarefas de faturação nos projetos e contratos do projeto
description: Este tópico fornece informações sobre como analisar o tempo, as despesas e os registos de tarefas dos produtos e como marcá-los como prontos para faturação.
author: rumant
ms.custom: ''
ms.author: rumant
ms.date: 03/11/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: cec09ca39563e3faf0f3b2c10cf9bde3feb020b0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008550"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a>Analisar o registo de tarefas de faturação nos projetos e contratos do projeto

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Quando uma transação está pronta para ter uma fatura criada e processada, a transação deve estar marcada como **Pronta para faturar**. Este tópico descreve os tipos de transações que podem ser criadas.

## <a name="review-the-time-and-material-billing-backlog"></a>Analisar o registo de tarefas de faturação de tempo e material

Quando uma entrada de tempo ou despesa é submetida e aprovada para um projeto, o PSA cria um valor real do projeto. Se a combinação do projeto e a classe de transação forem mapeadas para um item de contrato para um projeto de tempo e materiais, serão criados dois valores reais quando a entrada for aprovada:

- Custo real 
- Valor real de vendas não faturadas

Os valores reais de vendas não faturadas representam o registo de tarefas de faturação, sendo que o seu estado de faturação tem de ser definido como **Pronto para Faturar**. Quando é criada uma fatura do projeto, os valores reais de vendas não faturadas marcados como **Prontos para Faturar** são copiados como detalhes de linha de fatura.

Para analisar o registo de tarefas pendentes de faturação para tempo e materiais, aceda a **Vendas** \> **Faturação** \> **Registo de Tarefas Pendentes de Faturação de Tempo e Material**. Selecione todos os valores reais de vendas não faturadas que estão prontos para serem faturados e, em seguida, selecione **Pronto para Faturar**. O estado de faturação destes valores reais é alterado para **Pronto para Faturar**.

![Registo de tarefas pendentes de faturação de tempo e material](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a>Analisar o registo de tarefas pendentes de faturação de produtos

No PSA, quando um contrato do projeto tem itens de contrato baseados em produtos, esses itens são considerados para faturação sempre que é criada uma fatura para o contrato do projeto. Qualquer produto que tenha itens de contrato marcados como **Pronto para Faturar** é copiado para a fatura do projeto como linhas de fatura do projeto.

Para analisar o registo de tarefas pendentes de faturação de produtos, aceda a **Vendas** \> **Faturação** \> **Registo de Tarefas Pendentes de Faturação de Produtos**. Selecione todos os itens de contrato baseados em produtos que estão prontos para serem faturados e, em seguida, selecione **Pronto para Faturar**. O estado de faturação destes itens é alterado para **Pronto para Faturar**.

![Registo de tarefas pendentes de faturação de produtos](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a>Analisar marcos de faturação em contratos de preço fixo

Cada item de contrato do projeto com um método de faturação de preço fixo tem de definir os marcos do contrato. Estes marcos do contrato só podem ser faturados se estiverem marcados como **Pronto para Faturar**. 

Para analisar os marcos de faturação, aceda a **Vendas** \> **Faturação** \> **Marcos de Preço Fixo**. Selecione os marcos que estão prontos para serem faturados e, em seguida, selecione **Pronto para faturar**. O estado de faturação destes marcos é alterado para **Pronto para Faturar**.

![Marcos de preço fixo](media/FPBacklog.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]