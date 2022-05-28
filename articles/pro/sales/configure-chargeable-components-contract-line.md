---
title: Configurar componentes faturáveis de um item de contrato baseado em projetos
description: Este tópico fornece informações sobre como adicionar componentes faturáveis a itens de contrato no Project Operations.
author: rumant
ms.date: 10/08/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c02228c5b75afdc825ffbf0ada9ca57001a173ac
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593212"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a>Configurar componentes faturáveis de um item de contrato baseado em projetos

_**Aplica-se a:** Implementação leve - negociar à faturação pró-forma, Project Operations para cenários baseados em recursos/não armazenados_

Um item de contrato baseado em projeto tem componentes *incluídos* e componentes *faturáveis*.

Os componentes incluídos são componentes que estão sujeitos a:

  - Método de faturação e divisões de clientes
  - Limites a não exceder 
  - Definições de frequência de fatura definidas no item de contrato baseado em projeto

Um subconjunto dos componentes incluídos pode ser marcado como faturável utilizando o campo **Tipo de Faturação**. O campo **Tipo de Faturação** é um conjunto de opções que permite os seguintes valores no contexto de um item de contrato:

  - Faturável
  - Não faturável

Os componentes faturáveis podem ser definidos nas categorias de tarefas, funções e transações.

A capacidade de faturação é definida em tarefas para um item de contrato de projeto e aplica-se a todas as classes de transação incluídas no item. Se o campo **Incluir Tarefas** num item de contrato estiver em branco ou definido para **Todo o projeto**, o separador **Tarefas faturáveis** não estará disponível.

A capacidade de faturação definida nas funções de um item de contrato de projeto aplica-se apenas à classe de transação **Tempo**. Se o campo **Incluir Tempo** num item de contrato estiver definido para **Não**, o separador **Funções faturáveis** não estará disponível.

A capacidade de faturação definida nas categorias de transação de um item de contrato de projeto aplica-se apenas à classe de transação **Despesa**. Se o campo **Incluir Despesas** estiver definido para **Não**, o separador **Categorias faturáveis** não estará disponível.

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a>Atualizar uma tarefa de projeto como faturável ou não faturável

Uma tarefa do projeto pode ser faturável ou não faturável num item de contrato específico, que torna possível a seguinte configuração:

Se um item de contrato baseado em projeto incluir **Tempo** e uma determinada tarefa, **T1** é associado a ela como faturável. Se houver um segundo item de contrato que inclua **Despesas**, pode associar a tarefa T1 ao item de contrato como não faturável. O resultado é que todo o tempo registado na tarefa é faturado e todas as despesas são não faturáveis.

O tipo de faturação de uma tarefa pode ser configurado no separador **Tarefas Faturáveis** de um item de contrato, atualizando o campo **Tipo de Faturação** na subgrelha de tarefas do item de contrato. Em alternativa, pode atualizar o campo **Tipo de Faturação** na subgrelha da configuração de Faturação da tarefa de itens de contrato associados a uma tarefa.

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a>Atualizar uma função de projeto como faturável ou não faturável

Uma função pode ser faturável ou não faturável num item de contrato específico.

O tipo de faturação de uma função pode ser configurado no separador **Funções faturáveis** de um item de contrato. Para isso, atualize o campo **Tipo de Faturação** na subgrelha **Funções Faturáveis**.

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a>Atualizar uma categoria de transação como faturável ou não faturável

Uma categoria de transação pode ser faturável ou não faturável num item de contrato específico.

O tipo de faturação de uma transação pode ser configurado no separador **Categorias faturáveis** de um item de contrato baseado em projeto. Para isso, atualize o campo **Tipo de Faturação** na subgrelha **Categorias Faturáveis**.

### <a name="resolve-chargeability"></a>Resolver a capacidade de faturação

Uma estimativa ou um valor real criado para o tempo só é considerado faturável se:

   - **Tempo** está incluído na linha do contrato.
   - **Função** é configurado como responsável no item de contrato.
   - **Tarefas incluídas** estão definidas para **Tarefas selecionadas** no item de contrato.
 
 Se estas três coisas forem verdadeiras, a tarefa é configurada como faturável. 

