---
title: Estimar um item de contrato baseado no projeto – lite
description: Este artigo fornece informações sobre a estimativa de um item de contrato baseado em projeto.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 8b4379cc5822d08b55623f0f3d4d49791af90927
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914416"
---
# <a name="estimate-a-projectbased-contract-line---lite"></a>Estimar um item de contrato baseado no projeto – lite

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

No Dynamics 365 Project Operations, um item de contrato baseado em projetos tem detalhes que ajudam a estimar o custo e as receitas potenciais do trabalho envolvido para entregar o item de contrato.

Para estimar um item de contrato baseado em projetos, aceda ao separador **Detalhe do Item de Contrato** no **Item de Contrato** baseado em projetos.  Existem duas formas de criar uma estimativa num item de contrato baseado em projetos:

   - Crie uma estimativa diretamente no item de contrato adicionando manualmente detalhes do item de contrato.
   - Crie um projeto e um plano de projeto e, em seguida, associe o projeto e as tarefas ao item de contrato do projeto. Isto permite o processo através do qual pode importar a estimativa do plano de projeto para o item de contrato com base nos componentes incluídos no item de contrato.

## <a name="create-an-estimation-directly-on-a-projectbased-contract-line"></a>Criar uma estimativa diretamente num item de contrato baseado no projeto

Para criar uma estimativa diretamente num item de contrato baseado em projeto, siga estes passos:

1. Vá para o item de contrato e selecione o separador **Detalhe do Item de Contrato**. Os itens que cria neste separador são resumidos e exibidos como o **Valor Contratado** para este **Item de Contrato**. 
2. Na subgrelha **Detalhes do Item de Contrato**, selecione **Novo Detalhe de Item de Contrato**. Abre-se um controlador de deslize de criação rápida. Os seguintes campos estão disponíveis na página **Detalhes da linha de contrato**.

| Campo | Localização | Descrição | Impacto a jusante |
| --- | --- | --- | --- |
| **Descrição** | **Criação Rápida** | Uma descrição da estimativa específica. | Este valor é predefinido ao detalhe da linha de contrato relacionada para o custo que é automaticamente criado. |
| **Classe de Transação** | **Criação Rápida** | Esta é uma lista de classes de transações incluída no separador **Geral** do item de contrato baseado no projeto. | Este valor é predefinido ao detalhe da linha de contrato relacionada para o custo que é automaticamente criado. |
| **Selecionar Produto** | **Criação rápida** | Aplica-se quando a classe de transação é **Material**. Pode especificar se esta linha de estimativa é para um produto (catálogo) **Existente** ou para um produto **Acrescentado manualmente**. | Este valor é predefinido ao detalhe da linha de contrato relacionada para o custo que é automaticamente criado. |
| **Produto** | **Criação rápida** | O ID do produto do catálogo de produtos. Este campo só está ativado quando seleciona **Produto existente** no campo **Selecionar produto**. O ID é usado para recuperar o preço de venda da lista de preços do projeto no contrato. | Este valor é predefinido ao detalhe da linha de contrato relacionada com o custo que é automaticamente criado. |
| **Produto acrescentado manualmente** | **Criação rápida** | Um campo de texto para introduzir o nome do produto. Este campo só está ativado quando seleciona **Acrescentado manualmente** no campo **Selecionar produto**.| Este valor é predefinido ao detalhe da linha de contrato relacionada para o custo que é automaticamente criado. |
| **Função** | **Criação Rápida** | A função da pessoa que está a realizar este trabalho ou a incorrer nesta despesa. | Este valor é predefinido ao detalhe da linha de contrato relacionada para o custo que é automaticamente criado.|
| **Categoria** | **Criação Rápida** | A categoria do trabalho ou da despesa. |Este valor é predefinido ao detalhe da linha de contrato relacionada para o custo que é automaticamente criado.|
| **Data de Início** | **Criação Rápida** | A data de início do trabalho. | Este valor é predefinido ao detalhe da linha de contrato relacionada para o custo que é automaticamente criado. |
| **Data de Fim** | **Criação Rápida** | A data de fim do trabalho. | Este valor é predefinido ao detalhe da linha de contrato relacionada para o custo que é automaticamente criado. |
| **Unidade de Atribuição de Recursos** | **Criação Rápida** | A unidade de reabastecimento que incorre neste custo e fornece o recurso para trabalhar nele. |Este valor é predefinido ao detalhe do item de contrato relacionado para o custo que é automaticamente criado e usado na recuperação de preço de custo. |
| **Agenda de unidades** | **Criação rápida** | O grupo unitário do trabalho, produto ou despesas. As unidades pertencem a uma agenda de unidades ou a um grupo de unidades. Por exemplo, *milhas* e *quilómetros (kms)* são unidades que pertencem a um grupo de unidades que descrevem a distância. | Este valor é predefinido ao detalhe da linha de contrato relacionada para o custo que é automaticamente criado. |
| **Unidade** | **Criação Rápida** | A unidade de trabalho, produto ou despesas. | Este valor é predefinido ao detalhe da linha de contrato relacionada para o custo que é automaticamente criado. |
| **Quantidade** | **Criação Rápida** | A quantidade de trabalho, produto ou despesas. | Este valor é predefinido ao detalhe da linha de contrato relacionada para o custo que é automaticamente criado. |
| **Preço unitário** | **Criação Rápida** | A taxa de faturação do papel que está a desempenhar o trabalho, o preço unitário do produto ou o preço de venda do produto ou categoria de despesas. Este campo predefine o **Tempo** com base na combinação de valores de dimensão de preços na linha de preço de função da lista de preços do projeto que é eficaz para a data de início. Para **despesas**, a predefinição deste campo é da configuração de preços para a categoria de transação na lista de preços do projeto que é efetiva para a data de início. Se o método de cálculo de preços para a categoria de transação não for o **preço por unidade**, não existe valor predefinido e este campo é deixado em branco. Para produtos, esta predefinição de campo baseia-se na linha **Item da lista de preços** na lista de preço de projeto que é eficaz para a data de início.| A taxa de custo da função que está a desempenhar o trabalho, ou o custo por unidade da categoria de despesa ou o custo unitário do produto. Este campo predefine o **Tempo** com base na combinação de valores de dimensão de preços na linha de preço de função da lista de preços de custo anexada à unidade contratada que é eficaz para a data de início. Para despesas, a predefinição deste campo é baseada na linha de preços da categoria da lista de preços de custos anexada à unidade de contratação que é efetiva para a data de início. Se o método de cálculo de preços para a categoria de transação não for o preço por unidade, não existe valor predefinido e este campo é deixado em branco. Para produtos, esta predefinição de campo baseia-se na linha **Item da lista de preços** da lista de preço de curso anexada à unidade de contrato que é eficaz para a data de início.|
| **Imposto Estimado** | **Criação Rápida** | O imposto estimado para este trabalho ou despesa. | O imposto estimado para este trabalho ou despesa. |
| **Montante** | **Criação Rápida** | Pode adicionar o valor neste campo se os campos **Quantidade** e **Preço** ficarem em branco. Se **Quantidade** e **Preço** forem preenchidos, o campo **Montante** é apenas de leitura e é calculado como **(Quantidade \* Preço Unitário) + Imposto**. | &nbsp; |

