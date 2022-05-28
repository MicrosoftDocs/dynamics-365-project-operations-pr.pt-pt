---
title: Criar e confirmar Diários de correção
description: Este tópico fornece informações sobre como criar e confirmar um diário de correção.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: c15db854e3d130150ad7afc707a126b37c57f62d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582817"
---
# <a name="create-and-confirm-correction-journals"></a>Criar e confirmar Diários de correção

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

Ocasionalmente, é possível que uma entrada de tempo ou despesas seja inserida incorretamente. Por exemplo, um consultor pode selecionar a data errada quando cria uma entrada de tempo ou pode selecionar o projeto errado quando introduz uma despesa. Se um consultor não conseguir atualizar as entradas submetidas, um administrador de backend pode corrigir diretamente os valores reais de um projeto.

## <a name="correct-approved-time-entries"></a>Corrigir entradas de tempo aprovadas     

Conclua os passos seguintes para corrigir entradas individuais ou múltiplas para um projeto.

1. Na área **Vendas**, selecione **Transações** e selecione **Tempo Aprovado**. 

2. Na lista **Tempo Aprovado**, localize e selecione uma ou mais entradas de tempo aprovadas para correção. Pode utilizar o filtro para localizar as entradas relacionadas. Por exemplo, poderá filtrar por um ID de projeto e selecionar todas as entradas de tempo aprovadas com esse ID de projeto.

3. Selecione **Entradas corretas**. É criado automaticamente um novo diário de correções, com o tipo atribuído de **Correção de Hora**. As entradas selecionadas são adicionadas ao diário. 

4. Na página **Novo Diário**, introduza uma **Descrição** para o diário de correções e selecione o separador **Correções de Entrada de Hora**.  

5. Na secção **Novos Valores para Entradas de Hora**, atualize os campos com as informações corretas, conforme seja necessário. Por exemplo, poderá alterar o projeto atribuído ou o recurso reservável.

6. Selecione **Pré-visualizar**. Na caixa de diálogo, selecione **OK**. No separador **Linhas do diário**, pode ver uma lista dos valores reais originais que estão relacionados com as entradas de tempo selecionadas que foram revertidas e as linhas correspondentes corrigidas que foram criadas. Se forem necessárias correções adicionais, repita os passos 5 e 6. 

    > [!NOTE]
    > Todos os valores reais corrigidos terão os mesmos valores selecionados na secção **Novos Valores para Entradas de Hora**.

7. Se as correções aparecerem conforme esperado, selecione **Confirmar**. Na caixa de diálogo, selecione **OK**.

8. Regresse à área **Vendas**, selecione **Projetos** e, em seguida, abra o projeto para o qual acabou de atualizar as entradas de hora. 

9. Na página **Projetos**, no separador **Valores Reais**, veja as alterações que efetuou. 

    > [!NOTE]
    > Se o separador **Valores Reais** não for visível, selecione **Relacionados** > **Valores Reais**.  

10. Na lista **Vista Associada de Valor Real**, poderá ver que as entradas de tempo originais que foram revertidas continuam a ser listadas, tal como são as entradas de tempo corrigidas correspondentes. 

 
## <a name="correct-approved-expense-entries"></a>Corrigir entradas de despesa aprovadas

Conclua os seguintes passos para corrigir uma ou mais entradas de despesa. 

1. Na área **Vendas**, no painel de navegação esquerdo, em **Transações**, selecione **Despesas Aprovadas**.

2. Na lista **Despesas Aprovadas**, selecione o projeto que pretende corrigir e selecione **Entradas corretas**. Será criado automaticamente um novo diário de correções, com o tipo atribuído de **Correção de Despesa**. 

3. Na página **Novo Diário**, introduza uma **Descrição** para a correção e, no separador **Correção de Despesa**, na secção **Novos Valores para Despesas**, selecione os campos de dados que pretende corrigir para os itens de despesa selecionados. Por exemplo, pode atribuir a despesa a outro **Projeto** ou corrigir a **Categoria de Despesa**, **Data da Despesa** ou **Recurso Reservável**.

4. Selecione **Pré-visualizar**. Na caixa de diálogo, selecione **OK**. 

5. Verifique as correções no separador **Linhas do diário**. Pode ver uma lista dos valores reais originais que estão relacionados com as entradas de despesa selecionadas que foram revertidas e as linhas correspondentes corrigidas que foram criadas.

6. Se os valores corrigidos aparecerem conforme esperado, selecione **Confirmar**. Na caixa de diálogo, selecione **OK**. Se os valores não forem mostrados conforme esperado, selecione **Cancelar** para voltar à lista **Despesas Aprovadas**. Repita os passos 2 a 5. 

7. Depois de confirmar o diário de correção, regresse ao projeto ou projetos que atualizou para ver as alterações.

8. Na página do projeto, no separador **Valores reais**, reveja a lista **Vista Associada Real**. São listadas as entradas originais e as entradas corrigidas.


## <a name="correct-approved-material-usage-logs"></a>Corrigir registos de utilização de materiais aprovados

Conclua os seguintes passos para corrigir uma ou mais entradas do registo de utilização de material.

1. Na área **Vendas**, no painel de navegação esquerdo, por baixo de **Transações**, selecione **Valores Reais**.

2. Na lista **Valores Reais**, utilize filtros de coluna para selecionar a classe de transação **Material**, para que apenas os valores reais para materiais sejam apresentados. Utilize outros filtros de coluna para limitar ainda mais os valores reais apresentados. Depois de encontrar o conjunto pretendido de valores reais, selecione os valores reais e, em seguida, selecione **Corrigir entradas**. É criado automaticamente um novo diário de correção e é atribuído o tipo de **Correção de material**.

3. Na página **Novo diário**, no campo **Descrição**, introduza uma descrição para a correção. Em seguida, no separador **Correção de materiais**, na secção **Novos valores para materiais**, selecione os campos de dados a corrigir para as linhas de material selecionadas. Por exemplo, pode atribuir o material a outro projeto ou corrigir o produto, a data de material ou o subcontrato.

4. Selecione **Pré-visualizar**. Em seguida, na caixa de diálogo, selecione **OK**.

5. No separador **Linhas do diário**, verifique as correções. Pode ver uma lista dos valores reais originais relacionados com as entradas de material selecionadas que foram revertidas e as linhas correspondentes corrigidas que foram criadas.

6. Se os valores corrigidos aparecerem conforme esperado, selecione **Confirmar**. Em seguida, na caixa de diálogo, selecione **OK**. Se os valores não forem os esperados, selecione **Cancelar** para regressar à lista **Valores Reais**. Em seguida, repita os passos 2 a 5.

7. Depois de confirmar o diário de correção, regresse ao projeto ou projetos que atualizou para ver as alterações.

8. Na página do projeto, no separador **Valores reais**, reveja a lista **Vista Associada Real**. São listadas as entradas originais e as entradas corrigidas.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
