---
title: Descrição geral dos itens de contrato baseados em projetos
description: Este tópico fornece informações sobre trabalhar com itens de contrato baseados em projetos.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 22e8ff927c5ff6c3748a35031e7703e3fcfe0dab
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369930"
---
# <a name="project-based-contract-lines-overview"></a><span data-ttu-id="0caaf-103">Descrição geral dos itens de contrato baseados em projetos</span><span class="sxs-lookup"><span data-stu-id="0caaf-103">Project-based contract lines overview</span></span>

<span data-ttu-id="0caaf-104">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="0caaf-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0caaf-105">Os itens de contrato baseados em projetos no Dynamics 365 Project Operations destinam-se a manter os contratos de estimativa e faturação para componentes específicos do trabalho do projeto num compromisso.</span><span class="sxs-lookup"><span data-stu-id="0caaf-105">Project-based contract lines in Dynamics 365 Project Operations are designed to hold the estimate and billing agreements for specific components of project work on an engagement.</span></span> <span data-ttu-id="0caaf-106">A estrutura de um item de contrato baseado em projetos é alargado para estimativas de projetos e cenários de faturação com os seguintes conceitos:</span><span class="sxs-lookup"><span data-stu-id="0caaf-106">The structure of a project–based contract line is extended for project estimates and billing scenarios with the following concepts:</span></span>

- <span data-ttu-id="0caaf-107">Método de faturação</span><span class="sxs-lookup"><span data-stu-id="0caaf-107">Billing method</span></span>
- <span data-ttu-id="0caaf-108">Mapeamento de projetos e tarefas</span><span class="sxs-lookup"><span data-stu-id="0caaf-108">Project and task mapping</span></span>
- <span data-ttu-id="0caaf-109">Classes de transações incluídas</span><span class="sxs-lookup"><span data-stu-id="0caaf-109">Included transaction classes</span></span>
- <span data-ttu-id="0caaf-110">Limite a não exceder</span><span class="sxs-lookup"><span data-stu-id="0caaf-110">Not-to-exceed limit</span></span>
- <span data-ttu-id="0caaf-111">Configuração da exigibilidade</span><span class="sxs-lookup"><span data-stu-id="0caaf-111">Chargeability setup</span></span>
- <span data-ttu-id="0caaf-112">Estimativas que usam detalhes do item de contrato</span><span class="sxs-lookup"><span data-stu-id="0caaf-112">Estimates using contract line details</span></span>
- <span data-ttu-id="0caaf-113">Clientes do item de contrato</span><span class="sxs-lookup"><span data-stu-id="0caaf-113">Contract line customers</span></span>

<span data-ttu-id="0caaf-114">A tabela seguinte inclui os campos no separador **Geral** dos itens de contrato baseados em projetos que ajudam a configurar a base para uma estimativa detalhada, criada de raiz e acordos de faturação para trabalhos baseados em projetos.</span><span class="sxs-lookup"><span data-stu-id="0caaf-114">The following table includes the fields on the **General** tab of project–based contract lines that help set up the basis for a detailed, ground–up estimate and billing arrangements for project–based work.</span></span>

