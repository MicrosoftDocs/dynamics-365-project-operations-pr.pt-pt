---
title: Configurar e aplicar dados de configuração no Common Data Service
description: Este tópico fornece informações sobre como configurar e aplicar dados de configuração no Project Operations.
author: sigitac
ms.date: 05/10/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2ea00df6112fb69b61f1889463424fdfee79aec9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001305"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a><span data-ttu-id="7fbef-103">Configurar e aplicar dados de configuração no Common Data Service</span><span class="sxs-lookup"><span data-stu-id="7fbef-103">Set up and apply configuration data in the Common Data Service</span></span> 

<span data-ttu-id="7fbef-104">_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_</span><span class="sxs-lookup"><span data-stu-id="7fbef-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="7fbef-105">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="7fbef-105">Prerequisites</span></span>

<span data-ttu-id="7fbef-106">Antes de começar a configurar os dados no Common Data Service (CDS), os seguintes pré-requisitos devem ser cumpridos:</span><span class="sxs-lookup"><span data-stu-id="7fbef-106">Before you begin to configure data in the Common Data Service (CDS), the following prerequisites must be met:</span></span>

1.  <span data-ttu-id="7fbef-107">Aprovisionar um ambiente CDS e um ambiente Dynamics 365 Finance para o Project Operations.</span><span class="sxs-lookup"><span data-stu-id="7fbef-107">Provision a CDS environment and a Dynamics 365 Finance environment for Project Operations.</span></span>
2.  <span data-ttu-id="7fbef-108">As informações da entidade jurídica do Dynamics 365 Finance são partilhadas com o ambiente CDS.</span><span class="sxs-lookup"><span data-stu-id="7fbef-108">Legal entity information from Dynamics 365 Finance is shared to the CDS environment.</span></span> <span data-ttu-id="7fbef-109">Isto significa que a entidade **Empresa** tem os seguintes registos da empresa:</span><span class="sxs-lookup"><span data-stu-id="7fbef-109">This means that the **Company** entity in CDS has the following company records:</span></span>
  - <span data-ttu-id="7fbef-110">THPM</span><span class="sxs-lookup"><span data-stu-id="7fbef-110">THPM</span></span>
  - <span data-ttu-id="7fbef-111">USPM</span><span class="sxs-lookup"><span data-stu-id="7fbef-111">USPM</span></span>
  - <span data-ttu-id="7fbef-112">GBPM</span><span class="sxs-lookup"><span data-stu-id="7fbef-112">GBPM</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="7fbef-113">Instalar dados de configuração</span><span class="sxs-lookup"><span data-stu-id="7fbef-113">Install setup and configuration data</span></span>

1. <span data-ttu-id="7fbef-114">Transfira, desbloqueie e descompacte o [Pacote de Dados de Configuração](https://download.microsoft.com/download/e/2/d/e2da6c98-d5dd-450c-aabe-fd6bf2ba374b/ProjOpsSampleSetupData-%20Integrated%20Latest.zip).</span><span class="sxs-lookup"><span data-stu-id="7fbef-114">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/e/2/d/e2da6c98-d5dd-450c-aabe-fd6bf2ba374b/ProjOpsSampleSetupData-%20Integrated%20Latest.zip).</span></span>
2. <span data-ttu-id="7fbef-115">Navegue para a pasta descompactada e execute o ficheiro executável *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="7fbef-115">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="7fbef-116">Na página 1 do Assistente de Migração da Configuração do Common Data Service (CMT), selecione **Importar Dados** e, em seguida, selecione **Continuar**.</span><span class="sxs-lookup"><span data-stu-id="7fbef-116">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Migração da Configuração](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="7fbef-118">Na Página 2 do Assistente do CMT, selecione **Microsoft 365** como **Tipo de Implementação**.</span><span class="sxs-lookup"><span data-stu-id="7fbef-118">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="7fbef-119">Selecione as caixas de verificação **Apresentar lista de organizações disponíveis** e **Mostrar Avançadas**.</span><span class="sxs-lookup"><span data-stu-id="7fbef-119">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="7fbef-120">Selecione a região do seu inquilino, introduza as suas credenciais e selecione **Iniciar Sessão**.</span><span class="sxs-lookup"><span data-stu-id="7fbef-120">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Início de Sessão da Configuração](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="7fbef-122">Na página 3, a partir da lista de organizações no inquilino, selecione a organização para a qual pretende importar os dados de demonstração e selecione **Iniciar Sessão**.</span><span class="sxs-lookup"><span data-stu-id="7fbef-122">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="7fbef-123">Na página 4, selecione o ficheiro zip *SampleSetupAndConfigData* a partir da pasta descompactada.</span><span class="sxs-lookup"><span data-stu-id="7fbef-123">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Seleção de ficheiros Zip](./media/3ZipFile.png)

![Selecionar um ficheiro](./media/4SelectAFile.png)

