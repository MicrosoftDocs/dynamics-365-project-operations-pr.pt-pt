---
title: Ajustes ao projeto
description: Este artigo fornece informações sobre os ajustes ao projeto.
author: ryansandness
ms.date: 11/09/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: 52a262adce2bb624bc088e50858e25824f845e5c
ms.sourcegitcommit: bb03ac64e01112c93bb24035a51653a0a88cd5fc
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 11/18/2022
ms.locfileid: "9788307"
---
# <a name="project-adjustments"></a>Ajustes ao projeto

_**Aplica-se a:** Project Operations para cenários baseados em Stock/Produção_

## <a name="adjustments-overview"></a>Descrição geral dos ajustes

Pode configurar o Microsoft Dynamics 365 Project Operations para que os utilizadores possam efetuar alterações a transações publicadas. Pode ajustar as transações de projetos individualmente ou pode selecionar várias transações de cada vez numa lista de todas as transações de projetos. Os ajustes ao projeto são utilizados, por exemplo, para atualizar em massa o estado faturável, recalcular o custo após uma alteração de configuração ou atualizar as fontes de financiamento.

Os utilizadores podem aceder à funcionalidade de ajustes ao projeto de várias formas:

- Utilizando a página **Ajustar transações** que pode ser acedida a partir da **Gestão de Projetos e de contabilidade** \> **Configuração**.
- Utilizando o botão **Ajustes** na página **Transações de projeto publicadas** que pode ser acedida a partir de **Gestão de Projetos e de contabilidade** \> **Transações**.
- Utilizando o botão **Ajustes** na página **Transações de projeto publicadas** no contexto de um projeto. Esta página pode ser acedida a partir de **Gestão de Projetos e de contabilidade** \> **Todos os projetos**.

Para permitir ajustes, tem de ativar um ou mais estados de transação a partir da **Gestão de Projetos e de contabilidade** \> **Parâmetros da gestão de projetos e de contabilidade** no separador **Geral**, na secção **Permitir ajustes ao estado da transação**. Exemplos de estados de transações incluem transações publicadas, transações faturadas ou transações eliminadas. Qualquer estado de transações que esteja definido como **Não** terá transações nesse estado que não aparecerão no processo de ajuste como selecionáveis para ajuste.

Atualmente, está disponível uma opção de configuração denominada **Criar sempre transação de ajuste** nos Parâmetros de gestão de projetos e de contabilidade. Pode desativar esta opção para atualizar a transação original, em vez de criar novas transações durante o ajuste num subconjunto de cenários. Foi anunciado que este parâmetro será preterido até 1 de março de 2023. Depois de 1 de março de 2023, o sistema irá sempre comportar-se como se a opção estivesse ativada.

## <a name="adjustments-process-flow"></a>Fluxo do processo de ajustes

Os seguintes passos mostram o fluxo típico para os ajustes de processamento.

1. Abra a página **Ajustes do projeto**.
2. Selecione **Selecionar** para pesquisar por transações que cumprem os critérios esperados para ajuste.
3. Na lista de transações, selecione todas as transações ou um subconjunto das transações para ajuste.
4. Selecione **Ajustar** e modifique os atributos na linha. Em alternativa, se os valores foram especificados manualmente durante a entrada da transação, pode optar por introduzir valores de sistema predefinidos.
5. A lista de transações é obtida e uma marca de verificação aparece na coluna **Ajuste pendente** para indicar onde as alterações foram efetuadas. Quaisquer ajustes que tenham alterações pendentes são mostrados na metade inferior da página. Nessa página, poderá efetuar alterações detalhadas adicionais, para além do que foi mostrado na página anterior.
6. Selecione **Publicar** para publicar as transações de ajuste.

Dependendo da configuração, normalmente, são criadas novas transações para o ajuste.

- O campo **Estado da Fatura** da transação original está definido como **Ajustado**.
- É criada uma transação de estorno para estornar a transação original e o campo **Estado** está definido como **Ajustado**.
- É criada uma nova transação que tem as alterações que foram efetuadas durante o processo de ajustes.

