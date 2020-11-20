---
title: Descrição geral de linhas de proposta baseadas em projetos – lite
description: Este tópico fornece informações sobre como utilizar linhas de proposta baseadas no projeto para o trabalho de projeto. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: be1663c0d226fa19fe4b9df566e16d215f1fc08e
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181106"
---
# <a name="project-based-quote-lines-overview---lite"></a><span data-ttu-id="883a5-104">Descrição geral de linhas de proposta baseadas em projetos – lite</span><span class="sxs-lookup"><span data-stu-id="883a5-104">Project-based quote lines overview - lite</span></span>

<span data-ttu-id="883a5-105">_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_</span><span class="sxs-lookup"><span data-stu-id="883a5-105">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="883a5-106">As linhas de proposta baseadas em projetos foram concebidas para ajudar a estimar o trabalho do projeto numa cativação.</span><span class="sxs-lookup"><span data-stu-id="883a5-106">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="883a5-107">A estrutura de uma linha de proposta baseada em projetos é expandida para as estimativas de projeto com os seguintes conceitos:</span><span class="sxs-lookup"><span data-stu-id="883a5-107">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="883a5-108">Método de Faturação</span><span class="sxs-lookup"><span data-stu-id="883a5-108">Billing Method</span></span>
- <span data-ttu-id="883a5-109">Mapeamento de Projetos e Tarefas</span><span class="sxs-lookup"><span data-stu-id="883a5-109">Project and Task Mapping</span></span>
- <span data-ttu-id="883a5-110">Classes de transações incluídas</span><span class="sxs-lookup"><span data-stu-id="883a5-110">Included Transaction classes</span></span>
- <span data-ttu-id="883a5-111">Limite a Não Exceder</span><span class="sxs-lookup"><span data-stu-id="883a5-111">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="883a5-112">Configuração da exigibilidade</span><span class="sxs-lookup"><span data-stu-id="883a5-112">Chargeability setup</span></span>
- <span data-ttu-id="883a5-113">Estimativa baseada nos Detalhes de Linha de Proposta</span><span class="sxs-lookup"><span data-stu-id="883a5-113">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="883a5-114">Clientes da Linha de Proposta</span><span class="sxs-lookup"><span data-stu-id="883a5-114">Quote line Customers</span></span>

