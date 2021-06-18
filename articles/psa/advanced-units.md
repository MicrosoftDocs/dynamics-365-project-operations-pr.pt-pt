---
title: Grupos de unidades e unidades
description: Este tópico fornece informações sobre grupos de unidades e unidades.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
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
ms.openlocfilehash: e981f39bbb6ca4277778382a5816952df2a8a1fb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009585"
---
# <a name="unit-groups-and-units"></a>Grupos de unidades e unidades

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Os grupos de unidades e as unidades são entidades básicas do Microsoft Dynamics 365. Uma unidade é uma unidade de medida única e as várias unidades podem ser agrupadas em grupos de unidades. Por vezes, um grupo de unidades é referido como uma agenda de unidades na interface de utilizador (IU) do Dynamics 365. 

Seguem-se alguns exemplos de unidades e grupos de unidades:
 
- **Grupo de unidades**: Distância 
    - **Unidades**: Milha, Quilómetro, etc.
- **Grupo de unidades**: Tempo
    - **Unidades**: Hora, dia, semana, etc. 

Quando configura várias unidades num grupo de unidades, também tem de configurar um fator de conversão entre as mesmas, designando a primeira unidade que configurou como predefinida ou a unidade primária para o grupo de unidades. 

Por exemplo, num grupo de unidades **Tempo**, se configurar a **Hora** como a primeira unidade, o sistema designará a **Hora** como a unidade predefinida. Se a próxima unidade que configurar for **Dia**, tem de configurar um fator de conversão de **Dia** para **Hora**. Se, em seguida adicionar **Semana** como uma terceira unidade, tem de configurar um fator de conversão de **Semana** em termos de **Dia** ou **Hora**. 

A imagem seguinte mostra uma configuração de exemplo para a unidade **Dia**, em que o campo **Quantidade** mostra o número de horas num dia e uma **Semana**, em que o campo **Quantidade** mostra o número de dias que se encontram numa semana.

> ![Grupo de unidades: página de informações](media/advanced-2.png)

## <a name="using-units-and-unit-groups"></a>Utilizar grupos de unidades e unidades

O Dynamics 365 Project Service Automation utiliza unidades e grupos de unidades para processar estimativas e entradas para as despesas e o tempo. 

Para as despesas, cada categoria de despesa tem um grupo de unidades e uma unidade predefinidos. Estes valores são introduzidos como valores predefinidos nas entradas da lista de preços para as categorias de despesa. 

Por exemplo, tem uma categoria de despesa com o nome **Quilometragem**. Tem um grupo de unidades com nome **Distância** e uma unidade predefinida com o nome **Milha**. Se configurar o grupo de unidades **Distância** para que tenha duas unidades (**Milha** e **Quilómetro**), pode definir dois preços para a categoria **Quilometragem** numa lista de preços: preço por milha e preço por quilómetro.

| Categoria de despesa  | Grupo de unidades  | Unidade      | Método de definição de preços  | Preço unitário  |
|-------------------|---------------|-----------|-------------------|-------------------|
| Quilometragem           | Distância      | Milha      | Preço unitário    | 10 USD            |
| Quilometragem           | Distância      | Quilómetro | Preço unitário    |  6 USD            |

Quando introduzir uma despesa num projeto, o sistema determina o preço através da combinação da categoria e da unidade na despesa. 

| Descrição da despesa        | Categoria de despesa  | Unidade  | Quantidade  | Preço unitário   |
|----------------------------|---------------------|-------|-----------|----------------|
| Conduzir até à localização do cliente | Quilometragem             | Milha  | 10        | 10 USD         |

Quanto ao tempo, cada cabeçalho da lista de preços tem um campo **Unidade de Tempo Predefinida**. O valor é definido quando o cabeçalho da lista de preços é criado. Esta unidade é utilizada para definir todos os preços baseados em funções nessa lista de preços.

As linhas de estimativa para o campo **Tempo na Proposta** podem ser expressas em qualquer unidade de tempo. No entanto, as linhas de estimativa sobre os projetos e as entradas de tempo para os projetos só podem utilizar a unidade de tempo **Hora**. Se a unidade na entrada de tempo ou na linha de estimativa não corresponder à unidade na linha da lista de preços para essa função, o sistema converte o preço nas unidades definidas na estimativa do projeto ou na transação real do projeto.

O exemplo que se segue mostra como o PSA utiliza o grupo de unidades, as unidades e os fatores de conversão.
- Unidades

   - **Grupo de unidades**: Tempo 
   - **Unidades**: Hora 
    
    - **Dia** - Fator de conversão: 8 horas       
    - **Semana** - Fator de conversão: 40 horas  
        
- Configuração da lista de preços no projeto A:

    - **Nome**: preços de venda no Reino Unido 2016 
    - **Unidade de tempo predefinida**: Dia 
    - **Moeda**: GBP

| Função      | Grupo de unidades | Unidade | Unidade organizacional | Preço   |
|-----------|------------|------|---------------------|---------|
| Programador | Tempo       | Dia  | Contoso UK          | 800 GBP |

### <a name="time-entry"></a>Entrada de hora

A tabela seguinte mostra a transação do lado das vendas resultante criada pelo PSA para um projeto de três horas.


| Projeto   | Tarefa    | Função      | Quantidade | Unidade  | Preço unitário | Valor de vendas não faturadas |
|-----------|---------|-----------|----------|-------|------------|-----------------------|
| Projeto A | Estrutura  | Programador | 3        | Hour  | 100 GBP    | 300 GBP               |

## <a name="time-unit-faq"></a>FAQ sobre unidades de tempo

### <a name="does-psa-convert-to-different-units-in-the-case-of-expenses"></a>O PSA é convertido em unidades diferentes no caso das despesas?
Não. A conversão de unidades só funciona para o tempo. Quanto às despesas, se o sistema não conseguir encontrar um preço para a combinação das categorias e da unidade de despesa, o preço é definido como 0,00 por predefinição.

### <a name="why-does-psa-convert-time-units"></a>Por que é que o PSA converte unidades de tempo?
Em alguns países ou regiões, existe um requisito legal de que as taxas de faturação sejam configuradas em dias. A negociação e o desconto de preços durante o ciclo de criação de propostas são realizados utilizando taxas diárias para cada função faturável. A estimativa de agendamento e a entrada de tempo são efetuadas em horas. Para suportar esta diferença nas unidades de tempo, o PSA converte as unidades de tempo.

### <a name="can-time-units-be-changed-on-project-estimates"></a>As unidades de tempo podem ser alteradas nas estimativas de projeto?
Não. Atualmente, a estimativa de agendamento está restrita às horas e não pode ser alterada.

### <a name="can-units-and-unit-groups-be-edited-deleted-and-added"></a>As unidades e os grupos de unidades podem ser editados, eliminados e adicionados?
Sim. Com exceção do grupo de unidades **Tempo** e a unidade **Hora**, todas as unidades podem ser eliminadas ou editadas, e é possível adicionar novas unidades. No PSA, o grupo de unidades **Tempo** e a unidade **Hora** não podem ser eliminados. No entanto, podem ser atualizados com um texto traduzido para o campo **Nome**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]