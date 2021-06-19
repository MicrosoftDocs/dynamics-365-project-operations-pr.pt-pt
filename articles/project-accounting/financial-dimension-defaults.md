---
title: Dimensão financeira predefinida
description: Este tópico fornece informações sobre como configurar predefinições de dimensão financeira.
author: sigitac
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d2509f74d34ac3dce4c6915ca860283750eb50b1
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013320"
---
# <a name="financial-dimension-defaults"></a><span data-ttu-id="a5b4c-103">Dimensão financeira predefinida</span><span class="sxs-lookup"><span data-stu-id="a5b4c-103">Financial dimension defaults</span></span>

<span data-ttu-id="a5b4c-104">_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_</span><span class="sxs-lookup"><span data-stu-id="a5b4c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="a5b4c-105">O Dynamics 365 Project Operations utiliza a estrutura de [Dimensões financeiras](/dynamics365/finance/general-ledger/financial-dimensions) no Dynamics 365 Finance para fornecer informações adicionais sobre as transações do sub-livro razão e livro razão geral.</span><span class="sxs-lookup"><span data-stu-id="a5b4c-105">Dynamics 365 Project Operations uses the [Financial dimensions](/dynamics365/finance/general-ledger/financial-dimensions) framework in Dynamics 365 Finance to provide additional insights on project subledger and general ledger transactions.</span></span>

<span data-ttu-id="a5b4c-106">As dimensões financeiras predefinidas podem ser definidas num cliente, fonte de financiamento de projetos, marco, item de contrato de projeto ou projeto.</span><span class="sxs-lookup"><span data-stu-id="a5b4c-106">Default financial dimensions can be set on a customer, project funding source, milestone, project contract line, or project.</span></span>

## <a name="define-default-financial-dimensions-for-a-customer"></a><span data-ttu-id="a5b4c-107">Predefinir dimensões financeiras para um cliente</span><span class="sxs-lookup"><span data-stu-id="a5b4c-107">Define default financial dimensions for a customer</span></span>

<span data-ttu-id="a5b4c-108">As predefinições da dimensão do cliente são especificados no Finance.</span><span class="sxs-lookup"><span data-stu-id="a5b4c-108">Customer dimension defaults are specified in Finance.</span></span> <span data-ttu-id="a5b4c-109">Conclua os seguintes passos para predefinir a dimensão.</span><span class="sxs-lookup"><span data-stu-id="a5b4c-109">Complete the following steps to set dimension defaults.</span></span>

1. <span data-ttu-id="a5b4c-110">Vá a **Contas a receber** > **Clientes** > **Todos os clientes**.</span><span class="sxs-lookup"><span data-stu-id="a5b4c-110">Go to **Accounts receivable** > **Customers** > **All customers**.</span></span>
2. <span data-ttu-id="a5b4c-111">Na página **Clientes**, no separador **Dimensões financeiras**, defina os valores de dimensão financeira para o cliente específico.</span><span class="sxs-lookup"><span data-stu-id="a5b4c-111">On the **Customers** page, on the **Financial dimensions** tab, set the financial dimension values for specific customer.</span></span>

## <a name="define-default-financial-dimensions-for-project-contracts"></a><span data-ttu-id="a5b4c-112">Predefinir dimensões financeiras para contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="a5b4c-112">Define default financial dimensions for project contracts</span></span>

<span data-ttu-id="a5b4c-113">Os contratos de projeto são criados e mantidos no Common Data Service (CDS).</span><span class="sxs-lookup"><span data-stu-id="a5b4c-113">Project contracts are created and maintained in Common Data Service (CDS).</span></span> <span data-ttu-id="a5b4c-114">Os atributos contabilísticos para os contratos de projeto são definidos no módulo **Gestão de projetos e contabilística** no Finance.</span><span class="sxs-lookup"><span data-stu-id="a5b4c-114">Accounting attributes for project contracts are set in the **Project management and accounting** module in Finance.</span></span>

### <a name="set-financial-dimensions-for-a-project-funding-source"></a><span data-ttu-id="a5b4c-115">Definir dimensões financeiras para uma fonte de financiamento de projetos</span><span class="sxs-lookup"><span data-stu-id="a5b4c-115">Set financial dimensions for a project funding source</span></span>

1. <span data-ttu-id="a5b4c-116">Vá a **Gestão de projetos e contabilística** > **Projetos** > **Contratos de Projeto**.</span><span class="sxs-lookup"><span data-stu-id="a5b4c-116">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="a5b4c-117">Selecione o registo que pretende atualizar e, no separador **Contrato do projeto**, selecione **Mostrar contabilidade predefinida**.</span><span class="sxs-lookup"><span data-stu-id="a5b4c-117">Select the record you want to update, and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="a5b4c-118">Expanda **Informações relacionadas** e selecione o separador **Fontes de financiamento**.</span><span class="sxs-lookup"><span data-stu-id="a5b4c-118">Expand **Related information** and select the **Funding sources** tab.</span></span>
4. <span data-ttu-id="a5b4c-119">Defina as predefinições da dimensão financeira.</span><span class="sxs-lookup"><span data-stu-id="a5b4c-119">Set the financial dimension defaults.</span></span> <span data-ttu-id="a5b4c-120">Note que as dimensões financeiras assumem a predefinição da conta do cliente.</span><span class="sxs-lookup"><span data-stu-id="a5b4c-120">Notice that the financial dimensions default from the customer account.</span></span>

