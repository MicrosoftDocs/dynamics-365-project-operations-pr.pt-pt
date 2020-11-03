---
title: Contratos de projeto
description: Este tópico fornece exemplos dos contratos de projeto que pode criar para vários tipos de projetos e fontes de financiamento, e como pode gerir contratos e faturar os clientes do projeto.
author: Yowelle
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b7d15523f1b22bb8813a47f9f822f12bc4162104
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082535"
---
# <a name="project-contracts"></a><span data-ttu-id="59a0a-103">Contratos de projeto</span><span class="sxs-lookup"><span data-stu-id="59a0a-103">Project contracts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="59a0a-104">Este item fornece exemplos dos contratos de projeto que pode criar para vários tipos de projetos e fontes de financiamento, e como pode gerir contratos e faturar os clientes do projeto.</span><span class="sxs-lookup"><span data-stu-id="59a0a-104">This article provides examples of the project contracts that you can create for various types of projects and funding sources, and how you can manage contracts and invoice project customers.</span></span>

<span data-ttu-id="59a0a-105">O tipo de projeto que cria para um contrato de projeto determina o método que é utilizado para faturar os clientes do projeto.</span><span class="sxs-lookup"><span data-stu-id="59a0a-105">The type of project that you create for a project contract determines the method that is used to invoice project customers.</span></span> <span data-ttu-id="59a0a-106">Pode alterar um contrato de projeto e o projeto relacionado, mas não pode alterar o tipo de projeto.</span><span class="sxs-lookup"><span data-stu-id="59a0a-106">You can change a project contract and the related project, but you can't change the project type.</span></span> 

<span data-ttu-id="59a0a-107">Ao utilizar um contrato de projeto, pode faturar um ou mais projetos ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="59a0a-107">By using a project contract, you can invoice one or more projects at the same time.</span></span> <span data-ttu-id="59a0a-108">O contrato de projeto também ajuda a garantir um procedimento de faturação consistente para cada subprojecto numa estrutura de projetos.</span><span class="sxs-lookup"><span data-stu-id="59a0a-108">The project contract also helps guarantee a consistent invoicing procedure for every subproject in a project structure.</span></span> 

<span data-ttu-id="59a0a-109">Cada projeto que será faturado tem de estar associado a um contrato de projeto.</span><span class="sxs-lookup"><span data-stu-id="59a0a-109">Every project that will be invoiced must be associated with a project contract.</span></span> <span data-ttu-id="59a0a-110">As definições para um contrato de projeto aplicam-se a todos os projetos e subprojetos associados a esse contrato de projeto.</span><span class="sxs-lookup"><span data-stu-id="59a0a-110">The settings for a project contract apply to all projects and subprojects that are associated with that project contract.</span></span> 

<span data-ttu-id="59a0a-111">Um contrato de projeto pode especificar uma ou mais fontes de financiamento.</span><span class="sxs-lookup"><span data-stu-id="59a0a-111">A project contract can specify one or more sources of funding.</span></span> <span data-ttu-id="59a0a-112">Portanto, pode dividir a faturação entre vários financiadores, configurar limites de financiamento para as fontes de financiamento não serem faturadas mais do que um montante especificado e configurar regras de financiamento para cobrar gastos.</span><span class="sxs-lookup"><span data-stu-id="59a0a-112">Therefore, you can split the billing among multiple funders, set up funding limits so that funding sources are not billed more than a specified amount, and configure funding rules for charging expenditures.</span></span>

## <a name="funding-for-project-contracts"></a><span data-ttu-id="59a0a-113">Financiamento para contratos de projeto</span><span class="sxs-lookup"><span data-stu-id="59a0a-113">Funding for project contracts</span></span>
<span data-ttu-id="59a0a-114">Alguns contratos de projeto especificam que várias partes partilham a responsabilidade de financiamento dos custos de projeto.</span><span class="sxs-lookup"><span data-stu-id="59a0a-114">Some project contracts specify that multiple parties share the responsibility for funding the project costs.</span></span> <span data-ttu-id="59a0a-115">Seguem-se alguns exemplos:</span><span class="sxs-lookup"><span data-stu-id="59a0a-115">Here are some examples:</span></span>

-   <span data-ttu-id="59a0a-116">Um grande cliente com múltiplas divisões solicita que o financiamento de um projeto seja dividido por divisão.</span><span class="sxs-lookup"><span data-stu-id="59a0a-116">A large customer that has multiple divisions requests that funding of a project be split by division.</span></span>
-   <span data-ttu-id="59a0a-117">A sua empresa partilha os custos de um grande projeto com uma organização externa.</span><span class="sxs-lookup"><span data-stu-id="59a0a-117">Your company shares the costs of a large project with an external organization.</span></span>
-   <span data-ttu-id="59a0a-118">Um projeto rodoviário é cofinanciado por dois municípios.</span><span class="sxs-lookup"><span data-stu-id="59a0a-118">A  road project is co-funded by two municipalities.</span></span>
-   <span data-ttu-id="59a0a-119">Um projeto de ponte é financiado por uma subvenção do governo e uma empresa privada.</span><span class="sxs-lookup"><span data-stu-id="59a0a-119">A bridge project is funded by a government grant and a private corporation.</span></span>

<span data-ttu-id="59a0a-120">No Dynamics 365 Finance, pode dividir a faturação para uma única transação ou um projeto inteiro entre vários clientes, subvenções ou organizações.</span><span class="sxs-lookup"><span data-stu-id="59a0a-120">In Dynamics 365 Finance, you can split the billing for a single transaction or an entire project among multiple customers, grants, or organizations.</span></span> 

<span data-ttu-id="59a0a-121">Nos projetos com múltiplos financiadores, todas as partes que contribuem para o financiamento de um projeto de financiamento avançado são chamadas fontes de financiamento.</span><span class="sxs-lookup"><span data-stu-id="59a0a-121">In projects that have multiple funders, all parties that contribute to the funding of an advanced funding project are called funding sources.</span></span> <span data-ttu-id="59a0a-122">Depois de um cliente, organização ou subvenção ser definido como fonte de financiamento, pode ser atribuído a uma ou mais regras de financiamento.</span><span class="sxs-lookup"><span data-stu-id="59a0a-122">After a customer, organization, or grant is defined as a funding source, it can be assigned to one or more funding rules.</span></span> <span data-ttu-id="59a0a-123">As regras de financiamento contêm os critérios que determinam a forma como os encargos são atribuídos às várias fontes de financiamento para um projeto.</span><span class="sxs-lookup"><span data-stu-id="59a0a-123">Funding rules contain the criteria that determines how charges are allocated to the various funding sources for a project.</span></span> 

<span data-ttu-id="59a0a-124">Uma vez que os itens armazenados, como os que aparecem nas requisições de compra e nas notas de encomenda, não podem ser divididos, o montante do custo não pode ser dividido entre várias fontes de financiamento no momento da distribuição.</span><span class="sxs-lookup"><span data-stu-id="59a0a-124">Because stocked items, such as those that appear on purchase requisitions and purchase orders, can't be split, the cost amount can't be split among multiple funding sources at the time of distribution.</span></span> <span data-ttu-id="59a0a-125">Por conseguinte, o valor da fonte de financiamento mantém-se em 0 (zero) até a saída de stock ser lançada.</span><span class="sxs-lookup"><span data-stu-id="59a0a-125">Therefore, the funding source value remains 0 (zero) until the inventory issue is posted.</span></span> <span data-ttu-id="59a0a-126">Quando a saída de stock é lançada, o montante do custo é distribuído de acordo com as regras de distribuição da conta para o projeto.</span><span class="sxs-lookup"><span data-stu-id="59a0a-126">When the inventory issue is posted, the cost amount is distributed according to the account distribution rules for the project.</span></span>

