---
title: Configurar e aplicar dados de configuração no Common Data Service
description: Este tópico fornece informações sobre como configurar e aplicar dados de configuração no Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7de8db5e91265c77c79f34a513bf27d9a55b789a
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401142"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a><span data-ttu-id="f0f2e-103">Configurar e aplicar dados de configuração no Common Data Service</span><span class="sxs-lookup"><span data-stu-id="f0f2e-103">Set up and apply configuration data in the Common Data Service</span></span> 

<span data-ttu-id="f0f2e-104">_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_</span><span class="sxs-lookup"><span data-stu-id="f0f2e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f0f2e-105">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="f0f2e-105">Prerequisites</span></span>

<span data-ttu-id="f0f2e-106">Antes de configurar dados no Common Data Service (CDS), devem ser cumpridos os seguintes pré-requisitos:</span><span class="sxs-lookup"><span data-stu-id="f0f2e-106">Before you beging to configure data in the Common Data Service (CDS), the following prerequisites must be met:</span></span>

1.  <span data-ttu-id="f0f2e-107">Aprovisionar um ambiente CDS e um ambiente Dynamics 365 Finance para o Project Operations.</span><span class="sxs-lookup"><span data-stu-id="f0f2e-107">Provision a CDS environment and a Dynamics 365 Finance environment for Project Operations.</span></span>
2.  <span data-ttu-id="f0f2e-108">As informações da entidade jurídica do Dynamics 365 Finance são partilhadas com o ambiente CDS.</span><span class="sxs-lookup"><span data-stu-id="f0f2e-108">Legal entity information from Dynamics 365 Finance is shared to the CDS environment.</span></span> <span data-ttu-id="f0f2e-109">Isto significa que a entidade **Empresa** tem os seguintes registos da empresa:</span><span class="sxs-lookup"><span data-stu-id="f0f2e-109">This means that the **Company** entity in CDS has the following company records:</span></span>
  - <span data-ttu-id="f0f2e-110">THPM</span><span class="sxs-lookup"><span data-stu-id="f0f2e-110">THPM</span></span>
  - <span data-ttu-id="f0f2e-111">USPM</span><span class="sxs-lookup"><span data-stu-id="f0f2e-111">USPM</span></span>
  - <span data-ttu-id="f0f2e-112">GBPM</span><span class="sxs-lookup"><span data-stu-id="f0f2e-112">GBPM</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="f0f2e-113">Instalar dados de configuração</span><span class="sxs-lookup"><span data-stu-id="f0f2e-113">Install setup and configuration data</span></span>

1. <span data-ttu-id="f0f2e-114">Transfira, desbloqueie e descompacte o [Pacote de Dados de Configuração](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span><span class="sxs-lookup"><span data-stu-id="f0f2e-114">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span></span>
2. <span data-ttu-id="f0f2e-115">Navegue para a pasta descompactada e execute o ficheiro executável *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="f0f2e-115">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="f0f2e-116">Na página 1 do Assistente de Migração da Configuração do Common Data Service (CMT), selecione **Importar Dados** e, em seguida, selecione **Continuar**.</span><span class="sxs-lookup"><span data-stu-id="f0f2e-116">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Migração da Configuração](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="f0f2e-118">Na Página 2 do Assistente do CMT, selecione **Microsoft 365** como **Tipo de Implementação**.</span><span class="sxs-lookup"><span data-stu-id="f0f2e-118">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="f0f2e-119">Selecione as caixas de verificação **Apresentar lista de organizações disponíveis** e **Mostrar Avançadas**.</span><span class="sxs-lookup"><span data-stu-id="f0f2e-119">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="f0f2e-120">Selecione a região do seu inquilino, introduza as suas credenciais e selecione **Iniciar Sessão**.</span><span class="sxs-lookup"><span data-stu-id="f0f2e-120">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Início de Sessão da Configuração](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="f0f2e-122">Na página 3, a partir da lista de organizações no inquilino, selecione a organização para a qual pretende importar os dados de demonstração e selecione **Iniciar Sessão**.</span><span class="sxs-lookup"><span data-stu-id="f0f2e-122">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="f0f2e-123">Na página 4, selecione o ficheiro zip *SampleSetupAndConfigData* a partir da pasta descompactada.</span><span class="sxs-lookup"><span data-stu-id="f0f2e-123">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Seleção de ficheiros Zip](./media/3ZipFile.png)

![Selecionar um ficheiro](./media/4SelectAFile.png)

