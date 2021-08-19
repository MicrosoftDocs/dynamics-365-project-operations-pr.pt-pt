---
title: Configurar quilometragem utilizando níveis de taxa de quilometragem
description: Este tópico fornece informações sobre taxas de quilometragem e níveis de taxa de quilometragem.
author: suvaidya
ms.date: 05/20/2021
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: a44d32358a9e88824efc5452b2b5493ac8b97c7f
ms.sourcegitcommit: 18f99fbceccadd4b3e75875e1c5bcdd3e59ce206
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 05/20/2021
ms.locfileid: "6083685"
---
# <a name="set-up-mileage-using-mileage-rate-tiers"></a>Configurar quilometragem utilizando níveis de taxa de quilometragem

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

Quando uma despesa é comunicada e a categoria de despesas selecionada é **Quilometragem**, o montante dessa linha de despesas é calculado de acordo com o montante da *taxa por quilometragem*. Este montante é determinado utilizando níveis de quilometragem definidos ou, se não forem configurados níveis de taxa de quilometragem, seguindo uma taxa padrão de quilometragem. 

Os níveis de taxa de quilometragem podem ser configurados através de **Gestão de Despesas** > **Configuração** > **Geral** > **Categoria de despesas** > **Quilometragem** > **Configurar categoria**.

Depois de atualizar para a versão 10.0.18, se a sua organização utilizar a categoria de despesas de quilometragem, considere ativar a funcionalidade de quilometragem depois de rever as alterações de design abaixo. 

O novo design dos níveis de taxa de quilometragem tem impacto na forma como o valor no campo **Quantidade** é processado. Antes da versão 10.0.18, o valor no campo **Quantidade** foi considerado o limite inferior. Quando a acumulação cruzou esse valor, a taxa correspondente foi utilizada.  A partir de 10.0.18, o valor no campo **Quantidade** é considerado o limite superior. A taxa correspondente é utilizada quando a acumulação de quilometragem é inferior ao valor no campo **Quantidade**.  O novo modelo para níveis de quilometragem ajuda com consistência nos níveis de quilometragem e uma melhor capacidade de utilização.   

Todos os relatórios de despesas aprovados serão recalculados durante a publicação de acordo com o novo design.

## <a name="example"></a>Exemplo
 
### <a name="before-version-10018"></a>Antes da versão 10.0.18
Com dois níveis de taxa de quilometragem, o campo **Quantidade** em cada nível representa o limite de quilometragem mais baixo. Atualmente, o nível um tem um valor de zero (0) e uma taxa de 0,45, e o nível dois tem um valor de 1000 e uma taxa de 0,25. Se as milhas ou quilómetros acumulados cruzarem o valor no campo, a taxa relacionada é utilizada. Se não houver nenhuma linha com quantidade zero, o sistema utiliza a taxa de quilometragem definida na Gestão de despesas. 
 
Se um colaborador submeter um relatório de despesas com 1.500 milhas, as duas linhas de quilometragem no relatório de despesas publicado seriam: 1000 (taxa 0,45) + 500 (taxa 0,25) = 575,00.

### <a name="after-version-10018"></a>Após a versão 10.0.18
Na 10.0.18, o campo **Quantidade** em cada nível representa o limite superior do nível. Atualmente, o nível um tem um valor de 999 e uma taxa de 0,45, e o nível dois tem um valor de 999.999.999,00 e uma taxa de 0,25. Se as milhas ou quilómetros acumulados cruzarem o valor no campo **Quantidade**, a taxa relacionada é utilizada. Se todos os limites superiores forem excedidos, o sistema utiliza a taxa de quilometragem definida na Gestão de despesas. 
 
Para calcular corretamente o mesmo cenário, o nível configurado deve ser alterado. O campo **Quantidade** no nível um tem um valor de 999,00 e um valor de 999.999.999,00 no nível dois. Se um colaborador exceder a quantidade total de milhas ou quilómetros no nível um, o sistema utiliza a taxa de quilometragem definida na Gestão de despesas. 
  
Se um colaborador submeter um relatório de despesas com 1.500 milhas, as duas linhas de quilometragem no relatório de despesas publicado seriam: 1000 (taxa 0,45) + 500 (taxa 0,25) = 575

## <a name="enable-the-mileage-amount-calculation-for-multiple-mileage-tiers-with-same-rate-feature"></a>Ativar a funcionalidade Cálculo da quantidade de Quilometragem para vários níveis de quilometragem com a mesma taxa

A funcionalidade **Cálculo da quantidade de Quilometragem para vários níveis de quilometragem com a mesma taxa** melhora o cálculo da taxa de quilometragem. Complete os seguintes passos para ativar esta funcionalidade.

1. Aceda a **Áreas de Trabalho** > **Gestão de Funcionalidades**. 
2. Na lista, localize e selecione **Cálculo da quantidade de Quilometragem para vários níveis de quilometragem com a mesma taxa** e, em seguida, selecione **Ativar agora**.

Depois de ativar a funcionalidade, reponha os níveis de quilometragem para refletir corretamente o valor do campo **Quantidade**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]