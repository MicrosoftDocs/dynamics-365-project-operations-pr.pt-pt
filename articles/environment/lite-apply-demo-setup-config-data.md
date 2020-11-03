---
title: Aplicar dados de configuração da demonstração
description: Este tópico fornece informações sobre como aplicar dados de configuração da demonstração para o Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 33b85115963f3561718b8951e5b518fd34de7723
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082269"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations-lite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="5a4df-103">Aplicar os dados de configuração da demonstração para a a implementação do Project Operations lite - oportunidade potencial para fatura pró-forma</span><span class="sxs-lookup"><span data-stu-id="5a4df-103">Apply demo setup and configuration data for Project Operations lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="5a4df-104">_\*\*Implementação leve - oportunidade potencial para fatura pró-forma_</span><span class="sxs-lookup"><span data-stu-id="5a4df-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

1. <span data-ttu-id="5a4df-105">Transferir o [Pacote de Dados Mestres](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span><span class="sxs-lookup"><span data-stu-id="5a4df-105">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="5a4df-106">Navegue para a pasta *ProjOpsDemoDataSetupAndMaster - Integrated CMT* e execute o ficheiro executável *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="5a4df-106">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="5a4df-107">Na página 1 do Assistente de Migração da Configuração do Common Data Service (CMT), selecione **Importar Dados** e, em seguida, selecione **Continuar**.</span><span class="sxs-lookup"><span data-stu-id="5a4df-107">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Migração da Configuração](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="5a4df-109">Na Página 2 do Assistente do CMT, selecione **Microsoft 365** como **Tipo de Implementação**.</span><span class="sxs-lookup"><span data-stu-id="5a4df-109">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="5a4df-110">Selecione as caixas de verificação **Apresentar lista de organizações disponíveis** e **Mostrar Avançadas**.</span><span class="sxs-lookup"><span data-stu-id="5a4df-110">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="5a4df-111">Selecione a região do seu inquilino, introduza as suas credenciais e, em seguida, selecione **Iniciar Sessão**.</span><span class="sxs-lookup"><span data-stu-id="5a4df-111">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

![Início de Sessão da Configuração](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="5a4df-113">Na página 3, a partir da lista de Organizações no Inquilino, selecione a organização para a qual pretende importar os dados de demonstração e, em seguida, selecione **Iniciar Sessão**.</span><span class="sxs-lookup"><span data-stu-id="5a4df-113">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="5a4df-114">Na página 4, selecione o ficheiro zip, *MasterAndSetupData* a partir da pasta descompactada *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span><span class="sxs-lookup"><span data-stu-id="5a4df-114">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

![Ficheiro Zip](./media/3ZipFile.png)

![Selecionar um ficheiro](./media/4SelectAFile.png)

9. <span data-ttu-id="5a4df-117">Depois de selecionado o ficheiro zip, selecione **Importar Dados**.</span><span class="sxs-lookup"><span data-stu-id="5a4df-117">After the zip file is selected, select **Import Data**.</span></span>

![Importar Dados](./media/5ImportData.png)

10. <span data-ttu-id="5a4df-119">A importação será executada durante aproximadamente 2 a 10 minutos, consoante a velocidade da sua rede.</span><span class="sxs-lookup"><span data-stu-id="5a4df-119">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="5a4df-120">Depois de concluída, saia do Assistente de CMT.</span><span class="sxs-lookup"><span data-stu-id="5a4df-120">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="5a4df-121">Contacte a sua organização para obter dados nas seguintes 20 entidades:</span><span class="sxs-lookup"><span data-stu-id="5a4df-121">Check your organization for data in the following 20 entities:</span></span>

- <span data-ttu-id="5a4df-122">Moeda</span><span class="sxs-lookup"><span data-stu-id="5a4df-122">Currency</span></span>
- <span data-ttu-id="5a4df-123">Unidade Organizacional</span><span class="sxs-lookup"><span data-stu-id="5a4df-123">Organizational Unit</span></span>
- <span data-ttu-id="5a4df-124">Contacto</span><span class="sxs-lookup"><span data-stu-id="5a4df-124">Contact</span></span>
- <span data-ttu-id="5a4df-125">Grupo de Impostos</span><span class="sxs-lookup"><span data-stu-id="5a4df-125">Tax Group</span></span>
- <span data-ttu-id="5a4df-126">Grupo de Clientes</span><span class="sxs-lookup"><span data-stu-id="5a4df-126">Customer Group</span></span>
- <span data-ttu-id="5a4df-127">Unidade</span><span class="sxs-lookup"><span data-stu-id="5a4df-127">Unit</span></span>
- <span data-ttu-id="5a4df-128">Grupo de Unidades</span><span class="sxs-lookup"><span data-stu-id="5a4df-128">Unit Group</span></span>
- <span data-ttu-id="5a4df-129">Lista de Preços</span><span class="sxs-lookup"><span data-stu-id="5a4df-129">Price List</span></span>
- <span data-ttu-id="5a4df-130">Lista de Preços do Parâmetro do Projeto</span><span class="sxs-lookup"><span data-stu-id="5a4df-130">Project Parameter Price List</span></span>
- <span data-ttu-id="5a4df-131">Frequência da Fatura</span><span class="sxs-lookup"><span data-stu-id="5a4df-131">Invoice Frequency</span></span>
- <span data-ttu-id="5a4df-132">Detalhe de Frequência de Fatura</span><span class="sxs-lookup"><span data-stu-id="5a4df-132">Invoice Frequency Detail</span></span>
- <span data-ttu-id="5a4df-133">Categoria de Recurso Reservável</span><span class="sxs-lookup"><span data-stu-id="5a4df-133">Bookable Resource Category</span></span>
- <span data-ttu-id="5a4df-134">Categoria de Transação</span><span class="sxs-lookup"><span data-stu-id="5a4df-134">Transaction Category</span></span>
- <span data-ttu-id="5a4df-135">Categoria de Despesa</span><span class="sxs-lookup"><span data-stu-id="5a4df-135">Expense Category</span></span>
- <span data-ttu-id="5a4df-136">Preço da Função</span><span class="sxs-lookup"><span data-stu-id="5a4df-136">Role Price</span></span>
- <span data-ttu-id="5a4df-137">Preço de Categoria de Transação</span><span class="sxs-lookup"><span data-stu-id="5a4df-137">Transaction Category Price</span></span>
- <span data-ttu-id="5a4df-138">Característica</span><span class="sxs-lookup"><span data-stu-id="5a4df-138">Characteristic</span></span>
- <span data-ttu-id="5a4df-139">Recurso Reservável</span><span class="sxs-lookup"><span data-stu-id="5a4df-139">Bookable Resource</span></span>
- <span data-ttu-id="5a4df-140">Associação de categorias de recurso reservável</span><span class="sxs-lookup"><span data-stu-id="5a4df-140">Bookable resource category Assn</span></span>
- <span data-ttu-id="5a4df-141">Característica de Recurso Reservável</span><span class="sxs-lookup"><span data-stu-id="5a4df-141">Bookable Resource Characteristic</span></span>

![Concluir Importação](./media/6CompleteImport.png)
