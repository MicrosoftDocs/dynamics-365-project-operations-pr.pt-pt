---
title: Novidades ou alterações na Versão da Atualização 26 do Project Service Automation, V3
description: Este tópico lista as funcionalidades e correções disponíveis no Project Service Automation V3, Versão da Atualização 26, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.openlocfilehash: 6aafe66fe8c63dc886455a36e93f32d4a581d5cc
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005580"
---
# <a name="project-service-automation-update-release-26-v3"></a><span data-ttu-id="8b5d1-103">Versão da Atualização 26 do Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="8b5d1-103">Project Service Automation Update Release 26, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="8b5d1-104">Temos o prazer de anunciar a mais recente atualização à aplicação Project Service Automation para Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="8b5d1-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="8b5d1-105">Esta versão inclui algumas melhorias importantes na qualidade, desempenho e utilização.</span><span class="sxs-lookup"><span data-stu-id="8b5d1-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="8b5d1-106">Esta versão é compatível com o Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="8b5d1-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="8b5d1-107">Para atualizar esta versão, visite o Centro de Administração para o Dynamics 365 online e aceda à página de soluções para instalar a atualização.</span><span class="sxs-lookup"><span data-stu-id="8b5d1-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="8b5d1-108">Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="8b5d1-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="8b5d1-109">Este tópico lista as funcionalidades e correções novas ou alteradas para o Project Service Automation V3, Versão da Atualização 26, V3.</span><span class="sxs-lookup"><span data-stu-id="8b5d1-109">This topic lists the features and fixes that are new or changed for Project Service Automation Update Release 26, V3.</span></span> <span data-ttu-id="8b5d1-110">Esta versão tem um número de compilação V3.10.44.59 e está geralmente disponível através de uma atualização automática em dezembro de 2020.</span><span class="sxs-lookup"><span data-stu-id="8b5d1-110">This version has a build number of V3.10.44.59 and is generally available through a self-update in December 2020.</span></span>

## <a name="update-release-26"></a><span data-ttu-id="8b5d1-111">Versão da Atualização 26</span><span class="sxs-lookup"><span data-stu-id="8b5d1-111">Update Release 26</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="8b5d1-112">Correções de erros</span><span class="sxs-lookup"><span data-stu-id="8b5d1-112">Bug fixes</span></span>

<span data-ttu-id="8b5d1-113">**Tempo e Despesa**</span><span class="sxs-lookup"><span data-stu-id="8b5d1-113">**Time and Expense**</span></span>

<span data-ttu-id="8b5d1-114">Foram corrigidos os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="8b5d1-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="8b5d1-115">Os utilizadores podem alterar a tarefa numa entrada de hora que tenha sido aprovada/submetida.</span><span class="sxs-lookup"><span data-stu-id="8b5d1-115">Users are able to change the task on a time entry that has been approved/submitted.</span></span>
- <span data-ttu-id="8b5d1-116">Erro de "Referência de Objeto Não Definida" ao guardar a entrada de hora.</span><span class="sxs-lookup"><span data-stu-id="8b5d1-116">"Object Reference Not Set" error when saving time entry.</span></span>
- <span data-ttu-id="8b5d1-117">A importação de entrada de hora a partir de atribuições de recursos cria entradas de hora com os valores DateTime incorretos.</span><span class="sxs-lookup"><span data-stu-id="8b5d1-117">Time entry import from resource assignments creates time entries with the incorrect DateTime values.</span></span>
- <span data-ttu-id="8b5d1-118">Quando o Project Service Automation e a aplicação Field Service estão ambos instalados, o botão **Novo** é exibido duas vezes na barra de comando para entradas de hora na aplicação Field Service.</span><span class="sxs-lookup"><span data-stu-id="8b5d1-118">When Project Service Automation and the Field Service app are both installed, the **New** button is displaying twice on the command bar for time entries in the Field Service app.</span></span>
- <span data-ttu-id="8b5d1-119">Permitir atualizações de células de **Unidade** e de **Grupo de unidades** agora funciona na grelha **Estimativas de Despesas**.</span><span class="sxs-lookup"><span data-stu-id="8b5d1-119">**Allow Unit** and **Unit group** cells updates now work on the **Expense Estimates** grid.</span></span>
- <span data-ttu-id="8b5d1-120">O formulário **Atualizar Edição de entrada de hora** inclui **Linha cronológica**.</span><span class="sxs-lookup"><span data-stu-id="8b5d1-120">**Update Time Entry Edit** form includes **Timeline**.</span></span>
- <span data-ttu-id="8b5d1-121">A aprovação do tempo para entradas de hora de não projeto bloqueia o sistema ao procurar uma função de aprovação do projeto.</span><span class="sxs-lookup"><span data-stu-id="8b5d1-121">Time approval for non-project time entries blocks the system when searching for a project approver role.</span></span>

