---
title: Estimativas
description: Este tópico fornece informações sobre estimativas no Dynamics 365 Project Service Automation.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 1/31/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: fcb3c85af092667cc5a473ab4674c3be47e33327
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6007605"
---
# <a name="estimates"></a>Estimativas

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Numa proposta baseada em projetos, pode utilizar a entidade Detalhe de linha de proposta para estimar o trabalho que é necessário para entregar um projeto. Em seguida, pode partilhar essa estimativa com o cliente.

As linhas de proposta baseadas em projetos não têm de ter detalhes de linha de proposta. Em alternativa, podem ter muitos detalhes de linha de proposta. Os detalhes de linha de proposta são utilizados para estimar o tempo, as despesas ou as taxas. O PSA não permite estimativas de material em detalhes de linha de proposta. Estes são chamados de classes de transação. Os montantes de imposto estimados também podem ser introduzidos numa classe de transação.

Para além das classes de transação, os detalhes de linha de proposta têm um tipo de transação. O PSA suporta dois tipos de transação para obter detalhes de linha de proposta: **Custo** e **Contrato do Projeto**.

## <a name="estimate-by-using-a-contract"></a>Estimar utilizando um contrato

Se tiver utilizado uma proposta de PSA quando criou um contrato baseado em projetos, a estimativa que fez para cada linha de proposta na proposta é copiada para o contrato do projeto. A estrutura de um contrato do projeto é semelhante à estrutura da proposta do projeto que tem linhas, detalhes de linha e agendas de faturação.

As estimativas podem ser efetuadas diretamente num contrato do projeto, como numa proposta do projeto. Para obter uma proposta do projeto, a estimativa é efetuada através da utilização de itens de contrato e detalhes de item de contrato. Os detalhes de item de contrato também podem ser gerados a partir de um plano do projeto criado com a abordagem de estimativa de baixo para cima.

Os detalhes de item de contrato podem ser utilizados para estimar o tempo, as despesas ou as taxas. Os montantes de imposto estimados também podem ser introduzidos num detalhe de item de contrato.

O PSA não permite estimativas de material em detalhes de item de contrato.

Os processos suportados num contrato do projeto são a criação e confirmação de faturas. A criação de faturas cria um rascunho de uma fatura baseada em projetos que inclui todos os valores reais de vendas não faturadas até à data atual.

A confirmação faz com que o contrato seja só de leitura e altera o estado de **Rascunho** para **Confirmado**. Depois de executar esta ação, não é possível anulá-la. Uma vez que esta ação é permanente, é recomendável manter o contrato num estado de **Rascunho**.

A única diferença entre contratos de rascunho e contratos confirmados é o respetivo Estado e o facto de os contratos de rascunho poderem ser editados, ao passo que os contratos confirmados não podem. A criação de faturas e a monitorização de valores reais podem ser efetuadas em contratos de rascunho e em contratos confirmados.

O PSA não suporta ordens de alteração em contratos ou projetos.

## <a name="estimating-projects"></a>Estimar projetos

Pode estimar o tempo e as despesas dos projetos. O PSA não permite estimativas de materiais ou taxas em projetos.

As estimativas de tempo são geradas quando cria uma tarefa e identifica os atributos de um recurso genérico que é necessário para efetuar a tarefa. As estimativas de tempo são geradas a partir de tarefas de agendamento. As estimativas de tempo não são criadas se criar membros da equipa genéricos fora do contexto da agenda.

As estimativas de despesas são introduzidas na grelha da página **Estimativas**.

## <a name="understanding-estimation"></a>Compreender as estimativas

Utilize a tabela seguinte como um guia para compreender a lógica de negócio na fase de estimativa.

