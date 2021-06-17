---
title: Aplicar dados de configuração da demonstração – lite
description: Este tópico fornece informações sobre como aplicar dados de configuração da demonstração para o Project Operations.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7729b4a9ef5f498b78af298f7233d7dd45434bb3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997165"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a><span data-ttu-id="829e8-103">Aplicar dados de configuração de demonstração para Project Operations – lite</span><span class="sxs-lookup"><span data-stu-id="829e8-103">Apply demo setup and configuration data for Project Operations - lite</span></span> 

<span data-ttu-id="829e8-104">_\*\*Implementação leve - oportunidade potencial para fatura pró-forma_</span><span class="sxs-lookup"><span data-stu-id="829e8-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="829e8-105">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="829e8-105">Prerequisites</span></span>

<span data-ttu-id="829e8-106">Antes de iniciar a configuração, tem de ter um ambiente do Common Data Service (CDS) aprovisionado para o Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="829e8-106">Before you begin the configuration, you must have a Common Data Service (CDS) environment provisioned for Dynamics 365 Project Operations.</span></span>


## <a name="instructions"></a><span data-ttu-id="829e8-107">Instruções</span><span class="sxs-lookup"><span data-stu-id="829e8-107">Instructions</span></span>

1. <span data-ttu-id="829e8-108">Transferir o [Pacote de Dados Mestres](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip).</span><span class="sxs-lookup"><span data-stu-id="829e8-108">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip).</span></span> 
2. <span data-ttu-id="829e8-109">Navegue para a pasta *ProjOpsSampleSetupData - CE apenas CMT* e execute o ficheiro executável, *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="829e8-109">Navigate to the folder *ProjOpsSampleSetupData - CE only CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="829e8-110">Na página 1 do Assistente de Migração da Configuração do Common Data Service (CMT), selecione **Importar Dados** e, em seguida, selecione **Continuar**.</span><span class="sxs-lookup"><span data-stu-id="829e8-110">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

    ![Migração da Configuração](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="829e8-112">Na Página 2 do Assistente do CMT, selecione **Microsoft 365** como **Tipo de Implementação**.</span><span class="sxs-lookup"><span data-stu-id="829e8-112">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="829e8-113">Selecione as caixas de verificação **Apresentar lista de organizações disponíveis** e **Mostrar Avançadas**.</span><span class="sxs-lookup"><span data-stu-id="829e8-113">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="829e8-114">Selecione a região do seu inquilino, introduza as suas credenciais e, em seguida, selecione **Iniciar Sessão**.</span><span class="sxs-lookup"><span data-stu-id="829e8-114">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

   ![Início de Sessão da Configuração](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="829e8-116">Na página 3, a partir da lista de Organizações no Inquilino, selecione a organização para a qual pretende importar os dados de demonstração e, em seguida, selecione **Iniciar Sessão**.</span><span class="sxs-lookup"><span data-stu-id="829e8-116">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="829e8-117">Na página 4, selecione o ficheiro zip, *SampleSetupAndConfigData* da pasta desempacotada, *ProjOpsSampleSetupData - CE apenas CMT*.</span><span class="sxs-lookup"><span data-stu-id="829e8-117">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder, *ProjOpsSampleSetupData - CE only CMT*.</span></span>

   ![Ficheiro Zip](./media/3ZipFile.png)

   ![Selecionar um ficheiro](./media/4SelectAFile.png)

9. <span data-ttu-id="829e8-120">Depois de selecionado o ficheiro zip, selecione **Importar Dados**.</span><span class="sxs-lookup"><span data-stu-id="829e8-120">After the zip file is selected, select **Import Data**.</span></span>

   ![Importar Dados](./media/5ImportData.png)

10. <span data-ttu-id="829e8-122">A importação será executada durante aproximadamente 2 a 10 minutos, consoante a velocidade da sua rede.</span><span class="sxs-lookup"><span data-stu-id="829e8-122">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="829e8-123">Depois de concluída, saia do Assistente de CMT.</span><span class="sxs-lookup"><span data-stu-id="829e8-123">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="829e8-124">Contacte a sua organização para obter dados nas seguintes 18 entidades:</span><span class="sxs-lookup"><span data-stu-id="829e8-124">Check your organization for data in the following 18 entities:</span></span>

    -   <span data-ttu-id="829e8-125">Moeda</span><span class="sxs-lookup"><span data-stu-id="829e8-125">Currency</span></span>
    -   <span data-ttu-id="829e8-126">Conta</span><span class="sxs-lookup"><span data-stu-id="829e8-126">Account</span></span>
    -   <span data-ttu-id="829e8-127">Unidade Organizacional</span><span class="sxs-lookup"><span data-stu-id="829e8-127">Organizational Unit</span></span>
    -   <span data-ttu-id="829e8-128">Contacto</span><span class="sxs-lookup"><span data-stu-id="829e8-128">Contact</span></span>
    -   <span data-ttu-id="829e8-129">Unidade</span><span class="sxs-lookup"><span data-stu-id="829e8-129">Unit</span></span>
    -   <span data-ttu-id="829e8-130">Grupo de Unidades</span><span class="sxs-lookup"><span data-stu-id="829e8-130">Unit Group</span></span>
    -   <span data-ttu-id="829e8-131">Lista de Preços</span><span class="sxs-lookup"><span data-stu-id="829e8-131">Price List</span></span>
    -   <span data-ttu-id="829e8-132">Lista de Preços do Parâmetro do Projeto</span><span class="sxs-lookup"><span data-stu-id="829e8-132">Project Parameter Price List</span></span> 
    -   <span data-ttu-id="829e8-133">Frequência da Fatura</span><span class="sxs-lookup"><span data-stu-id="829e8-133">Invoice Frequency</span></span>
    -   <span data-ttu-id="829e8-134">Categoria de Recurso Reservável</span><span class="sxs-lookup"><span data-stu-id="829e8-134">Bookable Resource Category</span></span>
    -   <span data-ttu-id="829e8-135">Categoria de Transação</span><span class="sxs-lookup"><span data-stu-id="829e8-135">Transaction Category</span></span>
    -   <span data-ttu-id="829e8-136">Categoria de Despesa</span><span class="sxs-lookup"><span data-stu-id="829e8-136">Expense Category</span></span>
    -   <span data-ttu-id="829e8-137">Preço da Função</span><span class="sxs-lookup"><span data-stu-id="829e8-137">Role Price</span></span>
    -   <span data-ttu-id="829e8-138">Preço de Categoria de Transação</span><span class="sxs-lookup"><span data-stu-id="829e8-138">Transaction Category Price</span></span>
    -   <span data-ttu-id="829e8-139">Característica</span><span class="sxs-lookup"><span data-stu-id="829e8-139">Characteristic</span></span>
    -   <span data-ttu-id="829e8-140">Recurso Reservável</span><span class="sxs-lookup"><span data-stu-id="829e8-140">Bookable Resource</span></span>
    -   <span data-ttu-id="829e8-141">Associação de categorias de recurso reservável</span><span class="sxs-lookup"><span data-stu-id="829e8-141">Bookable resource category Assn</span></span>
    -   <span data-ttu-id="829e8-142">Característica de Recurso Reservável</span><span class="sxs-lookup"><span data-stu-id="829e8-142">Bookable Resource Characteristic</span></span>

    ![Concluir Importação](./media/6CompleteImport.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
