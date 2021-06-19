---
title: Projetos de estimativa de receitas de preço fixo
description: Este tópico fornece informações sobre a receita de preço fixo em projetos.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 639c6a104f2a90366a0f477c0d7cf384f19cdd81
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013815"
---
# <a name="fixed-price-revenue-estimate-projects"></a><span data-ttu-id="4ccc1-103">Projetos de estimativa de receitas de preço fixo</span><span class="sxs-lookup"><span data-stu-id="4ccc1-103">Fixed price revenue estimate projects</span></span> 

<span data-ttu-id="4ccc1-104">_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_</span><span class="sxs-lookup"><span data-stu-id="4ccc1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="4ccc1-105">Quando cria um item de contrato de projeto com os seguintes atributos no Dynamics 365 Project Operations no Microsoft Dataverse, o sistema cria automaticamente um projeto de estimativa de receitas de preço fixo.</span><span class="sxs-lookup"><span data-stu-id="4ccc1-105">When you create a project contract line with the following attributes in Dynamics 365 Project Operations on Microsoft Dataverse, the system automatically creates a fixed price revenue estimate project.</span></span> <span data-ttu-id="4ccc1-106">As informações neste projeto baseiam-se no seguinte:</span><span class="sxs-lookup"><span data-stu-id="4ccc1-106">The information in this project is based on the following:</span></span>

  - <span data-ttu-id="4ccc1-107">Um método de faturação de preço fixo.</span><span class="sxs-lookup"><span data-stu-id="4ccc1-107">A fixed price billing method.</span></span>
  - <span data-ttu-id="4ccc1-108">Um projeto associado.</span><span class="sxs-lookup"><span data-stu-id="4ccc1-108">An associated project.</span></span>
  - <span data-ttu-id="4ccc1-109">Pelo menos, um marco definido no separador **Agenda de faturas** na página **Item de contrato do projeto**.</span><span class="sxs-lookup"><span data-stu-id="4ccc1-109">At least one milestone defined on the **Invoice schedule** tab on the **Project contract line** page.</span></span>

## <a name="review-fixed-price-revenue-estimates-projects"></a><span data-ttu-id="4ccc1-110">Reveja projetos de estimativas de receitas de preço fixo</span><span class="sxs-lookup"><span data-stu-id="4ccc1-110">Review fixed price revenue estimates projects</span></span>
<span data-ttu-id="4ccc1-111">Para rever os projetos de estimativas de receitas de preços fixos, complete os seguintes passos:</span><span class="sxs-lookup"><span data-stu-id="4ccc1-111">To review fixed price revenue estimates projects, complete the following steps:</span></span>

1. <span data-ttu-id="4ccc1-112">No ambiente do Dynamics 365 Finance, vá a **Gestão de projetos e contabilística** > **Projetos** > **Projetos de estimativa de receitas de preço fixo**.</span><span class="sxs-lookup"><span data-stu-id="4ccc1-112">In the Dynamics 365 Finance environment, go to **Projects management and accounting** > **Projects** > **Fixed price revenue estimate projects**.</span></span>
2. <span data-ttu-id="4ccc1-113">Selecione o projeto que pretende visualizar e clique duas vezes em **ID do projeto de estimativa** para abrir o registo e rever os detalhes do projeto.</span><span class="sxs-lookup"><span data-stu-id="4ccc1-113">Select the project that you want to view and double-click the **Estimate project ID** to open the record and review the details of the project.</span></span>
3. <span data-ttu-id="4ccc1-114">Expanda o separador **Projeto**. Verá um projeto na grelha **Projetos selecionados**.</span><span class="sxs-lookup"><span data-stu-id="4ccc1-114">Expand the **Project** tab. You will see one project in the **Selected projects** grid.</span></span> <span data-ttu-id="4ccc1-115">O sistema usa isto como o projeto predefinido porque é o projeto associado ao item de contrato do projeto.</span><span class="sxs-lookup"><span data-stu-id="4ccc1-115">The system uses this as default project because it is the project associated to the project contract line.</span></span> 
4. <span data-ttu-id="4ccc1-116">Para alterar a associação, selecione projetos adicionais e adicione-os à grelha **Projetos selecionados**.</span><span class="sxs-lookup"><span data-stu-id="4ccc1-116">To change the association, select additional projects and add them to the **Selected projects** grid.</span></span> <span data-ttu-id="4ccc1-117">Se vários projetos forem selecionados nesta grelha, a percentagem de conclusão do projeto e as estimativas de receitas são calculadas em conjunto para todos os projetos selecionados.</span><span class="sxs-lookup"><span data-stu-id="4ccc1-117">If multiple projects are selected in this grid, the project percentage completion and revenue estimates are calculated together for of the all selected projects.</span></span>

  <span data-ttu-id="4ccc1-118">O custo do projeto, o perfil da receita, o modelo de custos e o código de período podem ser definidos manualmente.</span><span class="sxs-lookup"><span data-stu-id="4ccc1-118">Project cost, revenue profile, cost template, and the period code can be set manually.</span></span> <span data-ttu-id="4ccc1-119">Se não forem definidos manualmente, os valores assumem a predefinição durante o primeiro cálculo de estimativa para o projeto utilizando as regras configuradas para o custo do projeto e perfis de receitas.</span><span class="sxs-lookup"><span data-stu-id="4ccc1-119">If they aren't set manually, the values default during the first estimate calculation for the project using the rules configured for project cost and revenue profiles.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]