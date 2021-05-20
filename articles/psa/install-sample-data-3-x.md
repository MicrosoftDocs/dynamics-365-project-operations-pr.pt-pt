---
title: Instalação de dados de exemplo
description: Este tópico fornece informações sobre a instalação de dados de exemplo no Project Service Automation.
ms.custom: dyn365-projectservice
ms.date: 11/08/2018
ms.service: project-operations
ms.reviewer: kfend
ms.suite: ''
applies_to: Dynamics 365 Project Service Automation
author: ruhercul
ms.author: ruhercul
search.audienceType: IT Pro, Developer
search.app: ''
ms.openlocfilehash: c521fb4000b4856fc5c2fbf3275bf3b3e0dfa458
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950593"
---
# <a name="sample-data-installation-for-the-project-service-application"></a><span data-ttu-id="125de-103">Instalação de dados de exemplo para a aplicação Project Service</span><span class="sxs-lookup"><span data-stu-id="125de-103">Sample data installation for the Project Service application</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="125de-104">Para ajudar a criar os seus próprios ambientes de demonstração, a Microsoft fornece pacotes de dados de exemplo transferíveis para demonstrar as capacidades das suas aplicações.</span><span class="sxs-lookup"><span data-stu-id="125de-104">To help you build your own demo environments, Microsoft provides downloadable sample data packages that showcase the capabilities of your apps.</span></span> <span data-ttu-id="125de-105">Existem dois tipos de pacotes de dados de exemplo:</span><span class="sxs-lookup"><span data-stu-id="125de-105">There are two types of sample data packages:</span></span>
- <span data-ttu-id="125de-106">dados de referência/configuração</span><span class="sxs-lookup"><span data-stu-id="125de-106">reference/setup data</span></span>
- <span data-ttu-id="125de-107">dados de demonstração (dados de referência/configuração e transacionais, tais como ordens de intervenção e projetos)</span><span class="sxs-lookup"><span data-stu-id="125de-107">demo data (reference/setup and transactional data such as work orders and projects)</span></span>

<span data-ttu-id="125de-108">Os pacotes de dados de exemplo **referência** podem ser transferidos em três pacotes diferentes, para que possa instalar dados apenas no Project Service ou apenas no Field Service, ou para que possa instalar dados de exemplo nas duas aplicações em simultâneo.</span><span class="sxs-lookup"><span data-stu-id="125de-108">The sample **reference** data packages are downloadable in three different packages, so you can install data only for Project Service, or only for Field Service, or you can install sample data for both applications at once.</span></span>

<span data-ttu-id="125de-109">Os pacotes de dados de exemplo configuração/referência são:</span><span class="sxs-lookup"><span data-stu-id="125de-109">The sample setup/reference data packages are:</span></span>

