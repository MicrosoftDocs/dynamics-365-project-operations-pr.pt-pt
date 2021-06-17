---
title: Confirmar um contrato de projeto
description: Este tópico fornece informação sobre como confirmar um contrato no Project Operations.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b5eabcad028a8282f552f3571b170d9b933a7b88
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003690"
---
# <a name="confirm-a-project-contract"></a><span data-ttu-id="47877-103">Confirmar um contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="47877-103">Confirm a project contract</span></span>

<span data-ttu-id="47877-104">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="47877-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="47877-105">Um contrato de projeto em Dynamics 365 Project Operations pode ser ativo com uma razão de **Confirmado**, ou fechado com uma razão de **Perdido**.</span><span class="sxs-lookup"><span data-stu-id="47877-105">A project contract in Dynamics 365 Project Operations can be active with a reason of **Confirmed**, or closed with a reason of **Lost**.</span></span> <span data-ttu-id="47877-106">Quando confirma um contrato de projeto, o estado atualiza-se de **Rascunho** para **Ativo** e a razão do estado é **Confirmado**.</span><span class="sxs-lookup"><span data-stu-id="47877-106">When you confirm a project contract, the status updates from **Draft** to **Active** and the status reason is **Confirmed**.</span></span> <span data-ttu-id="47877-107">Um contrato ativo ou fechado não pode ser editado ou reaberto.</span><span class="sxs-lookup"><span data-stu-id="47877-107">An active or closed contract can't be edited or reopened.</span></span> 

### <a name="financial-impact-of-confirming-a-project-contract"></a><span data-ttu-id="47877-108">Impacto financeiro da confirmação de um contrato de projeto</span><span class="sxs-lookup"><span data-stu-id="47877-108">Financial impact of confirming a project contract</span></span>

<span data-ttu-id="47877-109">Depois de um contrato de projeto ser confirmado, a aplicação recalcula os custos ao inverter os valores reais do custo mais antigos e criar novos custos reais.</span><span class="sxs-lookup"><span data-stu-id="47877-109">After a project contract is confirmed, the application recalculates the costs by reversing the older cost actuals and creating new cost actuals.</span></span> <span data-ttu-id="47877-110">Os novos valores reais de custos são processados com base no método de faturação do item de contrato do projeto associado.</span><span class="sxs-lookup"><span data-stu-id="47877-110">The new cost actuals are then processed based on the billing method of the associated project contract line.</span></span> <span data-ttu-id="47877-111">Se os valores reais de custo fizerem referência um item de contrato de Tempo e Material, a aplicação recria automaticamente os valores reais de vendas não faturados correspondentes.</span><span class="sxs-lookup"><span data-stu-id="47877-111">If the cost actuals reference a Time and Material contract line, the application automatically re-creates corresponding unbilled sales actuals.</span></span> <span data-ttu-id="47877-112">Se os valores reais de custo fizerem referência a um item de contrato de Preço Fixo, a aplicação para de reprocessar os valores reais do custo.</span><span class="sxs-lookup"><span data-stu-id="47877-112">If the cost actuals reference a Fixed Price contract line, the application stops reprocessing the cost actuals.</span></span>

<span data-ttu-id="47877-113">Os limites A Não Exceder, a configuração de capacidade da faturação e os preços e custos sobre de valores reais é avaliado e, em seguida, atualizado como parte do processo de confirmação.</span><span class="sxs-lookup"><span data-stu-id="47877-113">Not-to-exceed limits, chargeability setup, and pricing and costing on the actuals is evaluated and then updated as part of the confirmations process.</span></span>

## <a name="close-a-project-contract-as-lost"></a><span data-ttu-id="47877-114">Fechar um contrato de projeto como perdido</span><span class="sxs-lookup"><span data-stu-id="47877-114">Close a project contract as lost</span></span>

<span data-ttu-id="47877-115">Quando fecha um contrato de projeto como perdido, o estado do contrato é atualizado para **Fechado** e a razão do estado é **Perdido**.</span><span class="sxs-lookup"><span data-stu-id="47877-115">When you close a project contract as lost, the contract status is updated to **Closed** and the status reason is **Lost**.</span></span> <span data-ttu-id="47877-116">O contrato do projeto torna-se apenas de leitura.</span><span class="sxs-lookup"><span data-stu-id="47877-116">The project contract becomes read-only.</span></span> <span data-ttu-id="47877-117">Um diálogo de confirmação é fornecido antes das alterações estarem completas porque não é possível reabrir um contrato de projeto fechado.</span><span class="sxs-lookup"><span data-stu-id="47877-117">A confirmation dialog is provided before the changes are complete because you can't reopen a closed project contract.</span></span>

<span data-ttu-id="47877-118">Se o contrato de projeto que está fechado como referências perdidas um projeto nas suas linhas, esse projeto também é marcado como fechado.</span><span class="sxs-lookup"><span data-stu-id="47877-118">If the project contract that is closed as lost references a project on its lines, that project is also marked as closed.</span></span> <span data-ttu-id="47877-119">Quaisquer reservas de recursos a partir desse dia são canceladas.</span><span class="sxs-lookup"><span data-stu-id="47877-119">Any resource bookings from that day forward are canceled.</span></span> <span data-ttu-id="47877-120">Quaisquer valores reais de vendas não faturados no contrato do projeto que ainda não estejam numa fatura, serão invertidos.</span><span class="sxs-lookup"><span data-stu-id="47877-120">Any unbilled sales actuals on the project contract that aren't already on an invoice, will be reversed.</span></span>

> [!NOTE]
> <span data-ttu-id="47877-121">Em Dynamics 365 Project Operations, fechar um contrato de projeto como perdido não terá impacto nesse estatuto da oportunidade associada.</span><span class="sxs-lookup"><span data-stu-id="47877-121">In Dynamics 365 Project Operations, closing a project contract as lost will not impact that status of the associated opportunity.</span></span> <span data-ttu-id="47877-122">A oportunidade permanecerá aberta e deve ser fechada manualmente.</span><span class="sxs-lookup"><span data-stu-id="47877-122">The opportunity will remain open and must be manually closed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]