9. <span data-ttu-id="f0f2e-126">Depois de selecionado o ficheiro zip, selecione **Importar Dados**.</span><span class="sxs-lookup"><span data-stu-id="f0f2e-126">After the zip file is selected, select **Import Data**.</span></span>

![Dados de Importação](./media/5ImportData.png)

10. <span data-ttu-id="f0f2e-128">A importação será executada durante aproximadamente 2 a 10 minutos, consoante a velocidade da sua rede.</span><span class="sxs-lookup"><span data-stu-id="f0f2e-128">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="f0f2e-129">Depois de concluída a importação, saia do Assistente de CMT.</span><span class="sxs-lookup"><span data-stu-id="f0f2e-129">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="f0f2e-130">Contacte a sua organização para obter dados nas seguintes 19 entidades:</span><span class="sxs-lookup"><span data-stu-id="f0f2e-130">Check your organization for data in the following 19 entities:</span></span>

  - <span data-ttu-id="f0f2e-131">Moeda</span><span class="sxs-lookup"><span data-stu-id="f0f2e-131">Currency</span></span>
  - <span data-ttu-id="f0f2e-132">Unidade Organizacional</span><span class="sxs-lookup"><span data-stu-id="f0f2e-132">Organizational Unit</span></span>
  - <span data-ttu-id="f0f2e-133">Contacto</span><span class="sxs-lookup"><span data-stu-id="f0f2e-133">Contact</span></span>
  - <span data-ttu-id="f0f2e-134">Grupo de Impostos</span><span class="sxs-lookup"><span data-stu-id="f0f2e-134">Tax Group</span></span>
  - <span data-ttu-id="f0f2e-135">Grupo de Clientes</span><span class="sxs-lookup"><span data-stu-id="f0f2e-135">Customer Group</span></span>
  - <span data-ttu-id="f0f2e-136">Unidade</span><span class="sxs-lookup"><span data-stu-id="f0f2e-136">Unit</span></span>
  - <span data-ttu-id="f0f2e-137">Grupo de Unidades</span><span class="sxs-lookup"><span data-stu-id="f0f2e-137">Unit Group</span></span>
  - <span data-ttu-id="f0f2e-138">Lista de Preços</span><span class="sxs-lookup"><span data-stu-id="f0f2e-138">Price List</span></span>
  - <span data-ttu-id="f0f2e-139">Lista de Preços do Parâmetro do Projeto</span><span class="sxs-lookup"><span data-stu-id="f0f2e-139">Project Parameter Price List</span></span>
  - <span data-ttu-id="f0f2e-140">Frequência da Fatura</span><span class="sxs-lookup"><span data-stu-id="f0f2e-140">Invoice Frequency</span></span>
  - <span data-ttu-id="f0f2e-141">Categoria de Recurso Reservável</span><span class="sxs-lookup"><span data-stu-id="f0f2e-141">Bookable Resource Category</span></span>
  - <span data-ttu-id="f0f2e-142">Categoria de Transação</span><span class="sxs-lookup"><span data-stu-id="f0f2e-142">Transaction Category</span></span>
  - <span data-ttu-id="f0f2e-143">Categoria de Despesa</span><span class="sxs-lookup"><span data-stu-id="f0f2e-143">Expense Category</span></span>
  - <span data-ttu-id="f0f2e-144">Preço da Função</span><span class="sxs-lookup"><span data-stu-id="f0f2e-144">Role Price</span></span>
  - <span data-ttu-id="f0f2e-145">Preço de Categoria de Transação</span><span class="sxs-lookup"><span data-stu-id="f0f2e-145">Transaction Category Price</span></span>
  - <span data-ttu-id="f0f2e-146">Característica</span><span class="sxs-lookup"><span data-stu-id="f0f2e-146">Characteristic</span></span>
  - <span data-ttu-id="f0f2e-147">Recurso Reservável</span><span class="sxs-lookup"><span data-stu-id="f0f2e-147">Bookable Resource</span></span>
  - <span data-ttu-id="f0f2e-148">Associação de categorias de recurso reservável</span><span class="sxs-lookup"><span data-stu-id="f0f2e-148">Bookable resource category Assn</span></span>
  - <span data-ttu-id="f0f2e-149">Característica de Recurso Reservável</span><span class="sxs-lookup"><span data-stu-id="f0f2e-149">Bookable Resource Characteristic</span></span>