Uma estimativa ou um valor real criado para a despesa só é considerado faturável se:

   - **Despesa** está incluído no item de contrato
   - **Categoria de transação** é configurado como faturável no item de contrato
   - **Tarefas incluídas** estão definidas para **Tarefa selecionadas** no item de contrato
  
 Se estas três coisas forem verdadeiras, a **Tarefa** é configurada como faturável. 

Uma estimativa ou um valor real criado para o material só é considerado faturável se:

   - **Materiais** está incluído no item de contrato
   - **Tarefas incluídas** estão definidas para **Tarefas selecionadas** no item de contrato

Se estas duas coisas forem verdadeiras, a **Tarefa** é configurada como faturável. 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>Inclui Tempo</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>Inclui Despesa</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>Incluir materiais</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
                    <strong>Tarefas Incluídas</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Função</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Categoria</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Tarefa</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
                    <strong>Impacto da possível faturação</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Sim </p>
            </td>
            <td width="78" valign="top">
                <p>
Sim </p>
            </td>
            <td width="63" valign="top">
                <p>
Sim </p>
            </td>
            <td width="75" valign="top">
                <p>
Todo o Projeto </p>
            </td>
            <td width="65" valign="top">
                <p>
Faturável </p>
            </td>
            <td width="70" valign="top">
                <p>
Faturável </p>
            </td>
            <td width="65" valign="top">
                <p>
Não pode ser definido </p>
            </td>
            <td width="350" valign="top">
                <p>
Faturação num valor real de tempo: <strong>Faturável</strong>
                </p>
                <p>
Tipo de faturação em valor real de despesas: <strong>Faturável</strong>
                </p>
                <p>
Tipo de faturação em valor real de material: <strong>Faturável</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Sim </p>
            </td>
            <td width="78" valign="top">
                <p>
Sim </p>
            </td>
            <td width="63" valign="top">
                <p>
Sim </p>
            </td>
            <td width="75" valign="top">
                <p>
Apenas tarefas selecionadas </p>
            </td>
            <td width="65" valign="top">
                <p>
Faturável </p>
            </td>
            <td width="70" valign="top">
                <p>
Faturável </p>
            </td>
            <td width="65" valign="top">
                <p>
Faturável </p>
            </td>
            <td width="350" valign="top">
                <p>
Faturação num valor real de tempo: <strong>Faturável</strong>
                </p>
                <p>
Tipo de faturação em valor real de despesas: <strong>Faturável</strong>
                </p>
                <p>
Tipo de faturação em valor real de material: <strong>Faturável</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Sim </p>
            </td>
            <td width="78" valign="top">
                <p>
Sim </p>
            </td>
            <td width="63" valign="top">
                <p>
Sim </p>
            </td>
            <td width="75" valign="top">
                <p>
Apenas tarefas selecionadas </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Não faturável</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Faturável </p>
            </td>
            <td width="65" valign="top">
                <p>
Faturável </p>
            </td>
            <td width="350" valign="top">
                <p>
Faturação num valor real de tempo: <strong>Não faturável</strong>
                </p>
                <p>
Tipo de faturação em valor real de despesas: Faturável </p>
                <p>
Tipo de faturação em valor real de material: Faturável </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Sim </p>
            </td>
            <td width="78" valign="top">
                <p>
Sim </p>
            </td>
            <td width="63" valign="top">
                <p>
Sim </p>
            </td>
            <td width="75" valign="top">
                <p>
Apenas tarefas selecionadas </p>
            </td>
            <td width="65" valign="top">
                <p>
Faturável </p>
            </td>
            <td width="70" valign="top">
                <p>
Faturável </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Não faturável</strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
Faturação num valor real de tempo: <strong>Não faturável</strong>
                </p>
                <p>
Tipo de faturação em valor real de despesas: <strong>Não faturável</strong>
                </p>
                <p>
Tipo de faturação em valor real de material: <strong>Não faturável</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Sim </p>
            </td>
            <td width="78" valign="top">
                <p>
Sim </p>
            </td>
            <td width="63" valign="top">
                <p>
Sim </p>
            </td>
            <td width="75" valign="top">
                <p>
Apenas tarefas selecionadas </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Não faturável</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Faturável </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Não faturável</strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
Faturação num valor real de tempo: <strong>Não faturável</strong>
                </p>
                <p>
Tipo de faturação em valor real de despesas: <strong>Não faturável</strong>
                </p>
                <p>
