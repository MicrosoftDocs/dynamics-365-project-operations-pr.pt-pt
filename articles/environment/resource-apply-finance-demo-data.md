---
title: Aplicar dados de demonstração a um ambiente alojado no Finance Cloud
description: Este tópico explica como aplicar dados de demonstração do Project Operations a um ambiente alojado na Cloud do Dynamics 365 Finance.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a7239301dc8b775dc4a53a1cf6c0bcba3956125a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289878"
---
# <a name="apply-demo-data-to-a-finance-cloud-hosted-environment"></a><span data-ttu-id="1256b-103">Aplicar dados de demonstração a um ambiente alojado no Finance Cloud</span><span class="sxs-lookup"><span data-stu-id="1256b-103">Apply demo data to a Finance Cloud-hosted environment</span></span>

<span data-ttu-id="1256b-104">_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_</span><span class="sxs-lookup"><span data-stu-id="1256b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1256b-105">Este tópico só é aplicável ao Microsoft Dynamics 365 Finance versão 10.0.13 e só pode ser executado num ambiente alojado na Cloud.</span><span class="sxs-lookup"><span data-stu-id="1256b-105">This topic is only applicable only Microsoft Dynamics 365 Finance version 10.0.13 and can be performed only on a Cloud-hosted environment.</span></span> <span data-ttu-id="1256b-106">Conclua os passos neste tópico **ANTES** de aplicar atualizações de qualidade ao ambiente.</span><span class="sxs-lookup"><span data-stu-id="1256b-106">Complete the steps in this topic **BEFORE** you apply quality updates to the environment.</span></span>

1. <span data-ttu-id="1256b-107">No seu projeto LCS, abra a página **Detalhes do ambiente**.</span><span class="sxs-lookup"><span data-stu-id="1256b-107">In your LCS project, open the **Environment details** page.</span></span> <span data-ttu-id="1256b-108">Note que inclui os detalhes necessários para ligar ao ambiente através do Protocolo RDP (Remote Desktop Protocol).</span><span class="sxs-lookup"><span data-stu-id="1256b-108">Notice that it includes the details needed to connect to the environment by using Remote Desktop Protocol (RDP).</span></span>

![Detalhes do ambiente ](./media/1EnvironmentDetails.png)

<span data-ttu-id="1256b-110">O primeiro conjunto de credenciais realçadas são as credenciais da conta local e contêm uma hiperligação à ligação de ambiente de trabalho remoto.</span><span class="sxs-lookup"><span data-stu-id="1256b-110">The first set of highlighted credentials are the local account credentials and contain a hyperlink to the remote desktop connection.</span></span> <span data-ttu-id="1256b-111">As credenciais incluem o nome de utilizador e a palavra-passe do administrador do ambiente.</span><span class="sxs-lookup"><span data-stu-id="1256b-111">The credentials include the environment admin username and password.</span></span> <span data-ttu-id="1256b-112">O segundo conjunto de credenciais é utilizado para iniciar sessão no SQL Server neste ambiente.</span><span class="sxs-lookup"><span data-stu-id="1256b-112">The second set of credentials are used to log in to SQL Server in this environment.</span></span>

2. <span data-ttu-id="1256b-113">Ligue-se remotamente ao ambiente pela hiperligação em **Contas Locais** e utilize as **Credenciais de Conta Local** autenticar.</span><span class="sxs-lookup"><span data-stu-id="1256b-113">Remote to the environment by the hyperlink in **Local Accounts**, and use the **Local Account credentials** to authenticate.</span></span>
3. <span data-ttu-id="1256b-114">Vá para **Serviços de Informação Internet** > **Conjuntos Aplicacionais** > **AOSService** e pare o serviço.</span><span class="sxs-lookup"><span data-stu-id="1256b-114">Go to **Internet Information Services** > **Application Pools** > **AOSService** and stop the service.</span></span> <span data-ttu-id="1256b-115">Está a parar o serviço neste momento para poder continuar a substituir a base de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="1256b-115">You are stopping the service at this point so that you can continue to replace the SQL database.</span></span>

![Parar AOS](./media/2StopAOS.png)

4. <span data-ttu-id="1256b-117">Vá para **Serviços** e pare os seguintes dois itens:</span><span class="sxs-lookup"><span data-stu-id="1256b-117">Go to **Services** and stop the following two items:</span></span>

- <span data-ttu-id="1256b-118">Microsoft Dynamics 365 Unified Operations: Serviço de Gestão em Lote</span><span class="sxs-lookup"><span data-stu-id="1256b-118">Microsoft Dynamics 365 Unified Operations: Batch Management Service</span></span>
- <span data-ttu-id="1256b-119">Microsoft Dynamics 365 Unified Operations: Quadro de Importação/Exportação de Dados</span><span class="sxs-lookup"><span data-stu-id="1256b-119">Microsoft Dynamics 365 Unified Operations: Data Import Export Framework</span></span>

![Parar Serviços](./media/3StopServices.png)

5. <span data-ttu-id="1256b-121">Abra o Microsoft SQL Server Management Studio.</span><span class="sxs-lookup"><span data-stu-id="1256b-121">Open Microsoft SQL Server Management Studio.</span></span> <span data-ttu-id="1256b-122">Inicie sessão com as credenciais de SQL Server e utilize o utilizador axdbadmin e a palavra-passe da página **Detalhes do ambiente** do LCS.</span><span class="sxs-lookup"><span data-stu-id="1256b-122">Log in with SQL server credentials and use the axdbadmin user and password from the LCS **Environments details** page.</span></span>

![SQL Server Management Studio](./media/4SSMS.png)

