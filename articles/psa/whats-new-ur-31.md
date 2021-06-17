---
title: Novidades ou alterações na Versão da Atualização 31 do Project Service Automation, V3
description: Este tópico lista as funcionalidades e correções disponíveis no Project Service Automation V3, Versão da Atualização 31, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
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
ms.openlocfilehash: 160187ba7b96547e85a7a4ec4bf84c86d8fd8257
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999145"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a><span data-ttu-id="c21b4-103">Novidades ou alterações na Versão da Atualização 31 do Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="c21b4-103">What's new or changed in Project Service Automation Update Release 31, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="c21b4-104">Temos o prazer de anunciar a mais recente atualização à aplicação Project Service Automation para Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="c21b4-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="c21b4-105">Esta versão inclui algumas melhorias importantes na qualidade, desempenho e utilização.</span><span class="sxs-lookup"><span data-stu-id="c21b4-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="c21b4-106">Esta versão é compatível com o Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="c21b4-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="c21b4-107">Para atualizar esta versão, visite o Centro de Administração para o Dynamics 365 online e aceda à página de soluções para instalar a atualização.</span><span class="sxs-lookup"><span data-stu-id="c21b4-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="c21b4-108">Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="c21b4-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="c21b4-109">Este tópico lista as funcionalidades e correções novas ou alteradas para o Project Service Automation V3, Versão da Atualização 31.</span><span class="sxs-lookup"><span data-stu-id="c21b4-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 31.</span></span> <span data-ttu-id="c21b4-110">Esta versão tem o número de compilação V3.10.52.77 e está geralmente disponível através de uma atualização automática em maio de 2021.</span><span class="sxs-lookup"><span data-stu-id="c21b4-110">This version has a build number of V3.10.52.77 and is generally available through a self-update in May 2021.</span></span>

## <a name="update-release-31"></a><span data-ttu-id="c21b4-111">Versão da Atualização 31</span><span class="sxs-lookup"><span data-stu-id="c21b4-111">Update Release 31</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="c21b4-112">Correções de erros</span><span class="sxs-lookup"><span data-stu-id="c21b4-112">Bug fixes</span></span>

<span data-ttu-id="c21b4-113">**Tempo e Despesa**</span><span class="sxs-lookup"><span data-stu-id="c21b4-113">**Time and Expense**</span></span>

<span data-ttu-id="c21b4-114">Foram corrigidos os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="c21b4-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="c21b4-115">Os botões de comando de controlo de entrada de tempo na página de **Recursos reservados** eram confusos.</span><span class="sxs-lookup"><span data-stu-id="c21b4-115">Time entry control command buttons on the **Bookable Resource** page were confusing.</span></span>
- <span data-ttu-id="c21b4-116">Uma exceção de referência nula foi gerada em **Project.SetTrackingFields** ao aprovar uma entrada de tempo.</span><span class="sxs-lookup"><span data-stu-id="c21b4-116">A null reference exception was generated in **Project.SetTrackingFields** when approving a time entry.</span></span>

<span data-ttu-id="c21b4-117">**Gestão de Recursos**</span><span class="sxs-lookup"><span data-stu-id="c21b4-117">**Resource Management**</span></span>

<span data-ttu-id="c21b4-118">Foram corrigidos os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="c21b4-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="c21b4-119">**Criar membro de equipa** não exibe corretamente a definição de metadados de configuração de reserva para **Estado comprometido de reserva predefinida**.</span><span class="sxs-lookup"><span data-stu-id="c21b4-119">**Create Team Member** doesn't correctly display the booking setup metadata setting for **Default Booking Committed Status**.</span></span>
- <span data-ttu-id="c21b4-120">Ao atualizar de PSA 1.X para 3.X, o processo de atualização falha em **UpgradeResourceRequirements**.</span><span class="sxs-lookup"><span data-stu-id="c21b4-120">When upgrading from PSA 1.X to 3.X, the upgrade process fails at **UpgradeResourceRequirements**.</span></span>


<span data-ttu-id="c21b4-121">**Vendas**</span><span class="sxs-lookup"><span data-stu-id="c21b4-121">**Sales**</span></span>

<span data-ttu-id="c21b4-122">Foram corrigidos os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="c21b4-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="c21b4-123">As receitas de valores reais convertem os montantes para a moeda do projeto na grelha de deteção de movimento.</span><span class="sxs-lookup"><span data-stu-id="c21b4-123">Actual revenue converts the amounts to the project currency in the tracking grid.</span></span>
- <span data-ttu-id="c21b4-124">A predefinição de moeda não é clara ao criar linhas de diário, linhas de cotação e linhas de contrato em cenários em que a moeda base de uma organização difere da moeda do projeto.</span><span class="sxs-lookup"><span data-stu-id="c21b4-124">The currency default is unclear when creating journal lines, quote lines, and contract lines in scenarios where an organization's base currency differs from the project currency.</span></span>
- <span data-ttu-id="c21b4-125">A consulta de **Validação do diário de correção pendente** não filtra por projeto.</span><span class="sxs-lookup"><span data-stu-id="c21b4-125">**Pending correction journal validation** query doesn't filter by project.</span></span>
- <span data-ttu-id="c21b4-126">As vendas remanescentes são calculadas incorretamente num projeto.</span><span class="sxs-lookup"><span data-stu-id="c21b4-126">Remaining sales are calculated incorrectly on a project.</span></span>
- <span data-ttu-id="c21b4-127">As cotações baseadas num falha de contacto quando são criadas sem uma tabela de preços.</span><span class="sxs-lookup"><span data-stu-id="c21b4-127">Quotes based on a contact fail when they are created without a price list.</span></span>
- <span data-ttu-id="c21b4-128">Não é mostrado nenhum girador de processamento quando seleciona **Confirmar fatura**.</span><span class="sxs-lookup"><span data-stu-id="c21b4-128">No processing spinner is shown when you select **Confirm Invoice**.</span></span>
- <span data-ttu-id="c21b4-129">Não é mostrado nenhum girador de processamento quando seleciona **Criar fatura**.</span><span class="sxs-lookup"><span data-stu-id="c21b4-129">No processing spinner is shown when you select **Create Invoice**.</span></span>
- <span data-ttu-id="c21b4-130">Fechar uma proposta como perdida não cancela as reservas.</span><span class="sxs-lookup"><span data-stu-id="c21b4-130">Closing a quote as lost doesn't cancel the bookings.</span></span>







