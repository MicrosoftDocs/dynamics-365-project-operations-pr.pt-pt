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
ms.openlocfilehash: acdd228a9eb9d6c6c56f126ccca416613332a838
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013185"
---
# <a name="submitting-a-resource-request"></a><span data-ttu-id="506d1-103">Submeter um pedido de recurso</span><span class="sxs-lookup"><span data-stu-id="506d1-103">Submitting a resource request</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="506d1-104">Pode submeter um requisito de recurso gerado como um pedido de recurso.</span><span class="sxs-lookup"><span data-stu-id="506d1-104">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="506d1-105">Em seguida, o pedido é enviado para um gestor de recursos para ser cumprido.</span><span class="sxs-lookup"><span data-stu-id="506d1-105">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="506d1-106">No Project Service Automation (PSA), na página **Projetos**, clique no separador **Equipa** para ver a lista de recursos reserváveis.</span><span class="sxs-lookup"><span data-stu-id="506d1-106">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab to view a list bookable resources.</span></span> 
2. <span data-ttu-id="506d1-107">Selecione o recurso genérico que tem um requisito de recurso a partir da lista e, em seguida, clique em **Submeter Pedido**.</span><span class="sxs-lookup"><span data-stu-id="506d1-107">Select the generic resource that has a resource requirement from the list and then click **Submit Request**.</span></span>

![Submeter um pedido de recurso](media/RM-how-to-18.png)

<span data-ttu-id="506d1-109">O estado do pedido do membro da equipa genérico será alterado para **Submetido**.</span><span class="sxs-lookup"><span data-stu-id="506d1-109">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="506d1-110">Depois de o pedido ser efetuado pelo gestor de recursos, o recurso genérico será substituído por um recurso nomeado se o gestor de recursos cumprir o pedido com a reserva de um recurso nomeado.</span><span class="sxs-lookup"><span data-stu-id="506d1-110">After the request is fulfilled by the resource manager, the generic resource will be replaced by a named resource if the resource manager fulfills the request with the booking of a named resource.</span></span> <span data-ttu-id="506d1-111">Caso contrário, o recurso genérico permanecerá na equipa e o estado do pedido será alterado para **Necessita de Revisão**, se o gestor de recursos tiver proposto um recurso nomeado.</span><span class="sxs-lookup"><span data-stu-id="506d1-111">Otherwise, the generic resource will remain on the team and the request status will change to **Needs Review**, if the resource manager has proposed a named resource.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]