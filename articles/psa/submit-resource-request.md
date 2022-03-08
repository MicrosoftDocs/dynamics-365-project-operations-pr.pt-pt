---
title: Submeter um pedido de recurso
description: Este tópico fornece informações sobre a submissão de um pedido para um recurso de projeto.
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
ms.topic: article
author: JohnPBurrows
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
ms.openlocfilehash: da3e2798079816409ffbcfed911c05f3d51307fef22c48d112802927828faeb2
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6985020"
---
# <a name="submitting-a-resource-request"></a>Submeter um pedido de recurso

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Pode submeter um requisito de recurso gerado como um pedido de recurso. Em seguida, o pedido é enviado para um gestor de recursos para ser cumprido.

1. No Project Service Automation (PSA), na página **Projetos**, clique no separador **Equipa** para ver a lista de recursos reserváveis. 
2. Selecione o recurso genérico que tem um requisito de recurso a partir da lista e, em seguida, clique em **Submeter Pedido**.

![Submeter um pedido de recurso.](media/RM-how-to-18.png)

O estado do pedido do membro da equipa genérico será alterado para **Submetido**.

Depois de o pedido ser efetuado pelo gestor de recursos, o recurso genérico será substituído por um recurso nomeado se o gestor de recursos cumprir o pedido com a reserva de um recurso nomeado. Caso contrário, o recurso genérico permanecerá na equipa e o estado do pedido será alterado para **Necessita de Revisão**, se o gestor de recursos tiver proposto um recurso nomeado.


[!INCLUDE[footer-include](../includes/footer-banner.md)]