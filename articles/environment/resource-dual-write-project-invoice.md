---
title: Integração de fatura de projeto
description: Este tópico fornece informações sobre a integração de escrita dupla do Project Operations para faturação de cliente.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1e7294360f041b030efca225c6754fe3bbc0eadf
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581252"
---
# <a name="project-invoice-integration"></a>Integração de fatura de projeto

Este tópico fornece informações sobre a integração de escrita dupla do Project Operations para faturação de cliente.

No Project Operations, o gestor do Projeto gere o atraso na faturação do projeto e cria uma fatura proforma para o cliente em Microsoft Dataverse. Com base nesta fatura proforma, o escriturário de contas a receber ou contabilista do Projeto cria uma fatura virada para o cliente. A integração de escrita dupla assegura que os detalhes da fatura pro-forma são sincronizados com as aplicações Finanças e Operações. Após a publicação da fatura virada para o cliente, o sistema atualiza os resultados do projeto relevante em Dataverse com o detalhe contabilístico. O gráfico a seguir proporciona uma visão conceptual de alto nível desta integração.

   ![Integração de fatura de projeto.](./media/DW5Invoicing.png)

Depois de o Gestor do Projeto confirmar a fatura pro-forma no Dataverse, as informações do cabeçalho da fatura proforma são sincronizadas com as aplicações de Finanças e Operações utilizando o mapa de tabela de escrita dupla, **Proposta de fatura do projeto V2 (faturas)**. Trata-se de uma integração de via única entre o Dataverse e as aplicações de Finanças e Operações. A criação ou eliminação de propostas de propostas de fatura do projeto diretamente nas aplicações de Finanças e Operações não é suportada.

A confirmação da fatura em Dataverse também desencadeia a lógica de negócio para criar registos relacionados com a faturação na entidade **Valores reais**. Estes registos reais são sincronizados com as aplicações de Finanças e Operações utilizando o mapa de tabela de escrita dupla, **Valores reais de integração do Project Operations (msdyn\_actuals).** Para mais informações, consulte [Estimativas e valores reais](resource-dual-write-estimates-actuals.md). 

As linhas de proposta de fatura do projeto são criadas pelo processo periódico, **Importar formulário de teste**. Este processo baseia-se nos detalhes de valores reais das vendas faturadas na tabela de **Teste de valores reais**. Para mais informações, consulte [Gerir as propostas de fatura do projeto](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
