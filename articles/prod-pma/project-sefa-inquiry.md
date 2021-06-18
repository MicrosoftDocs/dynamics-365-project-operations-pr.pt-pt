---
title: Inquérito da Agenda de Despesas de Inquérito de Prémios Federais
description: Este tópico fornece informações sobre o inquérito da Agenda de Despesas de Prémios Federais.
author: velofog
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: andchoi
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: a16b0fb097124e26da09e220a1239cd6df303f98
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010080"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="873ba-103">Inquérito da Agenda de Despesas de Inquérito de Prémios Federais</span><span class="sxs-lookup"><span data-stu-id="873ba-103">Schedule of Expenditures of Federal Awards inquiry</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="873ba-104">De acordo com o Office of Management and Budget Circular A-133, as agências que recebem fundos federais estão sujeitas a requisitos de auditoria, que também são conhecidas como auditorias únicas.</span><span class="sxs-lookup"><span data-stu-id="873ba-104">According to Office of Management and Budget Circular A-133, agencies that receive federal funds are subject to audit requirements, which are also known as single audits.</span></span> <span data-ttu-id="873ba-105">O processo de auditoria é utilizado para reportar, de forma recorrente, as receitas e as despesas das concessões federais.</span><span class="sxs-lookup"><span data-stu-id="873ba-105">The audit process is used to report on the revenues and expenditures of federal grants on a recurring basis.</span></span> <span data-ttu-id="873ba-106">Parte do relatório único de auditoria inclui a Lista de Despesas de Prémios Federais (SEFA).</span><span class="sxs-lookup"><span data-stu-id="873ba-106">Part of the single audit report includes the Schedule of Expenditures of Federal Awards (SEFA).</span></span>

<span data-ttu-id="873ba-107">O inquérito da Agenda de Despesas de Prémios Federais inclui o Título e número do Catálogo de Assistência Interna Federal (CFDA), o número de concessão, o ano da concessão, o nome da agência federal que disponibiliza os fundos, e o nome da entidade pass-through.</span><span class="sxs-lookup"><span data-stu-id="873ba-107">The Schedule of Expenditures of Federal Awards inquiry includes the Catalog of Federal Domestic Assistance (CFDA) title and number, the grant number, the year of the grant, the name of the federal agency that provides the funds, and the name of the pass-through entity.</span></span> <span data-ttu-id="873ba-108">O inquérito é para um período específico.</span><span class="sxs-lookup"><span data-stu-id="873ba-108">The inquiry is for a specific period.</span></span> <span data-ttu-id="873ba-109">Tipicamente, esse período é o mesmo que o período da declaração financeira, que é um ano fiscal.</span><span class="sxs-lookup"><span data-stu-id="873ba-109">Typically, that period is the same as the financial statement period, which is a fiscal year.</span></span>

<span data-ttu-id="873ba-110">O inquérito inclui concessões que tenham datas de projeção no intervalo de datas selecionadas.</span><span class="sxs-lookup"><span data-stu-id="873ba-110">The inquiry includes grants that have projection dates in the selected date range.</span></span> <span data-ttu-id="873ba-111">A coluna **Agência concessora** do inquérito mostra o cliente da concessão ou, para uma concessão pass-through, a agência concessora.</span><span class="sxs-lookup"><span data-stu-id="873ba-111">The **Grantor agency** column of the inquiry shows the grant customer or, for a pass-through grant, the grantor agency.</span></span> <span data-ttu-id="873ba-112">Para uma concessão pass-through, a coluna **Agência pass-through** mostra o cliente da concessão.</span><span class="sxs-lookup"><span data-stu-id="873ba-112">For a pass-through grant, the **Pass-through agency** column shows the grant customer.</span></span> <span data-ttu-id="873ba-113">Se a concessão não for uma concessão pass-through, a coluna **Agência pass-through** está em branco.</span><span class="sxs-lookup"><span data-stu-id="873ba-113">If the grant isn't a pass-through grant, the **Pass-through agency** column is blank.</span></span>

## <a name="set-up-the-cfda-clusters"></a><span data-ttu-id="873ba-114">Configurar os clusters CFDA</span><span class="sxs-lookup"><span data-stu-id="873ba-114">Set up the CFDA clusters</span></span>

