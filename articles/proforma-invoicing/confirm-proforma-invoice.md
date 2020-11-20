---
title: Confirmar uma fatura pró-forma
description: Este tópico fornece informações sobre como confirmar uma fatura pró-forma.
author: rumant
manager: AnnBe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fa1e6c17fbda76a283c2ec68760a00e846decf83
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128117"
---
# <a name="confirm-a-proforma-invoice"></a>Confirmar uma fatura pró-forma

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

Após a confirmação de uma fatura pró-forma, o estado da fatura do projeto atualiza para **Confirmada**. Quando uma fatura é confirmada, torna-se apenas de leitura. Daí para a frente, a fatura só pode ser corrigida se houver alguma correção ou crédito iniciado pelo cliente, ou quando estiver marcada como paga.

A tabela seguinte lista os valores reais criados pelo sistema. Estes valores reais são criados quando determinadas operações são realizadas na fatura do projeto antes de ser confirmada.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="416" valign="top">
                <p>
                    <strong>Cenário</strong>
                </p>
            </td>
            <td width="608" valign="top">
                <p>
                    <strong>Valores reais criados ao confirmar</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Faturar uma transação de tempo sem edições na fatura de rascunho.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Uma inversão de vendas não faturada para as horas e montante na aprovação de tempo original.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Um valor real de vendas faturado para as horas e montante na aprovação de tempo original.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Faturar uma transação de tempo que foi editada para reduzir a quantidade.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Uma inversão de vendas não faturada para as horas e montante na aprovação de tempo original.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Um novo valor real de vendas não faturada que é faturável pelas horas e montante no detalhe da linha de fatura editada, uma inversão do valor real de vendas não faturado, e um valor real de vendas faturado equivalente.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Um novo valor real de vendas não faturada que é não faturável pelas horas e montante restantes depois de deduzir os números corrigidos no detalhe da linha de fatura editada, uma inversão do valor real de vendas não faturado, e um valor real de vendas faturado equivalente.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Faturar uma transação de tempo que foi editada para aumentar a quantidade.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Uma inversão de vendas não faturada para as horas e montante na aprovação de tempo original.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Um novo valor real de vendas não faturada que é faturável pelas horas e montante no detalhe da linha de fatura editada, uma inversão do valor real de vendas não faturado, e um valor real de vendas faturado equivalente.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Faturar uma transação de despesa sem edições na fatura de rascunho.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Uma inversão de vendas não faturada para a quantidade e montante na aprovação de despesa original.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Um valor real de vendas faturado para a quantidade e montante na aprovação de despesa original.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Faturar uma transação de despesa que foi editada para reduzir a quantidade.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Uma inversão de vendas não faturada para a quantidade e montante na aprovação de despesa original.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Um novo valor real de vendas não faturada que é faturável pela quantidade e montante no detalhe da linha de fatura editada, uma inversão do valor real de vendas não faturado, e um valor real de vendas faturado equivalente. 
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Um novo valor real de vendas não faturada que é não faturável pela quantidade e montante restantes depois de deduzir os números corrigidos no detalhe da linha de fatura editada, uma inversão do valor real de vendas não faturado, e um valor real de vendas faturado equivalente.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Faturar uma transação de despesa que foi editada para aumentar a quantidade.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Uma inversão de vendas não faturada para a quantidade e montante na aprovação de despesa original.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Um novo valor real de vendas não faturada que é faturável pela quantidade e montante no detalhe da linha de fatura editada, uma inversão do valor real de vendas não faturado, e um valor real de vendas faturado equivalente.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Faturar uma taxa.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Uma inversão de vendas não faturada para o montante da taxa na linha do diário original.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Um valor real de vendas faturado para a quantidade e montante na linha de diário de taxa original.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Faturar um marco.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Um valor real de vendas faturado para o montante de marco no marco original no item de contrato do projeto.
                </p>
            </td>
        </tr>
    </tbody>
</table>