<span data-ttu-id="59a0a-127">Seguem-se alguns passos que pode dar para facilitar a divisão da faturação entre várias fontes de financiamento:</span><span class="sxs-lookup"><span data-stu-id="59a0a-127">Here are some steps that you can take to make it easier to split the billing among multiple funding sources:</span></span>

-   <span data-ttu-id="59a0a-128">Especifique que todas as transações introduzidas para um projeto utilizam a mesma moeda de venda que o contrato de projeto.</span><span class="sxs-lookup"><span data-stu-id="59a0a-128">Specify that all transactions that are entered for a project use the same sales currency as the project contract.</span></span>
-   <span data-ttu-id="59a0a-129">Configure limites de financiamento para uma fonte de financiamento não ser faturada mais do que um montante especificado para um projeto.</span><span class="sxs-lookup"><span data-stu-id="59a0a-129">Set up funding limits, so that a funding source isn't invoiced more than a specified amount toward a project.</span></span>
-   <span data-ttu-id="59a0a-130">Configure as regras de financiamento e os limites de financiamento para cada trabalhador, item, categoria, grupo de categorias e tipo de transação (ou para todos os tipos de transações).</span><span class="sxs-lookup"><span data-stu-id="59a0a-130">Configure funding rules and funding limits for each worker, item, category, category group, and transaction type (or for all transaction types).</span></span>
-   <span data-ttu-id="59a0a-131">Selecione as datas de início e fim opcionais para definir o período em que cada regra de financiamento é válida.</span><span class="sxs-lookup"><span data-stu-id="59a0a-131">Select optional start and end dates to define the period when each funding rule is valid.</span></span>
-   <span data-ttu-id="59a0a-132">Especifique a percentagem pela qual cada fonte de financiamento é responsável.</span><span class="sxs-lookup"><span data-stu-id="59a0a-132">Specify the percentage that each funding source is responsible for.</span></span>
-   <span data-ttu-id="59a0a-133">Especifique qual a fonte de financiamento responsável pela arredondamento das diferenças que são causadas pelos cálculos da alocação de financiamento.</span><span class="sxs-lookup"><span data-stu-id="59a0a-133">Specify which funding source is responsible for rounding differences that are caused by funding allocation calculations.</span></span>
-   <span data-ttu-id="59a0a-134">Configure regras que determinem como os custos do projeto são faturados aos clientes externos e cobrados às organizações internas.</span><span class="sxs-lookup"><span data-stu-id="59a0a-134">Set up rules that determine how project costs are invoiced to external customers and charged to internal organizations.</span></span>
-   <span data-ttu-id="59a0a-135">Registe as transações numa conta de financiamento retido até poder ser obtido financiamento adicional ou até decidir suportar os custos internamente.</span><span class="sxs-lookup"><span data-stu-id="59a0a-135">Record transactions in an on-hold funding account until additional funding can be obtained, or until you decide to bear the costs internally.</span></span>

<span data-ttu-id="59a0a-136">Para determinar o grupo fiscal a associar a uma transação, é procurada no projeto uma atribuição de grupo fiscal.</span><span class="sxs-lookup"><span data-stu-id="59a0a-136">To determine which tax group to associate with a transaction, the project is searched for a tax group assignment.</span></span> <span data-ttu-id="59a0a-137">Se não tiver sido feita nenhuma atribuição de grupos fiscais a nível do projeto, é procurado o contrato de projeto.</span><span class="sxs-lookup"><span data-stu-id="59a0a-137">If no tax group assignment has been made at the project level, the project contract is searched.</span></span>

### <a name="example-multiple-funding-sources-simple"></a><span data-ttu-id="59a0a-138">Exemplo: Múltiplas fontes de financiamento (simples)</span><span class="sxs-lookup"><span data-stu-id="59a0a-138">Example: Multiple funding sources (simple)</span></span>

<span data-ttu-id="59a0a-139">O quadro seguinte fornece cenários para gerir a alocação de financiamento entre múltiplas fontes de financiamento.</span><span class="sxs-lookup"><span data-stu-id="59a0a-139">The following table provides scenarios for managing funding allocation among multiple funding sources.</span></span> <span data-ttu-id="59a0a-140">Estes cenários baseiam-se nos seguintes pressupostos:</span><span class="sxs-lookup"><span data-stu-id="59a0a-140">These scenarios are based on the following assumptions:</span></span>

