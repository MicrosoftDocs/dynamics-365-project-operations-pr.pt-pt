---
title: Novidades ou alterações na Versão da Atualização 29 do Project Service Automation, V3
description: Este tópico lista as funcionalidades e correções disponíveis no Project Service Automation V3, Versão da Atualização 29, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: 711255ab66f84fe46d0f16fa72e5a10fe0360394
ms.sourcegitcommit: f78087174a8512199a1bcbd7e8610bbc80e64801
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 03/04/2021
ms.locfileid: "5499685"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a><span data-ttu-id="fd48a-103">Novidades ou alterações na Versão da Atualização 29 do Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="fd48a-103">What's new or changed in Project Service Automation Update Release 29, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="fd48a-104">Temos o prazer de anunciar a mais recente atualização à aplicação Project Service Automation para Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="fd48a-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="fd48a-105">Esta versão inclui algumas melhorias importantes na qualidade, desempenho e utilização.</span><span class="sxs-lookup"><span data-stu-id="fd48a-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="fd48a-106">Esta versão é compatível com o Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="fd48a-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="fd48a-107">Para atualizar esta versão, visite o Centro de Administração para o Dynamics 365 online e aceda à página de soluções para instalar a atualização.</span><span class="sxs-lookup"><span data-stu-id="fd48a-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="fd48a-108">Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="fd48a-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="fd48a-109">Este tópico lista as funcionalidades e correções novas ou alteradas para o Project Service Automation V3, Versão da Atualização 29.</span><span class="sxs-lookup"><span data-stu-id="fd48a-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 29.</span></span> <span data-ttu-id="fd48a-110">Esta versão tem um número de compilação V3.10.45.98 e está geralmente disponível através de uma atualização automática em fevereiro de 2021.</span><span class="sxs-lookup"><span data-stu-id="fd48a-110">This version has a build number of V3.10.45.98 and is generally available through a self-update in February 2021.</span></span>

## <a name="update-release-29"></a><span data-ttu-id="fd48a-111">Versão da Atualização 29</span><span class="sxs-lookup"><span data-stu-id="fd48a-111">Update Release 29</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="fd48a-112">Correções de erros</span><span class="sxs-lookup"><span data-stu-id="fd48a-112">Bug fixes</span></span>

<span data-ttu-id="fd48a-113">**Tempo e Despesa**</span><span class="sxs-lookup"><span data-stu-id="fd48a-113">**Time and Expense**</span></span>

<span data-ttu-id="fd48a-114">Foram corrigidos os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="fd48a-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="fd48a-115">Os utilizadores não podem ver horas de trabalho registadas em dias não úteis na grelha de entrada de tempo.</span><span class="sxs-lookup"><span data-stu-id="fd48a-115">Users can't see working hours logged on non-working days in the time entry grid.</span></span>
- <span data-ttu-id="fd48a-116">As entradas de despesas aprovadas podem ser editadas na grelha.</span><span class="sxs-lookup"><span data-stu-id="fd48a-116">Approved expense entries can be edited on the grid.</span></span>

<span data-ttu-id="fd48a-117">**Gestão de Projetos**</span><span class="sxs-lookup"><span data-stu-id="fd48a-117">**Project Management**</span></span>

<span data-ttu-id="fd48a-118">Foram corrigidos os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="fd48a-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="fd48a-119">Lógica de validação em falta para garantir que as horas de esforço de atribuição de recursos não podem ser negativas.</span><span class="sxs-lookup"><span data-stu-id="fd48a-119">Missing validation logic to ensure resource assignment effort hours can't be negative.</span></span>
- <span data-ttu-id="fd48a-120">A ação personalizada **AssignResourcesForTask** atualiza todos os campos em vez de apenas campos alterados.</span><span class="sxs-lookup"><span data-stu-id="fd48a-120">The custom action, **AssignResourcesForTask** updates all fields instead of only changed fields.</span></span>
- <span data-ttu-id="fd48a-121">Ao copiar um projeto num ambiente com plug-ins ou fluxos de trabalho registados no evento **CreateProject**, o atributo **msdyn_bulkgenerationstatus** não é atualizado se o **CopyWBSToProject** falhar.</span><span class="sxs-lookup"><span data-stu-id="fd48a-121">When copying a project in an environment with plug-ins or workflows that are registered on the **CreateProject** event, the **msdyn_bulkgenerationstatus** attribute isn't updated if the **CopyWBSToProject** fails.</span></span>
- <span data-ttu-id="fd48a-122">Quando se expande o calendário do projeto, os dias de trabalho não são classificados por ordem ascendente, fazendo com que algumas atualizações de tarefas do projeto falhem.</span><span class="sxs-lookup"><span data-stu-id="fd48a-122">When you expand the project calendar, the working days aren't sorted in ascending order causing some project task updates to fail.</span></span>
- <span data-ttu-id="fd48a-123">Mudar o Gestor de Projeto num projeto existente desencadeia a lógica de incumprimento da unidade organizacional.</span><span class="sxs-lookup"><span data-stu-id="fd48a-123">Changing the Project Manager on an existing project triggers the organizational unit defaulting logic.</span></span>

<span data-ttu-id="fd48a-124">**Vendas**</span><span class="sxs-lookup"><span data-stu-id="fd48a-124">**Sales**</span></span>

<span data-ttu-id="fd48a-125">Foram corrigidos os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="fd48a-125">The following issues have been fixed:</span></span>

- <span data-ttu-id="fd48a-126">O separador **Desempenho do Contrato** na página **Contrato** falha silenciosamente durante a inicialização quando não existem linhas contratuais.</span><span class="sxs-lookup"><span data-stu-id="fd48a-126">The **Contract Performance** tab on the **Contract** page fails silently during initialization when no contract lines are present.</span></span>
