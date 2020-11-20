---
title: Adiantamentos e contratos baseados em sinais – lite
description: Este tópico fornece informações sobre modelos de contratação baseados em sinais e adiantamentos no Project Operations.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 912b235af5e561349fdfb481e5f5b7c5514669c3
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180881"
---
# <a name="advances-and-retainer-based-contracts---lite"></a>Adiantamentos e contratos baseados em sinais – lite


_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

O Dynamics 365 Project Operations suporta contratos baseados em sinais. Um contrato baseado em sinais é um conjunto negociado de pagamentos igualmente distribuídos que o cliente será faturado durante toda a duração de um projeto. Este tipo de contrato é normalmente utilizado para modelos de faturação baseados em tempo e material ou consumo, onde é necessário dar ao cliente uma fatura e horário de pagamento previsíveis. Os valores reais de receitas acumuladas em cada período são reconciliados com o pagamento recebido pelo cliente no início do período. De acordo com o conceito do modelo de faturação de tempo e material, os valores de receita acumulados em cada período podem variar com os custos incorridos. Se as receitas acumuladas forem superiores ao montante recebido no início do período, a empresa de entrega do projeto poderá:

- Apenas faturar o cliente pelo excedente 
- Adiar a reconciliação das receitas para o próximo período de faturação e fazer uma conta final no final do projeto para quaisquer receitas restantes não reconciliadas

A principal diferença entre um modelo de contratação baseado em sinais e um modelo de contrato de preço fixo no Project Operations é que, no modelo do contrato de preço fixo, o valor da fatura não está ligado ou associado aos custos incorridos. A faturação segue uma abordagem baseada em marcos que está alinhada com os custos incorridos para esse período. Num contrato baseado em sinais, as receitas que podem ser faturadas são registadas com base no método de faturação do item de contrato. Quando o método de faturação é tempo e material, as receitas faturáveis estão ligadas aos custos incorridos em cada período e podem variar de período para período. No entanto, o cliente só é faturado pelo valor do sinal periódico. O sistema utiliza outra fatura no final do período para conciliar as receitas faturadas registadas durante o período em relação ao montante que o cliente foi faturado no início do período.

A vantagem deste método é que os custos do cliente se tornem previsíveis na agenda do sinal, ao contrário de um modelo típico de tempo e material. A organização que entrega o projeto também tem alguma margem para cobrir o risco de recuperação dos custos incorridos devido a quaisquer aumentos de âmbito que um modelo de preço fixo não lhe permitisse.

Além de um agenda periódica baseada em sinais, o Project Operations pode registar um adiantamento único de um cliente e conciliar isso com os diferentes componentes de custos do projeto.

O sinal no Project Operations não está disponível para utilização até que seja faturado ao cliente. Isto é indicado pelos seguintes campos na subgrelha para adiantamentos e sinais.

| Campo | Descrição | Impacto a jusante |
| --- | --- | --- |
| Valor disponível | O montante disponível para ser utilizado no registo de sinal ou adiantamento. | Até que o adiantamento ou sinal seja faturado, não está disponível para ser usado, o que significa que o valor disponível será zero. |
| Montante usado | O montante já utilizado no sinal ou adiantamento. | Um adiantamento ou sinal pode ser parcialmente reconciliado numa fatura com valores reais de custos que terão alguma parte marcada como já utilizada ou consumida. O resto do montante de adiantamento ou de sinal está disponível para conciliar numa futura fatura com os valores reais dos custos. |