<span data-ttu-id="883a5-115">A tabela seguinte fornece informações sobre os campos no separador **Geral** da linha de proposta baseada em projetos.</span><span class="sxs-lookup"><span data-stu-id="883a5-115">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="883a5-116">Estes campos ajudam a configurar a base para uma estimativa de raiz detalhada para o trabalho de projeto.</span><span class="sxs-lookup"><span data-stu-id="883a5-116">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="883a5-117">**Campo**</span><span class="sxs-lookup"><span data-stu-id="883a5-117">**Field**</span></span> | <span data-ttu-id="883a5-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="883a5-118">**Description**</span></span> | <span data-ttu-id="883a5-119">**Impacto a jusante**</span><span class="sxs-lookup"><span data-stu-id="883a5-119">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="883a5-120">Nome</span><span class="sxs-lookup"><span data-stu-id="883a5-120">Name</span></span> | <span data-ttu-id="883a5-121">O nome da linha de proposta que deve ajudá-lo a identificar o componente discreto da proposta que está a ser estimada.</span><span class="sxs-lookup"><span data-stu-id="883a5-121">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="883a5-122">Copiada para o item de contrato do projeto que é criada a partir desta linha de proposta quando a proposta é ganha.</span><span class="sxs-lookup"><span data-stu-id="883a5-122">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="883a5-123">Método de Faturação</span><span class="sxs-lookup"><span data-stu-id="883a5-123">Billing Method</span></span> | <span data-ttu-id="883a5-124">Numa proposta criada a partir de uma oportunidade, este valor é copiado a partir do campo correspondente na linha de oportunidade.</span><span class="sxs-lookup"><span data-stu-id="883a5-124">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="883a5-125">Este campo inclui os dois principais modelos de contratação suportados pelo Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="883a5-125">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="883a5-126">- Preço fixo</span><span class="sxs-lookup"><span data-stu-id="883a5-126">- Fixed price</span></span></br><span data-ttu-id="883a5-127">- Tempo e material.</span><span class="sxs-lookup"><span data-stu-id="883a5-127">- Time and material.</span></span>| <span data-ttu-id="883a5-128">Este valor do campo é copiado para o item de contrato do projeto que é criado a partir desta linha de proposta quando a proposta é ganha.</span><span class="sxs-lookup"><span data-stu-id="883a5-128">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="883a5-129">Project</span><span class="sxs-lookup"><span data-stu-id="883a5-129">Project</span></span> | <span data-ttu-id="883a5-130">Utilize este campo opcional para identificar o projeto que será utilizado para entregar o trabalho nesta cativação.</span><span class="sxs-lookup"><span data-stu-id="883a5-130">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="883a5-131">Quando um projeto é mapeado para uma linha de proposta, ajuda a configurar as tarefas faturáveis e também a trazer uma estimativa baseada em projetos para a linha de proposta como detalhes da linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="883a5-131">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="883a5-132">Quando um projeto não é mapeado para uma linha de proposta baseada em projetos, a estimativa deve ser criada manualmente ao criar cada detalhe da linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="883a5-132">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="883a5-133">Este valor do campo é copiado para o item de contrato do projeto que é criado a partir desta linha de proposta quando a proposta é ganha.</span><span class="sxs-lookup"><span data-stu-id="883a5-133">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="883a5-134">Tarefas Incluídas</span><span class="sxs-lookup"><span data-stu-id="883a5-134">Included Tasks</span></span> | <span data-ttu-id="883a5-135">Indica se esta linha de proposta é utilizada para todas ou algumas tarefas do projeto para o projeto selecionado.</span><span class="sxs-lookup"><span data-stu-id="883a5-135">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="883a5-136">Este campo tem os seguintes valores possíveis:</span><span class="sxs-lookup"><span data-stu-id="883a5-136">This field has the following possible values:</span></span></br><span data-ttu-id="883a5-137">- Todas as tarefas do projeto</span><span class="sxs-lookup"><span data-stu-id="883a5-137">- All project tasks</span></span></br><span data-ttu-id="883a5-138">- Apenas tarefas selecionadas do projeto</span><span class="sxs-lookup"><span data-stu-id="883a5-138">- Selected project tasks only</span></span></br><span data-ttu-id="883a5-139">Um valor em branco neste campo é equivalente à opção **Todas as tarefas do projeto**.</span><span class="sxs-lookup"><span data-stu-id="883a5-139">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="883a5-140">Quando **Apenas tarefas selecionadas do projeto** é selecionado na página do projeto, o separador **Configuração de Faturação de Tarefas** permite selecionar tarefas específicas para as associar a esta linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="883a5-140">When **Selected project tasks only** is selected then on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="883a5-141">Este valor do campo é copiado para o item de contrato do projeto que é criado a partir desta linha de proposta quando a proposta é ganha.</span><span class="sxs-lookup"><span data-stu-id="883a5-141">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="883a5-142">Incluir Tempo</span><span class="sxs-lookup"><span data-stu-id="883a5-142">Include Time</span></span> | <span data-ttu-id="883a5-143">Um sinalizador **Sim**/**Não** indica se as transações de tempo ou os custos de mão de obra no projeto selecionado serão incluídos na estimativa nesta linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="883a5-143">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="883a5-144">Um valor **Não** indica que as transações de tempo ou o custo de mão de obra não será incluído na estimativa nesta linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="883a5-144">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="883a5-145">Um valor **Sim** indica que as transações de tempo ou o custo de mão de obra será incluído na estimativa nesta linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="883a5-145">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="883a5-146">Este valor do campo é copiado para o item de contrato do projeto que é criado a partir desta linha de proposta quando a proposta é ganha.</span><span class="sxs-lookup"><span data-stu-id="883a5-146">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="883a5-147">Incluir Despesa</span><span class="sxs-lookup"><span data-stu-id="883a5-147">Include Expense</span></span> | <span data-ttu-id="883a5-148">Um sinalizador **Sim**/**Não** indica se os custos de despesa no projeto selecionado serão incluídos na estimativa nesta linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="883a5-148">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="883a5-149">Um valor **Não** indica que o custo de despesa não será incluído na estimativa nesta linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="883a5-149">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="883a5-150">Um valor **Sim** indica que o custo de despesa será incluído na estimativa nesta linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="883a5-150">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="883a5-151">Este valor do campo é copiado para o item de contrato do projeto que é criado a partir desta linha de proposta quando a proposta é ganha.</span><span class="sxs-lookup"><span data-stu-id="883a5-151">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="883a5-152">Incluir Taxa</span><span class="sxs-lookup"><span data-stu-id="883a5-152">Include Fee</span></span> | <span data-ttu-id="883a5-153">Um sinalizador **Sim**/**Não** indica se as tarifas no projeto selecionado serão incluídos na estimativa nesta linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="883a5-153">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="883a5-154">Um valor **Não** indica que as Tarifas não serão incluídas na estimativa nesta linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="883a5-154">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="883a5-155">Um valor **Sim** indica que as Tarifas serão incluídas na estimativa nesta linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="883a5-155">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="883a5-156">Este valor do campo é copiado para o item de contrato do Projeto que é criado a partir desta linha de proposta quando a proposta é ganha.</span><span class="sxs-lookup"><span data-stu-id="883a5-156">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="883a5-157">Montante da Proposta</span><span class="sxs-lookup"><span data-stu-id="883a5-157">Quoted Amount</span></span> | <span data-ttu-id="883a5-158">Este é o montante que será proposto ao cliente por todo o trabalho previsto nesta linha de proposta baseada em projetos.</span><span class="sxs-lookup"><span data-stu-id="883a5-158">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="883a5-159">Numa proposta criada a partir de uma oportunidade, este valor é copiado a partir do campo **Orçamento do Cliente** na linha de oportunidade.</span><span class="sxs-lookup"><span data-stu-id="883a5-159">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="883a5-160">Quando a linha de proposta baseada em projetos tem detalhes da linha, este campo é bloqueado para edição e é resumido a partir do montante nos detalhes da linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="883a5-160">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="883a5-161">Este valor do campo é copiado para o item de contrato do projeto que é criado a partir desta linha de proposta quando a proposta é ganha.</span><span class="sxs-lookup"><span data-stu-id="883a5-161">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="883a5-162">Imposto Estimado</span><span class="sxs-lookup"><span data-stu-id="883a5-162">Estimated Tax</span></span> | <span data-ttu-id="883a5-163">Este é um campo editável para o utilizador adicionar o montante do imposto estimado na linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="883a5-163">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="883a5-164">Quando uma linha de proposta baseada em projetos tem detalhes da linha, este campo é bloqueado para edição e é resumido a partir do montante do imposto nos detalhes da linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="883a5-164">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="883a5-165">Este valor do campo é copiado para o item de contrato do projeto que é criado a partir desta linha de proposta quando a proposta é ganha.</span><span class="sxs-lookup"><span data-stu-id="883a5-165">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="883a5-166">Montante da Proposta Após o Imposto</span><span class="sxs-lookup"><span data-stu-id="883a5-166">Quoted Amount after Tax</span></span> | <span data-ttu-id="883a5-167">Este campo é o montante da linha de proposta após impostos e é só de leitura.</span><span class="sxs-lookup"><span data-stu-id="883a5-167">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="883a5-168">O montante neste campo é calculado como *Montante da Proposta + Imposto*.</span><span class="sxs-lookup"><span data-stu-id="883a5-168">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="883a5-169">Este valor do campo é copiado para o item de contrato do projeto que é criado a partir desta linha de proposta quando a proposta é ganha.</span><span class="sxs-lookup"><span data-stu-id="883a5-169">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="883a5-170">Limite a não exceder</span><span class="sxs-lookup"><span data-stu-id="883a5-170">Not-to-exceed Limit</span></span> | <span data-ttu-id="883a5-171">Este campo é editável e só está disponível em linhas de proposta baseadas em projetos que têm um método de faturação **Tempo e Material**.</span><span class="sxs-lookup"><span data-stu-id="883a5-171">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="883a5-172">Este valor do campo é copiado para o item de contrato do projeto que é criado a partir desta linha de proposta quando a proposta é ganha.</span><span class="sxs-lookup"><span data-stu-id="883a5-172">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="883a5-173">Orçamento do Cliente</span><span class="sxs-lookup"><span data-stu-id="883a5-173">Customer Budget</span></span> | <span data-ttu-id="883a5-174">Este campo é editável e é copiado a partir do campo correspondente na linha de oportunidade se a proposta tiver sido criada a partir de uma oportunidade.</span><span class="sxs-lookup"><span data-stu-id="883a5-174">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="883a5-175">Este valor do campo é copiado para o item de contrato do projeto que é criado a partir desta linha de proposta quando a proposta é ganha.</span><span class="sxs-lookup"><span data-stu-id="883a5-175">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="883a5-176">Regras de validação para os campos no separador Geral das linhas de proposta baseadas em projetos</span><span class="sxs-lookup"><span data-stu-id="883a5-176">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="883a5-177">**Regra 1**: se o campo **Tarefas Incluídas** estiver em branco ou se estiver definido como **Todas as tarefas do projeto**, é incluído um projeto na linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="883a5-177">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="883a5-178">**Regra 2**: se o campo **Tarefas Incluídas** estiver em branco, ou se estiver definido como **Todas as tarefas do projeto**, um projeto e uma determinada classe de transações só podem ser incluídos numa linha de proposta baseada em projetos de uma proposta.</span><span class="sxs-lookup"><span data-stu-id="883a5-178">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="883a5-179">**Regra 3**: se o campo **Tarefas Incluídas** estiver definido como **Apenas tarefas selecionadas do projeto**, um projeto e uma determinada classe de transações só podem ser incluídos em várias linhas de proposta baseadas em projetos de uma proposta.</span><span class="sxs-lookup"><span data-stu-id="883a5-179">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="883a5-180">**Regra 4**: se uma oportunidade tiver várias proposta, poderá haver linhas de proposta de diferentes propostas em que todas referenciam o mesmo projeto e incluem a mesma classe de transações.</span><span class="sxs-lookup"><span data-stu-id="883a5-180">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="883a5-181">**Regra 5**: se as propostas não pertencerem à mesma oportunidade, não poderão incluir o mesmo projeto e classe de transações.</span><span class="sxs-lookup"><span data-stu-id="883a5-181">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="883a5-182">
                    <strong>Oportunidade</strong>
                </span><span class="sxs-lookup"><span data-stu-id="883a5-182">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="883a5-183">
                    <strong>Proposta</strong>
                </span><span class="sxs-lookup"><span data-stu-id="883a5-183">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="883a5-184">
                    <strong>Linha de proposta</strong>
                </span><span class="sxs-lookup"><span data-stu-id="883a5-184">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="883a5-185">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="883a5-185">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="90" valign="top">
                <p><span data-ttu-id="883a5-186">
                    <strong>Tarefas incluídas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="883a5-186">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="883a5-187">
                    <strong>Incluir Tempo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="883a5-187">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="883a5-188">
                    <strong>Incluir Despesa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="883a5-188">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="883a5-189">
                    <strong>Incluir</strong>
                </span><span class="sxs-lookup"><span data-stu-id="883a5-189">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="883a5-190">
                    <strong>Taxa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="883a5-190">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="883a5-191">
                    <strong>Válido/Não válido</strong>
                </span><span class="sxs-lookup"><span data-stu-id="883a5-191">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="883a5-192">
                    <strong>Razão</strong>
                </span><span class="sxs-lookup"><span data-stu-id="883a5-192">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="883a5-193">O1</span><span class="sxs-lookup"><span data-stu-id="883a5-193">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="883a5-194">T1</span><span class="sxs-lookup"><span data-stu-id="883a5-194">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="883a5-195">QL1</span><span class="sxs-lookup"><span data-stu-id="883a5-195">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="883a5-196">P1</span><span class="sxs-lookup"><span data-stu-id="883a5-196">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="883a5-197">Em Branco</span><span class="sxs-lookup"><span data-stu-id="883a5-197">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="883a5-198">Sim</span><span class="sxs-lookup"><span data-stu-id="883a5-198">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="883a5-199">Sim</span><span class="sxs-lookup"><span data-stu-id="883a5-199">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="883a5-200">Sim</span><span class="sxs-lookup"><span data-stu-id="883a5-200">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="883a5-201">Não é válido</span><span class="sxs-lookup"><span data-stu-id="883a5-201">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="883a5-202">Violação da Regra n.º 2.</span><span class="sxs-lookup"><span data-stu-id="883a5-202">Violation of Rule #2.</span></span> <span data-ttu-id="883a5-203">O Tempo, a Despesa e as Tarifas no projeto P1 estão incluídos nas linhas de proposta, QL1 e QL2.</span><span class="sxs-lookup"><span data-stu-id="883a5-203">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="883a5-204">O1</span><span class="sxs-lookup"><span data-stu-id="883a5-204">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="883a5-205">T1</span><span class="sxs-lookup"><span data-stu-id="883a5-205">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="883a5-206">QL2</span><span class="sxs-lookup"><span data-stu-id="883a5-206">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="883a5-207">P1</span><span class="sxs-lookup"><span data-stu-id="883a5-207">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="883a5-208">Em Branco</span><span class="sxs-lookup"><span data-stu-id="883a5-208">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="883a5-209">Sim</span><span class="sxs-lookup"><span data-stu-id="883a5-209">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="883a5-210">Sim</span><span class="sxs-lookup"><span data-stu-id="883a5-210">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="883a5-211">Sim</span><span class="sxs-lookup"><span data-stu-id="883a5-211">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="883a5-212">O1</span><span class="sxs-lookup"><span data-stu-id="883a5-212">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="883a5-213">T1</span><span class="sxs-lookup"><span data-stu-id="883a5-213">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="883a5-214">QL1</span><span class="sxs-lookup"><span data-stu-id="883a5-214">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="883a5-215">P1</span><span class="sxs-lookup"><span data-stu-id="883a5-215">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="883a5-216">Em Branco</span><span class="sxs-lookup"><span data-stu-id="883a5-216">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="883a5-217">Sim</span><span class="sxs-lookup"><span data-stu-id="883a5-217">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="883a5-218">No</span><span class="sxs-lookup"><span data-stu-id="883a5-218">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="883a5-219">Sim</span><span class="sxs-lookup"><span data-stu-id="883a5-219">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="883a5-220">Não é válido</span><span class="sxs-lookup"><span data-stu-id="883a5-220">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="883a5-221">Violação da Regra n.º 2.</span><span class="sxs-lookup"><span data-stu-id="883a5-221">Violation of Rule #2.</span></span> <span data-ttu-id="883a5-222">O Tempo e as Tarifas no projeto P1 estão incluídos nas linhas de proposta, QL1 e QL2.</span><span class="sxs-lookup"><span data-stu-id="883a5-222">Time and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="883a5-223">O1</span><span class="sxs-lookup"><span data-stu-id="883a5-223">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="883a5-224">T1</span><span class="sxs-lookup"><span data-stu-id="883a5-224">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="883a5-225">QL2</span><span class="sxs-lookup"><span data-stu-id="883a5-225">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="883a5-226">P1</span><span class="sxs-lookup"><span data-stu-id="883a5-226">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="883a5-227">Em Branco</span><span class="sxs-lookup"><span data-stu-id="883a5-227">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="883a5-228">Sim</span><span class="sxs-lookup"><span data-stu-id="883a5-228">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="883a5-229">Sim</span><span class="sxs-lookup"><span data-stu-id="883a5-229">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="883a5-230">Sim</span><span class="sxs-lookup"><span data-stu-id="883a5-230">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="883a5-231">O1</span><span class="sxs-lookup"><span data-stu-id="883a5-231">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="883a5-232">T1</span><span class="sxs-lookup"><span data-stu-id="883a5-232">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="883a5-233">QL1</span><span class="sxs-lookup"><span data-stu-id="883a5-233">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="883a5-234">P1</span><span class="sxs-lookup"><span data-stu-id="883a5-234">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="883a5-235">Em Branco</span><span class="sxs-lookup"><span data-stu-id="883a5-235">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="883a5-236">Sim</span><span class="sxs-lookup"><span data-stu-id="883a5-236">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="883a5-237">No</span><span class="sxs-lookup"><span data-stu-id="883a5-237">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="883a5-238">Sim</span><span class="sxs-lookup"><span data-stu-id="883a5-238">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="883a5-239">Válido</span><span class="sxs-lookup"><span data-stu-id="883a5-239">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
