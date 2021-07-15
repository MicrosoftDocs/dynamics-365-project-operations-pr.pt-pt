---
title: Descrição geral de linhas de proposta baseadas em projetos
description: Este tópico fornece informações sobre como utilizar linhas de proposta baseadas no projeto para o trabalho de projeto.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: b7076a4b9280472f8c30d0b58c3aa9b9bc86d651
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369885"
---
# <a name="project-based-quote-lines-overview"></a><span data-ttu-id="c5bd1-103">Descrição geral das linhas de proposta baseadas em projetos</span><span class="sxs-lookup"><span data-stu-id="c5bd1-103">Project-based quote lines overview</span></span> 

<span data-ttu-id="c5bd1-104">_**Aplica-se a:** Implementação leve - negociar à faturação pró-forma, Project Operations para cenários baseados em recursos/não armazenados_</span><span class="sxs-lookup"><span data-stu-id="c5bd1-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="c5bd1-105">As linhas de proposta baseadas em projetos foram concebidas para ajudar a estimar o trabalho do projeto numa cativação.</span><span class="sxs-lookup"><span data-stu-id="c5bd1-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="c5bd1-106">A estrutura de uma linha de proposta baseada em projetos é expandida para as estimativas de projeto com os seguintes conceitos:</span><span class="sxs-lookup"><span data-stu-id="c5bd1-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="c5bd1-107">Método de Faturação</span><span class="sxs-lookup"><span data-stu-id="c5bd1-107">Billing Method</span></span>
- <span data-ttu-id="c5bd1-108">Mapeamento de Projetos e Tarefas</span><span class="sxs-lookup"><span data-stu-id="c5bd1-108">Project and Task Mapping</span></span>
- <span data-ttu-id="c5bd1-109">Classes de transações incluídas</span><span class="sxs-lookup"><span data-stu-id="c5bd1-109">Included Transaction classes</span></span>
- <span data-ttu-id="c5bd1-110">Limite a Não Exceder</span><span class="sxs-lookup"><span data-stu-id="c5bd1-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="c5bd1-111">Configuração da exigibilidade</span><span class="sxs-lookup"><span data-stu-id="c5bd1-111">Chargeability setup</span></span>
- <span data-ttu-id="c5bd1-112">Estimativa baseada nos Detalhes de Linha de Proposta</span><span class="sxs-lookup"><span data-stu-id="c5bd1-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="c5bd1-113">Clientes da Linha de Proposta</span><span class="sxs-lookup"><span data-stu-id="c5bd1-113">Quote line Customers</span></span>

