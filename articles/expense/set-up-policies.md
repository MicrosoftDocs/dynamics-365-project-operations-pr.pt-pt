---
title: Definir políticas de despesas
description: Pode definir as políticas de despesas que os seus trabalhadores devem seguir ao introduzir e submeter relatórios de despesas e requisições de viagem.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: c55cec132649daf9ee08ea4d8db3668860247934
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128432"
---
# <a name="define-expense-policies"></a><span data-ttu-id="d8955-103">Definir políticas de despesas</span><span class="sxs-lookup"><span data-stu-id="d8955-103">Define expense policies</span></span>

<span data-ttu-id="d8955-104">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="d8955-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d8955-105">Pode definir as políticas que os seus trabalhadores devem seguir ao introduzir e submeter relatórios de despesas e requisições de viagem.</span><span class="sxs-lookup"><span data-stu-id="d8955-105">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="d8955-106">Implementar políticas de despesas pode ajudá-lo a gerir as despesas de forma eficaz.</span><span class="sxs-lookup"><span data-stu-id="d8955-106">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="d8955-107">Por exemplo, pode definir uma política para as despesas com hotéis em Nova Iorque, que diz que a despesa por noite não pode exceder USD 250.</span><span class="sxs-lookup"><span data-stu-id="d8955-107">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="d8955-108">Se um trabalhador apresentar um relatório de despesas ou requisição de viagem quando a taxa de quarto exceder esse valor, o sistema notificará</span><span class="sxs-lookup"><span data-stu-id="d8955-108">If a worker submits an expense report or travel requisition where the room rate exceeds this amount, the system will notify the</span></span>         
<span data-ttu-id="d8955-109">trabalhador que o montante da política para a despesa foi excedido.</span><span class="sxs-lookup"><span data-stu-id="d8955-109">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="d8955-110">Pode configurar a mensagem que o trabalhador irá receber quando</span><span class="sxs-lookup"><span data-stu-id="d8955-110">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="d8955-111">definir a política.</span><span class="sxs-lookup"><span data-stu-id="d8955-111">define the policy.</span></span>      
        
<span data-ttu-id="d8955-112">Pode definir três tipos de políticas:</span><span class="sxs-lookup"><span data-stu-id="d8955-112">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="d8955-113">**Aviso**: Permite ao trabalhador apresentar um relatório de despesas ou requisição de viagem, mas a despesa será marcada para todos os aprovadores e</span><span class="sxs-lookup"><span data-stu-id="d8955-113">**Warning**: Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>         
  <span data-ttu-id="d8955-114">para relatórios posteriores.</span><span class="sxs-lookup"><span data-stu-id="d8955-114">for later reporting.</span></span>        

- <span data-ttu-id="d8955-115">**Erro**: Exige que o trabalhador reveja as despesas para cumprir a política antes de apresentar o relatório de despesas ou a requisição de viagem.</span><span class="sxs-lookup"><span data-stu-id="d8955-115">**Error**: Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>        
 
 - <span data-ttu-id="d8955-116">**Justificação**: Exige que o trabalhador ou um gestor insira uma justificação por exceder o valor da apólice antes de apresentar o relatório de despesas ou a requisição de viagem.</span><span class="sxs-lookup"><span data-stu-id="d8955-116">**Justification**: Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="d8955-117">Sugestões de Política</span><span class="sxs-lookup"><span data-stu-id="d8955-117">Policy tips</span></span>
<span data-ttu-id="d8955-118">Aqui ficam algumas sugestões que podem ajudar na criação de novas políticas para a gestão de despesas:</span><span class="sxs-lookup"><span data-stu-id="d8955-118">Here are a few suggestions that can assist you when creating new policies for expense management:</span></span> 

- <span data-ttu-id="d8955-119">As políticas são válidas a partir da data, o que significa que uma apólice não produzirá efeito se for criada com uma data após a data em que a despesa ocorreu.</span><span class="sxs-lookup"><span data-stu-id="d8955-119">Policies are date effective which means a policy won't take effect if it's created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="d8955-120">Por exemplo, cria hoje uma nova política para impor uma despesa máxima de refeição de 50 euros.</span><span class="sxs-lookup"><span data-stu-id="d8955-120">For example, you create a new policy today to enforce a maximum meal expense of $50.</span></span> <span data-ttu-id="d8955-121">As despesas existentes registadas a partir de ontem não serão verificadas em relação a esta política.</span><span class="sxs-lookup"><span data-stu-id="d8955-121">Any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
- <span data-ttu-id="d8955-122">Ao criar uma política para uma categoria de despesas que possa ser discriminada, considere adicionar uma condição para o tipo de linha de despesas.</span><span class="sxs-lookup"><span data-stu-id="d8955-122">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="d8955-123">Algumas políticas, como a necessidade de um recibo, podem não fazer sentido para linhas discriminadas.</span><span class="sxs-lookup"><span data-stu-id="d8955-123">Some policies, such as requiring a receipt, may not make sense for itemized lines.</span></span> <span data-ttu-id="d8955-124">Nesta situação, a política só é aplicada à linha de cabeçalho ou a uma linha não discriminada.</span><span class="sxs-lookup"><span data-stu-id="d8955-124">In this situation, the policy only is applied to the header line or a non-itemized line.</span></span> 
- <span data-ttu-id="d8955-125">As políticas de gestão de despesas são avaliadas em relação à entidade de origem por defeito.</span><span class="sxs-lookup"><span data-stu-id="d8955-125">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="d8955-126">Para cenários entre empresas, pode definir a política a avaliar em relaçãoà entidade de destino (entidade tomadora de empréstimos) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="d8955-126">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="d8955-127">Para executar as políticas contra a entidade de destino, ligue a funcionalidade **Avaliar política de despesas em relação à entidade legal tomadora de empréstimos** na área de trabalho **Recurso de Gestão**.</span><span class="sxs-lookup"><span data-stu-id="d8955-127">To run the policies against the destination entity, turn on the **Evaluate Expense policy against borrowing legal entity** feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="d8955-128">Quando avaliar políticas</span><span class="sxs-lookup"><span data-stu-id="d8955-128">When to evaluate policies</span></span>

<span data-ttu-id="d8955-129">Nos parâmetros de gestão de despesas, pode selecionar para avaliar as políticas de gestão de despesas quando uma linha é guardada ou quando um relatório de despesas é submetido.</span><span class="sxs-lookup"><span data-stu-id="d8955-129">In expense management parameters, you can select to evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="d8955-130">Se optar por avaliar quando uma linha é guardada, os utilizadores terão visibilidade mais cedo sobre o que precisam de fazer para completar o seu relatório de despesas de uma só vez.</span><span class="sxs-lookup"><span data-stu-id="d8955-130">If you choose to evaluate when a line is saved, users will have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="d8955-131">Caso contrário, pode atrasar a avaliação da política e economizar tempo, validando no final, durante a submissão ao fluxo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="d8955-131">Otherwise, you can delay policy evaluation and save time by validating at the end, during the submission to workflow.</span></span>
