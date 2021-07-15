---
title: Integração de escrita dupla no Project Operations
description: Este tópico fornece uma visão geral da integração de escrita dupla no Project Operations.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: 540b6f74d8e79116e5fdb2ceffaa4bbb487ff08f
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368445"
---
# <a name="project-operations-dual-write-integration-overview"></a><span data-ttu-id="0ef4b-103">Visão geral da Integração de escrita dupla no Project Operations</span><span class="sxs-lookup"><span data-stu-id="0ef4b-103">Project Operations dual-write integration overview</span></span>

<span data-ttu-id="0ef4b-104">_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_</span><span class="sxs-lookup"><span data-stu-id="0ef4b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="0ef4b-105">O Project Operations utiliza [capacidades de dupla escrita](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) para sincronizar dados através de Microsoft Dataverse e Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="0ef4b-105">Project Operations uses [dual-write capabilities](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) to synchronize data across Microsoft Dataverse and Dynamics 365 Finance.</span></span>

<span data-ttu-id="0ef4b-106">A seguinte ilustração mostra como os dados são sincronizados como parte desta integração entre Dataverse e finanças.</span><span class="sxs-lookup"><span data-stu-id="0ef4b-106">The following illustration shows how data is synchronized as part of this integration between Dataverse and Finance.</span></span>

![Visão geral dos fluxos de dados do Project Operations](./media/ProjectOperationsFlows.jpg)

<span data-ttu-id="0ef4b-108">O Project Operations no Dataverse fornece uma interface de utilizador moderna (UI) e fácil extensibilidade sem código/código baixo utilizando as capacidades Power Platform.</span><span class="sxs-lookup"><span data-stu-id="0ef4b-108">Project Operations on Dataverse provides a modern user interface (UI) and easy no-code/low-code extensibility using Power Platform capabilities.</span></span> <span data-ttu-id="0ef4b-109">Gestores de projetos, gestores de recursos, membros da equipa do projeto, e outras personalidades de front-office, realizam as suas atividades no Project Operations no Dataverse.</span><span class="sxs-lookup"><span data-stu-id="0ef4b-109">Project managers, Resource managers, Project team members, and other front-office personas, perform their activities in Project Operations on Dataverse.</span></span>

<span data-ttu-id="0ef4b-110">O Project Operations em Finanças proporciona apoio à contabilidade do projeto e ao reconhecimento de receitas.</span><span class="sxs-lookup"><span data-stu-id="0ef4b-110">Project Operations in Finance provides project accounting and revenue recognition support.</span></span> <span data-ttu-id="0ef4b-111">O Project Operations liga-se ao quadro financeiro das Finanças para o cálculo do imposto sobre as vendas, as taxas de câmbio, o reporte de dimensão financeira e muito mais.</span><span class="sxs-lookup"><span data-stu-id="0ef4b-111">Project Operations plugs in to the financial framework in Finance for sales tax calculation, currency exchange rates, financial dimension reporting, and more.</span></span> <span data-ttu-id="0ef4b-112">As experiências de contabilista do Projeto são maioritariamente baseadas em Finanças.</span><span class="sxs-lookup"><span data-stu-id="0ef4b-112">The Project accountant experiences are mostly based in Finance.</span></span>

<span data-ttu-id="0ef4b-113">A integração do Project Operations consiste na seguinte integração de componentes:</span><span class="sxs-lookup"><span data-stu-id="0ef4b-113">Project Operations integration consists of the following component integration:</span></span>


- [<span data-ttu-id="0ef4b-114">Configuração do Project Operations e integração de dados de configuração</span><span class="sxs-lookup"><span data-stu-id="0ef4b-114">Project Operations setup and configuration data integration</span></span>](resource-dual-write-setup-integration.md) 
- [<span data-ttu-id="0ef4b-115">Valores reais e estimativas de Projeto</span><span class="sxs-lookup"><span data-stu-id="0ef4b-115">Project estimates and actuals</span></span>](resource-dual-write-estimates-actuals.md)
- [<span data-ttu-id="0ef4b-116">Faturas do Projeto</span><span class="sxs-lookup"><span data-stu-id="0ef4b-116">Project invoices</span></span>](resource-dual-write-project-invoice.md)
- [<span data-ttu-id="0ef4b-117">Gestão de despesas</span><span class="sxs-lookup"><span data-stu-id="0ef4b-117">Expense management</span></span>](resource-dual-write-expense.md)
- [<span data-ttu-id="0ef4b-118">Fatura de fornecedor</span><span class="sxs-lookup"><span data-stu-id="0ef4b-118">Vendor invoice</span></span>](resource-dual-write-vendor-invoice.md)
