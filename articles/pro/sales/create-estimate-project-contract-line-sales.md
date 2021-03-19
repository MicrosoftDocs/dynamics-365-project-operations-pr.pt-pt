---
title: Estimar um item de contrato baseado no projeto – lite
description: Este tópico fornece informações sobre a estimativa de um item de contrato baseado em projetos.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 186b982ee440576e10cf5b78922848b8877afd51
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273551"
---
# <a name="estimate-a-projectbased-contract-line---lite"></a>Estimar um item de contrato baseado no projeto – lite

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

No Dynamics 365 Project Operations, um item de contrato baseado em projetos tem detalhes que ajudam a estimar o custo e as receitas potenciais do trabalho envolvido para entregar o item de contrato.

Para estimar um item de contrato baseado em projetos, aceda ao separador **Detalhe do Item de Contrato** no **Item de Contrato** baseado em projetos.  Existem duas formas de criar uma estimativa num item de contrato baseado em projetos:

   - Crie uma estimativa diretamente no item de contrato adicionando manualmente detalhes do item de contrato.
   - Crie um projeto e um plano de projeto e, em seguida, associe o projeto e as tarefas ao item de contrato do projeto. Isto permite o processo através do qual pode importar a estimativa do plano de projeto para o item de contrato com base nos componentes incluídos no item de contrato.

## <a name="create-an-estimation-directly-on-a-projectbased-contract-line"></a>Criar uma estimativa diretamente num item de contrato baseado no projeto

1. Vá para o item de contrato e selecione o separador **Detalhe do Item de Contrato**. Os itens que cria neste separador são resumidos e exibidos como o **Valor Contratado** para este **Item de Contrato**. 
2. Na subgrelha **Detalhes do Item de Contrato**, selecione **+ Novo Detalhe de Item de Contrato**. Abre-se um controlador de deslize de criação rápida. Os seguintes campos estão disponíveis no formulário **Detalhes do Item de Contrato**:

| Campo | Localização | Descrição | Impacto a jusante |
| --- | --- | --- | --- |
| **Descrição** | **Criação Rápida** | Uma descrição da estimativa específica. | Este campo assume a predefinição do detalhe do item de contrato relacionado para os custos que são automaticamente criados. |
| **Classe de Transação** | **Criação Rápida** | Esta lista pendente é uma lista de classes de transações incluídas no separador **Geral** do item de contrato baseado em projeto. | Este campo assume a predefinição do detalhe do item de contrato relacionado para os custos que são automaticamente criados. |
| **Função** | **Criação Rápida** | A função da pessoa que está a realizar este trabalho ou a incorrer nesta despesa. | Este campo assume a predefinição do detalhe do item de contrato relacionado para os custos que são automaticamente criados. |
| **Categoria** | **Criação Rápida** | A categoria do trabalho ou da despesa. | Este campo assume a predefinição do detalhe do item de contrato relacionado para os custos que são automaticamente criados. |
| **Data de Início** | **Criação Rápida** | A data de início do trabalho. | Este campo assume a predefinição do detalhe do item de contrato relacionado para os custos que são automaticamente criados. |
| **Data de Fim** | **Criação Rápida** | A data de fim do trabalho. | Este campo assume a predefinição do detalhe do item de contrato para o custo que é automaticamente criado. |
| **Unidade de Atribuição de Recursos** | **Criação Rápida** | A unidade de atribuição de recursos que incorre neste custo e requer que o recurso trabalhe nele. | Este campo assume a predefinição do detalhe do item de contrato relacionado para os custos que são automaticamente criados. Este campo também é utilizado na obtenção do preço de custo. |
| **Agenda de unidades** | **Criação rápida** | O grupo de unidades do trabalho ou despesa. As unidades pertencem a uma agenda de unidades ou a um grupo de unidades. Por exemplo, *milhas* e *quilómetros (Kms)* são unidades que pertencem a um grupo de unidades que descrevem a distância. | Este campo assume a predefinição do detalhe do item de contrato relacionado para os custos que são automaticamente criados. |
| **Unidade** | **Criação Rápida** | A unidade do trabalho ou despesa. | Este campo assume a predefinição do detalhe do item de contrato relacionado para os custos que são automaticamente criados. |
| **Quantidade** | **Criação Rápida** | A quantidade do trabalho ou despesa. | Este campo assume a predefinição do detalhe do item de contrato relacionado para os custos que são automaticamente criados. |
| **Preço unitário** | **Criação Rápida** | A taxa de faturação da função que está a desempenhar o trabalho ou o preço de vendas da categoria de despesas. Este campo assume por predefinição o **Tempo** baseado na combinação da função e da unidade de atribuição de recursos na lista de preços do projeto em vigor para a data de início. Para despesas, a predefinição deste campo é da configuração de preços para a categoria de transação na lista de preços do projeto que é efetiva para a data de início. Se o método de cálculo de preços para a categoria de transação não for o **preço por unidade**, não existe valor predefinido e este campo é deixado em branco. | A taxa de custos da função que está a desempenhar o trabalho ou o custo por unidade da categoria de despesas. Este campo assume a predefinição **Tempo baseado na função** e na combinação da unidade de atribuição de recursos na linha de preços de função da lista de preços de custos anexada à unidade de contratação com efeito para a data de início. Para despesas, a predefinição deste campo é baseada na linha de preços da categoria da lista de preços de custos anexada à unidade de contratação que é efetiva para a data de início. Se o método de cálculo de preços para a categoria de transação não for o preço por unidade, não existe valor predefinido e este campo é deixado em branco. |
| **Imposto Estimado** | **Criação Rápida** | O imposto estimado para este trabalho ou despesa como entrada do utilizador. | O imposto estimado para este trabalho ou despesa como entrada do utilizador. |
| **Montante** | **Criação Rápida** | Este valor neste campo pode ser adicionado pelo utilizador se os campos **Quantidade** e **Preço** ficarem em branco. Se **Quantidade** e **Preço** forem preenchidos, o campo **Montante** é apenas de leitura e é calculado como **(Quantidade \* Preço Unitário) + Imposto**. | &nbsp; |