<span data-ttu-id="883a5-240">Tempo e Tarifas no projeto P1 estão incluídos no QL1.</span><span class="sxs-lookup"><span data-stu-id="883a5-240">Time and Fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="883a5-241">As Despesas no projeto P1 estão incluídas no QL2.</span><span class="sxs-lookup"><span data-stu-id="883a5-241">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="883a5-242">Não existe sobreposição no que está a ser incluído em cada linha de proposta e é válido.</span><span class="sxs-lookup"><span data-stu-id="883a5-242">There is no overlap in what is being included on each quote line and is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="883a5-243">O1</span><span class="sxs-lookup"><span data-stu-id="883a5-243">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="883a5-244">T1</span><span class="sxs-lookup"><span data-stu-id="883a5-244">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="883a5-245">QL2</span><span class="sxs-lookup"><span data-stu-id="883a5-245">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="883a5-246">P1</span><span class="sxs-lookup"><span data-stu-id="883a5-246">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="883a5-247">Em Branco</span><span class="sxs-lookup"><span data-stu-id="883a5-247">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="883a5-248">No</span><span class="sxs-lookup"><span data-stu-id="883a5-248">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="883a5-249">Sim</span><span class="sxs-lookup"><span data-stu-id="883a5-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="883a5-250">No</span><span class="sxs-lookup"><span data-stu-id="883a5-250">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="883a5-251">O1</span><span class="sxs-lookup"><span data-stu-id="883a5-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="883a5-252">T1</span><span class="sxs-lookup"><span data-stu-id="883a5-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="883a5-253">QL1</span><span class="sxs-lookup"><span data-stu-id="883a5-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="883a5-254">P1</span><span class="sxs-lookup"><span data-stu-id="883a5-254">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="883a5-255">Apenas tarefas selecionadas</span><span class="sxs-lookup"><span data-stu-id="883a5-255">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="883a5-256">Sim</span><span class="sxs-lookup"><span data-stu-id="883a5-256">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="883a5-257">Sim</span><span class="sxs-lookup"><span data-stu-id="883a5-257">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="883a5-258">Sim</span><span class="sxs-lookup"><span data-stu-id="883a5-258">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="883a5-259">Não é válido</span><span class="sxs-lookup"><span data-stu-id="883a5-259">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="883a5-260">Violação da Regra n.º 2 acima.</span><span class="sxs-lookup"><span data-stu-id="883a5-260">Violation of Rule #2 above</span></span> </p>
                <p>