<span data-ttu-id="c5bd1-114">A tabela seguinte fornece informações sobre os campos no separador **Geral** da linha de proposta baseada em projetos.</span><span class="sxs-lookup"><span data-stu-id="c5bd1-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="c5bd1-115">Estes campos ajudam a configurar a base para uma estimativa de raiz detalhada para o trabalho de projeto.</span><span class="sxs-lookup"><span data-stu-id="c5bd1-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="c5bd1-116">**Campo**</span><span class="sxs-lookup"><span data-stu-id="c5bd1-116">**Field**</span></span> | <span data-ttu-id="c5bd1-117">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c5bd1-117">**Description**</span></span> | <span data-ttu-id="c5bd1-118">**Impacto a jusante**</span><span class="sxs-lookup"><span data-stu-id="c5bd1-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="c5bd1-119">Nome</span><span class="sxs-lookup"><span data-stu-id="c5bd1-119">Name</span></span> | <span data-ttu-id="c5bd1-120">O nome da linha de proposta que o ajuda a identificar o componente discreto da proposta que está a ser estimada.</span><span class="sxs-lookup"><span data-stu-id="c5bd1-120">The name of quote line that helps you to identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="c5bd1-121">Copiada para o item de contrato do projeto que é criada a partir desta linha de proposta quando a proposta é ganha.</span><span class="sxs-lookup"><span data-stu-id="c5bd1-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c5bd1-122">Método de Faturação</span><span class="sxs-lookup"><span data-stu-id="c5bd1-122">Billing Method</span></span> | <span data-ttu-id="c5bd1-123">Numa proposta criada a partir de uma oportunidade, este valor é copiado a partir do campo correspondente na linha de oportunidade.</span><span class="sxs-lookup"><span data-stu-id="c5bd1-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="c5bd1-124">Este campo inclui os dois principais modelos de contratação suportados por Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="c5bd1-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="c5bd1-125">- Preço fixo</span><span class="sxs-lookup"><span data-stu-id="c5bd1-125">- Fixed price</span></span></br><span data-ttu-id="c5bd1-126">- Tempo e material.</span><span class="sxs-lookup"><span data-stu-id="c5bd1-126">- Time and material.</span></span>| <span data-ttu-id="c5bd1-127">Este valor é copiado para o item de contrato de projeto que é criado a partir desta linha de proposta quando a proposta é ganha.</span><span class="sxs-lookup"><span data-stu-id="c5bd1-127">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c5bd1-128">Project</span><span class="sxs-lookup"><span data-stu-id="c5bd1-128">Project</span></span> | <span data-ttu-id="c5bd1-129">Utilize este campo opcional para identificar o projeto que será utilizado para entregar o trabalho nesta cativação.</span><span class="sxs-lookup"><span data-stu-id="c5bd1-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="c5bd1-130">Quando um projeto é mapeado para uma linha de proposta, ajuda a configurar as tarefas faturáveis e também a trazer uma estimativa baseada em projetos para a linha de proposta como detalhes da linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="c5bd1-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="c5bd1-131">Quando um projeto não é mapeado para uma linha de proposta baseada em projetos, a estimativa deve ser criada manualmente ao criar cada detalhe da linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="c5bd1-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="c5bd1-132">Este valor é copiado para o item de contrato de projeto que é criado a partir desta linha de proposta quando a proposta é ganha.</span><span class="sxs-lookup"><span data-stu-id="c5bd1-132">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="c5bd1-133">Tarefas Incluídas</span><span class="sxs-lookup"><span data-stu-id="c5bd1-133">Included Tasks</span></span> | <span data-ttu-id="c5bd1-134">Indica se esta linha de proposta é utilizada para todas ou algumas tarefas do projeto para o projeto selecionado.</span><span class="sxs-lookup"><span data-stu-id="c5bd1-134">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="c5bd1-135">Este campo tem os seguintes valores possíveis:</span><span class="sxs-lookup"><span data-stu-id="c5bd1-135">This field has the following possible values:</span></span></br><span data-ttu-id="c5bd1-136">- Todas as tarefas do projeto</span><span class="sxs-lookup"><span data-stu-id="c5bd1-136">- All project tasks</span></span></br><span data-ttu-id="c5bd1-137">- Apenas tarefas selecionadas do projeto</span><span class="sxs-lookup"><span data-stu-id="c5bd1-137">- Selected project tasks only</span></span></br><span data-ttu-id="c5bd1-138">Um valor em branco neste campo é equivalente à opção **Todas as tarefas do projeto**.</span><span class="sxs-lookup"><span data-stu-id="c5bd1-138">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="c5bd1-139">Quando **Apenas tarefas de projeto selecionadas** é selecionado na página do projeto, o separador de **configuração de faturação de tarefas** permite-lhe selecionar tarefas específicas para as associar a esta linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="c5bd1-139">When **Selected project tasks only** is selected on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="c5bd1-140">Este valor é copiado para o item de contrato de projeto que é criado a partir desta linha de proposta quando a proposta é ganha.</span><span class="sxs-lookup"><span data-stu-id="c5bd1-140">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c5bd1-141">Incluir Tempo</span><span class="sxs-lookup"><span data-stu-id="c5bd1-141">Include Time</span></span> | <span data-ttu-id="c5bd1-142">Um valor **Sim**/**Não** indica se as transações de tempo ou os custos de mão de obra no projeto selecionado serão incluídos na estimativa desta linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="c5bd1-142">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="c5bd1-143">Um valor **Não** indica que as transações de tempo ou o custo de mão de obra não será incluído na estimativa nesta linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="c5bd1-143">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="c5bd1-144">Um valor **Sim** indica que as transações de tempo ou o custo de mão de obra será incluído na estimativa nesta linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="c5bd1-144">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="c5bd1-145">Este valor é copiado para o item de contrato de projeto que é criado a partir desta linha de proposta quando a proposta é ganha.</span><span class="sxs-lookup"><span data-stu-id="c5bd1-145">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c5bd1-146">Incluir Despesa</span><span class="sxs-lookup"><span data-stu-id="c5bd1-146">Include Expense</span></span> | <span data-ttu-id="c5bd1-147">Um valor **Sim**/**Não** indica se os custos de despesa no projeto selecionado serão incluídos na estimativa desta linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="c5bd1-147">A **Yes**/**No** value indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="c5bd1-148">Um valor **Não** indica que o custo de despesa não será incluído na estimativa nesta linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="c5bd1-148">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="c5bd1-149">Um valor **Sim** indica que o custo de despesa será incluído na estimativa nesta linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="c5bd1-149">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="c5bd1-150">Este valor é copiado para o item de contrato de projeto que é criado a partir desta linha de proposta quando a proposta é ganha.</span><span class="sxs-lookup"><span data-stu-id="c5bd1-150">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c5bd1-151">Incluir Material</span><span class="sxs-lookup"><span data-stu-id="c5bd1-151">Include Material</span></span> | <span data-ttu-id="c5bd1-152">Um valor **Sim**/**Não** indica se os custos de material no projeto selecionado serão incluídos na estimativa desta linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="c5bd1-152">A **Yes**/**No** value indicates if material costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="c5bd1-153">Um valor **Não** indica que custos de material não serão incluídos na estimativa desta linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="c5bd1-153">A **No** value indicates that the material costs will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="c5bd1-154">Um valor **Sim** indica que custos de material serão incluídos na estimativa desta linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="c5bd1-154">A **Yes** value indicates that the material costs will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="c5bd1-155">Este valor é copiado para o item de contrato de projeto que é criado a partir desta linha de proposta quando a proposta é ganha.</span><span class="sxs-lookup"><span data-stu-id="c5bd1-155">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c5bd1-156">Incluir Taxa</span><span class="sxs-lookup"><span data-stu-id="c5bd1-156">Include Fee</span></span> | <span data-ttu-id="c5bd1-157">Um valor **Sim**/**Não** indica se as taxas no projeto selecionado serão incluídas na estimativa desta linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="c5bd1-157">A **Yes**/**No** value indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="c5bd1-158">Um valor **Não** indica que as taxas não serão incluídas na estimativa nesta linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="c5bd1-158">A **No** value indicates that the fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="c5bd1-159">Um valor **Sim** indica que as taxas serão incluídas na estimativa nesta linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="c5bd1-159">A **Yes** value indicates that the fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="c5bd1-160">Este valor é copiado para o item de contrato de Projeto que é criado a partir desta linha de proposta quando a proposta é ganha.</span><span class="sxs-lookup"><span data-stu-id="c5bd1-160">This value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c5bd1-161">Montante da Proposta</span><span class="sxs-lookup"><span data-stu-id="c5bd1-161">Quoted Amount</span></span> | <span data-ttu-id="c5bd1-162">Este é o montante que será proposto ao cliente por todo o trabalho previsto nesta linha de proposta baseada em projetos.</span><span class="sxs-lookup"><span data-stu-id="c5bd1-162">This is the amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="c5bd1-163">Numa proposta criada a partir de uma oportunidade, este valor é copiado a partir do campo **Orçamento do Cliente** na linha de oportunidade.</span><span class="sxs-lookup"><span data-stu-id="c5bd1-163">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="c5bd1-164">Quando a linha de proposta baseada em projetos tem detalhes da linha, este campo é bloqueado para edição e é resumido a partir do montante nos detalhes da linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="c5bd1-164">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="c5bd1-165">Este valor é copiado para o item de contrato de projeto que é criado a partir desta linha de proposta quando a proposta é ganha.</span><span class="sxs-lookup"><span data-stu-id="c5bd1-165">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c5bd1-166">Imposto Estimado</span><span class="sxs-lookup"><span data-stu-id="c5bd1-166">Estimated Tax</span></span> | <span data-ttu-id="c5bd1-167">Este é um campo editável para o utilizador adicionar o montante do imposto estimado na linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="c5bd1-167">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="c5bd1-168">Quando uma linha de proposta baseada em projetos tem detalhes da linha, este campo é bloqueado para edição e é resumido a partir do montante do imposto nos detalhes da linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="c5bd1-168">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="c5bd1-169">Este valor é copiado para o item de contrato de projeto que é criado a partir desta linha de proposta quando a proposta é ganha.</span><span class="sxs-lookup"><span data-stu-id="c5bd1-169">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c5bd1-170">Montante da Proposta Após o Imposto</span><span class="sxs-lookup"><span data-stu-id="c5bd1-170">Quoted Amount after Tax</span></span> | <span data-ttu-id="c5bd1-171">Este campo é o montante da linha de proposta após impostos e é só de leitura.</span><span class="sxs-lookup"><span data-stu-id="c5bd1-171">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="c5bd1-172">O montante neste campo é calculado como *Montante da Proposta + Imposto*.</span><span class="sxs-lookup"><span data-stu-id="c5bd1-172">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="c5bd1-173">Este valor é copiado para o item de contrato de projeto que é criado a partir desta linha de proposta quando a proposta é ganha.</span><span class="sxs-lookup"><span data-stu-id="c5bd1-173">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c5bd1-174">Limite a não exceder</span><span class="sxs-lookup"><span data-stu-id="c5bd1-174">Not-to-exceed Limit</span></span> | <span data-ttu-id="c5bd1-175">Este campo é editável e só está disponível em linhas de proposta baseadas em projetos que têm um método de faturação **Tempo e Material**.</span><span class="sxs-lookup"><span data-stu-id="c5bd1-175">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="c5bd1-176">Este valor é copiado para o item de contrato de projeto que é criado a partir desta linha de proposta quando a proposta é ganha.</span><span class="sxs-lookup"><span data-stu-id="c5bd1-176">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c5bd1-177">Orçamento do Cliente</span><span class="sxs-lookup"><span data-stu-id="c5bd1-177">Customer Budget</span></span> | <span data-ttu-id="c5bd1-178">Este campo é editável e é copiado a partir do campo correspondente na linha de oportunidade se a proposta tiver sido criada a partir de uma oportunidade.</span><span class="sxs-lookup"><span data-stu-id="c5bd1-178">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="c5bd1-179">Este valor é copiado para o item de contrato de projeto que é criado a partir desta linha de proposta quando a proposta é ganha.</span><span class="sxs-lookup"><span data-stu-id="c5bd1-179">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="c5bd1-180">Regras de validação para os campos no separador Geral das linhas de proposta baseadas em projetos</span><span class="sxs-lookup"><span data-stu-id="c5bd1-180">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="c5bd1-181">**Regra 1**: se o campo **Tarefas Incluídas** estiver em branco ou se estiver definido como **Todas as tarefas do projeto**, é incluído um projeto na linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="c5bd1-181">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="c5bd1-182">**Regra 2**: se o campo **Tarefas Incluídas** estiver em branco, ou se estiver definido como **Todas as tarefas do projeto**, um projeto e uma determinada classe de transações só podem ser incluídos numa linha de proposta baseada em projetos de uma proposta.</span><span class="sxs-lookup"><span data-stu-id="c5bd1-182">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="c5bd1-183">**Regra 3**: se o campo **Tarefas Incluídas** estiver definido como **Apenas tarefas selecionadas do projeto**, um projeto e uma determinada classe de transações só podem ser incluídos em várias linhas de proposta baseadas em projetos de uma proposta.</span><span class="sxs-lookup"><span data-stu-id="c5bd1-183">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="c5bd1-184">**Regra 4**: se uma oportunidade tiver várias proposta, poderá haver linhas de proposta de diferentes propostas em que todas referenciam o mesmo projeto e incluem a mesma classe de transações.</span><span class="sxs-lookup"><span data-stu-id="c5bd1-184">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="c5bd1-185">**Regra 5**: se as propostas não pertencerem à mesma oportunidade, não poderão incluir o mesmo projeto e classe de transações.</span><span class="sxs-lookup"><span data-stu-id="c5bd1-185">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p><span data-ttu-id="c5bd1-186">
                    <strong>Oportunidade</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c5bd1-186">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="39" valign="top">
                <p><span data-ttu-id="c5bd1-187">
                    <strong>Proposta</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c5bd1-187">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="40" valign="top">
                <p><span data-ttu-id="c5bd1-188">
                    <strong>Linha de proposta</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c5bd1-188">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="c5bd1-189">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c5bd1-189">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="77" valign="top">
                <p><span data-ttu-id="c5bd1-190">
                    <strong>Tarefas incluídas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c5bd1-190">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="45" valign="top">
                <p><span data-ttu-id="c5bd1-191">
                    <strong>Incluir Tempo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c5bd1-191">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="46" valign="top">
                <p><span data-ttu-id="c5bd1-192">
                    <strong>Incluir Despesa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c5bd1-192">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="43" valign="top">
                <p><span data-ttu-id="c5bd1-193">
                    <strong>Incluir Material</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c5bd1-193">
                    <strong>Include Material</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="c5bd1-194">
                    <strong>Incluir</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c5bd1-194">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="c5bd1-195">
                    <strong>Taxa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c5bd1-195">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="49" valign="top">
                <p><span data-ttu-id="c5bd1-196">
                    <strong>Válido/Não válido</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c5bd1-196">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="200" valign="top">
                <p><span data-ttu-id="c5bd1-197">
                    <strong>Razão</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c5bd1-197">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="c5bd1-198">O1</span><span class="sxs-lookup"><span data-stu-id="c5bd1-198">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="c5bd1-199">T1</span><span class="sxs-lookup"><span data-stu-id="c5bd1-199">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="c5bd1-200">QL1</span><span class="sxs-lookup"><span data-stu-id="c5bd1-200">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c5bd1-201">P1</span><span class="sxs-lookup"><span data-stu-id="c5bd1-201">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="c5bd1-202">Em branco</span><span class="sxs-lookup"><span data-stu-id="c5bd1-202">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="c5bd1-203">Sim</span><span class="sxs-lookup"><span data-stu-id="c5bd1-203">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="c5bd1-204">Sim</span><span class="sxs-lookup"><span data-stu-id="c5bd1-204">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="c5bd1-205">Sim</span><span class="sxs-lookup"><span data-stu-id="c5bd1-205">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c5bd1-206">Sim</span><span class="sxs-lookup"><span data-stu-id="c5bd1-206">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c5bd1-207">Não é válido</span><span class="sxs-lookup"><span data-stu-id="c5bd1-207">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c5bd1-208">Violação da Regra n.º 2.</span><span class="sxs-lookup"><span data-stu-id="c5bd1-208">Violation of Rule #2.</span></span> <span data-ttu-id="c5bd1-209">O Tempo, a Despesa e as Taxas no projeto P1 estão incluídos nas linhas de proposta, QL1 e QL2</span><span class="sxs-lookup"><span data-stu-id="c5bd1-209">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="c5bd1-210">O1</span><span class="sxs-lookup"><span data-stu-id="c5bd1-210">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="c5bd1-211">T1</span><span class="sxs-lookup"><span data-stu-id="c5bd1-211">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="c5bd1-212">QL2</span><span class="sxs-lookup"><span data-stu-id="c5bd1-212">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c5bd1-213">P1</span><span class="sxs-lookup"><span data-stu-id="c5bd1-213">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="c5bd1-214">Em branco</span><span class="sxs-lookup"><span data-stu-id="c5bd1-214">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="c5bd1-215">Sim</span><span class="sxs-lookup"><span data-stu-id="c5bd1-215">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="c5bd1-216">Sim</span><span class="sxs-lookup"><span data-stu-id="c5bd1-216">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="c5bd1-217">Sim</span><span class="sxs-lookup"><span data-stu-id="c5bd1-217">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c5bd1-218">Sim</span><span class="sxs-lookup"><span data-stu-id="c5bd1-218">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="c5bd1-219">O1</span><span class="sxs-lookup"><span data-stu-id="c5bd1-219">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="c5bd1-220">T1</span><span class="sxs-lookup"><span data-stu-id="c5bd1-220">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="c5bd1-221">QL1</span><span class="sxs-lookup"><span data-stu-id="c5bd1-221">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c5bd1-222">P1</span><span class="sxs-lookup"><span data-stu-id="c5bd1-222">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="c5bd1-223">Em branco</span><span class="sxs-lookup"><span data-stu-id="c5bd1-223">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="c5bd1-224">Sim</span><span class="sxs-lookup"><span data-stu-id="c5bd1-224">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="c5bd1-225">No</span><span class="sxs-lookup"><span data-stu-id="c5bd1-225">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="c5bd1-226">Sim</span><span class="sxs-lookup"><span data-stu-id="c5bd1-226">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c5bd1-227">Sim</span><span class="sxs-lookup"><span data-stu-id="c5bd1-227">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c5bd1-228">Não é válido</span><span class="sxs-lookup"><span data-stu-id="c5bd1-228">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c5bd1-229">Violação da Regra n.º 2.</span><span class="sxs-lookup"><span data-stu-id="c5bd1-229">Violation of Rule #2.</span></span> <span data-ttu-id="c5bd1-230">O Tempo, o Material e as Taxas no projeto P1 estão incluídos nas linhas de proposta, QL1 e QL2</span><span class="sxs-lookup"><span data-stu-id="c5bd1-230">Time, Material, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="c5bd1-231">O1</span><span class="sxs-lookup"><span data-stu-id="c5bd1-231">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="c5bd1-232">T1</span><span class="sxs-lookup"><span data-stu-id="c5bd1-232">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="c5bd1-233">QL2</span><span class="sxs-lookup"><span data-stu-id="c5bd1-233">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c5bd1-234">P1</span><span class="sxs-lookup"><span data-stu-id="c5bd1-234">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="c5bd1-235">Em branco</span><span class="sxs-lookup"><span data-stu-id="c5bd1-235">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="c5bd1-236">Sim</span><span class="sxs-lookup"><span data-stu-id="c5bd1-236">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="c5bd1-237">Sim</span><span class="sxs-lookup"><span data-stu-id="c5bd1-237">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="c5bd1-238">Sim</span><span class="sxs-lookup"><span data-stu-id="c5bd1-238">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c5bd1-239">Sim</span><span class="sxs-lookup"><span data-stu-id="c5bd1-239">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="c5bd1-240">O1</span><span class="sxs-lookup"><span data-stu-id="c5bd1-240">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="c5bd1-241">T1</span><span class="sxs-lookup"><span data-stu-id="c5bd1-241">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="c5bd1-242">QL1</span><span class="sxs-lookup"><span data-stu-id="c5bd1-242">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c5bd1-243">P1</span><span class="sxs-lookup"><span data-stu-id="c5bd1-243">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="c5bd1-244">Em branco</span><span class="sxs-lookup"><span data-stu-id="c5bd1-244">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="c5bd1-245">Sim</span><span class="sxs-lookup"><span data-stu-id="c5bd1-245">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="c5bd1-246">No</span><span class="sxs-lookup"><span data-stu-id="c5bd1-246">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="c5bd1-247">Sim</span><span class="sxs-lookup"><span data-stu-id="c5bd1-247">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c5bd1-248">Sim</span><span class="sxs-lookup"><span data-stu-id="c5bd1-248">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c5bd1-249">Válido</span><span class="sxs-lookup"><span data-stu-id="c5bd1-249">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c5bd1-250">O tempo, material e as taxas no projeto P1 estão incluídos no QL1</span><span class="sxs-lookup"><span data-stu-id="c5bd1-250">Time, Material, and Fees on P1 project are included on QL1</span></span> <br>
