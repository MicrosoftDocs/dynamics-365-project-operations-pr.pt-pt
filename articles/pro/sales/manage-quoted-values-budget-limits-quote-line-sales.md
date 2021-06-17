---
title: Descrição geral de linhas de proposta baseadas em projetos
description: Este tópico fornece informações sobre como utilizar linhas de proposta baseadas no projeto para o trabalho de projeto.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 32337b05f09ef7c5b84fdff9870744d6367e2693
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994870"
---
# <a name="project-based-quote-lines-overview"></a><span data-ttu-id="e623e-103">Descrição geral das linhas de proposta baseadas em projetos</span><span class="sxs-lookup"><span data-stu-id="e623e-103">Project-based quote lines overview</span></span> 

<span data-ttu-id="e623e-104">_**Aplica-se a:** Implementação leve - negociar à faturação pró-forma, Project Operations para cenários baseados em recursos/não armazenados_</span><span class="sxs-lookup"><span data-stu-id="e623e-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="e623e-105">As linhas de proposta baseadas em projetos foram concebidas para ajudar a estimar o trabalho do projeto numa cativação.</span><span class="sxs-lookup"><span data-stu-id="e623e-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="e623e-106">A estrutura de uma linha de proposta baseada em projetos é expandida para as estimativas de projeto com os seguintes conceitos:</span><span class="sxs-lookup"><span data-stu-id="e623e-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="e623e-107">Método de Faturação</span><span class="sxs-lookup"><span data-stu-id="e623e-107">Billing Method</span></span>
- <span data-ttu-id="e623e-108">Mapeamento de Projetos e Tarefas</span><span class="sxs-lookup"><span data-stu-id="e623e-108">Project and Task Mapping</span></span>
- <span data-ttu-id="e623e-109">Classes de transações incluídas</span><span class="sxs-lookup"><span data-stu-id="e623e-109">Included Transaction classes</span></span>
- <span data-ttu-id="e623e-110">Limite a Não Exceder</span><span class="sxs-lookup"><span data-stu-id="e623e-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="e623e-111">Configuração da exigibilidade</span><span class="sxs-lookup"><span data-stu-id="e623e-111">Chargeability setup</span></span>
- <span data-ttu-id="e623e-112">Estimativa baseada nos Detalhes de Linha de Proposta</span><span class="sxs-lookup"><span data-stu-id="e623e-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="e623e-113">Clientes da Linha de Proposta</span><span class="sxs-lookup"><span data-stu-id="e623e-113">Quote line Customers</span></span>

