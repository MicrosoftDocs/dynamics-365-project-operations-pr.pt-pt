---
title: Novidades ou alterações na Versão da Atualização 21 do Project Service Automation, V3
description: Este tópico lista as funcionalidades e correções disponíveis no Project Service Automation V3, Versão da Atualização 21, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: dd894f27baac70238d0bd9e9b1a21a9a499e1ea7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002341"
---
# <a name="project-service-automation-update-release-21-v3"></a><span data-ttu-id="f9533-103">Versão da Atualização 21 do Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="f9533-103">Project Service Automation Update Release 21, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="f9533-104">Temos o prazer de anunciar a mais recente atualização à aplicação Project Service Automation para Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="f9533-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="f9533-105">Esta versão inclui algumas melhorias importantes na qualidade, desempenho e utilização.</span><span class="sxs-lookup"><span data-stu-id="f9533-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="f9533-106">Esta versão é compatível com o Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="f9533-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="f9533-107">Para atualizar esta versão, visite o Centro de Administração para o Dynamics 365 online e aceda à página de soluções para instalar a atualização.</span><span class="sxs-lookup"><span data-stu-id="f9533-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="f9533-108">Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="f9533-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="f9533-109">Este tópico lista as funcionalidades e correções novas ou alteradas para o Project Service Automation V3, Versão da Atualização 21.</span><span class="sxs-lookup"><span data-stu-id="f9533-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 21.</span></span> <span data-ttu-id="f9533-110">Esta versão tem o número de compilação V 3.10.32.50 e está geralmente disponível através de uma atualização automática em junho de 2020.</span><span class="sxs-lookup"><span data-stu-id="f9533-110">This version has a build number of V 3.10.32.50 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-21"></a><span data-ttu-id="f9533-111">Versão da Atualização 21</span><span class="sxs-lookup"><span data-stu-id="f9533-111">Update Release 21</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="f9533-112">Correções de erros</span><span class="sxs-lookup"><span data-stu-id="f9533-112">Bug fixes</span></span>

<span data-ttu-id="f9533-113">**Tempo e Despesa**</span><span class="sxs-lookup"><span data-stu-id="f9533-113">**Time and Expense**</span></span>

<span data-ttu-id="f9533-114">Foram corrigidos os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="f9533-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="f9533-115">Ao hospedar o **Controlo da Grelha de Entrada de Tempo** nos Dashboards, a grelha não utiliza toda a largura do recipiente da grelha do dashboard.</span><span class="sxs-lookup"><span data-stu-id="f9533-115">When hosting the **Time Entry Grid Control** in Dashboards, the grid does not utilize the full width of the dashboard grid container.</span></span>
- <span data-ttu-id="f9533-116">Para fusos horários específicos, o controlo da grelha de **Entrada de Tempo** não apresenta registos.</span><span class="sxs-lookup"><span data-stu-id="f9533-116">For specific time zones, the **Time Entry** grid control does not display records.</span></span>
- <span data-ttu-id="f9533-117">As entradas de tempo que são depois das 9:00 PM aparecem no dia errado.</span><span class="sxs-lookup"><span data-stu-id="f9533-117">Time entries that are after 9:00 PM appear on the wrong day.</span></span>
- <span data-ttu-id="f9533-118">Os utilizadores não podem apresentar despesas se a categoria de despesas, **Recibo de despesas exigido** não tiver qualquer valor.</span><span class="sxs-lookup"><span data-stu-id="f9533-118">Users are unable to submit expenses if the expense category, **Expense receipt required** has no value.</span></span>

<span data-ttu-id="f9533-119">**Gestão de Recursos**</span><span class="sxs-lookup"><span data-stu-id="f9533-119">**Resource Management**</span></span>

<span data-ttu-id="f9533-120">Foram corrigidos os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="f9533-120">The following issues have been fixed:</span></span>

- <span data-ttu-id="f9533-121">As reservas inativas são apresentadas na vista **Reconciliação**.</span><span class="sxs-lookup"><span data-stu-id="f9533-121">Inactive bookings are displayed in the **Reconciliation** view.</span></span>
- <span data-ttu-id="f9533-122">Faltava a validação genérica do recurso para garantir a existência de um estado de reserva válido.</span><span class="sxs-lookup"><span data-stu-id="f9533-122">Generic resource fulfillment was missing validation to ensure that a valid booking status exists.</span></span>

<span data-ttu-id="f9533-123">**Gestão de Projetos**</span><span class="sxs-lookup"><span data-stu-id="f9533-123">**Project Management**</span></span>

