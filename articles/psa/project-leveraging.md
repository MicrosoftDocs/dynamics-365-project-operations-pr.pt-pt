---
title: Estimativas e projetos de vendas
description: Este tópico fornece informações sobre como tirar partido da agenda e das estimativas no processo de vendas.
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: d8bb380519759659dc1b4151b62228a626ee7a26
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120692"
---
# <a name="sales-estimates-and-projects"></a>Estimativas e projetos de vendas

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Durante o processo de vendas, pode criar estimativas de vendas associando um projeto a uma proposta de vendas. Deste modo, a estimativa determinística pode ocorrer durante o processo de vendas, para tirar partido das capacidades de agendamento e estimativa do projeto. Se a venda for concluída, a agenda utilizada para fins de estimativa de vendas poderá ser utilizada como base para um refinamento adicional do plano do projeto.

## <a name="linking-a-project-to-a-quote-line"></a>Associar um projeto a uma linha de proposta

Quando cria uma linha de proposta baseada em projetos, pode criar um novo projeto ou associar um projeto existente na página **Linha de Proposta**. 

> ![Formulário de linha de proposta](media/project-8.png)
 
Quando cria um novo projeto a partir dos detalhes de linha de proposta, pode tirar partido dos modelos de projeto. Os modelos de projeto são projetos de modelo que representam planos do projeto padrão e estimativas financeiras que são típicos de uma organização. Também podem representar cópias de planos e estimativas de projeto a partir de projetos passados.

> ![Detalhes de linha de proposta](media/project-9.png)
  
Quando cria o projeto a partir da proposta, o projeto é associado automaticamente à linha de proposta.

## <a name="components-of-estimates-in-a-project"></a>Componentes de estimativas num projeto

Uma agenda permite-lhe dividir o trabalho em tarefas, manter uma hierarquia das tarefas, determinar quais os recursos necessários para concluir uma tarefa e atribuir uma estimativa do esforço necessário para concluir uma tarefa.

Pode definir o esforço de trabalho e agendar estimativas utilizando os campos no separador **Agenda** da página **Projeto**. Uma vez que uma lista de preços está associada ao projeto, as estimativas financeiras são calculadas através da utilização de preços de custo e de venda que são definidos na lista de preços.

## <a name="importing-estimates-from-a-project-into-a-quote"></a>Importar estimativas de um projeto para uma proposta

Depois de definir as estimativas do projeto, pode importá-las para a linha de proposta. Na página **Detalhes de Linha de Proposta**, selecione **Importar a partir da estimativa** a partir de estimativas no friso para resumir as estimativas de projeto por tipo de transação, função ou nível de tarefa.
