---
title: Novidades ou alterações na Versão da Atualização 17 do Project Service Automation, V3
description: Este tópico lista as funcionalidades e correções disponíveis no Project Service Automation V3, Versão da Atualização 17, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 7ba685568692dafe117de42a71bb14d391cd7cc4
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082360"
---
# <a name="project-service-automation-update-release-17-v3"></a><span data-ttu-id="cacd4-103">Versão da Atualização 17 do Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="cacd4-103">Project Service Automation Update Release 17, V3</span></span>

<span data-ttu-id="cacd4-104">Temos o prazer de anunciar a mais recente atualização à aplicação Project Service Automation para Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="cacd4-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="cacd4-105">Esta versão inclui algumas melhorias importantes na qualidade, desempenho e utilização.</span><span class="sxs-lookup"><span data-stu-id="cacd4-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="cacd4-106">Esta versão é compatível com o Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="cacd4-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="cacd4-107">Para atualizar esta versão, visite o Centro de Administração para o Dynamics 365 online e aceda à página de soluções para instalar a atualização.</span><span class="sxs-lookup"><span data-stu-id="cacd4-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="cacd4-108">Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="cacd4-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="cacd4-109">Este tópico lista as funcionalidades e correções novas ou alteradas para o PSA V3, Versão da Atualização 17.</span><span class="sxs-lookup"><span data-stu-id="cacd4-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 17.</span></span> <span data-ttu-id="cacd4-110">Esta versão tem um número de compilação de V3.10.6.34 e está geralmente disponível através de uma auto-atualização em março de 2020.</span><span class="sxs-lookup"><span data-stu-id="cacd4-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in March 2020.</span></span>


## <a name="update-release-17"></a><span data-ttu-id="cacd4-111">Versão da Atualização 17</span><span class="sxs-lookup"><span data-stu-id="cacd4-111">Update Release 17</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="cacd4-112">Correções de erros</span><span class="sxs-lookup"><span data-stu-id="cacd4-112">Bug fixes</span></span>

<span data-ttu-id="cacd4-113">**Gerais**</span><span class="sxs-lookup"><span data-stu-id="cacd4-113">**General**</span></span>

- <span data-ttu-id="cacd4-114">Corrigido: o Project Service Automation foi automatizado para impor licenças de Team Member (o Hub de Recursos do Projeto incluirá os metadados do plano Team Member Service 3.x)</span><span class="sxs-lookup"><span data-stu-id="cacd4-114">Fixed: Update Project Service Automation to enforce Team Member licenses (Project Resource Hub will include Team Member Service plan metadata 3.x)</span></span>
 
<span data-ttu-id="cacd4-115">**Tempo e Despesa**</span><span class="sxs-lookup"><span data-stu-id="cacd4-115">**Time and Expense**</span></span>

- <span data-ttu-id="cacd4-116">Corrigido: não é possível alterar uma estimativa de despesa de preço não zero para zero (0).</span><span class="sxs-lookup"><span data-stu-id="cacd4-116">Fixed: It is not possible to change an expense estimate from a non-zero price to zero (0).</span></span> <span data-ttu-id="cacd4-117">A alteração é ignorada.</span><span class="sxs-lookup"><span data-stu-id="cacd4-117">The change is ignored.</span></span>

<span data-ttu-id="cacd4-118">**Gestão de Projetos**</span><span class="sxs-lookup"><span data-stu-id="cacd4-118">**Project Management**</span></span>

- <span data-ttu-id="cacd4-119">Corrigido: foi adicionada uma verificação de valores nulos ao nome da posição de um membro de equipa.</span><span class="sxs-lookup"><span data-stu-id="cacd4-119">Fixed: A check for null values has been added on a team member's position name.</span></span>
- <span data-ttu-id="cacd4-120">Corrigido: o campo **msdyn_userresourceid** na entidade **msdyn_resourceassignment** foi preterido.</span><span class="sxs-lookup"><span data-stu-id="cacd4-120">Fixed: **msdyn_userresourceid** field on the **msdyn_resourceassignment** entity has been deprecated.</span></span>
- <span data-ttu-id="cacd4-121">Corrigido: a atualização de 2.x para 3.x agora trata dos contornos de esforço vazio nas atribuições de tarefa.</span><span class="sxs-lookup"><span data-stu-id="cacd4-121">Fixed: Upgrade from 2.x to 3.x now handles empty effort contours on task assignments.</span></span>

<span data-ttu-id="cacd4-122">**Sales**</span><span class="sxs-lookup"><span data-stu-id="cacd4-122">**Sales**</span></span>

- <span data-ttu-id="cacd4-123">Corrigido: **Invoice.PreValidateInvoiceUpdate** agora trata corretamente do cenário de reatribuição de proprietários dos registos.</span><span class="sxs-lookup"><span data-stu-id="cacd4-123">Fixed: **Invoice.PreValidateInvoiceUpdate** now handles the scenario of reassigning record owners properly.</span></span>
- <span data-ttu-id="cacd4-124">Corrigido: quando a classe de transação é **Hora** , **UnitGroup** é não editável para todas as entidades, incluindo, **QuoteLineDetails** , **JournalLine** , **InvoiceLineDetail** e **ContractLineDetails**.</span><span class="sxs-lookup"><span data-stu-id="cacd4-124">Fixed: When the transaction class is **Time** , **UnitGroup** is non-editable for all entities including, **QuoteLineDetails** , **JournalLine** , **InvoiceLineDetail** , and **ContractLineDetails**.</span></span> <span data-ttu-id="cacd4-125">No entanto, **Unidade** é não editável apenas para **JournalLine** e **InvoiceLineDetails**.</span><span class="sxs-lookup"><span data-stu-id="cacd4-125">However, **Unit** is non-editable only for **JournalLine** and **InvoiceLineDetails**.</span></span>


