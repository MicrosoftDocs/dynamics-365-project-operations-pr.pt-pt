---
title: Descrição geral da faturação interempresa
description: Este tópico fornece informações e exemplos sobre a faturação interempresa para projetos.
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 3ad75089de1a2f99646f7aba213e199a2bec347d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287342"
---
# <a name="intercompany-invoicing-overview"></a><span data-ttu-id="5e5f2-103">Descrição geral da faturação interempresa</span><span class="sxs-lookup"><span data-stu-id="5e5f2-103">Intercompany invoicing overview</span></span>

<span data-ttu-id="5e5f2-104">_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_</span><span class="sxs-lookup"><span data-stu-id="5e5f2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="5e5f2-105">A sua organização pode ter múltiplas divisões, subsidiárias e outras entidades jurídicas que transferem produtos e serviços entre si para projetos.</span><span class="sxs-lookup"><span data-stu-id="5e5f2-105">Your organization might have multiple divisions, subsidiaries, and other legal entities that transfer products and services to each other for projects.</span></span> <span data-ttu-id="5e5f2-106">A entidade legal que presta o serviço ou produto é denominada *entidade legal de concessão*.</span><span class="sxs-lookup"><span data-stu-id="5e5f2-106">The legal entity that provides the service or product is called the *lending legal entity*.</span></span> <span data-ttu-id="5e5f2-107">A entidade legal que recebe o serviço ou produto é denominada *entidade legal de contração*.</span><span class="sxs-lookup"><span data-stu-id="5e5f2-107">The legal entity that receives the service or product is called the *borrowing legal entity*.</span></span>

<span data-ttu-id="5e5f2-108">A seguinte ilustração mostra um cenário típico em que duas entidades legais, a Contoso Robotics USA (entidade legal de contração) e a Contoso Robotics UK (entidade legal de concessão) partilham recursos para entregar um projeto para o cliente, a Adventure Works.</span><span class="sxs-lookup"><span data-stu-id="5e5f2-108">The following illustration shows a typical scenario where two legal entities, Contoso Robotics USA (the borrowing legal entity) and Contoso Robotics UK (the lending legal entity) share resources to deliver a project for the customer, Adventure works.</span></span> <span data-ttu-id="5e5f2-109">Para este cenário, a Contoso Robotics USA está contratada para entregar o trabalho à Adventure Works.</span><span class="sxs-lookup"><span data-stu-id="5e5f2-109">For this scenario, Contoso Robotics USA is contracted to deliver the work to Adventure Works.</span></span>

![Faturação entre empresas](./media/IntercompanyScenario.png) 

<span data-ttu-id="5e5f2-111">O Dynamics 365 Project Operations utiliza o seguinte fluxo para processar transações interempresa:</span><span class="sxs-lookup"><span data-stu-id="5e5f2-111">Dynamics 365 Project Operations uses the following flow to process intercompany transactions:</span></span>

1. <span data-ttu-id="5e5f2-112">Os recursos da entidade legal de concessão registam o tempo ou as transações de despesas interempresa através da reserva de tempo e despesas contra projetos na entidade legal de contração.</span><span class="sxs-lookup"><span data-stu-id="5e5f2-112">Resources from the lending legal entity record intercompany time or expense transactions by booking time and expense against projects in the borrowing legal entity.</span></span>
2. <span data-ttu-id="5e5f2-113">Os custos de tempo e despesa são registados na empresa de concessão utilizando a lista de preços de custo de unidade da empresa de contração.</span><span class="sxs-lookup"><span data-stu-id="5e5f2-113">Time and expense costs are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
3. <span data-ttu-id="5e5f2-114">As transações de venda não faturadas interempresa são registadas na empresa de concessão utilizando a lista de preços de custo de unidade da empresa de contração.</span><span class="sxs-lookup"><span data-stu-id="5e5f2-114">Intercompany unbilled sale transactions are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
4. <span data-ttu-id="5e5f2-115">As receitas não faturadas são registadas na empresa de contração utilizando a lista de preços de vendas do contrato de projeto.</span><span class="sxs-lookup"><span data-stu-id="5e5f2-115">Unbilled revenue is recorded in the borrowing company using the project contract sales price list.</span></span> <span data-ttu-id="5e5f2-116">O cliente pode ser cobrado quando as receitas não faturadas são registadas.</span><span class="sxs-lookup"><span data-stu-id="5e5f2-116">The customer can be billed when unbilled revenue is recorded.</span></span> <span data-ttu-id="5e5f2-117">O cliente não tem de esperar até que o processamento da faturas interempresa esteja completo.</span><span class="sxs-lookup"><span data-stu-id="5e5f2-117">The customer doesn't have to wait until intercompany invoice processing is complete.</span></span>
5. <span data-ttu-id="5e5f2-118">As faturas de clientes interempresa são criadas periodicamente na empresa de concessão.</span><span class="sxs-lookup"><span data-stu-id="5e5f2-118">Intercompany customer invoices are created on a periodic basis in the lending company.</span></span> <span data-ttu-id="5e5f2-119">As faturas são criadas manualmente ou utilizando um processo automatizado periódico.</span><span class="sxs-lookup"><span data-stu-id="5e5f2-119">The invoices are created manually or by using a periodic automated process.</span></span> <span data-ttu-id="5e5f2-120">Uma única fatura pode ser criada para cada entidade legal de contração ou faturas separadas podem ser criadas por projeto.</span><span class="sxs-lookup"><span data-stu-id="5e5f2-120">A single invoice can be created for each borrowing legal entity or separate invoices can be created by project.</span></span>
6. <span data-ttu-id="5e5f2-121">Quando a fatura de cliente interempresa é publicada na entidade legal de concessão, a fatura de fornecedor correspondente é criada na entidade legal de contração.</span><span class="sxs-lookup"><span data-stu-id="5e5f2-121">When the intercompany customer invoice is posted in the lending legal entity, the corresponding pending vendor invoice is created in the borrowing legal entity.</span></span> <span data-ttu-id="5e5f2-122">Os custos na fatura de fornecedor pendente serão registados no sub-livro razão do projeto quando a fatura for publicada.</span><span class="sxs-lookup"><span data-stu-id="5e5f2-122">The costs in the pending vendor invoice will be recorded to the project subledger when the invoice is posted.</span></span>

<span data-ttu-id="5e5f2-123">O diagrama que se segue ilustra a faturação interempresa no que diz respeito a eventos contabilísticos e publicações esperadas no livro razão geral.</span><span class="sxs-lookup"><span data-stu-id="5e5f2-123">The following diagram illustrates intercompany invoicing as it relates to accounting events and expected postings to the general ledger.</span></span>

![Fluxo interempresa](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a><span data-ttu-id="5e5f2-125">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="5e5f2-125">Additional resources</span></span>

- [<span data-ttu-id="5e5f2-126">Configurar faturação interempresa</span><span class="sxs-lookup"><span data-stu-id="5e5f2-126">Configure intercompany invoicing</span></span>](configure-intercompany-invoicing.md)
- [<span data-ttu-id="5e5f2-127">Registar transações interempresa</span><span class="sxs-lookup"><span data-stu-id="5e5f2-127">Record intercompany transactions</span></span>](create-intercompany-transactions.md)
- [<span data-ttu-id="5e5f2-128">Criar faturas de clientes e fornecedores interempresa</span><span class="sxs-lookup"><span data-stu-id="5e5f2-128">Create intercompany customer and vendor invoices</span></span>](create-intercompany-customer-vendor-invoices.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]