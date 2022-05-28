---
title: Tempo de gravação, despesas e utilização de materiais para componentes subcontratados
description: Este tópico explica como o tempo, as despesas e a utilização de material registados em projetos a partir de componentes subcontratados são monitorizados pelo Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 5a31b4a1092cc4829cbfc789e8b8e30030b2826b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8599238"
---
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>Tempo de gravação, despesas e utilização de materiais em projetos para componentes subcontratados

[!include [banner](../../includes/dataverse-preview.md)]

_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_

Este tópico explica como o tempo, as despesas e a utilização de material registados em projetos a partir de componentes subcontratados são monitorizados pelo Microsoft Dynamics 365 Project Operations.

## <a name="costing-for-subcontractor-time-on-projects"></a>Custeamento para tempo de subcontratante em projetos
No Project Operations, os trabalhadores contratados podem registar o tempo em projetos de forma semelhante à dos colaboradores. Ao introduzir tempo em projetos e/ou tarefas de projeto, um trabalhador contratado pode selecionar um subcontrato e item de subcontrato específicos.

Quando o tempo submetido pelos trabalhadores contratados é aprovado, o custo do projeto é registado utilizando a taxa de custo unitário que é configurada para esse recurso de trabalhador contratado na secção **Preços de funções** da lista de preços de compra no subcontrato.

## <a name="costing-for-subcontracted-expenses-on-projects"></a>Custeamento para despesas subcontratadas em projetos
Ao introduzir despesas incorridas em projetos, pode selecionar um subcontrato e item de subcontrato na entrada de despesas. 

Quando esta entrada de despesa é submetida e aprovada, o custo da despesa é registado no projeto com base no custo unitário que é configurado para essa categoria de transação na secção **Preços de categorias** da lista de preços de compra no subcontrato.

## <a name="costing-for-subcontracted-materials-on-projects"></a>Custeamento para materiais subcontratados em projetos
Ao introduzir utilização de materiais em projetos, pode selecionar um subcontrato e item de subcontrato no registo de utilização de materiais. Quando o registo de utilização de materiais é submetido e aprovado, o custo dos materiais é registado no projeto com base no custo unitário que é configurado para esse produto na secção **Itens da lista de preços** da lista de preços do subcontrato.

A utilização de materiais também pode ser registada para acrescentar manualmente produtos a projetos. Este tipo de utilização de materiais também pode ser ligado a um subcontrato e item de subcontrato. Ao registar a utilização de materiais para produtos acrescentados manualmente, é necessário introduzir o custo por unidade do produto acrescentado manualmente. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
