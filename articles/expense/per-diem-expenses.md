---
title: Despesas per diem
description: Este artigo fornece informações sobre como trabalhar com despesas diárias.
author: suvaidya
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 0d2f95b677720726049d7d010e9738ad8c513802
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923202"
---
# <a name="per-diem-expenses"></a>Despesas per diem

> [!IMPORTANT] 
> A funcionalidade descrita neste artigo está disponível para utilizadores específicos como parte de uma versão de pré-visualização.

Um pagamento per diem é uma ajuda de custo diária fixa e predeterminada que a empresa paga aos seus colaboradores para alojamento (hotéis), refeições e despesas adicionais em que esses colaboradores incorrem quando viajam em trabalho. A empresa paga este valor aos colaboradores em vez de pagar as despesas reais de viagem. Os colaboradores podem utilizar as suas ajudas de custo per diem **Adicionais/Outras** para cobrir gorjetas, serviço de quartos, lavandaria ou serviços de limpeza a seco para reuniões de negócios importantes. A tarifa per diem pode variar, dependendo se o empregador opta por reembolsar o custo combinado de alojamento e refeições ou apenas o custo das refeições e adicionais.

As tarifas per diem podem basear-se na época do ano, na localização da viagem ou em ambas. Quando cria uma regra per diem, pode especificar que a percentagem da tarifa per diem será retida se um colaborador receber refeições ou serviços complementares. Também pode definir um número mínimo de horas e um número máximo de horas a que a tarifa per diem pode ser aplicada relativamente à viagem de um colaborador.

O valor per diem é calculado como a ajuda de custo total que é oferecida por dia menos a redução da refeição (custo das refeições complementares) que é fornecida ao colaborador.

## <a name="configure-per-diems"></a>Configurar per diem

Para configurar as despesas per diem, siga estes passos.

1. Aceda a **Gestão de despesas** \> **Configuração** \> **Geral** \> **Parâmetros de gestão de despesas**.
2. No separador **Per diem**, no campo **Calcular redução de refeição por**, selecione a forma como os per diem devem ser calculados:

    - **Tipo de refeição por viagem**– Calcular o per diem com base no tipo de refeição que foi inserido (pequeno-almoço, almoço ou jantar) e sobre a redução da refeição especificada para cada tipo de refeição para a ajuda de custo per diem durante a viagem.
    - **Tipo de refeição por dia**– Calcular o per diem com base no tipo de refeição que foi inserido (pequeno-almoço, almoço ou jantar) e sobre a redução da refeição especificada para cada tipo de refeição para a ajuda de custo per diem por dia.
    - **Número de refeições por dia** – Calcular o per diem com base no número de refeições introduzidas por dia e sobre a redução da refeição para o número de pessoas indicadas todos os dias.

3. Aceda a **Gestão de despesas** \> **Configuração** \> **Cálculos e códigos** \> **Localizações per diem**.
4. Adicione localizações onde os per diem podem ser utilizados.
5. Para cada localização que adicionar, no separador **Per diem**, selecione a tarifa per diem e a moeda, válidas entre datas de início e de fim específicas para situações de alojamento, refeições e outras despesas. Para configurar tarifas per diem e moedas, aceda a **Gestão de despesas** \> **Configuração** \> **Cálculos e códigos** \> **Per diems**.

## <a name="per-diems-in-the-reimagined-expense-interface"></a>Per diems na interface de despesas reinventada

A funcionalidade per diem é suportada na área de trabalho reinventada **Gestão de Despesas** no Microsoft Dynamics 365 Finance versão 10.0.25 e posterior.

Para ativar os per diem, siga estes passos.

1. Na área de trabalho **Gestão de Funcionalidades**, procure e selecione a funcionalidade **Relatórios de Despesas Reinventados** na lista e, em seguida, selecione **Ativar agora**.
2. Procure e selecione a funcionalidade **Per diem para relatórios de despesas da interface reinventada** na lista e, em seguida, selecione **Ativar agora**.

## <a name="how-the-feature-works"></a>Como funciona a característica

Esta secção fornece exemplos para três cenários de configuração. Para cada exemplo, o campo **Calcular redução da refeição** é definido com um valor diferente. Para os três exemplos, o montante total a pagamento é o mesmo até ser aplicada a redução da refeição. A partir daí, o montante total a pagamento é diferente para cada exemplo.

Para criar as despesas per diem utilizadas para os três exemplos, siga estes passos.

1. Aceda a **Áreas de trabalho** \> **Gestão de despesas**.
2. Selecione **Novo relatório de despesas** ou selecione um relatório de despesas existente.
3. Adicione uma nova despesa. No campo **Categoria**, seleccione **Per diem**. Selecione a localização e as datas de início e de fim da viagem. O valor per diem para alojamento, refeições e adicionais (outras despesas) é calculado com base na ajuda de custo diária definida para a localização selecionada.

    Por exemplo, selecione **Redmond (E.U.A.)** como localização. O valor indicado diariamente para essa localização é de 150 USD para alojamento, 75 USD para refeições e 5 USD para adicionais. A data de início é 10 de janeiro e a data de fim é 14 de janeiro. Por conseguinte, a duração selecionada é de cinco dias quando a configuração selecionada é dias de calendário com tempo, sendo que o tempo selecionado começa e termina à meia noite nas datas de início e de fim. Aqui estão os cálculos:

    - Montante total a pagamento = 5 × (150 + 75 + 5) = 5 × 230 = 1150 USD
    - Refeição e parte adicional do montante total = 5 × (75 + 5) = 400 USD

