---
title: Estimativas e projetos de vendas
description: Este artigo fornece informações sobre como tirar partido da agenda e das estimativas no processo de vendas.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 957c2337cce3b3bf65a0bfef7c1aee6a730971fc
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925410"
---
# <a name="sales-estimates-and-projects"></a>Estimativas e projetos de vendas

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Durante o processo de vendas, pode criar estimativas de vendas associando um projeto a uma proposta de vendas. Deste modo, a estimativa determinística pode ocorrer durante o processo de vendas, para tirar partido das capacidades de agendamento e estimativa do projeto. Se a venda for concluída, a agenda utilizada para fins de estimativa de vendas poderá ser utilizada como base para um refinamento adicional do plano do projeto.

## <a name="linking-a-project-to-a-quote-line"></a>Associar um projeto a uma linha de proposta

Quando cria uma linha de proposta baseada em projetos, pode criar um novo projeto ou associar um projeto existente na página **Linha de Proposta**. 

> ![Formulário de linha de proposta.](media/project-8.png)
 
Quando cria um novo projeto a partir dos detalhes de linha de proposta, pode tirar partido dos modelos de projeto. Os modelos de projeto são projetos de modelo que representam planos do projeto padrão e estimativas financeiras que são típicos de uma organização. Também podem representar cópias de planos e estimativas de projeto a partir de projetos passados.

> ![Detalhes de linha de proposta.](media/project-9.png)
  
Quando cria o projeto a partir da proposta, o projeto é associado automaticamente à linha de proposta.

## <a name="components-of-estimates-in-a-project"></a>Componentes de estimativas num projeto

Uma agenda permite-lhe dividir o trabalho em tarefas, manter uma hierarquia das tarefas, determinar quais os recursos necessários para concluir uma tarefa e atribuir uma estimativa do esforço necessário para concluir uma tarefa.

Pode definir o esforço de trabalho e agendar estimativas utilizando os campos no separador **Agenda** da página **Projeto**. Uma vez que uma lista de preços está associada ao projeto, as estimativas financeiras são calculadas através da utilização de preços de custo e de venda que são definidos na lista de preços.

## <a name="importing-estimates-from-a-project-into-a-quote"></a>Importar estimativas de um projeto para uma proposta

Depois de definir as estimativas do projeto, pode importá-las para a linha de proposta. Na página **Detalhes de Linha de Proposta**, selecione **Importar a partir da estimativa** a partir de estimativas no friso para resumir as estimativas de projeto por tipo de transação, função ou nível de tarefa.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