<span data-ttu-id="873ba-115">Tem de configurar os clusters CFDA que podem ser associados aos números CFDA no inquérito da Agenda de Despesas de Prémios Federais.</span><span class="sxs-lookup"><span data-stu-id="873ba-115">You must set up the CFDA clusters that can be associated with CFDA numbers in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="873ba-116">Vá a **Gestão e contabilidade de projetos \> Configurar \> Concessões \> clusters de Catálogo de Apoio Nacional Federal**.</span><span class="sxs-lookup"><span data-stu-id="873ba-116">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance clusters**.</span></span>
2. <span data-ttu-id="873ba-117">Selecione **Novo** para criar um cluster CFDA.</span><span class="sxs-lookup"><span data-stu-id="873ba-117">Select **New** to create a CFDA cluster.</span></span>
3. <span data-ttu-id="873ba-118">Introduza o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="873ba-118">Enter the cluster name.</span></span>
4. <span data-ttu-id="873ba-119">Selecione **Guardar** para guardar as alterações.</span><span class="sxs-lookup"><span data-stu-id="873ba-119">Select **Save** to save your changes.</span></span>

## <a name="set-up-cfda-numbers"></a><span data-ttu-id="873ba-120">Configurar números CFDA</span><span class="sxs-lookup"><span data-stu-id="873ba-120">Set up CFDA numbers</span></span>

<span data-ttu-id="873ba-121">Tem de configurar os números CFDA que podem ser adicionados a concessões e incluídos no inquérito da Agenda de Despesas de Prémios Federais.</span><span class="sxs-lookup"><span data-stu-id="873ba-121">You must set up CFDA numbers that can be added to grants and included in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="873ba-122">Vá a **Gestão e contabilidade de projetos \> Configurar \> Concessões \> números de Catálogo de Apoio Nacional Federal**.</span><span class="sxs-lookup"><span data-stu-id="873ba-122">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance numbers**.</span></span>
2. <span data-ttu-id="873ba-123">Selecione **Novo** para criar um número CFDA.</span><span class="sxs-lookup"><span data-stu-id="873ba-123">Select **New** to create a CFDA number.</span></span>
3. <span data-ttu-id="873ba-124">Na coluna **Número**, introduza o número CFDA.</span><span class="sxs-lookup"><span data-stu-id="873ba-124">In the **Number** column, enter the CFDA number.</span></span>
4. <span data-ttu-id="873ba-125">Prima a tecla **Tab**.</span><span class="sxs-lookup"><span data-stu-id="873ba-125">Press the **Tab** key.</span></span>
5. <span data-ttu-id="873ba-126">Na coluna **Descrição**, introduza o título CFDA.</span><span class="sxs-lookup"><span data-stu-id="873ba-126">In the **Description** column, enter the CFDA title.</span></span>
6. <span data-ttu-id="873ba-127">Prima a tecla **Tab**.</span><span class="sxs-lookup"><span data-stu-id="873ba-127">Press the **Tab** key.</span></span>
7. <span data-ttu-id="873ba-128">Opcional: No campo **Cluster do programa**, adicione o cluster CFDA apropriado.</span><span class="sxs-lookup"><span data-stu-id="873ba-128">Optional: In the **Program cluster** field, add the appropriate CFDA cluster.</span></span>
8. <span data-ttu-id="873ba-129">Selecione **Guardar** para guardar as alterações.</span><span class="sxs-lookup"><span data-stu-id="873ba-129">Select **Save** to save your changes.</span></span>

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="873ba-130">Configurar concessões para reportar para o inquérito de Agenda de Despesas de Prémios Federais</span><span class="sxs-lookup"><span data-stu-id="873ba-130">Set up grants to report for the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="873ba-131">Vá a **Gestão e contabilidade de projetos \> Concessões \> Concessões**, e selecione uma concessão existente.</span><span class="sxs-lookup"><span data-stu-id="873ba-131">Go to **Project management and accounting \> Grants \> Grants**, and select an existing grant.</span></span>
2. <span data-ttu-id="873ba-132">No Separador Rápido **Configuração**, no campo **Catálogo de Assistência Doméstica Federal**, atribua o número CFDA.</span><span class="sxs-lookup"><span data-stu-id="873ba-132">On the **Setup** FastTab, in the **Catalog of Federal Domestic Assistance** field, assign the CFDA number.</span></span> <span data-ttu-id="873ba-133">O número do CFDA na concessão determina o cluster CFDA a reportar.</span><span class="sxs-lookup"><span data-stu-id="873ba-133">The CFDA number on the grant determines the CFDA cluster for reporting.</span></span>
3. <span data-ttu-id="873ba-134">No Separador Rápido **Informações de contacto**, insira as informações do concessor seguindo estes passos:</span><span class="sxs-lookup"><span data-stu-id="873ba-134">On **Contact information** FastTab, enter the grantor information by following these steps:</span></span>

    1. <span data-ttu-id="873ba-135">No campo **Cliente da concessão**, insira o cliente responsável pela concessão.</span><span class="sxs-lookup"><span data-stu-id="873ba-135">In the **Grant customer** field, enter the customer who is responsible for the grant.</span></span> <span data-ttu-id="873ba-136">Para uma concessão existente, estas informações podem já estar inseridas.</span><span class="sxs-lookup"><span data-stu-id="873ba-136">For an existing grant, this information might already be entered.</span></span>
    2. <span data-ttu-id="873ba-137">Indique se o cliente da concessão é o financiador.</span><span class="sxs-lookup"><span data-stu-id="873ba-137">Indicate whether the grant customer is the funder.</span></span> <span data-ttu-id="873ba-138">Se o cliente de concessão for o financiador, deixe a caixa de verificação **Pass-through** por selecionar.</span><span class="sxs-lookup"><span data-stu-id="873ba-138">If the grant customer is the funder, leave the **Pass-through** check box cleared.</span></span> <span data-ttu-id="873ba-139">Se outro cliente for o financiador, e o cliente da concessão for responsável por gastar e monitorizar o dinheiro, selecione a caixa de verificação **Pass-through**.</span><span class="sxs-lookup"><span data-stu-id="873ba-139">If another customer is the funder, and the grant customer is responsible for spending and tracking the money, select the **Pass-through** check box.</span></span>

