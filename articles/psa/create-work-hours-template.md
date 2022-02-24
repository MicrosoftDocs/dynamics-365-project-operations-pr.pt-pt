---
title: Criar um modelo de horas de trabalho
description: Este tópico descreve como criar um modelo de horas de trabalho no Project Service.
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
ms.openlocfilehash: 525f601ad6fee902cb6d5c128b596cc2d33f30c4
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981269"
---
# <a name="create-a-work-hours-template-project-service"></a>Criar um modelo de horas de trabalho (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

Para criar e gerir um projeto, deve aplicar um modelo de calendário ao projeto. O modelo de calendário define os seguintes atributos do projeto:

- Horário de trabalho, incluindo início e fim
- Dias de trabalho
- Exceções do calendário, tais como dias não laborais

O modelo de calendário que é aplicado a um projeto é uma cópia do modelo de calendário definido nas definições da sua organização.

> [!NOTE]
> Se alterar o modelo de calendário, essas alterações não se propagam ao horário de trabalho do projeto. Para alterar o horário de trabalho do projeto, deve ser aplicado um novo modelo.

Para criar um modelo de calendário para a sua organização, existem dois requisitos-chave:

- Defina as horas de trabalho desejadas do modelo utilizando um recurso de reserva novo ou existente.
- Crie um novo modelo de calendário e associe o modelo ao recurso de reserva.

**Defina as horas de trabalho do modelo**

1. Aceda a **Recursos** \> **Recursos**.
2. Crie um novo recurso para fazer referência no modelo de calendário ou selecione um recurso existente.
3. Selecione o separador **Horas de Trabalho** do recurso e preencha as instruções em [Definir horário de trabalho para um recurso](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) para configurar as regras do calendário.

**Criar um novo modelo de calendário**

1. Ir a **Definições** \> **Modelo de calendário**.
2. Selecione **Novo** e introduza um nome, descrição e recurso de modelo.


> [!NOTE]
> Quando um recurso é referenciado num modelo de calendário, uma cópia do calendário do recurso está associada ao modelo do calendário. Se alterar o modelo copiado das horas de trabalho, essas alterações não se propagam ao modelo de calendário.


### <a name="see-also"></a>Consulte Também  
 [Configurar recursos](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
