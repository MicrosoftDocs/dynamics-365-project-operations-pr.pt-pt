---
title: Conjuntos de aprovações
description: Este artigo explica como trabalhar com conjuntos de aprovações, pedidos e os subconjuntos dessas operações.
author: stsporen
ms.date: 02/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: ca205073edbce2b399aab3ae273d635c8af96765
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 09/16/2022
ms.locfileid: "9524931"
---
# <a name="approval-sets"></a>Conjuntos de aprovações

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

Os conjuntos de aprovações agrupam os pedidos de aprovação em subconjuntos de operações mais pequenos. Este agrupamento permite que as aprovações sejam processadas por projeto, numa ordem específica, e permite repetições e sequenciações. O agrupamento de pedidos de aprovação melhora a fiabilidade e a rastreabilidade do processamento de aprovações no caso de grandes volumes de aprovações.

Os conjuntos de aprovações indicam o estado geral de processamento dos seus registos relacionados. Quando um registo de aprovação é processado utilizando um conjunto de aprovações, o registo muda de **Submetido** para **Aprovado** e deixa de estar associado ao conjunto de aprovações. Se um registo falhar quando for submetido a aprovação, o registo permanece num estado de **Submetido** e o conjunto de aprovação é marcado como falhado. O conjunto de aprovação regista a mensagem de erro da falha.

## <a name="processing-approvals-and-approval-sets"></a>Processamento de aprovações e conjuntos de aprovações
As aprovações que estão em fila para processamento são visíveis na vista **Processamento de Aprovações**. O sistema processa todas as entradas várias vezes de forma assíncrona, incluindo a repetição de uma aprovação se as tentativas anteriores falharem.

O campo **Duração do Conjunto de Aprovação** regista o número de tentativas restantes para processar o conjunto antes de ser marcado como falhado.

Os conjuntos de aprovações são processados através da ativação periódica com base num **Fluxo de cloud** nomeado **Project Service - Agendar periodicamente conjuntos de aprovações do projeto**. Isto pode ser encontrado na **Solução** denominada **Project Operations**. 

Certifique-se de que o fluxo está ativado concluindo os seguintes passos.

1. Como administrador, inicie sessão em [flow.microsoft.com](https://powerautomate.microsoft.com).
2. No canto superior direito, mude para o ambiente que utiliza para o Dynamics 365 Project Operations.
3. Selecione **Soluções** para listar as soluções que estão instaladas no ambiente.
4. Na lista de soluções, selecione **Project Operations**.
5. Altere o filtro de **Todos** para **Fluxos de cloud**.
6. Verifique se o fluxo **Project Service - Agendar periodicamente conjuntos de aprovações do projeto** está definido como **Ativado**. Se não estiver, selecione o fluxo e, em seguida, selecione **Ligar**.
7. Verifique se o processamento ocorre de cinco em cinco minutos, revendo a lista de **Tarefas de sistema** na área **Definições** no ambiente Project Operations Dataverse.

## <a name="failed-approvals-and-approval-sets"></a>Aprovações e conjuntos de aprovações falhados
A vista **Aprovações Com Falhas** lista todas as aprovações que necessitam de intervenção do utilizador. Abra os registos de conjunto de aprovação associados para identificar a causa da falha.
A seleção de **Repetir** adiciona à contagem de duração do conjunto de aprovação, move o conjunto de aprovação para um estado de **Processamento** e tenta processar os registos restantes.

## <a name="configure-approval-sets"></a>Configurar conjuntos de aprovação

### <a name="enable-the-approval-sets-feature"></a>Ativar a funcionalidade Conjuntos de aprovação
Antes de ativar a funcionalidade de Conjuntos de aprovação, verifique se não existem aprovações atualmente em processamento. Depois de esta caraterística ser ativada, não pode ser desativada.

- Aceda à página **Parâmetros do projeto** e selecione **Controlo de Funcionalidades** > **Ativar Aprovações Modernas**.

### <a name="configuring-the-asynchronous-threshold"></a>Configurar o limiar assíncrono 
Quando os conjuntos de aprovação são criados, o processamento move-se para segundo plano quando o número selecionado de registos de aprovação excede o limiar indicado. Utilize o campo **Limiar Assíncrono** para configurar quando o processamento de aprovação deve ser executado de forma síncrona ou assíncrona. Selecione um dos seguintes valores:

  - Zero: Todos os pedidos devem ser processados assincronamente. 
  - Números superiores a zero: As aprovações são processadas assincronamente apenas quando o número de aprovações submetidas excede este valor.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
