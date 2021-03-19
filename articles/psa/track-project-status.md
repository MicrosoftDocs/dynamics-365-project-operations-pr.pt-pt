---
title: Controlar o estado de um projeto
description: Como monitorizar o estado de um projeto no Project Service
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
ms.openlocfilehash: d57f33cdf240db4cae1f33fe962173790fe0fe7f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281942"
---
# <a name="track-a-projects-status-project-service"></a>Monitorizar o estado de um projeto (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Utilize as capacidades do [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] para controlar o progresso de um projeto do cliente.  

À medida que cativação progride, as fases do projeto refletem a fase da cativação:  


|              |                                                                                                                                                                                                                                                                                                  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   **Novo**    | Quando cria um projeto, a fase é definida como **Novo**. Se tiver criado o projeto a partir de um modelo, nesta fase o projeto pode ter uma agenda, estimativas e dados da equipa. Caso contrário, será o esquema do projeto e terá de introduzir manualmente os restantes componentes do projeto. |
|  **Proposta**   |      Quando associa um projeto a uma proposta ou o cria a partir de uma proposta, a fase de projeto é definida como **Proposta** e datas de início e de fim estimadas também são atualizadas. Quando o projeto está na fase de proposta, os detalhes da proposta são apresentados no separador **Vendas** na página **Projeto**.      |
|   **Planear**   |                                     Quando ganha uma proposta associada a um projeto e quando a cativação progride para a fase de contrato, a fase do projeto é atualizada para **Plano**. Os detalhes do contrato são apresentados no separador **Vendas** na página **Projeto**.                                      |
| **Concluída** |                    Quando o trabalho do projeto é concluído, pode mudar a fase para **Concluído**. Quando a fase do projeto é definida como concluído, entende-se que o trabalho está 100% concluído, mas o projeto é mantido aberto para serem registadas quaisquer horas ou despesas pendentes.                     |
|  **Fechar**   |           Depois de registadas todas as transações no projeto e não espera que sejam registadas mais, pode definir manualmente a fase como **Fecho**. Quando o projeto é definido como **Fecho**, não é possível registar mais transações no projeto e este passa a ser só de leitura.           |

## <a name="to-track-a-projects-status"></a>Para controlar o estado de um projeto  

1.  Vá para **Project Service > Projetos**.  

2.  Clique no projeto em que pretende trabalhar.  

3.  Na barra na parte superior do ecrã, selecione a seta para baixo junto ao nome do projeto e, em seguida, clique em **Monitorização do Projeto**.  

4.  Selecione **Controlo do Esforço** ou **Controlo dos Custos** na lista pendente acima da lista de tarefas.  

5.  Faça duplo clique em qualquer tarefa para editá-la. Também pode mover ou redimensionar as barras no gráfico Gantt para alterar o tempo e o progresso de uma tarefa.  

### <a name="see-also"></a>Consulte Também  
 [Guia do Gestor de Projeto](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]