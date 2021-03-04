---
title: Ordens de venda de projetos para projetos de tempo e material
description: Este tópico explica como criar ordens de venda baseadas no projeto para os projetos de tempo e material.
author: Yowelle
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 3653a6869dab323be88f1fd0f9fd0f2cb35c456f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082389"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a>Ordens de venda de projetos para projetos de tempo e material

[!include[banner](../includes/banner.md)]

Este tópico descreve como criar uma ordem de venda para um projeto. As ordens de venda só podem ser criadas para projetos do tipo **tempo e material**.

Se um projeto de tempo e material tiver múltiplas fontes de financiamento no contrato de projeto, tem de ativar o parâmetro **Permitir ordens de venda para projetos com múltiplas fontes de financiamento** na página **Parâmetros da gestão de projetos e contabilística**. 

> [!NOTE]
> - O suporte para ordens de venda de projetos com múltiplas fontes de financiamento está disponível a partir da versão de aplicação 10.0.2 e superior.
> - O parâmetro para ativar o suporte para ordens de venda de projetos com múltiplas fontes de financiamento será removido na segunda fase do lançamento de abril de 2020, após a qual a funcionalidade estará sempre ativada.

Pode criar ordens de venda baseadas em projetos de duas formas:

- Vá para o próprio projeto. No Painel de Ação, selecione **Gerir > Tarefas do item > Ordem de venda**. A informação do projeto assumirá por predefinição a ordem de venda do projeto. Se o contrato de projeto tiver mais de uma fonte de financiamento, terá de selecionar a fonte de financiamento para definir o cliente para a ordem de venda. Se existir apenas uma fonte de financiamento para o projeto, o cliente será definido automaticamente.
- Vá para a página da lista **Todas as ordens de venda** e crie uma nova ordem de venda. Terá de selecionar o projeto para a ordem de venda. Depois de selecionado o projeto, o cliente será definido a partir da fonte de financiamento ou terá de selecionar a fonte de financiamento se o contrato de projeto tiver múltiplas fontes de financiamento.



[!INCLUDE[footer-include](../includes/footer-banner.md)]