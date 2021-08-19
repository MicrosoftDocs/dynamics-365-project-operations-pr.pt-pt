---
title: Correções em massa dos valores reais criados pelas entradas de tempo e despesa aprovadas
description: Este tópico explica como um administrador pode fazer correções individuais ou em massa às entradas de tempo ou despesa aprovadas anteriormente se a faturação não for concluída.
author: rumant
ms.date: 04/02/2020
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
search.app:
- ProjectOperations
ms.openlocfilehash: 88706946e5c5c59be996640f4c7b37e958c1cf1d9fd14c72c0c6dc854a77dab4
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6995415"
---
# <a name="bulk-corrections-of-actuals-created-by-approved-time-and-expense-entries"></a>Correções em massa dos valores reais criados pelas entradas de tempo e despesa aprovadas

[!include [banner](../includes/psa-now-project-operations.md)]

Ocasionalmente, uma entrada de hora ou despesa pode ser introduzida incorretamente. Por exemplo, um consultor pode selecionar a data errada ao criar uma entrada de hora ou transpor os números ao introduzir uma despesa. Se um consultor não conseguir efetuar as atualizações às entradas submetidas, um administrador pode corrigir diretamente a entrada para um projeto.

Para concluir os procedimentos neste tópico, precisará de permissões de Administrador.

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

Por exemplo, no gráfico seguinte existem dois itens com a quantidade de 8 com débitos listados na coluna Montante. Além disso, existem dois itens com a quantidade -8 que mostram montantes creditados na coluna Montante. Estas correções repõem a quantidade para zero.

![Lista de vistas associadas de valor real.](https://github.com/MicrosoftDocs/dynamics-365-customer-engagement-pr/blob/bulk-corrections-actuals-created-by-approved-time-expense-entries.md/time-actuals.png)
 
## <a name="correct-approved-expense-entries"></a>Corrigir entradas de despesa aprovadas

Conclua os seguintes passos para corrigir uma ou mais entradas de despesa. 

1. Na área **Vendas**, no painel de navegação esquerdo, em **Transações**, selecione **Despesas Aprovadas**.

2. Na lista **Despesas Aprovadas**, selecione o projeto que pretende corrigir e selecione **Entradas corretas**. Será criado automaticamente um novo diário de correções, com o tipo atribuído de **Correção de Despesa**. 

3. Na página **Novo Diário**, introduza uma **Descrição** para a correção e, no separador **Correção de Despesa**, na secção **Novos Valores para Despesas**, selecione os campos de dados que pretende corrigir para os itens de despesa selecionados. Por exemplo, pode atribuir a despesa a outro **Projeto** ou corrigir a **Categoria de Despesa**, **Data da Despesa** ou **Recurso Reservável**.

4. Selecione **Pré-visualizar**. Na caixa de diálogo, selecione **OK**. 

5. Verifique as correções no separador **Linhas do diário**. Pode ver uma lista dos valores reais originais que estão relacionados com as entradas de despesa selecionadas que foram revertidas e as linhas correspondentes corrigidas que foram criadas.

6. Se os valores corrigidos aparecerem conforme esperado, selecione **Confirmar**. Na caixa de diálogo, selecione **OK**. Se os valores não forem mostrados conforme esperado, selecione **Cancelar** para voltar à lista **Despesas Aprovadas**. Repita os passos 2 a 5. 

> [!NOTE]
> Os valores reais corrigidos terão os mesmos valores selecionados na secção **Novos Valores para Despesas**.

7. Depois de confirmar o diário de correção, volte ao projeto ou projetos atualizados para ver as alterações.  

8. Na página do projeto, no separador **Valores Reais**, reveja a **Vista Associada de Valor Real**. São listadas as entradas originais e as entradas corrigidas. O gráfico seguinte mostra os montantes de entrada de despesa originais e os montantes de entrada de despesa corrigidos correspondentes. 

![Valores reais de despesa.](https://user-images.githubusercontent.com/60806505/77122219-4cd52900-69fa-11ea-8349-ccd2ffebf640.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]