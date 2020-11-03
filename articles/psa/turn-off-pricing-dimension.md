---
title: Desativar uma dimensão de definição de preços
description: Este tópico mostra como configurar dimensões de definição de preços na solução do Project Service.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 1ae95430c368370145c7081a5d94d6161a7700b4
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082489"
---
# <a name="turn-off-a-pricing-dimension"></a>Desativar uma dimensão de definição de preços

Poderá ter de analisar e atualizar a sua estratégia de definição de preços a cada ano. Quaisquer atualizações feitas podem exigir que desative uma dimensão de definição de preços existente e crie uma nova. Por exemplo, poderá ter de definir o preço anteriormente por **Função** , mas agora decidiu definir o preço por **Experiência de Trabalho**. Isto poderá fazer com que seja necessário desativar a **Função** como uma dimensão de definição de preços e criar uma **Experiência de Trabalho** como uma nova dimensão de definição de preços. 

A desativação de uma dimensão de definição de preços, independentemente de a mesma ser fornecida com o programa ou personalizada, pode ser efetuada definindo os campos **Aplicável ao Custo** e **Aplicável às Vendas** da Dimensão de Definição de Preços como **Não**.

No entanto, ao fazê-lo, poderá receber a seguinte mensagem de erro.

![É provável que haja um erro no processo de negócio ao desativar uma dimensão de definição de preços](media/Business-Process-Error.png)


Esta mensagem de erro indica que existem registos de preços configurados anteriormente para a dimensão que está a ser desativada. Todos os registos **Preço da Função** e **Margem de Lucro do Preço da Função** que façam referência a uma dimensão têm de ser eliminados antes de a aplicabilidade da dimensão poder ser definida como **Não**. Esta regra aplica-se às dimensões de definição de preços fornecidas com o programa e a quaisquer dimensões de definição de preços personalizadas que possa ter criado. O motivo dessa validação é porque o Project Service tem uma restrição de que cada registo **Preço da Função** deve ter uma combinação exclusiva de dimensões. Por exemplo, numa lista de preços denominada **Taxas de custo nos EUA 2018** , tem as seguintes linhas de **Preço da Função**. 

| Título Padrão         | Unidade Organizacional    |Unidade   |Preço  |Moeda  |
| -----------------------|-------------|-------|-------|----------|
| Engenheiro de Sistemas|Contoso EUA|Hour| 100|USD|
| Engenheiro de Sistemas Sénior|Contoso EUA|Hour| 150| USD|


Quando desativar o **Título Padrão** como a dimensão de definição de preços e o motor de definição de preços do Project Service procurar um preço, só irá utilizar o valor **Unidade Organizacional** do contexto de entrada. Se a **Unidade Organizacional** do contexto de entrada for "Contoso US", o resultado será não determinístico porque as duas linhas corresponderão. Para evitar este cenário, quando cria registos de **Preço da Função** , o Project Service valida que a combinação de dimensões é exclusiva. Se a dimensão for desativada após a criação dos registos de **Preço da Função** , esta restrição poderá ser violada. Consequentemente, é necessário que, antes de desativar uma dimensão, elimine todas as linhas de **Preço da Função** e **Margem de Lucro do Preço da Função** que tenham esse valor de dimensão preenchido.

