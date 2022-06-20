---
title: Descrição geral das linhas de proposta baseadas em projetos
description: Este artigo fornece informações sobre a utilização de linhas de proposta baseadas em projetos para trabalho do projeto.
author: rumant
ms.date: 03/30/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 90c5affa25b113476e43f0bbbadd5c9615f9c05c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8934472"
---
# <a name="project-based-quote-lines-overview"></a>Descrição geral das linhas de proposta baseadas em projetos 

_**Aplica-se a:** Implementação leve - negociar à faturação pró-forma, Project Operations para cenários baseados em recursos/não armazenados_

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
| Nome | O nome da linha de proposta que o ajuda a identificar o componente discreto da proposta que está a ser estimada. | Copiada para o item de contrato do projeto que é criada a partir desta linha de proposta quando a proposta é ganha. |
| Método de Faturação | Numa proposta criada a partir de uma oportunidade, este valor é copiado a partir do campo correspondente na linha de oportunidade. Este campo inclui os dois principais modelos de contratação suportados por Dynamics 365 Project Operations:</br>- Preço fixo</br>- Tempo e material.| Este valor é copiado para o item de contrato de projeto que é criado a partir desta linha de proposta quando a proposta é ganha. |
| Project | Utilize este campo opcional para identificar o projeto que será utilizado para entregar o trabalho nesta cativação. Quando um projeto é mapeado para uma linha de proposta, ajuda a configurar as tarefas faturáveis e também a trazer uma estimativa baseada em projetos para a linha de proposta como detalhes da linha de proposta. Quando um projeto não é mapeado para uma linha de proposta baseada em projetos, a estimativa deve ser criada manualmente ao criar cada detalhe da linha de proposta. | Este valor é copiado para o item de contrato de projeto que é criado a partir desta linha de proposta quando a proposta é ganha.|
| Tarefas Incluídas | Indica se esta linha de proposta é utilizada para todas ou algumas tarefas do projeto para o projeto selecionado. Este campo tem os seguintes valores possíveis:</br>- Todas as tarefas do projeto</br>- Apenas tarefas selecionadas do projeto</br>Um valor em branco neste campo é equivalente à opção **Todas as tarefas do projeto**. | Quando **Apenas tarefas de projeto selecionadas** é selecionado na página do projeto, o separador de **configuração de faturação de tarefas** permite-lhe selecionar tarefas específicas para as associar a esta linha de proposta. Este valor é copiado para o item de contrato de projeto que é criado a partir desta linha de proposta quando a proposta é ganha. |
| Incluir Tempo | Um valor **Sim**/**Não** indica se as transações de tempo ou os custos de mão de obra no projeto selecionado serão incluídos na estimativa desta linha de proposta. Um valor **Não** indica que as transações de tempo ou o custo de mão de obra não será incluído na estimativa nesta linha de proposta. Um valor **Sim** indica que as transações de tempo ou o custo de mão de obra será incluído na estimativa nesta linha de proposta. | Este valor é copiado para o item de contrato de projeto que é criado a partir desta linha de proposta quando a proposta é ganha. |
| Incluir Despesa | Um valor **Sim**/**Não** indica se os custos de despesa no projeto selecionado serão incluídos na estimativa desta linha de proposta. Um valor **Não** indica que o custo de despesa não será incluído na estimativa nesta linha de proposta. Um valor **Sim** indica que o custo de despesa será incluído na estimativa nesta linha de proposta. | Este valor é copiado para o item de contrato de projeto que é criado a partir desta linha de proposta quando a proposta é ganha. |
| Incluir Material | Um valor **Sim**/**Não** indica se os custos de material no projeto selecionado serão incluídos na estimativa desta linha de proposta. Um valor **Não** indica que custos de material não serão incluídos na estimativa desta linha de proposta. Um valor **Sim** indica que custos de material serão incluídos na estimativa desta linha de proposta. | Este valor é copiado para o item de contrato de projeto que é criado a partir desta linha de proposta quando a proposta é ganha. |
| Incluir Taxa | Um valor **Sim**/**Não** indica se as taxas no projeto selecionado serão incluídas na estimativa desta linha de proposta. Um valor **Não** indica que as taxas não serão incluídas na estimativa nesta linha de proposta. Um valor **Sim** indica que as taxas serão incluídas na estimativa nesta linha de proposta. | Este valor é copiado para o item de contrato de Projeto que é criado a partir desta linha de proposta quando a proposta é ganha. |
| Montante da Proposta | Este é o montante que será proposto ao cliente por todo o trabalho previsto nesta linha de proposta baseada em projetos. Numa proposta criada a partir de uma oportunidade, este valor é copiado a partir do campo **Orçamento do Cliente** na linha de oportunidade. Quando a linha de proposta baseada em projetos tem detalhes da linha, este campo é bloqueado para edição e é resumido a partir do montante nos detalhes da linha de proposta. | Este valor é copiado para o item de contrato de projeto que é criado a partir desta linha de proposta quando a proposta é ganha. |
| Imposto Estimado | Este é um campo editável para o utilizador adicionar o montante do imposto estimado na linha de proposta. Quando uma linha de proposta baseada em projetos tem detalhes da linha, este campo é bloqueado para edição e é resumido a partir do montante do imposto nos detalhes da linha de proposta. | Este valor é copiado para o item de contrato de projeto que é criado a partir desta linha de proposta quando a proposta é ganha. |
| Montante da Proposta Após o Imposto | Este campo é o montante da linha de proposta após impostos e é só de leitura. O montante neste campo é calculado como *Montante da Proposta + Imposto*. | Este valor é copiado para o item de contrato de projeto que é criado a partir desta linha de proposta quando a proposta é ganha. |
| Limite a não exceder | Este campo é editável e só está disponível em linhas de proposta baseadas em projetos que têm um método de faturação **Tempo e Material**. | Este valor é copiado para o item de contrato de projeto que é criado a partir desta linha de proposta quando a proposta é ganha. |
| Orçamento do Cliente | Este campo é editável e é copiado a partir do campo correspondente na linha de oportunidade se a proposta tiver sido criada a partir de uma oportunidade. | Este valor é copiado para o item de contrato de projeto que é criado a partir desta linha de proposta quando a proposta é ganha. |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a>Regras de validação para os campos no separador Geral das linhas de proposta baseadas em projetos

