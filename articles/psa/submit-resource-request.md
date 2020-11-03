---
title: Submeter um pedido de recurso
description: Este tópico fornece informações sobre a submissão de um pedido para um recurso de projeto.
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: bcea3d640d7e9ee2b071c55bff9ade3268edb319
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082497"
---
# <a name="submitting-a-resource-request"></a>Submeter um pedido de recurso

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Pode submeter um requisito de recurso gerado como um pedido de recurso. Em seguida, o pedido é enviado para um gestor de recursos para ser cumprido.

1. No Project Service Automation (PSA), na página **Projetos** , clique no separador **Equipa** para ver a lista de recursos reserváveis. 
2. Selecione o recurso genérico que tem um requisito de recurso a partir da lista e, em seguida, clique em **Submeter Pedido**.

![Submeter um pedido de recurso](media/RM-how-to-18.png)

O estado do pedido do membro da equipa genérico será alterado para **Submetido**.

Depois de o pedido ser efetuado pelo gestor de recursos, o recurso genérico será substituído por um recurso nomeado se o gestor de recursos cumprir o pedido com a reserva de um recurso nomeado. Caso contrário, o recurso genérico permanecerá na equipa e o estado do pedido será alterado para **Necessita de Revisão** , se o gestor de recursos tiver proposto um recurso nomeado.
