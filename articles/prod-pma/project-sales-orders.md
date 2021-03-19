---
title: Ordens de venda de projetos para projetos de tempo e material
description: Este tópico explica como criar ordens de venda baseadas no projeto para os projetos de tempo e material.
author: Yowelle
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 74a90ea0bdb8f760273c0f6b1c61bffcb70b6c8d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289068"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a><span data-ttu-id="762d7-103">Ordens de venda de projetos para projetos de tempo e material</span><span class="sxs-lookup"><span data-stu-id="762d7-103">Project sales orders for time and material projects</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="762d7-104">Este tópico descreve como criar uma ordem de venda para um projeto.</span><span class="sxs-lookup"><span data-stu-id="762d7-104">This topic describes how to create a sales order for a project.</span></span> <span data-ttu-id="762d7-105">As ordens de venda só podem ser criadas para projetos do tipo **tempo e material**.</span><span class="sxs-lookup"><span data-stu-id="762d7-105">Sales orders can only be created for projects of type **time and material**.</span></span>

<span data-ttu-id="762d7-106">Se um projeto de tempo e material tiver múltiplas fontes de financiamento no contrato de projeto, tem de ativar o parâmetro **Permitir ordens de venda para projetos com múltiplas fontes de financiamento** na página **Parâmetros da gestão de projetos e contabilística**.</span><span class="sxs-lookup"><span data-stu-id="762d7-106">If a time and material project has multiple funding sources on the project contract, you must enable the **Allow sales orders for projects with multiple funding sources** parameter on the **Project management and accounting parameters** page.</span></span> 

> [!NOTE]
> - <span data-ttu-id="762d7-107">O suporte para ordens de venda de projetos com múltiplas fontes de financiamento está disponível a partir da versão de aplicação 10.0.2 e superior.</span><span class="sxs-lookup"><span data-stu-id="762d7-107">Support for project sales orders with multiple funding sources is available starting with application release 10.0.2 and higher.</span></span>
> - <span data-ttu-id="762d7-108">O parâmetro para ativar o suporte para ordens de venda de projetos com múltiplas fontes de financiamento será removido na segunda fase do lançamento de abril de 2020, após a qual a funcionalidade estará sempre ativada.</span><span class="sxs-lookup"><span data-stu-id="762d7-108">The parameter to enable the support for project sales orders with multiple funding sources will be removed in the April 2020 release wave, after which the functionality will always be enabled.</span></span>

<span data-ttu-id="762d7-109">Pode criar ordens de venda baseadas em projetos de duas formas:</span><span class="sxs-lookup"><span data-stu-id="762d7-109">You can create project-based sales orders in two ways:</span></span>

- <span data-ttu-id="762d7-110">Vá para o próprio projeto.</span><span class="sxs-lookup"><span data-stu-id="762d7-110">Go to the project itself.</span></span> <span data-ttu-id="762d7-111">No Painel de Ação, selecione **Gerir > Tarefas do item > Ordem de venda**.</span><span class="sxs-lookup"><span data-stu-id="762d7-111">On the Action Pane, select **Manage > Item tasks > Sales order**.</span></span> <span data-ttu-id="762d7-112">A informação do projeto assumirá por predefinição a ordem de venda do projeto.</span><span class="sxs-lookup"><span data-stu-id="762d7-112">The project information will default to the sales order from the project.</span></span> <span data-ttu-id="762d7-113">Se o contrato de projeto tiver mais de uma fonte de financiamento, terá de selecionar a fonte de financiamento para definir o cliente para a ordem de venda.</span><span class="sxs-lookup"><span data-stu-id="762d7-113">If the project contract has more than one funding source, you will need to select the funding source to set the customer for the sales order.</span></span> <span data-ttu-id="762d7-114">Se existir apenas uma fonte de financiamento para o projeto, o cliente será definido automaticamente.</span><span class="sxs-lookup"><span data-stu-id="762d7-114">If there is only one funding source for the project, the customer will be automatically set.</span></span>
- <span data-ttu-id="762d7-115">Vá para a página da lista **Todas as ordens de venda** e crie uma nova ordem de venda.</span><span class="sxs-lookup"><span data-stu-id="762d7-115">Go to the **All sales order** list page and create a new sales order.</span></span> <span data-ttu-id="762d7-116">Terá de selecionar o projeto para a ordem de venda.</span><span class="sxs-lookup"><span data-stu-id="762d7-116">You will need to select the project for the sales order.</span></span> <span data-ttu-id="762d7-117">Depois de selecionado o projeto, o cliente será definido a partir da fonte de financiamento ou terá de selecionar a fonte de financiamento se o contrato de projeto tiver múltiplas fontes de financiamento.</span><span class="sxs-lookup"><span data-stu-id="762d7-117">After the project is selected, the customer will be set from the funding source or you will need to select the funding source if the project contract has multiple funding sources.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]