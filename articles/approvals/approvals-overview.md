---
title: Descrição geral das aprovações
description: Este tópico fornece informação sobre como trabalhar com aprovações no Project Operations.
author: stsporen
ms.date: 03/31/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 5e30b8a386805faee869f77e695d5ee492d78cdb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996715"
---
# <a name="approvals-overview"></a>Descrição geral das aprovações

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

O tempo, as despesas e as submissões de utilização do material passam por um fluxo de trabalho de aprovação. Após a aprovação das entradas, as transações são registadas em valores reais ou o tempo é reservado na agenda.

## <a name="approvals-workflow"></a>Fluxo de trabalho de aprovações
Quando cria e envia uma entrada de tempo, despesa ou utilização material, é criado um registo de aprovação. O aprovador ou gestor do projeto analisa e aprova a entrada. Se a entrada estiver relacionada com um projeto, os valores reais serão criados quando for aprovado. Isto permite monitorizar o custo e a faturação.

## <a name="approve-an-entry"></a>Aprovar uma entrada
A página **Aprovações** permite-lhe alternar entre diferentes pontos de vista para que possa ver os diferentes tipos de aprovações.
  
1. Aceda à página **Aprovações** e selecione **Despesas**, **Tempo**, **Utilização do Material** ou **Recordações**.
2. Reveja cada aprovação e selecione as que pretende aprovar.
3. Selecione **Aprovar** para aprovar as entradas selecionadas.
O sistema processa estas entradas e cria valores reais.

## <a name="reject-an-entry"></a>Rejeitar uma entrada
Como Aprovador do projeto, poderá ter de enviar uma entrada de volta para um utilizador para correção.
  
1. Vá à página **Aprovações** e selecione a entrada a rejeitar. 
2. Selecione **Rejeitar**.
3. Opcional, adicione um comentário na caixa de diálogo **Comentários de rejeição** para informar o utilizador porque é que a entrada está a ser rejeitada.
4. Selecione **OK**. A entrada será devolvida ao utilizador.
  
## <a name="cancel-approval"></a>Cancelar a aprovação
Nalguns casos, poderá ter de cancelar uma entrada previamente aprovada. O cancelamento de uma entrada previamente aprovada terá um impacto financeiro. 

## <a name="approving-recall-requests"></a>Aprovar pedidos de recuperação
Nalguns casos, um consultor pode precisar de recuperar uma entrada previamente aprovada. O cancelamento de uma entrada previamente aprovada terá um impacto financeiro. O aprovador do projeto é obrigado a aprovar a retirada para inverter a transação em Valores reais.

## <a name="specify-project-approvers"></a>Especificar Aprovadores do projeto
Cada projeto tem vários membros da equipa do projeto. Pode especificar os membros da equipa que também são Aprovadores do projeto.

1. Vá à página **Projetos** e abra o projeto a partir da lista.
2. No separador **Equipa**, selecione o membro da equipa que será Aprovador do projeto e, em seguida, selecione **Editar**.
3. Defina o campo **Aprovador do Projeto** como **Sim**.
4. Selecione **Guardar**.
5. Repita os passos 2 a 4 para adicionar Aprovadores do projeto adicionais.

## <a name="configure-the-users-manager"></a>Configurar o gestor do utilizador

1. Aceda a **Definições** > **Segurança** > **Utilizadores**.
2. Selecione o utilizador a quem está a atribuir um gestor e, na área **Informações da Organização**, selecione o gestor a partir da lista. 
3. Selecione **Guardar**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
