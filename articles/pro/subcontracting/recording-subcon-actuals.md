---
title: Tempo de gravação, despesas e utilização de materiais para componentes subcontratados
description: Este artigo explica como o tempo, as despesas e a utilização de material registados em projetos a partir de componentes subcontratados são monitorizados pelo Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b82c14412cfb0405040902a2329c3b6692422d89
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522528"
---
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>Tempo de gravação, despesas e utilização de materiais em projetos para componentes subcontratados

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

Este artigo explica como o tempo, as despesas e a utilização de material registados em projetos a partir de componentes subcontratados são monitorizados pelo Microsoft Dynamics 365 Project Operations.

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
