---
title: Atualizar atributos de plug-in para incluir novas dimensões de definição de preços
description: Este tópico fornece informações sobre a atualização de atributos de plug-in para dimensões de definição de preços.
author: Rumant
manager: kfend
ms.custom: ''
ms.date: 11/19/2018
ms.topic: article
ms.service: project-operations
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 603b0e9a10dc2fe23c9fa0fa7065bc3f500dc540
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147082"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a><span data-ttu-id="76201-103">Atualizar atributos de plug-in para incluir novas dimensões de definição de preços</span><span class="sxs-lookup"><span data-stu-id="76201-103">Update plug-in attributes to include new pricing dimensions</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

> [!NOTE]
> <span data-ttu-id="76201-104">Se não estiver a utilizar as funcionalidades de Criação de Propostas e Contratação do Project Service Automation (PSA), pode ignorar este tópico.</span><span class="sxs-lookup"><span data-stu-id="76201-104">If you are not using the Project Service Automation (PSA) Quoting and Contracting features, you can skip this topic.</span></span>

<span data-ttu-id="76201-105">Este tópico pressupõe que concluiu os procedimentos nos tópicos, [Criar campos e entidades personalizados](create-custom-fields-entities.md), [Adicionar campos personalizados às entidades de configuração de preços e transacionais](field-references.md) e [Configurar campos personalizados como dimensões de definição de preços](set-up-pricing-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="76201-105">This topic assumes that you have completed the procedures in the topics, [Create custom fields and entities](create-custom-fields-entities.md), [Add custom fields to price setup and transactional entities](field-references.md), and [Set up custom fields as pricing dimensions](set-up-pricing-dimensions.md).</span></span> <span data-ttu-id="76201-106">Se não tiver concluído esses procedimentos, volte a concluí-los e, em seguida, volte a este tópico.</span><span class="sxs-lookup"><span data-stu-id="76201-106">If you haven't completed those procedures, go back and complete them and then return to this topic.</span></span>

<span data-ttu-id="76201-107">Quando é criado um detalhe de linha de proposta na página **Linha de Proposta** para uma linha de proposta do projeto, o sistema cria duas linhas de estimativa em segundo plano -- uma linha para o lado do custo da estimativa e outra para o lado das vendas.</span><span class="sxs-lookup"><span data-stu-id="76201-107">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines in the background -- one line for the cost side of the estimate and one for sales side.</span></span> <span data-ttu-id="76201-108">É o mesmo para os itens de contrato do projeto.</span><span class="sxs-lookup"><span data-stu-id="76201-108">This is the same  for project contract lines.</span></span>

<span data-ttu-id="76201-109">Quando altera uma quantidade ou um campo no lado do custo, essa alteração é propagada para o lado das vendas.</span><span class="sxs-lookup"><span data-stu-id="76201-109">When you make a change to the quantity or a field on the cost side, that change is propagated to the sales side.</span></span> <span data-ttu-id="76201-110">Isto é possível devido aos seguintes plug-ins que devem ser registados novamente após uma alteração nas dimensões de definição de preços.</span><span class="sxs-lookup"><span data-stu-id="76201-110">This is possible because of the following plug-ins that must be re-registered after a change to pricing dimensions.</span></span>

- <span data-ttu-id="76201-111">PreOperationContractLineDetailUpdate - Updates **msdyn_orderlinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="76201-111">PreOperationContractLineDetailUpdate - Updates **msdyn_orderlinetransaction**.</span></span>
- <span data-ttu-id="76201-112">PreOperationQuoteLineDetailUpdate - Updates **msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="76201-112">PreOperationQuoteLineDetailUpdate - Updates **msdyn_quotelinetransaction**.</span></span>

<span data-ttu-id="76201-113">Os seguintes passos explicam-lhe o processo de registo dos plug-ins.</span><span class="sxs-lookup"><span data-stu-id="76201-113">The following steps walk you through the process of registering the plug-ins.</span></span>

1. <span data-ttu-id="76201-114">Abra o **PluginRegistrationTool** e ligue-se à sua instância online.</span><span class="sxs-lookup"><span data-stu-id="76201-114">Open the **PluginRegistrationTool** and connect to your online instance.</span></span>
2. <span data-ttu-id="76201-115">Clique em **Procurar** e procure o plug-in a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="76201-115">Click **Search** and search for the plug-in to be updated.</span></span>

 ![Captura de ecrã da árvore de pesquisa](media/PRT-1.png)

3. <span data-ttu-id="76201-117">Depois de o plug-in ser encontrado, selecione-o e, em seguida, clique em **Selecionar no Formulário Principal**.</span><span class="sxs-lookup"><span data-stu-id="76201-117">After the plug-in is found, select it and then click **Select on Main Form**.</span></span>

4. <span data-ttu-id="76201-118">Selecione o passo do plug-in a atualizar, clique com o botão direito do rato e, em seguida, selecione **Atualizar**.</span><span class="sxs-lookup"><span data-stu-id="76201-118">Select the step of the plug-in to be updated, right-click, and then select **Update**.</span></span>

 ![Captura de ecrã do plug-in a ser atualizado](media/PRT-2.png)
 
5. <span data-ttu-id="76201-120">Na janela de atualização, clique nas reticências (**...**) nos atributos de filtragem.</span><span class="sxs-lookup"><span data-stu-id="76201-120">In the update window, click the ellipsis (**...**) in the filtering attributes.</span></span>

 ![Captura de ecrã das informações de configuração Atualizar passo existente](media/PRT-3.png)
 
6. <span data-ttu-id="76201-122">Selecione as caixas de verificação do atributo de definição de preços.</span><span class="sxs-lookup"><span data-stu-id="76201-122">Select the pricing attribute check boxes.</span></span>

 ![Captura de ecrã que mostra a seleção da caixa de verificação para atributos de definição de preços](media/PRT-4.png)

7. <span data-ttu-id="76201-124">Clique em **OK** para fechar a página e, em seguida, selecione **Atualizar Passo**.</span><span class="sxs-lookup"><span data-stu-id="76201-124">Click **OK** to close the page and then select **Update Step**.</span></span>

 ![Captura de ecrã que mostra o botão "Atualizar Passo"](media/PRT-5.png)
 
8. <span data-ttu-id="76201-126">Repita este processo para o segundo plug-in, **PreOperationQuoteLineDetail - Update of msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="76201-126">Repeat this process for the second plug-in, **PreOperationQuoteLineDetail - Update of msdyn_quotelinetransaction**.</span></span>

9. <span data-ttu-id="76201-127">Feche o Plug-in Registration Tool.</span><span class="sxs-lookup"><span data-stu-id="76201-127">Close the plug-in registration tool.</span></span>

