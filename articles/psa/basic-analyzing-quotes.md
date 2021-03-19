---
title: Análise de propostas do projeto
description: Este tópico fornece informações sobre a análise de propostas do projeto.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: d1b79a61147bfccf13b0a33179464af91b45121e
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291273"
---
# <a name="analysis-of-project-quotes"></a><span data-ttu-id="a9c12-103">Análise de propostas do projeto</span><span class="sxs-lookup"><span data-stu-id="a9c12-103">Analysis of project quotes</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="a9c12-104">O Dynamics 365 Project Service Automation analisa as propostas do projeto para estimar a rentabilidade.</span><span class="sxs-lookup"><span data-stu-id="a9c12-104">Dynamics 365 Project Service Automation analyzes project quotes to estimate profitability.</span></span> <span data-ttu-id="a9c12-105">Também analisa como a proposta está alinhada com as expectativas do cliente sobre a data de entrega ou a data de conclusão, bem como sobre o orçamento.</span><span class="sxs-lookup"><span data-stu-id="a9c12-105">It also analyzes how well the quote is aligned with customer expectations about the delivery date or completion date, and about the budget.tions.</span></span>

## <a name="profitability-analysis"></a><span data-ttu-id="a9c12-106">Análise de rentabilidade</span><span class="sxs-lookup"><span data-stu-id="a9c12-106">Profitability analysis</span></span>

<span data-ttu-id="a9c12-107">O Project Service Automation analisa a rentabilidade utilizando a margem bruta e a margem bruta ajustada.</span><span class="sxs-lookup"><span data-stu-id="a9c12-107">Project Service Automation analyzes profitability by using the gross margin and the adjusted gross margin.</span></span>

- <span data-ttu-id="a9c12-108">As margens brutas são calculadas utilizando a seguinte fórmula:</span><span class="sxs-lookup"><span data-stu-id="a9c12-108">Gross margins are calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- <span data-ttu-id="a9c12-109">A margem bruta ajustada é calculada utilizando a seguinte fórmula:</span><span class="sxs-lookup"><span data-stu-id="a9c12-109">The adjusted gross margin is calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

<span data-ttu-id="a9c12-110">Se os valores para a margem bruta e a margem bruta ajustada forem diferentes por uma margem ampla, a maior parte do trabalho na proposta é classificada como não faturável.</span><span class="sxs-lookup"><span data-stu-id="a9c12-110">If the values for gross margin and adjusted gross margin differ by a wide margin, much of the work in the quote is classified as non-chargeable.</span></span>

## <a name="analysis-of-customer-expectations"></a><span data-ttu-id="a9c12-111">Análise das expectativas do cliente</span><span class="sxs-lookup"><span data-stu-id="a9c12-111">Analysis of customer expectations</span></span>

<span data-ttu-id="a9c12-112">Pode analisar as propostas e gerar gráficos para obter as expectativas do cliente sobre a agenda e o orçamento se introduzir valores nos seguintes campos:</span><span class="sxs-lookup"><span data-stu-id="a9c12-112">You can analyze quotes and generate charts for customer expectations about the schedule and budget if you enter values for the following fields:</span></span>

- <span data-ttu-id="a9c12-113">O campo **Data de entrega pretendida** no cabeçalho da proposta.</span><span class="sxs-lookup"><span data-stu-id="a9c12-113">The **Requested delivery date** field on the quote header.</span></span>
- <span data-ttu-id="a9c12-114">O campo **Orçamento do cliente** para cada linha de proposta (para linhas baseadas em projetos e linhas baseadas em produtos).</span><span class="sxs-lookup"><span data-stu-id="a9c12-114">The **Customer budget** field for each quote line (for project-based lines and product-based lines).</span></span>

<span data-ttu-id="a9c12-115">A análise das expectativas do cliente sobre a agenda é efetuada comparando a data de fim mais recente do detalhe da linha de proposta com a data de entrega pretendida em todas as linhas de proposta na proposta.</span><span class="sxs-lookup"><span data-stu-id="a9c12-115">Analysis of customer expectations about the schedule is done by comparing the latest end date of the quote line detail with the requested delivery date across all quote lines in the quote.</span></span>

<span data-ttu-id="a9c12-116">A análise das expectativas do cliente sobre o orçamento é efetuada através da comparação da soma do orçamento total do cliente com o montante proposto em todas as linhas de proposta.</span><span class="sxs-lookup"><span data-stu-id="a9c12-116">Analysis of customer expectations about the budget is done by comparing the sum of the total customer budget with the quoted amount across all quote lines.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]