4. <span data-ttu-id="873ba-140">Se selecionou a caixa de verificação **Pass-through** no passo anterior, no campo **Agência concessora**, insira o cliente que forneceu a concessão.</span><span class="sxs-lookup"><span data-stu-id="873ba-140">If you selected the **Pass-through** check box in the previous step, in the **Grantor agency** field, enter the customer who provided the grant.</span></span> <span data-ttu-id="873ba-141">A agência concessora e o cliente não podem ser o mesmo cliente.</span><span class="sxs-lookup"><span data-stu-id="873ba-141">The grantor agency and the grant customer can't be the same customer.</span></span>

<span data-ttu-id="873ba-142">Aqui está um exemplo de uma concessão pass-through:</span><span class="sxs-lookup"><span data-stu-id="873ba-142">Here is an example of a pass-through grant:</span></span>

<span data-ttu-id="873ba-143">O governo federal financiou um projeto de infraestrutura para um estado.</span><span class="sxs-lookup"><span data-stu-id="873ba-143">The federal government funded an infrastructure project for a state.</span></span> <span data-ttu-id="873ba-144">O governo federal deu o dinheiro ao estado para gastar.</span><span class="sxs-lookup"><span data-stu-id="873ba-144">The federal government gave the money to the state to spend.</span></span> <span data-ttu-id="873ba-145">Neste caso, o governo federal é a agência de concessão, e o estado é o cliente da concessão.</span><span class="sxs-lookup"><span data-stu-id="873ba-145">In this case, the federal government is the grantor agency, and the state is the grant customer.</span></span>

> [!NOTE] 
> <span data-ttu-id="873ba-146">Quando executar a funcionalidade pela primeira vez, os números CFDA iniciais serão introduzidos utilizando os números existentes nas concessões.</span><span class="sxs-lookup"><span data-stu-id="873ba-146">When you first turn on the feature, initial CFDA numbers will be entered by using the existing numbers on grants.</span></span>

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a><span data-ttu-id="873ba-147">Excluir concessões de relatórios SEFA com base no tipo de concessão</span><span class="sxs-lookup"><span data-stu-id="873ba-147">Exclude grants from SEFA reporting based on the grant type</span></span>

