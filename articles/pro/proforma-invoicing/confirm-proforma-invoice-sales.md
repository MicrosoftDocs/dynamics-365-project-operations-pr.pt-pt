---
title: Confirmar uma fatura pró-forma do projeto
description: Este artigo fornece informações sobre a confirmação de faturas de projeto proforma no Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 101e4564fcf57cbbfc713773ed760291b9d28410
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922236"
---
# <a name="confirm-a-proforma-project-invoice"></a>Confirmar uma fatura pró-forma do projeto 

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_


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
Um valor real de vendas não faturado de um montante negativo do sinal ou em adiantamento a ser utilizado para a reconciliação.
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
Um novo valor real de vendas não faturada que é não faturável pelas horas e montante restantes depois de deduzir os números corrigidos no detalhe da linha de fatura editada, uma inversão do valor real de vendas, e um valor real de vendas faturado equivalente.
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
Um valor real de vendas faturado para a quantidade e montante na aprovação de despesa original </p>
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
        <tr>
            <td width="216" valign="top">
                <p>
Faturar um item de contrato baseado em produtos.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Um valor real de vendas faturado para a linha do produto com a quantidade e montante provenientes do item de contrato baseado em produtos.
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
