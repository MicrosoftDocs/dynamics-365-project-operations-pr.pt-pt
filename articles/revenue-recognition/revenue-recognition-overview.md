---
title: Descrição geral do reconhecimento de receitas
description: Este tópico fornece informações sobre o reconhecimento de receitas no Project Operations.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: ab9b36b71223b1bcfe48de5f9b68b6fb6a98f388
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368040"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="f7232-103">Descrição geral do reconhecimento de receitas</span><span class="sxs-lookup"><span data-stu-id="f7232-103">Revenue recognition overview</span></span>

<span data-ttu-id="f7232-104">_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_</span><span class="sxs-lookup"><span data-stu-id="f7232-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="f7232-105">No Dynamics 365 Project Operations, os princípios de reconhecimento de receitas variam em função do método de faturação selecionado para um projeto ou parte do projeto.</span><span class="sxs-lookup"><span data-stu-id="f7232-105">In Dynamics 365 Project Operations, revenue recognition principles vary based on the selected billing method for a project or portion of the project.</span></span> <span data-ttu-id="f7232-106">Este tópico fornece informações sobre o reconhecimento de receitas no Project Operations.</span><span class="sxs-lookup"><span data-stu-id="f7232-106">This topic provides information about revenue recognition in Project Operations.</span></span>

## <a name="transactions-accounted-using-time-and-material-billing-method"></a><span data-ttu-id="f7232-107">Transações contabilizadas utilizando o método de faturação de tempo e material</span><span class="sxs-lookup"><span data-stu-id="f7232-107">Transactions accounted using time and material billing method</span></span>