## <a name="update-prices-on-contract-line-details"></a>Atualizar os preços nos detalhes do item de contrato

Se alterar os preços na lista de preços do projeto que está anexada ao contrato ou à lista de preços de custo da unidade contratante, pode atualizar os preços nos detalhes do item de contrato individual para refletir a alteração. Na página **Contrato**, selecione **Recalcular**. Um aviso abre para informá-lo que os preços de todas os itens de contrato deste contrato são repostos. Selecione **Sim** para atualizar os preços tanto para as vendas como para os detalhes do item de contrato de custos.

## <a name="access-contract-line-details-for-cost"></a>Aceder aos detalhes do item de contrato para custo

No separador **Detalhes do Item de Contrato**, selecione uma linha na grelha para apresentar ações na barra de ferramentas da subgrelha. A primeira ação na barra de ferramentas da subgrelha é **Abrir Detalhe do Custo**. Para ver a taxa de custos e o montante relacionados para este detalhe do item de contrato, selecione **Abrir Detalhe do Custo**. 

> [!NOTE]
> A alteração da empresa de atribuição de recursos, unidade de atribuição de recursos, quantidade, datas, função ou valores de categoria no detalhe do item de contrato para **Custo** também altera os valores correspondentes no detalhe do item de contrato para **Vendas**.

## <a name="currency-on-contract-line-details-for-cost-and-sales"></a>Moeda em detalhes do item de contrato para custos e vendas

O detalhe do item de contrato para **Vendas** define a moeda predefinida da lista de preços do projeto que é eficaz para a data de início do detalhe do item de contrato.

O detalhe do item de contrato para **Custo** define a moeda predefinida da lista de preços da unidade contratante do contrato que é eficaz para a data de início do detalhe do item de contrato para **Custo**.

Os cálculos de rentabilidade convertem os montantes dos detalhes do item de contrato para **Custo** e **Vendas** na moeda base do ambiente para reportar as margens efetivas e estimadas globais do contrato.

> [!NOTE]
> Podem ocorrer erros de arredondamento de moeda e margens alteradas devido à falta de taxas de câmbio efetivas da data. Utilize estes cálculos em contratos de projeto apenas como aproximações e não para relatórios estatutários ou outros que exijam maior precisão de arredondamento e sensibilização para a efetividade da data para as taxas de câmbio.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]