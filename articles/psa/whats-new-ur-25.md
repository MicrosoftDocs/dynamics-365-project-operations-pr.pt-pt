---
title: Novidades ou alterações na Versão da Atualização 25 do Project Service Automation, V3
description: Este tópico lista as funcionalidades e correções disponíveis no Project Service Automation V3, Versão da Atualização 25, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
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
ms.openlocfilehash: a5a81893c4a804deb09cf33e0ac3f1a25b8bca36
ms.sourcegitcommit: a2b810219d381716d3eedb14c4eb6cdefb5b5845
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 11/02/2020
ms.locfileid: "4183557"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a><span data-ttu-id="cc26f-103">Novidades ou alterações na Versão da Atualização 25 do Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="cc26f-103">What's new or changed in Project Service Automation Update Release 25, V3</span></span>

<span data-ttu-id="cc26f-104">Temos o prazer de anunciar a mais recente atualização à aplicação Project Service Automation para Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="cc26f-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="cc26f-105">Esta versão inclui algumas melhorias importantes na qualidade, desempenho e utilização.</span><span class="sxs-lookup"><span data-stu-id="cc26f-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="cc26f-106">Esta versão é compatível com o Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="cc26f-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="cc26f-107">Para atualizar esta versão, visite o Centro de Administração para o Dynamics 365 online e aceda à página de soluções para instalar a atualização.</span><span class="sxs-lookup"><span data-stu-id="cc26f-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="cc26f-108">Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="cc26f-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="cc26f-109">Este tópico lista as funcionalidades e correções novas ou alteradas para o Project Service Automation V3, Versão de Atualização 25 – esta versão tem um número de compilação V 3.10.43.76 e está geralmente disponível através de uma atualização automática em outubro de 2020.</span><span class="sxs-lookup"><span data-stu-id="cc26f-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 25 This version has a build number of V 3.10.43.76 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-25"></a><span data-ttu-id="cc26f-110">Versão da Atualização 25</span><span class="sxs-lookup"><span data-stu-id="cc26f-110">Update Release 25</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="cc26f-111">Correções de erros</span><span class="sxs-lookup"><span data-stu-id="cc26f-111">Bug fixes</span></span>

<span data-ttu-id="cc26f-112">**Tempo e Despesa**</span><span class="sxs-lookup"><span data-stu-id="cc26f-112">**Time and Expense**</span></span>

<span data-ttu-id="cc26f-113">O seguinte problema foi corrigido:</span><span class="sxs-lookup"><span data-stu-id="cc26f-113">The following issue has been fixed:</span></span>

- <span data-ttu-id="cc26f-114">Gráfico de entrada de tempo que mostra dados adicionais baseados num intervalo demasiado grande a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="cc26f-114">Time entry chart showing additional data based on too large of an interval being retrieved.</span></span>

<span data-ttu-id="cc26f-115">**Gestão de Recursos**</span><span class="sxs-lookup"><span data-stu-id="cc26f-115">**Resource Management**</span></span>

<span data-ttu-id="cc26f-116">O seguinte problema foi corrigido:</span><span class="sxs-lookup"><span data-stu-id="cc26f-116">The following issue has been fixed:</span></span>

- <span data-ttu-id="cc26f-117">Código do Package Deployer adicionado para ignorar a importação do patch do Universal Resource Scheduling se já existir uma versão do patch mais alta.</span><span class="sxs-lookup"><span data-stu-id="cc26f-117">Added package deployer code to skip the Universal Resource Scheduling patch import if a higher version patch already exists.</span></span>

<span data-ttu-id="cc26f-118">**Gestão de Projetos**</span><span class="sxs-lookup"><span data-stu-id="cc26f-118">**Project Management**</span></span>

<span data-ttu-id="cc26f-119">Foram corrigidos os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="cc26f-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="cc26f-120">Discrepâncias de arredondamento e taxas de câmbio corrigidas, resultando num custo planeado incorreto na grelha de monitorização do projeto.</span><span class="sxs-lookup"><span data-stu-id="cc26f-120">Corrected rounding and exchange rate discrepancies resulting in incorrect planned cost in the project tracking grid.</span></span>
- <span data-ttu-id="cc26f-121">Suporte a capacidade de exibir duas ou mais grelhas de reação no formulário **Projeto**.</span><span class="sxs-lookup"><span data-stu-id="cc26f-121">Support the ability to display two or more react grids on the **Project** form.</span></span>
- <span data-ttu-id="cc26f-122">Fornecida a validação para resolver a capacidade de atribuir uma tarefa para além da data de fim do calendário, o que resulta numa atribuição falhada de recursos.</span><span class="sxs-lookup"><span data-stu-id="cc26f-122">Provided validation to address the ability to assign a task past the calendar end date, which results in a failed resource assignment.</span></span>
- <span data-ttu-id="cc26f-123">Manuseamento de erros melhorado para resolver Exceção de Referência nula gerada a partir do seguinte:</span><span class="sxs-lookup"><span data-stu-id="cc26f-123">Improved error handling to address Null Reference Exception generated from the following:</span></span>

    - <span data-ttu-id="cc26f-124">Plug-in **PreValidateProjectTeamMemberCreate**</span><span class="sxs-lookup"><span data-stu-id="cc26f-124">**PreValidateProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="cc26f-125">**PreValidateProjectTaskCreate** quando uma tarefa de projeto é criada sem um projeto associado</span><span class="sxs-lookup"><span data-stu-id="cc26f-125">**PreValidateProjectTaskCreate** when a project task is created without an associated project</span></span>
    - <span data-ttu-id="cc26f-126">Plug-in **PreProjectTeamMemberCreate**</span><span class="sxs-lookup"><span data-stu-id="cc26f-126">**PreProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="cc26f-127">Plug-in **PostProjectTeamMemberDelete**</span><span class="sxs-lookup"><span data-stu-id="cc26f-127">**PostProjectTeamMemberDelete** plug-in</span></span>
    - <span data-ttu-id="cc26f-128">Plug-in **PreValidateProjectTaskDelete**</span><span class="sxs-lookup"><span data-stu-id="cc26f-128">**PreValidateProjectTaskDelete** plug-in</span></span>

<span data-ttu-id="cc26f-129">**Sales**</span><span class="sxs-lookup"><span data-stu-id="cc26f-129">**Sales**</span></span>

<span data-ttu-id="cc26f-130">Foram corrigidos os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="cc26f-130">The following issues have been fixed:</span></span>

- <span data-ttu-id="cc26f-131">Manuseamento de erros melhorado para resolver Exceções de Referência Nulas geradas pelo **Copiar Projeto: Estimativa de Gestão do HelperResource**.</span><span class="sxs-lookup"><span data-stu-id="cc26f-131">Improved error handling to address Null Reference Exceptions generated from **Copy Project: Estimates HelperResource Management**.</span></span>
- <span data-ttu-id="cc26f-132">**Não está pronto a Faturar** num **Registo de Tarefas Pendentes de Faturação de Tempo e Material** não limpa o estado da faturação.</span><span class="sxs-lookup"><span data-stu-id="cc26f-132">**Not ready to Invoice** on a **Time and Material Billing Backlog** doesn't clear the billing status.</span></span>
- <span data-ttu-id="cc26f-133">Corrigida a colocação errada de etiquetas dos botões **Preços** no separador **Preço de Função** e **Itens de Catálogo**.</span><span class="sxs-lookup"><span data-stu-id="cc26f-133">Corrected mislabeled **Prices** buttons on the **Role Price** and **Catalog Items** tab.</span></span>
