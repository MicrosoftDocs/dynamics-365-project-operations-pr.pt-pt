---
title: Criar e aplicar os termos de retenção de pagamento do fornecedor
description: Este tópico fornece informações sobre como configurar e manter termos de retenção para pagamentos a fornecedores.
author: Yowelle
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 09bb30f55ee8e1f24634e9d8b7dea95bd3dbd24f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006344"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a><span data-ttu-id="c91b2-103">Criar e aplicar os termos de retenção de pagamento do fornecedor</span><span class="sxs-lookup"><span data-stu-id="c91b2-103">Create and apply vendor payment retention terms</span></span>

[!include [banner](../includes/banner.md)] 

<span data-ttu-id="c91b2-104">A configuração dos termos de retenção de pagamento a fornecedores para um projeto é útil quando a sua organização quer reter parte dos pagamentos feitos a um fornecedor.</span><span class="sxs-lookup"><span data-stu-id="c91b2-104">Setting up vendor payment retention terms for a project is useful when your organization wants to retain part of the payments made to a vendor.</span></span> <span data-ttu-id="c91b2-105">Por exemplo, quando pretender reter o pagamento a um fornecedor até que os produtos entregues correspondam às suas expetativas.</span><span class="sxs-lookup"><span data-stu-id="c91b2-105">For example, when you want to hold payment to a vendor until the products delivered meet your expectations.</span></span> <span data-ttu-id="c91b2-106">As condições de retenção de pagamento do fornecedor podem ser especificadas quando negoceia um contrato de fornecedor.</span><span class="sxs-lookup"><span data-stu-id="c91b2-106">Vendor payment retention terms can be specified when you negotiate a vendor contract.</span></span>

## <a name="create-vendor-payment-retention-terms"></a><span data-ttu-id="c91b2-107">Criar os termos de retenção de pagamento do fornecedor</span><span class="sxs-lookup"><span data-stu-id="c91b2-107">Create vendor payment retention terms</span></span>

<span data-ttu-id="c91b2-108">Pode introduzir a percentagem de pagamento do fornecedor pela retenção e a percentagem dos montantes anteriormente retidos a serem libertados.</span><span class="sxs-lookup"><span data-stu-id="c91b2-108">You can enter the percentage of vendor payment for retention and the percentage of the previously retained amounts to be released.</span></span> <span data-ttu-id="c91b2-109">Os valores são automaticamente retidos nas faturas do fornecedor até que o contrato atinja o estado de conclusão especificado.</span><span class="sxs-lookup"><span data-stu-id="c91b2-109">Amounts are automatically retained on vendor invoices until the contract reaches the specified state of completion.</span></span> <span data-ttu-id="c91b2-110">Depois de configurar os termos de retenção, pode aplicá-los a qualquer projeto para esse fornecedor.</span><span class="sxs-lookup"><span data-stu-id="c91b2-110">After you set up the retention terms, you can apply them to any project for that vendor.</span></span>

<span data-ttu-id="c91b2-111">Utilize os seguintes passos para configurar e manter termos de retenção para os pagamentos do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="c91b2-111">Use the following steps to set up and maintain retention terms for vendor payments.</span></span> 

1. <span data-ttu-id="c91b2-112">Aceda a **Gestão de projetos e contabilística** > **Retenção** > **Termos de retenção de pagamento do fornecedor**.</span><span class="sxs-lookup"><span data-stu-id="c91b2-112">Go to **Project management and accounting** > **Retention** > **Vendor payment retention terms**.</span></span>
2. <span data-ttu-id="c91b2-113">Selecione **Novo** para adicionar um novo termo de retenção do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="c91b2-113">Select **New** to add a new vendor retention term.</span></span> <span data-ttu-id="c91b2-114">O valor **ID da Regra** para o novo termo é automaticamente introduzido.</span><span class="sxs-lookup"><span data-stu-id="c91b2-114">The **Rule ID** value for the new term is automatically entered.</span></span> 
3. <span data-ttu-id="c91b2-115">Introduza uma breve descrição no campo **Descrição** e, no Separador Rápido **Termos**, selecione **Adicionar linha** para introduzir valores de prazo para os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="c91b2-115">Enter a brief description in the **Description** field, and on the **Terms** FastTab, select **Add line** to enter term values for the following:</span></span>

   - <span data-ttu-id="c91b2-116">**Percentagem de unidades entregues**: Insira uma percentagem de conclusão para o termo.</span><span class="sxs-lookup"><span data-stu-id="c91b2-116">**Percentage of units delivered**: Enter a percentage of completion for the term.</span></span> <span data-ttu-id="c91b2-117">Os valores são automaticamente retidos nas faturas do fornecedor até que a fase de conclusão do projeto seja igual à percentagem especificada.</span><span class="sxs-lookup"><span data-stu-id="c91b2-117">Amounts are automatically retained on vendor invoices until the project stage of completion is equal to the specified percentage.</span></span> <span data-ttu-id="c91b2-118">Por exemplo, se introduzir 50,00, os valores são retidos até que o projeto esteja 50 por cento concluído.</span><span class="sxs-lookup"><span data-stu-id="c91b2-118">For example, if you enter 50.00, amounts are retained until the project is 50 percent completed.</span></span>
   - <span data-ttu-id="c91b2-119">**Percentagem a reter**: Introduza uma percentagem do valor da fatura do fornecedor a reter.</span><span class="sxs-lookup"><span data-stu-id="c91b2-119">**Percentage to retain**: Enter a percentage of the vendor invoice amount to be retained.</span></span> <span data-ttu-id="c91b2-120">Por exemplo, se introduzir 10,00, então 10 por cento do valor numa fatura de fornecedor é mantido até que o projeto atinja a percentagem de conclusão tal como definido no campo **Percentagem de unidades entregues**.</span><span class="sxs-lookup"><span data-stu-id="c91b2-120">For example, if you enter 10.00, then 10 percent of the amount on a vendor invoice is retained until the project reaches the percentage of completion as set in the **Percentage of units delivered field**.</span></span>
   - <span data-ttu-id="c91b2-121">**Percentagem a libertar**: Selecione **Adicionar linha** para introduzir uma percentagem de quaisquer montantes previamente retidos a serem libertados para o nível de conclusão do projeto selecionado.</span><span class="sxs-lookup"><span data-stu-id="c91b2-121">**Percentage to release**: Select **Add line** to enter a percentage of any previously retained amounts to be released for the selected level of project completion.</span></span>

