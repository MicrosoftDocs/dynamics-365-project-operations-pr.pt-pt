---
title: Conceitos de estimativa financeira
description: Este tópico fornece informações sobre estimativas financeiras de projetos no Project Operations.
author: rumant
ms.date: 03/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 488b61ee1e81aac47fa92fff141f17b023e4f1c0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002610"
---
# <a name="financial-estimation-concepts"></a>Conceitos de estimativa financeira

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

Em Dynamics 365 Project Operations, pode estimar financeiramente os seus projetos em duas fases: 
1. Durante a fase de pré-venda antes do negócio ser ganho. 
2. Durante a fase de execução após a criação do contrato do projeto. 

Pode criar uma estimativa financeira para o trabalho baseado em projetos utilizando qualquer uma das seguintes 3 páginas:
- A página da **Linha Proposta** utilizando os detalhes da linha de proposta.  
- A página da **Linha de contrato de projeto** utilizando os detalhes da linha de contrato. 
- A página do **Projeto**, utilizando as páginas do separador **Tarefas** ou **Estimativas de Despesas**.

## <a name="use-a-project-quote-to-create-an-estimate"></a>Use uma proposta do projeto para criar uma estimativa
Numa proposta baseada em projetos, pode utilizar a entidade **Detalhe de linha de proposta** para estimar o trabalho que é necessário para entregar um projeto. Em seguida, pode partilhar essa estimativa com o cliente.

As linhas de proposta baseadas em projetos podem ter de zero a muitos detalhes de linha de proposta. Os detalhes de linha de proposta são utilizados para estimar o tempo, as despesas ou as taxas. O Microsoft Dynamics 365 Project Operations não permite estimativas de material em detalhes de linha de proposta. Estes são chamados de classes de transação. Os montantes de imposto estimados também podem ser introduzidos numa classe de transação.

Para além das classes de transação, os detalhes de linha de proposta têm um tipo de transação. Dois tipos de transação são suportados para os detalhes de linha de proposta: **Custo** e **Contrato do Projeto**.

## <a name="use-a-project-contract-to-create-an-estimate"></a>Use um contrato do projeto para criar uma estimativa

Se tiver utilizado uma proposta quando criou um contrato baseado em projetos, a estimativa que fez para cada linha de proposta na proposta é copiada para o contrato do projeto. A estrutura de um contrato do projeto é semelhante à estrutura da proposta do projeto que tem linhas, detalhes de linha e agendas de faturação.

As estimativas podem ser efetuadas diretamente num contrato do projeto, como numa proposta do projeto. Para obter uma proposta do projeto, a estimativa é efetuada através da utilização de itens de contrato e detalhes de item de contrato. Os detalhes de item de contrato também podem ser gerados a partir de um plano do projeto criado com a abordagem de estimativa de baixo para cima.

Os detalhes de item de contrato podem ser utilizados para estimar o tempo, as despesas ou as taxas. Os montantes de imposto estimados também podem ser introduzidos num detalhe de item de contrato.

As estimativas de material não são permitidas em detalhes de item de contrato.

## <a name="use-a-project-to-create-an-estimate"></a>Use um projeto para criar uma estimativa 

Pode estimar o tempo e as despesas dos projetos. O Project Operations não suporta estimativas de materiais ou taxas em projetos.

As estimativas de tempo são geradas quando cria uma tarefa e identifica os atributos de um recurso genérico que é necessário para efetuar a tarefa. As estimativas de tempo são geradas a partir de tarefas de agendamento. As estimativas de tempo não são criadas se criar membros da equipa genéricos fora do contexto da agenda.

As estimativas de despesas são introduzidas na grelha da página **Estimativas de despesas**.

A criação de uma estimativa para um projeto é considerada uma boa prática porque pode construir estimativas detalhadas de baixo para cima para o trabalho ou tempo e despesas em cada tarefa no plano do projeto. Em seguida, pode utilizar esta estimativa detalhada para criar estimativas para cada linha de proposta e construir uma proposta mais credível para o cliente. Quando importa ou cria uma estimativa detalhada na linha de proposta utilizando o plano do projeto, o Project Operations importa os valores de venda e os valores de custo destas estimativas. Após a importação, pode ver as métricas de rentabilidade, margens e viabilidade na proposta do projeto.

## <a name="understanding-estimates"></a>Compreender estimativas

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
