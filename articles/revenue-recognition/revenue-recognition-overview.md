---
title: Descrição geral do reconhecimento de receitas
description: Este tópico fornece informações sobre o reconhecimento de receitas no Project Operations.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: f5f962572c6ec0298d2d91d33f83e4120a498a6f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013770"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="2bee2-103">Descrição geral do reconhecimento de receitas</span><span class="sxs-lookup"><span data-stu-id="2bee2-103">Revenue recognition overview</span></span>

<span data-ttu-id="2bee2-104">_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_</span><span class="sxs-lookup"><span data-stu-id="2bee2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="2bee2-105">No Dynamics 365 Project Operations, os princípios de reconhecimento de receitas variam em função do método de faturação selecionado para um projeto ou parte do projeto.</span><span class="sxs-lookup"><span data-stu-id="2bee2-105">In Dynamics 365 Project Operations, revenue recognition principles vary based on the selected billing method for a project or portion of the project.</span></span> <span data-ttu-id="2bee2-106">Este tópico fornece informações sobre o reconhecimento de receitas no Project Operations.</span><span class="sxs-lookup"><span data-stu-id="2bee2-106">This topic provides information about revenue recognition in Project Operations.</span></span>

## <a name="transactions-accounted-using-time-and-material-billing-method"></a><span data-ttu-id="2bee2-107">Transações contabilizadas utilizando o método de faturação de tempo e material</span><span class="sxs-lookup"><span data-stu-id="2bee2-107">Transactions accounted using time and material billing method</span></span>

