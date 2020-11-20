---
title: Descrição geral da implementação do Project Operations para cenários baseados em Recursos/Não Stock
description: Este tópico fornece informações sobre o tipo de implementação, Project Operations para cenários baseados em Recursos/Não Stock.
author: rumant
manager: Annbe
ms.date: 11/02/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 035ad22d2b51182c11e5c29d35f74f499fc903d5
ms.sourcegitcommit: d33ef0ae39f90fe3b0f6b4524f483e8052057361
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 11/03/2020
ms.locfileid: "4365580"
---
# <a name="project-operations-for-resourcenon-stocked-based-scenarios-deployment-overview"></a><span data-ttu-id="19b62-103">Descrição geral da implementação do Project Operations para cenários baseados em Recursos/Não Stock</span><span class="sxs-lookup"><span data-stu-id="19b62-103">Project Operations for resource/non-stocked based scenarios deployment overview</span></span>

<span data-ttu-id="19b62-104">_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_</span><span class="sxs-lookup"><span data-stu-id="19b62-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="19b62-105">O tipo de implementação, Dynamics 365 Project Operations para cenários baseados em Recursos/Não Stock tem as seguintes capacidades para empresas baseadas em projetos:</span><span class="sxs-lookup"><span data-stu-id="19b62-105">The deployment type, Dynamics 365 Project Operations for resource/non-stocked based scenarios has the following capabilities for project-based companies:</span></span>

- <span data-ttu-id="19b62-106">Planeamento de projetos com o Microsoft Project para a Web</span><span class="sxs-lookup"><span data-stu-id="19b62-106">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="19b62-107">Preços multidimensionais e custos para os recursos laborais</span><span class="sxs-lookup"><span data-stu-id="19b62-107">Multi-dimensional pricing and costing for labor resources</span></span>
- <span data-ttu-id="19b62-108">Preços baseados na categoria para categorias de despesas</span><span class="sxs-lookup"><span data-stu-id="19b62-108">Category-based pricing for expense categories</span></span>
- <span data-ttu-id="19b62-109">Gestão de vendas baseada em projetos utilizando capacidades do Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="19b62-109">Project-based sales management using Dynamics 365 Sales capabilities</span></span>
- <span data-ttu-id="19b62-110">Universal Resource Scheduling que se integra com outras aplicações, como o Dynamics 365 Field Service e o Dynamics 365 Customer Service</span><span class="sxs-lookup"><span data-stu-id="19b62-110">Universal resource scheduling that integrates with other applications such as Dynamics 365 Field Service and Dynamics 365 Customer Service</span></span>
- <span data-ttu-id="19b62-111">Monitorização do progresso e Tempo do Projeto</span><span class="sxs-lookup"><span data-stu-id="19b62-111">Project progress and Time Tracking</span></span>
- <span data-ttu-id="19b62-112">Experiências de gestão de Despesas básicas e completas para despesas de projeto e não projeto, incluindo a captura de recibos utilizando capacidades OCR</span><span class="sxs-lookup"><span data-stu-id="19b62-112">Basic and full Expense management experiences for project and non-project expenses including receipt capture using OCR capabilities</span></span>
- <span data-ttu-id="19b62-113">A faturação que se estende do pró-forma ao orientado para o cliente e é suportada por um sistema de taxas de vendas de classe empresarial e de taxa de câmbio eficaz.</span><span class="sxs-lookup"><span data-stu-id="19b62-113">Invoicing that extends from proforma to customer-facing and is backed by an enterprise-class sales tax and date-effective exchange rate system.</span></span>
- <span data-ttu-id="19b62-114">Custos de projeto configuráveis, perfis de receitas e regras para contabilidade e acréscimos do trabalho em curso (WIP)</span><span class="sxs-lookup"><span data-stu-id="19b62-114">Configurable project cost, revenue profiles, and rules for work in progress (WIP) accounting and accruals</span></span>
- <span data-ttu-id="19b62-115">Reconhecimento de receitas de projeto</span><span class="sxs-lookup"><span data-stu-id="19b62-115">Project revenue recognition</span></span>
- <span data-ttu-id="19b62-116">Extensibilidade através do Power Platform</span><span class="sxs-lookup"><span data-stu-id="19b62-116">Extensibility through the Power Platform</span></span>

<span data-ttu-id="19b62-117">Este tipo de implementação fornece uma extensão à funcionalidade fornecida pelas aplicações Dynamics 365 Finance e Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="19b62-117">This deployment type provides an extension to the functionality provided by Dynamics 365 Finance and Dynamics 365 Supply Chain Management applications.</span></span>

<span data-ttu-id="19b62-118">Este tipo de implementação deve ser escolhido se a expetativa do Project Operations for utilizar o ciclo de vida completo do projeto que inclui os seguintes requisitos:</span><span class="sxs-lookup"><span data-stu-id="19b62-118">This deployment should be chosen the expectation of Project Operations is to use the full project lifecycle that includes the following requirements:</span></span>

- <span data-ttu-id="19b62-119">Capacidade de gerir vendas baseadas em projetos com outros tipos de vendas utilizando as capacidades na aplicação Sales.</span><span class="sxs-lookup"><span data-stu-id="19b62-119">Ability to manage project-based sales with other types of sales using the capabilities in the Sales application.</span></span>
- <span data-ttu-id="19b62-120">Um sistema de gestão de projetos integrado que gere projetos internos e faturáveis para agendas e finanças, desde as vendas de projetos até à contabilidade.</span><span class="sxs-lookup"><span data-stu-id="19b62-120">An integrated project management system that manages internal and billable projects for schedules and financials from project sales to accounting.</span></span>
- <span data-ttu-id="19b62-121">Um sistema de gestão de despesas que inclui a aplicação de políticas e reembolsos para o acompanhamento de projetos e despesas de não projetos.</span><span class="sxs-lookup"><span data-stu-id="19b62-121">An expense management system that includes policy enforcements and reimbursements for tracking project and non-project expenses.</span></span>
- <span data-ttu-id="19b62-122">Requerem um motor de impostos de venda rico e de classe empresarial e de taxa de câmbio para gerar faturas viradas para o cliente para projetos.</span><span class="sxs-lookup"><span data-stu-id="19b62-122">Require a rich, enterprise-class sales tax and exchange rate engine to generate customer-facing invoices for projects.</span></span>
- <span data-ttu-id="19b62-123">Um sistema de reconhecimento de receitas e contabilidade de projetos em conformidade com as normas IFRS (International Financial Reporting Standards).</span><span class="sxs-lookup"><span data-stu-id="19b62-123">An International Financial Reporting Standards(IFRS)-compliant project accounting and revenue recognition system.</span></span>
- <span data-ttu-id="19b62-124">Aplicações Finance ou Supply Chain Management e integração de transações baseadas em projetos.</span><span class="sxs-lookup"><span data-stu-id="19b62-124">Finance or Supply Chain Management applications and integration of project-based transactions.</span></span>
