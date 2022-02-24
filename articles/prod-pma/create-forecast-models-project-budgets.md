---
title: Criar modelos de previsão para orçamentos de projetos
description: Este tópico descreve como criar um modelo de previsão para os restantes orçamentos.
author: Yowelle
manager: AnnBe
ms.date: 04/24/2020
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
ms.openlocfilehash: 5a3b9d3c154a85b50536a67ae0eb45d9b4f25f15
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271052"
---
# <a name="create-forecast-models-for-project-budgets"></a>Criar modelos de previsão para orçamentos de projetos 

[!include [banner](../includes/banner.md)]

Este tópico descreve como criar um modelo de previsão para os restantes orçamentos. Um projeto que está sujeito ao controlo orçamental utiliza dois tipos de orçamentos: originais e restantes. Quando criar um orçamento de projeto, deve especificar os modelos de previsão orçamental originais e restantes que foram criados na página de **Modelos de previsão**. Os orçamentos do projeto com base nos modelos especificados são criados quando submete o orçamento do projeto.

> [!NOTE]
> Um modelo de previsão que é usado para o controlo orçamental não pode ter um submodelo ou ser usado como um submodelo.

1. Selecione **Gestão de projetos e contabilística** > **Configurar** > **Previsões**  > **Modelos de previsão**.
2. Selecione **Novo** para criar um novo modelo de previsão e, em seguida, insira um número de ID do modelo e nome para o novo modelo. 
3. Defina a opção **Parado** como **Sim** para evitar alterações às linhas de previsão para o modelo de previsão. 
4. Se as linhas de previsão aos quais o modelo está associado gerarem previsões de fluxo de caixa no livro razão geral, defina **Incluir nas previsões de Fluxo de caixa** como **Sim**. 
5. Para utilizar a data do projeto como data da fatura, defina **Data da Fatura de Previsão** como **Sim**. 
6. No campo **Tipo de orçamento**, selecione um dos seguintes tipos de modelos:

   - **Orçamento original**: Utilize os montantes orçamentais originais que são submetidos quando o orçamento inicial é criado e aprovado.
   - **Orçamento restante**: Utilize os restantes montantes orçamentais durante a vida do projeto. Os saldos neste modelo de previsão são reduzidos por transações efetivas e aumentados ou diminuídos pelas revisões orçamentais.
   - **Transpor**: Utilize os montantes orçamentais transpostos para o projeto. A transposição é um processo opcional que pode ser executado para transferir os montantes orçamentais não utilizados de um ano fiscal para outro.

7. Defina as seguintes opções, conforme necessário:

   - Ative **Data da fatura de previsão** para utilizar a data do projeto como data da fatura.
   - Ative **Previsão com WIP** para prever com base no trabalho em curso (WIP) e, em seguida, selecione o tipo de WIP. 
   - Pode manter o **Tipo de orçamento** predefinido como **Nenhum** ou introduzir um novo tipo. O tipo de orçamento não pode ser alterado depois de mudar um registo.     
    > [!NOTE]
    > Se alterar o tipo de orçamento predefinido, todas as outras opções ficarão indisponíveis para atualização e não poderá reutilizar este modelo de previsão. 
   


 



[!INCLUDE[footer-include](../includes/footer-banner.md)]