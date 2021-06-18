---
title: Novidades ou alterações na Versão da Atualização 19 do Project Service Automation, V3
description: Este tópico lista as funcionalidades e correções disponíveis no Project Service Automation V3, Versão da Atualização 19, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
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
ms.openlocfilehash: 7812bc41f32f9d4116c63990059f7dbc0351cf9e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006615"
---
# <a name="project-service-automation-update-release-19-v3"></a><span data-ttu-id="cc750-103">Versão da Atualização 19 do Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="cc750-103">Project Service Automation Update Release 19, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="cc750-104">Temos o prazer de anunciar a mais recente atualização à aplicação Project Service Automation para Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="cc750-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="cc750-105">Esta versão inclui algumas melhorias importantes na qualidade, desempenho e utilização.</span><span class="sxs-lookup"><span data-stu-id="cc750-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="cc750-106">Esta versão é compatível com o Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="cc750-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="cc750-107">Para atualizar esta versão, visite o Centro de Administração para o Dynamics 365 online e aceda à página de soluções para instalar a atualização.</span><span class="sxs-lookup"><span data-stu-id="cc750-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="cc750-108">Para obter mais informações, consulte [Instalar, atualizar ou remover uma solução preferencial](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="cc750-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="cc750-109">Este tópico lista as funcionalidades e correções novas ou alteradas para o PSA V3, Versão da Atualização 19.</span><span class="sxs-lookup"><span data-stu-id="cc750-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 19.</span></span> <span data-ttu-id="cc750-110">Esta versão tem o número de compilação V3.10.30.41 e está geralmente disponível através de uma atualização automática em maio de 2020.</span><span class="sxs-lookup"><span data-stu-id="cc750-110">This version has a build number of V3.10.30.41 and is generally available through a self-update in May 2020.</span></span>

## <a name="update-release-19"></a><span data-ttu-id="cc750-111">Versão da Atualização 19</span><span class="sxs-lookup"><span data-stu-id="cc750-111">Update Release 19</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="cc750-112">Correções de erros</span><span class="sxs-lookup"><span data-stu-id="cc750-112">Bug fixes</span></span>

<span data-ttu-id="cc750-113">**Tempo e Despesa**</span><span class="sxs-lookup"><span data-stu-id="cc750-113">**Time and Expense**</span></span>

<span data-ttu-id="cc750-114">Foram corrigidos os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="cc750-114">The following issues have been fixed:</span></span> 

- <span data-ttu-id="cc750-115">Os erros derivados das importações de entrada de tempo não surgem corretamente.</span><span class="sxs-lookup"><span data-stu-id="cc750-115">Errors derived from time entry imports are not surfaced correctly.</span></span>
- <span data-ttu-id="cc750-116">A Grelha de Entrada de Tempo não suporta o comportamento do campo **Apenas Data**.</span><span class="sxs-lookup"><span data-stu-id="cc750-116">Time Entry Grid does not support **Date Only** field behavior.</span></span>
- <span data-ttu-id="cc750-117">Os Recursos do Projeto são incapazes de criar uma despesa com um projeto.</span><span class="sxs-lookup"><span data-stu-id="cc750-117">Project Resources are unable to create an expense with a project.</span></span>

<span data-ttu-id="cc750-118">**Gestão de Projetos**</span><span class="sxs-lookup"><span data-stu-id="cc750-118">**Project Management**</span></span>

<span data-ttu-id="cc750-119">Foram corrigidos os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="cc750-119">The following issues have been fixed:</span></span> 

-  <span data-ttu-id="cc750-120">A tarefa secundária causa uma estimativa de esforço incorreta durante o Cálculo de Conclusão (EAC).</span><span class="sxs-lookup"><span data-stu-id="cc750-120">Grandchild task causes an incorrect effort estimate during the Completion (EAC) Calculation.</span></span>

<span data-ttu-id="cc750-121">**Sales**</span><span class="sxs-lookup"><span data-stu-id="cc750-121">**Sales**</span></span>

<span data-ttu-id="cc750-122">Foram corrigidos os seguintes problemas:</span><span class="sxs-lookup"><span data-stu-id="cc750-122">The following issues have been fixed:</span></span> 