| Cenário                                                                                                                                                                                                                                                                                                                                          | Registo de entidade                                                                                                                                                                                                       | Tipo de Transação | Classe de Transação | Informações adicionais                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|-------------|-----------------------------------------------------------------------------------|
| Quando necessita de estimar o valor de vendas do tempo numa proposta                                                                                                                                                                                                                                                                                    | O registo do detalhe de linha de proposta (QLD) é criado                                                                                                                                                                               | Contrato do projeto | Time        | O campo Origem da transação na linha QLD do lado das vendas faz referência ao QLD do lado do custo |
|                                                                                                                                                                                                                                                                                     | Um segundo registo QLD é criado pelo sistema para armazenar os valores de custo correspondentes. Todos os campos não monetários são copiados do QLD de vendas para o QLD de custo pelo sistema.                                                                                                                                                                               | Custo | Time        | O campo Origem da transação na linha de detalhe de linha de proposta (QLD) do lado das vendas faz referência ao QLD do lado do custo |
| Quando necessita de estimar o valor de vendas do tempo num contrato                                                                                                                                                                                                                                                                                 | O registo do detalhe de item de contrato (CLD) do projeto é criado                                                                                                                                                                    | Contrato do Projeto | Time        | O campo Origem da transação na linha CLD do lado das vendas faz referência ao CLD do custo      |
|                                                                                                                                                                                                                                                                                  | Um segundo registo CLD é criado pelo sistema para armazenar os valores de custo correspondentes. Todos os campos não monetários são copiados do CLD de vendas para o CLD de custo pelo sistema.                                                                                                                                                                    | Custo | Time        | O campo Origem da transação na linha CLD do lado das vendas faz referência ao CLD do custo      |
| Quando o utilizador descreve um recurso numa tarefa do projeto                                                                                                                                                                                                                                                                                            | O registo da linha de estimativa para mostrar o valor de venda da tarefa é criado quando uma tarefa é criada com todas as dimensões de definição de preços necessárias. As unidades organizacionais e a função são as dimensões de definição de preços do Project Service OOB | Contrato do Projeto | Time        |                                                                                   |
|     | O registo da linha de estimativa para mostrar o valor de custo da tarefa é criado quando uma tarefa é criada com todas as dimensões de definição de preços necessárias. Todos os campos não monetários são copiados da linha de estimativa de vendas para a linha de estimativa de custo pelo sistema. A função e a unidade organizacional são as dimensões de definição de preços do PSA OOB para as taxas de faturação e o custo.                                                                                                                                                                                                                | Custo             | Time           |                                                                                   |



## <a name="customizing-the-quote-line-detail-and-contract-line-detail-entities"></a>Personalizar as entidades de Detalhe de linha de proposta e Detalhe de item de contrato

Se tiver adicionado um campo personalizado aos detalhes de linha de proposta e pretender que o sistema introduza o valor do campo como um valor predefinido na linha de custo relacionada que cria, utilize as ferramentas de registo de plug-in PreOperationContractLineDetailUpdate e PreOperationQuoteLineDetailUpdate. Estes plug-ins têm de ser registados após o detalhe de linha de proposta ou o detalhe de item de contrato ser alterado. Siga estes passos para concluir o processo.

1. Abra o PluginRegistrationTool e ligue-se à sua instância online.
2. Selecione **Procurar** e procure o plug-in para atualizar.

    ![Caixa de diálogo Árvore de Pesquisa](media/basic-guide-19.png)

3. Selecione o plug-in e, em seguida, na página principal, selecione **Selecionar**.
4. Selecione o passo do plug-in a atualizar, clique com o botão direito do rato e, em seguida, selecione **Atualizar**.

    ![Selecionar um passo no plug-in](media/basic-guide-20.png)

5. Na caixa de diálogo **Atualizar Passo Existente**, no campo **Atributos de Filtragem**, selecione o botão de reticências (**...**):
 
    ![Caixa de diálogo Atualizar Passo Existente](media/basic-guide-21.png)

6. Na caixa de diálogo **Selecionar Atributos**, selecione as caixas de verificação para obter os atributos personalizados.

    ![Caixa de diálogo Selecionar Atributos](media/basic-guide-22.png)

7. Selecione **OK** para fechar a caixa de diálogo e, em seguida, selecione **Atualizar Passo**.
 
    ![Botão Atualizar Passo](media/basic-guide-23.png)

8. Repita os passos 1 a 7 para o segundo plug-in.
9. Feche o PluginRegistrationTool.


[!INCLUDE[footer-include](../includes/footer-banner.md)]