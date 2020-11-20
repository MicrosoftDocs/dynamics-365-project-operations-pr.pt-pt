---
title: Novidades ou alterações na Versão da Atualização 22 do Project Service Automation, V3
description: Este tópico lista as funcionalidades e correções disponíveis no Project Service Automation V3, Versão da Atualização 22, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 07/28/2020
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
ms.openlocfilehash: 456ed68bc1d74c2c8e5d2420a3f5d1fb8e0465d6
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126632"
---
# <a name="project-service-automation-update-release-22-v3"></a><span data-ttu-id="cd934-103">Versão da Atualização 22 do Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="cd934-103">Project Service Automation Update Release 22, V3</span></span>

<span data-ttu-id="cd934-104">Temos o prazer de anunciar a mais recente atualização à aplicação Project Service Automation para Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="cd934-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="cd934-105">Esta versão inclui algumas melhorias importantes na qualidade, desempenho e utilização.</span><span class="sxs-lookup"><span data-stu-id="cd934-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="cd934-106">Esta versão é compatível com o Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="cd934-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="cd934-107">Para atualizar esta versão, visite o Centro de Administração para o Dynamics 365 online e aceda à página de soluções para instalar a atualização.</span><span class="sxs-lookup"><span data-stu-id="cd934-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="cd934-108">Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="cd934-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="cd934-109">Este tópico lista as funcionalidades e correções novas ou alteradas para o Project Service Automation V3, Versão da Atualização 22.</span><span class="sxs-lookup"><span data-stu-id="cd934-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 22.</span></span> <span data-ttu-id="cd934-110">Esta versão tem o número de compilação V 3.10.33.48 e está geralmente disponível através de uma atualização automática em junho de 2020.</span><span class="sxs-lookup"><span data-stu-id="cd934-110">This version has a build number of V 3.10.33.48 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-22"></a><span data-ttu-id="cd934-111">Versão da Atualização 22</span><span class="sxs-lookup"><span data-stu-id="cd934-111">Update Release 22</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="cd934-112">Correções de erros</span><span class="sxs-lookup"><span data-stu-id="cd934-112">Bug fixes</span></span>



<span data-ttu-id="cd934-113">**Tempo e Despesa**</span><span class="sxs-lookup"><span data-stu-id="cd934-113">**Time and Expense**</span></span>

<span data-ttu-id="cd934-114">Foram corrigidos os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="cd934-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="cd934-115">As **Entradas de tempo** não são automaticamente adicionadas à afe de de entradas de Tempo após a importação.</span><span class="sxs-lookup"><span data-stu-id="cd934-115">**Time entries** are not automatically added in the Time entries schedule after import.</span></span>
- <span data-ttu-id="cd934-116">O seletor de datas de grelha **Entrada de tempo** não reconhece as definições regionais de um utilizador.</span><span class="sxs-lookup"><span data-stu-id="cd934-116">The **Time Entry** grid date picker does not recognize a user's regional settings.</span></span>

<span data-ttu-id="cd934-117">**Gestão de Recursos**</span><span class="sxs-lookup"><span data-stu-id="cd934-117">**Resource Management**</span></span>

<span data-ttu-id="cd934-118">Foram corrigidos os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="cd934-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="cd934-119">No modo manual, as alterações aos contornos de **Atribuição de Recursos** não são reconhecidas ao gerar **Requisitos de Recursos**.</span><span class="sxs-lookup"><span data-stu-id="cd934-119">In manual mode, changes to **Resource Assignment** contours are not recognized when generating **Resource Requirements**.</span></span>
- <span data-ttu-id="cd934-120">Os **Pedidos de Recursos** não suportam os estados de pedidos personalizados.</span><span class="sxs-lookup"><span data-stu-id="cd934-120">**Resource Requests** do not support custom request statuses.</span></span>

<span data-ttu-id="cd934-121">**Gestão de Projetos**</span><span class="sxs-lookup"><span data-stu-id="cd934-121">**Project Management**</span></span>

