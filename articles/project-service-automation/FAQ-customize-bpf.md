---
title: Como posso personalizar o fluxo do processo do Project Stages?
description: Uma descrição geral para personalizar o fluxo do processo de negócio das Fases do Projeto.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 10/11/2018
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 3.x
author: JohnPBurrows
ms.assetid: 36f7df9e-117d-4f85-af4b-d842e93321bd
ms.author: john.burrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: d4b99f67e929ebcd1a684bcd1124756140107d17
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754491"
---
# <a name="how-do-i-customize-the-project-stages-business-process-flow"></a><span data-ttu-id="c6098-103">Como posso personalizar o fluxo do processo do Project Stages?</span><span class="sxs-lookup"><span data-stu-id="c6098-103">How do I customize the Project Stages business process flow?</span></span>
[!INCLUDE[cc-applies-to-psa-app-2-4x-9-0-platform](../includes/cc-applies-to-psa-app-2-4x-9-0-platform.md)]
[!INCLUDE[cc-applies-to-psa-app-1x-8-2-platform](../includes/cc-applies-to-psa-app-1x-8-2-platform.md)]

<span data-ttu-id="c6098-104">Não existe uma limitação conhecida em versões anteriores da aplicação Project Service em que os nomes das fases no fluxo do processo de negócio no Project Stages devem corresponder exatamente aos nomes de inglês esperados (**Quote**, **Plan**, **Close**).</span><span class="sxs-lookup"><span data-stu-id="c6098-104">There's a known limitation in earlier versions of the Project Service application that the names of the stages in the Project Stages business process flow must exactly match the expected English names (**Quote**, **Plan**, **Close**).</span></span> <span data-ttu-id="c6098-105">Caso contrário, a lógica de negócio, que utiliza os nomes de fase em inglês, não funciona conforme esperado.</span><span class="sxs-lookup"><span data-stu-id="c6098-105">Otherwise, the business logic, which relies on the English stage names, doesn't work as expected.</span></span> <span data-ttu-id="c6098-106">É por essa razão que não vê ações familiares tal como **Alternar Processo** ou **Editar Processo** disponíveis no formulário de projeto e personalizar o fluxo do processo de negócio não é recomendável.</span><span class="sxs-lookup"><span data-stu-id="c6098-106">That's why you don't see familiar actions such as **Switch Process** or **Edit Process** available on the project form, and customizing the business process flow isn't encouraged.</span></span> 

<span data-ttu-id="c6098-107">Esta limitação foi resolvida na versão 2.4.5.48 e posterior.</span><span class="sxs-lookup"><span data-stu-id="c6098-107">This limitation has been addressed in version 2.4.5.48 and later.</span></span> <span data-ttu-id="c6098-108">Se necessitar de personalizar o fluxo do processo de negócio predefinido em versões anteriores, este artigo fornece soluções sugeridas.</span><span class="sxs-lookup"><span data-stu-id="c6098-108">This article provides suggested workarounds if you need to customize the default business process flow for earlier versions.</span></span>  

## <a name="business-logic-requires-an-exact-match-with-english-stage-names"></a><span data-ttu-id="c6098-109">A lógica de negócio requer uma correspondência exata com nomes de fase em inglês</span><span class="sxs-lookup"><span data-stu-id="c6098-109">Business logic requires an exact match with English stage names</span></span>

<span data-ttu-id="c6098-110">O fluxo do processo de negócio do Project Stages inclui lógica de negócio que aciona os seguintes comportamentos na aplicação:</span><span class="sxs-lookup"><span data-stu-id="c6098-110">The Project Stages business process flow includes business logic that drives the following behaviors in the app:</span></span>
- <span data-ttu-id="c6098-111">Quando o projeto está associado a uma proposta, o código define fluxo do processo de negócio para a fase **Quote**.</span><span class="sxs-lookup"><span data-stu-id="c6098-111">When the project is associated with a quote, the code sets the business process flow to the **Quote** stage.</span></span>
- <span data-ttu-id="c6098-112">Quando o projeto está associado a um contrato, o código define fluxo do processo de negócio para a fase **Plan**.</span><span class="sxs-lookup"><span data-stu-id="c6098-112">When the project is associated with a contract, the code sets the business process flow to the **Plan** stage.</span></span>
- <span data-ttu-id="c6098-113">Quando o fluxo do processo de negócio é avançado para a fase **Close**, o registo de projeto é desativado.</span><span class="sxs-lookup"><span data-stu-id="c6098-113">When the business process flow is advanced to the **Close** stage, the project record is deactivated.</span></span> <span data-ttu-id="c6098-114">Quando do projeto é desativado, o formulário de projeto e a estrutura hierárquica do trabalho (WBS) são definidos como só de leitura, as reservas de recurso nomeadas são libertadas e quaisquer listas de preços associadas são desativadas.</span><span class="sxs-lookup"><span data-stu-id="c6098-114">When the project is deactivated, the project form and work breakdown structure (WBS) are set to read-only, the named resource bookings are released, and any associated price lists are deactivated.</span></span>

