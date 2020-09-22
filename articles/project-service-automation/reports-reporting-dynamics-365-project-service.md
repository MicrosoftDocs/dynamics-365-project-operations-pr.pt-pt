---
title: Home page de geração de relatórios
description: Este tópico fornece informações sobre a geração de relatórios no Dynamics 365 Project Service Automation.
author: ruhercul
manager: kfend
ms.service: dynamics-365-projectservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: ee9bdfc6-123d-4146-8706-eab76fa37b5f
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 42e24f42fd80b445718f81f4ff40e52c8cdaa7ba
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754588"
---
# <a name="reporting-home-page"></a><span data-ttu-id="930f4-103">Home page de geração de relatórios</span><span class="sxs-lookup"><span data-stu-id="930f4-103">Reporting home page</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="930f4-104">O Microsoft Dynamics 365 Project Service Automation permite que as organizações baseadas em projetos gerem com eficiência as operações dos seus negócios.</span><span class="sxs-lookup"><span data-stu-id="930f4-104">Microsoft Dynamics 365 Project Service Automation lets project-based organizations efficiently manage the operations of their business.</span></span> <span data-ttu-id="930f4-105">Em qualquer projeto, os membros da equipa devem gerir a oportunidade, a proposta e planear o trabalho, fornecer recursos aos projetos, gerir o trabalho de acordo com o plano, cobrar pelo trabalho e, em seguida, realizar o trabalho para concluir o projeto.</span><span class="sxs-lookup"><span data-stu-id="930f4-105">On any project, team members must manage the opportunity, quote and plan the work, resource the projects, manage the work according to the plan, bill for the work, and then do the work to complete the project.</span></span> <span data-ttu-id="930f4-106">A capacidade de gerar relatórios sobre operações é a chave que determina o estado de funcionamento da organização e tomar as ações corretivas necessárias.</span><span class="sxs-lookup"><span data-stu-id="930f4-106">The ability to report on operations is key to determining the health of the organization and taking any corrective action that's required.</span></span> <span data-ttu-id="930f4-107">O PSA utiliza os métodos e as tecnologias de geração de relatórios do Microsoft Dynamics 365 para todos os relatórios.</span><span class="sxs-lookup"><span data-stu-id="930f4-107">PSA uses Microsoft Dynamics 365 reporting methods and technologies for all its reporting.</span></span> <span data-ttu-id="930f4-108">Para mais informações sobre as opções para relatórios, consulte o [Guia de escrita de relatórios para Dynamics 365 Customer Engagement (on-premises), versão 9](../analytics/reporting-analytics-with-dynamics-365.md).</span><span class="sxs-lookup"><span data-stu-id="930f4-108">For more information about the options for reporting, see the [Report writing guide for Dynamics 365 Customer Engagement (on-premises), version 9](../analytics/reporting-analytics-with-dynamics-365.md).</span></span>

## <a name="report-wizard"></a><span data-ttu-id="930f4-109">Assistente de Relatórios</span><span class="sxs-lookup"><span data-stu-id="930f4-109">Report Wizard</span></span>

<span data-ttu-id="930f4-110">O Assistente de Relatórios permite que não programadores criem relatórios simples.</span><span class="sxs-lookup"><span data-stu-id="930f4-110">The Report Wizard lets non-developers create simple reports.</span></span> <span data-ttu-id="930f4-111">Uma vez que a aplicação está incorporada numa plataforma existente, a experiência é a mesma que a experiência que está documentada em [Criar ou editar um relatório utilizando o Assistente de Relatórios](../basics/create-edit-copy-report-wizard.md).</span><span class="sxs-lookup"><span data-stu-id="930f4-111">Because the app is built on an existing platform, the experience is the same as the experience that is documented in [Create or edit a report using the Report Wizard](../basics/create-edit-copy-report-wizard.md).</span></span> <span data-ttu-id="930f4-112">No entanto, irá utilizar as entidades específicas do Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="930f4-112">However, you will use the Project Service Automation-specific entities.</span></span>

## <a name="custom-sql-server-reporting-services-reports"></a><span data-ttu-id="930f4-113">Relatórios personalizados do SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="930f4-113">Custom SQL Server Reporting Services reports</span></span>

<span data-ttu-id="930f4-114">Se a sua empresa exigir um relatório específico que não possa ser criado utilizando o Assistente de Relatório, poderá criar um relatório personalizado.</span><span class="sxs-lookup"><span data-stu-id="930f4-114">If your business requires a specific report that can't be created by using the Report Wizard, you can create a custom report.</span></span> <span data-ttu-id="930f4-115">Tem de ter o Microsoft Visual Studio instalado, juntamente com o Microsoft SQL Server Data Tools e as Extensões de Criação de Relatórios adequadas.</span><span class="sxs-lookup"><span data-stu-id="930f4-115">You must have Microsoft Visual Studio installed, together with the appropriate Microsoft SQL Server Data Tools and Report Authoring Extensions.</span></span> <span data-ttu-id="930f4-116">Para mais informações sobre as ferramentas e as versões, consulte [Ambiente de escrita de relatórios com o SQL Server Data Tools](../analytics/report-writing-environment-using-sql-server-data-tools.md).</span><span class="sxs-lookup"><span data-stu-id="930f4-116">For more information about tools and versions, see [Report writing environment using SQL Server Data Tools](../analytics/report-writing-environment-using-sql-server-data-tools.md).</span></span> <span data-ttu-id="930f4-117">Para obter informações sobre como criar um relatório personalizado, consulte [Criar um novo relatório com o SQL Server Data Tools](../analytics/create-a-new-report-using-sql-server-data-tools.md).</span><span class="sxs-lookup"><span data-stu-id="930f4-117">For information about how to create a custom report, see [Create a new report using SQL Server Data Tools](../analytics/create-a-new-report-using-sql-server-data-tools.md).</span></span>

## <a name="power-bi-insights-apps"></a><span data-ttu-id="930f4-118">Aplicações de insights do Power BI</span><span class="sxs-lookup"><span data-stu-id="930f4-118">Power BI insights apps</span></span>

<span data-ttu-id="930f4-119">Juntos, o Microsoft Power BI e o Dynamics 365 oferecem uma maneira avançada de trabalhar com os seus dados, na forma de aplicações de insights.</span><span class="sxs-lookup"><span data-stu-id="930f4-119">Together, Microsoft Power BI and Dynamics 365 give you a powerful way to work with your data, in the form of insights apps.</span></span> <span data-ttu-id="930f4-120">Para obter informações sobre a disponibilidade de aplicações de insights, consulte a [página de aplicações de insights do Power BI](https://powerbi.microsoft.com/power-bi-insights-apps/).</span><span class="sxs-lookup"><span data-stu-id="930f4-120">For information about the availability of insights apps, see the [Power BI insights apps page](https://powerbi.microsoft.com/power-bi-insights-apps/).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="930f4-121">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="930f4-121">Additional resources</span></span>
<span data-ttu-id="930f4-122">Para mais informações sobre a geração de relatórios no PSA, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="930f4-122">For more information about reporting in PSA, see the following topics:</span></span>

- [<span data-ttu-id="930f4-123">Trabalhar com o modelo de dados do Project Service</span><span class="sxs-lookup"><span data-stu-id="930f4-123">Working with the Project Service data model</span></span>](reports-working-project-service-data-model.md)
- [<span data-ttu-id="930f4-124">Dashboards</span><span class="sxs-lookup"><span data-stu-id="930f4-124">Dashboards</span></span>](reports-dashboards.md)

