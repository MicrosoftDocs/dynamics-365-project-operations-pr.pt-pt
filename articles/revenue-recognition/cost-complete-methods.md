---
title: Métodos de custo para conclusão
description: Este artigo fornece informações sobre os métodos utilizados para calcular o custo para concluir um projeto.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 39c10673afd04ad7d4a94a01211c2f9d335a02c2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920304"
---
# <a name="cost-to-complete-methods"></a>Métodos de custo para conclusão

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

Este artigo fornece informações sobre os métodos utilizados para calcular o custo para concluir um projeto. Existem vários métodos que pode usar para calcular o custo para concluir um projeto. 

Quando criar uma estimativa para um projeto, na página **Criar estimativas**, no campo **Método de custo para conclusão**, pode selecionar um dos seguintes métodos de custo para conclusão.

| Método de custo para conclusão    | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Custo total – real            | Introduza os custos de estimativa manualmente nos campos **Custo total** ou **Quantidade total** utilizando o botão **Estimativa de custo** na **Página de estimativa**. O sistema subtrai os custos reais a partir dos totais que inseriu. O total é o custo para a conclusão do projeto. Este método não utiliza as estimativas de despesas e atribuições de recursos introduzidas no Project Operations criadas no Microsoft Dataverse. O custo total ou a quantidade total podem ser atualizados manualmente, se necessário.  |
| Previsão total – real        | As atribuições de recursos e as estimativas de despesas são usadas para determinar o valor total da previsão do projeto. Os custos reais são comparados com esta previsão para calcular o custo para a conclusão.                                                                                                                                                                                                                                                                          |
| Como estimativa anterior         | Os mesmos métodos de estimativa utilizados no período anterior são utilizados aqui. Este método requer um modelo de previsão se o período anterior requeria de um modelo de previsão.                                                                                                                                                                                                                                                                                                                           |
| Definir custo para conclusão como zero | Normalmente, usado antes do projeto de estimativa ser eliminado, este método corresponde às estimativas totais com transações reais publicadas e limpa a coluna **Custo para conclusão**. Quando concluído, o resultado é sempre 100 por cento. Para cada linha de custos que cria, a caixa de verificação **Previsão** é limpa e a estimativa total é copiada da estimativa de custos anterior. O consumo real para a estimativa do período é deduzido do custo para conclusão do projeto.              |
| Do modelo de custo           | O método de custo para conclusão que é configurado no modelo de custos que está associado ao projeto de estimativa selecionado.                                                                                                                                                                                                                                                                                                                                                                          |


[!INCLUDE[footer-include](../includes/footer-banner.md)]