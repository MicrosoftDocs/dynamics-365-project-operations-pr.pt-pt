---
title: Novidades de junho de 2021 - implementação leve do Project Operations
description: Este artigo fornece informações sobre as atualizações de qualidade disponíveis na versão de junho de 2021 da implementação do Project Operations Lite.
author: sigitac
ms.date: 06/10/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 16fffb06ebb72ac25982374bff27a015eccfae1b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913956"
---
# <a name="whats-new-june-2021---project-operations-lite-deployment"></a>Novidades de junho de 2021 - implementação leve do Project Operations

_Aplica-se a: Implementação lite – negócio para faturação pró-forma_

Este artigo aplica-se aos seguintes componentes e versões do Dynamics 365 Project Operations:

  - Project Operations na versão de ambiente 4.11.0.156 ou 4.11.0.164 do Dataverse.

## <a name="quality-updates"></a>Atualizações de qualidade

| **Área de funcionalidades** | **Número de referência** | **Atualização de qualidade** |
| --- | --- | --- |
| Faturação e Preços | 2281417 | Foi corrigido o problema relativa à falha da ação de criação automática de faturas através da agenda de faturação. |
| Faturação e Preços | 2287835 |   Desempenho melhorado da confirmação de faturas. |
| Gestão de oportunidades | 2222555 | A exigibilidade das estimativas de material tem de ser copiada corretamente para os detalhes da linha de proposta ao utilizar **Importar a partir da Estimativa do Projeto**. |
| Gestão de oportunidades | 2223427 | As personalizações são agora permitidas para a ação **GenerateRetainersFromRetainerScheduleOptions**. |
| Gestão de oportunidades | 2277528 | Cálculo do valor de marco de faturação fixo para os itens de contrato do projeto com vários clientes. |
| Planeamento e Monitorização de Projetos | 2226110 | Foi corrigido o problema intermitente com a função **Gerar Requisito** na grelha **Equipa do Projeto**. |
| Planeamento e Monitorização de Projetos | 2208109 | Os utilizadores não podem criar um projeto numa moeda com tarefas relacionadas noutra moeda. |
| Planeamento e Monitorização de Projetos | 2258228 | A lista de campos permitidos para modificar com entidades **Agendamento** que utilizam a API de Agenda foi atualizada. |
| Planeamento e Monitorização de Projetos | 2293989 | O idioma correto e as definições regionais têm de ser transmitidos para a grelha **Tarefas do Projeto**.|
| Gestão de Recursos | 2220493 | Foi corrigida a experiência de utilizador na grelha **Tarefa** ao marcar rapidamente um pedido de recurso como concluído. |
| Gestão de Recursos | 2330496 | Foi corrigido o problema de carregamento **Quadro da Agenda**. (A atualização da qualidade está disponível na versão 4.11.0.164) |
| Tempo e Despesa | 2194431 | A grelha **Entrada de hora** tem de respeitar o início da semana conforme definido nas **Definições de sistema**. |
| Tempo e Despesa | 2277311 | Depois de eliminar o valor numa célula na grelha **Entrada de hora**, o cursor mantém-se na grelha. |
