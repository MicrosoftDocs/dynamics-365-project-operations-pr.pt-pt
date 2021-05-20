---
title: Novidades ou alterações na Versão da Atualização 16 do Project Service Automation, V3
description: Este tópico lista as funcionalidades e correções disponíveis no Project Service Automation V3, Versão da Atualização 16, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
ms.topic: article
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
ms.openlocfilehash: 33a711816e8cca34c4595aa0929de9a808a48b0f
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949411"
---
# <a name="project-service-automation-update-release-16-v3"></a><span data-ttu-id="50c23-103">Versão da Atualização 16 do Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="50c23-103">Project Service Automation Update Release 16, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="50c23-104">Temos o prazer de anunciar a mais recente atualização à aplicação Project Service Automation para Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="50c23-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="50c23-105">Esta versão inclui algumas melhorias importantes na qualidade, desempenho e utilização.</span><span class="sxs-lookup"><span data-stu-id="50c23-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="50c23-106">Esta versão é compatível com o Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="50c23-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="50c23-107">Para atualizar esta versão, visite o Centro de Administração para o Dynamics 365 online e aceda à página de soluções para instalar a atualização.</span><span class="sxs-lookup"><span data-stu-id="50c23-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="50c23-108">Para obter mais informações, consulte [Instalar, Atualizar uma Solução Preferencial](/dynamics365/project-service/upgrade-psa-home-page).</span><span class="sxs-lookup"><span data-stu-id="50c23-108">For more information, see [Install, Update a Preferred Solution](/dynamics365/project-service/upgrade-psa-home-page).</span></span>
<span data-ttu-id="50c23-109">Este tópico lista as funcionalidades e correções novas ou alteradas para o PSA V3, Versão da Atualização 16.</span><span class="sxs-lookup"><span data-stu-id="50c23-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 16.</span></span> <span data-ttu-id="50c23-110">Esta versão tem um número de compilação de V3.10.6.34 e está geralmente disponível através de uma Atualização automática em janeiro de 2020.</span><span class="sxs-lookup"><span data-stu-id="50c23-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in January 2020.</span></span>


## <a name="update-release-16"></a><span data-ttu-id="50c23-111">Versão da Atualização 16</span><span class="sxs-lookup"><span data-stu-id="50c23-111">Update Release 16</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="50c23-112">Correções de erros</span><span class="sxs-lookup"><span data-stu-id="50c23-112">Bug fixes</span></span>

-   <span data-ttu-id="50c23-113">Tempo e Despesa</span><span class="sxs-lookup"><span data-stu-id="50c23-113">Time and Expense</span></span>

    -   <span data-ttu-id="50c23-114">Corrigido: os utilizadores que tentam submeter entradas de tempo e de gastos eliminadas para aprovação receberão agora mensagens de erro relevantes.</span><span class="sxs-lookup"><span data-stu-id="50c23-114">Fixed: Users attempting to submit deleted time and expense entries for approvals will now receive relevant error messages.</span></span>

-   <span data-ttu-id="50c23-115">Gestão de Projetos</span><span class="sxs-lookup"><span data-stu-id="50c23-115">Project Management</span></span>

    -   <span data-ttu-id="50c23-116">Corrigido: as unidades de atribuição de recursos definidas para os membros da equipa nos modelos são respeitadas e os modelos são aplicados a um novo projeto.</span><span class="sxs-lookup"><span data-stu-id="50c23-116">Fixed: The resourcing units defined for team members in templates are respected with the templates are applied to a new project.</span></span>

    -   <span data-ttu-id="50c23-117">Corrigido: foi melhorado o tratamento da reatribuição da propriedade dos registos.</span><span class="sxs-lookup"><span data-stu-id="50c23-117">Fixed: Improved handling of the re-assignment of record ownership.</span></span>

    -   <span data-ttu-id="50c23-118">Corrigido: os projetos em processo de cópia não terão permissão para serem copiados enquanto não forem concluídas todas as operações de cópia.</span><span class="sxs-lookup"><span data-stu-id="50c23-118">Fixed: Projects that are in the process of being copied will not be permitted to copied until all copy operations are complete.</span></span>

