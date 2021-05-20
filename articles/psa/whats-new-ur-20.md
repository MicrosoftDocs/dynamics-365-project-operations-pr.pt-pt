---
title: Novidades ou alterações na Versão da Atualização 20 do Project Service Automation, V3
description: Este tópico lista as funcionalidades e correções disponíveis na Versão da Atualização 20 do Project Service Automation, V3
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
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
ms.openlocfilehash: 124dad5438f9489d1ddbc952cecaee977b6b7f01
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949108"
---
# <a name="project-service-automation-update-release-20-v3"></a><span data-ttu-id="51c90-103">Versão da Atualização 20 do Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="51c90-103">Project Service Automation Update Release 20, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="51c90-104">Temos o prazer de anunciar a mais recente atualização à aplicação Project Service Automation para Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="51c90-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="51c90-105">Esta versão inclui algumas melhorias importantes na qualidade, desempenho e utilização.</span><span class="sxs-lookup"><span data-stu-id="51c90-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="51c90-106">Esta versão é compatível com o Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="51c90-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="51c90-107">Para atualizar esta versão, visite o Centro de Administração para o Dynamics 365 online e aceda à página de soluções para instalar a atualização.</span><span class="sxs-lookup"><span data-stu-id="51c90-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="51c90-108">Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="51c90-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="51c90-109">Este tópico lista as funcionalidades e correções novas ou alteradas para o Project Service Automation V3, Versão da Atualização 20.</span><span class="sxs-lookup"><span data-stu-id="51c90-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 20.</span></span> <span data-ttu-id="51c90-110">Esta versão tem o número de compilação V 3.10.31.37 e está geralmente disponível através de uma atualização automática em junho de 2020.</span><span class="sxs-lookup"><span data-stu-id="51c90-110">This version has a build number of V 3.10.31.37 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-20"></a><span data-ttu-id="51c90-111">Versão da Atualização 20</span><span class="sxs-lookup"><span data-stu-id="51c90-111">Update Release 20</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="51c90-112">Correções de erros</span><span class="sxs-lookup"><span data-stu-id="51c90-112">Bug fixes</span></span>

<span data-ttu-id="51c90-113">**Gestão de Projetos**</span><span class="sxs-lookup"><span data-stu-id="51c90-113">**Project Management**</span></span>

<span data-ttu-id="51c90-114">Foram corrigidos os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="51c90-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="51c90-115">Importar membros da equipa do projeto com um método de alocação que requer horas resulta numa mensagem de erro pouco clara quando as horas especificadas são zero.</span><span class="sxs-lookup"><span data-stu-id="51c90-115">Importing project team members with an allocation method that requires hours results in an unclear error message when the specified hours are zero.</span></span>
- <span data-ttu-id="51c90-116">Os utilizadores recebem um erro incorreto quando o número máximo de carateres foi introduzido no campo **Descrição** para uma tarefa de projeto.</span><span class="sxs-lookup"><span data-stu-id="51c90-116">Users receive an incorrect error when the maximum number of characters have been entered into the **Description** field for a project task.</span></span>
- <span data-ttu-id="51c90-117">A página de **descarregamento do add-in Microsoft Dynamics 365 Project Service Automation** redireciona para a página de descarregamento em inglês quando as definições de idioma do utilizador são definidas para japonês.</span><span class="sxs-lookup"><span data-stu-id="51c90-117">The **Microsoft Dynamics 365 Project Service Automation add-in download** page redirects to the English download page when the user’s language settings are set to Japanese.</span></span>
- <span data-ttu-id="51c90-118">Quando ocorre um erro do servidor, a etiqueta de sincronização no separador **Agendar** do formulário **Projetos** por vezes permanece.</span><span class="sxs-lookup"><span data-stu-id="51c90-118">When a server error occurs, the synchronization label on the **Schedule** tab of the **Projects** form sometimes remains.</span></span>
- <span data-ttu-id="51c90-119">Atualizações de tarefas redundantes são enviadas para o servidor quando uma tarefa é modificada.</span><span class="sxs-lookup"><span data-stu-id="51c90-119">Redundant task updates are being sent to the server when a task is modified.</span></span>

<span data-ttu-id="51c90-120">**Sales**</span><span class="sxs-lookup"><span data-stu-id="51c90-120">**Sales**</span></span>