<span data-ttu-id="e623e-114">A tabela seguinte fornece informações sobre os campos no separador **Geral** da linha de proposta baseada em projetos.</span><span class="sxs-lookup"><span data-stu-id="e623e-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="e623e-115">Estes campos ajudam a configurar a base para uma estimativa de raiz detalhada para o trabalho de projeto.</span><span class="sxs-lookup"><span data-stu-id="e623e-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="e623e-116">**Campo**</span><span class="sxs-lookup"><span data-stu-id="e623e-116">**Field**</span></span> | <span data-ttu-id="e623e-117">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e623e-117">**Description**</span></span> | <span data-ttu-id="e623e-118">**Impacto a jusante**</span><span class="sxs-lookup"><span data-stu-id="e623e-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="e623e-119">Nome</span><span class="sxs-lookup"><span data-stu-id="e623e-119">Name</span></span> | <span data-ttu-id="e623e-120">O nome da linha de proposta que o ajuda a identificar o componente discreto da proposta que está a ser estimada.</span><span class="sxs-lookup"><span data-stu-id="e623e-120">The name of quote line that helps you to identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="e623e-121">Copiada para o item de contrato do projeto que é criada a partir desta linha de proposta quando a proposta é ganha.</span><span class="sxs-lookup"><span data-stu-id="e623e-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e623e-122">Método de Faturação</span><span class="sxs-lookup"><span data-stu-id="e623e-122">Billing Method</span></span> | <span data-ttu-id="e623e-123">Numa proposta criada a partir de uma oportunidade, este valor é copiado a partir do campo correspondente na linha de oportunidade.</span><span class="sxs-lookup"><span data-stu-id="e623e-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="e623e-124">Este campo inclui os dois principais modelos de contratação suportados por Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="e623e-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="e623e-125">- Preço fixo</span><span class="sxs-lookup"><span data-stu-id="e623e-125">- Fixed price</span></span></br><span data-ttu-id="e623e-126">- Tempo e material.</span><span class="sxs-lookup"><span data-stu-id="e623e-126">- Time and material.</span></span>| <span data-ttu-id="e623e-127">Este valor é copiado para o item de contrato de projeto que é criado a partir desta linha de proposta quando a proposta é ganha.</span><span class="sxs-lookup"><span data-stu-id="e623e-127">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e623e-128">Project</span><span class="sxs-lookup"><span data-stu-id="e623e-128">Project</span></span> | <span data-ttu-id="e623e-129">Utilize este campo opcional para identificar o projeto que será utilizado para entregar o trabalho nesta cativação.</span><span class="sxs-lookup"><span data-stu-id="e623e-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="e623e-130">Quando um projeto é mapeado para uma linha de proposta, ajuda a configurar as tarefas faturáveis e também a trazer uma estimativa baseada em projetos para a linha de proposta como detalhes da linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="e623e-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="e623e-131">Quando um projeto não é mapeado para uma linha de proposta baseada em projetos, a estimativa deve ser criada manualmente ao criar cada detalhe da linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="e623e-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="e623e-132">Este valor é copiado para o item de contrato de projeto que é criado a partir desta linha de proposta quando a proposta é ganha.</span><span class="sxs-lookup"><span data-stu-id="e623e-132">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="e623e-133">Tarefas Incluídas</span><span class="sxs-lookup"><span data-stu-id="e623e-133">Included Tasks</span></span> | <span data-ttu-id="e623e-134">Indica se esta linha de proposta é utilizada para todas ou algumas tarefas do projeto para o projeto selecionado.</span><span class="sxs-lookup"><span data-stu-id="e623e-134">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="e623e-135">Este campo tem os seguintes valores possíveis:</span><span class="sxs-lookup"><span data-stu-id="e623e-135">This field has the following possible values:</span></span></br><span data-ttu-id="e623e-136">- Todas as tarefas do projeto</span><span class="sxs-lookup"><span data-stu-id="e623e-136">- All project tasks</span></span></br><span data-ttu-id="e623e-137">- Apenas tarefas selecionadas do projeto</span><span class="sxs-lookup"><span data-stu-id="e623e-137">- Selected project tasks only</span></span></br><span data-ttu-id="e623e-138">Um valor em branco neste campo é equivalente à opção **Todas as tarefas do projeto**.</span><span class="sxs-lookup"><span data-stu-id="e623e-138">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="e623e-139">Quando **Apenas tarefas de projeto selecionadas** é selecionado na página do projeto, o separador de **configuração de faturação de tarefas** permite-lhe selecionar tarefas específicas para as associar a esta linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="e623e-139">When **Selected project tasks only** is selected on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="e623e-140">Este valor é copiado para o item de contrato de projeto que é criado a partir desta linha de proposta quando a proposta é ganha.</span><span class="sxs-lookup"><span data-stu-id="e623e-140">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e623e-141">Incluir Tempo</span><span class="sxs-lookup"><span data-stu-id="e623e-141">Include Time</span></span> | <span data-ttu-id="e623e-142">Um valor **Sim**/**Não** indica se as transações de tempo ou os custos de mão de obra no projeto selecionado serão incluídos na estimativa desta linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="e623e-142">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="e623e-143">Um valor **Não** indica que as transações de tempo ou o custo de mão de obra não será incluído na estimativa nesta linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="e623e-143">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="e623e-144">Um valor **Sim** indica que as transações de tempo ou o custo de mão de obra será incluído na estimativa nesta linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="e623e-144">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="e623e-145">Este valor é copiado para o item de contrato de projeto que é criado a partir desta linha de proposta quando a proposta é ganha.</span><span class="sxs-lookup"><span data-stu-id="e623e-145">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e623e-146">Incluir Despesa</span><span class="sxs-lookup"><span data-stu-id="e623e-146">Include Expense</span></span> | <span data-ttu-id="e623e-147">Um valor **Sim**/**Não** indica se os custos de despesa no projeto selecionado serão incluídos na estimativa desta linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="e623e-147">A **Yes**/**No** value indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="e623e-148">Um valor **Não** indica que o custo de despesa não será incluído na estimativa nesta linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="e623e-148">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="e623e-149">Um valor **Sim** indica que o custo de despesa será incluído na estimativa nesta linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="e623e-149">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="e623e-150">Este valor é copiado para o item de contrato de projeto que é criado a partir desta linha de proposta quando a proposta é ganha.</span><span class="sxs-lookup"><span data-stu-id="e623e-150">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e623e-151">Incluir Material</span><span class="sxs-lookup"><span data-stu-id="e623e-151">Include Material</span></span> | <span data-ttu-id="e623e-152">Um valor **Sim**/**Não** indica se os custos de material no projeto selecionado serão incluídos na estimativa desta linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="e623e-152">A **Yes**/**No** value indicates if material costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="e623e-153">Um valor **Não** indica que custos de material não serão incluídos na estimativa desta linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="e623e-153">A **No** value indicates that the material costs will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="e623e-154">Um valor **Sim** indica que custos de material serão incluídos na estimativa desta linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="e623e-154">A **Yes** value indicates that the material costs will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="e623e-155">Este valor é copiado para o item de contrato de projeto que é criado a partir desta linha de proposta quando a proposta é ganha.</span><span class="sxs-lookup"><span data-stu-id="e623e-155">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e623e-156">Incluir Taxa</span><span class="sxs-lookup"><span data-stu-id="e623e-156">Include Fee</span></span> | <span data-ttu-id="e623e-157">Um valor **Sim**/**Não** indica se as taxas no projeto selecionado serão incluídas na estimativa desta linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="e623e-157">A **Yes**/**No** value indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="e623e-158">Um valor **Não** indica que as taxas não serão incluídas na estimativa nesta linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="e623e-158">A **No** value indicates that the fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="e623e-159">Um valor **Sim** indica que as taxas serão incluídas na estimativa nesta linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="e623e-159">A **Yes** value indicates that the fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="e623e-160">Este valor é copiado para o item de contrato de Projeto que é criado a partir desta linha de proposta quando a proposta é ganha.</span><span class="sxs-lookup"><span data-stu-id="e623e-160">This value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e623e-161">Montante da Proposta</span><span class="sxs-lookup"><span data-stu-id="e623e-161">Quoted Amount</span></span> | <span data-ttu-id="e623e-162">Este é o montante que será proposto ao cliente por todo o trabalho previsto nesta linha de proposta baseada em projetos.</span><span class="sxs-lookup"><span data-stu-id="e623e-162">This is the amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="e623e-163">Numa proposta criada a partir de uma oportunidade, este valor é copiado a partir do campo **Orçamento do Cliente** na linha de oportunidade.</span><span class="sxs-lookup"><span data-stu-id="e623e-163">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="e623e-164">Quando a linha de proposta baseada em projetos tem detalhes da linha, este campo é bloqueado para edição e é resumido a partir do montante nos detalhes da linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="e623e-164">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="e623e-165">Este valor é copiado para o item de contrato de projeto que é criado a partir desta linha de proposta quando a proposta é ganha.</span><span class="sxs-lookup"><span data-stu-id="e623e-165">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e623e-166">Imposto Estimado</span><span class="sxs-lookup"><span data-stu-id="e623e-166">Estimated Tax</span></span> | <span data-ttu-id="e623e-167">Este é um campo editável para o utilizador adicionar o montante do imposto estimado na linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="e623e-167">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="e623e-168">Quando uma linha de proposta baseada em projetos tem detalhes da linha, este campo é bloqueado para edição e é resumido a partir do montante do imposto nos detalhes da linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="e623e-168">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="e623e-169">Este valor é copiado para o item de contrato de projeto que é criado a partir desta linha de proposta quando a proposta é ganha.</span><span class="sxs-lookup"><span data-stu-id="e623e-169">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e623e-170">Montante da Proposta Após o Imposto</span><span class="sxs-lookup"><span data-stu-id="e623e-170">Quoted Amount after Tax</span></span> | <span data-ttu-id="e623e-171">Este campo é o montante da linha de proposta após impostos e é só de leitura.</span><span class="sxs-lookup"><span data-stu-id="e623e-171">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="e623e-172">O montante neste campo é calculado como *Montante da Proposta + Imposto*.</span><span class="sxs-lookup"><span data-stu-id="e623e-172">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="e623e-173">Este valor é copiado para o item de contrato de projeto que é criado a partir desta linha de proposta quando a proposta é ganha.</span><span class="sxs-lookup"><span data-stu-id="e623e-173">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e623e-174">Limite a não exceder</span><span class="sxs-lookup"><span data-stu-id="e623e-174">Not-to-exceed Limit</span></span> | <span data-ttu-id="e623e-175">Este campo é editável e só está disponível em linhas de proposta baseadas em projetos que têm um método de faturação **Tempo e Material**.</span><span class="sxs-lookup"><span data-stu-id="e623e-175">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="e623e-176">Este valor é copiado para o item de contrato de projeto que é criado a partir desta linha de proposta quando a proposta é ganha.</span><span class="sxs-lookup"><span data-stu-id="e623e-176">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e623e-177">Orçamento do Cliente</span><span class="sxs-lookup"><span data-stu-id="e623e-177">Customer Budget</span></span> | <span data-ttu-id="e623e-178">Este campo é editável e é copiado a partir do campo correspondente na linha de oportunidade se a proposta tiver sido criada a partir de uma oportunidade.</span><span class="sxs-lookup"><span data-stu-id="e623e-178">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="e623e-179">Este valor é copiado para o item de contrato de projeto que é criado a partir desta linha de proposta quando a proposta é ganha.</span><span class="sxs-lookup"><span data-stu-id="e623e-179">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="e623e-180">Regras de validação para os campos no separador Geral das linhas de proposta baseadas em projetos</span><span class="sxs-lookup"><span data-stu-id="e623e-180">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="e623e-181">**Regra 1**: se o campo **Tarefas Incluídas** estiver em branco ou se estiver definido como **Todas as tarefas do projeto**, é incluído um projeto na linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="e623e-181">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="e623e-182">**Regra 2**: se o campo **Tarefas Incluídas** estiver em branco, ou se estiver definido como **Todas as tarefas do projeto**, um projeto e uma determinada classe de transações só podem ser incluídos numa linha de proposta baseada em projetos de uma proposta.</span><span class="sxs-lookup"><span data-stu-id="e623e-182">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="e623e-183">**Regra 3**: se o campo **Tarefas Incluídas** estiver definido como **Apenas tarefas selecionadas do projeto**, um projeto e uma determinada classe de transações só podem ser incluídos em várias linhas de proposta baseadas em projetos de uma proposta.</span><span class="sxs-lookup"><span data-stu-id="e623e-183">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="e623e-184">**Regra 4**: se uma oportunidade tiver várias proposta, poderá haver linhas de proposta de diferentes propostas em que todas referenciam o mesmo projeto e incluem a mesma classe de transações.</span><span class="sxs-lookup"><span data-stu-id="e623e-184">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="e623e-185">**Regra 5**: se as propostas não pertencerem à mesma oportunidade, não poderão incluir o mesmo projeto e classe de transações.</span><span class="sxs-lookup"><span data-stu-id="e623e-185">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p><span data-ttu-id="e623e-186">
                    <strong>Oportunidade</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e623e-186">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="39" valign="top">
                <p><span data-ttu-id="e623e-187">
                    <strong>Proposta</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e623e-187">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="40" valign="top">
                <p><span data-ttu-id="e623e-188">
                    <strong>Linha de proposta</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e623e-188">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="e623e-189">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e623e-189">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="77" valign="top">
                <p><span data-ttu-id="e623e-190">
                    <strong>Tarefas incluídas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e623e-190">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="45" valign="top">
                <p><span data-ttu-id="e623e-191">
                    <strong>Incluir Tempo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e623e-191">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="46" valign="top">
                <p><span data-ttu-id="e623e-192">
                    <strong>Incluir Despesa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e623e-192">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="43" valign="top">
                <p><span data-ttu-id="e623e-193">
                    <strong>Incluir Material</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e623e-193">
                    <strong>Include Material</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="e623e-194">
                    <strong>Incluir</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e623e-194">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="e623e-195">
                    <strong>Taxa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e623e-195">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="49" valign="top">
                <p><span data-ttu-id="e623e-196">
                    <strong>Válido/Não válido</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e623e-196">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="200" valign="top">
                <p><span data-ttu-id="e623e-197">
                    <strong>Razão</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e623e-197">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="e623e-198">O1</span><span class="sxs-lookup"><span data-stu-id="e623e-198">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="e623e-199">T1</span><span class="sxs-lookup"><span data-stu-id="e623e-199">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="e623e-200">QL1</span><span class="sxs-lookup"><span data-stu-id="e623e-200">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e623e-201">P1</span><span class="sxs-lookup"><span data-stu-id="e623e-201">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="e623e-202">Em branco</span><span class="sxs-lookup"><span data-stu-id="e623e-202">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="e623e-203">Sim</span><span class="sxs-lookup"><span data-stu-id="e623e-203">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="e623e-204">Sim</span><span class="sxs-lookup"><span data-stu-id="e623e-204">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="e623e-205">Sim</span><span class="sxs-lookup"><span data-stu-id="e623e-205">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e623e-206">Sim</span><span class="sxs-lookup"><span data-stu-id="e623e-206">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e623e-207">Não é válido</span><span class="sxs-lookup"><span data-stu-id="e623e-207">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e623e-208">Violação da Regra n.º 2.</span><span class="sxs-lookup"><span data-stu-id="e623e-208">Violation of Rule #2.</span></span> <span data-ttu-id="e623e-209">O Tempo, a Despesa e as Taxas no projeto P1 estão incluídos nas linhas de proposta, QL1 e QL2</span><span class="sxs-lookup"><span data-stu-id="e623e-209">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="e623e-210">O1</span><span class="sxs-lookup"><span data-stu-id="e623e-210">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="e623e-211">T1</span><span class="sxs-lookup"><span data-stu-id="e623e-211">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="e623e-212">QL2</span><span class="sxs-lookup"><span data-stu-id="e623e-212">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e623e-213">P1</span><span class="sxs-lookup"><span data-stu-id="e623e-213">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="e623e-214">Em branco</span><span class="sxs-lookup"><span data-stu-id="e623e-214">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="e623e-215">Sim</span><span class="sxs-lookup"><span data-stu-id="e623e-215">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="e623e-216">Sim</span><span class="sxs-lookup"><span data-stu-id="e623e-216">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="e623e-217">Sim</span><span class="sxs-lookup"><span data-stu-id="e623e-217">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e623e-218">Sim</span><span class="sxs-lookup"><span data-stu-id="e623e-218">Yes</span></span> </p>
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
<span data-ttu-id="e623e-219">O1</span><span class="sxs-lookup"><span data-stu-id="e623e-219">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="e623e-220">T1</span><span class="sxs-lookup"><span data-stu-id="e623e-220">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="e623e-221">QL1</span><span class="sxs-lookup"><span data-stu-id="e623e-221">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e623e-222">P1</span><span class="sxs-lookup"><span data-stu-id="e623e-222">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="e623e-223">Em branco</span><span class="sxs-lookup"><span data-stu-id="e623e-223">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="e623e-224">Sim</span><span class="sxs-lookup"><span data-stu-id="e623e-224">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="e623e-225">No</span><span class="sxs-lookup"><span data-stu-id="e623e-225">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="e623e-226">Sim</span><span class="sxs-lookup"><span data-stu-id="e623e-226">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e623e-227">Sim</span><span class="sxs-lookup"><span data-stu-id="e623e-227">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e623e-228">Não é válido</span><span class="sxs-lookup"><span data-stu-id="e623e-228">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e623e-229">Violação da Regra n.º 2.</span><span class="sxs-lookup"><span data-stu-id="e623e-229">Violation of Rule #2.</span></span> <span data-ttu-id="e623e-230">O Tempo, o Material e as Taxas no projeto P1 estão incluídos nas linhas de proposta, QL1 e QL2</span><span class="sxs-lookup"><span data-stu-id="e623e-230">Time, Material, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="e623e-231">O1</span><span class="sxs-lookup"><span data-stu-id="e623e-231">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="e623e-232">T1</span><span class="sxs-lookup"><span data-stu-id="e623e-232">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="e623e-233">QL2</span><span class="sxs-lookup"><span data-stu-id="e623e-233">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e623e-234">P1</span><span class="sxs-lookup"><span data-stu-id="e623e-234">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="e623e-235">Em branco</span><span class="sxs-lookup"><span data-stu-id="e623e-235">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="e623e-236">Sim</span><span class="sxs-lookup"><span data-stu-id="e623e-236">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="e623e-237">Sim</span><span class="sxs-lookup"><span data-stu-id="e623e-237">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="e623e-238">Sim</span><span class="sxs-lookup"><span data-stu-id="e623e-238">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e623e-239">Sim</span><span class="sxs-lookup"><span data-stu-id="e623e-239">Yes</span></span> </p>
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
<span data-ttu-id="e623e-240">O1</span><span class="sxs-lookup"><span data-stu-id="e623e-240">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="e623e-241">T1</span><span class="sxs-lookup"><span data-stu-id="e623e-241">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="e623e-242">QL1</span><span class="sxs-lookup"><span data-stu-id="e623e-242">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e623e-243">P1</span><span class="sxs-lookup"><span data-stu-id="e623e-243">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="e623e-244">Em branco</span><span class="sxs-lookup"><span data-stu-id="e623e-244">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="e623e-245">Sim</span><span class="sxs-lookup"><span data-stu-id="e623e-245">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="e623e-246">No</span><span class="sxs-lookup"><span data-stu-id="e623e-246">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="e623e-247">Sim</span><span class="sxs-lookup"><span data-stu-id="e623e-247">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e623e-248">Sim</span><span class="sxs-lookup"><span data-stu-id="e623e-248">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e623e-249">Válido</span><span class="sxs-lookup"><span data-stu-id="e623e-249">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e623e-250">O tempo, material e as taxas no projeto P1 estão incluídos no QL1</span><span class="sxs-lookup"><span data-stu-id="e623e-250">Time, Material, and Fees on P1 project are included on QL1</span></span> <br>
<span data-ttu-id="e623e-251">As Despesas no projeto P1 estão incluídas no QL2</span><span class="sxs-lookup"><span data-stu-id="e623e-251">Expense on P1 project is included on QL2</span></span> <br>
<span data-ttu-id="e623e-252">Não há sobreposição no que está a ser incluído em cada linha de proposta e é, portanto, válido.</span><span class="sxs-lookup"><span data-stu-id="e623e-252">No overlap in what is being included on each quote line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="e623e-253">O1</span><span class="sxs-lookup"><span data-stu-id="e623e-253">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="e623e-254">T1</span><span class="sxs-lookup"><span data-stu-id="e623e-254">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="e623e-255">QL2</span><span class="sxs-lookup"><span data-stu-id="e623e-255">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e623e-256">P1</span><span class="sxs-lookup"><span data-stu-id="e623e-256">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="e623e-257">Em branco</span><span class="sxs-lookup"><span data-stu-id="e623e-257">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="e623e-258">No</span><span class="sxs-lookup"><span data-stu-id="e623e-258">No</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="e623e-259">Sim</span><span class="sxs-lookup"><span data-stu-id="e623e-259">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="e623e-260">No</span><span class="sxs-lookup"><span data-stu-id="e623e-260">No</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e623e-261">No</span><span class="sxs-lookup"><span data-stu-id="e623e-261">No</span></span> </p>
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
<span data-ttu-id="e623e-262">O1</span><span class="sxs-lookup"><span data-stu-id="e623e-262">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="e623e-263">T1</span><span class="sxs-lookup"><span data-stu-id="e623e-263">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="e623e-264">QL1</span><span class="sxs-lookup"><span data-stu-id="e623e-264">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e623e-265">P1</span><span class="sxs-lookup"><span data-stu-id="e623e-265">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="e623e-266">Apenas tarefas selecionadas</span><span class="sxs-lookup"><span data-stu-id="e623e-266">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="e623e-267">Sim</span><span class="sxs-lookup"><span data-stu-id="e623e-267">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="e623e-268">Sim</span><span class="sxs-lookup"><span data-stu-id="e623e-268">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="e623e-269">Sim</span><span class="sxs-lookup"><span data-stu-id="e623e-269">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e623e-270">Sim</span><span class="sxs-lookup"><span data-stu-id="e623e-270">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e623e-271">Não é válido</span><span class="sxs-lookup"><span data-stu-id="e623e-271">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e623e-272">Violação da Regra #2</span><span class="sxs-lookup"><span data-stu-id="e623e-272">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="e623e-273">O Q1 inclui tempo, material, despesas e taxas num subconjunto de tarefas no projeto P1</span><span class="sxs-lookup"><span data-stu-id="e623e-273">Q1 includes Time, Material, Expenses and Fees on a subset of tasks on project P1</span></span> </p>
                <p>
