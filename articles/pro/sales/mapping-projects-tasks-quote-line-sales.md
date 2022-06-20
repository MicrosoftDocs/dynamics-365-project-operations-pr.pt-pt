---
title: Mapear projetos e tarefas para uma linha de proposta baseada no projeto
description: Este artigo fornece informações sobre como mapear projetos e tarefas para uma linha de tarefas baseada em projetos.
author: rumant
ms.date: 10/05/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 8971a334bd19f0ef106f88034a1abbb3c338de22
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917176"
---
# <a name="map-projects-and-tasks-to-a-project-based-quote-line"></a>Mapear projetos e tarefas para uma linha de proposta baseada no projeto

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

Nas linhas de proposta baseadas em projetos, pode mapear as tarefas específicas de um projeto que já esteja associado a uma linha de proposta.

Quando mapeia tarefas para uma linha de proposta, os seguintes itens que definiu na linha de proposta aplicar-se-ão apenas a essas tarefas:

- Método de faturação
- Opções de exigibilidade
- Limites a não exceder
- Clientes

Por exemplo, pode ter um projeto onde uma fase é com preço fixo e todas as outras fases são tempo e materiais. Neste caso, pode associar a primeira fase, e todas as suas tarefas subordinadas, à linha de proposta para essa fase com um método de faturação de preço fixo. Em seguida, pode associar todas as outras fases à linha de proposta baseada em tempo e materiais.

## <a name="associate-tasks-to-project-based-quote-lines"></a>Associar tarefas a linhas de proposta baseadas em projetos

Pode associar tarefas a linhas de proposta a partir das seguintes localizações:

- Página **Projeto** > **Faturação de tarefas** tab (ideal)
- Página **Linha de Proposta** > separador **Tarefas Faturáveis** 

### <a name="from-the-project-page"></a>A partir da página Projeto

A página **Projeto** proporciona a experiência ideal para associar tarefas a linhas de proposta. Pode utilizar esta página para selecionar várias tarefas e associar todas, bem com as respetivas tarefas subordinadas, à linha de proposta selecionada.

1. No separador **Geral** de uma linha de proposta baseada em projetos, verifique se o campo **Projeto** está preenchido.
2. No campo **Tarefas incluídas**, selecione **Apenas tarefas selecionadas**.
3. Guarde a linha de proposta baseada em projetos. Quando o formulário é atualizado, é apresentado o separador **Tarefas Faturáveis**.
4. No separador **Geral**, selecione a ligação para o projeto a partir do campo **Projeto**.
5. Na página **Projeto**, selecione o separador **Faturação de Tarefas**.
6. Na segunda grelha, que se aplica à configuração da faturação específica da tarefa, selecione uma ou mais tarefas e, em seguida, selecione **Associar linhas de proposta**.
7. Na página de diálogo apresentada, selecione uma linha de proposta que apresente linhas de proposta baseadas em projetos na proposta.
8. No campo **Tipo de faturação**, indique se estas tarefas são faturáveis ou não faturáveis.
9. Selecione a caixa de verificação para indicar se a associação deve incluir as tarefas subordinadas das tarefas selecionadas. Selecionar a caixa irá associar as tarefas subordinadas das tarefas selecionadas à linha de proposta.
10. Selecione **OK** para fechar a caixa de diálogo.

### <a name="from-the-quote-line-page"></a>A partir da página Linha de proposta

Pode associar tarefas de projeto a linhas de proposta a partir do separador **Tarefas Faturáveis** na página **Linha de proposta**.

>[!NOTE]
>O local ideal para associar tarefas de projeto a linhas de proposta é o separador **Faturação de tarefas** na página **Projeto**. Se associar tarefas a partir do separador **Tarefas Faturáveis** na página **Linha de proposta**, tem de associar manualmente cada projeto.

1. No separador **Geral** de uma linha de proposta baseada em projetos, verifique se existe um projeto selecionado no campo **Projeto**.
2. No campo **Tarefas incluídas**, selecione **Apenas tarefas selecionadas**.
3. Guarde a linha de proposta baseada em projetos. Quando o formulário é atualizado, é apresentado o separador **Tarefas Faturáveis**.
4. No separador **Tarefas Faturáveis**, selecione **Adicionar uma tarefa de linha de proposta**.
5. Na página **Tarefa da Linha de Proposta**, no campo **Tarefas**, selecione a tarefa e, no campo **Tipo de faturação**, selecione **Guardar**. 
6. Feche a página. A tarefa selecionada está agora associada à linha de proposta.

## <a name="disassociate-tasks-from-projectbased-quote-lines"></a>Desassociar tarefas a partir de linhas de proposta baseadas em projetos

### <a name="from-the-project-page"></a>A partir da página Projeto

Este método proporciona a melhor experiência para desassociar as tarefas das linhas de proposta. Pode selecionar várias tarefas e desassociar todas, bem com as respetivas tarefas subordinadas, da linha de proposta selecionada.

1. No separador **Geral** de uma linha de proposta baseada em projetos, no campo **Projeto**, selecione a ligação do projeto.
2. Na página **Projeto**, selecione o separador **Faturação de Tarefas**.
3. Na segunda grelha, que se aplica à configuração da faturação específica da tarefa, selecione uma ou mais tarefas e, em seguida, selecione **Desassociar linhas de proposta**.
4. Na página de diálogo apresentada, selecione uma linha de proposta.
5. Selecione a caixa de verificação para indicar se a associação também deve ser removida das tarefas subordinadas das tarefas selecionadas. Selecionar a caixa irá desassociar as tarefas subordinadas das tarefas selecionadas à linha de proposta.
6. Selecione **OK**. Uma mensagem de aviso informa-o de que, se remover esta associação, quaisquer valores reais registados anteriormente na tarefa poderão ser revertidos. 
7. Selecione **OK** para continuar e remover a associação entre a tarefa e a linha de proposta baseada em projetos.

### <a name="from-the-quote-line-page"></a>A partir da página Linha de proposta

Também pode desassociar tarefas de projeto de linhas de proposta a partir do separador **Tarefas Faturáveis** na página **Linha de proposta**.

1. No separador **Tarefas Faturáveis**, selecione **Eliminar uma tarefa de linha de proposta**.
2. Selecione **OK**. Uma mensagem de aviso informa-o de que, se remover esta associação, quaisquer valores reais registados anteriormente na tarefa poderão ser revertidos. 
3. Selecione **OK** para continuar e remover a associação entre a tarefa e a linha de proposta baseada em projetos.

>[!NOTE]
> Este procedimento não elimina a tarefa do projeto. Apenas remove a associação da tarefa da linha de proposta baseada em projetos.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]