---
title: Submeter um pedido de recurso
description: Pode submeter um requisito de recurso gerado como um pedido de recurso. Em seguida, o pedido é enviado para um gestor de recursos para ser cumprido.
author: ruhercul
manager: Annbe
ms.date: 10/04/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 94cf0f0d88e9be2522936b45122ed0037434d4f3
ms.sourcegitcommit: 2cf93d8bf0be5b61a739195a41334c34d910e9ba
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961736"
---
# <a name="submit-a-resource-request"></a>Submeter um pedido de recurso

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

Pode submeter um requisito de recurso gerado como um pedido de recurso. Em seguida, o pedido é enviado para um gestor de recursos para ser cumprido.

1. No Dynamics 365 Project Operations, na página **Projetos**, selecione o separador **Equipa** para ver uma lista de recursos reserváveis. 
2. Selecione o recurso genérico que tem um requisito de recurso a partir da lista e, em seguida, clique em **Submeter Pedido**.

O estado do pedido do membro da equipa genérico será alterado para **Submetido**.

Depois de o pedido ser concluído, o recurso genérico é substituído por um recurso nomeado se o gestor de recursos concluir o pedido ao reservar um recurso nomeado. Caso contrário, se o gestor de recursos propuser um recurso nomeado, o recurso genérico permanece na equipa e o estado do pedido será alterado para **Necessita de Revisão**.
