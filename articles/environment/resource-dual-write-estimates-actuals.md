---
title: Estimativas do projeto e integração de valores reais
description: Este tópico fornece informações sobre a integração de escritas dupla do Project Operations para estimativas de projetos e valores reais.
author: sigitac
manager: Annbe
ms.date: 4/26/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 88df3385fac0a78a827d65a77d3b04c9d6499536
ms.sourcegitcommit: 02f00960198cc78a5e96955a9e4390c2c6393bbf
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/28/2021
ms.locfileid: "5955812"
---
# <a name="project-estimates-and-actuals-integration"></a><span data-ttu-id="ec71b-103">Estimativas do projeto e integração de valores reais</span><span class="sxs-lookup"><span data-stu-id="ec71b-103">Project estimates and actuals integration</span></span>

<span data-ttu-id="ec71b-104">_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_</span><span class="sxs-lookup"><span data-stu-id="ec71b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="ec71b-105">Este tópico fornece informações sobre a integração de escritas dupla do Project Operations para estimativas de projetos e valores reais.</span><span class="sxs-lookup"><span data-stu-id="ec71b-105">This topic provides information about Project Operations dual-write integration for project estimates and actuals.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="ec71b-106">Estimativas do projeto</span><span class="sxs-lookup"><span data-stu-id="ec71b-106">Project estimates</span></span>

<span data-ttu-id="ec71b-107">O trabalho de projeto, as estimativas de despesas e materiais são criados e mantidos no Microsoft Dataverse e sincronizados nas aplicações Finance and Operations com fins de gestão contabilística.</span><span class="sxs-lookup"><span data-stu-id="ec71b-107">Project labor, expense, and material estimates are created and maintained in Microsoft Dataverse and synchronized to Finance and Operations apps for accounting purposes.</span></span> <span data-ttu-id="ec71b-108">Criar, atualizar e eliminar operações não são suportados através das aplicações Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ec71b-108">Create, update, and delete operations aren't supported through the Finance and Operations apps.</span></span>

<span data-ttu-id="ec71b-109">A criação de estimativas requer uma configuração de gestão contabilística válida para o projeto.</span><span class="sxs-lookup"><span data-stu-id="ec71b-109">Creating estimates requires a valid accounting configuration for the project.</span></span> <span data-ttu-id="ec71b-110">Os projetos associados a linhas de contrato devem ter um perfil de custo e receita válido definido nas regras de custos e perfis de receitas do Projeto.</span><span class="sxs-lookup"><span data-stu-id="ec71b-110">Projects that are associated with contract lines must have a valid project cost and revenue profile defined in the Project cost and revenue profile rules.</span></span> <span data-ttu-id="ec71b-111">Para mais informações, consulte [Configurar Gestão contabilística para projetos faturáveis](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules).</span><span class="sxs-lookup"><span data-stu-id="ec71b-111">For more information, see [Configure accounting for billable projects](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules).</span></span>

## <a name="labor-estimates"></a><span data-ttu-id="ec71b-112">Estimativas de trabalho</span><span class="sxs-lookup"><span data-stu-id="ec71b-112">Labor estimates</span></span>

<span data-ttu-id="ec71b-113">As estimativas de trabalho são criadas pelo Gestor de Projeto ou Gestor de Recursos que também atribui um recurso genérico ou nomeado à tarefa do projeto.</span><span class="sxs-lookup"><span data-stu-id="ec71b-113">Labor estimates are created by the Project Manager or Resource manager who also assigns a generic or named resource to the project task.</span></span> <span data-ttu-id="ec71b-114">Os registos de atribuição de recursos podem ser revistos no separador **Atribuições de Recursos** na página **Detalhes do Projeto** no Dataverse.</span><span class="sxs-lookup"><span data-stu-id="ec71b-114">Resource assignment records can be reviewed on the **Resource Assignments** tab on the **Project Details** page in Dataverse.</span></span> <span data-ttu-id="ec71b-115">Os registos de atribuição de recursos em Dataverse criam registos de previsão de hora em aplicações Finance and Operations que utilizam a **entidade de integração do Project Operations para estimativas de horas (msdyn\_resourceassignments)**.</span><span class="sxs-lookup"><span data-stu-id="ec71b-115">Resource assignment records in Dataverse create hour forecast records in Finance and Operations apps using **Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**.</span></span>

   ![Integração de estimativas de trabalho](./Media/DW4LaborEstimates.png)