<span data-ttu-id="c6098-115">Esta lógica de negócio utiliza os nomes em inglês para as fases de projeto.</span><span class="sxs-lookup"><span data-stu-id="c6098-115">This business logic relies on the English names for the project stages.</span></span> <span data-ttu-id="c6098-116">Este dependência nos nomes de fase em inglês é o principal motivo por que a personalização do fluxo do processo de negócio do Project Stages não é encorajada, assim como, o motivo porque não visualiza as ações comuns do fluxo do processo de negócio como **Alternar Proces** ou **Editar Processo** na entidade do projeto.</span><span class="sxs-lookup"><span data-stu-id="c6098-116">This dependency on the English stage names is the main reason why customization of the Project Stages business process flow isn't encouraged, as well as why you don’t see the common business process flow actions like **Switch Process** or **Edit Process** on the project entity.</span></span>

## <a name="what-happens-if-the-stage-names-dont-match-the-english-names"></a><span data-ttu-id="c6098-117">O que acontece se os nomes de fase não corresponderem aos nomes em inglês?</span><span class="sxs-lookup"><span data-stu-id="c6098-117">What happens if the stage names don't match the English names?</span></span>

<span data-ttu-id="c6098-118">Na versão 1.x da aplicação Project Service na plataforma 8.2, quando os nomes de fase do processo de negócio não correspondem exatamente aos das fases em inglês, a lógica de negócio que define a fase adequada para propostas ou contratos, ou que fecha do projeto, é ignorada.</span><span class="sxs-lookup"><span data-stu-id="c6098-118">In the Project Service app version 1.x on the 8.2 platform, when the stage names in the business process flow don’t match the English stage names exactly, the business logic that sets the right stage for quotes or contracts, or that closes the project, is skipped.</span></span> <span data-ttu-id="c6098-119">Nenhuma mensagem de erro é apresentada.</span><span class="sxs-lookup"><span data-stu-id="c6098-119">No error messages are displayed.</span></span> <span data-ttu-id="c6098-120">Por conseguinte, parece que pode personalizar o fluxo do processo de negócio do Project Stages.</span><span class="sxs-lookup"><span data-stu-id="c6098-120">Therefore it appears that you are able to customize the Project Stages business process flow.</span></span> <span data-ttu-id="c6098-121">No entanto, não verá qualquer um dos processos automáticos a trabalhar para cotações, contratos e fecho do projeto.</span><span class="sxs-lookup"><span data-stu-id="c6098-121">However, you won’t see any of the automatic processes working for quotes, contracts, and project close.</span></span>

<span data-ttu-id="c6098-122">Na versão 2.4.4.30 da aplicação Project Service ou anterior na plataforma 9.0, ocorreu uma alteração significativa na arquitetura dos fluxos de processo de negócio, que necessitou de uma nova programação da lógica de negócio do fluxo de processo de negócio.</span><span class="sxs-lookup"><span data-stu-id="c6098-122">In the Project Service app version 2.4.4.30 or earlier on the 9.0 platform, there was a significant architectural change to business process flows, which required a re-write of the business process flow business logic.</span></span> <span data-ttu-id="c6098-123">Consequentemente, se os nomes de fase do processo não corresponderem aos nomes em inglês esperados, irá receber uma mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="c6098-123">As a result, if the process stage names don’t match the expected English names, you do receive an error message.</span></span> 

