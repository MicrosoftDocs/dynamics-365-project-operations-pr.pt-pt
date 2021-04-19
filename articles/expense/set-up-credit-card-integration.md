---
title: Configurar integração de cartão de crédito
description: Este tópico explica como trabalhar com transações de cartões de crédito relacionados com despesas.
author: suvaidya
manager: AnnBe
ms.date: 04/02/2021
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
ms.openlocfilehash: 72ff98f5985af4362cde3c9914e0d20247f1f09a
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866697"
---
# <a name="set-up-credit-card-integration"></a>Configurar integração de cartão de crédito

_**Aplica-se a:** Operações do projeto para cenários baseados em recursos/sem stock, implantação Lite - negócio para faturação pró-forma_

As transações de cartões de crédito relacionadas com despesas podem ser configuradas de modo a que sejam automaticamente importadas num horário recorrente. Em alternativa, as transações podem ser importadas manualmente conforme são necessárias. As transações de cartões de crédito são importadas através da entidade de dados de transações de Cartões de crédito.

## <a name="import-credit-card-transactions"></a>Importar transações de cartões de crédito

Para importar transações de cartões de crédito, siga estes passos:

1. Na página de **transações de cartões de crédito**, selecione **Importar transações**. Se estiver a abrir a gestão de dados pela primeira vez, o sistema deve atualizar a lista de entidades de dados antes de poder continuar.
2. No campo **Nome**, insira uma descrição única para o trabalho de importação.
3. No campo **formato de dados de origem**, selecione o formato do ficheiro que contém as transações de cartão de crédito a importar.
4. Selecione **Carregar** e, em seguida, encontre e selecione o ficheiro para importar.
5. Depois de o ficheiro ter sido carregado, validar o mapeamento do ficheiro de transações de cartões de crédito e as colunas da entidade de dados de transações de Cartões de crédito, selecionando a ligação **Ver mapa** no mosaico. Se houver erros de mapeamento, ou se tiver de alterar o mapeamento, faça as alterações de mapeamento a partir do separador de **Visualização de mapeamento** ou do separador **Detalhes do mapeamento**.
6. Para automatizar as transações de cartões de crédito, selecione **Criar tarefa de dados recorrente**. Em seguida, pode definir a periodicidade que define a frequência com que as transações com cartão de crédito devem ser importadas. Quando tiver terminado, selecione **OK**.
7. Para importar o ficheiro selecionado agora, selecione **Importar**.
8. Se ocorrerem erros durante a importação, pode ver o registo de execução ou os dados de teste para ver os erros que deve corrigir para ajudar a garantir uma importação bem sucedida.

> [!NOTE]
> Se precisar de importar mais de um formato de ficheiro, deve criar trabalhos de importação separados para cada tipo de formato.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Voltar a atribuir as transações de cartões de crédito para funcionários despedidos

Após terminar um registo de funcionário, a conta Active Directory Domain Services (AD DS) do funcionário é desativada. No entanto, pode haver transações ativas de cartões de crédito que ainda devem ser gastas e reembolsadas. Na página de **Transações de cartões de crédito**, pode reatribuir o empregado para qualquer transação de cartão de crédito onde o empregado associado tenha sido despedido.

Selecione uma ou mais transações de cartões de crédito e, em seguida, selecione **Reatribuir transações**. Em seguida, pode selecionar outro funcionário para atribuir as transações do cartão de crédito. Após a reatribuição das transações de cartões de crédito, podem ser selecionadas para um relatório de despesas e pagas através do processo habitual de reembolso do relatório de despesas.

## <a name="delete-credit-card-transactions"></a>Eliminar transações de cartões de crédito 

Por vezes, após a importação de transações com cartão de crédito, certas transações podem ter de ser eliminadas. Isto pode ser porque as transações são duplicadas ou porque os dados podem não ser precisos. Os administradores podem utilizar a função **Eliminar as transações de cartões de crédito** para selecionar e eliminar transações de cartões de crédito que estejam **não anexadas** a um relatório de despesas. 

1. Ir a **Tarefas periódicas** > **Eliminar transações de cartões de crédito**.
2. Selecione **Filtrar** e forneça informações para identificar os registos a incluir.
3. Selecione **Ok** para eliminar os registos. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
