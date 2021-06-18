---
title: Criar modelos de previsão para orçamentos de projetos
description: Este tópico descreve como criar um modelo de previsão para os restantes orçamentos.
author: Yowelle
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 3549b41fce72b44230ab27de081dade15a912266
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006307"
---
# <a name="create-forecast-models-for-project-budgets"></a><span data-ttu-id="74211-103">Criar modelos de previsão para orçamentos de projetos</span><span class="sxs-lookup"><span data-stu-id="74211-103">Create forecast models for project budgets</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="74211-104">Este tópico descreve como criar um modelo de previsão para os restantes orçamentos.</span><span class="sxs-lookup"><span data-stu-id="74211-104">This topic describes how to create a forecast model for remaining budgets.</span></span> <span data-ttu-id="74211-105">Um projeto que está sujeito ao controlo orçamental utiliza dois tipos de orçamentos: originais e restantes.</span><span class="sxs-lookup"><span data-stu-id="74211-105">A project that is subject to budget control uses two types of budgets: original and remaining.</span></span> <span data-ttu-id="74211-106">Quando criar um orçamento de projeto, deve especificar os modelos de previsão orçamental originais e restantes que foram criados na página de **Modelos de previsão**.</span><span class="sxs-lookup"><span data-stu-id="74211-106">When you create a project budget, you must specify the original and remaining budget forecast models that were created in the **Forecast models** page.</span></span> <span data-ttu-id="74211-107">Os orçamentos do projeto com base nos modelos especificados são criados quando submete o orçamento do projeto.</span><span class="sxs-lookup"><span data-stu-id="74211-107">Project budgets based on the specified models are created when you commit the project budget.</span></span>

> [!NOTE]
> <span data-ttu-id="74211-108">Um modelo de previsão que é usado para o controlo orçamental não pode ter um submodelo ou ser usado como um submodelo.</span><span class="sxs-lookup"><span data-stu-id="74211-108">A forecast model that is used for budget control can’t have a submodel or be used as a submodel.</span></span>

1. <span data-ttu-id="74211-109">Selecione **Gestão de projetos e contabilística** > **Configurar** > **Previsões**  > **Modelos de previsão**.</span><span class="sxs-lookup"><span data-stu-id="74211-109">Select **Project management and accounting** > **Setup** > **Forecasts**  > **Forecast models**.</span></span>
2. <span data-ttu-id="74211-110">Selecione **Novo** para criar um novo modelo de previsão e, em seguida, insira um número de ID do modelo e nome para o novo modelo.</span><span class="sxs-lookup"><span data-stu-id="74211-110">Select **New** to create a new forecast model, and then enter a model ID number and name for the new model.</span></span> 
3. <span data-ttu-id="74211-111">Defina a opção **Parado** como **Sim** para evitar alterações às linhas de previsão para o modelo de previsão.</span><span class="sxs-lookup"><span data-stu-id="74211-111">Set the **Stopped** option to **Yes** to prevent any changes to the forecast lines for the forecast model.</span></span> 
4. <span data-ttu-id="74211-112">Se as linhas de previsão aos quais o modelo está associado gerarem previsões de fluxo de caixa no livro razão geral, defina **Incluir nas previsões de Fluxo de caixa** como **Sim**.</span><span class="sxs-lookup"><span data-stu-id="74211-112">If the forecast lines that the model is associated with should generate cash flow forecasts in the general ledger, set **Include in Cash flow forecasts** to **Yes.**</span></span> 
5. <span data-ttu-id="74211-113">Para utilizar a data do projeto como data da fatura, defina **Data da Fatura de Previsão** como **Sim**.</span><span class="sxs-lookup"><span data-stu-id="74211-113">To use the project date as the invoice date, set **Forecast Invoice date** to **Yes**.</span></span> 
6. <span data-ttu-id="74211-114">No campo **Tipo de orçamento**, selecione um dos seguintes tipos de modelos:</span><span class="sxs-lookup"><span data-stu-id="74211-114">In the **Budget type** field, select one of the following model types:</span></span>

   - <span data-ttu-id="74211-115">**Orçamento original**: Utilize os montantes orçamentais originais que são submetidos quando o orçamento inicial é criado e aprovado.</span><span class="sxs-lookup"><span data-stu-id="74211-115">**Original budget**: Use the original budget amounts that are committed when the initial budget is created and approved.</span></span>
   - <span data-ttu-id="74211-116">**Orçamento restante**: Utilize os restantes montantes orçamentais durante a vida do projeto.</span><span class="sxs-lookup"><span data-stu-id="74211-116">**Remaining budget**: Use the remaining budget amounts during the life of the project.</span></span> <span data-ttu-id="74211-117">Os saldos neste modelo de previsão são reduzidos por transações efetivas e aumentados ou diminuídos pelas revisões orçamentais.</span><span class="sxs-lookup"><span data-stu-id="74211-117">The balances in this forecast model are reduced by actual transactions and increased or decreased by budget revisions.</span></span>
   - <span data-ttu-id="74211-118">**Transpor**: Utilize os montantes orçamentais transpostos para o projeto.</span><span class="sxs-lookup"><span data-stu-id="74211-118">**Carry-forward**: Use the carry-forward budget amounts for the project.</span></span> <span data-ttu-id="74211-119">A transposição é um processo opcional que pode ser executado para transferir os montantes orçamentais não utilizados de um ano fiscal para outro.</span><span class="sxs-lookup"><span data-stu-id="74211-119">Carry-forward is an optional process that can be run to transfer unused budget amounts from one fiscal year to another.</span></span>

7. <span data-ttu-id="74211-120">Defina as seguintes opções, conforme necessário:</span><span class="sxs-lookup"><span data-stu-id="74211-120">Set the following options as required:</span></span>

   - <span data-ttu-id="74211-121">Ative **Data da fatura de previsão** para utilizar a data do projeto como data da fatura.</span><span class="sxs-lookup"><span data-stu-id="74211-121">Enable **Forecast invoice date** to use the project date as the invoice date.</span></span>
   - <span data-ttu-id="74211-122">Ative **Previsão com WIP** para prever com base no trabalho em curso (WIP) e, em seguida, selecione o tipo de WIP.</span><span class="sxs-lookup"><span data-stu-id="74211-122">Enable **Forecast with WIP** to forecast based on work in progress (WIP), and then select the type of WIP.</span></span> 
   - <span data-ttu-id="74211-123">Pode manter o **Tipo de orçamento** predefinido como **Nenhum** ou introduzir um novo tipo.</span><span class="sxs-lookup"><span data-stu-id="74211-123">You can keep the default **Budget type** as **None** or enter a new type.</span></span> <span data-ttu-id="74211-124">O tipo de orçamento não pode ser alterado depois de mudar um registo.</span><span class="sxs-lookup"><span data-stu-id="74211-124">The budget type can't be changed after you change a record.</span></span>     
    > [!NOTE]
    > <span data-ttu-id="74211-125">Se alterar o tipo de orçamento predefinido, todas as outras opções ficarão indisponíveis para atualização e não poderá reutilizar este modelo de previsão.</span><span class="sxs-lookup"><span data-stu-id="74211-125">If you change the default budget type, all other options will become unavailable for updates, and you can't reuse this forecast model.</span></span> 
   


 



[!INCLUDE[footer-include](../includes/footer-banner.md)]