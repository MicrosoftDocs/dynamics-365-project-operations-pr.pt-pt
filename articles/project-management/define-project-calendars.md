---
title: Definir calendários de projetos
description: Esta tópico fornece informações sobre como aplicar um modelo de calendário a um projeto para acompanhar o calendário do projeto.
author: ruhercul
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 0d1a2c4bd2d4022bbf79afcef79170eb482e6418
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999010"
---
# <a name="define-project-calendars"></a>Definir calendários de projetos

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

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
3. Selecione o separador **Horas de Trabalho** do recurso e preencha as instruções em [Definir horário de trabalho para um recurso](/dynamics365/field-service/set-work-hours-resource.md) para configurar as regras do calendário.

**Criar um novo modelo de calendário**

1. Ir a **Definições** \> **Modelo de calendário**.
2. Selecione **Novo** e introduza um nome, descrição e recurso de modelo.

> [!NOTE]
> Quando um recurso é referenciado num modelo de calendário, uma cópia do calendário do recurso está associada ao modelo do calendário. Se alterar o modelo copiado das horas de trabalho, essas alterações não se propagam ao modelo de calendário.

Agora, pode associar o modelo de trabalho a um modelo de calendário do projeto.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

