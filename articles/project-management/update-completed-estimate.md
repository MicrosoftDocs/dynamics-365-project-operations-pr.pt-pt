---
title: Atualizar estimativa na conclusão
description: Este tópico fornece informações sobre a atualização da projeção do esforço num projeto.
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 0e63bdb815a6f758c57d055c8c03d92e04700445
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286442"
---
# <a name="update-estimate-at-completion"></a>Atualizar estimativa na conclusão

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

É comum que um gestor de projeto reveja as estimativas originais de uma tarefa. As reprojeções do projeto são a perceção de estimativas de um gestor de projeto, dado o estado atual de um projeto. No entanto, não recomendamos que os gestores de projeto alterem os valores da linha de base, porque a linha de base do projeto representa a fonte de verdade estabelecida para a agenda e a estimativa de custo do projeto acordadas por todos os intervenientes.

Existem duas formas de um gestor de projeto poder reprojetar o esforço nas tarefas:

- Substitua a estimativa predefinida para terminar (ETC) por uma nova estimativa do esforço real restante na tarefa. 
- Substitua a percentagem de progresso predefinida por uma nova estimativa do verdadeiro progresso na tarefa.

Cada uma destas abordagens causa um novo cálculo da ETC, da EAC e da estimativa a completar (EAC) e percentagem de progresso da tarefa e o desvio do esforço projetado numa tarefa. A EAC, a ETC e a percentagem de progresso das tarefas de resumo são recalculadas e produzem uma nova projeção de variância do esforço.


[!INCLUDE[footer-include](../includes/footer-banner.md)]