<span data-ttu-id="c6098-124">Por conseguinte, se pretender personalizar o fluxo do processo de negócio do Project Stages para a entidade de projeto, só pode adicionar novas fases ao fluxo do processo de negócio predefinido para a entidade de projeto e manter as fases **Quote**, **Plan** e **Fases** tal como estão.</span><span class="sxs-lookup"><span data-stu-id="c6098-124">Therefore, if you want to customize the Project Stages business process flow for the project entity, you can only add brand new stages to the default business process flow for the project entity, while keeping the **Quote**, **Plan**, and **Close** stages as-is.</span></span> <span data-ttu-id="c6098-125">Esta restrição assegura que não tem erros da lógica de negócio que espera os nomes de fase em inglês no fluxo do processo de negócio.</span><span class="sxs-lookup"><span data-stu-id="c6098-125">This restriction ensures that you don’t get errors from the business logic that expects the English stage names in the business process flow.</span></span>

<span data-ttu-id="c6098-126">Na versão 2.4.5.48 ou posterior, a lógica de negócio descrita neste artigo foi removida do fluxo do processo de negócio predefinido para a entidade de projeto.</span><span class="sxs-lookup"><span data-stu-id="c6098-126">In version 2.4.5.48 or later, the business logic described in this article has been removed from the default business process flow for the project entity.</span></span> <span data-ttu-id="c6098-127">Atualizar para essa versão ou posterior permitirá personalizar ou substituir o fluxo do processo de negócio predefinido com um dos seus.</span><span class="sxs-lookup"><span data-stu-id="c6098-127">Upgrading to that version or later will let you customize or replace the default business process flow with one of your own.</span></span> 

## <a name="workarounds-for-earlier-versions"></a><span data-ttu-id="c6098-128">Soluções para as versões anteriores</span><span class="sxs-lookup"><span data-stu-id="c6098-128">Workarounds for earlier versions</span></span>

<span data-ttu-id="c6098-129">Se a atualização não for uma opção, pode personalizar o fluxo do processo de negócio do Project Stages para a entidade de projeto de uma destas duas formas:</span><span class="sxs-lookup"><span data-stu-id="c6098-129">If upgrading isn't an option, you can customize the Project Stages business process flow for the project entity in one of these two ways:</span></span>

1. <span data-ttu-id="c6098-130">Adicionar fases adicionais à configuração predefinida, mantendo os nomes de fase em inglês para **Quote**, **Plan** e **Close**.</span><span class="sxs-lookup"><span data-stu-id="c6098-130">Add additional stages to the default configuration, while retaining the English stage names for **Quote**, **Plan**, and **Close**.</span></span>

   > [!div class="mx-imgBorder"] 
   > <span data-ttu-id="c6098-131">![Captura de ecrã de adição de fases à configuração predefinida](media/FAQ-Customize-BPF-1.png)</span><span class="sxs-lookup"><span data-stu-id="c6098-131">![Screenshot of adding stages to default configuration](media/FAQ-Customize-BPF-1.png)</span></span>
 
2. <span data-ttu-id="c6098-132">Criar o seu próprio fluxo do processo de negócio e torná-lo o fluxo do processo de negócio principal para a entidade de projeto, o que lhe permite ter os nomes de fase que pretender.</span><span class="sxs-lookup"><span data-stu-id="c6098-132">Create your own business process flow and make it the primary business process flow for the project entity, which lets you have any stage names you want.</span></span> <span data-ttu-id="c6098-133">No entanto, se quiser utilizar as mesmas fases de projeto padrão **Quote**, **Plan** e **Close**, necessita de efetuar algumas personalizações que partem dos nomes de fase personalizados.</span><span class="sxs-lookup"><span data-stu-id="c6098-133">However, if you want to use the same standard project stages **Quote**, **Plan**, and **Close**, you need to do some customizations that are driven off your custom stage names.</span></span> <span data-ttu-id="c6098-134">A lógica mais complexa está no encerramento do projeto, o qual ainda poderá acionar bastando desativar o registo de projeto.</span><span class="sxs-lookup"><span data-stu-id="c6098-134">The more complex logic is in the closing of the project, which you can still trigger by just deactivating the project record.</span></span>

   > [!div class="mx-imgBorder"] 
   > <span data-ttu-id="c6098-135">![Captura de ecrã da Personalização BPF](media/FAQ-Customize-BPF-2.png)</span><span class="sxs-lookup"><span data-stu-id="c6098-135">![Screenshot of BPF customization](media/FAQ-Customize-BPF-2.png)</span></span>

