---
title: Descrição geral dos itens de contrato baseados em projetos
description: Este tópico fornece informações sobre trabalhar com itens de contrato baseados em projetos.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8af32b0475650db9c5862ea23d185588a631ade6
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003150"
---
# <a name="project-based-contract-lines-overview"></a>Descrição geral dos itens de contrato baseados em projetos

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

Os itens de contrato baseados em projetos no Dynamics 365 Project Operations destinam-se a manter os contratos de estimativa e faturação para componentes específicos do trabalho do projeto num compromisso. A estrutura de um item de contrato baseado em projetos é alargado para estimativas de projetos e cenários de faturação com os seguintes conceitos:

- Método de faturação
- Mapeamento de projetos e tarefas
- Classes de transações incluídas
- Limite a não exceder
- Configuração da exigibilidade
- Estimativas que usam detalhes do item de contrato
- Clientes do item de contrato

A tabela seguinte inclui os campos no separador **Geral** dos itens de contrato baseados em projetos que ajudam a configurar a base para uma estimativa detalhada, criada de raiz e acordos de faturação para trabalhos baseados em projetos.

| Campo | Descrição | Impacto a jusante |
| --- | --- | --- |
| **Nome** | Nome do item de contrato. Isto identifica a componente discreta do contrato que está a ser estimado. Para um contrato de projeto criado a partir de uma proposta, este valor é copiado de um valor correspondente da linha de proposta baseada em projetos. | O nome copiado para a linha de fatura do projeto que é criada a partir deste item de contrato quando a fatura é criada. |
| **Método de Faturação** | Num contrato de projeto criado a partir de uma proposta, este valor é copiado do campo correspondente na linha de proposta. Trata-se de um conjunto de opções que representa os dois principais modelos de contratação suportados pelo Project Operations:</br>- **Preço Fixo**</br>- **Tempo e Material** | Com base no método de faturação do item de contrato referenciado, a transação real será processada. Se o item de contrato referenciado pelo valor real tiver um método de faturação de tempo e material, são criados registos de valor real de custos e vendas não faturados. Se o item de contrato referenciado pelo valor real tiver um método de faturação de preço fixo, apenas é criado um valor real de custo. |
| **Project** | Utilize este campo para identificar o projeto que será usado para entregar o trabalho neste compromisso. | Este valor será utilizado em conjunto com as **Tarefas Incluídas** e as **Classes de transações incluídas** para resolver a referência do item de contrato num registo de item real ou de estimativa. |
| **Tarefas Incluídas** | Indica se este item de contrato inclui todas as tarefas do projeto para o projeto selecionado ou apenas um subconjunto das tarefas. Trata-se de um conjunto de opções que tem os seguintes valores possíveis:</br>- **Todas as Tarefas do Projeto**</br>- **Apenas Tarefas Selecionadas do Projeto**. Um valor em branco neste campo é igual a selecionar **Todas as Tarefas do Projeto**. | Se for selecionado **Apenas Tarefas Selecionadas**, pode selecionar tarefas específicas e associá-las a este item de contrato no separador **Configuração de Faturação de Tarefas** na página **Projeto**. O valor será utilizado em conjunto com **Projeto** e classes de **Transações Incluídas** para resolver a referência do item de contrato num registo de linha de valor real ou de estimativa. |
| **Incluir Tempo** | Um valor **Sim**/**Não** indica se as transações de tempo ou os custos de mão de obra no projeto selecionado serão incluídos neste item de contrato. Um valor **Não** indica que as transações de tempo ou os custos de mão de obra não serão incluídos neste item de contrato. Um valor **Sim** indica que serão. | Este valor é utilizado em conjunto com o projeto para resolver a referência do item de contrato num registo de linha real ou de estimativa. |
| **Incluir Despesa** | Um valor **Sim**/**Não** indica se os custos de despesa no projeto selecionado serão incluídos neste item de contrato. Um valor **Não** indica que os custos de despesas não serão incluídos neste item de contrato. Um valor **Sim** indica que serão. | Este valor é utilizado em conjunto com o projeto para resolver a referência do item de contrato num registo de linha real ou de estimativa. |
| **Incluir materiais** | Um valor **Sim**/**Não** indica se os custos de material no projeto selecionado serão incluídos neste item de contrato. Um valor **Não** indica que custos de material não serão incluídos neste item de contrato. Um valor **Sim** indica que serão. | Este valor é utilizado em conjunto com o projeto para resolver a referência do item de contrato num registo de linha real ou de estimativa. |
| **Incluir Taxa** | Um valor **Sim**/**Não** indica se as taxas no projeto selecionado serão incluídas neste item de contrato. Um valor **Não** indica que as taxas não serão incluídos neste item de contrato. Um valor **Sim** indica que serão. | Este valor é utilizado em conjunto com o projeto para resolver a referência do item de contrato num registo de linha real ou de estimativa. |
| **Montante Contratado** | Num item de contrato de preço fixo, este montante é o valor acordado que será faturado ao cliente por todos os componentes de trabalho associados a este item de contrato. Num item de contrato de tempo e material, este montante é um valor estimado do que será faturado ao cliente por todos os componentes de trabalho associados a este item de contrato. Num contrato de projeto criado a partir de uma proposta, este valor é copiado do campo correspondente na linha de proposta. Quando um item de contrato baseado em projetos tem detalhes de linha, este campo está bloqueado para edição e é resumido a partir do montante nos detalhes do item de contrato. | Quando o item de contrato tem detalhes de linha, este valor pode ser modificado alterando os montantes nos detalhes da linha. Num item de contrato de preço fixo, este valor é utilizado para gerar o montante antes dos impostos sobre os marcos periódicos de faturação. |
| **Imposto Estimado** | O utilizador pode editar este campo para inserir o montante estimado do imposto no item de contrato. Quando um item de contrato baseado em projetos tem detalhes de linha, este campo está bloqueado para edição e é resumido a partir do montante de impostos nos detalhes do item de contrato. | Quando o item de contrato tem detalhes de linha, este valor pode ser modificado alterando os montantes de impostos nos detalhes da linha. Num item de contrato de preço fixo, este valor é utilizado para gerar o imposto sobre os marcos periódicos de faturação. |
| **Montante Contratado após o Imposto** | O montante do item de contrato após o imposto. Este campo é apenas de leitura e é calculado como **Montante Contratado + Imposto**. | Num item de contrato de preço fixo, este valor é utilizado para gerar os marcos periódicos de faturação. |
| **Limite a Não Exceder** | O utilizador pode editar este campo e só está disponível em itens de contrato baseados em projetos que tenham o método de faturação definido como tempo e material. | O utilizador pode editar este campo. Quando um valor real para tempo e material referencia este item de contrato por tempo e material, o montante sobre o valor real é avaliado em relação ao limite a não exceder no item de contrato. Esta avaliação é concluída após a contabilização dos montantes já gastos e comprometidos. |
| **Orçamento do Cliente** | Este campo é editável e é copiado do campo correspondente na linha de proposta se o contrato foi criado a partir de uma proposta. | Este campo é utilizado apenas para informações e não tem qualquer significado a jusante. |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a>Regras de validação das opções no separador Geral dos itens de contrato baseados em projetos

