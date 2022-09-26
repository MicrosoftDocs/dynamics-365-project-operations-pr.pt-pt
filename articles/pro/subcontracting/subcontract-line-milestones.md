---
title: Marcos do item de subcontrato
description: Este artigo explica como criar e manter uma agenda de faturas baseada em marcos para um subcontrato com um fornecedor.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 431a57adf82c79f72d44886636183d48e0931f53
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522479"
---
# <a name="subcontract-line-milestones"></a>Marcos do item de subcontrato

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

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

    | Campo | Descrição |Impacto funcional|
    | --- | --- |----------------------|
    | Nome do Marco | O nome do marco. |Será mostrado como a primeira coluna em todas as procuras baseadas em marcos do item de subcontrato. A linha da fatura do fornecedor criada com base neste marco também utilizará o nome do marco do item de subcontrato como o nome predefinido da linha da fatura do fornecedor.|
    | Descrição | Uma descrição do marco. |A linha da fatura do fornecedor criada com base neste marco também utilizará a descrição do marco do item de subcontrato como a descrição predefinida da linha da fatura do fornecedor.|
    | Data do Marco | A data em que o processo de criação automática de faturas deve procurar o estado deste marco para considerá-lo para faturação.| Este valor será utilizado como a data predefinida da linha da fatura do fornecedor aquando da faturação deste item de subcontrato. |
    | Montante | O montante ou valor do marco que será faturado ao cliente. |Este valor é utilizado como o montante predefinido da linha da fatura do fornecedor aquando da faturação deste item de subcontrato. |
    | Imposto | O valor do imposto aplicado ao marco.| Este valor é utilizado como o montante de imposto predefinido da linha da fatura do fornecedor aquando da faturação deste item de subcontrato. |
    | Montante após imposto | Este campo só de leitura é calculado como Valor + Imposto.|Este valor é utilizado como a predefinição da linha da fatura do fornecedor aquando da faturação deste item de subcontrato. |
    | Estado da Fatura | Quando o marco é criado, este estado é sempre definido como **Não pronto para faturação**.|  Quando o estado é **Pronto para Faturar**, a criação da fatura do fornecedor inclui este marco na fatura do fornecedor. |

5. Selecione **Guardar e Fechar**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
