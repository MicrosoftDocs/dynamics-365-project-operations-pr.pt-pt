---
title: Mapear projetos e tarefas para um item de contrato baseado em projetos – lite
description: Este tópico fornece informações sobre a adição e remoção de projetos e tarefas a um item de contrato.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4b86e03192625b0dabb89080f2ade1ed9e3567cf
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994646"
---
# <a name="map-projects-and-tasks-to-a-project-based-contract-line"></a>Mapear projetos e tarefas para um item de contrato baseado no projeto 

_**Aplica-se a:** Implementação leve - negociar à faturação pró-forma, Project Operations para cenários baseados em recursos/não armazenados_

Nos itens de contrato baseados em projetos, pode mapear tarefas específicas num projeto para o item de contrato.

Quando mapear tarefas específicas para um item de contrato, o método de faturação, opções de cobrança, limites A não exceder, e os clientes definidos no item de contrato serão aplicáveis apenas a essas tarefas específicas.

Se tiver um cenário em que uma fase de um projeto, por exemplo a Fase Protótipo, é de preço fixo e todas as outras fases são de tempo e material, poderá associar a fase Protótipo e todas as tarefas subordinadas associadas ao item de contrato para essa fase com um método de faturação de preço fixo.

Todas as outras fases da estrutura hierárquica do trabalho (WBS) do projeto podem ser associadas ao item de contrato baseado em tempo e material.

## <a name="associate-tasks-to-project-based-contract-lines"></a>Associar tarefas a itens de contrato baseadas em projetos

As tarefas podem ser associadas a itens de contrato a partir do separador **Tarefas Faturáveis** na página **Item de Contrato** ou do separador **Faturação de Tarefas** na página **Projeto**.

### <a name="from-the-contract-line-page"></a>A partir da página Item de contrato

Complete os seguintes passos para associar tarefas do projeto ao item de contrato a partir do separador **Tarefas Faturáveis** da página **Item de Contrato**.

1. No separador **Geral** de um item de contrato baseado em projetos, verifique se o campo **Projeto** está preenchido.
2. No campo **Tarefas Incluídas**, selecione **Apenas Tarefas Selecionadas**.
3. Guardar as suas alterações. O formulário irá atualizar e o separador **Tarefas Faturáveis** estará visível.
4. Selecione o separador **Tarefas Faturáveis** e, na subgrelha, selecione **Adicionar uma Tarefa de Item de Contrato**.
5. Na página **Tarefas do Item de Contrato**, no menu pendente **Tarefas**, selecione a tarefa. 
6. Introduza informações no campo **Tipo de Faturação** e, em seguida, selecione **Guardar e Fechar**. A tarefa selecionada é associada ao item de contrato.

> [!NOTE]
> Esta não é a experiência mais ideal para associar tarefas de projetos a itens de contrato. Cada projeto terá de ser associado manualmente nesta experiência. A forma preferida é a partir do separador **Faturação de Tarefas** na página **Projeto**.

### <a name="from-the-project-page"></a>A partir da página do projeto

Este é o método ideal para associar tarefas a itens de contrato. Pode selecionar várias tarefas e associá-las todas e as suas tarefas subordinadas para o item de contrato selecionado. Complete os seguintes passos para associar tarefas ao item de contrato a partir da página **Projeto**.

1. No separador **Geral** de um item de contrato baseado em projetos, verifique se o campo **Projeto** está preenchido.
2. No campo **Tarefas Incluídas**, selecione **Apenas Tarefas Selecionadas**.
3. Guarde o item de contrato baseado em projetos. O formulário irá atualizar e o separador **Tarefas Faturáveis** estará visível. Isto é apenas para efeitos de verificação.
4. No separador **Geral** do item de contrato baseado em projetos, no campo **Projeto**, selecione a ligação para o projeto.
5. Na página **Projeto**, selecione o separador **Configuração da Faturação de Tarefas**.
6. Existem duas grelhas. Uma grelha é para itens de contrato que se aplicam a todo o projeto. A segunda grelha aplica-se à configuração de faturação específica de tarefas. Na segunda grelha, selecione uma ou mais tarefas e, em seguida, selecione **Associar Itens de Contrato**.
7. Na página de diálogo que abre, selecione um item de contrato a partir do menu pendente.
8. Utilize o menu pendente **Tipo de Faturação** para marcar as tarefas como faturáveis ou não faturáveis.
9. Selecione a caixa de verificação para indicar se a associação também deve incluir tarefas subordinadas das tarefas selecionadas. A verificação da caixa também associará as tarefas subordinadas das tarefas selecionadas para o item de contrato.
10. Selecione **OK** para fechar a caixa de diálogo.

## <a name="unassociate-tasks-from-project-based-contract-lines"></a>Desassociar tarefas de itens de contrato baseadas em projetos

### <a name="from-the-contract-line-page"></a>A partir da página item de contrato

Complete os seguintes passos para desassociar tarefas do projeto ao item de contrato no separador **Tarefas Faturáveis** da página **Item de Contrato**.

1. No separador **Tarefas Faturáveis**, selecione **Eliminar uma Tarefa de Item de Contrato**.
2. Uma mensagem de aviso indica que remover esta associação pode resultar na inversão de quaisquer valores reais previamente registados na tarefa. Selecione **OK** no diálogo para remover a associação entre a tarefa e o item de contrato baseado em projetos. 

> [!NOTE]
> Isto não elimina a tarefa do projeto. Em vez disso, remove a associação de tarefas do item de contrato baseado em projetos.

### <a name="from-the-project-page"></a>A partir da página do projeto

Esta é a experiência mais ideal para desassociar tarefas de itens de contrato. Pode selecionar várias tarefas e desassociá-las todas e as suas tarefas subordinadas do item de contrato selecionado. Complete os seguintes passos para desassociar tarefas do item de contrato.

1. Do separador **Geral** do item de contrato baseado em projetos, no campo **Projeto**, clique na ligação para o projeto.
2. Na página **Projeto**, selecione o separador **Configuração da Faturação de Tarefas**.
3. Há duas grelhas na página. Uma grelha destina-se a itens de contrato que se aplicam a todo o projeto e a segunda aplica-se à configuração de faturação específica de tarefas. Na segunda grelha, selecione uma ou mais tarefas e, em seguida, selecione **Desassociar Itens de Contrato**.
4. Na página de diálogo que abre, selecione um item de contrato a partir do menu pendente.
5. Selecione a caixa de verificação para indicar se a associação também deve ser removida de quaisquer tarefas subordinadas das tarefas selecionadas. A verificação da caixa também desassociará as tarefas subordinadas das tarefas selecionadas do item de contrato.
6. Selecione **OK**. Uma mensagem de aviso indica que remover esta associação pode resultar na inversão de quaisquer valores reais previamente registados na tarefa. Selecione **OK** no diálogo de aviso para remover a associação entre a tarefa e o item de contrato baseado em projetos.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
