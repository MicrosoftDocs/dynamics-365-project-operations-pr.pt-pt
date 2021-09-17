---
title: Conjuntos de aprovações
description: Este tópico explica como trabalhar com conjuntos de aprovações, pedidos e subconjuntos dessas operações.
author: stsporen
manager: tfehr
ms.date: 08/10/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 1d9333033eb2b03966c6531d0fd6ad5b878acd93
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323250"
---
# <a name="approval-sets"></a>Conjuntos de aprovações

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

Os conjuntos de aprovações agrupam os pedidos de aprovação em subconjuntos de operações mais pequenos. Este agrupamento permite que as aprovações sejam processadas por projeto, numa ordem específica, e permite repetições e sequenciações. O agrupamento de pedidos de aprovação melhora a fiabilidade e a rastreabilidade do processamento de aprovações no caso de grandes volumes de aprovações.

Os conjuntos de aprovações indicam o estado geral de processamento dos seus registos relacionados. Quando um registo de aprovação é processado utilizando um conjunto de aprovações, o registo muda de **Submetido** para **Aprovado** e deixa de estar associado ao conjunto de aprovações. Se um registo falhar quando for submetido a aprovação, o registo permanece num estado de **Submetido** e o conjunto de aprovação é marcado como falhado. O conjunto de aprovação regista a mensagem de erro da falha.

## <a name="processing-approvals-and-approval-sets"></a>Processamento de aprovações e conjuntos de aprovações
As aprovações que estão em fila para processamento são visíveis na vista **Processamento de Aprovações**. O sistema processa todas as entradas várias vezes de forma assíncrona, incluindo a repetição de uma aprovação se as tentativas anteriores falharem.

O campo **Duração do Conjunto de Aprovação** regista o número de tentativas restantes para processar o conjunto antes de ser marcado como falhado.

## <a name="failed-approvals-and-approval-sets"></a>Aprovações e conjuntos de aprovações falhados
A vista **Aprovações Com Falhas** lista todas as aprovações que necessitam de intervenção do utilizador. Abra os registos de conjunto de aprovação associados para identificar a causa da falha.
A seleção de **Repetir** adiciona à contagem de duração do conjunto de aprovação, move o conjunto de aprovação para um estado de **Processamento** e tenta processar os registos restantes.

## <a name="configure-approval-sets"></a>Configurar conjuntos de aprovação

### <a name="enable-the-approval-sets-feature"></a>Ativar a funcionalidade Conjuntos de aprovação
Antes de ativar a funcionalidade de Conjuntos de aprovação, verifique se não existem aprovações atualmente em processamento.

- Aceda à página **Parâmetros do projeto** e selecione **Controlo de Funcionalidades** > **Ativar Aprovações Modernas**.

### <a name="turn-off-the-approval-sets-feature"></a>Desativar a funcionalidade Conjuntos de aprovação
Antes de desativar a funcionalidade de Conjuntos de aprovação, verifique se não existem aprovações atualmente em processamento.

- Aceda à página **Parâmetros do Projeto** e selecione **Controlo de Funcionalidades** > **Desativar Aprovações Modernas**.

### <a name="configuring-the-asynchronous-threshold"></a>Configurar o limiar assíncrono 
Quando os conjuntos de aprovação são criados, o processamento move-se para segundo plano quando o número selecionado de registos de aprovação excede o limiar indicado. Utilize o campo **Limiar Assíncrono** para configurar quando o processamento de aprovação deve ser executado de forma síncrona ou assíncrona. Selecione um dos seguintes valores:

  - Zero: Todos os pedidos devem ser processados assincronamente. 
  - Números superiores a zero: As aprovações são processadas assincronamente apenas quando o número de aprovações submetidas excede este valor.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