<span data-ttu-id="cd934-122">Foram corrigidos os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="cd934-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="cd934-123">A utilização de um duplo clique em EstimateGridControl não analisará corretamente os números de formato neerlandês.</span><span class="sxs-lookup"><span data-stu-id="cd934-123">Using double-click on EstimateGridControl will not correctly parse Dutch format numbers.</span></span>
- <span data-ttu-id="cd934-124">As horas atribuídas não atualizam corretamente quando as atribuições são alteradas utilizando o suplemento do cliente de ambiente de trabalho do Microsoft Project.</span><span class="sxs-lookup"><span data-stu-id="cd934-124">Assigned hours do not update correctly when assignments are changed using the Microsoft Project desktop client add-in.</span></span>
- <span data-ttu-id="cd934-125">As grelhas Estimativas e Rastreio de Projeto apresentam um código de moeda de venda incorreto quando a moeda do contrato é diferente da moeda do cliente e a organização é configurada para exibir códigos de moeda em vez de símbolos de moeda.</span><span class="sxs-lookup"><span data-stu-id="cd934-125">Project Tracking and Estimates grids display incorrect sales currency code when contract currency is different than customer currency and organization is configured to display currency codes instead of currency symbols.</span></span>
- <span data-ttu-id="cd934-126">A data de conclusão de um membro da Equipa acrescentará um dia se o horário de trabalho for de 24 horas por dia.</span><span class="sxs-lookup"><span data-stu-id="cd934-126">A Team member's finish date will add one day if the work hour schedule is 24-hours per day.</span></span>
- <span data-ttu-id="cd934-127">Na Agenda do Projeto, adicionar uma Categoria de Transação a uma tarefa não aciona o guardar automático.</span><span class="sxs-lookup"><span data-stu-id="cd934-127">On the Project Schedule, adding a Transaction Category to a task does not trigger auto save.</span></span>
- <span data-ttu-id="cd934-128">O seguinte erro é apresentado ao adicionar um membro da equipa ao Modelo de Projeto: "Os requisitos de recursos não podem ser associados a modelos de projeto".</span><span class="sxs-lookup"><span data-stu-id="cd934-128">The following error is displayed when adding a team member to the Project Template: "Resource requirements cannot be associated with project templates".</span></span> 
- <span data-ttu-id="cd934-129">O script da regra do friso "msdyn.Approval.CanApproveOrReject" apresenta um erro de tempo limite.</span><span class="sxs-lookup"><span data-stu-id="cd934-129">Ribbon rule script "msdyn.Approval.CanApproveOrReject" displays a timeout error.</span></span>

<span data-ttu-id="cd934-130">**Sales**</span><span class="sxs-lookup"><span data-stu-id="cd934-130">**Sales**</span></span>

<span data-ttu-id="cd934-131">Foram corrigidos os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="cd934-131">The following issues have been fixed:</span></span>

- <span data-ttu-id="cd934-132">A mensagem de erro de validação não apresentada quando uma Lista de Preços de Custo é selecionada na procura da Lista de Preços no formulário/entidade "Nova Lista de Preços de Projeto de Proposta".</span><span class="sxs-lookup"><span data-stu-id="cd934-132">Validation error message not displayed when a Cost Price List is selected in Price List lookup on 'New Quote Project Price List' form/entity.</span></span>
- <span data-ttu-id="cd934-133">Fechar a proposta como ganha não navega para o contrato criado se um BPF anexado à proposta estiver na fase final.</span><span class="sxs-lookup"><span data-stu-id="cd934-133">Closing the quote as won does not navigate to the created contract if a BPF attached to the quote is in the final stage.</span></span>
- <span data-ttu-id="cd934-134">Reverter **Vendas não fatutradas** está associado ao custo original quando uma entrada de tempo é recuperada.</span><span class="sxs-lookup"><span data-stu-id="cd934-134">Reversing **Unbilled Sales** is linked to original cost when a time entry is recalled.</span></span>
- <span data-ttu-id="cd934-135">Depois de selecionar o botão **Confirmar**, o estado da fatura não muda para **Confirmado** a menos que a fatura seja atualizada.</span><span class="sxs-lookup"><span data-stu-id="cd934-135">After selecting the **Confirm** button, the invoice status doesn't change to **Confirmed** unless the invoice is refreshed.</span></span>
