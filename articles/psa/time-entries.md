---
title: Criar entradas de tempo
description: Este tópico fornece informações sobre como criar entradas de tempo.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 8f86f69090e869bf5e6a7505a4cb1ad1c69b475b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5282167"
---
# <a name="create-time-entries"></a><span data-ttu-id="991b5-103">Criar entradas de tempo</span><span class="sxs-lookup"><span data-stu-id="991b5-103">Create time entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="991b5-104">Nas versões anteriores do Dynamics 365 Project Service Automation, as entradas de tempo foram introduzidas semanalmente.</span><span class="sxs-lookup"><span data-stu-id="991b5-104">In previous versions of Dynamics 365 Project Service Automation, time entries were entered on a weekly basis.</span></span> <span data-ttu-id="991b5-105">Na versão 3 do Project Service Automation, as entradas de tempo são introduzidas diariamente.</span><span class="sxs-lookup"><span data-stu-id="991b5-105">In version 3 of Project Service Automation, time entries are entered on a daily basis.</span></span> <span data-ttu-id="991b5-106">No entanto, depois de terem sido criadas algumas entradas de tempo, pode criá-las em massa ou copiá-las.</span><span class="sxs-lookup"><span data-stu-id="991b5-106">However, after a few time entries have been created, you can bulk create or copy them.</span></span>

## <a name="create-a-time-entry"></a><span data-ttu-id="991b5-107">Criar uma entrada de tempo</span><span class="sxs-lookup"><span data-stu-id="991b5-107">Create a time entry</span></span>

<span data-ttu-id="991b5-108">Siga estes passos para criar uma entrada de tempo.</span><span class="sxs-lookup"><span data-stu-id="991b5-108">Follow these steps to create a time entry.</span></span>

1. <span data-ttu-id="991b5-109">Na página **Entradas de Tempo**, selecione **Novo**.</span><span class="sxs-lookup"><span data-stu-id="991b5-109">On the **Time Entries** page, select **New**.</span></span>
2. <span data-ttu-id="991b5-110">Na caixa de diálogo **Criação Rápida: Entrada de Tempo**, introduza a duração da entrada de tempo em minutos, horas ou dias.</span><span class="sxs-lookup"><span data-stu-id="991b5-110">In the **Quick Create: Time Entry** dialog box, enter the duration of the time entry in minutes, hours, or days.</span></span> <span data-ttu-id="991b5-111">A duração tem de ser introduzida no seguinte formato: *x* minutos, *x* horas ou *x* dias.</span><span class="sxs-lookup"><span data-stu-id="991b5-111">The duration must be entered in the following format: *x* minutes, *x* hours, or *x* days.</span></span> <span data-ttu-id="991b5-112">As horas e os dias também podem ser introduzidos utilizando-se valores decimais, como *x.x* horas ou *x.x* dias.</span><span class="sxs-lookup"><span data-stu-id="991b5-112">Hours and days can also be entered as decimal values, such as *x.x* hours or *x.x* days.</span></span>
3. <span data-ttu-id="991b5-113">Selecione o tipo de entrada de tempo e o projeto para o qual está a introduzir a entrada de tempo.</span><span class="sxs-lookup"><span data-stu-id="991b5-113">Select the type of time entry and the project that you're entering the time entry for.</span></span>
4. <span data-ttu-id="991b5-114">No campo **Tarefa do Projeto**, localize a tarefa referente a esta entrada de tempo.</span><span class="sxs-lookup"><span data-stu-id="991b5-114">In the **Project Task** field, find the task for this time entry.</span></span>

    > [!NOTE]
    > <span data-ttu-id="991b5-115">Se estiver a criar uma entrada de tempo para uma tarefa que não está atribuída a um utilizador, no campo **Tarefa do Projeto**, selecione o botão **Pesquisar**, selecione **Alterar Vista** e, em seguida, selecione **Todas as Tarefas do Projeto Ativas** para listar todas as tarefas.</span><span class="sxs-lookup"><span data-stu-id="991b5-115">If you're creating a time entry for a task that isn't assigned to a user, in the **Project Task** field, select the **Search** button, select **Change View**, and then select **All Active Project Tasks** to list all tasks.</span></span>

5. <span data-ttu-id="991b5-116">Introduza uma descrição, se for necessária uma descrição e, em seguida, selecione **Guardar e Fechar**.</span><span class="sxs-lookup"><span data-stu-id="991b5-116">Enter a description, if a description is required, and then select **Save and Close**.</span></span>

<span data-ttu-id="991b5-117">Depois de a entrada de tempo ser criada e guardada, pode editá-la na grelha de entrada de tempo.</span><span class="sxs-lookup"><span data-stu-id="991b5-117">After the time entry is created and saved, you can edit it in the time entry grid.</span></span> <span data-ttu-id="991b5-118">A grelha de entrada de tempo suporta dois formatos:</span><span class="sxs-lookup"><span data-stu-id="991b5-118">The time entry grid supports two formats:</span></span>

- <span data-ttu-id="991b5-119">É possível introduzir entradas de tempo no formato **hh:mm**.</span><span class="sxs-lookup"><span data-stu-id="991b5-119">You can enter time entries in **hh:mm** format.</span></span> <span data-ttu-id="991b5-120">Em seguida, este formato é convertido em horas e frações.</span><span class="sxs-lookup"><span data-stu-id="991b5-120">This format is then converted to hours and fractions.</span></span>
- <span data-ttu-id="991b5-121">Pode introduzir horas e frações diretamente.</span><span class="sxs-lookup"><span data-stu-id="991b5-121">You can enter hours and fractions directly.</span></span>

