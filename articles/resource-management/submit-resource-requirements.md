---
title: Submeter um pedido de recurso
description: Pode submeter um requisito de recurso gerado como um pedido de recurso. Em seguida, o pedido é enviado para um gestor de recursos para ser cumprido.
author: ruhercul
manager: Annbe
ms.date: 10/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 18f43acc64ed72b1543a2d7d91a2648e7e185fc4
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128837"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="5c34e-104">Submeter um pedido de recurso</span><span class="sxs-lookup"><span data-stu-id="5c34e-104">Submit a resource request</span></span>

<span data-ttu-id="5c34e-105">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="5c34e-105">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5c34e-106">Pode submeter um requisito de recurso gerado como um pedido de recurso.</span><span class="sxs-lookup"><span data-stu-id="5c34e-106">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="5c34e-107">Em seguida, o pedido é enviado para um gestor de recursos para ser cumprido.</span><span class="sxs-lookup"><span data-stu-id="5c34e-107">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="5c34e-108">No Dynamics 365 Project Operations, na página **Projetos**, selecione o separador **Equipa** para ver uma lista de recursos reserváveis.</span><span class="sxs-lookup"><span data-stu-id="5c34e-108">In Dynamics 365 Project Operations, on the **Projects** page, select the **Team** tab to view a list of bookable resources.</span></span> 
2. <span data-ttu-id="5c34e-109">Selecione o recurso genérico que tem um requisito de recurso a partir da lista e, em seguida, clique em **Submeter Pedido**.</span><span class="sxs-lookup"><span data-stu-id="5c34e-109">Select the generic resource that has a resource requirement from the list, and then click **Submit Request**.</span></span>

<span data-ttu-id="5c34e-110">O estado do pedido do membro da equipa genérico será alterado para **Submetido**.</span><span class="sxs-lookup"><span data-stu-id="5c34e-110">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="5c34e-111">Depois de o pedido ser concluído, o recurso genérico é substituído por um recurso nomeado se o gestor de recursos concluir o pedido ao reservar um recurso nomeado.</span><span class="sxs-lookup"><span data-stu-id="5c34e-111">After the request is fulfilled, the generic resource is replaced by a named resource if the resource manager fulfills the request by booking a named resource.</span></span> <span data-ttu-id="5c34e-112">Caso contrário, se o gestor de recursos propuser um recurso nomeado, o recurso genérico permanece na equipa e o estado do pedido será alterado para **Necessita de Revisão**.</span><span class="sxs-lookup"><span data-stu-id="5c34e-112">Otherwise, if the resource manager proposes a named resource, the generic resource remains on the team and the request status will change to **Needs Review**.</span></span>
