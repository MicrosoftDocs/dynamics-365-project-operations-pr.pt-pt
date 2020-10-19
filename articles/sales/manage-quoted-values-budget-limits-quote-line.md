---
title: Linhas de proposta baseadas em projetos
description: Este tópico fornece informações sobre como utilizar linhas de proposta baseadas no projeto para o trabalho de projeto.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 06a47c45dc3b3b174658e2fba14d3d2050aabf85
ms.sourcegitcommit: a0f80d024a5d3112a39781815bd31d0c05ddaf6f
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 09/30/2020
ms.locfileid: "3906291"
---
# <a name="project-based-quote-lines"></a><span data-ttu-id="5f48c-103">Linhas de proposta baseadas em projetos</span><span class="sxs-lookup"><span data-stu-id="5f48c-103">Project-based quote lines</span></span>

<span data-ttu-id="5f48c-104">_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_</span><span class="sxs-lookup"><span data-stu-id="5f48c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="5f48c-105">As linhas de proposta baseadas em projetos foram concebidas para ajudar a estimar o trabalho do projeto numa cativação.</span><span class="sxs-lookup"><span data-stu-id="5f48c-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="5f48c-106">A estrutura de uma linha de proposta baseada em projetos é expandida para as estimativas de projeto com os seguintes conceitos:</span><span class="sxs-lookup"><span data-stu-id="5f48c-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="5f48c-107">Método de Faturação</span><span class="sxs-lookup"><span data-stu-id="5f48c-107">Billing Method</span></span>
- <span data-ttu-id="5f48c-108">Mapeamento de Projetos</span><span class="sxs-lookup"><span data-stu-id="5f48c-108">Project Mapping</span></span>
- <span data-ttu-id="5f48c-109">Classes de transações incluídas</span><span class="sxs-lookup"><span data-stu-id="5f48c-109">Included Transaction classes</span></span>
- <span data-ttu-id="5f48c-110">Limite a Não Exceder</span><span class="sxs-lookup"><span data-stu-id="5f48c-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="5f48c-111">Configuração da exigibilidade</span><span class="sxs-lookup"><span data-stu-id="5f48c-111">Chargeability setup</span></span>
- <span data-ttu-id="5f48c-112">Estimativa baseada nos Detalhes de Linha de Proposta</span><span class="sxs-lookup"><span data-stu-id="5f48c-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="5f48c-113">Clientes da Linha de Proposta</span><span class="sxs-lookup"><span data-stu-id="5f48c-113">Quote line Customers</span></span>

