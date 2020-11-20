---
title: Novidades ou alterações na Versão da Atualização 23 do Project Service Automation, V3
description: Este tópico lista as funcionalidades e correções disponíveis no Project Service Automation V3, Versão da Atualização 23, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 08/25/2020
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
ms.openlocfilehash: 07f1a274914d7e641ddf2fd42f377dce1da7f815
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131132"
---
# <a name="project-service-automation-update-release-23-v3"></a><span data-ttu-id="6c0c4-103">Versão da Atualização 23 do Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="6c0c4-103">Project Service Automation Update Release 23, V3</span></span>

<span data-ttu-id="6c0c4-104">Temos o prazer de anunciar a mais recente atualização à aplicação Project Service Automation para Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="6c0c4-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="6c0c4-105">Esta versão inclui algumas melhorias importantes na qualidade, desempenho e utilização.</span><span class="sxs-lookup"><span data-stu-id="6c0c4-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="6c0c4-106">Esta versão é compatível com o Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="6c0c4-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="6c0c4-107">Para atualizar esta versão, visite o Centro de Administração para o Dynamics 365 online e aceda à página de soluções para instalar a atualização.</span><span class="sxs-lookup"><span data-stu-id="6c0c4-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="6c0c4-108">Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="6c0c4-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="6c0c4-109">Este tópico lista as funcionalidades e correções novas ou alteradas para o Project Service Automation V3, Versão da Atualização 23.</span><span class="sxs-lookup"><span data-stu-id="6c0c4-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 23.</span></span> <span data-ttu-id="6c0c4-110">Esta versão tem um número de compilação de V 3.10.34.30 e está geralmente disponível através de uma Atualização automática em agosto de 2020.</span><span class="sxs-lookup"><span data-stu-id="6c0c4-110">This version has a build number of V 3.10.34.30 and is generally available through a self-update in August 2020.</span></span>

## <a name="update-release-23"></a><span data-ttu-id="6c0c4-111">Versão da Atualização 23</span><span class="sxs-lookup"><span data-stu-id="6c0c4-111">Update Release 23</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="6c0c4-112">Correções de erros</span><span class="sxs-lookup"><span data-stu-id="6c0c4-112">Bug fixes</span></span>

<span data-ttu-id="6c0c4-113">**Tempo e Despesa**</span><span class="sxs-lookup"><span data-stu-id="6c0c4-113">**Time and Expense**</span></span>

<span data-ttu-id="6c0c4-114">Foram corrigidos os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="6c0c4-114">The following issues have been fixed:</span></span>
- <span data-ttu-id="6c0c4-115">Lidar com o caso da borda em **Eliminação de Membro da Equipa de Projeto** para fornecer uma exceção significativa.</span><span class="sxs-lookup"><span data-stu-id="6c0c4-115">Handle edge case in **Project Team Member Delete** to provide a meaningful exception.</span></span>
- <span data-ttu-id="6c0c4-116">A importação de atribuição resulta num ecrã de remoção em branco.</span><span class="sxs-lookup"><span data-stu-id="6c0c4-116">Assignment import results in a blank remove screen.</span></span>

<span data-ttu-id="6c0c4-117">**Gestão de Recursos**</span><span class="sxs-lookup"><span data-stu-id="6c0c4-117">**Resource Management**</span></span>

<span data-ttu-id="6c0c4-118">Foram corrigidos os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="6c0c4-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="6c0c4-119">O **Cartão de recursos da grelha de utilização de recursos** mostra dados incorretos quando a escala de tempo é superior a cinco dias.</span><span class="sxs-lookup"><span data-stu-id="6c0c4-119">The **Resource utilization grid resource card** shows incorrect data when the time scale is more than five days.</span></span>
- <span data-ttu-id="6c0c4-120">Quando os clientes criam um recurso reservado, o plug-in falha intermitentemente ao adicionar automaticamente o recurso a um grupo do Microsoft Office 365.</span><span class="sxs-lookup"><span data-stu-id="6c0c4-120">When customers create a bookable resource, the plug-in intermittently fails to automatically add the resource to a Microsoft Office 365 group.</span></span>
- <span data-ttu-id="6c0c4-121">A vista **Reconciliação** apresenta contornos manuais incorretamente na vista **Semana** ou **Mês**.</span><span class="sxs-lookup"><span data-stu-id="6c0c4-121">**Reconciliation** view displays manual contours incorrectly in the **Week** or **Month** view.</span></span>

<span data-ttu-id="6c0c4-122">**Gestão de Projetos**</span><span class="sxs-lookup"><span data-stu-id="6c0c4-122">**Project Management**</span></span>

<span data-ttu-id="6c0c4-123">Foram corrigidos os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="6c0c4-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="6c0c4-124">Um número excessivo de entidades **RetrieveMultiple para usersettings** está a causar um desempenho degradado para aprovações de projetos e outras operações.</span><span class="sxs-lookup"><span data-stu-id="6c0c4-124">An excessive number of **RetrieveMultiple for usersettings** entities are causing degraded performance for project approvals and other operations.</span></span>
- <span data-ttu-id="6c0c4-125">A pesquisa de recursos da grelha **Planeamento de Tarefas** está limitada a apenas cinco membros da equipa do projeto.</span><span class="sxs-lookup"><span data-stu-id="6c0c4-125">The **Task Planning** grid resource lookup is limited to only show up to five team members from the project team.</span></span> 
- <span data-ttu-id="6c0c4-126">A pesquisa de recursos da grelha **Planeamento de Tarefas** não filtra recursos inativos.</span><span class="sxs-lookup"><span data-stu-id="6c0c4-126">The **Task Planning** grid resource lookup does not filter inactive resources.</span></span>
- <span data-ttu-id="6c0c4-127">O modo manual não está a funcionar como esperado na estrutura hierárquica do trabalho de planeamento do projeto.</span><span class="sxs-lookup"><span data-stu-id="6c0c4-127">Manual mode is not working as expected in the project planning work breakdown structure.</span></span>
- <span data-ttu-id="6c0c4-128">A grelha **Planeamento de Tarefas** mostra **Categorias de Transação Inativas**.</span><span class="sxs-lookup"><span data-stu-id="6c0c4-128">The **Task Planning** grid shows **Inactive Transaction Categories**.</span></span>
- <span data-ttu-id="6c0c4-129">A grelha **Atribuição de Recursos** arredonda incorretamente quando uma tarefa tem várias atribuições.</span><span class="sxs-lookup"><span data-stu-id="6c0c4-129">The **Resource Assignment** grid rounds incorrectly when a task has multiple assignments.</span></span>
- <span data-ttu-id="6c0c4-130">Os valores de arredondamento são diferentes entre o custo planeado e o custo real para uma única tarefa.</span><span class="sxs-lookup"><span data-stu-id="6c0c4-130">Rounding values are different between planned cost and actual cost for a single task.</span></span>

<span data-ttu-id="6c0c4-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="6c0c4-131">**Sales**</span></span>

<span data-ttu-id="6c0c4-132">Foram corrigidos os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="6c0c4-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="6c0c4-133">Clicar duas vezes em **Obter Todas as Categorias de Transações** cria várias linhas.</span><span class="sxs-lookup"><span data-stu-id="6c0c4-133">**Fetch All Transaction Categories** double-click creates multiple lines.</span></span>
