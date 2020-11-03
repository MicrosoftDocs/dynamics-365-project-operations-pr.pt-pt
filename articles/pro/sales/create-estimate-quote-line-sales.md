---
title: Estimar uma linha de proposta baseada no projeto
description: Este tópico fornece informações sobre como criar uma estimativa numa linha de proposta baseada em projetos.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 65aee7238781ac90f603e57c6d9b0b92cabd6644
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082308"
---
# <a name="estimating-a-project-based-quote-line"></a>Estimar uma linha de proposta baseada no projeto

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

Uma linha de proposta baseada em projetos tem detalhes que ajudam a estimar o custo e as receitas potenciais do trabalho envolvido para entregar a linha de proposta.

Para estimar uma linha de proposta baseada em projetos, na linha de proposta baseada em projetos, selecione o separador **Detalhe da Linha de Proposta**. Existem duas formas de criar uma estimativa numa linha de proposta baseada em projetos:

- Criar manualmente a estimativa diretamente na linha de proposta ao utilizar os detalhes da linha de proposta 
- Crie um projeto e um plano de projeto, e depois associe o projeto e as tarefas do projeto à linha de proposta. Será ativado o processo para importar as estimativas no plano de projeto para a linha de proposta baseado nas informações fornecidas.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Criar estimativas diretamente numa linha de proposta baseada em projetos

Para criar uma estimativa numa linha de proposta baseada em projetos, selecione o separador **Detalhe de Linha de Proposta**. O item que criar neste separador resumirá o valor proposto para esta linha de proposta. 

Para criar detalhes da linha de proposta, selecione **+ Novo detalhe da linha de proposta** na subgrelha **Detalhes de Linha de Proposta**. É aberto o controlo de deslize de criação rápida. Os seguintes campos no formulário **Linha de Proposta** :

| **Campo** | **Localização** | **Relevância, finalidade e orientação** | **Impacto a jusante** |
| --- | --- | --- | --- |
| Descrição | Criação rápida | Uma descrição da estimativa específica. | Este campo assume por predefinição o detalhe da linha de proposta relacionada para o custo que é criado automaticamente. |
| Classe de Transação | Criação rápida | Esta lista pendente fornece as classes de transações que estão incluídas no separador **Geral** da linha de proposta baseada em projetos.  | Este campo assume por predefinição o detalhe da linha de proposta relacionada para o custo que é criado automaticamente. |
| Função | Criação rápida | A pessoa que irá executar este trabalho ou incorrer nesta despesa. | Este campo assume por predefinição o detalhe da linha de proposta relacionada para o custo que é criado automaticamente. |
| Categoria | Criação rápida | Categoria do trabalho ou da despesa. | Este campo assume por predefinição o detalhe da linha de proposta relacionada para o custo que é criado automaticamente. |
| Data de Início | Criação rápida | Data de início do trabalho. | Este campo assume por predefinição o detalhe da linha de proposta relacionada para o custo que é criado automaticamente. |
| Data de Fim | Criação rápida | Data de fim do trabalho. | Este campo assume por predefinição o detalhe da linha de proposta relacionada para o custo que é criado automaticamente. |
| Unidade de Atribuição de Recursos | Criação rápida | Unidade de atribuição de recursos que incorrerá neste custo e fornecerá o recurso para trabalhar nele. | Este campo assume por predefinição o detalhe da linha de proposta relacionada para o custo que é criado automaticamente. Este campo também é utilizado na obtenção do preço de custo. |
| Agenda de unidades | Criação rápida | Grupo de unidades do trabalho ou da despesa. As unidades pertencem a uma agenda de unidades ou a um grupo de unidades. Por exemplo, Milhas e KMs são unidades que pertencem a um grupo de unidades que descrevem a distância. | Este campo assume por predefinição o detalhe da linha de proposta relacionada para o custo que é criado automaticamente. |
| Unidade | Criação rápida | Unidade do trabalho ou da despesa. | Este campo assume por predefinição o detalhe da linha de proposta relacionada para o custo que é criado automaticamente. |
| Quantidade | Criação rápida | Quantidade do trabalho ou da despesa | Este campo assume por predefinição o detalhe da linha de proposta relacionada para o custo que é criado automaticamente. |
| Preço unitário | Criação rápida | Taxa de faturação da função que está a executar o trabalho ou o Preço de venda da categoria de despesa. Este campo assume por predefinição o Tempo baseado na combinação da função e da unidade de atribuição de recursos na lista de preços do projeto em vigor para a data de início. Para as despesas, este campo assume por predefinição a configuração de preço para a categoria de transação na lista de preços do projeto em vigor para a data de início. Se o método de cálculo de preços para a categoria de transação não for o preço por unidade, não existe valor predefinido e este campo é deixado em branco. | Taxa de custo da função que está a executar o trabalho ou o custo por unidade da categoria de despesa. Este campo assume por predefinição o Tempo baseado na combinação da função e da unidade de atribuição de recursos da Unidade de contratação da Lista de Preços da Proposta em vigor para a data de início. Para as despesas, este campo assume por predefinição a configuração de preço para a categoria de transação na lista de preços de custo da Unidade de contratação em vigor para a data de início. Se o método de cálculo de preços para a categoria de transação não for o preço por unidade, não existe valor predefinido e este campo é deixado em branco. |
| Imposto Estimado | Criação rápida | Poderá introduzir manualmente o imposto estimado para este trabalho ou despesa. | Este campo não tem impacto a jusante. |
| Montante | Criação rápida | Pode introduzir manualmente as informações neste campo se os campos **Quantidade** e **Preço** forem deixados em branco. Se estes campos não estiverem em branco, este campo fica só de leitura e é calculado como (Quantidade \* Preço unitário) + Imposto. | Este campo não tem impacto a jusante. |