9. <span data-ttu-id="7fbef-126">Depois de selecionado o ficheiro zip, selecione **Importar Dados**.</span><span class="sxs-lookup"><span data-stu-id="7fbef-126">After the zip file is selected, select **Import Data**.</span></span>

![Dados de Importação](./media/5ImportData.png)

10. <span data-ttu-id="7fbef-128">A importação será executada durante aproximadamente 2 a 10 minutos, consoante a velocidade da sua rede.</span><span class="sxs-lookup"><span data-stu-id="7fbef-128">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="7fbef-129">Depois de concluída a importação, saia do Assistente de CMT.</span><span class="sxs-lookup"><span data-stu-id="7fbef-129">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="7fbef-130">Contacte a sua organização para obter dados nas seguintes 26 entidades:</span><span class="sxs-lookup"><span data-stu-id="7fbef-130">Check your organization for data in the following 26 entities:</span></span>

  - <span data-ttu-id="7fbef-131">Moeda</span><span class="sxs-lookup"><span data-stu-id="7fbef-131">Currency</span></span>
  - <span data-ttu-id="7fbef-132">Tabela de Contas</span><span class="sxs-lookup"><span data-stu-id="7fbef-132">Chart of Accounts</span></span>
  - <span data-ttu-id="7fbef-133">Calendário Fiscal</span><span class="sxs-lookup"><span data-stu-id="7fbef-133">Fiscal Calendar</span></span>
  - <span data-ttu-id="7fbef-134">Tipos de Câmbio de Moeda</span><span class="sxs-lookup"><span data-stu-id="7fbef-134">Currency Exchange Rate Types</span></span>
  - <span data-ttu-id="7fbef-135">Dia de Pagamento</span><span class="sxs-lookup"><span data-stu-id="7fbef-135">Payment Day</span></span>
  - <span data-ttu-id="7fbef-136">Agenda de Pagamento</span><span class="sxs-lookup"><span data-stu-id="7fbef-136">Payment Schedule</span></span>
  - <span data-ttu-id="7fbef-137">Prazo de Pagamento</span><span class="sxs-lookup"><span data-stu-id="7fbef-137">Payment Term</span></span>
  - <span data-ttu-id="7fbef-138">Unidade Organizacional</span><span class="sxs-lookup"><span data-stu-id="7fbef-138">Organizational Unit</span></span>
  - <span data-ttu-id="7fbef-139">Contacto</span><span class="sxs-lookup"><span data-stu-id="7fbef-139">Contact</span></span>
  - <span data-ttu-id="7fbef-140">Grupo de Impostos</span><span class="sxs-lookup"><span data-stu-id="7fbef-140">Tax Group</span></span>
  - <span data-ttu-id="7fbef-141">Grupo de Clientes</span><span class="sxs-lookup"><span data-stu-id="7fbef-141">Customer Group</span></span>
  - <span data-ttu-id="7fbef-142">Grupo de Fornecedores</span><span class="sxs-lookup"><span data-stu-id="7fbef-142">Vendor Group</span></span>
  - <span data-ttu-id="7fbef-143">Unidade</span><span class="sxs-lookup"><span data-stu-id="7fbef-143">Unit</span></span>
  - <span data-ttu-id="7fbef-144">Grupo de Unidades</span><span class="sxs-lookup"><span data-stu-id="7fbef-144">Unit Group</span></span>
  - <span data-ttu-id="7fbef-145">Lista de Preços</span><span class="sxs-lookup"><span data-stu-id="7fbef-145">Price List</span></span>
  - <span data-ttu-id="7fbef-146">Lista de Preços do Parâmetro do Projeto</span><span class="sxs-lookup"><span data-stu-id="7fbef-146">Project Parameter Price List</span></span>
  - <span data-ttu-id="7fbef-147">Frequência da Fatura</span><span class="sxs-lookup"><span data-stu-id="7fbef-147">Invoice Frequency</span></span>
  - <span data-ttu-id="7fbef-148">Categoria de Recurso Reservável</span><span class="sxs-lookup"><span data-stu-id="7fbef-148">Bookable Resource Category</span></span>
  - <span data-ttu-id="7fbef-149">Categoria de Transação</span><span class="sxs-lookup"><span data-stu-id="7fbef-149">Transaction Category</span></span>
  - <span data-ttu-id="7fbef-150">Categoria de Despesa</span><span class="sxs-lookup"><span data-stu-id="7fbef-150">Expense Category</span></span>
  - <span data-ttu-id="7fbef-151">Preço da Função</span><span class="sxs-lookup"><span data-stu-id="7fbef-151">Role Price</span></span>
  - <span data-ttu-id="7fbef-152">Preço de Categoria de Transação</span><span class="sxs-lookup"><span data-stu-id="7fbef-152">Transaction Category Price</span></span>
  - <span data-ttu-id="7fbef-153">Característica</span><span class="sxs-lookup"><span data-stu-id="7fbef-153">Characteristic</span></span>
  - <span data-ttu-id="7fbef-154">Recurso Reservável</span><span class="sxs-lookup"><span data-stu-id="7fbef-154">Bookable Resource</span></span>
  - <span data-ttu-id="7fbef-155">Associação de categorias de recurso reservável</span><span class="sxs-lookup"><span data-stu-id="7fbef-155">Bookable resource category Assn</span></span>
  - <span data-ttu-id="7fbef-156">Característica de Recurso Reservável</span><span class="sxs-lookup"><span data-stu-id="7fbef-156">Bookable Resource Characteristic</span></span>

