---
title: Calcular um item de contrato de projeto
description: Esta tópico fornece informações sobre estimativas num item de contrato de projeto.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 53e3c291043ab102eb2f59221ae879acf766bb98
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589076"
---
# <a name="estimate-a-project-contract-line"></a>Calcular um item de contrato de projeto

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_ 

No Dynamics 365 Project Operations, um item de contrato baseado em projetos tem detalhes que ajudam a estimar o custo e as receitas potenciais do trabalho envolvido para entregar o item de contrato.

Para estimar um item de contrato baseado em projetos, aceda ao separador **Detalhe do Item de Contrato** no **Item de Contrato** baseado em projetos.  Existem duas formas de criar uma estimativa num item de contrato baseado em projetos:

   - Crie uma estimativa diretamente no item de contrato adicionando manualmente detalhes do item de contrato.
   - Crie um projeto e um plano de projeto e, em seguida, associe o projeto e as tarefas ao item de contrato do projeto. Isto permite o processo através do qual pode importar a estimativa do plano de projeto para o item de contrato com base nos componentes incluídos no item de contrato.

## <a name="create-an-estimate-directly-on-a-project-contract-line"></a>Criar uma estimativa diretamente num projeto para um item de contrato

Para criar uma estimativa diretamente num item de contrato de projeto, siga estes passos:

1. Vá para o item de contrato e selecione o separador **Detalhe do Item de Contrato**. Os itens que cria neste separador são resumidos e exibidos como o **Valor Contratado** para este **Item de Contrato**. 
2. Na subgrelha **Detalhes do Item de Contrato**, selecione **Novo Detalhe de Item de Contrato**. Abre-se um controlador de deslize de criação rápida. Os seguintes campos estão disponíveis na página **Detalhes da linha de contrato**.

| Campo | Localização | Descrição | Impacto a jusante |
| --- | --- | --- | --- |
| **Descrição** | **Criação Rápida** | Uma descrição da estimativa específica. | Este valor é predefinido ao detalhe da linha de contrato relacionada para o custo que é automaticamente criado. |
| **Classe de Transação** | **Criação Rápida** | Esta lista de classes de transações está incluída no separador **Geral** do item de contrato baseado no projeto. | Este valor é predefinido ao detalhe da linha de contrato relacionada para o custo que é automaticamente criado. |
| **Selecionar Produto** | **Criação rápida** | Aplica-se quando a classe de transação é **Material**. Pode selecionar para especificar que esta linha de estimativa é para um produto (catálogo) **Existente** ou para um produto **Acrescentado manualmente**. | Este valor é predefinido ao detalhe da linha de contrato relacionada para o custo que é automaticamente criado. |
| **Produto** | **Criação rápida** | O ID do produto do catálogo de produtos. Este campo só está ativado quando seleciona **Produto existente** no campo **Selecionar produto**. O ID é usado para recuperar o preço de venda da lista de preços do projeto no contrato. | Este valor é predefinido ao detalhe da linha de contrato relacionada para o custo que é automaticamente criado. |
| **Produto acrescentado manualmente** | **Criação rápida** | Um campo de texto para introduzir o nome do produto. Este campo só está ativado quando seleciona **Acrescentado manualmente** no campo **Selecionar produto**.| Este valor é predefinido ao detalhe da linha de contrato relacionada para o custo que é automaticamente criado. |
| **Função** | **Criação Rápida** | A função da pessoa que está a realizar este trabalho ou a incorrer nesta despesa. | Este valor é predefinido ao detalhe da linha de contrato relacionada para o custo que é automaticamente criado.|
| **Categoria** | **Criação Rápida** | A categoria do trabalho ou da despesa. | Este valor é predefinido ao detalhe da linha de contrato relacionada para o custo que é automaticamente criado.|
| **Data de Início** | **Criação Rápida** | A data de início do trabalho. | Este valor é predefinido ao detalhe da linha de contrato relacionada para o custo que é automaticamente criado. |
| **Data de Fim** | **Criação Rápida** | A data de fim do trabalho. | Este valor é predefinido ao detalhe da linha de contrato relacionada para o custo que é automaticamente criado. |
| **Empresa de Recursos** | **Criação Rápida** | A empresa de recursos ou a entidade legal que incorre neste custo e fornece o recurso para trabalhar nele. | Este valor é predefinido ao detalhe do item de contrato relacionado para o custo que é automaticamente criado e usado na recuperação de preço de custo. |
| **Unidade de Atribuição de Recursos** | **Criação Rápida** | A unidade de reabastecimento que incorre neste custo e fornece o recurso para trabalhar nele. | Este valor é predefinido ao detalhe do item de contrato relacionado para o custo que é automaticamente criado e usado na recuperação de preço de custo. |
| **Agenda de unidades** | **Criação rápida** | O grupo unitário do trabalho, produto ou despesas. As unidades pertencem a uma agenda de unidades ou a um grupo de unidades. Por exemplo, *milhas* e *quilómetros (kms)* são unidades que pertencem a um grupo de unidades que descrevem a distância. | Este valor é predefinido ao detalhe da linha de contrato relacionada para o custo que é automaticamente criado. |
| **Unidade** | **Criação Rápida** | A unidade de trabalho, produto ou despesas. | Este valor é predefinido ao detalhe da linha de contrato relacionada para o custo que é automaticamente criado. |
| **Quantidade** | **Criação Rápida** | A quantidade de trabalho, produto ou despesas. | Este valor é predefinido ao detalhe da linha de contrato relacionada para o custo que é automaticamente criado. |
| **Preço unitário** | **Criação Rápida** | A taxa de faturação do papel que está a desempenhar o trabalho, o preço unitário do produto ou o preço de venda do produto ou categoria de despesas. A predefinição para **Tempo** baseia-se na combinação de valores de dimensão de preços na linha de preço de função da lista de preços do projeto que é eficaz para a data de início. Para **Despesas**, o padrão para este campo é da configuração de preços para a categoria de transação na lista de preços do projeto que é eficaz para a data de início. Se o método de cálculo de preços para a categoria de transação não for o **preço por unidade**, não existe valor predefinido e este campo é deixado em branco. Para produtos, esta predefinição de campo baseia-se na linha **Item da lista de preços** na lista de preço de projeto que é eficaz para a data de início.| A taxa de custo da função que está a desempenhar o trabalho, ou o custo por unidade da categoria de despesa ou o custo unitário do produto. A predefinição para **Tempo** baseia-se na combinação de valores de dimensão de preços na linha de preço de função da lista de preços de custo anexada à unidade contratada que é eficaz para a data de início. Para **Despesas**, o padrão para este campo baseia-se na linha de preço de categoria do item da lista de preços anexada à unidade de contrato que é eficaz para a data de início. Se o método de cálculo de preços para a categoria de transação não for o preço por unidade, não existe valor predefinido e este campo é deixado em branco. Para produtos, esta predefinição de campo baseia-se na linha **Item da lista de preços** da lista de preço de curso anexada à unidade de contrato que é eficaz para a data de início.|
| **Imposto Estimado** | **Criação Rápida** | O imposto estimado para este trabalho ou despesa como entrada do utilizador. | &nbsp; |
| **Montante** | **Criação Rápida** | O valor neste campo pode ser adicionado se os campos de **Quantidade** e **Preço** ficarem em branco. Se os campos de **Quantidade** e **Preço** estiverem preenchidos, o campo **Valor** é lido apenas e é calculado como **(Preço Unitário da Quantidade \*) + Imposto**. | &nbsp; |

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