<span data-ttu-id="51c90-121">Foram corrigidos os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="51c90-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="51c90-122">No formulário **Contrato**, clicar duas vezes com o botão direito do rato em **Criar Fatura** cria duas faturas para um único registo real.</span><span class="sxs-lookup"><span data-stu-id="51c90-122">On the **Contract** form, double-clicking **Create Invoice** creates two invoices for a single actuals record.</span></span>
- <span data-ttu-id="51c90-123">No Internet Explorer 11, os utilizadores são incapazes de criar entradas de despesas.</span><span class="sxs-lookup"><span data-stu-id="51c90-123">In Internet Explorer 11, users are unable to create expense entries.</span></span>
- <span data-ttu-id="51c90-124">A reversão do Custo e a reversão de Valores Reais de Vendas Não Faturáveis não estão ligados.</span><span class="sxs-lookup"><span data-stu-id="51c90-124">Reversal of Cost and reversal of Unbilled Sales Actuals are not linked.</span></span>
- <span data-ttu-id="51c90-125">O botão **Atualizar Valores Reais** no formulário **Projeto** não atualiza as **Horas Reais da Tarefa**.</span><span class="sxs-lookup"><span data-stu-id="51c90-125">The **Refresh Actuals** button on the **Project** form does not refresh **Task Actual Hours**.</span></span>
- <span data-ttu-id="51c90-126">O plug-in **PreValidateProjectTeamMemberCreate** pode criar recursos agendáveis genéricos duplicados quando o atributo **msdyn_isgenericresourceprojectscoped** é definido como **False**.</span><span class="sxs-lookup"><span data-stu-id="51c90-126">The **PreValidateProjectTeamMemberCreate** plug-in can create duplicate generic bookable resources when the attribute **msdyn_isgenericresourceprojectscoped** is set to **False**.</span></span>
- <span data-ttu-id="51c90-127">**Recalcular** elimina os custos faturáveis dos detalhes de item de proposta baseada e detalhes de item de contrato baseados em produtos.</span><span class="sxs-lookup"><span data-stu-id="51c90-127">**Recalculate** clears chargeable costs of product-based quote line details and contract line details.</span></span>
- <span data-ttu-id="51c90-128">Em cenários específicos, o plug-in **PostEstimateLineUpdate** apresenta um erro de exceção de referência nulo.</span><span class="sxs-lookup"><span data-stu-id="51c90-128">In specific scenarios, the **PostEstimateLineUpdate** plug-in displays a null teference exception error.</span></span>
- <span data-ttu-id="51c90-129">A duração da fase de tempo no **Gráfico de Análise de Rentabilidade** não corresponde à duração dos custos no detalhe do item de proposta de preço fixo da proposta.</span><span class="sxs-lookup"><span data-stu-id="51c90-129">Time phase duration on the **Profitability Analysis Chart** does not match duration of the costs in the fixed-price quote line detail of the quote.</span></span>
- <span data-ttu-id="51c90-130">Os valores de unidade e de grupo de unidades não são predefinidos corretamente para as categorias de despesas nos formulários **Detalhes do Item de Contrato** e **Detalhes do Item de Proposta**.</span><span class="sxs-lookup"><span data-stu-id="51c90-130">Unit and unit group values do not default correctly for expense categories on the **Contract Line Details** and **Quote Line Details** forms.</span></span>
- <span data-ttu-id="51c90-131">As listas de **Preço de Custo da Unidade Organizacional** permitem sobreposições na efetividade da data.</span><span class="sxs-lookup"><span data-stu-id="51c90-131">**Org Unit Cost Price** lists permit overlaps in the date effectivity.</span></span>
- <span data-ttu-id="51c90-132">Os utilizadores não estão autorizados a alterar **OrgUnit** quando o tipo de encomenda não é baseado no trabalho, pois irá conduzir a um erro de exceção de referência nulo.</span><span class="sxs-lookup"><span data-stu-id="51c90-132">Users are not permitted to change the **OrgUnit** when the order type is not work-based because it will lead to a null reference exception error.</span></span>
- <span data-ttu-id="51c90-133">Ao tentar navegar a partir do formulário **Detalhes do Item de Proposta**, regresse ao separador **Proposta**, o formulário atualiza e apresenta o separador **Resumo**.</span><span class="sxs-lookup"><span data-stu-id="51c90-133">When attempting to navigate from the **Quote Line Details** form, back to the **Quote** tab, the form refreshes and displays the **Summary** tab.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]