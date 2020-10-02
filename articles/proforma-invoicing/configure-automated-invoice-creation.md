---
title: Configurar uma criação automatizada de faturas
description: Este tópico fornece informações sobre como configurar o sistema para gerar faturas automaticamente.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 764fd4568619e4f5676ee3cbf7fce14ffb069548
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898140"
---
# <a name="configure-automated-invoice-creation"></a><span data-ttu-id="ca12e-103">Configurar uma criação automatizada de faturas</span><span class="sxs-lookup"><span data-stu-id="ca12e-103">Configure automated invoice creation</span></span>

<span data-ttu-id="ca12e-104">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="ca12e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ca12e-105">Complete os seguintes passos para configurar a execução de uma fatura automatizada nas operações do Projeto.</span><span class="sxs-lookup"><span data-stu-id="ca12e-105">Complete the following steps to configure an automated invoice run in Project operations.</span></span>

1. <span data-ttu-id="ca12e-106">Aceda a **Definições** \> **Tarefas de lote**.</span><span class="sxs-lookup"><span data-stu-id="ca12e-106">Go to **Settings** \> **Batch jobs**.</span></span>
2. <span data-ttu-id="ca12e-107">Crie uma tarefa de lote e atribua-lhe o nome **Criar faturas nas operações do Projeto**.</span><span class="sxs-lookup"><span data-stu-id="ca12e-107">Create a batch job, and name it **Project operations create invoices**.</span></span> <span data-ttu-id="ca12e-108">O nome da tarefa de lote tem de incluir o termo "criar faturas."</span><span class="sxs-lookup"><span data-stu-id="ca12e-108">The name of the batch job must include the term "create invoices."</span></span>
3. <span data-ttu-id="ca12e-109">No campo **Tipo de tarefa**, selecione **Nenhum**.</span><span class="sxs-lookup"><span data-stu-id="ca12e-109">In the **Job type** field, select **None**.</span></span> <span data-ttu-id="ca12e-110">Por predefinição, as opções **Frequência Diária** e **Está Ativo** estão definidas como **Sim**.</span><span class="sxs-lookup"><span data-stu-id="ca12e-110">By default, the **Frequency Daily** and **Is Active** options are set to **Yes**.</span></span>
4. <span data-ttu-id="ca12e-111">Selecione **Executar Fluxo de Trabalho**.</span><span class="sxs-lookup"><span data-stu-id="ca12e-111">Select **Run Workflow**.</span></span> <span data-ttu-id="ca12e-112">Na caixa de diálogo **Pesquisar Registo**, verá três fluxos de trabalho:</span><span class="sxs-lookup"><span data-stu-id="ca12e-112">In the **Look Up Record** dialog box, you will see three workflows:</span></span>

    - <span data-ttu-id="ca12e-113">ProcessRunCaller</span><span class="sxs-lookup"><span data-stu-id="ca12e-113">ProcessRunCaller</span></span>
    - <span data-ttu-id="ca12e-114">ProcessRunner</span><span class="sxs-lookup"><span data-stu-id="ca12e-114">ProcessRunner</span></span>
    - <span data-ttu-id="ca12e-115">UpdateRoleUtilization</span><span class="sxs-lookup"><span data-stu-id="ca12e-115">UpdateRoleUtilization</span></span>

5. <span data-ttu-id="ca12e-116">Selecione **ProcessRunCaller** e, em seguida, selecione **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="ca12e-116">Select **ProcessRunCaller**, and then select **Add**.</span></span>
6. <span data-ttu-id="ca12e-117">Na caixa de diálogo seguinte, selecione **OK**.</span><span class="sxs-lookup"><span data-stu-id="ca12e-117">In the next dialog box, select **OK**.</span></span> <span data-ttu-id="ca12e-118">Um fluxo de trabalho de **Suspensão** é seguido por um fluxo de trabalho do **Processo**.</span><span class="sxs-lookup"><span data-stu-id="ca12e-118">A **Sleep** workflow is followed by a **Process** workflow.</span></span>

    <span data-ttu-id="ca12e-119">Também pode selecionar **ProcessRunner** no passo 5.</span><span class="sxs-lookup"><span data-stu-id="ca12e-119">You can also select **ProcessRunner** in step 5.</span></span> <span data-ttu-id="ca12e-120">Em seguida, quando selecionar **OK**, um fluxo de trabalho do **Processo** é seguido por um fluxo de trabalho de **Suspensão**.</span><span class="sxs-lookup"><span data-stu-id="ca12e-120">Then, when you select **OK**, a **Process** workflow is followed by a **Sleep** workflow.</span></span>