<span data-ttu-id="c5bd1-251">As Despesas no projeto P1 estão incluídas no QL2</span><span class="sxs-lookup"><span data-stu-id="c5bd1-251">Expense on P1 project is included on QL2</span></span> <br>
<span data-ttu-id="c5bd1-252">Não há sobreposição no que está a ser incluído em cada linha de proposta e é, portanto, válido.</span><span class="sxs-lookup"><span data-stu-id="c5bd1-252">No overlap in what is being included on each quote line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="c5bd1-253">O1</span><span class="sxs-lookup"><span data-stu-id="c5bd1-253">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="c5bd1-254">T1</span><span class="sxs-lookup"><span data-stu-id="c5bd1-254">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="c5bd1-255">QL2</span><span class="sxs-lookup"><span data-stu-id="c5bd1-255">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c5bd1-256">P1</span><span class="sxs-lookup"><span data-stu-id="c5bd1-256">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="c5bd1-257">Em branco</span><span class="sxs-lookup"><span data-stu-id="c5bd1-257">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="c5bd1-258">No</span><span class="sxs-lookup"><span data-stu-id="c5bd1-258">No</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="c5bd1-259">Sim</span><span class="sxs-lookup"><span data-stu-id="c5bd1-259">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="c5bd1-260">No</span><span class="sxs-lookup"><span data-stu-id="c5bd1-260">No</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c5bd1-261">No</span><span class="sxs-lookup"><span data-stu-id="c5bd1-261">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="c5bd1-262">O1</span><span class="sxs-lookup"><span data-stu-id="c5bd1-262">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="c5bd1-263">T1</span><span class="sxs-lookup"><span data-stu-id="c5bd1-263">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="c5bd1-264">QL1</span><span class="sxs-lookup"><span data-stu-id="c5bd1-264">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c5bd1-265">P1</span><span class="sxs-lookup"><span data-stu-id="c5bd1-265">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="c5bd1-266">Apenas tarefas selecionadas</span><span class="sxs-lookup"><span data-stu-id="c5bd1-266">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="c5bd1-267">Sim</span><span class="sxs-lookup"><span data-stu-id="c5bd1-267">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="c5bd1-268">Sim</span><span class="sxs-lookup"><span data-stu-id="c5bd1-268">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="c5bd1-269">Sim</span><span class="sxs-lookup"><span data-stu-id="c5bd1-269">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c5bd1-270">Sim</span><span class="sxs-lookup"><span data-stu-id="c5bd1-270">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c5bd1-271">Não é válido</span><span class="sxs-lookup"><span data-stu-id="c5bd1-271">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c5bd1-272">Violação da Regra #2</span><span class="sxs-lookup"><span data-stu-id="c5bd1-272">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="c5bd1-273">O Q1 inclui tempo, material, despesas e taxas num subconjunto de tarefas no projeto P1</span><span class="sxs-lookup"><span data-stu-id="c5bd1-273">Q1 includes Time, Material, Expenses and Fees on a subset of tasks on project P1</span></span> </p>
                <p>
