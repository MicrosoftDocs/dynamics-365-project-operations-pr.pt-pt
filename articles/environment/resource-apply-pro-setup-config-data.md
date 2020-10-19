---
title: Configurar e aplicar dados de configuração no Common Data Service para o Project Operations
description: Este tópico fornece informações sobre como configurar e aplicar dados de configuração no Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d99ab4c7b2ebf6ba56b86a3e0151036c6247e484
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949020"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service-for-project-operations"></a><span data-ttu-id="46c9f-103">Configurar e aplicar dados de configuração no Common Data Service para o Project Operations</span><span class="sxs-lookup"><span data-stu-id="46c9f-103">Set up and apply configuration data in the Common Data Service for Project Operations</span></span>

<span data-ttu-id="46c9f-104">_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_</span><span class="sxs-lookup"><span data-stu-id="46c9f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="46c9f-105">Instalar dados de configuração</span><span class="sxs-lookup"><span data-stu-id="46c9f-105">Install setup and configuration data</span></span>

1. <span data-ttu-id="46c9f-106">Transfira, desbloqueie e descompacte o [Pacote de Dados de Configuração](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span><span class="sxs-lookup"><span data-stu-id="46c9f-106">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span></span>
2. <span data-ttu-id="46c9f-107">Navegue para a pasta descompactada e execute o ficheiro executável *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="46c9f-107">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="46c9f-108">Na página 1 do Assistente de Migração da Configuração do Common Data Service (CMT), selecione **Importar Dados** e, em seguida, selecione **Continuar**.</span><span class="sxs-lookup"><span data-stu-id="46c9f-108">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Migração da Configuração](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="46c9f-110">Na página 2 do Assistente do CMT, selecione **Office 365** como **Tipo de Implementação**.</span><span class="sxs-lookup"><span data-stu-id="46c9f-110">On Page 2 of the CMT Wizard, select **Office 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="46c9f-111">Selecione as caixas de verificação **Apresentar lista de organizações disponíveis** e **Mostrar Avançadas**.</span><span class="sxs-lookup"><span data-stu-id="46c9f-111">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="46c9f-112">Selecione a região do seu inquilino, introduza as suas credenciais e selecione **Iniciar Sessão**.</span><span class="sxs-lookup"><span data-stu-id="46c9f-112">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Início de Sessão da Configuração](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="46c9f-114">Na página 3, a partir da lista de organizações no inquilino, selecione a organização para a qual pretende importar os dados de demonstração e selecione **Iniciar Sessão**.</span><span class="sxs-lookup"><span data-stu-id="46c9f-114">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="46c9f-115">Na página 4, selecione o ficheiro zip *SampleSetupAndConfigData* a partir da pasta descompactada.</span><span class="sxs-lookup"><span data-stu-id="46c9f-115">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Seleção de ficheiros Zip](./media/3ZipFile.png)

![Selecionar um ficheiro](./media/4SelectAFile.png)

9. <span data-ttu-id="46c9f-118">Depois de selecionado o ficheiro zip, selecione **Importar Dados**.</span><span class="sxs-lookup"><span data-stu-id="46c9f-118">After the zip file is selected, select **Import Data**.</span></span>

![Dados de Importação](./media/5ImportData.png)