<span data-ttu-id="5f48c-114">A tabela seguinte fornece informações sobre os campos no separador **Geral** da linha de proposta baseada em projetos.</span><span class="sxs-lookup"><span data-stu-id="5f48c-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="5f48c-115">Estes campos ajudam a configurar a base para uma estimativa de raiz detalhada para o trabalho de projeto.</span><span class="sxs-lookup"><span data-stu-id="5f48c-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="5f48c-116">**Campo**</span><span class="sxs-lookup"><span data-stu-id="5f48c-116">**Field**</span></span> | <span data-ttu-id="5f48c-117">**Relevância, finalidade e orientação**</span><span class="sxs-lookup"><span data-stu-id="5f48c-117">**Relevance, purpose, and guidance**</span></span> | <span data-ttu-id="5f48c-118">**Impacto a jusante**</span><span class="sxs-lookup"><span data-stu-id="5f48c-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="5f48c-119">Nome</span><span class="sxs-lookup"><span data-stu-id="5f48c-119">Name</span></span> | <span data-ttu-id="5f48c-120">O nome da linha de proposta que deve ajudá-lo a identificar o componente discreto da proposta que está a ser estimada.</span><span class="sxs-lookup"><span data-stu-id="5f48c-120">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="5f48c-121">Copiada para o item de contrato do projeto que é criada a partir desta linha de proposta quando a proposta é ganha.</span><span class="sxs-lookup"><span data-stu-id="5f48c-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="5f48c-122">Método de Faturação</span><span class="sxs-lookup"><span data-stu-id="5f48c-122">Billing Method</span></span> | <span data-ttu-id="5f48c-123">Numa proposta criada a partir de uma oportunidade, este valor é copiado a partir do campo correspondente na linha de oportunidade.</span><span class="sxs-lookup"><span data-stu-id="5f48c-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="5f48c-124">Este campo inclui os dois principais modelos de contratação suportados pelo Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="5f48c-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="5f48c-125">- Preço fixo</span><span class="sxs-lookup"><span data-stu-id="5f48c-125">- Fixed price</span></span></br><span data-ttu-id="5f48c-126">- Tempo e material.</span><span class="sxs-lookup"><span data-stu-id="5f48c-126">- Time and material.</span></span>| <span data-ttu-id="5f48c-127">Este valor do campo é copiado para o item de contrato do projeto que é criado a partir desta linha de proposta quando a proposta é ganha.</span><span class="sxs-lookup"><span data-stu-id="5f48c-127">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="5f48c-128">Project</span><span class="sxs-lookup"><span data-stu-id="5f48c-128">Project</span></span> | <span data-ttu-id="5f48c-129">Utilize este campo opcional para identificar o projeto que será utilizado para entregar o trabalho nesta cativação.</span><span class="sxs-lookup"><span data-stu-id="5f48c-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="5f48c-130">Quando um projeto é mapeado para uma linha de proposta, ajuda a configurar as tarefas faturáveis e também a trazer uma estimativa baseada em projetos para a linha de proposta como detalhes da linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="5f48c-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="5f48c-131">Quando um projeto não é mapeado para uma linha de proposta baseada em projetos, a estimativa deve ser criada manualmente ao criar cada detalhe da linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="5f48c-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="5f48c-132">Este valor do campo é copiado para o item de contrato do projeto que é criado a partir desta linha de proposta quando a proposta é ganha.</span><span class="sxs-lookup"><span data-stu-id="5f48c-132">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="5f48c-133">Incluir Tempo</span><span class="sxs-lookup"><span data-stu-id="5f48c-133">Include Time</span></span> | <span data-ttu-id="5f48c-134">Um sinalizador **Sim**/**Não** indica se as transações de tempo ou os custos de mão de obra no projeto selecionado serão incluídos na estimativa nesta linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="5f48c-134">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="5f48c-135">Um valor **Não** indica que as transações de tempo ou o custo de mão de obra não será incluído na estimativa nesta linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="5f48c-135">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="5f48c-136">Um valor **Sim** indica que as transações de tempo ou o custo de mão de obra será incluído na estimativa nesta linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="5f48c-136">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="5f48c-137">Este valor do campo é copiado para o item de contrato do projeto que é criado a partir desta linha de proposta quando a proposta é ganha.</span><span class="sxs-lookup"><span data-stu-id="5f48c-137">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="5f48c-138">Incluir Despesa</span><span class="sxs-lookup"><span data-stu-id="5f48c-138">Include Expense</span></span> | <span data-ttu-id="5f48c-139">Um sinalizador **Sim**/**Não** indica se os custos de despesa no projeto selecionado serão incluídos na estimativa nesta linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="5f48c-139">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="5f48c-140">Um valor **Não** indica que o custo de despesa não será incluído na estimativa nesta linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="5f48c-140">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="5f48c-141">Um valor **Sim** indica que o custo de despesa será incluído na estimativa nesta linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="5f48c-141">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="5f48c-142">Este valor do campo é copiado para o item de contrato do projeto que é criado a partir desta linha de proposta quando a proposta é ganha.</span><span class="sxs-lookup"><span data-stu-id="5f48c-142">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="5f48c-143">Incluir Taxa</span><span class="sxs-lookup"><span data-stu-id="5f48c-143">Include Fee</span></span> | <span data-ttu-id="5f48c-144">Um sinalizador **Sim**/**Não** indica se as tarifas no projeto selecionado serão incluídos na estimativa nesta linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="5f48c-144">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="5f48c-145">Um valor **Não** indica que as Tarifas não serão incluídas na estimativa nesta linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="5f48c-145">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="5f48c-146">Um valor **Sim** indica que as Tarifas serão incluídas na estimativa nesta linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="5f48c-146">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="5f48c-147">Este valor do campo é copiado para o item de contrato do Projeto que é criado a partir desta linha de proposta quando a proposta é ganha.</span><span class="sxs-lookup"><span data-stu-id="5f48c-147">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="5f48c-148">Montante da Proposta</span><span class="sxs-lookup"><span data-stu-id="5f48c-148">Quoted Amount</span></span> | <span data-ttu-id="5f48c-149">Este é o montante que será proposto ao cliente por todo o trabalho previsto nesta linha de proposta baseada em projetos.</span><span class="sxs-lookup"><span data-stu-id="5f48c-149">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="5f48c-150">Numa proposta criada a partir de uma oportunidade, este valor é copiado a partir do campo **Orçamento do Cliente** na linha de oportunidade.</span><span class="sxs-lookup"><span data-stu-id="5f48c-150">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="5f48c-151">Quando a linha de proposta baseada em projetos tem detalhes da linha, este campo é bloqueado para edição e é resumido a partir do montante nos detalhes da linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="5f48c-151">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="5f48c-152">Este valor do campo é copiado para o item de contrato do projeto que é criado a partir desta linha de proposta quando a proposta é ganha.</span><span class="sxs-lookup"><span data-stu-id="5f48c-152">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="5f48c-153">Imposto Estimado</span><span class="sxs-lookup"><span data-stu-id="5f48c-153">Estimated Tax</span></span> | <span data-ttu-id="5f48c-154">Este é um campo editável para o utilizador adicionar o montante do imposto estimado na linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="5f48c-154">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="5f48c-155">Quando uma linha de proposta baseada em projetos tem detalhes da linha, este campo é bloqueado para edição e é resumido a partir do montante do imposto nos detalhes da linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="5f48c-155">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="5f48c-156">Este valor do campo é copiado para o item de contrato do projeto que é criado a partir desta linha de proposta quando a proposta é ganha.</span><span class="sxs-lookup"><span data-stu-id="5f48c-156">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="5f48c-157">Montante da Proposta Após o Imposto</span><span class="sxs-lookup"><span data-stu-id="5f48c-157">Quoted Amount after Tax</span></span> | <span data-ttu-id="5f48c-158">Este campo é o montante da linha de proposta após impostos e é só de leitura.</span><span class="sxs-lookup"><span data-stu-id="5f48c-158">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="5f48c-159">O montante neste campo é calculado como *Montante da Proposta + Imposto*.</span><span class="sxs-lookup"><span data-stu-id="5f48c-159">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="5f48c-160">Este valor do campo é copiado para o item de contrato do projeto que é criado a partir desta linha de proposta quando a proposta é ganha.</span><span class="sxs-lookup"><span data-stu-id="5f48c-160">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="5f48c-161">Limite a não exceder</span><span class="sxs-lookup"><span data-stu-id="5f48c-161">Not-to-exceed Limit</span></span> | <span data-ttu-id="5f48c-162">Este campo é editável e só está disponível em linhas de proposta baseadas em projetos que têm um método de faturação **Tempo e Material**.</span><span class="sxs-lookup"><span data-stu-id="5f48c-162">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="5f48c-163">Este valor do campo é copiado para o item de contrato do projeto que é criado a partir desta linha de proposta quando a proposta é ganha.</span><span class="sxs-lookup"><span data-stu-id="5f48c-163">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="5f48c-164">Orçamento do Cliente</span><span class="sxs-lookup"><span data-stu-id="5f48c-164">Customer Budget</span></span> | <span data-ttu-id="5f48c-165">Este campo é editável e é copiado a partir do campo correspondente na linha de oportunidade se a proposta tiver sido criada a partir de uma oportunidade.</span><span class="sxs-lookup"><span data-stu-id="5f48c-165">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="5f48c-166">Este valor do campo é copiado para o item de contrato do projeto que é criado a partir desta linha de proposta quando a proposta é ganha.</span><span class="sxs-lookup"><span data-stu-id="5f48c-166">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="5f48c-167">Regras de validação para os campos no separador Geral das linhas de proposta baseadas em projetos</span><span class="sxs-lookup"><span data-stu-id="5f48c-167">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="5f48c-168">**Regra 1**: uma determinada classe de transações no projeto selecionado só pode ser incluída numa linha de proposta baseada em projetos de uma proposta.</span><span class="sxs-lookup"><span data-stu-id="5f48c-168">**Rule 1**: A certain transaction class on the selected project can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="5f48c-169">**Regra 2**: se uma oportunidade tiver várias proposta, poderá haver linhas de proposta de diferentes propostas em que todas referenciam o mesmo projeto e incluem a mesma classe de transações.</span><span class="sxs-lookup"><span data-stu-id="5f48c-169">**Rule 2**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="5f48c-170">**Regra 3**: se as propostas não pertencerem à mesma oportunidade, não poderão incluir o mesmo projeto e classe de transações.</span><span class="sxs-lookup"><span data-stu-id="5f48c-170">**Rule 3**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="5f48c-171">
                    <strong>Oportunidade</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5f48c-171">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="5f48c-172">
                    <strong>Proposta</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5f48c-172">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="5f48c-173">
                    <strong>Linha de proposta</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5f48c-173">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="5f48c-174">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5f48c-174">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="5f48c-175">
                    <strong>Incluir tempo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5f48c-175">
                    <strong>Include time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="5f48c-176">
                    <strong>Incluir despesa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5f48c-176">
                    <strong>Include expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="5f48c-177">
                    <strong>Incluir</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5f48c-177">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="5f48c-178">
                    <strong>tarifa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5f48c-178">
                    <strong>fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="5f48c-179">
                    <strong>Válido/Não válido</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5f48c-179">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="5f48c-180">
                    <strong>Razão</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5f48c-180">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="5f48c-181">O1</span><span class="sxs-lookup"><span data-stu-id="5f48c-181">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5f48c-182">T1</span><span class="sxs-lookup"><span data-stu-id="5f48c-182">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5f48c-183">QL1</span><span class="sxs-lookup"><span data-stu-id="5f48c-183">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5f48c-184">P1</span><span class="sxs-lookup"><span data-stu-id="5f48c-184">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5f48c-185">Sim</span><span class="sxs-lookup"><span data-stu-id="5f48c-185">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5f48c-186">Sim</span><span class="sxs-lookup"><span data-stu-id="5f48c-186">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5f48c-187">Sim</span><span class="sxs-lookup"><span data-stu-id="5f48c-187">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5f48c-188">Não é válido</span><span class="sxs-lookup"><span data-stu-id="5f48c-188">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5f48c-189">Violação da Regra n.º 1.</span><span class="sxs-lookup"><span data-stu-id="5f48c-189">Violation of Rule #1.</span></span> <span data-ttu-id="5f48c-190">O Tempo, a Despesa e as Tarifas no projeto P1 estão incluídos nas duas linhas de proposta, QL1 e QL2.</span><span class="sxs-lookup"><span data-stu-id="5f48c-190">Time, Expense, and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="5f48c-191">O1</span><span class="sxs-lookup"><span data-stu-id="5f48c-191">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5f48c-192">T1</span><span class="sxs-lookup"><span data-stu-id="5f48c-192">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5f48c-193">QL2</span><span class="sxs-lookup"><span data-stu-id="5f48c-193">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5f48c-194">P1</span><span class="sxs-lookup"><span data-stu-id="5f48c-194">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5f48c-195">Sim</span><span class="sxs-lookup"><span data-stu-id="5f48c-195">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5f48c-196">Sim</span><span class="sxs-lookup"><span data-stu-id="5f48c-196">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5f48c-197">Sim</span><span class="sxs-lookup"><span data-stu-id="5f48c-197">Yes</span></span> </p>
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
<span data-ttu-id="5f48c-198">O1</span><span class="sxs-lookup"><span data-stu-id="5f48c-198">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5f48c-199">T1</span><span class="sxs-lookup"><span data-stu-id="5f48c-199">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5f48c-200">QL1</span><span class="sxs-lookup"><span data-stu-id="5f48c-200">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5f48c-201">P1</span><span class="sxs-lookup"><span data-stu-id="5f48c-201">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5f48c-202">Sim</span><span class="sxs-lookup"><span data-stu-id="5f48c-202">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5f48c-203">No</span><span class="sxs-lookup"><span data-stu-id="5f48c-203">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5f48c-204">Sim</span><span class="sxs-lookup"><span data-stu-id="5f48c-204">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5f48c-205">Não é válido</span><span class="sxs-lookup"><span data-stu-id="5f48c-205">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5f48c-206">Violação da Regra n.º 1.</span><span class="sxs-lookup"><span data-stu-id="5f48c-206">Violation of Rule #1.</span></span> <span data-ttu-id="5f48c-207">Tempo e Tarifas no projeto P1 estão incluídos nas duas linhas de proposta, QL1 e QL2.</span><span class="sxs-lookup"><span data-stu-id="5f48c-207">Time and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="5f48c-208">O1</span><span class="sxs-lookup"><span data-stu-id="5f48c-208">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5f48c-209">T1</span><span class="sxs-lookup"><span data-stu-id="5f48c-209">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5f48c-210">QL2</span><span class="sxs-lookup"><span data-stu-id="5f48c-210">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5f48c-211">P1</span><span class="sxs-lookup"><span data-stu-id="5f48c-211">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5f48c-212">Sim</span><span class="sxs-lookup"><span data-stu-id="5f48c-212">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5f48c-213">Sim</span><span class="sxs-lookup"><span data-stu-id="5f48c-213">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5f48c-214">Sim</span><span class="sxs-lookup"><span data-stu-id="5f48c-214">Yes</span></span> </p>
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
<span data-ttu-id="5f48c-215">O1</span><span class="sxs-lookup"><span data-stu-id="5f48c-215">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5f48c-216">T1</span><span class="sxs-lookup"><span data-stu-id="5f48c-216">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5f48c-217">QL1</span><span class="sxs-lookup"><span data-stu-id="5f48c-217">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5f48c-218">P1</span><span class="sxs-lookup"><span data-stu-id="5f48c-218">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5f48c-219">Sim</span><span class="sxs-lookup"><span data-stu-id="5f48c-219">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5f48c-220">No</span><span class="sxs-lookup"><span data-stu-id="5f48c-220">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5f48c-221">Sim</span><span class="sxs-lookup"><span data-stu-id="5f48c-221">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5f48c-222">Válido</span><span class="sxs-lookup"><span data-stu-id="5f48c-222">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
<span data-ttu-id="5f48c-223">O Tempo e as tarifas no projeto P1 estão incluídos no QL1.</span><span class="sxs-lookup"><span data-stu-id="5f48c-223">Time and fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="5f48c-224">As Despesas no projeto P1 estão incluídas no QL2.</span><span class="sxs-lookup"><span data-stu-id="5f48c-224">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="5f48c-225">Não existe sobreposição no que está a ser incluído em cada linha de proposta, pelo que é válido.</span><span class="sxs-lookup"><span data-stu-id="5f48c-225">There is no overlap in what is being included on each quote line so it is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="5f48c-226">O1</span><span class="sxs-lookup"><span data-stu-id="5f48c-226">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5f48c-227">T1</span><span class="sxs-lookup"><span data-stu-id="5f48c-227">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5f48c-228">QL2</span><span class="sxs-lookup"><span data-stu-id="5f48c-228">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5f48c-229">P1</span><span class="sxs-lookup"><span data-stu-id="5f48c-229">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5f48c-230">No</span><span class="sxs-lookup"><span data-stu-id="5f48c-230">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5f48c-231">Sim</span><span class="sxs-lookup"><span data-stu-id="5f48c-231">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5f48c-232">No</span><span class="sxs-lookup"><span data-stu-id="5f48c-232">No</span></span> </p>
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
<span data-ttu-id="5f48c-233">O1</span><span class="sxs-lookup"><span data-stu-id="5f48c-233">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5f48c-234">T1</span><span class="sxs-lookup"><span data-stu-id="5f48c-234">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5f48c-235">QL1</span><span class="sxs-lookup"><span data-stu-id="5f48c-235">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5f48c-236">P1</span><span class="sxs-lookup"><span data-stu-id="5f48c-236">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5f48c-237">Sim</span><span class="sxs-lookup"><span data-stu-id="5f48c-237">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5f48c-238">Sim</span><span class="sxs-lookup"><span data-stu-id="5f48c-238">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5f48c-239">Sim</span><span class="sxs-lookup"><span data-stu-id="5f48c-239">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5f48c-240">Não é válido</span><span class="sxs-lookup"><span data-stu-id="5f48c-240">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5f48c-241">Violação da Regra n.º 1 acima.</span><span class="sxs-lookup"><span data-stu-id="5f48c-241">Violation of Rule #1 above</span></span> </p>
                <p>
