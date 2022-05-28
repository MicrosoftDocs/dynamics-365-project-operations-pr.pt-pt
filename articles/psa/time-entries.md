---
title: Criar entradas de tempo
description: Este tópico fornece informações sobre como criar entradas de tempo.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 4b8f88da372cd56b19bed82ad6918da6ddd6f202
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593534"
---
# <a name="create-time-entries"></a>Criar entradas de tempo

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Nas versões anteriores do Dynamics 365 Project Service Automation, as entradas de tempo foram introduzidas semanalmente. Na versão 3 do Project Service Automation, as entradas de tempo são introduzidas diariamente. No entanto, depois de terem sido criadas algumas entradas de tempo, pode criá-las em massa ou copiá-las.

## <a name="create-a-time-entry"></a>Criar uma entrada de tempo

Siga estes passos para criar uma entrada de tempo.

1. Na página **Entradas de Tempo**, selecione **Novo**.
2. Na caixa de diálogo **Criação Rápida: Entrada de Tempo**, introduza a duração da entrada de tempo em minutos, horas ou dias. A duração tem de ser introduzida no seguinte formato: *x* minutos, *x* horas ou *x* dias. As horas e os dias também podem ser introduzidos utilizando-se valores decimais, como *x.x* horas ou *x.x* dias.
3. Selecione o tipo de entrada de tempo e o projeto para o qual está a introduzir a entrada de tempo.
4. No campo **Tarefa do Projeto**, localize a tarefa referente a esta entrada de tempo.

    > [!NOTE]
    > Se estiver a criar uma entrada de tempo para uma tarefa que não está atribuída a um utilizador, no campo **Tarefa do Projeto**, selecione o botão **Pesquisar**, selecione **Alterar Vista** e, em seguida, selecione **Todas as Tarefas do Projeto Ativas** para listar todas as tarefas.

5. Introduza uma descrição, se for necessária uma descrição e, em seguida, selecione **Guardar e Fechar**.

Depois de a entrada de tempo ser criada e guardada, pode editá-la na grelha de entrada de tempo. A grelha de entrada de tempo suporta dois formatos:

- É possível introduzir entradas de tempo no formato **hh:mm**. Em seguida, este formato é convertido em horas e frações.
- Pode introduzir horas e frações diretamente.

Note que as frações de uma hora não são minutos. Consequentemente, 1,5 horas representa 1 hora e 30 minutos. A mesma regra aplica-se a frações de um dia. Um dia é 24 horas e 0,5 dias representa 12 horas.

## <a name="bulk-create-time-entries"></a>Criação de entradas de tempo em massa

Depois de terem sido criadas algumas entradas de tempo, pode copiá-las para criar entradas de tempo adicionais em massa.

1. Na página **Entradas de Tempo**, selecione **Copiar Semana**.
2. No grupo de campos **Do Período**, nos campos **Data de Início** e **Data de Fim**, defina o intervalo de datas a partir do qual pretende copiar entradas de tempo.
3. No grupo de campos **Até ao período**, no campo **Data de Início**, especifique a data para a qual as entradas de tempo são criadas.
4. Selecione **Copiar** para criar uma cópia das entradas de tempo que correspondem ao dia da semana especificado no grupo de campos **Até ao Período**. Por exemplo, a entrada de tempo para a segunda-feira da semana passada é copiada para a segunda-feira da semana especificada no grupo de campos **Até ao Período**.

## <a name="import-data-for-time-entries"></a>Importar dados para entradas de tempo

Pode importar dados a partir de reservas e atribuições de projetos. Quando importa dados, pode especificar o intervalo de datas das reservas a importar e, em seguida, selecionar explicitamente as reservas que devem ser criadas como entradas de tempo de **Rascunho**.

## <a name="group-by-sort-search-and-filter-capabilities"></a>Agrupar por, ordenar, pesquisar e filtrar capacidades

Pode agrupar e filtrar entradas de tempo pelas dimensões especificadas nas colunas. No campo **Agrupar por**, selecione a dimensão a utilizar para filtrar entradas de tempo. Também pode ordenar os registos de entrada de tempo por ordem ascendente ou descendente utilizando a seta de ordenação nos cabeçalhos de coluna. Além disso, pode mostrar ou ocultar entradas selecionando o botão **Filtrar** nos cabeçalhos de coluna e, em seguida, na caixa **Pesquisar**, introduzindo o texto que deve ser utilizado para procurar entradas de tempo por nome de projeto, tarefa de projeto, entrada de tempo ou recurso.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
