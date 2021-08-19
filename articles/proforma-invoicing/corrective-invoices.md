---
title: Faturas corretivas baseadas em projeto
description: Esta tópico fornece informações sobre como criar e confirmar faturas corretivas baseadas em projetos no Project Operations.
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: aaa61c8473da0aab369bbb25acb10e9a3661379997737acbcc0b3d4ab33e0ce9
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997170"
---
# <a name="corrective-project-based-invoices"></a>Faturas corretivas baseadas em projeto

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

Uma fatura de projeto confirmada pode ser corrigida para processar alterações ou créditos conforme negociado com o cliente e gestor de projeto.

Para edição de uma fatura confirmada, abra a fatura confirmada e selecione **Corrigir esta Fatura**. 

> [!NOTE]
> Esta seleção não está disponível a menos que uma fatura do projeto seja confirmada ou a fatura baseada no projeto tenha adiantamentos ou retentores ou reconciliações de adiantamentos ou retentores.

Uma nova fatura é criada a partir da fatura confirmada. Todos os detalhes da linha de fatura da fatura previamente confirmada são copiados para o novo rascunho. Seguem-se alguns dos pontos-chave para compreender os detalhes da linha na nova fatura corrigida:

- Todas as quantidades são atualizadas para zero. Dynamics 365 Project Operations pressupõe que todos os itens faturados são totalmente creditados. Se necessário, pode atualizar manualmente estas quantidades para refletir a quantidade que está a ser faturada e não a quantidade que está a ser creditada. Com base na quantidade que inseriu, a aplicação calcula a quantidade creditada. Este valor reflete-se nos valores reais que são criados quando a fatura corrigida é confirmada. Se estiver a fazer alterações ao valor do imposto, tem de introduzir o valor correto do imposto e não o valor do imposto que está a ser creditado.
- As correções de marcos são sempre processadas como créditos completos.


> [!IMPORTANT]
> Para detalhes da linha de fatura que são correções a outros encargos já faturados, o campo de **Correção** é definido para **Sim**. Para faturas que têm detalhes de linha de fatura corrigidos, o campo de **Tem correções** é definido para **Sim**.

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a>Valores reais criados quando uma fatura corretiva é confirmada

A tabela a seguir lista os factos que são criados quando uma fatura corretiva é confirmada.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p>
                    <strong>Cenário</strong>
                </p>
            </td>
            <td width="808" valign="top">
                <p>
                    <strong>Valores reais criados ao confirmar</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Faturar o crédito total de uma transação de tempo previamente faturada.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Uma inversão de vendas faturada para as horas e montante no detalhe de linha original para tempo.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Um novo valor real de vendas por faturar para as horas e o montante no detalhe de linha da fatura original para tempo.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Faturar o crédito parcial numa transação de tempo.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Uma inversão de vendas faturada para as horas e montante faturados no detalhe de linha original para tempo.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Um novo valor real de vendas não faturada que é faturável pelas horas e montante no detalhe da linha de fatura editada, uma inversão deste, e um valor real de vendas faturado equivalente.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Um novo valor real de vendas não faturado que é faturável para as horas e montante restante após a dedução dos valores corrigidos no detalhe da linha de fatura.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Faturar crédito total de uma transação de despesas previamente faturada.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Uma inversão de vendas faturada para a quantidade e o montante no detalhe de linha da fatura original para as despesas.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Um novo valor real de vendas por faturar para a quantidade e o montante no detalhe de linha da fatura original para as despesas.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Faturar crédito parcial de uma transação de despesas previamente faturada.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Uma inversão de vendas faturada para a quantidade e o montante faturado no detalhe de linha da fatura original para uma despesa.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Um novo valor real de vendas não faturada que é faturável pela quantidade e montante no detalhe da linha de fatura corrigida, uma inversão deste, e um valor real de vendas faturado equivalente.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Um novo valor real de vendas não faturado que é faturável para a quantidade e montante restante após a dedução dos valores corrigidos no detalhe da linha de fatura.
                </p>
            </td>
        </tr>
                <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Faturação do crédito integral de uma transação material previamente faturada.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Uma inversão de vendas faturadas para a quantidade e montante no detalhe de linha de fatura para o material.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Um novo valor real de vendas não faturadas para a quantidade e montante no detalhe de linha de fatura para o material.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Faturar o crédito parcial numa transação material.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Uma inversão de vendas faturadas para a quantidade e montante faturado no detalhe de linha de fatura para o material.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Um novo valor real de vendas não faturadas é faturável pela quantidade e montante no detalhe da linha de fatura editada, uma inversão desta e um valor real de venda de faturação equivalente.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Um novo valor real de vendas não faturado que é faturável para a quantidade e montante restante após a dedução dos valores corrigidos no detalhe da linha de fatura.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Faturar o crédito total de uma transação de honorários previamente faturada.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Uma inversão de vendas faturada para a quantidade e o montante no detalhe de linha da fatura original para os honorários.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Um novo valor real de vendas por faturar para a quantidade e o montante no detalhe de linha da fatura original para os honorários.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Faturar o crédito parcial de uma transação de honorários previamente faturada.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Uma inversão de vendas faturada para a quantidade e o montante faturado no detalhe de linha da fatura original para honorários.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Um novo valor real de vendas não faturada que é faturável pela quantidade e montante no detalhe da linha de fatura corretiva editada, uma inversão deste, e um valor real de vendas faturado equivalente.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Faturar o crédito total de um marco previamente faturado.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Uma inversão de vendas faturada para o montante no detalhe de linha original para o marco.
                </p>
                <p>
O estado da fatura no marco é atualizado de <b>Fatura de cliente publicada</b> para <b>Pronta a faturar</b>.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Faturar o crédito parcial de um marco previamente faturado.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Este cenário não é suportado.
                </p>
            </td>
        </tr>       
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