10. <span data-ttu-id="46c9f-120">A importação será executada durante aproximadamente 2 a 10 minutos, consoante a velocidade da sua rede.</span><span class="sxs-lookup"><span data-stu-id="46c9f-120">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="46c9f-121">Depois de concluída a importação, saia do Assistente de CMT.</span><span class="sxs-lookup"><span data-stu-id="46c9f-121">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="46c9f-122">Contacte a sua organização para obter dados nas seguintes 19 entidades:</span><span class="sxs-lookup"><span data-stu-id="46c9f-122">Check your organization for data in the following 19 entities:</span></span>

  - <span data-ttu-id="46c9f-123">Moeda</span><span class="sxs-lookup"><span data-stu-id="46c9f-123">Currency</span></span>
  - <span data-ttu-id="46c9f-124">Unidade Organizacional</span><span class="sxs-lookup"><span data-stu-id="46c9f-124">Organizational Unit</span></span>
  - <span data-ttu-id="46c9f-125">Contacto</span><span class="sxs-lookup"><span data-stu-id="46c9f-125">Contact</span></span>
  - <span data-ttu-id="46c9f-126">Grupo de Impostos</span><span class="sxs-lookup"><span data-stu-id="46c9f-126">Tax Group</span></span>
  - <span data-ttu-id="46c9f-127">Grupo de Clientes</span><span class="sxs-lookup"><span data-stu-id="46c9f-127">Customer Group</span></span>
  - <span data-ttu-id="46c9f-128">Unidade</span><span class="sxs-lookup"><span data-stu-id="46c9f-128">Unit</span></span>
  - <span data-ttu-id="46c9f-129">Grupo de Unidades</span><span class="sxs-lookup"><span data-stu-id="46c9f-129">Unit Group</span></span>
  - <span data-ttu-id="46c9f-130">Lista de Preços</span><span class="sxs-lookup"><span data-stu-id="46c9f-130">Price List</span></span>
  - <span data-ttu-id="46c9f-131">Lista de Preços do Parâmetro do Projeto</span><span class="sxs-lookup"><span data-stu-id="46c9f-131">Project Parameter Price List</span></span>
  - <span data-ttu-id="46c9f-132">Frequência da Fatura</span><span class="sxs-lookup"><span data-stu-id="46c9f-132">Invoice Frequency</span></span>
  - <span data-ttu-id="46c9f-133">Categoria de Recurso Reservável</span><span class="sxs-lookup"><span data-stu-id="46c9f-133">Bookable Resource Category</span></span>
  - <span data-ttu-id="46c9f-134">Categoria de Transação</span><span class="sxs-lookup"><span data-stu-id="46c9f-134">Transaction Category</span></span>
  - <span data-ttu-id="46c9f-135">Categoria de Despesa</span><span class="sxs-lookup"><span data-stu-id="46c9f-135">Expense Category</span></span>
  - <span data-ttu-id="46c9f-136">Preço da Função</span><span class="sxs-lookup"><span data-stu-id="46c9f-136">Role Price</span></span>
  - <span data-ttu-id="46c9f-137">Preço de Categoria de Transação</span><span class="sxs-lookup"><span data-stu-id="46c9f-137">Transaction Category Price</span></span>
  - <span data-ttu-id="46c9f-138">Característica</span><span class="sxs-lookup"><span data-stu-id="46c9f-138">Characteristic</span></span>
  - <span data-ttu-id="46c9f-139">Recurso Reservável</span><span class="sxs-lookup"><span data-stu-id="46c9f-139">Bookable Resource</span></span>
  - <span data-ttu-id="46c9f-140">Associação de categorias de recurso reservável</span><span class="sxs-lookup"><span data-stu-id="46c9f-140">Bookable resource category Assn</span></span>
  - <span data-ttu-id="46c9f-141">Característica de Recurso Reservável</span><span class="sxs-lookup"><span data-stu-id="46c9f-141">Bookable Resource Characteristic</span></span>

