---
title: Trabalhar com despesas pessoais num relatório de despesas
description: Esta tópico fornece informações sobre como trabalhar com despesas pessoais incorridas pelos colaboradores durante a viagem para fins comerciais.
author: suvaidya
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: ae25eca08089d224f1e17e95eeb571054de8a5c0
ms.sourcegitcommit: fd6e9ff78392c7bac35591d9130c00d2750438ae
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/12/2021
ms.locfileid: "6025698"
---
# <a name="work-with-personal-expenses-on-an-expense-report"></a><span data-ttu-id="e5a41-103">Trabalhar com despesas pessoais num relatório de despesas</span><span class="sxs-lookup"><span data-stu-id="e5a41-103">Work with personal expenses on an expense report</span></span>

<span data-ttu-id="e5a41-104">_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_</span><span class="sxs-lookup"><span data-stu-id="e5a41-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e5a41-105">Durante as viagens de negócios, um empregado pode cobrar despesas pessoais ao seu cartão de crédito corporativo.</span><span class="sxs-lookup"><span data-stu-id="e5a41-105">During business travel, an employee might charge personal expenses to their corporate credit card.</span></span> <span data-ttu-id="e5a41-106">Se um processo não tiver sido definido para lidar com as despesas pessoais, o processo de aprovação do relatório de despesas pode ser interrompido quando um empregado apresentar o seu relatório de despesas discriminado.</span><span class="sxs-lookup"><span data-stu-id="e5a41-106">If a process hasn't been defined for handling personal expenses, the expense report approval process might be disrupted when an employee submits their itemized expense report.</span></span>

<span data-ttu-id="e5a41-107">Existem dois métodos que pode usar para trabalhar com as despesas pessoais de um empregado:</span><span class="sxs-lookup"><span data-stu-id="e5a41-107">There are two methods you can use to work with an employee's personal expenses:</span></span>

  - <span data-ttu-id="e5a41-108">**Pago pelo colaborador**: A sua organização não paga despesas pessoais que aparecem na conta do cartão de crédito corporativo.</span><span class="sxs-lookup"><span data-stu-id="e5a41-108">**Paid by employee**: Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="e5a41-109">Em vez disso, o empregado paga as despesas diretamente ao vendedor de cartões de crédito.</span><span class="sxs-lookup"><span data-stu-id="e5a41-109">Instead, the employee pays the credit card vendor directly for the expenses.</span></span> 
  - <span data-ttu-id="e5a41-110">**Pago pela empresa**: A sua organização paga a conta completa do cartão de crédito corporativo e, em seguida, debita a conta do trabalhador para as despesas pessoais.</span><span class="sxs-lookup"><span data-stu-id="e5a41-110">**Paid by company**: Your organization pays the full bill for the corporate credit card, and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="e5a41-111">Pode selecionar o método que a sua organização utiliza na página **Parâmetros de gestão de despesas**.</span><span class="sxs-lookup"><span data-stu-id="e5a41-111">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>


## <a name="enable-split-expense-function-when-personal-amount-field-has-value-defined"></a><span data-ttu-id="e5a41-112">Ativar a função de despesas divididas quando o campo de montante pessoal tiver valor definido</span><span class="sxs-lookup"><span data-stu-id="e5a41-112">Enable split expense function when personal amount field has value defined</span></span>

<span data-ttu-id="e5a41-113">A função **Ativar a função de despesas divididas quando o campo de montante pessoal tiver valor definido** aplica-se apenas aos relatórios de despesas aprovados através de um fluxo de trabalho de nível de linha.</span><span class="sxs-lookup"><span data-stu-id="e5a41-113">The feature, **Enable split expense function when personal amount field has value defined** only applies to expense reports that are approved using a line-level workflow.</span></span> <span data-ttu-id="e5a41-114">Os relatórios são aprovados através de **Processar relatórios de despesas** > **Relatórios de despesas atribuídos a mim** > **Abrir relatório de despesas**.</span><span class="sxs-lookup"><span data-stu-id="e5a41-114">Reports are approved by going to **Process expense reports** > **Expense reports assigned to me** > **Open expense report**.</span></span> 

<span data-ttu-id="e5a41-115">Para ativar esta funcionalidade, aceda a **Áreas de Trabalho** > **Gestão de Funcionalidades**, selecione **Ativar a função de despesas divididas quando o campo de montante pessoal tiver valor definido** e, em seguida, selecione **Ativar agora**.</span><span class="sxs-lookup"><span data-stu-id="e5a41-115">To enable this feature, go to **Workspaces** > **Feature Management**, select **Enable split expense function when personal amount field has value defined**, and then select **Enable now**.</span></span> 

<span data-ttu-id="e5a41-116">Quando a funcionalidade está ativa, as linhas de despesas que utilizam esta funcionalidade geram duas linhas quando o relatório é submetido.</span><span class="sxs-lookup"><span data-stu-id="e5a41-116">When the feature is enabled, expense lines that use this functionality generate two lines when the report is submitted.</span></span> <span data-ttu-id="e5a41-117">São geradas duas linhas para que o aprovador possa aprovar cada linha separadamente.</span><span class="sxs-lookup"><span data-stu-id="e5a41-117">Two lines are generated so that the approver can approve each line separately.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
