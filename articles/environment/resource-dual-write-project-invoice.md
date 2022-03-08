---
title: Integração de fatura de projeto
description: Este tópico fornece informações sobre a integração de escrita dupla do Project Operations para faturação de cliente.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7407c98aad79806dcbaf25e81ff3e08397b41ffe
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996580"
---
# <a name="project-invoice-integration"></a>Integração de fatura de projeto

Este tópico fornece informações sobre a integração de escrita dupla do Project Operations para faturação de cliente.

No Project Operations, o gestor do Projeto gere o atraso na faturação do projeto e cria uma fatura proforma para o cliente em Microsoft Dataverse. Com base nesta fatura proforma, o escriturário de contas a receber ou contabilista do Projeto cria uma fatura virada para o cliente. A integração de escrita dupla garante que os detalhes da fatura proforma são sincronizados com as aplicações Finance and Operations. Após a publicação da fatura virada para o cliente, o sistema atualiza os resultados do projeto relevante em Dataverse com o detalhe contabilístico. O gráfico a seguir proporciona uma visão conceptual de alto nível desta integração.

   ![Integração de fatura de projeto](./media/DW5Invoicing.png)

Depois de o gestor do Projeto confirmar a fatura proforma em Dataverse, a informação do cabeçalho da fatura proforma sincroniza-se com aplicações Finance and Operations que utilizam o mapa de tabelas de dupla escrita, **Proposta de fatura do Projeto V2 (faturas)**. Esta é uma integração unidirecional das aplicações Dataverse para Finance and Operations. A criação ou eliminação de propostas de faturas do projeto diretamente em aplicações Finance and Operations não é suportada.

A confirmação da fatura em Dataverse também desencadeia a lógica de negócio para criar registos relacionados com a faturação na entidade **Valores reais**. Estes registos de valores reais são sincronizados com aplicações Finance and Operations que utilizam o mapa de tabela de escrita dupla **Valores reais da integração do Project Operations (msdyn\_actuals).** Para mais informações, consulte [Estimativas e valores reais](resource-dual-write-estimates-actuals.md). 

As linhas de proposta de fatura do projeto são criadas pelo processo periódico, **Importar formulário de teste**. Este processo baseia-se nos detalhes de valores reais das vendas faturadas na tabela de **Teste de valores reais**. Para mais informações, consulte [Gerir as propostas de fatura do projeto](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
