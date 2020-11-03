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
# <a name="intercompany-expenses"></a>Despesas entre empresas

[!include [banner](../includes/banner.md)]

Um trabalhador que seja empregado por uma entidade legal numa organização pode realizar trabalho para outra entidade legal na mesma organização. Nesta situação, pode utilizar a função de despesa entre empresas para atribuir as despesas do trabalhador à entidade legal para a qual o trabalho foi realizado. A entidade legal que emprega o trabalhador é chamada de entidade legal emprestadora. A entidade legal para a qual o trabalhador incorre em despesas é chamada de entidade legal emprestada. 

Antes que um trabalhador possa criar e submeter despesas para o trabalho que é realizado para uma entidade legal diferente, na entidade legal de empréstimo, na página **Parâmetros de gestão de despesas** , selecione a opção **Permitir linhas de despesas entre empresas**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Tributação para despesas entre empresas

[!include [banner](../includes/banner.md)]

Se pretender utilizar grupos fiscais associados à entidade legal emprestadora (origem) em vez da entidade legal emprestada (destino) no seu relatório de despesas, terá de o configurar no imposto geral de venda de contabilidade configurado. Quando o parâmetro do livro razão Geral, a **entidade legal para a tributação entre empresas** é definida como **Origem** e **Aplicar regras de tributação de impostos sobre vendas** é definida como **Não** , a combinação fiscal para a entidade legal emprestadora será utilizada. Quando o mesmo parâmetro for definido como **Destino** , a combinação fiscal para a entidade legal emprestada será utilizada. Para as entidades jurídicas nos Estados Unidos, quando o parâmetro for definido para **Origem** , o campo **Imposto de vendas a receber** também deve ser configurado na nova página **Grupos de publicação do livro razão**. O motor contabilístico utilizará as informações deste campo para a entrada contabilística relacionada com os impostos.   
O comportamento é consistente para linhas de despesas publicadas com ou sem projeto.  
