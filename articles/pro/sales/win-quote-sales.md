---
title: Fechar uma proposta – lite
description: Este tópico fornece informações sobre como fechar uma proposta no Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5ad206232d616cdbdc83e2a17b9177cfb98ffda9
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/30/2020
ms.locfileid: "4175725"
---
# <a name="close-a-quote---lite"></a><span data-ttu-id="caa0a-103">Fechar uma proposta – lite</span><span class="sxs-lookup"><span data-stu-id="caa0a-103">Close a quote - lite</span></span>

<span data-ttu-id="caa0a-104">_**Aplica-se a:** Implementação leve - oportunidade potencial para fatura pró-forma_</span><span class="sxs-lookup"><span data-stu-id="caa0a-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="caa0a-105">Uma proposta de projeto pode ser fechada como Ganha ou Perdida.</span><span class="sxs-lookup"><span data-stu-id="caa0a-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="caa0a-106">As operações Ativar e Rever em propostas não são suportadas no Microsoft Dynamics 365 Project Operations, pelo que uma proposta de rascunho pode ser fechada.</span><span class="sxs-lookup"><span data-stu-id="caa0a-106">The Activate and Revise operations on quotes is not supported in Microsoft Dynamics 365 Project Operations, so a draft quote can be closed.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="caa0a-107">Fechar uma proposta como Ganha</span><span class="sxs-lookup"><span data-stu-id="caa0a-107">Close a quote as Won</span></span>

<span data-ttu-id="caa0a-108">Fechar uma proposta de projeto como Ganha fechará a proposta com o estado definido como Fechado e a razão do estado definida como Ganha.</span><span class="sxs-lookup"><span data-stu-id="caa0a-108">Closing a project quote as Won will close the quote with the status set to Closed and the status reason set to Won.</span></span> <span data-ttu-id="caa0a-109">Fechar a proposta torna a proposta de projeto só de leitura e cria um contrato de projeto de rascunho que contém as informações da proposta.</span><span class="sxs-lookup"><span data-stu-id="caa0a-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="caa0a-110">Como uma proposta fechada não pode ser reaberta, existe uma caixa de diálogo de confirmação antes de as alterações serem feitas, uma vez que uma proposta fechada não pode ser reaberta e as alterações são irreversíveis.</span><span class="sxs-lookup"><span data-stu-id="caa0a-110">Because a closed quote can't be reopened, a confirmation dialog There is a confirmation dialog before the changes are done since a closed quote cannot be re-opened and the changes are irreversible.</span></span>

<span data-ttu-id="caa0a-111">Se a proposta estiver anexada a uma oportunidade, quaisquer outras propostas de projeto na oportunidade são fechadas automaticamente como Perdidas.</span><span class="sxs-lookup"><span data-stu-id="caa0a-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="caa0a-112">Impacto financeiro de fechar uma proposta como Ganha</span><span class="sxs-lookup"><span data-stu-id="caa0a-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="caa0a-113">Se tiverem existido valores reais para o tempo registado num projeto enquanto ainda está anexado a uma proposta de rascunho, só o custo do tempo ou da despesa é registado.</span><span class="sxs-lookup"><span data-stu-id="caa0a-113">If there have been any actuals for time recorded on a project while it is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="caa0a-114">Depois de uma proposta ser fechada como Ganha, a aplicação irá refatorizar os custos ao inverter os valores reais do custo mais antigos e recriar novos custos reais.</span><span class="sxs-lookup"><span data-stu-id="caa0a-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="caa0a-115">A aplicação irá processar estes valores reais de custos baseados no método de Faturação do item de contrato do projeto associado.</span><span class="sxs-lookup"><span data-stu-id="caa0a-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="caa0a-116">Se os valores reais do custo referenciarem um item de contrato de tempo e material, o sistema criará automaticamente as vendas não faturadas correspondentes para quando a proposta estiver fechada e o contrato de projeto for criado.</span><span class="sxs-lookup"><span data-stu-id="caa0a-116">If the cost actuals reference a time and material contract line, the system will automatically create corresponding unbilled sales actuals for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="caa0a-117">Se os valores reais do custo referenciam um item de contrato de preço fixo, a aplicação deixará de reprocessar os valores reais do custo baseado nas regras de faturação dividida para os clientes do contrato de projeto.</span><span class="sxs-lookup"><span data-stu-id="caa0a-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="caa0a-118">Fechar uma proposta como perdida:</span><span class="sxs-lookup"><span data-stu-id="caa0a-118">Closing a quote as lost:</span></span>

<span data-ttu-id="caa0a-119">Fechar uma proposta de projeto como Perdida definirá o estado como Fechada e a razão do estado como Perdida.</span><span class="sxs-lookup"><span data-stu-id="caa0a-119">Closing a project quote as Lost will set the status to Closed and status reason to Lost.</span></span> <span data-ttu-id="caa0a-120">Fechar a proposta faz com que a proposta de projeto seja só de leitura.</span><span class="sxs-lookup"><span data-stu-id="caa0a-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="caa0a-121">Como uma proposta fechada não pode ser reaberta e, antes de fechar uma proposta, uma caixa de diálogo de confirmação confirmará as suas alterações.</span><span class="sxs-lookup"><span data-stu-id="caa0a-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="caa0a-122">Se a proposta de projeto que está fechada como Perdida tem um projeto referenciado em qualquer uma das suas linhas, esse projeto também é marcado como Fechado e quaisquer reservas de recursos a partir desse dia são canceladas.</span><span class="sxs-lookup"><span data-stu-id="caa0a-122">If the project quote that is closed as Lost has a project referenced on any of its lines, that project is also marked as Closed and any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="caa0a-123">No Project Operations, fechar uma proposta como Ganha ou Perdida não afetará esse estado da Oportunidade, que permanecerá aberta até ser fechada manualmente.</span><span class="sxs-lookup"><span data-stu-id="caa0a-123">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>
