---
title: Calcular uma linha de proposta de projeto
description: Este tópico fornece informações sobre como criar uma estimativa numa linha de proposta de um projeto.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 84283ac055aea802fadbd6814ea65a6d3dc01d29e1e3c6290ef11f72f6a75692
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003965"
---
# <a name="estimate-a-project-quote-line"></a>Calcular uma linha de proposta de projeto

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

Uma linha de proposta baseada em projetos tem detalhes que ajudam a estimar o custo e as receitas potenciais do trabalho envolvido para entregar a linha de proposta.

Para estimar uma linha de proposta baseada em projeto, na linha de proposta, selecione o separador **Detalhe da linha de proposta**. Existem duas formas de criar uma estimativa numa linha de proposta baseada em projeto:

   - Criar manualmente a estimativa diretamente na linha de proposta ao utilizar os detalhes da linha de proposta. 
   - Crie um projeto e um plano de projeto, e depois associe o projeto e as tarefas do projeto à linha de proposta. Será ativado o processo para importar as estimativas no plano de projeto para a linha de proposta baseado nas informações fornecidas.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Criar estimativas diretamente numa linha de proposta baseada em projetos

Para criar estimativas diretamente numa linha de proposta de projeto, siga estes passos:

1. Para criar uma estimativa numa linha de proposta baseada em projetos, selecione o separador **Detalhe de Linha de Proposta**. O item que criar neste separador resumirá o valor proposto para esta linha de proposta. 
2. Para criar detalhes da linha de proposta, selecione **Novo detalhe da linha de proposta** na subgrelha **Detalhes da Linha de Proposta**. É aberto o controlo de deslize de criação rápida. Os seguintes campos na página **Linha proposta**.

| **Campo** | **Localização** | **Descrição** | **Impacto a jusante** |
| --- | --- | --- | --- |
| Descrição | Criação rápida | Uma descrição da estimativa específica. | Este valor é predefinido ao detalhe da linha de proposta relacionada para o custo que é automaticamente criado. |
| Classe de Transação | Criação rápida | Esta lista pendente fornece as classes de transações que estão incluídas no separador **Geral** da linha de proposta baseada em projetos.  | Este valor é predefinido ao detalhe da linha de proposta relacionada para o custo que é automaticamente criado. |
| Selecionar Produto | Criação rápida | Aplica-se quando a classe de transação é **Material**. Pode selecionar para especificar que esta linha de estimativa é para um produto (catálogo) **Existente** ou para um produto **Acrescentado manualmente**. | Este valor é predefinido ao detalhe da linha de proposta relacionada para o custo que é automaticamente criado. |
| Produto | Criação rápida | O ID do produto do catálogo de produtos. Este campo só está ativado quando seleciona **Existente** no campo **Selecionar produto**. O ID é usado para recuperar o preço de venda da lista de preços do projeto na proposta. | Este valor é predefinido ao detalhe da linha de proposta relacionada para o custo que é automaticamente criado. |
| Produto Acrescentado Manualmente | Criação rápida | Uma caixa de texto para acrescentar manualmente no nome do produto. Este campo só está ativado quando seleciona **Acrescentado manualmente** no campo **Selecionar produto**.| Este valor é predefinido ao detalhe da linha de proposta relacionada para o custo que é automaticamente criado. |
| Função | Criação rápida | A função da pessoa que irá realizar este trabalho ou incorrer nesta despesa. | Este valor é predefinido ao detalhe da linha de proposta relacionada para o custo que é automaticamente criado. |
| Categoria | Criação rápida | A categoria do trabalho ou da despesa. | Este valor é predefinido ao detalhe da linha de proposta relacionada para o custo que é automaticamente criado. |
| Data de Início | Criação rápida | A data de início do trabalho. | Este campo é predefinido ao detalhe da linha de proposta para o custo que é automaticamente criado. |
| Data de Fim | Criação rápida | A data de fim do trabalho. | Este campo é predefinido ao detalhe da linha de proposta para o custo que é automaticamente criado. |
| Empresa de Recursos | Criação Rápida | A empresa de recursos ou a entidade legal que incorre neste custo e fornece o recurso para trabalhar nele. | O valor predefinido ao detalhe da linha de proposta relacionado para o custo que é automaticamente criado e usado na recuperação de preço de custo. |
| Unidade de Atribuição de Recursos | Criação rápida | A unidade de reabastecimento que incorre neste custo e fornece o recurso para trabalhar nele. | Este valor predefinido ao detalhe da linha de proposta relacionado para o custo que é automaticamente criado e usado na recuperação de preço de custo. |
| Agenda de unidades | Criação rápida | O grupo unitário do trabalho, produto ou despesas. As unidades pertencem a uma agenda de unidades ou a um grupo de unidades. Por exemplo, milhas e quilómetros (kms) são unidades que pertencem a um grupo de unidades que descrevem distância. | Este valor é predefinido ao detalhe da linha de proposta relacionada para o custo que é automaticamente criado. |
| Unidade | Criação rápida | A unidade do trabalho, produto ou despesas. | Este valor é predefinido ao detalhe da linha de proposta relacionada para o custo que é automaticamente criado. |
| Quantidade | Criação rápida | A quantidade de trabalho, produto ou despesas. | Este valor é predefinido ao detalhe da linha de proposta relacionada para o custo que é automaticamente criado. |
| Preço unitário | Criação Rápida |A taxa de faturação do papel que está a desempenhar o trabalho, o preço unitário do produto ou o preço de venda do produto ou categoria de despesas. A predefinição para **Tempo** baseia-se na combinação de valores de dimensão de preços na linha de preço de função da lista de preços do projeto que é eficaz para a data de início. Para **despesas**, a predefinição é da configuração de preços para a categoria de transação na lista de preços do projeto que é efetiva para a data de início. Se o método de cálculo de preços para a categoria de transação não for o preço por unidade, não existe valor predefinido e este campo é deixado em branco. Para produtos, esta predefinição de campo baseia-se na linha **Item da lista de preços** na lista de preço de projeto que é eficaz para a data de início.| A taxa de custo da função que está a desempenhar o trabalho; ou o custo por unidade da categoria de despesa ou o custo unitário do produto. A predefinição para **Tempo** baseia-se na combinação de valores de dimensão de preços na linha de preço de função da lista de preços de custo anexada à unidade contratada que é eficaz para a data de início. Para despesas, o padrão baseia-se na linha de preço de categoria do item da lista de preços anexada à unidade de contrato que é eficaz para a data de início. Se o método de preços para a categoria de transação não for preço por unidade, não há incumprimento e este campo fica em branco. Para produtos, esta predefinição de campo baseia-se na linha **Item da lista de preços** da lista de preço de curso anexada à unidade de contrato que é eficaz para a data de início.|
| Imposto Estimado | Criação rápida | Poderá introduzir manualmente o imposto estimado para este trabalho ou despesa. | Este campo não tem impacto a jusante. |
| Montante | Criação rápida | Pode introduzir manualmente as informações neste campo se os campos **Quantidade** e **Preço** forem deixados em branco. Se estes campos não estiverem em branco, este campo fica de só leitura e é calculado como (Quantidade \* Preço unitário) + Imposto. | Este campo não tem impacto a jusante. |