<span data-ttu-id="ec71b-117">A dupla escrita sincroniza os registos de atribuição de recursos à tabela de teste (**ProjCDSEstimateHoursImport**), e utiliza a lógica de negócio para criar e atualizar registos de previsão de horas (**ProjForecastEmpl**).</span><span class="sxs-lookup"><span data-stu-id="ec71b-117">Dual-write synchronizes resource assignment records to the staging table (**ProjCDSEstimateHoursImport**), and then uses business logic to create and update hour forecast records (**ProjForecastEmpl**).</span></span>

<span data-ttu-id="ec71b-118">O contabilista do Projeto analisa os registos de horas de previsão criados em aplicações Finance and Operations, indo para a **Gestão do projeto e contabilidade** > **Todos os projetos** > **Plano** > **Previsões horárias**.</span><span class="sxs-lookup"><span data-stu-id="ec71b-118">The Project accountant reviews forecast hour records created in Finance and Operations apps by going to **Project management and accounting** > **All projects** > **Plan** > **Hour forecasts**.</span></span>

## <a name="expense-estimates"></a><span data-ttu-id="ec71b-119">Estimativas de despesas</span><span class="sxs-lookup"><span data-stu-id="ec71b-119">Expense estimates</span></span>

<span data-ttu-id="ec71b-120">As estimativas de despesas são criadas pelo gestor do Projeto no separador **Estimativas de Despesas** na página **Detalhes do Projeto** em Dataverse.</span><span class="sxs-lookup"><span data-stu-id="ec71b-120">Expense estimates are created by the Project manager on the **Expense Estimates** tab on the **Project Details** page in Dataverse.</span></span> <span data-ttu-id="ec71b-121">Os registos de estimativa de despesas são armazenados na entidade da **Linha de Estimativa** em Dataverse.</span><span class="sxs-lookup"><span data-stu-id="ec71b-121">Expense estimate records are stored in the **Estimate Line** entity in Dataverse.</span></span> <span data-ttu-id="ec71b-122">Estes registos de estimativa têm classe de transações, **Despesa** e são sincronizados com registos de previsão de despesas em aplicações Finance and Operations que utilizam a **entidade de integração do Project Operations para estimativas de despesas (msdyn\_estimatelines)**.</span><span class="sxs-lookup"><span data-stu-id="ec71b-122">These estimate records have transaction class, **Expense** and are synchronized to expense forecast records in Finance and Operations apps using **Project Operations integration entity for expense estimates (msdyn\_estimatelines)**.</span></span>

   ![Integração de estimativas de despesa](./Media/DW4ExpenseEstimates.png)

<span data-ttu-id="ec71b-124">A dupla escrita sincroniza os registos de estimativa de despesa à tabela de teste, (**ProjCDSEstimateExpenseImport)** e utiliza a lógica de negócio para criar e atualizar registos de previsão de despesa (**ProjForecastCost**).</span><span class="sxs-lookup"><span data-stu-id="ec71b-124">Dual-write synchronizes expense estimate records to the staging table, **ProjCDSEstimateExpenseImport)** and then uses business logic to create and update expense forecast records (**ProjForecastCost**).</span></span> <span data-ttu-id="ec71b-125">Estimativa de linhas de loja estimativa de vendas e estimativa de custos recordes separadamente.</span><span class="sxs-lookup"><span data-stu-id="ec71b-125">Estimate lines store sales estimate and cost estimate records separately.</span></span> <span data-ttu-id="ec71b-126">A lógica de negócio em aplicações Finance and Operations povoa um único registo de previsão de despesas usando este detalhe na tabela de teste.</span><span class="sxs-lookup"><span data-stu-id="ec71b-126">The business logic in Finance and Operations apps populates a single Expense forecast record using this detail in the staging table.</span></span>