Tipo de faturação em valor real de material: <strong> Não faturável</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Sim </p>
            </td>
            <td width="78" valign="top">
                <p>
Sim </p>
            </td>
            <td width="63" valign="top">
                <p>
Sim </p>
            </td>
            <td width="75" valign="top">
                <p>
Apenas tarefas selecionadas </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Não faturável</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Não faturável</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Faturável </p>
            </td>
            <td width="350" valign="top">
                <p>
Faturação num valor real de tempo: <strong>Não faturável</strong>
                </p>
                <p>
Tipo de faturação em valor real de despesas: <strong> Não faturável</strong>
                </p>
                <p>
Tipo de faturação em valor real de material: Faturável </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
Sim </p>
            </td>
            <td width="63" valign="top">
                <p>
Sim </p>
            </td>
            <td width="75" valign="top">
                <p>
Todo o Projeto </p>
            </td>
            <td width="65" valign="top">
                <p>
Não pode ser definido </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Faturável</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Não pode ser definido </p>
            </td>
            <td width="350" valign="top">
                <p>
Faturação num valor real de tempo: <strong>Não disponível</strong>
                </p>
                <p>
Tipo de faturação em valor real de despesas: Faturável </p>
                <p>
Tipo de faturação em valor real de material: Faturável </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
Sim </p>
            </td>
            <td width="63" valign="top">
                <p>
Sim </p>
            </td>
            <td width="75" valign="top">
                <p>
Todo o Projeto </p>
            </td>
            <td width="65" valign="top">
                <p>
Não pode ser definido </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Não faturável</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Não pode ser definido </p>
            </td>
            <td width="350" valign="top">
                <p>
Faturação num valor real de tempo: <strong>Não disponível</strong>
                </p>
                <p>
Tipo de faturação em valor real de despesas: <strong> Não faturável</strong>
                </p>
                <p>
Tipo de faturação em valor real de material: Faturável </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Sim </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
Sim </p>
            </td>
            <td width="75" valign="top">
                <p>
Todo o Projeto </p>
            </td>
            <td width="65" valign="top">
                <p>
Faturável </p>
            </td>
            <td width="70" valign="top">
                <p>
Não pode ser definido </p>
            </td>
            <td width="65" valign="top">
                <p>
Não pode ser definido </p>
            </td>
            <td width="350" valign="top">
                <p>
Faturação num valor real de tempo: Faturável </p>
                <p>
Tipo de faturação em valor real de despesas:<strong> Não disponível</strong>
                </p>
                <p>
Tipo de faturação em valor real de material: Faturável </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Sim </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
Sim </p>
            </td>
            <td width="75" valign="top">
                <p>
Todo o Projeto </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Não faturável</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Não pode ser definido </p>
            </td>
            <td width="65" valign="top">
                <p>
Não pode ser definido </p>
            </td>
            <td width="350" valign="top">
                <p>
Faturação num valor real de tempo: <strong>Não faturável </strong>
                </p>
                <p>
Tipo de faturação em valor real de despesas:<strong> Não disponível</strong>
                </p>
                <p>
Tipo de faturação em valor real de material: Faturável </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Sim </p>
            </td>
            <td width="78" valign="top">
                <p>
Sim </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
Todo o Projeto </p>
            </td>
            <td width="65" valign="top">
                <p>
Faturável </p>
            </td>
            <td width="70" valign="top">
                <p>
Faturável </p>
            </td>
            <td width="65" valign="top">
                <p>
Não pode ser definido </p>
            </td>
            <td width="350" valign="top">
                <p>
Faturação num valor real de tempo: Faturável </p>
                <p>
Tipo de faturação em valor real de despesas: Faturável </p>
                <p>
Tipo de faturação em valor real de material: <strong> Não disponível</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Sim </p>
            </td>
            <td width="78" valign="top">
                <p>
Sim </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
Todo o Projeto </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Não faturável</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Não faturável</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Não pode ser definido </p>
            </td>
            <td width="350" valign="top">
                <p>
Faturação num valor real de tempo: <strong>Não faturável </strong>
                </p>
                <p>
Tipo de faturação em valor real de despesas:<strong> Não faturável </strong>
                </p>
                <p>
Tipo de faturação em valor real de material:<strong> Não disponível</strong>
                </p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
