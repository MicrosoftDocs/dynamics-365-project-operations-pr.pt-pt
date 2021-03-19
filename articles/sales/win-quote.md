---
title: Fechar uma proposta
description: Este tópico fornece informações sobre como fechar propostas no Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a2c752ba6395ed4bf025092219350dc245f7428f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277262"
---
# <a name="close-a-quote"></a><span data-ttu-id="642c9-103">Fechar uma proposta</span><span class="sxs-lookup"><span data-stu-id="642c9-103">Close a quote</span></span>

<span data-ttu-id="642c9-104">_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_</span><span class="sxs-lookup"><span data-stu-id="642c9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="642c9-105">Uma proposta de projeto pode ser fechada como Ganha ou Perdida.</span><span class="sxs-lookup"><span data-stu-id="642c9-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="642c9-106">Uma vez que as funções de Ativação e Revisão não são suportadas em propostas no Microsoft Dynamics 365 Project Operations, pode fechar uma proposta de rascunho.</span><span class="sxs-lookup"><span data-stu-id="642c9-106">Because the functions Activate and Revise are not supported on quotes in Microsoft Dynamics 365 Project Operations, you can close a draft quote.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="642c9-107">Fechar uma proposta como Ganha</span><span class="sxs-lookup"><span data-stu-id="642c9-107">Close a quote as Won</span></span>

<span data-ttu-id="642c9-108">Fechar uma proposta de projeto como Ganha definirá o estado da proposta como **Fechada** e a razão do estado como **Ganha**.</span><span class="sxs-lookup"><span data-stu-id="642c9-108">Closing a project quote as Won will set the status of the quote to **Closed** and status reason to **Won**.</span></span> <span data-ttu-id="642c9-109">Fechar as propostas torna-as só de leitura e cria um contrato de projeto de rascunho com todas as informações da proposta.</span><span class="sxs-lookup"><span data-stu-id="642c9-109">Closing the quotes makes it read-only and creates a draft project contract with all the quote information.</span></span> <span data-ttu-id="642c9-110">Como uma proposta fechada não pode ser reaberta, antes de fechar uma proposta, uma caixa de diálogo de confirmação confirmará as suas alterações.</span><span class="sxs-lookup"><span data-stu-id="642c9-110">Because a closed quote can't be reopened, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="642c9-111">O contrato de projeto criado a partir de uma proposta de projeto também é disponibilizado no módulo Gestão de projetos e contabilística do Project Operations.</span><span class="sxs-lookup"><span data-stu-id="642c9-111">The project contract created from a project quote is also made available in the Project management and accounting module of Project Operations.</span></span> <span data-ttu-id="642c9-112">Se um contrato de projeto não for mapeado para um projeto em nenhuma das suas linhas, este contrato de projeto será disponibilizado como um contrato de projeto inativo e torna-se ativo assim que um projeto é mapeado para, pelo menos, um dos seus itens de contrato.</span><span class="sxs-lookup"><span data-stu-id="642c9-112">If a project contract is not mapped to a project on any of its lines, this project contract is made available as an inactive project contract and becomes active as soon as a project is mapped to at least one of its contract lines.</span></span>

<span data-ttu-id="642c9-113">Se a proposta estiver anexada a uma oportunidade, quaisquer outras propostas de projeto na oportunidade são fechadas automaticamente como Perdidas.</span><span class="sxs-lookup"><span data-stu-id="642c9-113">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="642c9-114">Impacto financeiro de fechar uma proposta como Ganha</span><span class="sxs-lookup"><span data-stu-id="642c9-114">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="642c9-115">Se tiverem existido valores reais para o tempo registado num projeto enquanto ainda está anexado a uma proposta de rascunho, só o custo do tempo ou da despesa é registado.</span><span class="sxs-lookup"><span data-stu-id="642c9-115">If there have been any actuals for time recorded on a project while it is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="642c9-116">Depois de uma proposta ser fechada como Ganha, a aplicação irá refatorizar os custos ao inverter os valores reais do custo mais antigos e recriar novos custos reais.</span><span class="sxs-lookup"><span data-stu-id="642c9-116">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="642c9-117">A aplicação irá processar estes valores reais de custos baseados no método de Faturação do item de contrato do projeto associado.</span><span class="sxs-lookup"><span data-stu-id="642c9-117">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="642c9-118">Se os valores reais do custo referenciarem um item de contrato de tempo e material, o sistema criará automaticamente as vendas não faturadas correspondentes para quando a proposta estiver fechada e o contrato de projeto for criado.</span><span class="sxs-lookup"><span data-stu-id="642c9-118">If the cost actuals reference a time and material contract line, the system will automatically create corresponding unbilled sales actuals for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="642c9-119">Se os valores reais do custo referenciam um item de contrato de preço fixo, a aplicação deixará de reprocessar os valores reais do custo baseado nas regras de faturação dividida para os clientes do contrato de projeto.</span><span class="sxs-lookup"><span data-stu-id="642c9-119">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals based on the split billing rules for the project contract customers.</span></span>

<span data-ttu-id="642c9-120">Todos os valores reais reprocessados estão disponíveis no módulo Gestão de projetos e contabilística para a Gestão contabilística do projeto rever, atualizar e lançar no Razão geral.</span><span class="sxs-lookup"><span data-stu-id="642c9-120">All reprocessed actuals are available in the Project management and accounting module for the Project accountant to review, update, and post to the General ledger.</span></span> 

## <a name="close-a-quote-as-lost"></a><span data-ttu-id="642c9-121">Fechar uma proposta como Perdida</span><span class="sxs-lookup"><span data-stu-id="642c9-121">Close a quote as Lost</span></span>

<span data-ttu-id="642c9-122">Fechar uma proposta de projeto como Perdida definirá o estado como **Fechada** e a razão do estado como **Perdida**.</span><span class="sxs-lookup"><span data-stu-id="642c9-122">Closing a project quote as Lost will set the status to **Closed** and status reason to **Lost**.</span></span> <span data-ttu-id="642c9-123">Fechar a proposta torna-a só de leitura.</span><span class="sxs-lookup"><span data-stu-id="642c9-123">Closing the quote makes it read-only.</span></span> <span data-ttu-id="642c9-124">Como uma proposta fechada não pode ser reaberta e, antes de fechar uma proposta, uma caixa de diálogo de confirmação confirmará as suas alterações.</span><span class="sxs-lookup"><span data-stu-id="642c9-124">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="642c9-125">Se a proposta de projeto que está fechada como Perdida tem um projeto referenciado em qualquer uma das suas linhas, esse projeto também é marcado como Fechado e quaisquer reservas de recursos a partir desse dia são canceladas.</span><span class="sxs-lookup"><span data-stu-id="642c9-125">If the project quote that is closed as Lost has a project referenced on any of its lines, that project is also marked as Closed and any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="642c9-126">No Project Operations, fechar uma proposta como Ganha ou Perdida não afetará esse estado da Oportunidade, que permanecerá aberta até ser fechada manualmente.</span><span class="sxs-lookup"><span data-stu-id="642c9-126">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]