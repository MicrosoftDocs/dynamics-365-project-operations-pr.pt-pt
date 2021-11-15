---
title: Desinstale o Dynamics 365 Project Operations.
description: Este tópico fornece informações sobre como desinstalar o Dynamics 365 Project Operations.
author: stsporen
ms.date: 11/09/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b87c9324b1c95c10ef1e18b0fbf4572bdbe76827
ms.sourcegitcommit: b8b7a59eee7d93638446e93726d270316e45ab3d
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 11/10/2021
ms.locfileid: "7783657"
---
# <a name="uninstall-dynamics-365-project-operations"></a>Desinstale o Dynamics 365 Project Operations. 

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

Para desinstalar o Dynamics 365 Project Operations, tem de lhe ser atribuída a função de Administrador.

1. Aceda a **Definições** > **Soluções**.

    ![Página de definições.](./media/uninstall-proj-ops-solutions.png)
  
2. Remova as soluções pela ordem exata em que estão listadas na tabela seguinte. 

    | Passo | Nome da solução                                    | Nota                                                                                         |
    |------|----------------------------------------------------|----------------------------------------------------------------------------------------------|
    | 5 | msdyn_ProjectServiceUpgrade_managed.cab            | Se não for encontrada, ignore esta solução.                                                            |
    | 2 | ProjectOperations_Anchor                           | Se não for encontrada, ignore esta solução.                                                            |
    | 3 | Dynamics365ProjectOperationsDualWriteEntityMaps    | Se não for encontrada, ignore esta solução.                                                            |
    | 4 | Dynamics365ProjectOperationsDualWrite              | Se não for encontrada, ignore esta solução.                                                            |
    | 5 | ProjectService                                     | Sem notas adicionais.                                                                         |
    | 6 | ProjectServiceCore_Patch                           | Sem notas adicionais.                                                                         |
    | 7 | ProjectServiceCore                                 | Sem notas adicionais.                                                                         |
    | 8 | ProjectServiceDeprecatedComponents                 | Se não for encontrada, ignore esta solução.                                                            |
    | 9 | FieldServiceCommon                                 | Necessário para a escrita dupla com o Dynamics 365 Finance ou o Dynamics 365 Supply Chain Management.   |
    | 10 | msdyn_AssetCommon                                  | Necessário para a escrita dupla com o Dynamics 365 Finance ou o Dynamics 365 Supply Chain Management.   |
    | 11 | msdyn_TESA_Anchor                                  | Necessário para o Dynamics 365 Field Service.                                                     |
    | 12 | msdyn_TESA_Patch                                   | Necessário para o Dynamics 365 Field Service.                                                     |
    | 13 | msdyn_TESA                                         | Necessário para o Dynamics 365 Field Service.                                                     |
    | 14 | ResourceSchedulingControls                         | Necessário para o Dynamics 365 Field Service.                                                     |
    | 15 | MicrosoftDynamicsScheduling3_CumulativePatch       | Necessário para o Dynamics 365 Field Service.                                                     |
    | 17 | MicrosoftDynamicsScheduling_Patch_xx               | Necessário para o Dynamics 365 Field Service.                                                     |
    | 17 | MicrosoftDynamicsScheduling                        | Necessário para o Dynamics 365 Field Service.                                                     |
    | 18 | Dynamics365FinanceAndOperationsAnchor              | Se não for encontrada, ignore esta solução.                                                            |
    | 19 | Dynamics365Notes                                   | Se não for encontrada, ignore esta solução.                                                            |
    | 20 | Dynamics365FinanceAndOperationsDualWriteEntityMaps | Se não for encontrada, ignore esta solução.                                                            |
    | 21 | DualWriteCore                                      | Se não for encontrada, ignore esta solução.                                                            |
    | 22 | Dynamics365AssetManagementApp                      | Se não for encontrada, ignore esta solução.                                                            |
    | 23 | Dynamics365AssetManagement                         | Se não for encontrada, ignore esta solução.                                                            |
    | 24 | Dynamics365SupplyChainExtended                     | Se não for encontrada, ignore esta solução.                                                            |
    | 25 | Dynamics365FinanceExtended                         | Se não for encontrada, ignore esta solução.                                                            |
    | 26 | HCMCommon                                          | Se não for encontrada, ignore esta solução.                                                            |
    | 27 | Dynamics365FinanceAndOperationsCommon              | Se não for encontrada, ignore esta solução.                                                            |
    | 28 | Entidade                                              | Se não for encontrada, ignore esta solução.                                                            |
    | 29 | Dynamics365Company                                 | Se não for encontrada, ignore esta solução.                                                            |
    | 30 | CurrencyExchangeRates                              | Se não for encontrada, ignore esta solução.                                                            |
    | 31 | AssetCommon                                        | Se não for encontrada, ignore esta solução.                                                            |