## <a name="update-prices-on-quote-line-details"></a>Atualizar preços nos detalhes da linha de proposta

Se alterou os preços na lista de preços do projeto que está anexada à proposta, ou na lista de preços de custo da unidade de contratação, pode selecionar **Recalcular** na página **Proposta** para atualizar os preços nos detalhes da linha de proposta individual para refletir esta alteração. Quando selecionar **Recalcular** aparece um aviso que o informa que os preços em linha de proposta para todas as linhas de proposta desta proposta serão reiniciados. Selecione **Sim** para atualizar os preços tanto das vendas e os detalhes da linha de proposta de custos.

## <a name="access-quote-line-details-for-cost"></a>Aceder aos detalhes da linha de proposta para o custo

Para aceder aos detalhes da linha de proposta para custo, siga estes passos:

1. No separador **Detalhes da linha de proposta** selecione uma linha na grelha para ativar as ações na barra de ferramentas da subrede. 
2. Selecione **Abrir Detalhe de Custo** para ver a taxa de custo relacionada e o montante desta linha de proposta.

> [!NOTE]
> Alterar os valores da unidade de atribuição de recursos, quantidade, datas, função ou categoria no detalhe da linha de proposta para o custo alterará os valores correspondentes nos detalhes da linha de proposta para as vendas.

## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Moeda nos detalhes da linha de proposta para custos e vendas

A moeda no detalhe da linha de proposta para padrões de vendas da lista de preços do projeto que é eficaz para a data de início do detalhe da linha de proposta.

A moeda no detalhe da linha de proposta para padrões de custo da lista de preços da unidade contratante da proposta que é efetiva para a data de início do detalhe da linha de proposta para custo.

> [!NOTE]
> Os cálculos de rentabilidade convertem o montante nos detalhes da linha de proposta para o custo e as vendas na moeda base do ambiente para reportar a margem estimada global na proposta. Podem ocorrer erros de arredondamento de moeda e margens alteradas devido à falta de taxas de câmbio efetivas da data. Utilize estes cálculos apenas em propostas de projeto, uma vez que se trata de aproximações e não são relatórios estatutários ou outros que exijam maior precisão de arredondamento e sensibilização para a efetividade da data para as taxas de câmbio.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