### <a name="additional-considerations-for-project-service-app-version-24430-or-earlier-on-platform-90"></a><span data-ttu-id="c6098-136">Considerações adicionais para a versão 2.4.4.30 ou anterior da aplicação Project Service na plataforma 9.0</span><span class="sxs-lookup"><span data-stu-id="c6098-136">Additional considerations for Project Service app version 2.4.4.30 or earlier on platform 9.0</span></span>

<span data-ttu-id="c6098-137">No Project Service 2.4.4.30 ou anterior na plataforma 9.0, com um fluxo do processo de negócio personalizado o campo **Nome de Fase** na entidade de projeto utilizada nas vistas de lista do gráfico e projeto **Projeto por Fase** não atualizam porque está junto ao fluxo do processo de negócio predefinido do Project Stages.</span><span class="sxs-lookup"><span data-stu-id="c6098-137">In Project Service 2.4.4.30 or earlier on platform 9.0, with a custom business process flow the **Stage Name** field on the project entity used in the **Project By Stage** chart and project list views won’t update, because it’s coupled to the default Project Stages business process flow.</span></span> <span data-ttu-id="c6098-138">Isto pode ser abordado com os seguintes passos:</span><span class="sxs-lookup"><span data-stu-id="c6098-138">You can address this issue with the following steps:</span></span>

- <span data-ttu-id="c6098-139">Adicione um campo personalizado para capturar a fase de fluxo de processo de negócio atual que é atualizada à medida que o utilizador avança pelo fluxo do processo de negócio personalizado.</span><span class="sxs-lookup"><span data-stu-id="c6098-139">Add a custom field to capture the current business process flow stage that is updated as the user advances through the custom business process flow.</span></span>

- <span data-ttu-id="c6098-140">Modifique o gráfico **Projeto por Fase** para trabalhar com o campo personalizado em vez da configuração predefinida.</span><span class="sxs-lookup"><span data-stu-id="c6098-140">Modify the **Project By Stage** chart to work with your custom field instead of the default configuration.</span></span>

### <a name="steps-to-create-your-own-business-process-flow-for-the-project-entity"></a><span data-ttu-id="c6098-141">Passos para criar o seu próprio fluxo do processo de negócio para a entidade de projeto</span><span class="sxs-lookup"><span data-stu-id="c6098-141">Steps to create your own business process flow for the project entity</span></span>

<span data-ttu-id="c6098-142">Para criar o seu próprio fluxo do processo de negócio para a entidade de projeto faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c6098-142">To create your own business process flow for the project entity do the following:</span></span>

1. <span data-ttu-id="c6098-143">Aceda a **Definições** > **Centro de Processos**.</span><span class="sxs-lookup"><span data-stu-id="c6098-143">Go to **Settings** > **Process Center**.</span></span> <span data-ttu-id="c6098-144">Não copie o fluxo do processo de negócio do Project Stages visto que também copia a lógica de negócio do Project Service.</span><span class="sxs-lookup"><span data-stu-id="c6098-144">Don’t copy the Project Stages business process flow because that also copies the Project Service business logic.</span></span>

   > [!div class="mx-imgBorder"] 
   > <span data-ttu-id="c6098-145">![Captura de ecrã da Personalização BPF](media/FAQ-Customize-BPF-3.png)</span><span class="sxs-lookup"><span data-stu-id="c6098-145">![Screenshot of BPF customization](media/FAQ-Customize-BPF-3.png)</span></span>

2. <span data-ttu-id="c6098-146">Utilize o Designer de Processo para criar os nomes de fase pretendidos.</span><span class="sxs-lookup"><span data-stu-id="c6098-146">Use the Process Designer to create the stage names you want.</span></span> <span data-ttu-id="c6098-147">Se pretender a mesma funcionalidade das fases predefinidas para **Quote**, **Plan** e **Close**, terá de criar isso com base nos nomes de fase do seu fluxo processo de negócio personalizados.</span><span class="sxs-lookup"><span data-stu-id="c6098-147">If you want the same functionality as the default stages for **Quote**, **Plan**, and **Close**, you’ll have to create that based on your custom business process flow’s stage names.</span></span>

   > [!div class="mx-imgBorder"] 
   > <span data-ttu-id="c6098-148">![Captura de ecrã do Designer de Processo utilizado para personalizar BPF](media/FAQ-Customize-BPF-4.png)</span><span class="sxs-lookup"><span data-stu-id="c6098-148">![Screenshot of Process Designer used to customize BPF](media/FAQ-Customize-BPF-4.png)</span></span> 

