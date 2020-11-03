---
title: Configurar a integração do Project Operations por entidade legal
description: Este tópico fornece informações sobre como configurar integração por entidade legal no Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: c0e02ef2d17bf49209369f7adad681d9a5981e2a
ms.sourcegitcommit: 91ad491e94a421f256a378b0f4b26ed48c67bc93
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/22/2020
ms.locfileid: "4096766"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a><span data-ttu-id="9c6d8-103">Configurar a integração do Project Operations por entidade legal</span><span class="sxs-lookup"><span data-stu-id="9c6d8-103">Configure Project Operations integration per legal entity</span></span> 

<span data-ttu-id="9c6d8-104">_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_</span><span class="sxs-lookup"><span data-stu-id="9c6d8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="9c6d8-105">Este tópico percorre os passos necessários para configurar o Dynamics 365 Project Operations por entidade legal.</span><span class="sxs-lookup"><span data-stu-id="9c6d8-105">This topic walks you through the steps required to configure Dynamics 365 Project Operations per legal entity.</span></span>

## <a name="enable-feature-keys-in-dynamics-365-finance"></a><span data-ttu-id="9c6d8-106">Ativar chaves de funcionalidades no Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="9c6d8-106">Enable feature keys in Dynamics 365 Finance</span></span>

<span data-ttu-id="9c6d8-107">Complete os seguintes passos para ativar as funcionalidades necessárias.</span><span class="sxs-lookup"><span data-stu-id="9c6d8-107">Complete the following steps to enable required features.</span></span>

1. <span data-ttu-id="9c6d8-108">No Dynamics 365 Finance, vá para a área de trabalho **Gestão de Funcionalidades**.</span><span class="sxs-lookup"><span data-stu-id="9c6d8-108">In Dynamics 365 Finance, go to the **Feature Management** workspace.</span></span>
2. <span data-ttu-id="9c6d8-109">Na **Lista de funcionalidades** , encontre e ative as seguintes funcionalidades:</span><span class="sxs-lookup"><span data-stu-id="9c6d8-109">In **Feature list** , find and enable the following features:</span></span>
  
    - <span data-ttu-id="9c6d8-110">**Ativar vários itens de contrato para um projeto**</span><span class="sxs-lookup"><span data-stu-id="9c6d8-110">**Enable multiple contract lines for a project**</span></span>
    - <span data-ttu-id="9c6d8-111">**Ativar o Project Operations no Dynamics 365 Customer Engagement**</span><span class="sxs-lookup"><span data-stu-id="9c6d8-111">**Enable Project Operations on Dynamics 365 Customer Engagement**</span></span>

> [!NOTE]
> <span data-ttu-id="9c6d8-112">Se não vir as **Chaves de funcionalidades** listadas, verifique se a sua versão do Finance cumpre o requisito mínimo de versão (versão 10.0.13 com todas as atualizações de qualidade aplicadas ou superior).</span><span class="sxs-lookup"><span data-stu-id="9c6d8-112">If you don't see **Feature keys** listed, verify that your Finance version meets the minimum version requirement (application version 10.0.13 with all quality updates applied or higher).</span></span> <span data-ttu-id="9c6d8-113">Selecione **Verificar se há atualizações** para atualizar a lista de funcionalidades.</span><span class="sxs-lookup"><span data-stu-id="9c6d8-113">Select **Check for updates** to refresh the feature list.</span></span>

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a><span data-ttu-id="9c6d8-114">Definir o cenário de implementação do Project Operations para uma entidade legal</span><span class="sxs-lookup"><span data-stu-id="9c6d8-114">Define the Project Operations deployment scenario for a legal entity</span></span>

<span data-ttu-id="9c6d8-115">Pode ativar o Project Operations no Dynamics 365 Customer Engagement ao nível da entidade legal.</span><span class="sxs-lookup"><span data-stu-id="9c6d8-115">You can enable Project Operations on Dynamics 365 Customer Engagement on a legal entity level.</span></span> <span data-ttu-id="9c6d8-116">Pode ter uma entidade legal a usar o Project Operations no Dynamics 365 Customer Engagement para cenários baseados em recursos/não abastecidos.</span><span class="sxs-lookup"><span data-stu-id="9c6d8-116">You can have one legal entity using Project Operations on Dynamics 365 Customer Engagement for resource/non-stocked based scenarios.</span></span> <span data-ttu-id="9c6d8-117">No mesmo ambiente, pode ter outra entidade legal a utilizar o Project Operations para cenários de abastecimento/produção.</span><span class="sxs-lookup"><span data-stu-id="9c6d8-117">In the same environment, you can have another legal entity using Project Operations for stocked/production order scenarios.</span></span>

