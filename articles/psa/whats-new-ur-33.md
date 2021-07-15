---
title: Novidades ou alterações na Versão da Atualização 33 do Project Service Automation, V3
description: Este tópico lista as funcionalidades e correções disponíveis no Project Service Automation V3, Versão da Atualização 33, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
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
ms.openlocfilehash: 2c96e4abd484bb66285421baaad82ead9589bbe9
ms.sourcegitcommit: be5beba71ee9770c0083b4fe5cc89e7ec6b741b8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334584"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a><span data-ttu-id="9a7f3-103">Novidades ou alterações na Versão da Atualização 33 do Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="9a7f3-103">What's new or changed in Project Service Automation Update Release 33, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="9a7f3-104">Temos o prazer de anunciar a atualização mais recente para a aplicação Microsoft Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="9a7f3-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="9a7f3-105">Esta versão inclui algumas melhorias importantes na qualidade, desempenho e utilização.</span><span class="sxs-lookup"><span data-stu-id="9a7f3-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="9a7f3-106">É compatível com o Dynamics 365, versão 9.x.</span><span class="sxs-lookup"><span data-stu-id="9a7f3-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="9a7f3-107">Para atualizar para esta versão, visite a página de soluções online do Centro de Administração do Dynamics 365 e instale a atualização.</span><span class="sxs-lookup"><span data-stu-id="9a7f3-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="9a7f3-108">Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="9a7f3-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="9a7f3-109">Este tópico lista as funcionalidades e correções novas ou alteradas para o Project Service Automation V3, Versão da Atualização 33.</span><span class="sxs-lookup"><span data-stu-id="9a7f3-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 33.</span></span> <span data-ttu-id="9a7f3-110">Esta versão tem o número de compilação V3.10.54.98 e está em disponibilidade geral através de uma auto-atualização em julho de 2021.</span><span class="sxs-lookup"><span data-stu-id="9a7f3-110">This version has a build number of V3.10.54.98 and is generally available through a self-update in July 2021.</span></span>

## <a name="update-release-33"></a><span data-ttu-id="9a7f3-111">Versão da Atualização 33</span><span class="sxs-lookup"><span data-stu-id="9a7f3-111">Update Release 33</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="9a7f3-112">Correções de erros</span><span class="sxs-lookup"><span data-stu-id="9a7f3-112">Bug fixes</span></span>

<span data-ttu-id="9a7f3-113">**Tempo e Despesa**</span><span class="sxs-lookup"><span data-stu-id="9a7f3-113">**Time and Expense**</span></span>

<span data-ttu-id="9a7f3-114">Foram corrigidos os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="9a7f3-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="9a7f3-115">Dois campos bloqueados, **msdyn_description** e **msdyn_externaldescription**, são editáveis após a submissão.</span><span class="sxs-lookup"><span data-stu-id="9a7f3-115">Two locked fields, **msdyn_description** and **msdyn_externaldescription** are editable after submission.</span></span>
- <span data-ttu-id="9a7f3-116">Uma mensagem de erro ocorre se for criada uma despesa que não esteja relacionada com um projeto.</span><span class="sxs-lookup"><span data-stu-id="9a7f3-116">An error message occurs if an expense is created that isn't related to a project.</span></span>
- <span data-ttu-id="9a7f3-117">Quando uma entrada de hora é criada, a função de recurso assume por omissão uma função inativa.</span><span class="sxs-lookup"><span data-stu-id="9a7f3-117">When a time entry is created, the resource role defaults to an inactive role.</span></span>
- <span data-ttu-id="9a7f3-118">As linhas do diário associadas a uma despesa recuperada e eliminada não são eliminadas.</span><span class="sxs-lookup"><span data-stu-id="9a7f3-118">Journal lines associated with a recalled and deleted expense aren't deleted.</span></span>
- <span data-ttu-id="9a7f3-119">No **Formulário de Criação Rápida de Entrada de Hora**, atualize a vista **Lista de Tarefas do Projeto** para alterar a data apresentada por predefinição para a data de início da tarefa.</span><span class="sxs-lookup"><span data-stu-id="9a7f3-119">On the **Time entry Quick Create Form**, update the **Project Task List** view to change the date displayed by default to the start date of the task.</span></span>
- <span data-ttu-id="9a7f3-120">Quando cria uma entrada de hora a partir do separador **Relacionada** do recurso reservável, a entrada de hora é criada incorretamente para o utilizador com sessão iniciada em vez do recurso reservável principal.</span><span class="sxs-lookup"><span data-stu-id="9a7f3-120">When you create a time entry from the **Related** tab of the bookable resource, the time entry is incorrectly created for the signed-in user instead of the parent bookable resource.</span></span>
- <span data-ttu-id="9a7f3-121">São adicionados novos campos à caixa de diálogo **MDD de aprovação em massa**.</span><span class="sxs-lookup"><span data-stu-id="9a7f3-121">New fields are added to the **Bulk approval MDD** dialog box.</span></span>

