---
title: Estimativas financeiras para despesas em projetos
description: Este tópico fornece informações sobre como definir ou estimar as despesas baseadas em projetos.
author: rumant
manager: Annbe
ms.date: 03/19/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ad4901b1264289f1da881154bc147fc3f8da698f
ms.sourcegitcommit: 386921f44f1e9a8a828b140206d52945de07aee7
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 03/22/2021
ms.locfileid: "5701796"
---
# <a name="financial-estimates-for-expenses-on-projects"></a>Estimativas financeiras para despesas em projetos
_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

Dynamics 365 Project Operations permite que os gestores de projetos definam despesas baseadas em projetos para cada projeto ou uma tarefa. Cada item de despesa pode ser associado a uma tarefa específica do projeto. As despesas são categorizadas em diferentes categorias de despesas, que são definidas a nível organizacional. Os preços e os custos para cada categoria de despesas estão definidos na tabela de preços. 

Execute os seguintes passos para ver, adicionar ou eliminar uma despesa do projeto.

1. Vá para **Projetos** e selecione o projeto em que pretende trabalhar.
2. Selecione o separador **Estimativas do Projeto** e consulte a lista de despesas do projeto.
3. Selecione **Nova Despesa** para adicionar uma despesa. Também pode selecionar uma despesa a eliminar e, em seguida, selecionar **Eliminar Despesa**.

A tabela seguinte fornece informações sobre os campos na **Linha estimativa de despesas** de um projeto. 

| **Campo** | **Descrição** | **Impacto a jusante** |
| --- | --- | --- |
| Tarefa | Uma lista de tarefas no projeto. Isto inclui tarefas de resumo e nó de folha. | A seleção de uma tarefa para uma linha de estimativa de despesas terá impacto no custo estimado da despesa e nas vendas estimadas de despesas para uma tarefa. Se este campo ficar vazio, a estimativa de despesas é rastreada e resumida apenas ao nível do projeto. |
| Categoria | Uma lista de categorias de transações que têm categorias de despesas ligadas na aplicação. | Selecionar uma categoria impulsiona preços e custos na linha de estimativa de despesas. |
| Data de início | A data prevista na qual a despesa irá ocorrer. | Este campo não tem impacto a jusante. |
| Grupo de unidades | O valor predefinido neste campo provém do grupo de unidade que é configurado como padrão na categoria selecionada. Pode atualizar este campo para selecionar outro grupo de unidades. | Este campo não tem impacto a jusante. |
| Unidade | O valor neste campo é padrão para a unidade padrão da categoria selecionada. Pode atualizar este campo para selecionar outra unidade. | A alteração da unidade resulta num preço e custo unitário diferentes. |
| Quantidade | A quantidade da despesa estimada em que irá incorrer. | Este campo não tem impacto a jusante. |
| Custo Unitário | O custo da categoria selecionada e da combinação unitária, tal como estabelecido na tabela de preços de custos aplicáveis | O custo unitário é sempre mostrado na moeda de custo do projeto. |
| Preço Unitário | O preço da categoria selecionada e da combinação unitária, tal como estabelecido na lista de preços de vendas aplicáveis. | O preço unitário é sempre mostrado na moeda de vendas do projeto. |
| Custo Total | O custo calculado como custo unitário de quantidade \*.| O valor de custo é sempre mostrado na moeda de custo do projeto. |
| Total de Vendas | O valor de vendas calculado como preço unitário de quantidade \*. | O valor de vendas é sempre mostrado na moeda de vendas do projeto. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
