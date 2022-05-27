---
title: Colocar em lista as despesas
description: Este tópico explica como colocar em lista as despesas usando a área de trabalho de Despesas reinventada.
author: suvaidya
ms.date: 12/16/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 34b11c6bd8be729957973a60fccccc2dd32c2669
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574536"
---
# <a name="expense-itemization"></a>Colocar em lista as despesas

[!include [banner](../includes/banner.md)]

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

As organizações exigem frequentemente que os colaboradores forneçam uma discriminação detalhada das despesas incorridas durante as viagens. Por exemplo, um folio de hotel pode conter várias linhas em lista para a taxa de quarto, imposto, estacionamento e outras despesas diversas incorridas por dia durante a duração da estadia. Ou uma despesa de refeição pode requerer que forneça uma discriminação mais granular para o pequeno-almoço, almoço ou jantar. Quaisquer que sejam as necessidades da organização, cada categoria de despesas pode ser configurada para refletir as subcategorias ou os itens de linha que compõem uma despesa. Embora a colocação em lista de itens tenha sido sempre suportada na **Gestão de despesas**, a área de trabalho **Despesas reinventadas** permite uma colocação em lista de itens mais eficiente quando a funcionalidade **Capacidade de colocar em lista de itens despesas recorrentes rapidamente** está ativada.  

## <a name="enable-quick-itemization"></a>Ativar colocação em lista de itens rápida 

Pode utilizar a funcionalidade **Capacidade de colocar em lista de itens despesas recorrentes rapidamente** para colocar em lista de itens as despesas recorrentes rapidamente evitando a necessidade de introduzir as despesas diárias de cada vez durante a duração da estadia. Complete os seguintes passos para ativar a colocação em lista de itens rápida.

1. Vá à área de trabalho **Gestão de Funcionalidades** e, na lista de funcionalidades, localize e selecione **Relatórios de Despesas Reinventados**. 
2. Selecione **Ativar agora**. 
3. Na lista de funcionalidades, localize e selecione **Capacidade de colocar em lista de itens despesas recorrentes rapidamente**.
4. Selecione **Ativar agora**. 

## <a name="itemization-grid"></a>Grelha de colocação em lista de itens 

Se uma categoria de despesas tiver subcategorias ou componentes diferentes que compõem essa despesa, pode ser colocado em lista de itens. Para colocar em lista de itens uma despesa, selecione a linha de despesas no relatório de despesas e, no painel **Detalhes de despesas**, selecione **Ações** > **Colocar em lista de itens**. O controlo de deslize **Colocação em lista de itens** revela uma grelha com campos. A tabela que se segue fornece um exemplo de cada campo na grelha e de como o campo é composto no relatório de despesas. 

|     Campo          |     Description                                                                                  |     Exemplo              |
|--------------------|--------------------------------------------------------------------------------------------------|--------------------------|
|     Subcategoria    |     A lista de subcategorias configuradas sob o tipo de categoria de despesas, **Hotel**.             |     Tarifa diária do quarto      |
|     Data de início     |     A data em que o item de despesa foi inicialmente incorrido.                                           |     13/09/2021           |
|     Tarifa Diária     |     O montante incorrido para o item de despesa.                                                    |     200                  |
|     Quantidade       |     O número de vezes que o custo é repetido durante um período contínuo.                       |     3                    |

![Colocar em lista as despesas.](media/Itemization%20screen%201.png)

Quando guardar uma lista de itens, verá uma linha individual de lista de itens para a quantidade especificada na grelha de lista de itens. Cada linha começa na data especificada na grelha.

![Relatório colocado em lista de itens.](media/Itemization%20screen%202.png)