1. <span data-ttu-id="9c6d8-118">No Dynamics 365 Finance, vá para **Gestão de projetos e contabilística** > **Configurar** > **Parâmetros globais da Gestão de projetos e contabilística**.</span><span class="sxs-lookup"><span data-stu-id="9c6d8-118">In Dynamics 365 Finance, go to **Project management and accounting** > **Setup** > **Global project management and accounting parameters**.</span></span>
2. <span data-ttu-id="9c6d8-119">Na lista de entidades legais disponíveis, serão ativadas vários itens de contrato e o Project Operations nas funcionalidades do Dynamics 365 Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="9c6d8-119">In the list of available legal entities, select entities where multiple contract lines and Project Operations on Dynamics 365 Customer Engagement features will be enabled.</span></span> <span data-ttu-id="9c6d8-120">Deixe as entidades legais que utilizarão o Project Operations para cenários de encomenda de armazenamento/produção não selecionados.</span><span class="sxs-lookup"><span data-stu-id="9c6d8-120">Leave legal entities that will be using Project Operations for stocked/production order scenarios unselected.</span></span>

> [!NOTE]
> <span data-ttu-id="9c6d8-121">Uma entidade legal só pode ser selecionada se não tiver projetos existentes.</span><span class="sxs-lookup"><span data-stu-id="9c6d8-121">A legal entity can be selected only if it doesn't have any existing projects.</span></span>

## <a name="configure-project-management-and-accounting-parameters"></a><span data-ttu-id="9c6d8-122">Configurar os parâmetros de Gestão de projetos e contabilística</span><span class="sxs-lookup"><span data-stu-id="9c6d8-122">Configure Project management and accounting parameters</span></span>

<span data-ttu-id="9c6d8-123">Cada entidade legal que utiliza o Project Operations no Dynamics 365 Customer Engagement necessita de um conjunto de parâmetros predefinidos.</span><span class="sxs-lookup"><span data-stu-id="9c6d8-123">Each legal entity using Project Operations on Dynamics 365 Customer Engagement needs a set of default parameters.</span></span> <span data-ttu-id="9c6d8-124">Estes parâmetros estão configurados no separador **Project Operations** na página **Parâmetros da Gestão de projetos e contabilística**.</span><span class="sxs-lookup"><span data-stu-id="9c6d8-124">These parameters are configured on the **Project Operations** tab on the **Project management and accounting parameters** page.</span></span> <span data-ttu-id="9c6d8-125">Os parâmetros são:</span><span class="sxs-lookup"><span data-stu-id="9c6d8-125">The parameters are:</span></span>

  - <span data-ttu-id="9c6d8-126">**Predefinições do tipo de faturação** : O Project Operations utilizam um conjunto fixo de predefinições do tipo de faturação que devem ser mapeados para as propriedades de linha Finanças.</span><span class="sxs-lookup"><span data-stu-id="9c6d8-126">**Billing type defaults** : Project Operations uses a fixed set of billing type defaults that must be mapped to line properties Finance.</span></span> <span data-ttu-id="9c6d8-127">Criar um registo para cada tipo de faturação: **Não especificado** , **Faturável** , **Não faturável** , **Complementar** e **Não disponível**.</span><span class="sxs-lookup"><span data-stu-id="9c6d8-127">Create a record for each billing type: **Not specified** , **Chargeable** , **Non-chargeable** , **Complimentary** , and **Not available**.</span></span>
  - <span data-ttu-id="9c6d8-128">**Predefinições de categoria do projeto** : Selecione as categorias de projeto predefinidas a utilizar para cada tipo de transação.</span><span class="sxs-lookup"><span data-stu-id="9c6d8-128">**Project category defaults** : Select the default project categories to be used for each transaction type.</span></span> <span data-ttu-id="9c6d8-129">Estas predefinições serão utilizadas no **Diário de Integração do Project Operations** e em estimativas onde não é especificada nenhuma categoria de transação para o valor real do projeto.</span><span class="sxs-lookup"><span data-stu-id="9c6d8-129">These defaults will be used in the **Project Operations Integration journal** and in estimates where no transaction category is specified for the project actual.</span></span>
  - <span data-ttu-id="9c6d8-130">**Previsões** : Selecione o modelo de previsão a utilizar para estimativas de tempo e despesas.</span><span class="sxs-lookup"><span data-stu-id="9c6d8-130">**Forecasts** : Select the forecast model to be used for time and expense estimates.</span></span>
