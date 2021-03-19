---
title: Gerir contratos de projeto
description: Este tópico fornece informações sobre a visualização de contratos baseados em projetos.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5a4357d5cf184a3c6ada3ae33631694c31bb5b00
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273222"
---
# <a name="manage-project-contracts"></a><span data-ttu-id="a02ad-103">Gerir contratos de projeto</span><span class="sxs-lookup"><span data-stu-id="a02ad-103">Manage project contracts</span></span>

<span data-ttu-id="a02ad-104">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="a02ad-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a02ad-105">Os contratos de projeto no Dynamics 365 Project Operations capturam e gerem a alocações contratualmente acordadas e detalhes de faturação de um projeto.</span><span class="sxs-lookup"><span data-stu-id="a02ad-105">Project contracts in Dynamics 365 Project Operations capture and manage the contractually agreed on commitments and billing details of a project.</span></span> <span data-ttu-id="a02ad-106">A estrutura de um contrato do projeto no Project Operations está ajustado a trabalho baseado em projetos com os seguintes componentes:</span><span class="sxs-lookup"><span data-stu-id="a02ad-106">The structure of a project contract in Project Operations is tailored to project-based work with the following components:</span></span>

- <span data-ttu-id="a02ad-107">Os itens de contrato que identificam os componentes discretos do trabalho que serão apresentados como componentes de alto nível numa fatura de projeto.</span><span class="sxs-lookup"><span data-stu-id="a02ad-107">Contract lines that identify the discrete components of work that will be presented as high-level components on a project invoice.</span></span>
- <span data-ttu-id="a02ad-108">Os detalhes do item de contrato que identificam e estimam o trabalho para cada componente de alto nível ou item de contrato.</span><span class="sxs-lookup"><span data-stu-id="a02ad-108">Contract line details that identify and estimate the work for each high-level component or contract line.</span></span> <span data-ttu-id="a02ad-109">A estimativa inclui a agenda e os aspetos financeiros do trabalho estão ligados ao item de contrato.</span><span class="sxs-lookup"><span data-stu-id="a02ad-109">The estimate includes the schedule and the financial aspects for the work tied to the contract line.</span></span>
- <span data-ttu-id="a02ad-110">São criados modelos de contratação e componentes faturáveis para cada item de contrato que detenha o acordo de faturação de cada item de contrato e o contrato global.</span><span class="sxs-lookup"><span data-stu-id="a02ad-110">Contracting models and chargeable components are set up for each contract line that holds the billing arrangement for each contract line and the overall contract.</span></span>

## <a name="view-all-project-based-contracts"></a><span data-ttu-id="a02ad-111">Ver todos os contratos baseados em projetos</span><span class="sxs-lookup"><span data-stu-id="a02ad-111">View all project-based contracts</span></span>

<span data-ttu-id="a02ad-112">Uma lista de todos os contratos do projeto pode ser vista na página de lista **Contratos**.</span><span class="sxs-lookup"><span data-stu-id="a02ad-112">A list of all project contracts can be seen on the **Contracts** list page.</span></span> 

1. <span data-ttu-id="a02ad-113">Aceda a **Vendas** > **Contratos**.</span><span class="sxs-lookup"><span data-stu-id="a02ad-113">Go to **Sales** > **Contracts**.</span></span> <span data-ttu-id="a02ad-114">Uma lista de todas os seus Contratos do projeto no sistema são mostrados.</span><span class="sxs-lookup"><span data-stu-id="a02ad-114">A list of all your project Contracts in the system are shown.</span></span> 
2. <span data-ttu-id="a02ad-115">Selecione o **Alternador de vistas** (a seta pendente ao lado do nome da vista) para selecionar outras vistas filtradas.</span><span class="sxs-lookup"><span data-stu-id="a02ad-115">Select the **View switcher** (the drop-down arrow next to the name of the view) to select other filtered views.</span></span> <span data-ttu-id="a02ad-116">Pode criar as suas próprias vistas com critérios de filtro personalizados.</span><span class="sxs-lookup"><span data-stu-id="a02ad-116">You can create your own views with custom filter criteria.</span></span>

<span data-ttu-id="a02ad-117">Os contratos podem ser criados ou eliminados a partir desta página de lista ou páginas de detalhes.</span><span class="sxs-lookup"><span data-stu-id="a02ad-117">Contracts can be created or deleted from this list page or detail pages.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]