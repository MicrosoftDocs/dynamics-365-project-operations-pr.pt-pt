---
title: Novidades ou alterações na Versão da Atualização 18 do Project Service Automation, V3
description: Este tópico lista as funcionalidades e correções disponíveis no Project Service Automation V3, Versão da Atualização 18, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
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
ms.openlocfilehash: 3a6d3ee21ecf742b2253132f3d3cc1cb2b57af75
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119882"
---
# <a name="project-service-automation-update-release-18-v3"></a><span data-ttu-id="1bd8a-103">Versão da Atualização 18 do Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="1bd8a-103">Project Service Automation Update Release 18, V3</span></span>

<span data-ttu-id="1bd8a-104">Temos o prazer de anunciar a mais recente atualização à aplicação Project Service Automation para Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="1bd8a-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="1bd8a-105">Esta versão inclui algumas melhorias importantes na qualidade, desempenho e utilização.</span><span class="sxs-lookup"><span data-stu-id="1bd8a-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="1bd8a-106">Esta versão é compatível com o Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="1bd8a-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="1bd8a-107">Para atualizar esta versão, visite o Centro de Administração para o Dynamics 365 online e aceda à página de soluções para instalar a atualização.</span><span class="sxs-lookup"><span data-stu-id="1bd8a-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="1bd8a-108">Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="1bd8a-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="1bd8a-109">Este tópico lista as funcionalidades e correções novas ou alteradas para o Project Service Automation V3, Versão da Atualização 18.</span><span class="sxs-lookup"><span data-stu-id="1bd8a-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 18.</span></span> <span data-ttu-id="1bd8a-110">Esta versão tem o número de compilação V3.10.8.12 e está geralmente disponível através de uma atualização automática em abril de 2020.</span><span class="sxs-lookup"><span data-stu-id="1bd8a-110">This version has a build number of V3.10.8.12 and is generally available through a self-update in April 2020.</span></span>

## <a name="update-release-18"></a><span data-ttu-id="1bd8a-111">Versão da Atualização 18</span><span class="sxs-lookup"><span data-stu-id="1bd8a-111">Update Release 18</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="1bd8a-112">Correções de erros</span><span class="sxs-lookup"><span data-stu-id="1bd8a-112">Bug fixes</span></span>

<span data-ttu-id="1bd8a-113">**Tempo e Despesa**</span><span class="sxs-lookup"><span data-stu-id="1bd8a-113">**Time and Expense**</span></span>

- <span data-ttu-id="1bd8a-114">Corrigido: os fluxos **Revocar**, **Pedir** e **Cancelar Aprovação** lançam exceções com mensagens de erro ambíguas.</span><span class="sxs-lookup"><span data-stu-id="1bd8a-114">Fixed: **Recall**, **Request**, and **Cancel Approval** flows throw exceptions with unclear error messages.</span></span>
- <span data-ttu-id="1bd8a-115">Corrigido: quando **Cancelar Aprovação** falha para uma despesa, um erro de exceção relevante não é lançado.</span><span class="sxs-lookup"><span data-stu-id="1bd8a-115">Fixed: When **Cancel Approval** fails for an expense, a relevant exception error is not thrown.</span></span>
- <span data-ttu-id="1bd8a-116">Corrigido: a grelha Entrada de Hora processa incorretamente dias não úteis na Austrália após a mudança para a hora de verão (DST) em outubro.</span><span class="sxs-lookup"><span data-stu-id="1bd8a-116">Fixed: The Time Entry grid incorrectly handles non-working days in Australia after the daylight savings time (DST) switch in October.</span></span>
- <span data-ttu-id="1bd8a-117">Corrigido: a lógica de definição incorreta impede o envio de despesas.</span><span class="sxs-lookup"><span data-stu-id="1bd8a-117">Fixed: Incorrect defaulting logic prevents submission of expenses.</span></span>
- <span data-ttu-id="1bd8a-118">Corrigido: quando a aprovação da entrada de hora falha, a aprovação permanece num estado de **Pendente**.</span><span class="sxs-lookup"><span data-stu-id="1bd8a-118">Fixed: When time entry approval fails, the approval remains in a state of **Pending**.</span></span>
- <span data-ttu-id="1bd8a-119">Corrigido: erros SQL em aprovações em massa (impasse/tempo limite).</span><span class="sxs-lookup"><span data-stu-id="1bd8a-119">Fixed: SQL Errors on bulk approvals (deadlock/timeout).</span></span>
- <span data-ttu-id="1bd8a-120">Corrigido: problemas de desempenho significativos na experiência do utilizador causados pela atualização de membros da equipa durante a aprovação das entradas de hora.</span><span class="sxs-lookup"><span data-stu-id="1bd8a-120">Fixed: Significant performance issues in the user experience caused by updating team members while approving time entries.</span></span>