1. <span data-ttu-id="873ba-148">Vá para **Gestão e contabilidade de projetos \> Configurar \> Concessões \> Tipos de concessão**.</span><span class="sxs-lookup"><span data-stu-id="873ba-148">Go to **Project management and accounting \> Setup \> Grants \> Grant types**.</span></span>
2. <span data-ttu-id="873ba-149">No Separador Rápido **Informações predefinidas**, selecione a caixa de verificação **Excluir da Agenda de Despesas de Prémios Federais**.</span><span class="sxs-lookup"><span data-stu-id="873ba-149">On the **Default information** FastTab, select the **Exclude from Schedule of Expenditures of Federal Awards** check box.</span></span>
3. <span data-ttu-id="873ba-150">Selecione **Guardar** para guardar as alterações.</span><span class="sxs-lookup"><span data-stu-id="873ba-150">Select **Save** to save your changes.</span></span>

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="873ba-151">Execute o inquérito da Agenda de Despesas de Inquérito de Prémios Federais</span><span class="sxs-lookup"><span data-stu-id="873ba-151">Run the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="873ba-152">Vá à **Gestão e contabilidade de projetos \> Inquéritos e relatórios \> Inquérito de concessão \> Agenda de Despesas de Prémios Federais**.</span><span class="sxs-lookup"><span data-stu-id="873ba-152">Go to **Project management and accounting \> Inquiries and reports \> Grant inquiry \> Schedule of Expenditures of Federal Awards**.</span></span>
2. <span data-ttu-id="873ba-153">Na secção **Parâmetros**, siga estes passos:</span><span class="sxs-lookup"><span data-stu-id="873ba-153">In the **Parameters** section, follow these steps:</span></span>

    1. <span data-ttu-id="873ba-154">No campo **Intervalo de datas**, selecione o código para o intervalo de datas.</span><span class="sxs-lookup"><span data-stu-id="873ba-154">In the **Date interval** field, select the code for the date interval.</span></span> <span data-ttu-id="873ba-155">Alternativamente, nos campos **De data** e **Até data**, defina o intervalo de datas.</span><span class="sxs-lookup"><span data-stu-id="873ba-155">Alternatively, in the **From date** and **To date** fields, define the date interval.</span></span>
    2. <span data-ttu-id="873ba-156">Opcional: Para incluir apenas as transações faturadas como receita no inquérito, defina a opção **Incluir apenas receitas faturadas** como **Sim**.</span><span class="sxs-lookup"><span data-stu-id="873ba-156">Optional: To include only billed transactions as revenue in the inquiry, set the **Include only billed revenues** option to **Yes**.</span></span>

## <a name="columns"></a><span data-ttu-id="873ba-157">colunas</span><span class="sxs-lookup"><span data-stu-id="873ba-157">Columns</span></span>

<span data-ttu-id="873ba-158">A Agenda de Despesas de Prémios Federais inclui as seguintes colunas:</span><span class="sxs-lookup"><span data-stu-id="873ba-158">The Schedule of Expenditures of Federal Awards inquiry includes the following columns:</span></span>

- <span data-ttu-id="873ba-159">Nome do cluster do Catálogo de Assistência Nacional Federal</span><span class="sxs-lookup"><span data-stu-id="873ba-159">Catalog of Federal Domestic Assistance cluster name</span></span>
- <span data-ttu-id="873ba-160">Agência de concessão</span><span class="sxs-lookup"><span data-stu-id="873ba-160">Grantor agency</span></span>
- <span data-ttu-id="873ba-161">Agência pass-through</span><span class="sxs-lookup"><span data-stu-id="873ba-161">Pass-through agency</span></span>
- <span data-ttu-id="873ba-162">Nome da concessão</span><span class="sxs-lookup"><span data-stu-id="873ba-162">Grant name</span></span>
- <span data-ttu-id="873ba-163">ID da concessão</span><span class="sxs-lookup"><span data-stu-id="873ba-163">Grant ID</span></span>
- <span data-ttu-id="873ba-164">ID da aplicação da concessão</span><span class="sxs-lookup"><span data-stu-id="873ba-164">Grant application ID</span></span>
- <span data-ttu-id="873ba-165">Catálogo de Assistência Nacional Federal</span><span class="sxs-lookup"><span data-stu-id="873ba-165">Catalog of Federal Domestic Assistance</span></span>
- <span data-ttu-id="873ba-166">Recibos</span><span class="sxs-lookup"><span data-stu-id="873ba-166">Receipts</span></span>
- <span data-ttu-id="873ba-167">Despesas</span><span class="sxs-lookup"><span data-stu-id="873ba-167">Expenditures</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]