---
title: Sincronizar capacidade dos recursos
description: Este tópico fornece informações sobre como sincronizar a capacidade de um recurso em calendários e projetos.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 006ebbfea42572f17663fab324a20a10321b78f0
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082382"
---
# <a name="synchronize-resource-capacity"></a>Sincronizar capacidade dos recursos

[!include [banner](../includes/banner.md)]

Os processos para a sincronização de recursos ajudam a garantir que a informação para o calendário e o calendário base passam para o agendamento de recursos do projeto. Se o calendário for alterado, os processos fazem as atualizações necessárias ao agendamento dos recursos do projeto. Os processos também ajudam a melhorar o desempenho, porque a informação dos recursos do calendário é sincronizada com antecedência. Por isso, as atualizações da informação de agendamento de recursos são mais rápidas. Recomendamos que agende os processos em lote em vez de individualmente. Caso contrário, existe o risco de alguém esquecer as datas inclusivas quando a informação foi sincronizada pela última vez. Se não forem utilizadas datas inclusivas, poderão ocorrer lacunas durante a sincronização de datas.

![Sincronização do calendário](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a>Sincronizar acumulações de capacidade dos recursos

O processo de sincronização foi concebido para sincronizar todas as informações do calendário de recursos. Estas informações incluem as informações base do calendário sobre quaisquer alterações à tabela de capacidade do Calendário de recursos do projeto. Se forem adicionados novos recursos no projeto, a sincronização ajuda a garantir que a informação do calendário atualizada está disponível. Esta sincronização pode ser feita em qualquer altura.

Recomendamos que utilize um lote. As opções estão disponíveis durante a sincronização das reservas de capacidade.

1. Selecione **Gestão de projetos e contabilística** &gt; **Periódico** &gt; **Sincronização da capacidade** &gt; **Sincronizar acumulações de capacidade dos recursos**.
2. Defina as opções na seguinte tabela.

    | Opção      | Descrição |
    |-------------|-------------|
    | Código de período | Opcionalmente, selecione o código do intervalo de datas do Razão geral para definir as datas de início e fim para o processo de sincronização para acumulações de capacidade de recursos. |
    | Data de início  | Introduza a data de início para o processo de sincronização para acumulações de capacidade de recursos. |
    | Data de fim    | Introduza a data de fim para o processo de sincronização para acumulações de capacidade de recursos. |

[![Processo de sincronização](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]