---
title: Novidades ou alterações na Versão da Atualização 30 do Project Service Automation, V3
description: Este tópico lista as funcionalidades e correções disponíveis no Project Service Automation V3, Versão da Atualização 30, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
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
ms.openlocfilehash: 1169ee13c42e982cb30a40d92df660f8933786a9
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852883"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a><span data-ttu-id="eb37f-103">Novidades ou alterações na Versão da Atualização 30 do Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="eb37f-103">What's new or changed in Project Service Automation Update Release 30, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="eb37f-104">Temos o prazer de anunciar a mais recente atualização à aplicação Project Service Automation para Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="eb37f-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="eb37f-105">Esta versão inclui algumas melhorias importantes na qualidade, desempenho e utilização.</span><span class="sxs-lookup"><span data-stu-id="eb37f-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="eb37f-106">Esta versão é compatível com o Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="eb37f-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="eb37f-107">Para atualizar esta versão, visite o Centro de Administração para o Dynamics 365 online e aceda à página de soluções para instalar a atualização.</span><span class="sxs-lookup"><span data-stu-id="eb37f-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="eb37f-108">Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="eb37f-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="eb37f-109">Este tópico lista as funcionalidades e correções novas ou alteradas para o Project Service Automation V3, Versão da Atualização 30.</span><span class="sxs-lookup"><span data-stu-id="eb37f-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 30.</span></span> <span data-ttu-id="eb37f-110">Esta versão tem o número de compilação V3.10.51.61 e está geralmente disponível através de uma atualização automática em abril de 2021.</span><span class="sxs-lookup"><span data-stu-id="eb37f-110">This version has a build number of V3.10.51.61 and is generally available through a self-update in April 2021.</span></span>

## <a name="update-release-30"></a><span data-ttu-id="eb37f-111">Versão da Atualização 30</span><span class="sxs-lookup"><span data-stu-id="eb37f-111">Update Release 30</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="eb37f-112">Correções de erros</span><span class="sxs-lookup"><span data-stu-id="eb37f-112">Bug fixes</span></span>

<span data-ttu-id="eb37f-113">**Tempo e Despesa**</span><span class="sxs-lookup"><span data-stu-id="eb37f-113">**Time and Expense**</span></span>

<span data-ttu-id="eb37f-114">Foram corrigidos os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="eb37f-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="eb37f-115">Ocorre um erro quando cria e guarda uma entrada de tempo na página **Criação rápida** se o campo **Função** for removido.</span><span class="sxs-lookup"><span data-stu-id="eb37f-115">An error occurs when you create and save a time entry on the **Quick Create** page if the **Role** field is removed.</span></span>
- <span data-ttu-id="eb37f-116">O filtro Entrada de Tempo aplica o operador de filtro errado.</span><span class="sxs-lookup"><span data-stu-id="eb37f-116">The Time Entry filter applies the wrong filter operator.</span></span>
- <span data-ttu-id="eb37f-117">As folhas de tempo copiadas não são exibidas automaticamente quando seleciona **Copiar semana** no controlo de entrada de tempo.</span><span class="sxs-lookup"><span data-stu-id="eb37f-117">Copied timesheets aren't automatically displayed when you select **Copy Week** on the time entry control.</span></span>

<span data-ttu-id="eb37f-118">**Gestão de Recursos**</span><span class="sxs-lookup"><span data-stu-id="eb37f-118">**Resource Management**</span></span>

<span data-ttu-id="eb37f-119">Foram corrigidos os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="eb37f-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="eb37f-120">Quando prolonga uma reserva, o estado de reserva atribuído à reserva dura está incorreto.</span><span class="sxs-lookup"><span data-stu-id="eb37f-120">When you extend a booking, the booking status assigned to the hard booking is incorrect.</span></span> <span data-ttu-id="eb37f-121">O alargamento de uma reserva respeita o estado de reserva definido como **Comprometido** nos metadados de configuração de reserva.</span><span class="sxs-lookup"><span data-stu-id="eb37f-121">Extending a booking respects the booking status defined as **Committed** in the booking setup metadata.</span></span>
- <span data-ttu-id="eb37f-122">Quando um estado de reserva válido não é especificado, a mensagem de erro não é corretamente localizada.</span><span class="sxs-lookup"><span data-stu-id="eb37f-122">When a valid booking status isn't specified, the error message is not correctly localized.</span></span>

<span data-ttu-id="eb37f-123">**Gestão de Projetos**</span><span class="sxs-lookup"><span data-stu-id="eb37f-123">**Project Management**</span></span>

<span data-ttu-id="eb37f-124">Foram corrigidos os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="eb37f-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="eb37f-125">Os projetos não podem ser criados numa moeda e incluem tarefas relacionadas noutra moeda.</span><span class="sxs-lookup"><span data-stu-id="eb37f-125">Projects can't be created in one currency and include related tasks in another currency.</span></span>

<span data-ttu-id="eb37f-126">**Vendas**</span><span class="sxs-lookup"><span data-stu-id="eb37f-126">**Sales**</span></span>

<span data-ttu-id="eb37f-127">Foram corrigidos os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="eb37f-127">The following issues have been fixed:</span></span>

- <span data-ttu-id="eb37f-128">Quando uma lista de preços é copiada, os preços não são atualizados.</span><span class="sxs-lookup"><span data-stu-id="eb37f-128">When a price list is copied, prices aren't updated.</span></span>
- <span data-ttu-id="eb37f-129">Fechar uma proposta como ganha falha quando o detalhe de custos tem um valor de origem.</span><span class="sxs-lookup"><span data-stu-id="eb37f-129">Closing a quote as won fails when the cost detail has a value for origin.</span></span>
- <span data-ttu-id="eb37f-130">Na entidade de **Tarefa do projeto**, **Custo estimado** foi renomeado para **Custo Planeado (Base)**.</span><span class="sxs-lookup"><span data-stu-id="eb37f-130">On the **Project Task** entity, **Estimated Cost** has been renamed to **Planned Cost (Base)**.</span></span>
- <span data-ttu-id="eb37f-131">Uma exceção de referência nula é gerada quando as faturas são criadas ou eliminadas.</span><span class="sxs-lookup"><span data-stu-id="eb37f-131">A null reference exception is generated when invoices are created or deleted.</span></span>
