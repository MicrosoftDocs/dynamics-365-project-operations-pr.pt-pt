---
title: Faturas corrigidas – lite
description: Este tópico fornece informações sobre faturas corrigidas no Project Operations
author: rumant
manager: Annbe
ms.date: 10/15/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 55bec8ad1d9c2b55cabb453321f13df8b7cd1614
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176445"
---
# <a name="corrected-invoices---lite"></a>Faturas corrigidas – lite

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

Uma fatura de projeto confirmada pode ser corrigida para processar alterações ou créditos conforme negociado com o cliente e gestor de projeto.

Para edição de uma fatura confirmada, abra a fatura confirmada e selecione **Corrigir esta Fatura**. 

> [!NOTE]
> Esta seleção não está disponível a menos que uma fatura do projeto seja confirmada.

Uma nova fatura é criada a partir da fatura confirmada. Todos os detalhes da linha de fatura da fatura previamente confirmada são copiados para o novo rascunho. Seguem-se alguns dos pontos-chave para compreender os detalhes da linha na nova fatura corrigida:

- Todas as quantidades são atualizadas para zero. A aplicação pressupõe que todos os itens faturados são totalmente creditados. Se necessário, pode atualizar manualmente estas quantidades para refletir a quantidade que está a ser faturada e não a quantidade que está a ser creditada. Com base na quantidade que inseriu, a aplicação calcula a quantidade creditada. Este valor reflete-se nos valores reais que são criados quando a fatura corrigida é confirmada. Se estiver a fazer alterações ao valor do imposto, tem de introduzir o valor correto do imposto e não o valor do imposto que está a ser creditado.
- Os itens de contrato baseados em produtos previamente confirmados não são copiados. As correções de processamento de uma fatura de projeto baseada em produtos não são suportadas.
- As correções de marcos são sempre processadas como créditos completos.
- Os valores de sinal ou de adiantamento podem ser corrigidos se o cliente tiver sido faturado por um valor incorreto.
- As reconciliações entre os sinais e os adiantamentos podem ser corrigidas se for utilizado um montante incorreto para conciliar com as acusações de uma fatura previamente confirmada.

> [!IMPORTANT]
> Os detalhes da linha de fatura que são correções a outros encargos já faturados têm o campo **Correção** definido para **Sim**. As faturas que corrigiram os detalhes da linha de fatura têm um campo chamado **Tem correções** que também está definido para **Sim**.

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a>Valores reais criados na Confirmação de uma fatura corretiva:

Abaixo estão os valores reais criados pela aplicação na confirmação de um corretivo com base nas operações realizadas na fatura corretiva de rascunho antes da confirmação.

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
            <td width="216" rowspan="4" valign="top">
                <p>
Confirme a correção de um adiantamento ou sinal faturado.<strong></strong>
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
É criado um valor real de inversão de vendas faturado para o montante do sinal ou adiantamento para inverter as vendas faturadas originais.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
É criado um novo valor real de vendas faturado para o valor corrigido na linha de sinal ou de linha de fatura corrigida com base em adiantamento.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Um valor real de vendas não faturado de montante negativo da linha de fatura corrigida baseada em sinal ou em adiantamento, que será utilizada para a reconciliação.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
Confirmação da correção de um sinal ou adiantamento previamente reconciliado.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Uma inversão de vendas não faturada do sinal ou adiantamento que foi criado para a reconciliação. Este montante é positivo e destina-se a anular o negativo que foi criado quando a reconciliação anterior ocorreu.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Um valor real de reversão de vendas faturado para o valor da fatura anterior.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
É criado um novo valor real de vendas faturado para o montante de sinal corrigido que é aplicado na fatura corrigida.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Um valor real de vendas não faturado com um montante negativo do sinal ou em adiantamento restante corrigido, que será utilizada para a reconciliação ou faturas posteriores.
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
A fatura do marco ou o estado da faturação no item de contrato do projeto é atualizada para **Pronto a Faturar**.
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
Não suportado </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Créditos e correções de um item de contrato baseado em produto previamente faturado.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Não suportado </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]