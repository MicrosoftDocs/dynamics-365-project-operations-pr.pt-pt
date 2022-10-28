---
title: Estimativas financeiras para materiais em projetos
description: Este artigo fornece informações sobre a definição ou a estimativa de materiais baseados em projetos.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: eb33c8e2ead2a558bf53256095645011212ff343
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925721"
---
# <a name="financial-estimates-for-materials-on-projects"></a>Estimativas financeiras para materiais em projetos

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

Dynamics 365 Project Operations permite que os gestores de projetos definam custos de material baseados em projetos para cada projeto ou uma tarefa. Cada estimativa de material pode ser associado a uma tarefa específica do projeto. Os materiais utilizados em projetos podem ser produtos ou produtos escritos a partir do catálogo de produtos. Para cada combinação de um produto e uma unidade, um preço pode ser definido nas listas de preços do projeto para vendas e nas listas de preços do projeto para o custo.  

Complete os seguintes passos para visualizar, adicionar ou eliminar uma estimativa do material do projeto.

1. Vá a **Projetos** e selecione o projeto que pretende atualizar.
2. No separador **Estimativas de materiais**, consulte a lista de estimativas de material do projeto.
3. Selecione **Nova estimativa de material** para criar uma nova estimativa de material. Ou selecione uma estimativa de material para eliminar e, em seguida, selecione **Eliminar a estimativa de material**.

A tabela seguinte fornece informações sobre os campos na **Linha estimativa de material** num projeto. 

| **Campo** | **Descrição** | **Impacto a jusante** |
| --- | --- | --- |
| Tarefa | Uma lista de tarefas no projeto. Isto inclui tarefas de resumo e nó de folha. | Quando seleciona uma tarefa para uma linha de estimativa de material, o custo estimado do material e as vendas estimadas de material para uma tarefa são impactados. Se este campo ficar vazio, a estimativa de material é rastreada e resumida apenas ao nível do projeto. |
| Selecionar Produto |  Pode especificar se esta linha de estimativa é para um produto existente (catálogo) ou para um produto Escrever. | Este campo determina se seleciona um produto do catálogo ou um produto de acrescentar manualmente. |
| Produto | O ID do produto do catálogo de produtos. Ao selecionar um ID do produto, o valor no campo **Selecionar produto** é automaticamente atualizado para o **produto existente**. O ID é usado para obter os preços de custo e venda da lista de preços. | Este campo não tem impacto a jusante. |
| Descrição de produto acrescentado manualmente | Um campo de texto para acrescentar manualmente no nome do produto. Este campo deve ser usado quando seleciona **Acrescentado manualmente** no campo **Selecionar produto**.| Este campo não tem impacto a jusante. |
| Data de início | A data prevista para a utilização do material. | Este campo não tem impacto a jusante. |
| Grupo de unidades | O valor predefinido neste campo provém do grupo de unidade predefinido no produto do catálogo. Pode atualizar este campo para selecionar outro grupo de unidades. | Este campo não tem impacto a jusante. |
| Unidade | O valor neste campo tem origem na unidade padrão do produto selecionado. Pode atualizar este campo para selecionar outra unidade. | A alteração da unidade resulta num preço e custo unitário diferentes. |
| Quantidade | A quantidade estimada do produto que será utilizado no projeto. | Este campo não tem impacto a jusante. |
| Custo Unitário | O custo unitário do produto selecionado e da combinação unitária, tal como estabelecido na tabela de preços de custos aplicáveis. | O custo unitário é sempre mostrado na moeda de custo do projeto. Se não houver uma configuração do custo unitário para a combinação do produto e da configuração unitária na tabela de preços, o custo unitário será predefinido para 0,00. |
| Preço Unitário | O preço do produto selecionado e da combinação unitária, tal como estabelecido na lista de preços de vendas aplicáveis. | O preço unitário é sempre mostrado na moeda de vendas do projeto. Se não houver uma configuração do preço unitário para a combinação do produto e da configuração unitária na tabela de preços, então o preço unitário será predefinido para 0,00.|
| Custo Total | O custo calculado como custo unitário de quantidade \*.| O valor de custo é sempre mostrado na moeda de custo do projeto. |
| Total de Vendas | O valor de vendas calculado como preço unitário de quantidade \*. | O valor de vendas é sempre mostrado na moeda de vendas do projeto. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]