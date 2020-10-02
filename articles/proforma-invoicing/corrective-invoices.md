---
title: Faturas corrigidas
description: Este tópico fornece informações sobre as faturas corrigidas.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e14da1c07d5b697de6caf1b9041c30581ecff102
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898095"
---
# <a name="corrected-invoices"></a>Faturas corrigidas

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

As faturas corrigidas podem ser editadas. Quando edita uma fatura confirmada, um rascunho da fatura corrigida é criado. Dado que a pressuposição é que pretende reverter todas as transações e quantidades da fatura original, a fatura corrigida inclui todas as transações da fatura original e todas as quantidades são zero (0).

Quando alguma transação não necessitar de correção, pode removê-la da fatura corretiva de rascunho. Para reverter ou devolver apenas uma quantidade parcial, pode editar o campo Quantidade no detalhe de linha. Se abrir o detalhe de linha de fatura, poderá ver a quantidade original da fatura. Em seguida, pode editar a quantidade da fatura atual para que seja inferior ou superior à quantidade original da fatura.

Quando confirma uma fatura corretiva, o valor real de vendas faturadas originais é revertido e é criado um novo valor real de vendas faturadas. Se a quantidade tiver sido reduzida, a diferença causará a criação de um novo valor real de vendas não faturadas. Por exemplo, se a venda faturada original era de oito horas e o detalhe de linha de fatura corrigida tiver uma quantidade reduzida de seis horas, a linha de vendas faturadas originais é revertida e são criados dois novos valores reais:

- Um valor real de vendas faturadas durante seis horas.
- Uma valor real de vendas não faturadas para as duas horas restantes. Esta transação pode ser faturada mais tarde ou marcada como não faturável, dependendo das negociações com o cliente.