<span data-ttu-id="8b5d1-122">**Gestão de Recursos**</span><span class="sxs-lookup"><span data-stu-id="8b5d1-122">**Resource Management**</span></span>

<span data-ttu-id="8b5d1-123">Foram corrigidos os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="8b5d1-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="8b5d1-124">Validação adicionada no plug-in **PostProjectCreate** para verificar se há um requisito principal antes de criar um.</span><span class="sxs-lookup"><span data-stu-id="8b5d1-124">Added validation in the **PostProjectCreate** plug-in to check for a primary requirement before creating one.</span></span>
- <span data-ttu-id="8b5d1-125">O formulário de criação rápida **Membro da Equipa do Projeto** lança uma exceção de referência nula se os campos forem removidos do formulário.</span><span class="sxs-lookup"><span data-stu-id="8b5d1-125">**Project Team Member** quick create form throws a null reference exception if fields are removed from the form.</span></span>
- <span data-ttu-id="8b5d1-126">Gerar requisitos para 12 horas em 1 ano falhará.</span><span class="sxs-lookup"><span data-stu-id="8b5d1-126">Generate requirements for 12 hours over 1 year will fail.</span></span>
- <span data-ttu-id="8b5d1-127">Exceção de referência nula de mensagem de erro melhorada durante a criação de requisitos de recursos.</span><span class="sxs-lookup"><span data-stu-id="8b5d1-127">Improved error message null reference exception during resource requirement creation.</span></span>

<span data-ttu-id="8b5d1-128">**Gestão de Projetos**</span><span class="sxs-lookup"><span data-stu-id="8b5d1-128">**Project Management**</span></span>

<span data-ttu-id="8b5d1-129">Foram corrigidos os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="8b5d1-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="8b5d1-130">Validação melhorada para abordar a exceção de referência nula gerada no plug-in **PreProjectUpdate**.</span><span class="sxs-lookup"><span data-stu-id="8b5d1-130">Improved validation to address null reference exception generated in the **PreProjectUpdate** plug-in.</span></span>
- <span data-ttu-id="8b5d1-131">Os projetos publicados pelo suplemento de ambiente de trabalho do Microsoft Project eliminam atribuições não atribuídas.</span><span class="sxs-lookup"><span data-stu-id="8b5d1-131">Projects published by the Microsoft Project desktop add-in delete unassigned assignments.</span></span>
- <span data-ttu-id="8b5d1-132">Adicionou nova validação quando a referência do projeto de uma tarefa é inválida devido a uma exceção de referência nula no plug-in **PreValidateProjectTaskUpdate**.</span><span class="sxs-lookup"><span data-stu-id="8b5d1-132">Added new validation when a task’s project reference is invalid due to null reference exception in **PreValidateProjectTaskUpdate** plug-in.</span></span>
- <span data-ttu-id="8b5d1-133">A grelha de Membro da Equipa não mostra atribuições distintas no registo do membro da equipa.</span><span class="sxs-lookup"><span data-stu-id="8b5d1-133">Team Member grid does not show distinct assignments on the team member record.</span></span>
- <span data-ttu-id="8b5d1-134">Adicionadas novas mensagens de validação e de erro devido à exceção de referência nula no plug-in **PreProjectTaskDelete**.</span><span class="sxs-lookup"><span data-stu-id="8b5d1-134">Added new validation and error messages due to null reference exception in **PreProjectTaskDelete** plug-in.</span></span>

<span data-ttu-id="8b5d1-135">**Sales**</span><span class="sxs-lookup"><span data-stu-id="8b5d1-135">**Sales**</span></span>

<span data-ttu-id="8b5d1-136">Foram corrigidos os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="8b5d1-136">The following issues have been fixed:</span></span>

- <span data-ttu-id="8b5d1-137">Ao selecionar uma linha baseada em projeto em proposta ou contrato, o botão **Sugestão** só deve ser visível ao selecionar uma linha baseada no produto associada a um produto existente.</span><span class="sxs-lookup"><span data-stu-id="8b5d1-137">When selecting a project-based line in quote or contract, the **Suggestion** button should only be visible when selecting a product-based line associated with an existing product.</span></span>
- <span data-ttu-id="8b5d1-138">Divida o privilégio **Create_Product** do privilégio **Create_ProjectContract**.</span><span class="sxs-lookup"><span data-stu-id="8b5d1-138">Split **Create_Product** privilege from **Create_ProjectContract** privilege.</span></span>
- <span data-ttu-id="8b5d1-139">A eliminação de uma linha de fatura causa falha de referência nula em **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span><span class="sxs-lookup"><span data-stu-id="8b5d1-139">Deleting an invoice line causes null reference failure on **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]