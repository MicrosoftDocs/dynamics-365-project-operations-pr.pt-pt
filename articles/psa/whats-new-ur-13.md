---
title: Novidades ou alterações na Versão da Atualização 13 do Project Service Automation, V3
description: Esta tópico fornece informações sobre o que há de novo na Versão da Atualização 13 do Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: c328821064065e19938406856d327f690f577e7a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000315"
---
# <a name="project-service-automation-update-release-13-v3"></a><span data-ttu-id="9c5fd-103">Versão da Atualização 13 do Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="9c5fd-103">Project Service Automation Update Release 13, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="9c5fd-104">Temos o prazer de anunciar a atualização mais recente para a aplicação Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="9c5fd-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="9c5fd-105">Esta versão inclui algumas melhorias importantes na qualidade, desempenho e utilização.</span><span class="sxs-lookup"><span data-stu-id="9c5fd-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="9c5fd-106">Esta versão é compatível com o Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="9c5fd-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="9c5fd-107">Para atualizar esta versão, visite o Centro de Administração para o Dynamics 365 online e aceda à página de soluções para instalar a atualização.</span><span class="sxs-lookup"><span data-stu-id="9c5fd-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="9c5fd-108">Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="9c5fd-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="9c5fd-109">Este tópico lista as funcionalidades e correções novas ou alteradas para o Project Service Automation V3, Versão da Atualização 13.</span><span class="sxs-lookup"><span data-stu-id="9c5fd-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 13.</span></span> <span data-ttu-id="9c5fd-110">Esta versão tem um número de compilação de V3.10.3.18 e está disponível na seguinte agenda:</span><span class="sxs-lookup"><span data-stu-id="9c5fd-110">This version has a build number of V3.10.3.18 and is available on the following schedule:</span></span>

- <span data-ttu-id="9c5fd-111">**Disponibilidade geral (Atualização automática):** novembro de 2019</span><span class="sxs-lookup"><span data-stu-id="9c5fd-111">**General availability (self-update):** November 2019</span></span>
- <span data-ttu-id="9c5fd-112">**Atualização automática:** dezembro de 2019</span><span class="sxs-lookup"><span data-stu-id="9c5fd-112">**Auto-update:** December 2019</span></span>


## <a name="update-release-13"></a><span data-ttu-id="9c5fd-113">Versão da Atualização 13</span><span class="sxs-lookup"><span data-stu-id="9c5fd-113">Update Release 13</span></span> 

### <a name="bug-fixes"></a><span data-ttu-id="9c5fd-114">Correções de erros</span><span class="sxs-lookup"><span data-stu-id="9c5fd-114">Bug fixes</span></span>

- <span data-ttu-id="9c5fd-115">Tempo e Despesa</span><span class="sxs-lookup"><span data-stu-id="9c5fd-115">Time and Expense</span></span>

     - <span data-ttu-id="9c5fd-116">Corrigido: a funcionalidade de pesquisa na página **Aprovação de despesas** não funciona quando a pesquisa por finalidade de despesa é efetuada.</span><span class="sxs-lookup"><span data-stu-id="9c5fd-116">Fixed: Search functionality on the **Expense approval** page does not work when searching by expense purpose.</span></span>

- <span data-ttu-id="9c5fd-117">Gestão de Recursos</span><span class="sxs-lookup"><span data-stu-id="9c5fd-117">Resource Management</span></span>

     - <span data-ttu-id="9c5fd-118">Corrigido: os números na reconciliação foram atualizados para serem justificados à direita.</span><span class="sxs-lookup"><span data-stu-id="9c5fd-118">Fixed: Numbers in the reconciliation have been updated to be right justified.</span></span>
     - <span data-ttu-id="9c5fd-119">Corrigido: os Recursos Nomeados não podem ser atribuídos a tarefas através do separador **Agenda**.</span><span class="sxs-lookup"><span data-stu-id="9c5fd-119">Fixed: Named Resources can't be assigned to tasks through the **Schedule** tab.</span></span>

- <span data-ttu-id="9c5fd-120">Gestão de Projetos</span><span class="sxs-lookup"><span data-stu-id="9c5fd-120">Project Management</span></span>

     - <span data-ttu-id="9c5fd-121">Corrigido: exceção de referência nula ao atribuir um membro da equipa quando o **TransactionType** não contém informações de configuração para **Unidade** e **DefaultGroup**.</span><span class="sxs-lookup"><span data-stu-id="9c5fd-121">Fixed: Null reference exception when assigning team member when the **TransactionType** is missing setup information for **Unit** and **DefaultGroup**.</span></span>

- <span data-ttu-id="9c5fd-122">Sales</span><span class="sxs-lookup"><span data-stu-id="9c5fd-122">Sales</span></span>

     - <span data-ttu-id="9c5fd-123">Corrigido: os registos do tipo de transação duplicados devolvem um erro quando são criados registos de preço de função.</span><span class="sxs-lookup"><span data-stu-id="9c5fd-123">Fixed: Duplicate transaction type records return an error when role price records are created.</span></span>
     - <span data-ttu-id="9c5fd-124">Corrigido: Botões adicionais para **Nova Oportunidade**, **Proposta**, **Linha de Encomendas** e **Adicionar Produto** estão visíveis nos comandos de Oportunidades, Propostas, Produtos de Encomenda e a subgrelha das Linhas baseadas em projetos.</span><span class="sxs-lookup"><span data-stu-id="9c5fd-124">Fixed: Extra buttons for **New Opportunity**, **Quote**, **Order Line**, and **Add Product** are visible in commands for Opportunities, Quotes, Order Products, and the project-based Lines subgrid.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]