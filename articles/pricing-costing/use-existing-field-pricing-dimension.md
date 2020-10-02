---
title: Campos das Operações do projeto como dimensões de definição de preços
description: Este tópico fornece informações usando campos como dimensões dos preços no Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3ddf3098e45fdc9b99067b64df05e2adc0b6ad05
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896430"
---
# <a name="project-operations-fields-as-pricing-dimensions"></a>Campos das Operações do projeto como dimensões de definição de preços

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

A entidade **Atuais** tem muitos campos que podem ser usados como dimensões de definição de preços para preços baseados em recursos. Por exemplo, um campo comum é o **Recurso Reservável**. Empresas pequenas, com menos de 20-30 recursos faturáveis, podem achar que ter taxas de faturação e de custo específicas para cada recurso é uma abordagem mais simples. No entanto, à medida que a mão de obra faturada aumenta, pode tornar-se irrealista manter as taxas específicas de recursos. O custo dos recursos e taxas de faturação começam a variar à medida que os recursos são promovidos, ganham mais experiência ou adquirem um conjunto diferente de competências. 

Outro exemplo é a categoria de transação. Os clientes e os implementadores utilizavam a categoria de transação para classificar o trabalho e utilizavam o campo para definir o preço e o custo com base na categoria do trabalho.
