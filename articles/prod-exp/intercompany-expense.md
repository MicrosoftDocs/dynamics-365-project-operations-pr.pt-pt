---
title: Despesas entre empresas
description: Um trabalhador que seja empregado por uma entidade legal numa organização pode realizar trabalho para outra entidade legal na mesma organização. Nesta situação, pode utilizar a função de despesa entre empresas para atribuir as despesas do trabalhador à entidade legal para a qual o trabalho foi realizado.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082555"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="5608c-104">Despesas entre empresas</span><span class="sxs-lookup"><span data-stu-id="5608c-104">Intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5608c-105">Um trabalhador que seja empregado por uma entidade legal numa organização pode realizar trabalho para outra entidade legal na mesma organização.</span><span class="sxs-lookup"><span data-stu-id="5608c-105">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="5608c-106">Nesta situação, pode utilizar a função de despesa entre empresas para atribuir as despesas do trabalhador à entidade legal para a qual o trabalho foi realizado.</span><span class="sxs-lookup"><span data-stu-id="5608c-106">In this situation, you can use the intercompany expense feature to assign the worker’s expenses to the legal entity for which the work was performed.</span></span> <span data-ttu-id="5608c-107">A entidade legal que emprega o trabalhador é chamada de entidade legal emprestadora.</span><span class="sxs-lookup"><span data-stu-id="5608c-107">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="5608c-108">A entidade legal para a qual o trabalhador incorre em despesas é chamada de entidade legal emprestada.</span><span class="sxs-lookup"><span data-stu-id="5608c-108">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="5608c-109">Antes que um trabalhador possa criar e submeter despesas para o trabalho que é realizado para uma entidade legal diferente, na entidade legal de empréstimo, na página **Parâmetros de gestão de despesas** , selecione a opção **Permitir linhas de despesas entre empresas**.</span><span class="sxs-lookup"><span data-stu-id="5608c-109">Before a worker can create and submit expenses for work that is performed for a different legal entity, in the loaning legal entity, on the **Expense management parameters** page, select the **Allow intercompany expense lines** option.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="5608c-110">Tributação para despesas entre empresas</span><span class="sxs-lookup"><span data-stu-id="5608c-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5608c-111">Se pretender utilizar grupos fiscais associados à entidade legal emprestadora (origem) em vez da entidade legal emprestada (destino) no seu relatório de despesas, terá de o configurar no imposto geral de venda de contabilidade configurado.</span><span class="sxs-lookup"><span data-stu-id="5608c-111">If you want to use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you will need to configure this in the General ledger sales tax set up.</span></span> <span data-ttu-id="5608c-112">Quando o parâmetro do livro razão Geral, a **entidade legal para a tributação entre empresas** é definida como **Origem** e **Aplicar regras de tributação de impostos sobre vendas** é definida como **Não** , a combinação fiscal para a entidade legal emprestadora será utilizada.</span><span class="sxs-lookup"><span data-stu-id="5608c-112">When the General ledger parameter, **Legal entity for intercompany tax posting** is set to **Source** and **Apply sales tax taxation rules** is set to **No** , the tax combination for the loaning legal entity will be used.</span></span> <span data-ttu-id="5608c-113">Quando o mesmo parâmetro for definido como **Destino** , a combinação fiscal para a entidade legal emprestada será utilizada.</span><span class="sxs-lookup"><span data-stu-id="5608c-113">When the same parameter is set to **Destination** , the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="5608c-114">Para as entidades jurídicas nos Estados Unidos, quando o parâmetro for definido para **Origem** , o campo **Imposto de vendas a receber** também deve ser configurado na nova página **Grupos de publicação do livro razão**.</span><span class="sxs-lookup"><span data-stu-id="5608c-114">For legal entities in the United States, when the parameter is set to **Source** , the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="5608c-115">O motor contabilístico utilizará as informações deste campo para a entrada contabilística relacionada com os impostos.</span><span class="sxs-lookup"><span data-stu-id="5608c-115">The accounting engine will use the information from this field for tax related accounting entry.</span></span>   
<span data-ttu-id="5608c-116">O comportamento é consistente para linhas de despesas publicadas com ou sem projeto.</span><span class="sxs-lookup"><span data-stu-id="5608c-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  