-   <span data-ttu-id="59a0a-141">As definições prioritárias são tidas em conta na alocação de fundos antes de serem aplicados outros critérios de regras de financiamento.</span><span class="sxs-lookup"><span data-stu-id="59a0a-141">Priority settings are factored into the allocation of funds before other funding rule criteria are applied.</span></span>
-   <span data-ttu-id="59a0a-142">Não foi especificado nenhum intervalo de datas para definir o período d durante o qual a regra de financiamento é válida.</span><span class="sxs-lookup"><span data-stu-id="59a0a-142">No date range has been specified to define the period d when the funding rule is valid.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="59a0a-143"><strong>Cenário</strong></span><span class="sxs-lookup"><span data-stu-id="59a0a-143"><strong>Scenario</strong></span></span></td>
<td><span data-ttu-id="59a0a-144"><strong>Fonte de financiamento</strong></span><span class="sxs-lookup"><span data-stu-id="59a0a-144"><strong>Funding source</strong></span></span></td>
<td><span data-ttu-id="59a0a-145"><strong>Percentagem de alocação</strong></span><span class="sxs-lookup"><span data-stu-id="59a0a-145"><strong>Allocation percentage</strong></span></span></td>
<td><span data-ttu-id="59a0a-146"><strong>Prioridade da alocação</strong></span><span class="sxs-lookup"><span data-stu-id="59a0a-146"><strong>Allocation priority</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="59a0a-147">Pretende alocar custos a uma fonte de financiamento até os seus fundos serem esgotados, alocar custos a uma segunda fonte de financiamento até os seus fundos serem esgotados e, finalmente, alocar os custos restantes a uma terceira fonte de financiamento.</span><span class="sxs-lookup"><span data-stu-id="59a0a-147">You want to allocate costs to one funding source until its funds are exhausted, allocate costs to a second funding source until its funds are exhausted, and finally allocate the remaining costs to a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="59a0a-148">Fonte de financiamento 1</span><span class="sxs-lookup"><span data-stu-id="59a0a-148">Funding　source　1</span></span></li>
<li><span data-ttu-id="59a0a-149">Fonte de financiamento 2</span><span class="sxs-lookup"><span data-stu-id="59a0a-149">Funding　source　2</span></span></li>
<li><span data-ttu-id="59a0a-150">Fonte de financiamento 3</span><span class="sxs-lookup"><span data-stu-id="59a0a-150">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="59a0a-151">100%</span><span class="sxs-lookup"><span data-stu-id="59a0a-151">100%</span></span></li>
<li><span data-ttu-id="59a0a-152">100%</span><span class="sxs-lookup"><span data-stu-id="59a0a-152">100%</span></span></li>
<li><span data-ttu-id="59a0a-153">100%</span><span class="sxs-lookup"><span data-stu-id="59a0a-153">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="59a0a-154">5</span><span class="sxs-lookup"><span data-stu-id="59a0a-154">1</span></span></li>
<li><span data-ttu-id="59a0a-155">2</span><span class="sxs-lookup"><span data-stu-id="59a0a-155">2</span></span></li>
<li><span data-ttu-id="59a0a-156">3</span><span class="sxs-lookup"><span data-stu-id="59a0a-156">3</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="59a0a-157">Pretende alocar 75% dos custos a uma fonte de financiamento e 25% a uma segunda fonte de financiamento.</span><span class="sxs-lookup"><span data-stu-id="59a0a-157">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="59a0a-158">Quando qualquer uma dessas fontes de financiamento se esgotar, quer pagar os custos restantes de uma terceira fonte de financiamento.</span><span class="sxs-lookup"><span data-stu-id="59a0a-158">When either of those funding sources is exhausted, you want to pay the remaining costs from a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="59a0a-159">Fonte de financiamento 1</span><span class="sxs-lookup"><span data-stu-id="59a0a-159">Funding　source　1</span></span></li>
<li><span data-ttu-id="59a0a-160">Fonte de financiamento 2</span><span class="sxs-lookup"><span data-stu-id="59a0a-160">Funding　source　2</span></span></li>
<li><span data-ttu-id="59a0a-161">Fonte de financiamento 3</span><span class="sxs-lookup"><span data-stu-id="59a0a-161">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="59a0a-162">75%</span><span class="sxs-lookup"><span data-stu-id="59a0a-162">75%</span></span></li>
<li><span data-ttu-id="59a0a-163">25%</span><span class="sxs-lookup"><span data-stu-id="59a0a-163">25%</span></span></li>
<li><span data-ttu-id="59a0a-164">100%</span><span class="sxs-lookup"><span data-stu-id="59a0a-164">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="59a0a-165">5</span><span class="sxs-lookup"><span data-stu-id="59a0a-165">1</span></span></li>
<li><span data-ttu-id="59a0a-166">5</span><span class="sxs-lookup"><span data-stu-id="59a0a-166">1</span></span></li>
<li><span data-ttu-id="59a0a-167">2</span><span class="sxs-lookup"><span data-stu-id="59a0a-167">2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="59a0a-168">Pretende alocar 75% dos custos a uma fonte de financiamento e 25% a uma segunda fonte de financiamento.</span><span class="sxs-lookup"><span data-stu-id="59a0a-168">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="59a0a-169">Quando qualquer uma dessas fontes de financiamento se esgotar, quer dividir os custos restantes entre uma terceira fonte de financiamento e uma quarta fonte de financiamento.</span><span class="sxs-lookup"><span data-stu-id="59a0a-169">When either of those funding sources is exhausted, you want to split the remaining costs between a third funding source and a fourth funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="59a0a-170">Fonte de financiamento 1</span><span class="sxs-lookup"><span data-stu-id="59a0a-170">Funding　source　1</span></span></li>
<li><span data-ttu-id="59a0a-171">Fonte de financiamento 2</span><span class="sxs-lookup"><span data-stu-id="59a0a-171">Funding　source　2</span></span></li>
<li><span data-ttu-id="59a0a-172">Fonte de financiamento 3</span><span class="sxs-lookup"><span data-stu-id="59a0a-172">Funding　source　3</span></span></li>
<li><span data-ttu-id="59a0a-173">Fonte de financiamento 4</span><span class="sxs-lookup"><span data-stu-id="59a0a-173">Funding　source　4</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="59a0a-174">75%</span><span class="sxs-lookup"><span data-stu-id="59a0a-174">75%</span></span></li>
<li><span data-ttu-id="59a0a-175">25%</span><span class="sxs-lookup"><span data-stu-id="59a0a-175">25%</span></span></li>
<li><span data-ttu-id="59a0a-176">50%</span><span class="sxs-lookup"><span data-stu-id="59a0a-176">50%</span></span></li>
<li><span data-ttu-id="59a0a-177">50%</span><span class="sxs-lookup"><span data-stu-id="59a0a-177">50%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="59a0a-178">5</span><span class="sxs-lookup"><span data-stu-id="59a0a-178">1</span></span></li>
<li><span data-ttu-id="59a0a-179">5</span><span class="sxs-lookup"><span data-stu-id="59a0a-179">1</span></span></li>
<li><span data-ttu-id="59a0a-180">2</span><span class="sxs-lookup"><span data-stu-id="59a0a-180">2</span></span></li>
<li><span data-ttu-id="59a0a-181">2</span><span class="sxs-lookup"><span data-stu-id="59a0a-181">2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="59a0a-182">Pretende alocar os primeiros 25% dos custos a uma fonte de financiamento e o restante a uma segunda fonte de financiamento.</span><span class="sxs-lookup"><span data-stu-id="59a0a-182">You want to allocate the first 25 percent of costs to one funding source and the rest to a second funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="59a0a-183">Fonte de financiamento 1</span><span class="sxs-lookup"><span data-stu-id="59a0a-183">Funding　source　1</span></span></li>
<li><span data-ttu-id="59a0a-184">Fonte de financiamento 2</span><span class="sxs-lookup"><span data-stu-id="59a0a-184">Funding　source　2</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="59a0a-185">25%</span><span class="sxs-lookup"><span data-stu-id="59a0a-185">25%</span></span></li>
<li><span data-ttu-id="59a0a-186">100%</span><span class="sxs-lookup"><span data-stu-id="59a0a-186">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="59a0a-187">5</span><span class="sxs-lookup"><span data-stu-id="59a0a-187">1</span></span></li>
<li><span data-ttu-id="59a0a-188">2</span><span class="sxs-lookup"><span data-stu-id="59a0a-188">2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a><span data-ttu-id="59a0a-189">Exemplo: Múltiplas fontes de financiamento (complexo)</span><span class="sxs-lookup"><span data-stu-id="59a0a-189">Example: Multiple funding sources (complex)</span></span>

<span data-ttu-id="59a0a-190">Tem três fontes de financiamento que pretende utilizar pela seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="59a0a-190">You have three funding sources that you want to use in the following order:</span></span>

1.  <span data-ttu-id="59a0a-191">Utilize a fonte de financiamento 2 e a fonte de financiamento 3 equitativamente até a fonte de financiamento 2 estar esgotada.</span><span class="sxs-lookup"><span data-stu-id="59a0a-191">Use funding source 2 and funding source 3 equally until funding source 2 is exhausted.</span></span>
2.  <span data-ttu-id="59a0a-192">Continue a utilizar a fonte de financiamento 3 até estar esgotada.</span><span class="sxs-lookup"><span data-stu-id="59a0a-192">Continue to use funding source 3 until it is exhausted.</span></span>
3.  <span data-ttu-id="59a0a-193">Utilize a fonte de financiamento 1 depois de esgotada a fonte de financiamento 3.</span><span class="sxs-lookup"><span data-stu-id="59a0a-193">Use funding source 1 after funding source 3 is exhausted.</span></span>

<span data-ttu-id="59a0a-194">Para atingir este objetivo, tem de efetuar o seguinte:</span><span class="sxs-lookup"><span data-stu-id="59a0a-194">To accomplish this goal, you must do the following:</span></span>