| <span data-ttu-id="0caaf-115">Campo</span><span class="sxs-lookup"><span data-stu-id="0caaf-115">Field</span></span> | <span data-ttu-id="0caaf-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="0caaf-116">Description</span></span> | <span data-ttu-id="0caaf-117">Impacto a jusante</span><span class="sxs-lookup"><span data-stu-id="0caaf-117">Downstream impact</span></span> |
| --- | --- | --- |
| <span data-ttu-id="0caaf-118">**Nome**</span><span class="sxs-lookup"><span data-stu-id="0caaf-118">**Name**</span></span> | <span data-ttu-id="0caaf-119">Nome do item de contrato.</span><span class="sxs-lookup"><span data-stu-id="0caaf-119">Name of the contract line.</span></span> <span data-ttu-id="0caaf-120">Isto identifica a componente discreta do contrato que está a ser estimado.</span><span class="sxs-lookup"><span data-stu-id="0caaf-120">This identifies the discrete component of the contract that is being estimated.</span></span> <span data-ttu-id="0caaf-121">Para um contrato de projeto criado a partir de uma proposta, este valor é copiado de um valor correspondente da linha de proposta baseada em projetos.</span><span class="sxs-lookup"><span data-stu-id="0caaf-121">For a project contract created from a quote, this value is copied from a corresponding value of the project-based quote line.</span></span> | <span data-ttu-id="0caaf-122">O nome copiado para a linha de fatura do projeto que é criada a partir deste item de contrato quando a fatura é criada.</span><span class="sxs-lookup"><span data-stu-id="0caaf-122">The name copied over to the project invoice line that is created from this contract line when the invoice is created.</span></span> |
| <span data-ttu-id="0caaf-123">**Método de Faturação**</span><span class="sxs-lookup"><span data-stu-id="0caaf-123">**Billing Method**</span></span> | <span data-ttu-id="0caaf-124">Num contrato de projeto criado a partir de uma proposta, este valor é copiado do campo correspondente na linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="0caaf-124">On a project contract created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="0caaf-125">Trata-se de um conjunto de opções que representa os dois principais modelos de contratação suportados pelo Project Operations:</span><span class="sxs-lookup"><span data-stu-id="0caaf-125">This is an option set that represents the two main contracting models supported by Project Operations:</span></span></br><span data-ttu-id="0caaf-126">- **Preço Fixo**</span><span class="sxs-lookup"><span data-stu-id="0caaf-126">- **Fixed Price**</span></span></br><span data-ttu-id="0caaf-127">- **Tempo e Material**</span><span class="sxs-lookup"><span data-stu-id="0caaf-127">- **Time and Material**</span></span> | <span data-ttu-id="0caaf-128">Com base no método de faturação do item de contrato referenciado, a transação real será processada.</span><span class="sxs-lookup"><span data-stu-id="0caaf-128">Based on the billing method of the referenced contract line, the actual transaction will be processed.</span></span> <span data-ttu-id="0caaf-129">Se o item de contrato referenciado pelo valor real tiver um método de faturação de tempo e material, são criados registos de valor real de custos e vendas não faturados.</span><span class="sxs-lookup"><span data-stu-id="0caaf-129">If the contract line referenced by the actual has a time and material billing method, cost and unbilled sales actual records are created.</span></span> <span data-ttu-id="0caaf-130">Se o item de contrato referenciado pelo valor real tiver um método de faturação de preço fixo, apenas é criado um valor real de custo.</span><span class="sxs-lookup"><span data-stu-id="0caaf-130">If the contract line referenced by the actual has a fixed price billing method, only a cost actual is created.</span></span> |
| <span data-ttu-id="0caaf-131">**Project**</span><span class="sxs-lookup"><span data-stu-id="0caaf-131">**Project**</span></span> | <span data-ttu-id="0caaf-132">Utilize este campo para identificar o projeto que será usado para entregar o trabalho neste compromisso.</span><span class="sxs-lookup"><span data-stu-id="0caaf-132">Use this field to identify the project that will be used to deliver the work on this engagement.</span></span> | <span data-ttu-id="0caaf-133">Este valor será utilizado em conjunto com as **Tarefas Incluídas** e as **Classes de transações incluídas** para resolver a referência do item de contrato num registo de item real ou de estimativa.</span><span class="sxs-lookup"><span data-stu-id="0caaf-133">This value will be used in conjunction with **Included Tasks** and **Included Transaction Classes** to resolve the contract line reference on an actual or estimate line record.</span></span> |
| <span data-ttu-id="0caaf-134">**Tarefas Incluídas**</span><span class="sxs-lookup"><span data-stu-id="0caaf-134">**Included Tasks**</span></span> | <span data-ttu-id="0caaf-135">Indica se este item de contrato inclui todas as tarefas do projeto para o projeto selecionado ou apenas um subconjunto das tarefas.</span><span class="sxs-lookup"><span data-stu-id="0caaf-135">Indicates if this contract line includes all project tasks for the selected project or only a subset of the tasks.</span></span> <span data-ttu-id="0caaf-136">Trata-se de um conjunto de opções que tem os seguintes valores possíveis:</span><span class="sxs-lookup"><span data-stu-id="0caaf-136">This is an option set that has the following possible values:</span></span></br><span data-ttu-id="0caaf-137">- **Todas as Tarefas do Projeto**</span><span class="sxs-lookup"><span data-stu-id="0caaf-137">- **All Project Tasks**</span></span></br><span data-ttu-id="0caaf-138">- **Apenas Tarefas Selecionadas do Projeto**.</span><span class="sxs-lookup"><span data-stu-id="0caaf-138">- **Selected Project Tasks Only**.</span></span> <span data-ttu-id="0caaf-139">Um valor em branco neste campo é igual a selecionar **Todas as Tarefas do Projeto**.</span><span class="sxs-lookup"><span data-stu-id="0caaf-139">A blank value in this field is equal to selecting **All Project Tasks**.</span></span> | <span data-ttu-id="0caaf-140">Se for selecionado **Apenas Tarefas Selecionadas**, pode selecionar tarefas específicas e associá-las a este item de contrato no separador **Configuração de Faturação de Tarefas** na página **Projeto**.</span><span class="sxs-lookup"><span data-stu-id="0caaf-140">If **Selected Tasks Only** is selected, you can select specific tasks and associate them to this contract line on the **Task Billing Setup** tab on the **Project** page.</span></span> <span data-ttu-id="0caaf-141">O valor será utilizado em conjunto com **Projeto** e classes de **Transações Incluídas** para resolver a referência do item de contrato num registo de linha de valor real ou de estimativa.</span><span class="sxs-lookup"><span data-stu-id="0caaf-141">The value will be used in conjunction with **Project** and **Included Transaction** classes to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="0caaf-142">**Incluir Tempo**</span><span class="sxs-lookup"><span data-stu-id="0caaf-142">**Include Time**</span></span> | <span data-ttu-id="0caaf-143">Um valor **Sim**/**Não** indica se as transações de tempo ou os custos de mão de obra no projeto selecionado serão incluídos neste item de contrato.</span><span class="sxs-lookup"><span data-stu-id="0caaf-143">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="0caaf-144">Um valor **Não** indica que as transações de tempo ou os custos de mão de obra não serão incluídos neste item de contrato.</span><span class="sxs-lookup"><span data-stu-id="0caaf-144">A **No** value indicates that the time transactions or labor cost will not be included on this contract line.</span></span> <span data-ttu-id="0caaf-145">Um valor **Sim** indica que serão.</span><span class="sxs-lookup"><span data-stu-id="0caaf-145">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="0caaf-146">Este valor é utilizado em conjunto com o projeto para resolver a referência do item de contrato num registo de linha real ou de estimativa.</span><span class="sxs-lookup"><span data-stu-id="0caaf-146">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="0caaf-147">**Incluir Despesa**</span><span class="sxs-lookup"><span data-stu-id="0caaf-147">**Include Expense**</span></span> | <span data-ttu-id="0caaf-148">Um valor **Sim**/**Não** indica se os custos de despesa no projeto selecionado serão incluídos neste item de contrato.</span><span class="sxs-lookup"><span data-stu-id="0caaf-148">A **Yes**/**No** value indicates if expense costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="0caaf-149">Um valor **Não** indica que os custos de despesas não serão incluídos neste item de contrato.</span><span class="sxs-lookup"><span data-stu-id="0caaf-149">A **No** value indicates that the expense cost will not be included on this contract line.</span></span> <span data-ttu-id="0caaf-150">Um valor **Sim** indica que serão.</span><span class="sxs-lookup"><span data-stu-id="0caaf-150">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="0caaf-151">Este valor é utilizado em conjunto com o projeto para resolver a referência do item de contrato num registo de linha real ou de estimativa.</span><span class="sxs-lookup"><span data-stu-id="0caaf-151">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="0caaf-152">**Incluir materiais**</span><span class="sxs-lookup"><span data-stu-id="0caaf-152">**Include Materials**</span></span> | <span data-ttu-id="0caaf-153">Um valor **Sim**/**Não** indica se os custos de material no projeto selecionado serão incluídos neste item de contrato.</span><span class="sxs-lookup"><span data-stu-id="0caaf-153">A **Yes**/**No** value indicates if material costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="0caaf-154">Um valor **Não** indica que custos de material não serão incluídos neste item de contrato.</span><span class="sxs-lookup"><span data-stu-id="0caaf-154">A **No** value indicates that the material costs will not be included on this contract line.</span></span> <span data-ttu-id="0caaf-155">Um valor **Sim** indica que serão.</span><span class="sxs-lookup"><span data-stu-id="0caaf-155">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="0caaf-156">Este valor é utilizado em conjunto com o projeto para resolver a referência do item de contrato num registo de linha real ou de estimativa.</span><span class="sxs-lookup"><span data-stu-id="0caaf-156">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="0caaf-157">**Incluir Taxa**</span><span class="sxs-lookup"><span data-stu-id="0caaf-157">**Include Fee**</span></span> | <span data-ttu-id="0caaf-158">Um valor **Sim**/**Não** indica se as taxas no projeto selecionado serão incluídas neste item de contrato.</span><span class="sxs-lookup"><span data-stu-id="0caaf-158">A **Yes**/**No** value indicates if fees on the selected project will be included on this contract line.</span></span> <span data-ttu-id="0caaf-159">Um valor **Não** indica que as taxas não serão incluídos neste item de contrato.</span><span class="sxs-lookup"><span data-stu-id="0caaf-159">A **No** value indicates that the fees will not be included on this contract line.</span></span> <span data-ttu-id="0caaf-160">Um valor **Sim** indica que serão.</span><span class="sxs-lookup"><span data-stu-id="0caaf-160">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="0caaf-161">Este valor é utilizado em conjunto com o projeto para resolver a referência do item de contrato num registo de linha real ou de estimativa.</span><span class="sxs-lookup"><span data-stu-id="0caaf-161">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="0caaf-162">**Montante Contratado**</span><span class="sxs-lookup"><span data-stu-id="0caaf-162">**Contracted Amount**</span></span> | <span data-ttu-id="0caaf-163">Num item de contrato de preço fixo, este montante é o valor acordado que será faturado ao cliente por todos os componentes de trabalho associados a este item de contrato.</span><span class="sxs-lookup"><span data-stu-id="0caaf-163">On a fixed price contract line, this amount is the agreed-on value that will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="0caaf-164">Num item de contrato de tempo e material, este montante é um valor estimado do que será faturado ao cliente por todos os componentes de trabalho associados a este item de contrato.</span><span class="sxs-lookup"><span data-stu-id="0caaf-164">On a time and material contract line, this amount is an estimated value of what will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="0caaf-165">Num contrato de projeto criado a partir de uma proposta, este valor é copiado do campo correspondente na linha de proposta.</span><span class="sxs-lookup"><span data-stu-id="0caaf-165">On a project contract that is created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="0caaf-166">Quando um item de contrato baseado em projetos tem detalhes de linha, este campo está bloqueado para edição e é resumido a partir do montante nos detalhes do item de contrato.</span><span class="sxs-lookup"><span data-stu-id="0caaf-166">When a project–based contract line has line details, this field is locked for editing and is summarized from the amount on the contract line details.</span></span> | <span data-ttu-id="0caaf-167">Quando o item de contrato tem detalhes de linha, este valor pode ser modificado alterando os montantes nos detalhes da linha.</span><span class="sxs-lookup"><span data-stu-id="0caaf-167">When the contract line has line details, this value can be modified by changing the amounts on the line details.</span></span> <span data-ttu-id="0caaf-168">Num item de contrato de preço fixo, este valor é utilizado para gerar o montante antes dos impostos sobre os marcos periódicos de faturação.</span><span class="sxs-lookup"><span data-stu-id="0caaf-168">On a fixed price contract line, this value is used to generate the amount before tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="0caaf-169">**Imposto Estimado**</span><span class="sxs-lookup"><span data-stu-id="0caaf-169">**Estimated Tax**</span></span> | <span data-ttu-id="0caaf-170">O utilizador pode editar este campo para inserir o montante estimado do imposto no item de contrato.</span><span class="sxs-lookup"><span data-stu-id="0caaf-170">The user can edit this field to input the estimated tax amount on the contract line.</span></span> <span data-ttu-id="0caaf-171">Quando um item de contrato baseado em projetos tem detalhes de linha, este campo está bloqueado para edição e é resumido a partir do montante de impostos nos detalhes do item de contrato.</span><span class="sxs-lookup"><span data-stu-id="0caaf-171">When a project–based contract line has line details, this field is locked for editing and is summarized from the tax amount on the contract line details.</span></span> | <span data-ttu-id="0caaf-172">Quando o item de contrato tem detalhes de linha, este valor pode ser modificado alterando os montantes de impostos nos detalhes da linha.</span><span class="sxs-lookup"><span data-stu-id="0caaf-172">When the contract line has line details, this value can be modified by changing the tax amounts on the line details.</span></span> <span data-ttu-id="0caaf-173">Num item de contrato de preço fixo, este valor é utilizado para gerar o imposto sobre os marcos periódicos de faturação.</span><span class="sxs-lookup"><span data-stu-id="0caaf-173">On a fixed price contract line, this value is used to generate the tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="0caaf-174">**Montante Contratado após o Imposto**</span><span class="sxs-lookup"><span data-stu-id="0caaf-174">**Contracted Amount after Tax**</span></span> | <span data-ttu-id="0caaf-175">O montante do item de contrato após o imposto.</span><span class="sxs-lookup"><span data-stu-id="0caaf-175">The contract line amount after tax.</span></span> <span data-ttu-id="0caaf-176">Este campo é apenas de leitura e é calculado como **Montante Contratado + Imposto**.</span><span class="sxs-lookup"><span data-stu-id="0caaf-176">This field is read only and is calculated as **Contracted Amount + Tax**.</span></span> | <span data-ttu-id="0caaf-177">Num item de contrato de preço fixo, este valor é utilizado para gerar os marcos periódicos de faturação.</span><span class="sxs-lookup"><span data-stu-id="0caaf-177">On a fixed price contract line, this value is used to generate periodic billing milestones.</span></span> |
| <span data-ttu-id="0caaf-178">**Limite a Não Exceder**</span><span class="sxs-lookup"><span data-stu-id="0caaf-178">**Not-to-Exceed Limit**</span></span> | <span data-ttu-id="0caaf-179">O utilizador pode editar este campo e só está disponível em itens de contrato baseados em projetos que tenham o método de faturação definido como tempo e material.</span><span class="sxs-lookup"><span data-stu-id="0caaf-179">The user can edit this field and it is only available on project-based contract lines that have the billing method set as time and material.</span></span> | <span data-ttu-id="0caaf-180">O utilizador pode editar este campo.</span><span class="sxs-lookup"><span data-stu-id="0caaf-180">The user can edit this field.</span></span> <span data-ttu-id="0caaf-181">Quando um valor real para tempo e material referencia este item de contrato por tempo e material, o montante sobre o valor real é avaliado em relação ao limite a não exceder no item de contrato.</span><span class="sxs-lookup"><span data-stu-id="0caaf-181">When an actual for time and material references this contract line for time and material, the amount on the actual is evaluated against the not-to-exceed limit on the contract line.</span></span> <span data-ttu-id="0caaf-182">Esta avaliação é concluída após a contabilização dos montantes já gastos e comprometidos.</span><span class="sxs-lookup"><span data-stu-id="0caaf-182">This evaluation is completed after  the already spent and committed amounts are accounted for.</span></span> |
| <span data-ttu-id="0caaf-183">**Orçamento do Cliente**</span><span class="sxs-lookup"><span data-stu-id="0caaf-183">**Customer Budget**</span></span> | <span data-ttu-id="0caaf-184">Este campo é editável e é copiado do campo correspondente na linha de proposta se o contrato foi criado a partir de uma proposta.</span><span class="sxs-lookup"><span data-stu-id="0caaf-184">This field is editable and is copied from the corresponding field on the quote line if the contract was created from a quote.</span></span> | <span data-ttu-id="0caaf-185">Este campo é utilizado apenas para informações e não tem qualquer significado a jusante.</span><span class="sxs-lookup"><span data-stu-id="0caaf-185">This field is only used for information and does not have any downstream significance.</span></span> |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a><span data-ttu-id="0caaf-186">Regras de validação das opções no separador Geral dos itens de contrato baseados em projetos</span><span class="sxs-lookup"><span data-stu-id="0caaf-186">Validation rules for the options on the General tab of project-based contract lines</span></span>

<span data-ttu-id="0caaf-187">Regra 1: Se o campo **Tarefas Incluídas** estiver em branco ou definido como **Todas as Tarefas do Projeto**, todas as tarefas do projeto estão incluídas no item de contrato.</span><span class="sxs-lookup"><span data-stu-id="0caaf-187">Rule 1: If the **Included Tasks** field is blank or set to **All Project Tasks**, all tasks of the project are included on the contract line.</span></span>

<span data-ttu-id="0caaf-188">Regra 2: Quando o campo **Tarefas Incluídas** estiver em branco ou explicitamente definido como **Todas as Tarefas do Projeto**, um projeto e uma determinada classe de transações só podem ser incluídos num item de contrato baseado em projetos.</span><span class="sxs-lookup"><span data-stu-id="0caaf-188">Rule 2: When the **Included Tasks** field is blank or explicitly set to **All Project Tasks**, a project and a certain transaction class can only be included on one project-based contract line of a contract.</span></span>

<span data-ttu-id="0caaf-189">Regra 3: Quando o campo **Tarefas Incluídas** estiver definido como **Apenas Tarefas do Projeto Selecionadas**, um projeto e uma determinada classe de transações podem ser incluídos em vários itens de contrato baseado em projetos de um contrato.</span><span class="sxs-lookup"><span data-stu-id="0caaf-189">Rule 3: When the **Included Tasks** field is set to **Selected Project Tasks Only**, a project and a certain transaction class can be included on multiple project-based contract lines of a contract.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p><span data-ttu-id="0caaf-190">
                    <strong>Contrato</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0caaf-190">
                    <strong>Contract</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="0caaf-191">
                    <strong>Item de contrato</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0caaf-191">
                    <strong>Contract line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="0caaf-192">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0caaf-192">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="67" valign="top">
                <p><span data-ttu-id="0caaf-193">
                    <strong>Tarefas incluídas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0caaf-193">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="0caaf-194">
                    <strong>Incluir Tempo</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0caaf-194">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="0caaf-195">
                    <strong>Incluir Despesa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0caaf-195">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="0caaf-196">
                    <strong>Incluir materiais</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0caaf-196">
                    <strong>Include Materials</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="0caaf-197">
                    <strong>Incluir</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0caaf-197">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="0caaf-198">
                    <strong>Taxa</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0caaf-198">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="53" valign="top">
                <p><span data-ttu-id="0caaf-199">
                    <strong>Válido/Não válido</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0caaf-199">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="250" valign="top">
                <p><span data-ttu-id="0caaf-200">
                    <strong>Razão</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0caaf-200">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="0caaf-201">C1</span><span class="sxs-lookup"><span data-stu-id="0caaf-201">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="0caaf-202">CL1</span><span class="sxs-lookup"><span data-stu-id="0caaf-202">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0caaf-203">P1</span><span class="sxs-lookup"><span data-stu-id="0caaf-203">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="0caaf-204">Em branco</span><span class="sxs-lookup"><span data-stu-id="0caaf-204">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0caaf-205">Sim</span><span class="sxs-lookup"><span data-stu-id="0caaf-205">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0caaf-206">Sim</span><span class="sxs-lookup"><span data-stu-id="0caaf-206">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0caaf-207">Sim</span><span class="sxs-lookup"><span data-stu-id="0caaf-207">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0caaf-208">Sim</span><span class="sxs-lookup"><span data-stu-id="0caaf-208">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0caaf-209">Não é válido</span><span class="sxs-lookup"><span data-stu-id="0caaf-209">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0caaf-210">Violação da Regra n.º 2.</span><span class="sxs-lookup"><span data-stu-id="0caaf-210">Violation of Rule #2.</span></span> <span data-ttu-id="0caaf-211">O tempo, despesas, materiais e taxas no projeto P1 estão incluídos em ambos os itens de contrato CL1 e CL2.</span><span class="sxs-lookup"><span data-stu-id="0caaf-211">Time, Expense, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="0caaf-212">C1</span><span class="sxs-lookup"><span data-stu-id="0caaf-212">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="0caaf-213">CL2</span><span class="sxs-lookup"><span data-stu-id="0caaf-213">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0caaf-214">P1</span><span class="sxs-lookup"><span data-stu-id="0caaf-214">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="0caaf-215">Em branco</span><span class="sxs-lookup"><span data-stu-id="0caaf-215">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0caaf-216">Sim</span><span class="sxs-lookup"><span data-stu-id="0caaf-216">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0caaf-217">Sim</span><span class="sxs-lookup"><span data-stu-id="0caaf-217">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0caaf-218">Sim</span><span class="sxs-lookup"><span data-stu-id="0caaf-218">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0caaf-219">Sim</span><span class="sxs-lookup"><span data-stu-id="0caaf-219">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="0caaf-220">C1</span><span class="sxs-lookup"><span data-stu-id="0caaf-220">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="0caaf-221">CL1</span><span class="sxs-lookup"><span data-stu-id="0caaf-221">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0caaf-222">P1</span><span class="sxs-lookup"><span data-stu-id="0caaf-222">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="0caaf-223">Em branco</span><span class="sxs-lookup"><span data-stu-id="0caaf-223">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0caaf-224">Sim</span><span class="sxs-lookup"><span data-stu-id="0caaf-224">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0caaf-225">No</span><span class="sxs-lookup"><span data-stu-id="0caaf-225">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0caaf-226">Sim</span><span class="sxs-lookup"><span data-stu-id="0caaf-226">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0caaf-227">Sim</span><span class="sxs-lookup"><span data-stu-id="0caaf-227">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0caaf-228">Não é válido</span><span class="sxs-lookup"><span data-stu-id="0caaf-228">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0caaf-229">Violação da Regra n.º 2.</span><span class="sxs-lookup"><span data-stu-id="0caaf-229">Violation of Rule #2.</span></span> <span data-ttu-id="0caaf-230">O tempo, materiais e taxas no projeto P1 estão incluídos em ambos os itens de contrato CL1 e CL2.</span><span class="sxs-lookup"><span data-stu-id="0caaf-230">Time, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="0caaf-231">C1</span><span class="sxs-lookup"><span data-stu-id="0caaf-231">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="0caaf-232">CL2</span><span class="sxs-lookup"><span data-stu-id="0caaf-232">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0caaf-233">P1</span><span class="sxs-lookup"><span data-stu-id="0caaf-233">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="0caaf-234">Em branco</span><span class="sxs-lookup"><span data-stu-id="0caaf-234">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0caaf-235">Sim</span><span class="sxs-lookup"><span data-stu-id="0caaf-235">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0caaf-236">Sim</span><span class="sxs-lookup"><span data-stu-id="0caaf-236">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0caaf-237">Sim</span><span class="sxs-lookup"><span data-stu-id="0caaf-237">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0caaf-238">Sim</span><span class="sxs-lookup"><span data-stu-id="0caaf-238">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="0caaf-239">C1</span><span class="sxs-lookup"><span data-stu-id="0caaf-239">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="0caaf-240">CL1</span><span class="sxs-lookup"><span data-stu-id="0caaf-240">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0caaf-241">P1</span><span class="sxs-lookup"><span data-stu-id="0caaf-241">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="0caaf-242">Em branco</span><span class="sxs-lookup"><span data-stu-id="0caaf-242">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0caaf-243">Sim</span><span class="sxs-lookup"><span data-stu-id="0caaf-243">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0caaf-244">No</span><span class="sxs-lookup"><span data-stu-id="0caaf-244">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0caaf-245">Sim</span><span class="sxs-lookup"><span data-stu-id="0caaf-245">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0caaf-246">Sim</span><span class="sxs-lookup"><span data-stu-id="0caaf-246">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0caaf-247">Válido</span><span class="sxs-lookup"><span data-stu-id="0caaf-247">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0caaf-248">O tempo, os materiais e as taxas no projeto P1 estão incluídos no CL1.</span><span class="sxs-lookup"><span data-stu-id="0caaf-248">Time, Materials, and Fees on P1 project are included on CL1.</span></span>
                </p>
                <ul>
                    <li>
<span data-ttu-id="0caaf-249">As Despesas no projeto P1 estão incluídas no CL2.</span><span class="sxs-lookup"><span data-stu-id="0caaf-249">Expense on P1 project is included on CL2.</span></span>
                    </li>
                </ul>
                <p>
<span data-ttu-id="0caaf-250">Não há sobreposição no que está a ser incluído em cada item de contrato e é, portanto, válido.</span><span class="sxs-lookup"><span data-stu-id="0caaf-250">No overlap in what is being included on each Contract line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="0caaf-251">C1</span><span class="sxs-lookup"><span data-stu-id="0caaf-251">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="0caaf-252">CL2</span><span class="sxs-lookup"><span data-stu-id="0caaf-252">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0caaf-253">P1</span><span class="sxs-lookup"><span data-stu-id="0caaf-253">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="0caaf-254">Em branco</span><span class="sxs-lookup"><span data-stu-id="0caaf-254">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0caaf-255">No</span><span class="sxs-lookup"><span data-stu-id="0caaf-255">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0caaf-256">Sim</span><span class="sxs-lookup"><span data-stu-id="0caaf-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0caaf-257">No</span><span class="sxs-lookup"><span data-stu-id="0caaf-257">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0caaf-258">No</span><span class="sxs-lookup"><span data-stu-id="0caaf-258">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="0caaf-259">C1</span><span class="sxs-lookup"><span data-stu-id="0caaf-259">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="0caaf-260">CL1</span><span class="sxs-lookup"><span data-stu-id="0caaf-260">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0caaf-261">P1</span><span class="sxs-lookup"><span data-stu-id="0caaf-261">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="0caaf-262">Apenas tarefas selecionadas</span><span class="sxs-lookup"><span data-stu-id="0caaf-262">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0caaf-263">Sim</span><span class="sxs-lookup"><span data-stu-id="0caaf-263">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0caaf-264">Sim</span><span class="sxs-lookup"><span data-stu-id="0caaf-264">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0caaf-265">Sim</span><span class="sxs-lookup"><span data-stu-id="0caaf-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0caaf-266">Sim</span><span class="sxs-lookup"><span data-stu-id="0caaf-266">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0caaf-267">Não é válido</span><span class="sxs-lookup"><span data-stu-id="0caaf-267">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0caaf-268">Violação da Regra #2</span><span class="sxs-lookup"><span data-stu-id="0caaf-268">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="0caaf-269">O C1 inclui tempo, materiais, despesas e taxas num subconjunto de tarefas no projeto P1.</span><span class="sxs-lookup"><span data-stu-id="0caaf-269">C1 includes Time, Materials, Expenses and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="0caaf-270">O CL2 inclui tempo, materiais, despesas e taxas para todo o projeto P1 e, portanto, sobrepõe-se ao que está incluído no C1.</span><span class="sxs-lookup"><span data-stu-id="0caaf-270">CL2 includes Time, Materials, Expenses and Fees for the whole project P1 and therefore overlaps with what is included on C1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="0caaf-271">C1</span><span class="sxs-lookup"><span data-stu-id="0caaf-271">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="0caaf-272">CL2</span><span class="sxs-lookup"><span data-stu-id="0caaf-272">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0caaf-273">P1</span><span class="sxs-lookup"><span data-stu-id="0caaf-273">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="0caaf-274">Em branco</span><span class="sxs-lookup"><span data-stu-id="0caaf-274">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0caaf-275">Sim</span><span class="sxs-lookup"><span data-stu-id="0caaf-275">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0caaf-276">Sim</span><span class="sxs-lookup"><span data-stu-id="0caaf-276">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0caaf-277">Sim</span><span class="sxs-lookup"><span data-stu-id="0caaf-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0caaf-278">Sim</span><span class="sxs-lookup"><span data-stu-id="0caaf-278">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="0caaf-279">C1</span><span class="sxs-lookup"><span data-stu-id="0caaf-279">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="0caaf-280">CL1</span><span class="sxs-lookup"><span data-stu-id="0caaf-280">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0caaf-281">P1</span><span class="sxs-lookup"><span data-stu-id="0caaf-281">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="0caaf-282">Apenas tarefas selecionadas</span><span class="sxs-lookup"><span data-stu-id="0caaf-282">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0caaf-283">Sim</span><span class="sxs-lookup"><span data-stu-id="0caaf-283">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0caaf-284">Sim</span><span class="sxs-lookup"><span data-stu-id="0caaf-284">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0caaf-285">Sim</span><span class="sxs-lookup"><span data-stu-id="0caaf-285">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0caaf-286">Sim</span><span class="sxs-lookup"><span data-stu-id="0caaf-286">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0caaf-287">Válido</span><span class="sxs-lookup"><span data-stu-id="0caaf-287">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0caaf-288">Pela Regra n.º 3</span><span class="sxs-lookup"><span data-stu-id="0caaf-288">Per Rule #3</span></span> </p>
                <p>
<span data-ttu-id="0caaf-289">O C1 inclui tempo, despesas, materiais e taxas num subconjunto de tarefas no projeto P1.</span><span class="sxs-lookup"><span data-stu-id="0caaf-289">C1 includes Time, Expenses, Materials, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="0caaf-290">O CL2 inclui tempo, despesas, materiais e taxas para um subconjunto de tarefas no projeto P1.</span><span class="sxs-lookup"><span data-stu-id="0caaf-290">CL2 includes Time, Expenses, Materials, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="0caaf-291">A única validação adicional está em redor do subconjunto de tarefas no CL1 e é diferente do subconjunto de tarefas no CL2 para garantir que não existem sobreposições.</span><span class="sxs-lookup"><span data-stu-id="0caaf-291">The only additional validation is around the subset of tasks on CL1 is different from the subset of tasks on CL2 to ensure that there are no overlaps there.</span></span> <span data-ttu-id="0caaf-292">Isto é feito pelo sistema quando as tarefas são associadas.</span><span class="sxs-lookup"><span data-stu-id="0caaf-292">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="0caaf-293">C1</span><span class="sxs-lookup"><span data-stu-id="0caaf-293">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="0caaf-294">CL2</span><span class="sxs-lookup"><span data-stu-id="0caaf-294">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0caaf-295">P1</span><span class="sxs-lookup"><span data-stu-id="0caaf-295">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="0caaf-296">Apenas tarefas selecionadas</span><span class="sxs-lookup"><span data-stu-id="0caaf-296">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0caaf-297">Sim</span><span class="sxs-lookup"><span data-stu-id="0caaf-297">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0caaf-298">Sim</span><span class="sxs-lookup"><span data-stu-id="0caaf-298">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0caaf-299">Sim</span><span class="sxs-lookup"><span data-stu-id="0caaf-299">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0caaf-300">Sim</span><span class="sxs-lookup"><span data-stu-id="0caaf-300">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
