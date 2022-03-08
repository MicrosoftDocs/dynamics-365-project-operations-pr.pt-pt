---
title: Corrigir a gestão contabilística nas propostas de fatura do projeto de rascunho
description: Este tópico explica como ajustar as informações relacionadas com a gestão contabilística numa proposta de fatura de rascunho.
author: sigitac
ms.date: 06/07/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 387dc9a81db9c22f170b664152cbafeddf72d149
ms.sourcegitcommit: e93f436afbb92a312fc71b6371866f01927e49d5
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/14/2021
ms.locfileid: "6251258"
---
# <a name="correct-the-accounting-on-draft-project-invoice-proposals"></a>Corrigir a gestão contabilística nas propostas de fatura do projeto de rascunho

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

Os *detalhes operacionais* das faturas do projeto são mantidos pelo gestor de projeto numa fatura pro forma. Estes detalhes incluem a decisão sobre as horas, as despesas, os materiais ou os marcos que têm de ser faturados, as tarifas, e a aplicação de montantes de adiantamento e de sinal. Depois de confirmar a fatura pro forma original, pode ajustar os detalhes operacionais ao criar e confirmar uma [fatura pro forma de correção](../proforma-invoicing/corrective-invoices.md).

Os *detalhes contabilísticos* para as faturas do projeto são mantidos num documento de fatura orientado para o cliente. Estes detalhes incluem o cálculo do imposto sobre vendas e as dimensões financeiras que são aplicadas à fatura. Esta tópico fornece detalhes sobre como estes detalhes contabilísticos podem ser ajustados numa proposta de fatura do projeto de rascunho.

## <a name="adjust-sales-tax"></a>Ajustar imposto sobre vendas

Os grupos de impostos sobre vendas de artigos e os grupos de impostos sobre vendas de faturação predefinidos podem ser ajustados diretamente no documento da proposta de fatura. Para ajustar estes grupos, selecione **Editar** e, em seguida, em cada linha da proposta de fatura do projeto, introduza um novo valor no campo **Grupo de impostos sobre vendas** ou **Grupo de impostos sobre vendas de artigos**.

## <a name="adjust-financial-dimensions"></a>Ajustar dimensões financeiras

Não é possível editar as dimensões financeiras diretamente numa linha da proposta de fatura do projeto. Em vez disso, siga estes passos para ajustar as dimensões financeiras numa proposta de fatura do projeto.

1. Na proposta de fatura do projeto, selecione **Eliminar tudo** para remover as linhas da proposta de fatura do projeto.

    > [!NOTE]
    > O botão **Eliminar tudo** só está disponível depois de o administrador de sistema ativar a funcionalidade **Eliminar linhas da proposta de fatura ao utilizar o Project Operations para cenários baseados em recursos/não em stock** na área de trabalho **Gestão de funcionalidades**.

2. Ajustar as dimensões financeiras:

    - **Transações na conta (marcos de faturação):** vá para **Todos os projetos** \> **Gerir** \> **Transações na conta** e selecione o marco que necessita de ajuste. Em seguida, no separador **Dimensões financeiras**, atualize os valores conforme seja necessário.
    - **Transações de tempo, despesas e materiais:** na página **Transações de projeto publicadas**, selecione **Ajustar a contabilidade** para atualizar as dimensões financeiras.

3. Depois de terminar o ajuste dos valores de dimensão financeira, vá para **Gestão de projetos e contabilística** \> **Periódica** \> **Integração do Project Operations** e selecione **Importar a partir da tabela de transição** para executar o processo periódico. Este processo utiliza os valores atualizados da dimensão financeira para recriar as linhas da proposta de fatura do projeto. Em seguida, os valores atualizados são utilizados no razão auxiliar do projeto e o razão geral quando a fatura do projeto é lançada.