- <span data-ttu-id="2bee2-108">O reconhecimento de custo e receitas estão ligados.</span><span class="sxs-lookup"><span data-stu-id="2bee2-108">Cost and revenue recognition are connected.</span></span> <span data-ttu-id="2bee2-109">O custo de transação e as vendas não faturadas são publicados através do [diário de Integração do Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="2bee2-109">Transaction cost and unbilled sales are posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span>
- <span data-ttu-id="2bee2-110">O perfil de custos e receitas do projeto determinam se as transações de vendas não faturadas são publicadas no livro razão geral.</span><span class="sxs-lookup"><span data-stu-id="2bee2-110">Project cost and revenue profile determine if unbilled sales transactions are posted to the general ledger.</span></span> <span data-ttu-id="2bee2-111">Se a **Receita de acréscimo** for selecionada, o sistema utiliza o **Valor de vendas WIP** e as contas **Valor de vendas de receita de acréscimo** durante a publicação.</span><span class="sxs-lookup"><span data-stu-id="2bee2-111">If **Accrue revenue** is selected, the system uses the **WIP sales value** and the **Accrued revenue sales value** accounts during posting.</span></span> <span data-ttu-id="2bee2-112">O seguinte é um exemplo deste método.</span><span class="sxs-lookup"><span data-stu-id="2bee2-112">The following is an example of this method.</span></span>  

  | <span data-ttu-id="2bee2-113">Tipo de transação</span><span class="sxs-lookup"><span data-stu-id="2bee2-113">Transaction type</span></span> | <span data-ttu-id="2bee2-114">Débito/Crédito</span><span class="sxs-lookup"><span data-stu-id="2bee2-114">Debit/Credit</span></span> | <span data-ttu-id="2bee2-115">Montante</span><span class="sxs-lookup"><span data-stu-id="2bee2-115">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="2bee2-116">Valor de Vendas WIP</span><span class="sxs-lookup"><span data-stu-id="2bee2-116">WIP Sales value</span></span> | <span data-ttu-id="2bee2-117">Débito</span><span class="sxs-lookup"><span data-stu-id="2bee2-117">Debit</span></span> | <span data-ttu-id="2bee2-118">100</span><span class="sxs-lookup"><span data-stu-id="2bee2-118">100</span></span> |
  | <span data-ttu-id="2bee2-119">Valor das vendas de receitas acumuladas</span><span class="sxs-lookup"><span data-stu-id="2bee2-119">Accrued revenue sales value</span></span> | <span data-ttu-id="2bee2-120">Crédito</span><span class="sxs-lookup"><span data-stu-id="2bee2-120">Credit</span></span> | <span data-ttu-id="2bee2-121">100</span><span class="sxs-lookup"><span data-stu-id="2bee2-121">100</span></span> |

- <span data-ttu-id="2bee2-122">A receita é reconhecida durante a faturação.</span><span class="sxs-lookup"><span data-stu-id="2bee2-122">Revenue is recognized during invoicing.</span></span> <span data-ttu-id="2bee2-123">O sistema utiliza a conta de **Receitas faturadas** durante a publicação.</span><span class="sxs-lookup"><span data-stu-id="2bee2-123">The system uses the **Invoiced revenue** account during posting.</span></span> <span data-ttu-id="2bee2-124">O seguinte é um exemplo deste método.</span><span class="sxs-lookup"><span data-stu-id="2bee2-124">The following is an example of this method.</span></span>  

  | <span data-ttu-id="2bee2-125">Tipo de transação</span><span class="sxs-lookup"><span data-stu-id="2bee2-125">Transaction type</span></span> | <span data-ttu-id="2bee2-126">Débito/Crédito</span><span class="sxs-lookup"><span data-stu-id="2bee2-126">Debit/Credit</span></span> | <span data-ttu-id="2bee2-127">Montante</span><span class="sxs-lookup"><span data-stu-id="2bee2-127">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="2bee2-128">Saldo do cliente</span><span class="sxs-lookup"><span data-stu-id="2bee2-128">Customer balance</span></span> | <span data-ttu-id="2bee2-129">Débito</span><span class="sxs-lookup"><span data-stu-id="2bee2-129">Debit</span></span> | <span data-ttu-id="2bee2-130">120</span><span class="sxs-lookup"><span data-stu-id="2bee2-130">120</span></span> |
  | <span data-ttu-id="2bee2-131">Valor de imposto pagável</span><span class="sxs-lookup"><span data-stu-id="2bee2-131">Sales tax payable</span></span> | <span data-ttu-id="2bee2-132">Crédito</span><span class="sxs-lookup"><span data-stu-id="2bee2-132">Credit</span></span> | <span data-ttu-id="2bee2-133">20</span><span class="sxs-lookup"><span data-stu-id="2bee2-133">20</span></span> |
  | <span data-ttu-id="2bee2-134">Receitas Faturadas</span><span class="sxs-lookup"><span data-stu-id="2bee2-134">Invoiced Revenue</span></span> | <span data-ttu-id="2bee2-135">Crédito</span><span class="sxs-lookup"><span data-stu-id="2bee2-135">Credit</span></span> | <span data-ttu-id="2bee2-136">100</span><span class="sxs-lookup"><span data-stu-id="2bee2-136">100</span></span> |

- <span data-ttu-id="2bee2-137">Se as receitas forem acumuladas quando as vendas não faturadas forem publicadas, o sistema reverterá as receitas acumuladas na faturação.</span><span class="sxs-lookup"><span data-stu-id="2bee2-137">If revenue was accrued when the unbilled sales are posted, the system will reverse the accrued revenue at invoicing.</span></span>

  | <span data-ttu-id="2bee2-138">Tipo de transação</span><span class="sxs-lookup"><span data-stu-id="2bee2-138">Transaction type</span></span> | <span data-ttu-id="2bee2-139">Débito/Crédito</span><span class="sxs-lookup"><span data-stu-id="2bee2-139">Debit/Credit</span></span> | <span data-ttu-id="2bee2-140">Montante</span><span class="sxs-lookup"><span data-stu-id="2bee2-140">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="2bee2-141">Valor de Vendas WIP</span><span class="sxs-lookup"><span data-stu-id="2bee2-141">WIP Sales value</span></span> | <span data-ttu-id="2bee2-142">Crédito</span><span class="sxs-lookup"><span data-stu-id="2bee2-142">Credit</span></span> | <span data-ttu-id="2bee2-143">100</span><span class="sxs-lookup"><span data-stu-id="2bee2-143">100</span></span> |
  | <span data-ttu-id="2bee2-144">Valor das vendas de receitas acumuladas</span><span class="sxs-lookup"><span data-stu-id="2bee2-144">Accrued revenue sales value</span></span> | <span data-ttu-id="2bee2-145">Débito</span><span class="sxs-lookup"><span data-stu-id="2bee2-145">Debit</span></span> | <span data-ttu-id="2bee2-146">100</span><span class="sxs-lookup"><span data-stu-id="2bee2-146">100</span></span> |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a><span data-ttu-id="2bee2-147">Transações contabilizadas utilizando o método de faturação de preço fixo</span><span class="sxs-lookup"><span data-stu-id="2bee2-147">Transactions accounted using the fixed price billing method</span></span>

- <span data-ttu-id="2bee2-148">O reconhecimento de custo e receitas estão separados.</span><span class="sxs-lookup"><span data-stu-id="2bee2-148">Cost and revenue recognition are separate.</span></span> <span data-ttu-id="2bee2-149">O custo de transação é publicado através do [diário de Integração do Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="2bee2-149">Transaction cost is posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="2bee2-150">As transações de vendas não faturadas não são criadas.</span><span class="sxs-lookup"><span data-stu-id="2bee2-150">Unbilled sales transactions aren't created.</span></span>
- <span data-ttu-id="2bee2-151">As receitas podem ser reconhecidas durante a faturação se o perfil de custo e receita do projeto tiver o **Princípio utilizado para os cálculos de conclusão do projeto** definidos como **Sem WIP**.</span><span class="sxs-lookup"><span data-stu-id="2bee2-151">Revenue can be recognized during invoicing if the project cost and revenue profile have **Principle used for project completion calculations** set to **No WIP**.</span></span> <span data-ttu-id="2bee2-152">Utilize apenas este método para projetos simples e de curto prazo.</span><span class="sxs-lookup"><span data-stu-id="2bee2-152">Only use this method for short term, simple projects.</span></span>
- <span data-ttu-id="2bee2-153">As receitas podem ser reconhecidas usando estimativas de receitas de preço fixo, com o método **Contrato concluído** ou **Reconhecimento de receitas de conclusão de percentagem**.</span><span class="sxs-lookup"><span data-stu-id="2bee2-153">Revenue can be recognized using fixed price revenue estimates, with either the **Completed contract** or **Percent completion revenue recognition** method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2bee2-154">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="2bee2-154">Additional resources</span></span>
[<span data-ttu-id="2bee2-155">Artigo Configurar gestão contabilística para projetos faturáveis</span><span class="sxs-lookup"><span data-stu-id="2bee2-155">Configure accounting for billable projects article</span></span>](../project-accounting/configure-accounting-billable-projects.md)

[<span data-ttu-id="2bee2-156">Projetos de estimativa de receitas de preço fixo</span><span class="sxs-lookup"><span data-stu-id="2bee2-156">Fixed price revenue estimate projects</span></span>](rev-rec-percentage-completion-method.md)

[<span data-ttu-id="2bee2-157">Gerir estimativas de receitas</span><span class="sxs-lookup"><span data-stu-id="2bee2-157">Manage revenue estimates</span></span>](rev-rec-completed-contract-method.md)

[<span data-ttu-id="2bee2-158">Métodos de custo para conclusão</span><span class="sxs-lookup"><span data-stu-id="2bee2-158">Cost to complete methods</span></span>](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]