---
title: Fechar uma proposta – lite
description: Este tópico fornece informações sobre como fechar uma proposta no Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6214e1b5bec5c9173a6b6e69578de14654da633e
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272297"
---
# <a name="close-a-quote---lite"></a><span data-ttu-id="8d1e8-103">Fechar uma proposta – lite</span><span class="sxs-lookup"><span data-stu-id="8d1e8-103">Close a quote - lite</span></span>

<span data-ttu-id="8d1e8-104">_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_</span><span class="sxs-lookup"><span data-stu-id="8d1e8-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8d1e8-105">Uma proposta de projeto pode ser fechada como Ganha ou Perdida.</span><span class="sxs-lookup"><span data-stu-id="8d1e8-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="8d1e8-106">Um rascunho de cotação pode ser fechado porque as operações de Ativação e Revisão em cotações não são suportadas no Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="8d1e8-106">A draft quote can be closed because the Activate and Revise operations on quotes isn't supported in Microsoft Dynamics 365 Project Operations.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="8d1e8-107">Fechar uma proposta como Ganha</span><span class="sxs-lookup"><span data-stu-id="8d1e8-107">Close a quote as Won</span></span>

<span data-ttu-id="8d1e8-108">Quando fecha uma citação do projeto como Ganho, o estado está definido para Fechado e o razão do estado é Ganho.</span><span class="sxs-lookup"><span data-stu-id="8d1e8-108">When you close a project quote as Won, the status is set to Closed and the status reason is Won.</span></span> <span data-ttu-id="8d1e8-109">Fechar a proposta torna a proposta de projeto só de leitura e cria um contrato de projeto de rascunho que contém as informações da proposta.</span><span class="sxs-lookup"><span data-stu-id="8d1e8-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="8d1e8-110">Uma vez que uma cotação fechada não pode ser reaberta, um diálogo de confirmação confirmará as suas alterações.</span><span class="sxs-lookup"><span data-stu-id="8d1e8-110">Because a closed quote can't be reopened, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="8d1e8-111">Se a proposta estiver anexada a uma oportunidade, quaisquer outras propostas de projeto na oportunidade são fechadas automaticamente como Perdidas.</span><span class="sxs-lookup"><span data-stu-id="8d1e8-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="8d1e8-112">Impacto financeiro de fechar uma proposta como Ganha</span><span class="sxs-lookup"><span data-stu-id="8d1e8-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="8d1e8-113">Se houver algum tempo real num projeto enquanto ainda estiver anexado a um projeto de cotação, apenas o custo do tempo ou da despesa é registado.</span><span class="sxs-lookup"><span data-stu-id="8d1e8-113">If there are any actuals for time on a project while is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="8d1e8-114">Depois de uma proposta ser fechada como Ganha, a aplicação irá refatorizar os custos ao inverter os valores reais do custo mais antigos e recriar novos custos reais.</span><span class="sxs-lookup"><span data-stu-id="8d1e8-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="8d1e8-115">A aplicação irá processar estes valores reais de custos baseados no método de Faturação do item de contrato do projeto associado.</span><span class="sxs-lookup"><span data-stu-id="8d1e8-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="8d1e8-116">Se os resultados de custo referem uma linha de contrato de tempo e material, os correspondentes resultados de vendas não faturados são criados para quando a cotação é fechada e o contrato do projeto é criado.</span><span class="sxs-lookup"><span data-stu-id="8d1e8-116">If the cost actuals reference a time and material contract line, corresponding unbilled sales actuals are created for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="8d1e8-117">Se os custos reais referem uma linha de contrato de preço fixo, a aplicação deixará de reprocessar os custos reais que se baseiam nas regras de faturação divididas para os clientes do contrato de projeto.</span><span class="sxs-lookup"><span data-stu-id="8d1e8-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals that are based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="8d1e8-118">Fechar uma proposta como perdida:</span><span class="sxs-lookup"><span data-stu-id="8d1e8-118">Closing a quote as lost:</span></span>

<span data-ttu-id="8d1e8-119">Quando fecha uma citação do projeto como Perdido, o estado está definido para Fechado e o razão do estado é Perdido.</span><span class="sxs-lookup"><span data-stu-id="8d1e8-119">When you close a project quote as Lost, the status is set to Closed and status reason is Lost.</span></span> <span data-ttu-id="8d1e8-120">Fechar a proposta faz com que a proposta de projeto seja só de leitura.</span><span class="sxs-lookup"><span data-stu-id="8d1e8-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="8d1e8-121">Como uma proposta fechada não pode ser reaberta e, antes de fechar uma proposta, uma caixa de diálogo de confirmação confirmará as suas alterações.</span><span class="sxs-lookup"><span data-stu-id="8d1e8-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="8d1e8-122">Se a citação do projeto que está fechada como Perdido refere um projeto em qualquer uma das suas linhas, esse projeto também é marcado como Perdido.</span><span class="sxs-lookup"><span data-stu-id="8d1e8-122">If the project quote that is closed as Lost references a project on any of its lines, that project is also marked as Closed.</span></span> <span data-ttu-id="8d1e8-123">Quaisquer reservas de recursos a partir desse dia são canceladas.</span><span class="sxs-lookup"><span data-stu-id="8d1e8-123">Any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="8d1e8-124">No Project Operations, fechar uma proposta como Ganha ou Perdida não afetará esse estado da Oportunidade, que permanecerá aberta até ser fechada manualmente.</span><span class="sxs-lookup"><span data-stu-id="8d1e8-124">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]