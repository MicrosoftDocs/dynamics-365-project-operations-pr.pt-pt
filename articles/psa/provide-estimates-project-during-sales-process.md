---
title: Apresentar estimativas de trabalho para um projeto durante o processo de vendas
description: Como apresentar estimativas de trabalho para um projeto durante o processo de vendas no Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 7bd83b6872d437f1d074d6ea2336c751bdfdd9e6
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120602"
---
# <a name="provide-work-estimates-for-a-project-during-the-sales-process-project-service"></a>Apresentar estimativas de trabalho para um projeto durante o processo de vendas (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Durante o processo de vendas, poderá determinar as estimativas de vendas de raiz com as linhas de proposta. As capacidades do [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] no [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] oferecem uma forma mais científica e determinística de criar as estimativas de vendas ao dividir os itens de trabalho e ao associar os atributos relevantes que contribuem para as estimativas do projeto na estrutura hierárquica do trabalho.  
  
 Quando ganha a venda, pode utilizar a estrutura hierárquica do trabalho associada no plano do projeto ao refiná-lo conforme for necessário para concluir o projeto com êxito.  
  
## <a name="link-a-project-to-a-quote-line"></a>Associar um projeto a uma linha de proposta  
 Quando cria uma linha de proposta baseada no projeto, pode criar um novo projeto a partir da linha de proposta. Poderá utilizar os modelos de projeto, que são planos de projeto padrão pré-configurados e estimativas financeiras comuns à sua organização, ou uma cópia de um plano do projeto e estimativas de um projeto passado. Quando cria um projeto, a escolha de um modelo de projeto fornece uma base para refinar o plano do projeto, as estimativas e os requisitos da função. Ao criar o projeto a partir da proposta, o projeto é associado automaticamente à linha de proposta.  
  
## <a name="project-estimate-components"></a>Componentes da estimativa do projeto  
 A estrutura hierárquica do trabalho num projeto fornece uma forma de dividir o trabalho em tarefas, manter de uma hierarquia de tarefas e atribuir uma estimativa do esforço necessário para concluir cada tarefa. Também poderá associar funções a uma tarefa para indicar uma estimativa do tipo de recurso necessário para concluir uma tarefa e uma agenda.  
  
 A estrutura hierárquica do trabalho ajuda a determinar o esforço do trabalho e as estimativas de agenda. Por predefinição, o projeto utiliza listas de preços predefinidas que definiu anteriormente. O custo e os preços de vendas definidos nas listas de preços ajudam a determinar as estimativas financeiras para a divisão hierárquica do trabalho do projeto.  
  
 Se o projeto estiver associado a uma proposta, e esta tiver uma lista de preços diferente da predefinição, é utilizada a lista de preços da proposta para as estimativas.  
  
## <a name="import-estimates-from-a-project-into-a-quote"></a>Importar estimativas de um projeto para uma proposta  
 Quando tiver as estimativas do projeto no projeto, poderá importá-las para linha de proposta:  
  
-   Em **Detalhes de Linha de Proposta**, clique em **Importar a partir da estimativa**. 

-   Selecione se pretende importar as estimativas do projeto resumidas por nível de nó da estrutura hierárquica do trabalho, tipo de transação ou função.  
  
### <a name="see-also"></a>Consulte Também  
 [Guia do Gestor de Projeto](../psa/project-manager-guide.md)