-   <span data-ttu-id="59a0a-195">Configure limites de financiamento para a fonte de financiamento 2 e a fonte de financiamento 3, para os respetivos montantes.</span><span class="sxs-lookup"><span data-stu-id="59a0a-195">Set up funding limits for funding source 2 and funding source 3, for their respective amounts.</span></span>
-   <span data-ttu-id="59a0a-196">Crie as seguintes regras de financiamento:</span><span class="sxs-lookup"><span data-stu-id="59a0a-196">Create the following funding rules:</span></span>
    -   <span data-ttu-id="59a0a-197">Regra 1 (Prioridade 1): Alocar 50% das transações à fonte de financiamento 2 e 50% à fonte de financiamento 3.</span><span class="sxs-lookup"><span data-stu-id="59a0a-197">Rule 1 (Priority 1): Allocate 50 percent of transactions to funding source 2 and 50 percent to funding source 3.</span></span>
    -   <span data-ttu-id="59a0a-198">Regra 2 (Prioridade 2): Alocar 100% das transações à fonte de financiamento 3.</span><span class="sxs-lookup"><span data-stu-id="59a0a-198">Rule 2 (Priority 2): Allocate 100 percent of transactions to funding source 3.</span></span>
    -   <span data-ttu-id="59a0a-199">Regra 3 (Prioridade 3): Alocar 100% das transações à fonte de financiamento 1.</span><span class="sxs-lookup"><span data-stu-id="59a0a-199">Rule 3 (Priority 3): Allocate 100 percent of transactions to funding source 1.</span></span>

<span data-ttu-id="59a0a-200">Esta configuração funciona porque as transações são comparadas com as regras e os limites para determinar se alguma delas se aplica à transação.</span><span class="sxs-lookup"><span data-stu-id="59a0a-200">This setup works because transactions are checked against rules and limits to determine whether any of them apply to the transaction.</span></span> <span data-ttu-id="59a0a-201">Se não forem aplicáveis regras ou limites específicos à transação, aplica-se a regra Todas as transações.</span><span class="sxs-lookup"><span data-stu-id="59a0a-201">If no specific rules or limits apply to the transaction, the All transactions rule applies.</span></span> <span data-ttu-id="59a0a-202">A regra Todas as transações corresponde a todas as transações.</span><span class="sxs-lookup"><span data-stu-id="59a0a-202">The All transactions rule matches all transactions.</span></span> 

<span data-ttu-id="59a0a-203">Se for encontrada uma regra que corresponda a uma transação, a percentagem que foi alocada nessa regra é aplicada primeiro, mas só depois de verificadas as correspondências tendo em conta quaisquer limites que tenham sido configurados.</span><span class="sxs-lookup"><span data-stu-id="59a0a-203">If a rule is found that matches a transaction, the percentage that has been allocated in that rule is applied first, but only after the matches are checked against any limits that have been set up.</span></span> <span data-ttu-id="59a0a-204">Se tiver sido atingido um limite e os fundos de uma fonte de financiamento estiverem esgotados, a regra de financiamento que está associada ao limite de financiamento é ignorada, e o programa verifica a regra seguinte aplicável.</span><span class="sxs-lookup"><span data-stu-id="59a0a-204">If a limit has been met, and a funding source’s funds are exhausted, the funding rule that is associated with the funding limit is disregarded, and the program checks for the next rule that applies.</span></span> 

<span data-ttu-id="59a0a-205">Em alguns casos, só parte de uma transação pode ser alocada de acordo com uma regra.</span><span class="sxs-lookup"><span data-stu-id="59a0a-205">In some cases, only part of a transaction can be allocated under a rule.</span></span> <span data-ttu-id="59a0a-206">Isto pode acontecer porque é atingido um limite quando a transação é alocada.</span><span class="sxs-lookup"><span data-stu-id="59a0a-206">This might happen because a limit is reached when the transaction is allocated.</span></span> <span data-ttu-id="59a0a-207">Neste caso, só é alocado um determinado montante de acordo com essa regra, como 50% a cada fonte de financiamento.</span><span class="sxs-lookup"><span data-stu-id="59a0a-207">In this case, only a certain amount is allocated according to that rule, such as 50 percent to each funding source.</span></span> <span data-ttu-id="59a0a-208">É o caso da regra 1, descrita anteriormente nesta secção.</span><span class="sxs-lookup"><span data-stu-id="59a0a-208">This is the case in rule 1, which is described earlier in this section.</span></span> <span data-ttu-id="59a0a-209">O restante é alocado de acordo com a regra seguinte na sequência.</span><span class="sxs-lookup"><span data-stu-id="59a0a-209">The remainder is allocated according to the next rule in the sequence.</span></span> 

