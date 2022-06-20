---
title: Configurar modelos de custos
description: Este artigo fornece informações sobre como criar e utilizar modelos de custo no Project Operations.
author: sigitac
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: ffb45d46cf1305fffd5933f4c10b169bf802046d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918418"
---
# <a name="set-up-cost-templates"></a>Configurar modelos de custos

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_


Este artigo fornece informações sobre como criar e utilizar modelos de custo no Project Operations. Um modelo de custos determina:

- As categorias de projetos para previsão e transações efetivas devem ser incluídas numa percentagem do cálculo da conclusão do projeto. O valor por cento completo é então usado para calcular a quantidade de receitas reconhecidas.
- Se a percentagem de conclusão pode ser modificada se for calculada automaticamente.
- Se a percentagem de conclusão é calculada com base em montantes ou unidades.

## <a name="cost-template-example"></a>Exemplo de modelo de custos

Está a trabalhar num projeto de design de site para um cliente no qual cobra uma taxa fixa de 10.000 USD. Previu que levará 100 horas (5.000 USD) para concluir o projeto. Também prevê dois bilhetes de avião e quatro noites num hotel para viagens ao site do cliente (1.800 USD). Isto resulta num custo total previsto de 6.800 USD.

Quando executa o processo de reconhecimento de receitas de preço fixo para criar uma estimativa no final do mês, descobre que trabalhou 35 horas no projeto. Isto ainda não inclui voos ou custos do hotel. Também mandou um assistente fazer cinco horas de pesquisa para o projeto com um custo de 100 USD, que não tinha planeado.

Ao calcular o valor de percentagem de conclusão deste projeto, tem as seguintes escolhas a fazer:

- Deseja incluir todos os custos (horas e despesas) ou apenas horas?
- Deseja incluir todos as horas ou apenas horas planeadas?
- Deseja calcular a percentagem de conclusão com base no custo do dólar das horas planeadas (5.000 USD) ou apenas no número de horas (100)?

As suas respostas a estas perguntas determinam as opções que definiu no modelo de custos e nas categorias que seleciona nas linhas do modelo de custos.

A tabela a seguir ilustra os resultados de diferentes métodos de cálculo do valor de percentagem de conclusão para este cenário.

| Conclusão baseada em | Custo do dólar ou unidades | Percentagem de conclusão | Cálculo |
| --- | --- | --- | --- |
| Todas as horas, sem despesas | Custo do dólar | 37% 35 x 50 USD + 100 USD = 1.850 USD 1.850 USD/5.000 USD |
| Todas as horas, sem despesas | Unidades | 40% | 40 horas/100 horas (incluindo cinco horas não planeadas) |
| Horas planeadas, sem despesas | Custo do dólar ou unidade | 35% | 35/100 horas ou 35 x 50/5.000 USD |
| Todas as horas e despesas | Custo do dólar | 27,2% | 1.850 USD/6.800 USD |

Decidir qual a abordagem a tomar para criar um modelo de custos pode depender de várias considerações:

- Se incluir horas não planeadas no modelo de custos, arrisca-se a chegar a 100 por cento antes de o projeto estar terminado. Isto porque as horas reais serão maiores do que as horas planeadas. Se utilizar um dos dois primeiros métodos listados na tabela, deve alterar o plano (unidades previstas) quando tiver conhecimento de desvios. Neste caso, iria adicionar ou subtrair horas com base no seu conhecimento do que é necessário para terminar o projeto. Se o projeto necessitar de mais 65 horas para ser concluído, adicionará cinco horas ao plano para um total de 105. Se souber que o seu assistente fará mais cinco horas de pesquisa, o total passará a ser de 110 horas.
- Se utilizar o terceiro método listado na tabela, apenas atualizará as horas planeadas para o seu tempo para manter preciso o cálculo de percentagem de conclusão. A sua rentabilidade mudará quando as horas não planeadas forem registadas, mas permanecerá numa trajetória de percentagem de conclusão conhecida.
- Se utilizar o quarto método listado na tabela, o risco é que as despesas ocorram em momentos irregulares e possam não se refletir no seu progresso de conclusão. Portanto, se as despesas forem incluídas, podem fazer com que a sua percentagem de conclusão oscile mais do que é desejável. Por exemplo, como ainda não apanhou um voo, a sua percentagem de conclusão era de 27 por cento em vez de 35 por cento ou 37 por cento se baseasse o cálculo apenas no tempo. Se tivesse feito uma viagem por duas noites e previsto com precisão os custos do seu voo e hotel, a percentagem de conclusão teria sido de 40,4 por cento (1850 USD para trabalho e 900 USD para despesas = 2750 USD/6800 USD = 40,4 por cento). Portanto, incorrer nas despesas de apenas uma viagem de avião mudaria a percentagem completa de 27 por cento para 40 por cento.

## <a name="create-cost-templates"></a>Criar modelos de custos
Para criar modelos de custos, siga estes passos:

1. Para aceder a modelos de custo, no ambiente Dynamics 365 Finance, aceda a **Gestão de projetos e contabilidade** > **Configuração** > **Estimativas** > **Modelo de custo**.
2. Selecione **Novo** para criar um novo modelo de custos. Introduza um nome e descrição.
3. Forneça o ID de linha de custo para cada tipo de transação.
4. Selecione um método de conclusão predefinido:

  - **Automático**: a percentagem de conclusão é calculada automaticamente num projeto. Não é possível alterar o valor resultante.
  - **Manual**: a percentagem de conclusão é calculada automaticamente num projeto. É possível alterar o valor resultante.

  > [!NOTE]
  > Para cálculos manuais, a percentagem de conclusão é mantida em **Cálculo manual** no separador **Geral** na página **Estimativa**.

5. Em **Conclusão com base em**, selecione um dos seguintes valores:

  - **Montante**: o montante em moeda contabilística calcula a percentagem de conclusão.
  - **Unidade**: a quantidade calcula a percentagem de conclusão.
  - **Linha reta**: o sistema calcula a percentagem de conclusão numa base proporcional utilizando as datas de início e de fim do projeto para determinar a duração do projeto.

6. Selecione **Linhas de custo** para rever as linhas de custo do modelo de custos. É necessária, pelo menos, uma linha de custos para cada tipo de transação. No entanto, pode criar várias linhas de custo para os mesmos tipos de transação e definir os atributos desejados para estas linhas.
7. No separador **Categorias**, selecione as categorias de projeto a incluir na linha do modelo de custos.
8. No separador **Geral**, selecione se esta linha será incluída na percentagem de cálculo de conclusão.
9. Selecione o custo para completar o método a utilizar no cálculo da percentagem de conclusão.


[!INCLUDE[footer-include](../includes/footer-banner.md)]