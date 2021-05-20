---
title: Novidades ou alterações na Versão da Atualização 15 do Project Service Automation, V3
description: Esta tópico fornece informações sobre o que há de novo na Versão da Atualização 15 do Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
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
ms.openlocfilehash: fe1e2b2046faeee4e4c71484a976d70e8722e090
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949333"
---
# <a name="project-service-automation-update-release-15-v3"></a><span data-ttu-id="84b1b-103">Versão da Atualização 15 do Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="84b1b-103">Project Service Automation Update Release 15, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="84b1b-104">Temos o prazer de anunciar a atualização mais recente para a aplicação Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="84b1b-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="84b1b-105">Esta versão inclui algumas melhorias importantes na qualidade, desempenho e utilização.</span><span class="sxs-lookup"><span data-stu-id="84b1b-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="84b1b-106">Esta versão é compatível com o Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="84b1b-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="84b1b-107">Para atualizar esta versão, visite o Centro de Administração para o Dynamics 365 online e aceda à página de soluções para instalar a atualização.</span><span class="sxs-lookup"><span data-stu-id="84b1b-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="84b1b-108">Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="84b1b-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="84b1b-109">Este tópico lista as funcionalidades e correções novas ou alteradas para o PSA V3, Versão da Atualização 15.</span><span class="sxs-lookup"><span data-stu-id="84b1b-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 15.</span></span> <span data-ttu-id="84b1b-110">Esta versão tem um número de compilação de V3.10.5.28 e está geralmente disponível através de uma Atualização automática em janeiro de 2020.</span><span class="sxs-lookup"><span data-stu-id="84b1b-110">This version has a build number of V3.10.5.28 and is generally available through a self-update in January 2020.</span></span>

## <a name="update-release-15"></a><span data-ttu-id="84b1b-111">Versão da Atualização 15</span><span class="sxs-lookup"><span data-stu-id="84b1b-111">Update Release 15</span></span> 

### <a name="enhancements"></a><span data-ttu-id="84b1b-112">Melhorias</span><span class="sxs-lookup"><span data-stu-id="84b1b-112">Enhancements</span></span>

- <span data-ttu-id="84b1b-113">Gestão de Projetos</span><span class="sxs-lookup"><span data-stu-id="84b1b-113">Project Management</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="84b1b-114">Correções de erros</span><span class="sxs-lookup"><span data-stu-id="84b1b-114">Bug fixes</span></span>

- <span data-ttu-id="84b1b-115">Tempo e Despesa</span><span class="sxs-lookup"><span data-stu-id="84b1b-115">Time and Expense</span></span>

  - <span data-ttu-id="84b1b-116">Corrigido: Adicione a manipulação de erros no carregamento na vista de reconciliação.</span><span class="sxs-lookup"><span data-stu-id="84b1b-116">Fixed: Add on-load error handling in the reconciliation view.</span></span>
  - <span data-ttu-id="84b1b-117">Corrigido: Hub de Recursos de Projeto: renomeiar **Quantidade** para reduzir a ambiguidade.</span><span class="sxs-lookup"><span data-stu-id="84b1b-117">Fixed: Project Resource Hub: Rename **Amount** to reduce ambiguity.</span></span>
  - <span data-ttu-id="84b1b-118">Corrigido: ajuste a vista **Copiar Colunas de Entrada de Hora** para incluir o tipo.</span><span class="sxs-lookup"><span data-stu-id="84b1b-118">Fixed: Adjust the view **Copy Time Entry Columns** to include the type.</span></span>
  - <span data-ttu-id="84b1b-119">Corrigido: a edição da duração da entrada de tempo na vista de grelha utilizando números decimais resulta em erro desconhecido para alguns números.</span><span class="sxs-lookup"><span data-stu-id="84b1b-119">Fixed: Editing time entry duration in the grid view using decimal numbers results in unknown error for some numbers.</span></span>

