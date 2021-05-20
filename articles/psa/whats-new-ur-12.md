---
title: Novidades ou alterações na Versão da Atualização 12 do Project Service Automation, V3
description: Esta tópico fornece informações sobre o que há de novo na Versão da Atualização 12 do Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: 58a12ded135712d8194499ce4a9ba9e4e2aa99bd
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949513"
---
# <a name="project-service-automation-update-release-12-v3"></a><span data-ttu-id="36010-103">Versão da Atualização 12 do Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="36010-103">Project Service Automation Update Release 12, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="36010-104">Temos o prazer de anunciar a atualização mais recente para a aplicação Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="36010-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="36010-105">Esta versão inclui algumas melhorias importantes na qualidade, desempenho e utilização.</span><span class="sxs-lookup"><span data-stu-id="36010-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="36010-106">Esta versão é compatível com o Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="36010-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="36010-107">Para atualizar esta versão, visite o Centro de Administração para o Dynamics 365 online e aceda à página de soluções para instalar a atualização.</span><span class="sxs-lookup"><span data-stu-id="36010-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="36010-108">Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="36010-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="36010-109">Este tópico lista as funcionalidades e correções novas ou alteradas para o Project Service Automation V3, Versão da Atualização 12.</span><span class="sxs-lookup"><span data-stu-id="36010-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 12.</span></span> <span data-ttu-id="36010-110">Esta versão tem um número de compilação de V3.10.2.34 e está geralmente disponível através de uma Atualização automática em outubro de 2019.</span><span class="sxs-lookup"><span data-stu-id="36010-110">This version has a build number of V3.10.2.34 and is generally available through a self-update in October 2019.</span></span>

## <a name="update-release-12"></a><span data-ttu-id="36010-111">Versão da Atualização 12</span><span class="sxs-lookup"><span data-stu-id="36010-111">Update Release 12</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="36010-112">Correções de erros</span><span class="sxs-lookup"><span data-stu-id="36010-112">Bug fixes</span></span>

- <span data-ttu-id="36010-113">Tempo e Despesa</span><span class="sxs-lookup"><span data-stu-id="36010-113">Time and Expense</span></span>

    - <span data-ttu-id="36010-114">Corrigido: a mensagem de erro de entrada de tempo foi atualizada com um contexto mais relevante.</span><span class="sxs-lookup"><span data-stu-id="36010-114">Fixed: Time entry error messaging has been updated with more relevant context.</span></span>
    - <span data-ttu-id="36010-115">Corrigido: a grelha de hora de entrada e a agenda apresentam corretamente a barra de deslocamento vertical quando necessário.</span><span class="sxs-lookup"><span data-stu-id="36010-115">Fixed: Time entry grid and schedule correctly displays the vertical scrollbar when required.</span></span>
    - <span data-ttu-id="36010-116">Corrigido: entradas de despesas e de hora submetidas podem ser aprovadas.</span><span class="sxs-lookup"><span data-stu-id="36010-116">Fixed: Submitted expense and time entries can be approved.</span></span>
    - <span data-ttu-id="36010-117">Corrigido: a mensagem de diálogo Cancelar confirmação de aprovação foi corrigida para refletir o estado da aprovação quando alterado de **Aprovada** para **Submetida**.</span><span class="sxs-lookup"><span data-stu-id="36010-117">Fixed: Cancel approval confirmation dialog message has been corrected to reflect the status of the approval when changed from **Approved** to **Submitted**.</span></span>
    - <span data-ttu-id="36010-118">Corrigido: os campos **Preço**, **Unidade** e **Quantidade** agora estão bloqueados no registo Despesas depois de terem sido aprovados.</span><span class="sxs-lookup"><span data-stu-id="36010-118">Fixed: **Price**, **Unit**, and **Quantity** fields are now locked on the Expense record after it is has been approved.</span></span>

- <span data-ttu-id="36010-119">Gestão de Projetos</span><span class="sxs-lookup"><span data-stu-id="36010-119">Project Management</span></span>

    - <span data-ttu-id="36010-120">Corrigido: a ação **Nova** no formulário principal **Membro da equipa** foi removida.</span><span class="sxs-lookup"><span data-stu-id="36010-120">Fixed: **New** action on **Team member** main form has been removed.</span></span>
    - <span data-ttu-id="36010-121">Corrigido: as atribuições de recursos foram atualizadas para considerar erros de arredondamento imprecisos, que resultavam em mudanças na data de fim de uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="36010-121">Fixed: Resource assignments have been updated to account for inaccurate rounding errors, which lead to a shift in a task’s end date.</span></span>
    - <span data-ttu-id="36010-122">Corrigido: na grelha de tarefas, os erros relevantes do lado do servidor serão apresentados ao utilizador.</span><span class="sxs-lookup"><span data-stu-id="36010-122">Fixed: In the task grid, relevant server-side errors will be surfaced to the user.</span></span>
    - <span data-ttu-id="36010-123">Corrigido: o nome do membro da equipa agora é composto no seletor de pessoas da tarefa em vez de no nome da posição.</span><span class="sxs-lookup"><span data-stu-id="36010-123">Fixed: The team member’s name now renders in the task people picker instead of the position name.</span></span>

- <span data-ttu-id="36010-124">Gestão de Recursos</span><span class="sxs-lookup"><span data-stu-id="36010-124">Resource Management</span></span>

    - <span data-ttu-id="36010-125">Corrigido: os detalhes do requisito de recurso para projetos criados a partir de um modelo agora utilizam o calendário do projeto.</span><span class="sxs-lookup"><span data-stu-id="36010-125">Fixed: Resource requirement details for projects created from a template now use the project calendar.</span></span>
    - <span data-ttu-id="36010-126">Corrigido: as qualificações e competências agora são predefinidas a partir dos dados principais de função para o requisito de recurso criado para essa função.</span><span class="sxs-lookup"><span data-stu-id="36010-126">Fixed: Skills and competencies now default from role master data to the resource requirement created for that role.</span></span>

- <span data-ttu-id="36010-127">Sales</span><span class="sxs-lookup"><span data-stu-id="36010-127">Sales</span></span>

    - <span data-ttu-id="36010-128">Corrigido: IDs de objetos duplicados no formulário **Principal do contrato**.</span><span class="sxs-lookup"><span data-stu-id="36010-128">Fixed: Duplicate object IDs found on the **Contract main** form.</span></span>
    - <span data-ttu-id="36010-129">Corrigido: a lógica foi atualizada para tornar visível o separador **Análise de Proposta**, de modo a apresentar a configuração de metadados do separador.</span><span class="sxs-lookup"><span data-stu-id="36010-129">Fixed: Logic has been updated to make the **Quote Analysis** tab visible so that it displays the metadata setup of the tab.</span></span>
    - <span data-ttu-id="36010-130">Corrigido: a data contabilística do registo real agora provém da data da hora da entrada da hora/despesa e não da data de aprovação.</span><span class="sxs-lookup"><span data-stu-id="36010-130">Fixed: Accounting date on the actual record now comes from the date of the time/expense entry date and not the date of the approval.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]