**Regra 1**: se o campo **Tarefas Incluídas** estiver em branco ou se estiver definido como **Todas as tarefas do projeto**, é incluído um projeto na linha de proposta.

**Regra 2**: se o campo **Tarefas Incluídas** estiver em branco, ou se estiver definido como **Todas as tarefas do projeto**, um projeto e uma determinada classe de transações só podem ser incluídos numa linha de proposta baseada em projetos de uma proposta.

**Regra 3**: se o campo **Tarefas Incluídas** estiver definido como **Apenas tarefas selecionadas do projeto**, um projeto e uma determinada classe de transações só podem ser incluídos em várias linhas de proposta baseadas em projetos de uma proposta.

**Regra 4**: se uma oportunidade tiver várias proposta, poderá haver linhas de proposta de diferentes propostas em que todas referenciam o mesmo projeto e incluem a mesma classe de transações.

**Regra 5**: se as propostas não pertencerem à mesma oportunidade, não poderão incluir o mesmo projeto e classe de transações.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p>
                    <strong>Oportunidade</strong>
                </p>
            </td>
            <td width="39" valign="top">
                <p>
                    <strong>Proposta</strong>
                </p>
            </td>
            <td width="40" valign="top">
                <p>
                    <strong>Linha de proposta</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="77" valign="top">
                <p>
                    <strong>Tarefas incluídas</strong>
                </p>
            </td>
            <td width="45" valign="top">
                <p>
                    <strong>Incluir Tempo</strong>
                </p>
            </td>
            <td width="46" valign="top">
                <p>
                    <strong>Incluir Despesa</strong>
                </p>
            </td>
            <td width="43" valign="top">
                <p>
                    <strong>Incluir Material</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Incluir</strong>
                </p>
                <p>
                    <strong>Taxa</strong>
                </p>
            </td>
            <td width="49" valign="top">
                <p>
                    <strong>Válido/Não válido</strong>
                </p>
            </td>
            <td width="200" valign="top">
                <p>
                    <strong>Razão</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Em branco </p>
            </td>
            <td width="45" valign="top">
                <p>
Sim </p>
            </td>
            <td width="46" valign="top">
                <p>
Sim </p>
            </td>
            <td width="43" valign="top">
                <p>
Sim </p>
            </td>
            <td width="41" valign="top">
                <p>
Sim </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Não é válido </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Violação da Regra n.º 2. O Tempo, a Despesa e as Taxas no projeto P1 estão incluídos nas linhas de proposta, QL1 e QL2 </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Em branco </p>
            </td>
            <td width="45" valign="top">
                <p>
Sim </p>
            </td>
            <td width="46" valign="top">
                <p>
Sim </p>
            </td>
            <td width="43" valign="top">
                <p>
Sim </p>
            </td>
            <td width="41" valign="top">
                <p>
Sim </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Em branco </p>
            </td>
            <td width="45" valign="top">
                <p>
Sim </p>
            </td>
            <td width="46" valign="top">
                <p>
No </p>
            </td>
            <td width="43" valign="top">
                <p>
Sim </p>
            </td>
            <td width="41" valign="top">
                <p>
Sim </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Não é válido </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Violação da Regra n.º 2. O Tempo, o Material e as Taxas no projeto P1 estão incluídos nas linhas de proposta, QL1 e QL2 </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Em branco </p>
            </td>
            <td width="45" valign="top">
                <p>
Sim </p>
            </td>
            <td width="46" valign="top">
                <p>
Sim </p>
            </td>
            <td width="43" valign="top">
                <p>