<span data-ttu-id="c5bd1-274">O QL2 inclui tempo, despesas e taxas para todo o projeto P1 e, portanto, sobrepõe-se ao que está incluído no Q1.</span><span class="sxs-lookup"><span data-stu-id="c5bd1-274">QL2 includes Time, Expenses, and Fees for the whole project P1 and therefore overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="c5bd1-275">O1</span><span class="sxs-lookup"><span data-stu-id="c5bd1-275">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="c5bd1-276">T1</span><span class="sxs-lookup"><span data-stu-id="c5bd1-276">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="c5bd1-277">QL2</span><span class="sxs-lookup"><span data-stu-id="c5bd1-277">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c5bd1-278">P1</span><span class="sxs-lookup"><span data-stu-id="c5bd1-278">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="c5bd1-279">Em branco</span><span class="sxs-lookup"><span data-stu-id="c5bd1-279">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="c5bd1-280">Sim</span><span class="sxs-lookup"><span data-stu-id="c5bd1-280">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="c5bd1-281">Sim</span><span class="sxs-lookup"><span data-stu-id="c5bd1-281">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="c5bd1-282">Sim</span><span class="sxs-lookup"><span data-stu-id="c5bd1-282">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c5bd1-283">Sim</span><span class="sxs-lookup"><span data-stu-id="c5bd1-283">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="c5bd1-284">O1</span><span class="sxs-lookup"><span data-stu-id="c5bd1-284">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="c5bd1-285">T1</span><span class="sxs-lookup"><span data-stu-id="c5bd1-285">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="c5bd1-286">QL1</span><span class="sxs-lookup"><span data-stu-id="c5bd1-286">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c5bd1-287">P1</span><span class="sxs-lookup"><span data-stu-id="c5bd1-287">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="c5bd1-288">Apenas tarefas selecionadas</span><span class="sxs-lookup"><span data-stu-id="c5bd1-288">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="c5bd1-289">Sim</span><span class="sxs-lookup"><span data-stu-id="c5bd1-289">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="c5bd1-290">Sim</span><span class="sxs-lookup"><span data-stu-id="c5bd1-290">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="c5bd1-291">Sim</span><span class="sxs-lookup"><span data-stu-id="c5bd1-291">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c5bd1-292">Sim</span><span class="sxs-lookup"><span data-stu-id="c5bd1-292">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c5bd1-293">Válido</span><span class="sxs-lookup"><span data-stu-id="c5bd1-293">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c5bd1-294">Pela Regra n.º 3,</span><span class="sxs-lookup"><span data-stu-id="c5bd1-294">Per Rule #3,</span></span> </p>
                <p>