- <span data-ttu-id="84b1b-120">Gestão de Projetos</span><span class="sxs-lookup"><span data-stu-id="84b1b-120">Project Management</span></span>

  - <span data-ttu-id="84b1b-121">Corrigido: o menu pendente para **Utilização na Vista de Monitorização** expande-se agora com base na largura das opções.</span><span class="sxs-lookup"><span data-stu-id="84b1b-121">Fixed: The drop-down menu for **Use in Tracking View** now expands based on the width of the options.</span></span>
  - <span data-ttu-id="84b1b-122">Corrigido: quando gerir projetos no fuso horário de +13, os cálculos das tarefas podem apresentar resultados imprecisos.</span><span class="sxs-lookup"><span data-stu-id="84b1b-122">Fixed: When managing projects in the +13 time zone, tasks calculations can display inaccurate results.</span></span>
  - <span data-ttu-id="84b1b-123">Corrigido: a **Hora de fim do membro da equipa** foi corrigida ao utilizar um calendário de 24 horas.</span><span class="sxs-lookup"><span data-stu-id="84b1b-123">Fixed: **Team Member End Time** has been corrected when using a 24-hour calendar.</span></span>
  - <span data-ttu-id="84b1b-124">Corrigido: reativado o **BPF** no formulário principal **msdyn_project**.</span><span class="sxs-lookup"><span data-stu-id="84b1b-124">Fixed: Re-activated the **BPF** in **msdyn_project** main form.</span></span>
  - <span data-ttu-id="84b1b-125">Corrigido: o cálculo de atribuições deixa de ignorar um dia.</span><span class="sxs-lookup"><span data-stu-id="84b1b-125">Fixed: Assignments calculation no longer ignores one day.</span></span>
  - <span data-ttu-id="84b1b-126">Corrigido: foi adicionada uma nova faixa de notificação ao formulário do projeto quando o fuso horário é diferente entre o utilizador e o projeto.</span><span class="sxs-lookup"><span data-stu-id="84b1b-126">Fixed: A new notification banner has been added to the project form when the time zone differs between user and project.</span></span>

- <span data-ttu-id="84b1b-127">Sales</span><span class="sxs-lookup"><span data-stu-id="84b1b-127">Sales</span></span>

  - <span data-ttu-id="84b1b-128">Corrigido: a pesquisa de categorias de estimativa de despesas pode ser utilizada para filtrar duplicados.</span><span class="sxs-lookup"><span data-stu-id="84b1b-128">Fixed: Expense estimate category lookup can be used to filter duplicates.</span></span>
  - <span data-ttu-id="84b1b-129">Corrigido: código em **PluginDomain.ExecuteInTryCatchBlock(..)** já não oculta a origem da exceção.</span><span class="sxs-lookup"><span data-stu-id="84b1b-129">Fixed: Code in **PluginDomain.ExecuteInTryCatchBlock(..)** no longer hides the origin of the exception.</span></span>
  - <span data-ttu-id="84b1b-130">Corrigido: já não obtém uma mensagem de erro na **Pesquisa de projeto** no formulário **Linha da Proposta** quando existem mais de 1000 projetos.</span><span class="sxs-lookup"><span data-stu-id="84b1b-130">Fixed: No longer get an error message in **Project lookup** in the **Quote Line** form when there are more than 1000 projects.</span></span>
  - <span data-ttu-id="84b1b-131">Corrigido: a grelha **Estimativas** para estimativas de mão-de-obra e estimativas de despesas apresenta agora o símbolo de moeda correto.</span><span class="sxs-lookup"><span data-stu-id="84b1b-131">Fixed: **Estimates** grid for labor estimates and expense estimates now displays the correct currency symbol.</span></span>
  - <span data-ttu-id="84b1b-132">Corrigido: depois de uma organização atualizar o PSA da Versão da Atualização 14 para a Versão da Atualização 15, o separador **Agenda** deixa de aparecer como em branco no formulário **Projeto**.</span><span class="sxs-lookup"><span data-stu-id="84b1b-132">Fixed: After an organization updates PSA from Update Release 14 to Update Release 15, the **Schedule** tab no longer appears as blank on the **Project** form.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]