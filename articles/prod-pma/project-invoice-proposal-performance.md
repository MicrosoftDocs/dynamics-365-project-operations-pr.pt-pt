---
title: Desempenho da proposta de fatura de projeto
description: Este tópico fornece informações sobre melhorias de desempenho nas propostas de faturas do projeto.
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 20121-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 8b6df8baf1013720778308ce536b037dec4775f040d2925a47508fb373900f81
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 08/06/2021
ms.locfileid: "7005720"
---
# <a name="project-invoice-proposal-performance"></a>Desempenho da proposta de fatura de projeto

[!include [banner](../includes/banner.md)]

Quando criar uma nova proposta de fatura poderá encontrar problemas de desempenho à medida que o número de projetos e subprojectos aumenta. Para melhorar o desempenho, existe uma funcionalidade que reduz o tempo necessário para criar uma nova proposta de fatura para transações de projetos publicados.

## <a name="enable-project-invoice-proposal-performance-enhancement"></a>Permitir a melhoria do desempenho da proposta de fatura do projeto
Para ativar a funcionalidade de melhoria do desempenho da proposta de fatura do projeto, complete os seguintes passos.

1.  Vá à **Gestão de recursos** > **Tudo**. Na lista de funcionalidades, localize **Desempenho da proposta de fatura do Projeto**.
2.  Selecione **Ativar agora**.
3.  Atualize o seu navegador e, em seguida, crie uma nova proposta de fatura.

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a>Desligue a melhoria do desempenho da proposta de fatura do projeto
Complete os passos seguintes para desligar a melhoria do desempenho da proposta de fatura do projeto.

1.  Vá à **Gestão de recursos** > **Tudo**. Na lista de funcionalidades, localize **Desempenho da proposta de fatura do Projeto**.
2.  Selecione **Desativar**.
3.  Atualize o seu browser.

> [!NOTE]
> O desempenho da proposta de fatura não pode ser aplicado quando as regras de faturação estão ativadas.
> 
> Durante o processamento em lote para criar propostas de fatura, o número de subtarefas irá dividir as tarefas a um número máximo baseado no número de contratos com transações faturáveis, independentemente do que tenha introduzido. Por exemplo, se introduzir **3** para o número de subtarefas para a criação de propostas de fatura em lote, e só existirem dois contratos com transações faturáveis, só serão criadas duas subtarefas.
