---
title: Definições manuais de preço com data efetiva
description: Este artigo explica como configurar as definições manuais de preços para preços específicos na lista de preços.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 41af5176c0809c9621fc0fa946a04492da7d152b
ms.sourcegitcommit: 37293b0b28f072deafc00112ddbbea91c48a7802
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 09/08/2022
ms.locfileid: "9445977"
---
# <a name="date-effective-price-overrides"></a>Definições manuais de preço com data efetiva 

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

As *Definições manuais de preço com data efetiva* oferecem uma forma de definir manualemnte ou alterar preços específicos na lista de preços. Por exemplo, tem uma lista de preços standar que entrou cujo período em vigor é de 1 de janeiro de 2022 a 31 de dezembro de 2022. Esta lista de preços tem preços para muitas funções. O preço que está configurado para a função **Técnico de Rede** é de 100 dólares americanos (USD) por hora. Quando um técnico de rede regista tempos entre 1 de janeiro de 2022 e 31 de dezembro de 2022, a hora é cotada a 100 USD. A 1 de outubro de 2022, deve ajustar o preço *apenas* para a função **Técnico de Rede**, de 100 USD à hora para 110 USD à hora. A funcionalidade **Definições manuais de preço com data efetiva** permite-lhe configurar esta alteração como uma definição manual da linha por esse preço de função específico. Por conseguinte, não tem de copiar a lista de preços completa e alterar o preço apenas dessa linha.

## <a name="date-effective-price-overrides-for-labor-pricing"></a>Definições manuais de preço com data efetiva para preços de mão de obra

O processo de configuração das definições manuais de preço com data efetiva para tempo de mão de obra num projeto consiste em dois passos básicos.

1. Ative a funconalidade **Definições manuais de preços com data efetiva**.
1. Configure uma definição manual de preço com data efetiva.

### <a name="enable-the-date-effective-price-overrides-feature"></a>Ativar a funconalidade Definições manuais de preços com data efetiva

> [!NOTE]
> Depois de a funcionalidade **Definições manuais de preços com data efetiva** estar ativada, não pode ser desativada.

Para ativar a funcionalidade **Definições manuais de preços com data efetiva**, siga estes passos.

1. Aceda a **Definições** \> **Parâmetros**.
1. Abra o registo **Parâmetros**.
1. No Painel de Ações, no separador **Controlo de funcionalidades**, selecione **Ativar definições manuais de preços com data efetiva**.
1. Na caixa de diálogo de confirmação, selecione **OK**.
1. Depois de alguns minutos, atualize o browser. As capacidades de definições manuais de preços com data efetiva deve ficar disponível. Ficará a saber que estas capacidades foram ativadas se **Ativar definições manuais de preços com data efetiva** deixar de aparecer no Painel de Ações.

### <a name="set-up-a-date-effective-price-override"></a>Configure uma definição manual de preço com data efetiva

As definições manuais de preços com data efetiva podem ser configuradas nas listas de preços **Custo**, **Vendas** ou **Compra**.

> [!NOTE]
>O comportamento das **Definições manuais de preços com data efetiva** tem atualmente as seguintes limitações:
>
> - Apenas os preços das funções e as margens de lucros de preços de funções suportam a funcionalidade **Definições manuais de preços com data efetiva** no Project Operations.
> - Quando copia uma lista de preços utilizando a ação **Copiar** na página **Detalhes da lista de preços** e quando cria uma lista de preços do projeto a partir de uma lista de preços standard ou personalizada durante a criação de contratos, as Definições manuais de preços com data efetiva **não** são copiadas a partir da lista de preços de origem.

Para configurar uma definição manual de preços com data efetiva para um preço de função ou uma margem de lucro de preço de função, siga estes passos.