<span data-ttu-id="c5bd1-295">O Q1 inclui tempo, material, despesas e taxas num subconjunto de tarefas no projeto P1.</span><span class="sxs-lookup"><span data-stu-id="c5bd1-295">Q1 includes Time, Material, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="c5bd1-296">O QL2 inclui tempo, materiais, despesas e taxas para um subconjunto de tarefas no projeto P1.</span><span class="sxs-lookup"><span data-stu-id="c5bd1-296">QL2 includes Time, Material, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="c5bd1-297">A única validação adicional está em redor do subconjunto de tarefas no QL1 que é diferente do subconjunto de tarefas no QL2 para garantir que não há sobreposição.</span><span class="sxs-lookup"><span data-stu-id="c5bd1-297">The only additional validation is around the subset of tasks on QL1 which is different from the subset of tasks on QL2 to ensure that there is no overlap.</span></span> <span data-ttu-id="c5bd1-298">Isto é feito pelo sistema quando as tarefas são associadas.</span><span class="sxs-lookup"><span data-stu-id="c5bd1-298">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="c5bd1-299">O1</span><span class="sxs-lookup"><span data-stu-id="c5bd1-299">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="c5bd1-300">T1</span><span class="sxs-lookup"><span data-stu-id="c5bd1-300">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="c5bd1-301">QL2</span><span class="sxs-lookup"><span data-stu-id="c5bd1-301">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c5bd1-302">P1</span><span class="sxs-lookup"><span data-stu-id="c5bd1-302">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="c5bd1-303">Apenas tarefas selecionadas</span><span class="sxs-lookup"><span data-stu-id="c5bd1-303">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="c5bd1-304">Sim</span><span class="sxs-lookup"><span data-stu-id="c5bd1-304">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="c5bd1-305">Sim</span><span class="sxs-lookup"><span data-stu-id="c5bd1-305">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="c5bd1-306">Sim</span><span class="sxs-lookup"><span data-stu-id="c5bd1-306">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c5bd1-307">Sim</span><span class="sxs-lookup"><span data-stu-id="c5bd1-307">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="c5bd1-308">O1</span><span class="sxs-lookup"><span data-stu-id="c5bd1-308">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="c5bd1-309">T1</span><span class="sxs-lookup"><span data-stu-id="c5bd1-309">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="c5bd1-310">QL1</span><span class="sxs-lookup"><span data-stu-id="c5bd1-310">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c5bd1-311">P1</span><span class="sxs-lookup"><span data-stu-id="c5bd1-311">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="c5bd1-312">Todas as tarefas do projeto ou em branco</span><span class="sxs-lookup"><span data-stu-id="c5bd1-312">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="c5bd1-313">Sim</span><span class="sxs-lookup"><span data-stu-id="c5bd1-313">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="c5bd1-314">Sim</span><span class="sxs-lookup"><span data-stu-id="c5bd1-314">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="c5bd1-315">Sim</span><span class="sxs-lookup"><span data-stu-id="c5bd1-315">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c5bd1-316">Sim</span><span class="sxs-lookup"><span data-stu-id="c5bd1-316">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c5bd1-317">Válido</span><span class="sxs-lookup"><span data-stu-id="c5bd1-317">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c5bd1-318">De acordo com as regras #5, Q1 e Q2 são duas propostas sobre a mesma oportunidade, para que ambas possam estimar para os mesmos componentes de um projeto.</span><span class="sxs-lookup"><span data-stu-id="c5bd1-318">Per Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="c5bd1-319">O1</span><span class="sxs-lookup"><span data-stu-id="c5bd1-319">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="c5bd1-320">T2</span><span class="sxs-lookup"><span data-stu-id="c5bd1-320">Q2</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="c5bd1-321">QL1</span><span class="sxs-lookup"><span data-stu-id="c5bd1-321">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c5bd1-322">P1</span><span class="sxs-lookup"><span data-stu-id="c5bd1-322">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="c5bd1-323">Todas as tarefas do projeto ou em branco</span><span class="sxs-lookup"><span data-stu-id="c5bd1-323">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="c5bd1-324">Sim</span><span class="sxs-lookup"><span data-stu-id="c5bd1-324">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="c5bd1-325">Sim</span><span class="sxs-lookup"><span data-stu-id="c5bd1-325">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="c5bd1-326">Sim</span><span class="sxs-lookup"><span data-stu-id="c5bd1-326">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c5bd1-327">Sim</span><span class="sxs-lookup"><span data-stu-id="c5bd1-327">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="c5bd1-328">O1</span><span class="sxs-lookup"><span data-stu-id="c5bd1-328">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="c5bd1-329">T1</span><span class="sxs-lookup"><span data-stu-id="c5bd1-329">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="c5bd1-330">QL1</span><span class="sxs-lookup"><span data-stu-id="c5bd1-330">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c5bd1-331">P1</span><span class="sxs-lookup"><span data-stu-id="c5bd1-331">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="c5bd1-332">Todas as tarefas do projeto ou em branco</span><span class="sxs-lookup"><span data-stu-id="c5bd1-332">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="c5bd1-333">Sim</span><span class="sxs-lookup"><span data-stu-id="c5bd1-333">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="c5bd1-334">Sim</span><span class="sxs-lookup"><span data-stu-id="c5bd1-334">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="c5bd1-335">Sim</span><span class="sxs-lookup"><span data-stu-id="c5bd1-335">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c5bd1-336">Sim</span><span class="sxs-lookup"><span data-stu-id="c5bd1-336">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c5bd1-337">Não é Válido</span><span class="sxs-lookup"><span data-stu-id="c5bd1-337">Not Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c5bd1-338">De acordo com as regras #4, Q1 e Q2 são duas propostas sobre oportunidades diferentes, para que não possam estimar para os mesmos componentes de um mesmo projeto.</span><span class="sxs-lookup"><span data-stu-id="c5bd1-338">Per Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="c5bd1-339">O2</span><span class="sxs-lookup"><span data-stu-id="c5bd1-339">O2</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="c5bd1-340">T1</span><span class="sxs-lookup"><span data-stu-id="c5bd1-340">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="c5bd1-341">QL1</span><span class="sxs-lookup"><span data-stu-id="c5bd1-341">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c5bd1-342">P1</span><span class="sxs-lookup"><span data-stu-id="c5bd1-342">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="c5bd1-343">Todas as tarefas do projeto ou em branco</span><span class="sxs-lookup"><span data-stu-id="c5bd1-343">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="c5bd1-344">Sim</span><span class="sxs-lookup"><span data-stu-id="c5bd1-344">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="c5bd1-345">Sim</span><span class="sxs-lookup"><span data-stu-id="c5bd1-345">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="c5bd1-346">Sim</span><span class="sxs-lookup"><span data-stu-id="c5bd1-346">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c5bd1-347">Sim</span><span class="sxs-lookup"><span data-stu-id="c5bd1-347">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