-   <span data-ttu-id="50c23-119">Gestão de Recursos</span><span class="sxs-lookup"><span data-stu-id="50c23-119">Resource Management</span></span>

    -   <span data-ttu-id="50c23-120">Corrigido: agora, as reservas alargadas tratam corretamente as curtas durações e já não criam zero horas para as reservas alargadas.</span><span class="sxs-lookup"><span data-stu-id="50c23-120">Fixed: Extend bookings now handles short durations correctly and no longer creates zero hours for extended bookings.</span></span>

    -   <span data-ttu-id="50c23-121">Corrigido: agora, a vista de reconciliação é composta quando o fuso horário do projeto é +5:30 GMT e a hora do utilizador por si só é diferente.</span><span class="sxs-lookup"><span data-stu-id="50c23-121">Fixed: The reconciliation view now renders when the project time zone is +5:30 GMT and the user’s time aone is different.</span></span>

-   <span data-ttu-id="50c23-122">Sales</span><span class="sxs-lookup"><span data-stu-id="50c23-122">Sales</span></span>

    -   <span data-ttu-id="50c23-123">Corrigido: quando um projeto mapeado para um item de contrato é removido e é mapeado um novo projeto, os registos reais no novo projeto não eram reavaliados com base nas regras de faturação e definição de preços definidas no item de contrato.</span><span class="sxs-lookup"><span data-stu-id="50c23-123">Fixed: When a project mapped to a contract line is removed and a new project is mapped, the actual records on the new project were not getting re-evaluated based on the billing and pricing rules defined on the contract line.</span></span> <span data-ttu-id="50c23-124">Este problema foi corrigido nesta versão.</span><span class="sxs-lookup"><span data-stu-id="50c23-124">This has been fixed in this release.</span></span> <span data-ttu-id="50c23-125">A definição de preços e os registos reais no projeto mapeado recentemente serão revertidos e recriados corretamente com base nas regras de definição de preços e faturação do item de contrato.</span><span class="sxs-lookup"><span data-stu-id="50c23-125">Pricing and actual records on the newly mapped project will get reversed and re-created correctly based on the pricing and billing rules of the contract line.</span></span> <span data-ttu-id="50c23-126">Os registos reais do projeto não mapeado também serão reavaliados e recriados como consequência.</span><span class="sxs-lookup"><span data-stu-id="50c23-126">The actual records of the un-mapped project will also get re-evaluated and re-created as a consequence.</span></span>

    -   <span data-ttu-id="50c23-127">Corrigido: foi adicionada validação adicional ao campo **Montante** da linha da estimativa para assegurar que os valores nulos não são mantidos.</span><span class="sxs-lookup"><span data-stu-id="50c23-127">Fixed: Additional validation has been added to an estimate line’s **Amount** field to ensure that null values are not persisted.</span></span>

    -   <span data-ttu-id="50c23-128">Corrigido: depois de atualizados os valores reais num projeto, foi adicionado um botão de atualização ao formulário principal do projeto para permitir que os utilizadores repitam a sincronização dos valores reais.</span><span class="sxs-lookup"><span data-stu-id="50c23-128">Fixed: When actuals have been updated on a project, a refresh button has been added to the project main form to allow users to re-sync the actuals.</span></span>

    -   <span data-ttu-id="50c23-129">Corrigido: quando os utilizadores fazem a atualização da versão 2.X para 3.X, serão permitidos projetos com um valor NULL para um nome de projeto.</span><span class="sxs-lookup"><span data-stu-id="50c23-129">Fixed: When users upgrade from 2.X to 3.X, projects with a NULL value for project name will be permitted.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]