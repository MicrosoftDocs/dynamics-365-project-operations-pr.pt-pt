---
title: Configurar os custos padrão da mão-de-obra e das despesas
description: Este tópico explica como configurar os custos padrão da mão-de-obra e das despesas de um projeto.
author: Yowelle
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b3eb6b1d4d75b095383689dd53a59a15fe9e884a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082461"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a>Configurar os custos padrão da mão-de-obra e das despesas

[!include [banner](../../includes/banner.md)]

Este tópico explica como configurar os custos padrão da mão-de-obra e das despesas de um projeto. Esta tarefa utiliza o conjunto de dados USSI.

1. No painel de navegação, vá para **Módulos > Gestão de projetos e contabilística > Configurar > Preços > Preço de custo (hora)**.
2. Selecione **Novo**.
3. No campo **Data efetiva**, introduza uma data.
4. No campo **Preço de custo**, introduza um número. Pode configurar um preço de custo padrão para a categoria do projeto ou configurar um preço de custo por número de trabalhador, número de projeto, categoria, data ou qualquer combinação destes. O preço de custo que é aplicado é o preço de custo com o mais alto nível de detalhe.  
5. Selecione **Guardar**.
6. No painel de navegação, vá para **Módulos > Gestão de projetos e contabilística > Configurar > Preços > Preço de venda (hora)**.
7. Selecione **Novo**.
8. No campo **Data efetiva**, introduza uma data.
9. No campo **Válido até**, selecione uma opção.
10. No campo **Preços**, introduza um número. Pode configurar um preço de venda padrão para transações por hora ou para uma categoria de projeto. Também pode configurar os preços de venda por número de trabalhador, número de projeto, categoria, data de transação ou qualquer combinação destes. O preço de venda real, que é aplicado quando um trabalhador introduza uma transação no Diário de horas, é o preço de venda com o mais alto nível de detalhe. Por exemplo, se estiver configurado um preço de venda geral e um preço de venda específico do trabalhador, será utilizado o preço de venda específico do trabalhador.  
11. Selecione **Guardar**.
12. Feche a página.
13. No painel de navegação, vá para **Módulos > Gestão de projetos e contabilística > Configurar > Preços > Preço de custo (despesa)**.
14. Selecione **Novo**.
15. No campo **Data efetiva**, introduza uma data.
16. No campo **Preço de custo**, introduza um número. Podem ser preenchidos vários campos, mas este é o mínimo necessário para guardar o registo.  
17. Selecione **Guardar**.
18. No painel de navegação, vá para **Módulos > Gestão de projetos e contabilística > Configurar > Preços > Preço de venda (despesa)**.
19. Selecione **Novo**.
20. No campo **Data efetiva**, introduza uma data.
21. No campo **Válido até**, selecione uma opção.
22. No campo **Preços**, introduza um número. O preço de venda real, que é aplicado quando um trabalhador introduza transações num diário de despesas, é o preço de venda com o mais alto nível de detalhe. Por exemplo, se estiver configurado um preço de venda geral e específico do trabalhador, será utilizado o preço de venda específico do trabalhador.  
23. Selecione **Guardar**.

