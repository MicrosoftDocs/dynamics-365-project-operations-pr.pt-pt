---
title: Configurar políticas de despesas
description: Pode configurar as políticas de despesas que os seus trabalhadores devem seguir ao introduzir e submeter relatórios de despesas e requisições de viagem no Microsoft Dynamics 365 Finance.
author: suvaidya
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f74f6906cc1137b9645a830360a546432dc5207f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082551"
---
# <a name="set-up-expense-policies"></a><span data-ttu-id="fa289-103">Configurar políticas de despesas</span><span class="sxs-lookup"><span data-stu-id="fa289-103">Set up expense policies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fa289-104">Pode definir as políticas que os seus trabalhadores devem seguir ao introduzir e submeter relatórios de despesas e requisições de viagem.</span><span class="sxs-lookup"><span data-stu-id="fa289-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="fa289-105">Implementar políticas de despesas pode ajudá-lo a gerir as despesas de forma eficaz.</span><span class="sxs-lookup"><span data-stu-id="fa289-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="fa289-106">Por exemplo, pode definir uma política para as despesas com hotéis em Nova Iorque, que diz que a despesa por noite não pode exceder USD 250.</span><span class="sxs-lookup"><span data-stu-id="fa289-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="fa289-107">Se um trabalhador apresentar um relatório de despesas ou uma requisição de viagem em que a taxa de quarto exceder esse valor, o sistema notificará</span><span class="sxs-lookup"><span data-stu-id="fa289-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="fa289-108">trabalhador que o montante da política para a despesa foi excedido.</span><span class="sxs-lookup"><span data-stu-id="fa289-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="fa289-109">Pode configurar a mensagem que o trabalhador irá receber quando</span><span class="sxs-lookup"><span data-stu-id="fa289-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="fa289-110">definir a política.</span><span class="sxs-lookup"><span data-stu-id="fa289-110">define the policy.</span></span>      
        
<span data-ttu-id="fa289-111">Pode definir três tipos de políticas:</span><span class="sxs-lookup"><span data-stu-id="fa289-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="fa289-112">Aviso – Permite ao trabalhador apresentar um relatório de despesas ou requisição de viagem, mas a despesa será marcada para todos os aprovadores e</span><span class="sxs-lookup"><span data-stu-id="fa289-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
  <span data-ttu-id="fa289-113">para relatórios posteriores.</span><span class="sxs-lookup"><span data-stu-id="fa289-113">for later reporting.</span></span>        

- <span data-ttu-id="fa289-114">Erro – Exige que o trabalhador reveja as despesas para cumprir a política antes de apresentar o relatório de despesas ou a requisição de viagem.</span><span class="sxs-lookup"><span data-stu-id="fa289-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
 - <span data-ttu-id="fa289-115">Justificação – Exige que o trabalhador ou um gestor insira uma justificação por exceder o valor da apólice antes de apresentar o relatório de despesas ou a requisição de viagem.</span><span class="sxs-lookup"><span data-stu-id="fa289-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="fa289-116">Sugestões de Política</span><span class="sxs-lookup"><span data-stu-id="fa289-116">Policy tips</span></span>
<span data-ttu-id="fa289-117">Aqui ficam algumas sugestões que podem ajudar na criação de novas políticas para a gestão de despesas.</span><span class="sxs-lookup"><span data-stu-id="fa289-117">Here are a few suggestions that can assist you when creating new policies for expense management.</span></span> 
* <span data-ttu-id="fa289-118">As políticas são válidas a partir da data e não produzirá efeito se a política for criada com uma data após a data em que a despesa ocorreu.</span><span class="sxs-lookup"><span data-stu-id="fa289-118">Policies are date effective and won't take effect if the policy is created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="fa289-119">Por exemplo, se estiver a criar uma nova política hoje para impor uma despesa de refeição máxima de 50 $, então quaisquer despesas existentes inscritas a partir de ontem não serão verificadas contra esta política.</span><span class="sxs-lookup"><span data-stu-id="fa289-119">For example, if you are creating a new policy today to enforce a maximum meal expense of $50, then any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
* <span data-ttu-id="fa289-120">Ao criar uma política para uma categoria de despesas que possa ser discriminada, considere adicionar uma condição para o tipo de linha de despesas.</span><span class="sxs-lookup"><span data-stu-id="fa289-120">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="fa289-121">Algumas políticas, tais como a necessidade de um recibo, podem não fazer sentido para linhas discriminadas e só devem ser aplicadas à linha de cabeçalho ou a uma linha não discriminada.</span><span class="sxs-lookup"><span data-stu-id="fa289-121">Some policies such as requiring a receipt may not make sense for itemized lines and should only be applied to the header line or a non-itemized line.</span></span> 
* <span data-ttu-id="fa289-122">As políticas de gestão de despesas são avaliadas em relação à entidade de origem por defeito.</span><span class="sxs-lookup"><span data-stu-id="fa289-122">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="fa289-123">Para cenários entre empresas, pode definir a política a avaliar em relaçãoà entidade de destino (entidade tomadora de empréstimos) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="fa289-123">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="fa289-124">Para executar as políticas contra a entidade de destino, ligue a funcionalidade "Avaliar política de despesas em relação à entidade legal" tomadora de empréstimos na área de trabalho **Gestão de Funcionalidades**.</span><span class="sxs-lookup"><span data-stu-id="fa289-124">To run the policies against the destination entity, turn on the "Evaluate Expense policy against borrowing legal entity" feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="fa289-125">Quando avaliar políticas</span><span class="sxs-lookup"><span data-stu-id="fa289-125">When to evaluate policies</span></span>

<span data-ttu-id="fa289-126">Nos parâmetros de gestão de despesas, existe uma opção para avaliar as políticas de gestão de despesas quando uma linha é guardada ou quando um relatório de despesas é submetido.</span><span class="sxs-lookup"><span data-stu-id="fa289-126">In expense management parameters, there is an option to either evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="fa289-127">Se optar por avaliar quando uma linha é guardada, isto garante que os utilizadores terão visibilidade mais cedo sobre o que precisam de fazer para completar o seu relatório de despesas de uma só vez.</span><span class="sxs-lookup"><span data-stu-id="fa289-127">If you choose to evaluate when a line is saved this ensures that users have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="fa289-128">Caso contrário, pode atrasar a avaliação da política e economizar tempo se fizer com que a validação ocorra no final, durante a submissão ao fluxo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="fa289-128">Otherwise, you can delay policy evaluation and save time if you have validation occur at the end, during submission to workflow.</span></span>