<span data-ttu-id="e623e-274">O QL2 inclui tempo, despesas e taxas para todo o projeto P1 e, portanto, sobrepõe-se ao que está incluído no Q1.</span><span class="sxs-lookup"><span data-stu-id="e623e-274">QL2 includes Time, Expenses, and Fees for the whole project P1 and therefore overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="e623e-275">O1</span><span class="sxs-lookup"><span data-stu-id="e623e-275">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="e623e-276">T1</span><span class="sxs-lookup"><span data-stu-id="e623e-276">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="e623e-277">QL2</span><span class="sxs-lookup"><span data-stu-id="e623e-277">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e623e-278">P1</span><span class="sxs-lookup"><span data-stu-id="e623e-278">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="e623e-279">Em branco</span><span class="sxs-lookup"><span data-stu-id="e623e-279">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="e623e-280">Sim</span><span class="sxs-lookup"><span data-stu-id="e623e-280">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="e623e-281">Sim</span><span class="sxs-lookup"><span data-stu-id="e623e-281">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="e623e-282">Sim</span><span class="sxs-lookup"><span data-stu-id="e623e-282">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e623e-283">Sim</span><span class="sxs-lookup"><span data-stu-id="e623e-283">Yes</span></span> </p>
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
<span data-ttu-id="e623e-284">O1</span><span class="sxs-lookup"><span data-stu-id="e623e-284">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="e623e-285">T1</span><span class="sxs-lookup"><span data-stu-id="e623e-285">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="e623e-286">QL1</span><span class="sxs-lookup"><span data-stu-id="e623e-286">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e623e-287">P1</span><span class="sxs-lookup"><span data-stu-id="e623e-287">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="e623e-288">Apenas tarefas selecionadas</span><span class="sxs-lookup"><span data-stu-id="e623e-288">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="e623e-289">Sim</span><span class="sxs-lookup"><span data-stu-id="e623e-289">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="e623e-290">Sim</span><span class="sxs-lookup"><span data-stu-id="e623e-290">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="e623e-291">Sim</span><span class="sxs-lookup"><span data-stu-id="e623e-291">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e623e-292">Sim</span><span class="sxs-lookup"><span data-stu-id="e623e-292">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e623e-293">Válido</span><span class="sxs-lookup"><span data-stu-id="e623e-293">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e623e-294">Pela Regra n.º 3,</span><span class="sxs-lookup"><span data-stu-id="e623e-294">Per Rule #3,</span></span> </p>
                <p>
