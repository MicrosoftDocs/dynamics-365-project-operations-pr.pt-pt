---
title: Modelos de competências e proficiência
description: Este tópico fornece informações sobre como utilizar os modelos de competências e proficiência.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/13/2019
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
ms.openlocfilehash: cd243544df062e5801bbfa0a3bd75c4d9a116a6f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082624"
---
# <a name="skills-and-proficiency-models"></a>Modelos de competências e proficiência

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

As competências são características do recurso partilhadas entre o Dynamics 365 Project Service Automation e, se existir, o Dynamics 365 Field Service. 

Para manter o repositório de competências no Project Service Automation, aceda a **Recursos** \> **Competências do Recurso**. 

> ![Competências do Recurso](media/Resource-Management-image84.png)

## <a name="use-proficiency-models-to-rate-resources"></a>Utilizar modelos de proficiência para classificar recursos

As competências para os recursos são classificadas por modelos de proficiência. As classificações individuais estão num modelo de proficiência. 

1. Para criar um modelo de proficiência, aceda a **Recursos** \> **Modelos de Proficiência** e selecione **Novo**.
2. No novo modelo de classificação, especifique o valor mínimo de classificação, o valor máximo de classificação e a entidade que está a ser avaliada.
3. Na subgrelha **Valores de Classificação** , é possível definir os diferentes valores de classificação, desde o mínimo até ao máximo.

> ![Classificações mínimas e máximas definidas](media/Resource-Management-image85.png)

Estes valores de classificação são apresentados nos filtros **Requisitos de Recursos** , **Quadro da Agenda** e **Assistente da Agenda**.