<span data-ttu-id="ca12e-121">Os fluxos de trabalho **ProcessRunCaller** e **ProcessRunner** criam faturas.</span><span class="sxs-lookup"><span data-stu-id="ca12e-121">The **ProcessRunCaller** and **ProcessRunner** workflows create invoices.</span></span> <span data-ttu-id="ca12e-122">O **ProcessRunCaller** chama o **ProcessRunner**.</span><span class="sxs-lookup"><span data-stu-id="ca12e-122">**ProcessRunCaller** calls **ProcessRunner**.</span></span> <span data-ttu-id="ca12e-123">**ProcessRunner** é o fluxo de trabalho que, na realidade, cria as faturas.</span><span class="sxs-lookup"><span data-stu-id="ca12e-123">**ProcessRunner** is the workflow that actually creates the invoices.</span></span> <span data-ttu-id="ca12e-124">Passa por todos os itens de contrato para os quais é necessário criar faturas e cria faturas para essas linhas.</span><span class="sxs-lookup"><span data-stu-id="ca12e-124">It goes through all the contract lines that invoices must be created for, and it creates invoices for those lines.</span></span> <span data-ttu-id="ca12e-125">Para determinar os itens de contrato para os quais devem ser criadas faturas, a tarefa examina as datas de execução da fatura para os itens de contrato.</span><span class="sxs-lookup"><span data-stu-id="ca12e-125">To determine the contract lines that invoices must be created for, the job looks at invoice run dates for the contract lines.</span></span> <span data-ttu-id="ca12e-126">Se os itens de contrato que pertencem a um contrato tiverem a mesma data de execução da fatura, as transações são combinadas numa fatura que tem duas linhas de fatura.</span><span class="sxs-lookup"><span data-stu-id="ca12e-126">If contract lines that belong to one contract have the same invoice run date, the transactions are combined into one invoice that has two invoice lines.</span></span> <span data-ttu-id="ca12e-127">Se não houver transações para as quais criar faturas, a tarefa ignorará a criação da fatura.</span><span class="sxs-lookup"><span data-stu-id="ca12e-127">If there are no transactions to create invoices for, the job skips invoice creation.</span></span>

<span data-ttu-id="ca12e-128">Depois de **ProcessRunner** ter terminado a execução, chama o **ProcessRunCaller**, fornece a hora de fim e é fechado.</span><span class="sxs-lookup"><span data-stu-id="ca12e-128">After **ProcessRunner** has finished running, it calls **ProcessRunCaller**, provides the end time, and is closed.</span></span> <span data-ttu-id="ca12e-129">**ProcessRunCaller** em seguida, inicia um temporizador que funciona durante 24 horas a partir da hora de fim especificada.</span><span class="sxs-lookup"><span data-stu-id="ca12e-129">**ProcessRunCaller** then starts a timer that runs for 24 hours from the specified end time.</span></span> <span data-ttu-id="ca12e-130">No final do temporizador, o **ProcessRunCaller** é fechado.</span><span class="sxs-lookup"><span data-stu-id="ca12e-130">At the end of the timer, **ProcessRunCaller** is closed.</span></span>

<span data-ttu-id="ca12e-131">A tarefa de processamento em lote para criar faturas é uma tarefa recorrente.</span><span class="sxs-lookup"><span data-stu-id="ca12e-131">The batch process job for creating invoices is a recurrent job.</span></span> <span data-ttu-id="ca12e-132">Se este processamento em lote for executado muitas vezes, são criadas várias instâncias da tarefa e causam erros.</span><span class="sxs-lookup"><span data-stu-id="ca12e-132">If this batch process is run many times, multiple instances of the job are created and cause errors.</span></span> <span data-ttu-id="ca12e-133">Consequentemente, deverá iniciar o processamento em lote apenas uma vez, e só deverá reiniciá-lo se parar de ser executado.</span><span class="sxs-lookup"><span data-stu-id="ca12e-133">Therefore, you should start the batch process only one time, and you should restart it only if it stops running.</span></span>

> [!NOTE]
> <span data-ttu-id="ca12e-134">A faturação do lote só funciona para itens de contrato do projeto que são configurados por horários da fatura.</span><span class="sxs-lookup"><span data-stu-id="ca12e-134">Batch invoicing only runs for project contract lines that are configured by invoice schedules.</span></span> <span data-ttu-id="ca12e-135">Uma linha de contrato com um método de faturação de preço fixo tem de ter marcos configurados.</span><span class="sxs-lookup"><span data-stu-id="ca12e-135">A contract line with a fixed price billing method must have milestones configured.</span></span> <span data-ttu-id="ca12e-136">Uma linha de contrato de projeto com um método de faturação de tempo e material necessitará de uma configuração de agenda de faturamento baseado em datas.</span><span class="sxs-lookup"><span data-stu-id="ca12e-136">A project contract line with a time and material billing method will need a date-based invoice schedule set up.</span></span> <span data-ttu-id="ca12e-137">O mesmo se aplica a uma linha de contratos baseada em projetos.</span><span class="sxs-lookup"><span data-stu-id="ca12e-137">The same applies to a project-based contract line.</span></span>     
