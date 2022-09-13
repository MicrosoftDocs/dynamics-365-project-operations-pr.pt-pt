---
title: Ativar e rever uma proposta de projeto
description: Este artigo fornece informações sobre a ativação e revisão de proporstas no Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e71102078832ac7d5f8e5edb40cc484df927eda4
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410351"
---
# <a name="activate-and-revise-a-project-quote"></a>Ativar e rever uma proposta de projeto

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

As capacidades de ativação e revisão ajudam-no a monitorizar o controlo de versões das cotações baseadas em projetos durante as fases de estimativa e de negociação. Quando um rascunho de uma proposta é ativado, passa a ser só de leitura.

As capacidades de ativação e revisão permitem-lhe executar as seguintes tarefas:

- Ganhar ou perder cotações apenas após a ativação.
- Reveja uma proposta para fazer alterações à proposta existente ou para criar uma nova versão.

> [!NOTE]
> Depois de a funcionalidade de ativação e revisão de propostas estar ativada, não pode ser desativada.

Para ativar a funcionalidade de ativar e rever cotações baseadas em projetos, siga estes passos.

1. Aceda a **Definições** \> **Parâmetros**.
1. Abra o registo **Parâmetros**.
1. No Painel de ativação, no separador **Controlo de funcionalidades**, selecione **Ativar a ativação e revisão de propostas**.
1. Na caixa de diálogo de confirmação, selecione **OK**.
1. Depois de alguns minutos, atualize o browser. As capacidades de ativação e revisão deverão estar agora disponíveis. Ficará a saber que estas capacidades foram ativadas se o botão **Ativar a ativação e revisão para propostas** deixar de aparecer no Painel de Ação.

## <a name="activating-a-quote"></a>Ativação de uma proposta

Depois de a funcionalidade de ativação e revisão de propostas estar ativada, os botões **Fechar proposta como ganha** e **Fechar proposta como perdida** no Painel de Ação não estão disponíveis para rascunhos de propostas do projeto. Só estão disponíveis depois de uma proposta ser ativada.

A ativação representa a fase no processo de proposta em que pretende impedir mais alterações à proposta. Nesta fase, a proposta é enviada para revisão interna ou para o cliente.

Os botões **Fechar proposta como ganha** e **Fechar proposta como perdida** no Painel de Ação está disponível para propostas ativadas. Dependendo do resultado da revisão interna ou do cliente, pode utilizar um destes botões para fechar uma proposta activada. Pode fazer negociações e alterações nas ropostas ativadas selecionando **Rever proposta**.

## <a name="revising-a-quote"></a>Rever uma proposta

Se tiver de efetuar alterações a uma proposta ativada, selecione **Rever proposta**. A proposta é fechada e o código de razão **revisto** é utilizado. É criada uma nova proposta com o mesmo ID e um número de revisão incrementado. Todos os detalhes da proposta original são copiados para a nova proposta. A nova proposta está em estado de rascunho e pode ser editada conforme necessário.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