<span data-ttu-id="e623e-295">O Q1 inclui tempo, material, despesas e taxas num subconjunto de tarefas no projeto P1.</span><span class="sxs-lookup"><span data-stu-id="e623e-295">Q1 includes Time, Material, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="e623e-296">O QL2 inclui tempo, materiais, despesas e taxas para um subconjunto de tarefas no projeto P1.</span><span class="sxs-lookup"><span data-stu-id="e623e-296">QL2 includes Time, Material, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="e623e-297">A única validação adicional está em redor do subconjunto de tarefas no QL1 que é diferente do subconjunto de tarefas no QL2 para garantir que não há sobreposição.</span><span class="sxs-lookup"><span data-stu-id="e623e-297">The only additional validation is around the subset of tasks on QL1 which is different from the subset of tasks on QL2 to ensure that there is no overlap.</span></span> <span data-ttu-id="e623e-298">Isto é feito pelo sistema quando as tarefas são associadas.</span><span class="sxs-lookup"><span data-stu-id="e623e-298">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="e623e-299">O1</span><span class="sxs-lookup"><span data-stu-id="e623e-299">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="e623e-300">T1</span><span class="sxs-lookup"><span data-stu-id="e623e-300">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="e623e-301">QL2</span><span class="sxs-lookup"><span data-stu-id="e623e-301">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e623e-302">P1</span><span class="sxs-lookup"><span data-stu-id="e623e-302">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="e623e-303">Apenas tarefas selecionadas</span><span class="sxs-lookup"><span data-stu-id="e623e-303">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="e623e-304">Sim</span><span class="sxs-lookup"><span data-stu-id="e623e-304">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="e623e-305">Sim</span><span class="sxs-lookup"><span data-stu-id="e623e-305">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="e623e-306">Sim</span><span class="sxs-lookup"><span data-stu-id="e623e-306">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e623e-307">Sim</span><span class="sxs-lookup"><span data-stu-id="e623e-307">Yes</span></span> </p>
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
<span data-ttu-id="e623e-308">O1</span><span class="sxs-lookup"><span data-stu-id="e623e-308">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="e623e-309">T1</span><span class="sxs-lookup"><span data-stu-id="e623e-309">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="e623e-310">QL1</span><span class="sxs-lookup"><span data-stu-id="e623e-310">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e623e-311">P1</span><span class="sxs-lookup"><span data-stu-id="e623e-311">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="e623e-312">Todas as tarefas do projeto ou em branco</span><span class="sxs-lookup"><span data-stu-id="e623e-312">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="e623e-313">Sim</span><span class="sxs-lookup"><span data-stu-id="e623e-313">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="e623e-314">Sim</span><span class="sxs-lookup"><span data-stu-id="e623e-314">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="e623e-315">Sim</span><span class="sxs-lookup"><span data-stu-id="e623e-315">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e623e-316">Sim</span><span class="sxs-lookup"><span data-stu-id="e623e-316">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e623e-317">Válido</span><span class="sxs-lookup"><span data-stu-id="e623e-317">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e623e-318">De acordo com as regras #5, Q1 e Q2 são duas propostas sobre a mesma oportunidade, para que ambas possam estimar para os mesmos componentes de um projeto.</span><span class="sxs-lookup"><span data-stu-id="e623e-318">Per Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="e623e-319">O1</span><span class="sxs-lookup"><span data-stu-id="e623e-319">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="e623e-320">T2</span><span class="sxs-lookup"><span data-stu-id="e623e-320">Q2</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="e623e-321">QL1</span><span class="sxs-lookup"><span data-stu-id="e623e-321">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e623e-322">P1</span><span class="sxs-lookup"><span data-stu-id="e623e-322">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="e623e-323">Todas as tarefas do projeto ou em branco</span><span class="sxs-lookup"><span data-stu-id="e623e-323">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="e623e-324">Sim</span><span class="sxs-lookup"><span data-stu-id="e623e-324">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="e623e-325">Sim</span><span class="sxs-lookup"><span data-stu-id="e623e-325">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="e623e-326">Sim</span><span class="sxs-lookup"><span data-stu-id="e623e-326">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e623e-327">Sim</span><span class="sxs-lookup"><span data-stu-id="e623e-327">Yes</span></span> </p>
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
<span data-ttu-id="e623e-328">O1</span><span class="sxs-lookup"><span data-stu-id="e623e-328">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="e623e-329">T1</span><span class="sxs-lookup"><span data-stu-id="e623e-329">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="e623e-330">QL1</span><span class="sxs-lookup"><span data-stu-id="e623e-330">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e623e-331">P1</span><span class="sxs-lookup"><span data-stu-id="e623e-331">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="e623e-332">Todas as tarefas do projeto ou em branco</span><span class="sxs-lookup"><span data-stu-id="e623e-332">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="e623e-333">Sim</span><span class="sxs-lookup"><span data-stu-id="e623e-333">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="e623e-334">Sim</span><span class="sxs-lookup"><span data-stu-id="e623e-334">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="e623e-335">Sim</span><span class="sxs-lookup"><span data-stu-id="e623e-335">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e623e-336">Sim</span><span class="sxs-lookup"><span data-stu-id="e623e-336">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e623e-337">Não é Válido</span><span class="sxs-lookup"><span data-stu-id="e623e-337">Not Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e623e-338">De acordo com as regras #4, Q1 e Q2 são duas propostas sobre oportunidades diferentes, para que não possam estimar para os mesmos componentes de um mesmo projeto.</span><span class="sxs-lookup"><span data-stu-id="e623e-338">Per Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="e623e-339">O2</span><span class="sxs-lookup"><span data-stu-id="e623e-339">O2</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="e623e-340">T1</span><span class="sxs-lookup"><span data-stu-id="e623e-340">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="e623e-341">QL1</span><span class="sxs-lookup"><span data-stu-id="e623e-341">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e623e-342">P1</span><span class="sxs-lookup"><span data-stu-id="e623e-342">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="e623e-343">Todas as tarefas do projeto ou em branco</span><span class="sxs-lookup"><span data-stu-id="e623e-343">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="e623e-344">Sim</span><span class="sxs-lookup"><span data-stu-id="e623e-344">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="e623e-345">Sim</span><span class="sxs-lookup"><span data-stu-id="e623e-345">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="e623e-346">Sim</span><span class="sxs-lookup"><span data-stu-id="e623e-346">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e623e-347">Sim</span><span class="sxs-lookup"><span data-stu-id="e623e-347">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
