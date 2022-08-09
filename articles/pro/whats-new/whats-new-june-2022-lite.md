---
title: Novidades de junho de 2022 - implementação leve do Project Operations
description: Este artigo fornece informações sobre as atualizações de qualidade que estão disponíveis na versão de junho de 2022 da implementação lite do Microsoft Dynamics 365 Project Operations.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 8313288ecf7ff1350cd82c62d3d0c291d8a3ded4
ms.sourcegitcommit: 7772d72a7c96a44ffb23369f8ffb436813449239
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/20/2022
ms.locfileid: "9031207"
---
# <a name="whats-new-june-2022---project-operations-lite-deployment"></a>Novidades de junho de 2022 - implementação leve do Project Operations

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

Este artigo aplica-se aos seguintes componentes e versões do Microsoft Dynamics 365 Project Operations:

- Project Operations num ambiente Dataverse, versão 4.43.0.77 ou 4.43.0.119

## <a name="quality-updates"></a>Atualizações de qualidade

| Área de funcionalidades | Número de referência | Atualização de qualidade |
| --- | --- | --- |
| Subcontratos | 2708885 | Corrigida a mensagem de erro que aparecia quando um utilizador criava um registo de cabeçalho de reserva de recursos reservável onde nenhum recurso reservável foi preenchido. |
| Planeamento e monitorização de projetos | 2629441 | Corrigida a lógica de acionamento do fluxo de trabalho para ajudar a impedir um ciclo infinito quando as tarefas do projeto são atualizadas. |
| Tempo e despesa | 2641209 | As importações de entrada de tempo a partir de atribuições/reservas têm de reter uma referência de recurso reservável. |
| Planeamento e monitorização de projetos | 2651148 | O cabeçalho de documentos do projeto tem de ser protegido.|
| Planeamento e monitorização de projetos | 2653145 | Validações adicionadas para garantir que não é possível criar um registo de projeto que tenha carateres não válidos no mesmo. |
| Tempo e despesa | 2654710 | Corrigida a filtragem na página **Aprovações**. |
| Faturação e preços | 2667805 | Validações adicionadas para ajudar a impedir a criação de valores reais de vendas faturados se não existirem valores reais de vendas não faturados. |
| Faturação e preços | 2668378 | Validações adicionadas para ajudar a impedir a adição de uma dimensão de preços personalizada, a menos que um nome lógico e um nome de campo sejam preenchidos. |
| Tempo e despesa | 2700428 | Melhorada a lógica de aprovações para garantir que outros conjuntos de aprovações para o projeto podem ser processados, mesmo que um dos conjuntos de aprovações esteja preso em tarefas de sistema. |
