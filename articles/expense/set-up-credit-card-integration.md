---
title: Configurar integração de cartão de crédito
description: Este tópico explica como importar e manter as transações de cartões de crédito relacionados com despesas.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: e0004f9096ea8a03745dbfce35fe0d32d3d707f6
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120872"
---
# <a name="set-up-credit-card-integration"></a>Configurar integração de cartão de crédito

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

As transações de cartões de crédito relacionadas com despesas podem ser configuradas de modo a que sejam automaticamente importadas num horário recorrente. Em alternativa, as transações podem ser importadas manualmente conforme são necessárias. As transações de cartões de crédito são importadas através da entidade de dados de transações de cartões de crédito.

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