Regra 1: Se o campo **Tarefas Incluídas** estiver em branco ou definido como **Todas as Tarefas do Projeto**, todas as tarefas do projeto estão incluídas no item de contrato.

Regra 2: Quando o campo **Tarefas Incluídas** estiver em branco ou explicitamente definido como **Todas as Tarefas do Projeto**, um projeto e uma determinada classe de transações só podem ser incluídos num item de contrato baseado em projetos.

Regra 3: Quando o campo **Tarefas Incluídas** estiver definido como **Apenas Tarefas do Projeto Selecionadas**, um projeto e uma determinada classe de transações podem ser incluídos em vários itens de contrato baseado em projetos de um contrato.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p>
                    <strong>Contrato</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Item de contrato</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="67" valign="top">
                <p>
                    <strong>Tarefas incluídas</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Incluir Tempo</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Incluir Despesa</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Incluir materiais</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Incluir</strong>
                </p>
                <p>
                    <strong>Taxa</strong>
                </p>
            </td>
            <td width="53" valign="top">
                <p>
                    <strong>Válido/Não válido</strong>
                </p>
            </td>
            <td width="250" valign="top">
                <p>
                    <strong>Razão</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Em branco </p>
            </td>
            <td width="48" valign="top">
                <p>
Sim </p>
            </td>
            <td width="48" valign="top">
                <p>