<span data-ttu-id="59a0a-210">A tabela seguinte examina este cenário em maior detalhe.</span><span class="sxs-lookup"><span data-stu-id="59a0a-210">The following table examines this scenario in more detail.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="59a0a-211"><strong>Foco</strong></span><span class="sxs-lookup"><span data-stu-id="59a0a-211"><strong>Focus</strong></span></span></td>
<td><span data-ttu-id="59a0a-212"><strong>Detalhes</strong></span><span class="sxs-lookup"><span data-stu-id="59a0a-212"><strong>Details</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="59a0a-213">Regras de financiamento</span><span class="sxs-lookup"><span data-stu-id="59a0a-213">Funding rules</span></span></td>
<td><ul>
<li><span data-ttu-id="59a0a-214">Regra 1 (Prioridade 1): Todas as transações.</span><span class="sxs-lookup"><span data-stu-id="59a0a-214">Rule 1 (Priority 1): All transactions.</span></span> <span data-ttu-id="59a0a-215">Alocar fonte de financiamento 2 a 50% e a fonte de financiamento 3 a 50%.</span><span class="sxs-lookup"><span data-stu-id="59a0a-215">Allocate funding source 2 at 50% and funding source 3 at 50%.</span></span></li>
<li><span data-ttu-id="59a0a-216">Regra 2 (Prioridade 2): Todas as transações.</span><span class="sxs-lookup"><span data-stu-id="59a0a-216">Rule 2 (Priority 2): All transactions.</span></span> <span data-ttu-id="59a0a-217">Alocar fonte de financiamento 3 a 100%.</span><span class="sxs-lookup"><span data-stu-id="59a0a-217">Allocate funding source 3 at 100%.</span></span></li>
<li><span data-ttu-id="59a0a-218">Regra 3 (Prioridade 2): Todas as transações.</span><span class="sxs-lookup"><span data-stu-id="59a0a-218">Rule 3 (Priority 2): All transactions.</span></span> <span data-ttu-id="59a0a-219">Alocar fonte de financiamento 1 a 100%.</span><span class="sxs-lookup"><span data-stu-id="59a0a-219">Allocate funding source 1 at 100%.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="59a0a-220">Limites de financiamento</span><span class="sxs-lookup"><span data-stu-id="59a0a-220">Funding limits</span></span></td>
<td><ul>
<li><span data-ttu-id="59a0a-221">Limite da fonte de financiamento 1 = 10.000,00</span><span class="sxs-lookup"><span data-stu-id="59a0a-221">Funding source 1 limit = 10,000.00</span></span></li>
<li><span data-ttu-id="59a0a-222">Limite da fonte de financiamento 2 = 500,00</span><span class="sxs-lookup"><span data-stu-id="59a0a-222">Funding source 2 limit = 500.00</span></span></li>
<li><span data-ttu-id="59a0a-223">Limite da fonte de financiamento 3 = 750,00</span><span class="sxs-lookup"><span data-stu-id="59a0a-223">Funding source 3 limit = 750.00</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="59a0a-224">Transação 1</span><span class="sxs-lookup"><span data-stu-id="59a0a-224">Transaction 1</span></span></td>
<td><span data-ttu-id="59a0a-225"><strong>Montante da transação:</strong> 100,00<strong>Financiamento:</strong> A transação é paga apenas de acordo com a regra 1, porque a transação é paga totalmente após a aplicação da regra 1.</span><span class="sxs-lookup"><span data-stu-id="59a0a-225"><strong>Transaction amount:</strong> 100.00<strong>Funding:</strong> The transaction is paid according to rule 1 only, because the transaction is fully paid after rule 1 is applied.</span></span> <span data-ttu-id="59a0a-226">A transação é financiada igualmente entre a fonte de financiamento 2 e a fonte de financiamento 3.</span><span class="sxs-lookup"><span data-stu-id="59a0a-226">The transaction is funded equally between funding source 2 and funding source 3.</span></span>
<ul>
<li><span data-ttu-id="59a0a-227">Fonte de financiamento 2: 50,00</span><span class="sxs-lookup"><span data-stu-id="59a0a-227">Funding source 2: 50.00</span></span></li>
<li><span data-ttu-id="59a0a-228">Fonte de financiamento 3: 50,00</span><span class="sxs-lookup"><span data-stu-id="59a0a-228">Funding source 3: 50.00</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="59a0a-229">Transação 2</span><span class="sxs-lookup"><span data-stu-id="59a0a-229">Transaction 2</span></span></td>
<td><span data-ttu-id="59a0a-230"><strong>Montante da transação:</strong> 5.000,00<strong>Financiamento:</strong> A transação é paga de acordo com as três regras.</span><span class="sxs-lookup"><span data-stu-id="59a0a-230"><strong>Transaction amount:</strong> 5,000.00<strong>Funding:</strong> The transaction is paid according to all three rules.</span></span> <span data-ttu-id="59a0a-231"><strong>Regra 1</strong>
</span><span class="sxs-lookup"><span data-stu-id="59a0a-231"><strong>Rule 1</strong>
</span></span><ul>
<li><span data-ttu-id="59a0a-232">Fonte de financiamento 2: 450,00</span><span class="sxs-lookup"><span data-stu-id="59a0a-232">Funding source 2: 450.00</span></span></li>
<li><span data-ttu-id="59a0a-233">Fonte de financiamento 3: 450,00</span><span class="sxs-lookup"><span data-stu-id="59a0a-233">Funding source 3: 450.00</span></span></li>
</ul><span data-ttu-id="59a0a-234">
<strong>Regra 2</strong>
</span><span class="sxs-lookup"><span data-stu-id="59a0a-234">
<strong>Rule 2</strong>
</span></span><ul>
<li><span data-ttu-id="59a0a-235">Fonte de financiamento 3: 250,00 (= 750,00 – 50,00 – 450,00)</span><span class="sxs-lookup"><span data-stu-id="59a0a-235">Funding source 3: 250.00 (= 750.00 – 50.00 – 450.00)</span></span></li>
</ul><span data-ttu-id="59a0a-236">
<strong>Regra 3</strong>
</span><span class="sxs-lookup"><span data-stu-id="59a0a-236">
<strong>Rule 3</strong>
</span></span><ul>
<li><span data-ttu-id="59a0a-237">Fonte de financiamento 1: 3.850,00 (= 5.000,00 – 450,00 – 450,00 – 250,00)</span><span class="sxs-lookup"><span data-stu-id="59a0a-237">Funding source 1: 3,850.00 (= 5,000.00 – 450.00 – 450.00 – 250.00)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="59a0a-238">Total de fundos distribuídos por cada fonte de financiamento</span><span class="sxs-lookup"><span data-stu-id="59a0a-238">Total funds that are distributed for each funding source</span></span></td>
<td><ul>
<li><span data-ttu-id="59a0a-239">Fonte de financiamento 1: 3.850,00</span><span class="sxs-lookup"><span data-stu-id="59a0a-239">Funding source 1: 3,850.00</span></span></li>
<li><span data-ttu-id="59a0a-240">Fonte de financiamento 2: 500,00</span><span class="sxs-lookup"><span data-stu-id="59a0a-240">Funding source 2: 500.00</span></span></li>
<li><span data-ttu-id="59a0a-241">Fonte de financiamento 3: 750,00</span><span class="sxs-lookup"><span data-stu-id="59a0a-241">Funding source 3: 750.00</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a><span data-ttu-id="59a0a-242">Regras de faturação</span><span class="sxs-lookup"><span data-stu-id="59a0a-242">Billing rules</span></span>
<span data-ttu-id="59a0a-243">Quando negoceia um contrato de projeto com um cliente, define como e quando pode faturar o cliente pelo trabalho num projeto.</span><span class="sxs-lookup"><span data-stu-id="59a0a-243">When you negotiate a project contract with a customer, you define how and when you can invoice the customer for work on a project.</span></span> <span data-ttu-id="59a0a-244">Depois de configurar o contrato de projeto e o projeto, pode configurar regras de faturação para o projeto.</span><span class="sxs-lookup"><span data-stu-id="59a0a-244">After you set up the project contract and the project, you can set up billing rules for the project.</span></span> <span data-ttu-id="59a0a-245">As regras de faturação baseiam-se nos termos do projeto especificados no contrato do projeto.</span><span class="sxs-lookup"><span data-stu-id="59a0a-245">Billing rules are based on the project terms that are specified in the project contract.</span></span> <span data-ttu-id="59a0a-246">As regras de faturação que pode criar dependem dos termos do contrato de projeto e do tipo de projeto, como o Tempo e material ou Preço fixo, que associa à regra de faturação.</span><span class="sxs-lookup"><span data-stu-id="59a0a-246">The billing rules that you can create depend on the terms of the project contract and the project type, such as Time and material or Fixed-price, that you associate with the billing rule.</span></span> <span data-ttu-id="59a0a-247">Pode criar mais de uma regra de faturação para um contrato de projeto.</span><span class="sxs-lookup"><span data-stu-id="59a0a-247">You can create more than one billing rule for a project contract.</span></span> <span data-ttu-id="59a0a-248">Também pode atribuir uma regra de faturação a vários projetos que estão associados ao mesmo contrato de projeto e têm termos de faturação semelhantes.</span><span class="sxs-lookup"><span data-stu-id="59a0a-248">You can also assign a billing rule to multiple projects that are associated with the same project contract and have similar billing terms.</span></span> 

<span data-ttu-id="59a0a-249">Pode configurar os seguintes tipos de regras de faturação:</span><span class="sxs-lookup"><span data-stu-id="59a0a-249">You can set up the following types of billing rules:</span></span>

-   <span data-ttu-id="59a0a-250">**Unidade de entrega** – Faturar um cliente quando conclui uma unidade de entrega.</span><span class="sxs-lookup"><span data-stu-id="59a0a-250">**Unit of delivery** – Invoice a customer when you complete a unit of delivery.</span></span> <span data-ttu-id="59a0a-251">Defina as unidades de entrega no contrato.</span><span class="sxs-lookup"><span data-stu-id="59a0a-251">You define the units of delivery in the contract.</span></span>
-   <span data-ttu-id="59a0a-252">**Progresso** – Faturar um cliente quando conclui uma percentagem especificada do projeto.</span><span class="sxs-lookup"><span data-stu-id="59a0a-252">**Progress** – Invoice a customer when you complete a specified percentage of the project.</span></span> <span data-ttu-id="59a0a-253">Pode configurar uma regra de faturação para calcular automaticamente a percentagem de trabalho concluído, ou pode calcular manualmente a percentagem de trabalho concluído e o montante a faturar o cliente.</span><span class="sxs-lookup"><span data-stu-id="59a0a-253">You can set up a billing rule to automatically calculate the percentage of work completed, or you can manually calculate the percentage of work completed and the amount to invoice the customer.</span></span>
-   <span data-ttu-id="59a0a-254">**Marco** – Faturar um cliente pelo montante total de um marco de projeto quando o marco é atingido.</span><span class="sxs-lookup"><span data-stu-id="59a0a-254">**Milestone** – Invoice a customer for the full amount of a project milestone when the milestone is reached.</span></span>
-   <span data-ttu-id="59a0a-255">**Tarifa** – Faturar um cliente pelos seus serviços, acrescido de uma tarifa de gestão, que normalmente é uma percentagem do custo dos serviços.</span><span class="sxs-lookup"><span data-stu-id="59a0a-255">**Fee** – Invoice a customer for your services plus a management fee, which is typically a percentage of the cost of services.</span></span>
-   <span data-ttu-id="59a0a-256">**Tempo e material** – Faturar um cliente pelo valor do tempo e dos materiais que são utilizados num projeto.</span><span class="sxs-lookup"><span data-stu-id="59a0a-256">**Time and material** – Invoice a customer for the value of time and materials that are used on a project.</span></span>

