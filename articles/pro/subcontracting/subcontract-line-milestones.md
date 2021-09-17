---
title: Marcos do item de subcontrato
description: Este tópico explica como criar e manter uma agenda de faturação baseada em marcos para um subcontrato com um fornecedor.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3301e5a627e4842009fcd5e352f1b76fd3053ee3
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323790"
---
# <a name="subcontract-line-milestones"></a>Marcos do item de subcontrato

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

No Dynamics 365 Project Operations, um item de subcontrato com um método de faturação de preço fixo pode especificar uma agenda de faturação baseada em marcos com o fornecedor.

Os marcos para a faturação do fornecedor podem ser gerados automaticamente utilizando uma frequência definida, ou pode criá-los manualmente.

## <a name="automatically-create-a-milestone-based-invoice-schedule-for-a-subcontract-line"></a>Criar automaticamente uma agenda de faturação baseada em marcos para um item de subcontrato

Execute os seguintes passos para gerar automaticamente uma agenda de faturação baseada em marcos para um conjunto fixo de marcos distribuídos igualmente.

1. Aceda a **Definições** > **Frequências de Fatura** e configure a frequência da fatura para os itens de subcontrato.
2. Abra a página **Subcontratos**, abra o subcontrato com o qual pretende trabalhar e, em seguida, abra o item de subcontrato de preço fixo para o qual criará uma agenda de marcos.
3. No separador **Marcos de Item de Subcontrato**, selecione **Gerar Marcos Periódicos**.
4. Na caixa de diálogo, introduza ou selecione um intervalo de datas, o número de marcos e a frequência da fatura. Pode selecionar uma data de início, ou pode selecionar o número de marcos e a frequência da fatura ou data de início, ou pode selecionar a data de fim e a frequência da fatura. Não pode selecionar a data de fim e o número de marcos.
Com estas informações, o sistema gera marcos e registos que são apresentados na grelha **Marcos**.

   - **Nome do Marco** - O nome do marco é definido com a data do marco com base na frequência da fatura.
   - **Data do Marco** - A data com base na frequência da fatura.
   - **Montante do Marco** - Calculado através da divisão do montante do subtotal no item de subcontrato pelo número de marcos.

Se o item de subcontrato tiver um valor no campo **Montante de Imposto Estimado**, este valor é adicionado a cada marco de igual forma quando gerar marcos periódicos.

A soma dos montantes no marco do item de subcontrato tem de ser igual ao valor do item de subcontrato. Se não forem iguais, ocorre um erro. Pode corrigir o erro e confirmar que o total do marco é igual ao valor do item de subcontrato, criando, editando ou eliminando os montantes de marcos e impostos. Depois de efetuadas as alterações, guarde e atualize a página para se certificar de que não existem mais erros.

## <a name="manually-create-subcontract-line-milestones"></a>Criar manualmente marcos de item de subcontrato

Os marcos de preço fixo num item de subcontrato podem ser gerados manualmente quando não são divididos periodicamente. Para criar um marco de item de subcontrato manualmente, execute os seguintes passos.

1. No painel de navegação, selecione **Subcontratos** e abra o subcontrato com o qual pretende trabalhar.
2. Abra o item de subcontrato de preço fixo para o qual pretende criar um marco.
3. No separador **Marcos do item de subcontrato**, na subgrelha, selecione **+ Novo Marco do Item de Subcontrato**.
4. Na página **Novo Marco do Item de Subcontrato**, introduza as informações necessárias com base na seguinte tabela.

    | Campo | Descrição |
    | --- | --- |
    | Nome do Marco | O nome do marco. |
    | Descrição | Uma descrição do marco.  |
    | Data do Marco | A data em que o processo de criação automática de faturas deve procurar o estado deste marco para considerá-lo para faturação. Este valor está incluído na linha de fatura do fornecedor ao faturar para este subcontrato. |
    | Montante | O montante ou valor do marco que será faturado ao cliente. Este valor está incluído na linha de fatura do fornecedor ao faturar para este subcontrato. |
    | Imposto | O valor do imposto aplicado ao marco. Este valor está incluído na linha de fatura do fornecedor ao faturar para este subcontrato. |
    | Montante após imposto | Este campo só de leitura é calculado como Montante + Imposto. Este valor está incluído na linha de fatura do fornecedor ao faturar para este subcontrato. |
    | Estado da Fatura | Quando o marco é criado, este estado é sempre definido como **Não pronto para faturação**.  Quando o estado é **Pronto para Faturar**, a criação da fatura do fornecedor inclui este marco na fatura do fornecedor. |

5. Selecione **Guardar e Fechar**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