3. <span data-ttu-id="c6098-149">No Designer de Processo, clique em **Fluxo do Processo de Encomenda** para tornar o fluxo do processo de negócio personalizadas no principal para a entidade de projeto movendo-o acima do fluxo do processo de negócio do Project Stages para o topo da lista.</span><span class="sxs-lookup"><span data-stu-id="c6098-149">In the Process Designer, click **Order Process Flow** to make the custom business process flow the primary business process flow for the project entity by moving it above the Project Stages business process flow to the top of the list.</span></span>

   > [!div class="mx-imgBorder"] 
   > <span data-ttu-id="c6098-150">![Captura de ecrã de utilização do Fluxo do Processo de Encomenda](media/FAQ-Customize-BPF-5-720.png)</span><span class="sxs-lookup"><span data-stu-id="c6098-150">![Screenshot of using Order Process Flow](media/FAQ-Customize-BPF-5-720.png)</span></span>

### <a name="the-following-steps-apply-to-project-service-app-24430-or-earlier-on-the-90-platform"></a><span data-ttu-id="c6098-151">Os seguintes passos aplicam-se a aplicação Project Service 2.4.4.30 ou anterior na plataforma 9.0</span><span class="sxs-lookup"><span data-stu-id="c6098-151">The following steps apply to Project Service app 2.4.4.30 or earlier on the 9.0 platform</span></span>

4. <span data-ttu-id="c6098-152">Adicione um novo campo personalizado para a entidade de projeto para capturar as fases personalizadas no seu fluxo do processo de negócio personalizado.</span><span class="sxs-lookup"><span data-stu-id="c6098-152">Add a new custom field to the project entity to capture the custom stages in your custom business process flow.</span></span> <span data-ttu-id="c6098-153">Terá de adicionar lógica de negócio (plug-in/fluxo de trabalho) para atualizar este campo quando é atualizada a fase no fluxo do processo de negócio personalizado.</span><span class="sxs-lookup"><span data-stu-id="c6098-153">You’ll need to add business logic (plugin/workflow) to update this field when the stage on the custom business process flow is updated.</span></span>

   > [!div class="mx-imgBorder"] 
   > <span data-ttu-id="c6098-154">![Captura de ecrã de personalização da Entidade de projeto](media/FAQ-Customize-BPF-6-720.png)</span><span class="sxs-lookup"><span data-stu-id="c6098-154">![Screenshot of customizing Project entity](media/FAQ-Customize-BPF-6-720.png)</span></span>

5. <span data-ttu-id="c6098-155">Modifique o gráfico **Projeto por Fase** para utilizar o novo campo personalizado para fases.</span><span class="sxs-lookup"><span data-stu-id="c6098-155">Modify the **Project By Stage** chart to use your new custom field for stages.</span></span>

   > [!div class="mx-imgBorder"] 
   > <span data-ttu-id="c6098-156">![Captura de ecrã de utilização do gráfico Projeto por Fase](media/FAQ-Customize-BPF-7-720.png)</span><span class="sxs-lookup"><span data-stu-id="c6098-156">![Screenshot of using the Project By Stage chart](media/FAQ-Customize-BPF-7-720.png)</span></span>

6. <span data-ttu-id="c6098-157">Modifique quaisquer vistas para a entidade de projeto para incluir o novo campo personalizado para fases.</span><span class="sxs-lookup"><span data-stu-id="c6098-157">Modify any views for the project entity to include your new custom field for stages.</span></span>

   > [!div class="mx-imgBorder"] 
   > <span data-ttu-id="c6098-158">![Captura de ecrã de modificação de vistas de Entidade de projeto](media/FAQ-Customize-BPF-8-720.png)</span><span class="sxs-lookup"><span data-stu-id="c6098-158">![Screenshot of modifying views on the Project entity](media/FAQ-Customize-BPF-8-720.png)</span></span>