<span data-ttu-id="59a0a-257">Para todos os tipos de regras de faturação, pode especificar uma percentagem de retenção que é deduzida das faturas do cliente até um projeto atingir uma fase acordada.</span><span class="sxs-lookup"><span data-stu-id="59a0a-257">For all types of billing rules, you can specify a retention percentage that is deducted from customer invoices until a project reaches an agreed-upon stage.</span></span> <span data-ttu-id="59a0a-258">A percentagem de retenção de pagamentos é especificada no contrato de projeto.</span><span class="sxs-lookup"><span data-stu-id="59a0a-258">The payment retention percentage is specified in the project contract.</span></span> <span data-ttu-id="59a0a-259">O montante é calculado e é subtraído do valor total das linhas numa fatura do cliente.</span><span class="sxs-lookup"><span data-stu-id="59a0a-259">The amount is calculated based on, and subtracted from, the total value of the lines in a customer invoice.</span></span> 

<span data-ttu-id="59a0a-260">Para as regras de faturação **Tempo e material** e **Progresso** , pode atribuir categorias faturáveis.</span><span class="sxs-lookup"><span data-stu-id="59a0a-260">For **Time and material** and **Progress** billing rules, you can assign chargeable categories.</span></span> <span data-ttu-id="59a0a-261">As categorias faturáveis indicam as transações que devem ser incluídas nas faturas dos clientes.</span><span class="sxs-lookup"><span data-stu-id="59a0a-261">Chargeable categories indicate the transactions that should be included in customer invoices.</span></span> 

<span data-ttu-id="59a0a-262">Quando estiver pronto para faturar o cliente, o montante da faturação do projeto é calculado com base nas regras de faturação e é gerada uma proposta de fatura do projeto.</span><span class="sxs-lookup"><span data-stu-id="59a0a-262">When you are ready to invoice the customer, the amount to invoice for the project is calculated based on the billing rules, and a project invoice proposal is generated.</span></span> 

<span data-ttu-id="59a0a-263">As secções seguintes fornecem exemplos que mostram como configurar e gerir as regras de faturação para um projeto.</span><span class="sxs-lookup"><span data-stu-id="59a0a-263">The following sections provide examples that show how to set up and manage billing rules for a project.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a><span data-ttu-id="59a0a-264">Exemplo: Criar uma regra de faturação baseada no número de unidades entregues</span><span class="sxs-lookup"><span data-stu-id="59a0a-264">Example: Create a billing rule that is based on the number of units delivered</span></span>

<span data-ttu-id="59a0a-265">A sua organização celebra um contrato para fornecer um total de cinco sessões de formação aos colaboradores de um cliente por um custo de 10.000 por sessão de formação.</span><span class="sxs-lookup"><span data-stu-id="59a0a-265">Your organization enters into an agreement to provide a total of five training sessions to a customer’s employees at a cost of 10,000 per training session.</span></span> <span data-ttu-id="59a0a-266">Fature o cliente após cada sessão de formação.</span><span class="sxs-lookup"><span data-stu-id="59a0a-266">You invoice the customer after each training session.</span></span> 

<span data-ttu-id="59a0a-267">Quando configurar as regras de faturação do contrato, utilize os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="59a0a-267">When you set up the billing rules for the contract, you use the following values:</span></span>

-   <span data-ttu-id="59a0a-268">A unidade de entrega é uma sessão de formação.</span><span class="sxs-lookup"><span data-stu-id="59a0a-268">The unit of delivery is one training session.</span></span>
-   <span data-ttu-id="59a0a-269">O preço unitário é de 10.000 por sessão de formação.</span><span class="sxs-lookup"><span data-stu-id="59a0a-269">The unit price is 10,000 per training session.</span></span>
-   <span data-ttu-id="59a0a-270">O número total de unidades é de cinco sessões de formação.</span><span class="sxs-lookup"><span data-stu-id="59a0a-270">The total number of units is five training sessions.</span></span>

<span data-ttu-id="59a0a-271">Depois de concluir uma sessão de formação, pode criar uma fatura de 10.000, para a primeira unidade que foi entregue, e enviar a fatura ao cliente.</span><span class="sxs-lookup"><span data-stu-id="59a0a-271">When you have completed one training session, you can create an invoice for 10,000, for the first unit that was delivered, and send the invoice to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a><span data-ttu-id="59a0a-272">Exemplo: Criar uma regra de faturação baseada numa percentagem especificada de conclusão do projeto (cálculo manual)</span><span class="sxs-lookup"><span data-stu-id="59a0a-272">Example: Create a billing rule that is based on a specified percentage of project completion (manual calculation)</span></span>

<span data-ttu-id="59a0a-273">A sua organização, uma empresa de consultoria de software, celebra um acordo com um cliente para desenvolver parte de um produto que o cliente está a desenvolver.</span><span class="sxs-lookup"><span data-stu-id="59a0a-273">Your organization, a software consulting firm, enters into an agreement with a customer to develop part of a product that the customer is developing.</span></span> <span data-ttu-id="59a0a-274">A sua organização concorda entregar o código de software durante um período de seis meses.</span><span class="sxs-lookup"><span data-stu-id="59a0a-274">Your organization agrees to deliver the software code over a period of six months.</span></span> <span data-ttu-id="59a0a-275">O cliente concorda pagar à sua organização um total de 100.000 pelo trabalho.</span><span class="sxs-lookup"><span data-stu-id="59a0a-275">The customer agrees to pay your organization a total of 100,000 for the work.</span></span> <span data-ttu-id="59a0a-276">Crie uma regra de faturação para faturar o cliente baseado na percentagem de trabalho que é concluída no projeto, conforme especificado no contrato.</span><span class="sxs-lookup"><span data-stu-id="59a0a-276">You create a billing rule to invoice the customer based on the percentage of work that is completed on the project, as specified in the contract.</span></span>

-   <span data-ttu-id="59a0a-277">No final do primeiro mês, encontra-se com o cliente para determinar a percentagem de trabalho concluído.</span><span class="sxs-lookup"><span data-stu-id="59a0a-277">At the end of the first month, you meet with the customer to determine the percentage of work completed.</span></span> <span data-ttu-id="59a0a-278">Depois , com o o cliente rever o projeto, decide que o projeto está 15% concluído.</span><span class="sxs-lookup"><span data-stu-id="59a0a-278">After you and the customer review the project, you decide that the project is 15 percent completed.</span></span>
-   <span data-ttu-id="59a0a-279">Crie uma fatura para 15.000 (15% de 100.000) e envie-a ao cliente.</span><span class="sxs-lookup"><span data-stu-id="59a0a-279">You create an invoice for 15,000 (15 percent of 100,000) and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a><span data-ttu-id="59a0a-280">Exemplo: Criar uma regra de faturação baseada numa percentagem especificada de conclusão do projeto (cálculo automático)</span><span class="sxs-lookup"><span data-stu-id="59a0a-280">Example: Create a billing rule that is based on a specified percentage of project completion (automatic calculation)</span></span>

