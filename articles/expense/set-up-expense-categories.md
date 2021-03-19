---
title: Configurar categorias de despesas
description: Este tópico fornece informações sobre como configurar categorias de despesas e categorias partilhadas para relatórios de despesas.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 1589cf82626e744d35f31fef8e8437a5ad71360d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276137"
---
# <a name="set-up-expense-categories"></a>Configurar categorias de despesas

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

Quando os colaboradores criam relatórios de despesas, cada despesa que registam tem de ser associada a uma categoria de despesas. As categorias de despesas são derivadas das categorias partilhadas que podem ser partilhadas pelas entidades legais na sua organização. Consoante a forma como a sua organização é definida, estas categorias de despesas também podem ser partilhadas noutras áreas. Com base na definição da sua organização e na orientação da equipa de implementação, tem de determinar se as categorias que são utilizadas na Gestão de despesas serão utilizadas apenas na Gestão de despesas ou se devem ser partilhadas noutras áreas.

> [!NOTE]
> Estas categorias podem ser partilhadas entre a Gestão de projeto, a Gestão contabilística e a Gestão de despesas, ou entre a Gestão de projeto, a Gestão contabilística e a Produção. No entanto, não podem ser partilhadas entre a Gestão de despesas e a Produção.

Antes de iniciar o processo de configuração, têm de ser tomadas as seguintes decisões para cada categoria de despesas:

- O que é uma categoria de despesa? Os exemplos incluem categorias para voos, hotel ou quilometragem.
- A categoria de despesa também pode ser utilizada na Gestão de projetos e contabilística? Se puder, também tem de tomar as seguintes decisões:

    - Que contas de custos serão utilizadas para as seguintes despesas?

        - Custo
        - Alocação de vencimentos
        - Valor do custo WIP
        - Item de custo
        - Item de valor de custo WIP
        - Perdas acumuladas
        - Perdas acumuladas WIP

    - Que contas de receitas serão utilizadas para as seguintes origens de receitas?

        - Receitas faturadas
        - Valor das vendas de receitas acumuladas
        - Valor de vendas WIP
        - Produção de receitas acumuladas
        - Produção WIP
        - Lucros de receitas acumuladas
        - Lucros WIP
        - Subscrição de receitas acumuladas
        - Subscrição WIP

- O que é um tipo de despesa?
- Qual o método de pagamento predefinido para a categoria de despesa?
- As despesas na categoria de despesa têm de ser discriminadas?
- Qual a conta predefinida principal para a categoria de despesa?
- Qual o grupo de impostos sobre as vendas de artigos predefinido para a categoria de despesa?
- São permitidos métodos de pagamento adicionais para a categoria de despesa? Nesse caso, o que são?
- Existem subcategorias nesta categoria de despesa? Se existirem subcategorias, também tem de tomar as seguintes decisões:

    - Alguma das subcategorias está excluída da recuperação de impostos?
    - Qual o grupo impostos sobre vendas de artigos das subcategorias?


[!INCLUDE[footer-include](../includes/footer-banner.md)]