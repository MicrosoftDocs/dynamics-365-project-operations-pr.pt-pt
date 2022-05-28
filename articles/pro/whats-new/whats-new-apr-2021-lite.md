---
title: O que há de novo abril de 2021 - Implementação leve do Project Operations
description: Este tópico fornece informações sobre as atualizações de qualidade disponíveis no lançamento de abril de 2021 da implementação leve do Project Operations.
author: sigitac
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 10d9498636d8c5f72b7544be4ec30f399d5e0311
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598134"
---
# <a name="whats-new-april-2021---project-operations-lite-deployment"></a>O que há de novo abril de 2021 - Implementação leve do Project Operations

_Aplica-se a: Implementação lite – negócio para faturação pró-forma_

Este tópico aplica-se aos seguintes componentes e versões do Dynamics 365 Project Operations:

  - Project Operations na versão 4.9.0.221 do ambiente Dataverse 

## <a name="features-included-in-this-release"></a>Funcionalidades incluídas nesta versão

Estão incluídas nesta versão as seguintes funcionalidades:

- Materiais não armazenados para projetos. As capacidades-chave incluem:
  - Estimar e definir preços de materiais não armazenados durante o ciclo de vendas de um projeto. Para mais informações ver [Configurar taxas de custo e de venda para produtos de catálogo - leve](../pricing-costing/set-up-cost-sales-rates-catalog-products.md).
  - Monitorização da utilização de materiais não armazenados durante a entrega do projeto. Para obter mais informações, consulte [Registar utilização de material em projetos e tarefas de projeto](../../material/material-usage-log.md).
  - A faturação utilizou custos materiais não armazenados. Para obter mais informações, consulte [Gerir o registo de tarefas pendentes de faturação - leve](../proforma-invoicing/manage-billing-backlog-sales.md#product-billing-backlog).
  - As novas APIs no Dynamics 365 Dataverse permitem criar, atualizar e eliminar operações com **Entidades de agendamento**. Para mais informações, ver [Utilizar APIs de Agenda para realizar operações com entidades de agendamento](../../project-management/schedule-api-preview.md).

## <a name="quality-updates"></a>Atualizações de qualidade

| **Área de funcionalidades** | **Número de referência** | **Atualização de qualidade** |
| --- | --- | --- |
| Faturação e preços | 2224568 | Lógica adicional para permitir personalizações que envolvem invocar o plug-in de confirmação da fatura. |
| Faturação e preços | 2101098 | Melhorou a lógica dos campos predefinidos para fatura pró-forma: **Fatura para endereço**, **Fatura a nome** e **Termos de pagamento** estão agora por defeito a partir do registo correspondente do cliente do contrato de projeto. |
| Faturação e preços | 2021413 | Atualizou os campos de **Custos reais** e **Vendas** na entidade **Tarefa** para incluir valores de venda de despesas não faturadas e faturadas em tarefas. |
| Faturação e preços | 2182110 | Ao copiar um contrato de projeto, o item de contrato ID é regenerado no contrato de projeto de destino para garantir que é único. |
| Gestão de oportunidades | 2186741 | Validações adicionais para garantir que o campo **Origem** e **tipo de transação** não podem ser atualizados nos detalhes da linha de proposta existentes. |
| Gestão de oportunidades | 2191353 | Os marcos não devem ser criados num item de contrato de tempo e material. |
| Gestão de oportunidades | 2216956 | Problemas solucionados com **Atualizar preços**. |
| Planeamento e deteção de movimentos | 2182979 | A função de cópia do projeto melhorou para garantir que as linhas de estimativa de despesas são copiadas do projeto original. |
| Planeamento e deteção de movimentos | 2184144 | A função de cópia do projeto melhorou para garantir que o nome da posição do recurso é copiado do projeto original. |
| Planeamento e deteção de movimentos | 2184799 | Cópia do projeto: Controlo apertado para garantir que a data de início estimada não pode ser alterada enquanto a cópia está em andamento. |
| Planeamento e deteção de movimentos | 2185134 | Cópia do projeto: A data de início estimada do projeto de destino está marcada para a data de hoje. |
| Planeamento e deteção de movimentos | 2196373 | Cópia do projeto: Certifique-se de que os registos do gestor do projeto e dos membros da equipa não são duplicados na equipa do projeto. |
| Planeamento e deteção de movimentos | 2211833 | Cópia do projeto: As atribuições de recursos são copiadas da tarefa do projeto de origem para o projeto de destino. |
| Planeamento e deteção de movimentos | 2186541 | Problemas solucionados na grelha de **Estimativas** ao agrupar por recurso. |
| Planeamento e deteção de movimentos | 2166906 | A categoria de transação a partir de uma tarefa deve ser copiada para a entidade de **Atribuição de recursos**. |
| Gestão de Recursos | 2125362 | Problemas solucionados com a criação de um membro genérico da equipa usando um método de atribuição baseado em horas. |
| Tempo e Despesa | 2113603 | Corrigiu o problema relacionado com a personalização com a remoção de atributos da página **Entrada de tempo**. O sistema verifica agora se o atributo existe na página antes de aceder aos mesmos utilizando um script. |
| Tempo e Despesa | 2204377 | As folhas de tempo copiadas devem aparecer automaticamente quando selecionar **Copiar semana** durante a entrada de tempo. |
| Tempo e Despesa | 2209059 | O campo **Estado** pode ser editado para entradas de tempo do Dynamics 365 Field Service. |