<span data-ttu-id="59a0a-281">A sua organização, uma empresa de desenvolvimento de software, concorda desenvolver um pacote de cálculo das folhas de pagamento para um cliente por 30.000.</span><span class="sxs-lookup"><span data-stu-id="59a0a-281">Your organization, a software development firm, agrees to develop a payroll accounting package for a customer for 30,000.</span></span> <span data-ttu-id="59a0a-282">O cliente concorda pagar à sua organização com base na percentagem de trabalho concluída.</span><span class="sxs-lookup"><span data-stu-id="59a0a-282">The customer agrees to pay your organization based on the percentage of work completed.</span></span> <span data-ttu-id="59a0a-283">Estima que os custos do projeto são de 20.000.</span><span class="sxs-lookup"><span data-stu-id="59a0a-283">You estimate that the project costs are 20,000.</span></span> <span data-ttu-id="59a0a-284">O contrato de projeto especifica as categorias de trabalho que utiliza no processo de faturação.</span><span class="sxs-lookup"><span data-stu-id="59a0a-284">The project contract specifies the categories of work that you use in the billing process.</span></span> <span data-ttu-id="59a0a-285">Configura regras de faturação que calculam automaticamente os montantes da fatura para a percentagem de trabalho que está concluída para cada categoria.</span><span class="sxs-lookup"><span data-stu-id="59a0a-285">You set up billing rules that automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="59a0a-286">Crie um orçamento para cada categoria:</span><span class="sxs-lookup"><span data-stu-id="59a0a-286">You set up a budget for each category:</span></span>

-   <span data-ttu-id="59a0a-287">**Desenvolvimento** – Custo de 15.000 e receitas de 20.000</span><span class="sxs-lookup"><span data-stu-id="59a0a-287">**Development** – Cost of 15,000 and revenue of 20,000</span></span>
-   <span data-ttu-id="59a0a-288">**Instalação** – Custo de 5.000 e receitas de 10.000</span><span class="sxs-lookup"><span data-stu-id="59a0a-288">**Installation** – Cost of 5,000 and revenue of 10,000</span></span>

<span data-ttu-id="59a0a-289">Quando cria uma fatura do cliente pela primeira vez, o montante da fatura é calculado automaticamente com base nas seguintes informações:</span><span class="sxs-lookup"><span data-stu-id="59a0a-289">When you create a customer invoice for the first time, the invoice amount is automatically calculated based on the following information:</span></span>

-   <span data-ttu-id="59a0a-290">Após um mês, o trabalhador do projeto submete uma folha de horas para o projeto.</span><span class="sxs-lookup"><span data-stu-id="59a0a-290">After a month, the worker on the project submits a timesheet for the project.</span></span> <span data-ttu-id="59a0a-291">O custo das horas do trabalhador é de 5.000 para o desenvolvimento e 1.000 para a instalação.</span><span class="sxs-lookup"><span data-stu-id="59a0a-291">The cost of the worker’s hours is 5,000 for development and 1,000 for installation.</span></span> <span data-ttu-id="59a0a-292">O trabalho de desenvolvimento está 33% concluído (5.000 custos reais/15.000 custos orçamentais) e o trabalho de instalação está 20% concluído (1.000 custos reais/5.000 custos orçamentais).</span><span class="sxs-lookup"><span data-stu-id="59a0a-292">The development work is 33 percent completed (5,000 actual cost/15,000 budget cost), and the installation work is 20 percent completed (1,000 actual cost/5,000 budget cost).</span></span>
-   <span data-ttu-id="59a0a-293">O montante da fatura de 8.667 é calculado automaticamente (33% de 20.000 + 20% de 10.000).</span><span class="sxs-lookup"><span data-stu-id="59a0a-293">The invoice amount of 8,667 is automatically calculated (33 percent of 20,000 + 20 percent of 10,000).</span></span>
-   <span data-ttu-id="59a0a-294">Crie uma fatura para 8.667 e envie-a ao cliente.</span><span class="sxs-lookup"><span data-stu-id="59a0a-294">You create an invoice for 8,667 and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a><span data-ttu-id="59a0a-295">Exemplo: Criar uma regra de faturação baseada em marcos acordados</span><span class="sxs-lookup"><span data-stu-id="59a0a-295">Example: Create a billing rule that is based on agreed-upon milestones</span></span>

<span data-ttu-id="59a0a-296">A sua organização, uma empresa de consultoria de gestão, concorda em realizar pesquisas de mercado para um produto de consumo que o cliente planeia vender.</span><span class="sxs-lookup"><span data-stu-id="59a0a-296">Your organization, a management consulting firm, agrees to conduct market research for a consumer product that the customer plans to sell.</span></span> <span data-ttu-id="59a0a-297">O cliente concorda utilizar os seus serviços por um período de três meses, a partir de março, e concorda em pagar à sua organização 50.000.</span><span class="sxs-lookup"><span data-stu-id="59a0a-297">The customer agrees to use your services for a period of three months, starting in March, and agrees to pay your organization 50,000.</span></span> <span data-ttu-id="59a0a-298">O projeto tem três marcos:</span><span class="sxs-lookup"><span data-stu-id="59a0a-298">The project has three milestones:</span></span>

-   <span data-ttu-id="59a0a-299">Marco 1: Recolher dados de consumidores – 31 de março</span><span class="sxs-lookup"><span data-stu-id="59a0a-299">Milestone 1: Collect consumer data – March 31</span></span>
-   <span data-ttu-id="59a0a-300">Marco 2: Analisar os dados dos consumidores – 30 de abril</span><span class="sxs-lookup"><span data-stu-id="59a0a-300">Milestone 2: Analyze consumer data – April 30</span></span>
-   <span data-ttu-id="59a0a-301">Marco 3: Apresentar uma proposta de viabilidade do produto – 31 de maio</span><span class="sxs-lookup"><span data-stu-id="59a0a-301">Milestone 3: Present a product viability proposal – May 31</span></span>

<span data-ttu-id="59a0a-302">O cliente concorda pagar à sua organização 10.000 pelo primeiro marco, 20.000 pelo segundo marco e 20.000 pelo terceiro marco.</span><span class="sxs-lookup"><span data-stu-id="59a0a-302">The customer agrees to pay your organization 10,000 for the first milestone, 20,000 for the second milestone, and 20,000 for the third milestone.</span></span> 

<span data-ttu-id="59a0a-303">Ao configurar o contrato de projeto, concorda faturar o cliente com base no marco que foi concluído.</span><span class="sxs-lookup"><span data-stu-id="59a0a-303">When you set up the project contract, you agree to bill the customer based on the milestone that has been completed.</span></span> <span data-ttu-id="59a0a-304">A configuração da regra de faturação inclui os seguintes passos:</span><span class="sxs-lookup"><span data-stu-id="59a0a-304">The billing rule setup includes the following steps:</span></span>

-   <span data-ttu-id="59a0a-305">Definir os marcos do projeto.</span><span class="sxs-lookup"><span data-stu-id="59a0a-305">Define the project milestones.</span></span>
-   <span data-ttu-id="59a0a-306">Definir o montante a faturar o cliente quando cada marco estiver concluído.</span><span class="sxs-lookup"><span data-stu-id="59a0a-306">Define the amount to invoice the customer when each milestone is completed.</span></span>