- <span data-ttu-id="cc750-123">A ação **Recalcular** não funciona com detalhes de item de contrato de despesas ou detalhes de item de proposta.</span><span class="sxs-lookup"><span data-stu-id="cc750-123">The **Recalculate** action does not work with expense contract line details or quote line details.</span></span>
- <span data-ttu-id="cc750-124">**Atualizar preços** está em falta das estimativas de despesas.</span><span class="sxs-lookup"><span data-stu-id="cc750-124">**Update Prices** is missing for expense estimates.</span></span>
-  <span data-ttu-id="cc750-125">Os clientes não conseguem selecionar razões do estado do contrato personalizadas a partir da página **Contrato do Projeto**.</span><span class="sxs-lookup"><span data-stu-id="cc750-125">Customers are unable to select custom contract status reasons from the **Project Contract** page.</span></span>
- <span data-ttu-id="cc750-126">Os clientes experimentam um desempenho degradado ao criar uma lista de preços personalizada a partir de uma proposta.</span><span class="sxs-lookup"><span data-stu-id="cc750-126">Customers experience degraded performance when creating a custom price list from a quote.</span></span>
- <span data-ttu-id="cc750-127">Os clientes experimentam inconsistência com predefinições de **unidade** nas páginas **Detalhes de Item de Proposta** e **Detalhes de Item de Contrato**.</span><span class="sxs-lookup"><span data-stu-id="cc750-127">Customers experience inconsistency with **unit** defaults on **Quote Line Details** and **Contract Line Details** pages.</span></span>
- <span data-ttu-id="cc750-128">A adição de itens de categoria de transação não faturável a um item de contrato faturável não respeitará o tipo de faturação **Não faturável** da categoria de transação.</span><span class="sxs-lookup"><span data-stu-id="cc750-128">Adding non-chargeable transaction category items to a chargeable contract line will not respect the **Non-chargeable** billing type of the transaction category.</span></span>
- <span data-ttu-id="cc750-129">Os clientes não podem utilizar as funções e categorias recém-adicionadas em contratos previamente criados.</span><span class="sxs-lookup"><span data-stu-id="cc750-129">Customers can't use the newly added roles and category on previously created contracts.</span></span>
- <span data-ttu-id="cc750-130">Clientes experimentam desempenho degradado de recuperação desnecessária em PreValidateProjectTeamMemberUpdate.cs</span><span class="sxs-lookup"><span data-stu-id="cc750-130">Customers experience degraded performance Unnecessary retrieve in PreValidateProjectTeamMemberUpdate.cs</span></span>
- <span data-ttu-id="cc750-131">As funções configuradas como não faturáveis na lista **Categorias de Recursos** devem ser adicionadas ao separador **Funções Faturáveis** como **Não Faturáveis** no item de contrato de um projeto.</span><span class="sxs-lookup"><span data-stu-id="cc750-131">Roles set up as non-chargeable in the **Resource Categories** list should be added to the **Chargeable Roles** tab as **Non0chargeable** on the contract line for a project.</span></span>
- <span data-ttu-id="cc750-132">Os clientes podem experimentar um desempenho degradado ao criar um projeto porque **GetBookableResourceIdFromUser** recupera todas as colunas de recursos reservados em vez de apenas o ID primário.</span><span class="sxs-lookup"><span data-stu-id="cc750-132">Customers may experience degraded performance when creating a project because **GetBookableResourceIdFromUser** retrieves all columns of bookable resources instead of just the primary ID.</span></span>
- <span data-ttu-id="cc750-133">A entidade **TransactionType** que não tem o plug-in de atualização de pré-validação para impedir que os utilizadores entrem em **Unidades** e **GruposUnitários** que não são válidos para tipos de transação.</span><span class="sxs-lookup"><span data-stu-id="cc750-133">**TransactionType** entity missing the pre-validation update plug-in to prevent users from entering **Units** and **UnitGroups** that are not valid for transaction types.</span></span>
- <span data-ttu-id="cc750-134">O passo **Remover** não funciona para a importação de entrada de tempo.</span><span class="sxs-lookup"><span data-stu-id="cc750-134">The **Remove** step does not work for time entry import.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]