![Concluir Importação](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="f0f2e-151">Atualizar configurações do Project Operations</span><span class="sxs-lookup"><span data-stu-id="f0f2e-151">Update Project Operations configurations</span></span>

1. <span data-ttu-id="f0f2e-152">Navegye para o ambiente CE.</span><span class="sxs-lookup"><span data-stu-id="f0f2e-152">Navigate to the CE environment.</span></span> <span data-ttu-id="f0f2e-153">Pode encontrá-lo ao abrir o [Centro de Administração do Power Platform](https://admin.powerplatform.microsoft.com/environments), selecionar o ambiente e, em seguida, selecionar **Abrir Ambiente**.</span><span class="sxs-lookup"><span data-stu-id="f0f2e-153">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Abrir Ambiente](./media/7OpenEnvironment.png)

2. <span data-ttu-id="f0f2e-155">Vá para **Projetos** > **Recursos** e, em seguida, selecione **Novo** para criar um recurso reservável para o seu utilizador.</span><span class="sxs-lookup"><span data-stu-id="f0f2e-155">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Recursos Reserváveis](./media/8BookableResources.png)

3. <span data-ttu-id="f0f2e-157">No separador **Geral**, selecione o seu utilizador administrador.</span><span class="sxs-lookup"><span data-stu-id="f0f2e-157">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="f0f2e-158">Verifique se o fuso horário corresponde àquele em que está.</span><span class="sxs-lookup"><span data-stu-id="f0f2e-158">Verify that the time zone matches the one you are in.</span></span> 

![Novo Recurso Reservável](./media/9NewBookableResource.png)

4. <span data-ttu-id="f0f2e-160">No separador **Agendamento**, no campo **Empresa**, escolha a empresa **USPM** e, em seguida, selecione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="f0f2e-160">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Separador Agendamento](./media/10SchedulingTab.png)

5. <span data-ttu-id="f0f2e-162">Selecione o separador **Horas de trabalho**.</span><span class="sxs-lookup"><span data-stu-id="f0f2e-162">Select the **Work hours** tab.</span></span>  

![Horas de Trabalho](./media/11WorkHours.png)

6. <span data-ttu-id="f0f2e-164">Faça duplo clique em qualquer valor no calendário e selecione **Editar** > **Todos os eventos na série**.</span><span class="sxs-lookup"><span data-stu-id="f0f2e-164">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Calendário de Trabalho](./media/12WorkCalendar.png)

7. <span data-ttu-id="f0f2e-166">Altere as horas de trabalho para um dia de trabalho de oito (8) horas, marque os fins de semana como dias de descanso e certifique-se de que o fuso horário corresponde ao seu.</span><span class="sxs-lookup"><span data-stu-id="f0f2e-166">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="f0f2e-167">Selecione **Guardar e fechar**.</span><span class="sxs-lookup"><span data-stu-id="f0f2e-167">Select **Save and close**.</span></span>

![Atualizar Calendário](./media/13UpdateCalendar.png)

9. <span data-ttu-id="f0f2e-169">Vá para **Definições** > **Modelos de calendário** e selecione **Novo**.</span><span class="sxs-lookup"><span data-stu-id="f0f2e-169">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Modelos de Calendário](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="f0f2e-171">Introduza um nome, selecione o recurso de modelo que criou e, em seguida, selecione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="f0f2e-171">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Guardar Modelo de Calendário](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="f0f2e-173">Vá para **Parâmetros** e faça duplo clique no registo.</span><span class="sxs-lookup"><span data-stu-id="f0f2e-173">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Parâmetros do Projeto](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="f0f2e-175">Atualize os seguintes campos:</span><span class="sxs-lookup"><span data-stu-id="f0f2e-175">Update the following fields:</span></span>

 - <span data-ttu-id="f0f2e-176">**Empresa predefinida**: USPM</span><span class="sxs-lookup"><span data-stu-id="f0f2e-176">**Default company**: USPM</span></span>
 - <span data-ttu-id="f0f2e-177">**Unidade Organizacional Predefinida**: Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="f0f2e-177">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="f0f2e-178">**Frequência da Fatura**: Sétimo e Último dia</span><span class="sxs-lookup"><span data-stu-id="f0f2e-178">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="f0f2e-179">**Modelo de horas de trabalho**: altere para o modelo que criou.</span><span class="sxs-lookup"><span data-stu-id="f0f2e-179">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="f0f2e-180">Selecione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="f0f2e-180">Select **Save**.</span></span> 

![Parâmetros do Projeto Atualizados](./media/17UpdatedProjectParameters.png)