<span data-ttu-id="59a0a-307">Quando o primeiro marco estiver concluído a 31 de março, marque o marco como concluído e, em seguida, crie uma fatura de 10.000 e envie-a para o cliente.</span><span class="sxs-lookup"><span data-stu-id="59a0a-307">When the first milestone is completed on March 31, you mark the milestone as completed, and then create an invoice for 10,000 and send it to the customer.</span></span> <span data-ttu-id="59a0a-308">Não pode criar uma fatura para um marco enquanto não tiver marcado o marco como concluído.</span><span class="sxs-lookup"><span data-stu-id="59a0a-308">You can’t create an invoice for a milestone until you have marked the milestone as completed.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a><span data-ttu-id="59a0a-309">Exemplo: Criar uma regra de faturação baseada nos serviços, acrescida de uma taxa de gestão</span><span class="sxs-lookup"><span data-stu-id="59a0a-309">Example: Create a billing rule that is based on services plus a management fee</span></span>

<span data-ttu-id="59a0a-310">A sua organização, uma empresa de consultoria de gestão, concorda fazer um estudo de mercado para avaliar a viabilidade de um produto que o cliente, uma empresa de retalho, está a desenvolver.</span><span class="sxs-lookup"><span data-stu-id="59a0a-310">Your organization, a management consulting firm, agrees to conduct market research to evaluate the viability of a product that the customer, a retail company, is developing.</span></span> <span data-ttu-id="59a0a-311">Os termos do acordo especificam que irá fornecer os serviços dos seus três principais consultores de gestão, que conduzirão o estudo em função do tempo e dos materiais.</span><span class="sxs-lookup"><span data-stu-id="59a0a-311">The terms of the agreement specify that you will provide the services of your top three management consultants, who will conduct the research on a time-and-materials basis.</span></span> <span data-ttu-id="59a0a-312">O cliente concorda pagar 100 por hora, acrescido de uma taxa de gestão de 10% para as horas de consultoria que são cobradas ao projeto.</span><span class="sxs-lookup"><span data-stu-id="59a0a-312">The customer agrees to pay 100 per hour, plus a 10 percent management fee for the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="59a0a-313">Quando configura o contrato de projeto, crie uma regra de faturação para adicionar uma taxa de gestão de 10% às horas de consultoria que são cobradas ao projeto.</span><span class="sxs-lookup"><span data-stu-id="59a0a-313">When you set up the project contract, create a billing rule to add a 10 percent management fee to the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="59a0a-314">Quando cria uma fatura para o cliente, o cliente é faturado uma taxa de gestão de 10%, acrescida do custo das horas de consultoria.</span><span class="sxs-lookup"><span data-stu-id="59a0a-314">When you create an invoice for the customer, the customer is billed a 10 percent management fee plus the cost of the consulting hours.</span></span> <span data-ttu-id="59a0a-315">Por exemplo, se os três consultores trabalharam um total de 200 horas no projeto, é criada uma fatura de 22.000 com base no seguinte cálculo:</span><span class="sxs-lookup"><span data-stu-id="59a0a-315">For example, if the three consultants worked a total of 200 hours on the project, an invoice for 22,000 is created based on the following calculation:</span></span>

-   <span data-ttu-id="59a0a-316">200 horas a 100 por hora = 20.000</span><span class="sxs-lookup"><span data-stu-id="59a0a-316">200 hours at 100 per hour = 20,000</span></span>
-   <span data-ttu-id="59a0a-317">10% de taxa de gestão = 2.000</span><span class="sxs-lookup"><span data-stu-id="59a0a-317">10 percent management fee = 2,000</span></span>
-   <span data-ttu-id="59a0a-318">Montante total da fatura = 22.000</span><span class="sxs-lookup"><span data-stu-id="59a0a-318">Total invoice amount = 22,000</span></span>

<span data-ttu-id="59a0a-319">Se as tarifas forem tributáveis para um cliente, e selecionar um grupo de impostos sobre vendas no contrato do projeto, o grupo de impostos sobre vendas é automaticamente inscrito numa regra de faturação de tarifas.</span><span class="sxs-lookup"><span data-stu-id="59a0a-319">If fees are taxable to a customer, and you select a sales tax group in the project contract, the sales tax group is automatically entered in a billing rule for fees.</span></span>

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a><span data-ttu-id="59a0a-320">Exemplo: Criar uma regra de faturação para o valor de tempo e materiais</span><span class="sxs-lookup"><span data-stu-id="59a0a-320">Example: Create a billing rule for the value of time and materials</span></span>

<span data-ttu-id="59a0a-321">A sua organização, uma empresa de consultoria de software, concorda fornecer cinco consultores técnicos para trabalharem num projeto de desenvolvimento de software para um cliente durante os próximos seis meses.</span><span class="sxs-lookup"><span data-stu-id="59a0a-321">Your organization, a software consulting firm, agrees to provide five technical consultants to work on a software development project for a customer for the next six months.</span></span> <span data-ttu-id="59a0a-322">O cliente concorda pagar 150 por cada hora de consultoria, acrescido do custo dos materiais de escritório.</span><span class="sxs-lookup"><span data-stu-id="59a0a-322">The customer agrees to pay 150 for each consulting hour, plus the cost of office supplies.</span></span> <span data-ttu-id="59a0a-323">A sua organização envia uma fatura ao cliente no final de cada mês.</span><span class="sxs-lookup"><span data-stu-id="59a0a-323">Your organization sends an invoice to the customer at the end of each month.</span></span> 

<span data-ttu-id="59a0a-324">Ao configurar o contrato de projeto, concorda faturar o cliente todos os meses pelo tempo e material no projeto.</span><span class="sxs-lookup"><span data-stu-id="59a0a-324">When you set up the project contract, you agree to bill the customer each month for time and materials on the project.</span></span> <span data-ttu-id="59a0a-325">Crie uma regra de faturação que inclua as seguintes informações:</span><span class="sxs-lookup"><span data-stu-id="59a0a-325">You create a billing rule that includes the following information:</span></span>

-   <span data-ttu-id="59a0a-326">O período de contrato é de seis meses.</span><span class="sxs-lookup"><span data-stu-id="59a0a-326">The contract period is six months.</span></span>
-   <span data-ttu-id="59a0a-327">O tempo de consultoria é calculado a uma tarifa de 150 por hora.</span><span class="sxs-lookup"><span data-stu-id="59a0a-327">Consulting time is calculated at a rate of 150 per hour.</span></span>
-   <span data-ttu-id="59a0a-328">Os materiais de escritório são faturados ao custo, e o custo total do projeto não pode exceder 10.000.</span><span class="sxs-lookup"><span data-stu-id="59a0a-328">Office supplies are invoiced at cost, and the total cost for the project must not exceed 10,000.</span></span>
-   <span data-ttu-id="59a0a-329">Crie uma fatura do cliente no final de cada mês de calendário durante o projeto.</span><span class="sxs-lookup"><span data-stu-id="59a0a-329">You create a customer invoice at the end of each calendar month during the project.</span></span>

<span data-ttu-id="59a0a-330">Durante o primeiro mês, é registo um total de 800 horas pelos consultores do projeto.</span><span class="sxs-lookup"><span data-stu-id="59a0a-330">During the first month, a total of 800 hours are recorded by the consultants on the project.</span></span> <span data-ttu-id="59a0a-331">O custo dos materiais de escritório que são cobrados ao projeto é de 2.000.</span><span class="sxs-lookup"><span data-stu-id="59a0a-331">The cost of office supplies that are charged to the project is 2,000.</span></span> <span data-ttu-id="59a0a-332">Assim, no final do mês, cria uma fatura pelos 122.000, que é calculada como 800 horas a 150 por hora, mais 2.000 para material de escritório.</span><span class="sxs-lookup"><span data-stu-id="59a0a-332">Therefore, at the end of the month, you create an invoice for 122,000, which is calculated as 800 hours at 150 per hour, plus 2,000 for office supplies.</span></span>