<span data-ttu-id="ec71b-127">O contabilista do Projeto pode rever os registos de previsão de despesa criados em aplicações Finance and Operations, indo para a **Gestão do projeto e contabilidade** > **Todos os projetos** > **Plano** > **Previsões de despesa**.</span><span class="sxs-lookup"><span data-stu-id="ec71b-127">The Project accountant can review expense forecast records in Finance and Operations apps by going to **Project management and accounting** > **All projects** > **Plan** > **Expense forecasts**.</span></span>

## <a name="material-estimates"></a><span data-ttu-id="ec71b-128">Estimativas de material</span><span class="sxs-lookup"><span data-stu-id="ec71b-128">Material estimates</span></span>

<span data-ttu-id="ec71b-129">As estimativas de material são criadas pelo gestor do Projeto no separador **Estimativas de material** na página **Detalhes do Projeto** em Dataverse.</span><span class="sxs-lookup"><span data-stu-id="ec71b-129">Material estimates are created by the Project manager on the **Material Estimates** tab on the **Project Details** page in Dataverse.</span></span> <span data-ttu-id="ec71b-130">Os registos de estimativa de material são armazenados na entidade da **Linha de Estimativa** em Dataverse.</span><span class="sxs-lookup"><span data-stu-id="ec71b-130">Material estimate records are stored in the **Estimate Line** entity in Dataverse.</span></span> <span data-ttu-id="ec71b-131">Estes registos de estimativa têm a classe de transações, **Material** e são sincronizados com registos de previsão de artigos em aplicações Finance and Operations que utilizam a **tabela do Project Operations para estimativas de material (msdyn\_estimatelines)**.</span><span class="sxs-lookup"><span data-stu-id="ec71b-131">These estimate records have the transaction class, **Material** and are synchronized to item forecast records in Finance and Operations apps using **Project integration table for material estimates (msdyn\_estimatelines)**.</span></span>

   ![Integração de estimativas de material](./Media/DW4MaterialEstimates.png)

<span data-ttu-id="ec71b-133">A dupla escrita sincroniza os registos de estimativa de material à tabela de teste **ProjForecastSalesImpor**, e utiliza a lógica de negócio para criar e atualizar registos de previsão de artigo (**ForecastSales**).</span><span class="sxs-lookup"><span data-stu-id="ec71b-133">Dual-write synchronizes material estimate records to the staging table **ProjForecastSalesImpor**, and then uses business logic to create and update item forecast records (**ForecastSales**).</span></span> <span data-ttu-id="ec71b-134">Estimativa de linhas de loja estimativa de vendas e estimativa de custos recordes separadamente.</span><span class="sxs-lookup"><span data-stu-id="ec71b-134">Estimate lines store sales estimate and cost estimate records separately.</span></span> <span data-ttu-id="ec71b-135">A lógica de negócio em aplicações Finance and Operations povoa um único registo de previsão de artigo usando este detalhe na tabela de teste.</span><span class="sxs-lookup"><span data-stu-id="ec71b-135">The business logic in Finance and Operations apps populates a single Item forecast record using this detail in the staging table.</span></span>

<span data-ttu-id="ec71b-136">O contabilista do Projeto pode rever os registos de previsão de artigo criados em aplicações Finance and Operations, indo para a **Gestão do projeto e contabilidade** > **Todos os projetos** > **Plano** > **Previsões de artigo**.</span><span class="sxs-lookup"><span data-stu-id="ec71b-136">The Project accountant can review item forecast records in Finance and Operations apps by going to **Project management and accounting** > **All projects** > **Plan** > **Item forecasts**.</span></span>

## <a name="project-actuals"></a><span data-ttu-id="ec71b-137">Valores reais do projeto</span><span class="sxs-lookup"><span data-stu-id="ec71b-137">Project actuals</span></span>