Sim </p>
            </td>
            <td width="41" valign="top">
                <p>
Sim </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Em branco </p>
            </td>
            <td width="45" valign="top">
                <p>
Sim </p>
            </td>
            <td width="46" valign="top">
                <p>
No </p>
            </td>
            <td width="43" valign="top">
                <p>
Sim </p>
            </td>
            <td width="41" valign="top">
                <p>
Sim </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Válido </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
O tempo, material e as taxas no projeto P1 estão incluídos no QL1 <br>
As Despesas no projeto P1 estão incluídas no QL2 <br>
Não há sobreposição no que está a ser incluído em cada linha de proposta e é, portanto, válido.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Em branco </p>
            </td>
            <td width="45" valign="top">
                <p>
No </p>
            </td>
            <td width="46" valign="top">
                <p>
Sim </p>
            </td>
            <td width="43" valign="top">
                <p>
No </p>
            </td>
            <td width="41" valign="top">
                <p>
No </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Apenas tarefas selecionadas </p>
            </td>
            <td width="45" valign="top">
                <p>
Sim </p>
            </td>
            <td width="46" valign="top">
                <p>
Sim </p>
            </td>
            <td width="43" valign="top">
                <p>
Sim </p>
            </td>
            <td width="41" valign="top">
                <p>
Sim </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Não é válido </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Violação da Regra #2 </p>
                <p>
O Q1 inclui tempo, material, despesas e taxas num subconjunto de tarefas no projeto P1 </p>
                <p>
O QL2 inclui tempo, despesas e taxas para todo o projeto P1 e, portanto, sobrepõe-se ao que está incluído no Q1.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Em branco </p>
            </td>
            <td width="45" valign="top">
                <p>
Sim </p>
            </td>
            <td width="46" valign="top">
                <p>
Sim </p>
            </td>
            <td width="43" valign="top">
                <p>
Sim </p>
            </td>
            <td width="41" valign="top">
                <p>
Sim </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Apenas tarefas selecionadas </p>
            </td>
            <td width="45" valign="top">
                <p>
Sim </p>
            </td>
            <td width="46" valign="top">
                <p>
Sim </p>
            </td>
            <td width="43" valign="top">
                <p>
Sim </p>
            </td>
            <td width="41" valign="top">
                <p>
Sim </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Válido </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Pela Regra n.º 3, </p>
                <p>
O Q1 inclui tempo, material, despesas e taxas num subconjunto de tarefas no projeto P1.
                </p>
                <p>
O QL2 inclui tempo, materiais, despesas e taxas para um subconjunto de tarefas no projeto P1.
                </p>
                <p>
A única validação adicional está em redor do subconjunto de tarefas no QL1 que é diferente do subconjunto de tarefas no QL2 para garantir que não há sobreposição. Isto é feito pelo sistema quando as tarefas são associadas.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Apenas tarefas selecionadas </p>
            </td>
            <td width="45" valign="top">
                <p>
Sim </p>
            </td>
            <td width="46" valign="top">
                <p>
Sim </p>
            </td>
            <td width="43" valign="top">
                <p>
Sim </p>
            </td>
            <td width="41" valign="top">
                <p>
Sim </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Todas as tarefas do projeto ou em branco </p>
            </td>
            <td width="45" valign="top">
                <p>
Sim </p>
            </td>
            <td width="46" valign="top">
                <p>
Sim </p>
            </td>
            <td width="43" valign="top">
                <p>
Sim </p>
            </td>
            <td width="41" valign="top">
                <p>
Sim </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Válido </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
De acordo com as regras #5, Q1 e Q2 são duas propostas sobre a mesma oportunidade, para que ambas possam estimar para os mesmos componentes de um projeto.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T2 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Todas as tarefas do projeto ou em branco </p>
            </td>
            <td width="45" valign="top">
                <p>
Sim </p>
            </td>
            <td width="46" valign="top">
                <p>
Sim </p>
            </td>
            <td width="43" valign="top">
                <p>
Sim </p>
            </td>
            <td width="41" valign="top">
                <p>
Sim </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Todas as tarefas do projeto ou em branco </p>
            </td>
            <td width="45" valign="top">
                <p>
Sim </p>
            </td>
            <td width="46" valign="top">
                <p>
Sim </p>
            </td>
            <td width="43" valign="top">
                <p>
Sim </p>
            </td>
            <td width="41" valign="top">
                <p>
Sim </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Não é Válido </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
De acordo com as regras #4, Q1 e Q2 são duas propostas sobre oportunidades diferentes, para que não possam estimar para os mesmos componentes de um mesmo projeto.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O2 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Todas as tarefas do projeto ou em branco </p>
            </td>
            <td width="45" valign="top">
                <p>
Sim </p>
            </td>
            <td width="46" valign="top">
                <p>
Sim </p>
            </td>
            <td width="43" valign="top">
                <p>
Sim </p>
            </td>
            <td width="41" valign="top">
                <p>
Sim </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
