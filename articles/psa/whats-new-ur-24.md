---
title: Novidades ou alterações na Versão da Atualização 24 do Project Service Automation, V3
description: Este tópico lista as funcionalidades e correções disponíveis no Project Service Automation V3, Versão da Atualização 24, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: c95a9dcada4fbf6c462df29d450aaafab4e73aa5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000270"
---
# <a name="project-service-automation-update-release-24-v3"></a><span data-ttu-id="99fa3-103">Versão da Atualização 24 do Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="99fa3-103">Project Service Automation Update Release 24, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="99fa3-104">Temos o prazer de anunciar a mais recente atualização à aplicação Project Service Automation para Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="99fa3-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="99fa3-105">Esta versão inclui algumas melhorias importantes na qualidade, desempenho e utilização.</span><span class="sxs-lookup"><span data-stu-id="99fa3-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="99fa3-106">Esta versão é compatível com o Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="99fa3-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="99fa3-107">Para atualizar esta versão, visite o Centro de Administração para o Dynamics 365 online e aceda à página de soluções para instalar a atualização.</span><span class="sxs-lookup"><span data-stu-id="99fa3-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="99fa3-108">Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="99fa3-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="99fa3-109">Este tópico lista as funcionalidades e correções novas ou alteradas para o Project Service Automation V3, Versão da Atualização 24.</span><span class="sxs-lookup"><span data-stu-id="99fa3-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 24.</span></span> <span data-ttu-id="99fa3-110">Esta versão tem um número de compilação de V 3.10.42.43 e está geralmente disponível através de uma Atualização automática em outubro de 2020.</span><span class="sxs-lookup"><span data-stu-id="99fa3-110">This version has a build number of V 3.10.42.43 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-24"></a><span data-ttu-id="99fa3-111">Versão da Atualização 24</span><span class="sxs-lookup"><span data-stu-id="99fa3-111">Update Release 24</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="99fa3-112">Correções de erros</span><span class="sxs-lookup"><span data-stu-id="99fa3-112">Bug fixes</span></span>

<span data-ttu-id="99fa3-113">**Sales**</span><span class="sxs-lookup"><span data-stu-id="99fa3-113">**Sales**</span></span>

<span data-ttu-id="99fa3-114">Foram corrigidos os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="99fa3-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="99fa3-115">Problema ao definir a lista de preços predefinidos dos produtos.</span><span class="sxs-lookup"><span data-stu-id="99fa3-115">Problem while setting default price list of products.</span></span>
- <span data-ttu-id="99fa3-116">O desempenho da vitória de Proposta é lento devido à lista de preços incorporados e à cópia dos registos de preços de função.</span><span class="sxs-lookup"><span data-stu-id="99fa3-116">Performance of Quote win is slow due to the embedded price list and role price records copy.</span></span>
- <span data-ttu-id="99fa3-117">**Contrato do Projet/Hub de Vendas** > **Quantidade de Linha de Item/Encomenda de Linha de Produtos** é automaticamente arredondado para o número inteiro mais próximo.</span><span class="sxs-lookup"><span data-stu-id="99fa3-117">**Project Contract/Sales Hub** > **Product Line Item/Order Line Quantity** is automatically rounded to the nearest integer.</span></span>
- <span data-ttu-id="99fa3-118">Elevar para privilégios do sistema ao ler listas de preços.</span><span class="sxs-lookup"><span data-stu-id="99fa3-118">Elevate to system privileges when reading price lists.</span></span>
- <span data-ttu-id="99fa3-119">Copie os campos de endereço do cliente **address1_freighttermscode** e **address1_shippingmethodcode** para Proposta/Encomenda.</span><span class="sxs-lookup"><span data-stu-id="99fa3-119">Copy customer address fields **address1_freighttermscode** and **address1_shippingmethodcode** to Quote/Order.</span></span> 


<span data-ttu-id="99fa3-120">**Tempo e Despesa**</span><span class="sxs-lookup"><span data-stu-id="99fa3-120">**Time and Expense**</span></span>

<span data-ttu-id="99fa3-121">Foram corrigidos os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="99fa3-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="99fa3-122">A **Grelha de Entrada de Tempo** não suporta o comportamento de tempo **Apenas Data**.</span><span class="sxs-lookup"><span data-stu-id="99fa3-122">The **Time Entry Grid** doesn't support **Date Only** time behavior.</span></span>
- <span data-ttu-id="99fa3-123">**Entrada de Tempo** não atualizar automaticamente.</span><span class="sxs-lookup"><span data-stu-id="99fa3-123">**Time Entry** is not refreshing automatically.</span></span> <span data-ttu-id="99fa3-124">É necessária uma atualização manual.</span><span class="sxs-lookup"><span data-stu-id="99fa3-124">A manual refresh is required.</span></span>
- <span data-ttu-id="99fa3-125">Não é possível importar as entradas de tempo de uma atribuição quando há uma pausa (0 horas) nas atribuições de um recurso.</span><span class="sxs-lookup"><span data-stu-id="99fa3-125">Unable to import the time entries from an assignment when there is a break (0 hours) in a resource's assignments.</span></span>
- <span data-ttu-id="99fa3-126">Ao criar uma entrada de tempo, defina o início para o mesmo **msdyn_date**.</span><span class="sxs-lookup"><span data-stu-id="99fa3-126">When creating a time entry, set the start to the same as **msdyn_date**.</span></span>
- <span data-ttu-id="99fa3-127">Reativar a edição em massa para entrada de tempo.</span><span class="sxs-lookup"><span data-stu-id="99fa3-127">Re-enable bulk edit for time entry.</span></span>