<span data-ttu-id="ec71b-138">Os valores reais do projeto são criados em Dataverse, com base no tempo, despesas, material e atividade de faturação.</span><span class="sxs-lookup"><span data-stu-id="ec71b-138">Project actuals are created in Dataverse, based on time, expense, material, and billing activity.</span></span> <span data-ttu-id="ec71b-139">Todos os atributos operacionais destas transações, incluindo quantidade, preço de custo, preço de venda e projeto são capturados nesta entidade Dataverse.</span><span class="sxs-lookup"><span data-stu-id="ec71b-139">All operational attributes of these transactions including quantity, cost price, sales price, and project are captured in this Dataverse entity.</span></span> <span data-ttu-id="ec71b-140">Para mais informações, ver [Valores reais](../actuals/actuals-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ec71b-140">For more information, see [Actuals](../actuals/actuals-overview.md).</span></span> <span data-ttu-id="ec71b-141">Os registos de valores reais são sincronizados com aplicações Finance and Operations que utilizam o mapa de tabela de escrita dupla **Valores reais da integração do Project Operations (msdyn\_actuals)** para contabilidade a jusante.</span><span class="sxs-lookup"><span data-stu-id="ec71b-141">Actual records are synchronized to Finance and Operations apps using the dual-write table map **Project Operations integration actuals (msdyn\_actuals)** for downstream accounting.</span></span>

   ![Integração de valores reais](./Media/DW4Actuals.png)

<span data-ttu-id="ec71b-143">O mapa de tabela de **Valores reais de integração do Project Operations** sincroniza todos os registos da entidade **Valores reais** em Dataverse, com o atributo **Skip Sync (apenas uso interno)** definido como **Falso**.</span><span class="sxs-lookup"><span data-stu-id="ec71b-143">The **Project Operations integration actuals** table map synchronizes all the records from the **Actuals** entity in Dataverse, with the attribute **Skip Sync (internal use only)** set to **False**.</span></span> <span data-ttu-id="ec71b-144">Este valor de atributo é definido em Dataverse automaticamente quando o registo é criado.</span><span class="sxs-lookup"><span data-stu-id="ec71b-144">This attribute value is set in Dataverse automatically when the record is created.</span></span> <span data-ttu-id="ec71b-145">Exemplos em que este atributo é definido para **Verdadeiro** são:</span><span class="sxs-lookup"><span data-stu-id="ec71b-145">Examples where this attribute is set to **True** are:</span></span>

  - <span data-ttu-id="ec71b-146">Os valores reais de custo do projeto para transações interempresa.</span><span class="sxs-lookup"><span data-stu-id="ec71b-146">Project cost actuals for intercompany transactions.</span></span> <span data-ttu-id="ec71b-147">Para obter mais informações, consulte [Criar transações interempresa](../project-accounting/create-intercompany-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="ec71b-147">For more information, see [Create intercompany transactions](../project-accounting/create-intercompany-transactions.md).</span></span> <span data-ttu-id="ec71b-148">Estes registos são ignorados porque o sistema recria o custo real do projeto em aplicações Finance and Operations quando a fatura do fornecedor interempresa é publicada.</span><span class="sxs-lookup"><span data-stu-id="ec71b-148">These records are skipped because the system recreates the project cost actual in Finance and Operations apps when the intercompany vendor invoice is posted.</span></span>
  - <span data-ttu-id="ec71b-149">Registos de vendas negativos não faturados criados quando a fatura proforma é confirmada.</span><span class="sxs-lookup"><span data-stu-id="ec71b-149">Negative unbilled sales records created when the proforma invoice is confirmed.</span></span> <span data-ttu-id="ec71b-150">Estes registos são ignorados porque o sub-livro razão do projeto em aplicações Finance and Operations não inverte o registo de vendas não faturados na faturação, mas altera o estado para faturar totalmente.</span><span class="sxs-lookup"><span data-stu-id="ec71b-150">These records are skipped because the project subledger in Finance and Operations apps doesn't reverse the unbilled sales record at invoicing but changes the status to fully invoiced.</span></span>

<span data-ttu-id="ec71b-151">O mapa de tabela de dupla escrita sincroniza os valores reais da tabela de teste, **ProjCDSActualsImport**.</span><span class="sxs-lookup"><span data-stu-id="ec71b-151">The dual-write table map synchronizes the actuals records to the staging table, **ProjCDSActualsImport**.</span></span> <span data-ttu-id="ec71b-152">Estes registos são processados pelo processo periódico **Importar da tabela de teste** ao criar linhas de diário do Project Operations e linhas de proposta de fatura de projeto.</span><span class="sxs-lookup"><span data-stu-id="ec71b-152">These records are processed by the periodic process **Import from staging table** when creating Project Operations integration journal lines and project invoice proposal lines.</span></span> <span data-ttu-id="ec71b-153">Para mais informações, consulte [diário de Integração no Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="ec71b-153">For more information, see [Integration journal in Project Operations](../project-accounting/project-operations-integration-journal.md).</span></span>

<span data-ttu-id="ec71b-154">Dataverse captura também as ligações entre as transações de valores reais do projeto na entidade de **ligação de transações**.</span><span class="sxs-lookup"><span data-stu-id="ec71b-154">Dataverse also captures the links between the project actual transactions in the **Transaction connection** entity.</span></span> <span data-ttu-id="ec71b-155">Para obter mais informações, consulte [ligar valores reais para registos originais](../actuals/linkingactuals.md).</span><span class="sxs-lookup"><span data-stu-id="ec71b-155">For more information, see [Link actuals to original records](../actuals/linkingactuals.md).</span></span> <span data-ttu-id="ec71b-156">As ligações entre transações de valores reais também são sincronizadas com aplicações Finance and Operations que utilizam o mapa de tabelas de dupla escrita, **entidade de integração para relações de transação de projetos (msdyn\_transactionconnections)**.</span><span class="sxs-lookup"><span data-stu-id="ec71b-156">Links between actual transactions are also synchronized to Finance and Operations apps using the dual-write table map, **Integration entity for project transaction relationships (msdyn\_transactionconnections)**.</span></span> <span data-ttu-id="ec71b-157">Estes registos são usados pelo processo periódico, **Importar da tabela de teste** ao criar linhas de diário do Project Operations e linhas de proposta de fatura de projeto.</span><span class="sxs-lookup"><span data-stu-id="ec71b-157">These records are used by the periodic process, **Import from staging table** when creating Project Operations integration journal lines and Project invoice proposal lines.</span></span>

<span data-ttu-id="ec71b-158">A publicação de um diário de integração do Project Operations e de uma proposta de fatura do projeto despoleta uma atualização nos respetivos registos na tabela de teste, **ProjCDSActualsImport**.</span><span class="sxs-lookup"><span data-stu-id="ec71b-158">Posting a Project Operations integration journal and a project invoice proposal triggers an update in respective records in the staging table, **ProjCDSActualsImport**.</span></span> <span data-ttu-id="ec71b-159">O sistema captura e regista os seguintes atributos contabilísticos para transações de valores reais:</span><span class="sxs-lookup"><span data-stu-id="ec71b-159">The system captures and records the following accounting attributes for actuals transactions:</span></span>

- <span data-ttu-id="ec71b-160">Montante de moeda contabilística</span><span class="sxs-lookup"><span data-stu-id="ec71b-160">Accounting currency amount</span></span>
- <span data-ttu-id="ec71b-161">Câmbio</span><span class="sxs-lookup"><span data-stu-id="ec71b-161">Exchange rate</span></span>
- <span data-ttu-id="ec71b-162">Número de voucher</span><span class="sxs-lookup"><span data-stu-id="ec71b-162">Voucher number</span></span>
- <span data-ttu-id="ec71b-163">Valor de imposto sobre vendas</span><span class="sxs-lookup"><span data-stu-id="ec71b-163">Sales tax amount</span></span>

<span data-ttu-id="ec71b-164">O mapa da tabela **Valores reais de integração do Project Operations** atualiza os registos dos respetivos registos de valores reais no Dataverse com esta informação.</span><span class="sxs-lookup"><span data-stu-id="ec71b-164">The **Project Operations integration actuals** table map updates respective actuals records in Dataverse with this information.</span></span>