- <span data-ttu-id="f7232-108">O reconhecimento de custo e receitas estão ligados.</span><span class="sxs-lookup"><span data-stu-id="f7232-108">Cost and revenue recognition are connected.</span></span> <span data-ttu-id="f7232-109">O custo de transação e as vendas não faturadas são publicados através do [diário de Integração do Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="f7232-109">Transaction cost and unbilled sales are posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span>
- <span data-ttu-id="f7232-110">O perfil de custos e receitas do projeto determinam se as transações de vendas não faturadas são publicadas no livro razão geral.</span><span class="sxs-lookup"><span data-stu-id="f7232-110">Project cost and revenue profile determine if unbilled sales transactions are posted to the general ledger.</span></span> <span data-ttu-id="f7232-111">Se a **Receita de acréscimo** for selecionada, o sistema utiliza o **Valor de vendas WIP** e as contas **Valor de vendas de receita de acréscimo** durante a publicação.</span><span class="sxs-lookup"><span data-stu-id="f7232-111">If **Accrue revenue** is selected, the system uses the **WIP sales value** and the **Accrued revenue sales value** accounts during posting.</span></span> <span data-ttu-id="f7232-112">O seguinte é um exemplo deste método.</span><span class="sxs-lookup"><span data-stu-id="f7232-112">The following is an example of this method.</span></span>  

  | <span data-ttu-id="f7232-113">Tipo de transação</span><span class="sxs-lookup"><span data-stu-id="f7232-113">Transaction type</span></span> | <span data-ttu-id="f7232-114">Débito/Crédito</span><span class="sxs-lookup"><span data-stu-id="f7232-114">Debit/Credit</span></span> | <span data-ttu-id="f7232-115">Montante</span><span class="sxs-lookup"><span data-stu-id="f7232-115">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="f7232-116">Valor de Vendas WIP</span><span class="sxs-lookup"><span data-stu-id="f7232-116">WIP Sales value</span></span> | <span data-ttu-id="f7232-117">Débito</span><span class="sxs-lookup"><span data-stu-id="f7232-117">Debit</span></span> | <span data-ttu-id="f7232-118">100</span><span class="sxs-lookup"><span data-stu-id="f7232-118">100</span></span> |
  | <span data-ttu-id="f7232-119">Valor das vendas de receitas acumuladas</span><span class="sxs-lookup"><span data-stu-id="f7232-119">Accrued revenue sales value</span></span> | <span data-ttu-id="f7232-120">Crédito</span><span class="sxs-lookup"><span data-stu-id="f7232-120">Credit</span></span> | <span data-ttu-id="f7232-121">100</span><span class="sxs-lookup"><span data-stu-id="f7232-121">100</span></span> |

- <span data-ttu-id="f7232-122">A receita é reconhecida durante a faturação.</span><span class="sxs-lookup"><span data-stu-id="f7232-122">Revenue is recognized during invoicing.</span></span> <span data-ttu-id="f7232-123">O sistema utiliza a conta de **Receitas faturadas** durante a publicação.</span><span class="sxs-lookup"><span data-stu-id="f7232-123">The system uses the **Invoiced revenue** account during posting.</span></span> <span data-ttu-id="f7232-124">O seguinte é um exemplo deste método.</span><span class="sxs-lookup"><span data-stu-id="f7232-124">The following is an example of this method.</span></span>  

  | <span data-ttu-id="f7232-125">Tipo de transação</span><span class="sxs-lookup"><span data-stu-id="f7232-125">Transaction type</span></span> | <span data-ttu-id="f7232-126">Débito/Crédito</span><span class="sxs-lookup"><span data-stu-id="f7232-126">Debit/Credit</span></span> | <span data-ttu-id="f7232-127">Montante</span><span class="sxs-lookup"><span data-stu-id="f7232-127">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="f7232-128">Saldo do cliente</span><span class="sxs-lookup"><span data-stu-id="f7232-128">Customer balance</span></span> | <span data-ttu-id="f7232-129">Débito</span><span class="sxs-lookup"><span data-stu-id="f7232-129">Debit</span></span> | <span data-ttu-id="f7232-130">120</span><span class="sxs-lookup"><span data-stu-id="f7232-130">120</span></span> |
  | <span data-ttu-id="f7232-131">Valor de imposto pagável</span><span class="sxs-lookup"><span data-stu-id="f7232-131">Sales tax payable</span></span> | <span data-ttu-id="f7232-132">Crédito</span><span class="sxs-lookup"><span data-stu-id="f7232-132">Credit</span></span> | <span data-ttu-id="f7232-133">20</span><span class="sxs-lookup"><span data-stu-id="f7232-133">20</span></span> |
  | <span data-ttu-id="f7232-134">Receitas Faturadas</span><span class="sxs-lookup"><span data-stu-id="f7232-134">Invoiced Revenue</span></span> | <span data-ttu-id="f7232-135">Crédito</span><span class="sxs-lookup"><span data-stu-id="f7232-135">Credit</span></span> | <span data-ttu-id="f7232-136">100</span><span class="sxs-lookup"><span data-stu-id="f7232-136">100</span></span> |

- <span data-ttu-id="f7232-137">Se as receitas forem acumuladas quando as vendas não faturadas forem publicadas, o sistema reverterá as receitas acumuladas na faturação.</span><span class="sxs-lookup"><span data-stu-id="f7232-137">If revenue was accrued when the unbilled sales are posted, the system will reverse the accrued revenue at invoicing.</span></span>

  | <span data-ttu-id="f7232-138">Tipo de transação</span><span class="sxs-lookup"><span data-stu-id="f7232-138">Transaction type</span></span> | <span data-ttu-id="f7232-139">Débito/Crédito</span><span class="sxs-lookup"><span data-stu-id="f7232-139">Debit/Credit</span></span> | <span data-ttu-id="f7232-140">Montante</span><span class="sxs-lookup"><span data-stu-id="f7232-140">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="f7232-141">Valor de Vendas WIP</span><span class="sxs-lookup"><span data-stu-id="f7232-141">WIP Sales value</span></span> | <span data-ttu-id="f7232-142">Crédito</span><span class="sxs-lookup"><span data-stu-id="f7232-142">Credit</span></span> | <span data-ttu-id="f7232-143">100</span><span class="sxs-lookup"><span data-stu-id="f7232-143">100</span></span> |
  | <span data-ttu-id="f7232-144">Valor das vendas de receitas acumuladas</span><span class="sxs-lookup"><span data-stu-id="f7232-144">Accrued revenue sales value</span></span> | <span data-ttu-id="f7232-145">Débito</span><span class="sxs-lookup"><span data-stu-id="f7232-145">Debit</span></span> | <span data-ttu-id="f7232-146">100</span><span class="sxs-lookup"><span data-stu-id="f7232-146">100</span></span> |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a><span data-ttu-id="f7232-147">Transações contabilizadas utilizando o método de faturação de preço fixo</span><span class="sxs-lookup"><span data-stu-id="f7232-147">Transactions accounted using the fixed price billing method</span></span>

- <span data-ttu-id="f7232-148">O reconhecimento de custo e receitas estão separados.</span><span class="sxs-lookup"><span data-stu-id="f7232-148">Cost and revenue recognition are separate.</span></span> <span data-ttu-id="f7232-149">O custo de transação é publicado através do [diário de Integração do Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="f7232-149">Transaction cost is posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="f7232-150">As transações de vendas não faturadas não são criadas.</span><span class="sxs-lookup"><span data-stu-id="f7232-150">Unbilled sales transactions aren't created.</span></span>
- <span data-ttu-id="f7232-151">As receitas podem ser reconhecidas durante a faturação se o perfil de custo e receita do projeto tiver o **Princípio utilizado para os cálculos de conclusão do projeto** definidos como **Sem WIP**.</span><span class="sxs-lookup"><span data-stu-id="f7232-151">Revenue can be recognized during invoicing if the project cost and revenue profile have **Principle used for project completion calculations** set to **No WIP**.</span></span> <span data-ttu-id="f7232-152">Utilize apenas este método para projetos simples e de curto prazo.</span><span class="sxs-lookup"><span data-stu-id="f7232-152">Only use this method for short term, simple projects.</span></span>
- <span data-ttu-id="f7232-153">As receitas podem ser reconhecidas usando estimativas de receitas de preço fixo, com o método **Contrato concluído** ou **Reconhecimento de receitas de conclusão de percentagem**.</span><span class="sxs-lookup"><span data-stu-id="f7232-153">Revenue can be recognized using fixed price revenue estimates, with either the **Completed contract** or **Percent completion revenue recognition** method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f7232-154">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="f7232-154">Additional resources</span></span>
[<span data-ttu-id="f7232-155">Artigo Configurar gestão contabilística para projetos faturáveis</span><span class="sxs-lookup"><span data-stu-id="f7232-155">Configure accounting for billable projects article</span></span>](../project-accounting/configure-accounting-billable-projects.md)

[<span data-ttu-id="f7232-156">Projetos de estimativa de receitas de preço fixo</span><span class="sxs-lookup"><span data-stu-id="f7232-156">Fixed price revenue estimate projects</span></span>](rev-rec-percentage-completion-method.md)

[<span data-ttu-id="f7232-157">Gerir estimativas de receitas</span><span class="sxs-lookup"><span data-stu-id="f7232-157">Manage revenue estimates</span></span>](rev-rec-completed-contract-method.md)

[<span data-ttu-id="f7232-158">Métodos de custo para conclusão</span><span class="sxs-lookup"><span data-stu-id="f7232-158">Cost to complete methods</span></span>](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]