- [<span data-ttu-id="125de-110">**V902PSMasterData** - Project Service versão 3.x apenas</span><span class="sxs-lookup"><span data-stu-id="125de-110">**V902PSMasterData** - Project Service version 3.x only</span></span>](https://go.microsoft.com/fwlink/?linkid=2026540&clcid=0x409)

- [<span data-ttu-id="125de-111">**V902FSMasterData** - Field Service versão 8.x apenas</span><span class="sxs-lookup"><span data-stu-id="125de-111">**V902FSMasterData** - Field Service version 8.x only</span></span>](https://go.microsoft.com/fwlink/?linkid=2026536&clcid=0x409)

- [<span data-ttu-id="125de-112">**V902FPSMasterData** - Field Service 8.x e Project Service 3.x</span><span class="sxs-lookup"><span data-stu-id="125de-112">**V902FPSMasterData** - Field Service 8.x and Project Service 3.x</span></span>](https://go.microsoft.com/fwlink/?linkid=2026041&clcid=0x409)

<span data-ttu-id="125de-113">O último pacote de dados de **demonstração** é:</span><span class="sxs-lookup"><span data-stu-id="125de-113">The latest **demo** data package is:</span></span>

 - [<span data-ttu-id="125de-114">**FPSDemoData** - Field Service 8.x e Project Service 3.x</span><span class="sxs-lookup"><span data-stu-id="125de-114">**FPSDemoData** - Field Service 8.x and Project Service 3.x</span></span>](https://aka.ms/fpsdemodatapackage)

   <span data-ttu-id="125de-115">As instruções de instalação diferem ligeiramente nos utilizadores para criar e configurar uma secção, mas o resto é igual como na anterior [**publicação do blogue**](https://aka.ms/fpsdemodatablog).</span><span class="sxs-lookup"><span data-stu-id="125de-115">Installation instructions differ slightly in the users to create and configure section but the rest is the same as in the previous [**blog post**](https://aka.ms/fpsdemodatablog).</span></span> <span data-ttu-id="125de-116">Este pacote apresenta um conjunto de dados de demonstração reduzido e demora aproximadamente 3 horas para instalar.</span><span class="sxs-lookup"><span data-stu-id="125de-116">This package features a reduced demo data set and takes approximately 3 hours to install.</span></span>

<span data-ttu-id="125de-117">Estes pacotes de dados de exemplo só estão disponíveis em inglês.</span><span class="sxs-lookup"><span data-stu-id="125de-117">These sample data packages are available in English only.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="125de-118">**Não é possível desinstalar os dados de exemplo.**</span><span class="sxs-lookup"><span data-stu-id="125de-118">**There is no way to uninstall the sample data.**</span></span> <span data-ttu-id="125de-119">Só deve instalar estes pacotes nos sistemas de demonstração, avaliação, formação ou teste.</span><span class="sxs-lookup"><span data-stu-id="125de-119">You should only install these packages on demonstration, evaluation, training, or test systems.</span></span> <span data-ttu-id="125de-120">Note também que instalar um pacote individual e, em seguida, instalar o outro pacote individual, não é suportado.</span><span class="sxs-lookup"><span data-stu-id="125de-120">Also note that installing an individual package, and then installing the other individual package, is not supported.</span></span> <span data-ttu-id="125de-121">(Ou seja, não é possível instalar **FSMasterData** e, em seguida, **PSMasterData**, ou vice versa.) Se necessitar de dados de exemplo para as duas aplicações mais tarde, deverá instalar o pacote **v902FPSMasterData**.</span><span class="sxs-lookup"><span data-stu-id="125de-121">(In other words, you can't install **FSMasterData** followed by **PSMasterData**, or vice versa.) If you see yourself needing sample data for both applications at any point in the future, you should install the **v902FPSMasterData** package.</span></span>

<span data-ttu-id="125de-122">Quando instala qualquer um dos pacotes de dados de exemplo, o processo de instalação efetua as seguintes acções:</span><span class="sxs-lookup"><span data-stu-id="125de-122">When you install any of the sample data packages, the installation process performs the following actions:</span></span>

- <span data-ttu-id="125de-123">Cria ou define parâmetros predefinidos para utilizar o Project Service, Field Service ou ambas as aplicações (se aplicável).</span><span class="sxs-lookup"><span data-stu-id="125de-123">Creates or sets default parameters for using Project Service, Field Service, or both applications (if applicable).</span></span>

- <span data-ttu-id="125de-124">Importa dados de exemplo para as aplicações, tais como recursos reserváveis, direitos específicos da aplicação, listas de vendas e preços de custo, unidades organizacionais, registos do processo de vendas e outras entidades para demonstrar as principais capacidades.</span><span class="sxs-lookup"><span data-stu-id="125de-124">Imports sample data for the applications, such as bookable resources, application-specific roles, sales and cost price lists, organizational units, sales process records, and other entities to demonstrate key capabilities.</span></span>  

<span data-ttu-id="125de-125">Com o pacote **dados de demonstração**, obtém os dados de transações acima e adicionais, tais como ordens de intervenção e projetos.</span><span class="sxs-lookup"><span data-stu-id="125de-125">With the **demo data** package, you get the above and additional transactional data such as work orders and projects.</span></span>

<span data-ttu-id="125de-126">Não sabe que capacidades pode demonstrar com os dados de exemplo?</span><span class="sxs-lookup"><span data-stu-id="125de-126">Wondering what capabilities you can demo with the sample data?</span></span> <span data-ttu-id="125de-127">Veja o cenário fictício da Fabrikam Robotics nas [Notas técnicas](#technical-notes).</span><span class="sxs-lookup"><span data-stu-id="125de-127">See the Fabrikam Robotics fictitious scenario in [Technical notes](#technical-notes).</span></span>

<span data-ttu-id="125de-128">Se tiver dúvidas sobre a instalação destes pacotes de dados de exemplo, [envie-nos um e-mail para fpsdemodata@microsoft.com](mailto:fpsdemodata@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="125de-128">If you have questions about installing these sample data packages, [send us an email at fpsdemodata@microsoft.com](mailto:fpsdemodata@microsoft.com).</span></span>

## <a name="requirements"></a><span data-ttu-id="125de-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="125de-129">Requirements</span></span>

<span data-ttu-id="125de-130">O protocolo de instalação assume o seguinte sobre a instância alvo (org):</span><span class="sxs-lookup"><span data-stu-id="125de-130">The installation protocol assumes the following about your target instance (org):</span></span>

- <span data-ttu-id="125de-131">O idioma base é inglês e a moeda base é dólares norte-americanos (USD, $).</span><span class="sxs-lookup"><span data-stu-id="125de-131">Base language is English and base currency is US dollar (USD,$).</span></span>

- <span data-ttu-id="125de-132">A organização ainda não tem dados do Project Service ou Field Service ou apenas tem dados predefinidos de barebones que são fornecidos com qualquer organização nova.</span><span class="sxs-lookup"><span data-stu-id="125de-132">The org has no Project Service or Field Service data already, or only has barebones default data that comes with any new org.</span></span>

- <span data-ttu-id="125de-133">A versão correta da aplicação de negócio já está instalada:</span><span class="sxs-lookup"><span data-stu-id="125de-133">The correct version of the business application is already installed:</span></span>
       
    - <span data-ttu-id="125de-134">**Para FPSDemoData ou v902FPSMasterData:** a organização tem o Field Service versão 8.x e Project Service versão 3.x instalados.</span><span class="sxs-lookup"><span data-stu-id="125de-134">**For FPSDemoData or v902FPSMasterData:** The org has Field Service version 8.x and Project Service version 3.x installed.</span></span>

    - <span data-ttu-id="125de-135">**Para v902PSMasterData:** a organização tem o Project Service versão 3.x instalado.</span><span class="sxs-lookup"><span data-stu-id="125de-135">**For v902PSMasterData:** The org has Project Service version 3.x installed.</span></span>

    - <span data-ttu-id="125de-136">**Para v902FSMasterData:** a organização tem o Field Service versão 8.x instalado.</span><span class="sxs-lookup"><span data-stu-id="125de-136">**For v902FSMasterData:** The org has Field Service version 8.x installed.</span></span>

> [!NOTE]
> <span data-ttu-id="125de-137">Se necessitar de instalar os dados de exemplo sobre uma versão de avaliação ou ambiente de demonstração existente do Project Service e Field Service que já contém dados (não recomendado), terá de suspender as pré-verificações de segurança efetuadas pelo programa de instalação.</span><span class="sxs-lookup"><span data-stu-id="125de-137">If you need to install the sample data on top of an existing Project Service and Field Service trial or demo environment that already has data (not recommended), you'll need to suspend the safety prechecks performed by the installer.</span></span> <span data-ttu-id="125de-138">Para mais informações, consulte as notas técnicas abaixo.</span><span class="sxs-lookup"><span data-stu-id="125de-138">For more information, see the technical notes below.</span></span>

## <a name="prepare-for-installation"></a><span data-ttu-id="125de-139">Preparar a instalação</span><span class="sxs-lookup"><span data-stu-id="125de-139">Prepare for installation</span></span>

<span data-ttu-id="125de-140">Tem de executar o programa de instalação num computador com uma versão recente do Windows (Windows 10 preferencialmente).</span><span class="sxs-lookup"><span data-stu-id="125de-140">You need to run the installer on a computer with a recent version of Windows (Windows 10 preferred).</span></span>

<span data-ttu-id="125de-141">Deverá planear que o computador permaneça com ligação a uma rede e que a instalação fique a executar até **1 hora** para **dados de configuração/referência**.</span><span class="sxs-lookup"><span data-stu-id="125de-141">You should plan for the computer to remain connected to a network, and for the installation to run for up to **1 hour** for **setup/reference data**.</span></span> <span data-ttu-id="125de-142">(Normalmente a instalação demora cerca de 30 minutos para **FPSMasterData**, que inclui dados de exemplo para ambas as aplicações.) Para **FPSDemoData**, a instalação demorará cerca de **3 horas**.</span><span class="sxs-lookup"><span data-stu-id="125de-142">(Normally the installation takes around 30 minutes for **FPSMasterData**, which includes sample data for both applications.) For the **FPSDemoData**, the installation will take around **3 hours**.</span></span>

<span data-ttu-id="125de-143">O computador deverá ter a função de proteção de ecrã desativada.</span><span class="sxs-lookup"><span data-stu-id="125de-143">The computer should have the screen saver function turned off.</span></span> <span data-ttu-id="125de-144">Caso contrário, as credenciais de sessão para a instalação podem ser perdidas quando a proteção de ecrã é acionada (a menos que mantenha a sua sessão sempre ativa).</span><span class="sxs-lookup"><span data-stu-id="125de-144">Otherwise, session credentials for the installation may be lost when the screen saver engages (unless you keep your session active throughout).</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="125de-145">![Captura de ecrã das definições da proteção de ecrã, com a proteção de ecrã desativada](media/sample-data-1.png)</span><span class="sxs-lookup"><span data-stu-id="125de-145">![Screenshot of screen saver settings, with screen saver turned off](media/sample-data-1.png)</span></span>

## <a name="download-and-unpack"></a><span data-ttu-id="125de-146">Transferir e descompactar</span><span class="sxs-lookup"><span data-stu-id="125de-146">Download and unpack</span></span>

<span data-ttu-id="125de-147">O programa de instalação de dados de exemplo do Project Service e Field Service é distribuído como executável de extração automática.</span><span class="sxs-lookup"><span data-stu-id="125de-147">The Project Service and Field Service sample data installer is distributed as a self-extracting executable.</span></span> <span data-ttu-id="125de-148">Os nomes de ficheiro podem variar consoante o pacote de dados de exemplo, mas caso contrário, os passos são iguais seja qual for o pacote que instale.</span><span class="sxs-lookup"><span data-stu-id="125de-148">The file names may vary depending on the sample data package, but otherwise the steps are the same no matter which package you install.</span></span>

<span data-ttu-id="125de-149">Depois de transferir um pacote, execute o ficheiro .exe e, em seguida, aceite os termos e condições para descompactar o ficheiro comprimido zip.</span><span class="sxs-lookup"><span data-stu-id="125de-149">After downloading a package, run the .exe file, and then accept terms and conditions to unpack the compressed zip file.</span></span> <span data-ttu-id="125de-150">Depois tem de extrair o conteúdo desse ficheiro para uma pasta no computador.</span><span class="sxs-lookup"><span data-stu-id="125de-150">You then need to extract contents of that file to a folder on the computer.</span></span>

<span data-ttu-id="125de-151">Consoante as definições de segurança e do sistema operativo, poderá ter de realizar os seguintes passos após a descompactação do ficheiro zip:</span><span class="sxs-lookup"><span data-stu-id="125de-151">Depending on the operating system and security settings, you may need to perform the following steps after unpacking the zip file:</span></span>

1. <span data-ttu-id="125de-152">Localize e clique com o botão direito do rato no ficheiro **FPSDemoData.dll** na pasta **v902FPSMasterData** / **PackageDeployer_FPSDemoData**.</span><span class="sxs-lookup"><span data-stu-id="125de-152">Find and right-click the **FPSDemoData.dll** file in the **v902FPSMasterData** / **PackageDeployer_FPSDemoData** folder.</span></span>

2. <span data-ttu-id="125de-153">Escolha **Desbloquear**.</span><span class="sxs-lookup"><span data-stu-id="125de-153">Choose **Unblock**.</span></span>

3. <span data-ttu-id="125de-154">Selecione **Aplicar**.</span><span class="sxs-lookup"><span data-stu-id="125de-154">Select **Apply**.</span></span>

4. <span data-ttu-id="125de-155">Selecione **OK**.</span><span class="sxs-lookup"><span data-stu-id="125de-155">Select **OK**.</span></span>


## <a name="create-or-configure-users"></a><span data-ttu-id="125de-156">Criar ou configurar os utilizadores</span><span class="sxs-lookup"><span data-stu-id="125de-156">Create or configure users</span></span>

<span data-ttu-id="125de-157">O pacote **FPSDemoData** requer seis utilizadores, enquanto que os pacotes **FPSMasterData** requerem um utilizador.</span><span class="sxs-lookup"><span data-stu-id="125de-157">The **FPSDemoData** package requires six users while **FPSMasterData** packages require one user.</span></span> <span data-ttu-id="125de-158">Consulte o mais adequado para o seu pacote de dados de exemplo.</span><span class="sxs-lookup"><span data-stu-id="125de-158">Refer to the correct one for your sample data package.</span></span>

## <a name="create-or-configure-users---setupreference-data-packages"></a><span data-ttu-id="125de-159">Criar ou configurar utilizadores - pacotes de dados de configuração/referência</span><span class="sxs-lookup"><span data-stu-id="125de-159">Create or configure users - setup/reference data packages</span></span>

<span data-ttu-id="125de-160">O pacote **FPSMasterData** foi concebido para instalar com um utilizador denominado Spencer Low com as definições descritas aqui.</span><span class="sxs-lookup"><span data-stu-id="125de-160">The **FPSMasterData** package is designed to install with one user named Spencer Low with the settings described here.</span></span> <span data-ttu-id="125de-161">Para instalar o pacote corretamente, é necessário criar (ou mudar o nome temporariamente dos) utilizadores no seu ambiente para que correspondam à configuração de dados de exemplo de entrada.</span><span class="sxs-lookup"><span data-stu-id="125de-161">To install the package correctly, you need to create (or temporarily rename) users in your environment to match the incoming sample data configuration.</span></span>

<span data-ttu-id="125de-162">Para criar ou configurar os utilizadores, vá a **Definições** > **Segurança** > **Utilizadores** e efetue o seguinte:</span><span class="sxs-lookup"><span data-stu-id="125de-162">To create or configure users, go to **Settings** > **Security** > **Users**, and do the following:</span></span>

1. <span data-ttu-id="125de-163">Defina UserFullname="Spencer Low" com o nome de utilizador "spencerl" (**letra minúscula**) para as funções de Gestor de projeto e Gestor de práticas.</span><span class="sxs-lookup"><span data-stu-id="125de-163">Set UserFullname="Spencer Low" with username "spencerl" (**lowercase**) to the Project Manager and Practice Manager roles.</span></span>

2. <span data-ttu-id="125de-164">Selecione o utilizador **Spencer Low** e, em seguida, selecione **Gerir Funções**.</span><span class="sxs-lookup"><span data-stu-id="125de-164">Select the **Spencer Low** user, and then select **Manage Roles**.</span></span> <span data-ttu-id="125de-165">Localize e selecione a função **Administrador de sistema** e, em seguida, selecione **Ok** para conceder direitos de administração completos a Spencer Low.</span><span class="sxs-lookup"><span data-stu-id="125de-165">Find and select the **System Administrator** role, and then select **OK** to grant full admin rights to Spencer Low.</span></span> <span data-ttu-id="125de-166">Este passo é necessário para assegurar que os registos de exemplo são criados com a propriedade do utilizador correta e, assim, povoar vistas corretamente.</span><span class="sxs-lookup"><span data-stu-id="125de-166">This step is necessary to ensure that sample records are created with the correct user ownership and therefore populate views correctly.</span></span>

3. <span data-ttu-id="125de-167">Do pacote transferido, é necessário atualizar um ficheiro de mapeamento de dados com endereços de e-mail do contexto de utilizador predefinido.</span><span class="sxs-lookup"><span data-stu-id="125de-167">From the downloaded package, you need to update a data mapping file with email addresses of the default user context.</span></span> <span data-ttu-id="125de-168">Para tal, abra **PkgFolder** e, em seguida, localize e abra o ficheiro **ImportUserMapFile.xml** no Bloco de Notas (ou Visual Studio ou outro editor de XML).</span><span class="sxs-lookup"><span data-stu-id="125de-168">To do this, open **PkgFolder**, and then find and open the **ImportUserMapFile.xml** file in Notepad (or Visual Studio or another XML editor).</span></span> <span data-ttu-id="125de-169">Defina o campo **DefaultUserToMapTo=** com o endereço de e-mail do utilizador Spencer Low.</span><span class="sxs-lookup"><span data-stu-id="125de-169">Set the **DefaultUserToMapTo=** field to the email address of the Spencer Low user.</span></span>

4. <span data-ttu-id="125de-170">Se não utilizar Spencer Low com o nome de utilizador **spencerl**, necessita de atualizar um ficheiro adicional.</span><span class="sxs-lookup"><span data-stu-id="125de-170">If you aren't using Spencer Low with username **spencerl**, you need to update an additional file.</span></span> <span data-ttu-id="125de-171">Abra o ficheiro **DemoDataPreImportConfig.xml** e, em seguida, localize a etiqueta **userstocreateandconfigure**.</span><span class="sxs-lookup"><span data-stu-id="125de-171">Open the **DemoDataPreImportConfig.xml** file, and then find the **userstocreateandconfigure** tag.</span></span> <span data-ttu-id="125de-172">Atualize a etiqueta **\<login\>** com o nome de utilizador do utilizador Rafael Alvarez.</span><span class="sxs-lookup"><span data-stu-id="125de-172">Update the **\<login\>** tag with the username of your Spencer Low user.</span></span> <span data-ttu-id="125de-173">Para mais informações, consulte as [Notas técnicas](#technical-notes).</span><span class="sxs-lookup"><span data-stu-id="125de-173">For additional details, see [Technical notes](#technical-notes).</span></span>

## <a name="create-or-configure-users---demo-data-package"></a><span data-ttu-id="125de-174">Criar ou configurar utilizadores - pacote de dados de demonstração</span><span class="sxs-lookup"><span data-stu-id="125de-174">Create or configure users - demo data package</span></span>

<span data-ttu-id="125de-175">O pacote de dados de demonstração requer seis utilizadores.</span><span class="sxs-lookup"><span data-stu-id="125de-175">The demo data package requires six users.</span></span> <span data-ttu-id="125de-176">Para que o pacote seja instalado corretamente, efectue o seguinte:</span><span class="sxs-lookup"><span data-stu-id="125de-176">For the package to install correctly, do the following:</span></span>

 1. <span data-ttu-id="125de-177">Crie ou mude o nome temporariamente dos utilizadores existentes para corresponder à configuração dos dados de exemplo recebidos, acedendo a **Definições** > **Segurança** > **Utilizadores**.</span><span class="sxs-lookup"><span data-stu-id="125de-177">Create or temporarily rename existing users to match incoming sample data configuration by going to **Settings** > **Security** > **Users**.</span></span>
 
    <span data-ttu-id="125de-178">Estes direitos só são necessários para demonstrações baseadas nas pessoas.</span><span class="sxs-lookup"><span data-stu-id="125de-178">These roles are only needed for persona-based demos.</span></span>  
    - <span data-ttu-id="125de-179">Utilizador Fullname="David So" como Técnico de Field Service</span><span class="sxs-lookup"><span data-stu-id="125de-179">User Fullname="David So" as Field Service Technician</span></span>   
    - <span data-ttu-id="125de-180">Utilizador Fullname = "Jaime Reding" como Expedidor de Customer Service & Field Service</span><span class="sxs-lookup"><span data-stu-id="125de-180">User Fullname="Jamie Reding" as Customer Service & Field Service Dispatcher</span></span>   
    - <span data-ttu-id="125de-181">Utilizador Fullname = "Molly Clark" como Gestor de Contas</span><span class="sxs-lookup"><span data-stu-id="125de-181">User Fullname="Molly Clark" as Account Manager</span></span>   
    - <span data-ttu-id="125de-182">Utilizador Fullname = "Spencer Low" como Gestor de Práticas e de Projeto</span><span class="sxs-lookup"><span data-stu-id="125de-182">User Fullname="Spencer Low" as Practice and Project Manager</span></span>  
    - <span data-ttu-id="125de-183">Utilizador Fullname = "Veronica Quek" como Membro da Equipa</span><span class="sxs-lookup"><span data-stu-id="125de-183">User Fullname="Veronica Quek" as Team Member</span></span>   
    - <span data-ttu-id="125de-184">Nome completo do utilizador="William Contoso"</span><span class="sxs-lookup"><span data-stu-id="125de-184">User Fullname="William Contoso"</span></span>
  
2. <span data-ttu-id="125de-185">Para fins de importação de dados de demonstração, atribua os seis utilizadores acima da função de Administrador para que os registos de exemplo sejam importados corretamente.</span><span class="sxs-lookup"><span data-stu-id="125de-185">For the purposes of demo data import, assign the six users above the Administrator role so sample records import correctly.</span></span> 

3. <span data-ttu-id="125de-186">Abra **PkgFolder** e, em seguida, localize e abra **ImportUserMapFile.xml**.</span><span class="sxs-lookup"><span data-stu-id="125de-186">Open **PkgFolder** and then find and open **ImportUserMapFile.xml**.</span></span> <span data-ttu-id="125de-187">Atualize os campos **Novos=** para os endereços de e-mail dos utilizadores correspondentes do seu sistema.</span><span class="sxs-lookup"><span data-stu-id="125de-187">Update the **New=** fields to the email addresses of corresponding Users in your system.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="125de-188">![Captura de ecrã do UserMapFile](media/sample-data-7.png)</span><span class="sxs-lookup"><span data-stu-id="125de-188">![Screen shot of UserMapFile](media/sample-data-7.png)</span></span>

4. <span data-ttu-id="125de-189">Se o utilizador de nome completo "Spencer Low" tiver um ID de utilizador diferente de **"spencerl"**, então, necessita de atualizar um ficheiro adicional.</span><span class="sxs-lookup"><span data-stu-id="125de-189">If your "Spencer Low" full name user has a different user ID than **"spencerl"**, then you need to update an additional file.</span></span> <span data-ttu-id="125de-190">Abra **DemoDataPreImportConfig.xml** e localize a etiqueta **userstocreateandconfigure**.</span><span class="sxs-lookup"><span data-stu-id="125de-190">Open **DemoDataPreImportConfig.xml** and find the **userstocreateandconfigure** tag.</span></span> <span data-ttu-id="125de-191">Atualize a etiqueta **\<login\>** com o loginId (sensível às maiúsculas e minúsculas).</span><span class="sxs-lookup"><span data-stu-id="125de-191">Update the **\<login\>** tag with the loginId (case-sensitive).</span></span> 

5. <span data-ttu-id="125de-192">O calendário do primeiro utilizador (na etiqueta **userstocreateandconfigure**) é utilizado para povoar as horas de trabalho para todos os recursos reserváveis na importação de dados de demonstração.</span><span class="sxs-lookup"><span data-stu-id="125de-192">The first user's calendar (in the **userstocreateandconfigure** tag) is used to populate the work hours for all bookable resources on import of demo data.</span></span> <span data-ttu-id="125de-193">Navegue para **Definições** > **Segurança** > **Utilizadores**, localize o utilizador "Spencer Low" e abra a opção "Horas de trabalho".</span><span class="sxs-lookup"><span data-stu-id="125de-193">Navigate to **Settings** > **Security** > **Users**, find your "Spencer Low" user, and open the "Work Hours" option.</span></span> <span data-ttu-id="125de-194">Edite as horas de trabalho existentes, selecionando a opção **Agenda semanal periódica completa do início ao fim**.</span><span class="sxs-lookup"><span data-stu-id="125de-194">Edit the existing work hours, selecting the **Entire recurring weekly schedule from start to end** option.</span></span> <span data-ttu-id="125de-195">Verifique se as **Horas de trabalho estão definidas das 8:00 às 17:00 (9 horas), de segunda a sexta-feira e com o fuso horário definido como Hora do Pacífico (E.U.A. e Canadá)**.</span><span class="sxs-lookup"><span data-stu-id="125de-195">Ensure the **Work hours are set to 8 AM - 5 PM (9 Hours), Monday to Friday and with the Timezone set to Pacific Time (US & Canada)**.</span></span> <span data-ttu-id="125de-196">Isto é necessário para assegurar que o quadro da Agenda e do Projeto mostram conforme esperado.</span><span class="sxs-lookup"><span data-stu-id="125de-196">This is needed to ensure that the Project and Schedule board show as expected.</span></span>

<span data-ttu-id="125de-197">**Recomendação:** considere a criação de uma cópia de segurança da sua organização agora, no caso de necessitar de reverter para o ponto de partida se algo correr mal durante a instalação de dados de exemplo.</span><span class="sxs-lookup"><span data-stu-id="125de-197">**Recommendation:** Consider creating a backup of your org now, in case you need to revert to your starting point if something goes wrong during the sample data installation.</span></span> <span data-ttu-id="125de-198">Para mais informações, consulte [Fazer cópias de segurança e restaurar instâncias](/dynamics365/customer-engagement/admin/backup-restore-instances).</span><span class="sxs-lookup"><span data-stu-id="125de-198">For more information, see [Backup and restore instances](/dynamics365/customer-engagement/admin/backup-restore-instances).</span></span>

## <a name="run-the-package-deployer"></a><span data-ttu-id="125de-199">Executar o Package Deployer</span><span class="sxs-lookup"><span data-stu-id="125de-199">Run the Package Deployer</span></span>

1. <span data-ttu-id="125de-200">Localize e execute **PackageDeployer.exe** na pasta **v902FPSMasterData** OU **PackageDeployer_FPSDemoData**.</span><span class="sxs-lookup"><span data-stu-id="125de-200">Find and run **PackageDeployer.exe** in the **v902FPSMasterData** OR **PackageDeployer_FPSDemoData** folder.</span></span>

2. <span data-ttu-id="125de-201">Aceite os termos e condições.</span><span class="sxs-lookup"><span data-stu-id="125de-201">Accept the terms and conditions.</span></span>

3. <span data-ttu-id="125de-202">Na janela seguinte:</span><span class="sxs-lookup"><span data-stu-id="125de-202">On the next window:</span></span>

   <span data-ttu-id="125de-203">a.</span><span class="sxs-lookup"><span data-stu-id="125de-203">a.</span></span> <span data-ttu-id="125de-204">Selecione o tipo de implementação **Office 365**.</span><span class="sxs-lookup"><span data-stu-id="125de-204">Select deployment type **Office 365**.</span></span>

   <span data-ttu-id="125de-205">b.</span><span class="sxs-lookup"><span data-stu-id="125de-205">b.</span></span> <span data-ttu-id="125de-206">Utilize o utilizador e palavra-passe do utilizador de administrador de sistema configurado em "Criar ou configurar utilizadores" ("Spencer Low" com o nome de utilizador "spencerl").</span><span class="sxs-lookup"><span data-stu-id="125de-206">Use the user and password of the system administrator user configured in "Create or configure users" ("Spencer Low" with "spencerl" username).</span></span>

   <span data-ttu-id="125de-207">c.</span><span class="sxs-lookup"><span data-stu-id="125de-207">c.</span></span> <span data-ttu-id="125de-208">Certifique-se de que **Apresentar lista de organizações disponíveis** está selecionado.</span><span class="sxs-lookup"><span data-stu-id="125de-208">Make sure **Display list of available organizations** is selected.</span></span>

      > [!div class="mx-imgBorder"]
      > <span data-ttu-id="125de-209">![Captura de ecrã da janela do Package Deployer com "Apresentar lista de organizações disponíveis" selecionado](media/sample-data-2.png)</span><span class="sxs-lookup"><span data-stu-id="125de-209">![Screenshot of Package Deployer window with "Display list of available organizations" selected](media/sample-data-2.png)</span></span>

4. <span data-ttu-id="125de-210">Selecione a organização onde pretende instalar os dados de exemplo.</span><span class="sxs-lookup"><span data-stu-id="125de-210">Select the organization where you want to install the sample data.</span></span>

5. <span data-ttu-id="125de-211">Selecione **Seguinte** até ver a caixa de diálogo **Configuração de dados de demonstração**.</span><span class="sxs-lookup"><span data-stu-id="125de-211">Select **Next** until you see the **Demo Data Setup** dialog.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="125de-212">![Captura de ecrã da janela do estado do programa de instalação de dados de demonstração](media/sample-data-3.png)</span><span class="sxs-lookup"><span data-stu-id="125de-212">![Screenshot of the demo data installer status window](media/sample-data-3.png)</span></span>

6. <span data-ttu-id="125de-213">Antes de continuar, tenha em atenção que a instalação de dados de exemplo poderá demorar até uma hora (normalmente cerca de 10 minutos).</span><span class="sxs-lookup"><span data-stu-id="125de-213">Before proceeding, note that installing sample data could take up to one hour (normally ~10 minutes).</span></span> <span data-ttu-id="125de-214">Terá de certificar-se de que o computador permanece ligado a uma rede ao longo do processo de instalação e a sessão permanece ativa.</span><span class="sxs-lookup"><span data-stu-id="125de-214">You'll need to make sure the computer remains on and connected to a network throughout the installation process, and that your session remains active.</span></span>   

7. <span data-ttu-id="125de-215">Quando estiver pronto, clique em **Seguinte** para iniciar o processo de instalação de dados de exemplo.</span><span class="sxs-lookup"><span data-stu-id="125de-215">When you're ready, click **Next** to start the sample data installation process.</span></span> <span data-ttu-id="125de-216">Depois de carregar os dados de exemplo, clique em **Concluir**.</span><span class="sxs-lookup"><span data-stu-id="125de-216">After the sample data is loaded, click **Finish**.</span></span>

## <a name="verify-the-sample-data-installation"></a><span data-ttu-id="125de-217">Verificar a instalação dos dados de exemplo</span><span class="sxs-lookup"><span data-stu-id="125de-217">Verify the sample data installation</span></span>

<span data-ttu-id="125de-218">Para uma verificação completa, verifique se o número de registos e tipos de entidades listados no cenário fictício Fabrikam Robotics aparecem conforme esperado.</span><span class="sxs-lookup"><span data-stu-id="125de-218">For a sanity check, verify that the number of records and types of entities listed in Fabrikam Robotics fictitious scenario appear as expected.</span></span>

<span data-ttu-id="125de-219">Depois de carregar os dados de exemplo totalmente, inicie sessão como utilizador Spencer Low e confirme:</span><span class="sxs-lookup"><span data-stu-id="125de-219">After the sample data completely loads, sign in as the Spencer Low user and confirm the following:</span></span>

- <span data-ttu-id="125de-220">Se a aplicação Project Service está instalada, vá a **Project Service** > **Definições** > **Listas de preços**.</span><span class="sxs-lookup"><span data-stu-id="125de-220">If the Project Service application is installed, go to **Project Service** > **Settings** > **Price Lists**.</span></span> <span data-ttu-id="125de-221">Confirme se as taxas de faturação e taxas de custos existem com a moeda adequada para cada país/região no conjunto de dados.</span><span class="sxs-lookup"><span data-stu-id="125de-221">Confirm that bill rates and costs rates exist with the appropriate currency for each country/region in the data set.</span></span>

- <span data-ttu-id="125de-222">Se a aplicação Project Service está instalada, vá para **Universal Resource Scheduling** > **Definições** > **Unidades Organizacionais**.</span><span class="sxs-lookup"><span data-stu-id="125de-222">If the Project Service application is installed, go to **Universal Resource Scheduling** > **Settings** > **Organizational Units**.</span></span> <span data-ttu-id="125de-223">Confirme se uma lista de preços de custos com a moeda apropriada foi associada a cada unidade organizacional (excluindo entradas de localidade).</span><span class="sxs-lookup"><span data-stu-id="125de-223">Confirm that a cost price list with the appropriate currency has been associated with each org unit (excluding city entries).</span></span> <span data-ttu-id="125de-224">Se faltar algum, localize e associe a lista de preços de custos correta.</span><span class="sxs-lookup"><span data-stu-id="125de-224">If any are missing, find and associate the correct cost price list.</span></span>

- <span data-ttu-id="125de-225">Se a aplicação Field Service está instalada, vá a **Project Service** > **Definições** > **Listas de preços**.</span><span class="sxs-lookup"><span data-stu-id="125de-225">If the Field Service application is installed, go to **Project Service** > **Settings** > **Price Lists**.</span></span> <span data-ttu-id="125de-226">Confirme se existem taxas de custos e taxas de faturação.</span><span class="sxs-lookup"><span data-stu-id="125de-226">Confirm that bill rates and costs rates exist.</span></span> <span data-ttu-id="125de-227">Aceda a **Field Service** > **Definições** > **Listas de preços** e verifique se existem taxas de faturação e taxas de custos, com a moeda adequada, para cada país/região no conjunto de dados.</span><span class="sxs-lookup"><span data-stu-id="125de-227">Go to **Field Service** > **Settings** > **Price Lists** and check that bill rates and costs rates exist, with the appropriate currency, for each country/region in the data set.</span></span>

  > [!div class="mx-imgBorder"]
  > <span data-ttu-id="125de-228">![Captura de ecrã de listas de preços ativas](media/sample-data-4.png)</span><span class="sxs-lookup"><span data-stu-id="125de-228">![Screenshot of active price lists](media/sample-data-4.png)</span></span>

  > [!div class="mx-imgBorder"]
  > <span data-ttu-id="125de-229">![Captura de ecrã de unidades organizacionais ativas](media/sample-data-5.png)</span><span class="sxs-lookup"><span data-stu-id="125de-229">![Screenshot of active organizational units](media/sample-data-5.png)</span></span>

## <a name="technical-notes"></a><span data-ttu-id="125de-230">Notas técnicas</span><span class="sxs-lookup"><span data-stu-id="125de-230">Technical notes</span></span>

<span data-ttu-id="125de-231">Consulte abaixo para obter mais detalhes técnicos sobre a instalação destes dados.</span><span class="sxs-lookup"><span data-stu-id="125de-231">See below for more technical details on the installation of this data.</span></span>

### <a name="installing-sample-data-on-top-of-existing-data-not-recommended"></a><span data-ttu-id="125de-232">Instalar dados de exemplo sobre os dados existentes (não recomendado)</span><span class="sxs-lookup"><span data-stu-id="125de-232">Installing sample data on top of existing data (not recommended)</span></span>

<span data-ttu-id="125de-233">Se necessitar de instalar dados de exemplo sobre uma versão de avaliação ou ambiente de demonstração existente do Field Service ou Project Service que já contém dados, terá de suspender as pré-verificações de segurança efetuadas pelo programa de instalação.</span><span class="sxs-lookup"><span data-stu-id="125de-233">If you need to install sample data on top of an existing Field Service or Project Service trial or demo environment that already has data, you'll need to suspend the safety prechecks performed by the installer.</span></span>

<span data-ttu-id="125de-234">Para tal, vá à pasta **PkgFolder** para localizar e abrir o ficheiro **DemoDataPreImportConfig.xml** com o Bloco de Notas (ou outro editor de XML).</span><span class="sxs-lookup"><span data-stu-id="125de-234">To do this, go to the **PkgFolder** folder to find and open the **DemoDataPreImportConfig.xml** file with Notepad (or another XML editor).</span></span>

<span data-ttu-id="125de-235">Localize o valor seguinte e, em seguida, altere a definição de verdadeiro para falso:</span><span class="sxs-lookup"><span data-stu-id="125de-235">Find the following value, and then change the setting from true to false:</span></span>

```alias
<TerminateOnPreCheckFailure>true</TerminateOnPreCheckFailure>
```

<span data-ttu-id="125de-236">Esta alteração faz com que o programa de instalação ignore algumas verificações importantes de segurança, incluindo:</span><span class="sxs-lookup"><span data-stu-id="125de-236">This change causes the installer to bypass some important safety checks, including:</span></span>

- <span data-ttu-id="125de-237">Confirmar de que não existe mais do que um registo ativo **Unidade organizacional** e, em seguida, mudar o nome para **Fabrikam US**.</span><span class="sxs-lookup"><span data-stu-id="125de-237">Confirming that there is no more than one active **Organizational Unit** record, and then renaming it to **Fabrikam US**.</span></span>

- <span data-ttu-id="125de-238">Confirmar de que não existe mais do que um registo ativo **Modelo de trabalho**.</span><span class="sxs-lookup"><span data-stu-id="125de-238">Confirming that there is no more than one active **Work Template** record.</span></span>

- <span data-ttu-id="125de-239">Confirmar de que não existe mais do que um registo ativo **Parâmetro do Projeto** e, em seguida, mudar o nome dessa entrada para **Parâmetros**.</span><span class="sxs-lookup"><span data-stu-id="125de-239">Confirming that there is no more than one active **Project Parameter** record, and then renaming that entry to **Parameters**.</span></span>

### <a name="configuration-components"></a><span data-ttu-id="125de-240">Componentes de configuração</span><span class="sxs-lookup"><span data-stu-id="125de-240">Configuration components</span></span>

<span data-ttu-id="125de-241">Existem outros componentes de configuração neste ficheiro de configuração de pré-importação.</span><span class="sxs-lookup"><span data-stu-id="125de-241">There are a number of other configuration components in this pre-import configuration file.</span></span> <span data-ttu-id="125de-242">Para utilizadores técnicos, alguns incluem:</span><span class="sxs-lookup"><span data-stu-id="125de-242">For technical users, some of these include:</span></span>

- <span data-ttu-id="125de-243">**\<RequiredSolutions\>** especifica as instalações de soluções pré-requisito e os números de versão.</span><span class="sxs-lookup"><span data-stu-id="125de-243">**\<RequiredSolutions\>** specifies prerequisite solution installations and their version numbers.</span></span>

- <span data-ttu-id="125de-244">**\<InstallSampleData\>** controla se os dados de exemplo fornecidos com o programa para as aplicações estão instalados.</span><span class="sxs-lookup"><span data-stu-id="125de-244">**\<InstallSampleData\>** controls whether out-of-the-box sample data for the apps is installed.</span></span>

    - <span data-ttu-id="125de-245">falso - ignora a instalação destes dados incorporadas (que são removidos)</span><span class="sxs-lookup"><span data-stu-id="125de-245">false - skips installation of this built-in data (which is removable)</span></span>

    - <span data-ttu-id="125de-246">verdadeiro - instala os dados incorporados em simultâneo com a instalação dos dados de exemplo FS e PSA</span><span class="sxs-lookup"><span data-stu-id="125de-246">true - installs the built-in data concurrent with installation of the FS and PSA sample data</span></span>

- <span data-ttu-id="125de-247">**\<PreImportDataCollection\>** especifica os Mapas de Dados de ficheiro simples e registos associados para serem importados antes da instalação de dados de exemplo principal.</span><span class="sxs-lookup"><span data-stu-id="125de-247">**\<PreImportDataCollection\>** specifies flat-file Data Maps and associated Records to be imported ahead of the main sample data installation.</span></span>

- <span data-ttu-id="125de-248">**\<EntitiesToEnableScheduling\>** especifica as entidades que devem ser ativadas para Reserva no Microsoft Dynamics Scheduling (também conhecido como Universal Resource Scheduling).</span><span class="sxs-lookup"><span data-stu-id="125de-248">**\<EntitiesToEnableScheduling\>** specifies which entities should be enabled for Booking in Microsoft Dynamics Scheduling (aka Universal Resource Scheduling).</span></span>

- <span data-ttu-id="125de-249">**\<UsersToCreateAndConfigure\>** especifica os Recursos reserváveis que serão criados (se não existirem já) antes da importação de dados de exemplo ser executada.</span><span class="sxs-lookup"><span data-stu-id="125de-249">**\<UsersToCreateAndConfigure\>** specifies Bookable Resources that will be created (if they don't exist already) before the sample data import executes.</span></span> <span data-ttu-id="125de-250">Note que os Recursos reserváveis dos dados de exemplo do sistema de origem correspondem aos registos de Recursos reserváveis do sistema de destino no FullName e início de sessão de cada recurso.</span><span class="sxs-lookup"><span data-stu-id="125de-250">Note that the source system sample data Bookable Resource match with the target system Bookable Resource records on the FullName and login of each resource.</span></span> <span data-ttu-id="125de-251">Por conseguinte, NÃO é possível alterar os nomes existentes neste ficheiro de pré-configuração, a menos que importe primeiro dados de exemplo para um sistema de destino utilizando estes nomes, depois mudar o nome dos Recursos reserváveis para o nome pretendido de acordo com os registos de utilizador ativados e, em seguida, exportar os dados novamente para importar para o sistema de destino final (atualizar as entradas Antigas e Novas de **ImportUserMapFile.xml** em conformidade).</span><span class="sxs-lookup"><span data-stu-id="125de-251">Therefore, it is NOT possible to change the names in this preconfiguration file unless you first import sample data into a target system using these names, then rename the Bookable Resources to your desired name set along with the Enabled User records, and then export the data again for import into your final destination system (updating the **ImportUserMapFile.xml** Old and New entries accordingly).</span></span>

- <span data-ttu-id="125de-252">**\<PluginsToDisable\>** especifica plug-ins itens muito discretos que devem ser desativados durante a importação de dados de exemplo e, em seguida, reativados posteriormente.</span><span class="sxs-lookup"><span data-stu-id="125de-252">**\<PluginsToDisable\>** specifies very discrete line-item plug-ins that must be disabled during the sample data import and then reenabled afterwards.</span></span>

### <a name="fabrikam-robotics-fictitious-scenario"></a><span data-ttu-id="125de-253">Cenário fictício Fabrikam Robotics</span><span class="sxs-lookup"><span data-stu-id="125de-253">Fabrikam Robotics fictitious scenario</span></span>

<span data-ttu-id="125de-254">Os pacotes de dados de referência de exemplo de Field Service e Project Service instalam a solução **Fabrikam Manufacturing Master Data (v3.0.0.0)**, juntamente com aproximadamente 4000 registos e aproximadamente 40 entidades diferentes.</span><span class="sxs-lookup"><span data-stu-id="125de-254">The Field Service and Project Service sample reference data packages install the **Fabrikam Manufacturing Master Data (v3.0.0.0) solution**, along with approximately 4,000 records and approximately 40 different entities.</span></span> <span data-ttu-id="125de-255">Os pacotes de dados de exemplo separados para Field Service ou Project Service contêm um subconjunto dos dados de exemplo **v902FPSMasterData** para essa aplicação.</span><span class="sxs-lookup"><span data-stu-id="125de-255">The separate sample data packages for Field Service or Project Service contain a subset of the **v902FPSMasterData** sample data for that application.</span></span> <span data-ttu-id="125de-256">O pacote **Dados de demonstração** instala a **solução de dados de demonstração da Fabrikam Manufacturing (v3.0.0.7)** com aproximadamente 22.000 registos de 148 entidades.</span><span class="sxs-lookup"><span data-stu-id="125de-256">The **Demo Data** package installs the **Fabrikam Manufacturing Demo Data (v3.0.0.7) solution** with approximately 22,000 records across 148 entities.</span></span>

<span data-ttu-id="125de-257">A empresa fictícia, Fabrikam Robotics, é um fabricante de robôs de linha de montagem de dispositivos electrónicos e é conhecido pela qualidade de produtos, inovação e sólido suporte ao cliente, incluindo planeamento de instalação, implementação e serviços de manutenção contínuos.</span><span class="sxs-lookup"><span data-stu-id="125de-257">The fictional company, Fabrikam Robotics, is a manufacturer of electronic device assembly line robots and is known for their product quality, innovation, and solid customer service, including installation planning, implementation, and ongoing maintenance services.</span></span> <span data-ttu-id="125de-258">A Fabrikam tem sede nos Estados Unidos (Fabrikam US) e operações de serviços com base em projetos em França, Índia, Reino Unido e Suíça.</span><span class="sxs-lookup"><span data-stu-id="125de-258">Fabrikam is headquartered in the United States (Fabrikam US), and has project-based service operations in France, India, the United Kingdom, and Switzerland.</span></span>

<span data-ttu-id="125de-259">As operações de serviço no terreno estão centralizadas nos Estados Unidos, sobretudo, na zona de Seattle.</span><span class="sxs-lookup"><span data-stu-id="125de-259">Field service operations are centered in the United States, mostly in the greater Seattle area.</span></span> <span data-ttu-id="125de-260">A empresa concentra-se na utilização da conectividade da Internet das coisas (IoT) para monitorizar o desempenho ativo do cliente e fornecer serviços mais proativos no local.</span><span class="sxs-lookup"><span data-stu-id="125de-260">The company is focused on leveraging Internet of Things (IoT) connectivity to monitor customer asset performance and deliver increasingly proactive onsite services.</span></span>

<span data-ttu-id="125de-261">Uma descrição geral de alto nível dos dados de exemplo é:</span><span class="sxs-lookup"><span data-stu-id="125de-261">A high-level overview of the sample data is as follows:</span></span>

- <span data-ttu-id="125de-262">Elementos de dados de exemplo comuns (incluídos para ambas as aplicações)</span><span class="sxs-lookup"><span data-stu-id="125de-262">Common sample data elements (included for both applications)</span></span>

    - <span data-ttu-id="125de-263">1 utilizador</span><span class="sxs-lookup"><span data-stu-id="125de-263">1 user</span></span>

    - <span data-ttu-id="125de-264">71 contas</span><span class="sxs-lookup"><span data-stu-id="125de-264">71 accounts</span></span>

    - <span data-ttu-id="125de-265">137 contactos</span><span class="sxs-lookup"><span data-stu-id="125de-265">137 contacts</span></span>

    - <span data-ttu-id="125de-266">Vários tipos e categorias de transação</span><span class="sxs-lookup"><span data-stu-id="125de-266">Various transaction types and categories</span></span>

    - <span data-ttu-id="125de-267">50 produtos com a lista de preços de 1 produto</span><span class="sxs-lookup"><span data-stu-id="125de-267">50 products with 1 product price list</span></span>

    - <span data-ttu-id="125de-268">14 listas de preço/custo</span><span class="sxs-lookup"><span data-stu-id="125de-268">14 price/cost lists</span></span>

    - <span data-ttu-id="125de-269">31 características (competências de recurso) em 2 modelos de classificação com 3 níveis (valores de classificação)</span><span class="sxs-lookup"><span data-stu-id="125de-269">31 characteristics (resource skills) in 2 rating models with 3 levels (rating values)</span></span>

- <span data-ttu-id="125de-270">Project Service</span><span class="sxs-lookup"><span data-stu-id="125de-270">Project Service</span></span>

    - <span data-ttu-id="125de-271">8 unidades organizacionais</span><span class="sxs-lookup"><span data-stu-id="125de-271">8 organizational units</span></span>

    - <span data-ttu-id="125de-272">6 níveis de utilização específicas da função</span><span class="sxs-lookup"><span data-stu-id="125de-272">6 role-specific utilization levels</span></span>

    - <span data-ttu-id="125de-273">2.8 k + especificações de preços de função</span><span class="sxs-lookup"><span data-stu-id="125de-273">2.8k+ role-price specifications</span></span>

- <span data-ttu-id="125de-274">Field Service</span><span class="sxs-lookup"><span data-stu-id="125de-274">Field Service</span></span>

    - <span data-ttu-id="125de-275">4 territórios</span><span class="sxs-lookup"><span data-stu-id="125de-275">4 territories</span></span>

    - <span data-ttu-id="125de-276">5 tipos de ordem de intervenção</span><span class="sxs-lookup"><span data-stu-id="125de-276">5 work order types</span></span>

    - <span data-ttu-id="125de-277">22 ativos de cliente</span><span class="sxs-lookup"><span data-stu-id="125de-277">22 customer assets</span></span>

    - <span data-ttu-id="125de-278">9 tipos de incidente com uma variedade de características de recursos associadas (9), serviços (13) e tarefas de serviço (13)</span><span class="sxs-lookup"><span data-stu-id="125de-278">9 incident types with a range of associated resource characteristics (9), services (13) and service tasks (13)</span></span>
   
<span data-ttu-id="125de-279">O pacote **Dados de demonstração** instala aproximadamente 179 ordens de intervenção, 12 projetos e dados das transações associados.</span><span class="sxs-lookup"><span data-stu-id="125de-279">The **Demo Data** package installs approximately 179 work orders, 12 projects, and associated transactional data.</span></span> 

### <a name="change-the-work-hours-for-sample-resources"></a><span data-ttu-id="125de-280">Alterar as horas de trabalho para recursos de exemplo</span><span class="sxs-lookup"><span data-stu-id="125de-280">Change the work hours for sample resources</span></span>

<span data-ttu-id="125de-281">Por predefinição, todos os recursos reserváveis têm um calendário de 24 horas de trabalho.</span><span class="sxs-lookup"><span data-stu-id="125de-281">By default, all bookable resources have a 24 work hours calendar.</span></span>

<span data-ttu-id="125de-282">Se precisar de alterar as horas de trabalho por recursos reserváveis de exemplo, vá para **Universal Resource Scheduling** > **Agendamento** > **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="125de-282">If you need to change the work hours for sample bookable resources, go to **Universal Resource Scheduling** > **Scheduling** > **Resources**.</span></span>

<span data-ttu-id="125de-283">Selecione um utilizador (por exemplo, Spencer Low) e altere as horas de trabalho do Spencer para as horas de trabalho que pretende aplicar a vários utilizadores.</span><span class="sxs-lookup"><span data-stu-id="125de-283">Select a user (for example, Spencer Low) and change Spencer's work hours to the hours you want to apply to multiple users.</span></span> <span data-ttu-id="125de-284">Aceda a **Universal Resource Scheduling** > **Definições** > **Modelos de Horas de Trabalho** e edite o registo **Modelo de Trabalho Predefinido**.</span><span class="sxs-lookup"><span data-stu-id="125de-284">Go to **Universal Resource Scheduling** > **Settings** > **Work Hour Templates** and edit the **Default Work Template** record.</span></span> <span data-ttu-id="125de-285">No campo **Recurso do Modelo**, selecione um utilizador com horas de trabalho que pretende aplicar para outros recursos.</span><span class="sxs-lookup"><span data-stu-id="125de-285">In the **Template Resource** field, select a user with work hours that you want to apply to other resources.</span></span> <span data-ttu-id="125de-286">Aceda a **Universal Resource Scheduling** > **Agendamento** > **Recursos** > **Recursos Reserváveis Ativos**.</span><span class="sxs-lookup"><span data-stu-id="125de-286">Go to **Universal Resource Scheduling** > **Scheduling** > **Resources** > **Active Bookable Resources**.</span></span> <span data-ttu-id="125de-287">Selecione os recursos que pretende alterar e, em seguida, selecione **Definir calendário**.</span><span class="sxs-lookup"><span data-stu-id="125de-287">Select the resources you want to change, and then select **Set Calendar**.</span></span> <span data-ttu-id="125de-288">Na lista pendente **Modelo de trabalho**, selecione o modelo **Horas de trabalho predefinidas** ou outro modelo com o recurso correcto de modelos.</span><span class="sxs-lookup"><span data-stu-id="125de-288">On the **Work Template** drop-down list, select the **Default Work Hour** template or another template with the correct templating resource.</span></span> <span data-ttu-id="125de-289">Quando vai ao quadro da agenda, deverá ver que os recursos agora atualizaram as horas de trabalho.</span><span class="sxs-lookup"><span data-stu-id="125de-289">When you go to the schedule board, you should see that the resources now have updated work hours.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="125de-290">![Captura de ecrã de recursos reserváveis ativos](media/sample-data-6.png)</span><span class="sxs-lookup"><span data-stu-id="125de-290">![Screenshot of active bookable resources](media/sample-data-6.png)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]