---
title: Atualizar atributos de plug-in com novas dimensões de preços
description: Este tópico fornece informações sobre como atualizar atributos de plug-in para dimensões de preços.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 54b87a993929edbf89ef48741ba0a06c6c42ec4e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004635"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a><span data-ttu-id="ba642-103">Atualizar atributos de plug-in com novas dimensões de preços</span><span class="sxs-lookup"><span data-stu-id="ba642-103">Update plug-in attributes with new pricing dimensions</span></span>

<span data-ttu-id="ba642-104">Este tópico fornece informações sobre como atualizar atributos de plug-in para dimensões de preços.</span><span class="sxs-lookup"><span data-stu-id="ba642-104">This topic provides information about how to update plug-in attributes for pricing dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="ba642-105">Este tópico só é aplicável às funcionalidades de proposta e de contrato no Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="ba642-105">This topic is only applicable to the quote and contract features in Dynamics 365 Project Operations.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ba642-106">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="ba642-106">Prerequisites</span></span>
<span data-ttu-id="ba642-107">Antes de completar os passos deste tópico, deve ter concluído os procedimentos nos seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="ba642-107">Before you complete the steps in this topic, you must have completed the procedures in the following topics:</span></span>

  - [<span data-ttu-id="ba642-108">Criar campos e entidades personalizados</span><span class="sxs-lookup"><span data-stu-id="ba642-108">Create custom fields and entities</span></span>](create-custom-fields-entities-pricing-dimensions.md) 
  - [<span data-ttu-id="ba642-109">Adicionar campos personalizados às entidades de configuração de preços e transacionais</span><span class="sxs-lookup"><span data-stu-id="ba642-109">Add custom fields to price setup and transactional entities</span></span>](add-custom-fields-price-setup-transactional-entities.md)
  - <span data-ttu-id="ba642-110">[Configurar campos personalizados como dimensões de preços](set-up-custom-fields-pricing-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="ba642-110">[Set up custom fields as pricing dimensions](set-up-custom-fields-pricing-dimensions.md).</span></span> 
  
<span data-ttu-id="ba642-111">Se não tiver concluído esses procedimentos, conclua-os e, em seguida, volte a este tópico.</span><span class="sxs-lookup"><span data-stu-id="ba642-111">If you haven't completed those procedures, complete them and then return to this topic.</span></span>

## <a name="register-a-plug-in"></a><span data-ttu-id="ba642-112">Registar um plug-in</span><span class="sxs-lookup"><span data-stu-id="ba642-112">Register a plug-in</span></span>
<span data-ttu-id="ba642-113">Quando um detalhe da linha de proposta é criado na página **Linha de proposta** para uma linha de proposta do projeto, o sistema cria duas linhas de estimativa.</span><span class="sxs-lookup"><span data-stu-id="ba642-113">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines.</span></span> <span data-ttu-id="ba642-114">Uma linha é para o lado do custo da estimativa e a outra linha é para o lado das vendas.</span><span class="sxs-lookup"><span data-stu-id="ba642-114">One line is for the cost side of the estimate and the other line is for sales the side.</span></span> <span data-ttu-id="ba642-115">É o mesmo para os itens de contrato do projeto.</span><span class="sxs-lookup"><span data-stu-id="ba642-115">This is the same  for project contract lines.</span></span>

<span data-ttu-id="ba642-116">Quando altera uma quantidade ou um campo no lado do custo, essa alteração é também efetuada no lado das vendas.</span><span class="sxs-lookup"><span data-stu-id="ba642-116">When you make a change to the quantity or a field on the cost side, that change is also made on the sales side.</span></span> <span data-ttu-id="ba642-117">Isto é possível porque os plug-ins PreOperation na Quotelinedetail e as entidades de detalhes do item de contrato ligam atributos específicos do lado do custo ao lado das vendas da transação.</span><span class="sxs-lookup"><span data-stu-id="ba642-117">This is possible because the PreOperation plug-ins on Quotelinedetail and contractline detail entities connect specific attributes on the cost side to the sales side of the transaction.</span></span> <span data-ttu-id="ba642-118">Se necessitar de alterar os valores de dimensão dos preços do lado das vendas, a fim de ser feita também do lado dos custos, os seguintes plug-ins devem ser registados novamente após a alteração de uma dimensão de preços.</span><span class="sxs-lookup"><span data-stu-id="ba642-118">If you need changes made to the pricing dimension values on the sales side to also be made on the cost side, the following plug-ins must be re-registered after making changes to a pricing dimension.</span></span>

<span data-ttu-id="ba642-119">Estes são os plug-ins a atualizar e a registar novamente:</span><span class="sxs-lookup"><span data-stu-id="ba642-119">These are the plug-ins to update and re-register:</span></span>

- <span data-ttu-id="ba642-120">PreOperationContractLineDetailUpdate – **Atualizar msdyn_orderlinetransaction**</span><span class="sxs-lookup"><span data-stu-id="ba642-120">PreOperationContractLineDetailUpdate - **Update msdyn_orderlinetransaction**</span></span>
- <span data-ttu-id="ba642-121">PreOperationQuoteLineDetailUpdate – **Atualiza msdyn_quotelinetransaction**</span><span class="sxs-lookup"><span data-stu-id="ba642-121">PreOperationQuoteLineDetailUpdate - **Updates msdyn_quotelinetransaction**</span></span>

<span data-ttu-id="ba642-122">Preencha os seguintes passos para atualizar e voltar a registar os plug-ins.</span><span class="sxs-lookup"><span data-stu-id="ba642-122">Complete the following steps to update and re-register the plug-ins.</span></span>

1. <span data-ttu-id="ba642-123">Abra **PluginRegistrationTool** e ligue-se ao ambiente do Dataverse do Project Operations.</span><span class="sxs-lookup"><span data-stu-id="ba642-123">Open **PluginRegistrationTool** and connect to your Project Operations Dataverse environment.</span></span>
2. <span data-ttu-id="ba642-124">Selecione **Pesquisar** e digite as primeiras letras do plug-in a atualizar.</span><span class="sxs-lookup"><span data-stu-id="ba642-124">Select **Search**, and type in the first few letters of the plug-in to be updated.</span></span>
3. <span data-ttu-id="ba642-125">Depois do plug-in ser encontrado, selecione-o e, em seguida, selecione **Selecionar no Formulário Principal**.</span><span class="sxs-lookup"><span data-stu-id="ba642-125">After the plug-in is found, select it, and then select **Select on Main Form**.</span></span>
4. <span data-ttu-id="ba642-126">Selecione o passo **Atualizar msdyn_orderlinetransaction**, clique com o botão direito do rato e, em seguida, selecione **Atualizar**.</span><span class="sxs-lookup"><span data-stu-id="ba642-126">Select the **Update msdyn_orderlinetransaction** step, right-click, and then select **Update**.</span></span>
5. <span data-ttu-id="ba642-127">Na página de diálogo **Atualizar**, selecione as reticências (**...**) nos atributos de filtragem.</span><span class="sxs-lookup"><span data-stu-id="ba642-127">In the **Update** dialog page, select the ellipsis (**...**) in the filtering attributes.</span></span>
6. <span data-ttu-id="ba642-128">A janela de atributos de filtragem abre-se e fornece uma lista de todos os atributos na entidade e nas dimensões dos preços.</span><span class="sxs-lookup"><span data-stu-id="ba642-128">The filtering attributes window opens and provides a list of all attributes in the entity and the pricing dimensions.</span></span> <span data-ttu-id="ba642-129">Selecione as caixas de verificação para os atributos da dimensão dos preços.</span><span class="sxs-lookup"><span data-stu-id="ba642-129">Select the check boxes for the pricing dimension attributes.</span></span>
7. <span data-ttu-id="ba642-130">Selecione **OK** para fechar a página e, em seguida, selecione **Atualizar Passo**.</span><span class="sxs-lookup"><span data-stu-id="ba642-130">Select **OK** to close the page, and then select **Update Step**.</span></span>
8. <span data-ttu-id="ba642-131">Repita os passos 2-7 para o segundo plug-in, **PreOperationQuoteLineDetail**.</span><span class="sxs-lookup"><span data-stu-id="ba642-131">Repeat steps 2-7 for the second plug-in, **PreOperationQuoteLineDetail**.</span></span> <span data-ttu-id="ba642-132">Para este plug-in, precisa de atualizar o passo **Atualizar msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="ba642-132">For this plug-in, you need to update the **Update of msdyn_quotelinetransaction** step.</span></span>
9. <span data-ttu-id="ba642-133">Feche **PluginRegistrationTool**.</span><span class="sxs-lookup"><span data-stu-id="ba642-133">Close **PluginRegistrationTool**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]