1. Abra a página para a lista de preços em que pretende configurar a definição manual de preços com data efetiva.
1. Selecione o separador **Preços da função**. Este separador lista todos os registos de **Preços da função** na lista de preços.
1. Selecione o registo **Preços da função** para o qual pretende configurar uma nova definição manual de preços com data efetiva e, em seguida, faça duplo toque (ou duplo clique) em **Preço da função** para abrir a página **Detalhes do preço da função**.
1. Selecione o separador **Definições manuais com data efetiva**. A grelha neste separador lista todas as definições manuais de preços com data efetiva para o registo de **Preço de função** selecionado.
1. Na barra de ferramentas acima da grelha, selecione **Nova substituição manual de preço de função**. O controlo de deslize **Nova definição manual de preço de função** abre.
1. Especifique a data a partir da qual entra em vigor, a unidade e o novo preço para a definição manual de preço. Em seguida, selecione **Guardar** e feche o formulário.

> [!NOTE]
> - Uma definição manual de preço com data efetiva para um preço de função ou margem de lucro de preço de função é aplicável à mesma combinação de valores de dimensão de preço que existem na linha de elemento principal **Preço da função** ou **Margem de lucro de preço da função**.
> - A data selecionada no campo **Em vigor a partir de** deve estar entre as datas efetivas da lista de preços principal. A definição manual de preços irá entrar em vigor na data selecionada no campo **Em vigor a partir de** e aplica-se até ao término da data de fim na lista de preços principal. Se configurar outra definição manual de preço com data efetiva para o mesmo preço de função, a primeira definição manual de preços entra em vigor na data selecionada no campo **Em vigor a partir de** e aplica-se até ao início da segunda definição manual.

## <a name="examples"></a>Exemplos

### <a name="example-1-determining-date-effectivity-for-a-role-price-that-has-role-price-overrides"></a>Exemplo 1: determinar a data de efetividade para um preço de função que tem definições manuais de preço da função

O exemplo que se segue mostra como a data de efetividade é determinada para um preço de função específico para o qual as definições manuais de preço estão configuradas.

**Lista de preços A: 1 de janeiro a 30 de junho**

*Preço da função*

| Preço da função | Unidade | Preço | Em vigor nos preços das transações a receber |
|---|---|---|---|
| Técnico de Rede | Hora | 100 | Este preço será utilizado em quaisquer transações em que a data da transação seja entre 1 de janeiro e 14 de março. |

*Definição manual do preço da função*

| Em vigor a partir de | Unidade | Preço | Em vigor nos preços das transações a receber |
|---|---|---|---|
| Março de 15 | Hora | 110 | Este preço será utilizado em quaisquer transações em que a data da transação seja entre 15 de março e 30 de março. |
| Abril de 1 | Hora | 120 | Este preço será utilizado em quaisquer transações em que a data da transação seja entre 1 de abril e 30 de junho. |

### <a name="example-2-determining-date-effectivity-for-a-role-price-markup-that-has-role-price-markup-overrides"></a>Exemplo 2: determinar a data de efetividade para uma margem de lucro de preço de função que tem definições manuais de margem de lucro de preço da função

O exemplo que se segue mostra como a data de efetividade é determinada para uma margem de lucro de preço de função específico para o qual as definições manuais de margem de lucro de preço estão configuradas.

**Lista de preços A: 1 de janeiro a 30 de junho**

*Preço da função*

| Preço da função | Horas de trabalho | Unidade | Preço | Em vigor nos preços das transações a receber |
|---|---|---|---|---|
| Técnico de rede | Normal | Hora | 100 | Este preço será utilizado em quaisquer transações em que a data da transação seja entre 1 de janeiro e 14 de março. |

*Margem de lucro do preço da função*

| Unidade organizacional | Horas de trabalho | % da margem de lucro |
|---|---|---|
| Contoso EUA | Horas Extraordinárias | 10% |

*Definição manual da margem de lucro do preço da função*

| Em vigor a partir de | Preço | Em vigor nos preços das transações a receber |
|---|---|---|
| Março de 15 | 20% | Esta percentagem de margem de lucro será utilizada em quaisquer transações em que a data da transação seja entre 15 de março e 30 de março. |
| Abril de 1 | 25% | Esta margem de lucro será utilizada em quaisquer transações em que a data da transação seja entre 1 de abril e 30 de junho. |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
