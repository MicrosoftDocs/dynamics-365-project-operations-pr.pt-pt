---
title: Despesas entre empresas
description: Esta tópico fornece informações sobre como utilizar as despesas interempresa para atribuir as despesas de um trabalhador à entidade jurídica para a qual o trabalho foi realizado.
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
ms.openlocfilehash: 553ddbe622210169db8de4aa506dcf1ea1e9d5ef
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960846"
---
# <a name="intercompany-expenses"></a>Despesas entre empresas

Um trabalhador que seja empregado por uma entidade legal numa organização pode realizar trabalho para outra entidade legal na mesma organização. Pode utilizar as despesas interempresa para atribuir as despesas do trabalhador à entidade jurídica para a qual o trabalho foi realizado. A entidade legal que emprega o trabalhador é chamada de entidade legal emprestadora. A entidade legal para a qual o trabalhador incorre em despesas é chamada de entidade legal emprestada. 

Antes que um trabalhador possa criar e submeter despesas interempresa, deve ativar linhas de despesas interempresa. Na entidade legal de empréstimo, na página de **parâmetros de gestão de despesas**, selecione **Permitir linhas de despesas interempresa**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Tributação para despesas entre empresas

[!include [banner](../includes/banner.md)]

Antes de poder utilizar grupos fiscais associados à entidade legal de empréstimo (fonte) em vez da entidade legal de empréstimo (destino) no seu relatório de despesas, deve ativar a funcionalidade na configuração do imposto geral sobre as vendas. Quando a entidade jurídica para o parâmetro de **Entidade legal para publicação fiscal interempresa** estiver definida para **Fonte** e **Aplicar regras de tributação de impostos sobre vendas** estiver definida como **N.º**, é usada a combinação fiscal para a entidade legal de empréstimo. Quando o mesmo parâmetro for definido como **Destino**, a combinação fiscal para a entidade legal emprestada será utilizada. Para as entidades jurídicas nos Estados Unidos, quando o parâmetro for definido para **Origem**, o campo **Imposto de vendas a receber** também deve ser configurado na nova página **Grupos de publicação do livro razão**. O motor contabilístico utilizará as informações deste campo para a entrada contabilística relacionada com os impostos.   
O comportamento é consistente para linhas de despesas publicadas com ou sem projeto.  


[!INCLUDE[footer-include](../includes/footer-banner.md)]