> [!NOTE]
> <span data-ttu-id="c91b2-122">Se tiver mais de um marco para diferentes níveis de conclusão do projeto, insira uma linha de fim de tempo de retenção separada para cada regra de retenção.</span><span class="sxs-lookup"><span data-stu-id="c91b2-122">If you have more than one milestone for different levels of project completion, enter a separate vendor retention term line for each retention rule.</span></span> <span data-ttu-id="c91b2-123">Cada linha pode especificar uma percentagem de retenção diferente e uma percentagem de libertação diferente para cada nível de conclusão do projeto designado.</span><span class="sxs-lookup"><span data-stu-id="c91b2-123">Each line can specify a different retention percentage and a different release percentage for each designated level of project completion.</span></span>

<span data-ttu-id="c91b2-124">Depois de criar termos de retenção do fornecedor para um fornecedor, pode aplicá-los aos termos de um projeto.</span><span class="sxs-lookup"><span data-stu-id="c91b2-124">After you create vendor retention terms for a vendor, you can apply the terms to a project.</span></span>

## <a name="apply-vendor-retention-terms-to-a-project"></a><span data-ttu-id="c91b2-125">Aplicar termos de retenção de fornecedor a um projeto</span><span class="sxs-lookup"><span data-stu-id="c91b2-125">Apply vendor retention terms to a project</span></span>

1. <span data-ttu-id="c91b2-126">Vá a **Gestão de projetos e contabilística** > **Projetos** > **Todos os projetos** e abra um projeto a partir da página da lista de projetos.</span><span class="sxs-lookup"><span data-stu-id="c91b2-126">Go to **Project management and accounting** > **Projects** > **All projects** and open a project from the project list page.</span></span>
2. <span data-ttu-id="c91b2-127">No Separador Rápido **Contratos de fornecedor**, selecione **Adicionar linha**.</span><span class="sxs-lookup"><span data-stu-id="c91b2-127">On the **Vendor agreements** FastTab, select **Add line**.</span></span>
3. <span data-ttu-id="c91b2-128">No campo **Código da conta**, selecione uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="c91b2-128">In the **Account code field**, select one of the following options:</span></span> 

   - <span data-ttu-id="c91b2-129">**Tabela**: Os termos de retenção do fornecedor aplicam-se a um único fornecedor.</span><span class="sxs-lookup"><span data-stu-id="c91b2-129">**Table**: The vendor retention terms apply to a single vendor.</span></span>
   - <span data-ttu-id="c91b2-130">**Grupo**: Os termos de retenção do fornecedor aplicam-se a todos os fornecedores de um grupo de fornecedores.</span><span class="sxs-lookup"><span data-stu-id="c91b2-130">**Group**: The vendor retention terms apply to all vendors in a vendor group.</span></span>
   - <span data-ttu-id="c91b2-131">**Todos**: Os termos de retenção do fornecedor aplicam-se a todos os fornecedores.</span><span class="sxs-lookup"><span data-stu-id="c91b2-131">**All**: The vendor retention terms apply to all vendors.</span></span>

4. <span data-ttu-id="c91b2-132">No campo **Fornecedor/Grupo de Fornecedores**, selecione o fornecedor ou grupo de fornecedores ao qual se aplicam os termos de retenção do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="c91b2-132">In the **Vendor/Vendor group field**, select the vendor or vendor group to which the vendor retention terms apply.</span></span> <span data-ttu-id="c91b2-133">Se selecionou **Todos** no passo anterior, este campo não está disponível.</span><span class="sxs-lookup"><span data-stu-id="c91b2-133">If you selected **All** in the previous step, this field is unavailable.</span></span>
5. <span data-ttu-id="c91b2-134">No campo **Termos de retenção do fornecedor**, selecione os termos de retenção que criou no procedimento anterior.</span><span class="sxs-lookup"><span data-stu-id="c91b2-134">In the **Vendor retention terms** field, select the retention terms that you created in the previous procedure.</span></span>
6. <span data-ttu-id="c91b2-135">Se o projeto também tiver termos paga quando pago (PWP) criados para o fornecedor, insira a percentagem de limiar para o projeto no campo **Percentagem de limiar PWP**.</span><span class="sxs-lookup"><span data-stu-id="c91b2-135">If the project also has pay-when-paid (PWP) terms set up for the vendor, enter the threshold percentage for the project in the **PWP threshold percentage** field.</span></span>

<span data-ttu-id="c91b2-136">Os termos de retenção do fornecedor também são apresentados em notas de encomenda que cria para o fornecedor.</span><span class="sxs-lookup"><span data-stu-id="c91b2-136">The vendor retention terms are also displayed on purchase orders that you create for the vendor.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]