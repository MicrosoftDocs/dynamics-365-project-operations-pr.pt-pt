---
title: Descrição geral das aprovações
description: Este tópico fornece informação sobre como trabalhar com aprovações no Project Operations.
author: stsporen
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 37994422e9146765076fdbb77f5c763b4f1d0802
ms.sourcegitcommit: 2cf93d8bf0be5b61a739195a41334c34d910e9ba
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961180"
---
# <a name="approvals-overview"></a>Descrição geral das aprovações

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

As submissões de Tempo e Despesa passam por um fluxo de trabalho de aprovação. Após a aprovação das entradas, as transações são registadas em valores reais ou o tempo é reservado na agenda.

## <a name="approvals-workflow"></a>Fluxo de trabalho de aprovações
Quando cria e envia uma entrada de hora ou despesa, é criada uma entrada de aprovação. O Aprovador do projeto ou o seu gestor analisa e aprova a sua entrada. Se a entrada estiver relacionada com um projeto, quando for aprovada, serão criados os valores reais. Isto permite monitorizar o custo e a faturação. 

## <a name="approve-an-entry"></a>Aprovar uma entrada
O formulário **Aprovações** permite-lhe alternar entre diferentes vistas para poder ver os diferentes tipos de aprovação.
  
1. Vá para o formulário **Aprovações** e selecione **Despesas**, **Tempo** ou **Recuperações**.
2. Reveja cada aprovação e selecione as que pretende aprovar.
3. Selecione **Aprovar** para aprovar as entradas selecionadas.
O sistema processará estas entradas e criará os valores reais ou uma reserva.

## <a name="reject-an-entry"></a>Rejeitar uma entrada
Como Aprovador do projeto, poderá ter de enviar uma entrada de volta para um utilizador para correção.
  
1. Vá para o formulário **Aprovações** e selecione a entrada a rejeitar. 
2. Selecione **Rejeitar**.
3. Opcional - Adicione um comentário na caixa de diálogo **Comentários de Rejeição** para informar o utilizador por que motivo a entrada está a ser rejeitada.
4. Selecione **OK**. A entrada será devolvida ao utilizador.
  
## <a name="recall-entries"></a>Recuperar entradas
A dada altura, poderá ter de recuperar uma entrada submetida. Se a entrada não tiver sido aprovada, será devolvida imediatamente. No entanto, uma entrada aprovada pode ter um impacto material. O Aprovador do projeto tem de aprovar a recuperação para reverter a transação em Valores Reais.

## <a name="specify-project-approvers"></a>Especificar Aprovadores do projeto
Cada projeto tem vários membros da equipa do projeto. Pode especificar os membros da equipa que também são Aprovadores do projeto.

1. Vá para o formulário **Projetos** e abra o projeto a partir da lista.
2. No separador **Equipa**, selecione o membro da equipa que será Aprovador do projeto e, em seguida, selecione **Editar**.
3. Defina o campo **Aprovador do Projeto** como **Sim**.
4. Selecione **Guardar**.
5. Repita os passos 2 a 4 para adicionar Aprovadores do projeto adicionais.

## <a name="configure-the-users-manager"></a>Configurar o gestor do utilizador

1. Aceda a **Definições** > **Segurança** > **Utilizadores**.
2. Selecione o utilizador a quem está a atribuir um gestor e, na área **Informações da Organização**, selecione o gestor a partir da lista. 
3. Selecione **Guardar**.


