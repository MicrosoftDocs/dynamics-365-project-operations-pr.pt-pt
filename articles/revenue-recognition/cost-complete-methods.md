---
title: Métodos de custo para conclusão
description: Este tópico fornece informações sobre os métodos utilizados para calcular o custo para a conclusão de um projeto.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: fe42ea0e1a5c562ec648fbf2a2924648af80381b9db8ffe0c209cb5247bb2ba2
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997980"
---
# <a name="cost-to-complete-methods"></a>Métodos de custo para conclusão

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

Este tópico fornece informações sobre os métodos utilizados para calcular o custo para a conclusão de um projeto. Existem vários métodos que pode usar para calcular o custo para concluir um projeto. 

Quando criar uma estimativa para um projeto, na página **Criar estimativas**, no campo **Método de custo para conclusão**, pode selecionar um dos seguintes métodos de custo para conclusão.

| Método de custo para conclusão    | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Custo total – real            | Introduza os custos de estimativa manualmente nos campos **Custo total** ou **Quantidade total** utilizando o botão **Estimativa de custo** na **Página de estimativa**. O sistema subtrai os custos reais a partir dos totais que inseriu. O total é o custo para a conclusão do projeto. Este método não utiliza as estimativas de despesas e atribuições de recursos introduzidas no Project Operations criadas no Microsoft Dataverse. O custo total ou a quantidade total podem ser atualizados manualmente, se necessário.  |
| Previsão total – real        | As atribuições de recursos e as estimativas de despesas são usadas para determinar o valor total da previsão do projeto. Os custos reais são comparados com esta previsão para calcular o custo para a conclusão.                                                                                                                                                                                                                                                                          |
| Como estimativa anterior         | Os mesmos métodos de estimativa utilizados no período anterior são utilizados aqui. Este método requer um modelo de previsão se o período anterior requeria de um modelo de previsão.                                                                                                                                                                                                                                                                                                                           |
| Definir custo para conclusão como zero | Normalmente, usado antes do projeto de estimativa ser eliminado, este método corresponde às estimativas totais com transações reais publicadas e limpa a coluna **Custo para conclusão**. Quando concluído, o resultado é sempre 100 por cento. Para cada linha de custos que cria, a caixa de verificação **Previsão** é limpa e a estimativa total é copiada da estimativa de custos anterior. O consumo real para a estimativa do período é deduzido do custo para conclusão do projeto.              |
| Do modelo de custo           | O método de custo para conclusão que é configurado no modelo de custos que está associado ao projeto de estimativa selecionado.                                                                                                                                                                                                                                                                                                                                                                          |


[!INCLUDE[footer-include](../includes/footer-banner.md)]