---
title: Definições do projeto
description: Este tópico fornece informações sobre as definições de gestão do projeto.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: c9b8659f3b7ee81d2e21ef52743debd521fa9bb9
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082567"
---
# <a name="project-settings"></a>Definições do projeto

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Utilize as seguintes definições para aceder às funcionalidades de planeamento do projeto.

## <a name="work-template"></a>Modelo de trabalho

Para criar uma agenda de projeto, cria um modelo de calendário do projeto que define o número de horas de trabalho por dia e todos os encerramentos de companhia. Para criar um modelo de calendário do projeto, associe um modelo de trabalho ao campo **Modelo de calendário** do projeto. Siga estes passos para criar um modelo de trabalho.

1. No PSA, no painel de navegação esquerdo, clique em **Recursos**. 
2. Na página da lista de **Recursos** , abra o registo de utilizador e selecione **Mostrar Horas de Trabalho**.

  > [!NOTE]
  > Certifique-se de que permite pop-ups na página do browser. Isto permite-lhe ver as horas de trabalho definidas para o recurso.
  
3. No separador **Vista Mensal** , clique em **Configurar**. É apresentada uma lista de três opções: 

  - Nova Agenda Semanal
  - Agenda de Trabalho Para Um Dia
  - Intervalo

> ![Configurar opções](media/project-13.png)

4. Selecione **Nova Agenda Semanal** e, em seguida, defina as opções para esta agenda de recursos. É possível definir uma agenda semanal periódica, os parâmetros de hora diária, os encerramentos de companhia e muito mais.
5. Defina o intervalo de datas, selecione **Guardar** e clique em **Fechar**. 
6. Volte à página da lista de **Recursos** e selecione o recurso para o qual define as horas de trabalho. 
7. Selecione **Definir Calendário Como** para definir o modelo de trabalho. 
8. Na caixa de diálogo **Modelo de Trabalho** , introduza um nome para o modelo de trabalho e selecione **Aplicar**. 

Agora, pode associar o modelo de trabalho a um modelo de calendário do projeto.

## <a name="resource-roles"></a>Funções do recurso

O termo *função do recurso* refere-se ao conjunto de qualificações, competências e certificações que uma pessoa tem de ter para executar um conjunto de tarefas específicas num projeto. O PSA permite-lhe contabilizar e faturar o tempo de um recurso com base na função à qual o recurso está associado. Cada organização tem de configurar estas funções utilizando a navegação à esquerda no menu **Project Service**.

Cada organização tem de configurar estas funções na página **Categorias de Recurso Ativas**. Para abrir esta página, no painel de navegação esquerdo, selecione **Funções do Recurso**.

## <a name="price-lists"></a>Listas de preços

As listas de preços permitem definir preços de custo e vendas para funções de recursos, categorias de despesa, produtos e outros elementos numa organização. Antes de definir estimativas financeiras para o trabalho que deve ser entregue para um projeto, deve criar uma lista de preços de custo e venda subjacente. Na secção de parâmetros, também deverá configurar uma lista de preços de custo e de venda predefinida que se aplique a todos os projetos criados na organização. Na página **Parâmetros do Projeto Ativos** , certifique-se de que configurou uma lista de preços de custo e venda predefinida.