### <a name="selecting-multiple-posted-project-transactions-at-a-time-for-adjustments-and-credit-notes"></a>Selecionar várias transações de projeto publicadas de uma vez para ajustes e notas de crédito

Uma nova caraterística que foi introduzida na versão 10.0.30 permite a seleção de várias transações para ajustes de uma vez a partir da página **Transações do projeto publicadas**.

Antes de poder utilizar esta caraterística, tem de ser ativada no sistema. Os admins podem utilizar a área de trabalho **Gestão de caraterísticas** para verificar o estado da caraterística e ativá-la, se necessário. Na área de trabalho **Gestão de caraterísticas**, pesquise por e selecione **Seleção múltipla de transações do projeto publicadas para ajustes e notas de créditos** e, em seguida, selecione **Ativar agora**.

Esta caraterística permite a seguinte funcionalidade-chave:

- Pode ser acedido a partir da página da transação publicada num projeto utilizando o botão **Ajuste** existente.
- Permite um controlo de seleção de múltiplas linhas na página **Transações do projeto publicadas**. Pode aplicar filtros à página de lista e selecionar os registos antes de começar os ajustes.
- Desativa o botão **Ajuste** se não for possível ajustar uma única transação ou se selecionar uma combinação de notas de crédito e diários, em vez de individualmente.
- Devido à adição do controlo de seleção de múltiplas linhas, a ligação **Custo aprovado** no friso deixa de ser desativado se forem selecionadas múltiplas linhas.
- Adicionar a seguinte mensagem de aviso: "Selecionou mais do que (número selecionado) registos para ajuste. Continuar com esta ação poderá demorar algum tempo. Tem a certeza de que pretende prosseguir com esta ação?"

Esta caraterística também remove o passo 2 do fluxo do processo descrito anteriormente neste artigo. Consequentemente, quaisquer transações que foram selecionadas antes da página **Ajustar transações** ter sido aberta serão incluídas na lista de transações para ajuste. Não precisa de utilizar o botão **Selecionar** para pesquisar por elas.

> [!NOTE] 
> Mesmo que esta caraterística esteja desativada, pode selecionar múltiplos registos para ajuste. No entanto, só um registo *permanecerá selecionado* e a caixa de diálogo **Selecionar transações** aparecerá imediatamente depois de selecionar abrir ajustes.

## <a name="adjustment-transaction-statuses-that-can-be-enabled-or-disabled-for-adjustments"></a>Estados da transação de ajustes que podem ser ativados ou desativados para ajustes

Os seguintes estados podem ser ativados ou desativados no separador **Geral** da página **Parâmetros de gestão de projetos e de contabilidade**:

- Publicada
- Proposta de Fatura
- Faturado
- Estimado
- Eliminado
- Saldo inicial (hora)

## <a name="adjustment-parameters"></a>Parâmetros de ajuste

Estes parâmetros estão listados na página **Parâmetros de gestão de projetos e de contabilidade** no separador **Geral**, sob o grupo **Ajuste** e irá modificar o comportamento do modo como os ajustes são processados. 

| Nome do parâmetro | Description |
|----------------|-------------
| Criar sempre uma transação de ajuste | Se este parâmetro estiver ativado, o processo de ajuste irá sempre criar uma nova transação de estorno e nova transação ajustada quando houver um impacto financeiro ou de relatório. Se o parâmetro estiver desativado, o processo de ajuste irá atualizar a transação original, em vez de criar uma transação de estorno e nova para um cenário, como, por exemplo, uma atualização do texto da transação. |
| Atualizar automaticamente o campo | Se este parâmetro estiver ativado, o sistema irá recalcular o preço de custo e o preço de venda. |
| Utilizar a data de ajuste como novo projeto | Este parâmetro é utilizado para mover transações para período fiscal futuro antes de o sistema suportar esta função. Não recomendamos que o utilize porque altera a data de negócio da transação e será preterido numa versão futura. |
| Permitir atividades fechadas | Normalmente, não é possível criar transações para atividades fechadas. Se este parâmetro estiver ativado, esse comportamento é substituído. Por conseguinte, é possível criar ajustes para atividades fechadas. |