Se tiverem sido fornecidos pequeno-almoço, almoço e jantar durante a viagem, essas viagens devem ser contabilizadas para uma redução da refeição.

### <a name="example-1-per-diem-where-meal-reductions-are-based-on-meal-type-per-trip"></a>Exemplo 1: per diem em que as reduções de refeição se baseiam no tipo de refeição por viagem

Neste exemplo, a redução da refeição é de 30% para o pequeno-almoço, 30% para o almoço e 40% para o jantar. Na página **Parâmetros de gestão de despesas**, o campo **Calcular redução de refeição por** está definido como **Tipo de refeição por viagem**. Eis os cálculos se forem fornecidos três pequenos-almoços, dois almoços e zero jantares ao colaborador:

- Redução de custos = (3 × \[75 × 30%\]) + (2 × \[75 × 30%\]) + 0 = (3 × 22,50) + (2 × 22,50) + 0 = 67,50 + 45 + 0 = 112,50 USD
- Refeições e adicionais = 400 – 112,50 = 287,50 USD
- Montante total a pagamento = Ajuda de custos total – Redução de refeição = 1.150 – 112,50 = 1.037,50 USD

![Despesa per diem em que a redução de refeição se baseia no tipo de refeição por viagem.](media/1-meal-type-per-trip.png)

### <a name="example-2-per-diem-where-meal-reductions-are-based-on-meal-type-per-day"></a>Exemplo 2: per diem em que as reduções de refeição se baseiam no tipo de refeição por dia

Neste exemplo, a redução da refeição é de 30% para o pequeno-almoço, 30% para o almoço e 40% para o jantar. Na página **Parâmetros de gestão de despesas**, o campo **Calcular redução de refeição por** está definido como **Tipo de refeição por dia**. Neste caso, na grelha **Refeições** na caixa de diálogo **Editar despesa**, desmarca as caixas de verificação para indicar que refeições lhe foram fornecidas durante a viagem.

Por exemplo, eis os cálculos se tiver sido fornecido pequeno-almoço durante os primeiros três dias da viagem:

- Redução da refeição diária por cada um dos três primeiros dias = 75 × 30% = 22,50 USD
- Redução total da refeição = 3 × 22,50 = 67,50 USD
- Refeições e adicionais dos dias 1 a 3 = 75 – 22,50 = 57,50 USD
- Total de refeições e adicionais = Soma das refeições e adicionais ao longo dos cinco dias = 400 – 67,50 = 332,50 USD
- Montante total a pagamento = Montante total – Redução de refeição = 1.150 – 67,50 = 1.082,50 USD

![Despesa per diem em que a redução de refeição se baseia no tipo de refeição por dia.](media/2-meal-type-per-day.png)

### <a name="example-3-per-diem-where-meal-reductions-are-based-on-number-of-meals-per-day"></a>Exemplo 3: per diem em que as reduções de refeição se baseiam no número de refeições por dia

Neste exemplo, a redução da refeição é calculada com base no número de refeições que foram fornecidas por dia (ou seja, o campo **Calcular redução da refeição por** na página **Parâmetros de gestão de despesas** está definido para **Número de refeições por dia**). Na grelha **Refeições**, na caixa de diálogo **Editar despesa**, desmarque as caixas de verificação para indicar que refeições lhe foram fornecidas.
Neste caso, a redução da taxa de refeição baseia-se apenas no número de refeições fornecidas e não no tipo de refeição ( pequeno-almoço/almoço/jantar) fornecido.

Eis os cálculos de por diems quando as ajudas de custo diárias são de 150 USD para alojamento, 75 USD para refeições e 5 USD para adicionais:

- **Montante total a pagamento** = 5 × (150 + 75 + 5) = 5 × 230 = 1.150 USD
- **Uma refeição:** redução da refeição = 20% = 15 USD
- **Duas refeições:** redução da refeição = 50% = 37,50 USD
- **Três refeições:** redução da refeição = 100% = 75 USD

Eis os cálculos para **as ajudas de custos de refeição e adicionais**, que incluem 5 USD para adicionais:

- Dia 1 - Duas refeições fornecidas = (75 – 37,50) + 5 = 37,50 + 5 = 42,50 USD
- Dia 2 - Duas refeições fornecidas = (75 – 37,50) + 5 = 37,50 + 5 = 42,50 USD
- Dia 3 - Zero refeições fornecidas = (75 – 15) + 5 = 60 + 5 = 65 USD
- Dia 4 - Zero refeições fornecidas = (75 - 0) + 5 = 75 + 5 = 80 USD
- Dia 5 - Três refeições fornecidas = (75 – 75) + 5 = 0 + 5 = 5 USD

- Total de refeições e adicionais = Refeições e adicionais para o Dia 1 + Dia 2 + Dia 3 + Dia 4 + Dia 5 = 235 USD
- Redução total da refeição = Redução da refeição para o Dia 1 + Dia 2 + Dia 3 + Dia 4 + Dia 5 = 37,5 + 37,5 + 15 + 0 + 75 = 165 USD
- Montante total a pagamento = Ajuda de custos total – Redução total de refeição = 1.150 USD – 165 USD = 985 USD

![Despesa per diem em que a redução de refeição se baseia no número de refeições por dia.](media/3-number-of-meals-per-day.png)

> [!NOTE]
> A partir do programa Finance versão 10.0.23, se utilizar a interface de despesas reinventada, não pode criar despesas per diem que tenham datas sobrepostas. Se tentar, receberá uma mensagem de erro.
