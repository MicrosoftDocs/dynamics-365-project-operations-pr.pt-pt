---
title: Importar e manter transações de cartões de crédito
description: Este tópico explica como importar e manter as transações de cartões de crédito relacionados com despesas. Estas transações podem ser configuradas de modo a que sejam automaticamente importadas numa agenda recorrente, ou podem ser importadas manualmente conforme são necessárias.
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: df5c6bce8a534f4f8b1872e2bd5cc8a58ef11189
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271592"
---
# <a name="import-and-maintain-credit-card-transactions"></a>Importar e manter transações de cartões de crédito

As transações de cartões de crédito relacionadas com despesas podem ser configuradas de modo a que sejam automaticamente importadas num horário recorrente. Em alternativa, as transações podem ser importadas manualmente conforme são necessárias. As transações de cartões de crédito são importadas através da entidade de dados de transações de cartões de crédito.

Para obter mais informações sobre entidades de dados, consulte [Entidades de dados](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).

## <a name="import-credit-card-transactions"></a>Importar transações de cartões de crédito

1. Na página de **transações de cartões de crédito**, selecione **Importar transações**. Se estiver a abrir a gestão de dados pela primeira vez, o sistema deve atualizar a lista de entidades de dados antes de poder continuar.
2. No campo **Nome**, introduza uma descrição única da tarefa de importação.
3. No campo **formato de dados de origem**, selecione o formato do ficheiro que contém as transações de cartão de crédito a importar.
4. Selecione **Carregar** e, em seguida, encontre e selecione o ficheiro para importar.
5. Depois de o ficheiro ter sido carregado, validar o mapeamento do ficheiro de transações de cartões de crédito e as colunas da entidade de dados de transações de cartões de Crédito, selecionando a ligação **Ver mapa** no mosaico. Se houver erros de mapeamento, ou se tiver de alterar o mapeamento, faça as alterações de mapeamento a partir do separador de **Visualização de mapeamento** ou do separador **Detalhes do mapeamento**.
6. Para automatizar as transações de cartões de crédito, selecione **Criar tarefa de dados recorrente**. Em seguida, pode definir a periodicidade que define a frequência com que as transações com cartão de crédito devem ser importadas. Quando tiver terminado, selecione **OK**.
7. Para importar o ficheiro selecionado agora, selecione **Importar**.
8. Se ocorrerem erros durante a importação, pode ver o registo de execução ou os dados de teste para ver os erros que deve corrigir para ajudar a garantir uma importação bem sucedida.

> [!NOTE]
> Se tiver de importar mais do que um formato de ficheiro, deve criar tarefas de importação separadas para cada tipo de formato.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Voltar a atribuir as transações de cartões de crédito para funcionários despedidos

Após terminar um registo de funcionário, a conta Active Directory Domain Services (AD DS) do funcionário é desativada. No entanto, pode haver transações ativas de cartões de crédito que ainda devem ser gastas e reembolsadas. A partir da página de **transações de cartões de crédito**, pode reatribuir o funcionário a qualquer transação de cartão de crédito onde o funcionário associado tenha sido despedido.

Selecione uma ou mais transações de cartões de crédito e, em seguida, selecione **Reatribuir transações**. Em seguida, pode selecionar outro funcionário para atribuir as transações do cartão de crédito. Após a reatribuição das transações de cartões de crédito, podem ser selecionadas para um relatório de despesas e pagas através do processo habitual de reembolso do relatório de despesas.


[!INCLUDE[footer-include](../includes/footer-banner.md)]