<span data-ttu-id="883a5-261">O Q1 inclui Tempo, Despesas e Tarifas num subconjunto de tarefas no projeto P1.</span><span class="sxs-lookup"><span data-stu-id="883a5-261">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="883a5-262">O QL2 inclui Tempo, Despesas e Tarifas para todo o projeto P1 e sobrepõe-se ao que está incluído no Q1.</span><span class="sxs-lookup"><span data-stu-id="883a5-262">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="883a5-263">O1</span><span class="sxs-lookup"><span data-stu-id="883a5-263">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="883a5-264">T1</span><span class="sxs-lookup"><span data-stu-id="883a5-264">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="883a5-265">QL2</span><span class="sxs-lookup"><span data-stu-id="883a5-265">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="883a5-266">P1</span><span class="sxs-lookup"><span data-stu-id="883a5-266">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="883a5-267">Em Branco</span><span class="sxs-lookup"><span data-stu-id="883a5-267">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="883a5-268">Sim</span><span class="sxs-lookup"><span data-stu-id="883a5-268">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="883a5-269">Sim</span><span class="sxs-lookup"><span data-stu-id="883a5-269">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="883a5-270">Sim</span><span class="sxs-lookup"><span data-stu-id="883a5-270">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="883a5-271">O1</span><span class="sxs-lookup"><span data-stu-id="883a5-271">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="883a5-272">T1</span><span class="sxs-lookup"><span data-stu-id="883a5-272">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="883a5-273">QL1</span><span class="sxs-lookup"><span data-stu-id="883a5-273">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="883a5-274">P1</span><span class="sxs-lookup"><span data-stu-id="883a5-274">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="883a5-275">Apenas tarefas selecionadas</span><span class="sxs-lookup"><span data-stu-id="883a5-275">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="883a5-276">Sim</span><span class="sxs-lookup"><span data-stu-id="883a5-276">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="883a5-277">Sim</span><span class="sxs-lookup"><span data-stu-id="883a5-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="883a5-278">Sim</span><span class="sxs-lookup"><span data-stu-id="883a5-278">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="883a5-279">Válido</span><span class="sxs-lookup"><span data-stu-id="883a5-279">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="883a5-280">Pela Regra n.º 3 acima,</span><span class="sxs-lookup"><span data-stu-id="883a5-280">Per Rule #3 above,</span></span> </p>
                <p>
