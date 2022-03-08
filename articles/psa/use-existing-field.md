---
title: Utilizar um campo existente no Project Service como dimensão de definição de preços
description: Este tópico inclui informações sobre a utilização de campos existentes do Project Service como dimensões de definição de preços.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 075461042724c92e480e0df5ba976baf58542f479661f4c615aa442a150d0f8a
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 08/06/2021
ms.locfileid: "7004595"
---
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a>Utilizar um campo existente no Project Service como dimensão de definição de preços

[!include [banner](../includes/psa-now-project-operations.md)]

O PSA (Project Service Automation) tem vários campos na entidade **Valores Reais** que podem ser utilizados como dimensões de definição de preços para a definição de preços com base em recursos em organizações de projetos. Por exemplo, um campo comum é o **Recurso Reservável**. Empresas pequenas, com menos de 20-30 recursos faturáveis, podem achar que ter taxas de faturação e de custo específicas para cada recurso é uma abordagem mais simples. Entretanto, à medida que a força de trabalho faturável cresce, taxas específicas podem tornar-se irreais de manter, pois as taxas de faturação e o custo dos recursos começam a variar à medida que os recursos são promovidos, ganham mais experiência ou adquirem conjuntos de competências diferentes. Como esta abordagem ainda funciona para empresas de um determinado porte, consulte [Utilizar um recurso reservável como uma dimensão de definição de preços](bookable-resource-pricing-dimension.md) para compreender como um campo existente do Project Service pode ser utilizado como uma dimensão de definição de preços.

Outro exemplo é a categoria de transação. Os clientes e os implementadores utilizavam a categoria de transação do PSA para classificar o trabalho e utilizavam o campo para definir o preço e o custo com base na categoria do trabalho. Para obter mais informações, consulte [Utilizar categoria de transação como uma dimensão de definição de preços](transaction-category-pricing-dimension.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]