### <a name="set-financial-dimensions-for-a-project-contract-line"></a><span data-ttu-id="a5b4c-121">Definir dimensões financeiras para um item de contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="a5b4c-121">Set financial dimensions for a project contract line</span></span>

1. <span data-ttu-id="a5b4c-122">Vá a **Gestão de projetos e contabilística** > **Projetos** > **Contratos de Projeto**.</span><span class="sxs-lookup"><span data-stu-id="a5b4c-122">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="a5b4c-123">Selecione o registo que pretende atualizar e, no separador **Contrato do projeto**, selecione **Mostrar contabilidade predefinida**.</span><span class="sxs-lookup"><span data-stu-id="a5b4c-123">Select the record you want to update and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="a5b4c-124">Expanda **Informações relacionadas** e selecione o separador **Itens de contrato**.</span><span class="sxs-lookup"><span data-stu-id="a5b4c-124">Expand **Related information** and select the **Contract lines** tab.</span></span>
4. <span data-ttu-id="a5b4c-125">Defina as predefinições da dimensão financeira.</span><span class="sxs-lookup"><span data-stu-id="a5b4c-125">Set the financial dimension defaults.</span></span> <span data-ttu-id="a5b4c-126">As predefinições da dimensão financeira são aplicáveis e só podem ser utilizadas com itens de contrato de Preço fixo (marco).</span><span class="sxs-lookup"><span data-stu-id="a5b4c-126">The financial dimension defaults are applicable and can be used only with Fixed price (milestone) contract lines.</span></span>

<span data-ttu-id="a5b4c-127">Estas predefinições são utilizadas em transações em conta de projetos relacionados e linhas de fatura.</span><span class="sxs-lookup"><span data-stu-id="a5b4c-127">These defaults are used on related project on-account transactions and invoice lines.</span></span>

## <a name="define-default-financial-dimensions-for-projects"></a><span data-ttu-id="a5b4c-128">Predefinir dimensões financeiras para projetos</span><span class="sxs-lookup"><span data-stu-id="a5b4c-128">Define default financial dimensions for projects</span></span>

<span data-ttu-id="a5b4c-129">Os projetos são criados e mantidos no CDS.</span><span class="sxs-lookup"><span data-stu-id="a5b4c-129">Projects are created and maintained in CDS.</span></span> <span data-ttu-id="a5b4c-130">Os atributos contabilísticos para os projetos são definidos no módulo **Gestão de projetos e contabilidade** no Finance.</span><span class="sxs-lookup"><span data-stu-id="a5b4c-130">Accounting attributes for projects are set in the **Project management and accounting** module in Finance.</span></span>

1. <span data-ttu-id="a5b4c-131">Vá para **Gestão de projetos e contabilística** > **Projetos** > **Todos os projetos**.</span><span class="sxs-lookup"><span data-stu-id="a5b4c-131">Go to **Project management and accounting** > **Projects** > **All projects**.</span></span>
2. <span data-ttu-id="a5b4c-132">Selecione o registo que pretende atualizar e, no separador **Projeto**, selecione **Mostrar contabilidade predefinida**.</span><span class="sxs-lookup"><span data-stu-id="a5b4c-132">Select the record that you want to update and on the **Project** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="a5b4c-133">Expanda **Informações relacionadas** e selecione o separador **Configurar**.</span><span class="sxs-lookup"><span data-stu-id="a5b4c-133">Expand **Related information** and select the **Setup** tab.</span></span>
4. <span data-ttu-id="a5b4c-134">Defina as predefinições da dimensão financeira.</span><span class="sxs-lookup"><span data-stu-id="a5b4c-134">Set the financial dimension defaults.</span></span> <span data-ttu-id="a5b4c-135">Note que as dimensões financeiras assumem a predefinição da conta do cliente.</span><span class="sxs-lookup"><span data-stu-id="a5b4c-135">Notice that financial dimensions default from the customer account.</span></span> <span data-ttu-id="a5b4c-136">Se o projeto estiver associado a um item de contrato com vários clientes de contratos de projeto, o cliente principal é utilizado para predefinir dimensões financeiras.</span><span class="sxs-lookup"><span data-stu-id="a5b4c-136">If the project is associated with a contract line with multiple project contract customers, the primary customer is used to default financial dimensions.</span></span>

<span data-ttu-id="a5b4c-137">As dimensões financeiras predefinidas do projeto são usadas para predefinir linhas de diário para tempo, despesas e transações de taxas no **Diário de Integração do Project Operations** e em linhas de fatura de projeto relacionadas.</span><span class="sxs-lookup"><span data-stu-id="a5b4c-137">Project default financial dimensions are used to set journal line defaults for time, expense, and fee transactions in the **Project Operations Integration Journal** and on related project invoice lines.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]