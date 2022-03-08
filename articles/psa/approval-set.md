---
title: Conjuntos de aprovações
description: Este tópico fornece informações sobre o conjunto de aprovações, os pedidos e os subconjuntos dessas operações.
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: e57944b3031ff8b6da163125bb6668875ae77bd06f23a5b8c4ef06f396210e4f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6995505"
---
# <a name="approval-sets"></a>Conjuntos de aprovações

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Os conjuntos de aprovações agrupam os pedidos de aprovação em subconjuntos de operações mais pequenos. Este agrupamento permite que as aprovações sejam processadas por ordem do Projeto e permite a repetição e sequenciação. O agrupamento melhora a fiabilidade e a rastreabilidade do processamento de aprovação para grandes volumes de aprovações.

Os conjuntos de aprovações indicam o estado geral de processamento dos seus registos relacionados. Quando um registo de aprovação é processado usando um conjunto de aprovação, o registo passa de **Submetido** a **Aprovado** e é desassociado do conjunto de aprovação. Se um registo falhar quando for submetido a aprovação, o registo permanece num estado de **Submetido** e o conjunto de aprovação é marcado como falhado. O conjunto de aprovação regista a mensagem de erro da falha.

## <a name="processing-approvals-and-approval-sets"></a>Processamento de aprovações e conjuntos de aprovações
As aprovações que estão em fila para processamento são visíveis na vista **Processamento de Aprovações**. O sistema tenta processar todas as entradas várias vezes assincronamente, incluindo repetir uma aprovação se as tentativas anteriores tiverem falhado.

O campo **Duração do Conjunto de Aprovação** regista o número de tentativas restantes para processar o conjunto antes de ser marcado como falhado.

## <a name="failed-approvals-and-approval-sets"></a>Aprovações e conjuntos de aprovações falhados
A vista **Aprovações Falhadas** lista todas as aprovações que requerem intervenção do utilizador. Abra os registos de conjunto de aprovação associados para identificar a causa da falha.
A seleção de **Repetir** adiciona à contagem de duração do conjunto de aprovação, move o conjunto de aprovação para um estado de **Processamento** e tenta processar os registos restantes.

## <a name="configure-approval-sets"></a>Configurar conjuntos de aprovação

###  <a name="enable-the-approval-sets-feature"></a>Ativar a funcionalidade Conjuntos de aprovação
Antes de ativar a funcionalidade de Conjuntos de aprovação, verifique se não existem aprovações atualmente em processamento.

- Aceda à página **Parâmetros do projeto** e selecione **Controlo de Funcionalidades** > **Ativar Aprovações Modernas**.

### <a name="turn-off-the-approval-sets-feature"></a>Desativar a funcionalidade Conjuntos de aprovação
Antes de desativar a funcionalidade de Conjuntos de aprovação, verifique se não existem aprovações atualmente em processamento.

- Aceda à página **Parâmetros do Projeto** e selecione **Controlo de Funcionalidades** > **Desativar Aprovações Modernas**.

### <a name="configuring-the-asynchronous-threshold"></a>Configurar o limiar assíncrono 
Quando os conjuntos de aprovação são criados, o processamento move-se para segundo plano quando o número selecionado de registos de aprovação excede o limiar indicado. Utilize o campo **Limiar Assíncrono** para configurar quando o processamento de aprovação deve ser executado de forma síncrona ou assíncrona.
Os valores válidos são:

  - Zero: Todos os pedidos devem ser processados assincronamente. 
  - Números superiores a zero: As aprovações são processadas assincronamente apenas quando o número de aprovações submetidas excede este valor.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
