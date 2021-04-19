---
title: Confirmar uma fatura pró-forma baseada em projeto
description: Esta tópico fornece informações sobre a confirmação de uma fatura baseada em projetos pró-forma.
author: rumant
manager: AnnBe
ms.date: 04/05/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 53c647dca506822312053fb5c9b086a2947974c2
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867145"
---
# <a name="confirm-a-proforma-project-based-invoice"></a>Confirmar uma fatura pró-forma baseada em projeto

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

Após a confirmação de uma fatura pró-forma, o estado da fatura do projeto atualiza para **Confirmada**. Quando uma fatura é confirmada, torna-se apenas de leitura. Avançando, a fatura só pode ser corrigida se houver alguma correção ou crédito iniciado pelo cliente.

A tabela seguinte lista os valores reais criados pelo sistema. Estes valores reais são criados quando determinadas operações são realizadas na fatura do projeto antes de ser confirmada.

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
Faturar um adiantamento ou um sinal </p>
            </td>
            <td width="408" valign="top">
                <p>
Um valor real de vendas faturado do tipo <strong>Sinal</strong> é criado para o montante sobre o adiantamento ou sinal.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Um valor real de venda não faturada com um montante negativo do retentor ou adiantamento a utilizar para a reconciliação.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Depois de reconciliar completamente um sinal ou adiantamento numa fatura.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Uma inversão de vendas não faturada do sinal ou adiantamento que foi criado para a reconciliação. Este montante é positivo porque se destina a anular o negativo que foi criado quando o sinal ou adiantamento foi faturado.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Um valor real de vendas faturado para o valor nesta fatura.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Depois de reconciliar parcialmente um sinal ou adiantamento numa fatura.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Uma inversão de vendas não faturada do sinal ou adiantamento que foi criado para a reconciliação. Este montante é positivo porque se destina a anular o negativo que foi criado quando o sinal ou adiantamento foi faturado.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Um valor real de vendas faturado para o valor nesta fatura.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Um valor real de vendas não faturado negativo do montante restante do sinal ou adiantamento a ser utilizado para a reconciliação em faturas futuras.
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
Um novo valor real de vendas não faturada que é faturável pelas horas e montante no detalhe da linha de fatura editada, uma inversão do valor real de vendas, e um valor real de vendas faturado equivalente.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Uma nova venda não faturada real que é não faturável para as horas restantes e montante após dedução dos valores corrigidos no detalhe da linha de fatura editada, uma inversão das vendas efetivas e um equivalente faturado de valor real de vendas.
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
Faturação de uma transação material sem edições na fatura do projeto.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Uma inversão de vendas não faturadas para a quantidade e montante na aprovação original de utilização do material.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Um valor real de vendas faturadas para a quantidade e montante na aprovação original de utilização do material.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Faturar uma transação de material que foi editada para reduzir a quantidade.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Uma inversão de vendas não faturadas para a quantidade e montante na aprovação original de tempo original.
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
Faturar uma transação de material que foi editada para aumentar a quantidade.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Uma inversão de vendas não faturadas para a quantidade e montante na aprovação original de utilização do material.
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

[!INCLUDE[footer-include](../includes/footer-banner.md)]
