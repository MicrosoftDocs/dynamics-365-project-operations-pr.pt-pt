---
title: Despesas entre empresas
description: Esta tópico fornece informações sobre como utilizar as despesas interempresa para atribuir as despesas de um trabalhador à entidade jurídica para a qual o trabalho foi realizado.
author: ShylaThompson
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d2cdba8d5368a8b26bf4d98226bda76a58261cf0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005085"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="b6e7e-103">Despesas entre empresas</span><span class="sxs-lookup"><span data-stu-id="b6e7e-103">Intercompany expenses</span></span>

<span data-ttu-id="b6e7e-104">Um trabalhador que seja empregado por uma entidade legal numa organização pode realizar trabalho para outra entidade legal na mesma organização.</span><span class="sxs-lookup"><span data-stu-id="b6e7e-104">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="b6e7e-105">Pode utilizar as despesas interempresa para atribuir as despesas do trabalhador à entidade jurídica para a qual o trabalho foi realizado.</span><span class="sxs-lookup"><span data-stu-id="b6e7e-105">You can use intercompany expenses to assign the worker’s expenses to the legal entity for which the  work was performed.</span></span> <span data-ttu-id="b6e7e-106">A entidade legal que emprega o trabalhador é chamada de entidade legal emprestadora.</span><span class="sxs-lookup"><span data-stu-id="b6e7e-106">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="b6e7e-107">A entidade legal para a qual o trabalhador incorre em despesas é chamada de entidade legal emprestada.</span><span class="sxs-lookup"><span data-stu-id="b6e7e-107">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="b6e7e-108">Antes que um trabalhador possa criar e submeter despesas interempresa, deve ativar linhas de despesas interempresa.</span><span class="sxs-lookup"><span data-stu-id="b6e7e-108">Before a worker can create and submit intercompany expenses, you must enable intercompany expense lines.</span></span> <span data-ttu-id="b6e7e-109">Na entidade legal de empréstimo, na página de **parâmetros de gestão de despesas**, selecione **Permitir linhas de despesas interempresa**.</span><span class="sxs-lookup"><span data-stu-id="b6e7e-109">In the loaning legal entity, on the **Expense management parameters** page, select **Allow intercompany expense lines**.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="b6e7e-110">Tributação para despesas entre empresas</span><span class="sxs-lookup"><span data-stu-id="b6e7e-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b6e7e-111">Antes de poder utilizar grupos fiscais associados à entidade legal de empréstimo (fonte) em vez da entidade legal de empréstimo (destino) no seu relatório de despesas, deve ativar a funcionalidade na configuração do imposto geral sobre as vendas.</span><span class="sxs-lookup"><span data-stu-id="b6e7e-111">Before you can use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you must enable the functionality in the General ledger sales tax setup.</span></span> <span data-ttu-id="b6e7e-112">Quando a entidade jurídica para o parâmetro de **Entidade legal para publicação fiscal interempresa** estiver definida para **Fonte** e **Aplicar regras de tributação de impostos sobre vendas** estiver definida como **N.º**, é usada a combinação fiscal para a entidade legal de empréstimo.</span><span class="sxs-lookup"><span data-stu-id="b6e7e-112">When the **Legal entity for intercompany tax posting** parameter is set to **Source** and **Apply sales tax taxation rules** is set to **No**, the tax combination for the loaning legal entity is used.</span></span> <span data-ttu-id="b6e7e-113">Quando o mesmo parâmetro for definido como **Destino**, a combinação fiscal para a entidade legal emprestada será utilizada.</span><span class="sxs-lookup"><span data-stu-id="b6e7e-113">When the same parameter is set to **Destination**, the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="b6e7e-114">Para as entidades jurídicas nos Estados Unidos, quando o parâmetro for definido para **Origem**, o campo **Imposto de vendas a receber** também deve ser configurado na nova página **Grupos de publicação do livro razão**.</span><span class="sxs-lookup"><span data-stu-id="b6e7e-114">For legal entities in the United States, when the parameter is set to **Source**, the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="b6e7e-115">O motor contabilístico utilizará as informações deste campo para a entrada contabilística relacionada com os impostos.</span><span class="sxs-lookup"><span data-stu-id="b6e7e-115">The accounting engine will use the information from this field for tax-related accounting entry.</span></span>   
<span data-ttu-id="b6e7e-116">O comportamento é consistente para linhas de despesas publicadas com ou sem projeto.</span><span class="sxs-lookup"><span data-stu-id="b6e7e-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  


[!INCLUDE[footer-include](../includes/footer-banner.md)]