<span data-ttu-id="9a7f3-122">**Planeamento de projeto**</span><span class="sxs-lookup"><span data-stu-id="9a7f3-122">**Project planning**</span></span>

<span data-ttu-id="9a7f3-123">Foram corrigidos os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="9a7f3-123">The following issues have been fixed:</span></span>
- <span data-ttu-id="9a7f3-124">Desempenho lento de criação de projetos quando são aplicados modelos de horas de trabalho do projeto com calendários complexos.</span><span class="sxs-lookup"><span data-stu-id="9a7f3-124">Slow project creation performance when project work hour templates are applied with complex calendars.</span></span>
- <span data-ttu-id="9a7f3-125">Quando a data de início é posterior à data de fim, é apresentado um erro no modelo do projeto de texto devido a diferenças no componente de tempo de cada campo.</span><span class="sxs-lookup"><span data-stu-id="9a7f3-125">When the start date is greater than the end date, an error displays on the copy project template because of differences in the time component of each field.</span></span>

<span data-ttu-id="9a7f3-126">**Gestão de recursos**</span><span class="sxs-lookup"><span data-stu-id="9a7f3-126">**Resource management**</span></span>

<span data-ttu-id="9a7f3-127">Foram corrigidos os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="9a7f3-127">The following issues have been fixed:</span></span>
- <span data-ttu-id="9a7f3-128">Um parâmetro incorreto é utilizado na consulta de utilização do recursos e o XML leva a resultados incorretos do filtro na grelha **Utilização do Recurso**.</span><span class="sxs-lookup"><span data-stu-id="9a7f3-128">An incorrect parameter is used in the resource utilization query and the XML leads to incorrect filter results on the **Resource Utilization** grid.</span></span>
- <span data-ttu-id="9a7f3-129">A confirmação **Expandir reservas** apresenta uma data de fim incorreta para as reservas.</span><span class="sxs-lookup"><span data-stu-id="9a7f3-129">The **Extend Bookings** confirmation displays incorrect end date for bookings.</span></span>

<span data-ttu-id="9a7f3-130">**Vendas**</span><span class="sxs-lookup"><span data-stu-id="9a7f3-130">**Sales**</span></span>

<span data-ttu-id="9a7f3-131">Foram corrigidos os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="9a7f3-131">The following issues have been fixed:</span></span>
- <span data-ttu-id="9a7f3-132">É apresentada uma mensagem de erro se um preço de categoria for criado com valores em falta.</span><span class="sxs-lookup"><span data-stu-id="9a7f3-132">An error message occurs if a category price is created with missing values.</span></span>
- <span data-ttu-id="9a7f3-133">É apresentada uma mensagem de erro se um marco do item de contrato for criado sem uma linha de encomenda.</span><span class="sxs-lookup"><span data-stu-id="9a7f3-133">An error message occurs if a contract line milestone is created without an order line.</span></span>