<span data-ttu-id="1bd8a-121">**Gestão de Projetos**</span><span class="sxs-lookup"><span data-stu-id="1bd8a-121">**Project Management**</span></span>

- <span data-ttu-id="1bd8a-122">Corrigido: a notificação de fuso horário moveu-se da vista **Reconciliação** para o formulário principal **Projeto**.</span><span class="sxs-lookup"><span data-stu-id="1bd8a-122">Fixed: Time zone notification moved from the **Reconciliation** view to the **Project** main form.</span></span>
- <span data-ttu-id="1bd8a-123">Corrigido: o modelo de calendário não é predefinido corretamente quando é aberto um novo formulário de projeto.</span><span class="sxs-lookup"><span data-stu-id="1bd8a-123">Fixed: Calendar template is not correctly defaulting when a new project form opens.</span></span>
- <span data-ttu-id="1bd8a-124">Corrigido: para browsers baseados em chromium, os utilizadores não conseguem selecionar facilmente as tarefas predecessoras a eliminar.</span><span class="sxs-lookup"><span data-stu-id="1bd8a-124">Fixed: For chromium-based browsers, users are unable to easily select predecessor tasks to delete.</span></span>
- <span data-ttu-id="1bd8a-125">Corrigido: a criação ou copia do **Projeto a partir de Modelo Vazio** obtém atribuições não relacionadas.</span><span class="sxs-lookup"><span data-stu-id="1bd8a-125">Fixed: Creating or copying **Project from Empty template** fetches unrelated assignments.</span></span>
- <span data-ttu-id="1bd8a-126">Corrigido: em casos específicos do Edge, a criação de uma nova atribuição a partir da grelha de tarefas resulta na criação de registos duplicados.</span><span class="sxs-lookup"><span data-stu-id="1bd8a-126">Fixed: In specific edge cases, creating a new assignment from the task grid results in duplicate records being created.</span></span>
- <span data-ttu-id="1bd8a-127">Corrigido: no modo manual, os utilizadores não conseguem atualizar as datas de início das tarefas para serem posteriores à data atual guardada.</span><span class="sxs-lookup"><span data-stu-id="1bd8a-127">Fixed: In manual mode, users are unable to update task start dates to be later than the current date saved.</span></span>

<span data-ttu-id="1bd8a-128">**Gestão de Recursos**</span><span class="sxs-lookup"><span data-stu-id="1bd8a-128">**Resource Management**</span></span>

- <span data-ttu-id="1bd8a-129">Corrigido: a linha de subtotal da vista de **Reconciliação** calcula incorretamente a variância das reservas após a extensão de reservas.</span><span class="sxs-lookup"><span data-stu-id="1bd8a-129">Fixed: **Reconciliation** view subtotal row incorrectly calculates bookings variance after extending bookings.</span></span>
- <span data-ttu-id="1bd8a-130">Corrigido: a vista de **Reconciliação** apresenta incorretamente as atribuições de recursos quando o recurso que é agendado tem um calendário que não corresponde ao calendário do projeto.</span><span class="sxs-lookup"><span data-stu-id="1bd8a-130">Fixed: **Reconciliation** view incorrectly displays resource assignments when the bookable resource has a calendar that does not match the project calendar.</span></span>

<span data-ttu-id="1bd8a-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="1bd8a-131">**Sales**</span></span>

- <span data-ttu-id="1bd8a-132">Corrigido: quando as entradas de hora são reaprovadas (**Aprovar > Cancelar >** são aprovadas novamente), é criado um valor real não cobrável duplicado.</span><span class="sxs-lookup"><span data-stu-id="1bd8a-132">Fixed: When time entries are re-approved (**Approve > Cancel >** approve again), a duplicate non-chargeable actual is created.</span></span>