<span data-ttu-id="991b5-122">Note que as frações de uma hora não são minutos.</span><span class="sxs-lookup"><span data-stu-id="991b5-122">Note that the fractions of an hour aren't minutes.</span></span> <span data-ttu-id="991b5-123">Consequentemente, 1,5 horas representa 1 hora e 30 minutos.</span><span class="sxs-lookup"><span data-stu-id="991b5-123">Therefore, 1.5 hours represents 1 hour and 30 minutes.</span></span> <span data-ttu-id="991b5-124">A mesma regra aplica-se a frações de um dia.</span><span class="sxs-lookup"><span data-stu-id="991b5-124">The same rule applies to fractions of a day.</span></span> <span data-ttu-id="991b5-125">Um dia é 24 horas e 0,5 dias representa 12 horas.</span><span class="sxs-lookup"><span data-stu-id="991b5-125">One day is 24 hours, and 0.5 days represents 12 hours.</span></span>

## <a name="bulk-create-time-entries"></a><span data-ttu-id="991b5-126">Criação de entradas de tempo em massa</span><span class="sxs-lookup"><span data-stu-id="991b5-126">Bulk create time entries</span></span>

<span data-ttu-id="991b5-127">Depois de terem sido criadas algumas entradas de tempo, pode copiá-las para criar entradas de tempo adicionais em massa.</span><span class="sxs-lookup"><span data-stu-id="991b5-127">After a few time entries have been created, you can copy them to create additional time entries in bulk.</span></span>

1. <span data-ttu-id="991b5-128">Na página **Entradas de Tempo**, selecione **Copiar Semana**.</span><span class="sxs-lookup"><span data-stu-id="991b5-128">On the **Time Entries** page, select **Copy Week**.</span></span>
2. <span data-ttu-id="991b5-129">No grupo de campos **Do Período**, nos campos **Data de Início** e **Data de Fim**, defina o intervalo de datas a partir do qual pretende copiar entradas de tempo.</span><span class="sxs-lookup"><span data-stu-id="991b5-129">In the **From Period** field group, in the **Start Date** and **End Date** fields, define the date range to copy time entries from.</span></span>
3. <span data-ttu-id="991b5-130">No grupo de campos **Até ao período**, no campo **Data de Início**, especifique a data para a qual as entradas de tempo são criadas.</span><span class="sxs-lookup"><span data-stu-id="991b5-130">In the **To Period** field group, in the **Start Date** field, specify the date to create time entries for.</span></span>
4. <span data-ttu-id="991b5-131">Selecione **Copiar** para criar uma cópia das entradas de tempo que correspondem ao dia da semana especificado no grupo de campos **Até ao Período**.</span><span class="sxs-lookup"><span data-stu-id="991b5-131">Select **Copy** to create a copy of the time entries that correspond to the day of the week that is specified in the **To Period** field group.</span></span> <span data-ttu-id="991b5-132">Por exemplo, a entrada de tempo para a segunda-feira da semana passada é copiada para a segunda-feira da semana especificada no grupo de campos **Até ao Período**.</span><span class="sxs-lookup"><span data-stu-id="991b5-132">For example, the time entry for Monday of last week is copied to Monday of the week that is specified in the **To Period** field group.</span></span>

## <a name="import-data-for-time-entries"></a><span data-ttu-id="991b5-133">Importar dados para entradas de tempo</span><span class="sxs-lookup"><span data-stu-id="991b5-133">Import data for time entries</span></span>

<span data-ttu-id="991b5-134">Pode importar dados a partir de reservas e atribuições de projetos.</span><span class="sxs-lookup"><span data-stu-id="991b5-134">You can import data from project bookings and assignments.</span></span> <span data-ttu-id="991b5-135">Quando importa dados, pode especificar o intervalo de datas das reservas a importar e, em seguida, selecionar explicitamente as reservas que devem ser criadas como entradas de tempo de **Rascunho**.</span><span class="sxs-lookup"><span data-stu-id="991b5-135">When you import data, you can specify the date range of the bookings to import and then explicitly select the bookings that should be created as **Draft** time entries.</span></span>

## <a name="group-by-sort-search-and-filter-capabilities"></a><span data-ttu-id="991b5-136">Agrupar por, ordenar, pesquisar e filtrar capacidades</span><span class="sxs-lookup"><span data-stu-id="991b5-136">Group by, sort, search, and filter capabilities</span></span>

<span data-ttu-id="991b5-137">Pode agrupar e filtrar entradas de tempo pelas dimensões especificadas nas colunas.</span><span class="sxs-lookup"><span data-stu-id="991b5-137">You can group and filter time entries by the dimensions that are specified in the columns.</span></span> <span data-ttu-id="991b5-138">No campo **Agrupar por**, selecione a dimensão a utilizar para filtrar entradas de tempo.</span><span class="sxs-lookup"><span data-stu-id="991b5-138">In the **Group by** field, select the dimension to use to filter time entries.</span></span> <span data-ttu-id="991b5-139">Também pode ordenar os registos de entrada de tempo por ordem ascendente ou descendente utilizando a seta de ordenação nos cabeçalhos de coluna.</span><span class="sxs-lookup"><span data-stu-id="991b5-139">You can also sort the time entry records in ascending or descending order by using the sort arrow on the column headings.</span></span> <span data-ttu-id="991b5-140">Além disso, pode mostrar ou ocultar entradas selecionando o botão **Filtrar** nos cabeçalhos de coluna e, em seguida, na caixa **Pesquisar**, introduzindo o texto que deve ser utilizado para procurar entradas de tempo por nome de projeto, tarefa de projeto, entrada de tempo ou recurso.</span><span class="sxs-lookup"><span data-stu-id="991b5-140">Additionally, you can show or hide entries by selecting the **Filter** button on the column headings, and then, in the **Search** box, entering the text that should be used to search for time entries by project name, project task, time entry, or resource.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]