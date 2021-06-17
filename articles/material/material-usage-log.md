---
title: Registar a utilização do material em projetos e tarefas de projeto
description: Esta tópico fornece informações sobre como registar o uso do material contra projetos e tarefas de projeto.
author: rumant
ms.date: 03/31/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3c739d7fabb96a845eaf139fcc9eab21247b0860
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001575"
---
# <a name="record-material-usage-on-projects-and-project-tasks"></a>Registar a utilização do material em projetos e tarefas de projeto

_**Aplica-se a:** Project Operations para cenários baseados em recursos/não armazenados, implementação leve - negócio para faturação pró-forma_

À medida que uma equipa de projeto trabalha através de tarefas num projeto, consomem ou usam materiais. Um registo de utilização de material fornece uma forma de registar esta utilização para que possa ser aprovado pelo gestor do projeto e eventualmente faturado ao cliente. 

Para registar a utilização de materiais de catálogo ou de inscrição e os submeter ao aprovador, siga estes passos: 

1. No painel de navegação, selecione **Utilização do Material** e, em seguida, selecione **Novo**.
2. Na página **Utilização de novo material**, insira as informações de utilização do material necessárias e, em seguida, selecione **Guardar**.

A tabela seguinte fornece informações sobre os campos na página **Registo de utilização de material**. 

| **Campo** | **Descrição** | **Impacto a jusante** |
| --- | --- | --- |
| Descrição | Uma descrição do uso específico do material. | Este campo não tem impacto a jusante. |
| Data | A data na qual se prevê utilizar o material. | Este campo não tem impacto a jusante. |
| Project | Uma lista de projetos que estão ativos. | A seleção de um projeto para um registo de utilização de material tem impacto no campo **Tarefa** para mostrar apenas as tarefas que estão no projeto. |
| Tarefa | Uma lista de tarefas para o projeto, incluindo tarefas de resumo e nó de folha. | A seleção de uma tarefa para um registo de utilização de material afeta o custo real do material e as vendas reais de material para uma tarefa. Se este campo ficar vazio, o correspondente custo e vendas de utilização de material é rastreado e resumido apenas ao nível do projeto. |
| Selecionar Produto | Especificar se esta utilização de material é para um produto (catálogo) **Existente** ou para um produto **Acrescentado manualmente**. | Este campo determina o tipo de produto. |
| Produto | O ID do produto do catálogo de produtos. Ao selecionar um ID do produto, o campo **Selecionar produto** é automaticamente atualizado para **Produto existente**. O ID é usado para obter os preços de custo e venda da lista de preços. | Este campo não tem impacto a jusante. |
| Descrição de produto acrescentado manualmente | Um campo de texto para acrescentar manualmente no nome do produto. Este campo está disponível quando seleciona **Acrescentado manualmente** produto no campo **Selecionar produto**.| Este campo não tem impacto a jusante. |
| Recurso Reservável| Recurso que usou este material no projeto. O padrão para este campo é o recurso reservado do utilizador registado, mas pode ser alterado para gravar o uso em nome de outros membros da equipa do projeto. | Este campo não tem impacto a jusante. |
| Grupo de unidades | O valor predefinido neste campo provém do grupo de unidade que é configurado como padrão no produto de catálogo. Pode atualizar este campo para selecionar outro grupo de unidades. | Este campo não tem impacto a jusante. |
| Unidade | O valor predefinido neste campo é a unidade padrão do produto selecionado. Pode atualizar este campo para selecionar outra unidade. | A alteração da unidade resulta num preço e custo unitário diferentes. |
| Quantidade | A quantidade do produto que foi utilizado no projeto ou na tarefa do projeto. | Este campo não tem impacto a jusante. |
| Custo Unitário | O custo unitário do produto selecionado e da combinação unitária, tal como estabelecido na tabela de preços de custos aplicáveis. | O custo unitário é sempre mostrado na moeda de custo do projeto. Se não houver um custo unitário para a combinação do produto e da unidade na lista de preços, o custo unitário será predefinido para 0,00. |
| Custo Total | O custo calculado como custo unitário de quantidade \*.| O valor de custo é sempre mostrado na moeda de custo do projeto. |


## <a name="submit-material-usage-for-review-and-approval"></a>Submeter a utilização do material para revisão e aprovação 
Depois de capturar todo o seu uso do material e estiver pronto para o aprovar, deve submeter as informações de utilização para revisão.

1. Ir a **Registo de Utilização de Material** e selecionar uma ou mais entradas. Ou, selecione todos os registos de utilização do material utilizando a caixa de verificação no cabeçalho.
2. Selecione **Submeter**. O sistema processa as entradas selecionadas e, em seguida, cria pedidos de aprovação de utilização do material.

## <a name="recall-a-material-usage-log"></a>Recuperar um registo de utilização de material

Quando necessário, pode recuperar uma utilização do material submetida. O tempo necessário para recuperar uma entrada de utilização do material depende da fase de aprovação.  Se o aprovador ainda não tiver aprovado a entrada, a recuperação poderá ocorrer imediatamente. No entanto, se a entrada já tiver sido aprovada, é pedido ao aprovador para aprovar a recuperação e reverter as transações.

1. Aceda a **Utilização de material** e, na lista de registos de utilização de materiais, selecione a utilização do material para recuperar.
2. Selecione **Recuperar**. Se a entrada de utilização do material ainda não tiver sido aprovada, o sistema recupera-a imediatamente. Se a entrada do material já tiver sido aprovada, é criado um pedido de retirada para notificar o aprovador de que pretende recuperar a utilização do material. Em seguida, o aprovador confirmará que a reversão pode ser feita e a entrada será devolvida.

## <a name="delete-a-material-usage-log"></a>Eliminar um registo de utilização de material

Pode eliminar registos de utilização de materiais que não tenham sido submetidos. Para eliminar um registo de utilização de material que já tenha sido submetido, deve primeiro recuperá-lo.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
