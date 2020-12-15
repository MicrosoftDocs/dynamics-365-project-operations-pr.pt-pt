---
title: Desativar uma dimensão de definição de preços
description: Este tópico fornece informações sobre como desativar dimensões de definição de preço.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
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
ms.openlocfilehash: 986fae72c6b44b3f76281aefb81ffdaa96f71ae7
ms.sourcegitcommit: 13a4e58eddbb0f81aca07c1ff452c420dbd8a68f
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 11/30/2020
ms.locfileid: "4650063"
---
# <a name="turning-off-a-pricing-dimension"></a>Desativar uma dimensão de definição de preços

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

Poderá ter de analisar e atualizar a sua estratégia de definição de preços a cada ano. Quaisquer atualizações feitas podem exigir que desative uma dimensão de definição de preços existente e crie uma nova. Por exemplo, poderá ter de definir o preço anteriormente por **Função**, mas agora decidiu definir o preço por **Experiência de Trabalho**. Isto poderá fazer com que seja necessário desativar a **Função** como uma dimensão de definição de preços e criar uma **Experiência de Trabalho** como uma nova dimensão de definição de preços. 

A desativação de uma dimensão de definição de preços, independentemente de a mesma ser fornecida com o programa ou personalizada, pode ser efetuada definindo os campos **Aplicável ao Custo** e **Aplicável às Vendas** da Dimensão de Definição de Preços como **Não**.

No entanto, quando o fizer, poderá receber a mensagem de erro, **a dimensão da definição dos preços não pode ser atualizada ou eliminada se existirem registos de preços associados.**

![É provável que haja um erro no processo de negócio ao desativar uma dimensão de definição de preços](media/Business-Process-Error.png)

Esta mensagem de erro indica que existem registos de preços configurados anteriormente para a dimensão que está a ser desativada. Todos os registos **Preço da Função** e **Margem de Lucro do Preço da Função** que façam referência a uma dimensão têm de ser eliminados antes de a aplicabilidade da dimensão poder ser definida como **Não**. Esta regra aplica-se às dimensões de definição de preços fornecidas com o programa e a quaisquer dimensões de definição de preços personalizadas que possa ter criado. O motivo desta validação é porque cada registo **Preço da Função** deve ter uma combinação exclusiva de dimensões. Por exemplo, numa lista de preços denominada **Taxas de custo nos EUA 2018**, tem as seguintes linhas de **Preço da Função**. 

| Título Padrão         | Unidade Organizacional    |Unidade   |Preço  |Moeda  |
| -----------------------|-------------|-------|-------|----------|
| Engenheiro de Sistemas|Contoso EUA|Hour| 100|USD|
| Engenheiro de Sistemas Sénior|Contoso EUA|Hour| 150| USD|


Quando desativar o **Título Padrão** como a dimensão de definição de preços e o motor de definição de preços procurar um preço, só irá utilizar o valor **Unidade Organizacional** do contexto de entrada. Se a **Unidade Organizacional** do contexto de entrada for "Contoso US", o resultado será não determinístico porque as duas linhas corresponderão. Para evitar este cenário, quando cria registos de **Preço da Função**, o sistema valida que a combinação de dimensões é exclusiva. Se a dimensão for desativada após a criação dos registos de **Preço da Função**, esta restrição poderá ser violada. Consequentemente, é necessário que, antes de desativar uma dimensão, elimine todas as linhas de **Preço da Função** e **Margem de Lucro do Preço da Função** que tenham esse valor de dimensão preenchido.
