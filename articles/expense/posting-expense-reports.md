---
title: Publicar relatórios de despesas
description: Este artigo explica como publicar relatórios de despesas.
author: ramagadu
ms.date: 08/12/2022
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: d0ae4559a08553236158a663513401cb38cbe28f
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 09/16/2022
ms.locfileid: "9524884"
---
# <a name="post-expense-reports"></a>Publicar relatórios de despesas

Após a aprovação e transferência de um relatório de despesas para o diário geral, pode ser lançado. Quando lança um relatório de despesas, as despesas elegíveis para recuperação de Imposto sobre o Valor Acrescentado (IVA) são identificadas. A tarefa de verificação e recuperação dos pagamentos do IVA é atribuída ao funcionário responsável pela verificação do relatório de despesas.

Se as despesas num relatório de despesas forem cobradas a uma empresa diferente da empresa que emprega o funcionário, tem de verificar tanto a empresa à qual essas despesas são devidas como a empresa que as deve. Por exemplo, o funcionário que submeteu um relatório de despesas trabalha para a empresa DAT, mas cobrou uma despesa à empresa DIR. Neste caso, a DAT é a empresa à qual a despesa é devida e a DIR é a empresa que deve a despesa. Depois de verificar estas linhas do diário, pode lançar as linhas de despesas no razão geral.

Para lançar um relatório de despesas, na página **Relatórios de despesas aprovados**, selecione o relatório de despesas e, em seguida, no Painel de Ação, selecione **Publicar**.

Também pode lançar todos os relatórios de despesas na lista ao mesmo tempo. Selecione todos os relatórios de despesas e, em seguida, selecione **Publicar**.

## <a name="enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature"></a>Ativar a caraterística Capacidade de publicar o passivo de despesas na moeda do fornecedor para o método de pagamento em numerário

A caraterística **Capacidade de publicar o passivo de despesas na moeda do fornecedor para o método de pagamento em numerário** permite a publicação de relatórios de despesas numa moeda de fornecedor para o método de pagamento em numerário.

Atualmente, quando submete despesas em numerário, os relatórios de despesas são publicados na moeda contabilística. Devido à conversão do montante entre a moeda de transação, a moeda contabilística e a moeda do fornecedor, é pago um montante incorreto aos fornecedores se a data da transação da despesa e a data de pagamento real tiver taxas de câmbio diferentes.

Esta caraterística irá assegurar que o saldo do fornecedor é registado na moeda do fornecedor quando o relatório de despesas é publicado.

1. Aceda a **Áreas de Trabalho** \> **Gestão de Funcionalidades**.
2. Na lista, localize e selecione **Capacidade de publicar o passivo de despesas na moeda do fornecedor para o método de pagamento em numerário** e, em seguida, selecione **Ativar agora**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