## <a name="update-prices-on-quote-line-details"></a>Atualizar preços nos detalhes da linha de proposta

Se alterou os preços na lista de preços do projeto que está anexada à proposta, ou na lista de preços de custo da unidade de contratação, pode selecionar **Recalcular** na página **Proposta** para atualizar os preços nos detalhes da linha de proposta individual para refletir esta alteração. Quando selecionar **Recalcular** , é gerado um aviso que o informa que os preços nos detalhes da linha de proposta para todas as linhas de proposta desta proposta serão repostos. Selecione **Sim** para atualizar os preços tanto das vendas e os detalhes da linha de proposta de custos.

## <a name="access-quote-line-details-for-cost"></a>Aceder aos detalhes da linha de proposta para o custo

No separador **Detalhes de Linha de Proposta** , selecione uma linha na grelha para ativar algumas ações na barra de ferramentas da subgrelha. A primeira ação na barra de ferramentas da subgrelha quando um detalhe da linha de proposta é selecionado é **Abrir Detalhe de Custo**. Selecione **Abrir Detalhe de Custo** para ver a taxa de custo relacionada e o montante desta linha de proposta.

> [!NOTE]
> Alterar os valores da unidade de atribuição de recursos, quantidade, datas, função ou categoria no detalhe da linha de proposta para o custo alterará os valores correspondentes nos detalhes da linha de proposta para as vendas.
## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Moeda nos detalhes da linha de proposta para custos e vendas

A moeda no detalhe da linha de proposta para as vendas assume por predefinição a lista de preços do projeto que está em vigor para a data de início do detalhe da linha de proposta.

A moeda no detalhe da linha de proposta para o custo assume por predefinição a lista de preços da unidade de contratação da proposta que está em vigor para a data de início do detalhe da linha de proposta para o custo.

Os cálculos de rentabilidade convertem o montante nos detalhes da linha de proposta para o custo e as vendas na moeda base do ambiente para reportar a margem estimada global na proposta.

Isto pode resultar em erros de arredondamento da moeda e na alteração das margens, dada a falta de taxas de câmbio em vigor na data. Utilize estes cálculos nas Propostas do Projeto apenas como aproximações e não como relatórios legais ou de outro tipo que exigem uma maior precisão de arredondamento e conhecimento da data efetiva para as taxas de câmbio.
