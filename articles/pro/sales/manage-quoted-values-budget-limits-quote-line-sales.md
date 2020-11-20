---
title: Descrição geral de linhas de proposta baseadas em projetos – lite
description: Este tópico fornece informações sobre como utilizar linhas de proposta baseadas no projeto para o trabalho de projeto. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: be1663c0d226fa19fe4b9df566e16d215f1fc08e
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181106"
---
# <a name="project-based-quote-lines-overview---lite"></a>Descrição geral de linhas de proposta baseadas em projetos – lite

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

As linhas de proposta baseadas em projetos foram concebidas para ajudar a estimar o trabalho do projeto numa cativação. A estrutura de uma linha de proposta baseada em projetos é expandida para as estimativas de projeto com os seguintes conceitos:

- Método de Faturação
- Mapeamento de Projetos e Tarefas
- Classes de transações incluídas
- Limite a Não Exceder
- Configuração da exigibilidade
- Estimativa baseada nos Detalhes de Linha de Proposta
- Clientes da Linha de Proposta

A tabela seguinte fornece informações sobre os campos no separador **Geral** da linha de proposta baseada em projetos. Estes campos ajudam a configurar a base para uma estimativa de raiz detalhada para o trabalho de projeto.

| **Campo** | **Descrição** | **Impacto a jusante** |
| --- | --- | --- |
| Nome | O nome da linha de proposta que deve ajudá-lo a identificar o componente discreto da proposta que está a ser estimada. | Copiada para o item de contrato do projeto que é criada a partir desta linha de proposta quando a proposta é ganha. |
| Método de Faturação | Numa proposta criada a partir de uma oportunidade, este valor é copiado a partir do campo correspondente na linha de oportunidade. Este campo inclui os dois principais modelos de contratação suportados pelo Dynamics 365 Project Operations:</br>- Preço fixo</br>- Tempo e material.| Este valor do campo é copiado para o item de contrato do projeto que é criado a partir desta linha de proposta quando a proposta é ganha. |
| Project | Utilize este campo opcional para identificar o projeto que será utilizado para entregar o trabalho nesta cativação. Quando um projeto é mapeado para uma linha de proposta, ajuda a configurar as tarefas faturáveis e também a trazer uma estimativa baseada em projetos para a linha de proposta como detalhes da linha de proposta. Quando um projeto não é mapeado para uma linha de proposta baseada em projetos, a estimativa deve ser criada manualmente ao criar cada detalhe da linha de proposta. | Este valor do campo é copiado para o item de contrato do projeto que é criado a partir desta linha de proposta quando a proposta é ganha.|
| Tarefas Incluídas | Indica se esta linha de proposta é utilizada para todas ou algumas tarefas do projeto para o projeto selecionado. Este campo tem os seguintes valores possíveis:</br>- Todas as tarefas do projeto</br>- Apenas tarefas selecionadas do projeto</br>Um valor em branco neste campo é equivalente à opção **Todas as tarefas do projeto**. | Quando **Apenas tarefas selecionadas do projeto** é selecionado na página do projeto, o separador **Configuração de Faturação de Tarefas** permite selecionar tarefas específicas para as associar a esta linha de proposta. Este valor do campo é copiado para o item de contrato do projeto que é criado a partir desta linha de proposta quando a proposta é ganha. |
| Incluir Tempo | Um sinalizador **Sim**/**Não** indica se as transações de tempo ou os custos de mão de obra no projeto selecionado serão incluídos na estimativa nesta linha de proposta. Um valor **Não** indica que as transações de tempo ou o custo de mão de obra não será incluído na estimativa nesta linha de proposta. Um valor **Sim** indica que as transações de tempo ou o custo de mão de obra será incluído na estimativa nesta linha de proposta. | Este valor do campo é copiado para o item de contrato do projeto que é criado a partir desta linha de proposta quando a proposta é ganha. |
| Incluir Despesa | Um sinalizador **Sim**/**Não** indica se os custos de despesa no projeto selecionado serão incluídos na estimativa nesta linha de proposta. Um valor **Não** indica que o custo de despesa não será incluído na estimativa nesta linha de proposta. Um valor **Sim** indica que o custo de despesa será incluído na estimativa nesta linha de proposta. | Este valor do campo é copiado para o item de contrato do projeto que é criado a partir desta linha de proposta quando a proposta é ganha. |
| Incluir Taxa | Um sinalizador **Sim**/**Não** indica se as tarifas no projeto selecionado serão incluídos na estimativa nesta linha de proposta. Um valor **Não** indica que as Tarifas não serão incluídas na estimativa nesta linha de proposta. Um valor **Sim** indica que as Tarifas serão incluídas na estimativa nesta linha de proposta. | Este valor do campo é copiado para o item de contrato do Projeto que é criado a partir desta linha de proposta quando a proposta é ganha. |
| Montante da Proposta | Este é o montante que será proposto ao cliente por todo o trabalho previsto nesta linha de proposta baseada em projetos. Numa proposta criada a partir de uma oportunidade, este valor é copiado a partir do campo **Orçamento do Cliente** na linha de oportunidade. Quando a linha de proposta baseada em projetos tem detalhes da linha, este campo é bloqueado para edição e é resumido a partir do montante nos detalhes da linha de proposta. | Este valor do campo é copiado para o item de contrato do projeto que é criado a partir desta linha de proposta quando a proposta é ganha. |
| Imposto Estimado | Este é um campo editável para o utilizador adicionar o montante do imposto estimado na linha de proposta. Quando uma linha de proposta baseada em projetos tem detalhes da linha, este campo é bloqueado para edição e é resumido a partir do montante do imposto nos detalhes da linha de proposta. | Este valor do campo é copiado para o item de contrato do projeto que é criado a partir desta linha de proposta quando a proposta é ganha. |
| Montante da Proposta Após o Imposto | Este campo é o montante da linha de proposta após impostos e é só de leitura. O montante neste campo é calculado como *Montante da Proposta + Imposto*. | Este valor do campo é copiado para o item de contrato do projeto que é criado a partir desta linha de proposta quando a proposta é ganha. |
| Limite a não exceder | Este campo é editável e só está disponível em linhas de proposta baseadas em projetos que têm um método de faturação **Tempo e Material**. | Este valor do campo é copiado para o item de contrato do projeto que é criado a partir desta linha de proposta quando a proposta é ganha. |
| Orçamento do Cliente | Este campo é editável e é copiado a partir do campo correspondente na linha de oportunidade se a proposta tiver sido criada a partir de uma oportunidade. | Este valor do campo é copiado para o item de contrato do projeto que é criado a partir desta linha de proposta quando a proposta é ganha. |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a>Regras de validação para os campos no separador Geral das linhas de proposta baseadas em projetos

**Regra 1**: se o campo **Tarefas Incluídas** estiver em branco ou se estiver definido como **Todas as tarefas do projeto**, é incluído um projeto na linha de proposta.

**Regra 2**: se o campo **Tarefas Incluídas** estiver em branco, ou se estiver definido como **Todas as tarefas do projeto**, um projeto e uma determinada classe de transações só podem ser incluídos numa linha de proposta baseada em projetos de uma proposta.

**Regra 3**: se o campo **Tarefas Incluídas** estiver definido como **Apenas tarefas selecionadas do projeto**, um projeto e uma determinada classe de transações só podem ser incluídos em várias linhas de proposta baseadas em projetos de uma proposta.

**Regra 4**: se uma oportunidade tiver várias proposta, poderá haver linhas de proposta de diferentes propostas em que todas referenciam o mesmo projeto e incluem a mesma classe de transações.

**Regra 5**: se as propostas não pertencerem à mesma oportunidade, não poderão incluir o mesmo projeto e classe de transações.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p>
                    <strong>Oportunidade</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Proposta</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Linha de proposta</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="90" valign="top">
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
                    <strong>Incluir</strong>
                </p>
                <p>
                    <strong>Taxa</strong>
                </p>
            </td>
            <td width="54" valign="top">
                <p>
                    <strong>Válido/Não válido</strong>
                </p>
            </td>
            <td width="308" valign="top">
                <p>
                    <strong>Razão</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Em Branco </p>
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
            <td width="54" rowspan="2" valign="top">
                <p>
Não é válido </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Violação da Regra n.º 2. O Tempo, a Despesa e as Tarifas no projeto P1 estão incluídos nas linhas de proposta, QL1 e QL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Em Branco </p>
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
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Em Branco </p>
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
            <td width="54" rowspan="2" valign="top">
                <p>
Não é válido </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Violação da Regra n.º 2. O Tempo e as Tarifas no projeto P1 estão incluídos nas linhas de proposta, QL1 e QL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Em Branco </p>
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
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Em Branco </p>
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
            <td width="54" rowspan="2" valign="top">
                <p>
Válido </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
Tempo e Tarifas no projeto P1 estão incluídos no QL1.
As Despesas no projeto P1 estão incluídas no QL2.
Não existe sobreposição no que está a ser incluído em cada linha de proposta e é válido.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Em Branco </p>
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
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
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
            <td width="54" rowspan="2" valign="top">
                <p>
Não é válido </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Violação da Regra n.º 2 acima. </p>
                <p>
O Q1 inclui Tempo, Despesas e Tarifas num subconjunto de tarefas no projeto P1.
                </p>
                <p>
O QL2 inclui Tempo, Despesas e Tarifas para todo o projeto P1 e sobrepõe-se ao que está incluído no Q1.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Em Branco </p>
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
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
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
            <td width="54" rowspan="2" valign="top">
                <p>
Válido </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Pela Regra n.º 3 acima, </p>
                <p>
O Q1 inclui Tempo, Despesas e Tarifas num subconjunto de tarefas no projeto P1.
                </p>
                <p>
O QL2 inclui Tempo, Despesas e Tarifas para um subconjunto de tarefas no projeto P1.
                </p>
                <p>
A única validação adicional é feita à volta do subconjunto de tarefas no QL1, que são diferentes do subconjunto de tarefas no QL2. Isto assegura que não há sobreposições. Isto é feito pelo sistema quando as tarefas são associadas.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
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
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Todas as tarefas do projeto ou em branco </p>
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
            <td width="54" valign="top">
                <p>
Válido </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Baseado na Regra n.º 5, Q1 e Q2 são duas propostas na mesma oportunidade, pelo que ambos podem estimar para os mesmos componentes de um projeto.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T2 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Todas as tarefas do projeto ou em branco </p>
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
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Todas as tarefas do projeto ou em branco </p>
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
            <td width="54" valign="top">
                <p>
Válido </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Baseado na Regra n.º 4, Q1 e Q2 são duas propostas em oportunidades diferentes, pelo que ambos podem estimar para os mesmos componentes do mesmo projeto.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O2 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Todas as tarefas do projeto ou em branco </p>
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
            <td width="54" valign="top">
                <p>
Não é Válido </p>
            </td>
        </tr>
    </tbody>
</table>

