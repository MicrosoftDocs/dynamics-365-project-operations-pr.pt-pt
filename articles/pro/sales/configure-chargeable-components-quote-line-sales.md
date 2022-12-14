---
title: Configurar os componentes faturáveis em linhas de proposta do projeto
description: Este artigo fornece informações sobre a configuração de componentes faturáveis e não faturáveis numa linha de proposta baseada em projetos.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 1e454278a1c5c24ac346c537c778b25448d9ea03
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825532"
---
# <a name="configure-chargeable-components-on-project-quote-lines"></a>Configurar os componentes faturáveis em linhas de proposta do projeto

_**Aplica-se a:** Implementação leve - negociar à faturação pró-forma, Project Operations para cenários baseados em recursos/não armazenados_

Uma linha de proposta baseada em projeto tem o conceito de componentes *incluídos* e componentes *faturáveis*.

Os componentes incluídos estão sujeitos a:

  - Método de faturação e divisões de clientes
  - Limites a não exceder 
  - Definições de frequência de fatura definidas na linha de proposta baseada em projeto

Um subconjunto dos componentes incluídos pode ser marcado como faturável utilizando o campo **Tipo de Faturação**. O campo **Tipo de Faturação** é um conjunto de opções que permite os seguintes valores no contexto de uma linha de proposta:

  - Faturável
  - Não faturável

Os componentes faturáveis podem ser definidos nas categorias de tarefas, funções e transações.

A capacidade de faturação é definida nas tarefas para uma linha de proposta e aplica-se a todas as classes de transação incluídas na linha. Se o campo **Incluir Tarefas** for definido para **Todo o projeto** ou for deixado em branco, o separador **Tarefas Faturáveis** não está disponível.

A capacidade de faturação é definida nas funções de uma linha de proposta e aplica-se apenas à classe de transação **Tempo**. Se o campo **Incluir Tempo** estiver definido para **Não** numa linha de proposta, o separador **Funções Faturáveis** não está disponível.

A capacidade de faturação é definida nas categorias de transação de uma linha de proposta e aplica-se apenas à classe de transação **Despesa**. Se o campo **Incluir Despesas** estiver definido para **Não** numa linha de proposta, o separador **Categorias Faturáveis** não está disponível.

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a>Atualizar uma tarefa de projeto para faturável ou não faturável

Uma tarefa do projeto pode ser faturável ou não faturável no contexto de uma linha de proposta baseada em projeto específica que torna possível a seguinte configuração.

Se uma linha de proposta baseada em projeto inclui **Tempo** e a tarefa **T1**, a tarefa está associada à linha de proposta como faturável. Se houver uma segunda linha de proposta que inclua **Despesas**, pode associar a tarefa **T1** à linha de proposta como não faturável. O resultado é que todo o tempo registado na tarefa é faturado e todas as despesas registadas na tarefa são não faturáveis.

O tipo de faturação de uma tarefa pode ser configurado no separador **Tarefas Faturáveis** de uma linha de proposta baseada em projeto, atualizando o campo **Tipo de Faturação** na subgrelha **Tarefas da linha de Proposta**. Em alternativa, pode atualizar o tipo de faturação para uma tarefa de projeto no campo **Tipo de Faturação** na subgrelha na configuração de faturação da tarefa de um projeto que mostra as linhas de proposta associadas a uma tarefa.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Atualizar uma função de projeto como faturável ou não faturável

Uma função pode ser faturável ou não faturável no contexto de uma linha de proposta específica baseada em projetos.

O tipo de faturação de uma função pode ser configurado no separador **Funções Faturáveis** de uma linha de proposta baseada em projeto, atualizando o campo **Tipo de Faturação** na subgrelha **Funções Faturáveis**.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Atualizar uma categoria de transação como faturável ou não faturável

Uma categoria de transação pode ser faturável ou não faturável numa linha de proposta específica.

O tipo de faturação de uma transação pode ser configurado no separador **Categorias Faturáveis** de uma linha de proposta baseada em projeto, atualizando o campo **Tipo de Faturação** na subgrelha **Categorias Faturáveis**.

### <a name="resolve-chargeability"></a>Resolver a capacidade de faturação
Uma estimativa ou um valor real criado para o tempo só será considerado faturável se:

   - **Tempo** está incluído na linha da proposta.
   - **Função** é configurado como responsável na linha de proposta.
   - **Tarefas incluídas** estão definidas para **Tarefas selecionadas** na linha de proposta. 

Se estas três coisas forem verdadeiras, a **Tarefa** é também configurada como faturável. 

Uma estimativa ou um valor real criado para a despesa só é considerado faturável se: 

   - **Despesa** está incluído na linha da proposta.
   - **Categoria de transação** é configurado como faturável na linha de proposta.
   - **Tarefas incluídas** estão definidas para **Tarefas selecionadas** na linha de proposta.

Se estas três coisas forem verdadeiras, a **Tarefa** é também configurada como faturável. 

Uma estimativa ou um valor real criado para o material só será considerado faturável se:

   - **Materiais** está incluído na linha da proposta.
   - **Tarefas incluídas** estão definidas para **Tarefas selecionadas** na linha de proposta.

Se estas duas coisas forem verdadeiras, a **Tarefa** também deveria ser configurada como faturável. 


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
Faturação num valor real de tempo: Faturável </p>
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
Faturável </p>
            </td>
            <td width="350" valign="top">
                <p>
Faturação num valor real de tempo: Faturável </p>
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