![Concluir Importação](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="46c9f-143">Atualizar configurações do Project Operations</span><span class="sxs-lookup"><span data-stu-id="46c9f-143">Update Project Operations configurations</span></span>

1. <span data-ttu-id="46c9f-144">Navegye para o ambiente CE.</span><span class="sxs-lookup"><span data-stu-id="46c9f-144">Navigate to the CE environment.</span></span> <span data-ttu-id="46c9f-145">Pode encontrá-lo ao abrir o [Centro de Administração do Power Platform](https://admin.powerplatform.microsoft.com/environments), selecionar o ambiente e, em seguida, selecionar **Abrir Ambiente**.</span><span class="sxs-lookup"><span data-stu-id="46c9f-145">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Abrir Ambiente](./media/7OpenEnvironment.png)

2. <span data-ttu-id="46c9f-147">Vá para **Projetos** > **Recursos** e, em seguida, selecione **Novo** para criar um recurso reservável para o seu utilizador.</span><span class="sxs-lookup"><span data-stu-id="46c9f-147">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Recursos Reserváveis](./media/8BookableResources.png)

3. <span data-ttu-id="46c9f-149">No separador **Geral**, selecione o seu utilizador administrador.</span><span class="sxs-lookup"><span data-stu-id="46c9f-149">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="46c9f-150">Verifique se o fuso horário corresponde àquele em que está.</span><span class="sxs-lookup"><span data-stu-id="46c9f-150">Verify that the time zone matches the one you are in.</span></span> 

![Novo Recurso Reservável](./media/9NewBookableResource.png)

4. <span data-ttu-id="46c9f-152">No separador **Agendamento**, no campo **Empresa**, escolha a empresa **USPM** e, em seguida, selecione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="46c9f-152">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Separador Agendamento](./media/10SchedulingTab.png)

5. <span data-ttu-id="46c9f-154">Selecione o separador **Horas de trabalho**.</span><span class="sxs-lookup"><span data-stu-id="46c9f-154">Select the **Work hours** tab.</span></span>  

![Horas de Trabalho](./media/11WorkHours.png)

6. <span data-ttu-id="46c9f-156">Faça duplo clique em qualquer valor no calendário e selecione **Editar** > **Todos os eventos na série**.</span><span class="sxs-lookup"><span data-stu-id="46c9f-156">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Calendário de Trabalho](./media/12WorkCalendar.png)

7. <span data-ttu-id="46c9f-158">Altere as horas de trabalho para um dia de trabalho de oito (8) horas, marque os fins de semana como dias de descanso e certifique-se de que o fuso horário corresponde ao seu.</span><span class="sxs-lookup"><span data-stu-id="46c9f-158">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="46c9f-159">Selecione **Guardar e fechar**.</span><span class="sxs-lookup"><span data-stu-id="46c9f-159">Select **Save and close**.</span></span>

![Atualizar Calendário](./media/13UpdateCalendar.png)

9. <span data-ttu-id="46c9f-161">Vá para **Definições** > **Modelos de calendário** e selecione **Novo**.</span><span class="sxs-lookup"><span data-stu-id="46c9f-161">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Modelos de Calendário](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="46c9f-163">Introduza um nome, selecione o recurso de modelo que criou e, em seguida, selecione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="46c9f-163">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Guardar Modelo de Calendário](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="46c9f-165">Vá para **Parâmetros** e faça duplo clique no registo.</span><span class="sxs-lookup"><span data-stu-id="46c9f-165">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Parâmetros do Projeto](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="46c9f-167">Atualize os seguintes campos:</span><span class="sxs-lookup"><span data-stu-id="46c9f-167">Update the following fields:</span></span>

 - <span data-ttu-id="46c9f-168">**Empresa predefinida**: USPM</span><span class="sxs-lookup"><span data-stu-id="46c9f-168">**Default company**: USPM</span></span>
 - <span data-ttu-id="46c9f-169">**Unidade Organizacional Predefinida**: Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="46c9f-169">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="46c9f-170">**Frequência da Fatura**: Sétimo e Último dia</span><span class="sxs-lookup"><span data-stu-id="46c9f-170">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="46c9f-171">**Modelo de horas de trabalho**: altere para o modelo que criou.</span><span class="sxs-lookup"><span data-stu-id="46c9f-171">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="46c9f-172">Selecione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="46c9f-172">Select **Save**.</span></span> 

![Parâmetros do Projeto Atualizados](./media/17UpdatedProjectParameters.png)
