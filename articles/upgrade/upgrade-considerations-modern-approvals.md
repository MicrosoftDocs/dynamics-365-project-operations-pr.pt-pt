---
title: Considerações de atualização para aprovações modernas
description: O tópico abrange os pontos que os administradores devem considerar quando ativarem a funcionalidade Aprovações Modernas.
author: stsporen
ms.date: 01/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: a3757f057a801318feccde9be3e49c7b40fa8fcb
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578400"
---
# <a name="upgrade-considerations-for-modern-approvals"></a>Considerações de atualização para aprovações modernas 

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

Como parte da Versão da Onda 1 de abril de 2022, a funcionalidade Aprovações Modernas será ativada por predefinição. Esta funcionalidade melhora a fiabilidade da lógica de aprovação e assegura que pode determinar a razão se a lógica de aprovação falhar.

Como parte desta alteração, as alterações de estado às aprovações do projeto estão atualizadas. Agora, o estado passa diretamente de **Submetido** a **Aprovado**. O estado **Pendente** já não é um estado para aprovações. Para determinar se a aprovação está pendente, verifique se a aprovação faz parte de um conjunto de aprovações e reveja o estado do conjunto de aprovações anexado.

## <a name="before-you-upgrade"></a>Antes de atualizar

Antes de atualizar para as Aprovações Modernas, certifique-se de que não tem aprovações pendentes. As Aprovações Modernas não utilizam o estado **Pendente**. Assim, quaisquer aprovações que ainda estão marcadas como **Pendentes** após a atualização não serão processadas.

## <a name="after-you-upgrade"></a>Depois de atualizar

Depois de atualizar para as Aprovações Modernas, um Administrador tem de validar que o fluxo de cloud que processa as aprovações foi ativado.

1. Iniciar sessão em [flow.microsoft.com](https://flow.microsoft.com)
2. No canto superior direito da página, altere o ambiente para o ambiente que atualizou.
3. Selecione **Soluções** para listar as soluções que estão instaladas no ambiente.
4. Na lista de soluções, selecione **Project Operations** ou **Project Service**.
5. Altere o filtro de **Todos** para **Fluxos de cloud**.
6. Verifique se a opção **Project Service - Agendar periodicamente conjuntos de aprovações do projeto** está definida como **Ativada**. Se não estiver, selecione o fluxo e, em seguida, selecione **Ligar**.
7. Verifique se o processamento está a ocorrer de cinco em cinco minutos, revendo a lista **Tarefas de sistema** na área **Definições**.

## <a name="short-term-rollback"></a>Reversão a curto prazo

Se não conseguir captar as alterações ou se encontrar um problema grave com esta funcionalidade, pode reverter temporariamente para o fluxo de aprovação original executando os seguintes passos:
1. Inicie sessão no seu ambiente e verifique se não existem aprovações pendentes.
2. Aceda a **Definições** > **Parâmetros do projeto**.
3. Selecione **Controlo de Funcionalidades** e, em seguida, selecione **Aprovações Modernas** para desativar a funcionalidade.

## <a name="removing-the-feature-flag"></a>Remover a sinalização de funcionalidades

Na atualização da Onda 2 de outubro de 2022, a capacidade de desativar esta funcionalidade será removida.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
