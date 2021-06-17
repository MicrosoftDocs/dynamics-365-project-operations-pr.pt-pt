---
title: Despesas pessoais num relatório de despesas
description: Este tópico explica os dois métodos para processar as despesas pessoais de um trabalhador no Microsoft Dynamics 365 Finance.
author: saraschi2
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 355e47054c20b32193c9819844c41c03cadf7fad
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005445"
---
# <a name="personal-expenses-on-an-expense-report"></a><span data-ttu-id="b9fd2-103">Despesas pessoais num relatório de despesas</span><span class="sxs-lookup"><span data-stu-id="b9fd2-103">Personal expenses on an expense report</span></span>

<span data-ttu-id="b9fd2-104">Durante as viagens de negócios, os trabalhadores podem, por vezes, cobrar despesas pessoais aos seus cartões de crédito corporativos.</span><span class="sxs-lookup"><span data-stu-id="b9fd2-104">During business travel, workers might sometimes charge personal expenses to their corporate credit cards.</span></span> <span data-ttu-id="b9fd2-105">Se não definir um processo de tratamento de despesas pessoais, o processo de aprovação dos relatórios de despesas poderá ser interrompido quando os trabalhadores apresentarem os seus relatórios de despesas discriminados.</span><span class="sxs-lookup"><span data-stu-id="b9fd2-105">If you don't define a process for handling personal expenses, the approval process for expense reports might be disrupted when workers submit their itemized expense reports.</span></span> 

<span data-ttu-id="b9fd2-106">Existem dois métodos para processar despesas pessoais de um trabalhador:</span><span class="sxs-lookup"><span data-stu-id="b9fd2-106">There are two methods for handling a worker's personal expenses:</span></span>

- <span data-ttu-id="b9fd2-107">**Pago pelo colaborador** – A sua organização não paga despesas pessoais que aparecem na conta do cartão de crédito corporativo.</span><span class="sxs-lookup"><span data-stu-id="b9fd2-107">**Paid by employee** – Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="b9fd2-108">Em vez disso, cria um relatório que mostra as despesas pessoais juntamente com as despesas corporativas que foram cobradas ao cartão de crédito corporativo.</span><span class="sxs-lookup"><span data-stu-id="b9fd2-108">Instead, it creates a report that shows personal expenses together with the corporate expenses that were charged to the corporate credit card.</span></span>
- <span data-ttu-id="b9fd2-109">**Pago pela empresa** – A sua organização paga a conta total do cartão de crédito corporativo e depois debita a conta do trabalhador para as despesas pessoais.</span><span class="sxs-lookup"><span data-stu-id="b9fd2-109">**Paid by company** – Your organization pays the whole bill for the corporate credit card and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="b9fd2-110">Pode selecionar o método que a sua organização utiliza na página **Parâmetros de gestão de despesas**.</span><span class="sxs-lookup"><span data-stu-id="b9fd2-110">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]