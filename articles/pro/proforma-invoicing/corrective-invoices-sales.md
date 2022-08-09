---
title: Faturas corretivas de projeto
description: Este artigo fornece informações sobre como criar e confirmar faturas corretivas no Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3e8e10d69368f4704ec6121106fbfd35394dc441
ms.sourcegitcommit: 95dacb0e74fa8970f56fdb1cbaa915d3fbec6e0f
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/17/2022
ms.locfileid: "9023673"
---
# <a name="corrective-project-invoices"></a>Faturas corretivas de projeto

_**Aplica-se a:** Implementação leve - negociar à faturação pró-forma, Project Operations para cenários baseados em recursos/não armazenados_

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
