---
title: Tipos de período
description: Este tópico fornece informações sobre como configurar tipos de período para estimativas de receitas.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6bcd988fbd074c66d64f7e327b4329d3de27e950
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531521"
---
# <a name="period-types"></a><span data-ttu-id="a71c6-103">Tipos de período</span><span class="sxs-lookup"><span data-stu-id="a71c6-103">Period types</span></span>

<span data-ttu-id="a71c6-104">_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_</span><span class="sxs-lookup"><span data-stu-id="a71c6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="a71c6-105">Um tipo de período define a frequência com que as receitas de um projeto são estimadas.</span><span class="sxs-lookup"><span data-stu-id="a71c6-105">A period type defines how frequently revenue on a project is estimated.</span></span> <span data-ttu-id="a71c6-106">Este tópico fornece informações sobre como configurar tipos de período para estimativas de receitas.</span><span class="sxs-lookup"><span data-stu-id="a71c6-106">This topic provides information about how to set up period types for revenue estimation.</span></span> 

## <a name="create-and-work-with-period-types"></a><span data-ttu-id="a71c6-107">Criar e trabalhar com tipos de períodos</span><span class="sxs-lookup"><span data-stu-id="a71c6-107">Create and work with period types</span></span>
<span data-ttu-id="a71c6-108">Para criar e trabalhar com tipos de períodos, complete os seguintes passos:</span><span class="sxs-lookup"><span data-stu-id="a71c6-108">To create and work with period types, complete the following steps:</span></span>

1. <span data-ttu-id="a71c6-109">No seu ambiente do Dynamics 365 Finance, aceda a **Gestão de projetos e contabilística** > **Configurar** > **Estimativas** > **Tipos de períodos**.</span><span class="sxs-lookup"><span data-stu-id="a71c6-109">In your Dynamics 365 Finance environment, go to **Project management and accounting** > **Setup** > **Estimates** > **Period types**.</span></span>
2. <span data-ttu-id="a71c6-110">Selecione **Novo** para criar um novo tipo de período.</span><span class="sxs-lookup"><span data-stu-id="a71c6-110">Select **New** to create new period type.</span></span> <span data-ttu-id="a71c6-111">Introduza um nome e descrição.</span><span class="sxs-lookup"><span data-stu-id="a71c6-111">Enter a name and description.</span></span>
3. <span data-ttu-id="a71c6-112">No campo **Frequência**, selecione um valor:</span><span class="sxs-lookup"><span data-stu-id="a71c6-112">In the **Frequency** field, select a value:</span></span>

    - <span data-ttu-id="a71c6-113">Se selecionar **Semana**, **Quinzenal**, **Semi-mensal**, **Mês**, **Dia**, **Trimestre** ou **Ano**, o calendário será utilizado para gerar os períodos.</span><span class="sxs-lookup"><span data-stu-id="a71c6-113">If you select **Week**, **Bi-weekly**, **Semi-monthly**, **Month**, **Day**, **Quarter**, or **Year**, the calendar will be used to generate the periods.</span></span> 
    - <span data-ttu-id="a71c6-114">Se selecionar o **Período do livro razão**, serão utilizados períodos de contabilidade a partir da configuração do livro razão geral para gerar períodos.</span><span class="sxs-lookup"><span data-stu-id="a71c6-114">If you select **Ledger period**, ledger periods from the General ledger configuration will be used to generate periods.</span></span>
    - <span data-ttu-id="a71c6-115">Se selecionar **Ilimitado**, pode especificar os períodos personalizados.</span><span class="sxs-lookup"><span data-stu-id="a71c6-115">If you select **Unlimited**, you can specify custom periods.</span></span>
4. <span data-ttu-id="a71c6-116">Selecione o registo do tipo de período e, em seguida, selecione **Gerar períodos** para criar períodos para o tipo de período.</span><span class="sxs-lookup"><span data-stu-id="a71c6-116">Select the period type record and then select **Generate periods** to create periods for the period type.</span></span> <span data-ttu-id="a71c6-117">Com base na frequência de período que selecionou, poderá ter a opção de especificar uma data de início ou o número de períodos a gerar.</span><span class="sxs-lookup"><span data-stu-id="a71c6-117">Based on the period frequency that you selected, you might have the option to specify a start date or the number of periods to generate.</span></span>
5. <span data-ttu-id="a71c6-118">Selecione **Períodos** para rever os períodos gerados.</span><span class="sxs-lookup"><span data-stu-id="a71c6-118">Select **Periods** to review generated periods.</span></span>

