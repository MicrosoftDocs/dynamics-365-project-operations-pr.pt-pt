---
title: Despesas entre empresas
description: Esta tópico fornece informações sobre como utilizar as despesas interempresa para atribuir as despesas de um trabalhador à entidade jurídica para a qual o trabalho foi realizado.
author: suvaidya
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6788a590879bd839ebb9dedc45895dc047cc9f15
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/04/2022
ms.locfileid: "8684248"
---
# <a name="intercompany-expenses"></a>Despesas entre empresas

Um trabalhador que seja empregado por uma entidade legal numa organização pode realizar trabalho para outra entidade legal na mesma organização. Pode utilizar as despesas interempresa para atribuir as despesas do trabalhador à entidade jurídica para a qual o trabalho foi realizado. A entidade legal que emprega o trabalhador é chamada de entidade legal emprestadora. A entidade legal para a qual o trabalhador incorre em despesas é chamada de entidade legal emprestada. 

Antes que um trabalhador possa criar e submeter despesas interempresa, deve ativar linhas de despesas interempresa. Na entidade legal de empréstimo, na página de **parâmetros de gestão de despesas**, selecione **Permitir linhas de despesas interempresa**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Tributação para despesas entre empresas

[!include [banner](../includes/banner.md)]

Antes de poder utilizar grupos fiscais associados à entidade legal de empréstimo (fonte) em vez da entidade legal de empréstimo (destino) no seu relatório de despesas, deve ativar a funcionalidade na configuração do imposto geral sobre as vendas. Quando a entidade jurídica para o parâmetro de **Entidade legal para publicação fiscal interempresa** estiver definida para **Fonte** e **Aplicar regras de tributação de impostos sobre vendas** estiver definida como **N.º**, é usada a combinação fiscal para a entidade legal de empréstimo. Quando o mesmo parâmetro for definido como **Destino**, a combinação fiscal para a entidade legal emprestada será utilizada. Para as entidades jurídicas nos Estados Unidos, quando o parâmetro for definido para **Origem**, o campo **Imposto de vendas a receber** também deve ser configurado na nova página **Grupos de publicação do livro razão**. O motor contabilístico utilizará as informações deste campo para a entrada contabilística relacionada com os impostos.   
O comportamento é consistente para linhas de despesas publicadas com ou sem projeto.  

## <a name="new-expense-expression-builder"></a>Novo construtor de expressões de despesas

O novo construtor de expressões de despesas resolve problemas com cenários de despesas entre empresas que utilizam projetos. Esta funcionalidade garante que, quando cria uma despesa entre empresas, a política de despesas é corretamente validada relativamente ao projeto que é selecionado na linha de despesas, e que o relatório de despesas pode ser submetido com sucesso.

Para que a funcionalidade de construtor de expressões de despesas funcione, deve ser ativada. Além disso, deve ser criada a política de despesas que tem um ID do projeto.

Se já tiver configurado políticas que validam o ID do projeto na linha de despesas, essas políticas devem ser retiradas. Em seguida, pode ativar a funcionalidade e reconfigurar as políticas.

Para ativar a funcionalidade, siga estes passos.

1. Aceda a **Áreas de Trabalho** \> **Gestão de Funcionalidades**.
2. Na lista, selecione **Novo construtor de expressões de despesas para resolver problemas com os cenários de despesas entre empresas que utilizam projetos**. Em seguida, selecione **Ativar agora**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
