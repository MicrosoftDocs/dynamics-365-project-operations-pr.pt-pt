---
title: O que há de novo maio de 2021 - Implementação leve do Project Operations
description: Este artigo fornece informações sobre as atualizações de qualidade disponíveis na versão de maio de 2021 da implementação do Project Operations Lite.
author: sigitac
ms.date: 05/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: a5d67159b732e0309e03c64fb6dadcc7b8cbff51
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8934196"
---
# <a name="whats-new-may-2021---project-operations-lite-deployment"></a>O que há de novo maio de 2021 - Implementação leve do Project Operations

_Aplica-se a: Implementação lite – negócio para faturação pró-forma_

Este artigo aplica-se aos seguintes componentes e versões do Dynamics 365 Project Operations:

   - Project Operations na versão 4.10.0.186 do ambiente Dataverse.

## <a name="features-included-in-this-release"></a>Funcionalidades incluídas nesta versão

Estão incluídas nesta versão as seguintes funcionalidades:

- [Modos de agendamento](../../project-management/scheduling-modes.md): Os gestores de projeto podem agora definir se um projeto deve ser gerido utilizando um modo de agendamento de duração fixa, trabalho fixo ou unidades fixas.

## <a name="quality-updates"></a>Atualizações de qualidade

| **Área de funcionalidades** | **Número de referência** | **Atualização de qualidade** |
| --- | --- | --- |
| Faturação e preços | 2224568 | Lógica adicional para permitir personalizações que envolvem invocar o plug-in de confirmação da fatura. |
| Faturação e preços | 2101098 | Melhorou a lógica dos campos predefinidos para a fatura pró-forma. Estes campos incluem **Morada para faturação**, **Nome para faturação** e **Termos de pagamento**. Os campos agora são predefinidos do registo correspondente do cliente do contrato de projeto. |
| Faturação e preços | 2021413 | Atualizou os campos de **Custos reais** e **Vendas** na entidade **Tarefa** para incluir valores de venda de despesas não faturadas e faturadas em tarefas. |
| Faturação e preços | 2182110 | Ao copiar um contrato de projeto, o item de contrato ID é regenerado no contrato de projeto de destino para garantir que é único. |
| Gestão de oportunidades | 2186741 | Validações adicionais para garantir que o campo **Origem** e o tipo de transação não podem ser atualizados nos detalhes da linha de proposta existentes. |
| Gestão de oportunidades | 2191353 | A criação de marcos não deve ser permitida num item de contrato de tempo e material. |
| Gestão de oportunidades | 2216956 | Problemas solucionados com **Atualizar preços**. |
| Planeamento e deteção de movimentos | 2182979 | A função de cópia do projeto melhorou para garantir que as linhas de estimativa de despesas são copiadas do projeto original. |
| Planeamento e deteção de movimentos | 2184144 | A função de cópia do projeto melhorou para garantir que o nome da posição do recurso é copiado do projeto original. |
| Planeamento e deteção de movimentos | 2184799 | Controlo apertado ao copiar um projeto para garantir que a data de início estimada não pode ser alterada enquanto a cópia está em progresso. |
| Planeamento e deteção de movimentos | 2185134 | Durante a cópia de um projeto a data de início estimada do projeto de destino está marcada para a data de hoje. |
| Planeamento e deteção de movimentos | 2196373 | Certifique-se de que os registos do gestor do projeto e dos membros da equipa não são duplicados na equipa do projeto ao copiar um projeto. |
| Planeamento e deteção de movimentos | 2211833 | As atribuições de recursos são copiadas da tarefa do projeto de origem para o projeto de destino. |
| Planeamento e deteção de movimentos | 2186541 | Problemas solucionados na grelha **Estimativas** ao agrupar por **Recurso**. |
| Planeamento e deteção de movimentos | 2166906 | A categoria de transação a partir de uma tarefa deve ser copiada para a entidade **Atribuição de recursos**. |
| Gestão de Recursos | 2125362 | Problemas solucionados com a criação de um membro genérico da equipa usando o método de atribuição baseado em horas. |
| Tempo e Despesa | 2113603 | Corrigiu o problema relacionado com a personalização com a remoção de atributos da página **Entrada de tempo**. O sistema verifica se o atributo existe na página antes de aceder ao atributo utilizando um script. |
| Tempo e Despesa | 2204377 | As folhas de tempo copiadas devem aparecer automaticamente quando selecionar **Copiar Semana**. |
| Tempo e Despesa | 2209059 | O campo **Estado** é editável para entradas de tempo do Dynamics 365 Field Service. |