## <a name="update-prices-on-contract-line-details"></a>Atualizar os preços nos detalhes do item de contrato

Se alterar os preços na lista de preços do projeto que está anexada ao contrato ou à lista de preços de custo da unidade contratante, pode atualizar os preços nos detalhes do item de contrato individual para refletir a alteração. Na página **Contrato**, selecione **Recalcular**. Um aviso parece informá-lo que os preços de todas as linhas contratuais deste contrato são repostos. Selecione **Sim** para atualizar os preços tanto para as vendas como para os detalhes do item de contrato de custos.

## <a name="access-contract-line-details-for-cost"></a>Aceder aos detalhes do item de contrato para custo

No separador **Detalhes do Item de Contrato**, selecione uma linha na grelha para apresentar ações na barra de ferramentas da subgrelha. A primeira ação na barra de ferramentas da subgrelha é **Abrir Detalhe do Custo**. Para ver a taxa de custos e o montante relacionados para este detalhe do item de contrato, selecione **Abrir Detalhe do Custo**. 

> [!NOTE]
> A alteração da empresa de atribuição de recursos, unidade de atribuição de recursos, quantidade, datas, função ou valores de categoria no detalhe do item de contrato para **Custo** também altera os valores correspondentes no detalhe do item de contrato para **Vendas**.

## <a name="currency-on-contract-line-details-for-cost-and-sales"></a>Moeda em detalhes do item de contrato para custos e vendas

O detalhe do item de contrato para **Vendas** define a moeda predefinida da lista de preços do projeto que é eficaz para a data de início do detalhe do item de contrato.

O detalhe do item de contrato para **Custo** define a moeda predefinida da lista de preços da unidade contratante do contrato que é eficaz para a data de início do detalhe do item de contrato para **Custo**.

Os cálculos de rentabilidade convertem os montantes dos detalhes do item de contrato para **Custo** e **Vendas** na moeda base do ambiente para reportar as margens efetivas e estimadas globais do contrato.

> [!NOTE]
> Podem ocorrer erros de arredondamento de moeda e margens alteradas devido à falta de taxas de câmbio efetivas da data. Utilize estes cálculos apenas em contratos de projeto, uma vez que se trata de aproximações e não são para relatórios estatutários ou outros que exijam maior precisão de arredondamento e sensibilização para a efetividade da data para as taxas de câmbio.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