<span data-ttu-id="883a5-281">O Q1 inclui Tempo, Despesas e Tarifas num subconjunto de tarefas no projeto P1.</span><span class="sxs-lookup"><span data-stu-id="883a5-281">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="883a5-282">O QL2 inclui Tempo, Despesas e Tarifas para um subconjunto de tarefas no projeto P1.</span><span class="sxs-lookup"><span data-stu-id="883a5-282">QL2 includes Time, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="883a5-283">A única validação adicional é feita à volta do subconjunto de tarefas no QL1, que são diferentes do subconjunto de tarefas no QL2.</span><span class="sxs-lookup"><span data-stu-id="883a5-283">The only additional validation is around the subset of tasks on QL1 which are different from the subset of tasks on QL2.</span></span> <span data-ttu-id="883a5-284">Isto assegura que não há sobreposições.</span><span class="sxs-lookup"><span data-stu-id="883a5-284">This ensures that there are no overlaps.</span></span> <span data-ttu-id="883a5-285">Isto é feito pelo sistema quando as tarefas são associadas.</span><span class="sxs-lookup"><span data-stu-id="883a5-285">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="883a5-286">O1</span><span class="sxs-lookup"><span data-stu-id="883a5-286">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="883a5-287">T1</span><span class="sxs-lookup"><span data-stu-id="883a5-287">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="883a5-288">QL2</span><span class="sxs-lookup"><span data-stu-id="883a5-288">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="883a5-289">P1</span><span class="sxs-lookup"><span data-stu-id="883a5-289">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="883a5-290">Apenas tarefas selecionadas</span><span class="sxs-lookup"><span data-stu-id="883a5-290">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="883a5-291">Sim</span><span class="sxs-lookup"><span data-stu-id="883a5-291">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="883a5-292">Sim</span><span class="sxs-lookup"><span data-stu-id="883a5-292">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="883a5-293">Sim</span><span class="sxs-lookup"><span data-stu-id="883a5-293">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="883a5-294">O1</span><span class="sxs-lookup"><span data-stu-id="883a5-294">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="883a5-295">T1</span><span class="sxs-lookup"><span data-stu-id="883a5-295">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="883a5-296">QL1</span><span class="sxs-lookup"><span data-stu-id="883a5-296">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="883a5-297">P1</span><span class="sxs-lookup"><span data-stu-id="883a5-297">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="883a5-298">Todas as tarefas do projeto ou em branco</span><span class="sxs-lookup"><span data-stu-id="883a5-298">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="883a5-299">Sim</span><span class="sxs-lookup"><span data-stu-id="883a5-299">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="883a5-300">Sim</span><span class="sxs-lookup"><span data-stu-id="883a5-300">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="883a5-301">Sim</span><span class="sxs-lookup"><span data-stu-id="883a5-301">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="883a5-302">Válido</span><span class="sxs-lookup"><span data-stu-id="883a5-302">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="883a5-303">Baseado na Regra n.º 5, Q1 e Q2 são duas propostas na mesma oportunidade, pelo que ambos podem estimar para os mesmos componentes de um projeto.</span><span class="sxs-lookup"><span data-stu-id="883a5-303">Based on Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="883a5-304">O1</span><span class="sxs-lookup"><span data-stu-id="883a5-304">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="883a5-305">T2</span><span class="sxs-lookup"><span data-stu-id="883a5-305">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="883a5-306">QL1</span><span class="sxs-lookup"><span data-stu-id="883a5-306">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="883a5-307">P1</span><span class="sxs-lookup"><span data-stu-id="883a5-307">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="883a5-308">Todas as tarefas do projeto ou em branco</span><span class="sxs-lookup"><span data-stu-id="883a5-308">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="883a5-309">Sim</span><span class="sxs-lookup"><span data-stu-id="883a5-309">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="883a5-310">Sim</span><span class="sxs-lookup"><span data-stu-id="883a5-310">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="883a5-311">Sim</span><span class="sxs-lookup"><span data-stu-id="883a5-311">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="883a5-312">O1</span><span class="sxs-lookup"><span data-stu-id="883a5-312">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="883a5-313">T1</span><span class="sxs-lookup"><span data-stu-id="883a5-313">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="883a5-314">QL1</span><span class="sxs-lookup"><span data-stu-id="883a5-314">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="883a5-315">P1</span><span class="sxs-lookup"><span data-stu-id="883a5-315">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="883a5-316">Todas as tarefas do projeto ou em branco</span><span class="sxs-lookup"><span data-stu-id="883a5-316">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="883a5-317">Sim</span><span class="sxs-lookup"><span data-stu-id="883a5-317">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="883a5-318">Sim</span><span class="sxs-lookup"><span data-stu-id="883a5-318">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="883a5-319">Sim</span><span class="sxs-lookup"><span data-stu-id="883a5-319">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="883a5-320">Válido</span><span class="sxs-lookup"><span data-stu-id="883a5-320">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="883a5-321">Baseado na Regra n.º 4, Q1 e Q2 são duas propostas em oportunidades diferentes, pelo que ambos podem estimar para os mesmos componentes do mesmo projeto.</span><span class="sxs-lookup"><span data-stu-id="883a5-321">Based on Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="883a5-322">O2</span><span class="sxs-lookup"><span data-stu-id="883a5-322">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="883a5-323">T1</span><span class="sxs-lookup"><span data-stu-id="883a5-323">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="883a5-324">QL1</span><span class="sxs-lookup"><span data-stu-id="883a5-324">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="883a5-325">P1</span><span class="sxs-lookup"><span data-stu-id="883a5-325">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="883a5-326">Todas as tarefas do projeto ou em branco</span><span class="sxs-lookup"><span data-stu-id="883a5-326">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="883a5-327">Sim</span><span class="sxs-lookup"><span data-stu-id="883a5-327">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="883a5-328">Sim</span><span class="sxs-lookup"><span data-stu-id="883a5-328">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="883a5-329">Sim</span><span class="sxs-lookup"><span data-stu-id="883a5-329">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="883a5-330">Não é Válido</span><span class="sxs-lookup"><span data-stu-id="883a5-330">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>

