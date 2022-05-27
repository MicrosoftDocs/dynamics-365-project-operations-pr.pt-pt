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
ms.reviewer: johnmichalak
ms.openlocfilehash: d22f52771f55a551416d1ba2f7105d59d7b912f0
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8577480"
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
