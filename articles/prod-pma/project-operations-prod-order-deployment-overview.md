---
title: Descrição geral da implementação do Project Operations para cenários baseados em Stock/Produção
description: Este tópico fornece informações sobre o tipo de implementação, Project Operations para cenários baseados em Stock/Produção.
author: rumant
manager: Annbe
ms.date: 11/02/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7bad4de10a508f0c1aa2cc6bb0c41081f81fb259
ms.sourcegitcommit: d33ef0ae39f90fe3b0f6b4524f483e8052057361
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 11/03/2020
ms.locfileid: "4365583"
---
# <a name="project-operations-for-stockedproduction-based-scenarios-deployment-overview"></a><span data-ttu-id="f7686-103">Descrição geral da implementação do Project Operations para cenários baseados em Stock/Produção</span><span class="sxs-lookup"><span data-stu-id="f7686-103">Project Operations for stocked/production-based scenarios deployment overview</span></span>

<span data-ttu-id="f7686-104">_**Aplica-se a:** Project Operations para cenários baseados em Stock/Produção_</span><span class="sxs-lookup"><span data-stu-id="f7686-104">_**Applies To:** Project Operations for stocked/production-based scenarios_</span></span>


<span data-ttu-id="f7686-105">Este tipo de implementação tem as seguintes capacidades para empresas baseadas em projetos:</span><span class="sxs-lookup"><span data-stu-id="f7686-105">This deployment type has the following capabilities for project-based companies:</span></span>

- <span data-ttu-id="f7686-106">Planeamento de projetos utilizando a [Estrutura hierárquica do trabalho](work-breakdown-structures.md)</span><span class="sxs-lookup"><span data-stu-id="f7686-106">Project planning using the [Work breakdown structures](work-breakdown-structures.md)</span></span>
- <span data-ttu-id="f7686-107">Adquirir e consumir inventário armazenado para projetos</span><span class="sxs-lookup"><span data-stu-id="f7686-107">Procure and consume stocked inventory for projects</span></span>
- <span data-ttu-id="f7686-108">Gerir vendas baseadas em projetos utilizando o módulo **Vendas e marketing** em aplicações Dynamics 365 Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f7686-108">Managing project-based sales using the **Sales and marketing** module in Dynamics 365 Finance and Operations apps</span></span>
- <span data-ttu-id="f7686-109">Preços do projeto e custos usando a taxa de custos e configurações da taxa de fatura em aplicações Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f7686-109">Project pricing and costing using the cost rate and bill rate configurations in Finance and Operations apps</span></span>
- <span data-ttu-id="f7686-110">Gestão de recursos para projetos em aplicações Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f7686-110">Resource management for projects in Finance and Operations apps</span></span>
- <span data-ttu-id="f7686-111">Monitorização do progresso e tempo do projeto em aplicações Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f7686-111">Project progress and time tracking in Finance and Operations apps</span></span>
- <span data-ttu-id="f7686-112">Experiências de gestão de despesas para despesas de projeto e não projeto com a captura de recibos utilizando capacidades OCR</span><span class="sxs-lookup"><span data-stu-id="f7686-112">Expense management experiences for project and non-project expenses with receipt capture using OCR capabilities</span></span>
- <span data-ttu-id="f7686-113">Faturação utilizando um sistema de taxas de venda e de câmbio com eficácia de data de classe empresarial</span><span class="sxs-lookup"><span data-stu-id="f7686-113">Invoicing using an enterprise-class sales tax and date-effective exchange rates system</span></span>
- <span data-ttu-id="f7686-114">Grupos de projetos configuráveis para contabilidade e acréscimos WIP</span><span class="sxs-lookup"><span data-stu-id="f7686-114">Configurable project groups for WIP accounting and accruals</span></span>
- <span data-ttu-id="f7686-115">Reconhecimento de receitas de projeto</span><span class="sxs-lookup"><span data-stu-id="f7686-115">Project revenue recognition</span></span>

<span data-ttu-id="f7686-116">Este tipo de implementação também fornece uma extensão à funcionalidade fornecida pelas aplicações Dynamics 365 Finance e Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f7686-116">This deployment type also provides an extension to the functionality provided by the Dynamics 365 Finance and Dynamics 365 Supply Chain Management applications.</span></span>

<span data-ttu-id="f7686-117">Selecione este tipo de implementação para utilizar o Dynamics 365 Project Operations para o ciclo de vida completo do projeto, incluindo os seguintes requisitos chave:</span><span class="sxs-lookup"><span data-stu-id="f7686-117">Select this deployment type to use Dynamics 365 Project Operations for the full project lifecycle, including the following key requirements:</span></span>

- <span data-ttu-id="f7686-118">Um sistema de Gestão de projetos extenso que gere itens inventariados e custos de encomendas de tarefas/produção para projetos internos e faturáveis para agendas e itens financeiros.</span><span class="sxs-lookup"><span data-stu-id="f7686-118">An extensive Project management system that manages inventoried items and job/production order costing for internal and billable projects for schedules and financials.</span></span>
- <span data-ttu-id="f7686-119">A organização já tem as aplicações Dynamics 365 Finance ou Dynamics 365 Supply Chain and Manufacturing e integrar transações baseadas em projetos irá simplificar as necessidades de acesso a dados e relatórios.</span><span class="sxs-lookup"><span data-stu-id="f7686-119">The organization already has Dynamics 365 Finance or Dynamics 365 Supply Chain and Manufacturing apps and integrating project-based transactions will simplify data access and reporting needs.</span></span>
- <span data-ttu-id="f7686-120">Um sistema de gestão de despesas totalmente funcional que inclui a aplicação de políticas e reembolsos para o acompanhamento de projetos e despesas de não projecos.</span><span class="sxs-lookup"><span data-stu-id="f7686-120">A fully functional Expense management system that includes policy enforcements and reimbursements for tracking project and non-project expenses.</span></span>
- <span data-ttu-id="f7686-121">Um motor de impostos de venda rico e de classe empresarial e de taxa de câmbio para gerar faturas viradas para o cliente para projetos.</span><span class="sxs-lookup"><span data-stu-id="f7686-121">An enterprise-class sales tax and exchange rate engine to generate customer-facing invoices for projects.</span></span>
- <span data-ttu-id="f7686-122">Um sistema de reconhecimento de receitas e contabilidade de projetos em conformidade com as normas IFRS (International Financial Reporting Standards).</span><span class="sxs-lookup"><span data-stu-id="f7686-122">An International Financial Reporting Standards(IFRS)-compliant project accounting and revenue recognition system.</span></span>

