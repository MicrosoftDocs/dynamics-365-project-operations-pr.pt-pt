---
title: Gerir estimativas de receitas
description: Este tópico fornece informações sobre como gerir e trabalhar com estimativas de receitas para projetos.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 98df0301eaa8e9f8e9cd51fc5714254ae3bbc83d
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531519"
---
# <a name="manage-revenue-estimates"></a>Gerir estimativas de receitas

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

É possível criar, calcular, publicar, reverter ou eliminar estimativas de receitas. Pode fazê-lo manualmente ou utilizando um processo periódico. Este tópico fornece informações sobre como gerir e trabalhar com estimativas de receitas para projetos.

### <a name="manage-revenue-estimates-manually"></a>Gerir estimativas de receitas manualmente

No projeto de estimativa de receitas de preço fixo ou na página **Inquérito de estimativa** (**Gestão de projetos e contabilística** > **Relatórios e inquéritos** > **Estimativas de inquéritos e relatórios**), selecione **Estimativas**.

### <a name="manage-revenue-estimates-using-a-periodic-process"></a>Gerir estimativas de receitas utilizando um processo periódico

Vá a **Gestão de projetos e contabilística** > **Periódicas** > **Estimativas** e selecione o processo correspondente.

## <a name="create-a-revenue-estimate"></a>Criar uma estimativa de receitas

Conclua os seguintes passos para criar uma estimativa de receita. 

1. Vá a **Gestão de projetos e contabilística** > **Periódica** > **Estimativas**.
2. Selecione **Novo**. Na página **Criação de estimativa**, selecione os seguintes parâmetros:

   - **Código de período**: este código determina a frequência com que as estimativas são publicadas.
   - **Data de estimativa**: a data em que a estimativa é processada.
   - **Contínua**: selecione esta caixa de verificação para criar estimativas apenas se as estimativas forem publicadas no período anterior, ou se a estimativa for a primeira estimativa que foi criada. Se esta não for selecionada, as estimativas são criadas mesmo que as estimativas não tenham sido publicadas no período anterior.
   - **Método de custo para conclusão**: defina como estimar o restante trabalho do projeto. Para obter mais informações, consulte [Métodos de custo para conclusão](cost-complete-methods.md).
   - **Método de conclusão**: selecione um método de conclusão a partir das seguintes opções:
     - **Automático**: a percentagem de conclusão é calculada automaticamente e com base nas linhas de custo incluídas no cálculo. O modelo de custo define as linhas de custo que estão incluídas.
     - **Manual**: a percentagem de conclusão é igual à percentagem de conclusão da última estimativa. Após a criação da estimativa, pode alterar o **Cálculo manual** na página **Estimativas**.
     - **Modelo Do custo**: uma combinação dos métodos automáticos e manuais. Esta opção é definida automaticamente ou manualmente, dependendo do valor predefinido no modelo de custos.
   - **Modelo de previsão**: selecione um modelo de previsão para a estimativa.
   - **Imprimir lista de estimativas**: crie e mostre uma lista de estimativas. A lista contém o estado da função atual. Pode imprimir qualquer aviso sobre a estimativa do relatório. As seguintes condições fazem com que as advertências apareçam na lista de estimativas:
     - Uma percentagem de conclusão superior a 100 por cento.
     - Uma percentagem de conclusão inferior a zero por cento.
     - Um montante negativo na coluna **Para concluir**.
     - Uma estimativa sem o valor do contrato correspondente.
     - Uma estimativa sem estimativa de custos anexada.
   - **Mostrar Registo de Informações**: selecione esta opção para receber uma mensagem que contenha informações sobre os projetos de estimativa que foram processados quando o trabalho foi executado.


## <a name="post-wip-or-accruals"></a>Pós-WIP ou acréscimos

Após a avaliação das estimativas, estas são mantidas, diminuídas ou aumentadas. Em seguida, pode publicar o WIP quando trabalhar com o princípio de avaliação do **Contrato concluído**, ou publicar os acréscimos quando trabalhar com o princípio de avaliação de **Percentagem de conclusão**.
  
O estado do período de estimativa muda de **Criada** para **Publicada**.

## <a name="reverse-wip-or-accruals"></a>Reverter WIP ou acréscimos

Use a opção de reversão para creditar WIP ou acréscimos já publicados e, em seguida, crie estimativas para o período.

> [!NOTE]
> Para inverter um período que se encontra entre outros períodos, reverta os períodos de estimativa necessários e, em seguida, volte a publicá-los. Como todos os períodos subsequentes dependem das estimativas do período anterior, não ignore quaisquer períodos.

## <a name="eliminate-the-estimate-project-and-finish-the-project"></a>Elimine o projeto de estimativa e termine o projeto

O passo final no processo de estimativa é eliminar o projeto de estimativa e terminar o projeto de preço fixo quando a percentagem de conclusão chega aos 100 por cento.

O seguinte ocorre quando executa a eliminação:

- Para um projeto de preço fixo com contrato concluído, os valores WIP são limpos das contas de saldo e publica as contas de lucro e perda.
- Para um projeto de preço fixo com uma percentagem de conclusão, os acréscimos são retirados das contas de lucro e perda.

A estimativa altera o estado para **Eliminado**.

> [!NOTE]
> Em casos especiais, a percentagem pode estender-se para além dos 100 por cento. Quando isso acontecer, reduza a percentagem de conclusão utilizando o **Método Definir custo para conclusão para zero** para chegar aos 100 por cento.

## <a name="reverse-elimination"></a>Reverter eliminação

1. Aceda a **Gestão de projetos e contabilística** > **Periódica** > **Estimativas** > **Reverter eliminação**. 
2. No Painel de Ação, no separador **Processo**, no grupo **Manter**, selecione **Estimativa**. 
3. Selecione **Reverter eliminação**.

Utilize esta página para reverter todas as eliminações com uma data de estimativa especificada e com um estado de estimativa de **Eliminada**. O estado de transação muda depois de selecionar os campos apropriados.

Isto também altera automaticamente o estado do projeto para **Em processo** se a fase do projeto estiver definida para Concluída. O estado de estimativa do período de projeto volta a **Publicado**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]