---
title: Predefinir dimensões financeiras para entradas de tempo do projeto
description: Este artigo fornece informações sobre como a predefinição de dimensões financeiras são aplicadas a entradas de tempo.
author: stsporen
ms.date: 01/24/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 9863738a2d6d0e001961554043939f62f65d9ce5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916578"
---
# <a name="defaulting-financial-dimensions-for-project-time-entries"></a>Predefinir dimensões financeiras para entradas de tempo do projeto

[!include [banner](../includes/banner.md)]

Quando usa dimensões financeiras para entradas de tempo do projeto, o valor de dimensão predefinido é avaliado pela seguinte ordem:

1. recurso
2. Project
3. Fonte de financiamento

Por exemplo, se a dimensão predefinida for especificada num recurso, o valor predefinido será aplicado sobre o valor predefinido especificado para o projeto. Da mesma forma, se a dimensão predefinida for especificada num projeto, o valor predefinido será aplicado sobre o valor predefinido especificado para a fonte de financiamento.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
