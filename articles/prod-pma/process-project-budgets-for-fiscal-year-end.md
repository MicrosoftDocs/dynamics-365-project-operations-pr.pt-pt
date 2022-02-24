---
title: Transferir orçamentos do projeto no final do ano fiscal
description: Este artigo fornece informações sobre como transferir os montantes orçamentais restantes para anos futuros e criar detalhes do registo orçamental.
author: Yowelle
manager: AnnBe
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 26e013ab99e9a0aeafe25916715ce0ee024df3f7
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4082537"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a>Transferir orçamentos do projeto no final do ano fiscal

[!include [banner](../includes/banner.md)]

Ao trabalhar num projeto com vários anos, poderá ter o orçamento restante no final do ano fiscal. Pode transferir os restantes montantes orçamentais para um ano futuro e criar detalhes do registo orçamental para os montantes nas contas gerais associadas. Antes de transpor os restantes montantes, reveja e analise os restantes montantes orçamentais.

## <a name="review-and-analyze-remaining-budget-amounts"></a>Rever e analisar os montantes orçamentais remanescentes

Complete as seguintes medidas para rever os montantes orçamentais do final do ano para projetos, mas não levar os montantes para a frente.

1. Vá a **Gestão de projetos e contabilística** > **Periódico** > **Orçamentos** > **Transpor orçamentos**. 
2. Na página **Processo de transposição do orçamento do projeto** no separador **Opções de final de ano**, verifique se **Montantes orçamentais de projeto restantes transpostos** não estão ativados.
3. No separador **Parâmetros**, no campo **Ano de orçamento do projeto**, selecione o ano fiscal para o qual pretende ver o restante montante orçamental. 
4. No campo **Abrir ano fiscal** para o qual pretende ver o restante montante orçamental. 
5. No campo **Do modelo de previsão**, selecione **Orçamento restante**. 
6. Para incluir projetos que satisfaçam os seus critérios selecionados e não tenham orçamento remanescente, selecione **Mostrar zero restantes**.  
7. No separador **Selecionar Orçamentos**, selecione **Obter todos os orçamentos** para carregar todos os orçamentos que correspondam aos critérios selecionados e, em seguida, selecione **Processar**. 
8. Para conceber uma consulta de base de dados que carregue um conjunto específico de orçamentos no painel, selecione **Obter orçamentos selecionados**.

Para obter mais informações sobre uma linha específica no painel, selecione a linha e, em seguida, selecione **Ver detalhes do orçamento** ou **Ver contas**.

## <a name="carry-forward-remaining-budget-amounts"></a>Transpor os restantes montantes orçamentais 

Quando processa os montantes orçamentais restantes, pode criar transações no livro razão geral para os montantes que está a transpor. Para criar transações gerais de livro razão, complete os passos na secção [Transpor os montantes orçamentais e criar transações gerais de livro razão](#carry-forward). 

> [!NOTE]
> Os montantes orçamentais que são transferidos para o modelo de previsão que é selecionado na página **Modelos de previsão** como o modelo de previsão a transpor.  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a>Transpor os montantes orçamentais e criar transações gerais de livro razão

1.  Selecione **Gestão de projetos e contabilística** > **Periódico** > **Orçamentos** > **Transpor orçamentos**. 
2. Na página **Processo de transposição do orçamento do projeto**, selecione **Final do Ano** e, em seguida, ative **Transpor montantes orçamentais restantes do projeto** e **Criar entradas de registo orçamental no livro razão**. 
3. No separador **Parâmetros**, no grupo de campos **Parâmetros do projeto**, selecione o seguinte:

   - **Ano orçamental do projeto**: selecione o início do ano fiscal para o qual pretende ver os restantes montantes orçamentais. 
   - **Lucros e perdas**: Criar transações de lucros e perdas no livro razão geral. 
   -  **WIP**: Criar transações de Trabalho em Progresso (WIP) no livro razão geral.
   -  **Folha de pagamentos**: Criar transações de atribuição de folha de pagamentos no livro razão geral. 

5. No grupo de campos **Livro razão geral**, forneça as seguintes informações: 

   - No campo **Abrir ano fiscal**, selecione o ano fiscal para o qual pretende transferir os restantes montantes orçamentais para os projetos. O valor predefinido é de um ano após o valor no campo **Ano orçamental do projeto**.
   -  No campo **Transpor período**, selecione o período para o qual pretende criar os detalhes do registo orçamental no livro razão. Este é tipicamente o primeiro período na ano fiscal a abrir.

6. No grupo de campos **Copiar de/para**, forneça as seguintes informações:

   - No campo **Do modelo de previsão**, selecione o modelo de previsão do orçamento do projeto associado aos restantes montantes orçamentais que pretende transferir para os projetos. 
   - No campo **Para modelo orçamental do livro razão**, selecione o modelo orçamental do livro razão associado aos montantes orçamentais que pretende transferir para o livro razão geral. 
   -  Selecione **Transferir a moeda de venda** para usar a moeda de venda do projeto para as transações do livro razão geral que são criadas quando transfere os montantes orçamentais para os projetos. Quando a opção não é selecionada, as transações utilizam a moeda contabilística. 
   -  Selecione **Mostrar zero restantes** para incluir projetos que não têm montantes orçamentais restantes, mas satisfaça os outros critérios que seleciona nos projetos apresentados no painel inferior.

7. No separador **Selecionar Orçamentos**, selecione **Obter todos os orçamentos** para carregar todos os orçamentos que correspondam aos critérios que selecionou. Se preferir conceber uma consulta de base de dados que carregue um conjunto específico de orçamentos de projeto no painel, selecione **Obter orçamentos selecionados**.
8. Para cada projeto que pretende processar, selecione a opção no início da linha para o projeto.

    > [!TIP]
    > Para selecionar todos ou a maioria dos projetos, selecione a marca de verificação no canto superior esquerdo. Para excluir o processamento de qualquer projeto, limpe a marca de verificação para esse projeto.

9. Para transferir os restantes montantes orçamentais para os projetos selecionados para o ano fiscal selecionado e criar detalhes do registo orçamental no livro razão geral, selecione **Processar**.

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a>Transpor os montantes orçamentais sem criar transações gerais de livro razão

1. Vá a **Gestão de projetos e contabilística** > **Periódico** > **Orçamentos** > **Transpor orçamentos**.
2. Na página **Processo de transposição do orçamento do projeto** no campo **Opções de final de ano**, selecione **Montantes orçamentais de projeto restantes transpostos**.
3. No grupo **Parâmetros**, no campo **Ano de orçamento do projeto**, selecione o ano fiscal para o qual pretende ver os restante montantes orçamentais.
4. No grupo **Copiar de/para**, forneça as seguintes informações:

   - No campo **Do modelo de previsão**, selecione o modelo de previsão do orçamento do projeto associado aos restantes montantes orçamentais que pretende transferir para os projetos. 
   - Selecione **Mostrar zero restantes** para incluir projetos que não tenham orçamento remanescente, mas que correspondam aos outros critérios que selecionou.
   - No grupo **Selecionar Orçamentos**, selecione **Obter todos os orçamentos** para carregar todos os orçamentos que correspondam aos critérios que selecionou. Para conceber uma consulta de base de dados que carregue um conjunto específico de orçamentos de projeto no painel, selecione **Obter orçamentos selecionados**.

5. Para cada projeto que pretende processar, selecione a opção no início da linha para o projeto. 
6. Selecione **Processar** para transferir os montantes orçamentais restantes para os projetos selecionados para o ano fiscal selecionado.