<span data-ttu-id="5f48c-242">O Q1 inclui Tempo, Despesas e Tarifas para todo o projeto P1.</span><span class="sxs-lookup"><span data-stu-id="5f48c-242">Q1 includes Time, Expenses, and Fees for the whole project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="5f48c-243">O QL2 inclui Tempo, Despesas e Tarifas para todo o projeto P1 e sobrepõe-se ao que está incluído no Q1.</span><span class="sxs-lookup"><span data-stu-id="5f48c-243">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="5f48c-244">O1</span><span class="sxs-lookup"><span data-stu-id="5f48c-244">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5f48c-245">T1</span><span class="sxs-lookup"><span data-stu-id="5f48c-245">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5f48c-246">QL2</span><span class="sxs-lookup"><span data-stu-id="5f48c-246">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5f48c-247">P1</span><span class="sxs-lookup"><span data-stu-id="5f48c-247">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5f48c-248">Sim</span><span class="sxs-lookup"><span data-stu-id="5f48c-248">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5f48c-249">Sim</span><span class="sxs-lookup"><span data-stu-id="5f48c-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5f48c-250">Sim</span><span class="sxs-lookup"><span data-stu-id="5f48c-250">Yes</span></span> </p>
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
<span data-ttu-id="5f48c-251">O1</span><span class="sxs-lookup"><span data-stu-id="5f48c-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5f48c-252">T1</span><span class="sxs-lookup"><span data-stu-id="5f48c-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5f48c-253">QL1</span><span class="sxs-lookup"><span data-stu-id="5f48c-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5f48c-254">P1</span><span class="sxs-lookup"><span data-stu-id="5f48c-254">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5f48c-255">Sim</span><span class="sxs-lookup"><span data-stu-id="5f48c-255">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5f48c-256">Sim</span><span class="sxs-lookup"><span data-stu-id="5f48c-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5f48c-257">Sim</span><span class="sxs-lookup"><span data-stu-id="5f48c-257">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="5f48c-258">Válido</span><span class="sxs-lookup"><span data-stu-id="5f48c-258">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5f48c-259">Baseado na Regra n.º 2, Q1 e Q2 são duas propostas na mesma oportunidade, pelo que ambos podem estimar para os mesmos componentes de um projeto.</span><span class="sxs-lookup"><span data-stu-id="5f48c-259">Based on Rule #2, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="5f48c-260">O1</span><span class="sxs-lookup"><span data-stu-id="5f48c-260">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5f48c-261">T2</span><span class="sxs-lookup"><span data-stu-id="5f48c-261">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5f48c-262">QL1 em Q2</span><span class="sxs-lookup"><span data-stu-id="5f48c-262">QL1 on Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5f48c-263">P1</span><span class="sxs-lookup"><span data-stu-id="5f48c-263">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5f48c-264">Sim</span><span class="sxs-lookup"><span data-stu-id="5f48c-264">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5f48c-265">Sim</span><span class="sxs-lookup"><span data-stu-id="5f48c-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5f48c-266">Sim</span><span class="sxs-lookup"><span data-stu-id="5f48c-266">Yes</span></span> </p>
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
<span data-ttu-id="5f48c-267">O1</span><span class="sxs-lookup"><span data-stu-id="5f48c-267">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5f48c-268">T1</span><span class="sxs-lookup"><span data-stu-id="5f48c-268">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5f48c-269">QL1</span><span class="sxs-lookup"><span data-stu-id="5f48c-269">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5f48c-270">P1</span><span class="sxs-lookup"><span data-stu-id="5f48c-270">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5f48c-271">Sim</span><span class="sxs-lookup"><span data-stu-id="5f48c-271">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5f48c-272">Sim</span><span class="sxs-lookup"><span data-stu-id="5f48c-272">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5f48c-273">Sim</span><span class="sxs-lookup"><span data-stu-id="5f48c-273">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="5f48c-274">Válido</span><span class="sxs-lookup"><span data-stu-id="5f48c-274">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5f48c-275">Baseado na Regra n.º 3, Q1 e Q2 são duas propostas em oportunidades diferentes, pelo que ambos podem estimar para os mesmos componentes do mesmo projeto.</span><span class="sxs-lookup"><span data-stu-id="5f48c-275">Based on Rule #3, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="5f48c-276">O2</span><span class="sxs-lookup"><span data-stu-id="5f48c-276">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="5f48c-277">T1</span><span class="sxs-lookup"><span data-stu-id="5f48c-277">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5f48c-278">QL1</span><span class="sxs-lookup"><span data-stu-id="5f48c-278">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5f48c-279">P1</span><span class="sxs-lookup"><span data-stu-id="5f48c-279">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5f48c-280">Sim</span><span class="sxs-lookup"><span data-stu-id="5f48c-280">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="5f48c-281">Sim</span><span class="sxs-lookup"><span data-stu-id="5f48c-281">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="5f48c-282">Sim</span><span class="sxs-lookup"><span data-stu-id="5f48c-282">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="5f48c-283">Não é Válido</span><span class="sxs-lookup"><span data-stu-id="5f48c-283">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>

