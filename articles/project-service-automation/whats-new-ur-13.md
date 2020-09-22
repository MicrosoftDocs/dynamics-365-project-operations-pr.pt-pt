---
title: Novidades na Versão da Atualização 13 do Project Service Automation, V3
description: Esta tópico fornece informações sobre o que há de novo na Versão da Atualização 13 do Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: c6f6a5b6-b5bb-467c-b7c7-7fb962504c6d
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 5f1b6b3879c94a77ab62082aad1e470a3ba66552
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754535"
---
# <a name="project-service-automation-v3-update-release-13"></a><span data-ttu-id="54bb9-103">Versão da Atualização do Project Service Automation V3, Versão da Atualização 13</span><span class="sxs-lookup"><span data-stu-id="54bb9-103">Project Service Automation V3, Update Release 13</span></span>
<span data-ttu-id="54bb9-104">Temos o prazer de anunciar a atualização mais recente para a aplicação Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="54bb9-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="54bb9-105">Esta versão inclui algumas melhorias importantes na qualidade, desempenho e utilização.</span><span class="sxs-lookup"><span data-stu-id="54bb9-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="54bb9-106">Esta versão é compatível com o Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="54bb9-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="54bb9-107">Para atualizar esta versão, visite o Centro de Administração para o Dynamics 365 online e aceda à página de soluções para instalar a atualização.</span><span class="sxs-lookup"><span data-stu-id="54bb9-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="54bb9-108">Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="54bb9-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="54bb9-109">Este tópico lista as funcionalidades e correções novas ou alteradas para o Project Service Automation V3, Versão da Atualização 13.</span><span class="sxs-lookup"><span data-stu-id="54bb9-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 13.</span></span> <span data-ttu-id="54bb9-110">Esta versão tem um número de compilação de V3.10.3.18 e está disponível na seguinte agenda:</span><span class="sxs-lookup"><span data-stu-id="54bb9-110">This version has a build number of V3.10.3.18 and is available on the following schedule:</span></span>

- <span data-ttu-id="54bb9-111">**Disponibilidade geral (Atualização automática):** novembro de 2019</span><span class="sxs-lookup"><span data-stu-id="54bb9-111">**General availability (self-update):** November 2019</span></span>
- <span data-ttu-id="54bb9-112">**Atualização automática:** dezembro de 2019</span><span class="sxs-lookup"><span data-stu-id="54bb9-112">**Auto-update:** December 2019</span></span>


## <a name="update-release-13"></a><span data-ttu-id="54bb9-113">Versão da Atualização 13</span><span class="sxs-lookup"><span data-stu-id="54bb9-113">Update Release 13</span></span> 

### <a name="bug-fixes"></a><span data-ttu-id="54bb9-114">Correções de erros</span><span class="sxs-lookup"><span data-stu-id="54bb9-114">Bug fixes</span></span>

- <span data-ttu-id="54bb9-115">Tempo e Despesa</span><span class="sxs-lookup"><span data-stu-id="54bb9-115">Time and Expense</span></span>

     - <span data-ttu-id="54bb9-116">Corrigido: a funcionalidade de pesquisa na página **Aprovação de despesas** não funciona quando a pesquisa por finalidade de despesa é efetuada.</span><span class="sxs-lookup"><span data-stu-id="54bb9-116">Fixed: Search functionality on the **Expense approval** page does not work when searching by expense purpose.</span></span>

- <span data-ttu-id="54bb9-117">Gestão de Recursos</span><span class="sxs-lookup"><span data-stu-id="54bb9-117">Resource Management</span></span>

     - <span data-ttu-id="54bb9-118">Corrigido: os números na reconciliação foram atualizados para serem justificados à direita.</span><span class="sxs-lookup"><span data-stu-id="54bb9-118">Fixed: Numbers in the reconciliation have been updated to be right justified.</span></span>
     - <span data-ttu-id="54bb9-119">Corrigido: os Recursos Nomeados não podem ser atribuídos a tarefas através do separador **Agenda**.</span><span class="sxs-lookup"><span data-stu-id="54bb9-119">Fixed: Named Resources can't be assigned to tasks through the **Schedule** tab.</span></span>

- <span data-ttu-id="54bb9-120">Gestão de Projetos</span><span class="sxs-lookup"><span data-stu-id="54bb9-120">Project Management</span></span>

     - <span data-ttu-id="54bb9-121">Corrigido: exceção de referência nula ao atribuir um membro da equipa quando o **TransactionType** não contém informações de configuração para **Unidade** e **DefaultGroup**.</span><span class="sxs-lookup"><span data-stu-id="54bb9-121">Fixed: Null reference exception when assigning team member when the **TransactionType** is missing setup information for **Unit** and **DefaultGroup**.</span></span>

- <span data-ttu-id="54bb9-122">Sales</span><span class="sxs-lookup"><span data-stu-id="54bb9-122">Sales</span></span>

     - <span data-ttu-id="54bb9-123">Corrigido: os registos do tipo de transação duplicados devolvem um erro quando são criados registos de preço de função.</span><span class="sxs-lookup"><span data-stu-id="54bb9-123">Fixed: Duplicate transaction type records return an error when role price records are created.</span></span>
     - <span data-ttu-id="54bb9-124">Corrigido: os botões adicionais para **Nova Oportunidade**, **Proposta**, **Linha de Proposta** e **Adicionar Produto** são visíveis em comandos para Oportunidades, Propostas, Produtos de Propostas e na subgrelha de linhas baseadas no projeto.</span><span class="sxs-lookup"><span data-stu-id="54bb9-124">Fixed: Extra buttons for **New Opportunity**, **Quote**, **Order Line**, and **Add Product** are visible in commands for Opportunities, Quotes, Order Products, and the project-based Lines sub-grid.</span></span>


