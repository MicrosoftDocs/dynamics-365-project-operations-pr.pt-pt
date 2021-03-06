---
title: Descrição geral da estimativa de projetos
description: Este tópico fornece informações sobre as estimativas no Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8e7ee4888a907b9d8c3ce06c1597f6b05be84477
ms.sourcegitcommit: 6eb26bab511ec09201ab70c3e2808dece3f74c4c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/07/2020
ms.locfileid: "3968057"
---
# <a name="estimate-projects-overview"></a>Descrição geral da estimativa de projetos

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

Numa proposta baseada em projetos, pode utilizar a entidade **Detalhe de linha de proposta** para estimar o trabalho que é necessário para entregar um projeto. Em seguida, pode partilhar essa estimativa com o cliente.

As linhas de proposta baseadas em projetos podem ter de zero a muitos detalhes de linha de proposta. Os detalhes de linha de proposta são utilizados para estimar o tempo, as despesas ou as taxas. O Microsoft Dynamics 365 Project Operations não permite estimativas de material em detalhes de linha de proposta. Estes são chamados de classes de transação. Os montantes de imposto estimados também podem ser introduzidos numa classe de transação.

Para além das classes de transação, os detalhes de linha de proposta têm um tipo de transação. Dois tipos de transação são suportados para os detalhes de linha de proposta: **Custo** e **Contrato do Projeto**.

## <a name="estimate-by-using-a-contract"></a>Estimar utilizando um contrato

Se tiver utilizado uma proposta quando criou um contrato baseado em projetos, a estimativa que fez para cada linha de proposta na proposta é copiada para o contrato do projeto. A estrutura de um contrato do projeto é semelhante à estrutura da proposta do projeto que tem linhas, detalhes de linha e agendas de faturação.

As estimativas podem ser efetuadas diretamente num contrato do projeto, como numa proposta do projeto. Para obter uma proposta do projeto, a estimativa é efetuada através da utilização de itens de contrato e detalhes de item de contrato. Os detalhes de item de contrato também podem ser gerados a partir de um plano do projeto criado com a abordagem de estimativa de baixo para cima.

Os detalhes de item de contrato podem ser utilizados para estimar o tempo, as despesas ou as taxas. Os montantes de imposto estimados também podem ser introduzidos num detalhe de item de contrato.

As estimativas de material não são permitidas em detalhes de item de contrato.

Os processos suportados num contrato do projeto são a criação e confirmação de faturas. A criação de faturas cria um rascunho de uma fatura baseada em projetos que inclui todos os valores reais de vendas não faturadas até à data atual.

A confirmação faz com que o contrato seja só de leitura e altera o estado de **Rascunho** para **Confirmado**. Depois de executar esta ação, não é possível anulá-la. Uma vez que esta ação é permanente, é recomendável manter o contrato num estado de **Rascunho**.

A única diferença entre contratos de rascunho e contratos confirmados é o respetivo Estado e o facto de os contratos de rascunho poderem ser editados, ao passo que os contratos confirmados não podem. A criação de faturas e a monitorização de valores reais podem ser efetuadas em contratos de rascunho e em contratos confirmados.

As operações de Projeto não suporta ordens de alteração em contratos ou projetos.

## <a name="estimating-projects"></a>Estimar projetos

Pode estimar o tempo e as despesas dos projetos. As operações de Projeto não permite estimativas de materiais ou taxas em projetos.

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
| Quando o utilizador descreve um recurso numa tarefa do projeto                                                                                                                                                                                                                                                                                            | O registo da linha de estimativa para mostrar o valor de venda da tarefa é criado quando uma tarefa é criada com todas as dimensões de definição de preços necessárias. As unidades organizacionais e a função são as dimensões de definição de preços | Contrato do Projeto | Tempo        |                                                                                   |
|     | O registo da linha de estimativa para mostrar o valor de custo da tarefa é criado quando uma tarefa é criada com todas as dimensões de definição de preços necessárias. Todos os campos não monetários são copiados da linha de estimativa de vendas para a linha de estimativa de custo pelo sistema. A função e a unidade organizacional são as dimensões de definição de preços para as taxas de faturação e o custo.                                                                                                                                                                                                                | Custo             | Tempo           |                                                                                   |



## <a name="customize-the-quote-line-detail-and-contract-line-detail-entities"></a>Personalizar as entidades de Detalhe de linha de proposta e Detalhe de item de contrato

Se tiver adicionado um campo personalizado aos detalhes de linha de proposta e pretender que o sistema introduza o valor do campo como um valor predefinido na linha de custo relacionada que cria, utilize as ferramentas de registo de plug-in **PreOperationContractLineDetailUpdate** e **PreOperationQuoteLineDetailUpdate**. Estes plug-ins têm de ser registados após o detalhe de linha de proposta ou o detalhe de item de contrato ser alterado. Siga estes passos para concluir o processo.

1. Abra o PluginRegistrationTool e ligue-se à sua instância online.
2. Selecione **Procurar** e procure o plug-in para atualizar.
3. Selecione o plug-in e, em seguida, na página principal, clique em **Selecionar**.
4. Selecione o passo do plug-in a atualizar, clique com o botão direito do rato e, em seguida, selecione **Atualizar**.
5. Na caixa de diálogo **Atualizar Passo Existente**, no campo **Atributos de Filtragem**, selecione o botão de reticências (**...**):
6. Na caixa de diálogo **Selecionar Atributos**, selecione as caixas de verificação para obter os atributos personalizados.
7. Selecione **OK** para fechar a caixa de diálogo e, em seguida, selecione **Atualizar Passo**.
8. Repita os passos 1 a 7 para o segundo plug-in.
9. Feche o **PluginRegistrationTool**.
