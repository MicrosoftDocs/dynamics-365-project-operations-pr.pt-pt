---
title: Configurar definições de parâmetros adicionais
description: Como configurar definições de parâmetros adicionais no Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: de2fe830-4313-4711-b03b-76d56bf56cb6
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: f3e110163088f8e3b78da9f273113d74775bf24c
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754629"
---
# <a name="configure-additional-parameter-settings-project-service"></a><span data-ttu-id="f231b-103">Configurar definições de parâmetros adicionais (Project Service)</span><span class="sxs-lookup"><span data-stu-id="f231b-103">Configure additional parameter settings (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="f231b-104">Depois de configurar os itens nos tópicos anteriores, terá de definir parâmetros do projeto adicionais para utilizar nos seus projetos.</span><span class="sxs-lookup"><span data-stu-id="f231b-104">Once you’ve configured the items in previous topics, you need to set additional project parameters to use for your projects.</span></span> <span data-ttu-id="f231b-105">Quando o [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] foi instalado pela primeira vez, criou uma definição de parâmetros para criar todos os registos necessários para o [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] funcionar.</span><span class="sxs-lookup"><span data-stu-id="f231b-105">When you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you created a parameters setting to first create all the records required for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to work.</span></span> <span data-ttu-id="f231b-106">Agora é o momento de voltar atrás e configurar os campos adicionais para estas definições.</span><span class="sxs-lookup"><span data-stu-id="f231b-106">Now it’s time to go back and configure additional fields for these settings.</span></span>  
  
 <span data-ttu-id="f231b-107">Terá de ter configurado as seguintes definições:</span><span class="sxs-lookup"><span data-stu-id="f231b-107">You’ll need to have configured the following settings:</span></span>  
  
-   <span data-ttu-id="f231b-108">Unidade organizacional</span><span class="sxs-lookup"><span data-stu-id="f231b-108">Organizational unit</span></span>  
  
-   <span data-ttu-id="f231b-109">Frequência da Fatura</span><span class="sxs-lookup"><span data-stu-id="f231b-109">Invoice frequency</span></span>  
  
-   <span data-ttu-id="f231b-110">Modelo de horas de trabalho</span><span class="sxs-lookup"><span data-stu-id="f231b-110">Work hours template</span></span>  
  
-   <span data-ttu-id="f231b-111">Lista de preços</span><span class="sxs-lookup"><span data-stu-id="f231b-111">Price list</span></span>  
 
<span data-ttu-id="f231b-112">Neste passo, indique também o tipo de alocação de recursos pretende:</span><span class="sxs-lookup"><span data-stu-id="f231b-112">In this step, you’ll also indicate what type of resource allocation you want:</span></span>  
  
- <span data-ttu-id="f231b-113">**Central**.</span><span class="sxs-lookup"><span data-stu-id="f231b-113">**Central**.</span></span> <span data-ttu-id="f231b-114">Só os gestores de recursos podem alocar recursos a projetos.</span><span class="sxs-lookup"><span data-stu-id="f231b-114">Only resource managers can allocate resources to projects.</span></span>  
  
- <span data-ttu-id="f231b-115">**Híbrido**.</span><span class="sxs-lookup"><span data-stu-id="f231b-115">**Hybrid**.</span></span> <span data-ttu-id="f231b-116">Os gestores de recursos, os gestores de projetos e os gestores de contas podem alocar recursos a projetos.</span><span class="sxs-lookup"><span data-stu-id="f231b-116">Resource managers, project managers, and account managers can allocate resources to projects.</span></span>  
  
 
<span data-ttu-id="f231b-117">Para definir os parâmetros do projeto:</span><span class="sxs-lookup"><span data-stu-id="f231b-117">To set project parameters:</span></span>  
  
1. <span data-ttu-id="f231b-118">Vá para **Project Service > Parâmetros**.</span><span class="sxs-lookup"><span data-stu-id="f231b-118">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="f231b-119">Clique na definição de parâmetros que pretende configurar (a que criou quando instalou o [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] pela primeira vez) ou clique em **Novo** para criar um novo.</span><span class="sxs-lookup"><span data-stu-id="f231b-119">Click the parameters setting you want to configure (the one you created when you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), or click **New** to create a new one.</span></span>  
  
3. <span data-ttu-id="f231b-120">Na área **Geral**, defina todas as opções para os parâmetros do projeto.</span><span class="sxs-lookup"><span data-stu-id="f231b-120">In the **General** area, set all the options for your project parameters.</span></span>  
  
4. <span data-ttu-id="f231b-121">Na área **Lista de Preços**, clique em **+** para adicionar uma lista de preços, selecione uma lista de preços na lista pendente **Lista de Preços do Parâmetro do Projeto** e clique em **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="f231b-121">In the **Price List** area, click **+** to add a price list, select a price list in the **Project Parameter Price List** drop-down list, and then click **Save**.</span></span>  
  
5. <span data-ttu-id="f231b-122">Clique no botão **Guardar** no canto inferior direito do ecrã.</span><span class="sxs-lookup"><span data-stu-id="f231b-122">Click the **Save** button in the bottom right corner of the screen.</span></span>  

> [!NOTE]
> <span data-ttu-id="f231b-123">O registo de parâmetro do projeto tem de ser mantido para que o Project Service funcione corretamente.</span><span class="sxs-lookup"><span data-stu-id="f231b-123">The project parameter record must be maintained for Project Service to function correcly.</span></span> <span data-ttu-id="f231b-124">Este registo não deve ser eliminado.</span><span class="sxs-lookup"><span data-stu-id="f231b-124">This record should not be deleted.</span></span>

### <a name="see-also"></a><span data-ttu-id="f231b-125">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="f231b-125">See Also</span></span>  
 [<span data-ttu-id="f231b-126">Configurar recursos</span><span class="sxs-lookup"><span data-stu-id="f231b-126">Set up resources</span></span>](../project-service/set-up-resources.md)
