---
title: Predefinir dimensões financeiras para entradas de tempo do projeto
description: Este tópico fornece informações sobre como a predefinição de dimensões financeiras são aplicadas a entradas de tempo.
author: stsporen
ms.date: 01/24/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: cc51fcdcbbfec23591471c0f7522d571be813a84
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8597950"
---
# <a name="defaulting-financial-dimensions-for-project-time-entries"></a>Predefinir dimensões financeiras para entradas de tempo do projeto

[!include [banner](../includes/banner.md)]

Quando usa dimensões financeiras para entradas de tempo do projeto, o valor de dimensão predefinido é avaliado pela seguinte ordem:

1. recurso
2. Project
3. Fonte de financiamento

Por exemplo, se a dimensão predefinida for especificada num recurso, o valor predefinido será aplicado sobre o valor predefinido especificado para o projeto. Da mesma forma, se a dimensão predefinida for especificada num projeto, o valor predefinido será aplicado sobre o valor predefinido especificado para a fonte de financiamento.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
