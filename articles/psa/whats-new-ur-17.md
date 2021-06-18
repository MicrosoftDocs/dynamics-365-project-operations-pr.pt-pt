---
title: Novidades ou alterações na Versão da Atualização 17 do Project Service Automation, V3
description: Este tópico lista as funcionalidades e correções disponíveis no Project Service Automation V3, Versão da Atualização 17, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
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
ms.openlocfilehash: 364a64e0ea501ac5b7faaf254c7af3648cfe1f9b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006705"
---
# <a name="project-service-automation-update-release-17-v3"></a><span data-ttu-id="28ffb-103">Versão da Atualização 17 do Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="28ffb-103">Project Service Automation Update Release 17, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="28ffb-104">Temos o prazer de anunciar a mais recente atualização à aplicação Project Service Automation para Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="28ffb-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="28ffb-105">Esta versão inclui algumas melhorias importantes na qualidade, desempenho e utilização.</span><span class="sxs-lookup"><span data-stu-id="28ffb-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="28ffb-106">Esta versão é compatível com o Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="28ffb-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="28ffb-107">Para atualizar esta versão, visite o Centro de Administração para o Dynamics 365 online e aceda à página de soluções para instalar a atualização.</span><span class="sxs-lookup"><span data-stu-id="28ffb-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="28ffb-108">Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="28ffb-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="28ffb-109">Este tópico lista as funcionalidades e correções novas ou alteradas para o PSA V3, Versão da Atualização 17.</span><span class="sxs-lookup"><span data-stu-id="28ffb-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 17.</span></span> <span data-ttu-id="28ffb-110">Esta versão tem um número de compilação de V3.10.6.34 e está geralmente disponível através de uma auto-atualização em março de 2020.</span><span class="sxs-lookup"><span data-stu-id="28ffb-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in March 2020.</span></span>


## <a name="update-release-17"></a><span data-ttu-id="28ffb-111">Versão da Atualização 17</span><span class="sxs-lookup"><span data-stu-id="28ffb-111">Update Release 17</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="28ffb-112">Correções de erros</span><span class="sxs-lookup"><span data-stu-id="28ffb-112">Bug fixes</span></span>

<span data-ttu-id="28ffb-113">**Gerais**</span><span class="sxs-lookup"><span data-stu-id="28ffb-113">**General**</span></span>

- <span data-ttu-id="28ffb-114">Corrigido: o Project Service Automation foi automatizado para impor licenças de Team Member (o Hub de Recursos do Projeto incluirá os metadados do plano Team Member Service 3.x)</span><span class="sxs-lookup"><span data-stu-id="28ffb-114">Fixed: Update Project Service Automation to enforce Team Member licenses (Project Resource Hub will include Team Member Service plan metadata 3.x)</span></span>
 
<span data-ttu-id="28ffb-115">**Tempo e Despesa**</span><span class="sxs-lookup"><span data-stu-id="28ffb-115">**Time and Expense**</span></span>

- <span data-ttu-id="28ffb-116">Corrigido: não é possível alterar uma estimativa de despesa de preço não zero para zero (0).</span><span class="sxs-lookup"><span data-stu-id="28ffb-116">Fixed: It is not possible to change an expense estimate from a non-zero price to zero (0).</span></span> <span data-ttu-id="28ffb-117">A alteração é ignorada.</span><span class="sxs-lookup"><span data-stu-id="28ffb-117">The change is ignored.</span></span>

<span data-ttu-id="28ffb-118">**Gestão de Projetos**</span><span class="sxs-lookup"><span data-stu-id="28ffb-118">**Project Management**</span></span>

- <span data-ttu-id="28ffb-119">Corrigido: foi adicionada uma verificação de valores nulos ao nome da posição de um membro de equipa.</span><span class="sxs-lookup"><span data-stu-id="28ffb-119">Fixed: A check for null values has been added on a team member's position name.</span></span>
- <span data-ttu-id="28ffb-120">Corrigido: o campo **msdyn_userresourceid** na entidade **msdyn_resourceassignment** foi preterido.</span><span class="sxs-lookup"><span data-stu-id="28ffb-120">Fixed: **msdyn_userresourceid** field on the **msdyn_resourceassignment** entity has been deprecated.</span></span>
- <span data-ttu-id="28ffb-121">Corrigido: a atualização de 2.x para 3.x agora trata dos contornos de esforço vazio nas atribuições de tarefa.</span><span class="sxs-lookup"><span data-stu-id="28ffb-121">Fixed: Upgrade from 2.x to 3.x now handles empty effort contours on task assignments.</span></span>

<span data-ttu-id="28ffb-122">**Sales**</span><span class="sxs-lookup"><span data-stu-id="28ffb-122">**Sales**</span></span>

- <span data-ttu-id="28ffb-123">Corrigido: **Invoice.PreValidateInvoiceUpdate** agora trata corretamente do cenário de reatribuição de proprietários dos registos.</span><span class="sxs-lookup"><span data-stu-id="28ffb-123">Fixed: **Invoice.PreValidateInvoiceUpdate** now handles the scenario of reassigning record owners properly.</span></span>
- <span data-ttu-id="28ffb-124">Corrigido: quando a classe de transação é **Hora**, **UnitGroup** é não editável para todas as entidades, incluindo, **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail** e **ContractLineDetails**.</span><span class="sxs-lookup"><span data-stu-id="28ffb-124">Fixed: When the transaction class is **Time**, **UnitGroup** is non-editable for all entities including, **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail**, and **ContractLineDetails**.</span></span> <span data-ttu-id="28ffb-125">No entanto, **Unidade** é não editável apenas para **JournalLine** e **InvoiceLineDetails**.</span><span class="sxs-lookup"><span data-stu-id="28ffb-125">However, **Unit** is non-editable only for **JournalLine** and **InvoiceLineDetails**.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]