<span data-ttu-id="f9533-124">Foram corrigidos os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="f9533-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="f9533-125">As grelhas de formulário do **Projeto** (**Atribuição de Recursos**, **Tarefa**, vista **Reconciliação**, **Estimativas de Despesas**) continuam a ser editáveis mesmo quando um projeto não está ativo.</span><span class="sxs-lookup"><span data-stu-id="f9533-125">The **Project** form grids (**Resource Assignment**, **Task**, **Reconciliation** view, **Expense Estimates**) remain editable even when a project is not active.</span></span>
- <span data-ttu-id="f9533-126">Os clientes duplicados não podem ser unidos a clientes que estejam ligados a contratos de projeto confirmados.</span><span class="sxs-lookup"><span data-stu-id="f9533-126">Duplicate customers can't be merged with customers that are linked to confirmed project contracts.</span></span>
- <span data-ttu-id="f9533-127">Quando um recurso que não tenha um calendário válido é adicionado, o sistema não devolve uma mensagem de erro amigável ao utilizador.</span><span class="sxs-lookup"><span data-stu-id="f9533-127">When a resource who does not have a valid calendar is added, the system does not return a user friendly-error message.</span></span>
- <span data-ttu-id="f9533-128">O botão **Adicionar Tarefa** na grelha de tarefas está ativado quando o projeto está ligado ao **Suplemento do Microsoft Project**.</span><span class="sxs-lookup"><span data-stu-id="f9533-128">The **Add Task** button on the task grid is enabled when the project is linked to **Microsoft Project add-in**.</span></span>
- <span data-ttu-id="f9533-129">O esforço cresce incontrolavelmente quando uma tarefa com uma categoria é atribuída a um recurso com uma função para a qual existe um preço de custo definido.</span><span class="sxs-lookup"><span data-stu-id="f9533-129">Effort grows uncontrollably when a task with a category is assigned to a resource with a role for which there is a cost price defined.</span></span>

<span data-ttu-id="f9533-130">**Sales**</span><span class="sxs-lookup"><span data-stu-id="f9533-130">**Sales**</span></span>

<span data-ttu-id="f9533-131">Foram feitos os seguintes melhoramentos:</span><span class="sxs-lookup"><span data-stu-id="f9533-131">The following enhancements have been made:</span></span>

- <span data-ttu-id="f9533-132">A **Frequência de Fatura** e o **Início da Faturação** foram transferidos para o separador **Agenda de Faturas**.</span><span class="sxs-lookup"><span data-stu-id="f9533-132">**Invoice Frequency** and **Billing Start** have been moved to the **Invoice Schedule** tab.</span></span>

<span data-ttu-id="f9533-133">Foram corrigidos os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="f9533-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="f9533-134">O **Preço Total de Venda** é zero (0) para **Categoria**, embora a **Função** tenha um preço de venda total que não é zero.</span><span class="sxs-lookup"><span data-stu-id="f9533-134">**Total Sales Price** is zero (0) for **Category** even though **Role** has a total sales price that is not zero.</span></span>
- <span data-ttu-id="f9533-135">Os clientes não podem alterar o valor do campo de **Estado da Fatura** para **Pronto para Faturação** quando outro processo personalizado está a atualizar um campo adicional.</span><span class="sxs-lookup"><span data-stu-id="f9533-135">Customers can't change the value of the **Invoice Status** field to **Ready for invoicing** when another customized process is updating an additional field.</span></span>
- <span data-ttu-id="f9533-136">O botão **Atualizar Linhas de Fatura** pode criar várias linhas duplicadas se for repetidamente selecionado.</span><span class="sxs-lookup"><span data-stu-id="f9533-136">The **Refresh Invoice Lines** button can create multiple duplicated lines if it is repeatedly selected.</span></span>
- <span data-ttu-id="f9533-137">O botão **Atualizar Preços** não funciona na subgrelha **Preços de Função** no formulário **Vista Rápida**.</span><span class="sxs-lookup"><span data-stu-id="f9533-137">The **Update Prices** button doesn't work on the **Role Prices** subgrid in the **Quick View** form.</span></span>
- <span data-ttu-id="f9533-138">A lógica de **Resolução da Lista de Preços de Venda** processa incorretamente fusos horários, resultando na seleção incorreta das listas de preços.</span><span class="sxs-lookup"><span data-stu-id="f9533-138">The **Sales Price List Resolution** logic improperly handles time zones, resulting in the incorrect selection of price lists.</span></span>
- <span data-ttu-id="f9533-139">O **Custo Total Real** de um projeto pode estar incorreto por um valor fracional após a aprovação de uma única entrada.</span><span class="sxs-lookup"><span data-stu-id="f9533-139">A project’s **Total Actual Cost** can be off by a fractional amount after a single time entry is approved.</span></span>
- <span data-ttu-id="f9533-140">A lógica de **Resolução de Preços** não fornece uma mensagem de erro amigável se **RolePrice Recuperado** não tiver valores nos campos **Unidade Principal** e **Preço na Unidade Principal**.</span><span class="sxs-lookup"><span data-stu-id="f9533-140">The **Price Resolution** logic does not provide a user-friendly error message if **Retrieved RolePrice** doesn't have values in **'Primary Unit'** and **'Price In Primary Unit'** fields.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]