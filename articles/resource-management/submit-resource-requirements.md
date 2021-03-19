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
ms.openlocfilehash: bc97af1ec90e60417c502eb329a85004e769e05b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279152"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="57dfe-104">Submeter um pedido de recurso</span><span class="sxs-lookup"><span data-stu-id="57dfe-104">Submit a resource request</span></span>

<span data-ttu-id="57dfe-105">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="57dfe-105">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="57dfe-106">Pode submeter um requisito de recurso gerado como um pedido de recurso.</span><span class="sxs-lookup"><span data-stu-id="57dfe-106">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="57dfe-107">Em seguida, o pedido é enviado para um gestor de recursos para ser cumprido.</span><span class="sxs-lookup"><span data-stu-id="57dfe-107">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="57dfe-108">No Dynamics 365 Project Operations, na página **Projetos**, selecione o separador **Equipa** para ver uma lista de recursos reserváveis.</span><span class="sxs-lookup"><span data-stu-id="57dfe-108">In Dynamics 365 Project Operations, on the **Projects** page, select the **Team** tab to view a list of bookable resources.</span></span> 
2. <span data-ttu-id="57dfe-109">Selecione o recurso genérico que tem um requisito de recurso a partir da lista e, em seguida, clique em **Submeter Pedido**.</span><span class="sxs-lookup"><span data-stu-id="57dfe-109">Select the generic resource that has a resource requirement from the list, and then click **Submit Request**.</span></span>

<span data-ttu-id="57dfe-110">O estado do pedido do membro da equipa genérico será alterado para **Submetido**.</span><span class="sxs-lookup"><span data-stu-id="57dfe-110">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="57dfe-111">Depois de o pedido ser concluído, o recurso genérico é substituído por um recurso nomeado se o gestor de recursos concluir o pedido ao reservar um recurso nomeado.</span><span class="sxs-lookup"><span data-stu-id="57dfe-111">After the request is fulfilled, the generic resource is replaced by a named resource if the resource manager fulfills the request by booking a named resource.</span></span> <span data-ttu-id="57dfe-112">Caso contrário, se o gestor de recursos propuser um recurso nomeado, o recurso genérico permanece na equipa e o estado do pedido será alterado para **Necessita de Revisão**.</span><span class="sxs-lookup"><span data-stu-id="57dfe-112">Otherwise, if the resource manager proposes a named resource, the generic resource remains on the team and the request status will change to **Needs Review**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]