Sim </p>
            </td>
            <td width="42" valign="top">
                <p>
Sim </p>
            </td>
            <td width="42" valign="top">
                <p>
Sim </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Não é válido </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Violação da Regra n.º 2. O tempo, despesas, materiais e taxas no projeto P1 estão incluídos em ambos os itens de contrato CL1 e CL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Em branco </p>
            </td>
            <td width="48" valign="top">
                <p>
Sim </p>
            </td>
            <td width="48" valign="top">
                <p>
Sim </p>
            </td>
            <td width="42" valign="top">
                <p>
Sim </p>
            </td>
            <td width="42" valign="top">
                <p>
Sim </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Em branco </p>
            </td>
            <td width="48" valign="top">
                <p>
Sim </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
Sim </p>
            </td>
            <td width="42" valign="top">
                <p>
Sim </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Não é válido </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Violação da Regra n.º 2. O tempo, materiais e taxas no projeto P1 estão incluídos em ambos os itens de contrato CL1 e CL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Em branco </p>
            </td>
            <td width="48" valign="top">
                <p>
Sim </p>
            </td>
            <td width="48" valign="top">
                <p>
Sim </p>
            </td>
            <td width="42" valign="top">
                <p>
Sim </p>
            </td>
            <td width="42" valign="top">
                <p>
Sim </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Em branco </p>
            </td>
            <td width="48" valign="top">
                <p>
Sim </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
Sim </p>
            </td>
            <td width="42" valign="top">
                <p>
Sim </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Válido </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
O tempo, os materiais e as taxas no projeto P1 estão incluídos no CL1.
                </p>
                <ul>
                    <li>
As Despesas no projeto P1 estão incluídas no CL2.
                    </li>
                </ul>
                <p>
Não há sobreposição no que está a ser incluído em cada item de contrato e é, portanto, válido.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Em branco </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="48" valign="top">
                <p>
Sim </p>
            </td>
            <td width="42" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
No </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Apenas tarefas selecionadas </p>
            </td>
            <td width="48" valign="top">
                <p>
Sim </p>
            </td>
            <td width="48" valign="top">
                <p>
Sim </p>
            </td>
            <td width="42" valign="top">
                <p>
Sim </p>
            </td>
            <td width="42" valign="top">
                <p>
Sim </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Não é válido </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Violação da Regra #2 </p>
                <p>
O C1 inclui tempo, materiais, despesas e taxas num subconjunto de tarefas no projeto P1.
                </p>
                <p>
O CL2 inclui tempo, materiais, despesas e taxas para todo o projeto P1 e, portanto, sobrepõe-se ao que está incluído no C1.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Em branco </p>
            </td>
            <td width="48" valign="top">
                <p>
Sim </p>
            </td>
            <td width="48" valign="top">
                <p>
Sim </p>
            </td>
            <td width="42" valign="top">
                <p>
Sim </p>
            </td>
            <td width="42" valign="top">
                <p>
Sim </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Apenas tarefas selecionadas </p>
            </td>
            <td width="48" valign="top">
                <p>
Sim </p>
            </td>
            <td width="48" valign="top">
                <p>
Sim </p>
            </td>
            <td width="42" valign="top">
                <p>
Sim </p>
            </td>
            <td width="42" valign="top">
                <p>
Sim </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Válido </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Pela Regra n.º 3 </p>
                <p>
O C1 inclui tempo, despesas, materiais e taxas num subconjunto de tarefas no projeto P1.
                </p>
                <p>
O CL2 inclui tempo, despesas, materiais e taxas para um subconjunto de tarefas no projeto P1.
                </p>
                <p>
A única validação adicional está em redor do subconjunto de tarefas no CL1 e é diferente do subconjunto de tarefas no CL2 para garantir que não existem sobreposições. Isto é feito pelo sistema quando as tarefas são associadas.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Apenas tarefas selecionadas </p>
            </td>
            <td width="48" valign="top">
                <p>
Sim </p>
            </td>
            <td width="48" valign="top">
                <p>
Sim </p>
            </td>
            <td width="42" valign="top">
                <p>
Sim </p>
            </td>
            <td width="42" valign="top">
                <p>
Sim </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
