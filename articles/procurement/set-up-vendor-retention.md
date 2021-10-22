---
title: Configurar a retenção de fornecedores
description: Este tópico explica como configurar a retenção de fornecedores.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9511da6212aafbf5b173efc6eb1ceaacbc8264a2
ms.sourcegitcommit: 098ea345ecfaf4445520094c32f5511b67e7953c
ms.translationtype: HT
ms.contentlocale: pt-PT
ms.lasthandoff: 10/02/2021
ms.locfileid: "7594618"
---
# <a name="set-up-vendor-retention"></a>Configurar a retenção de fornecedores

_**Aplica-se A:** Project Operations para cenários baseados em recursos/não armazenados_

Este tópico fornece informações sobre como configurar a retenção de fornecedores.

## <a name="set-up-a-vendor-retention-account-in-general-ledger"></a>Configurar uma conta de retenção de fornecedores no Razão geral

1. No Dynamics 365 Finance, aceda a **Razão geral** > **Configuração do registo** > **Contas para transações automáticas**.
2. Adicione uma nova linha.
3. No campo **Tipo registo**, selecione **Retenção de fornecedores**.
4. Selecione a conta principal para o registo da retenção de fornecedores.

## <a name="create-vendor-retention-terms"></a>Criar termos de retenção de fornecedores

Utilize a página **Termos de retenção de fornecedores** para configurar e manter os termos de retenção dos pagamentos dos fornecedores. Introduza a percentagem de retenção do pagamento do fornecedor e a percentagem de libertação dos montantes anteriormente retidos. Os valores são automaticamente retidos nas faturas do fornecedor até que o contrato atinja o estado de conclusão especificado. Após a configuração dos termos de retenção de um fornecedor, pode aplicá-los a qualquer projeto em que o fornecedor trabalhe.

1. No Finance, aceda a **Gestão e contabilidade de projetos** > **Configurar** > **Retenção** > **Termos de retenção de pagamentos do fornecedor**.
2. Selecione **Novo** para adicionar um novo termo de retenção do fornecedor. O valor no campo **ID da Regra** para o novo termo é introduzido automaticamente. 
3. No campo **Descrição**, introduza um nome descritivo para o novo termo.
4. No separador **Termos**, selecione **Adicionar linha** para introduzir um termo de retenção de fornecedores.
5. No campo **Percentagem de unidades entregues**, introduza uma percentagem de conclusão para a regra. Os montantes são retidos automaticamente nas faturas dos fornecedores até que a fase de conclusão do projeto seja igual à percentagem introduzida. Por exemplo, se introduzir 50,00, os valores são retidos até que o projeto esteja 50 por cento concluído.
6. No campo **Percentagem a reter**, introduza a percentagem de retenção do montante de uma fatura do fornecedor. Por exemplo, se introduzir 10,00 neste campo, 10 por cento do montante nas faturas do fornecedor é retido até que o projeto atinja a percentagem de conclusão selecionada no campo **Percentagem de unidades entregues**.
7. No campo **Percentagem a libertar**, introduza a percentagem de libertação de quaisquer montantes previamente retidos ao nível selecionado de conclusão do projeto.

> [!NOTE]
> Se tiver mais de um marco para diferentes níveis de conclusão do projeto, introduza uma linha de termo de retenção do fornecedor separada para cada regra de retenção. Cada linha pode especificar uma percentagem de retenção diferente e uma percentagem de libertação diferente para cada nível designado de conclusão do projeto.

## <a name="set-up-a-vendor-agreement-for-the-project"></a>Configurar um contrato de fornecedor para o projeto

Configure os termos de retenção de fornecedores aplicáveis ao projeto. Os termos de retenção do fornecedor também são apresentados em notas de encomenda que cria para o fornecedor.

1. Em Finance, aceda a **Gestão e contabilidade de projetos** > **Projetos** > **Todos os projetos**. 
2. Selecione um projeto e, no Painel de Ações, selecione **Grupo de projeto** > **Contratos de fornecedores**.
3. Na página **Contratos de fornecedores**, adicione uma nova linha.
4. No campo **Código da conta**, selecione uma das seguintes opções:
   - **Tabela**: Os termos de retenção do fornecedor aplicam-se a um único fornecedor.
   - **Grupo**: Os termos de retenção do fornecedor aplicam-se a todos os fornecedores de um grupo de fornecedores.
   - **Todos**: Os termos de retenção do fornecedor aplicam-se a todos os fornecedores.
5. No campo **Fornecedor/Grupo de fornecedores**, selecione o fornecedor ou o grupo de fornecedores ao qual se aplicam os termos de retenção de fornecedores. Se selecionou **Tudo** no passo anterior, este campo não está disponível.
6. No campo **Termos de retenção de fornecedores**, selecione o ID da regra dos termos de retenção aplicáveis a este fornecedor.