![Concluir Importação](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="7fbef-158">Atualizar configurações do Project Operations</span><span class="sxs-lookup"><span data-stu-id="7fbef-158">Update Project Operations configurations</span></span>

1. <span data-ttu-id="7fbef-159">Navegye para o ambiente CE.</span><span class="sxs-lookup"><span data-stu-id="7fbef-159">Navigate to the CE environment.</span></span> <span data-ttu-id="7fbef-160">Pode encontrá-lo ao abrir o [Centro de Administração do Power Platform](https://admin.powerplatform.microsoft.com/environments), selecionar o ambiente e, em seguida, selecionar **Abrir Ambiente**.</span><span class="sxs-lookup"><span data-stu-id="7fbef-160">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Abrir Ambiente](./media/7OpenEnvironment.png)

2. <span data-ttu-id="7fbef-162">Vá para **Projetos** > **Recursos** e, em seguida, selecione **Novo** para criar um recurso reservável para o seu utilizador.</span><span class="sxs-lookup"><span data-stu-id="7fbef-162">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Recursos Reserváveis](./media/8BookableResources.png)

3. <span data-ttu-id="7fbef-164">No separador **Geral**, selecione o seu utilizador administrador.</span><span class="sxs-lookup"><span data-stu-id="7fbef-164">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="7fbef-165">Verifique se o fuso horário corresponde àquele em que está.</span><span class="sxs-lookup"><span data-stu-id="7fbef-165">Verify that the time zone matches the one you are in.</span></span> 

![Novo Recurso Reservável](./media/9NewBookableResource.png)

4. <span data-ttu-id="7fbef-167">No separador **Agendamento**, no campo **Empresa**, escolha a empresa **USPM** e, em seguida, selecione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="7fbef-167">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Separador Agendamento](./media/10SchedulingTab.png)

5. <span data-ttu-id="7fbef-169">Selecione o separador **Horas de trabalho**.</span><span class="sxs-lookup"><span data-stu-id="7fbef-169">Select the **Work hours** tab.</span></span>  

![Horas de Trabalho](./media/11WorkHours.png)

6. <span data-ttu-id="7fbef-171">Faça duplo clique em qualquer valor no calendário e selecione **Editar** > **Todos os eventos na série**.</span><span class="sxs-lookup"><span data-stu-id="7fbef-171">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Calendário de Trabalho](./media/12WorkCalendar.png)

7. <span data-ttu-id="7fbef-173">Altere as horas de trabalho para um dia de trabalho de oito (8) horas, marque os fins de semana como dias de descanso e certifique-se de que o fuso horário corresponde ao seu.</span><span class="sxs-lookup"><span data-stu-id="7fbef-173">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="7fbef-174">Selecione **Guardar e fechar**.</span><span class="sxs-lookup"><span data-stu-id="7fbef-174">Select **Save and close**.</span></span>

![Atualizar Calendário](./media/13UpdateCalendar.png)

9. <span data-ttu-id="7fbef-176">Vá para **Definições** > **Modelos de calendário** e selecione **Novo**.</span><span class="sxs-lookup"><span data-stu-id="7fbef-176">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Modelos de Calendário](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="7fbef-178">Introduza um nome, selecione o recurso de modelo que criou e, em seguida, selecione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="7fbef-178">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Guardar Modelo de Calendário](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="7fbef-180">Vá para **Parâmetros** e faça duplo clique no registo.</span><span class="sxs-lookup"><span data-stu-id="7fbef-180">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Parâmetros do Projeto](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="7fbef-182">Atualize os seguintes campos:</span><span class="sxs-lookup"><span data-stu-id="7fbef-182">Update the following fields:</span></span>

 - <span data-ttu-id="7fbef-183">**Empresa predefinida**: USPM</span><span class="sxs-lookup"><span data-stu-id="7fbef-183">**Default company**: USPM</span></span>
 - <span data-ttu-id="7fbef-184">**Unidade Organizacional Predefinida**: Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="7fbef-184">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="7fbef-185">**Frequência da Fatura**: Sétimo e Último dia</span><span class="sxs-lookup"><span data-stu-id="7fbef-185">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="7fbef-186">**Modelo de horas de trabalho**: altere para o modelo que criou.</span><span class="sxs-lookup"><span data-stu-id="7fbef-186">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="7fbef-187">Selecione **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="7fbef-187">Select **Save**.</span></span> 

![Parâmetros do Projeto Atualizados](./media/17UpdatedProjectParameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
