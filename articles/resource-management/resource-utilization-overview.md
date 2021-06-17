---
title: Descrição geral da utilização de recursos
description: Este tópico fornece informações sobre a vista de utilização de recursos no Project Operations.
author: ruhercul
ms.date: 11/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: a683931bcd6a357c5feec9198b190b948ad17a40
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000810"
---
# <a name="resource-utilization-overview"></a><span data-ttu-id="a5bcd-103">Descrição geral da utilização de recursos</span><span class="sxs-lookup"><span data-stu-id="a5bcd-103">Resource utilization overview</span></span>

<span data-ttu-id="a5bcd-104">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="a5bcd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a5bcd-105">Os recursos podem ter uma utilização faturável de destino.</span><span class="sxs-lookup"><span data-stu-id="a5bcd-105">Resources can have a target billable utilization.</span></span> <span data-ttu-id="a5bcd-106">Esta utilização de destino é definida como um atributo na função predefinida de um recurso ou definida no registo do recurso reservável individual.</span><span class="sxs-lookup"><span data-stu-id="a5bcd-106">This target utilization is defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="a5bcd-107">Os cálculos de utilização baseiam-se nas horas reais que os recursos reportaram através da utilização de entradas de tempo aprovadas.</span><span class="sxs-lookup"><span data-stu-id="a5bcd-107">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="a5bcd-108">As fórmulas que se seguem são utilizadas para calcular a utilização:</span><span class="sxs-lookup"><span data-stu-id="a5bcd-108">The following formulas are used to calculate utilization:</span></span>

  - <span data-ttu-id="a5bcd-109">Utilização faturável = Horas reais faturáveis ÷ Capacidade do recurso</span><span class="sxs-lookup"><span data-stu-id="a5bcd-109">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
  - <span data-ttu-id="a5bcd-110">Utilização não faturável = Tempo real com ID do tipo de faturação = Não faturável, Grátis ou Não disponível ÷ Capacidade do recurso</span><span class="sxs-lookup"><span data-stu-id="a5bcd-110">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
  - <span data-ttu-id="a5bcd-111">Interno = Tempo real sem contrato de vendas ÷ Capacidade do recurso</span><span class="sxs-lookup"><span data-stu-id="a5bcd-111">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
  - <span data-ttu-id="a5bcd-112">Capacidade do recurso = Horas de trabalho de recursos – Fora do escritório – Dias de descanso</span><span class="sxs-lookup"><span data-stu-id="a5bcd-112">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="a5bcd-113">Pode localizar a vista **Utilização de Recursos** no painel **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="a5bcd-113">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

<span data-ttu-id="a5bcd-114">Cada célula da grelha representa a percentagem de utilização faturável do recurso num período, tal como um dia, uma semana ou um mês.</span><span class="sxs-lookup"><span data-stu-id="a5bcd-114">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="a5bcd-115">As fórmulas que se seguem são utilizadas para colorir as células:</span><span class="sxs-lookup"><span data-stu-id="a5bcd-115">The following formulas are used to color the cells:</span></span>

  - <span data-ttu-id="a5bcd-116">**Verde**: Utilização faturável >= Utilização de destino do recurso</span><span class="sxs-lookup"><span data-stu-id="a5bcd-116">**Green**: Billable utilization >= Resource target utilization</span></span>
  - <span data-ttu-id="a5bcd-117">**Amarelo**: Utilização de destino – 20 < = Utilização faturável < Utilização de destino</span><span class="sxs-lookup"><span data-stu-id="a5bcd-117">**Yellow**: Target utilization – 20 <= Billable utilization < Target utilization</span></span>
  - <span data-ttu-id="a5bcd-118">**Vermelho**: Utilização faturável < Utilização de destino – 20</span><span class="sxs-lookup"><span data-stu-id="a5bcd-118">**Red**: Billable utilization < Target utilization – 20</span></span>

<span data-ttu-id="a5bcd-119">Uma vez a vista **Utilização de Recursos** é baseada no Quadro da Agenda, pode utilizar as capacidades de filtragem do Quadro da Agenda para filtrar os resultados.</span><span class="sxs-lookup"><span data-stu-id="a5bcd-119">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="a5bcd-120">A grelha requer que defina uma utilização de destino na função ou no recurso individual.</span><span class="sxs-lookup"><span data-stu-id="a5bcd-120">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="a5bcd-121">Para efetuar esta configuração, aceda a **Recursos** > **Funções do recurso**.</span><span class="sxs-lookup"><span data-stu-id="a5bcd-121">To do this setup, go to **Resources** > **Resource roles**.</span></span>

<span data-ttu-id="a5bcd-122">Além disso, deve ser atribuída uma função predefinida a cada recurso reservável.</span><span class="sxs-lookup"><span data-stu-id="a5bcd-122">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="a5bcd-123">Aceda a **Recursos** > **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="a5bcd-123">Go to **Resources** > **Resources**.</span></span> <span data-ttu-id="a5bcd-124">No separador **Project Service**, verifique se está definida uma função de recurso e se o campo **É Predefinição** está definido como **Sim**.</span><span class="sxs-lookup"><span data-stu-id="a5bcd-124">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field is set to **Yes**.</span></span> <span data-ttu-id="a5bcd-125">Pode adicionar funções adicionais em que **É Predefinição** = **Não**.</span><span class="sxs-lookup"><span data-stu-id="a5bcd-125">You can add additional roles where **Is Default** = **No**.</span></span> <span data-ttu-id="a5bcd-126">A função em que **É Predefinição** = **Sim** é utilizada para avaliar a utilização do recurso relativamente ao alvo dessa função.</span><span class="sxs-lookup"><span data-stu-id="a5bcd-126">The role where the **Is Default** = **Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

<span data-ttu-id="a5bcd-127">No separador **Project Service**, também pode definir uma utilização de destino individual para o recurso.</span><span class="sxs-lookup"><span data-stu-id="a5bcd-127">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="a5bcd-128">Em seguida, o cálculo da utilização utiliza essa utilização de destino para avaliar o destino do recurso em vez do destino da função predefinida do recurso.</span><span class="sxs-lookup"><span data-stu-id="a5bcd-128">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="a5bcd-129">A utilização é apenas mostrada para um recurso se esse recurso tiver aprovado, um tempo faturável durante o período mostrado na grelha.</span><span class="sxs-lookup"><span data-stu-id="a5bcd-129">Utilization is only shown for a resource if that resource has approved, chargeable time during the period shown in the grid.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]