6. <span data-ttu-id="1256b-124">No Explorador de Objetos, **Bases de Dados** e localize **AXDB**.</span><span class="sxs-lookup"><span data-stu-id="1256b-124">In Object Explorer, **Databases** and locate **AXDB**.</span></span> <span data-ttu-id="1256b-125">Irá substituir a base de dados por uma nova base de dados que está localizada no [Centro de Transferências](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip).</span><span class="sxs-lookup"><span data-stu-id="1256b-125">You will replace database with a new database that is located in the [Download Center](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip).</span></span> 
7. <span data-ttu-id="1256b-126">Copie o ficheiro zip para a VM à qual está ligado remotamente e extraia o conteúdo do zip.</span><span class="sxs-lookup"><span data-stu-id="1256b-126">Copy the zip file to the VM you are remoted into and extract zip contents.</span></span>
8. <span data-ttu-id="1256b-127">No SQL Server Management Studio, clique com o botão direito do rato em **AxDB** e, em seguida, selecione **Tarefas** > **Repor** > **Base de Dados**.</span><span class="sxs-lookup"><span data-stu-id="1256b-127">In SQL Server Management Studio, right-click **AxDB**, and then select **Tasks** > **Restore** > **Database**.</span></span>

![Repor Base de Dados](./media/5RestoreDatabase.png)

9. <span data-ttu-id="1256b-129">Selecione **Dispositivo de Origem** navegue para o ficheiro extraído do ficheiro zip que copiou.</span><span class="sxs-lookup"><span data-stu-id="1256b-129">Select **Source Device** and navigate to the file extracted from zip you copied.</span></span>

![Dispositivos de Origem](./media/6SourceDevice.png)

10. <span data-ttu-id="1256b-131">Selecione **Opções** e, em seguida, selecione **Substituir a base de dados existente** e **Fechar ligações existentes à base de dados de destino**.</span><span class="sxs-lookup"><span data-stu-id="1256b-131">Select **Options**, and then select **Overwrite the existing database** and **Close existing connections to destination database**.</span></span> 
11. <span data-ttu-id="1256b-132">Selecione **OK**.</span><span class="sxs-lookup"><span data-stu-id="1256b-132">Select **OK**.</span></span>

![Repor Definições](./media/7RestoreSetting.png)

<span data-ttu-id="1256b-134">Receberá a confirmação de que a reposição do AXDB foi concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="1256b-134">You will receive confirmation that the AXDB restore was successful.</span></span> <span data-ttu-id="1256b-135">Depois de receber esta confirmação, poderá fechar o SQL Services Management Studio.</span><span class="sxs-lookup"><span data-stu-id="1256b-135">After you receive this confirmation, you can close SQL Services Management Studio.</span></span>

12. <span data-ttu-id="1256b-136">Vá para **Serviços de Informação Internet** > **Conjuntos Aplicacionais** > **AOSService** e inicie o AOSService.</span><span class="sxs-lookup"><span data-stu-id="1256b-136">Go back to **Internet Information Services** > **Application Pools** > **AOSService** and start the AOSService.</span></span>
13. <span data-ttu-id="1256b-137">Vá para **Serviços** e inicie os dois serviços que parou anteriormente.</span><span class="sxs-lookup"><span data-stu-id="1256b-137">Go to **Services** and start the two services you stopped earlier.</span></span>

14. <span data-ttu-id="1256b-138">Localize a ferramenta AdminUserProvisioning nesta VM.</span><span class="sxs-lookup"><span data-stu-id="1256b-138">Locate the AdminUserProvisioning tool on this VM.</span></span> <span data-ttu-id="1256b-139">Procure em K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.</span><span class="sxs-lookup"><span data-stu-id="1256b-139">Look under, K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.</span></span>
15. <span data-ttu-id="1256b-140">Execute o ficheiro .ext através do seu endereço de utilizador no campo **Endereço de E-mail**.</span><span class="sxs-lookup"><span data-stu-id="1256b-140">Run the .ext file using your user address in the **Email Address** field.</span></span> 
16. <span data-ttu-id="1256b-141">Selecione **Submeter**.</span><span class="sxs-lookup"><span data-stu-id="1256b-141">Select **Submit**.</span></span>

![Aprovisionamento de Utilizadores Administradores](./media/8AdminUserProvisioning.png)

<span data-ttu-id="1256b-143">Isto demora alguns minutos a concluir.</span><span class="sxs-lookup"><span data-stu-id="1256b-143">This takes a couple of minutes to complete.</span></span> <span data-ttu-id="1256b-144">Deve receber uma mensagem de confirmação de que o Utilizador administrador foi atualizado com sucesso.</span><span class="sxs-lookup"><span data-stu-id="1256b-144">You should receive a confirmation message that the Admin user was successfully updated.</span></span>

17. <span data-ttu-id="1256b-145">Por último, execute a Linha de Comandos como Administrador e execute iisreset</span><span class="sxs-lookup"><span data-stu-id="1256b-145">Lastly, run Command Prompt as Administrator and perform iisreset</span></span>

![Reposição do IIS](./media/9IISReset.png)

18. <span data-ttu-id="1256b-147">Feche a sessão de ambiente de trabalho remota e utilize a página **Detalhes do ambiente** do LCS para iniciar sessão no ambiente para confirmar que está a funcionar conforme esperado.</span><span class="sxs-lookup"><span data-stu-id="1256b-147">Close the remote desktop session and use the LCS **Environment details** page to log in to the environment to confirm it is working as expected.</span></span>

![Finance and Operations](./media/10FinanceAndOperations.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]