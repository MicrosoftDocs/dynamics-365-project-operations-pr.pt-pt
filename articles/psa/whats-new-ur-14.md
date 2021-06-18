---
title: Novidades ou alterações na Versão da Atualização 14 do Project Service Automation, V3
description: Esta tópico fornece informações sobre o que há de novo na Versão da Atualização 14 do Project Service Automation V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
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
ms.openlocfilehash: 8754f8eace50f1fa5743c5611d94f8c86693ebc9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006885"
---
# <a name="project-service-automation-update-release-14-v3"></a><span data-ttu-id="e8ee2-103">Versão da Atualização 14 do Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="e8ee2-103">Project Service Automation Update Release 14, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="e8ee2-104">Temos o prazer de anunciar a atualização mais recente para a aplicação Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="e8ee2-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="e8ee2-105">Esta versão inclui algumas melhorias importantes na qualidade, desempenho e utilização.</span><span class="sxs-lookup"><span data-stu-id="e8ee2-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="e8ee2-106">Esta versão é compatível com o Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="e8ee2-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="e8ee2-107">Para atualizar esta versão, visite o Centro de Administração para o Dynamics 365 online e aceda à página de soluções para instalar a atualização.</span><span class="sxs-lookup"><span data-stu-id="e8ee2-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="e8ee2-108">Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="e8ee2-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="e8ee2-109">Este tópico lista as funcionalidades e correções novas ou alteradas para o PSA V3, Versão da Atualização 14.</span><span class="sxs-lookup"><span data-stu-id="e8ee2-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 14.</span></span> <span data-ttu-id="e8ee2-110">Esta versão tem um número de compilação de V3.10.4.21 e está disponível na seguinte agenda:</span><span class="sxs-lookup"><span data-stu-id="e8ee2-110">This version has a build number of V3.10.4.21 and is available on the following schedule:</span></span>

- <span data-ttu-id="e8ee2-111">**Disponibilidade geral (Atualização automática):** janeiro de 2020</span><span class="sxs-lookup"><span data-stu-id="e8ee2-111">**General availability (self-update):** January 2020</span></span>
- <span data-ttu-id="e8ee2-112">**Atualização automática:** fevereiro de 2020</span><span class="sxs-lookup"><span data-stu-id="e8ee2-112">**Auto-update:** February 2020</span></span>

## <a name="update-release-14"></a><span data-ttu-id="e8ee2-113">Versão da Atualização 14</span><span class="sxs-lookup"><span data-stu-id="e8ee2-113">Update Release 14</span></span>

### <a name="enhancements"></a><span data-ttu-id="e8ee2-114">Melhorias</span><span class="sxs-lookup"><span data-stu-id="e8ee2-114">Enhancements</span></span>

- <span data-ttu-id="e8ee2-115">Sales</span><span class="sxs-lookup"><span data-stu-id="e8ee2-115">Sales</span></span>

     - <span data-ttu-id="e8ee2-116">Os valores de campos personalizados de **Detalhes da Linha da Proposta** são copiados para os **Detalhes do Item de Contrato do Projeto** quando uma proposta é atualizada para **Fechada como ganha**.</span><span class="sxs-lookup"><span data-stu-id="e8ee2-116">Custom field values from **Quote Line Details** are copied to **Project Contract Line Details** when a quote is updated to **Closed as won**.</span></span>
     - <span data-ttu-id="e8ee2-117">Os projetos confirmados podem ser **Fechados como perdidos**.</span><span class="sxs-lookup"><span data-stu-id="e8ee2-117">Confirmed projects can be **Closed as lost**.</span></span>

- <span data-ttu-id="e8ee2-118">Gestão de Recursos</span><span class="sxs-lookup"><span data-stu-id="e8ee2-118">Resource Management</span></span>

     - <span data-ttu-id="e8ee2-119">Ao expandir as reservas, será apresentada aos utilizadores uma caixa de diálogo de confirmação para resumir os resultados da reserva e fornecer uma hiperligação para Manter Reservas.</span><span class="sxs-lookup"><span data-stu-id="e8ee2-119">When extending bookings, users will be prompted with a confirmation dialog box to summarize booking results and provide a link to Maintain Bookings.</span></span>


### <a name="bug-fixes"></a><span data-ttu-id="e8ee2-120">Correções de erros</span><span class="sxs-lookup"><span data-stu-id="e8ee2-120">Bug fixes</span></span>

- <span data-ttu-id="e8ee2-121">Tempo e Despesa</span><span class="sxs-lookup"><span data-stu-id="e8ee2-121">Time and Expense</span></span>

     - <span data-ttu-id="e8ee2-122">Corrigido: melhorou a experiência do utilizador quando o utilizador não tiver selecionado nenhuma entrada a ser corrigida.</span><span class="sxs-lookup"><span data-stu-id="e8ee2-122">Fixed: Improved the user experience when the user has not selected any entries to be corrected.</span></span>

- <span data-ttu-id="e8ee2-123">Gestão de Recursos</span><span class="sxs-lookup"><span data-stu-id="e8ee2-123">Resource Management</span></span>

     - <span data-ttu-id="e8ee2-124">Corrigido: a reserva de um recurso várias vezes sobrepõem-se ao nome do recurso agendável.</span><span class="sxs-lookup"><span data-stu-id="e8ee2-124">Fixed: Booking a resource multiple times overflows the name of the bookable resource.</span></span>

- <span data-ttu-id="e8ee2-125">Sales</span><span class="sxs-lookup"><span data-stu-id="e8ee2-125">Sales</span></span>

     - <span data-ttu-id="e8ee2-126">Corrigido: o preço de vendas total não é calculado até que o utilizador também introduza um preço de custo para estimativa de despesas num projeto.</span><span class="sxs-lookup"><span data-stu-id="e8ee2-126">Fixed: The total sales price is not calculated until the user also inputs a cost price for expense estimates on a project.</span></span>
     - <span data-ttu-id="e8ee2-127">Corrigido: fechar uma proposta como **Ganha** falha se o contrato de projeto associado não estiver num estado de **Rascunho**.</span><span class="sxs-lookup"><span data-stu-id="e8ee2-127">Fixed: Closing a quote as **Won** fails if the associated project contract is not in a **Draft** state.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]