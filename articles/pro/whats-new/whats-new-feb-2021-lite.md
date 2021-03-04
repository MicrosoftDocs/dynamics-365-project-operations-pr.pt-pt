---
title: O que há de novo fevereiro de 2021 - Implementação de Project Operations lite
description: Este tópico fornece informações sobre as atualizações de qualidade disponíveis na versão de fevereiro de 2021 da implementação do Project Operations lite.
author: sigitac
manager: tfehr
ms.date: 02/08/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: bfc4c622c423e689938e58666ae47abbe3c23d48
ms.sourcegitcommit: 625b5244aaadff5a24a79d9addff91f87c6b015a
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/09/2021
ms.locfileid: "5141342"
---
# <a name="whats-new-february-2021---project-operations-lite-deployment"></a>O que há de novo fevereiro de 2021 - Implementação de Project Operations lite

Este tópico aplica-se aos seguintes componentes e versões do Dynamics 365 Project Operations:

  - Project Operations na versão 4.7.0.95 do ambiente Dataverse

## <a name="quality-updates"></a>Atualizações de qualidade

| **Área de funcionalidades** | **Número de referência** | **Atualização de qualidade** |
| --- | --- | --- |
| **Faturação e Preços** | 2053736 | Os detalhes da linha de fatura passam a estar acessíveis através **Fatura** > **Informação relacionada**. |
| **Faturação e Preços** | 2122613 | As ações **Ativar** e **Desativar** foram removidas das entidades da associação **Lista de preços**. |
| **Faturação e Preços** | 2128606 | Resolveu o problema com **ullReferenceException** no plug-in **GetEstimatesForProject**. |
| **Implementação e configuração** | 2140569 | A solução de projeto não deve ser instalada nos ambientes Equipas Dataverse. |
| **Implementação e configuração** | 2086991 | Localização restrita de personalização de recursos web. |
| **Gestão de oportunidades** | 2136794 | Apresenta uma mensagem de erro correta quando o processo **Confirmar fatura** ou **Marcar fatura como paga** falha, |
| **Gestão de oportunidades** | 2146376 | O valor do imposto corrigido num valor real não faturável é criado a partir da confirmação da fatura. |
| **Planeamento e Monitorização de Projetos** | 2099879 | A implementação do ambiente Dataverse deve criar uma categoria de transação padrão com um ID estático e não gerar aleatoriamente um por ambiente. |
| **Planeamento e Monitorização de Projetos** | 2128577 | Fixou os privilégios do utilizador do Project Service para atualizar a categoria de transação numa atribuição de recursos. |
| **Planeamento e Monitorização de Projetos** | 2164035 | Problemas solucionados com a função **Copiar**. |
| **Entrada de hora** | 2129161 | São aplicadas restrições mais apertadas para garantir que os utilizadores não podem alterar e atualizar uma entrada de tempo que tenha sido submetida ou aprovada. |
| **Entrada de hora** | 2103572 | A aprovação do tempo para as entradas no tempo não-projeto não deve estar à procura de um papel aprovador do projeto. |