<span data-ttu-id="99fa3-128">**Gestão de Recursos**</span><span class="sxs-lookup"><span data-stu-id="99fa3-128">**Resource Management**</span></span>

<span data-ttu-id="99fa3-129">Foram corrigidos os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="99fa3-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="99fa3-130">Tentar atualizar o estado de uma reserva inter-diária sem um requisito irá lançar uma exceção null-ref.</span><span class="sxs-lookup"><span data-stu-id="99fa3-130">Trying to update the status of an inter-day booking without a requirement will throw a null-ref exception.</span></span>
- <span data-ttu-id="99fa3-131">Erro ao carregar a **Vista de Reconciliação**.</span><span class="sxs-lookup"><span data-stu-id="99fa3-131">Error loading the **Reconciliation View**.</span></span>


<span data-ttu-id="99fa3-132">**Gestão de Projetos**</span><span class="sxs-lookup"><span data-stu-id="99fa3-132">**Project Management**</span></span>

<span data-ttu-id="99fa3-133">Foram corrigidos os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="99fa3-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="99fa3-134">Na **Agenda do Projeto**, ao mudar de **Manual** para **Automático**, a atualização automática não é concluída.</span><span class="sxs-lookup"><span data-stu-id="99fa3-134">In the **Project Schedule**, when changing from **Manual** to **Auto**, auto save is not completing.</span></span>
- <span data-ttu-id="99fa3-135">Os custos de despesas não contam para a variância na **Grelha de Monitorização do Projeto**.</span><span class="sxs-lookup"><span data-stu-id="99fa3-135">Expense costs should not calculate toward variance on the **Project Tracking Grid**.</span></span>
- <span data-ttu-id="99fa3-136">Comportamento inconsistente para colunas de **Etiqueta de estimativas** durante o carregamento vs. alterar o tipo **Fase de Tempo**.</span><span class="sxs-lookup"><span data-stu-id="99fa3-136">Inconsistent behavior for **Estimates tag** columns during load versus changing the **Time-Phase** type.</span></span>
- <span data-ttu-id="99fa3-137">O custo real de um projeto pode não refletir os totais de **Atuais**.</span><span class="sxs-lookup"><span data-stu-id="99fa3-137">The actual cost on a project may not reflect the totals from **Actuals**.</span></span>
- <span data-ttu-id="99fa3-138">**Data de Conclusão Estimada** no separador **Resumo** não corresponde à **Agenda WBS**.</span><span class="sxs-lookup"><span data-stu-id="99fa3-138">**Estimated Finish Date** on the **Summary** tab does not match the **WBS Schedule**.</span></span>
- <span data-ttu-id="99fa3-139">**Atualizar Horas Atuais** no avanço não funciona corretamente.</span><span class="sxs-lookup"><span data-stu-id="99fa3-139">**Update Actual Hours** on outdent does not work correctly.</span></span>
- <span data-ttu-id="99fa3-140">Um Gestor de projetos fora da raiz **BU** não pode criar um projeto.</span><span class="sxs-lookup"><span data-stu-id="99fa3-140">A Project manager outside of root **BU** can't create a project.</span></span>
- <span data-ttu-id="99fa3-141">As alterações à tarefa ou à categoria em **Estimativas de Despesas** não persistem.</span><span class="sxs-lookup"><span data-stu-id="99fa3-141">Changes to task or category on **Expense Estimates** are not persisted.</span></span>
- <span data-ttu-id="99fa3-142">**Cópia do contrato** copia os horários da fatura e o estado da execução.</span><span class="sxs-lookup"><span data-stu-id="99fa3-142">**Copy of contract** copies the invoice schedules and the run status.</span></span>
- <span data-ttu-id="99fa3-143">O botão **Atualizar Atuais** calcula incorretamente as tarefas resumidas.</span><span class="sxs-lookup"><span data-stu-id="99fa3-143">**Refresh Actuals** button incorrectly calculates summary tasks.</span></span>
- <span data-ttu-id="99fa3-144">Microsoft Project Add-in: Corrigir um erro de referência nulo se algum membro da equipa tiver uma unidade de recursos vazia.</span><span class="sxs-lookup"><span data-stu-id="99fa3-144">Microsoft Project Add-in: Fix null reference error if any team member has an empty resourcing unit.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]